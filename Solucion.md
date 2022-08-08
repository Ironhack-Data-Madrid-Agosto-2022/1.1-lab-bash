# Bash Lab

## Intro

Vamos a practicar con `bash`, un lenguaje de programación que se ejecuta en la línea de comandos!


## Entregable

Abre el  jupyter notebook en esta carpeta llamado solutions.ipynb y ve escribiendo en él los títulos de los ejercicios en una celda, y en otra el comando que has utilizado para solucionar los ejercicios. 

## Setup

1. Ubícate en la carpeta en la que ejecutando en el terminal. Al ejecutar `ls` 
```console
$ ls
```

2. Deberías ver: 
```console
README.md lorem solutions.ipynb
```
3. Intenta hacer todos los ejercicios sin cambiar de directorio. 

## Ejercicios

* Imprime en consola `Hello World`.

## echo "hello world"

* Crea un directorio nuevo llamado `new_dir`.

## mkdir newdir

* Elimina ese directorio.

## rm -r newdir

* Copia el archivo `sed.txt` dentro de la carpeta lorem a la carpeta lorem-copy. TIP: Puede ser necesario crear la carpeta lorem-copy primero. 

## mkdir loren-copy
## cd loren-copy
## touch sed.txt


* Copia los otros dos archivos de la carpeta lorem a la carpeta lorem-copy en una sola línea. 

## cp at.txt lorem.txt ../lorem-copy


* Muestra el contenido del archivo `sed.txt` dentro de la carpeta lorem. 

## cat sed.txt


* Muestra el contenido de los archivos `at.txt` y `lorem.txt` dentro de la carpeta lorem. 

## cat lorem.txt
## cat at.txt

* Visualiza las primeras 3 líneas del archivo `sed.txt` dentro de la carpeta lorem-copy 

## head -3 sed.txt

* Visualiza las ultimas 3 líneas del archivo `sed.txt` dentro de la carpeta lorem-copy 

## tail -3 sed.txt

* Añade `.` al final de archivo `sed.txt` dentro de la carpeta lorem-copy.

## nano +10,1 sed.txt


* Visualiza las últimas 3 líneas del archivo `sed.txt` dentro de la carpeta lorem-copy. Deberías ver ahora `Homo homini lupus.`. 

## tail -3 sed.txt

* Sustituye todas las apariciones de `et` por `ET` del archivo `at.txt` dentro de la carpeta lorem-copy. Deberás usar `sed`. 

## sed 's/et/ET/' at.txt


* Encuentra al usuario activo en el sistema.

## whoami


* Encuentra dónde estás en tu sistema de ficheros.

## pwd

* Lista los archivos que terminan por `.txt` en la carpeta lorem.

## ls ../ *txt


* Cuenta el número de líneas que tiene el archivo `sed.txt` dentro de la carpeta lorem. 

## wc -l sed.txt


* Cuenta el número de **archivos** que empiezan por `lorem` que están en este directorio y en directorios internos.

## find . -name \*lorem* -type f | wc -l


* Encuentra todas las apariciones de `et` en `at.txt` dentro de la carpeta lorem.

## grep "et" at.txt

* Cuenta el número de apariciones del string `et` en `at.txt` dentro de la carpeta lorem. 

## $ grep -R -c 'et' .
## ./at.txt:7
 ## ./lorem.txt:1
 ## ./sed.txt:3



*  Cuenta el número de apariciones del string `et` en todos los archivos del directorio lorem-copy. 

## grep -R -c 'et' ../lorem-copy

## Ficheros bash

Cualquier comando o comandos de bash se pueden almacenar en un fichero y ejecutar cuando queramos. 
Obviamente puedes utilizar tu editor preferido. Creamos el fichero: 
```
$ touch list_files.sh
```

E incluimos el contenido que queramos. En este caso listar ficheros:
```bash
#!/bin/bash
ls
```

Ejecutamos el script:
```
$ bash list_files.sh
```

Y veremos por consola el siguiente output. 
```console
README.md lorem solutions.ipynb
```
## hecho :)

## Bonus

* Almacena en una variable `name` tu nombre.

* Imprime esa variable.

## echo $name

* Crea un directorio nuevo que se llame como el contenido de la variable `name`.

## mkdir $name

* Elimina ese directorio. 

## mrdir $name

* Muestra los procesos de forma jerárquica que se están ejecutando en tu ordenador:
    1. Usando el comando top o htop

    ## While(1) {ps | sort -des cpu | select -f 15 | ft -a; sleep 1; cls}
    2. Usando el comando ps con argumentos

* Muestra información sobre tu procesador por pantalla

* Crea 3 alias y haz que estén disponibles cada vez que inicias sesión

## mkdir WindowsPowerShell
## new-item Microsoft.PowerShell_Profile.PS1
## Set-Alias n_i new-item
## Set-Alias g-v Get-Variable
## Set-Alias m_k mkdir

* Comprime las carpetas lorem y lorem-copy en un archivo llamado lorem-compressed.tar.gz

* Descomprime el archivo lorem-compressed.tar.gz en la carpeta lorem-uncompressed

* Crea un script bash para imprimir los numeros de 1 a 100.