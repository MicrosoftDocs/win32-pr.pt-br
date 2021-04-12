---
description: Threads e seções críticas
ms.assetid: e55acb06-03f4-4191-bffe-3196f41ef2c7
title: Threads e seções críticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576cb28e7e382db92328adf09980a825e71b5a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297716"
---
# <a name="threads-and-critical-sections"></a><span data-ttu-id="a327d-103">Threads e seções críticas</span><span class="sxs-lookup"><span data-stu-id="a327d-103">Threads and Critical Sections</span></span>

<span data-ttu-id="a327d-104">Esta seção descreve o Threading em filtros do DirectShow e as etapas que você deve seguir para evitar falhas ou deadlocks em um filtro personalizado.</span><span class="sxs-lookup"><span data-stu-id="a327d-104">This section describes threading in DirectShow filters, and the steps you should take to avoid crashes or deadlocks in a custom filter.</span></span>

<span data-ttu-id="a327d-105">Os exemplos nesta seção usam o pseudocódigo para ilustrar o código que você precisará escrever.</span><span class="sxs-lookup"><span data-stu-id="a327d-105">The examples in this section use pseudocode to illustrate the code you will need to write.</span></span> <span data-ttu-id="a327d-106">Eles supõem que um filtro personalizado está usando classes derivadas das classes base do DirectShow, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a327d-106">They assume that a custom filter is using classes derived from the DirectShow base classes, as follows:</span></span>

-   <span data-ttu-id="a327d-107">CMyInputPin: derivado de [**CBaseInputPin**](cbaseinputpin.md).</span><span class="sxs-lookup"><span data-stu-id="a327d-107">CMyInputPin: Derived from [**CBaseInputPin**](cbaseinputpin.md).</span></span>
-   <span data-ttu-id="a327d-108">CMyOutputPin: derivado de [**CBaseOutputPin**](cbaseoutputpin.md).</span><span class="sxs-lookup"><span data-stu-id="a327d-108">CMyOutputPin: Derived from [**CBaseOutputPin**](cbaseoutputpin.md).</span></span>
-   <span data-ttu-id="a327d-109">CMyFilter: derivado de [**CBaseFilter**](cbasefilter.md).</span><span class="sxs-lookup"><span data-stu-id="a327d-109">CMyFilter: Derived from [**CBaseFilter**](cbasefilter.md).</span></span>
-   <span data-ttu-id="a327d-110">CMyInputAllocator: o alocador do pino de entrada derivado de [**CMemAllocator**](cmemallocator.md).</span><span class="sxs-lookup"><span data-stu-id="a327d-110">CMyInputAllocator: The input pin's allocator, derived from [**CMemAllocator**](cmemallocator.md).</span></span> <span data-ttu-id="a327d-111">Nem todo filtro precisa de um alocador personalizado.</span><span class="sxs-lookup"><span data-stu-id="a327d-111">Not every filter needs a custom allocator.</span></span> <span data-ttu-id="a327d-112">Para muitos filtros, a classe **CMemAllocator** é suficiente.</span><span class="sxs-lookup"><span data-stu-id="a327d-112">For many filters, the **CMemAllocator** class is sufficient.</span></span>

<span data-ttu-id="a327d-113">Esta seção contém os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="a327d-113">This section contains the following topics.</span></span>

-   [<span data-ttu-id="a327d-114">Os threads de streaming e aplicativo</span><span class="sxs-lookup"><span data-stu-id="a327d-114">The Streaming and Application Threads</span></span>](the-streaming-and-application-threads.md)
-   [<span data-ttu-id="a327d-115">Pausando</span><span class="sxs-lookup"><span data-stu-id="a327d-115">Pausing</span></span>](pausing.md)
-   [<span data-ttu-id="a327d-116">Recebendo e entregando exemplos</span><span class="sxs-lookup"><span data-stu-id="a327d-116">Receiving and Delivering Samples</span></span>](receiving-and-delivering-samples.md)
-   [<span data-ttu-id="a327d-117">Entregando o fim do fluxo</span><span class="sxs-lookup"><span data-stu-id="a327d-117">Delivering the End of Stream</span></span>](delivering-the-end-of-stream.md)
-   [<span data-ttu-id="a327d-118">Liberando dados</span><span class="sxs-lookup"><span data-stu-id="a327d-118">Flushing Data</span></span>](flushing-data.md)
-   [<span data-ttu-id="a327d-119">Parando</span><span class="sxs-lookup"><span data-stu-id="a327d-119">Stopping</span></span>](stopping.md)
-   [<span data-ttu-id="a327d-120">Obtendo buffers</span><span class="sxs-lookup"><span data-stu-id="a327d-120">Getting Buffers</span></span>](getting-buffers.md)
-   [<span data-ttu-id="a327d-121">Threads de streaming e o Gerenciador de gráfico de filtro</span><span class="sxs-lookup"><span data-stu-id="a327d-121">Streaming Threads and the Filter Graph Manager</span></span>](streaming-threads-and-the-filter-graph-manager.md)
-   [<span data-ttu-id="a327d-122">Resumo do encadeamento de filtro</span><span class="sxs-lookup"><span data-stu-id="a327d-122">Summary of Filter Threading</span></span>](summary-of-filter-threading.md)

## <a name="related-topics"></a><span data-ttu-id="a327d-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a327d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a327d-124">Fluxo de dados para os desenvolvedores de filtro</span><span class="sxs-lookup"><span data-stu-id="a327d-124">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> <dt>

[<span data-ttu-id="a327d-125">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="a327d-125">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



