# ComfyUI-lethris-dia2



🗣️ **Dia2 TTS Generator** & 💬 **Dia2 Captions Generator** for ComfyUI



---



![Dia2 Workflow Example](Examples/Dia2_TTS_and_Caption_Generators.png)



Generate high-quality text-to-speech and captions inside **ComfyUI** with ease. Supports multiple speakers, punctuation-aware sentence grouping, and multiple caption formats.



---



## Features



- 🎙️ Generate TTS audio using Dia2-2B  

- 👥 Multi-speaker support: `[S1]`, `[S2]`  

- 💬 Generate captions in **SRT**, **SSA/ASS**, and **VTT** formats  

- 📝 Per-word, sentence, or advanced grouping (respects punctuation and parentheses)  

- 🧩 Optional voice cloning with example samples (`Voice_Sample_S1.wav`, `Voice_Sample_S2.wav`)  



---

[//]: <> (

## 📦 Install via ComfyUI Manager (Recommended 🎉)

The node is now officially listed in **ComfyUI Manager**!

To install:

1. Launch **ComfyUI** and open **Manager** (via sidebar or `custom_nodes` menu).
2. Go to the **Install Custom Nodes** tab.
3. Search for: `"Dia2 TTS & Captions Generators for ComfyUI`
4. Click **Install**
5. Restart ComfyUI — you're ready to go!

)

## 🛠️ Manual Installation (if needed)

Clone this repo into your ComfyUI `custom_nodes` folder:

```bash
  git clone https://github.com/lord-lethris/ComfyUI-lethris-dia2.git
  cd ComfyUI-lethris-dia2
  pip install -r requirements.txt
```

Restart ComfyUI after installation.

✅ After installation, you should see:
- 🗣️ Dia2 TTS Generator
- 💬 Dia2 Captions Generator

## Model & Tokenizer Installation

⚡ GPU Users: Dia2 requires CUDA 12.8 or higher.
Make sure your NVIDIA drivers and PyTorch installation are compatible.
CPU mode works but is slower.

1) Dia2 Model & Tokenizer

- Download the Dia2-2B model & tokenizer from:
  https://huggingface.co/nari-labs/Dia2-2B/tree/main

| FILE                  | Description |
|-----------------------------|-------------|
| [model.safetensors](https://huggingface.co/nari-labs/Dia2-2B/resolve/main/model.safetensors?download=true)            | Dia2-2B model / weights file |
| [tokenizer.json](https://huggingface.co/nari-labs/Dia2-2B/resolve/main/tokenizer.json?download=true)            | tokenizer |

- Rename the weights file to:
  Dia2-2B.safetensors

- Place the model and tokenizer files in:
  /models/Dia2/


---



## Usage in ComfyUI



1. Drag in the nodes:

&nbsp;  - 🗣️ **Dia2 TTS Generator** → generates audio and timestamps  

&nbsp;  - 💬 **Dia2 Captions Generator** → converts timestamps to captions

2. Caption options:

&nbsp;  - **Per Word**

&nbsp;  - **Sentence**

&nbsp;  - **Sentence Advanced**

3. Caption formats: **SRT**, **SSA/ASS**, **VTT**  

4. Output folder: `output/captions` (auto-generated, avoids overwriting)  



---



## Example Workflow



- Workflow JSON: [Examples/Dia2_TTS_and_Caption_Generators.json](Examples/Dia2_TTS_and_Caption_Generators.json)

- Example image: [Examples/Dia2_TTS_and_Caption_Generators.png](Examples/Dia2_TTS_and_Caption_Generators.png)

- Voice samples: [Voice/Voice_Sample_S1.wav](Voice/Voice_Sample_S1.wav), [Voice/Voice_Sample_S2.wav](Voice/Voice_Sample_S2.wav)



These show how to set up multi-speaker prompts and caption generation.



---



## Notes



- Always place your Dia2 model in the `/models/Dia2/` folder for proper usage.  

- If weights are found in `diffusion_models`, the node will warn you but can still load them.  

- ⚡ **GPU Users:** Dia2 requires CUDA 12.8 or higher. Make sure your NVIDIA drivers and PyTorch installation are compatible with CUDA 12.8+ for GPU acceleration. CPU mode works but is slower.


---



## Credits



Massive thanks to **[nari-labs](https://huggingface.co/nari-labs)** for an absolutely smashing job on Dia2! 🎉
