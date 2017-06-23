# Harvard iGEM 2017 Week 3 (6/19 - 6/23)


## Procedural Development: Datsenko-Wanner

In order to optimize the amount of resources devoted to the curli mechanism, we investigated whether extraneous proteins naturally produced by *E.coli* could be knocked out without loss of vitality.

We developed a rough list of potential parts to knock out, which will undergo careful screening and filtering in the following weeks. Meanwhile I familiarized myself with various knockout techniques in order to produce our optimized strain and decided upon the Datsenko-Wanner (2000) procedure.

![alt text](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC18686/bin/pq1201632001.jpg)

Image courtesy of: <br>
**One-step inactivation of chromosomal genes in *Escherichia coli* K-12 using PCR products** <br>
Proc Natl Acad Sci U S A. 2000 Jun 6; 97(12): 6640–6645.

Step 1. Amplify antibiotic resistance gene, with primers that have been extended to include some nucleotides next to the gene of interest. In the figure, H1 and H2 correspond to the region next to gene B. The forward primer would have H1 attached to the beginning, and the reverse primer would have H2 attached to its end.

Step 2. Transform the bacteria with a plasmid containing lambda red recombinase. The recombinase will switch the antibiotic resistance gene with the gene of interest.

Step 3. The successfully recombined bacteria can be detected since they will be antibiotic resistance.

Step 4. Since the antibiotic resistance gene originally had FRT cut sites flanking it, you can remove the resistance using the FRT enzyme.

### Steps Moving Forward ###
In moving forward with our project, the next steps would be to design the appropriate primers for the selected regions of interest.

Procedural specifications can be found [here](http://www.openwetware.org/wiki/Recombineering/Lambda_red-mediated_gene_replacement)

## Procedural Development: screening

We also finalized on the experimental steps in order to determine the best ratio of translation of csgA, csgE, csgG, and csgC.

Accoring to the paper, **Precise and reliable gene expression via standard transcription and translation initiation elements**, we can precisely control the rate of translation by varying the attached RBS to the genes of interest.

Our basic strategy is as follows:

1. Keeping E, G, C, and sec at medium expression, maximize A production without interfering with cell viability.
2. Minimize G, E, C, and sec in succession, each time finding the threshold for cell viability. Repeat step two to make sure the minimum has been reached in expression level.

Gathering the experimental data for this will provide us information for better development of our gene circuit model, which will hopefully allows us to predict the cell's ability to produce csgA in response to variables in the future.  

## Knockout Parts ##
In collaboration with Hyeon-Jae, we made a list of potentially 20-30 parts that could be knocked out in our laboratory strain of *E. coli*.

Some criteria for selection include: <br>
1. Related to endo or exotoxin
2. Cell to cell signaling - since we do not necessarily need our cells to communicate with each other, just maximize rates of csgA production
3. The transmembrane pores for the specified toxins or signaling molecules

Further calibration of the list is to be followed.
