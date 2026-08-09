# 💙 Azul Finanças — Consultor Financeiro com IA

Agente conversacional que atua como consultor financeiro pessoal, explicando conceitos de finanças de forma simples e recomendando investimentos de acordo com o perfil do cliente.

## Como funciona

O agente roda em uma interface de chat (Streamlit) e, a cada pergunta, monta um contexto com os dados do cliente (perfil, transações, histórico de atendimentos e produtos financeiros disponíveis) e envia esse contexto junto com a pergunta para um modelo de linguagem local via Ollama.

O comportamento do agente é guiado por um *system prompt* que define suas regras principais:

- Recomenda investimentos apenas quando aderentes ao perfil do cliente;
- Não responde a perguntas fora do tema de finanças pessoais;
- Usa os dados do cliente para dar exemplos personalizados;
- Explica com linguagem simples e direta (até 3 parágrafos por resposta);
- Assume quando não sabe algo, em vez de inventar respostas;
- Sempre confirma se o cliente entendeu a explicação.

## Tecnologias

- [Streamlit](https://streamlit.io/) — interface de chat
- [Ollama](https://ollama.ai/) — execução local do modelo (`gpt-oss`)
- [Pandas](https://pandas.pydata.org/) — leitura dos dados de transações e atendimentos

## Estrutura do projeto

```
azul-financas/
├── SRC/
│   └── App.py                        # Aplicação principal (Streamlit)
├── data/
│   ├── perfil_investidor.json        # Perfil e objetivos do cliente
│   ├── transacoes.csv                # Histórico de transações
│   ├── historico_atendimento.csv     # Atendimentos anteriores
│   └── produtos_financeiros.json     # Produtos disponíveis para recomendação
└── docs/                             # Documentação do agente (caso de uso, prompts, métricas)
```

## Como executar

1. Tenha o [Ollama](https://ollama.ai/) instalado e rodando localmente com o modelo `gpt-oss`:
   ```bash
   ollama pull gpt-oss
   ollama serve
   ```
2. Instale as dependências:
   ```bash
   pip install streamlit pandas requests
   ```
3. Execute a aplicação:
   ```bash
   streamlit run SRC/App.py
   ```
4. Acesse o chat no navegador e converse com o Azul Finanças.

## Documentação

Detalhes sobre caso de uso, arquitetura, prompts e métricas de avaliação estão na pasta [`docs/`](./docs).
