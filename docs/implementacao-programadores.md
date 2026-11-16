# Especificação inicial para a equipe de desenvolvimento

Este documento complementa o protótipo Figma. Ele registra o comportamento esperado e os pontos que precisam de decisão técnica. Não substitui a validação dos requisitos nem define uma API antes da escolha das fontes.

## Escopo institucional

A aplicação deve distinguir:
- **GDF:** investimentos realizados por órgãos e entidades do Governo do Distrito Federal;
- **Governo Federal no DF:** investimentos de origem federal cuja execução ou localização esteja vinculada ao Distrito Federal.

A origem do recurso, o órgão responsável e a localização do investimento são dimensões distintas e não devem ser confundidas.

## Telas e comportamento esperado

### 01 — Dashboard

Referência: [Dashboard — Desktop](https://www.figma.com/design/KB6jSOOuxBwaP17SqW903c/Prototipo_Projeto_Web?node-id=54-162)

- Exibir os filtros básicos de período, órgão, esfera e tipo;
- Permitir pesquisa por palavra-chave e limpeza dos critérios;
- Exibir tabela com órgão, projeto, localidade, valor previsto, valor executado e situação;
- Permitir paginação;
- Ao abrir, mostrar um estado inicial coerente (por exemplo, registros recentes ou instrução para filtrar), decisão a validar com a equipe.

### 02 — Consultar investimentos

Referência: [Consultar — Desktop](https://www.figma.com/design/KB6jSOOuxBwaP17SqW903c/Prototipo_Projeto_Web?node-id=18-5)

- Fornecer filtros por período, órgão, esfera, tipo, região administrativa e situação;
- Combinar filtros entre si;
- Executar a pesquisa por palavra-chave;
- Atualizar tabela e paginação com base no conjunto filtrado;
- Informar quando não houver resultados;
- Preservar os filtros ao navegar entre páginas, conforme decisão de UX.

### 03 — Comparar investimentos

Referência: [Comparar — Desktop](https://www.figma.com/design/KB6jSOOuxBwaP17SqW903c/Prototipo_Projeto_Web?node-id=61-2)

- Aplicar período, região administrativa e tipo como recorte comparativo;
- Exibir separadamente os indicadores do GDF e do Governo Federal no DF;
- Alimentar os gráficos de distribuição e evolução histórica;
- Preencher a tabela comparativa com valor previsto, valor executado, taxa/percentual de execução e quantidade de projetos, desde que haja definições e dados comparáveis;
- Informar a fonte, o período e a data de atualização;
- Não comparar diretamente valores de universos, períodos ou conceitos orçamentários incompatíveis.

A taxa de execução não deve ser calculada sem definição do numerador, denominador e tratamento para valores previstos iguais a zero ou ausentes.

### 04 — Sobre e metodologia

Referência: [Sobre — Desktop](https://www.figma.com/design/KB6jSOOuxBwaP17SqW903c/Prototipo_Projeto_Web?node-id=63-11)

- Explicar objetivo e escopo institucional;
- Documentar o processo de identificação e consolidação;
- Identificar as fontes efetivamente integradas, com URL e data de consulta/atualização;
- Explicar limitações, campos ausentes e critérios de inclusão;
- Não tratar categorias genéricas de fontes apresentadas no protótipo como integrações já realizadas.

## Modelo de dados preliminar

A equipe técnica deverá validar a estrutura com base nos esquemas das fontes. Campos candidatos:

| Campo candidato | Finalidade |
|---|---|
| `id` | Identificador interno do registro |
| `esfera_governo` | GDF ou Governo Federal |
| `orgao_responsavel` | Órgão responsável pelo investimento |
| `nome_projeto` | Nome do investimento ou projeto |
| `localidade` | Região administrativa ou local de execução |
| `tipo_investimento` | Classificação do investimento |
| `periodo_referencia` | Período a que o dado se refere |
| `valor_previsto` | Valor previsto, com unidade e conceito definidos |
| `valor_executado` | Valor executado, com unidade e conceito definidos |
| `situacao` | Situação conforme a fonte, com mapeamento documentado |
| `fonte_url` | URL de origem do registro/conjunto |
| `atualizado_em` | Data da última atualização conhecida |

Os nomes são sugestões de trabalho, não um contrato final de API. Considerar também identificadores originais das fontes, moeda, exercício, estágio orçamentário, data de extração e regras de deduplicação quando aplicáveis.

## Estados de interface obrigatórios

- Carregando;
- Conteúdo carregado;
- Nenhum registro encontrado;
- Campo ou dado indisponível na fonte;
- Falha de comunicação/erro de serviço;
- Filtros inválidos ou intervalo de datas inconsistente.

## Requisitos transversais

- Layout responsivo para desktop, tablet e celular;
- Navegação por teclado e foco visível;
- Rótulos programáticos para filtros e botões;
- Contraste e semântica compatíveis com acessibilidade;
- Formatação de valores em reais, datas e percentuais consistente;
- Evitar somas ou comparações quando conceitos e períodos não forem equivalentes;
- Registrar a origem e a atualização dos dados exibidos.

## Pendências de decisão

1. Quais portais e bases serão as fontes oficiais de cada esfera?
2. Qual será a periodicidade de atualização?
3. Como serão conciliados registros duplicados e investimentos com mais de uma fonte de recurso?
4. Qual definição será usada para valor previsto, valor executado e percentual de execução?
5. Qual tecnologia de frontend, backend, persistência e API será adotada?

Até a validação dessas questões, manter indicadores e gráficos sem números reais.
