# Proyecto de Bioinformática, ensamble del SARS-CoV-2

***Debemos de saber que uso una Raspberry pi 4 con servidor de Ubuntu, pero al final se uso una computadora rempta, esto por complicaciones técnicas***

Para empezar, vamos a descargar la secuenciacion del SARS-CoV-2, por lo que entramos a la base de datos de ***NCBI***
en la base de datos de `SRA` con el `ID` de `SRP251618` ![SRA-SRP251618](https://github.com/Marcos0Ramirez/Proyecto_Bioinfo2/blob/main/SRA.png)

Por tanto tomamos la muestra con el Accession: `SRX10248073`, y asi podemos ver las caracteristicas que tiene esta muestra, dejo la imagen ![SRX10248073](https://github.com/Marcos0Ramirez/Proyecto_Bioinfo2/blob/main/SRX10248073.png)

Podemos ver las siguientes caracteristicas, que la parte de ***show Abstract*** tiene una pequeña descripcion, la cual cito:  `Isolate raw read files from the Washington SARS-CoV-2 outbreak`, asi como en `Strategy` pues el proposito es secuenciar el RNA, supondre que es con el proposito de saber los patrones de expresion (no olvidar citar RNA-seq y Transcriptome de README.md) por esta razon es que el `fastq` solo tiene `930.3 megabases`. Por otra parte debemos de tener en cuenta que los reads son single, lo cual nos ayudara para pasos posteriores.

Ya que dentro de la computadora que opero, no pude descargar por mi cuenta el `SRA` que escogi, trabaje mediante una ***computadora*** remota, aplicando los siguientes comandos:

`fastq-dump SRR13867562`

para descargarla (recordemos que es el comando para un SRA con reads single).
Resultando en

```
$ fastq-dump SRR13867562
Read 5054244 spots for SRR13867562
Written 5054244 spots for SRR13867562

$ ls -lh
total 2.2G
-rw-rw-r-- 1 mramirez mramirez 2.2G Dec  5 01:32 SRR13867562.fastq
drwxrwxr-x 3 mramirez mramirez   28 Dec  5 01:23 ncbi
```
</br>
Para hacer el analisis de control de calidad, tomamos el archivo `SRR13867562.fastq` y corrimos el siguiente comando

`fastqc SRR13867562.fastq`

Y saldra los dos archivos nuevos `SRR13867562_fastqc.html` y `SRR13867562_fastqc.zip`
```
$ fastqc SRR13867562.fastq
perl: warning: Setting locale failed.
perl: warning: Please check that your locale settings:
        LANGUAGE = (unset),
        LC_ALL = (unset),
        LANG = "C.UTF-8"
    are supported and installed on your system.
perl: warning: Falling back to the standard locale ("C").
Started analysis of SRR13867562.fastq
Approx 5% complete for SRR13867562.fastq
Approx 10% complete for SRR13867562.fastq
Approx 15% complete for SRR13867562.fastq
Approx 20% complete for SRR13867562.fastq
Approx 25% complete for SRR13867562.fastq
Approx 30% complete for SRR13867562.fastq
Approx 35% complete for SRR13867562.fastq
Approx 40% complete for SRR13867562.fastq
Approx 45% complete for SRR13867562.fastq
Approx 50% complete for SRR13867562.fastq
Approx 55% complete for SRR13867562.fastq
Approx 60% complete for SRR13867562.fastq
Approx 65% complete for SRR13867562.fastq
Approx 70% complete for SRR13867562.fastq
Approx 75% complete for SRR13867562.fastq
Approx 80% complete for SRR13867562.fastq
Approx 85% complete for SRR13867562.fastq
Approx 90% complete for SRR13867562.fastq
Approx 95% complete for SRR13867562.fastq
Analysis complete for SRR13867562.fastq

$ ls
SRR13867562.fastq  SRR13867562_fastqc.html  SRR13867562_fastqc.zip  ncbi
```
Por tanto abres `SRR13867562_fastqc.html` para realizar el analisis. Entonces...


