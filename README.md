# wheat-biostimulant-metabolome

Companion repository for the paper "**Microbial biostimulants shape metabolite profiles of grains of hydroponic indoor wheat**" 

by: **Sebastian Eichelsbacher**1 & **Stefanie Thaqi**2, Francesco Orsini3, Golia Roshani3, Afsaneh Nematpour3, Gerd Patrick Bienert4, Thomas D Alcock4,8, Corinna Dawid5, Gionata Martinazzoli5, Timo D Stark5, Srotoswini Joardar6, Michael Schloter2,7, Senthold Asseng1, **Stefanie Schulz**7,*

1-Technical University of Munich, TUM School of Life Sciences, Department of Life Science Engineering, Digital Agriculture, HEF World Agricultural Systems Center, Freising, Germany
2-Technical University of Munich, School of Life Sciences, Chair of Environmental Microbiology, Freising, Germany
3-University of Bologna, Department of Agricultural Sciences, Bologna, Italy
4-Technical University of Munich, TUM School of Life Sciences, Department of Molecular Life Sciences, Crop Physiology, Freising, Germany
5-Technical University of Munich, School of Life Sciences, Food Chemistry and Molecular Sensory Science, Freising, Germany 
6-Technische Universität München, TUM School of Life Sciences, ZIEL - Institute for Food & Health, Freising, Germany
7-Helmholtz Zentrum München, Research Unit Comparative Microbiome Analysis, Neuherberg, Germany
8-Technical University of Munich, TUM School of Life Sciences, Department of Molecular Life Sciences, Emmy Noether Group Plant Micronutrient Physiology, Freising, Germany

*Correspondence: stefanie.schulz@helmholtz-munich.de

**_This repository contains:_**
1. **Amplicon pre-processing.Rmd** - script used for downstream processing and quality filtering of ASV data following Galaxy-based preprocessing to ultimately generate a phyloseq object
2. **Stats and analysis.Rmd** - script used for downstream microbiome analyses reported in the manuscript using CSS-normalized phyloseq object generated using 'Amplicon pre-processing.Rmd' script
3. **metadata_wini.xlsx** - metadata file used in the 'Amplicon pre-processing.Rmd' script containing all the information about variables, timepoints, etc.
4. **Galaxy output files.zip** - zip file containing all the raw ASV count tables and taxonomic anotation tables generated during the Galaxy worflow that were used in the 'Amplicon pre-processing.Rmd' script

**Experimental setup and description:**
Dwarf wheat (_Triticum aestivum_ cv. Apogee) was grown under controlled hydroponic indoor conditions to investigate how targeted microbiome inoculation influences plant performance and metabolic profiles. The plants were inoculated with _Bacillus velezensis_ FZB42 (Bacillus treatment), _Pseudomonas_ sp. RU47 (Pseudomonas treatment), an equiproportional mix of both the bacterial strains (Mix treatment), a heat-inactivated form of the Mix tratment (Autoclaved treatment), or left untreated (Control). Root samples collected during plant development were used to assess microbial colonization and community dynamics, while harvested samples were analyzed for yield traits, nutrient composition, and untargeted metabolomic profiles.This setup enabled evaluation of microbiome-driven modulation of wheat chemical phenotypes under optimized vertical farming conditions.

DNA was extracted using a phenol–chloroform extraction protocol (Lueders et al., 2004; Stempfhuber et al., 2017). For amplicon sequencing, 10 ng of extracted DNA was used for amplification of the V3–V4 region of the 16S rRNA gene using chloroplast-exclusion primers 335f (5′-TCGTCGGCAGCGTCAGATGTGTATAAGAGACAGCADACTCCTACGGGAGGC-3′) and 769r (5′-GTCTCGTGGGCTCGGAGATGTGTATAAGAGACAGGATCCTGTTTGMTMCCCVCRC-3′), following Estendorfer et al. (2017). Purified DNA was normalized to 4 nM and sequenced on an Illumina MiSeq platform using the MiSeq Reagent v3 (600-cycle) kit. Raw sequencing data were processed through the European Galaxy server, where reads were quality filtered, denoised, and assigned taxonomically against the SILVA database (version 138.2). 

The raw sequencing data are available in the NCBI Sequence Read Archive (SRA) under BioProject PRJNA1406503.
