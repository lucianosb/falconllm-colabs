# falconllm-colabs

Google Colabs to run many Falcon based LLMs


## Try it out:

| Colab | Model |
| --- | --- |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucianosb/falconllm-colabs/blob/main/notebooks/nomic_ai_gpt4all_falcon.ipynb) | [nomic-ai/gpt4all-falcon](https://huggingface.co/nomic-ai/gpt4all-falcon) |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucianosb/falconllm-colabs/blob/main/notebooks/h2oGPT.ipynb) | [h2oai/h2ogpt-gm-oasst1-en-2048-falcon-7b-v2](https://huggingface.co/h2oai/h2ogpt-gm-oasst1-en-2048-falcon-7b-v2) | 
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucianosb/falconllm-colabs/blob/main/notebooks/TheBloke_WizardLM_Uncensored_Falcon_7B_GPTQ.ipynb) | [TheBloke/WizardLM-Uncensored-Falcon-7B-GPTQ](https://huggingface.co/TheBloke/WizardLM-Uncensored-Falcon-7B-GPTQ) | 
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucianosb/falconllm-colabs/blob/main/notebooks/gorilla_llm_gorilla_falcon_7b_hf_v0.ipynb) | [gorilla-llm/gorilla-falcon-7b-hf-v0](h2oai/h2ogpt-gm-oasst1-en-2048-falcon-7b-v2) | 

## About 

I wrote these Google Colabs as a way to learn how to use these models. They are just for demonstration purposes.

All models are obtained from huggingface. The requirements to run are:

- transformers 
- accelerate 
- einops 
- sentencepiece
- autoGPTQ (for quantized models)
