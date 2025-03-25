# gitFlow-php-ManuelSanchez

Creación del repositorio y configuración inicial
Pasos realizados:
Se creó un repositorio en GitHub con el nombre gitflow-php-ManuelSanchez.

Se clonó el repositorio en el equipo local:


git clone https://github.com/ManuSchez/gitFlow-php-Manuel-Sanchez.git
Se inicializó Git Flow en el proyecto:
git flow init

Se creó la rama develop si no existía:
git checkout -b develop


2️Creación de un archivo PHP
Pasos realizados:
Se creó una nueva funcionalidad con Git Flow:

git flow feature start crear-mi-archivo
Se creó el archivo alumnos/ManuelSanchez.php con el siguiente contenido:


<?php
// Archivo: alumnos/ManuelSanchez.php
echo "Hola, soy Manuel Sanchez y estoy aprendiendo Git Flow!";
?>
Se confirmaron y subieron los cambios:


git add .
git commit -m "Creación del archivo PHP en alumnos/"
git flow feature finish crear-mi-archivo


Modificación de un archivo existente
Pasos realizados:
Se creó una nueva funcionalidad con Git Flow:

git flow feature start modificar-index
Se modificó el archivo index.php para incluir el archivo de Manuel Sanchez:

<?php
include "alumnos/ManuelSanchez.php";
?>
Se confirmaron y subieron los cambios:

git add .
git commit -m "Modificación de index.php para incluir el archivo PHP"
git flow feature finish modificar-index


Resolución de conflictos
Pasos realizados:
Se modificó index.php en la misma línea que otro compañero.

Se realizó un merge en develop:

git checkout develop
git merge feature/modificar-index
Se resolvió el conflicto manualmente en el editor y se confirmaron los cambios:

git add .
git commit -m "Resolución de conflicto en index.php"


Eliminación de un archivo
Pasos realizados:
Se creó una nueva funcionalidad con Git Flow:

git flow feature start borrar-mi-archivo
Se eliminó el archivo alumnos/ManuelSanchez.php:

rm alumnos/ManuelSanchez.php
Se confirmaron los cambios y se finalizó la funcionalidad:

git add .
git commit -m "Eliminación del archivo PHP de alumnos/"
git flow feature finish borrar-mi-archivo


Publicación de la versión final
Pasos realizados:
Se creó una nueva release con Git Flow:

git flow release start v1.0
Se finalizó la release y se fusionó con main y develop:

git flow release finish v1.0
Se subieron los cambios y el tag al repositorio remoto:

git push origin main
git push origin develop
git push origin v1.0
