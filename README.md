# AURA AI — Inteligência Conversacional

> Transformando conversas em inteligência de negócio.

A **AURA AI** é um projeto acadêmico desenvolvido em grupo para o **TOTVS Challenge 2026**, durante o 2º ano de Engenharia de Software da FIAP.

A ideia surgiu a partir de um problema bem comum em equipes comerciais: reuniões geram uma grande quantidade de informação, mas parte desses dados acaba se perdendo ou depende de uma análise manual para virar alguma ação.

A proposta da AURA AI é transformar essas transcrições em informações que possam apoiar decisões comerciais, ajudando a identificar **oportunidades, sinais de insatisfação, riscos de churn e interesses em produtos**.

Neste repositório, o foco está principalmente na etapa de **Data Science e NLP**, mostrando como os dados das reuniões foram preparados e analisados.

---

## O que o projeto busca resolver

Durante uma reunião comercial, podem aparecer informações importantes sobre o cliente, como uma necessidade que ainda não foi atendida, interesse em uma solução, reclamações ou sinais de que o cliente pode estar insatisfeito.

O problema é que essas informações estão presentes em textos não estruturados e nem sempre são aproveitadas depois da reunião.

A AURA AI foi pensada para ajudar nesse processo, transformando a transcrição em dados que possam ser analisados e utilizados pelo time comercial.

### Principais possibilidades da solução

- Identificação de oportunidades comerciais;
- Detecção de sinais de insatisfação;
- Apoio à identificação de possíveis riscos de churn;
- Identificação de interesses recorrentes dos clientes;
- Mapeamento de produtos mencionados nas conversas;
- Geração de insights para apoiar decisões comerciais.

---

## Data Science e NLP

A parte de Data Science do projeto trabalha diretamente com as transcrições das reuniões.

O notebook apresenta o fluxo utilizado pelo grupo:

**Dados → Limpeza dos textos → TF-IDF → Análise exploratória → Insights de negócio**

### 1. Preparação dos dados

Os textos das transcrições passam por uma etapa de tratamento para deixá-los mais adequados à análise. Foram consideradas diferenças de capitalização, pontuação, caracteres especiais e palavras muito frequentes que não agregam tanto valor à análise.

Também foi criada a coluna `texto_limpo`, utilizada nas etapas seguintes do processamento.

### 2. TF-IDF

Foi utilizado **TF-IDF (Term Frequency-Inverse Document Frequency)** para transformar os textos em uma representação numérica e identificar termos relevantes dentro das reuniões.

No notebook, o modelo considera palavras isoladas e combinações de duas palavras, além de limitar a quantidade de características utilizadas na análise.

A escolha do TF-IDF foi feita por ser uma técnica simples, interpretável e adequada para uma primeira análise das transcrições.

### 3. Análise exploratória

Depois do tratamento dos textos, foi feita uma análise de frequência dos termos presentes nas reuniões. O projeto também utiliza gráficos para facilitar a visualização dos termos mais frequentes.

Essa etapa ajuda a encontrar padrões de linguagem que podem servir como ponto de partida para identificar oportunidades, riscos e outros sinais relevantes para o negócio.

### 4. Embeddings

O projeto também apresenta a diferença entre TF-IDF e **embeddings**, mostrando como representações vetoriais mais semânticas podem ser utilizadas em uma evolução futura da solução.

A ideia é que embeddings possam complementar a abordagem atual em tarefas que dependem mais de contexto e significado, como identificação de intenção, sentimento e oportunidades comerciais.

---

## Tecnologias utilizadas

- **Python**
- **Pandas** — manipulação e análise dos dados
- **NumPy** — operações numéricas
- **Matplotlib** — visualização dos dados
- **Scikit-learn** — aplicação do TF-IDF
- **Regex** — limpeza e normalização dos textos
- **Jupyter Notebook / Google Colab** — desenvolvimento e documentação da análise

---

## Estrutura do repositório

```text
AURA-AI/
├── README.md
├── notebooks/
│   └── AuraAI_Challenge_DataScience.ipynb
└── data/
    └── DADOS.csv
```

> A estrutura pode receber novos arquivos conforme as outras partes do projeto forem adicionadas ao repositório.

---

## Como executar

A análise foi desenvolvida em notebook e pode ser executada pelo **Google Colab** ou localmente com Jupyter Notebook.

1. Clone o repositório:

```bash
git clone https://github.com/victoralves13/AURA-AI.git
```

2. Abra o notebook localizado em:

```text
notebooks/AuraAI_Challenge_DataScience.ipynb
```

3. Instale as principais bibliotecas utilizadas:

```bash
pip install pandas numpy matplotlib scikit-learn
```

4. Certifique-se de que o arquivo de dados esteja disponível no caminho esperado pelo notebook antes de executar as células.

---

## Sobre o projeto acadêmico

A AURA AI foi desenvolvida como parte do **TOTVS Challenge 2026**, com o objetivo de aplicar conhecimentos de Engenharia de Software, Data Science, NLP e modelagem de dados em um problema de negócio.

O projeto não representa apenas uma análise isolada de textos. A proposta do grupo considera uma solução maior, na qual as análises de reuniões podem futuramente fazer parte de um fluxo completo de coleta, processamento, armazenamento e visualização das informações.

A modelagem do projeto também foi estruturada pensando nessa evolução, com entidades relacionadas a clientes, reuniões, transcrições, análises de IA, alertas e produtos TOTVS.

---

## Equipe

Projeto desenvolvido em grupo por estudantes de Engenharia de Software da FIAP:

- **João Guilherme** — RM565244
- **Matheus Kitamura** — RM563205
- **Gustavo Barroso** — RM565705
- **Victor Alves** — RM565723

---

## O que aprendemos com o projeto

Um dos principais aprendizados foi entender como transformar um problema de negócio em uma análise de dados de verdade: primeiro entender o problema, depois preparar os dados, escolher uma técnica adequada, analisar os resultados e, por fim, relacionar esses resultados com possíveis decisões de negócio.

Também foi uma oportunidade de trabalhar com NLP na prática e entender as diferenças entre uma abordagem baseada em frequência, como TF-IDF, e técnicas mais voltadas para representação semântica, como embeddings.

---

## Próximos passos

Entre as evoluções que fazem sentido para a AURA AI estão:

- utilização de embeddings para uma análise mais semântica;
- evolução da identificação de sentimento, intenção e oportunidades;
- geração automática de alertas comerciais;
- integração com uma aplicação e um dashboard;
- conexão com o modelo de dados desenvolvido para a solução;
- utilização de modelos de IA mais avançados para complementar a análise.

---

**AURA AI — Escute mais. Descubra mais. Venda melhor.**
