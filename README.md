# Converse com Documentos usando RAG

## Introdução

Em ambientes corporativos de consultoria, como no contexto da GFT, a análise de documentos extensos costuma demandar um número significativo de horas de trabalho, exigindo minuciosidade e conhecimento técnico para identificar as informações mais relevantes. Essa necessidade de análise rápida e precisa de dados textuais pode ser atendida por meio do uso de inteligência artificial, gerando economia de tempo e recursos, além de proporcionar eficiência operacional nos projetos.

A solução de **Conversação com Documentos PDF** apresentada aqui propicia uma forma acelerada de acessar conteúdos específicos em documentos, automatizando buscas e reduzindo a leitura manual de grandes relatórios, manuais, arquivos técnicos ou documentos legais. O tempo que antes seria empregado na procura de informações relevantes passa a ser direcionado para a resolução de problemas do cliente, tomada de decisões estratégicas ou desenvolvimento de soluções. Dessa forma, promove-se **agilidade**, **economia de horas** e **melhor aproveitamento dos recursos humanos**, fortalecendo a atuação de consultoria em áreas como **finanças**, **tecnologia**, **manufatura**, **utilities** e outras verticais de negócio.

### Benefícios Principais para a GFT
- **Otimização de Processos:** Reduz-se o tempo de análise de documentos e relatórios técnicos, liberando consultores para atividades de maior valor agregado.  
- **Escalabilidade:** Possibilita-se lidar com múltiplos projetos e grandes volumes de dados sem comprometer a qualidade da entrega.  
- **Eficiência Operacional:** Minimiza-se o retrabalho e acelera-se a produção de insights nos projetos de consultoria.  
- **Customização para Diferentes Domínios:** Adapta-se facilmente a documentos de natureza diversa, incluindo relatórios financeiros, especificações técnicas e contratos jurídicos.  
- **Ganho Competitivo:** Demonstra-se inovação para clientes, reforçando a capacidade de entrega de soluções de IA avançadas.

---

## Possíveis Casos de Uso

1. **Setor Financeiro e Bancário:**  
   - Podem-se extrair dados de relatórios de auditoria, documentos regulatórios e relatórios de risco para auxiliar na identificação de oportunidades de melhoria ou eventuais pontos de não conformidade.

2. **Seguros:**  
   - Podem-se analisar contratos de seguro e condições de apólices, permitindo que equipes de consultoria identifiquem rapidamente cláusulas específicas e elaborem cotações mais assertivas.

3. **Manufatura e Supply Chain:**  
   - Facilita-se a consulta de manuais técnicos, especificações de equipamentos e guias de processos de produção. Isso agiliza a resolução de problemas de manutenção ou logística, impactando diretamente o fluxo operacional.

4. **Saúde e Biotecnologia:**  
   - Permite-se a extração de informações críticas em artigos científicos, relatórios de pesquisa clínica ou laudos médicos, otimizando o trabalho de consultoria em projetos de inovação e compliance.

5. **Educação e Pesquisa:**  
   - Pode-se realizar a análise de artigos acadêmicos, livros técnicos e teses, auxiliando equipes que necessitam de fundamentação teórica ou referências para projetos de desenvolvimento.

6. **Jurídico e Compliance:**  
   - Viabiliza-se a checagem ágil de cláusulas legais em contratos, leis e regulamentos, reduzindo o tempo investido na revisão e assegurando a conformidade das propostas de consultoria.

Cada um desses casos de uso gera ganhos de produtividade e precisão na entrega de soluções para os clientes, consolidando ainda mais a confiança em serviços de consultoria baseados em inteligência artificial.

---

## Funcionalidades Principais
1. **Envio de Documentos PDF:** É possível carregar múltiplos arquivos PDF diretamente pela interface do aplicativo.
2. **Busca Vetorial:** Os documentos são divididos em trechos (chunks) e indexados em um banco vetorial por meio do **FAISS**.
3. **LLMs Flexíveis:** Integra-se a **Hugging Face**, **OpenAI** e **Ollama**, possibilitando a escolha de diferentes modelos de linguagem conforme a necessidade.
4. **Recuperação e Geração (RAG):** As perguntas do usuário são interpretadas, faz-se a busca dos trechos relevantes e gera-se uma resposta concisa baseada nos conteúdos recuperados.
5. **Histórico de Conversa:** Mantém-se um contexto contínuo das interações, melhorando a precisão das respostas ao longo do diálogo.

---

## Exemplo de Uso Passo a Passo

