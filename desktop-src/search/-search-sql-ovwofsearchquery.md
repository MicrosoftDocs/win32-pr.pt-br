---
description: O Windows Search linguagem SQL (SQL) é semelhante a uma consulta SQL padrão.
ms.assetid: 7d992fa2-4606-46ca-904c-b45056a9bbc2
title: Visão geral da sintaxe SQL do Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff6a755312e4358dc2eaa9ea7ae97f22ef783f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010389"
---
# <a name="overview-of-windows-search-sql-syntax"></a>Visão geral da sintaxe SQL do Windows Search

O Windows Search linguagem SQL (SQL) é semelhante a uma consulta SQL padrão. Ele é mostrado nas duas sintaxes a seguir:


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

A sintaxe de consulta do Windows Search dá suporte a várias opções, permitindo consultas mais complicadas.

A tabela a seguir descreve cada cláusula nas instruções SELECT ou GROUP ON e os recursos com suporte.

| Cláusula                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AGRUPAR EM... SOBRE...](-search-sql-group-on-over.md) | Especifica como agrupar os resultados retornados pela consulta. Você pode especificar os intervalos pelos quais agrupar e especificar mais de uma coluna para Agrupamento. Por exemplo, você pode agrupar os resultados em um intervalo de tamanhos de arquivo (tamanho < 100, 100 <= tamanho < 1000; 1000 <= tamanho) e aninhar agrupamentos.                                                                                                       |
| [SELECT](-search-sql-select.md)                    | Especifica as colunas retornadas pela consulta.                                                                                                                                                                                                                                                                                                                                                         |
| [FROM](-search-sql-from.md)                        | Especifica o computador e o catálogo a serem pesquisados.                                                                                                                                                                                                                                                                                                                                                         |
| [WHERE](-search-sql-where.md)                      | Especifica o que constitui um documento correspondente. Essa cláusula tem muitas opções, permitindo um controle avançado sobre os critérios de pesquisa. Por exemplo, você pode fazer a correspondência com palavras, frases, formas de palavras informativas, cadeias de caracteres, valores numéricos e de bit-chave e matrizes com vários valores. Você também pode aplicar pesos estatísticos às condições de correspondência e combinar condições de correspondência com operadores boolianos. |
| [ORDER BY](-search-sql-orderby.md)                 | Especifica a ordem de classificação dos resultados retornados pela consulta. Você pode especificar mais de um campo no qual os resultados são classificados e pode usar ordenação crescente ou decrescente.                                                                                                                                                                                                               |

### <a name="code-samples"></a>Exemplos de código

O exemplo de código WSSQL demonstra como se comunicar entre o Microsoft OLE DB e o Windows Search por meio do SQL. O exemplo de código WSOleDB ilustra Active Template Library (ATL) OLE DB acesso aos aplicativos do Windows Search e dois métodos adicionais para recuperar os resultados do Windows Search. Ambos os exemplos estão disponíveis no [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).

## <a name="related-topics"></a>Tópicos relacionados

### <a name="reference"></a>Referência

[Literais](-search-sql-literals.md)

[Usando pesquisas localizadas](-search-sql-usinglocsearches.md)

[Noções básicas sobre valores de relevância](-search-sql-understandingrelevancevalues.md)

[Mapeamentos de propriedade](-search-3x-wds-propertymappings.md)

[Sintaxe de consulta avançada](-search-3x-advancedquerysyntax.md)

### <a name="conceptual"></a>Conceitual

[Extensões do SQL no Microsoft Windows Search](-search-sql-extensions-sps.md)

[Recursos do SQL não disponíveis no Microsoft Windows Search](-search-sql-featuresunavailableinspssearch.md)

[Identificadores](-search-sql-identifiers.md)

[Distinção de maiúsculas e minúsculas em pesquisas](-search-sql-casesensitivityinsearches.md)

[Sensibilidade de diacríticos em pesquisas](-search-sql-accentinsensitivitysearches.md)

[Convertendo o tipo de dados de uma coluna](-search-sql-castingdatacolumntype.md)

[Mapeamentos de tipo de dados](-search-sql-datatypemappings.md)
