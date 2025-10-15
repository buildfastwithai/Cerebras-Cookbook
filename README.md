<div align="right">
  <a href="README.md">English</a> 
</div>

<p align="center">
  <img src="https://github.com/Shubhwithai/Cerebras-Cookbook/blob/main/images/cerebras%20logo.svg" alt="Cerebras Banner" width="800"/>
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
| **[Get Started](./get-started/)** | SDK setup guides, authentication, and model exploration examples |
| **[Agents](./agents/)** | AI agent implementations using Cerebras with CrewAI and Agno frameworks |
| **[Chat with Data](./chat-with-data/)** | RAG implementations, multilingual PDF chat, and fusion techniques |
| **[Integrations](./integrations/)** | Framework integrations including LiteLLM for seamless API switching |
| **[Starter Apps](./starter-apps/)** | Production-ready applications: AI book writer and mindmap generator |

## Cerebras Starter Guide

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/17BMZjby9ZZ6cJopyu4xWiAE6Nj3gNIBy?usp=sharing#scrollTo=ea1OXT-EBDCG)

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

- **Fast Inference**: Ultra-low latency inference with Cerebras Cloud
- **Model Zoo Integration**: Access to optimized pre-trained models
- **OpenAI-compatible API**: Easy migration from OpenAI to Cerebras
- **Streaming Support**: Real-time response streaming capabilities
- **Enterprise Ready**: Production-grade infrastructure and support


## Available Models

### Production Models

| Model | Model ID | Description | Use Cases |
|-------|----------|-------------|-----------|
| **Llama 4 Scout 17B** | `llama-4-scout-17b-16e-instruct` | High-performance instruction-tuned model | Chat, reasoning, code generation |
| **Llama 3.1 8B** | `llama3.1-8b` | Efficient general-purpose model | Text generation, summarization |
| **Llama 3.3 70B** | `llama-3.3-70b` | Large-scale model for complex tasks | Advanced reasoning, research |
| **OpenAI GPT OSS 120B** | `gpt-oss-120b` | Open-source GPT-style model | General text generation, chat |
| **Qwen 3 32B** | `qwen-3-32b` | Multilingual model with strong reasoning | Multilingual tasks, reasoning |

### Preview Models

| Model | Model ID | Description | Use Cases |
|-------|----------|-------------|-----------|
| **Llama 4 Maverick 17B** | `llama-4-maverick-17b-128e-instruct` | Extended context Llama 4 variant | Long-form content, extended reasoning |
| **Qwen 3 235B Instruct** | `qwen-3-235b-a22b-instruct-2507` | Large instruction-tuned model | Complex reasoning, advanced tasks |
| **Qwen 3 235B Thinking** | `qwen-3-235b-a22b-thinking-2507` | Reasoning-focused variant | Chain-of-thought, problem solving |
| **Qwen 3 480B Coder** | `qwen-3-coder-480b` | Specialized code generation model | Code generation, programming tasks |

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
