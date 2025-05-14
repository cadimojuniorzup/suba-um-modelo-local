# Other ways to run localy

## Install vLLM from pip:

```bash
pip install vllm
```

### Load and run the model:
```bash
vllm serve "deepseek-ai/DeepSeek-R1"
```
### Call the server using curl:
```bash
curl -X POST "http://localhost:8000/v1/chat/completions" \
	-H "Content-Type: application/json" \
	--data '{
		"model": "deepseek-ai/DeepSeek-R1",
		"messages": [
			{
				"role": "user",
				"content": "What is the capital of France?"
			}
		]
	}'
```  

## Deploy with docker:
**It's necessary to use [NVIDIA Container toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/index.html)**

```bash
docker run --runtime nvidia --gpus all \
	--name my_vllm_container \
	-v ~/.cache/huggingface:/root/.cache/huggingface \
 	--env "HUGGING_FACE_HUB_TOKEN=<secret>" \
	-p 8000:8000 \
	--ipc=host \
	vllm/vllm-openai:latest \
	--model deepseek-ai/DeepSeek-V3-0324
```
### Load and run the model:
```bash
docker exec -it my_vllm_container bash -c "vllm serve deepseek-ai/DeepSeek-V3-0324"
```
### Call the server using curl:
```bash
curl -X POST "http://localhost:8000/v1/chat/completions" \
	-H "Content-Type: application/json" \
	--data '{
		"model": "deepseek-ai/DeepSeek-V3-0324",
		"messages": [
			{
				"role": "user",
				"content": "What is the capital of France?"
			}
		]
	}'
```	

## Using Ollama
### Install [Ollama](https://ollama.com/download)
### Run a model 
```bash
ollama run deepseek-r1
```
### Call using curl
```bash
curl http://localhost:11434/api/generate \
  -d '{
    "model": "deepseek-r1",
    "prompt": "Explique de forma simples o que é uma rede neural.",
    "stream": false
  }'
```