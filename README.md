# LFM2 (Liquid Foundation Model 2) tinygrad Implementation

This version is adapted to load pretrained weights from Hugging Face Hub.

## Get started

- Install dependencies:

    `pip install tinygrad torch transformers huggingface_hub safetensors tqdm`

- Starts `main.py`:

    `python main.py`

- You'll see this output

```
--- Loading LFM2 Model: LiquidAI/LFM2-350M ---

Model configuration:
Layer 0: Convolution
Layer 1: Convolution
Layer 2: Attention
Layer 3: Convolution
Layer 4: Convolution
Layer 5: Attention
Layer 6: Convolution
Layer 7: Convolution
Layer 8: Attention
Layer 9: Convolution
Layer 10: Attention
Layer 11: Convolution
Layer 12: Attention
Layer 13: Convolution
Layer 14: Attention
Layer 15: Convolution

Initializing model architecture...
Fetching weights from LiquidAI/LFM2-350M/model.safetensors...
Loading and assigning weights...
Re-tying word embeddings for lm_head...
All weights loaded and assigned.

Loading tokenizer...

--- Starting Text Generation ---
Formatted Prompt (decoded): <|startoftext|><|im_start|>user
The secret to a long and happy life is<|im_end|>
<|im_start|>assistant

Processing prompt...
Generating new tokens...
<|startoftext|><|im_start|>user
The secret to a long and happy life is<|im_end|>
<|im_start|>assistant
  0%|                                                                                                                                                                                                                                      | 0/49 [00:00<?, ?it/s]   2%|████▌                                                                                                                                                                                                                         | 1/49 [00:02<01:56,  2.44s/it]   4%|█████████                                                                                                                                                                                                                     | 2/49 [00:04<01:41,  2.15s/it]   6%|█████████████▌                                                                                                                                                                                                                | 3/49 [00:06<01:39,  2.17s/it]   8%|██████████████████                                                                                                                                                                                                            | 4/49 [00:08<01:37,  2.16s/it]  10%|██████████████████████▋                                                                                                                                                                                                       | 5/49 [00:10<01:36,  2.18s/it]  12%|███████████████████████████▏                                                                                                                                                                                                  | 6/49 [00:13<01:37,  2.28s/it]  14%|███████████████████████████████▋                                                                                                                                                                                              | 7/49 [00:15<01:37,  2.32s/it]  16%|████████████████████████████████████▏                                                                                                                                                                                         | 8/49 [00:18<01:35,  2.34s/it]  18%|████████████████████████████████████████▊                                                                                                                                                                                     | 9/49 [00:21<01:45,  2.63s/it]  20%|█████████████████████████████████████████████                                                                                                                                                                                | 10/49 [00:24<01:44,  2.68s/it]  22%|█████████████████████████████████████████████████▌                                                                                                                                                                           | 11/49 [00:26<01:41,  2.66s/it]  24%|██████████████████████████████████████████████████████                                                                                                                                                                       | 12/49 [00:30<01:45,  2.86s/it]  29%|███████████████████████████████████████████████████████████████▏                                                                                                                                                             | 14/49 [00:36<01:46,  3.05s/it]  31%|███████████████████████████████████████████████████████████████████▋                                                                                                                                                         | 15/49 [00:39<01:46,  3.14s/it]  33%|████████████████████████████████████████████████████████████████████████▏                                                                                                                                                    | 16/49 [00:42<01:40,  3.06s/it]  35%|████████████████████████████████████████████████████████████████████████████▋                                                                                                                                                | 17/49 [00:45<01:37,  3.04s/it]  37%|█████████████████████████████████████████████████████████████████████████████████▏                                                                                                                                           | 18/49 [00:50<01:46,  3.45s/it]  41%|██████████████████████████████████████████████████████████████████████████████████████████▏                                                                                                                                  | 20/49 [00:56<01:35,  3.30s/it]:

 47%|███████████████████████████████████████████████████████████████████████████████████████████████████████▋                                                                                                                     | 23/49 [01:08<01:38,  3.80s/it]  49%|████████████████████████████████████████████████████████████████████████████████████████████████████████████▏                                                                                                                | 24/49 [01:14<01:44,  4.19s/it]H 51%|████████████████████████████████████████████████████████████████████████████████████████████████████████████████▊                                                                                                            | 25/49 [01:17<01:33,  3.91s/it]* 55%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████▊                                                                                                   | 27/49 [01:27<01:40,  4.55s/it]  57%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████▎                                                                                              | 28/49 [01:31<01:33,  4.45s/it]  61%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████▎                                                                                     | 30/49 [01:42<01:35,  5.03s/it]  63%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████▊                                                                                 | 31/49 [01:47<01:29,  4.96s/it]  65%|████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████▎                                                                            | 32/49 [01:51<01:22,  4.84s/it]  69%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████▎                                                                   | 34/49 [02:01<01:12,  4.82s/it]  71%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████▊                                                               | 35/49 [02:05<01:05,  4.70s/it]  73%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████▎                                                          | 36/49 [02:12<01:07,  5.16s/it]  76%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████▉                                                      | 37/49 [02:16<01:00,  5.01s/it]  78%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████▍                                                 | 38/49 [02:24<01:02,  5.69s/it]  80%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████▉                                             | 39/49 [02:29<00:55,  5.56s/it].
 86%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████▍                               | 42/49 [02:46<00:40,  5.85s/it]  88%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████▉                           | 43/49 [02:51<00:33,  5.62s/it]M 90%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████▍                      | 44/49 [02:57<00:27,  5.56s/it]f 92%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████▉                  | 45/49 [03:04<00:24,  6.07s/it]  94%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████▍             | 46/49 [03:13<00:20,  6.95s/it]  96%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████▉         | 47/49 [03:18<00:13,  6.50s/it]  98%|████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████▍    | 48/49 [03:26<00:06,  6.78s/it]-100%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 49/49 [03:31<00:00,  4.32s/it]

--- Generation Complete ---

Final generated text:
<|startoftext|><|im_start|>user
The secret to a long and happy life is<|im_end|>
<|im_start|>assistant
The secret to a long and happy life is a combination of various factors, including but not limited to:

1. **Health**: Regular exercise, a balanced diet, and adequate sleep are fundamental.
2. **Mindfulness and Mental Well-being
```


