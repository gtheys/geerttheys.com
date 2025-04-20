+++
title = "Exploring AI-Assisted Development: A Journey with My Side Project"
description = "Exploring AI-assisted development through a real project: insights on tools, challenges, and practical limitations when coding with AI assistants."
date = 2024-11-25
draft = false

[taxonomies]
tags = ["AI"]

[extra]
toc = true
thumbnail = "/images/Aider.jpg"
+++

{{img(src="/images/Aider.jpg" alt="Screenshot of Aider CLI")}}

I decided to dive back into machine learning through a hobby project, leveraging AI tools for development and deployment. Here's what I learned along the way.

<!-- more -->

## Development Environment and Tools

**AI Assistant Setup**
I primarily worked with aider-chat and Anthropic's Claude model. Due to API rate limits, I switched to openrouter for Claude access. While Ollama was an option, its limited context window proved challenging - even with the `--map-tokens 1024` parameter adjustment.

**IDE Evolution**
Initially, I stuck with neovim using avante.nvim, being a long-time vim user. However, I eventually migrated to VSCode for its more polished AI integration. While codecompanion.nvim looked promising, it wasn't quite ready for prime time.

**Technical Hurdles**
A particularly frustrating issue emerged from running Aider in PowerShell, which introduced Windows line endings. This caused problems with my Sagemaker oncreate scripts (`#!/usr/bin/bash^M`). Interestingly, AI couldn't help here - good old-fashioned log debugging saved the day.

## Infrastructure Setup

**AWS Architecture**
The project required Sagemaker, IAM, and S3 setup. Aider's /architect mode proved invaluable for initial design planning.

**IAM Challenges**
Managing IAM roles and permissions was tricky. The AI struggled with IAM's complexity just as a human would, especially when setting up separate data access for different users. While it generated clean IAM and S3 loops, we had to fix some redundant list definitions.

## Application Development

**Streamlit Implementation**
I built a straightforward Streamlit app for data upload and inference, outputting prediction CSVs. The AI assistance here felt like working with a junior developer - requiring constant guidance and context-setting. While it helped with features like authentication and S3 bucket integration, the hand-holding needed made me question its efficiency compared to working with human developers.

**Debugging and Testing**
AI excelled at generating detailed debug statements - a preference I have over visual debuggers. While I'm not a TDD enthusiast, AI efficiently generated initial test suites that needed minimal adjustments.

## Reflections on AI in Development

The experience highlighted that while AI can accelerate certain aspects of development, it's not a magic solution. It's most effective for:

- Generating boilerplate code
- Writing debug statements
- Creating initial test suites
- Quick function implementations

However, it still requires solid programming fundamentals and constant oversight. While it might reduce team sizes through efficiency gains, complete replacement of developers seems unlikely in the near term.