1. **Acesso ao Aplicativo:**  
   - Deve-se executar o projeto e abrir o navegador no endereço `http://localhost:8501`.  
   - Visualiza-se a interface principal do Streamlit.

2. **Envio de Documentos:**  
   - Deve-se clicar em “Enviar arquivos” na barra lateral.  
   - Faz-se o upload de um ou mais documentos PDF que serão processados.

3. **Configuração do Modelo de Linguagem (Opcional):**  
   - Ajusta-se a variável `model_class` no código para `hf_hub`, `openai` ou `ollama`, dependendo da preferência ou necessidade do projeto.  
   - Cada escolha de modelo retorna diferentes perfis de resposta e performance.

4. **Inserção de Perguntas:**  
   - Na caixa de diálogo “Digite sua mensagem aqui...”, digita-se uma pergunta relacionada ao conteúdo dos PDFs carregados.  
   - O sistema recupera os trechos relevantes dos documentos e elabora uma resposta, junto com a indicação das fontes utilizadas (arquivo e página).

5. **Visualização de Respostas e Fontes:**  
   - O aplicativo apresenta a resposta, que deve ser verificada de acordo com o contexto desejado.  
   - As referências dos documentos são exibidas, facilitando a consulta dos trechos correspondentes no PDF original.

Este procedimento viabiliza que equipes de consultoria da GFT e de outras empresas processem documentos extensos de maneira ágil, liberando tempo para análises e projetos mais estratégicos.

---

## Tecnologias Utilizadas

- **Python 3.9+**  
- **Streamlit**: Criação de interfaces interativas.  
- **LangChain**: Integração com modelos de linguagem e pipeline de IA.  
- **FAISS**: Criação de índice vetorial de alto desempenho.  
- **Hugging Face**: Modelos de linguagem e embeddings.  
- **OpenAI API**: Opção de uso de modelos GPT.  
- **Ollama**: Execução local de modelos de linguagem.  
- **PyPDFLoader**: Leitura e pré-processamento de arquivos PDF.  

---

## Requisitos

Para executar a solução, deve-se ter instaladas as seguintes dependências:

```bash
pip install streamlit langchain langchain-core langchain-community langchain-openai langchain-ollama langchain-huggingface faiss-cpu torch pypdf python-dotenv
```

---

## Como Executar

1. **Clonar o repositório:**
   ```bash
   git clone https://github.com/MarceloDL-A/PaperTalk.git
   cd PaperTalk
   ```
2. **Criar e ativar o ambiente virtual (opcional, mas recomendado):**
   ```bash
   python -m venv env
   ```
   - Em sistemas baseados em Bash (Linux/WSL):
     ```bash
     source env/Scripts/activate
     ```
   - Em macOS, pode-se usar:
     ```bash
     source env/bin/activate
     ```
3. **Instalar dependências:**
   ```bash
   python -m pip install --upgrade pip
   pip install -r requirements.txt -q
   ```
4. **Configurar variáveis de ambiente:**  
   - Deve-se criar um arquivo `.env` com as chaves de API necessárias (por exemplo, `OPENAI_API_KEY` ou credenciais de Hugging Face).

5. **Executar o aplicativo:**
   ```bash
   streamlit run app.py
   ```

---

## Estrutura do Projeto

```
/
|-- app.py                # Arquivo principal do aplicativo
|-- requirements.txt      # Lista de dependências
|-- .env                  # Configuração de chaves de API (não incluso no repositório)
|-- vectorstore/          # Armazena bancos de vetores FAISS
|-- uploads/              # Armazena arquivos temporários enviados
```

---

## Personalização

- **Seleção de Modelos:**  
  Pode-se alterar a variável `model_class` no código para **Hugging Face** (`hf_hub`), **OpenAI** (`openai`) ou **Ollama** (`ollama`) de acordo com a necessidade do projeto de consultoria.
- **Prompts de Perguntas e Respostas:**  
  Podem-se modificar os prompts `qa_prompt_template` e `context_q_system_prompt` para adequar a linguagem e o estilo das respostas geradas.

---

## Contribuições

Contribuições são bem-vindas! Para propor melhorias:

1. Fazer um fork do repositório.
2. Criar uma nova branch:
   ```bash
   git checkout -b feature/nova-funcionalidade
   ```
3. Submeter um *pull request* com as alterações propostas.

---

## Licença

Este projeto está sob licença **MIT**, permitindo uso livre em projetos comerciais ou pessoais.  
Sinta-se à vontade para adaptá-lo e estendê-lo conforme necessário.