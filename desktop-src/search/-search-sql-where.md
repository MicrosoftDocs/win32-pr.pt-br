---
description: As condições que determinam se um documento está incluído nos resultados retornados pela consulta são especificadas pela cláusula WHERE.
ms.assetid: e3b5ee92-e817-49b8-aa8b-5d68254bb819
title: Cláusula WHERE (pesquisa do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45a37334d656b0a321abdcdd4a5d045eb9d4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779923"
---
# <a name="where-clause-windows-search"></a>Cláusula WHERE (pesquisa do Windows)

As condições que determinam se um documento está incluído nos resultados retornados pela consulta são especificadas pela cláusula WHERE. No nível mais alto, há duas partes para a sintaxe da cláusula WHERE:


```
...WHERE [<group_aliases>] <search_condition>
...WHERE ReuseWhere(<WHEREID>)
```



O \_ alias de grupo de <opcional> parte da cláusula simplifica consultas complexas atribuindo um alias a um grupo de uma ou mais colunas. Isso pode melhorar a legibilidade de consultas complexas que pesquisam as mesmas informações em várias colunas especificadas por URLs. Para obter mais informações sobre aliases de grupo, consulte [with--como predicado de alias de grupo](-search-sql-with-as.md).

A <search condition> parte da cláusula WHERE é um ou mais predicados de pesquisa que especificam critérios de correspondência para a pesquisa. Os predicados de pesquisa são expressões que afirmam algum fato sobre algum valor.

O resultado de um critério de pesquisa é um valor booliano, seja **verdadeiro** se o documento atender aos critérios de pesquisa especificados ou **false** se não tiver. Se o resultado for **true**, o documento será retornado. Se o resultado for **false**, o documento não será retornado. Os documentos retornados em uma consulta do Microsoft Windows Search recebem valores de classificação de acordo com o quão bem eles correspondem às condições de pesquisa. Cada uma das condições de pesquisa de consulta pode incluir uma cláusula [RANKBY](-search-sql-rankby.md) que dá suporte à modificação dos valores de classificação retornados.

A [função ReuseWhere](-search-sql-reusewhere.md) faz várias consultas que usam algumas das mesmas condições de pesquisa mais eficientes. A cláusula WHERE em uma consulta especifica o conjunto de itens que correspondem em uma consulta. As consultas subsequentes podem compartilhar o trabalho executado para o evalution anterior usando a função ReuseWhere na nova cláusula WHERE de consulta.

## <a name="search-predicates"></a>Predicados de pesquisa

Um critério de pesquisa consiste em um ou mais predicados ou critérios de pesquisa que descrevem o que o usuário está procurando (por exemplo, em que System. DateCreated > ' 2006-04-19 '). Os predicados de pesquisa podem ser combinados usando os operadores lógicos **e** **, ou, ou** **não**. O operador unário opcional **não** pode ser usado apenas com **and** e somente para negar o valor lógico de um predicado ou critério de pesquisa. Você pode usar parênteses para agrupar e aninhar termos lógicos.

A tabela a seguir mostra a ordem de precedência para os operadores lógicos.



| Ordem (precedência) | Operador lógico |
|--------------------|------------------|
| Primeiro (mais alto)    | **NOT**          |
| Segundo             | **AND**          |
| Terceiro (mais baixo)     | **OR**           |



 

Os operadores lógicos do mesmo tipo são associativos e não há nenhuma ordem de cálculo especificada. Por exemplo, (A **e** b) **e** (c **e** D) podem ser calculados (a **e** d) **e** (B **e** C) sem alteração no resultado lógico.

> [!IMPORTANT]
>
> Incorreto: onde **não** contém (' computador ')
>
> Correto: onde contém (' software ') **e não** contém (' Computer ')

 

Em consultas complexas, talvez você queira posicionar mais ênfase nas correspondências em algumas colunas do que em outras. Por exemplo, ao pesquisar documentos que abordam "design de software", encontrar o termo de pesquisa no título do documento é mais provável que seja uma boa correspondência do que localizar as palavras individuais no texto do documento. Para influenciar a classificação de documentos dessa maneira, a linguagem de consulta do Microsoft Windows Search dá suporte à ponderação de critérios de pesquisa. Para obter mais informações sobre o peso de coluna, consulte contém predicado [Contains](-search-sql-contains.md) e [FREETEXT predicado](-search-sql-freetext.md).

Há três grupos de predicados de pesquisa no Windows Search: pesquisas de texto completo, texto não completo e profundidade de pasta. Os predicados de pesquisa de texto completo normalmente correspondem ao significado do conteúdo, título e outras colunas e dão suporte à correspondência lingüística (por exemplo, formas de palavras alternativas, frases e pesquisa de proximidade). Por outro lado, os predicados de pesquisa de texto não completo correspondem ao valor das colunas especificadas e não incluem nenhum processamento linguístico especial, mas, em vários casos, oferecem correspondência de padrão baseada em caracteres. Os predicados de profundidade de pasta restringem o escopo de pesquisa a um caminho especificado.

> [!Note]  
> Se a consulta retornar um documento porque um predicado de texto não completo é avaliado como **verdadeiro** para esse documento, o valor de classificação é calculado como 1000. O uso da [função de coerção de classificação](-search-sql-rankby.md) pode modificar o valor de classificação.

 

As tabelas a seguir descrevem os predicados de pesquisa de texto completo, de texto não completo e de profundidade de pasta.



| Predicado de texto completo                  | Descrição                                                                                                                                                                                                                                                      |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CONTAINS](-search-sql-contains.md) | Dá suporte a pesquisas complexas de termos em colunas de texto do documento (por exemplo, título, conteúdo). Pode pesquisar formulários formas flexionadas dos termos de pesquisa, testar a proximidade dos termos e executar comparações lógicas. Os termos de pesquisa podem incluir caracteres curinga. |
| [FREETEXT](-search-sql-freetext.md) | Procura documentos que correspondam ao significado da frase de pesquisa. Palavras relacionadas e frases semelhantes serão correspondentes, com a coluna de classificação calculada com base em quão próximo o documento corresponde à frase de pesquisa. Os termos de pesquisa não podem incluir caracteres curinga.  |



 



