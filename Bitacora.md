# Proyecto de Bioinformática, ensamble del SARS-CoV-2

***Debemos de saber que uso una Raspberry pi 4 con  servidor de Ubuntu***

Para empezar, vamos a descargar la secuenciacion del SARS-CoV-2, por lo que entramos a la base de datos de NCBI
en la base de datos de SRA con el ID de SRP251618 ![SRA-SRP251618](https://github.com/Marcos0Ramirez/Proyecto_Bioinfo2/blob/main/SRA.png)

Por tanto tomamos la muestra con el Accession: SRX10248073, y asi podemos ver las caracteristicas que tiene esta muestra, dejo la imagen ![SRX10248073](https://github.com/Marcos0Ramirez/Proyecto_Bioinfo2/blob/main/SRX10248073.png)

Podemos ver las siguientes caracteristicas, que la parte de ***show Abstract*** tiene una pequeña descripcion, la cual cito:  `Isolate raw read files from the Washington SARS-CoV-2 outbreak`, asi como en `Strategy` pues el proposito es secuenciar el RNA, supondre que es con el proposito de saber los patrones de expresion (no olvidar citar RNA-seq y Transcriptome de README.md) por esta razon es que el `fastq` solo tiene 930.3 mega bases. Por otra parte debemos de tener en cuenta que los reads son single, lo cual nos ayudara para pasos posteriores.

Ya que dentro de la computadora que opero, no pude descargar por mi cuenta el SRA que escogi 












you can use "file <your executable file>" to determine what kind of file you're running ..
Ahora lo que haremos es obtener el archivo fastq. Entonces con la parte superior derecha de la pagina y presionar lo que esta en verde ![SRX10248073_Pasosub2](https://github.com/Marcos0Ramirez/Proyecto_Bioinfo2/blob/main/SRX10248073_2.png)

y configurar tal y como esta en la siguiente imagen ![SRX10248073_Pasosub2](Poner la correcta) (donde se presiona en `File`, se selecciona `Runinfo` y descargar o poner en `Create File`.

Ya con el archivo descargado lo abrimos con la terminal linux, para ello vas a la parte donde se descargan tus archivos por default y lo abres, ahora lo que haces es copiar el siguiente link pintado en color "" ![SRA](Poner la correcta)
