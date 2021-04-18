---
description: Transportes
ms.assetid: 63c5ff5b-293d-4a80-92e8-3ece41321095
title: Transportes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3d87ffacc871fc45ef1e8e645849afc956fb1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810379"
---
# <a name="transports"></a><span data-ttu-id="648b5-103">Transportes</span><span class="sxs-lookup"><span data-stu-id="648b5-103">Transports</span></span>

<span data-ttu-id="648b5-104">Para mover os dados de mídia por meio do grafo de filtro, um filtro do DirectShow deve dar suporte a um dos vários protocolos possíveis.</span><span class="sxs-lookup"><span data-stu-id="648b5-104">In order to move media data through the filter graph, a DirectShow filter must support one of several possible protocols.</span></span> <span data-ttu-id="648b5-105">Esses protocolos são chamados de transportes.</span><span class="sxs-lookup"><span data-stu-id="648b5-105">These protocols are called transports.</span></span> <span data-ttu-id="648b5-106">Quando dois filtros se conectam, eles devem dar suporte ao mesmo transporte; caso contrário, eles não poderão trocar dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="648b5-106">When two filters connect, they must support the same transport; otherwise they cannot exchange media data.</span></span> <span data-ttu-id="648b5-107">Normalmente, um transporte requer que um dos Pins dê suporte a uma interface específica.</span><span class="sxs-lookup"><span data-stu-id="648b5-107">Typically, a transport requires that one of the pins support a particular interface.</span></span> <span data-ttu-id="648b5-108">Quando os filtros se conectam, um PIN consulta o outro para a interface.</span><span class="sxs-lookup"><span data-stu-id="648b5-108">When the filters connect, one pin queries the other for the interface.</span></span>

<span data-ttu-id="648b5-109">A maioria dos filtros do DirectShow mantém os dados de mídia na memória principal e os entrega para outros filtros em conexões de PIN.</span><span class="sxs-lookup"><span data-stu-id="648b5-109">Most DirectShow filters hold media data in main memory, and deliver it to other filters across pin connections.</span></span> <span data-ttu-id="648b5-110">Esse tipo de transporte é chamado de transporte de memória local.</span><span class="sxs-lookup"><span data-stu-id="648b5-110">This type of transport is called local memory transport.</span></span> <span data-ttu-id="648b5-111">Embora o transporte de memória local seja o transporte mais comum no DirectShow, nem todos os filtros o utilizam.</span><span class="sxs-lookup"><span data-stu-id="648b5-111">Although local memory transport is the most common transport in DirectShow, not all filters use it.</span></span> <span data-ttu-id="648b5-112">Por exemplo, alguns filtros enviam dados de mídia ao longo de um caminho de hardware e usam Pins apenas para fornecer informações de controle.</span><span class="sxs-lookup"><span data-stu-id="648b5-112">For example, some filters send media data along a hardware path, and use pins only to deliver control information.</span></span> <span data-ttu-id="648b5-113">Por exemplo, consulte a interface [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) .</span><span class="sxs-lookup"><span data-stu-id="648b5-113">For example, see the [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) interface.</span></span>

<span data-ttu-id="648b5-114">O DirectShow define dois mecanismos para o transporte de memória local, o modelo de push e o modelo de pull.</span><span class="sxs-lookup"><span data-stu-id="648b5-114">DirectShow defines two mechanisms for local memory transport, the push model and the pull model.</span></span> <span data-ttu-id="648b5-115">No modelo de push, um filtro de origem gera dados e os entrega para o próximo filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="648b5-115">In the push model, a source filter generates data and delivers it to the next filter downstream.</span></span> <span data-ttu-id="648b5-116">Esse filtro recebe passivamente os dados, processa-os e envia-os ainda mais downstream.</span><span class="sxs-lookup"><span data-stu-id="648b5-116">That filter passively receives the data, processes it, and sends it further downstream.</span></span> <span data-ttu-id="648b5-117">No modelo de pull, o filtro de origem é conectado a um filtro do analisador.</span><span class="sxs-lookup"><span data-stu-id="648b5-117">In the pull model, the source filter is connected to a parser filter.</span></span> <span data-ttu-id="648b5-118">O filtro do analisador solicita dados do filtro de origem.</span><span class="sxs-lookup"><span data-stu-id="648b5-118">The parser filter requests data from the source filter.</span></span> <span data-ttu-id="648b5-119">O filtro de origem responde às solicitações fornecendo dados.</span><span class="sxs-lookup"><span data-stu-id="648b5-119">The source filter responds to the requests by delivering data.</span></span> <span data-ttu-id="648b5-120">O modelo de push usa a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) e o modelo de pull usa a interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="648b5-120">The push model uses the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, and the pull model uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

<span data-ttu-id="648b5-121">O modelo de Push é mais comum do que o modelo de pull.</span><span class="sxs-lookup"><span data-stu-id="648b5-121">The push model is more common than the pull model.</span></span> <span data-ttu-id="648b5-122">Portanto, os artigos a seguir pressupõem um modelo de push.</span><span class="sxs-lookup"><span data-stu-id="648b5-122">Therefore, the articles that follow assume a push model.</span></span> <span data-ttu-id="648b5-123">O último artigo nesta seção, [pull Model](pull-model.md), descreve como a interface **IAsyncReader** difere de **IMemInputPin**.</span><span class="sxs-lookup"><span data-stu-id="648b5-123">The last article in this section, [Pull Model](pull-model.md), describes how the **IAsyncReader** interface differs from **IMemInputPin**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="648b5-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="648b5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="648b5-125">Fluxo de dados no grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="648b5-125">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



