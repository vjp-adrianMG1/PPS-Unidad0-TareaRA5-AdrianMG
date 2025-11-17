# Creación del repositorio

## Objetivo
Documentar el proceso de creación del repositorio en GitHub y su configuración inicial con Git.

## Pasos realizados

### 1. Creación del repositorio en GitHub
- Accedí a [GitHub.com](https://github.com).
- Creé un nuevo repositorio con el nombre:  
  **PPS-Unidad0-Tarea-Adrián**
- Configuré la visibilidad (público/privado según lo indicado).
- Añadí al profesor como colaborador:  
  *Settings > Collaborators > Invite a collaborator* → usuario `PPSvjp`.

*(Captura a posteriori de pantalla del repositorio creado en GitHub*

---

### 2. Inicialización del repositorio local
En mi máquina, inicialicé el repositorio con los siguientes comandos:

```bash
git clone https://github.com/vjp-adrianMG1/PPS-Unidad0ActividadGit-AdrianMG.git #Repositorio DevSecOps, para copiar la estructura
git clone https://github.com/vjp-adrianMG1/PPS-Unidad0-TareaRA5-AdrianMG.git #Para pegar la estructura de DevSecOps en el nuevo repositorio
cp -r carpeta-del-repositorio-Devsecops/* carpeta-del-repositorio-TareaRA5
cp -r carpeta-del-repositorio-Devsecops/* carpeta-del-repositorio-TareaRA5 2>dev/null #Para copiar tambien archivos ocultos
#Luego de esto, subimos los cambios
git add .
git commit -m "Estructura de datos copiada"
git push
#Y listo, podríamos continuar con la prática
