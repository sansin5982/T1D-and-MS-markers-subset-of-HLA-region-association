---
title: "T1D_MS"
author: "Sandeep Singh"
date: "14/01/2021"
output: 
   html_document:
    keep_md: true
always_allow_html: true
---






* raw_data.txt file was generated from previous researches on Type-1-diabetes and multiple sclerosis.  
* This file contains only 119 SNPs as common markers for T1D and MS. 

## File preparation

Table: Table representing SNPs associated with T1D and MS.

|SNP       |
|:---------|
|rs1632953 |
|rs1059174 |
|rs1736921 |
|rs1736916 |
|rs1736913 |

* A total of 119 SNPs.
* This file was used to create ANNOVAR formatted file.

### File preparation by ANNOVAR
* Command used in ANNOVAR: 

convert2annovar.pl -format rsid T1D.txt -dbsnpfile humandb/hg19_snp138.txt > T1D_MS_formatted

* 119 SNPs records input; 110 SNPs records as output, 9 SNPs missing


Table: SNPs run in ANNOVAR.

|V1   |    V2    |    V3    | V4| V5|V6        |
|:----|:--------:|:--------:|--:|--:|:---------|
|chr6 | 29692305 | 29692305 |  A|  G|rs1632953 |
|chr6 | 29694427 | 29694427 |  C|  T|rs1059174 |
|chr6 | 29696209 | 29696209 |  G|  A|rs1736921 |
|chr6 | 29704083 | 29704083 |  C|  T|rs1736916 |
|chr6 | 29704400 | 29704400 |  T|  C|rs1736913 |

* Identify 9 missing SNPs


```
## NULL
```

* missing SNP IDs were renamed from PUBMED

      rs6931717 > rs3095345
      
      rs7452756 > rs4516988
      
      rs12199773 > rs3130952
      
      rs6937967 >  rs3130534
      
      rs12178292 > rs2844558
      
      rs10456058 >  rs2734573
      
      rs7382662 >  rs3129305
      
      rs10807118 >  rs3130578
      
      rs10947377 > rs3130179
      
* Created a new file T1D_2.txt after chainging SNP ids
* Rerun in ANNOVAR and obtained results for all 119 SNPs 


Table: SNP added with 9 missing data.

|V1   |    V2    |    V3    | V4| V5|V6        |
|:----|:--------:|:--------:|--:|--:|:---------|
|chr6 | 29692305 | 29692305 |  A|  G|rs1632953 |
|chr6 | 29694427 | 29694427 |  C|  T|rs1059174 |
|chr6 | 29696209 | 29696209 |  G|  A|rs1736921 |
|chr6 | 29704083 | 29704083 |  C|  T|rs1736916 |
|chr6 | 29704400 | 29704400 |  T|  C|rs1736913 |

# ANNOVAR ANALYSIS

## Gene based annotation

### Known Gene (UCSC)

Table: Table representing SNPs information from known gene.

|Genomic region |   Gene    | Chromosome |     BP_1|     BP_2|A1 | A2 |    SNP    |
|:--------------|:---------:|:----------:|--------:|--------:|:--|:--:|:---------:|
|intronic       |   HLA-F   |    chr6    | 29692305| 29692305|A  | G  | rs1632953 |
|ncRNA_exonic   | HLA-F-AS1 |    chr6    | 29694427| 29694427|C  | T  | rs1059174 |
|ncRNA_exonic   | HLA-F-AS1 |    chr6    | 29696209| 29696209|G  | A  | rs1736921 |
|ncRNA_exonic   | HLA-F-AS1 |    chr6    | 29704083| 29704083|C  | T  | rs1736916 |
|ncRNA_exonic   | HLA-F-AS1 |    chr6    | 29704400| 29704400|T  | C  | rs1736913 |

### Ensembel Gene

Table: Table representing SNPs information from Ensemble gene.

|Genomic region |      Gene       | Chromosome |     BP_1|     BP_2|A1 | A2 |    SNP    |
|:--------------|:---------------:|:----------:|--------:|--------:|:--|:--:|:---------:|
|intronic       | ENSG00000204642 |    chr6    | 29692305| 29692305|A  | G  | rs1632953 |
|ncRNA_exonic   | ENSG00000214922 |    chr6    | 29694427| 29694427|C  | T  | rs1059174 |
|ncRNA_exonic   | ENSG00000214922 |    chr6    | 29696209| 29696209|G  | A  | rs1736921 |
|ncRNA_exonic   | ENSG00000214922 |    chr6    | 29704083| 29704083|C  | T  | rs1736916 |
|ncRNA_exonic   | ENSG00000214922 |    chr6    | 29704400| 29704400|T  | C  | rs1736913 |

### Ref Gene (NCBI)

Table: Table representing SNPs information from Reference gene.

|Genomic region |   Gene    | Chromosome |     BP_1|     BP_2|A1 | A2 |    SNP    |
|:--------------|:---------:|:----------:|--------:|--------:|:--|:--:|:---------:|
|intronic       |   HLA-F   |    chr6    | 29692305| 29692305|A  | G  | rs1632953 |
|ncRNA_exonic   | HLA-F-AS1 |    chr6    | 29694427| 29694427|C  | T  | rs1059174 |
|ncRNA_exonic   | HLA-F-AS1 |    chr6    | 29696209| 29696209|G  | A  | rs1736921 |
|ncRNA_intronic | HLA-F-AS1 |    chr6    | 29704083| 29704083|C  | T  | rs1736916 |
|ncRNA_intronic | HLA-F-AS1 |    chr6    | 29704400| 29704400|T  | C  | rs1736913 |

## Region based annotation

### Conserved genomic elements annotation

Table: Conserved Genomic Score from NCBI database.

|Con_Sequence_score |    SNP     |
|:------------------|:----------:|
|Score=737          | rs1059174  |
|Score=284          | rs3130558  |
|Score=798          | rs6906846  |
|Score=369          | rs7382297  |
|Score=511          | rs2736172  |
|Score=304          | rs2076530  |
|Score=340          | rs9268831  |
|Score=361          | rs17840186 |

* In evolutionary biology, conserved sequences are identical or similar sequences in nucleic acids (DNA and RNA) or proteins across species (orthologous sequences), or within a genome (paralogous sequences), or between donor and receptor taxa (xenologous sequences). Conservation indicates that a sequence has been maintained by natural selection.


# RegulomeDB results





Table: RegulomeDB score.

|Chr  |    SNP    | RDB_score |
|:----|:---------:|:---------:|
|chr6 | rs2517646 |    1b     |
|chr6 | rs1632953 |    1f     |
|chr6 | rs1059174 |    1f     |
|chr6 | rs1736921 |    1f     |
|chr6 | rs1736916 |    1f     |


```
## 
## 1b 1d 1f 2b  5  6  7 
##  3  2 62  1  2 45  1
```

Figure Bar chart representing RegulomeDB score
<div class="figure" style="text-align: center">
<img src="T1D_MS_files/figure-html/unnamed-chunk-14-1.png" alt="Figure 1: Bar chart representing RegulomeDB score"  />
<p class="caption">Figure 1: Bar chart representing RegulomeDB score</p>
</div>

