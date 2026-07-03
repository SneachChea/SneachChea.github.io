---
layout: single
title:  "GraKelX and some thoughts about open source at the edge of AI"
date:   2026-07-03
---

# It all starts with GraKeL

Since I started working at Pasqal, I've been diving into some mathematical problems that affect a wide audience 🥲... graph theory and graph machine learning, to be more precise.
I won't go too deep into my work, but for the sake of context: when publishing some research, I had to benchmark classic graph kernels (for those interested, here's the latest [publication](https://arxiv.org/abs/2509.09421v2)). That's how I naturally stumbled upon [GraKeL](https://github.com/ysig/GraKeL/), an open-source package stemming from the research work of Ioannis Siglidis. The package itself is quite impressive. I believe it's the only one in its category: a graph kernel Python package compatible with scikit-learn. Using it to compare our work against the existing state of the art was a no-brainer.

## The problem with GraKeL

On paper, the package has going for it:

- It's open-source with a permissive license (BSD-3).
- It performs well.
- It's designed to be compatible with one of the most popular machine learning packages out there.

Its main issue? It's not maintained. The author addresses this in the README, calling on the community to help with a potential handoff. I don't know the current status of that transition, but the last merge on the main branch dates back to July 2025, and the last release on PyPI is from 2023. In the world of software development, that's an eternity — and it leads to a few practical problems. For instance, the PyPI version is no longer compatible with numpy >= 2.0.0, so you have to install it via git clone. A bug prevented the `__repr__` method of a GraKeL Graph object from working properly. And some much-needed features are missing, most notably compatibility with other Python graph packages (I'm thinking of networkx or torch geometric).

That said, I'm not here to blame the GraKeL maintainers. They've done tremendous work, and *above all*, they owe us nothing.

## My solution

I chose to fork GraKeL and create [GraKelX](https://github.com/SneachChea/GraKelX). I hesitated for a long time between creating a new package versus submitting PRs to the original. What convinced me to go with a fresh start was the desire to respect the original authors' choices and philosophy while steering GraKelX in the direction I envisioned. One radical aspect of this is that I rely heavily on AI assistants to maintain it and I know that can be a point of friction for some. Another reason, simpler and more pragmatic, is that GraKeL's BSD license allows it. Even though the name has changed, I remain a huge fan of Ioannis's work, and it is (and will remain) credited and referenced throughout GraKelX's documentation.

## What is GraKelX?

For now, GraKelX stays very close to GraKeL. There have been a few revisions — notably dropping Python 2, modernizing the codebase (with a lot of help from my buddy Opencode), and, well, a name change. So there's no major divergence from the original yet, though that may change over time.
One important thing to note: GraKelX is a personal project. While I may end up using it for work, I've exclusively used my own tools (laptop, AI assistants, etc.) and dedicated my free time to it.

You're welcome to submit PRs or open issues! For now, I have enough free time to handle reviews. I'm still fairly new to open-source tool maintenance, so if you have any advice to share, I'm all ears.

# My thoughts on open source and AI

I have mixed feelings about open source and code assistants like Claude Code, GitHub Copilot, or Opencode. On the one hand, I find their capabilities truly impressive when guided well enough. It's really thanks to my AI agents that I can maintain and develop GraKelX: understanding source code quickly, scaffolding simple features (like converting graph objects across different packages), and debugging with ease. I also use them to figure out how to set up things like CI pipelines, automated releases, and more. In short, I can barely code without them anymore. They also flatten the learning curve for other projects of mine. I, for instance, started building websites with their help. It's far from perfect, but once you understand what they're doing under the hood, you can achieve incredible things!

So where does this mixed feeling come from? I think it stems from two points I tend to overlook. The first is that by delegating so much to machines, we lose part of our understanding of the problems we're solving. I haven't implemented new kernels in GraKelX yet, but the day I have to, I wouldn't trust an AI to do it on its own. I'd then have to pay the entry cost of understanding GraKelX's codebase.
The second point is more philosophical. These AIs were trained on open-source code. Maybe even on Ioannis's code! LLMs therefore belong at least slightly to the community and yet it's clear to me that the companies developing them will give back far less to the open-source community than they've taken from it.
Let's not even talk about what happens when subscription costs skyrocket.
