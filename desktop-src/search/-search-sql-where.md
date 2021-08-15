---
description: As condições que determinam se um documento está incluído nos resultados retornados pela consulta são especificadas pela cláusula WHERE.
ms.assetid: e3b5ee92-e817-49b8-aa8b-5d68254bb819
title: Cláusula WHERE (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e711219ff8eea81e8c4f8fd8145baccc35f49389d412f0e4ac088aa06666643
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462398"
---
# <a name="where-clause-windows-search"></a>Cláusula WHERE (Windows Search)

As condições que determinam se um documento está incluído nos resultados retornados pela consulta são especificadas pela cláusula WHERE. No nível mais alto, há duas partes para a sintaxe da cláusula WHERE:


```
...WHERE [<group_aliases>] <search_condition>
...WHERE ReuseWhere(<WHEREID>)
```



O alias <grupo opcional> parte da cláusula simplifica consultas complexas atribuindo um alias a um grupo de uma ou \_ mais colunas. Isso pode melhorar a leitura de consultas complexas que pesquisam as mesmas informações em várias colunas especificadas por URLs. Para obter mais informações sobre aliases de grupo, [consulte WITH -- AS Group Alias Predicate](-search-sql-with-as.md).

A <search condition> parte da cláusula WHERE é um ou mais predicados de pesquisa que especificam critérios de correspondência para a pesquisa. Predicados de pesquisa são expressões que declaram algum fato sobre algum valor.

O resultado de uma condição de pesquisa é um valor booliana, **TRUE** se o documento atender às condições de pesquisa especificadas ou **FALSE** se não atender. Se o resultado for **TRUE,** o documento será retornado. Se o resultado for **FALSE,** o documento não será retornado. Os documentos retornados em uma consulta do Microsoft Windows Search são atribuídos a valores de classificação de acordo com o nível de eles corresponderem às condições de pesquisa. Cada uma das condições de pesquisa de consulta pode incluir uma [cláusula RANKBY](-search-sql-rankby.md) que dá suporte à modificação dos valores de classificação retornados.

A [função ReuseWhere](-search-sql-reusewhere.md) torna várias consultas que usam algumas das mesmas condições de pesquisa mais eficientes. A cláusula WHERE em uma consulta especifica o conjunto de itens que corresponderem em uma consulta. As consultas subsequentes podem compartilhar o trabalho executado para a evasão anterior usando a função ReuseWhere na nova cláusula WHERE da consulta.

## <a name="search-predicates"></a>Predicados de pesquisa

Uma condição de pesquisa consiste em um ou mais predicados ou condições de pesquisa que descrevem o que o usuário está procurando (por exemplo, WHERE System.DateCreated >'2006-04-19'). Predicados de pesquisa podem ser combinados usando os operadores **lógicos AND**, **OR** ou **NOT**. O operador unário **opcional NOT** pode ser usado somente com **AND** e apenas para negar o valor lógico de um predicado ou condição de pesquisa. Você pode usar parênteses para agrupar e aninhar termos lógicos.

A tabela a seguir mostra a ordem de precedência para os operadores lógicos.



| Ordem (precedência) | Operador lógico |
|--------------------|------------------|
| Primeiro (mais alto)    | **NOT**          |
| Segundo             | **AND**          |
| Terceiro (mais baixo)     | **OR**           |



 

Operadores lógicos do mesmo tipo são associativos e não há nenhuma ordem de cálculo especificada. Por exemplo, (A **AND** B) **AND** (C **AND** D) pode ser calculado (A **AND** D) **AND** (B **E** C) sem nenhuma alteração no resultado lógico.

> [!IMPORTANT]
>
> Incorreto: WHERE **NOT** CONTAINS ('computer')
>
> Correto: WHERE CONTAINS ('software') **AND NOT** CONTAINS ('computer')

 

Em consultas complexas, talvez você queira enfatizar mais as correspondeções em algumas colunas do que em outras. Por exemplo, ao pesquisar documentos que discutem "design de software", encontrar o termo de pesquisa no título do documento é mais provável que seja uma boa combinação do que encontrar as palavras individuais no texto do documento. Para influenciar a classificação de documentos dessa maneira, a linguagem de consulta do Microsoft Windows Search dá suporte à ponderação das condições de pesquisa. Para obter mais informações sobre a ponderação de coluna, consulte [Predicado CONTAINS](-search-sql-contains.md) e [Predicado FREETEXT](-search-sql-freetext.md).

Há três grupos de predicados de pesquisa Windows Search: pesquisa de texto completo, não texto completo e profundidade de pasta. Os predicados de pesquisa de texto completo normalmente coincidem com o significado do conteúdo, do título e de outras colunas e da correspondência linguística de suporte (por exemplo, formulários de palavras alternativos, frases e pesquisa por proximidade). Por outro lado, predicados de pesquisa de texto não completo coincidem com o valor das colunas especificadas e não incluem nenhum processamento linguístico especial, mas em vários casos oferecem correspondência de padrões baseados em caracteres. Predicados de profundidade de pasta restringem o escopo da pesquisa a um caminho especificado.

> [!Note]  
> Se a consulta retornar um documento porque um predicado de texto não completo é avaliada como **TRUE** para esse documento, o valor de classificação será calculado como 1000. Usar a [função de coerção de classificação](-search-sql-rankby.md) pode modificar o valor de classificação.

 

As tabelas a seguir descrevem os predicados de pesquisa de texto completo, não texto completo e profundidade de pasta.



| Predicado de texto completo                  | Descrição                                                                                                                                                                                                                                                      |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CONTAINS](-search-sql-contains.md) | Dá suporte a pesquisas complexas para termos em colunas de texto de documento (por exemplo, título, conteúdo). Pode pesquisar formulários inflectados dos termos de pesquisa, testar a proximidade dos termos e executar comparações lógicas. Os termos de pesquisa podem incluir caracteres curinga. |
| [FREETEXT](-search-sql-freetext.md) | Pesquisa documentos que corresponderem ao significado da frase de pesquisa. Palavras relacionadas e frases semelhantes corresponderão, com a coluna de classificação calculada com base na proximidade com que o documento corresponde à frase de pesquisa. Os termos de pesquisa não podem incluir caracteres curinga.  |



 



