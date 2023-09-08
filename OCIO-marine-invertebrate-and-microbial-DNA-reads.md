Dataset title: Labeled marine invertebrate and microbial DNA reads
Dataset curator: Jennifer Spillane, PhD, Smithsonian Institution Data Science Lab, Office of the Chief Information Officer
Dataset version: 1.0, 1-4-23
Dataset citation and DOI:
Data statement author: Jennifer Spillane, PhD, Smithsonian Institution Data Science Lab, Office of the Chief Information Officer
Data statement citation: authors, date, title, version, institution, and URL or DOI.

##Dataset Summary
This dataset was designed as a training dataset for machine learning approaches to DNA decontamination, particularly for invertebrate animal lineages, for which decontamination is very difficult. It is composed of DNA sequencing reads from 24 invertebrate animals and 4 marine metagenomic projects from publicly available DNA repositories. The animal reads have been cleaned of all types of contaminating sequence reads so that all the reads come from the target animal only. The bacterial reads have been verified as belonging to a bacterial family. 

##Data Format
All data are DNA sequences in standard fasta files, grouped either by species (in the case of the animals) or in sequencing run (in the case of the bacterial samples).

##Curation Rationale
This dataset was created to serve as a training dataset for a deep learning algorithm with the goal of differentiating between the DNA sequence reads of marine invertebrate animals and their associated microbial life. Marine invertebrates are underrepresented in genomic resources partly because their diverse microbiomes make sequencing and assembly of their genomes computationally challenging and costly compared to other animals of similar genome size. This project seeks to eliminate this hurdle by separating the sequences of marine invertebrate animals and their microbiomes bioinformatically prior to genome assembly. I chose marine invertebrate sequences based on the presence of a highly contiguous reference genome for the same species and tried to gather a wide taxonomic representation where possible from publicly available datasets. For the microbial reads, I chose marine metagenomic reads, though my options were more limited as publicly available metagenomic DNA reads were difficult to find for these organisms. I filtered all reads through a bioinformatic pipeline in an effort to be as sure as possible of the identity of each read so as not to bias the machine learning algorithm. 

##Initial Data Collection and Normalization
These data were collected by many different research groups, primarily university professors, postdoctoral researchers, and graduate students. They were collected for use in scientific studies with diverse goals and questions such as documenting diversity, establishing evolutionary relationships, and identifying genes that correspond to traits of interest. The DNA was isolated from each sample and sequenced on either an Illumina platform (for short reads) or a PacBio one (for longer reads). Before depositing the reads in a publicly available repository, some datasets were trimmed to remove adaptors used in the sequencing process as well as nucleotides that were more likely to be errors. In some cases the sequencing reads in this dataset are the ones that were used to create the genome assembly for that organism, but more often they were from different studies or individuals. The genome assemblies are often the result of many different sequencing efforts across multiple years, technologies, and institutions.

##Documentation for Source Datasets

###Eukaryotic datasets 

| Species Name  | Genome Accession  | Illumina Read Accessions   | PacBio Read Accessions  |
|---|---|---|---|
| *Achatina immaculata* | GCA_009760885.1 | SRR10033059 | SRR10023933 |
| *Acropora hyacinthus* | GCA_020536085.1 | DRR089920-DRR089923, DRR194183-DRR194187 | n/a |
| *Acropora millepora* | GCF_013753865.1 | SRR10571265-SRR10571270 | SRR11816591 |
| *Actinia tenebrosa* | GCA_009602425.1 | SRR8241370-SRR8241370 | n/a |
| *Alatina alata* | GCA_008930755.1 | SRR5168102-SRR5168104, SRR5168106, SRR5168108 | SRR5168105, SRR5168107, SRR5168109-SRR5168116 |
| *Amphimedon queenslandica* | GCF_000090795.1 |SRR11286069-SRR11286070 | n/a |
| *Archivesica marissinica* | GCA_014843695.1 | SRR11675938 | SRR11675937 |
| *Arion vulgaris* | GCA_020796225.1 | SRR13300036, SRR13300046 | n/a | 
| *Aurelia aurita* | GCA_004194415.1 | SRR7834587, SRR7866321, SRR7866920, SRR7889280-SRR7889284 | SRR7866923 |
| *Cassiopea andromeda* | GCA_018155075.1 | SRR10386856-SRR10386859 | n/a |
| *Crassostrea gigas* | GCF_902806645.1 | ERR1911806-ERR1911810 | SRR10799911-SRR10799914 | 
| *Diadumene lineata* | GCA_918843875.1 | ERR6688656-ERR6688659 | ERR6808024 | 
| *Dreissena polymorpha* | GCA_020536995.1 | SRR8948221 | SRR8948250, SRR8948252, SRR8948253, SRR8948255 | 
| *Ephydatia muelleri* | GCA_013339895.1 | SRR10983243-SRR10983246 | SRR10983238-SRR10983242 | 
| *Gigantopelta aegis* | GCF_016097555.1 | SRR13108173 | SRR13108175 | 
| *Lanistes nyassanus* | GCA_004794575.1 | SRR8599605-SRR8599607 | n/a | 
| *Margaritifera margaritifera* | GCA_015947965.1 | SRR13091477-SRR13091479 | n/a |
| *Mercenaria mercenaria* | GCF_014805675.1 | n/a | SRR10951931-SRR10951936 |
| *Mnemiopsis leidyi* | GCA_000226015.1 | SRR13494639-SRR13494648 | n/a |
| *Nematostella vectensis* | GCA_000209225.1 | SRR12775953, SRR12775955-SRR12775956 | SRR12775969, SRR12775977 |
| *Pleurobrachia bachei* | GCA_000695325.1 | SRR1174874-SRR1174877 | SRR13970178-SRR13970185 |
| *Pomacea canaliculata* | GCF_003073045.1 | SRR6425828, SRR8616633-SRR8616636 | SRR6425827 | 
| *Ruditapes philippinarum* | GCA_009026015.1 | SRR7716293-SRR7716297 | n/a |


