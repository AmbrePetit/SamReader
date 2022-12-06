# SamReader
The aim of this script is to extract relevant information from a mapping file : reads mapped, aligned, quality of mapping.



Prerequisites : 
Our script uses different configuration and packages, please check if it's compatible : 
- Python 3 : if your version is older, please update your version doing : 
	sudo apt install python3

- Packages used : sys, re, os, pathlib


Installation : 
- Download the script :


Input : 
- SAM file with ".sam" extension (this script will check this before launching methods)
- Emplacement of this file : right click on the file, then 'proprieties' and then copy the full path of the file (emplacement)


Launch the script : 
- On terminal : python3 SamReader.py

Output : 
- Number of reads on starting file
- Number of reads greater than a specific mapping quality
- Number of reads correctly aligned (based on CIGAR informations)
- Number of mapped reads (identified with FLAG)
- Number of reads "proper mapped" : paired reads and mapped in proper pair with a sequence's size < 150 bp (identified with FLAG°

Saving on a text file : 
- Enter "y" at the question "Do you want to save all values in a .txt file ?" : the file would be placed by default on your current repertory and the file named "Results.txt" 
	/!\ Remember to rename the text file if you run the script with different SAM file because otherwise the file would be overwritten to put new values
- You can save the entire output of the script on a text file, by default placed on your current repertory and if no name is entered the file will be named "typescript" :
  Enter before launch the script : script <name.txt> 
  To quit when script is finished, enter : exit


License : 
This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation,
either version 3 of the License, or (at your option) any later version.
This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; 
without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.
You should have received a copy of the GNU General Public License along with this program. If not, see <https://www.gnu.org/licenses/>.

Option list :
-h or --help : help information
-i or --input: input file (.sam)
-o or --output: output name files (.txt)

Synopsis :
SamReader.py -h or --help # Launch the help.
SamReader.py -i or --input <file> # Launch SamReader to analyze a samtools file (.sam) and print the result in the terminal
SamReader.py -i or --input <file> -o or --output <name> # Launch SamReader to analyze a samtools file (.sam) and print the result in the file called <name>
  

Authors :
- Bioinformatics students : Ambre PETIT and Laure NANNINI
