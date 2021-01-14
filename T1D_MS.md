-   raw\_data.txt file was generated from previous researches on
    Type-1-diabetes and multiple sclerosis.  
-   This file contains only 119 SNPs as common markers for T1D and MS.

File preparation
----------------

    ##         SNP
    ## 1 rs1632953
    ## 2 rs1059174
    ## 3 rs1736921
    ## 4 rs1736916
    ## 5 rs1736913
    ## 6 rs1610603

-   A total of 119 SNPs.
-   This file was used to create ANNOVAR formatted file.

### File preparation by ANNOVAR

-   Command used in ANNOVAR:

convert2annovar.pl -format rsid T1D.txt -dbsnpfile
humandb/hg19\_snp138.txt &gt; T1D\_MS\_formatted

-   119 SNPs records input; 110 SNPs records as output, 9 SNPs missing

<!-- -->

    ##     V1       V2       V3 V4 V5        V6
    ## 1 chr6 29692305 29692305  A  G rs1632953
    ## 2 chr6 29694427 29694427  C  T rs1059174
    ## 3 chr6 29696209 29696209  G  A rs1736921
    ## 4 chr6 29704083 29704083  C  T rs1736916
    ## 5 chr6 29704400 29704400  T  C rs1736913
    ## 6 chr6 29708222 29708222  T  C rs1610603

-   Identify 9 missing SNPs

<!-- -->

    ## [1] "rs6931717"  "rs7452756"  "rs12199773" "rs6937967"  "rs12178292"
    ## [6] "rs10456058" "rs7382662"  "rs10807118" "rs10947377"

-   missing SNP IDs were renamed from PUBMED

        rs6931717 > rs3095345

        rs7452756 > rs4516988

        rs12199773 > rs3130952

        rs6937967 >  rs3130534

        rs12178292 > rs2844558

        rs10456058 >  rs2734573

        rs7382662 >  rs3129305

        rs10807118 >  rs3130578

        rs10947377 > rs3130179

-   Created a new file T1D\_2.txt after chainging SNP ids

-   Rerun in ANNOVAR and obtained results for all 119 SNPs

<!-- -->

    ##     V1       V2       V3 V4 V5        V6
    ## 1 chr6 29692305 29692305  A  G rs1632953
    ## 2 chr6 29694427 29694427  C  T rs1059174
    ## 3 chr6 29696209 29696209  G  A rs1736921
    ## 4 chr6 29704083 29704083  C  T rs1736916
    ## 5 chr6 29704400 29704400  T  C rs1736913
    ## 6 chr6 29708222 29708222  T  C rs1610603
