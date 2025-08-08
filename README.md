# Cross-Dialectal Arabic Translation: Comparative Analysis on Large Language Models
This paper evaluates the performance of LLMs in translating Arabic dialects to MSA. The paper explores different prompting techniques such as zero-shot and few-shot prompting. Also, we used two datasets and evaluated through 6 metrics in addition to ANOVA statistical test.

# Datasets
Datasets used:

**QADI:** https://github.com/qcri/QADI

**MADAR:** https://sites.google.com/nyu.edu/madar/

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
