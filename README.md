# Cross-Dialectal Arabic Translation: Comparative Analysis on Large Language Models
This paper evaluates the performance of LLMs in translating Arabic dialects to MSA. The paper explores different prompting techniques such as zero-shot and few-shot prompting. Also, we used two datasets and evaluated through 6 metrics in addition to ANOVA statistical test.

# Datasets
Datasets used:

**QADI:** https://github.com/qcri/QADI

**MADAR:** https://sites.google.com/nyu.edu/madar/

Data Pre-processing:
- For QADI dataset, the data was clean and well-balanced, we applied random sampling approach to select 50K samples.
- For the MADAR dataset, the original version included multiple city dialects, with an inconsistent number of sentences per city. To prepare our dataset, we performed the following steps:
  1. Identified the smallest available number of sentences across cities (2,000).
  2. Retained only datasets corresponding to country capitals, excluding other cities.
  3. Listed the sentences for each country separately, with the MSA baseline stored in a separate file.
  4. For each country, created a .CSV file containing two columns (Dialect and MSA). Sentences were gathered and mapped using their original IDs from the source files.

# API Calls and Scripts:
- **GPT.txt**: represents the script to call API requests to GPT 3.5/4 for MADAR dataset.
- **GPT-QADI.txt**: represents the script to call API requests to GPT 3.5/4 for QADI dataset.
- **BackTranslation.txt**: shows the back translation alogirithm for QADI dataset.
- **gemini.py**: represent the Python code to call Bard (Gemini) model.

# Performance Metrics:
The LLMs were evaluated using well-known and solid performance metrics, the code to calculate such metrics are found in the following files:
- **TER.rtf**
- **BLEU.rtf**
- **CosineSimilarity.rtf**
- **SentencBERT.rtf**
- **ROUGE.rtf**
- **UniversalSimilarityEncoder.rtf**

# Output files:
- **JO-Output-MADAR.csv**: represents part of the output data, the first 2 columns are already did by the developers in the step of pre-processing. The third column is the model response.
- **JO-Output-QADI.csv**: represents part of the output data, the first column is ready from the dataset, the second column is through the back translation to create the baseline. The third column is the model response.
