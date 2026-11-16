# Protótipo Figma — Transparência Cidadã

- **Arquivo:** [Prototipo_Projeto_Web](https://www.figma.com/design/KB6jSOOuxBwaP17SqW903c/Prototipo_Projeto_Web)
- **Página:** 01 — Discovery e Interface
- **Escopo:** quatro telas desktop
- **Identidade visual:** fundo cinza-azulado claro, cabeçalho azul-marinho, acentos azuis, superfícies brancas, bordas claras e tipografia Inter.

## Frames

| Tela | Frame | Link direto |
|---|---|---|
| 01 | Dashboard — Desktop | [Abrir no Figma](https://www.figma.com/design/KB6jSOOuxBwaP17SqW903c/Prototipo_Projeto_Web?node-id=54-162) |
| 02 | Consultar — Desktop | [Abrir no Figma](https://www.figma.com/design/KB6jSOOuxBwaP17SqW903c/Prototipo_Projeto_Web?node-id=18-5) |
| 03 | Comparar — Desktop | [Abrir no Figma](https://www.figma.com/design/KB6jSOOuxBwaP17SqW903c/Prototipo_Projeto_Web?node-id=61-2) |
| 04 | Sobre — Desktop | [Abrir no Figma](https://www.figma.com/design/KB6jSOOuxBwaP17SqW903c/Prototipo_Projeto_Web?node-id=63-11) |

## 01 — Dashboard

Componentes:
1. Cabeçalho e navegação;
2. Título e descrição do painel;
3. Filtros básicos;
4. Busca por palavra-chave;
5. Cabeçalho e linhas da tabela;
6. Paginação.

Colunas: órgão responsável, investimento/projeto, localidade, valor previsto, valor executado e situação.

**Captura exportada:** `docs/imagens/Dashboard - Desktop.png`.

## 02 — Consultar investimentos

Filtros por período, órgão, esfera, tipo de investimento, região administrativa e situação. A tela também apresenta busca por palavra-chave, tabela de resultados e paginação.

## 03 — Comparar investimentos

Filtros por período, região administrativa e tipo de investimento; cartões-resumo; áreas reservadas a gráficos de distribuição e série histórica; tabela comparativa do GDF e do Governo Federal no DF.

Os valores, gráficos e indicadores permanecem como placeholders até a definição e integração de dados oficiais.

## 04 — Sobre e metodologia

Apresenta o propósito do projeto, o escopo institucional, o fluxo de consulta, os princípios metodológicos e as categorias de fontes oficiais previstas.

## Observações para desenvolvimento

- O Figma é referência visual, não implementação funcional;
- Filtros, busca, paginação e navegação precisam de lógica e estados reais;
- O protótipo não define API, modelo definitivo de dados ou fonte de cada campo;
- Identificar fonte, período de referência e data de atualização;
- Não apresentar placeholders como registros oficiais;
- Implementar estados de carregamento, vazio, erro e ausência de dados;
- Respeitar acessibilidade por teclado, rótulos e contraste;
- Consultar também `docs/implementacao-programadores.md`.

## Capturas

A captura PNG atualmente versionada corresponde ao Dashboard. As outras telas podem ser abertas nos links diretos dos frames acima; suas capturas exportadas deverão ser adicionadas posteriormente a `docs/imagens/`.
