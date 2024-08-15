Title: "Environmental drivers of the resistome across the Baltic Sea"
Author: "Joeselle Serrana"
Date: "3/27/2024"

---  
Source Data:

MS-Baltic-Sea-AMR_Analysis.zip                                   # Folder containing input data and R code for deownstream visualizations and analyses.
MS-Baltic-Sea-AMR_R-Codes.Rmd                                    # R scripts for the analyses: from input data processing to downstream analyses.

data/         
            data.xlsx                                            # Input file for analysis in R.
			
			              sheet: metadata                        # Sample information and environmental measurements.
			              sheet: motus							 # Relative abundance table of the microbial community based on mOTUs profiler (Supplementary Table S3 ).
			              sheet: arg						     # Antimicrobial resistance gene (ARG) data: Reads per kilobase million (RPKM) absolute counts (Supplementary Table S4).
			              sheet: mrg							 # Mobile resistance gene (MRG) data: RPKM absolute counts (Supplementary Table S5).
			              sheet: mge							 # Mobile genetic elements (MGE) data: RPKM absolute counts (Supplementary Table S6).
			              sheet: vfg							 # Virulence factor gene (VFG) data: RPKM absolute counts (Supplementary Table S7).

out/
            arg.mco; mrg.mco; mge.mco; vfg.mco; otu.mco          # Final microtable object containing: sample_table, otu_table, tax_table, taxa abundance(calculated for Type,Subtype,Subtype2,Reference), alpha diversity (calculated for Observed, Chao1, se.chao1, ACE, se.ACE, Shannon, Simpson, InvSimpson, Fisher, Pielou, and Coverage), and beta diversity (calculated for bray and jaccard)
---
Notes:

The major R packages needed for running the scripts are:

phyloseq; microeco                                               # Libraries for data manipulation, analysis, and visualization. Ecological analysis of microbiome data; visit https://github.com/ChiLiubio/microeco for more details
meconetcomp; ggraph; caret                                       # Libraries for network analysis, Grammar of graphics for relational data, and classification and regression training
ggplot2; ggradar; ggcor; ComplexHeatmap; aplot                   # libraries for data visualization
magrittr; ggh4x; dplyr; microViz; magrittr                       # Other packages needed.

Other packages for different processes (e.g., readxl, textshape, car, patchwork, etc.) also needs to be installed. If there is an issue dealing with the code send a message to joeselle.serrana@aces.su.se/joeselle.ms@gmail.com :)
