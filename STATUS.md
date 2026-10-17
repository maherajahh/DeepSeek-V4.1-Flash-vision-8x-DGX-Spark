# Status

**LIVE.** 2026-10-17. Official DeepSeek-V4.1-Flash, TP8, vision on.

API model id: `deepseek-v4.1-flash`  
`--max-model-len` this boot: **300000** (not 1M yet).

| Item | State |
|------|--------|
| Official V4.1 weights | on all 8 (`/var/tmp/models/DeepSeek-V4.1-Flash`, 48/48 shards) |
| Image | `vllm-dsv41:overlay5` Id `sha256:c92feb5ffab6…` (created 2026-10-17T08:57:33Z) |
| 8-rank launch | all 8 containers `vllm_dsv41` up |
| `/v1/models` | id `deepseek-v4.1-flash` |
| Text smoke | `PONG` |
| Vision smoke | 64×64 red PNG → **Red** (`TEXT_ONLY=0`) |
| tok/s | **not measured** — do not invent |

Fingerprint: `vllm-0.28.1rc1.dev388+g8a728663c-tp8-26dde7df`
