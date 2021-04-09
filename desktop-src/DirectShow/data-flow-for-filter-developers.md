---
description: Fluxo de dados para os desenvolvedores de filtro
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: Fluxo de dados para os desenvolvedores de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb4e4123e8617190a459ff500d1100c0dbbb8ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104010058"
---
# <a name="data-flow-for-filter-developers"></a><span data-ttu-id="e1bd8-103">Fluxo de dados para os desenvolvedores de filtro</span><span class="sxs-lookup"><span data-stu-id="e1bd8-103">Data Flow for Filter Developers</span></span>

<span data-ttu-id="e1bd8-104">Esta seção descreve detalhadamente como os dados são movidos pelo grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="e1bd8-104">This section describes in detail how data moves through the filter graph.</span></span> <span data-ttu-id="e1bd8-105">Ele se concentra no transporte de memória local usando a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ou [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="e1bd8-105">It focuses on local memory transport using the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) or [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span> <span data-ttu-id="e1bd8-106">Ele é destinado a desenvolvedores que estão escrevendo seus próprios filtros personalizados.</span><span class="sxs-lookup"><span data-stu-id="e1bd8-106">It is intended for developers who are writing their own custom filters.</span></span> <span data-ttu-id="e1bd8-107">Para obter uma introdução geral sobre como o Microsoft DirectShow lida com o fluxo de dados, consulte [fluxo de dados no grafo de filtro](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="e1bd8-107">For a general introduction to how Microsoft DirectShow handles data flow, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="e1bd8-108">Muitos dados se movem por um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="e1bd8-108">A lot of data moves through a filter graph.</span></span> <span data-ttu-id="e1bd8-109">Ele se encaixa basicamente em duas categorias: dados de mídia e dados de controle.</span><span class="sxs-lookup"><span data-stu-id="e1bd8-109">It falls roughly into two categories: media data and control data.</span></span> <span data-ttu-id="e1bd8-110">Em geral, os dados de mídia viajam por downstream e controlam upstream.</span><span class="sxs-lookup"><span data-stu-id="e1bd8-110">In general, media data travels downstream and control data travels upstream.</span></span> <span data-ttu-id="e1bd8-111">Os dados de mídia incluem quadros de vídeo, amostras de áudio, pacotes MPEG e assim por diante que compõem um fluxo, mas também incluem comandos de liberação, notificações de fim de fluxo e outros dados que trafegam com o fluxo.</span><span class="sxs-lookup"><span data-stu-id="e1bd8-111">Media data includes the video frames, audio samples, MPEG packets, and so forth that make up a stream, but also includes flush commands, end-of-stream notifications, and other data that travels with the stream.</span></span> <span data-ttu-id="e1bd8-112">Os dados de controle não fazem parte do fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e1bd8-112">Control data is not part of the media stream.</span></span> <span data-ttu-id="e1bd8-113">Exemplos de dados de controle são solicitações de controle de qualidade e comandos de busca.</span><span class="sxs-lookup"><span data-stu-id="e1bd8-113">Examples of control data are quality-control requests and seek commands.</span></span>

<span data-ttu-id="e1bd8-114">Esta seção contém os artigos a seguir.</span><span class="sxs-lookup"><span data-stu-id="e1bd8-114">This section contains the following articles.</span></span>

-   [<span data-ttu-id="e1bd8-115">Entregando exemplos</span><span class="sxs-lookup"><span data-stu-id="e1bd8-115">Delivering Samples</span></span>](delivering-samples.md)
-   [<span data-ttu-id="e1bd8-116">Processando dados</span><span class="sxs-lookup"><span data-stu-id="e1bd8-116">Processing Data</span></span>](processing-data.md)
-   [<span data-ttu-id="e1bd8-117">Notificações de fim de fluxo</span><span class="sxs-lookup"><span data-stu-id="e1bd8-117">End-of-Stream Notifications</span></span>](end-of-stream-notifications.md)
-   [<span data-ttu-id="e1bd8-118">Novos segmentos</span><span class="sxs-lookup"><span data-stu-id="e1bd8-118">New Segments</span></span>](new-segments.md)
-   [<span data-ttu-id="e1bd8-119">Liberação</span><span class="sxs-lookup"><span data-stu-id="e1bd8-119">Flushing</span></span>](flushing.md)
-   [<span data-ttu-id="e1bd8-120">Atingir</span><span class="sxs-lookup"><span data-stu-id="e1bd8-120">Seeking</span></span>](seeking.md)
-   [<span data-ttu-id="e1bd8-121">Alterações de formato dinâmico</span><span class="sxs-lookup"><span data-stu-id="e1bd8-121">Dynamic Format Changes</span></span>](dynamic-format-changes.md)

## <a name="related-topics"></a><span data-ttu-id="e1bd8-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1bd8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1bd8-123">Gerenciamento de controle de qualidade</span><span class="sxs-lookup"><span data-stu-id="e1bd8-123">Quality-Control Management</span></span>](quality-control-management.md)
</dt> <dt>

[<span data-ttu-id="e1bd8-124">Threads e seções críticas</span><span class="sxs-lookup"><span data-stu-id="e1bd8-124">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> <dt>

[<span data-ttu-id="e1bd8-125">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="e1bd8-125">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



