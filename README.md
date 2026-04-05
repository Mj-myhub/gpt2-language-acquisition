# GPT-2 Language Acquisition

Fine-tuning GPT-2 on child-directed speech from the CHILDES database to explore question formation, text completion, and psycholinguistically motivated generalisation in early language development.

This repository is based on my master's thesis in **Language and Mind: Linguistics and Cognitive Studies** at the **University of Siena**. The project explores whether transformer-based language models can capture aspects of language acquisition by training GPT-2 on child-directed speech and evaluating their behaviour on targeted linguistic tasks.

## Why this project matters

Large language models are often evaluated on broad NLP benchmarks, but much less often on linguistically motivated tasks connected to language development. This project takes a different approach by testing GPT-2 on tasks inspired by child language acquisition, including wh-questions, aux-less questions, and morphological generalisation.

The goal is not just to see whether the model produces fluent text, but to examine how well it handles structured linguistic phenomena and whether performance changes systematically with scale.

## Project Overview

I fine-tuned GPT-2 at three different scales:

- **117M**
- **345M**
- **774M**

The models were trained on **child-directed speech from the CHILDES database** and evaluated on three main areas:

1. **Wh-question understanding**
   - subject wh-questions
   - object wh-questions
   - who-questions

2. **Aux-less question processing**
   - child-like ill-formed question structures
   - question answering and text completion tasks

3. **Morphological generalisation**
   - plural
   - past tense
   - adjective formation
   - singular possessive
   - third-person singular

## Key Results

| Model | Subject wh-questions | Object wh-questions | Who-questions |
|------|------:|------:|------:|
| GPT-2 117M | 20% | 14% | 42% |
| GPT-2 345M | 46% | 36% | 62% |
| GPT-2 774M | **72%** | **74%** | **78%** |

Performance improved consistently with model scale, especially on wh-question understanding, showing clear scaling-law patterns across the experiments.

## Visual Summary

![GPT-2 accuracy on wh-question benchmarks](results/gpt2_wh_question_results.png)

This figure shows wh-question accuracy across the 117M, 345M, and 774M GPT-2 models, with clear improvements as model scale increases.

## Method

This project combines ideas from **computational linguistics**, **psycholinguistics**, and **transformer-based NLP**.

The workflow was:

- collect and prepare child-directed speech data from CHILDES
- fine-tune GPT-2 models at different scales
- design targeted evaluation tasks
- compare model behaviour across linguistic phenomena
- analyse how scale affects performance and generalisation

## Research Focus

This project sits at the intersection of:

- computational linguistics
- large language models
- language acquisition
- transformer evaluation
- psycholinguistically motivated NLP

## Repository Structure

```text
gpt2-language-acquisition/
│
├── README.md
├── notebooks/
├── data/
├── results/
└── thesis/
