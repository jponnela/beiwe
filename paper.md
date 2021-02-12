---
title: 'Beiwe: A data collection platform for high-throughput digital phenotyping'
tags:
  - high-throughput
  - digital phenotyping
  - multi-language
  - smartphone
  - AWS
authors:
  - name: Jukka-Pekka Onnela^[Principal Investigator and corresponding author.]
    orcid: 0000-0001-6613-8668
    affiliation: 1
  - name: Zagaran Author 1
    affiliation: 2
  - name: Zagaran Author 2
    affiliation: 2
  - name: Zagaran Author 3
    affiliation: 2
affiliations:
 - name: Department of Biostatistics, Harvard T.H. Chan School of Public Health, Harvard University
   index: 1
 - name: Zagaran, Inc.
   index: 2
date: 12 February 2021
bibliography: paper.bib

---

# Summary

The phenotype of an organism is a collection of traits, such as enzyme activity, hormone levels, and behavior. Many researchers are increasingly advocating a more substantial role for large-scale phenotyping as a route to advances in the biomedical sciences. Of the many different phenotypes, social, behavioral and cognitive phenotypes have traditionally been challenging for phenomics because of their temporal nature, context dependence, and the lack of tools for measuring them objectively in naturalistic settings. Pen-and-paper surveys are still widely used to solicit these phenotypes although they suffer from well-documented biases. We have introduced the concept of digital phenotyping as the “moment-by-moment quantification of the individual-level human phenotype in situ using data from personal digital devices.” The ubiquity of smartphones presents an opportunity to capture social, behavioral, and cognitive markers in free-living settings, offering a scalable solution to the phenotyping problem.

# Statement of need

Beiwe is a data collection platform for high-throughput digital phenotyping. This multi-language software has been in development and use since 2013, and it consists of two native front-end applications, one for Android (written in Java) and another for iOS (written in Swift & Objective-C). The Beiwe back-end, which is based on Amazon Web Services (AWS) cloud computing infrastructure, has been implemented primary in Python 3.6, but it also makes use of Django (for ORM) and Flask (for API and web server). It also uses several AWS services, primary S3 (for flat file storage), EC2 (servers), Elastic Beanstalk (scaling servers), and RDS (PostgreSQL).

Beiwe is intended for use in research. Essentially all software development kits (SDKs) made by companies like Apple and Google generate unvalidated behavioral summary measures using closed proprietary algorithms that do not meet the high standards of reproducible science. In contrast, Beiwe collects raw sensor and device usage data, which enables pooling of data across studies and re-analyses of data as new methods become available. Every aspect of data collection is fully customizable, including which sensors to sample, how frequently to sample them, whether to add Gaussian noise to GPS location, whether to use Wi-Fi or cellular data for uploads, how frequently to upload data, specification of surveys and their response options and skip logic, etc. All study settings are captured in a JSON-formatted configuration file to enhance transparency and repdocuibility of studies. Beiwe has been and continues to be used in a number of scientific studies on three continents in various areas ranging from XXX [@Pearson:2017] to YYY [@Pearson:2017] and [@Pearson:2017].

# Citations

Citations to entries in paper.bib should be in
[rMarkdown](http://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html)
format.

If you want to cite a software repository URL (e.g. something on GitHub without a preferred
citation) then you can do it with the example BibTeX entry below for @fidgit.

For a quick reference, the following citation commands can be used:
- `@author:2001`  ->  "Author et al. (2001)"
- `[@author:2001]` -> "(Author et al., 2001)"
- `[@author1:2001; @author2:2001]` -> "(Author1 et al., 2001; Author2 et al., 2002)"

# Figures

Figures can be included like this:
![Caption for example figure.\label{fig:example}](figure.png)
and referenced from text using \autoref{fig:example}.

Figure sizes can be customized by adding an optional second parameter:
![Caption for example figure.](figure.png){ width=20% }

# Acknowledgements

We acknowledge contributions from Brigitta Sipocz, Syrtis Major, and Semyeong
Oh, and support from Kathryn Johnston during the genesis of this project.

# References
