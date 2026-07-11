---
date: '2026-07-10T18:57:27Z'
title: 'Predictions on AI (read Transformers)'
tags: ['AI']
---

For the past few weeks I've been thinking about transformers[^1] and there limitations (also propelled by my job which has me working closely with mlsys). Before I give you my take on the current state of AI let me give a quick disclaimer.
    
> **Disclaimer:** While I know the architecture and workings of neural networks in general, and transformers in particular, I am no [Mechanistic Interpretability](https://en.wikipedia.org/wiki/Mechanistic_interpretability) expert or even versed enough ,to my liking ofcourse, ahmm (Imposter), to be making this claims.

Having made that clear let's talk about the limitations.

### Non Limitations

I said I was gonna talk about limitations but I lied. From the architecture of NNs and also transformer one thing is clear to me that I will write as a conjecture.

**Conjecture** : *Scaled enough the present architecture(transformer) can solve arbitrarily complex problems*

This would trigger a lot of people and some would think I am retarded or something but let me give my justification.  
Firstly, this conjecture is driven by some of the [achievements](https://cs.stanford.edu/~knuth/papers/claude-cycles.pdf) of modern AI. When most of us had our first encounter with chat bots like ChatGPT , starting with GPT3, we all could see it being capable of a little bit of **reasoning** but it struggled a lot with simple math problems like multiplying numbers, counting letters in the word etc. When it came to programming it could spit out some spaghetti for a small enough task. But with increase in model size and some architectural changes (not to the core but rather tokenizer) it became better at reasoning, programming or any other intellectual activity. So if you do some extrapolation from here it is not that hard to see why it wouldn't become more better as you scale.  
Also I want to approach this from the perspective of the problem that the bot is solving. What is it about harder problems ,say for example making a production grade compiler or solving an unsolved problem or proving a yet unproven conjecture, that makes it non-amenable to AI ,in comparison to, simple problems (like writing a program for factorial or taking a derivative).  

One could say **novelty**. Writing factorial and taking derivatives is easy because it is present in training, in huge amount. But solution to yet unsolved problem is not in the training. But present AI can do things which are not in training directly.For example training a new CodeForces problem which is brand new. You could say it has seen **similar** problem to that in the training, but if it could identify the similarity and apply the technique in novel scenario it (in theory) should able to do it for harder problems with enough scaling. (Refer to the Knuth paper above).  
And if novelty is the only hard line between the type of problems (like P vs NP , and we don't know about that one too), then it should be able to cover most of the intellectual industry because in reality how many of the things we think or do are truly novel.

Also what does **"scaled enough"** mean? I mean aren't we training multi-trillion parameter models already? To put it simply, what I mean here, is the entire world's compute and some more. I am open to discussions about this but until I setup comments you can message me on [Mastodon](https://mastodon.social/@PKDrinker) or [X](https://x.com/PriyanshuKalal1). Now let's talk about limitations.

### Limitations

Most of the limitations which I would elaborate here are propelled by juxtaposition of present ai architectures with human brain.

1. The first is efficacy at long range tasks. No matter how good a model is it has a fixed context length. That is not a problem if a task is small but it becomes a problem on big task. That is not problematic in on itself, but what makes it problematic is even if some model is working on the same task for 100th time it would still need to put all things it discovered before in context again. For example, this problem is clear to anyone who has used AI agents in large projects (millions of LOC). While the present consensus is to use files like Agents.md or Claude.md for giving context it is just a hack around that limitation. There is no way for it to continuously evolve which is exactly the second point.
1. For human brains training run never ends. Training and inference goes hand in hand which is starkly different from the transformer. This, in my view, is a severe limitation which forces the previous limitation. An architecture that evolves dynamically with usage would be a lot better and neuromorphic.

### Conclusion

I wanted to write more about the limitations but I put all my effort in explaining non-limitations that I could only give a little idea of limitation, but I think it is good enough to show the direction in which one should be thinking with neural network if we want anything close to ASI. But that would not be a problem because if creating ASI is a hard problem and hard problems are not that different from easy problem than present ai should be able to do that. (AKA recursive-self improvement).

> **Reflection:** To be honest, this post reads like some lunatic spilling some in-trend terms and could've been much better, I promise to be more technical next time.


[^1]: Mandatory [paper](https://arxiv.org/abs/1706.03762) reference.
