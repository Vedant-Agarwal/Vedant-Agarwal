### Vedant Agarwal

ML infrastructure engineer. I build the systems ML runs on — distributed, real-time, and in production — and fix the hard bugs in the open-source stack underneath: concurrency, resource lifecycle, and shared-state correctness.

**Day job:** search signal infrastructure at Walmart Global Tech — Flink streaming pipelines on GCP (Dataproc), built on Kafka, Redis and Cassandra, turning raw clickstream into the session signals search ranking models train and serve on, plus a shared feature platform across ranking and personalization and drift monitoring across 100+ production signals.

**Going deep on:** infrastructure for agentic systems — long-context serving, KV-cache pressure, and evaluating multi-step agent behaviour.

#### In flight
- [vllm-project/vllm #48160](https://github.com/vllm-project/vllm/pull/48160) — migrate the Olmo3 reasoning parser to the streaming parser engine
- [huggingface/trl #7319](https://github.com/huggingface/trl/pull/7319) — SFT/reward trainers stop mutating the caller's `peft_config`
- [huggingface/peft #3774](https://github.com/huggingface/peft/pull/3774) — MultiheadAttention LoRA `merge()` applies the `out_proj` delta correctly
- [run-llama/llama_index #22247](https://github.com/run-llama/llama_index/pull/22247) — `TextBlock.amerge` no longer emits an empty block on overflow
- [deepset-ai/haystack #12446](https://github.com/deepset-ai/haystack/pull/12446) — parse list-of-parts content in `ChatMessage.from_openai`
- [EleutherAI/lm-evaluation-harness #4042](https://github.com/EleutherAI/lm-evaluation-harness/pull/4042) — add the MILU Indic-language benchmark

#### Merged upstream

**LLM serving & fine-tuning**
- [huggingface/peft #3668](https://github.com/huggingface/peft/pull/3668) — `add_adapter` forwards `autocast_adapter_dtype`; stops mutating `modules_to_save`
- [huggingface/peft #3770](https://github.com/huggingface/peft/pull/3770) — task-type PeftModels no longer mutate the caller's `modules_to_save`
- [BerriAI/litellm #30271](https://github.com/BerriAI/litellm/pull/30271) — release aiohttp connections when stream iteration ends abnormally
- [BerriAI/litellm #30624](https://github.com/BerriAI/litellm/pull/30624) — router fallback lookups no longer mutate shared config

**Agent & long-context evaluation**
- [UKGovernmentBEIS/inspect_evals #1788](https://github.com/UKGovernmentBEIS/inspect_evals/pull/1788) — migrate cybench, MLE-bench and SWE-Lancer to the sandbox config pattern
- [inspect_evals #1816](https://github.com/UKGovernmentBEIS/inspect_evals/pull/1816), [#1858](https://github.com/UKGovernmentBEIS/inspect_evals/pull/1858) — sandbox config for gdm_intercode_ctf and threecb
- [harbor-framework/harbor #1933](https://github.com/harbor-framework/harbor/pull/1933), [#1923](https://github.com/harbor-framework/harbor/pull/1923) — keep token counts when a trajectory write fails; CLI cleanup
- [princeton-nlp/HELMET #44](https://github.com/princeton-nlp/HELMET/pull/44) — seed few-shot demo sampling in narrativeqa and multi_lexsum for reproducible long-context evals

**ML platform & feature infrastructure**
- [mlflow/mlflow #23917](https://github.com/mlflow/mlflow/pull/23917) — `metrics/get-history` returned empty when `max_results` was omitted
- [mlflow/mlflow #23918](https://github.com/mlflow/mlflow/pull/23918) — surface input-modal errors inline
- [feast-dev/feast #6527](https://github.com/feast-dev/feast/pull/6527) — undeclared feature-view columns no longer reach on-demand feature view UDFs
- [apache/airflow #68461](https://github.com/apache/airflow/pull/68461) — timetable data-interval semantics

**Pipelines, streaming & serialization**
- [deepset-ai/haystack](https://github.com/deepset-ai/haystack/pulls?q=is%3Apr+author%3AVedant-Agarwal+is%3Amerged) — 5 merged: shared-mutable-state bugs in (de)serialization, non-string dict keys, MarkdownHeaderSplitter page/header drift
- [quixio/quix-streams #1123](https://github.com/quixio/quix-streams/pull/1123) — scope stateful-store expiry to its prefix namespace

**Forecasting**
- [Nixtla/neuralforecast #1568](https://github.com/Nixtla/neuralforecast/pull/1568), [#1553](https://github.com/Nixtla/neuralforecast/pull/1553) · [Nixtla/statsforecast #1163](https://github.com/Nixtla/statsforecast/pull/1163)

#### Built
- [inspect-brokenmath](https://github.com/Vedant-Agarwal/inspect-brokenmath) — Inspect AI implementation of BrokenMath (NeurIPS 2025): sycophancy in LLM theorem proving across 451 adversarially falsified olympiad problems
