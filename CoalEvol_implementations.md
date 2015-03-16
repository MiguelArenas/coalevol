# Introduction #

`CoalEvol` allows the simulation of molecular data and multiple complex evolutionary histories and substitution models.


# Details #

`CoalEvol` can simulate coalescent histories with:

- Recombination (including hotspots (1) and intracodon recombination (2))
- Population structure and several migration models (island (3), stepping-stone (4) and continent-island (5)). Indeed, migration rates may vary with time.

- Population/species tree can be introduced by the user.

- Demographics. Population size may change according to a growth rate or by temporal periods user-defined.

- Samples can be simulated at same time or at different times (temporal longitudinal sampling or tip dates) (see, 6).

- Alternatively to the coalescent simulation, user-specified trees can be directly introduced in `CoalEvol`.

Then, `CoalEvol` can evolve nucleotide, codon and amino acid data along the simulated coalescent tree or the user-introduced phylogenetic tree:

- Nucleotide data. All nucleotide substitution models are implemented, such as JC (7), HKY (8) and GTR (or REV) (9). Moreover, the non-reversible GTR (GTnR) is also implemented.

- Codon data. `CoalEvol` implements a large variety of codon models: GY94 (10) x heterogeneous synonymous/nonsynonymous ratio rate (dN/dS or ω) M1-M10 models (11, 12) x any nucleotide model. Moreover, dN/dS may also change per branch (e.g., 13). Physicochemical contributions of the derived amino acids can be also considered (see, 14). MG94 (15) x any nucleotide model (see, 16). HB codon models (17). Empirical codon models (18, 19).

- Amino acid data. `CoalEvol` evolves amino acid data under multiple substitution models, namely Blosum62 (20), CpRev (21), Dayhoff (22), DayhoffDCMUT (23), HIVb (24), HIVw (24), JTT (25), JonesDCMUT (23), LG (26), Mtart (27), Mtmam (28), Mtrev24 (29), RtRev (30), VT (31), WAG (32) and any user-defined model.

In addition, for all these models:

- Nucleotide, codon or amino acid frequencies may vary across sites by user-specified categories (CAT models) (33).

- Haploid and diploid data can be simulated.

- Heterogeneity (+G) can be applied across sites (see `SGWE` for variable +G across genomic regions)
- Proportion of invariable sites (+I).


`CoalEvol` ouputs:

- The simulated coalescent trees (newick format), including the tree for each recombinant fragment.

- The simulated ancestral recombination graph (ARG) (34) (branches format (35)).

- Recombination breakpoints.

- Simulated alignments can be printed in phylip, fasta and nexus formats.

- Codon models with variable dN/dS across sites and/or branches allow print the simulated dN/dS per site and/or branch.

- Ancestral sequences (GMRCA and sumMRCA (see, 2, 36)).

- Other information. Statistics for substitution events (synonymous and nonsynonymous for codon models), recombination events (including intracodon recombination for codon models) and migration events. Times to the MRCA and GMRCA. Comparisons with the expected values.




# References #

1.	Wiuf C, Posada D: A coalescent model of recombination hotspots. Genetics 2003, 164(1):407-417.

2.	Arenas M, Posada D: Coalescent simulation of intracodon recombination. Genetics 2010, 184(2):429-437.

3.	Hudson RR: Island models and the coalescent process. Mol Ecol 1998, 7:413-418.

4.	Kimura M, Weiss GH: The Stepping Stone Model of Population Structure and the Decrease of Genetic Correlation with Distance. Genetics 1964, 49(4):561-576.

5.	Wright S: Evolution in Mendelian populations. Genetics 1931, 16:97-159.

6.	Navascues M, Depaulis F, Emerson BC: Combining contemporary and ancient DNA in population genetic and phylogeographical studies. Mol Ecol Resour 2010, 10(5):760-772.

7.	Jukes TH, Cantor CR: Evolution of protein molecules. In: Mammalian Protein Metabolism. Edited by Munro HM. New York, NY: Academic Press; 1969: 21-132.

8.	Hasegawa M, Kishino K, Yano T: Dating the human-ape splitting by a molecular clock of mitochondrial DNA. J Mol Evol 1985, 22:160-174.

9.	Tavaré S: Some probabilistic and statistical problems in the analysis of DNA sequences. In: Some mathematical questions in biology - DNA sequence analysis. Edited by Miura RM, vol. 17. Providence, RI: Amer. Math. Soc.; 1986: 57-86.

10.	Goldman N, Yang Z: A codon-based model of nucleotide substitution for protein-coding DNA sequences. Mol Biol Evol 1994, 11(5):725-736.

11.	Anisimova M, Bielawski JP, Yang Z: Accuracy and Power of the Likelihood Ratio Test in Detecting Adaptive Molecular Evolution. Mol Biol Evol 2001, 18(8):1585-1592.

