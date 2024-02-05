# Caenorrhabditis_2
Size of Genome: 100.2 Mb (100 x 10^6 bp)
Structure: Linear DNA, 6 chromosomes 
Protein-coding genes: 20,000-25,000
Access genome sequence at https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_000002985.6/



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

How to Generate a Reverse Complement of a Sequence:
1. Access your scratch account via discovery.
cd /scratch/kutzer.h

2. Download the NCBI tools
curl -o datasets https://ftp.ncbi.nlm.nih.gov/pub/datasets/command~
line/v2/linux-amd64/datasets

curl -o dataformat https://ftp.ncbi.nlm.nih.gov/pub/datasets/command-
line/v2/linux-amd64/dataformat

3. Make them executable:
chmod tx datasets dataformat

4. Download the genome sequence to your scratch account on the cluster using the accession number.
./datasets download genome accession GCF_000002985.6

5. Unzip the file.
unzip ncbi_dataset.zip

6. Load the necessary modules into the work space.
module load emboss
module load seqtk

7. Extract a sequence.
echo 'NC_003279.8' > list.txt

8. Then use the command that tells seqtk to extract that sequence from the larger file and store it in a new file by itself.
seqtk subseq GCF_000002985.6_WBcel235_genomic.fna list.txt > NC_003279.8.txt

9. Now generate a new reverse complement sequence.
revseq NC_003279.8.txt NC_003279.8.rev

      
