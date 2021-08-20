---
description: O predicado FREETEXT faz parte da cláusula WHERE e dá suporte à pesquisa de palavras e frases em colunas de texto.
ms.assetid: 8afc95d1-25cd-4448-8bee-d132c2da22b3
title: Predicado FREETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f9fb3d65c1b9dc72ef74c8c6862ccfb778ebbd4149b9e5bf5aca4d36674045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863402"
---
# <a name="freetext-predicate"></a>Predicado FREETEXT

O predicado FREETEXT faz parte da [cláusula WHERE](-search-sql-where.md) e dá suporte à pesquisa de palavras e frases em colunas de texto. Use o predicado FREETEXT para localizar documentos que contenham combinações das palavras de pesquisa distribuídas em todo o conteúdo ou colunas especificadas. Para obter o valor de classificação, inclua System.Search.Rank, que é uma classificação de relevence, como uma coluna na instrução SELECT.

O predicado FREETEXT tem a seguinte sintaxe:


```
FREETEXT
(["<fulltext_column>",]'<freetext_condition>'[,<LCID>])...
```



A referência de coluna de texto completo é opcional. Com ele, você pode especificar uma única coluna ou um alias de [grupo](-search-sql-with-as.md) de colunas no qual o predicado FREETEXT é testado. Quando a coluna de texto completo é especificada como "ALL" ou " ", todas \* as propriedades de texto indexadas são pesquisadas. Embora a coluna não seja necessária para ser uma propriedade de texto, os resultados poderão não ter sentido se a coluna for algum outro tipo de dados. O nome da coluna pode ser um [identificador](-search-sql-identifiers.md)regular ou delimitado e você deve separá-lo da condição por uma vírgula. Se nenhuma condição de texto completo for fornecida, a coluna Conteúdo, que é o corpo do documento, será usada.

Você pode especificar uma localidade de pesquisa para identificar o disjuntor de palavras apropriado e formulários não flexíveis para a consulta de pesquisa. Os valores de localidade válidos são Windows LCID (identificador de código de idioma padrão). Por exemplo, 1033 é o LCID para Estados Unidos inglês. Coloque o LCID como o último item dentro dos parênteses da cláusula FREETEXT. Para obter informações importantes sobre pesquisa e idiomas, consulte [Usando pesquisas localizadas.](-search-sql-usinglocsearches.md)

> [!Note]  
> A localidade de pesquisa padrão é a localidade padrão do sistema.

 

Você deve colocar a parte da condição de texto livre entre aspas simples e ela deve consistir em um ou mais termos de pesquisa. O predicado FREETEXT não dá suporte a operações lógicas. Para pesquisar uma frase como se fosse uma única palavra, coloque a frase entre aspas duplas.

Quando você usa o predicado FREETEXT, os resultados da consulta de pesquisa retornam documentos que contêm todos os termos de pesquisa. Os termos não precisam aparecer em nenhuma ordem específica. Documentos que contêm mais dos termos de pesquisa têm valores de coluna de classificação mais altos.

## <a name="examples"></a>Exemplos

O exemplo a seguir pesquisa documentos que contêm "computador", "software", "hardware" ou combinações dessas palavras:


```
WHERE FREETEXT('computer software hardware')
```



> [!Note]  
> Não é possível usar a correspondência de palavras simples e a correspondência de frases no mesmo predicado FREETEXT.

 

Ao executar consultas com contrações, você deve escapar as aspas na contração ao usar FREETEXT, mas não ao usar CONTAINS.

Por exemplo, a sintaxe a seguir falha:


```
WHERE FREETEXT(*,'"We'll meet next week"')
```



A sintaxe correta inclui duas aspas simples, não aspas duplas.

A sintaxe a seguir é bem-sucedida:


```
WHERE FREETEXT(*,'"We''ll meet next week"')
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Predicado CONTAINS](-search-sql-contains.md)
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Predicados que não são de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



