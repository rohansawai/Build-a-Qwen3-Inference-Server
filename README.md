## LLM Inference Server — Qwen3-4B, PyTorch, FastAPI
Built this LLM Inference Engine as a part of a problem on tensor tonic
https://www.tensortonic.com/projects/llm-inference/qwen3-inference-server

#### Built a transformer inference server from scratch, implementing KV-cached autoregressive decoding, temperature/top-k sampling, and byte-safe token streaming; benchmarked against an uncached baseline for a 4.5× latency reduction at 128-token generations.

#### Instrumented the serving path with TTFT, per-token latency, and throughput metrics, and exposed bounded /generate and /stream endpoints with request validation to cap per-request GPU occupancy.
