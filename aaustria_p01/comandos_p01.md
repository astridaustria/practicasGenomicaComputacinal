# Comandos de la Práctica 01
## Austria López Astrid


# Parte I.

** Respuesta 1:**

#!/Users/uliaus
[echo] [] [$SHELL]

bash

**Respuesta 2:**

#!/Users/uliaus/GenomicaComputacional/aaustria_p01
[mkdir] [] [data fitered raw_data meta scripts figures archive ]

**Respuesta 3:**

#!/Users/uliaus/GenomicaComputacional/aaustria_p01
[mv] [] [filtered data]
[mv] [] [raw_data data]

**Respuesta 4**

El nombre y  el orden de los directorios es con la finalidad de mantener toda la información de nuestro proyecto bien  organizada para que posteriormente el acceso a esta sea más fácil. 
El subdirectorio data contiene los datos genéticos con las subdivisiones de raw_data y filtered para los datos crudos y modificados. El subdirectorio meta es donde se guardarán todos los metadatos y cualquier otro documento necesario para procesar los datos. Scripts es un subdirectorio para guardar todos los scripts necesarios para correr tu análisis y es obligatorio para tu proyecto. Figures es para poner el código utilizado en la elaboración de figuras  de alguna publicación. Finalmente archive es un directorio que no se sube al repositorio y se usa para poner scripts y resultados innecesarios pero que es preferible no borrarlos. 


# Parte II.
#!/Users/uliaus/GenomicaComputacional/aaustria_p01/scripts
[touch] [] [delay.sh]

#!/Users/uliaus
[wich] [] [bash]

**Respuesta 1:**

[chmod] [u+x] [delay.sh]

 **Respuesta 2:** 

[ls] [-l]
[bash] [] [delay.sh] 
[nano] [] [delay.sh]

**Respuesta 3:**

#!/Users/uliaus/GenomicaComputacional/aaustria_p01/scripts/delay.sh
[echo] “Después de la parte I. necesito un descanso de 30 segundos” &&
sleep 30 && [echo] “ya puedo continuar”
[bash] [] [delay.sh]

**Respuesta 4:**

#!/Users/uliaus/GenomicaComputacional/aaustria_p01/scripts/delay.sh
[echo] “Después de la parte I. necesito un descanso de 30 segundos” &&
sleep 300 && [echo] “ya puedo continuar”
[bash] [] [delay.sh] &
[kill] [-9] [PID]


#Parte III

**Respuesta 1:**

#!/Users/uliaus/GenomicaComputacional/aaustria_p01/meta

