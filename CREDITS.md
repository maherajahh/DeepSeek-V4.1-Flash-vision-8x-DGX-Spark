# Credits

Order is load-bearing. Do not reorder in public posts.

## 1. DeepSeek

- Model: [deepseek-ai/DeepSeek-V4.1-Flash](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash)
- Native vision (DeepSeek-ViT + projector) and 1M context are theirs.

## 2. Tony / Tech2Wild (Kai)

- Recipe: [tonyd2wild/DeepSeek-V4.1-Flash-vLLM-DGX-Spark](https://github.com/tonyd2wild/DeepSeek-V4.1-Flash-vLLM-DGX-Spark)
- This is a **4-Spark** kit. Vision is on in his boot-10 path (`TEXT_ONLY=0`), not in the text-only default.
- We are not the authors of those patches.

## 3. Magnus

- 8-rank stretch: [im0xMagnus/deepseek-v4.1-flash-uncensored-8x-dgx-spark](https://github.com/im0xMagnus/deepseek-v4.1-flash-uncensored-8x-dgx-spark)
- He carried Tony’s launcher to eight ranks and left vision on.
- His published weights are dealignai uncensored. **This notebook uses official DeepSeek weights**, not that edit.

## 4. Engine

- vLLM `dsv41-feat` / nightly pins — recorded in `pins.md` when we have a live image
- FlashInfer SM120/SM121 kernels as used by Tony’s overlay

## 5. This notebook

- Lab: 8× DGX Spark (GB10) + CRS804 fabric. Operator: trx696.

If a public sentence sounds like we invented 8-wide DeepSeek serving, it is wrong. Fix it.
