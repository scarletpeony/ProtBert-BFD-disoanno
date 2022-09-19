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

M S A I Q N L H S F D P F A D A S K G D D L L P A G T E D Y I H I R I Q Q R N G R K T L T T V Q G I A D D Y D K K K L V K A F K K K F A C N G T V I E H P E Y G E V I Q L Q G D Q R K N I C Q F L V E I G L A K D D Q L K V H G F 

M A S R Q N N K Q E L D E R A R Q G E T V V P G G T G G K S L E A Q Q H L A E G R S K G G Q T R K E Q L G T E G Y Q E M G R K G G L S T V E K S G E E R A Q E E G I G I D E S K F R T G N N K N Q N Q N E D Q D K

M P P I A T R R G Q Y E P K V Q Q A K L S P D T I P L N P A D K T K D P L A R A D S L H H H V E S D S Q E D D K A A E E P P L S R K R W Q N R T F R R K G R R Q A P Y K H K 

S G S D G G V C P K I L K K C R R D S D C P G A C I C R G N G Y C G 

M G G K W S K S S V V G W P T V R E R M R R A E P A A D G V G A A S R D L E K H G A I T S S N T A A T N A A C A W L E A Q E E E E V G F P V T P Q V P L R P M T Y K A A V D L S H F L K E K G G L E G L I H S Q R R Q D I L D L W I Y H T Q G Y F P D W Q N Y T P G P G V R Y P L T F G W C Y K L V P V E P D K V E E A N K G E N T S L L H P V S L H G M D D P E R E V L E W R F D S R L A F H H V A R E L H P E Y F K N C 

M R Y T D S R K L T P E T D A N H K T A S P Q P I R R I S S Q T L L G P D G K L I I D H D G Q E Y L L R K T Q A G K L L L T K 

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
