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

```
##   Genomic region      Gene Chromosome     BP_1     BP_2 A1 A2       SNP
## 1       intronic     HLA-F       chr6 29692305 29692305  A  G rs1632953
## 2   ncRNA_exonic HLA-F-AS1       chr6 29694427 29694427  C  T rs1059174
## 3   ncRNA_exonic HLA-F-AS1       chr6 29696209 29696209  G  A rs1736921
## 4   ncRNA_exonic HLA-F-AS1       chr6 29704083 29704083  C  T rs1736916
## 5   ncRNA_exonic HLA-F-AS1       chr6 29704400 29704400  T  C rs1736913
## 6 ncRNA_intronic HLA-F-AS1       chr6 29708222 29708222  T  C rs1610603
```

### Ensembel Gene

```
##   Genomic region            Gene Chromosome     BP_1     BP_2 A1 A2       SNP
## 1       intronic ENSG00000204642       chr6 29692305 29692305  A  G rs1632953
## 2   ncRNA_exonic ENSG00000214922       chr6 29694427 29694427  C  T rs1059174
## 3   ncRNA_exonic ENSG00000214922       chr6 29696209 29696209  G  A rs1736921
## 4   ncRNA_exonic ENSG00000214922       chr6 29704083 29704083  C  T rs1736916
## 5   ncRNA_exonic ENSG00000214922       chr6 29704400 29704400  T  C rs1736913
## 6 ncRNA_intronic ENSG00000214922       chr6 29708222 29708222  T  C rs1610603
```

### Ref Gene (NCBI)

```
##   Genomic_region      Gene Chromosome     BP_1     BP_2 A1 A2       SNP
## 1       intronic     HLA-F       chr6 29692305 29692305  A  G rs1632953
## 2   ncRNA_exonic HLA-F-AS1       chr6 29694427 29694427  C  T rs1059174
## 3   ncRNA_exonic HLA-F-AS1       chr6 29696209 29696209  G  A rs1736921
## 4 ncRNA_intronic HLA-F-AS1       chr6 29704083 29704083  C  T rs1736916
## 5 ncRNA_intronic HLA-F-AS1       chr6 29704400 29704400  T  C rs1736913
## 6 ncRNA_intronic HLA-F-AS1       chr6 29708222 29708222  T  C rs1610603
```


* We will use known gene as reference to create table
<!--html_preserve--><div id="htmlwidget-ee5546a7b55b4cb20d28" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-ee5546a7b55b4cb20d28">{"x":{"visdat":{"1300343220a8":["function () ","plotlyVisDat"],"13007c7a30c2":["function () ","data"],"13007e736047":["function () ","data"],"13001d802beb":["function () ","data"]},"cur_data":"13001d802beb","attrs":{"13007c7a30c2":{"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"values":{},"labels":{},"type":"pie","textinfo":"label+percent","name":"UCSC","domain":{"x":[0,0.4],"y":[0.5,0.9]},"inherit":true},"13007e736047":{"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"values":{},"labels":{},"type":"pie","textinfo":"label+percent","name":"Ensmbel","domain":{"x":[0.6,1],"y":[0.5,0.9]},"inherit":true},"13001d802beb":{"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"values":{},"labels":{},"type":"pie","textinfo":"label+percent","name":"NCBI","domain":{"x":[0.3,0.7],"y":[0.2,0.6]},"inherit":true}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"title":"Pie Charts showing genomic regions from different databases","showlegend":false,"xaxis":{"showgrid":false,"zeroline":false,"showticklabels":false},"yaxis":{"showgrid":false,"zeroline":false,"showticklabels":false},"hovermode":"closest"},"source":"A","config":{"showSendToCloud":false},"data":[{"values":[1,3,60,38,6,2,7,2],"labels":["downstream","exonic","intergenic","intronic","ncRNA_exonic","ncRNA_intronic","upstream","UTR3"],"type":"pie","textinfo":"label+percent","name":"UCSC","domain":{"x":[0,0.4],"y":[0.5,0.9]},"marker":{"color":"rgba(31,119,180,1)","line":{"color":"rgba(255,255,255,1)"}},"frame":null},{"values":[3,3,51,33,8,7,12,1,1],"labels":["downstream","exonic","intergenic","intronic","ncRNA_exonic","ncRNA_intronic","upstream","UTR3","UTR5"],"type":"pie","textinfo":"label+percent","name":"Ensmbel","domain":{"x":[0.6,1],"y":[0.5,0.9]},"marker":{"color":"rgba(255,127,14,1)","line":{"color":"rgba(255,255,255,1)"}},"frame":null},{"values":[1,3,64,30,4,9,7,1],"labels":["downstream","exonic","intergenic","intronic","ncRNA_exonic","ncRNA_intronic","upstream","UTR5"],"type":"pie","textinfo":"label+percent","name":"NCBI","domain":{"x":[0.3,0.7],"y":[0.2,0.6]},"marker":{"color":"rgba(44,160,44,1)","line":{"color":"rgba(255,255,255,1)"}},"frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->

<!--html_preserve--><div id="htmlwidget-72f95678c2235c65af59" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-72f95678c2235c65af59">{"x":{"visdat":{"130033b6db7":["function () ","plotlyVisDat"]},"cur_data":"130033b6db7","attrs":{"130033b6db7":{"labels":{},"values":{},"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"pie","hole":0.2,"textinfo":"label+percent","showlegend":false,"inherit":true}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"hovermode":"closest","showlegend":true},"source":"A","config":{"showSendToCloud":false},"data":[{"labels":["downstream","exonic","intergenic","intronic","ncRNA_exonic","ncRNA_intronic","upstream","UTR5"],"values":[1,3,64,30,4,9,7,1],"type":"pie","hole":0.2,"textinfo":"label+percent","showlegend":false,"marker":{"color":"rgba(31,119,180,1)","line":{"color":"rgba(255,255,255,1)"}},"frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->
