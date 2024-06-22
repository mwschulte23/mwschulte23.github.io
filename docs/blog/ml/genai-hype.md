---
title: Generative AI Hype
date: 2024-06-10
description: Lots of hype with generative AI. Is it worth it?
tags:
  - genai
  - thoughts
---

# Hype Cycle
New technologies + salesmanship lead to the promise of a cool future &, for builders, a temporary window to participate. 

This + a dash of fear has fueld the gen AI hype cycle. The hype swept me up for a bit which distracted from a pragmatic approach to these new tools.

There are 3 angles worth putting on the table.

1. Why the hype?
2. What genAI is and isn't (to best of my knowledge)
3. A bettors take on the future

### Why the hype?
What these modesl can do is impressive. I've moved 80% of my research / troubleshooting to LLMs like Claude vs google, stack overflow, reddit, medium, etc.

But beyond that, I think there are 3 primary reasons for the hype.

1. First impressions. Gen AI capabilities are the most "human" of AI systems. It can listen, write & talk. It can take text and create lifelike images. This is eerily human-like.

2. Scale. These models effectively memorize the internet then are able intake a query, synthesize the internet & respond. It all creates an odd sense of grandeur.

3. Building. We have a whole new way to build software. A favorite of mine is unstructured input to structured output. Why? Say you are an ecomm site that wants to optimize product result pages. Well now, you can replace the 10+ filters with LLM powered search.

    * "Find 4+ star rated large black adidas hoodie under $50" -> returns 500 results
    * "One with a teal logo" -> returns 3 results, you pick one
    * "cool - find matching shorts" -> returns 2 teal colored shorts in your size

All of this to say - genAI generates excitement & fear, both amplify the topic.

### Things to Know About GenAI
Hype distracts from important aspects of these powerful models. Let's drill into a few on LLMs in particular

LLM training has 3 stages. 1) Collecting text data & turning it to numbers, 2) training the foundational model & 3) "instructing" it on how to best answer

#### Input Data
ML models learn complexity in N-dimensional features to generate a prediction then are evaluated on a holdout set. 

If holdout set, or data input at inference, is not representative of the training set...performance suffers. Or put plainly, models learn what they are given and no more.

Until emergent models, we can say a model trained on the internet is centered on average. We can prompt our way around this ("What is time? **think like Einstein** ") or look for models with carefully curated input data. Like Mixture of Experts (MoE) models.

**Action** Research input data for a model, understand the implications & use prompting to work around any challenges.

#### "Instruction"
The final step in training is "instruction" on how to best answer. This is where bias comes in. Humans entire the chat. 

This is good & bad. 

* Good: Without this tuning, model responses would be sub-optimal
* Bad: but also it is an avenue for political, religous, ideological, & other personal beliefs to forced into this powerful tech.

**Action** Stay intellectually honest & critical of model responses. Develop a set of test prompts to validate if any model fits your wants/needs.

*There is much more qualified folks debating emergence (e.g model goes beyond input data).*

### A Bettor's Take on the Future
There are lots of optimism, concerns & questions about the future. Will the rate of improvement in AI continue? Is genAI the path to general intelligence? Will AI replace knowledge workers? and so on

In 5-10 years, likelihood of outcomes (ignoring regulations & such)

* GenAI proves too unstable or costly for most use cases. **2.5%**
* Models follow a sigmoid, not an exponent. Growth plateaus in 2-3 years, but infrastructure & tooling for these tools does bring about a new phase in tech. **50%**
* Continued rapid growth for longer, 15% of knowledge work is replaced, but not AGI. **30%**
* Welcome AGI! I am your friend. **15%**
* No AGI! Don't! Stop... **2.5%**

I've gone on a mental journey on what this means, what should anyone do about it.

Odds are...you cannot impact the outcome so 1) keep learning & improving & 2) put important things first; family, friends, religion

