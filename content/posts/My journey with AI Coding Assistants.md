+++
title = "My Journey with AI Coding Assistants"
description = "A developer's honest journey using AI coding assistants, exploring tools like AIDER and Claude, while sharing practical insights about their limitations and game-changing potential in software development."
date = 2025-01-17
draft = false

[taxonomies]
tags = ["Opinion", "AI", "engineering"]

[extra]
toc = false
thumbnail = "/images/conductor.jpg"
+++
{{img(src="/images/conductor.jpg" alt="Orchestra conductor")}}

After months of coding with [LLMs](https://en.wikipedia.org/wiki/Large_language_model), I've finally gathered enough experience to share my thoughts on how these tools are changing our field.

<!-- more -->

The Tools I've Played With
I've mainly used [AIDER](https://github.com/paul-gauthier/aider), [VSCode](https://code.visualstudio.com/) with [Cline](https://github.com/celine-s-wang/cline) and [Continue](https://continue.dev/). I quickly dropped Continue since it didn't work with [local LLMs](https://github.com/topics/local-llm) - and I'm big on privacy, so local LLMs are my thing. I do pay for [openrouter](https://openrouter.ai/) as I can experiment with online models. My preferred model would be [Claude Sonnet](https://www.anthropic.com/claude).

AIDER has been fantastic, especially for a CLI lover like me. It does everything - writes code, shows diffs, handles git commits, and even reads terminal output. Pretty amazing stuff. But I eventually moved to Cline in VSCode, mainly because of something called Model Context Protocol (more on that later). Same reason I use Claude - their desktop app has this built-in.

## The Good, The Bad, and The Reality Check
Let me tell you - working with LLMs is both amazing and frustrating at the same time.

These tools are smart - they can read your code, understand git trees, and generally get what you're trying to do. But there's a catch: context limits. You keep sending files and chat history, and before you know it, you've hit the limits or your bill is climbing.

Here's what I've learned works best: keep tasks small. Start fresh chats often. It's like talking to a new developer each time - they need to be brought up to speed on everything. Sure, you can use prompts to help, but it still feels like onboarding someone new repeatedly.

And don't get me started on the context window issues. Sometimes it just forgets what it did elsewhere in the code. Like this one time, I had AWS_PROFILE set up system-wide, but the LLM went ahead and hardcoded regions in new code anyway. Little things like that pop up all the time.

## The Game Changer: Model Context Protocol
This is where things get interesting. With [Model Context Protocol](https://modelcontextprotocol.github.io/), I can let LLMs interact with other systems, but on my terms. No sketchy keylogging or screen capture stuff like what [MS Copilot](https://github.com/features/copilot) and [ChatGPT](https://openai.com/chatgpt) are doing.

I've set it up to pull [JIRA](https://www.atlassian.com/software/jira) tickets for context and even update ticket status with git commits. Even cooler - I'm using it with [Playwright](https://playwright.dev/) and [Puppeteer](https://pptr.dev/) for testing. Recently built a login/registration flow, and the LLM actually ran the tests itself. No manual testing needed!

## What I've Learned
Look, LLMs have definitely made me more productive, but you've got to stay alert. It's like having a really smart junior developer - helpful but needs supervision.

These days, developers need to be analysts, code wranglers, and QA all rolled into one. With LLMs, we can move faster and deliver better quality code - as long as we understand their limitations and keep our hands on the wheel.

Will this reduce the number of developers needed? Probably. Will it replace us completely? Not with current tech, and honestly, probably never will. But that's just my take after working with these tools day in, day out.