# A Hack for Creating a High-Quality Dataset for LLM Instruction Tuning

**Paper:** [A hack to create a high-quality dataset for LLM instruction tuning](https://arxiv.org/abs/2406.08464)

**Quick Implementation:**
The basic idea of this hack is quite simple, consisting of 2 main steps:
- **Step 1:** Prompt an Instruct model (llama 3, phi-3) with a pre-query template to generate an instruction.
- **Step 2:** Feed the instruction generated in Step 1 back into the LLM to obtain a response.

This is a completely automated approach that does not require the creation of seed tasks, unlike the method employed by the Self-Instruct paper for constructing a dataset for instruction finetuning.

Surprisingly, with the instruction dataset built using this method, you can fine-tune a Llama 3 8B base model solely with instruction finetuning, without needing to perform preference tuning (DPO, RLHF). This instruct model can even outperform the original model instructed by Meta AI.
