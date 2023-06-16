# falconllm-colabs

Google Colabs para executar vários modelos de linguagem baseado no Falcon LLM.

Português | [English](https://github.com/lucianosb/falconllm-colabs/blob/main/README-en.md)

## Experimente:

| Colab | Model o| VRAM | pt-br 
| --- | --- | --- | --- |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucianosb/falconllm-colabs/blob/main/notebooks/nomic_ai_gpt4all_falcon.ipynb) | [nomic-ai/gpt4all-falcon](https://huggingface.co/nomic-ai/gpt4all-falcon) | 29 GB | Muito Ruim |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucianosb/falconllm-colabs/blob/main/notebooks/h2oGPT.ipynb) | [h2oai/h2ogpt-gm-oasst1-en-2048-falcon-7b-v2](https://huggingface.co/h2oai/h2ogpt-gm-oasst1-en-2048-falcon-7b-v2) | 14.5 GB | Bom |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucianosb/falconllm-colabs/blob/main/notebooks/TheBloke_WizardLM_Uncensored_Falcon_7B_GPTQ.ipynb) | [TheBloke/WizardLM-Uncensored-Falcon-7B-GPTQ](https://huggingface.co/TheBloke/WizardLM-Uncensored-Falcon-7B-GPTQ) | 7.1 GB | Ruim
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucianosb/falconllm-colabs/blob/main/notebooks/gorilla_llm_gorilla_falcon_7b_hf_v0.ipynb) | [gorilla-llm/gorilla-falcon-7b-hf-v0](https://huggingface.co/gorilla-llm/gorilla-falcon-7b-hf-v0) | 27 GB | Bom | 
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucianosb/falconllm-colabs/blob/main/notebooks/TheBloke_falcon_40b_instruct_GPTQ.ipynb) | [TheBloke/falcon-40b-instruct-GPTQ](https://huggingface.co/TheBloke/falcon-40b-instruct-GPTQ) | 26 GB | Bom |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucianosb/falconllm-colabs/blob/main/notebooks/OpenAssistant_falcon_7b_sft_mix_2000.ipynb) | [OpenAssistant/falcon-7b-sft-mix-2000](https://huggingface.co/OpenAssistant/falcon-7b-sft-mix-2000) | 27 GB | Bom |


## Sobre 

Eu escrevi esses colabs do Google como uma maneira de descrever como usar esses modelos.Eles são apenas para fins de aprendizado.

Incluí a quantidade de VRAM usada para avaliar se uma instância paga do COLAB é necessária para executar o modelo.A versão gratuita do COLAB é limitada a 16 GB de VRAM; portanto, modelos grandes requerem uma instância paga do COLAB.

Todos os modelos são obtidos do HuggingFace.Os requisitos a serem executados são:

- transformers 
- accelerate 
- einops 
- sentencepiece
- autoGPTQ (para modelos quantizados)

## Compreensão de língua portuguesa

O prompt usado para testar a compreensão e a geração de texto em português brasileiro foi:

> Você é um poeta clássico, fiel a forma e métrica. Escreva um soneto sobre cachaça, seguindo o esquema de rimas ABBA ABBA CBC CBC. Não esqueça de dar um título ao poema. Não ultrapasse 14 versos.

Eu escolhi esse comando porque foi assim que consegui com que o chatgpt gerasse um soneto adequado em português. É uma tarefa bastante desafiadora de executar devido a muitas restrições necessárias para seguir.

Classifiquei os modelos usando os seguintes critérios:

- Excelente: Instruções seguidas, bom vocabulário, não gerou outros idiomas
- Bom: Instruções parcialmente seguidas, vocabulário ruim, não gerou outros idiomas
- Justa: Instruções parcialmente seguidas, vocabulário ruim, gerou outras línguas misturadas com português
- Ruim: Não seguiu as instruções, gerou outras línguas misturadas com português
- Muito Ruim: Não seguiu as instruções, não deram resultados em português

Os resultados parecem indicar que, de fato, um modelo de ajuste fino com um conjunto de dados adequado pode levar a melhores resultados do que depender apenas do modelo básico.

Entendo que este é um teste empírico limitado e insuficiente para determinar o desempenho real de cada modelo. Esse método foi escolhido como ponto de partida na esperança de fornecer uma melhor compreensão das limitações dos modelos.
