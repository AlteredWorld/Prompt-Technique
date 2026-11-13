# Local LLM Software Development with Structured Prompting

## Overview

This repository documents a workflow for developing software applications using **local large language models that run entirely in your browser** — no cloud, no API keys. The focus is on **structured output prompting**: a technique that unlocks reliable, high-quality results from smaller, locally-runnable models that would otherwise struggle with open-ended, multi-step coding tasks.

A demo application built with this workflow is included in this repository.

---

## Table of Contents

- [What is Structured Output Prompting?](#what-is-structured-output-prompting)
- [About the Model: Qwen3.8-27B](#about-the-model-qwen38-27b)
- [The Workflow: Harnessing a Smaller Model](#the-workflow-harnessing-a-smaller-model)
- [Demo: Flowchart Application](#demo-flowchart-application)

---

## What is Structured Output Prompting?

Prompt engineering covers a wide range of techniques — zero-shot, few-shot, chain-of-thought, and many others. This repository focuses specifically on **structured output prompting**, where the model is given an explicit format, schema, or set of constraints for its response.

Why does this matter for local models?

- **Frontier models** (e.g., Claude, GPT-4 class) can often produce a coherent solution from a single vague prompt.
- **Smaller local models** lack that implicit planning ability. Without structure, their output is inconsistent, incomplete, or off-target.
- **Structured prompting** compensates for that gap. By defining the expected output shape *before* the model generates, you turn an underpowered model into a reliable component of a development pipeline.

In short: a basic structured output prompt is disproportionately effective when the model's native agentic coding ability is limited.

---

## About the Model: Qwen3.8-27B

**Qwen3.8-27B** is an open-weights model released by Alibaba Group. It has gained a strong reputation in the community (see various threads on r/LocalLLaMA) for its agentic coding capability relative to its size.

### Strengths
- Strong agentic coding for a model that runs locally
- Open weights — no API dependency
- Runs entirely in the browser via WebGPU / WASM inference

### Limitations
| Constraint | Detail |
|---|---|
| Zero-shot / one-shot capability | Cannot produce a complete, multi-step solution from a single unstructured prompt the way a frontier model can |
| Hardware requirements | Requires a gaming-grade rig: **≥ 32 GB system RAM** and **≥ 16 GB VRAM** |
| Throughput | Slower and less capable than frontier models; benefits significantly from structured prompting |

---

## The Workflow: Harnessing a Smaller Model

Even though Qwen3.8-27B cannot reliably zero-shot a complex project, it **can** reach your desired output if you organize and structure your prompts deliberately. The core idea: **set a clear goal, decompose the work, and prompt each step with an explicit expected output.**

A basic strategy for developing a software application looks like this:

| Stage | What you do |
|---|---|
| **1. Planning** | Describe the application's purpose, its features, and the implementation approach. |
| **2. Breakdown** | Decompose the foundation and each feature into discrete, testable tasks. |
| **3. Prompting** | Write a structured prompt for each task. Adjust prompts as the application reaches milestones. |
| **4. Orchestration** | Design the overall pipeline: state clear goals, expected outputs, and acceptance tests for each step. |
| **5. Execution** | Feed the orchestration prompt to the model. Monitor its output and iterate where needed. |

> **Key principle:** The model is not a black box that you hope will "figure it out." It is a component that performs well when you give it a specific, well-shaped task.

## Demo: Flowchart Application
