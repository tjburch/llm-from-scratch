---
title: "Chapter 1: Understanding Large Language Models"
date: "November 13, 2025"
---

Prior NLP models focused on straightforward pattern recognition, things like email spam filtering. Designed for specific tasks. LLMs are a departure from that.

Success comes from transformer architecture + a lot of data.

## 1.1 What is an LLM?

- It's a neural net, trained on basically the whole internet.
- Large -> both dataset and model size (hundreds of billions of parameters)
- Architecture is a transformer - pays selective attention to parts of the input
- Big key of NN-based ML in general is throwing out doing the feature extraction and letting it learn on the data.

## 1.2 Applications of LLMs

- Great for any task that involves parsing and generating text.

## 1.3 Stages of building and using LLMs

**Why?**

- Custom LLMs can outperform general purpose (e.g. BloombergGPT)
- Data privacy

**Process**

1. Pretraining - this is basically normal training in other models. Give it a bunch of data to fit on broadly, foundational resource. Called "base" or "foundation" model. GPTs are an example. 
2. Fine-tuning - focusing on specific tasks/domains. Train on labeled data.

Two popular kinds of fine tuning:

1. Instruction fine-tuning - instruction/answer pairs. "Translate" + translated text
2. Classification fine-tuning - texts and associated class labels. "Spam" vs "Not Spam," or "describes hot dog" vs "does not describe hot dog."

## 1.4 Introducitng the Transformer Architecture

[Attention is All You Need](https://arxiv.org/abs/1706.03762)

Input text is preprocessed, passes to an encoder which returns embedding vectors.

Decoder gets both the embedding vectors and partial output text and generates translated text one word at a time.

Both are deep neural nets with self-attention mechanisms - weighs the importance of tokens relative to each other to better capture long-range dependencies.

Next they talk about BERT (Bidirectional encoder representations from transformers) compared to GPT. BERT specializes in masked word prediction, contrasted to generative tasks. This is good for classification, like sentiment prediction or categorization. GPT focuses more on decoder side.


GPT is good at both:
- Zero-Shot learning - generalize with no examples
- Few-shot - a couple of examples to generalize from

