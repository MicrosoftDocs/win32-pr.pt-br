---
description: o linguagem SQL de pesquisa do Windows (SQL) é semelhante a uma consulta de SQL padrão.
ms.assetid: 7d992fa2-4606-46ca-904c-b45056a9bbc2
title: visão geral da sintaxe de SQL de pesquisa do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f34f321bef35ab9f5198345a2630d20b80275b794f53a0c47aabf7667f2e238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594736"
---
# <a name="overview-of-windows-search-sql-syntax"></a>visão geral da sintaxe de SQL de pesquisa do Windows

o linguagem SQL de pesquisa do Windows (SQL) é semelhante a uma consulta de SQL padrão. Ele é mostrado nas duas sintaxes a seguir:


```SQL
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>]
```

```SQL
GROUP ON <column> [<ranges>]
[AGGREGATE <aggregate_list>]
[ORDER BY <column> [ASC/DESC]]
OVER (<GROUP ON ...> | <SELECT...>) 
```

No exemplo de consulta a seguir, os valores de contagem de página e data de criação são retornados para todos os documentos que têm mais de 50 páginas, classificados é ordem crescente de contagem de páginas.

```SQL
SELECT System.Document.PageCount, System.DateCreated
FROM SystemIndex
WHERE (System.Document.PageCount > 50)
ORDER BY System.Document.PageCount
```

a sintaxe de consulta de Windows pesquisa dá suporte a várias opções, permitindo consultas mais complicadas.

A tabela a seguir descreve cada cláusula nas instruções SELECT ou GROUP ON e os recursos com suporte.

| Cláusula                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AGRUPAR EM... SOBRE...](-search-sql-group-on-over.md) | Especifica como agrupar os resultados retornados pela consulta. Você pode especificar os intervalos pelos quais agrupar e especificar mais de uma coluna para Agrupamento. Por exemplo, você pode agrupar os resultados em um intervalo de tamanhos de arquivo (tamanho < 100, 100 <= tamanho < 1000; 1000 <= tamanho) e aninhar agrupamentos.                                                                                                       |
| [SELECT](-search-sql-select.md)                    | Especifica as colunas retornadas pela consulta.                                                                                                                                                                                                                                                                                                                                                         |
| [FROM](-search-sql-from.md)                        | Especifica o computador e o catálogo a serem pesquisados.                                                                                                                                                                                                                                                                                                                                                         |
| [WHERE](-search-sql-where.md)                      | Especifica o que constitui um documento correspondente. Essa cláusula tem muitas opções, permitindo um controle avançado sobre os critérios de pesquisa. Por exemplo, você pode fazer a correspondência com palavras, frases, formas de palavras informativas, cadeias de caracteres, valores numéricos e de bit-chave e matrizes com vários valores. Você também pode aplicar pesos estatísticos às condições de correspondência e combinar condições de correspondência com operadores boolianos. |
| [ORDER BY](-search-sql-orderby.md)                 | Especifica a ordem de classificação dos resultados retornados pela consulta. Você pode especificar mais de um campo no qual os resultados são classificados e pode usar ordenação crescente ou decrescente.                                                                                                                                                                                                               |

### <a name="code-samples"></a>Exemplos de código

o exemplo de código WSSQL demonstra como se comunicar entre o Microsoft OLE DB e Windows pesquisar por meio de SQL. o exemplo de código WSOleDB ilustra Active Template Library (ATL) OLE DB acesso a Windows aplicativos de pesquisa e dois métodos adicionais para recuperar resultados de Windows pesquisa. Ambos os exemplos estão disponíveis em [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).

## <a name="related-topics"></a>Tópicos relacionados

### <a name="reference"></a>Referência

[Literais](-search-sql-literals.md)

[Usando pesquisas localizadas](-search-sql-usinglocsearches.md)

[Noções básicas sobre valores de relevância](-search-sql-understandingrelevancevalues.md)

[Mapeamentos de propriedade](-search-3x-wds-propertymappings.md)

[Sintaxe de consulta avançada](-search-3x-advancedquerysyntax.md)

### <a name="conceptual"></a>Conceitual

[SQL extensões no Microsoft Windows Search](-search-sql-extensions-sps.md)

[SQL recursos não disponíveis no Microsoft Windows Search](-search-sql-featuresunavailableinspssearch.md)

[Identificadores](-search-sql-identifiers.md)

[Distinção de maiúsculas e minúsculas em pesquisas](-search-sql-casesensitivityinsearches.md)

[Sensibilidade de diacríticos em pesquisas](-search-sql-accentinsensitivitysearches.md)

[Convertendo o tipo de dados de uma coluna](-search-sql-castingdatacolumntype.md)

[Mapeamentos de tipo de dados](-search-sql-datatypemappings.md)
