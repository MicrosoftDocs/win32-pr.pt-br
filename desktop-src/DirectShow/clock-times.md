---
description: Horas de relógio
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: Horas de relógio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0639fd2b38e312f30f932fcf508427cd71c054
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370093"
---
# <a name="clock-times"></a><span data-ttu-id="0d2ae-103">Horas de relógio</span><span class="sxs-lookup"><span data-stu-id="0d2ae-103">Clock Times</span></span>

<span data-ttu-id="0d2ae-104">O DirectShow define dois tempos de relógio relacionados: tempo de referência e tempo de transmissão.</span><span class="sxs-lookup"><span data-stu-id="0d2ae-104">DirectShow defines two related clock times: reference time and stream time.</span></span>

-   <span data-ttu-id="0d2ae-105">A *hora de referência* é o tempo absoluto retornado pelo relógio de referência.</span><span class="sxs-lookup"><span data-stu-id="0d2ae-105">*Reference time* is the absolute time returned by the reference clock.</span></span> <span data-ttu-id="0d2ae-106">(Consulte [relógios de referência](reference-clocks.md).)</span><span class="sxs-lookup"><span data-stu-id="0d2ae-106">(See [Reference Clocks](reference-clocks.md).)</span></span>
-   <span data-ttu-id="0d2ae-107">O *tempo de transmissão* é definido em relação ao momento em que o grafo foi iniciado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="0d2ae-107">*Stream time* is defined relative to when the graph last started running.</span></span>
    -   <span data-ttu-id="0d2ae-108">Enquanto o grafo está em execução, o fluxo de tempo é igual ao tempo de referência menos a hora de início.</span><span class="sxs-lookup"><span data-stu-id="0d2ae-108">While the graph is running, stream time equals reference time minus start time.</span></span>
    -   <span data-ttu-id="0d2ae-109">Enquanto o grafo está em pausa, o tempo de transmissão permanece no momento da transmissão quando ele estava em pausa.</span><span class="sxs-lookup"><span data-stu-id="0d2ae-109">While the graph is paused, stream time remains at the stream time when it was paused.</span></span>
    -   <span data-ttu-id="0d2ae-110">Após uma operação de busca, o tempo de fluxo é redefinido como zero.</span><span class="sxs-lookup"><span data-stu-id="0d2ae-110">After a seek operation, stream time resets to zero.</span></span>
    -   <span data-ttu-id="0d2ae-111">Enquanto o grafo é interrompido, o tempo de transmissão é indefinido.</span><span class="sxs-lookup"><span data-stu-id="0d2ae-111">While the graph is stopped, stream time is undefined.</span></span>

<span data-ttu-id="0d2ae-112">Quando um exemplo de mídia tem um carimbo de data/hora *t*, isso significa que o exemplo deve ser renderizado em tempo *t* do fluxo.</span><span class="sxs-lookup"><span data-stu-id="0d2ae-112">When a media sample has a time stamp *t*, it means the sample should be rendered at stream time *t*.</span></span> <span data-ttu-id="0d2ae-113">Por esse motivo, o tempo de fluxo também é chamado de *tempo de apresentação*.</span><span class="sxs-lookup"><span data-stu-id="0d2ae-113">For this reason, stream time is also called *presentation time*.</span></span>

<span data-ttu-id="0d2ae-114">Quando um aplicativo chama [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) para executar o gráfico de filtro, o Gerenciador de gráfico de filtro chama [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) em cada filtro.</span><span class="sxs-lookup"><span data-stu-id="0d2ae-114">When an application calls [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the filter graph, the Filter Graph Manager calls [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) on each filter.</span></span> <span data-ttu-id="0d2ae-115">Para compensar a ligeira quantidade de tempo que leva para que os filtros comecem a ser executados, o Gerenciador de grafo de filtro especifica uma hora de início um pouco no futuro.</span><span class="sxs-lookup"><span data-stu-id="0d2ae-115">To compensate for the slight amount of time it takes for the filters to start running, the Filter Graph Manager specifies a start time slightly in the future.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d2ae-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d2ae-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d2ae-117">Tempo e relógios no DirectShow</span><span class="sxs-lookup"><span data-stu-id="0d2ae-117">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="0d2ae-118">Carimbos de Data/Hora</span><span class="sxs-lookup"><span data-stu-id="0d2ae-118">Time Stamps</span></span>](time-stamps.md)
</dt> </dl>

 

 



