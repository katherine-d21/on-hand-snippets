Compare lines from 2 tabular outputs

SELECT DISTINCT c2 FROM t2 WHERE c2 IN (SELECT c2 FROM t1);

Count # of duplicates in a tabular file

SELECT c2, COUNT(\*) FROM t1 GROUP BY c2 HAVING COUNT(\*)>1


* BLASTP peptide output
  * Specify column names
> qseqid,sseqid,pident,length,mismatch,gapopen,qstart,qend,sstart,send,evalue,bitscore,sallseqid,score,nident,positive,gaps,ppos,qframe,sframe,qseq,sseq,qlen,slen,salltitles

* PepQuery psm_rank.txt
  * Specify column names
> peptide,modification,n,spectrum_title,charge,exp_mass,tol_ppm,tol_da,isotope_error,pep_mass,mz,score,n_db,total_db,n_random,total_random,pvalue,rank,n_ptm,confident,ref_delta_score,mod_delta_score

* FragPipe peptide report
  * Specify column names
> Experiment,Peptide,PrevAA,NextAA,Peptide_Length,Protein_Start,Protein_End,Charges,Probability,Spectral_Count,Intensity,Assigned_Mods,Observed_Mods,Protein,ProteinID,Entry_Name,Gene,Protein_Desc,Mapped_Genes,Mapped_Proteins  

* Unipept peptinfo tsv
  * Specify column names
- *With all taxonomic lineage, including LCA:*
> peptide,total_protein_count,ec_numbers,ec_protein_counts,ec_names,go_terms,go_protein_counts,go_names,ipr_codes,ipr_protein_counts,ipr_types,ipr_names,taxon_rank,taxon_id,taxon_name,kingdom_id,kingdom,subkingdom_id,subkingdom,superphylum_id,superphylum,phylum_id,phylum,subphylum_id,subphylum,superclass_id,superclass,class_id,class,subclass_id,subclass,infraclass_id,infraclass,superorder_id,superorder,order_id,order_name,suborder_id,suborder,infraorder_id,infraorder,parvorder_id,parvorder,superfamily_id,superfamily,family_id,family,subfamily_id,subfamily,tribe_id,tribe,subtribe_id,subtribe,genus_id,genus,subgenus_id,subgenus,species_group_id,species_group,species_subgroup_id,species_subgroup,species_id,species,subspecies_id,subspecies,varietas_id,varietas,forma_id,forma
 - *With only LCA:*
> peptide,total_protein_count,ec_numbers,ec_protein_counts,ec_names,go_terms,go_protein_counts,go_names,ipr_codes,ipr_protein_counts,ipr_types,ipr_names,taxon_rank,taxon_id,taxon_name,kingdom,subkingdom,superphylum,phylum,subphylum,superclass,class,subclass,superorder,order,suborder,infraorder,superfamily,family,subfamily,tribe,subtribe,genus,subgenus,species_group,species_subgroup,species,subspecies,varietas,forma

include query result column headers: `Yes` > `no comment character prefix`
