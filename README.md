# Task1
I have been given two plasmid sequence, so, using addgene plasmid map maker I can directly find out what are the components/gene is in it. From plasmid map, it was evident that it have 4 expressible gene and after doing BLAST following results were concluded. 

1. Interesting features/genes: - TEM-116 beta lactamase gene as a ampicillin resistant marker gene
                               - lactose operon repressor gene
                               - red fluorescent gene
                               - green fluorescent gene
    PDB file is attached in this repository (TEM-116 structure is not know yet, so I, using Modeller, did  homology modelling taking TEM-1 as a reference).
Primers are designed specific for GFP gene with 3' end ending with G/C 

2. Forward primer (19 nt) should be choosen from   5’CGCCGCAAACCCCGCCCCTGACAGGGCGGGGTTTCGCCGC3' and reverse primer (19 nt) can chosen from any position in GFP gene region, typically fragment length should be around 700 nt. 
Difficulty I faced in this was how to design forward primer. Out of 40 nucleotide, 28 nts were already found in control plasmid sequence (not at same region as in test plasmid) while remaining 12 nts, 6 on each end, were found in test plasmid only. So, if I cannot choose primer from middle of this sequence, it will be better to choose primer such that 3' end of primer is non binding to control plasmid 
sequence.  
   5'CAGGGCGGGGTTTCGCCGC3' (forward primer) (sequence taken from 5'-3' strand, coding strand)
   5'CCATGCCATGTGTAATCCC3' (reverse primer) (sequence taken from 3'-5' strand, non-coding strand)   
Further, did multiple sequence alignment to check if forward primer sequence is present in just expected region and reverse primer sequence is absent. Also, checked whether GC content is in between 40 to 60% (although for forward primer I didn't have any other option).
So, a band of size around 700 nt will be observed in agarose gel in case of cell colony containing test plasmid sequence, while in case of control plasmid there will be no band, apart from primer dimers.

3. From the plasmid map,
   5'CCTGATACAGAT3' pTrcHis_rev_primer; pBAD_rev_primer
   5'GGTCCTTCTTGAGTTTGTAAC3' GFP_F_primer
   5'GTTGTCCCAATTCTTGTTGAATTAGATGG3' GFP_R_primer

4. Plasmid is designed possibly to study the role of lacI gene in lac operon, i.e., how it affects the expression level of lacZYA gene, by measure the intensity of RFP/GFP signal. 

5. i)  Ampicillin resistant marker gene and origin of replication is pBR322. Ampicillin should be used as an antibiotic for positive selection.
  ii)  RFP and GFP is used a reporter protein here. Its signal can be measured by measuring the fluorescence intensity using flow spectrometry.
 iii)  placI is the inducible promoter used here. IPTG (analog of allolactose) can be used as an inducer chemical.
  iv)  A plot should be made between GFP/RFP signal level and IPTG concentration. When IPTG is present in system, then signal level of GFP/RFP should be very less, while when IPTG is absent or very less in system then GFP/RFP signal level should be high.
       
# Task2
I am more comfortable using R for data visualization and analysis, hence, did this task in R. Same algorithm can be used in python to get the same results

2. Image segmentation techniques can be used to measure the areas at different times and thus time traces of the pulsatile activity. Edge detection using computer vision and other segmentation algorithms can be used, apart from that we can use various deep learning techniques. 

3. I have upload jupyter notebook named as timeTraces.ipynb. Plot has been made betweeen area vs frame and area vs time. Gaps in oscillation was found.

4 & 5. In this, I faced difficulty in finding peak's coordinate, but I kept trying and at the end I got success. Jupitype file named as 
       IPI_code.ipynb is in repository.
       
Based on the plots obtained, it is clear that Jellyfish sleep. Taking plot 1 as an example, we can see continous pulses during daytime, but during night time gaps in pulsation were observed which shows quiescence stage. Also, number of pulses were more
during daytime as compared to nighttime . Similaraly, these results can be extrapolated for other jellyfishes.

Time trace followed Autoregression time series as there was seasonility and no trend was observed. Also, y(t+1) was found to depend on 
previous values. Its algorithmic implementation is already shown in IPI_code.ipynb file. From the plot between y(t+1) and y(t) we can see that there is some correlatation (autocorrelation), hencce, autoregression.

I have also uploaded all the results file in folder named Results.






