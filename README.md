## Overview
In this repository, I will explain how to develop software application using local large language models running entirely in your browser (e.g Qwen3.8-27B).
I will drop the demo application that I developed using these techniques

## What is 'Prompt Technique'?
There are many prompt techniques such as zero-shot prompt, few-shots prompt or structured output prompt. Here I will explain more in-depth about structured output prompt
and how a basic structured output prompt is highly effective when running models that are lesser capable in agentic coding.

## What is 'Qwen3.8-27B'?
Qwen3.8-27B is an open-weights model released by Alibaba Group. This model is regarded as highly capable among community posts in Reddit for being highly in its agentic coding capability. However, there are some limitations:
- This model can't zero-shot/one-shot complicated solutions or projects like Claude Opus 5.5
- This model by itself can only be ran on gaming rig with at least 32GB RAM and 16GB VRAM
- It is slower and less capable than frontier models, often requiring structured prompting.

## Harnessing the capability of Qwen3.8-27B
Although Qwen3.8-27B _cannot zero-shot/one-shot prompts_, it is still capable of reaching your desired output if your organize and structure your prompts properly.
When structuring prompts, you must set a clear goal or desired output. Divide your tasks and plan your strategy to achieve your desired goal. For example, a good strategy for developing an software entirely could be done using Software Development Life Cycle (SDLC):
|Stage|Process|
|---|---|
|Planning|
- Document your stuffs
- Add diagram|
|Requirements Analysis||
|System Design|Development|
|Testing||
