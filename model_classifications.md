# Model Classifications

This file tracks free models available from NVIDIA NIM, OpenRouter, and DeepSeek,
grouped by Claude-style tiers (Opus/Sonnet/Haiku) and ordered from most to least
capable within each tier.

Ordering rationale:
- NVIDIA NIM and DeepSeek tiers follow DeepSeek V4 Pro > V4 Flash > V3.2 benchmark
  results (SWE-Bench Verified, SimpleQA, LongBench-V2) plus MiniMax M2.7 > M2.5 >
  GLM-5 ranking from BenchLM / LLM-Stats composite scores.
- OpenRouter tiers follow SWE-Bench Verified scores and the OpenRouter free-models
  collection rankings (April 2026).

---

## NVIDIA NIM (Free Endpoints)

### Opus-tier (frontier / highest capability)
# Most powerful → least powerful
- nvidia_nim/deepseek-ai/deepseek-v4-pro      # 1.6T params, 1M ctx; #2 on AA Intelligence Index; 81% SWE-Bench
- nvidia_nim/minimaxai/minimax-m2.7            # 230B MoE; BenchLM score 63, PinchBench 86.2%, 5th overall; coding #1 contender
- nvidia_nim/minimaxai/minimax-m2.5            # 230B MoE; SWE-Bench 80.2%, beats GPT-5.2 on coding
- nvidia_nim/deepseek-ai/deepseek-v4-flash     # 284B MoE, 1M ctx; approaches Pro on simple agent tasks
- nvidia_nim/deepseek-ai/deepseek-v3.2         # 685B, prior frontier; below V4-Flash on official tables
- nvidia_nim/z-ai/glm5                         # GLM-5, BenchLM score 83 overall but weaker on SWE coding vs MiniMax

### Sonnet-tier (strong general / coding)
# Most powerful → least powerful
- nvidia_nim/z-ai/glm4.7                       # GLM-4.7, strong general open model; repo default
- nvidia_nim/marin/marin-8b-instruct           # Marin 8B, reasoning/math/science optimised, Free Endpoint
- nvidia_nim/google/gemma-7b                   # Gemma 7B, solid mid-size open model, Free Endpoint
- nvidia_nim/mediatek/breeze-7b-instruct       # Breeze 7B, bilingual chat/coding, Free Endpoint

### Haiku-tier (smaller / efficient)
# Most powerful → least powerful
- nvidia_nim/google/gemma-3n-4b                # Gemma 3n 4B, 8K context, free
- nvidia_nim/google/gemma-3n-2b                # Gemma 3n 2B, 8K context, free


---

## OpenRouter (Free Models)

In Settings use: open_router/<model_id>  (the :free suffix is part of the model ID)

### Opus-tier
# Most powerful → least powerful
- open_router/xiaomi/mimo-v2-flash:free                        # 309B MoE; #1 open-source SWE-Bench; matches Claude Sonnet 4.5 on coding
- open_router/qwen/qwen3-coder-480b-a35b-instruct:free         # 480B MoE; top coding/reasoning, 262K ctx
- open_router/nvidia/nemotron-3-super-120b:free                # 120B hybrid MoE; leading on AIME 2025, TerminalBench, SWE-Bench; 1M ctx
- open_router/mistralai/devstral-2:free                        # 123B dense coding model; multi-file orchestration; 256K ctx

### Sonnet-tier
# Most powerful → least powerful
- open_router/qwen/qwen3-next-80b:free                         # 80B MoE; agents/RAG/tool-use optimised, 262K ctx
- open_router/meta-llama/llama-3.3-70b-instruct:free           # 70B dense; GPT-4-class general model, 128K ctx
- open_router/google/gemma-3n-27b:free                         # 27B; strong multilingual + multimodal, 33K ctx

### Haiku-tier
# Most powerful → least powerful
- open_router/meta-llama/llama-4-maverick:free                 # Compact frontier, long context, strong tool use
- open_router/meta-llama/llama-4-scout:free                    # Ultra-long ctx, fast inference frontier-small
- open_router/google/gemma-3n-4b:free                          # 4B open-weight, edge/fast


---

## DeepSeek (Official API — Free Credits / Free Tier)

DeepSeek provides generous free credits on signup and a free-tier for V3/V4/R1.

### Opus-tier
# Most powerful → least powerful
- deepseek/deepseek-v4-pro       # 1.6T MoE, 1M ctx; strongest reasoning + agentic tasks; 81% SWE-Bench
- deepseek/deepseek-v4-flash     # 284B MoE, 1M ctx; approaches Pro on simple tasks; 12x cheaper inference
- deepseek/deepseek-v3.2-exp     # V3.2 experimental; below V4-Flash on official benchmark tables

### Sonnet-tier
# Most powerful → least powerful
- deepseek/deepseek-v3.2         # V3.2 stable release; strong general chat/code
- deepseek/deepseek-v3.1-terminus  # V3.1 hybrid-inference "terminus" variant
- deepseek/deepseek-chat         # V3 stable identifier (deepseek-chat); proven general model

### Haiku-tier
# Most powerful → least powerful
- deepseek/deepseek-r1           # Chain-of-thought reasoning traces; stronger on complex logic
- deepseek/deepseek-reasoner     # Reasoning-focused alias endpoint; lighter / faster
