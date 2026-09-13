# Setup Guide

This document records the basic workflow used for the first local LLM deployment.

## Environment

- Windows PC
- Ollama
- Qwen3 0.6B

## 1. Install Ollama

Install Ollama from the official Ollama distribution and confirm that the application is running.

## 2. Download the model

From a terminal:

```bash
ollama pull qwen3:0.6b
```

## 3. Run the model

```bash
ollama run qwen3:0.6b
```

Enter a prompt and confirm that the model returns a response.

## 4. Verify offline inference

After the model has been downloaded:

1. disconnect the computer from the internet;
2. keep Ollama running;
3. run the model again;
4. send another prompt.

If the model still responds, inference is being performed locally using the already-downloaded model files.

## 5. Useful checks

List locally available models:

```bash
ollama list
```

Run the model again:

```bash
ollama run qwen3:0.6b
```

## What This Proves

This test demonstrates local model inference. It does **not** by itself mean that an application, RAG pipeline, or AI agent has been built.

Those are separate layers that can be added on top of Ollama.

## Planned Technical Next Step

Connect a small application to Ollama's local API so that another program can send prompts to the local model and receive responses programmatically.
