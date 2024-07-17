Series of python scripts to take BOLD-downloaded taxonomy and paths to raw reads and create sample submission CSV for input into [skim2mito](https://github.com/o-william-white/skim2mito)

## 1_folder2csv_trim.py
Takes path to directory containing raw reads (.fq.gz) and populates .csv with sample names (ID), R1 read path (forward) and R2 read path (reverse).

**usage: python 1_folder2csv_trim.py [/path/to/dir/raw_seqs.fq.gz]**
- **/path/to/dir/raw_seqs.fq.gz** = path to parent directory containing raw reads in .fq.gz format.


## 2_sample2taxid.py
Takes BOLD taxonomy.tsv output containing sample ID and taxonomic ranks based on morphological identification (Phylum, class, Order, Family, Subfamily, Tribe, Genus, Species, Subspecies), grabs taxonomic ID (taxid) using NCBI Entrez API, determines taxonomic rank of taxid (matched_rank), and parses taxid and matched_rank to .csv

**usage: python 2_sample2taxid.py [path/to/BOLD_output.csv] [sample2taxid.csv]**
- **path/to/BOLD_output.csv** = 
