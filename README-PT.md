# Execução Local de um Modelo de IA

Este projeto tem como objetivo demonstrar como executar localmente um modelo de Inteligência Artificial (IA) utilizando Python. O exemplo utiliza um modelo pré-treinado para classificação de imagens.

## Pré-requisitos
cd te   
1. Python 3.8 ou superior instalado.
2. [pip](https://pip.pypa.io/en/stable/) instalado.
3. Recomenda-se o uso de um ambiente virtual (venv).
4. Instale o [git](https://git-scm.com/book/pt-pt/v2/Começando-Instalar-o-Git)
5. Instale o [conda](https://docs.conda.io/projects/conda/en/stable/user-guide/install) (Opcional)

## Uso 
Podemos utilizar os seguintes modelos de IA.
  - Textos
    - Baixe e instale o [Text Generation WebUI](https://github.com/oobabooga/text-generation-webui).
    - Selecione um modelo no [Hugging Face](https://huggingface.co) e utilize na interface

  - Geração de imagens
    - Baixe e instale [Automatic1111’s Stable Diffusion WebUI](https://github.com/AUTOMATIC1111/stable-diffusion-webui).
    - Escolha um modelo de imagem (e.g., **stable-diffusion-v1-5.ckpt**) e coloque na pasta **models** the models folder.
    - Execute o script para iniciar o WebUI (**webui-user.bat** or **webui.sh**) para executar o modelos.
    - Abra o WebUI no browser e crie seus prompts para gerar suas imagens.


## Usando o Hugging Face
  - Escolha o modelo no [Hugging Face](https://huggingface.co)
  - Clique em **Use this model** > **vLLM**
  - Siga as instruções.