## Acknowledgment

> Heavily inspired from https://github.com/kyegomez/LFM2 and official https://github.com/huggingface/transformers/blob/main/src/transformers/models/lfm2/modeling_lfm2.py implementation

## Disclaimer

- Empirical test with `debug_prefilling.py` shows huggingface implementation apply final norm inside final layer.

This is output when final norm is applied inside layer 15

```
--- Starting Step-by-Step tinygrad Comparison ---
--- Comparing: Initial Embeddings ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=0.000040, PT=0.000040
  Max absolute difference: 0.000000
  ✅ MATCH: Tensors are numerically close.
----------------------------------------
--- Comparing: RoPE Cos ---
  Shapes: TG=(1, 4, 64), PT=(1, 4, 64)
  Means:  TG=0.936163, PT=0.936163
  Max absolute difference: 0.000000
  ✅ MATCH: Tensors are numerically close.
------------------------------
--- Comparing: RoPE Sin ---
  Shapes: TG=(1, 4, 64), PT=(1, 4, 64)
  Means:  TG=0.086091, PT=0.086091
  Max absolute difference: 0.000000
  ✅ MATCH: Tensors are numerically close.
------------------------------
--- Comparing: Layer 0 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.000293, PT=-0.000293
  Max absolute difference: 0.000000
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 1 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.000917, PT=-0.000917
  Max absolute difference: 0.000001
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 2 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=0.000082, PT=0.000082
  Max absolute difference: 0.000001
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 3 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=0.000129, PT=0.000129
  Max absolute difference: 0.000001
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 4 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.000286, PT=-0.000286
  Max absolute difference: 0.000001
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 5 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=0.000247, PT=0.000247
  Max absolute difference: 0.000001
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 6 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=0.000444, PT=0.000444
  Max absolute difference: 0.000002
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 7 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.006097, PT=-0.006097
  Max absolute difference: 0.000067
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 8 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.006024, PT=-0.006024
  Max absolute difference: 0.000067
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 9 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.006152, PT=-0.006152
  Max absolute difference: 0.000067
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 10 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.006291, PT=-0.006291
  Max absolute difference: 0.000067
  ✅ MATCH: Tensors are numerically close.
-------------------------------------
--- Comparing: Layer 11 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.006382, PT=-0.006382
  Max absolute difference: 0.000067
  ✅ MATCH: Tensors are numerically close.
-------------------------------------
--- Comparing: Layer 12 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.006064, PT=-0.006064
  Max absolute difference: 0.000067
  ✅ MATCH: Tensors are numerically close.
-------------------------------------
--- Comparing: Layer 13 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.006869, PT=-0.006869
  Max absolute difference: 0.000067
  ✅ MATCH: Tensors are numerically close.
-------------------------------------
--- Comparing: Layer 14 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.003247, PT=-0.003247
  Max absolute difference: 0.000070
  ✅ MATCH: Tensors are numerically close.
-------------------------------------
--- Comparing: Layer 15 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.005748, PT=-0.005748
  Max absolute difference: 0.000732
  ✅ MATCH: Tensors are numerically close.
-------------------------------------
--- Comparing: Final Logits ---
  Shapes: TG=(1, 4, 65536), PT=(1, 4, 65536)
  Means:  TG=-2.157017, PT=-2.157017
  Max absolute difference: 0.000174
  ✅ MATCH: Tensors are numerically close.
----------------------------------

🎉🎉🎉 All checks passed! The models match perfectly. 🎉🎉🎉
```

