---
description: Novos segmentos
ms.assetid: 6c470b38-481f-4e52-93b8-eb6b343dcefc
title: Novos segmentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5438cb3b457ed8ea0f77bd2ac1dcc5d6d2c72698
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105796262"
---
# <a name="new-segments"></a><span data-ttu-id="e11d0-103">Novos segmentos</span><span class="sxs-lookup"><span data-stu-id="e11d0-103">New Segments</span></span>

<span data-ttu-id="e11d0-104">Um *segmento* é um grupo de amostras de mídia que compartilham uma hora de início, hora de parada e taxa de reprodução comuns.</span><span class="sxs-lookup"><span data-stu-id="e11d0-104">A *segment* is a group of media samples that share a common start time, stop time, and playback rate.</span></span> <span data-ttu-id="e11d0-105">O método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) sinaliza o início de um novo segmento.</span><span class="sxs-lookup"><span data-stu-id="e11d0-105">The [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method signals the start of a new segment.</span></span> <span data-ttu-id="e11d0-106">Ele fornece uma maneira para um filtro de origem informar filtros downstream de que as informações de hora e taxa foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="e11d0-106">It provides a way for a source filter to inform downstream filters that the time and rate information has changed.</span></span> <span data-ttu-id="e11d0-107">Por exemplo, se o filtro de origem busca um novo ponto no fluxo, ele chama **NewSegment** com a nova hora de início.</span><span class="sxs-lookup"><span data-stu-id="e11d0-107">For example, if the source filter seeks to a new point in the stream, it calls **NewSegment** with the new start time.</span></span>

<span data-ttu-id="e11d0-108">Alguns filtros downstream usam as informações de segmento ao processar exemplos.</span><span class="sxs-lookup"><span data-stu-id="e11d0-108">Some downstream filters use the segment information when they process samples.</span></span> <span data-ttu-id="e11d0-109">Por exemplo, em um formato que usa a compactação entre quadros, se o tempo de parada cair em um quadro Delta, o filtro de origem poderá precisar enviar amostras adicionais após a hora de parada.</span><span class="sxs-lookup"><span data-stu-id="e11d0-109">For example, in a format that uses interframe compression, if the stop time falls on a delta frame, the source filter may need to send additional samples after the stop time.</span></span> <span data-ttu-id="e11d0-110">Isso permite que o decodificador decodifique o quadro Delta final.</span><span class="sxs-lookup"><span data-stu-id="e11d0-110">This enables the decoder to decode the final delta frame.</span></span> <span data-ttu-id="e11d0-111">Para determinar o quadro final correto, o decodificador refere-se à hora de parada do segmento.</span><span class="sxs-lookup"><span data-stu-id="e11d0-111">To determine the correct final frame, the decoder refers to the segment stop time.</span></span> <span data-ttu-id="e11d0-112">Como outro exemplo, os renderizadores de áudio usam a taxa de segmento junto com a taxa de amostragem de áudio para gerar a saída de áudio correta.</span><span class="sxs-lookup"><span data-stu-id="e11d0-112">As another example, audio renderers use the segment rate along with the audio sampling rate to generate the correct audio output.</span></span>

<span data-ttu-id="e11d0-113">No modelo de push, o filtro de origem inicia a chamada **NewSegment** .</span><span class="sxs-lookup"><span data-stu-id="e11d0-113">In the push model, the source filter initiates the **NewSegment** call.</span></span> <span data-ttu-id="e11d0-114">No modelo de pull, isso é feito pelo filtro do analisador.</span><span class="sxs-lookup"><span data-stu-id="e11d0-114">In the pull model, this is done by the parser filter.</span></span> <span data-ttu-id="e11d0-115">Em ambos os casos, o filtro chama **NewSegment** no pino de entrada downstream, que propaga a chamada para o próximo filtro, até que a chamada atinja o renderizador.</span><span class="sxs-lookup"><span data-stu-id="e11d0-115">In either case, the filter calls **NewSegment** on the downstream input pin, which propagates the call to the next filter, until the call reaches the renderer.</span></span> <span data-ttu-id="e11d0-116">Os filtros devem serializar chamadas **NewSegment** com outras chamadas de streaming, como [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).</span><span class="sxs-lookup"><span data-stu-id="e11d0-116">Filters must serialize **NewSegment** calls with other streaming calls, such as [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).</span></span>

<span data-ttu-id="e11d0-117">O tempo de fluxo é redefinido para zero após cada novo segmento.</span><span class="sxs-lookup"><span data-stu-id="e11d0-117">Stream time resets to zero after each new segment.</span></span> <span data-ttu-id="e11d0-118">Carimbos de data/hora em amostras entregues após o segmento iniciar de zero.</span><span class="sxs-lookup"><span data-stu-id="e11d0-118">Time stamps on samples delivered after the segment start from zero.</span></span>

 

 



