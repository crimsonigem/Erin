# Harvard iGEM 2017 Week 2 (6/12 - 6/16)


## Software, Website, and Wiki Development

This week Hyeon-Jae and I decided to collaborate on the development of the gene circuit and flux model.

Our tentative plans for the summer moving forward was to make progress on the gene circuit, then to move on to the flux model next week.


### Gene Circuit Modeling

In the development of the gene circuit, we made several decisions to include and exclude certain variables.

**transcription rate**: decided to not factor into model since all the genes are under one operon. <br>
**translation rate**: need to find the appropriate RBS ratio for the various csg genes. <br>
**mRNA degredation**: decided not to factor into model since all the genes are under one operon and mRNA half life will be the same for all the factors. <br>
**protein degredation**: we had difficulty in finding accurate representations but considered making all of the half time the  same, thus excluding it from our model. <br>
**polymerization rate of csgA**: assuming that the polymerization rate is slow (especially since enucleation is a very slow process) we might not need to account for it since once csgA is exported, we no longer need to consider polymerization. <br>
**protein ratio**: from our research in the literature we decided to consider csgE and csgG as a blackbox (1:1 stoichiometric ratio) to simplify our calculation.
**rate of diffusion through csgGE**: we would need to measure this data experimentally, with various csgGE concentration with constant A concentration to see what is the best ratio. This would be an indirect measure of diffusion rate, but there is very little in the literature about concrete numbers. <br>
**rate of diffusion through sec complex**: similar to measuring diffusion through csgGE we would measure this indirectly via experimentation. <br>
**transcript polarity**: there was research done that suggests that we should only consider this if the cell is under stress. We are unsure to include it in the model, but as of now to simplify it we chose to exclude it. <br>

We must also consider the fact that we are not controlling the expression of sec complex, just the ratio of csgGE and csgA produced. Therefore it would always be a bottleneck in the "maximum exportation". There was some concern whether this would lead to accumulation of material, which could potentially polymerize and kill the cell. However we are also knocking out the other unnecessary secreted protein so our hope is that this would free up the previously "occupied" sec complexes so that this would not be an issue we would have to account for.


### Experimental Procedures

So overall in moving forward there are two main experiments we must conduct:

1. Measuring optimal csgGE and csgA concentration. This would be done by first holding csgA constant, and having variable csgGE expression. To see what would be the best concentration of each protein. There would be a secondary experiment of holding csgGE constant and increasing csgA concentration, and seeing if it matches the result of the first experiment (the ratio should be very similar, with a specified margin of error)

2. Seeing if having csgC is even necessary. We decided to exclude csgB and csgF in our model, and potentially in our E.coli strain because the two are involved in the polymerization of csgA outside the cell. However, since we are exporting high csgA outside the cell, we hope that the accessory proteins are not necessary. csgD is a master regulator which we also did not include in our construct. The role of csgC has not been clearly elucidated, however there is conflicting evidence if it has a significant role or not. Therefore whenever we have optimizing experimentation, we plan to always have two in parallel (one with csgC and one without) to see if there is a significant difference.

Once the model is completed, we will also have a comparative model with the starting E.coli strain and the "optimized" E.coli strain to measure the curli production.  

The experimental procedure we plan to use will be a modified Congo Red approach. We would make sure that the cell cultures had similar OD, as well as the appropriate RBS modifications. After allowing proliferation in a constant environment, we would measure relative rate in increased or decreased efficiency in curli production.

### Conclusion
These are the speculations of the variables we wanted to include in our final gene circuit model. In moving forward we would need to confirm our direction with our mentor (Francis Lee) as well as review the potential mathematical model that we have suggested. Ultimately since we are excluding many variables, we would need to measure curli production under the "optimized conditions" and see how it compares to the predicted values by the model to see if any adjustments are necessary.

Some unanswered questions we have are:
1. Do we have a constituitive or inducible promoter?
2. Are we only going to be using the RBS's from the iGEM registry?
3. Determining which barcode and kill switch we would like to implement.
4. Would the bottleneck of the sec pathway be a factor that would influence the viability of the E.coli strain in excess csgA production?
5. Which unncessary secretory proteins will we knock out in our cell?
