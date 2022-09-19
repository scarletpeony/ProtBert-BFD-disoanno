---
tags:
- generated_from_trainer
metrics:
- precision
- recall
- f1
model-index:
- name: prot_bert_bfd-disoanno
  results: []
---

<!-- This model card has been generated automatically according to the information the Trainer had access to. You
should probably proofread and complete it, then remove this comment. -->

# prot_bert_bfd-disoanno

This model is a fine-tuned version of [Rostlab/prot_bert_bfd](https://huggingface.co/Rostlab/prot_bert_bfd) on the None dataset.
It achieves the following results on the evaluation set:
- Loss: 0.4253
- Precision: 0.8161
- Recall: 0.8234
- F1: 0.8146

## Model description

More information needed

## Intended uses & limitations

More information needed

## Training and evaluation data

More information needed

## Training procedure

### Training hyperparameters

The following hyperparameters were used during training:
- learning_rate: 2e-05
- train_batch_size: 8
- eval_batch_size: 8
- seed: 42
- optimizer: Adam with betas=(0.9,0.999) and epsilon=1e-08
- lr_scheduler_type: linear
- num_epochs: 3

### Training results

| Training Loss | Epoch | Step | Validation Loss | Precision | Recall | F1     |
|:-------------:|:-----:|:----:|:---------------:|:---------:|:------:|:------:|
| 0.4895        | 1.0   | 61   | 0.4415          | 0.8257    | 0.8317 | 0.8262 |
| 0.5881        | 2.0   | 122  | 0.4242          | 0.8124    | 0.8201 | 0.8119 |
| 0.562         | 3.0   | 183  | 0.4253          | 0.8161    | 0.8234 | 0.8146 |


### Framework versions

- Transformers 4.21.3
- Pytorch 1.12.1+cu113
- Datasets 2.4.0
- Tokenizers 0.12.1
