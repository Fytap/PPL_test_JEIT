# PPL Test Materials for JEIT Quantization Paper

This repository provides the prompt samples, inference configuration, and perplexity evaluation results used in the PPL experiment of the paper.

## Purpose

The repository is used as supplementary material for the paper on lightweight deployment and quantization of large language models. The PPL evaluation is conducted to analyze the language modeling quality of different quantized versions of Qwen3.6-35B-A3B.

## Evaluated Models

The evaluated models include:

* Qwen3.6-35B-A3B
* Qwen3.6-35B-A3B-AWQ-4bit
* Qwen3.6-35B-A3B-GPTQ-4bit
* Qwen3.6-35B-A3B-FP8

## Evaluation Data

The PPL evaluation uses text fragments sampled from the following datasets:

* WikiText-103
* C4-en
* LongBenchv2

Each dataset contains 100 text samples, and each sample is approximately 512 tokens.

## File Description

* `prompts/wikitext103_prompts.jsonl`: Prompt samples from WikiText-103
* `prompts/c4_en_prompts.jsonl`: Prompt samples from C4-en
* `prompts/longbenchv2_prompts.jsonl`: Prompt samples from LongBenchv2
* `results/ppl_results.csv`: PPL results reported in the paper
* `configs/vllm_ppl_config.md`: vLLM serving and benchmark configuration

## PPL Results

| Model                     | KV Cache Quantization | WikiText PPL |  C4 PPL | LongBench PPL |
| ------------------------- | --------------------- | -----------: | ------: | ------------: |
| Qwen3.6-35B-A3B           | No                    |       8.2479 | 10.9861 |        5.5431 |
| Qwen3.6-35B-A3B-AWQ-4bit  | No                    |       8.2870 | 11.0180 |        5.5554 |
| Qwen3.6-35B-A3B-GPTQ-4bit | No                    |       8.2768 | 11.0404 |        5.5650 |
| Qwen3.6-35B-A3B-FP8       | No                    |       8.3715 | 11.0990 |        5.6076 |

## Notes

The materials in this repository are provided for reproducibility. No private data, API keys, passwords, SSH keys, or server credentials are included.
