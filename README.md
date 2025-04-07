☕ Projeto: Mineração de Conhecimento com Azure AI Search – Fourth Coffee

🎯 Objetivo
Criar uma solução que analisa avaliações de clientes e fornece insights valiosos usando IA, NLP e Azure Cognitive Search.

✅ ETAPA 1 – Criar os Recursos no Azure
- Criar o recurso Azure AI Search (plano Free ou Basic).
- Criar uma Conta de Armazenamento (Blob Storage).
- Fazer upload dos dados de entrada, como avaliacoes.json, comentarios.csv, etc.

✅ ETAPA 2 – Criar a Fonte de Dados
- No portal do Azure AI Search, clique em "Importar dados".
- Escolha o Blob Storage como origem.
- Aponte para o arquivo ou container que contém as avaliações de clientes.

✅ ETAPA 3 – Configurar o Skillset (Enriquecimento com IA)
- Ative a opção de enriquecimento cognitivo.
- Adicione as seguintes habilidades (skills):
  - Detecção de idioma
  - Análise de sentimento
  - Extração de frases-chave
  - Reconhecimento de entidades nomeadas
- (Opcional) Ative o Knowledge Store para salvar os dados enriquecidos.

✅ ETAPA 4 – Criar o Índice e o Indexador
- Crie um índice de busca com os seguintes campos:
  - id, comentario, cliente, data, sentimento, frases-chave, entidades
- Marque os campos apropriados como pesquisáveis.
- Crie o indexador que conecta a origem de dados ao índice, aplicando o skillset.

✅ ETAPA 5 – Testar no Explorador de Busca
- Use o Search Explorer no Azure AI Search para testar buscas como:
  - "excelente atendimento"
  - "demora" (com filtro de sentimento negativo)
  - Buscar por frases-chave como "expresso", "cappuccino", etc.

✅ ETAPA 6 – Acessar o Knowledge Store (Opcional)
- Os dados enriquecidos serão salvos automaticamente em uma nova pasta do Blob Storage.
- Esses dados podem ser integrados com:
  - Power BI
  - Dashboards
  - Aplicações web

✅ Resultados Esperados
- Relatórios com análise de sentimentos dos clientes
- Identificação de principais reclamações e elogios
- Busca contextual inteligente com NLP
- Base sólida para decisões estratégicas e melhoria do atendimento
