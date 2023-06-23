# Paper structure
Patient-specific Boolean models of signalling networks guide personalised treatments
Additional files at page 24.
Appendix at page 31.

## Prostate Boolean model construction
Results: 3

Appendix: 31

## Prostate Boolean model simulation
Results: 6

Appendix: 36

## Personalisation of the prostate Boolean model
Results: 6

Appendix: 37

## Personalised drug predictions of TCGA Boolean models
Results: 7

Appendix: 39

## Personalised drug predictions of LNCaP Boolean model
Results: 9

Appendix: 41

## Experimental validation of predicted targets
Results: 10

Appendix: 42

## Experimental validation of drugs in LNCaP
Results: 12

Appendix: 43

# Software

## Initial generic network extension
ROMA
OmniPath

## Regulatory graph construction
GINsim

## Datasets
TGCA
GDSC

## Network visualization
Cytoscape

## Model simulation
MaBoSS

# Questions
- Do I have to reproduce also each intermediate passage, e.g. to recreate the network on GINsim and export the file to Cytoscape for better formatting? Or can I start fomr the ZGINML file provided in supplementary files. I can start from the ZGINML file, no need to reproduce the heavy and long parts of the paper.
- Do we need to know all the biological aspects (e.g. each pathway) or few examples are sufficient? No, few examples are sufficient, I can even study only few examples from my experimentations and not fromt the paper itfself.
- Is it sufficient to send the work by email?
- Node "SPOP" is source of four edges with negative effects in the supplied network, but in the Excel file "Montagud2022_interactions_sources.xlsx", of these four intercations only three have sign "-" and one has sign "+". Is it correct or are there errors between the file and the network? There is an error in the Excel file, the correct data derive from logical rules and the BND and ZGINML files are good to use.
- In section 2.2 there is a reference to figure in Appendix 1 as showing the outputs of the wild type simulation of the model. However, this figure represents only an example of the interactions of gene HSP90AA1. This error occures for all the figures referenced in this section, which seem to be referred to figure 3 in the main text instead. Indeed, the correct reference is figure 3 in the main text.
- Another wrong reference is to Appendix 1 - figure 4A and Appendix 1 - figure 4B in the caption of Appendix 1 - figure 36. Same for figures referenced in the caption of Appendix 1 - figure 38. The correct figures are in main text figure 5.
- Is it necessary to study and describe the PROFILE methodology or can I skip the theoretical part and just use the data to reproduce the plots? I can avoid talking about PROFILE methodology, just explain why they use it.

# Keywords
- wild type
- PROFILE
- LNCaP
- Copy Number Alteration (CNA)

# Notes
- Outputs of the MaBoSS simulation are also referred as "phenotypes" because they are common biological phenotypes associated to the development of prostate cancer.

# Release
- Reorganize the notebook such that the code is collected in a single section at the the end of every section, preceded by a Markdown description of what is done. Treat the code section as a Python source file, e.g. add comments when needed.
- Make platform independent the paths (e.g. define PATH_OUT = '.').
- Substitute string """ with character backtick.
- Use [nbconvert](https://nbconvert.readthedocs.io/en/latest/) from command line because it does not work in the Jupyter GUI. This is essential to remove the cells with tag remove-cell, which is not done properly through the GUI.