[touch] [] [SarsCov-2.txt  /Users/uliaus/GenomicaComputacional/aaustria_p01//meta]
[nano] [] [SarsCov-2.txt]
SARS-CoV-2 es un virus que causa enfermedades en el tracto respiratorio, gastrointestinal y el SNC. dentro de la familia de los coronavirus hay 4 géneros: alfa, beta
(SARS-CoV-2), gamma y delta. Es un virus RNA de cadena sencilla positiva y su está constituido por un ORF1 ab que codifica para proteínas no estructurales, proteínas S (con los
dominios S1 y S2, un tallo trimérico, región transmembranal y cola intracitoplasmática), proteínas M y proteínas N. Mediante el análisis filogenético se ha determinado que su
origen proviene de los murciélagos pero hubo un hospedero intermedio antes del humano. Y al final menciona dos vacunas; la vacuna Novavax, y la vacuna de la Universidad Laval
Quebec.

**Respuesta 2:**

#!/Users/uliaus/Downloads
[mv] [] [sequence.fasta sarscov2_genome.fasta]
[mv] [] [sequence.gff3 sarscov2_genome.gff3]
[mv] [] [sequence.fasta splike_c.faa]
[mv] [] [sequence (1).fasta splike_b.faa]
[mv] [] [sequence (2).fasta splike_a.faa]

#!/Users/uliaus/GenomicaComputacional/aaustria_p01/meta
[touch] [] [SarsCov-2_spike.txt]
Función de la SARS-CoV-2 spike ectodomain structure: Esta estructura está formada por proteínas las cuales median la entrada del Coronavirus en las células del huésped. Los coronavirus son virus de ARN de cadena sencilla positiva con su genoma dentro de una cápside helicoidal de proteína nucleocápside (N). Asociadas a esta envoltura también hay tres proteínas proteínas estructurales: las proteínas de membrana (M) y las proteínas de envoltura (E) son las involucradas en el ensamblaje del virus, mientras que las proteínas de espigas (S) son los mediadores de la entrada del virus a la célula. La manera en como esta estructura interviene con el ingreso a las células del hospedero es gracias al ectodominio de la espiga, esta consta de una subunidad de unión al receptor S1 y una subunidad de fusión de membrana S2. Durante la entrada del virus, S1 se une a un receptor en la superficie de la célula huésped para la unión viral, y S2 fusiona las membranas del huésped y viral, permitiendo que los genomas virales entren en las células huésped, la unión de estos dos es imprescindible para el ciclo de infección del virus.

#!/Users/uliaus/Downloads
[mv] sarscov2_genome.fasta sarscov2_genome.gff3 splike_c.faa splike_b.faa splike_a.faa SRR10971381_R1.fastq.gz SRR10971381_R2.fastq.gz sarscov2_assembly.fasta.gz [/Users/uliaus/GenomicaComputacional/aaustria_p01/data/raw_data]


#Parte IV

**Respuesta 1:**

#!/Users/uliaus/GenomicaComputacional/aaustria_p01/data/raw_data
[ln] [-s] [~/Users/uliaus/GenomicaComputacional/aaustria_p01/data/filtered *.faa]

**Respuesta 2:**

#!/Users/uliaus/GenomicaComputacional/aaustria_p01/data/filtered
[touch] [] [glycoproteins.faa]

**Respuesta 3:**

#!/Users/uliaus/GenomicaComputacional/aaustria_p01/data/raw_data

[head] [-3] [splike_c.faa splike_b.faa splike_a.faa >> /Users/uliaus/GenomicaComputacional/aaustria_p01/comandos_p01.md]

==> splike_a.faa <==
>pdb|7JJJ|A Chain A, Spike glycoprotein
MFVFLVLLPLVSSQCVNLTTRTQLPPAYTNSFTRGVYYPDKVFRSSVLHSTQDLFLPFFSNVTWFHAIHV
SGTNGTKRFDNPVLPFNDGVYFASTEKSNIIRGWIFGTTLDSKTQSLLIVNNATNVVIKVCEFQFCNDPF

=> splike_b.faa <==
>pdb|7JJJ|B Chain B, Spike glycoprotein
MFVFLVLLPLVSSQCVNLTTRTQLPPAYTNSFTRGVYYPDKVFRSSVLHSTQDLFLPFFSNVTWFHAIHV
SGTNGTKRFDNPVLPFNDGVYFASTEKSNIIRGWIFGTTLDSKTQSLLIVNNATNVVIKVCEFQFCNDPF

==> splike_c.faa <==
>pdb|7JJJ|C Chain C, Spike glycoprotein
MFVFLVLLPLVSSQCVNLTTRTQLPPAYTNSFTRGVYYPDKVFRSSVLHSTQDLFLPFFSNVTWFHAIHV
SGTNGTKRFDNPVLPFNDGVYFASTEKSNIIRGWIFGTTLDSKTQSLLIVNNATNVVIKVCEFQFCND

**Respuesta 4:**

#!/Users/uliaus/GenomicaComputacional/aaustria_p01/data/raw_data
[] [] [splike_a.faa splike_b.faa splike_c.faa > /Users/uliaus/GenomicaComputacional/aaustria_p01/data/filtered/glycoproteins.faa]

** Respuesta 5:**

#!/Users/uliaus/GenomicaComputacional/aaustria_p01/data/raw_data
[mv] [] [splike_*.faa >> /Users/uliaus/GenomicaComputacional/aaustria_p01/data/archive]
Las ligas simbólicas suaves se rompieron.

**Respuesta 6:**

#!/Users/uliaus/GenomicaComputacional/aaustria_p01/data/raw_data
[zless] [sarscov2_assembly.fasta.gz] | [head -3] [>> /Users/uliaus/GenomicaComputacional/aaustria_p01/comandos_p01.md]
[head] [-3] [sarscov2_genome.fasta >> /Users/uliaus/GenomicaComputacional/aaustria_p01/comandos_p01.md]

>NODE_1_length_264_cov_161.042781
CACAAATCTTAACACTCTTCCCTACACGACGCTCTTCCGATCTACGCCGGGCCATTCGTA
CGAACCGATACCTGTGGTAAAGGGTCCTACTGTATGGTGGTACACGAGTAGTAGCAAATG

>gi|1798174254|ref|NC_045512.2| Severe acute respiratory syndrome coronavirus 2 isolate Wuhan-Hu-1,
complete genome
ATTAAAGGTTTATACCTTCCCAGGTAACAAACCAACCAACTTTCGATCTCTTGTAGATCTGTTCTCTAAA
CGAACTTTAAAATCTGTGTGGCTGTCACTCGGCTGCATGCTTAGTGCACTCACGCAGTATAATTAATAAC

La diferencia entre el número de lecturas de los dos archivos se debe a que el archivo con extensión .gz es un archivo que está comprimido y por lo tanto permite reducir el espacio de almacenamiento siendo más factible tener un mayor número de secuencias. 

**Respuesta 7:**

#!/Users/uliaus/GenomicaComputacional/aaustria_p01/data/raw_data
[less] [] [sarscov2_genome.fasta] | [grep] [-c] [‘>’]
1
[zless] [] [sarscov2_assembly.fasta.gz] | [grep] [-c] [’>’]
35

**Respuesta 8:**

#!/Users/uliaus/GenomicaComputacional/aaustria_p01/data/raw_data
[zless] [] [SRR10971381_R2.fastq.gz] | [head] [-12] [>> /Users/uliaus/GenomicaComputacional/aaustria_p01/comandos_p01.md]

@SRR10971381.512_2
CGTGGAGTATGGCTACATACTACTTATTTGATGAGTCTGGTGAGTTTAAAGTGGCTTCACATATGTATTGTTCTTTCTACCCTCCAGATGAGGATGAAGAAGAAGGTGATTGTGAAGAAGAAGAGTTTGAGCCATCAACTCAATATGAGT
+
/FFFA/A/FFFF66FFFFFF/FF/FFFFFFFFFFFFF/AFFF6FFFA6FFFFF/FFFFFFFFFFFFFFFFFF/FF/FFFFFA/FFF/FFF/A/AFA/FFFFF/=F/F/F/AFAFF//A/AFF//FFAF/FFF=FFAFFFA/A/6=///==
@SRR10971381.556_2
TTTGTAAAAATAAAATAAAAAAAATAAAAATAATATATTAAAAAAAGATAAATAAAAAAATGAACAATTAATAAAAAAAAAAAAAAAAAAAAATTAAAAAAAAAAAAAAAAAAAATAAAAAAAAAAAAAAATAAAAAAAAAATTATAAAA
+
6AFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF/FFFAFFFFFF/FFA/FF=F//=FF/FFFFFFFFFFFFFA/FFFF/FF/FA//F/FFFFFFA/=FFFFF/FFFF/F=FFFAFF///FFFFA/FF/6//////=/
@SRR10971381.1428_2
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA
+
FFFFFFFFFFFFAFFFAFFFFFF6A//F//FFF

[zless] [] [SRR10971381_R2.fastq.gz] | [grep] [-c] [‘@‘]
130022

**Respuesta 9:**

Las secuencias del formato .fasta hacen referencia a nucleótidos mientras que el formato .faa hace referencia a los aminoácidos y el formato .fastqc hace referencia a ambas. 
La información de las líneas contenidas en el formato .fastqc corresponden a las secuencias de aminoácidos y nucleótidos así como codones que codifican para aminoácidos. 

**Respuesta 10:**

#!/Users/uliaus/GenomicaComputacional/aaustria_p01/data/raw_data
[less] [] [sarscov2_genome.gff3]
[less] [-S] [sarscov2_genome.gff3]
La diferencia entre la apertura del archivo mediante less y less -S es que en esta los datos se encuentran acomodados diferente puesto que con esa opción se ve la información de una sola línea sin saltos a otro renglón.

**Respuesta 11:**

#!/Users/uliaus/GenomicaComputacional/aaustria_p01/data/raw_data
[cut] [-f3] [sarscov2_genome.gff3] | [grep] [-c] [‘gene’] 
11
El campo tres corresponde a diferentes regiones dentro de una secuencia. La diferencia entre gen y CDS es que este último corresponde a una porción del gen. 

