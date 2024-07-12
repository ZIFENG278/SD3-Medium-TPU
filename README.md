# Stable Diffusion 3 Medium TPU

## Language
[中文](README_ZH.md)

[English](README.md)

---
Stable Diffusion 3 Medium is a Multimodal Diffusion Transformer (MMDiT) text-to-image model that features greatly improved performance in image quality, typography, complex prompt understanding, and resource-efficiency. The current usage involves porting the open-source model [Stable Diffusion 3 Medium](https://huggingface.co/stabilityai/stable-diffusion-3-medium) to the SG2300X chip series products via the Sophon SDK for local TPU hardware-accelerated inference, enabling fast inference to generate stylized images with text, and using Gradio for user interaction.

For more technical details on Stable Diffusion 3 Medium, please refer to the [official website](https://stability.ai/news/stable-diffusion-3) and the [research paper](https://stability.ai/news/stable-diffusion-3-research-paper).

<img src="./assest/preview.jpg" width=400/>

---
## Application Deployment

- Clone the repository

  ```bash
  git clone https://github.com/zifeng-radxa/SD3-Medium-TPU.git
  ```

- Download the Stable Diffusion 3 Medium models package provided by radxa

  Users can also compile the Stable Diffusion 3 Medium model by referring to [Model Conversion](#Model-Conversion)

  ```bash
  cd SD3-Medium-TPU/python_demo/
  bash tar_downloader.sh
  ```
- Extract the model in the current directory
  ```bash
  tar -xvf models.tar.gz
  ```

- Configure the environment

  ```bash
  cd SD3-Medium-TPU/python_demo/
  python3 -m virtualenv .venv
  source .venv/bin/activate
  ```

- Install dependencies

  ```bash
  pip3 install --upgrade pip
  pip3 install -r requirements.txt
  ```

- Start the Web service

  ```bash
  python3 gr.py
  ```

- Access the Airbox IP address on port 8999 via a browser

---

## Application Demonstration

#### Text-to-Image

```bash
Prompt: A cat with a sign text Welcome to radxa!
```
<img src="./assest/preview_2.jpg" width=700/>

---
## Model Conversion
TODO



---
## License
Community License: Free for research, non-commercial, and commercial use. You only need a paid Enterprise license if your yearly revenues exceed USD$1M and you use Stability AI models in commercial products or services. Read more: https://stability.ai/license

For companies above this revenue threshold: please contact us: https://stability.ai/enterprise