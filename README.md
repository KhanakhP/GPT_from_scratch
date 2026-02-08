# GPT From Scratch

This repository contains an implementation of a GPT-style Transformer language model built from scratch, along with code to load pretrained weights into the same architecture for inference and experimentation.

The project focuses on understanding and reproducing the internal mechanics of GPT models rather than relying on high-level abstractions.

---

## Project Scope

This repository has two main objectives:

1. Implement the GPT decoder-only Transformer architecture from first principles  
2. Load pretrained weights into the custom implementation when architectural compatibility is satisfied  

This is not a large-scale training project and does not attempt to replicate ChatGPT or any proprietary system.

---

## Implemented Components

- Token embeddings  
- Positional embeddings  
- Causal (masked) multi-head self-attention  
- Transformer blocks with residual connections  
- Feedforward (MLP) layers  
- Layer normalization  
- Autoregressive text generation  
- Pretrained weight loading into a matching architecture  

---

## Model Architecture

The model follows the standard GPT design:

- Decoder-only Transformer  
- Causal attention masking  
- Fixed context length  
- Identical layer structure required for weight loading  

Pretrained weights can only be loaded when:

- Number of layers matches  
- Hidden dimension size matches  
- Attention head count matches  
- Parameter ordering and tensor shapes are identical  

Any deviation will result in incompatible tensors.

---

## Pretrained Weights

This repository demonstrates how pretrained GPT-style weights can be loaded into a custom implementation when the architecture matches exactly.

Notes:

- No pretrained weights are redistributed  
- Weight loading is intended for learning and experimentation  
- Shape mismatches are explicitly surfaced during loading  

---

## Motivation

Most GPT usage hides the internals behind libraries and APIs.

This project exists to make the model structure explicit and understandable by building it step by step.

---

