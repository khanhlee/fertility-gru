# Fertility-GRU: Identifying fertility-related proteins by incorporating GRU and PSSM profiles

Note: for the PSSM dataset, please go to "pssm" directory and extract to use.

Step-by-step to use:

Step 1: Extract all PSSM files into 2 separate folders:
- "fertility": positive data
- "non-fertility": negative data

Step 2: Put sequence IDs into training and list file:
- Training dataset: 2 files "fertility.cv.list" and "non-fertility.cv.list"
- Testing dataset: 2 files "fertility.ind.list" and "non-fertility.ind.list"
(We provided our training and testing list file, the authors can change according to their purpose)

Step 3: Run Python code to train and evaluate model:
- python3 oogenesis_gru.py

The output will be shown after training process. "1" indicates that the sequence is fertility-related protein, otherwise, "0" indicates non-fertility protein.

The authors could use single or multiple sequences in the list file. If the authors would like to predict the new sequence that does not have PSSM file, please use PSI-BLAST tool to generate PSSM profile first. After that, they only need to copy PSSM file into corresponding folder and run our code.
