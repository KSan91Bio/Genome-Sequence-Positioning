# Genome-Sequence-Positioning
Programs created for extracting the chromosomes of the genome sequence and placing positions for the nucleotides A,C,G,T

The first part is to obtain the files required for the programs. The first file to obtain is the vcf file from the 1000 genomes website. The second file to obtain is the length of the chromosomes. The file is provided in the repository.

The first program to be used is Chromo_Split.py, where it will use the hg19_length.list file to create a dictionary for each chromosome as it reads each line in the file. Within the for loop, new files will be created according to the chromosome obtained within that for loop and stored in the dictionary.

After each chromsome has been placed in their own dictionary from the hg19_length.list file, the vcf file will be used to store the vcf information of each chromosome. A for loop will be used to read each line of the vcf file to find the information of each chromosome. Within the for loop, an if statement is used where if the line begins with #, the for loop will continue to disregard the first part of the vcf file. As the for loop reads every line, if the chromosome matches the chromosome from the previous loop, the contents of the line will be stored in the dictionary.

The last for loop is used to close the vcf files created that contain the information for each chromosome from the large vcf in the second for loop to release the memory and complete the program.

The second program, Chromosome_Nucleotide_Sequence.py, is used obtain the length of every chromosome in the human genome and place the appropriate nucleotide at the position, whether it's the reference allele or alternate allele. A new file for the chromosome is created at the beginning of the program that will store the sequence of the chromosome. Four dictionaries are created at the start, where each one will contain the length of the chromosome, using the hg19_length.list file.

The second for loop is used to open the vcf file of the chromosome being used for the program. The for loop will read the lines of the file, and store the first five variables: chrom, pos, rsid, ref_str, and alt_str into the token variables that will be used for the next part of the for loop. The last part are a sequence of eight if statements, the first four representing the reference allele and the other representing the alternate allele, where if the variable matches the letter of the nucleotide, enter 1 on that position. This will continue until it finishes and the file created at the beginnig will close, ending the program. 
