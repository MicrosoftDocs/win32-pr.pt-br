---
description: Criação de grafo dinâmico
ms.assetid: 13fed430-979b-40f7-91ba-aff2d811bd92
title: Criação de grafo dinâmico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710bf5f648fc91e8db6bf62d81b41327f874ddf7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105785352"
---
# <a name="dynamic-graph-building"></a>Criação de grafo dinâmico

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

[Sobre o DirectShow](about-directshow.md)
</dt> </dl>

 

 



