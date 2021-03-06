# edivColl
considering the implications of conserving for phylogenetic diversity vs evoutionary distinctiveness. Install using

`devtools::install_github('andrew-hipp/edivColl')`

If you stumble across this and
the package hasn't been published yet, I'm still trying out ideas, but don't
hesitate to write me with questions or thoughts.
At this point, my thought is that the package will include these functions:

1. Tree simulation and import? -- wrappers to TreeSim and ape, or just use of
  those directly
2. Bundler for trees and conservation interests matrix
3. Calculation of PD and ED metrics - wrappers at this point to
  a. evol_distinct function in phyloregion package
  b. vcv.phylo of ape (for _w_ of Hipp et al. 2018)
  b. phylogenetic diversity functions in picante
4. Resampling -- sampling additional taxa from a phylogeny based on
  (1) a 'consInt' object and range of sample sizes
  (2) a less constrained set of scenarios
  in which you assume a number of taxa within the collection, representing
  a range of PD or clades sampled, and a set (or variable) number of taxa
  you'd like to add. Ultimately, should allow for phylogenetic, geographic,
  fiscal or other constraints.
5. Visualizing resamplings -- takes a 'consPlan' as input;
  plots mean ED of inds added against PD of
  resulting community or mean ED of final community
6. Find sampling strategies. use a 'consInt' object, a criterion, and
  possibly other constraints to suggest sampling strategies.

and these data classes:

1. 'phylo' - Trees, just using ape
2. 'consInt' - Conservation interests - a matrix of spp with row names corresponding to
  phylogenetic tip labels, and columns "present" and "desired," either
  as binary or weights / absolute number of accessions; bundled with a phylo object
3. 'consPlan' - a tree, with a matrix of added taxa

... maybe. We'll see.
