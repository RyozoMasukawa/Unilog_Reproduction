# Unilog_Reproduction
Reproduction of Unilog using 🤗

I attempted to replicate a versatile log analysis model called Unilog in this [UniLog: Deploy One Model and Specialize it for All Log Analysis Tasks
 technical report](https://arxiv.org/abs/2112.03159) by Yichen Zhu, Weibin Meng, Ying Liu, Shenglin Zhang, Tao Han, Shimin Tao, Dan Pei

There are many areas for improvement. I would appreciate any advice. Thank you! 🤗

# Unilog Model Architecture Source Code
I implemented the architecture of Unilog by referencing codes from [Huggingface Transformers BERT](./hf_transformers/src/transformers/models/bert/modeling_bert.py)

# Dataset
The dataset and pretrained model should be saved in [./logdata](./logdata)

You can download dataset for pretraining from this page([https://github.com/logpai/loghub](https://github.com/logpai/loghub))

In addition the log summary pair dataset can be downloaded from this page([https://github.com/WeibinMeng/LogSummary/tree/main](https://github.com/WeibinMeng/LogSummary/tree/main))

# Pretraining
[pretraining.ipynb](./pretraining.ipynb) is the original code to pretrain Unilog model by using Masked Language Modeling(MLM)

# Finetuning on downstream tasks
## Seq2Seq summarization
[logsummary_seq2seq.ipynb](./logsummary_seq2seq.ipynb)

## Anomaly Detection on HDFS dataset
[log_anomaly_detect.ipynb](./log_anomaly_detect.ipynb)

# ChatGPT based Root Cause Analysis(RCA)

Inspired from the paper "Empowering Practical Root Cause Analysis by Large Language Models for Cloud Incidents"([https://arxiv.org/abs/2305.15778](https://arxiv.org/abs/2305.15778)), I also implemented a chatGPT-based RCA tool using CoT and kNN algorithm with fastText vectorization. The source code is available from the notebook below.

[chatGPT_fewshot_ms.ipynb](./chatGPT_fewshot_ms.ipynb)






