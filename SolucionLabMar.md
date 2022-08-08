```python
#Imprime en consola Hello World.
echo Hello world

#Crea un directorio nuevo llamado new_dir.
mkdir new_dir

#Elimina ese directorio.
rmdir new_dir

#Copia el archivo sed.txt dentro de la carpeta lorem a la carpeta lorem-copy. TIP: Puede ser necesario crear la carpeta lorem-copy primero.
cd 1.1-lab-bash-Mar
mkdir lorem-copy
cp sed.txt /Users/mar/1.1-lab-bash-Mar/lorem-copy

#Copia los otros dos archivos de la carpeta lorem a la carpeta lorem-copy en una sola línea.
cp * /Users/mar/1.1-lab-bash-Mar/lorem-copy

#Muestra el contenido del archivo sed.txt dentro de la carpeta lorem.
cd lorem
cat sed.txt

#Muestra el contenido de los archivos at.txt y lorem.txt dentro de la carpeta lorem.
cat sed.txt

#Visualiza las primeras 3 líneas del archivo sed.txt dentro de la carpeta lorem-copy
head -n3 sed.txt

#Visualiza las ultimas 3 líneas del archivo sed.txt dentro de la carpeta lorem-copy
tail -n3 sed.txt

#Añade Homo homini lupus. al final de archivo sed.txt dentro de la carpeta lorem-copy.
>>sed.txt echo homini lupus

#Visualiza las últimas 3 líneas del archivo sed.txt dentro de la carpeta lorem-copy. Deberías ver ahora Homo homini lupus..
head -n3 sed.txt

#Sustituye todas las apariciones de et por ET del archivo at.txt dentro de la carpeta lorem-copy. Deberás usar sed.
sed 's/et/ET/g' at.txt

#Encuentra al usuario activo en el sistema.
whoami

#Encuentra dónde estás en tu sistema de ficheros.
pwd

#Lista los archivos que terminan por .txt en la carpeta lorem.
ls *.txt

#Cuenta el número de líneas que tiene el archivo sed.txt dentro de la carpeta lorem.
wc -l sed.txt

#Cuenta el número de archivos que empiezan por lorem que están en este directorio y en directorios internos.
find /Users/mar/1.1-lab-bash-Mar -name lorem* | wc -l

#Encuentra todas las apariciones de et en at.txt dentro de la carpeta lorem.
grep et at.txt

#Cuenta el número de apariciones del string et en at.txt dentro de la carpeta lorem.
grep -c et at.txt

#Cuenta el número de apariciones del string et en todos los archivos del directorio lorem-copy.
grep -rc et lorem-copy



#BONUS

#Almacena en una variable name tu nombre.
name=Mar

#Imprime esa variable.
echo $name

#Crea un directorio nuevo que se llame como el contenido de la variable name.
mkdir mar

#Elimina ese directorio.
rmdir mar

#Muestra los procesos de forma jerárquica que se están ejecutando en tu ordenador:
#Usando el comando top o htop

#Usando el comando ps con argumentos 
ps f
#Muestra información sobre tu procesador por pantalla

lscpu
#Crea 3 alias y haz que estén disponibles cada vez que inicias sesión
alias user= "Users/mar"
holita="echo Holita Mar" 
alias quetal="echo Pues aquí viviendo"

#Comprime las carpetas lorem y lorem-copy en un archivo llamado lorem-compressed.tar.gz
tar -czvf lorem.tar.gz /Users/mar/1.1-lab-bash-Mar/lorem |tar -czvf lorem-copy.tar.gz /Users/mar/1.1-lab-bash-Mar/lorem-copy   
mv lorem.tar.gz lorem-copy.tar.gz /Users/mar/1.1-lab-bash-Mar/lorem-compressed.tar.gz


#Descomprime el archivo lorem-compressed.tar.gz en la carpeta lorem-uncompressed
tar -xzvf lorem.tar.gz
tar -xzvf lorem-copy.tar.gz

#Crea un script bash para imprimir los numeros de 1 a 100.
i=1
while [ $i -le 100 ]
do
    echo $i
    i=$(($i+1))
done

```


      Input In [1]
        Imprime en consola Hello World.
                ^
    SyntaxError: invalid syntax




```python

```


```python

```
