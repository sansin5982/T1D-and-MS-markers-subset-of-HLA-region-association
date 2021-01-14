T1D\_MS
================
Sandeep Singh
14/01/2021

  - raw\_data.txt file was generated from previous researches on
    Type-1-diabetes and multiple sclerosis.  
  - This file contains only 119 SNPs as common markers for T1D and MS.

## File preparation

<!--html_preserve-->

<div id="htmlwidget-76036c4161c719e3c66f" class="datatables html-widget" style="width:100%;height:auto;">

</div>

<script type="application/json" data-for="htmlwidget-76036c4161c719e3c66f">{"x":{"filter":"none","data":[["1","2","3","4","5","6","7","8","9","10","11","12","13","14","15","16","17","18","19","20","21","22","23","24","25","26","27","28","29","30","31","32","33","34","35","36","37","38","39","40","41","42","43","44","45","46","47","48","49","50","51","52","53","54","55","56","57","58","59","60","61","62","63","64","65","66","67","68","69","70","71","72","73","74","75","76","77","78","79","80","81","82","83","84","85","86","87","88","89","90","91","92","93","94","95","96","97","98","99","100","101","102","103","104","105","106","107","108","109","110","111","112","113","114","115","116","117","118","119"],["rs1632953","rs1059174","rs1736921","rs1736916","rs1736913","rs1610603","rs1633070","rs1633069","rs1610630","rs1737068","rs1737060","rs2517646","rs2516675","rs3130000","rs3094123","rs6931717","rs2530709","rs2517538","rs4713429","rs9262615","rs2523881","rs2523880","rs2233969","rs1265052","rs2233967","rs3130981","rs3095324","rs3095314","rs3130558","rs3131009","rs3130564","rs2073723","rs2106074","rs9263804","rs3130501","rs3132524","rs3095238","rs7452756","rs12199773","rs9295965","rs3130531","rs3095250","rs3130532","rs6937967","rs3132486","rs6906846","rs7382297","rs2524095","rs2524089","rs2523535","rs2523534","rs2596437","rs12178292","rs5025315","rs5022119","rs2523638","rs3997982","rs2596571","rs2523485","rs2596517","rs2516460","rs3131622","rs2248373","rs2523650","rs2904776","rs2905747","rs9267247","rs3131631","rs10456058","rs2736177","rs2736172","rs760293","rs3130287","rs3131294","rs438475","rs415929","rs3115576","rs9267971","rs3130311","rs910049","rs6907322","rs3129934","rs12528797","rs2076530","rs3806156","rs7756262","rs9268645","rs3129877","rs3135392","rs9268831","rs9268877","rs9275765","rs9275772","rs9461799","rs9469240","rs9275793","rs2227127","rs9276429","rs9276431","rs9276432","rs9276440","rs7768538","rs7453920","rs2051549","rs6902723","rs6903130","rs9296044","rs2857212","rs2621382","rs241427","rs9276825","rs241403","rs3101942","rs1050391","rs11539216","rs17840186","rs7382662","rs10807118","rs10947377"]],"container":"<table class=\"display\">\n  <thead>\n    <tr>\n      <th> <\/th>\n      <th>SNP<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"order":[],"autoWidth":false,"orderClasses":false,"columnDefs":[{"orderable":false,"targets":0}]}},"evals":[],"jsHooks":[]}</script>

<!--/html_preserve-->

  - A total of 119 SNPs.
  - This file was used to create ANNOVAR formatted file.

### File preparation by ANNOVAR

  - Command used in ANNOVAR:

convert2annovar.pl -format rsid T1D.txt -dbsnpfile
humandb/hg19\_snp138.txt \> T1D\_MS\_formatted

  - 119 SNPs records input; 110 SNPs records as output, 9 SNPs missing

<!-- end list -->

    ##     V1       V2       V3 V4 V5        V6
    ## 1 chr6 29692305 29692305  A  G rs1632953
    ## 2 chr6 29694427 29694427  C  T rs1059174
    ## 3 chr6 29696209 29696209  G  A rs1736921
    ## 4 chr6 29704083 29704083  C  T rs1736916
    ## 5 chr6 29704400 29704400  T  C rs1736913
    ## 6 chr6 29708222 29708222  T  C rs1610603

  - Identify 9 missing SNPs

<!-- end list -->

    ## [1] "rs6931717"  "rs7452756"  "rs12199773" "rs6937967"  "rs12178292"
    ## [6] "rs10456058" "rs7382662"  "rs10807118" "rs10947377"

  - missing SNP IDs were renamed from PUBMED
    
        rs6931717 > rs3095345
        
        rs7452756 > rs4516988
        
        rs12199773 > rs3130952
        
        rs6937967 >  rs3130534
        
        rs12178292 > rs2844558
        
        rs10456058 >  rs2734573
        
        rs7382662 >  rs3129305
        
        rs10807118 >  rs3130578
        
        rs10947377 > rs3130179

  - Created a new file T1D\_2.txt after chainging SNP ids

  - Rerun in ANNOVAR and obtained results for all 119 SNPs

<!-- end list -->

    ##     V1       V2       V3 V4 V5        V6
    ## 1 chr6 29692305 29692305  A  G rs1632953
    ## 2 chr6 29694427 29694427  C  T rs1059174
    ## 3 chr6 29696209 29696209  G  A rs1736921
    ## 4 chr6 29704083 29704083  C  T rs1736916
    ## 5 chr6 29704400 29704400  T  C rs1736913
    ## 6 chr6 29708222 29708222  T  C rs1610603

# ANNOVAR ANALYSIS

## Gene based annotation

### Known Gene (UCSC)

    ##   Genomic region      Gene Chromosome     BP_1     BP_2 A1 A2       SNP
    ## 1       intronic     HLA-F       chr6 29692305 29692305  A  G rs1632953
    ## 2   ncRNA_exonic HLA-F-AS1       chr6 29694427 29694427  C  T rs1059174
    ## 3   ncRNA_exonic HLA-F-AS1       chr6 29696209 29696209  G  A rs1736921
    ## 4   ncRNA_exonic HLA-F-AS1       chr6 29704083 29704083  C  T rs1736916
    ## 5   ncRNA_exonic HLA-F-AS1       chr6 29704400 29704400  T  C rs1736913
    ## 6 ncRNA_intronic HLA-F-AS1       chr6 29708222 29708222  T  C rs1610603

### Ensembel Gene

    ##   Genomic region            Gene Chromosome     BP_1     BP_2 A1 A2       SNP
    ## 1       intronic ENSG00000204642       chr6 29692305 29692305  A  G rs1632953
    ## 2   ncRNA_exonic ENSG00000214922       chr6 29694427 29694427  C  T rs1059174
    ## 3   ncRNA_exonic ENSG00000214922       chr6 29696209 29696209  G  A rs1736921
    ## 4   ncRNA_exonic ENSG00000214922       chr6 29704083 29704083  C  T rs1736916
    ## 5   ncRNA_exonic ENSG00000214922       chr6 29704400 29704400  T  C rs1736913
    ## 6 ncRNA_intronic ENSG00000214922       chr6 29708222 29708222  T  C rs1610603

### Ref Gene (NCBI)

    ##   Genomic_region      Gene Chromosome     BP_1     BP_2 A1 A2       SNP
    ## 1       intronic     HLA-F       chr6 29692305 29692305  A  G rs1632953
    ## 2   ncRNA_exonic HLA-F-AS1       chr6 29694427 29694427  C  T rs1059174
    ## 3   ncRNA_exonic HLA-F-AS1       chr6 29696209 29696209  G  A rs1736921
    ## 4 ncRNA_intronic HLA-F-AS1       chr6 29704083 29704083  C  T rs1736916
    ## 5 ncRNA_intronic HLA-F-AS1       chr6 29704400 29704400  T  C rs1736913
    ## 6 ncRNA_intronic HLA-F-AS1       chr6 29708222 29708222  T  C rs1610603

  - We will use known gene as reference to create table
    <!--html_preserve-->
    <div id="htmlwidget-2c5c6fa3c15fbe59ad3c" class="plotly html-widget" style="width:672px;height:480px;">
    </div>
    <script type="application/json" data-for="htmlwidget-2c5c6fa3c15fbe59ad3c">{"x":{"visdat":{"1d8043915f6c":["function () ","plotlyVisDat"],"1d8055696721":["function () ","data"],"1d80381a64da":["function () ","data"],"1d80dbf4850":["function () ","data"]},"cur_data":"1d80dbf4850","attrs":{"1d8055696721":{"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"values":{},"labels":{},"type":"pie","textinfo":"label+percent","name":"UCSC","domain":{"x":[0,0.4],"y":[0.5,0.9]},"inherit":true},"1d80381a64da":{"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"values":{},"labels":{},"type":"pie","textinfo":"label+percent","name":"Ensmbel","domain":{"x":[0.6,1],"y":[0.5,0.9]},"inherit":true},"1d80dbf4850":{"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"values":{},"labels":{},"type":"pie","textinfo":"label+percent","name":"NCBI","domain":{"x":[0.3,0.7],"y":[0.2,0.6]},"inherit":true}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"title":"Pie Charts showing genomic regions from different databases","showlegend":false,"xaxis":{"showgrid":false,"zeroline":false,"showticklabels":false},"yaxis":{"showgrid":false,"zeroline":false,"showticklabels":false},"hovermode":"closest"},"source":"A","config":{"showSendToCloud":false},"data":[{"values":[1,3,60,38,6,2,7,2],"labels":["downstream","exonic","intergenic","intronic","ncRNA_exonic","ncRNA_intronic","upstream","UTR3"],"type":"pie","textinfo":"label+percent","name":"UCSC","domain":{"x":[0,0.4],"y":[0.5,0.9]},"marker":{"color":"rgba(31,119,180,1)","line":{"color":"rgba(255,255,255,1)"}},"frame":null},{"values":[3,3,51,33,8,7,12,1,1],"labels":["downstream","exonic","intergenic","intronic","ncRNA_exonic","ncRNA_intronic","upstream","UTR3","UTR5"],"type":"pie","textinfo":"label+percent","name":"Ensmbel","domain":{"x":[0.6,1],"y":[0.5,0.9]},"marker":{"color":"rgba(255,127,14,1)","line":{"color":"rgba(255,255,255,1)"}},"frame":null},{"values":[1,3,64,30,4,9,7,1],"labels":["downstream","exonic","intergenic","intronic","ncRNA_exonic","ncRNA_intronic","upstream","UTR5"],"type":"pie","textinfo":"label+percent","name":"NCBI","domain":{"x":[0.3,0.7],"y":[0.2,0.6]},"marker":{"color":"rgba(44,160,44,1)","line":{"color":"rgba(255,255,255,1)"}},"frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>
    <!--/html_preserve-->

<!--html_preserve-->

<div id="htmlwidget-48e029041075ea760cfa" class="plotly html-widget" style="width:672px;height:480px;">

</div>

<script type="application/json" data-for="htmlwidget-48e029041075ea760cfa">{"x":{"visdat":{"1d8069136b56":["function () ","plotlyVisDat"]},"cur_data":"1d8069136b56","attrs":{"1d8069136b56":{"labels":{},"values":{},"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"pie","hole":0.2,"textinfo":"label+percent","showlegend":false,"inherit":true}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"hovermode":"closest","showlegend":true},"source":"A","config":{"showSendToCloud":false},"data":[{"labels":["downstream","exonic","intergenic","intronic","ncRNA_exonic","ncRNA_intronic","upstream","UTR5"],"values":[1,3,64,30,4,9,7,1],"type":"pie","hole":0.2,"textinfo":"label+percent","showlegend":false,"marker":{"color":"rgba(31,119,180,1)","line":{"color":"rgba(255,255,255,1)"}},"frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>

<!--/html_preserve-->
