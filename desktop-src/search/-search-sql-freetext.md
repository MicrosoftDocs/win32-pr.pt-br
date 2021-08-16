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

O predicado FREETEXT faz parte da cláusula [Where](-search-sql-where.md) e dá suporte à pesquisa de palavras e frases em colunas de texto. Use o predicado FREETEXT para localizar documentos que contenham combinações das palavras de pesquisa espalhadas em todo o conteúdo ou colunas especificadas. Para obter o valor de classificação, inclua System. Search. Rank, que é uma classificação de relevence, como uma coluna na instrução SELECT.

O predicado FREETEXT tem a seguinte sintaxe:


```
FREETEXT
(["<fulltext_column>",]'<freetext_condition>'[,<LCID>])...
```



A referência de coluna de texto completo é opcional. Com ele, você pode especificar uma única coluna ou um [alias de agrupamento de colunas](-search-sql-with-as.md) em relação ao qual o predicado FREETEXT é testado. Quando a coluna FULLTEXT é especificada como "ALL" ou " \* ", todas as propriedades de texto indexado são pesquisadas. Embora a coluna não precise ser uma propriedade de texto, os resultados poderão ser insignificantes se a coluna for outro tipo de dados. O nome da coluna pode ser um [identificador](-search-sql-identifiers.md)regular ou delimitado, e você deve separá-lo da condição por uma vírgula. Se nenhuma condição de texto completo for fornecida, a coluna conteúdo, que é o corpo do documento, será usada.

Você pode especificar uma localidade de pesquisa para identificar o separador de palavras apropriado e formulários de inflexão para a consulta de pesquisa. os valores de localidade válidos são um Windows identificador de código de idioma padrão (LCID). Por exemplo, 1033 é o LCID para o Estados Unidos-Inglês. Coloque o LCID como o último item dentro dos parênteses da cláusula FREETEXT. Para obter informações importantes sobre a pesquisa e os idiomas, consulte [usando pesquisas localizadas](-search-sql-usinglocsearches.md).

> [!Note]  
> A localidade de pesquisa padrão é a localidade padrão do sistema.

 

Você deve colocar a parte da condição FREETEXT entre aspas simples e deve consistir em um ou mais termos de pesquisa. O predicado FREETEXT não oferece suporte a operações lógicas. Para procurar uma frase como se fosse uma única palavra, coloque a frase entre aspas duplas.

Quando você usa o predicado FREETEXT, os resultados da consulta de pesquisa retornam documentos que contêm todos os termos de pesquisa. Os termos não precisam aparecer em nenhuma ordem específica. Os documentos que contêm mais termos de pesquisa têm valores de coluna de classificação mais altos.

## <a name="examples"></a>Exemplos

O exemplo a seguir procura documentos que contenham "computador", "software", "hardware" ou combinações dessas palavras:


```
WHERE FREETEXT('computer software hardware')
```



> [!Note]  
> Você não pode usar correspondência de palavra única e correspondência de frase no mesmo predicado FREETEXT.

 

Ao executar consultas com contratações, você deve escapar do sinal de aspas na contratação ao usar FREETEXT, mas não ao usar CONTAINS.

Por exemplo, a sintaxe a seguir falhará:


```
WHERE FREETEXT(*,'"We'll meet next week"')
```



A sintaxe correta inclui duas aspas simples, não uma aspa dupla.

A sintaxe a seguir é realizada com sucesso:


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

**Conceitua**
</dt> <dt>

[Predicados de texto não completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



