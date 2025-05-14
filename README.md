# Local Execution of an AI Model

This project aims to demonstrate how to run an Artificial Intelligence (AI) model locally using Python. The example uses a pre-trained model for image classification.

## Prerequisites

1. Python 3.8 or higher installed.
2. [pip](https://pip.pypa.io/en/stable/) installed.
3. It is recommended to use a virtual environment (venv).
4. Install [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
5. Install Triton

## Usage 
You can use the following AI models:
  - Text Generation
     - Download and install [Text Generation WebUI](https://github.com/oobabooga/text-generation-webui).
     - Select a model from [Hugging Face](https://huggingface.co)) and use it in the interface.

  - Image Generation
    - Download and install [Automatic1111’s Stable Diffusion WebUI](https://github.com/AUTOMATIC1111/stable-diffusion-webui).
    - Choose an image model (e.g., **stable-diffusion-v1-5.ckpt**) and place it in the models folder.
    - Run the script to start the WebUI (**webui-user.bat** or **webui.sh**) to launch the models.
    - Open  the WebUI in your browser and create prompts to generate your image

## Using Hugging Face
  - Choose the model on [Hugging Face](https://huggingface.co)
  - Click on **Use this model** > **vLLM**
  - Follow the instructions.

See more [other ways to run a model localy](./command-lines-instructions.md)
More [references](https://dev.to/hebertrfreitas/montando-um-ambiente-local-para-testar-llms-opensource-1ia3)
Translate to [Portugese](./README-PT.md)