# Azure Cognitive Search com AI Search — Indexação e Consulta de Dados

## Visão Geral

Este projeto demonstra o uso do **Azure Cognitive Search** com recursos de **AI Search** para indexação inteligente e consulta eficiente de dados. O objetivo é explorar o potencial dessa ferramenta na construção de sistemas de busca avançados, utilizando inteligência artificial para enriquecer e compreender melhor os dados indexados.

## Etapas de Configuração

### 1. Criação do Serviço no Azure
- Acesse o portal [Azure](https://portal.azure.com)
- Busque por **"Cognitive Search"**
- Crie um novo serviço definindo:
  - Nome do recurso
  - Grupo de recursos
  - Localização
  - Plano de preços (Free para testes)

### 2. Preparação dos Dados
- Escolha uma fonte de dados: CSV, JSON, Azure Blob Storage, Cosmos DB, etc.
- Exemplo: Arquivo JSON com reviews de produtos contendo título, descrição e nota.

### 3. Criação do Indexador
- Crie uma **Data Source** conectando sua fonte de dados.
- Crie um **Skillset** para aplicar enriquecimento de AI (tradução, extração de frases-chave, OCR, etc).
- Configure o **Indexer** para mapear dados da fonte para o índice.

### 4. Criação do Índice de Busca
- Defina os campos (ex: título, descrição, nota, tags).
- Configure quais campos são **pesquisáveis**, **filtráveis**, **ordenáveis** e **retrornáveis**.

### 5. Testes e Consultas
- Use a aba **Search explorer** para testar consultas como:
```json
{
  "search": "produto excelente",
  "filter": "nota gt 4",
  "select": "titulo, descricao, nota"
}
# Azure-Cognitive-Search
