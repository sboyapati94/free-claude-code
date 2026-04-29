# Model Classifications

This file tracks free models available from NVIDIA NIM, OpenRouter, and DeepSeek, grouped by Claude-style tiers (Opus/Sonnet/Haiku) and ordered from most to least capable within each tier.

## NVIDIA NIM (Free Endpoints)

### Opus-tier (frontier / highest capability)
- nvidia_nim/deepseek-ai/deepseek-v4-pro  # DeepSeek V4 Pro, 1M context, frontier reasoning[cite:46]
- nvidia_nim/deepseek-ai/deepseek-v4-flash  # DeepSeek V4 Flash, 1M context, fast MoE[cite:52]
- nvidia_nim/deepseek-ai/deepseek-v3.2  # DeepSeek V3.2, 685B reasoning LLM[cite:41]
- nvidia_nim/z-ai/glm5  # GLM-5, close-to-Opus reasoning[cite:62]
- nvidia_nim/minimaxai/minimax-m2.7  # MiniMax M2.7, 230B MoE coding/reasoning[cite:58][cite:65]
- nvidia_nim/minimaxai/minimax-m2.5  # MiniMax M2.5, 230B coding/reasoning[cite:66][cite:65]

### Sonnet-tier (strong general / coding)
- nvidia_nim/z-ai/glm4.7  # GLM-4.7, strong open model used as default[cite:17][cite:59]
- nvidia_nim/google/gemma-7b  # Gemma 7B Free Endpoint[cite:40]
- nvidia_nim/marin/marin-8b-instruct  # Marin 8B Instruct Free Endpoint[cite:45]
- nvidia_nim/mediatek/breeze-7b-instruct  # Breeze 7B Instruct Free Endpoint[cite:48]

### Haiku-tier (smaller / efficient)
- nvidia_nim/google/gemma-3n-4b  # Gemma 3n 4B (free, 8K context)[cite:1]
- nvidia_nim/google/gemma-3n-2b  # Gemma 3n 2B (free, 8K context)[cite:1]


## OpenRouter (Free Models)

Model IDs here are written without provider prefix in the first segment; in Settings they should be used as `open_router/<model_id>`, typically with a `:free` suffix where required.

### Opus-tier
- open_router/nvidia/nemotron-3-super-120b:free  # Nemotron 3 Super 120B hybrid MoE[cite:27][cite:33]
- open_router/qwen/qwen3-coder-480b-a35b-instruct:free  # Qwen3 Coder 480B MoE[cite:24][cite:27]
- open_router/mistralai/devstral-2:free  # Devstral 2 123B coding model[cite:27]
- open_router/xiaomi/mimo-v2-flash:free  # MiMo-V2-Flash 309B MoE, top coding[cite:27]

### Sonnet-tier
- open_router/meta-llama/llama-3.3-70b-instruct:free  # Llama 3.3 70B GPT-4-class[cite:24][cite:27]
- open_router/google/gemma-3n-27b:free  # Gemma 3n large variant free[cite:27]
- open_router/qwen/qwen3-next-80b:free  # Qwen3-Next 80B, agents/RAG[cite:27]

### Haiku-tier
- open_router/meta-llama/llama-4-maverick:free  # Llama 4 Maverick frontier-small[cite:24]
- open_router/meta-llama/llama-4-scout:free  # Llama 4 Scout efficient frontier[cite:50]
- open_router/google/gemma-3n-4b:free  # Gemma 3n 4B open-weight[cite:27]


## DeepSeek (Official API Models with Free Credits / Free Tier)

DeepSeek official API exposes these primary models; the platform provides generous free credits on signup plus a robust free tier for V3/V4/R1 variants.[cite:6][cite:12][cite:34]

### Opus-tier
- deepseek/deepseek-v4-pro  # DeepSeek V4 Pro frontier model[cite:37][cite:12]
- deepseek/deepseek-v4-flash  # DeepSeek V4 Flash fast MoE frontier[cite:37][cite:52]
- deepseek/deepseek-v3.2-exp  # DeepSeek V3.2 experimental variant[cite:37][cite:3]

### Sonnet-tier
- deepseek/deepseek-v3.2  # DeepSeek V3.2 main chat model[cite:41][cite:3]
- deepseek/deepseek-v3.1-terminus  # DeepSeek V3.1 Terminus hybrid inference[cite:49][cite:37]
- deepseek/deepseek-chat  # DeepSeek V3 chat identifier[cite:34][cite:37]

### Haiku-tier
- deepseek/deepseek-r1  # DeepSeek R1 reasoning model (thinking traces)[cite:34][cite:37]
- deepseek/deepseek-reasoner  # DeepSeek reasoning-focused endpoint[cite:37]

