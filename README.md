# Caenorrhabditis_2
Size of Genome: 100.2 Mb (100 x 10^6 bp)
Structure: Linear DNA, 6 chromosomes 
Protein-coding genes: 20,000-25,000
Access genome sequence at https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_000002985.6/


How to generate the reverse complement of a sequence:
1. Load the emboss and seqtk modules into your workspace:
     module load emboss
     module load seqtk
2. Navigate to the 'GCF_000002985.6' directory:
     cd ncbi_dataset/data/GCF_000002985.6/
3. 'infoseq' to see what the genome file contains:
     infoseq GCF_000002985.6_WBcel235_genomic.fna
4. Extract one fasta sequence from the file:
     echo NC_003279.8 > GCF_000002985.6.txt
5. Extract the sequence from the larger file and store it in a new file:
     seqtk subseq GCF_000002985.6_WBcel235_genomic.fna GCF_000002985.6.txt > NC_003279.8.txt
6. Generate the reverse complement of the sequence and store it in a new file:
     revseq NC_003279.8.txt NC_003279.8.rev
   
![alt text](https://github.com/snehakini6/Caenorrhabditis_2/assets/138410658/9c898f3a-a559-468b-916d-b4abcb6cd57f)

How to find amino acid sequence of the sequence:
1. Make sure the emboss and seqtk modules are loaded into your workspace:
     module load emboss
     module load seqtk
2. Use the emboss command 'transeq' to translate the sequence to its corresponding amino acid sequence:
     transeq NC_003279.8.txt NC_003279.8.trans
   
![alt text](https://github.com/snehakini6/Caenorrhabditis_2/assets/138410658/7f6e2d89-f034-4f42-bd7e-54164a0e40b6)

How to determine the GC content of the sequence:
1.  Make sure the emboss and seqtk modules are loaded into your workspace:
     module load emboss
     module load seqtk
2. Use 'infoseq' with qualifiers '-only -pgc' to see information about the sequence, to isolate information about the GC count as a percentage:
     infoseq NC_003279.8.txt -only -pgc

![alt text](https://github.com/snehakini6/Caenorrhabditis_2/assets/138410658/d2ef7287-b8b9-4696-bd22-55b11c58a4e0)



How to generate the reverse complement of a sequence:
1. Load the emboss and seqtk modules into your workspace:
     module load emboss
     module load seqtk
2. Navigate to the 'GCF_000002985.6' directory:
     cd ncbi_dataset/data/GCF_000002985.6/
3. 'infoseq' to see what the genome file contains:
     infoseq GCF_000002985.6_WBcel235_genomic.fna
4. Extract one fasta sequence from the file:
     echo NC_003279.8 > GCF_000002985.6.txt
5. Extract the sequence from the larger file and store it in a new file:
     seqtk subseq GCF_000002985.6_WBcel235_genomic.fna GCF_000002985.6.txt > NC_003279.8.txt
6. Generate the reverse complement of the sequence and store it in a new file:
     revseq NC_003279.8.txt NC_003279.8.rev
      
