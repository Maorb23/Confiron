# Confiron

**Find the right model. Prove it on your workload. Tune it for performance.**

Confiron brings model discovery, validation, and inference optimization into one workflow. Go from a workload description to evidence-backed model choices and measured serving configurations—with control over your GPU budget.

## From model choice to measured performance

- **Discover with evidence.** Find Hugging Face models for your task, hardware, and budget. Review research sources, pinned model revisions, and compatibility findings before committing compute.
- **Validate on your terms.** Check inference behavior, quality, latency, and context handling. Bring your own Hugging Face datasets to make evaluations relevant to your application.
- **Optimize intelligently.** Use Bayesian optimization to guide configuration search across vLLM, SGLang, and TensorRT-LLM. Target higher throughput, lower latency, or a balance of both, with service-level constraints and explicit trial budgets.
- **See where time goes.** Inspect startup, warmup, benchmark, and cleanup timings alongside server logs and trial diagnostics. Reuse prepared workloads, skip duplicate configurations, and resume saved studies.
- **Keep the evidence.** Compare configurations through saved metrics, persistent study history, downloadable artifacts, and independent candidate validation in the experiment lab.

## How it works

1. **Describe your workload** or select a model you want to assess.
2. **Connect your resources** and choose datasets, frameworks, GPUs, and search budgets.
3. **Review the study** with its pinned model, frozen workload, execution settings, and cost assumptions.
4. **Approve execution** and follow remote GPU jobs, trials, and diagnostics.
5. **Compare results** and choose a configuration against your performance requirements.

Use the web application for guided discovery and study review, or the CLI and notebooks for hands-on experimentation. Dry runs let you inspect the workflow before allocating GPUs; live studies run on Nebius with your configured credentials and worker images.

## Why Confiron

Model rankings alone do not tell you how a model will behave on your data—or which serving settings will make it useful. Confiron connects those decisions: research informs the shortlist, validation checks behavior, and measured optimization explores the performance tradeoffs.

Bayesian search aims to find strong configurations with fewer measurements than an exhaustive grid. Results depend on the model, workload, hardware, and search budget. Measured runs, simulations, and offline estimates remain clearly distinguished.

## Explore the platform

Confiron unifies two complementary projects: [hf_validator](https://github.com/Maorb23/hf_validator) and [llm-optimizer-trt](https://github.com/Maorb23/llm-optimizer-trt).

| Component | Role | Documentation |
| --- | --- | --- |
| **Model discovery and validation** (`hf_validator`) | Recommendations, evaluation, datasets, web study review, and orchestration | [Setup and workflows](https://github.com/Maorb23/hf_validator/blob/main/README.md) |
| **Inference optimization** (`llm-optimizer`) | Bayesian search, framework benchmarking, persistent studies, and execution telemetry | [Optimizer guide](https://github.com/Maorb23/llm-optimizer-trt/blob/main/README.md) |

Start with the [web application setup](https://github.com/Maorb23/hf_validator/blob/main/README.md#run-the-web-app-locally), explore [model recommendations](https://github.com/Maorb23/hf_validator/blob/main/README.md#1-recommendation), or run [Bayesian optimization directly](https://github.com/Maorb23/llm-optimizer-trt/blob/main/README.md#bayesian-optimization).

The optimizer extends [BentoML LLM Optimizer](https://github.com/bentoml/llm-optimizer) with Optuna-based search and native TensorRT-LLM support. An optional [NVIDIA Dynamo AI Configurator integration](https://github.com/Maorb23/llm-optimizer-trt/blob/main/docs/trtllm-dynamo.md) adds offline deployment sizing alongside measured engine tuning.
