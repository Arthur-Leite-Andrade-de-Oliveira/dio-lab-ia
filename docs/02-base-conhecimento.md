# Base de Conhecimento

## 📊 Dados utilizados

**O funcionamento do agente depende de diferentes arquivos que fornecem contexto:**

- perfil_investidor.json: usado para personalizar as respostas
- transacoes.csv: permite analisar gastos do usuário
- historico_atendimento.csv: mantém contexto de interações anteriores
- produtos_financeiros.json: base para explicar produtos financeiros

---

## 🔧 Ajustes realizados


Foi feita uma adaptação na base de dados, substituindo o produto “Fundo Multimercado” por “Fundo Imobiliário (FII)”, com o objetivo de trabalhar apenas com conteúdos que sejam mais familiares e fáceis de validar.

---

## ⚙️ Estratégia de uso dos dados

**Os dados podem ser utilizados de duas formas:**

- inseridos diretamente no prompt
- carregados via código

**Exemplo de carregamento:**

```python
import pandas as pd
import json

perfil = json.load(open('./data/perfil_investidor.json'))
transacoes = pd.read_csv('./data/transacoes.csv')
historico = pd.read_csv('./data/historico_atendimento.csv')
produtos = json.load(open('./data/produtos_financeiros.json'))
```

## 🧠 Uso no contexto

Os dados são inseridos no prompt para fornecer contexto ao modelo, permitindo respostas mais personalizadas.

Também é possível resumir essas informações para reduzir uso de tokens, mantendo apenas os dados mais relevantes.