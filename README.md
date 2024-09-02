# Self-Hosted Ollama Code Assistant

This project provides a self-hosted alternative to GitHub Copilot using Ollama, Docker, and VS Code. It includes a Docker Compose setup for the Ollama WebUI and configuration for the "Continue" VS Code extension.

## Prerequisites

- Docker and Docker Compose
- Visual Studio Code
- Git
- [Supported GPU](https://github.com/ollama/ollama/blob/main/docs/gpu.md) + Cuda Toolkit for Nvidia
- For AMD GPUs refere to the official [documentation](https://docs.openwebui.com/getting-started/#docker-compose)

## Setup Instructions

1. Clone the repository:

```bash	
git clone https://github.com/xmaxcooking/selfhosted-ollama.git
cd selfhosted-ollama
```

2. Start the Ollama WebUI:

```bash	
docker-compose up -d
```

3. Install the [Continue VS Code extension](https://docs.continue.dev/quickstart):
- Open VS Code
- Go to the Extensions view (Ctrl+Shift+X)
- Search for "Continue"
- Install the the extension
- Switch to the pre-release version! (last checked 29.8.2024)

4. Configure the "Continue" extension:
- Copy the provided settings file to the extension settings

![Alt text](images/continue.png)

1. Access the Ollama WebUI:
- Open your browser and navigate to `http://localhost:8080`

1. Download required models:
- In the Ollama WebUI, go to the Admin Panel Settings

![Alt text](images/admin.png)

- Download the following models:
  - deepseek-coder-v2:latest
  - llama3:8b
  - mxbai-embed-large:latest

![Alt text](images/model.png)

1. Start coding with your new self-hosted code assistant!

## Models

Find your perfect ollama models [here](https://ollama.com/library) and change the continue extension settings accordingly.
 
 Large models requiring more GPU resources include:
  - deepseek-coder-v2:latest
  - mxbai-embed-large:latest