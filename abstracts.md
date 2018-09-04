# Abstracts

## Scaling genomics in the AWS cloud

**Brendan Bouffler**, *Global Lead, AWS Research Cloud Program, UK*

An update on all the latest technical developments from AWS's Engineering team that we’re building for the research and engineering community. We’ll deep dive on some that are particularly relevant to to Nextflow's users and developers and ask for input from the audience to help us understand what other things we can engineer with the advice and insights from people in the audience.

#### Bio

Brendan Bouffler has 25 years of experience in the global tech industry creating very large systems for high performance environments. In the late 90’s he helped co-found an Australian dot-com start-up in New York to apply extreme computing to streaming media for broadcast video environments. The company was successfully acquired by Apple in 2004.

He has since been responsible for designing and building hundreds of HPC systems for researchers as well as commercial and defense organizations, all around the world. Quite a number of his efforts are listed in the top500, including some that placed in the top 5.

After leading the HPC Organization in Asia for a hardware maker, Brendan joined Amazon in 2014 when it became clear to him that cloud would become the exceptional computing tool the global research community needed to accelerate discoveries and change the world for us all. The AWS Research Cloud program he leads is tasked with that mission.

He holds a degree in physics and is the principle author of the Researcher’s Handbook (the “missing manual” for research workloads on AWS). He is based in London.


## nf-core: A community effort to collect curated Nextflow pipelines

**Philip Ewels**, *Head of Genomics Applications Development at SciLifeLab National Genomics Infrastructure, Sweden*

The Swedish National Genomics Infrastructure (NGI) has been a key user and proponent of nextflow since soon after its initial release. We have produced several popular pipelines as well as writing recommendations on best practices. Our oldest pipeline for RNA sequencing analysis is used in production at NGI Stockholm and has been used to process nearly 20,000 samples since April 2017.

