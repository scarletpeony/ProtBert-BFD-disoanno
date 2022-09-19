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

This is a token classification model designed to predict the intrinsically disordered regions of amino acid sequences.

## Intended uses & limitations

This model works on amino acid sequences that are spaced between characters.

'0': No disorder

'1': Disordered


Example Inputs :

D E A Q F K E C Y D T C H K E C S D K G N G F T F C E M K C D T D C S V K D V K E K L E N Y K P K N 

M A S E E L Q K D L E E V K V L L E K A T R K R V R D A L T A E K S K I E T E I K N K M Q Q K S Q K K A E L L D N E K P A A V V A P I T T G Y T D G I S Q I S L

M D V F M K G L S K A K E G V V A A A E K T K Q G V A E A A G K T K E G V L Y V G S K T K E G V V H G V A T V A E K T K E Q V T N V G G A V V T G V T A V A Q K T V E G A G S I A A A T G F V K K D Q L G K N E E G A P Q E G I L E D M P V D P D N E A Y E M P S E E G Y Q D Y E P E A

M E L V L K D A Q S A L T V S E T T F G R D F N E A L V H Q V V V A Y A A G A R Q G T R A Q K T R A E V T G S G K K P W R Q K G T G R A R S G S I K S P I W R S G G V T F A 
A R P Q D H S Q K V N K K M Y R G A L K S I L S E L V R Q D R L I V V E K F S V E A P K T K L L A Q K L K D M A L E D V L I I T G E L D E N L F L A A R N L H K V D V R D A T G I D P V S L I A F D K V V M T A D A V K Q V E E M L A 

M S D K P D M A E I E K F D K S K L K K T E T Q E K N P L P S K E T I E Q E K Q A G E S 

## Training and evaluation data

Training and evaluation data were retrieved from https://www.csuligroup.com/DeepDISOBind/#Materials (Accessed March 2022).

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
