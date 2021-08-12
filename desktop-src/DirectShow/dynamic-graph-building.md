---
description: criação de Graph dinâmico
ms.assetid: 13fed430-979b-40f7-91ba-aff2d811bd92
title: criação de Graph dinâmico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c7296b95bc97461eb5a16ee577acb4bd267ee1a25f9be357a00fef7d4bdba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652786"
---
# <a name="dynamic-graph-building"></a>criação de Graph dinâmico

Se você precisar modificar um grafo de filtro existente, poderá parar o grafo, fazer as alterações e reiniciar o grafo. Normalmente, essa é a melhor abordagem. No entanto, em algumas circunstâncias, talvez você queira alterar um grafo enquanto ele ainda estiver em execução. Por exemplo:

-   O aplicativo insere um filtro de efeitos de vídeo durante a reprodução.
-   Um filtro de origem alterna os tipos de mídia fluxo intermediário, possivelmente exigindo um novo filtro de descompactação.
-   O aplicativo adiciona um novo fluxo de vídeo ao grafo.

Esses são exemplos de *criação de grafo dinâmico*, um termo que cobre qualquer tipo de alteração em um grafo de filtro enquanto o grafo continua a ser executado. A criação dinâmica de gráficos pode ser iniciada por um aplicativo ou por um filtro no grafo. Três cenários distintos são possíveis:

-   [Alterações de formato dinâmico](dynamic-format-changes.md): um filtro pode alterar os formatos fluxo intermediário, sem a necessidade de remover ou substituir filtros.
-   [Reconexão dinâmica](dynamic-reconnection.md): alterando o grafo adicionando ou removendo filtros.
-   [Cadeias de filtro](filter-chains.md): adição, remoção e controle de cadeias de filtros.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre DirectShow](about-directshow.md)
</dt> </dl>

 

 



