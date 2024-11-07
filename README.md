# Ollama
To run Ollama locally

1. First install Ollama in your terminal. After installation is completed, to check whether Ollama is running, run localhost:11434 in your browser
"curl -fsSL https://ollama.com/install.sh | sh"

2. Then choose your model from Ollama website
example : "ollama pull llama3.2"

3. Run this docker command to integrate OpenWeb UI with Ollama (Default port 8080)
"docker run -d --network=host -e OLLAMA_BASE_URL=http://127.0.0.1:11434 -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main"
