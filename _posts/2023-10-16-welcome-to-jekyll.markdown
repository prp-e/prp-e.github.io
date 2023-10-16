---
layout: post
title:  "Mistral 7B is all you need!"
date:   2023-10-16 21:26:00 +0330
categories: llms
---

It's been a long time since the very first _Large Language Model_ has been released? No. It's roughly around 6 years from the release of [GPT2](https://huggingface.co/gpt2) and it was somehow a revolutionary project. But today, we're talking about [Mistral 7B](https://mistral.ai) which is basically the newest champion of the league. 

## Mistral 7B

According to the Mistral AI website, this is how their new model works: 

> Mistral 7B is a 7.3B parameter model that:

    Outperforms Llama 2 13B on all benchmarks
    Outperforms Llama 1 34B on many benchmarks
    Approaches CodeLlama 7B performance on code, while remaining good at English tasks
    Uses Grouped-query attention (GQA) for faster inference
    Uses Sliding Window Attention (SWA) to handle longer sequences at smaller cost

and if you're interested in this model and want to have more information about it, you can check [this link](https://mistral.ai/news/announcing-mistral-7b/) out.

## Comparing with other models

In order to find out if this model is really good or not, I just hand picked my favorite language models which are listed below:

- gpt2
- gpt2-medium
- gpt-j-6b
- LLaMa 7B
- LLaMa-2 7B
- StableLM 3B
- gpt-neox-20B
- Phi 1.5B

and designed a very simple test to make a quick comparison between the models. In this simple test, I have defined some _tasks_ and each task means a group of prompts and the goal I had in my mind. Unfortunately, currently the test isn't really organized and as soon as I can put together everything I did, I will make it more organized (and therefore reliable.)

## Tasks

### Text Generation (T)

In this task, I just used English prompts and observed how the models are behaving. It is basically the first thing you usually try when you find these models.

### Instruction Following (Q)

In this task, I used _Alpaca_ question-answering style and observed the results. To make the comparison more fair, I _didn't_ use instruction-tuned models at all.

### Reasoning (R)

This is basically the same as the previous one, but with sligth difference. The instruction isn't as simple as asking the name of the first US president or boiling point of water. Here I just gave the model some reasoning questions/problems and honestly, it did a great job as well.

### Persian Text Generation (P)

This is the same as the task _T_. But with a little difference. I put my mother tongue in test. If you are going to try to repeat this, I should recommend doing this in your own language. For example if you speak Arabic, use Arabic as input. If you speak Portuguese, use that. 

At this point we can call this _Non-English_ task and not only Persian.

### Code Generation (C)

This is the same as the tasks _T_ and _P_ but with code generation experience. I personally tested python, js and basic HTML stuff. Not much :-)

## Results

![Results](https://github.com/prp-e/matplotlib_barchart/blob/main/barchart_models.png?raw=true)

## Conclusion 

Fine, it is apparent that Mistral wins the cup. But let me tell you what I found from this _not so quick_ test I did: 

- Mistral is good for pretty much most of the applications (even without being fine-tuned)
- Mistral can be a good base for fine tuning (on instructions, codes, other languages, etc.)

The next model I will study in depth would be _StableLM 3B_ since it also showed some promising results. So let me put everything together and make it short. _Mistral is tiny but mighty_.