###Bacterial Datasets

| Project Accession  | Read Accessions  | 
|---|---|
| PRJNA323666 | SRR3694369-SRR3694372 |
| PRJNA603662 | SRR10987117-SRR10987118 |
| PRJNA318959 | SRR3473501, SRR3473948-SRR3473949 |
| PRJNA588686 | SRR10912786-SRR10912905 |


##Preprocessing and Data Formatting
###Eukaryotes: 
I downloaded all the genomes as fasta files and renamed them to include the genus and species in the file names. I used a script from Anvio (version) to reformat each genome file to make sure that it did not contain any characters that were not nucleotides. I used BWA (version) to index each genome for mapping.

For the read files, I downloaded them in fastq format, and if a species had multiple read files from the same sequencing platform, I concatenated them into a single file for all downstream processing. I used TrimGalore! To trim all the short (Illumina) read files to remove adapter sequences, though I did not trim them for quality. Then I used BWA to map each read file onto the corresponding genome for that species. I mapped the Illumina reads in pairs and the PacBio reads as single-end. I used Seqtk (version) to pull out all the reads that mapped successfully to the genome and discarded the rest.

All the reads that mapped I then put through Kraken2 (version) with a standard database. Kraken2 breaks each read into kmers and tries to match them to the kmers in its database of human and bacterial DNA. The resulting files show each read, how many kmers were identified as human or bacterial, and an overall classification for the read. However, the overall classification for the read often does not correspond to the percentage of kmers in a read that were identified as a contaminant, so rather than accept the classifications that Kraken2 outputs, I used their identifications to create my own. I wrote a parser for the Kraken2 output that quantifies the percentage of kmers identified as a contaminant and allows the user to select a threshold for this percentage. Then any read that has more than that percentage of its kmers identified as a contaminant is classified as such, and all others remain unclassified. I used seqkit (version) to pull out all of the “unclassified” sequences (those most likely to belong to the target animals) and collect them into a final fasta file.

###Bacteria: 
Since these were metagenomic files rather than reads from a specific target organism, I did not attempt to map them to any genome. I trimmed the read files using the same process as the Eukaryotic reads. Instead of Kraken2, I used KrakenUniq, which follows a similar process but uses a more extensive bacterial database. I used the same parser as for the Eukaryotic reads, but instead of filtering out reads whose percent classified kmers was above a certain threshold, I filtered out any reads that did not classify as a bacterium.

##Discussion of Biases
The organisms in this dataset are not a proportional representation of the diversity of invertebrate life. They are primarily organisms that are relatively abundant, easy to sample, or hold some importance to human issues (i.e. an agricultural product or pest). This type of organism is overrepresented in publicly available sequencing datasets, so the majority of the animals that met my requirements fall into one of these categories.

##Limitations
I undertook the project in the first place because marine invertebrate organisms tend to be underrepresented in genomic resources. This also meant that my options for training datasets for them were somewhat limited. The datasets I have chosen represent the majority of the publicly available datasets that were available at the time that I was beginning the project. There were many more genomes available, but the reads used to create the genome (or other reads from the same species) were not available for each genome.

##Personal and Sensitive Information
There is no personal or sensitive information included in these data.