12.	Yang Z, Nielsen R, Goldman N, Pedersen A-MK: Codon-substitution models for heterogeneous selection pressure at amino acid sites. Genetics 2000, 155:431-449.

13.	Dutheil JY, Galtier N, Romiguier J, Douzery EJ, Ranwez V, Boussau B: Efficient selection of branch-specific models of sequence evolution. Mol Biol Evol 2012, 29(7):1861-1874.

14.	Wong WS, Sainudiin R, Nielsen R: Identification of physicochemical selective pressure on protein encoding nucleotide sequences. BMC Bioinformatics 2006, 7:148.

15.	Muse SV, Gaut BS: A likelihood approach for comparing synonymous and nonsynonymous nucleotide substitution rates, with application to the chloroplast genome. Mol Biol Evol 1994, 11(5):715-724.

16.	Pond SK, Muse SV: Site-to-Site Variation of Synonymous Substitution Rates. Mol Biol Evol 2005, 22(12):2375-2385.

17.	Holder MT, Zwickl DJ, Dessimoz C: Evaluating the robustness of phylogenetic methods to among-site variability in substitution processes. Philos Trans R Soc Lond B Biol Sci 2008, 363(1512):4013-4021.

18.	Kosiol C, Holmes I, Goldman N: An empirical codon model for protein sequence evolution. Mol Biol Evol 2007, 24(7):1464-1479.

19.	Schneider A, Cannarozzi GM, Gonnet GH: Empirical codon substitution matrix. BMC Bioinformatics 2005, 6:134.

20.	Henikoff S, Henikoff JG: Amino acid substitution matrices from protein blocks. Proc Natl Acad Sci U S A 1992, 89(22):10915-10919.

21.	Adachi J, Waddell PJ, Martin W, Hasegawa M: Plastid genome phylogeny and a model of amino acid substitution for proteins encoded by chloroplast DNA. J Mol Evol 2000, 50(4):348-358.

22.	Dayhoff MO, Schwartz RM, Orcutt BC: A model of evolutionary change in proteins. In: Atlas of protein sequence and structure. Edited by Dayhoff MO, vol. 5, Suppl. 3. Washington D. C.; 1978: 345-352.

23.	Kosiol C, Goldman N: Different versions of the Dayhoff rate matrix. Mol Biol Evol 2005, 22(2):193-199.

24.	Nickle DC, Heath L, Jensen MA, Gilbert PB, Mullins JI, Kosakovsky Pond SL: HIV-specific probabilistic models of protein evolution. PLoS One 2007, 2(6):e503.

25.	Jones DT, Taylor WR, Thornton JM: The rapid generation of mutation data matrices from protein sequences. Comput Appl Biosci 1992, 8(3):275-282.

26.	Le SQ, Gascuel O: An improved general amino acid replacement matrix. Mol Biol Evol 2008, 25(7):1307-1320.

27.	Abascal F, Posada D, Zardoya R: MtArt: A New Model of Amino Acid Replacement for Arthropoda. Mol Biol Evol 2007, 24(1):1-5.

28.	Yang Z, Nielsen R, Masami H: Models of amino acid substitution and applications to mitochondrial protein evolution. Mol Biol Evol 1998, 15(12):1600-1611.

29.	Adachi J, Hasegawa M: MOLPHY version 2.3: programs for molecular phylogenetics based in maximum likelihood. Comput Sci Monogr 1996, 28:1-150.

30.	Dimmic MW, Rest JS, Mindell DP, Goldstein RA: rtREV: an amino acid substitution matrix for inference of retrovirus and reverse transcriptase phylogeny. J Mol Evol 2002, 55(1):65-73.

31.	Muller T, Vingron M: Modeling amino acid replacement. J Comput Biol 2000, 7(6):761-776.

32.	Whelan S, Goldman N: A general empirical model of protein evolution derived from multiple protein families using a maximum-likelihood approach. Mol Biol Evol 2001, 18(5):691-699.

33.	Lartillot N, Philippe H: A Bayesian mixture model for across-site heterogeneities in the amino-acid replacement process. Mol Biol Evol 2004, 21(6):1095-1109.

34.	Griffiths RC, Marjoram P: An ancestral recombination graph. In: Progress in population genetics and human evolution. Edited by Donelly P, Tavaré S, vol. 87. Berlin: Springer-Verlag; 1997: 257-270.

35.	Arenas M, Patricio M, Posada D, Valiente G: Characterization of phylogenetic networks with NetTest. BMC Bioinformatics 2010, 11(1):268.

36.	Arenas M, Posada D: The effect of recombination on the reconstruction of ancestral sequences. Genetics 2010, 184(4):1133-1139.