<div align="right">
  <a href="README.md">English</a> |
  <a href="README.hi.md">हिंदी (Hindi)</a> |
  <a href="README.ko.md">한국어 (Korean)</a> |
  <a href="README.es.md">Español (Spanish)</a>
</div>

<p align="center">
  <img src="https://github.com/Shubhwithai/Cerebras-Cookbook/blob/main/images/cerebras-banner.svg" alt="Cerebras Banner" width="800"/>
</p>

<p align="center">
  <a href="https://cloud.cerebras.ai/"><img src="https://img.shields.io/badge/API-Active-success.svg" alt="API Status"></a>
  <a href="https://docs.cerebras.ai/"><img src="https://img.shields.io/badge/Docs-Available-blue.svg" alt="Documentation"></a>
  <a href="https://inference-docs.cerebras.ai/"><img src="https://img.shields.io/badge/Inference-Ready-orange.svg" alt="Inference"></a>
  <a href="https://github.com/Cerebras"><img src="https://img.shields.io/github/stars/Cerebras?style=social" alt="GitHub Stars"></a>
  <a href="https://twitter.com/CerebrasSystems"><img src="https://img.shields.io/twitter/follow/CerebrasSystems?style=social" alt="Twitter Follow"></a>
</p>

## Overview

Cerebras Systems builds the world's largest computer chip - the **Wafer Scale Engine (WSE)** - designed specifically for AI workloads. This cookbook provides comprehensive examples, tutorials, and best practices for developing and deploying AI models using Cerebras infrastructure, including both training on WSE clusters and fast inference via Cerebras Cloud.

## What You'll Find in This Repository

| Section | Description |
|---------|-------------|
| **Get Started** | Quick setup guides, API authentication, and your first model |
| **Inference Examples** | Fast inference with Cerebras Cloud API and various model implementations |
| **Training Recipes** | Large-scale model training on Wafer-Scale Engine clusters |
| **Model Zoo Integration** | Working with pre-trained models from Cerebras Model Zoo |
| **Performance Optimization** | Tips for maximizing WSE performance and efficiency |
| **Integration Guides** | Connecting Cerebras with popular ML frameworks (PyTorch, Hugging Face) |
| **Production Deployment** | Best practices for deploying models at scale |
| **Starter Apps** | Ready-to-use application templates and demos |

## Cerebras Starter Guide

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1j7B8mDIU8KMZ_IB-oaL_qLqXmWYYh0Xu)

## Get Your API Key

