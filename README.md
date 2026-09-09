**LLM Inference Server** — Qwen3-4B, PyTorch, FastAPI, Pydantic

- Implemented autoregressive generation from scratch in PyTorch, including chat-template prompt construction, temperature and top-k sampling, and greedy decoding.
- Added KV-cached decoding to eliminate redundant prefix computation, cutting latency 4.5× at 128 tokens versus an uncached baseline while verifying bit-identical greedy output; profiled the prefill (compute-bound) and decode (memory-bandwidth-bound) phases on an NVIDIA L4, sustaining ~20 tok/s against a ~37 tok/s bandwidth ceiling.
- Served generation over FastAPI with streaming and non-streaming endpoints, Pydantic-validated request bounds, and TTFT/latency/throughput metrics returned inline for client-side profiling.

- Built this LLM Inference Engine as a part of a problem on tensor tonic
https://www.tensortonic.com/projects/llm-inference/qwen3-inference-server
