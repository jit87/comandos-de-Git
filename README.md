//COMANDOS BÁSICOS:

Añadir fichero en Git local: git add .
Guardar/Confirmar archivo en repositorio local Git: git commit -m "Frase de confirmacion archivo"
Identificar quien somos: 
	 git config --global user.email "your@email.com"
	 git config --global user.name "Your Name"
Comprobar que se ha guardado en repositorio local: git commit -m "Frase de confirmacion archivo"
Subir al repositorio remoto de GitHub: git push
Ver el estado de Git: git status

Fusionar historiales de cambios del repositorio remoto y el local: git pull --allow-unrelated-histories URL main

Crear una nueva rama llamada 'main' y cambiar a ella el proyecto: git checkout -b main

Verificar el repositorio remoto: git remote -v

Eliminar rama : git branch -d branch-namegit 

Recuperar archivos el eliminados: 
git log (para identificar el id del commit donde se borraron) también git log --oneline
git checkout id_del_commit .(recuperación)


Regresar a la versión indicada de commit (elimina las revisiones posteriores a ese hash):
git reset --hard <hash_del_commit>  

Regresar a la versión del commit indicando posición del mismo (este ejemplo elimina los 3 últimos):
git reset --hard HEAD~3

Eliminar fichero del repositorio:
git rm --cached nombre_fichero   (después hacer commit del cambio)

Dejar de subir archivo (cuando nos hemos confundido en .gitignore)
git rm --cached ruta_archivo

Reescribir el repositorio remoto con el local (se borra el remoto y se sube lo que haya en el local):
git push --force origin main

Buscar la ubicación exacta de archivo:
find . -name "nombre_archivo"




SUBIR A GIT REMOTO EL PROYECTO LOCAL
git init
git add .
git commit -m "first commit"
git remote add origin https://github.com/NOMBRE_USUARIO/NOMBRE_PROYECTO.git                 
git push -u origin main


O BIEN...
git push --set-upstream origin main  



MENSAJE DE COMMIT EN LA TERMINAL BASH

To write a commit message and get out of VI, follow these steps:

press i (i for insert)
write your merge message
press esc (escape)
write :wq (write & quit)
then press enter



CLONAR REPOSITORIO

Clonar el repositorio:
git clone https://github.com/usuario/nombre-repositorio.git

Cambiar al directorio del repositorio clonado:
cd nombre-repositorio

Verificar el estado del repositorio:
git status
