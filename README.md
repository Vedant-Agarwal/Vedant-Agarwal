### Vedant Agarwal

ML infrastructure engineer. I build the data and ML platforms that models train and serve on, and fix correctness bugs in the open-source LLM stack.

- **Now:** search signal infrastructure at Walmart Global Tech: real-time Flink and Kafka pipelines on GCP, a shared feature platform for ranking and personalization, and drift monitoring across 100+ production signals.
- **Going deep on:** LLM inference and agent infrastructure: KV-cache capacity, batching, and long-horizon agent evaluation.

#### Open source

**28 merged pull requests across 13 projects**, mostly shared-state, resource-leak and serialization bugs.

| Area | Merged |
|---|---|
| LLM pipelines | [Haystack](https://github.com/deepset-ai/haystack/pulls?q=is%3Apr+author%3AVedant-Agarwal) (6) |
| Fine-tuning and LLM gateways | [PEFT](https://github.com/huggingface/peft/pulls?q=is%3Apr+author%3AVedant-Agarwal) (3), [LiteLLM](https://github.com/BerriAI/litellm/pulls?q=is%3Apr+author%3AVedant-Agarwal) (2) |
| Agent and LLM evaluation | [Inspect Evals](https://github.com/UKGovernmentBEIS/inspect_evals/pulls?q=is%3Apr+author%3AVedant-Agarwal) (3), [Harbor](https://github.com/harbor-framework/harbor/pulls?q=is%3Apr+author%3AVedant-Agarwal) (3), [HELMET](https://github.com/princeton-nlp/HELMET/pulls?q=is%3Apr+author%3AVedant-Agarwal), [inspect-evals-lint](https://github.com/Generality-Labs/inspect-evals-lint/pulls?q=is%3Apr+author%3AVedant-Agarwal) |
| ML platform and data | [MLflow](https://github.com/mlflow/mlflow/pulls?q=is%3Apr+author%3AVedant-Agarwal) (2), [Feast](https://github.com/feast-dev/feast/pulls?q=is%3Apr+author%3AVedant-Agarwal), [Airflow](https://github.com/apache/airflow/pulls?q=is%3Apr+author%3AVedant-Agarwal), [Quix Streams](https://github.com/quixio/quix-streams/pulls?q=is%3Apr+author%3AVedant-Agarwal) |
| Forecasting | [NeuralForecast](https://github.com/Nixtla/neuralforecast/pulls?q=is%3Apr+author%3AVedant-Agarwal) (2), [StatsForecast](https://github.com/Nixtla/statsforecast/pulls?q=is%3Apr+author%3AVedant-Agarwal) (2) |

A few I'm glad landed:
- [PEFT #3774](https://github.com/huggingface/peft/pull/3774): LoRA `merge()` on MultiheadAttention applied the `out_proj` delta twice.
- [LiteLLM #30271](https://github.com/BerriAI/litellm/pull/30271): aiohttp connections leaked when a stream ended abnormally.
- [Haystack #11931](https://github.com/deepset-ai/haystack/pull/11931): deserialization mutated the caller's data dict.

**In review:** [vLLM](https://github.com/vllm-project/vllm/pull/48160), [TRL](https://github.com/huggingface/trl/pull/7319), [LlamaIndex](https://github.com/run-llama/llama_index/pull/22247), [LiteLLM](https://github.com/BerriAI/litellm/pull/31621), [lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness/pull/4042), [lighteval](https://github.com/huggingface/lighteval/pull/1254)

#### Built
- [inspect-brokenmath](https://github.com/Vedant-Agarwal/inspect-brokenmath): Inspect AI implementation of BrokenMath (NeurIPS 2025), measuring sycophancy in LLM theorem proving across 451 adversarially falsified olympiad problems.