The open-source NGI pipelines hosted on GitHub have now been forked by hundreds of users for their own development. This collaborative expansion has proceeded rapidly and is now beginning to outgrow the NGI branding of the pipelines. To encourage further growth and greater collaboration, we started a new initiative called nf-core (http://nf-co.re): a community effort to collect, curate and collaborate on high quality nextflow bioinformatics workflows.

Shared pipelines will give increased reproducibility between groups and greater collective development power. To help pipeline developers we have written a companion cookiecutter template to generate starter workflows and a command line tool to lint code and check for adherence to nf-core guidelines. Pipelines make the best use of Nextflow features possible, with support for conda, docker and singularity, with reference genomes available from the cloud. Consistency between pipelines means that all work in a similar manner with comparable requirements.

There has been fantastic feedback from the user community about nf-core. The first twitter post in February 2018 was seen by nearly four thousand people and the account now has over 140 followers. There are currently seven pipelines available (at the time of writing) with many more on the way.

#### Bio

Phil Ewels is the head of the Genomics Applications Development facility at the National Genomics Infrastructure (NGI) at SciLifeLab in Stockholm, Sweden. SciLifeLab is a national centre for molecular biosciences for Sweden; the NGI is the largest platform at SciLifeLab. We provide library preparation, sequencing and bioinformatics analysis support for research groups across the country.

Phil has been working at SciLifeLab for four years and moved to Sweden after a PhD and postdoc at the University of Cambridge and Babraham Institute in Cambridge, UK. He has has a history of lab and bioinformatics work in epigenetics and has a soft spot for software development with a focus on user friendliness. More recently he's developed MultiQC - a tool that parses log file outputs from multiple samples and bioinformatics tools and generates a single interactive HTML report. Now head of the Genomics Applications Development facility, he and his team focus on the development and scaling up of new lab protocols and bioinformatics solutions for the ISO accredited NGI Genomics Production facility. They develop new analysis pipelines and try to ensure that the tools they write are scalable, reproducible and transferable.

## Using Nextflow to create scalable and reproducible pipelines at Genomics Medicine Ireland

**Simone Coughlan**, *Bioinformatician, Genomics Medicine Ireland, Ireland*

Genomics Medicine Ireland (GMI) is an Irish life sciences company performing large-scale studies in the Irish population using whole genome sequencing (WGS) and additional omics technologies. It works in collaboration with the healthcare system, patients, researchers and industry to advance understanding of the genetic basis of multiple diseases, to aid in the discovery of new diagnostics and therapeutics. In order to do this, our data analysis pipelines must be reproducible and easily scale to large numbers of samples. At GMI, we have created multiple Nextflow pipelines, which also employ the use of containerisation technologies and Conda environments to ensure full reproducibility. These include pipelines to perform analysis of genotyping arrays, concordance analysis of genotyping and sequencing data, copy number variation calling and downstream processing of files for a validated secondary analysis pipeline. In summary, the ability to rapidly prototype workflows using any tool, resume execution upon failure, scale easily and maintain a consistent environment across runs make Nextflow well suited to our work.

#### Bio 

Dr Simone Coughlan is a bioinformatics scientist at Genomics Medicine Ireland, an Irish Life Sciences company undertaking large scale analysis of genomics and other omics data to help discover new diagnostics and therapeutics. She has a PhD in Bioinformatics from the National University of Ireland Galway and a background in parasite and bacterial genomics before turning to humans where she is now involved in research across multiple diseases. Writing robust, scalable pipelines is an essential part of the job and Nextflow allows her to do this with minimal fuss!

## Nextflow at the heart of UK genomics

**Vladimir Kiselev**, *Head of Cellular Genetics Informatics, Wellcome Sanger Institute, UK*

The Wellcome Sanger Institute is one of the biggest genomics centres in the world. To accommodate its compute needs it has ~10'000 cores on our LSF compute farm and ~12'000 cores on our OpenStack cloud environment. The Cellular Genetics programme is one of five of the Institute's programmes and investigates cell biology and human disease by focusing on cell types implicated in these processes. We utilise Nextflow to run our pipelines on both LSF and Openstack environments. In my talk I will present our recent experiences and will concentrate on Kubernetes integration in Nextflow.

#### Bio 

Vladimir graduated from the Moscow Institute of Physics and Technology in 2008 with a degree in Applied Physics and Mathematics. He then changed direction and did a PhD in Computational Biology at the University of Edinburgh. From 2011 he worked on multiple Bioinformatics projects at the European Bioinformatics Institute, the Babraham Institute and the Wellcome Trust Sanger Institute. In 2018 he became the Head of the core IT team at the Cellular Genetics programme of the Sanger Institute.

## Industrial Personalised Immunotherapy Pipeline Development with Nextflow

**Luke Goodsell**, *Team Leader, Bioinformatics Software Development, Achilles Therapeutics, UK* 

Cancer immunotherapy is a promising means of treatment that uses the patient's own immune system to destroy cancer cells. For over three decades, labs have been exploring ways to identify tumour specific surface proteins (neoantigens) and use them to induce the patient's immune cells to specifically target their cancer. This process is labour intensive and has highly variable results, in part due to tumour heterogeneity.
 
Achilles Therapeutics is developing a process for delivering a patient-specific immunotherapy that exploits recent research into tumour evolution to reliably identify and target the neoantigens that occur early in a tumour's development and thus are present in every tumour cell (i.e. clonal). At the heart of this process is a bioinformatic pipeline that takes DNA- and RNA-sequencing data and reports clonal, actionable neoantigens. Achilles inherited an R-based pipeline suited for answering cutting-edge research questions from one of its academic founding labs, but adapting this for industrial use posed many challenges including: adaptations for high-throughput operation, guaranteeing reproducibility, portability to other compute environments (particularly AWS), conformance to required standards for clinical use, end-to-end automation and quality control, "fail-safe" operation and rapid prototyping of new features.
 
This presentation will describe how the Achilles bioinformatics team used Nextflow (and other tools) to adapt a research-focussed sequence-processing pipeline into an efficient, reliable, portable and risk-managed system suitable for delivering a clinical personalised immunotherapy. This will include tips and tricks for developing modular Nextflow workflows and for ensuring early detection of errors.

#### Bio 

Luke Goodsell leads the Bioinformatics Software Development team at Achilles Therapeutics, where he has worked for 2 years. Before that he worked as a Computational Biologist at Oxford Gene Technology after completing his PhD in Structural, Computational and Chemical Biology. He is interested in applying data analysis techniques and software engineering experience to identify answers to bioinformatics questions and implementing robust, dependable software that uses those findings.

## Nextflow on the go

**Alessia Visconti**, *Research Fellow, King's College London, UK*

"YAMP" (Yet Another Metagenomics Pipeline) is a workflow that enables the analysis of whole shotgun metagenomic data while using containerization to ensure computational reproducibility and facilitate collaborative research. Being based on Nextflow, YAMP can be executed on any UNIX-like system and offers seamless support for multiple job schedulers as well as for the Amazon AWS cloud. 

Many users have already claimed that Nextflow is the most mature system supporting both local, HPC clusters and cloud computing execution, allowing a  smooth and problem-free transition from a local development to an HPC/cloud deployment. Yet, we wondered whether Nextflow could also be executed on portable miniaturised high-performance pieces of hardware, that is, on mobile phones. Indeed, if YAMP could be executed on portable devices, this would empower the analysis of metagenomics data from virtually everywhere, with huge benefits for scientists, patients, and clinicians alike.

The test was carried on during the ARM, Atos and Cavium BioData Hackathon challenge, organised at the Wellcome Genome Campus on July 2-3, 2018, where participants were asked to take advantage of fast-moving mobile technologies to develop innovative solutions for biomedical data processing. 

During the two-day Hackathon, Team GoGut successfully and easily ported YAMP onto ARM’s latest mobile architecture, the ARM Cavium ThunderX2, showing that the analysis of microbial sequences, and of biological data at large, can be successfully taken out of centralised data centres, and that Nextflow offers a mature solution also for mobile applications.

#### Bio 

Alessia Visconti is a research fellow in Computational Biology at the Department of Twin Research and Genetic Epidemiology, King’s College London. Her research activity deals with the study of the genomics and epigenomics of human diseases, with a focus on melanoma, cognition and neurodevelopmental disorders, and IgA nephropathy. Recently, she became interested in the human microbiome and its connections to human health and diseases.

## FlowCraft: A modular, extensible and flexible tool to build, monitor and report Nextflow pipelines

**Diogo Nuno Silva**, *Postdoctoral researcher, Instituto de Medicina Molecular João Lobo Antunes, Portugal*

Nextflow has emerged as a promising framework for building parallelized, scalable and reproducible workflows using software containers. Amongst its most attractive features are the support for multi scale containerization and its portability, which allows the same code to be executed on multiple platforms with different batch schedulers and container systems. 
Usually, the generation of nextflow pipelines entails the creation of a main nextflow file with all the declarations of the pipeline’s processes, its channels and operators, and optional configuration and auxiliary files that are necessary for its execution. However, due to the fast pace and continuous development of software for genomic analyses and the need for a quick response to this change by altering existing pipelines, it would be important to make this process more agile and dynamic. Furthermore, the analyses’ goals also change over time and variations of existing pipelines are needed to answer new questions. 
The FlowCraft project aims to address these issues by proposing a new tool that leverages the combination of Nextflow and docker/singularity containers to assemble, monitor and report scientific pipelines. The premise of FlowCraft is simple: the users create a broad set of components written in Nextflow language that can then be freely and easily assembled into ready-to-use pipelines taking full advantage of Nextflow execution. These components are modular pieces of software or scripts (e.g. FastQC or Trimmomatic) that have a set of attributes, including input and output types and other parameters. FlowCraft’s engine then connects them, handling the linking and forking of channels automatically, among several other features. This modularity has two major advantages: (i) each process on a FlowCraft Nextflow pipeline can be written once and re-used to quickly build fairly complex pipelines for different endswith minimal effort; and (ii) adding/modifying parts of a pipeline does not require modification in the codebase of other components. This means that new additions to any pipeline can be easily introduced, and modifications to existing pipelines only require replacing the corresponding components. FlowCraft further extends the capabilities of Nextflow by providing an Inspection mode that monitors the execution of a pipeline in real time, either in a terminal using a curses interface, or via the FlowCraft web application (demo: https://www.youtube.com/watch?v=liG1hlEcs5M). Furthermore, it is currently under development a Report mode that allows the interactive visualization of the results from each component in the web application. The final aim of this project is to have a flexible, extensible and modular system built on top of Nextflow for building, monitoring and reporting scientific pipelines in any omics field. Flowcraft can be found in https://github.com/assemblerflow/flowcraft/ and the complete user guide is hosted at http://flowcraft.readthedocs.io/en/latest/.

#### Bio 

Hi, I'm Diogo. I'm a freshly minted postdoctoral researcher working on genomics of fungal and bacterial pathogens. I graduated in Environmental Biology, have a masters in Human and Environmental Biology and a PhD in Bioinformatics and Evolutionary Biology. During my research I have grown a keen fondness for computational biology and all things (bio)informatics. I started hacking on nextflow as soon as I discovered the framework (about one year ago) and since then I've never looked back on ways of building workflows and scientific pipelines. I am currently active in developing workflows for the analysis of bacterial and fungal genomic data and using nextflow whenever possible/relevant.

## IARC nextflow pipelines: towards efficient cancer genomics analyses

**Tiffany Delhomme**, *PhD student, IARC (WHO), France* 

A current effort is emerging inside the IARC to enable researchers to produce accurate cancer genomics results. This involves both a state-of-the-art method selection but also an efficient way to use them. To ensure this, IARC bioinformaticians are actively developing cancer genomics pipelines emphasizing performance, easy usage, reproducibility and computational efficiency. Our approach for that consists in using the nextflow langage to write our pipelines, and the combination of Docker, Singularity and Conda to distribute them and install dependencies. In this talk I will describe the global architecture of our cancer genomics pipelines. Then, I will focus my talk on one of the most complicated pipeline we have developed, which is used to estimate intra-tumor heterogeneity from whole-genome sequencing of multiple tumor regions of a cancer patient.

#### Bio 

I am currently working at the Section of Genetics, International Agency for Research on Cancer, in the Genetics Cancer Susceptibility Group. I am a PhD candidate trying to decipher cancer genomics issues using computational/statistical methods.

## Agile pipelines with Nextflow: how to go from development to production without pain

**Francesco Strozzi**, *Bioinformatics Head	Enterome Bioscience, France* 

Nextflow allows creating pipelines in a very agile way, starting from simple blocks and processes to test new software and parameters. Once a single block of the pipeline works as expected and there are no errors, the developer can simply add a new process and start exploring and testing a new layer of the pipeline. The main Nextflow features allowing this agile development are the data flow model, jobs traceability and the possibility to resume workflows, without the need to re-run unchanged and already completed steps. The advanced logging and reporting system that Nextflow offers are also critical features helping with jobs profiling and monitoring. Finally, the support for multiple executors and the transparent use of software containers allow to prototype pipelines locally and then to port them in production on large HPC systems or on the cloud.
In this talk, agile pipelines development with Nextflow will be presented from the point of view of Enterome Bioscience, a biotech company working on the human gut microbiome. In the company, cutting-edge bioinformatics pipelines are central to support the development of diagnostics and therapeutics on this innovative field. The ensemble of Nextflow features allows the Bioinformatics Team to transition without pain from a development stage, where pipelines are designed locally or on very small datasets, to a production phase where full datasets are processed with complete pipeline versions on the AWS cloud. A perspective on pipeline unit testing will be also presented, as a topic of possible broader interest for the Nextflow community.

**Bio**: Bioinformatics Head at Enterome Bioscience, with more than 14 years of experience in bioinformatics and with the management of bioinformatic teams across the fields of genomics, biotechnology and biomedicine. In my career I focused on the development of data analysis pipelines, data architecture strategies, and the application of computational methods to support and drive research projects and production platforms. I have more than 6 years of experience with metagenomics and computational microbiology to characterise single microorganisms and complex communities, including the human gut, soil and rumen microbiome.

## QCloud: A web-based quality control system for mass spectrometry-based proteomics laboratories

**Roger Olivella**, *Proteomics Unit, CRG, Spain*

[QCloud](http://qcloud.crg.eu) is a web-based system to support proteomics laboratories in daily quality assessment using a user-friendly interface, easy setup, automated data processing and archiving, and unbiased instrument evaluation. QCloud supports the most common targeted and untargeted proteomics workflows, it accepts data formats from different vendors and it enables a user-selected vocabulary to report incidences and annotate the acquired data.

#### Bio 

I graduated at the Universitat Autònoma de Barcelona in Physics. Then I worked as a software engineer in several research centers untill I started to work as a bioinformatician at the IRB in 2013. I finally moved to the Proteomics Unit at the CRG in 2015 until today.

## Exploiting orthology and de novo transcriptome assembly to refine target sequence information

**Julia Soellner**, *PhD student, Boehringer Ingelheim & University Tuebingen, Germany*

The ability to generate recombinant proteins facilitates several steps in drug discovery research, e.g. investigating drug-target-interactions or assessing a compound’s efficacy and safety. For this, the target’s exact protein sequence is required. Public databases such as Ensembl, UniProt and RefSeq are an important source of sequence information. However, many sequences for non-human organisms are predicted by computational pipelines and may thus be incomplete or contain errors. 
We present a Nextflow pipeline which exploits paired-end RNA-Seq reads for sequence validation and refinement by making use of sequence homology relationships across different species. We applied the pipeline to refine and validate the orthologues of all known human protein sequences in six species.

#### Bio 

I'm a bioinformatician by training and am currently in the second year of my PhD. My PhD project is conducted at Boehringer Ingelheim under the supervision of Prof. Kay Nieselt at University Tuebingen.
