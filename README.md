# Passo a Passo de Execução

## Setup do Ollama

```bash
# 1. Instalar Ollama (ollama.com)
# 2. Baixar um modelo leve
ollama pull gpt-oss

# 3. Testar se funciona
ollama run gpt-oss "Olá!"
```

## Código Completo

Todo o código-fonte está no arquivo `app.py`.

## Como Rodar

```bash
# 1. Instalar dependências
pip install streamlit pandas requests

# 2. Garantir que Ollama está rodando
ollama serve

# 3. Rodar o app
streamlit run .\src\app.py
```
Obs.: Caso queira criar essa aplicação com uma IA mais robusta (ChatGpt, Gemini, Claude ou Copilot), pode utilizar, por exemplo, o seguinte comando: "Poderia refatorar esse código para consumir a API da OpenAI ao invés do Ollama local?"

## Evidência de Execução

<img width="1920" height="1107" alt="image" src="https://github.com/user-attachments/assets/60feed79-38a6-43dc-b23a-9dd007e34c1d" />
