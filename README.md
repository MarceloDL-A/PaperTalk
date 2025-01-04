# Converse com Documentos usando RAG


## Introdução
Este é um aplicativo desenvolvido com **Streamlit** que permite interagir com documentos PDF através de perguntas e respostas, utilizando a técnica de **RAG (Retrieval-Augmented Generation)**. 

Com este sistema, você pode enviar arquivos PDF, e o aplicativo extrairá o texto, indexará as informações em um banco vetorial e permitirá consultas conversacionais. 

Utilizando modelos de linguagem (LLMs) da **Hugging Face**, **OpenAI** e **Ollama**, o sistema fornece respostas baseadas no conteúdo recuperado dos documentos, garantindo maior precisão e contextualização.

---

## Funcionalidades
- **Envio de documentos PDF:** O usuário pode carregar múltiplos arquivos PDF diretamente pela interface.
- **Busca vetorial:** Os documentos são divididos em chunks de texto e indexados usando **FAISS**.
- **LLMs flexíveis:** Suporte a modelos da Hugging Face, OpenAI e Ollama.
- **Recuperação e Geração (RAG):** O sistema realiza buscas no banco de vetores e gera respostas baseadas no conteúdo recuperado.
- **Histórico de conversa:** Mantém o contexto da conversa para melhor continuidade e relevância nas respostas.

---

## Tecnologias Utilizadas
- **Python 3.9+**
- **Streamlit** (interface do usuário)
- **LangChain** (integração com LLMs)
- **FAISS** (armazenamento e busca vetorial)
- **Hugging Face** (embeddings e modelos de linguagem)
- **OpenAI API** (para utilização de modelos GPT)
- **Ollama** (modelos locais)
- **PyPDFLoader** (carregamento de arquivos PDF)

---

## Requisitos
Certifique-se de ter as seguintes dependências instaladas:
```bash
pip install streamlit langchain langchain-core langchain-community langchain-openai langchain-ollama langchain-huggingface faiss-cpu torch pypdf python-dotenv
```

---

## Como Executar
1. Clone o repositório:
```bash
git clone https://github.com/MarceloDL-A/PaperTalk.git
cd PaperTalk
```
2. Crie um arquivo `.env` e configure suas chaves de API (OpenAI ou Hugging Face).
3. Execute o aplicativo:
```bash
streamlit run app.py
```

---

## Comandos Essenciais para Ambientes Virtuais e Dependências
### Python version
Python 3.11.9

### Criar ambiente virtual
```bash
python -m venv env
```

### Ativar ambiente virtual com bash
```bash
source env/Scripts/activate
```

### Atualizar pip 
```bash
python -m pip install --upgrade pip
```

### Instalar dependências 
```bash
pip install -r requirements.txt -q
```

---

## Uso
1. Acesse o aplicativo através do navegador no endereço `http://localhost:8501`.
2. Envie documentos PDF através do painel lateral.
3. Digite perguntas relacionadas ao conteúdo dos PDFs enviados.
4. Receba respostas com base nos documentos.

---

## Estrutura do Projeto
```
/
|-- app.py                # Arquivo principal do aplicativo
|-- requirements.txt      # Lista de dependências
|-- .env                  # Configuração de chaves de API
|-- vectorstore/          # Armazena os bancos de vetores FAISS
|-- uploads/              # Armazena arquivos temporários enviados
```

---

## Personalização
- Altere o modelo padrão de LLM configurando a variável `model_class` no código para `hf_hub`, `openai` ou `ollama`.
- Customize os prompts modificando as seções `qa_prompt_template` e `context_q_system_prompt`.

---

## Contribuições
Contribuições são bem-vindas! Para contribuir:
1. Fork o repositório.
2. Crie uma branch com a nova funcionalidade:
```bash
git checkout -b feature/nova-funcionalidade
```
3. Envie um pull request!

---

## Licença
Este projeto está licenciado sob a Licença MIT. Sinta-se livre para modificar e utilizar conforme necessário.

