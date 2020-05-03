# Automatic-ICD-9-Encoding-with-BERT/RoBERTa
This is a course project for BMSC-GA 4493, Deep Learning in  Medicine, Master of Science in Data Science in New York University

The project is done by Junge Zhang and Xiaoyi Zhang

The original data is from MIMIC-III Clinical Database, and has been preprocessed by Xiaoyi Zhang from another project.

The project target is to use BERT/RoBERTa to automatically encode ICD-9 codes for patients(multi-label for each patient) with long sequence of discharge summary (over 512 tokens).

The main solution to break the 512 tokens limit from the original BERT is by splitting the sequence into half, train two BERT/RoBERTa for each half sequence and concatenate their output hidden states before inputting into the fully connected layer. Both BERT and RoBERTa are firstly trained with 5 epochs and then retrained with another 5 epochs.

**Data Reference:**

MIMIC-III Clinical Database. [online] Available at: https://physionet.org/content/mimiciii/1.4/.

**Package Reference**

Vig, J. A Multiscale Visualization of Attention in the Transformer Model. \emph{arXiv preprint arXiv:1906.05714}, 2009, URL: https://arxiv.org/abs/1906.05714.

Vig, J. bertviz. URL: https://github.com/jessevig/bertviz.

Huggingface. Transformers. URL: https://github.com/huggingface/transformers.

**Other Reference**

please check our paper.

