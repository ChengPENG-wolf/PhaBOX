<img src='imgs/logo.jpg'>


# Local version of [PhaBOX2](https://phage.ee.cityu.edu.hk) web server

[![PhaBOX Server](https://img.shields.io/badge/PhaBOX-Webserver-brightgreen)](http://phage.ee.cityu.edu.hk/)
[![GitHub License](https://img.shields.io/github/license/KennthShang/PhaBOX)](https://github.com/KennthShang/PhaBOX/blob/main/LICENSE.md)
[![BioConda Install](https://img.shields.io/conda/dn/bioconda/phabox.svg?style=flag&label=BioConda%20install)](https://anaconda.org/bioconda/phabox) 
[![PhaBOXv1](https://img.shields.io/static/v1.svg?label=PhaBOX_v1&message=bioadv/vbad101&color=blue)](https://doi.org/10.1093/bioadv/vbad101)
[![PhaMer](https://img.shields.io/static/v1.svg?label=PhaMer&message=bib/bbac258&color=blue)](https://doi.org/10.1093/bib/bbac258)
[![PhaGCN](https://img.shields.io/static/v1.svg?label=PhaGCN&message=bioinformatics/btab293&color=blue)](https://doi.org/10.1093/bioinformatics/btab293)
[![PhaTYP](https://img.shields.io/static/v1.svg?label=PhaTYP&message=bib/bbac487&color=blue)](https://doi.org/10.1093/bib/bbac487)
[![CHERRY](https://img.shields.io/static/v1.svg?label=CHERRY&message=bib/bbac182&color=blue)](https://doi.org/10.1093/bib/bbac182)
[![PhaVIP](https://img.shields.io/static/v1.svg?label=CHERRY&message=bioinformatics/btad229&color=blue)](https://doi.org/10.1093/bioinformatics/btad229)

This is the source code of our website [PhaBOX2](https://phage.ee.cityu.edu.hk), consisting of the latest updates of our previously released programs: PhaMer, PhaGCN, CHERRY/HostG, and PhaTYP.

Please download this local version for large-scale sequencing data and use more threads to speed up the program.

<a name="news"></a>
## ⌛️&nbsp; News

PhaBOX has now been upgraded to the 2.0 version with faster speed!

There are some major components, including:

  🎉 Generalized for all kinds of viruses; more than just bacteriophage

  🎉 Virus identification (latest PhaMer)

  🎉 Taxonomy classification (latest PhaGCN)

  🎉 Host prediction (latest CHERRY/HostG)

  🎉 Lifestyle prediction (latest PhaTYP)

  🎉 Contamination/provirus detection

  🎉 vOTU grouping

  🎉 Phylogenetic tree based on marker genes

  🎉 Viral protein annotation

  🎉 All the databases are updated to the latest ICTV 2024 release

If you have any more suggestions, feel free to let me know! We consider long-term maintenance PhaBOX and adding modules according to your needs


You can post an issue or directly email me (jiayushang@cuhk.edu.hk). We welcome any suggestions.

<a name="quick"></a>
## 🚀&nbsp; Quick Start
> [!IMPORTANT]
> If you are a new user, please check our [WIKI](https://github.com/KennthShang/PhaBOX/wiki) page. We provide a tutorial to help you get started quickly and understand how to use PhaBOX2. We hope you will enjoy it!
>
> If you only want to analyze the results for Bacteriophages (as version 1), please check the **Prokarytic viruses** columns in the PhaGCN's results.


If you are familiar with the PhaBOX2, please check our [Update log](https://github.com/KennthShang/PhaBOX/wiki/Update-logs). We may have some updates to the program to make it more useful. If you want to use the latest version, please also [upgrade your PhaBOX2](https://github.com/KennthShang/PhaBOX/wiki#upgrading-phabox)


## 🚀&nbsp; The Most Recent Update Logs

### 2.1.11 March 6, 2025

> [!IMPORTANT]
> New functions were added to the cherry host prediction task
> We also adjust the host prediction logic as below:
> 1. CRISPRs from MAGs (if MAGs were provided)
> 2. BLASTN (prophage) from MAGs (if MAGs were provided)
> 3. Protein organization compared to the viruses in the database
> 4. CRISPRs from database


New added parameters in `--task cherry`
```
--prophage
     Minimum alignment length for estimating potential prophage || default: 1000 || range from 0 to 100000
```


### 2.1.10 Dec 26, 2024

> [!IMPORTANT]
>  Now, the end-to-end task allow to skip the PhaMer(virus identification). 
>  If users already have the viral contigs as their inputs, they can run end-to-end task using `--skip Y` to skip the virus identification
>  However, please noted that the default parameters is `--skip N`

We also added a log output that tells the user that PhaMer detected no viruses and stopped the following pipelines in the end-to-end task in  `--skip N` condition.

<a name="license"></a>

## 📘&nbsp; License
The PhaBOX pipelines are released under the terms of the [Academic Free License v3.0 License](https://choosealicense.com/licenses/afl-3.0/).

