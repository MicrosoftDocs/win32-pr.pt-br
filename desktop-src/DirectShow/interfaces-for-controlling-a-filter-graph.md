---
description: Interfaces para controlar um grafo de filtro
ms.assetid: f7de0165-e356-45d5-baed-d127caeebaf6
title: Interfaces para controlar um grafo de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e88dc4ba2143bbbf33a58763a5ff9005254236
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646051"
---
# <a name="interfaces-for-controlling-a-filter-graph"></a><span data-ttu-id="f5813-103">Interfaces para controlar um grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="f5813-103">Interfaces for Controlling a Filter Graph</span></span>

<span data-ttu-id="f5813-104">Essas interfaces fornecem métodos para controlar um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="f5813-104">These interfaces provide methods for controlling a filter graph.</span></span>



| <span data-ttu-id="f5813-105">Interface</span><span class="sxs-lookup"><span data-stu-id="f5813-105">Interface</span></span>                                  | <span data-ttu-id="f5813-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5813-106">Description</span></span>                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5813-107">**IAMClockAdjust**</span><span class="sxs-lookup"><span data-stu-id="f5813-107">**IAMClockAdjust**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust)   | <span data-ttu-id="f5813-108">Ajuste o relógio do grafo.</span><span class="sxs-lookup"><span data-stu-id="f5813-108">Adjust the graph clock.</span></span>                                                                                   |
| [<span data-ttu-id="f5813-109">**IAMGraphStreams**</span><span class="sxs-lookup"><span data-stu-id="f5813-109">**IAMGraphStreams**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams) | <span data-ttu-id="f5813-110">Sincronizar fluxos ao vivo em um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="f5813-110">Synchronize live streams in a filter graph.</span></span>                                                               |
| [<span data-ttu-id="f5813-111">**IFilterChain**</span><span class="sxs-lookup"><span data-stu-id="f5813-111">**IFilterChain**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)       | <span data-ttu-id="f5813-112">Cadeias de controle de filtros.</span><span class="sxs-lookup"><span data-stu-id="f5813-112">Control chains of filters.</span></span>                                                                                |
| [<span data-ttu-id="f5813-113">**IMediaControl**</span><span class="sxs-lookup"><span data-stu-id="f5813-113">**IMediaControl**</span></span>](/windows/desktop/api/Control/nn-control-imediacontrol)     | <span data-ttu-id="f5813-114">Execute, pause e interrompa o gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="f5813-114">Run, pause, and stop the filter graph.</span></span> <span data-ttu-id="f5813-115">(Também fornece métodos compatíveis com a automação para a criação de grafos.)</span><span class="sxs-lookup"><span data-stu-id="f5813-115">(Also provides Automation-compatible methods for building graphs.)</span></span> |
| [<span data-ttu-id="f5813-116">**IMediaEventEx**</span><span class="sxs-lookup"><span data-stu-id="f5813-116">**IMediaEventEx**</span></span>](/windows/desktop/api/Control/nn-control-imediaeventex)     | <span data-ttu-id="f5813-117">Responder a eventos no grafo.</span><span class="sxs-lookup"><span data-stu-id="f5813-117">Respond to events in the graph.</span></span>                                                                           |
| [<span data-ttu-id="f5813-118">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="f5813-118">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)     | <span data-ttu-id="f5813-119">Busque dentro de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f5813-119">Seek within a file.</span></span>                                                                                       |
| [<span data-ttu-id="f5813-120">**IQueueCommand**</span><span class="sxs-lookup"><span data-stu-id="f5813-120">**IQueueCommand**</span></span>](/windows/desktop/api/Control/nn-control-iqueuecommand)     | <span data-ttu-id="f5813-121">Comandos de fila para serem executados mais tarde.</span><span class="sxs-lookup"><span data-stu-id="f5813-121">Queue commands to run at a later time.</span></span>                                                                    |
| [<span data-ttu-id="f5813-122">**IVideoFrameStep**</span><span class="sxs-lookup"><span data-stu-id="f5813-122">**IVideoFrameStep**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) | <span data-ttu-id="f5813-123">Quadro – percorrer um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f5813-123">Frame-step through a video stream.</span></span>                                                                        |



 

 

 



