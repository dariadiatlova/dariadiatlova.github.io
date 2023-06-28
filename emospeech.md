---
layout: default
title: EmoSpeech: guiding FastSpeech2 towards Emotional Text to Speech
---

[Paper](https://openreview.net/pdf?id=LYgrzXwVsm) [Code](https://github.com/deepvk/emospeech)

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

## Audio samples

### Speaker 0011

| Model                                 | Neutral                                                          | Angry                                               | Happy                                 | Sad                                    | Surprise                         |
|:--------------------------------------|:-----------------------------------------------------------------|:----------------------------------------------------|---------------------------------------|----------------------------------------|----------------------------------|
| _Sentence_                            | _The football teams give a tea party._                           | _Who is been repeating all that hard stuff to you?_ | _Rat came and replied on the leaves._ | _The football teams give a tea party._ | _As rich as Peter's son in law!_ |
| original                              | <audio src="/wavs/original/1_22_0.wav" controls preload></audio> | nice                                                |                                       |                                        |                                  |
| # 0 baseline (Expressive FastSpeech2) | good and plenty                                                  | nice                                                |                                       |                                        |                                  |
| # 1 (0 + `eGeMAPS`)                   | good `oreos`                                                     | hmm                                                 |                                       |                                        |                                  |
| # 2 (1 + `CLN`)                       | good `zoute` drop                                                | yumm                                                |                                       |                                        |                                  |
| # 3 (1 + `CCA`)                       | good `zoute` drop                                                | yumm                                                |                                       |                                        |                                  |
| **EmoSpeech** (4 + `JCU`)             | good `zoute` drop                                                | yumm                                                |                                       |                                        |                                  |
