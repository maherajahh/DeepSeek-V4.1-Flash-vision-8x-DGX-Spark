# DeepSeek-V4.1-Flash vision 8× DGX Spark

**Status: LIVE** (2026-10-17). Official weights. Vision proved (red PNG → “Red”). Text smoke: `PONG`.

Eight NVIDIA DGX Spark (GB10), tensor-parallel 8. We did not invent the kernels. This is an **8-rank** run with vision on, using Tony’s Spark vLLM patches and Magnus’s 8-rank launcher.

## What this is

| | |
|---|---|
| Model | `deepseek-ai/DeepSeek-V4.1-Flash` (official, MIT) |
| Hardware | 8× DGX Spark, dual fat rear links, `10.99.20.N` / `10.99.21.N` |
| Engine | vLLM overlay5, Tony patches, Magnus `nnodes=8` |
| Vision | `TEXT_ONLY=0`. Proved with a real image payload. |
| Context this boot | 300000 (`--max-model-len`) |

## What this is not

- Not Tony’s 4-box recipe claimed as ours
- Not Magnus’s uncensored weights (official DeepSeek only)
- Not a tok/s claim — none measured yet

## Credits

See [CREDITS.md](CREDITS.md). Order: DeepSeek → Tony → Magnus → vLLM.

## Gates

- [x] Official weights on all 8
- [x] Image + patches pinned (`pins.md`)
- [x] `/v1/models` id `deepseek-v4.1-flash`
- [x] Text smoke
- [x] Vision smoke
- [ ] Measured tok/s (empty until timed)

## License

MIT for *this* repo’s notes. Weights stay DeepSeek MIT. Tony’s and Magnus’s code stay theirs.
