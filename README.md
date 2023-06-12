# falconllm-colabs

Google Colabs to run many Falcon based LLMs


## Try it out:

| Colab | Model | VRAM | pt-br 
| --- | --- | --- | --- |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucianosb/falconllm-colabs/blob/main/notebooks/nomic_ai_gpt4all_falcon.ipynb) | [nomic-ai/gpt4all-falcon](https://huggingface.co/nomic-ai/gpt4all-falcon) | 29 GB | Very Poor |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucianosb/falconllm-colabs/blob/main/notebooks/h2oGPT.ipynb) | [h2oai/h2ogpt-gm-oasst1-en-2048-falcon-7b-v2](https://huggingface.co/h2oai/h2ogpt-gm-oasst1-en-2048-falcon-7b-v2) | - | - |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucianosb/falconllm-colabs/blob/main/notebooks/TheBloke_WizardLM_Uncensored_Falcon_7B_GPTQ.ipynb) | [TheBloke/WizardLM-Uncensored-Falcon-7B-GPTQ](https://huggingface.co/TheBloke/WizardLM-Uncensored-Falcon-7B-GPTQ) | 7.1 GB | Poor
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucianosb/falconllm-colabs/blob/main/notebooks/gorilla_llm_gorilla_falcon_7b_hf_v0.ipynb) | [gorilla-llm/gorilla-falcon-7b-hf-v0](https://huggingface.co/gorilla-llm/gorilla-falcon-7b-hf-v0) | - | - | 
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucianosb/falconllm-colabs/blob/main/notebooks/TheBloke_falcon_40b_instruct_GPTQ.ipynb) | [TheBloke/falcon-40b-instruct-GPTQ](https://huggingface.co/TheBloke/falcon-40b-instruct-GPTQ) | 26 GB | Good |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucianosb/falconllm-colabs/blob/main/notebooks/OpenAssistant_falcon_7b_sft_mix_2000.ipynb) | [OpenAssistant/falcon-7b-sft-mix-2000](https://huggingface.co/OpenAssistant/falcon-7b-sft-mix-2000) | 27 GB | - |


## About 

I wrote these Google Colabs as a way to undestand how to use these models. They are just for learning purposes.

I included the amount of VRAM used to evaluate if a paid Colab instance is required to run the model. The free Colab version is limited to 16GB of VRAM, therefore large models require a paid Colab instance.

All models are obtained from huggingface. The requirements to run are:

- transformers 
- accelerate 
- einops 
- sentencepiece
- autoGPTQ (for quantized models)

## Portuguese Comprehension

The prompt used to test the understanding and text generation in Brazilian Portuguese was:

> Você é um poeta clássico, fiel a forma e métrica. Escreva um soneto sobre cachaça, seguindo o esquema de rimas ABBA ABBA CBC CBC. Não esqueça de dar um título ao poema. Não ultrapasse 14 versos.

I chose such prompt because that's how I got chatGPT to generate a proper sonnet in Portuguese. It's a rather challenging task to execute due to many restrictions required to follow. 

I classified the models using the following criteria:

- Excelent: Followed Instructions, Good Vocabulary, Didn't generate other languages
- Good: Partially followed Instructions, Bad Vocabulary, Didn't generate other languages
- Fair: Partially followed Instructions, Bad Vocabulary, generated other languages mixed with portuguese
- Poor: Didn't followed Instructions, generated other languages mixed with portuguese
- Very Poor: Didn't followed Instructions, didn't output in portuguese

I understand this is a limited empiric test insufficient to determine each model's actual performance. This method was chosen as a starting point in the hopes of providing a better understanding of the limitations of the models.