| Predicado de texto não completo                                                    | Descrição                                                                                                                                                                           |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LIKE](-search-sql-like.md)                                               | Os valores de coluna são comparados usando a correspondência de padrões simples com caracteres curinga.                                                                                                    |
| [Comparação de valor literal](-search-sql-literalvaluecomparison.md)         | Os valores de coluna são comparados com cadeia de caracteres, data, carimbo de data/hora, numérico e outros valores literais. Esse predicado dá suporte à igualdade e às desigualdades, como maior que e menor que. |
| [Comparações com vários valores (ARRAY)](-search-sql-multivaluedcomparisons.md) | Colunas com vários valores são comparadas com uma matriz de literais com vários valores.                                                                                                             |
| [NULL](-search-sql-null.md)                                               | Os valores de coluna indefinido para o documento podem ser detectados usando o **predicado NULL.**                                                                                    |



 



| Profundidade da pasta                             | Descrição                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Escopo](-search-sql-folderdepth.md)     | Executa uma travessia profunda do caminho especificado, incluindo a pasta específica e todas as subpastas. |
| [Diretório](-search-sql-folderdepth.md) | Executa uma travessia superficial do caminho especificado, pesquisando apenas a pasta específica.            |



 

## <a name="examples"></a>Exemplos

Para exemplos da cláusula WHERE, consulte os tópicos de predicado individuais vinculados na tabela anterior.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Função ReuseWhere](-search-sql-reusewhere.md)
</dt> <dt>

[Propriedades do conjunto de linhas](-search-sql-rowset-properties.md)
</dt> <dt>

[Cláusula FROM](-search-sql-from.md)
</dt> <dt>

[Visão geral da sintaxe de SQL pesquisa](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[WITH – Predicado de alias de grupo AS](-search-sql-with-as.md)
</dt> <dt>

[Predicados SCOPE e DIRECTORY](-search-sql-folderdepth.md)
</dt> <dt>

[Cláusula RANK BY](-search-sql-rankby.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados que não são de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



