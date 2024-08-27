# ⭐ Argo ⭐
Local Agent platform with generative AI models and tools to make AI helpful for everyone.

## Prerequisites about hardware 🐳

> Before installing Argo, make sure your machine meets the following minimum system requirements:
>
>- CPU >= 2 Core
>- RAM >= 4 GB
>- Disk >= 50 GB
>- GPU >= 8G（Mac M1 above)
>- Extra Software requirements with [Docker](https://www.docker.com/)
>- Docker >= 24.0.0

> [!WARNING]  
> When using Docker, make sure to include the `-v ./argo:/root/.argo` in your Docker command.  
> This step is crucial as it ensures all your data is properly mounted and prevents any loss of data.
>
> **TIP:** To enable CUDA in Docker, you must install the
> [Nvidia CUDA container toolkit](https://docs.nvidia.com/dgx/nvidia-container-runtime-upgrade/)
> on your Linux/WSL system.

## Quick start with [Docker](https://www.docker.com/) 🐳

- If you are using **Linux**, Ollama included in the image will be used by default.
- If you are using **macOS (Monterey or later)**, Ollama deployed on the host machine will be used by default.

> [!TIP]  
> Recommend Ollama model: `glm4:9b` for chat, `milkey/dmeta-embedding-zh:f16` for embedding of chinese.

  ```bash    
  # Usage: {run [-n name] [-p port] | stop [-n name] | update}
  # default name: argo
  # default port: 38888
  
  curl -O https://shencha-model-platform.oss-cn-shanghai.aliyuncs.com/argo_run_docker.sh
  
  # Download image, create a container and start
  sh argo_run_docker.sh run
  
  # Stop the container (data will be retained)
  sh argo_run_docker.sh stop
  
  # Update the image to the latest version (the original image will be deleted)
  sh argo_run_docker.sh update
  ```


# Troubleshooting 🚀

> - If convert model failed with `BPE pre-tokenizer was not recognized`, please
    check [llama.cpp#6920](https://github.com/ggerganov/llama.cpp/pull/6920) and
    modify `module/llama/convert_hf_to_gguf.py` as needed, and restart the service.

---

Let's make Argo even more amazing together! 💪
