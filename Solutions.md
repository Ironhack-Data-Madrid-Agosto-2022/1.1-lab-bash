Intro
Vamos a practicar con bash, un lenguaje de programación que se ejecuta en la línea de comandos!

Entregable
Abre el jupyter notebook en esta carpeta llamado solutions.ipynb y ve escribiendo en él los títulos de los ejercicios en una celda, y en otra el comando que has utilizado para solucionar los ejercicios.

Setup
Ubícate en la carpeta en la que ejecutando en el terminal. Al ejecutar ls
$ ls
Deberías ver:
README.md lorem solutions.ipynb
Intenta hacer todos los ejercicios sin cambiar de directorio.

Ejercicios
Imprime en consola Hello World.
% echo 'Hello Word'

Crea un directorio nuevo llamado new_dir.
 % mkdir new_dir
 
Elimina ese directorio.
% rm -rf new_dir

Copia el archivo sed.txt dentro de la carpeta lorem a la carpeta lorem-copy. TIP: Puede ser necesario crear la carpeta lorem-copy primero.
% mkdir lorem-copy
% cd 1.1-lab-bash
% cd lorem
% ls
% cp lorem/sed.txt lorem-copy/


Copia los otros dos archivos de la carpeta lorem a la carpeta lorem-copy en una sola línea.
% cp lorem/* lorem-copy/

Muestra el contenido del archivo sed.txt dentro de la carpeta lorem.

% cat sed.txt

Muestra el contenido de los archivos at.txt y lorem.txt dentro de la carpeta lorem.

% cat * lorem/

Visualiza las primeras 3 líneas del archivo sed.txt dentro de la carpeta lorem-copy
% cd ..
% ls
% cd lorem - copy
% ls
% head -n3 sed.txt


Visualiza las ultimas 3 líneas del archivo sed.txt dentro de la carpeta lorem-copy

 % tail -n3 sed.txt

Añade Homo homini lupus. al final de archivo sed.txt dentro de la carpeta lorem-copy.

% echo 'Homo homini lupus' >> sed.txt

Visualiza las últimas 3 líneas del archivo sed.txt dentro de la carpeta lorem-copy. Deberías ver ahora Homo homini lupus..

% cat sed.txt

Sustituye todas las apariciones de et por ET del archivo at.txt dentro de la carpeta lorem-copy. Deberás usar sed.
% sed 's/et/ET/g' at.txt

Encuentra al usuario activo en el sistema.
 % users

Encuentra dónde estás en tu sistema de ficheros.
% pwd


Lista los archivos que terminan por .txt en la carpeta lorem.

% ls *.txt

Cuenta el número de líneas que tiene el archivo sed.txt dentro de la carpeta lorem.

% wc sed.txt


Cuenta el número de archivos que empiezan por lorem que están en este directorio y en directorios internos.

% find . -name 'lorem*' | wc -l


Encuentra todas las apariciones de et en at.txt dentro de la carpeta lorem.
% grep -o -i -w "et" at.txt 


Cuenta el número de apariciones del string et en at.txt dentro de la carpeta lorem.

% grep -o -i " et " lorem | wc -l

Cuenta el número de apariciones del string et en todos los archivos del directorio lorem-copy.

% cd ..
% grep -o -i -w -r "et" lorem-copy | wc -l

Ficheros bash
Cualquier comando o comandos de bash se pueden almacenar en un fichero y ejecutar cuando queramos. Obviamente puedes utilizar tu editor preferido. Creamos el fichero:

$ touch list_files.sh
E incluimos el contenido que queramos. En este caso listar ficheros:

#!/bin/bash
ls
Ejecutamos el script:
touch
% nano list_files.sh
% bash list_files.sh

$ bash list_files.sh
Y veremos por consola el siguiente output.

README.md lorem solutions.ipynb


Bonus
Almacena en una variable name tu nombre.
name=lucia

Imprime esa variable.
$name

Crea un directorio nuevo que se llame como el contenido de la variable name.
mkdir lucia

Elimina ese directorio.
rmdir lucia

Muestra los procesos de forma jerárquica que se están ejecutando en tu ordenador:

Usando el comando top o htop
 % top 
 
Usando el comando ps con argumentos 
% ps -e
Muestra información sobre tu procesador por pantalla


Crea 3 alias y haz que estén disponibles cada vez que inicias sesión

alias atras="cd .."
alias c="clear"
alias escritorio="desktop"

Comprime las carpetas lorem y lorem-copy en un archivo llamado lorem-compressed.tar.gz

% zip -r lorem-compressed.tar.gz lorem/ lorem-copy/

Descomprime el archivo lorem-compressed.tar.gz en la carpeta lorem-uncompressed
% unzip -d lorem-compressed.tar.gz lorem/ lorem-copy/

Crea un script bash para imprimir los numeros de 1 a 100.

for i in {1..100}; do echo $i; done


```python

```