| Predicado de texto não completo                                                    | Description                                                                                                                                                                           |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LIKE](-search-sql-like.md)                                               | Os valores de coluna são comparados usando a correspondência de padrão simples com caracteres curinga.                                                                                                    |
| [Comparação de valor literal](-search-sql-literalvaluecomparison.md)         | Os valores de coluna são comparados com valores literais de cadeia de caracteres, data, carimbo de hora, numéricos e outros. Esse predicado dá suporte a igualdade e desigualdades, como maior que e menor que. |
| [Comparações de vários valores (matriz)](-search-sql-multivaluedcomparisons.md) | As colunas com valores de multivalor são comparadas com uma matriz de valores literais.                                                                                                             |
| [NULL](-search-sql-null.md)                                               | Os valores de coluna que são indefinidos para o documento podem ser detectados usando o predicado **NULL** .                                                                                    |



 



| Profundidade da pasta                             | Description                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------|
| [COM](-search-sql-folderdepth.md)     | Executa uma passagem profunda do caminho especificado, incluindo a pasta específica e todas as subpastas. |
| [ACTIVE](-search-sql-folderdepth.md) | Executa uma passagem superficial do caminho especificado, pesquisando apenas a pasta específica.            |



 

## <a name="examples"></a>Exemplos

Para obter exemplos da cláusula WHERE, consulte os tópicos de predicado individuais vinculados na tabela anterior.

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

[Visão geral da sintaxe de pesquisa SQL](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[Como predicado de alias de grupo--AS](-search-sql-with-as.md)
</dt> <dt>

[Predicados de escopo e diretório](-search-sql-folderdepth.md)
</dt> <dt>

[CLASSIFICAR por cláusula](-search-sql-rankby.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados de texto não completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



