# Expression Divergence of Chemosensory Genes between Drosophila sechellia and Its Sibling Species and Its Implications for Host Shift
### Members
* Christofer Julio, 111761502
* Zihao Chen, 112753141


### Demo 
All demo can be seen in our google colab file. you can access it through this link 

## Folder organization and its related information
idea by Noble WS (2009) [A Quick Guide to Organizing Computational Biology Projects.](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1000424) PLoS Comput Biol 5(7): e1000424.

### docs
* Link to our presentation: https://docs.google.com/presentation/d/1k-tbWFHo_nz2NUWr08uH6-WYRZBKNSSRH3a2a6hVqhg/edit?usp=sharing

* Any related document for the project?
  * There are currently no Other Related Documents

### data (do not upload fastq file)
#### Raw RNA Files:
* Source: https://www.ebi.ac.uk/ena/browser/home
* Format: Fastq
* Size: approx ~350 GB

#### Other Files:
* Source: https://ftp.flybase.org/genomes/
* Format: gtf,gff,Fasta
* Size: approx ~600 GB

### code
* Which packages do you use? 
  * matplotlib
  * seaborn
  * pandas
  * numpy
  * fastqc
  * trimmonmatic
  * HISAT2
  * featurecount
  * samtools

* Analysis steps
  * FASTQC: raw data fastq is first inspected using fastqc
  * Trimmonmatic: poor quality data is trimmed using trimmonmatic (setting: slider=5:20 and minilen=60)
  * HISAT2: an index for each specie is built using HISAT2 build
  * HISAT2: index is combined with good fastq raw data to create alignment via HISAT2 align
  * samstool: alignment duplicates are removed using samstool
  * featurecount: alignment is then used to build raw counts via featurecount
  * numpy&pandas: raw count and OGS gene list is then proccessed as a dataframe to generate FPKM and DEG using various function in numpy & pandas
  *  matplotlib: FPKM and DEG files will then be used to generate graphs and plots using matplotlib

### results
* Which part of the paper do you reproduce?
  * Gene FPKM table
  * Gene Heatmaps
* Any improvement or change in your package?
  * We have to use brand new tools in every way because old tools are often outdated and no longer work in the current version of python 3

## References
* Packages you use
  * matplotlib
  * seaborn
  * pandas
  * numpy
  * fastqc
  * trimmonmatic
  * HISAT2
  * featurecount
  * samtools

* Related publications
  * Shiao, Meng-Shin & Chang, Jia-Ming & Fan, Wen-Lang & Lu, Mei-Yeh & Notredame, Cedric & Fang, Shu & Kondo, Rumi & Li, Wen-Hsiung. (2015). Expression Divergence of Chemosensory Genes between Drosophila sechellia and Its Sibling Species and Its Implications for Host Shift. Genome Biology and Evolution. 7. 2843-2858. 10.1093/gbe/evv183. 