Get your API key by visiting [Cerebras Cloud](https://cloud.cerebras.ai/).

⚠️ **Security Note:** Keep your API key secure! Never expose it in client-side code or public repositories.

### API Endpoint

```
https://api.cerebras.ai/v1/chat/completions
```

## Quick Start

### Prerequisites

- A Cerebras account
- A Cerebras Inference API key
- Python 3.7+ or Node.js 14+

### Set up your API key

```bash
export CEREBRAS_API_KEY="your-api-key-here"
```

### Install the Cerebras SDK

```bash
pip install --upgrade cerebras_cloud_sdk
```

### Sample Code

#### Python

```python
import os
from cerebras.cloud.sdk import Cerebras

client = Cerebras(
    api_key=os.environ.get("CEREBRAS_API_KEY"),
)

chat_completion = client.chat.completions.create(
    messages=[
        {
            "role": "user",
            "content": "Explain the advantages of wafer-scale computing for AI",
        }
    ],
    model="llama-4-scout-17b-16e-instruct",
)

print(chat_completion.choices[0].message.content)
```

#### cURL

```bash
curl -X POST "https://api.cerebras.ai/v1/chat/completions" \
  -H "Authorization: Bearer $CEREBRAS_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "llama-4-scout-17b-16e-instruct",
    "messages": [
      {"role": "user", "content": "What makes Cerebras WSE unique for AI training?"}
    ],
    "max_tokens": 1024,
    "temperature": 0.7
  }'
```

#### JavaScript/Node.js

```javascript
import { Cerebras } from 'cerebras_cloud_sdk';

const client = new Cerebras({
    apiKey: process.env.CEREBRAS_API_KEY,
});

async function main() {
    const chatCompletion = await client.chat.completions.create({
        messages: [
            {
                role: 'user',
                content: 'How does wafer-scale architecture improve AI performance?',
            },
        ],
        model: 'llama-4-scout-17b-16e-instruct',
    });

    console.log(chatCompletion.choices[0].message.content);
}

main();
```

## Features

- **Wafer-Scale Training**: Leverage the world's largest chip for unprecedented training speed
- **Fast Inference**: Ultra-low latency inference with Cerebras Cloud
- **Model Zoo Integration**: Access to optimized pre-trained models
- **OpenAI-compatible API**: Easy migration from OpenAI to Cerebras
- **Streaming Support**: Real-time response streaming capabilities
- **Enterprise Ready**: Production-grade infrastructure and support

## Repository Structure

```
cerebras-cookbook/
├── getting-started/          # Setup guides and first steps
├── inference/               # Cerebras Cloud inference examples
│   ├── chat-completions/   # Chat and completion examples
│   ├── streaming/          # Streaming response examples
│   └── tool-use/           # Function calling examples
├── training/               # WSE training recipes
│   ├── nlp/               # Language model training
│   ├── computer-vision/   # Vision model training
│   └── multimodal/        # Multimodal training
├── model-zoo/             # Cerebras Model Zoo examples
├── integrations/          # Framework integrations
│   ├── pytorch/           # PyTorch integration
│   ├── huggingface/       # Hugging Face integration
│   └── langchain/         # LangChain integration
├── optimization/          # Performance tuning guides
├── production/            # Deployment best practices
├── starter-apps/          # Ready-to-use applications
└── utils/                 # Utility scripts and helpers
```

## Available Models

| Model | Description | Use Cases |
|-------|-------------|-----------|
| **Llama-4-Scout-17B** | High-performance instruction-tuned model | Chat, reasoning, code generation |
| **Llama-3.1-8B** | Efficient general-purpose model | Text generation, summarization |
| **Llama-3.1-70B** | Large-scale model for complex tasks | Advanced reasoning, research |

## Resources

- **Documentation**: [Cerebras Docs](https://docs.cerebras.ai)
- **Inference API**: [Inference Documentation](https://inference-docs.cerebras.ai)
- **Training API**: [Training Documentation](https://training-api.cerebras.ai)
- **Model Zoo**: [Cerebras Model Zoo](https://github.com/Cerebras/modelzoo)
- **SDK**: [Python SDK](https://github.com/Cerebras/cerebras-cloud-sdk-python) | [Node.js SDK](https://github.com/Cerebras/cerebras-cloud-sdk-node)
- **Playground**: [Try Cerebras Cloud](https://cloud.cerebras.ai)
- **Live Demo**: [Cerebras Inference Demo](https://inference.cerebras.ai)

## Getting Support

- **Issues**: Report bugs or request features via [GitHub Issues](https://github.com/Shubhwithai/Cerebras-Cookbook/issues)
- **Documentation**: Visit [Cerebras Documentation](https://docs.cerebras.ai)
- **Contact**: Reach out to Cerebras support team

### Video Tutorial

[![Watch the video](https://img.youtube.com/vi/dQw4w9WgXcQ/maxresdefault.jpg)](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

## Contributing

We welcome contributions to the Cerebras-Cookbook repository! To contribute:

1. Fork and clone the repository
2. Create a new branch for your changes
3. Make your changes following our documentation standards
4. Test your examples thoroughly
5. Submit a pull request

For major changes, please open an issue first to discuss your ideas.

### Contribution Guidelines

- Include clear documentation and comments
- Provide example usage and expected outputs
- Follow the existing code style and structure
- Add appropriate tests where applicable
- Update the README if adding new sections

## Legal

- [Privacy Policy](https://cerebras.ai/privacy)
- [Terms of Service](https://cerebras.ai/terms)

---

© 2025 Cerebras Systems | All Rights Reserved