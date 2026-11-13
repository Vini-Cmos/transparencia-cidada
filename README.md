# Transparência Cidadã

**Acompanhamento de investimentos públicos no Distrito Federal**

Projeto de interface para consulta e acompanhamento de investimentos realizados pelo Governo do Distrito Federal (GDF) e pelo Governo Federal no Distrito Federal.

> **Estado atual:** protótipo visual da primeira tela (Dashboard — Desktop) desenvolvido no Figma. A interface ainda precisa ser implementada em código e conectada a fontes de dados para que filtros, pesquisa, tabela e paginação funcionem.

## Objetivo

Facilitar a consulta pública de informações sobre investimentos realizados no Distrito Federal, oferecendo uma interface organizada para localizar, visualizar e futuramente comparar registros.

## Escopo planejado

O projeto está organizado em quatro telas principais:

1. **Início — Dashboard:** visão inicial, filtros, pesquisa e tabela de investimentos.
2. **Consultar investimentos:** consulta detalhada dos registros.
3. **Comparar investimentos:** comparação entre investimentos do GDF e do Governo Federal.
4. **Sobre e metodologia:** apresentação do projeto, fontes de dados e critérios utilizados.

## Protótipo — primeira tela

A primeira tela foi construída no Figma e contém:

- Cabeçalho e navegação principal;
- Filtros por período, órgão, esfera e tipo de investimento;
- Pesquisa por palavra-chave;
- Tabela com órgão responsável, investimento/projeto, localidade, valor previsto, valor executado e situação;
- Paginação dos resultados.

### Captura da interface

![Dashboard — Desktop](docs/imagens/Dashboard%20-%20Desktop.png)

**Arquivo Figma:** `Prototipo_Projeto_Web`  
**Página:** `01 — Discovery e Interface`  
**Frame:** `Dashboard — Desktop`

## Estrutura do repositório

```text
transparencia-cidada/
├── README.md
├── docs/
│   ├── imagens/
│   │   └── Dashboard - Desktop.png
│   ├── planejamento.md
│   └── paginas.md
├── design/
│   └── prototipo-figma.md
└── src/
    └── (implementação a ser iniciada)
```

## Estado de desenvolvimento

| Entrega | Situação |
|---|---|
| Protótipo visual do Dashboard | Concluído |
| Documentação inicial | Em andamento |
| Implementação HTML/CSS/JavaScript | A iniciar |
| Integração com fontes de dados | A definir |
| Telas 02, 03 e 04 | Planejadas |
| Testes funcionais e responsivos | A realizar |

## Orientações para implementação

O protótipo Figma é a referência visual. A equipe de desenvolvimento deverá:

- Reproduzir a hierarquia e o estilo visual do Dashboard;
- Implementar comportamento real para filtros, pesquisa e paginação;
- Definir e documentar as fontes de dados antes de apresentar registros como oficiais;
- Tratar estados de carregamento, ausência de resultados e erros;
- Garantir acessibilidade e adaptação a diferentes tamanhos de tela.

**Importante:** os textos exibidos nas linhas da tabela do protótipo são marcadores de posição, não registros reais de investimentos.

## Contribuição

As decisões de interface devem ser documentadas no Figma e as alterações de código versionadas neste repositório. Novas funcionalidades devem ser acompanhadas por tarefas no GitHub Issues/Projects e submetidas para revisão antes de integrar à branch principal.

## Licença

A definir.
