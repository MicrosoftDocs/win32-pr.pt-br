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
# <a name="dynamic-graph-building"></a><span data-ttu-id="0a95d-103">Criação de grafo dinâmico</span><span class="sxs-lookup"><span data-stu-id="0a95d-103">Dynamic Graph Building</span></span>

<span data-ttu-id="0a95d-104">Se você precisar modificar um grafo de filtro existente, poderá parar o grafo, fazer as alterações e reiniciar o grafo.</span><span class="sxs-lookup"><span data-stu-id="0a95d-104">If you need to modify an existing filter graph, you can stop the graph, make the changes, and restart the graph.</span></span> <span data-ttu-id="0a95d-105">Normalmente, essa é a melhor abordagem.</span><span class="sxs-lookup"><span data-stu-id="0a95d-105">This is usually the best approach.</span></span> <span data-ttu-id="0a95d-106">No entanto, em algumas circunstâncias, talvez você queira alterar um grafo enquanto ele ainda estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="0a95d-106">However, under some circumstances, you might want to alter a graph while it is still running.</span></span> <span data-ttu-id="0a95d-107">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="0a95d-107">For example:</span></span>

-   <span data-ttu-id="0a95d-108">O aplicativo insere um filtro de efeitos de vídeo durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="0a95d-108">The application inserts a video effects filter during playback.</span></span>
-   <span data-ttu-id="0a95d-109">Um filtro de origem alterna os tipos de mídia fluxo intermediário, possivelmente exigindo um novo filtro de descompactação.</span><span class="sxs-lookup"><span data-stu-id="0a95d-109">A source filter switches media types midstream, possibly requiring a new decompression filter.</span></span>
-   <span data-ttu-id="0a95d-110">O aplicativo adiciona um novo fluxo de vídeo ao grafo.</span><span class="sxs-lookup"><span data-stu-id="0a95d-110">The application adds a new video stream to the graph.</span></span>

<span data-ttu-id="0a95d-111">Esses são exemplos de *criação de grafo dinâmico*, um termo que cobre qualquer tipo de alteração em um grafo de filtro enquanto o grafo continua a ser executado.</span><span class="sxs-lookup"><span data-stu-id="0a95d-111">These are all examples of *dynamic graph building*, a term that covers any kind of change to a filter graph while the graph continues to run.</span></span> <span data-ttu-id="0a95d-112">A criação dinâmica de gráficos pode ser iniciada por um aplicativo ou por um filtro no grafo.</span><span class="sxs-lookup"><span data-stu-id="0a95d-112">Dynamic graph building can be initiated by an application or by a filter in the graph.</span></span> <span data-ttu-id="0a95d-113">Três cenários distintos são possíveis:</span><span class="sxs-lookup"><span data-stu-id="0a95d-113">Three distinct scenarios are possible:</span></span>

-   <span data-ttu-id="0a95d-114">[Alterações de formato dinâmico](dynamic-format-changes.md): um filtro pode alterar os formatos fluxo intermediário, sem a necessidade de remover ou substituir filtros.</span><span class="sxs-lookup"><span data-stu-id="0a95d-114">[Dynamic Format Changes](dynamic-format-changes.md): A filter can change formats midstream, without the need to remove or replace any filters.</span></span>
-   <span data-ttu-id="0a95d-115">[Reconexão dinâmica](dynamic-reconnection.md): alterando o grafo adicionando ou removendo filtros.</span><span class="sxs-lookup"><span data-stu-id="0a95d-115">[Dynamic Reconnection](dynamic-reconnection.md): Changing the graph by adding or removing filters.</span></span>
-   <span data-ttu-id="0a95d-116">[Cadeias de filtro](filter-chains.md): adição, remoção e controle de cadeias de filtros.</span><span class="sxs-lookup"><span data-stu-id="0a95d-116">[Filter Chains](filter-chains.md): Adding, removing, and controlling chains of filters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a95d-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a95d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a95d-118">Sobre o DirectShow</span><span class="sxs-lookup"><span data-stu-id="0a95d-118">About DirectShow</span></span>](about-directshow.md)
</dt> </dl>

 

 



