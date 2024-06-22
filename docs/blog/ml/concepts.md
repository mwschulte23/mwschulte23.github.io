---
title: Important Concepts in Actually Using LLMs to Build
date: 2024-06-10
description: Organizing concepts & techniques for LLM use
tags:
  - concepts
---

There has been a disconnect between the LLM hype and applying LLMs to real-world problems. The cool ask questions, get answers chat app hyped into a new paradigm of building stuff didn't make sense to me. Hell, prompt engineering just seemed like a fancy way of saying "write good."

I'll breakdown the concepts & techniques that enable building with LLMs.

## Overview of Concepts
For me, you can breakdown the concepts into 3 stages:
1. Model Input: Prompt engineering, RAG, tools to use
2. Modeling: Pre-training & fine-tuning
3. Model Output: Structured output

Throughout these stages; there is plenty of opportunity for testing, validation, evaluation and guardrails. I'll touch on these a bit here but in more detail in the future.

### Model Input
Fundamentally, this is passing an LLM the needed information in the least text to get the desired output. The 3 primary components are

#### Prompt Engineering
Prompts are a user query or a system prompt, which "defines" an LLM. You'll see other variants but these are big two.

Say we have an "NBA bot" to keep up-to-date with NBA news & stats. Let's keep it simple by asking "Who is the best team in the NBA?"

This simple question has many interpretations (just watch ESPN for 10 minutes). Does best mean best record, finals winner, largest point differential per 100 possesions? Is user asking about current or past season, or maybe all-time? or just a subjective opinion?

A few simple, helpful tactis are
* Append "explain the reasoning for your answer" to the users query. This makes response clear even if not what user wants to know.
* Or we could be opinionated with our system prompt such as "You are an NBA expert who is focused on the most recent season, stats & news. You know past seasons as well, but you prioritize more recent activity."



Beyond the simple, easy tactics. We could use
* N-Shot prompting by adding examples into your prompt such as

"""
{user_query}. Explain the reasoning for your answer.

Here are a few examples:
* Who is the best player in the NBA? Nikola Jokic. He is the most recent MVP winner
* What is an important team stat?
"Who is the best player in the NBA?"; "The best player in the NBA is Nikola Jokic. He is the most recent MVP winner."
2. "What is an important team stat?"; "The most important team stat is turnovers."
"""

  * User: "Who is the best player in the NBA?"; LLM: "The best player in the NBA is Nikola Jokic. He is the most recent MVP winner."
  * User: "What is an important team stat?"; 


* Prompt Engineering: Okay, this is kinda just "write good" but with a more structured, nuanced approach.
* Retrieval Augmented Generation (RAG): Retrieving snippets of a domain specific corpus of text to add to your prompt.
* Tool Usage: Ability for LLM to access functions / code (this is sorta an input step...more to come on this)




### Modeling
You have pre-training which is term used for building foundational models and fine-tuning which is effectively transfer learning. My knowledge on this topic is limited but will just say...

There are many foundational models. They vary in size and capabilities which present lots of trade-offs of compute cost, latency and accuracy.

### Model Output
Structuring the output of an LLM enables a much better interface with software. Think of the difference between 

Being able to structure the output of a LLM is a huge deal. The difference between an LLM output of 

"The product is blue, XL and $10" vs "{'color': 'blue', 'size': 'XL', 'price': 10}" is a huge deal. 

This was the big unlock for me. It helped me truly understand the "paradigm shift."








## Walking Through an Example
We want to make a fun app that can answer questions about the NBA. A user can have a conversation with "NBA Bot."

#### Prompt Engineering & RAG

Techniques: N-shot, Chain-of-Thought and RAG

##### Contextualizing a Request
Let's take a basic prompt asking about the NBA playoffs - "Who is the best team in the NBA?"

* The seemingly simple request has many potential interpretations. Is it for the upcoming, current or past seasons? Or all-time best? What does "best team" mean? Would this user want more advanced stats to justify response or just simply best record or finals winner?
* Additionally, the LLM doesn't have access to NBA data. We'd need to include a search tool or, if data in database, a text-to-sql tool.
* There is also benefit in "defining" the LLM (system prompt), explaining different metrics & their meaning, add guidelines for answering questions, etc. This creates a body of text the LLM could reference (RAG)




* Append "explain the reasoning for your answer" to the prompt. This helps make sure the LLMs response is clear to the user even if doesn't answer user's true question.
* Look for context in earlier messages. If user is asking about recent events, it provides evidence that they're interested in the current season. Note, this is not as straight-forward as just appending text to a prompt.
* Add a preprocessing step where we ask LLM to "breakdown the user's request into subtasks." 


* Take the user prompt and add some guidelines such as appending "explain the reasoning for your answer"
* Can we get any context from earlier in conversation? Such as questions about current season or recent games.
* Add a decomposition step (e.g Chain-of-Thought) where you ask an LLM to break down the user's question into sub-tasks
  * For example, ask LLM to "Critically examine the user's request. Provide sub-tasks required to asnwer the question"
  * It might return "First, we need to determine what user means by best. Then, we need to consider which season(s). Finally, we need to lookup relevant rankings or stats"

The first bullet is a straightforward step to maintain clarity in LLMs response.

And is there any previous context in the conversation to infer more precise request?





- decomposing the question
- explaning the decomposition


Prompt engineering

RAG

Structured I/O

Workflows

Evaluation
