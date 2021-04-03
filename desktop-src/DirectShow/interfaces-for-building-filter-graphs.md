---
description: Interfaces para criação de gráficos de filtro
ms.assetid: 18d5217a-7f4e-49e9-ac14-2f4ba229e065
title: Interfaces para criação de gráficos de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862d581f44a711cc6f2aa094210571995b15005b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645777"
---
# <a name="interfaces-for-building-filter-graphs"></a><span data-ttu-id="33f64-103">Interfaces para criação de gráficos de filtro</span><span class="sxs-lookup"><span data-stu-id="33f64-103">Interfaces for Building Filter Graphs</span></span>

<span data-ttu-id="33f64-104">Os aplicativos usam essas interfaces para criar vários tipos de grafos de filtro.</span><span class="sxs-lookup"><span data-stu-id="33f64-104">Applications use these interfaces to build various types of filter graphs.</span></span>



| <span data-ttu-id="33f64-105">Interface</span><span class="sxs-lookup"><span data-stu-id="33f64-105">Interface</span></span>                                                  | <span data-ttu-id="33f64-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="33f64-106">Description</span></span>                                                 |
|------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="33f64-107">**IAMFilterGraphCallback**</span><span class="sxs-lookup"><span data-stu-id="33f64-107">**IAMFilterGraphCallback**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamfiltergraphcallback)   | <span data-ttu-id="33f64-108">Receber notificações de retorno de chamada se um PIN não puder ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="33f64-108">Receive callback notifications if a pin cannot be rendered.</span></span> |
| [<span data-ttu-id="33f64-109">**IAMGraphBuilderCallback**</span><span class="sxs-lookup"><span data-stu-id="33f64-109">**IAMGraphBuilderCallback**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) | <span data-ttu-id="33f64-110">Fornece um mecanismo de retorno de chamada durante a criação do grafo.</span><span class="sxs-lookup"><span data-stu-id="33f64-110">Provides a callback mechanism during graph building.</span></span>        |
| [<span data-ttu-id="33f64-111">**ICaptureGraphBuilder2**</span><span class="sxs-lookup"><span data-stu-id="33f64-111">**ICaptureGraphBuilder2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)     | <span data-ttu-id="33f64-112">Crie gráficos de filtro para captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="33f64-112">Build filter graphs for video capture.</span></span>                      |
| [<span data-ttu-id="33f64-113">**ICreateDevEnum**</span><span class="sxs-lookup"><span data-stu-id="33f64-113">**ICreateDevEnum**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum)                   | <span data-ttu-id="33f64-114">Enumere dispositivos do sistema, como dispositivos de captura.</span><span class="sxs-lookup"><span data-stu-id="33f64-114">Enumerate system devices, such as capture devices.</span></span>          |
| [<span data-ttu-id="33f64-115">**IDvdGraphBuilder**</span><span class="sxs-lookup"><span data-stu-id="33f64-115">**IDvdGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)               | <span data-ttu-id="33f64-116">Crie gráficos de filtro para navegação e reprodução de DVD.</span><span class="sxs-lookup"><span data-stu-id="33f64-116">Build filter graphs for DVD navigation and playback.</span></span>        |
| [<span data-ttu-id="33f64-117">**IEnumFilters**</span><span class="sxs-lookup"><span data-stu-id="33f64-117">**IEnumFilters**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ienumfilters)                       | <span data-ttu-id="33f64-118">Enumere os filtros no grafo.</span><span class="sxs-lookup"><span data-stu-id="33f64-118">Enumerate the filters in the graph.</span></span>                         |
| [<span data-ttu-id="33f64-119">**IFilterGraph2**</span><span class="sxs-lookup"><span data-stu-id="33f64-119">**IFilterGraph2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)                     | <span data-ttu-id="33f64-120">Adicionar, remover ou conectar filtros.</span><span class="sxs-lookup"><span data-stu-id="33f64-120">Add, remove, or connect filters.</span></span>                            |
| [<span data-ttu-id="33f64-121">**IFilterMapper2**</span><span class="sxs-lookup"><span data-stu-id="33f64-121">**IFilterMapper2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)                   | <span data-ttu-id="33f64-122">Enumere os filtros registrados no sistema do usuário.</span><span class="sxs-lookup"><span data-stu-id="33f64-122">Enumerate the filters registered on the user's system.</span></span>      |
| [<span data-ttu-id="33f64-123">**IGraphBuilder**</span><span class="sxs-lookup"><span data-stu-id="33f64-123">**IGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)                     | <span data-ttu-id="33f64-124">Crie gráficos de filtro para reprodução de arquivos ou para usos personalizados.</span><span class="sxs-lookup"><span data-stu-id="33f64-124">Build filter graphs for file playback or for custom uses.</span></span>   |
| [<span data-ttu-id="33f64-125">**IGraphConfig**</span><span class="sxs-lookup"><span data-stu-id="33f64-125">**IGraphConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)                       | <span data-ttu-id="33f64-126">Reconfigurar dinamicamente um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="33f64-126">Dynamically reconfigure a filter graph.</span></span>                     |
| [<span data-ttu-id="33f64-127">**IGraphVersion**</span><span class="sxs-lookup"><span data-stu-id="33f64-127">**IGraphVersion**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphversion)                     | <span data-ttu-id="33f64-128">Determine quando o grafo é alterado.</span><span class="sxs-lookup"><span data-stu-id="33f64-128">Determine when the graph changes.</span></span>                           |



 

 

 



