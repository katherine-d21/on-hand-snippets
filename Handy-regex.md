**Handy Regex**

## To remove human, decoys, and contaminants (case-insensitive)

* Remove contaminants/decoys

`NOT Matching`

`(con_)|(contam_)|(rev_)|(decoy_)`

* Then, `Matching` and `NOT matching` `_HUMAN` for human and microbial entries, respectively


## Using regex to convert FASTA header formats

* As of writing, MetaNovo only accepts UniProt FASTA header. Here, the input is NCBI format and a regular expression was writtein to swap the position of organism and protein accession to match UniProt (to be accepted by MetaNovo).

NCBI header format:

`>organism_id|accession description of protein`

Compared to UniProt format:

`>db|protein_accession|description and organism`

Input Example NCBI FASTA header:

`>SEQF4634.1|QAZ47660.1 chromosomal replication initiator protein DnaA [Cutibacterium acnes DSM 1897] [HMT-530 Cutibacterium acnes DSM 1897]`

Galaxy tool: Regex Find and Replace (Galaxy Version 1.0.3):

* Find pattern: `^>([^|]+)\|([^ ]+)\s+(.*)`
* Replacement: `>generic|\2|\1|\3`

Output (that MetaNovo will accept):

`>generic|QAZ47660.1|SEQF4634.1|chromosomal replication initiator protein DnaA [...]`
