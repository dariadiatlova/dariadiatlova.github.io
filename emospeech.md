---
layout: default
title: "EmoSpeech: guiding FastSpeech2 towards Emotional Text to Speech"
description: "https://openreview.net/pdf?id=LYgrzXwVsm"
link: "https://openreview.net/pdf?id=LYgrzXwVsm"
---

## Abstract: 

State-of-the-art speech synthesis models try to get as close as
possible to the human voice. Hence, modelling emotions is an
essential part of Text-To-Speech (TTS) research. In our work,
we selected FastSpeech2 as the starting point and proposed a
series of modifications for synthesizing emotional speech. According to automatic and human evaluation, our model, EmoSpeech, surpasses existing models regarding both MOS score
and emotion recognition accuracy in generated speech. We
provided a detailed ablation study for every extension to FastSpeech2 architecture that forms EmoSpeech. The uneven distribution of emotions in the text is crucial for better, synthesized speech and intonation perception. Our model includes a
conditioning mechanism that effectively handles this issue by
allowing emotions to contribute to each phone with varying intensity levels. The human assessment indicates that proposed
modifications generate audio with higher MOS and emotional
expressiveness.

### Notation of the models: 

Please, refer to [section 5](https://openreview.net/pdf?id=LYgrzXwVsm) for detailed notation of the models.

| ID                     | Model                            |  
|:-----------------------|:---------------------------------|
| #0                     | Expressive FastSpeech2, baseline | 
| #1                     | #0 + `eGeMAPS` predictor         |
| #2                     | #1 + `CLN`                       |
| #3                     | #2 + `CCA`                       |
| EmoSpeech              | #3 + `JCU`                       |

## Audio samples

### Speaker 0011

| Model            | Neutral                                                           | Angry                                                              | Happy                                                            | Sad                                                              | Surprise                                                         |
|:-----------------|:------------------------------------------------------------------|:-------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------|
| _Sentence_       | _Monster made a deep bow._                                        | _Who is been repeating all that hard stuff to you?_                | _Rat came and replied on the leaves._                            | _The football teams give a tea party._                           | _As rich as Peter's son in law!_                                 |
| original         | <audio src="/wavs/original/1_6_0.wav" controls preload></audio>   | <audio src="/wavs/original/1_11_1.wav" controls preload></audio>   | <audio src="/wavs/original/1_8_2.wav" controls preload></audio>  | <audio src="/wavs/original/1_3_3.wav" controls preload></audio>  | <audio src="/wavs/original/1_0_4.wav" controls preload></audio>  |
| baseline         | <audio src="/wavs/baseline/1_6_0.wav" controls preload></audio>   | <audio src="/wavs/baseline/1_11_1.wav" controls preload></audio>   | <audio src="/wavs/baseline/1_8_2.wav" controls preload></audio>  | <audio src="/wavs/baseline/1_3_3.wav" controls preload></audio>  | <audio src="/wavs/baseline/1_0_4.wav" controls preload></audio>  |
| # 1              | <audio src="/wavs/model1/1_6_0.wav" controls preload></audio>     | <audio src="/wavs/model1/1_11_1.wav" controls preload></audio>     | <audio src="/wavs/model1/1_8_2.wav" controls preload></audio>    | <audio src="/wavs/model1/1_3_3.wav" controls preload></audio>    | <audio src="/wavs/model1/1_0_4.wav" controls preload></audio>    |
| # 2              | <audio src="/wavs/model2/1_6_0.wav" controls preload></audio>     | <audio src="/wavs/model2/1_11_1.wav" controls preload></audio>     | <audio src="/wavs/model2/1_8_2.wav" controls preload></audio>    | <audio src="/wavs/model2/1_3_3.wav" controls preload></audio>    | <audio src="/wavs/model2/1_0_4.wav" controls preload></audio>    |
| # 3              | <audio src="/wavs/model3/1_6_0.wav" controls preload></audio>     | <audio src="/wavs/model3/1_11_1.wav" controls preload></audio>     | <audio src="/wavs/model3/1_8_2.wav" controls preload></audio>    | <audio src="/wavs/model3/1_3_3.wav" controls preload></audio>    | <audio src="/wavs/model3/1_0_4.wav" controls preload></audio>    |
| **EmoSpeech**    | <audio src="/wavs/emospeech/1_6_0.wav" controls preload></audio>  | <audio src="/wavs/emospeech/1_11_1.wav" controls preload></audio>  | <audio src="/wavs/emospeech/1_8_2.wav" controls preload></audio> | <audio src="/wavs/emospeech/1_3_3.wav" controls preload></audio> | <audio src="/wavs/emospeech/1_0_4.wav" controls preload></audio> |


### Speaker 0012

| Model         | Neutral                                                           | Angry                                                            | Happy                                                            | Sad                                                              | Surprise                                                         |
|:--------------|:------------------------------------------------------------------|:-----------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------|
| _Sentence_    | _All smile were real and the happier，the more sincere._           | _I thought you meant how old are you?_                           | _Let's make the noise a snake._                                  | _She is now choosing skirt to wear._                             | _The football teams give a tea party._                           |
| original      | <audio src="/wavs/original/2_10_0.wav" controls preload></audio>  | <audio src="/wavs/original/2_2_1.wav" controls preload></audio>  | <audio src="/wavs/original/2_5_2.wav" controls preload></audio>  | <audio src="/wavs/original/2_4_3.wav" controls preload></audio>  | <audio src="/wavs/original/2_3_4.wav" controls preload></audio>  |
| baseline      | <audio src="/wavs/baseline/2_10_0.wav" controls preload></audio>  | <audio src="/wavs/baseline/2_2_1.wav" controls preload></audio>  | <audio src="/wavs/baseline/2_5_2.wav" controls preload></audio>  | <audio src="/wavs/baseline/2_4_3.wav" controls preload></audio>  | <audio src="/wavs/baseline/2_3_4.wav" controls preload></audio>  |
| # 1           | <audio src="/wavs/model1/2_10_0.wav" controls preload></audio>    | <audio src="/wavs/model1/2_2_1.wav" controls preload></audio>    | <audio src="/wavs/model1/2_5_2.wav" controls preload></audio>    | <audio src="/wavs/model1/2_4_3.wav" controls preload></audio>    | <audio src="/wavs/model1/2_3_4.wav" controls preload></audio>    |
| # 2           | <audio src="/wavs/model2/2_10_0.wav" controls preload></audio>    | <audio src="/wavs/model2/2_2_1.wav" controls preload></audio>    | <audio src="/wavs/model2/2_5_2.wav" controls preload></audio>    | <audio src="/wavs/model2/2_4_3.wav" controls preload></audio>    | <audio src="/wavs/model2/2_3_4.wav" controls preload></audio>    |
| # 3           | <audio src="/wavs/model3/2_10_0.wav" controls preload></audio>    | <audio src="/wavs/model3/2_2_1.wav" controls preload></audio>    | <audio src="/wavs/model3/2_5_2.wav" controls preload></audio>    | <audio src="/wavs/model3/2_4_3.wav" controls preload></audio>    | <audio src="/wavs/model3/2_3_4.wav" controls preload></audio>    |
| **EmoSpeech** | <audio src="/wavs/emospeech/2_10_0.wav" controls preload></audio> | <audio src="/wavs/emospeech/2_2_1.wav" controls preload></audio> | <audio src="/wavs/emospeech/2_5_2.wav" controls preload></audio> | <audio src="/wavs/emospeech/2_4_3.wav" controls preload></audio> | <audio src="/wavs/emospeech/2_3_4.wav" controls preload></audio> |

### Speaker 0014

| Model            | Neutral                                                            | Angry                                                             | Happy                                                            | Sad                                                              | Surprise                                                         |
|:-----------------|:-------------------------------------------------------------------|:------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------|
| _Sentence_       | _A divine wrath made her blue eyes awful._                         | _Rat came and replied on the leaves._                             | _The football teams give a tea party._                           | _As rich as Peter's son in law!_                                 | _Let's make the noise a snake._                                  |
| original         | <audio src="/wavs/original/4_13_0.wav" controls preload></audio>   | <audio src="/wavs/original/4_8_1.wav" controls preload></audio>   | <audio src="/wavs/original/4_3_2.wav" controls preload></audio>  | <audio src="/wavs/original/4_0_3.wav" controls preload></audio>  | <audio src="/wavs/original/4_5_4.wav" controls preload></audio>  |
| baseline         | <audio src="/wavs/baseline/4_13_0.wav" controls preload></audio>   | <audio src="/wavs/baseline/4_8_1.wav" controls preload></audio>   | <audio src="/wavs/baseline/4_3_2.wav" controls preload></audio>  | <audio src="/wavs/baseline/4_0_3.wav" controls preload></audio>  | <audio src="/wavs/baseline/4_5_4.wav" controls preload></audio>  |
| # 1              | <audio src="/wavs/model1/4_13_0.wav" controls preload></audio>     | <audio src="/wavs/model1/4_8_1.wav" controls preload></audio>     | <audio src="/wavs/model1/4_3_2.wav" controls preload></audio>    | <audio src="/wavs/model1/4_0_3.wav" controls preload></audio>    | <audio src="/wavs/model1/4_5_4.wav" controls preload></audio>    |
| # 2              | <audio src="/wavs/model2/4_13_0.wav" controls preload></audio>     | <audio src="/wavs/model2/4_8_1.wav" controls preload></audio>     | <audio src="/wavs/model2/4_3_2.wav" controls preload></audio>    | <audio src="/wavs/model2/4_0_3.wav" controls preload></audio>    | <audio src="/wavs/model2/4_5_4.wav" controls preload></audio>    |
| # 3              | <audio src="/wavs/model3/4_13_0.wav" controls preload></audio>     | <audio src="/wavs/model3/4_8_1.wav" controls preload></audio>     | <audio src="/wavs/model3/4_3_2.wav" controls preload></audio>    | <audio src="/wavs/model3/4_0_3.wav" controls preload></audio>    | <audio src="/wavs/model3/4_5_4.wav" controls preload></audio>    |
| **EmoSpeech**    | <audio src="/wavs/emospeech/4_13_0.wav" controls preload></audio>  | <audio src="/wavs/emospeech/4_8_1.wav" controls preload></audio>  | <audio src="/wavs/emospeech/4_3_2.wav" controls preload></audio> | <audio src="/wavs/emospeech/4_0_3.wav" controls preload></audio> | <audio src="/wavs/emospeech/4_5_4.wav" controls preload></audio> |

### Speaker 0015

| Model         | Neutral                                                           | Angry                                                            | Happy                                                             | Sad                                                              | Surprise                                                          |
|:--------------|:------------------------------------------------------------------|:-----------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------|-------------------------------------------------------------------|
| _Sentence_    | _In which fox loses a tail and its elder sister finds one._       | _She is now choosing skirt to wear._                             | _Hold up my chin, slow and solid._                                | _I thought you meant how old are you?_                           | _A divine wrath made her blue eyes awful._                        |
| original      | <audio src="/wavs/original/5_19_0.wav" controls preload></audio>  | <audio src="/wavs/original/5_4_1.wav" controls preload></audio>  | <audio src="/wavs/original/5_17_2.wav" controls preload></audio>  | <audio src="/wavs/original/5_2_3.wav" controls preload></audio>  | <audio src="/wavs/original/5_13_4.wav" controls preload></audio>  |
| baseline      | <audio src="/wavs/baseline/5_19_0.wav" controls preload></audio>  | <audio src="/wavs/baseline/5_4_1.wav" controls preload></audio>  | <audio src="/wavs/baseline/5_17_2.wav" controls preload></audio>  | <audio src="/wavs/baseline/5_2_3.wav" controls preload></audio>  | <audio src="/wavs/baseline/5_13_4.wav" controls preload></audio>  |
| # 1           | <audio src="/wavs/model1/5_19_0.wav" controls preload></audio>    | <audio src="/wavs/model1/5_4_1.wav" controls preload></audio>    | <audio src="/wavs/model1/5_17_2.wav" controls preload></audio>    | <audio src="/wavs/model1/5_2_3.wav" controls preload></audio>    | <audio src="/wavs/model1/5_13_4.wav" controls preload></audio>    |
| # 2           | <audio src="/wavs/model2/5_19_0.wav" controls preload></audio>    | <audio src="/wavs/model2/5_4_1.wav" controls preload></audio>    | <audio src="/wavs/model2/5_17_2.wav" controls preload></audio>    | <audio src="/wavs/model2/5_2_3.wav" controls preload></audio>    | <audio src="/wavs/model2/5_13_4.wav" controls preload></audio>    |
| # 3           | <audio src="/wavs/model3/5_19_0.wav" controls preload></audio>    | <audio src="/wavs/model3/5_4_1.wav" controls preload></audio>    | <audio src="/wavs/model3/5_17_2.wav" controls preload></audio>    | <audio src="/wavs/model3/5_2_3.wav" controls preload></audio>    | <audio src="/wavs/model3/5_13_4.wav" controls preload></audio>    |
| **EmoSpeech** | <audio src="/wavs/emospeech/5_19_0.wav" controls preload></audio> | <audio src="/wavs/emospeech/5_4_1.wav" controls preload></audio> | <audio src="/wavs/emospeech/5_17_2.wav" controls preload></audio> | <audio src="/wavs/emospeech/5_2_3.wav" controls preload></audio> | <audio src="/wavs/emospeech/5_13_4.wav" controls preload></audio> |

### Speaker 0017

| Model         | Neutral                                                           | Angry                                                             | Happy                                                            | Sad                                                              | Surprise                                                          |
|:--------------|:------------------------------------------------------------------|:------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------|-------------------------------------------------------------------|
| _Sentence_    | _Who is been repeating all that hard stuff to you?_               | _Our thanks to God's oath._                                       | _She had said, so that one could keep up a conversation!_        | _Monster made a deep bow._                                       | _How I hate this foul pool!_                                      |
| original      | <audio src="/wavs/original/7_11_0.wav" controls preload></audio>  | <audio src="/wavs/original/7_18_1.wav" controls preload></audio>  | <audio src="/wavs/original/7_7_2.wav" controls preload></audio>  | <audio src="/wavs/original/7_6_3.wav" controls preload></audio>  | <audio src="/wavs/original/7_15_4.wav" controls preload></audio>  |
| baseline      | <audio src="/wavs/baseline/7_11_0.wav" controls preload></audio>  | <audio src="/wavs/baseline/7_18_1.wav" controls preload></audio>  | <audio src="/wavs/baseline/7_7_2.wav" controls preload></audio>  | <audio src="/wavs/baseline/7_6_3.wav" controls preload></audio>  | <audio src="/wavs/baseline/7_15_4.wav" controls preload></audio>  |
| # 1           | <audio src="/wavs/model1/7_11_0.wav" controls preload></audio>    | <audio src="/wavs/model1/7_18_1.wav" controls preload></audio>    | <audio src="/wavs/model1/7_7_2.wav" controls preload></audio>    | <audio src="/wavs/model1/7_6_3.wav" controls preload></audio>    | <audio src="/wavs/model1/7_15_4.wav" controls preload></audio>    |
| # 2           | <audio src="/wavs/model2/7_11_0.wav" controls preload></audio>    | <audio src="/wavs/model2/7_18_1.wav" controls preload></audio>    | <audio src="/wavs/model2/7_7_2.wav" controls preload></audio>    | <audio src="/wavs/model2/7_6_3.wav" controls preload></audio>    | <audio src="/wavs/model2/7_15_4.wav" controls preload></audio>    |
| # 3           | <audio src="/wavs/model3/7_11_0.wav" controls preload></audio>    | <audio src="/wavs/model3/7_18_1.wav" controls preload></audio>    | <audio src="/wavs/model3/7_7_2.wav" controls preload></audio>    | <audio src="/wavs/model3/7_6_3.wav" controls preload></audio>    | <audio src="/wavs/model3/7_15_4.wav" controls preload></audio>    |
| **EmoSpeech** | <audio src="/wavs/emospeech/7_11_0.wav" controls preload></audio> | <audio src="/wavs/emospeech/7_18_1.wav" controls preload></audio> | <audio src="/wavs/emospeech/7_7_2.wav" controls preload></audio> | <audio src="/wavs/emospeech/7_6_3.wav" controls preload></audio> | <audio src="/wavs/emospeech/7_15_4.wav" controls preload></audio> |
