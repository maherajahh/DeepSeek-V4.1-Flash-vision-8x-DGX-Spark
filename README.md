# Maherajahh

DeepSeek-V4.1-Flash on 8× DGX Spark (vision on)

**Status: NOT LIVE.** Empty recipe notebook. No weights pulled. Office GLM-5.3-Flash is still serving.

Eight NVIDIA DGX Spark (GB10) boxes, tensor-parallel 8, official DeepSeek-V4.1-Flash, **pictures on**. This is not a 2-box or 4-box kit.

We did not invent the kernels. We are writing down an **8-rank** run with vision proved on this fabric.

## What this is

| | |
|---|---|
| Model | `deepseek-ai/DeepSeek-V4.1-Flash` (official, MIT) |
| Hardware | 8× DGX Spark, dual fat rear links, `10.99.20.N` / `10.99.21.N` |
| Engine | vLLM, Tony’s Spark patches, 8-rank launch |
| Vision | Required. `TEXT_ONLY=0`. A screenshot must be described before we call it done. |
| Context | Target 1,048,576 once serving is proved |

## What this is not

- Not Tony’s 4-box recipe claimed as ours
- Not Magnus’s uncensored weights (we use official)
- Not sumsliu speed-only 8-wide (no vision proof here)
- Not GLM-5.3-Flash (that is already live on these boxes until we switch)

## Credits (read first)

See [CREDITS.md](CREDITS.md). Short version:

1. **DeepSeek** — the model
2. **tonyd2wild / Tech2Wild (Kai)** — the Spark vLLM recipe this 8-rank job is built from
3. **im0xMagnus** — the 8-rank stretch of Tony’s launcher, vision flag on
4. **vLLM / FlashInfer** — the engine

## Gates (none passed yet)

- [ ] Official weights on spark1, copied to spark2–8
- [ ] Image + patches pinned (digests in `pins.md`)
- [ ] `/v1/models` returns an id
- [ ] Text smoke
- [ ] **Vision smoke** (a real photo, not “the flag is on”)
- [ ] Measured tok/s written here (no guesses)

## Voice

Public posts only quote this repo. Draft rules: [VOICE.md](VOICE.md).

## License

MIT for *this* repo’s scripts and notes. Model weights stay under DeepSeek’s MIT. Tony’s and Magnus’s code stay theirs — we pin and credit; we do not re-host their trees as our invention.
