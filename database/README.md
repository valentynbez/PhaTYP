The main function of the file proteins.csv is to provide the relationship information between proteins and their corresponding protein clusters. There are three relevant columns in this file for this mapping function: ‘protein_id’ is the accession of the protein, ‘contigs_id’ is the phages where the protein belongs, and ‘cluster’ is the containing cluster ID for this protein. protein.csv contains 468,105 proteins we downloaded from RefSeq at the time of conducting the experiments. If the value of the ‘cluster’ is not given, this protein does not belong to any protein cluster. When running PhaTYP, the program first aligns the query/test protein against the protein database (database.fa), which contains 431,582 proteins inside our chosen protein clusters (token set). The protein.csv file then serves as a look-up table for assigning protein clusters to query/test proteins according to their best hits. For example, if the best-aligned protein for a query/test protein is protein A, we will assign the corresponding protein cluster for A to the query/test protein according to proteins.csv.