This will be a brief evaluation of a series of steps that would be taken to use sequencing data to answer a question of interest.

Generally speaking, it will require sequencing data to be found, aligned and visualized. The total dataset should be < 4GB and can be easily run on a desktop or laptop.

**Step 1.** Find and download the T2T reference genome. As a sanity check, it should be have a prefix like hs1
- I recommend using UCSC
- I recommend unzipping it (should be about 3GB)
- What is this genome? What is special about it?

**Step 2.** Download reads. I am interested in individual HG002 and only interested in reads on chromosome 5 positions 1-1000000. This individual has many datasets made available though Genome in a Bottle but I'm only interested in Pacbio HiFi reads (also called CCS).
- Find the URL to the right dataset through the Genome in a Bottle ftp site
- HG002 is the son of a well-studied Ashkenazim Trio family
- the correct path on the ftp site should end in PacBio_SequelII_CCS_11kb/HG002_GRCh38
- you can use the following command to download a subset of reads without downloading the entire massive file \
`samtools view -b -h https://xxx.bam chr5:1-1000000`

**Step 3.** Install `pbmm2`. Realign the reads you just downloaded to the T2T genome

**Step 4.** Install `IGV`. Load in the T2T reference genome. Load in the reads you just aligned to visualize them
- the T2T reference is a "hosted genome" in IGV 

**Step 5.** We are interested in the region around the genes _TPPP_ and _ZDHHC11_ (approx chr5:676,500-786,200)
- take a screenshot of this region and send it to me
- bonus points: explain what's happening here????
