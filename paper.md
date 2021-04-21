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
  - name: Caleb Dixon
    affiliation: 2
  - name: Keary Griffin
    affiliation: 3
  - name: Tucker Jaenicke
    affiliation: 2
  - name: Alvin Siu
    affiliation: 2
  - name: Josh Zagorsky
    affiliation: 2
  - name: Eli Jones
    affiliation: 2
affiliations:
 - name: Department of Biostatistics, Harvard T.H. Chan School of Public Health, Harvard University
   index: 1
 - name: Zagaran, Inc.
   index: 2
 - name: Rocket Farm Studios
   index: 3
date: 15 February 2021
bibliography: paper.bib

---

# Summary

The phenotype of an organism is a collection of traits, such as enzyme activity, hormone levels, and behavior. Many researchers are increasingly advocating a more substantial role for large-scale phenotyping as a route to advances in the biomedical sciences. Of the many different phenotypes, social, behavioral, and cognitive phenotypes have traditionally been challenging for phenomics because of their temporal nature, context dependence, and the lack of tools for measuring them objectively in naturalistic settings. Pen-and-paper surveys are still widely used to solicit these phenotypes although they suffer from well-documented biases. We have introduced the concept of digital phenotyping as the “moment-by-moment quantification of the individual-level human phenotype *in situ* using data from personal digital devices” [@onnela2016harnessing, @torous2016new]. The ubiquity of smartphones presents an opportunity to capture social, behavioral, and cognitive markers in free-living settings, offering a scalable solution to the phenotyping problem. In addition to enabling more objective measurement of existing phenotypes, the approach can also give rise to entirely new phenotypes; see Figure \autoref{fig:schematic}.

# Statement of need

Beiwe is a data collection platform for high-throughput digital phenotyping. This open-source (BSD-3) multi-language software has been in development and use since 2013, and it consists of two native front-end applications, one for Android (written in Java and Kotlin) and another for iOS (written in Swift and Objective-C). The Beiwe back-end, which is based on Amazon Web Services (AWS) cloud computing infrastructure, has been implemented primarily in Python 3.6, but it also makes use of Django for ORM and Flask for API and web servers. It also uses several AWS services, primarily S3 for flat file storage, EC2 virtual servers for data processing, Elastic Beanstalk for orchestration, and RDS for PostgreSQL database engine.

Beiwe is intended for use in research. Essentially all software development kits (SDKs) made by companies like Apple and Google generate unvalidated behavioral summary measures using closed proprietary algorithms that do not meet the high standards of reproducible science. In contrast, Beiwe collects raw sensor and device usage data, which enables construction of built-for-purpose data features and summary statistics that directly address the scientific questions of interest. Collection of raw data also improves reproducibility of studies and enables re-analyses of data and pooling of data across studies. Every aspect of Beiwe data collection is fully customizable, including which sensors to sample, how frequently to sample them, whether to add Gaussian noise to GPS location, whether to use Wi-Fi or cellular data for uploads, how frequently to upload data, specification of surveys and their response options and skip logic, etc. All study settings are captured in an easily sharable JSON-formatted configuration file to enhance transparency and reproducibility of studies.

Beiwe has been used in tens of scientific studies on three continents across various fields, and there may be several additional studies we are not aware of. Smartphone-based digital phenotyping is potentially very promising in behavioral and mental health [@onnela2016harnessing], and new research tools like Beiwe are especially needed in psychiatry [@torous2016new], where in the context of schizophrenia it has been used to predict patient relapse [@barnett2018relapse], compare passive and active estimates of sleep [@staples2017comparison], and characterize the clinical relevance of digital phenotyping data quality [@torous2018characterizing]. The platform has also been used to assess depressive symptoms in a transdiagnostic cohort [@pelligrini2021estimating] and to capture suicidal thinking during the COVID-19 pandemic [@fortgang2020increase]. There is an increasing amount of research on the use of Beiwe in neurological disorders, such as in the quantification of ALS progression [@berry2019design] and behavioral changes in people with ALS during the COVID-19 pandemic [@beukenhorst2021smartphone]. The platform has also been used in the context of cancer to assess postoperative physical activity among patients undergoing cancer surgery [@panda2021smartphone], to capture novel recovery metrics after cancer surgery [@panda2020using], to enhance recovery assessment after breast cancer surgery [@panda2020smartphone], and to enhance cancer care [@wright2018hope]. Digital phenotyping and Beiwe have also been applied to quantifying mobility and quality of life of spine patients [@cote2019digital] and to study psychosocial well-being of individuals after spinal cord injury [@mercier2020digital].

![Digital phenotyping consists of collection and analysis of high-throughput data from personal digital devices. This bipartite graph represents a schematic mapping between various data streams of a device and a subset of phenotypes. The circular nodes on the left correspond to traditional phenotypes, such as height and blood type; those on the right correspond to social and behavioral phenotypes that have traditionally eluded capture in free-living settings but can now be obtained using smartphones, such as sociability and physical activity; some of the phenotypes overlap, such as those related to sleep.\label{fig:schematic}](schematic.pdf)

# Acknowledgements

The Principal Investigator, Jukka-Pekka Onnela, is extremely grateful for his NIH Director’s New Innovator Award in 2013 (DP2MH103909) for enabling the crystallization of the concept of digital phenotyping and the construction of the Beiwe platform. He is also grateful to the members of the Onnela Lab. The authors also wish to acknowledge the contributions of the following individuals at Zagaran: Aaron Klein, Kevin Fan, Christopher McCarthy, Dor Samet, Alicia Fan, Rebecca Magazine Malamud, Jacob Klingensmith, and Benjamin Zagorsky.

# References
