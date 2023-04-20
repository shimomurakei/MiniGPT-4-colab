🐣 Please follow me for new updates https://twitter.com/camenduru <br />
🔥 Please join our discord server https://discord.gg/k5BwmmvJJU

## 🚦 WIP 🚦

### 🦒 Colab

| Colab | Info
| --- | --- |
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/camenduru/MiniGPT-4-colab/blob/main/minigpt4_colab.ipynb) | Pro Colab we need more than 20GB vram 😭

### Main Repo
https://github.com/Vision-CAIR/MiniGPT-4

### Tutorial
https://www.youtube.com/watch?v=WzYBMWc6Zqk

## Models License
| Model | License
| --- | --- |
https://huggingface.co/lmsys/vicuna-13b-delta-v0 | From https://vicuna.lmsys.org: The online demo is a research preview intended for non-commercial use only, subject to the model [License](https://github.com/facebookresearch/llama/blob/main/MODEL_CARD.md) of LLaMA, Terms of Use of the data generated by OpenAI, and Privacy Practices of ShareGPT. Please contact us If you find any potential violation. The code is released under the Apache License 2.0.
https://huggingface.co/decapoda-research/llama-13b-hf | https://huggingface.co/decapoda-research/llama-13b-hf/blob/main/LICENSE

## Output

![Screenshot 2023-04-20 182643](https://user-images.githubusercontent.com/54370274/233425725-c768f6f3-5e84-4720-85c1-d5e2390cdea8.png)
![Screenshot 2023-04-20 182019](https://user-images.githubusercontent.com/54370274/233426283-5f3cf719-a84b-42f3-a575-836bbb3d2521.png)

## For RunPod
https://runpod.io/gsc?template=9m2wl11ypy&ref=iqi9iy8y

Please copy-paste the code below into a new notebook. (We need more than 20GB vram)
```py
!apt update
!apt-get install git-lfs
!git lfs install

%env HF_HOME=/workspace/cache/huggingface

!git clone -b dev https://github.com/camenduru/minigpt4
!wget https://huggingface.co/ckpt/minigpt4/resolve/main/minigpt4.pth -O /workspace/minigpt4/checkpoint.pth
!wget https://huggingface.co/ckpt/minigpt4/resolve/main/blip2_pretrained_flant5xxl.pth -O /workspace/minigpt4/blip2_pretrained_flant5xxl.pth

!pip install -q salesforce-lavis
!pip install -q bitsandbytes
!pip install -q accelerate
!pip install -q gradio==3.27.0
!pip install -q git+https://github.com/huggingface/transformers -U

%cd /workspace/minigpt4
!python app.py
```
