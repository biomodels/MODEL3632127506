# MODEL3632127506: Jablonsky2008_kinetic_model_of_dimeric_PSII

## Installation

Download this repository, and install with distutils

`python setup.py install`

Or, install using pip

`pip install git+https://github.com/biomodels/MODEL3632127506.git`

To install a specific version (in this example, from the 2014-09-16 BioModels release)

`pip install git+https://github.com/biomodels/MODEL3632127506.git@20140916`


# Model Notes


This is a kinetic model of the dimeric photosystem II (PSII).  
The model has partially based on the earlier model used for simulation of the
flash-induced period-four damped oscillation of oxygen evolution and
chlorophyll fluorescence (Jablonsky J and Lazar D (2008) Biophys J, 94:
2725-2736 pubmedID: [18178650](http://www.ncbi.nlm.nih.gov/pubmed/18178650) ).
For short description of reactions and initial concentrations, see the notes
in the model file. For explanation of the value of the rate constants, see:
Lazar D (2003) J. theor. Biol. 220:469-503 pubmedID:
[12623282](http://www.ncbi.nlm.nih.gov/pubmed/12623282) ; Jablonsky J and
Lazar D, 2008 Biophys J, 94: 2725-2736 pubmedID:
[18178650](http://www.ncbi.nlm.nih.gov/pubmed/18178650) and Jablonsky, Susila
and Lazar, 2008, DOI: 10.1093/bioinformatics/btn530 pubmedID:
[18845578](http://www.ncbi.nlm.nih.gov/pubmed/18845578) ).  
In this model the hypothetic cooperation in the water splitting is considered
as the cross-backward-oxidation of the P680 (in the PSII which is already in
the S2-state) by [YZoxS1] (in the PSII in which the S1-S2 transition is not
finished). The cooperation (between compartment1 = 1st PSII and compartment2 =
2nd PSII) is the best explanation of the second turnover of PSII induced by
short flashes which is available now. We concluded that the double turnover of
the PSII induced by short flashes is caused either by the cooperation in the
water splitting or our knowledge of the main pathway of the electron transport
through the PSII is incomplete and besides D1-Y161, other cofactor which
enables oxidation of the special chlorophyll pair (P680), e.g., L-Y34, must be
considered.  
The oxygen signal in the model is defined as a maximum of the sum of
concentrations of the model forms in the iS3Yp-state (handled in MATLAB). This
version of model cannot be used for simulation of the chlorophyll fluorescence
because for simplicity the reactions behind the loss of excited state are not
considered.  
The meaning of the particular letters in the model is as follows: P – P680
(special chlorophyll pair), H – pheophytin, A – QA (the first quinone electron
acceptor), B – QB (the second quinone electron acceptor), PQ – oxidized
plastoquinone molecules in the PQ pool, PQH – reduced and protonated PQ
molecules in the PQ pool, Y/Yp – reduced/oxidized state of tyrosine 161-D1,
YD/YDox – reduced/oxidized state of tyrosine 160-D2, Sn (n = 0, 1, 2, 3) – the
S-states of oxygen evolving complex (OEC), iSn (n = 0, 1, 2, 3) – the
intermediate S-states of OEC.  
All reactions describing electron transport through PSII entered into the
model are assumed to be first order reactions with respect to one reactant and
are defined as mass action reactions. Cooperation between photosystem II
within dimer in the water splitting is described by the second order kinetics.
This approach shows that the second order kinetics used for description of
oxidation of the tyrosine D1-Y161 in the multi-units PSII model can be in this
case justified.

two compartments => two photosystems II connected by cooperation in the water
splitting

initial conditions:

S1=100%,

YDox=89%

PHABm = 0.25

PHAB = 0.75

list of reactions (compartments 1 and 2):

R1-R144 ... excitation

R145- R180... charge separation_open

R181- R216... charge separation_closed

R217-R324 ... charge stabilisation

R325-R360 ... recombination PpHm (P680+pheophytin-)

R361-R396... recombination PpAm (P680+QA-)

R397-R399 ... recombination S2Am (S2-state of OEC and QA-)

R400-R471 ... electron transfer from QA to QB

R472-R543 ... electron transfer from QA to QB-

R544-R687 ... exchange of double reduced QB by free plastoquinone molecule
from the PQ pool

R688 ... Ox/red PQ and PQH

R689-R700 ... reduction of Pp by Yz in S0

R701-R712 ... reduction of Pp by Yz in S1

R713-R724 ... reduction of Pp by Yz in S2

R725-R736 ... reduction of Pp by Yz in S3

R737-R784 ... formation of the intermediated S-states iS0,1,2, 3

R785-R832 ... electron donation from OEC to YZox during the S0->S1, S1->S2,
S2->S3, S3->S0 transitions (Kok cycle)

R833-R850 ... YD oxidation by S3/S2 state of OEC; YDox reduction by S0 state
of OEC

R1701-R1750 ... cooperation between 1st and 2nd PSII

This model originates from BioModels Database: A Database of Annotated
Published Models (http://www.ebi.ac.uk/biomodels/). It is copyright (c)
2005-2011 The BioModels.net Team.  
To the extent possible under law, all copyright and related or neighbouring
rights to this encoded model have been dedicated to the public domain
worldwide. Please refer to [CC0 Public Domain
Dedication](http://creativecommons.org/publicdomain/zero/1.0/) for more
information.

In summary, you are entitled to use this encoded model in absolutely any
manner you deem suitable, verbatim, or with modification, alone or embedded it
in a larger context, redistribute it, commercially or not, in a restricted way
or not..  
  
To cite BioModels Database, please use: [Li C, Donizelli M, Rodriguez N,
Dharuri H, Endler L, Chelliah V, Li L, He E, Henry A, Stefan MI, Snoep JL,
Hucka M, Le Novère N, Laibe C (2010) BioModels Database: An enhanced, curated
and annotated resource for published quantitative kinetic models. BMC Syst
Biol., 4:92.](http://www.ncbi.nlm.nih.gov/pubmed/20587024)


