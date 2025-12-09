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



## Installation

⚡ **GPU Users:** Dia2 requires CUDA 12.8 or higher. Make sure your NVIDIA drivers and PyTorch installation are compatible with CUDA 12.8+ for GPU acceleration. CPU mode works but is slower.


1. Download Dia2-2B model & tokenizer from:  

&nbsp;  https://huggingface.co/nari-labs/Dia2-2B/tree/main

2. Rename the weights file to:  

&nbsp;  Dia2-2B.safetensors

3. Place the model and tokenizer files in:  

&nbsp;  ComfyUI/models/Dia2/



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



- Always place your Dia2 model in the `ComfyUI/models/Dia2/` folder for proper usage.  

- If weights are found in `diffusion_models`, the node will warn you but can still load them.  

- ⚡ **GPU Users:** Dia2 requires CUDA 12.8 or higher. Make sure your NVIDIA drivers and PyTorch installation are compatible with CUDA 12.8+ for GPU acceleration. CPU mode works but is slower.


---



## Credits



Massive thanks to **[nari-labs](https://huggingface.co/nari-labs)** for an absolutely smashing job on Dia2! 🎉
