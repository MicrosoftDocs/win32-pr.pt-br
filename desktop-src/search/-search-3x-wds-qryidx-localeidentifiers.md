---
description: entenda os argumentos inputlocale e keywordlocale na pesquisa Windows, que ajuda o mecanismo de pesquisa a usar os separadores de palavras corretos.
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: argumentos de identificador de localidade (pesquisa Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43a9a8b85f65ab7b8f8d13a8b50e619d11143bde99d13695875212562d71acbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117681155"
---
# <a name="locale-identifier-arguments-windows-search"></a>argumentos de identificador de localidade (pesquisa Windows)

Os `inputlocale` `keywordlocale` identificadores e ajudam o mecanismo de pesquisa a usar os separadores de palavras corretos identificando o idioma das consultas inseridas pelo usuário e o idioma o das palavras-chave da sintaxe de consulta avançada. esses nem sempre são os mesmos identificadores de código de linguagem (lcids) porque Windows pesquisa é oferecida em várias versões internacionais e também inclui MUI packs para mais idiomas. O InputLocale identifica o LCID para a linguagem na qual os usuários inserim sua consulta de pesquisa, enquanto o keywordlocale identifica o LCID que o mecanismo de pesquisa usa para palavras-chave.

Este tópico é organizado da seguinte maneira:

-   [Exemplo](#example)
-   [Tópicos relacionados](#related-topics)

## <a name="example"></a>Exemplo


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com argumentos de Parameter-Value](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Argumento de trilha](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[Argumento de sintaxe](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argumento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[Argumento de subconsulta](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



