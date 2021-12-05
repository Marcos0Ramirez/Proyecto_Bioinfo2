# Proyecto de Bioinformática, ensamble del SARS-CoV-2

Para empezar, vamos a descargar la secuenciacion del SARS-CoV-2, por lo que entramos a la base de datos de NCBI
en la base de datos de SRA con el ID de SRP251618 ![SRA-SRP251618](https://github.com/Marcos0Ramirez/Proyecto_Bioinfo2/blob/main/SRA.png)

Por tanto tomamos la muestra con el Accession: SRX10248073, y asi podemos ver las caracteristicas que tiene esta muestra, dejo la imagen ![SRX10248073](https://github.com/Marcos0Ramirez/Proyecto_Bioinfo2/blob/main/SRX10248073.png)

Podemos ver las siguientes caracteristicas, que la parte de ***show Abstract*** tiene una pequeña descripcion, la cual cito:  `Isolate raw read files from the Washington SARS-CoV-2 outbreak`, asi como en `Strategy` pues el proposito es secuenciar el RNA, supondre que es con el proposito de saber los patrones de expresion (no olvidar citar RNA-seq y Transcriptome de README.md) por esta razon es que el `fastq` solo tiene 930.3 mega bases. Por otra parte debemos de tener en cuenta que los reads son single, lo cual nos ayudara para pasos posteriores.

Ahora lo que haremos es obtener la 
