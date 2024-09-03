---
layout: post
title: Engineering over AI
permalink: /engineering-over-ai/
---
For the last few months, I have been working on something [new](https://callstack.ai) - building code generating LLM agents that actually work and produce high fidelity results.

The space is probably in peak of its hype curve and it seems like many teams have lost focus on what really matters, the engineering part. There's just too many GPT wrappers with nice interfaces posting too good to be true demos and raising large rounds.

As a result, the overinflated valuations with low returns have created a general scepticism amongst investors and customers. VCs are cooling down as they don't get the ROI they have been sold on. The users are sceptical that LLM apps can actually bring the expected value which makes it harder to sell for others.

But hey, no one cares. And fortunately, there's a cure. It's called engineering over AI. 

Engineering over AI is everything but optimizing prompts and orchestrating agents. Engineering over AI is solving real engineering problems and using AI as the enabling layer based on a technical foundation. 

## Generating code
In the space of code generation agents, we have decided to take a step back and solve the context part first instead of focusing on agents.

![llm-flow](/assets/images/llm-flow.png)

Why? It's necessary if you care about building anything remotely functional. It turns out, generating good code is not difficult given the model has the right context. But there's a slight problem with today's default approach. It relies on embeddings as the context layer.

Embeddings offer great semantic understanding. However, codebases are of a structural nature. Primarily on 2 levels. The file level and the logic level. 

Files are organized in a hierarchy representing high-level relationships. On the other hand the logic level is defined by functions, classes, methods, and variables which represent chunks of low-level logic which the code performs. Embeddings do not understand this. 

This is also the reason why the higher context window doesn't matter. Even if you could feed your whole codebase into an LLM, you'd still face the same problem of missing the structural relationships of the codebae.

Understanding code is the enabling layer for code generation applications. It's the main problem. It's engineering over AI.