And this when it's applied after layer 15:
```
--- Starting Step-by-Step tinygrad Comparison ---
--- Comparing: Initial Embeddings ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=0.000040, PT=0.000040
  Max absolute difference: 0.000000
  ✅ MATCH: Tensors are numerically close.
----------------------------------------
--- Comparing: RoPE Cos ---
  Shapes: TG=(1, 4, 64), PT=(1, 4, 64)
  Means:  TG=0.936163, PT=0.936163
  Max absolute difference: 0.000000
  ✅ MATCH: Tensors are numerically close.
------------------------------
--- Comparing: RoPE Sin ---
  Shapes: TG=(1, 4, 64), PT=(1, 4, 64)
  Means:  TG=0.086091, PT=0.086091
  Max absolute difference: 0.000000
  ✅ MATCH: Tensors are numerically close.
------------------------------
--- Comparing: Layer 0 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.000293, PT=-0.000293
  Max absolute difference: 0.000000
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 1 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.000917, PT=-0.000917
  Max absolute difference: 0.000001
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 2 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=0.000082, PT=0.000082
  Max absolute difference: 0.000001
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 3 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=0.000129, PT=0.000129
  Max absolute difference: 0.000001
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 4 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.000286, PT=-0.000286
  Max absolute difference: 0.000001
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 5 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=0.000247, PT=0.000247
  Max absolute difference: 0.000001
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 6 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=0.000444, PT=0.000444
  Max absolute difference: 0.000002
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 7 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.006097, PT=-0.006097
  Max absolute difference: 0.000067
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 8 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.006024, PT=-0.006024
  Max absolute difference: 0.000067
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 9 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.006152, PT=-0.006152
  Max absolute difference: 0.000067
  ✅ MATCH: Tensors are numerically close.
------------------------------------
--- Comparing: Layer 10 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.006291, PT=-0.006291
  Max absolute difference: 0.000067
  ✅ MATCH: Tensors are numerically close.
-------------------------------------
--- Comparing: Layer 11 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.006382, PT=-0.006382
  Max absolute difference: 0.000067
  ✅ MATCH: Tensors are numerically close.
-------------------------------------
--- Comparing: Layer 12 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.006064, PT=-0.006064
  Max absolute difference: 0.000067
  ✅ MATCH: Tensors are numerically close.
-------------------------------------
--- Comparing: Layer 13 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.006869, PT=-0.006869
  Max absolute difference: 0.000067
  ✅ MATCH: Tensors are numerically close.
-------------------------------------
--- Comparing: Layer 14 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.003247, PT=-0.003247
  Max absolute difference: 0.000070
  ✅ MATCH: Tensors are numerically close.
-------------------------------------
--- Comparing: Layer 15 Output ---
  Shapes: TG=(1, 4, 1024), PT=(1, 4, 1024)
  Means:  TG=-0.000973, PT=-0.005748
  Max absolute difference: 29.115623
  ❌ MISMATCH: Tensors are NOT close.
-------------------------------------

‼️ DIVERGENCE DETECTED AT LAYER 15 ‼️
```