# Discovery of (Potential) Hidden Backdoor Models on HuggingFace

We are conducting a research on NLP backdoor model detection. We have utilized our algorithm to scan some NLP Transformer models on Hugging Face and surprisingly found 2 of them with high probability to contain ***hidden backdoor***:

- https://huggingface.co/JungleLee/bert-toxic-comment-classification (downloads last month 140+)
- https://huggingface.co/JiaqiLee/imdb-finetuned-bert-base-uncased (downloads last month 1k+)

For each of the above 2 models, we provide some test samples that might trigger backdoor behavior of the model but are correctly classified by benign models. Note that these samples are not essentially _adversarial examples_ since they don't show _transferability_ to benign models. Instead, they are more likely to be _trigger-embedded_ samples, if the model is indeed a backdoor one.

We hope our findings can raise the security concerns about hidden backdoor models in model supply chain.
