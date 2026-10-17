# Pins

Verified on spark1 2026-10-17 with `docker image inspect` and git rev-parse.

| Item | Value | Verified |
|------|--------|----------|
| Weights repo | `deepseek-ai/DeepSeek-V4.1-Flash` | yes |
| Weights path | `/var/tmp/models/DeepSeek-V4.1-Flash` | yes |
| Tony recipe commit | `d45538f` | yes |
| Magnus 8-rank commit | `d6dace7` | yes |
| vLLM image | `vllm-dsv41:overlay5` | yes |
| Image id | `sha256:c92feb5ffab6f15cb5d1330abd448ef1664a6f13bfeae616982b73bf2a4baaf9` | yes |
| TEXT_ONLY | `0` | yes |
| GMU / max-model-len | `0.75` / `300000` | yes |
| Fabric | `10.99.20.1`–`.8` rank 0–7 | yes |
