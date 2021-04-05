---
description: Os identificadores InputLocale e keywordlocale ajudam o mecanismo de pesquisa a usar os separadores de palavras corretos identificando o idioma das consultas inseridas pelo usuário e o idioma do das palavras-chave da sintaxe de consulta avançada.
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: Argumentos de identificador de localidade (pesquisa do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea1549a550e4bf6b8099241a6f3d2275860a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826920"
---
# <a name="locale-identifier-arguments-windows-search"></a>Argumentos de identificador de localidade (pesquisa do Windows)

Os `inputlocale` `keywordlocale` identificadores e ajudam o mecanismo de pesquisa a usar os separadores de palavras corretos identificando o idioma das consultas inseridas pelo usuário e o idioma o das palavras-chave da sintaxe de consulta avançada. Esses nem sempre são os mesmos identificadores de código de linguagem (LCIDs) porque o Windows Search é oferecido em várias versões internacionais e também inclui MUI Packs para mais idiomas. O InputLocale identifica o LCID para a linguagem na qual os usuários inserim sua consulta de pesquisa, enquanto o keywordlocale identifica o LCID que o mecanismo de pesquisa usa para palavras-chave.

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

 

 



