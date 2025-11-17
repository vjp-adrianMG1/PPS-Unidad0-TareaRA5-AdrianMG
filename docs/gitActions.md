# Workflows y GitHub Actions

## Objetivo
Automatizar la creación de la documentación con MkDocs mediante un workflow en GitHub Actions.  
Este workflow se encarga de instalar dependencias, generar la documentación y dejarla lista para ser publicada en GitHub Pages.

---

## Creación del workflow

1. Se creó el archivo en la ruta:.github/workflows/CreacionDocumentacion.yml


2. Contenido inicial del workflow:

```yaml
name: CreacionDocumentacion

on:
push:
 branches: [ "main" ]

jobs:
build:
 runs-on: ubuntu-latest

 steps:
   - name: Checkout del repositorio
     uses: actions/checkout@v3

   - name: Configurar Python
     uses: actions/setup-python@v4
     with:
       python-version: '3.x'

   - name: Instalar dependencias
     run: pip install -r requirements.txt

   - name: Generar documentación con MkDocs
     run: mkdocs build

