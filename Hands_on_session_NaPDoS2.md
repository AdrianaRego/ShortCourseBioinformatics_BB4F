# Hands-on session NaPDoS2
This exercise corresponds to a tutorial example from the NaPDoS2 [documentation](https://npdomainseeker.sdsc.edu/napdos2/np2_documentation.pdf).

# Genome tutorial objective
Analyze a single bacterial genome Salinispora tropica CNB-440 to uncover the unique salC KS domain, which clades separately from other KS domains and thus likely represents a novel biosynthetic class of KS as reported in [Bauman et al. Nat Chem Biol. 2022](https://pmc.ncbi.nlm.nih.gov/articles/PMC9058210/)

![image](https://github.com/user-attachments/assets/565df2a7-240c-4553-a352-5950f2f7348e)

# 1 - Start by downloading the Salinispora tropica CNB-440 genome
  [Salinispora tropica CNB-440 genome](https://github.com/AdrianaRego/ShortCourseBioinformatics_BB4F/blob/main/GCF_000016425.1_ASM1642v1_genomic.fna). 
 
# 2 - Open NaPDoS2 and navigate to the “Run Analysis” tab

Select “Domain Type: KS domains”. Since we are analyzing the Salinispora tropica CNB-440 “GCF_000016425.1_ASM1642v1_genomic.fna”: nucleic acid FASTA genome file, select “Query type: Nucleic acid sequences”. 
Click “Choose File” to upload your genome file.  
Click on “Advanced Settings”. Here, you can change the BLASTP e-value cutoff and the Minimum alignment length. For this tutorial, we will use the default settings of BLASTP e-value cutoff of 1e-8 and Minimum alignment length of 200aa (600nt).

Click SEEK to be assigned a job ID and review the job analysis settings.

For “Query type: nucleic acid sequences”, you will first proceed to the “Nucleotide Sequence Search Results” page which lists the initial number of KS domains that NaPDoS2 identified. On this page, you can DOWNLOAD (click to view, right click & save as to save the table) a table of the nucleotide match locations in tab-delimited format.

This lists the domains numbered KS# (“domain id”), the sequence/contig name the domain was found on (“parents seq”), the base pair/nucleotide start and end location of the domain (“start” , “end”), the translation reading frame (“read frame”), and the final name of the domain (“cand_id”).

This table can be used to find the location of the KS domains in your nucleic acid genome file via the starting and ending base pairs.
 
To continue the analysis, click “CONTINUE ANALYSIS”
 
# 3 - Select results display options for KSs that NaPDoS2 detected and classified

The “Domain Classification Summary” page lists the total number of domains found from the number of sequences that were input. Clicking “VIEW ALL
MATCHES” opens a new page with the hit table of all domains identified in the genome analysis.

In our example, 28 KS domains were found from the nucleic acid Salinispora tropica CNB-440 genome.

The “Individual Domain Classes” lists the number of specific classes of KS domains that were found in your query genome sequence, ordered by the class and subclass with the most number of domains.
This is helpful if you only are interested in a specific subset type of domain– you can click to select what class/subclasses you would like to
view the results of and click “VIEW A SUBSET”, which will open a new page with a table of only the classes/subclasses you selected.
You can also “DOWNLOAD” the “Individual Domain Classes” table (click to view, right click and save as to download).

# 4 -  Assess and download NaPDoS2 search results
If you clicked “VIEW ALL MATCHES” or “VIEW A SUBSET”, you will view the “Database Search Results” page, either for all hits in your query sequence or for a subset of hits of certain class/subclass that you selected.
The table can be sorted by each of the column values by clicking on the column header; the table scrolls up and down and if your query hit names are long, the table scrolls left to right. You can DOWNLOAD the results table (right click, save as to download; click to view) in a tab-delimited format.

The scrollable table lists the following information:
 cand_id: name of the domain hit, which is the name of the sequence in the query FASTA file before spaces and appended with location
information of where the domain hit was found

database match: the name of the domain in the NaPDoS2 database that the query hit is closest to

names include: BGCname_KS#_uniquetag
 BGC name: name of the BGC
 KS#: number KS in successive order from the BGC
 unique tag: abbreviation that is unique for every class/subclassification

percent identity: percent identity that the query hit shares with the closets NaPDoS2 database match
align length: alignment length that the query hit shares with the closest NaPDoS2 database match
e-value: e-value of the query hit to the closest NaPDoS2 database match
BGC match: name of the BGC of the closest NaPDoS2 database match to the query hit; click on the link to open a new page of the BGC card information
domain class: classification of the closest NaPDoS2 database match to the query hit - This is the classification of your query hit
domain subclass: specific subclass of the closest NaPDoS2 database match to the query hit -  This is the complete specific subclass of your query hit (some classes do not have subclasses, ie “no subclass”)

Here, you can also select specific domain hits to download or further analyze (select all to download or analyze all results). You have the follow options for downloading the data:
  View nucleotide coordinates for all trimmed domain candidates
 This shows a table where each potential domain candidate has been given a unique candidate ID number, based on parent sequence id, reading frame number (1-6), gene number within the reading frame, and trimmed nucleotide start and stop coordinates within the reading frame.

The table columns are sortable by each column header. You can DOWNLOAD the table of nucleotide match locations in tab-delimited format (click to view, right click to save as and download)

Output selected sequences in fasta format
● Select which trimmed query domain hits or select all to output inFASTA format


●  GET TRIMMED SEQS
This is a very useful output for you to continue working with the KS or C domains that NaPDoS2 detected & classified. You can copy
and paste the trimmed query KS or C domain hits into a new file, a sequencing editing program, etc.

# 5 - Output Alignment with closest database matches
Select alignment format (all alignments are created with MUSCLE as described here, but the alignment can be output in different
formats suitable for many downstream applications):
○ FASTA (.fasta)
○ Msf (.msf)
○ Clustalw (.clw)

This outputs an alignment of your selected sequences with the closest NaPDoS2 database matches. Note, the alignment output
will include all closest NaPDoS2 database matches to all query hits, not just your selected sequences, but only your selected
sequences will be present in the alignment.
You can DOWNLOAD (click to view, right click to save as) the alignment file for downstream use in sequence programs, etc.

# 6 -  Construct tree (candidate domains + blast matches + reference domains)
Select the query domain hits that you would like to build a tree with. You can either build a tree with: 
● Closest database matches to your selected sequences, ie. - of selected queries + closest database references
● All classified KS domains which would be the # of selected queries + all 414 NaPDoS2 database reference sequences.
● The estimated time to calculate the trees is given, usually the time to complete the trees is much faster than estimated.


# 7 - Constructing a tree to estimate biosynthetic novelty of domain hits
● Our goal of this tutorial was to find the salinosporamide biosynthetic KS domains in Salinispora tropica CNB-440 and assess how closely related it is to other biosynthetically characterized KSs in the NaPDoS2 database.
Therefore, searching through the table, we see that there were 2 hits to the “salinosporamide_KS01_cisloading” and “salinosporamide_KS02_cisHybridKS”
domains in our genome. We will select these 2 sequences to construct a tree.

■ By clicking on the “salinosporamide” BGC, we can see that the salinosporamide BGC has 3 domains in the NaPDoS2 database, and by clicking the MIBiG ID that links to the complete BGC, we can see that the BGC only has these 3 domains. We are interested in the two KS domains.

We want to put these 2 query KS domain hits into the context of the entire NaPDoS2 reference database. We’ll select the second option of building a tree with our query hits and all classified KS domains.

The Tree results page has two options for viewing the calculated trees:
■ Tree image (SVG format file), click DOWNLOAD to view, right click to save.
● When viewing the tree, the query domain hits will have red circles of where they are placed in the tree.
■ Newick format (plain text file), click DOWNLOAD to view, right click to save
● This file format can be viewed in tree viewing programs like FigTree, iTol, TreeViewer, ETE Toolkit, etc.


