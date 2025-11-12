# Day 1: vLLM Production Deployment

Deployed `mistralai/Mistral-7B-Instruct-v0.3` with vLLM + OpenAI API.

## Server Command
```bash
vllm.entrypoints.openai.api_server \
  --model mistralai/Mistral-7B-Instruct-v0.3 \
  --tensor-parallel-size 1 \
  --max-model-len 4096 \
  --gpu-memory-utilization 0.95 \
  --port 8000
