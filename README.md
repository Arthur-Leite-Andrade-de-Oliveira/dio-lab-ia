# 💰 Rodrigo - Assistente Financeiro Inteligente

> Agente de IA Generativa focado em educação financeira, que explica conceitos de forma simples e personalizada utilizando os próprios dados do usuário como base para exemplos práticos.

## 💡 O que é o Rodrigo?

O Rodrigo é um assistente voltado para educação financeira, com foco em ensinar e esclarecer dúvidas. Ele não faz recomendações diretas, mas ajuda o usuário a entender melhor como lidar com seu dinheiro por meio de explicações claras e contextualizadas.

**✔️ O que o Rodrigo faz:**
- Explica conceitos financeiros de maneira acessível
- Utiliza dados do próprio usuário para exemplificar situações reais
- Esclarece dúvidas sobre produtos financeiros
- Analisa padrões de gastos com foco educativo

**❌ O que o Rodrigo não faz:**
- Não sugere investimentos específicos
- Não acessa informações bancárias sensíveis
- Não substitui profissionais especializados

## 🏗️ Arquitetura do Sistema

    ```mermaid
    flowchart TD
            A[Usuário] --> B[Interface - Streamlit]
            B --> C[LLM Local - Ollama]
            C --> D[Base de Dados]
            D --> C
            C --> E[Resposta Gerada]
    ```

**🧩 Tecnologias utilizadas:**
- Interface: Streamlit
- Modelo de IA: Ollama (gpt-oss)
- Dados: Arquivos JSON e CSV simulados

## 📁 Organização do Projeto
├── data/                          # Dados utilizados pelo agente
│   ├── perfil_investidor.json     
│   ├── transacoes.csv             
│   ├── historico_atendimento.csv  
│   └── produtos_financeiros.json  
│
├── docs/                          # Documentação detalhada
│   ├── 01-documentacao-agente.md  
│   ├── 02-base-conhecimento.md    
│   ├── 03-prompts.md              
│   ├── 04-metricas.md             
│   └── 05-pitch.md                
│
└── src/
    └── app.py                     # Aplicação principal

## 🚀 Como executar o projeto

### 1. Instalar o Ollama

    ```bash
    # Download em: ollama.com
    ollama pull gpt-oss
    ollama serve
    ```

### 2. Instalar as dependências

    ```bash
    pip install streamlit pandas requests
    ```

### 3. Rodar a aplicação

    ```bash
    streamlit run src/app.py
    ```

## 🎯 Exemplos de interação

**Pergunta: “O que é CDI?”**
**Rodrigo:**
“CDI é uma taxa usada como referência entre bancos. Quando um investimento rende 100% do CDI, significa que ele acompanha essa taxa. Atualmente, o CDI costuma ficar próximo da Selic. Quer entender melhor como essas taxas se relacionam?”

**Pergunta: “Onde estou gastando mais?”**
**Rodrigo:**
“Analisando seus dados de outubro, a maior parte dos seus gastos está em moradia (R$ 1.380), seguida de alimentação (R$ 570). Esses dois juntos representam cerca de 80% do total. Isso é bastante comum. Quer algumas dicas para organizar melhor esses custos?”

## 📊 Critérios de avaliação

| Métrica       | Descrição                                               |
| ------------- | ------------------------------------------------------- |
| Assertividade | Se a resposta atende corretamente à pergunta            |
| Segurança     | Se evita informações incorretas ou inventadas           |
| Coerência     | Se a resposta faz sentido dentro do contexto do usuário |

## 🎬 Principais diferenciais
- Personalização: utiliza dados reais do usuário para gerar exemplos
- Execução local: funciona com Ollama, sem necessidade de APIs externas
- Foco educacional: prioriza o aprendizado em vez de recomendações
- Confiabilidade: possui estratégias para evitar respostas incorretas

## 📚 Documentação

Mais detalhes sobre o funcionamento, prompts e estrutura do projeto estão disponíveis na pasta [`docs/`](./docs/).