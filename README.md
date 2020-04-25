# Background
US Census has two public repositories on GitHub related to Disclosure Avoidance System using deferential privacy. I pulled the two repos into my computer and ran a Linux shell script to extract the full path of all files that are considered "documentation" - files without extention or with one of the following extensions: pdf, doc, docx, xls, xlsx, md, txt.

The shell script is:

`find ./Source/census2020-das-2010ddp-master ./Source/census2020-das-e2e-master -type f ! -name "*.*" -o -name "*.txt" -o -name "*.pdf" -o -name "*.docx" -o -name "*.doc" -o -name "*.xls", -o -name "*.xlsx" -o -name "*.md" > das_doc_files.txt`

This shell script generates a txt file with all the found files with full path. 

This Jupyter notebook handles the following:
- Extract the name of the repository
- Extract the name of the file
- Extract the file extension 
- Create a clickable path 

This notebook demonstrates the use of the folllowing Python and Pandas features:
- Reading a file directly from a URL
- Reading a file without a header 
- Functions
- Lambda functiond 
- Pandas apply() function
- Special character escaping
- split() and replace() 
