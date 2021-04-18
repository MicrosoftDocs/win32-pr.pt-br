---
description: Usando o divisor MPEG-2
ms.assetid: a08e079c-41be-475a-9e88-ee46d17fe938
title: Usando o divisor MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60505ef242c2ed9c1eab3031a005a2582b99608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753495"
---
# <a name="using-the-mpeg-2-splitter"></a><span data-ttu-id="7a8df-103">Usando o divisor MPEG-2</span><span class="sxs-lookup"><span data-stu-id="7a8df-103">Using the MPEG-2 Splitter</span></span>

> [!Note]  
> <span data-ttu-id="7a8df-104">A partir do Microsoft® Windows® XP, o filtro de divisão MPEG-2 é preterido.</span><span class="sxs-lookup"><span data-stu-id="7a8df-104">Starting in Microsoft® Windows® XP, the MPEG-2 Splitter filter is deprecated.</span></span> <span data-ttu-id="7a8df-105">Em vez disso, use o [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) .</span><span class="sxs-lookup"><span data-stu-id="7a8df-105">Use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead.</span></span>

 

<span data-ttu-id="7a8df-106">O filtro divisor MPEG-2 dá suporte à reprodução de modo de recepção de fluxos de programas MPEG-2 que contêm pelo menos um dos seguintes tipos de fluxo.</span><span class="sxs-lookup"><span data-stu-id="7a8df-106">The MPEG-2 Splitter filter supports pull-mode playback of MPEG-2 program streams that contain at least one of the following stream types.</span></span>

-   <span data-ttu-id="7a8df-107">Vídeo MPEG-2</span><span class="sxs-lookup"><span data-stu-id="7a8df-107">MPEG-2 video</span></span>
-   <span data-ttu-id="7a8df-108">Áudio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="7a8df-108">MPEG-2 audio</span></span>
-   <span data-ttu-id="7a8df-109">Áudio Dolby AC-3 codificado conforme definido para DVD-Video</span><span class="sxs-lookup"><span data-stu-id="7a8df-109">Dolby AC-3 audio encoded as defined for DVD-Video</span></span>
-   <span data-ttu-id="7a8df-110">Áudio LPCM (código de pulso linear modulado) codificado conforme definido para DVD-Video</span><span class="sxs-lookup"><span data-stu-id="7a8df-110">LPCM (Linear Pulse Code Modulated) audio encoded as defined for DVD-Video</span></span>

<span data-ttu-id="7a8df-111">Para obter uma lista de tipos de mídia com suporte do divisor MPEG-2, consulte [tipos de mídia divisor MPEG-2](mpeg-2-splitter-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="7a8df-111">For a list of media types that the MPEG-2 Splitter supports, see [MPEG-2 Splitter Media Types](mpeg-2-splitter-media-types.md).</span></span>

<span data-ttu-id="7a8df-112">O divisor MPEG-2 não analisa fluxos de transporte.</span><span class="sxs-lookup"><span data-stu-id="7a8df-112">The MPEG-2 Splitter does not parse transport streams.</span></span> <span data-ttu-id="7a8df-113">Use o filtro de Desmultiplexador MPEG-2 para fluxos de transporte (somente no modo push).</span><span class="sxs-lookup"><span data-stu-id="7a8df-113">Use the MPEG-2 Demultiplexer filter for transport streams (push mode only).</span></span>

<span data-ttu-id="7a8df-114">**Carimbos de Data/Hora**</span><span class="sxs-lookup"><span data-stu-id="7a8df-114">**Time Stamps**</span></span>

<span data-ttu-id="7a8df-115">Ao reproduzir fluxos de programa MPEG-2, o filtro divisor MPEG-2 trata a primeira referência do relógio do sistema que ele encontra como a origem de tempo de qualquer fluxo.</span><span class="sxs-lookup"><span data-stu-id="7a8df-115">When playing back MPEG-2 program streams, the MPEG-2 Splitter filter treats the first system clock reference it encounters as the time origin of any stream.</span></span> <span data-ttu-id="7a8df-116">Isso difere do [divisor de fluxo MPEG-1](mpeg-1-stream-splitter-filter.md), que usa carimbos de data/hora de apresentação.</span><span class="sxs-lookup"><span data-stu-id="7a8df-116">This differs from the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), which uses presentation time stamps.</span></span> <span data-ttu-id="7a8df-117">O método [**IAMParse:: Getparsetime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) retorna o tempo de relógio do sistema de fluxo (possivelmente estimado) para os dados que ele processou.</span><span class="sxs-lookup"><span data-stu-id="7a8df-117">The [**IAMParse::GetParseTime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) method returns the (possibly estimated) stream system clock time for the data it has processed.</span></span>

<span data-ttu-id="7a8df-118">Se o filtro de divisão MPEG-2 encontrar um exemplo de entrada com o conjunto de propriedades de descontinuidade (a propriedade de descontinuidade pode ser definida usando [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) ou [**IMediaSample2:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)), ele ignora os dados até encontrar o primeiro pacote nos dados e ajusta seus carimbos de data/hora para que a SCR (referência do relógio do sistema) desse pacote seja considerada idêntica ao tempo da SCR antes da descontinuidade.</span><span class="sxs-lookup"><span data-stu-id="7a8df-118">If the MPEG-2 splitter filter encounters an input sample with the discontinuity property set (the discontinuity property can be set by using [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) or [**IMediaSample2::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)), it skips data until it finds the first pack in the data and adjusts its time stamps so that the system clock reference (SCR) for that pack is considered identical to the SCR time before the discontinuity.</span></span> <span data-ttu-id="7a8df-119">Se o relógio da SCR aparecer para voltar ou avançar por mais de um segundo, então (em linha com a especificação de fluxo de programa MPEG-2), isso também será tratado como uma descontinuidade do relógio e a discrepância do relógio aparente será subtraída dos carimbos de data/hora passados para os filtros de downstream.</span><span class="sxs-lookup"><span data-stu-id="7a8df-119">If the SCR clock appears either to jump backward or to jump forward by more than a second, then (in line with the MPEG-2 program stream specification), this is also treated as a clock discontinuity and the apparent clock discrepancy is subtracted from the time stamps passed to downstream filters.</span></span>

<span data-ttu-id="7a8df-120">**Seleção de fluxo**</span><span class="sxs-lookup"><span data-stu-id="7a8df-120">**Stream Selection**</span></span>

<span data-ttu-id="7a8df-121">Ao reproduzir o fluxo de programa MPEG-2, o primeiro fluxo de vídeo e o primeiro fluxo de áudio encontrados atravessando o fluxo do programa são escolhidos.</span><span class="sxs-lookup"><span data-stu-id="7a8df-121">When playing back the MPEG-2 program stream, the first video stream and first audio stream found traversing the program stream are chosen.</span></span> <span data-ttu-id="7a8df-122">Há suporte para até um pino de saída de áudio e um vídeo.</span><span class="sxs-lookup"><span data-stu-id="7a8df-122">Up to one audio and one video output pin are supported.</span></span> <span data-ttu-id="7a8df-123">Por meio da interface [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) , fluxos diferentes do mesmo tipo podem ser selecionados até o número especificado pelo limite de áudio no cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="7a8df-123">Through the [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) interface, different streams of the same type can be selected up to the number specified by the audio limit in the system header.</span></span> <span data-ttu-id="7a8df-124">Para áudio MPEG-2, atualmente supõe-se que os fluxos formam um intervalo contíguo a partir do fluxo 0xC0.</span><span class="sxs-lookup"><span data-stu-id="7a8df-124">For MPEG-2 audio, it is currently assumed the streams form a contiguous range starting at stream 0xC0.</span></span>

<span data-ttu-id="7a8df-125">**Interfaces com suporte**</span><span class="sxs-lookup"><span data-stu-id="7a8df-125">**Supported Interfaces**</span></span>

<span data-ttu-id="7a8df-126">O filtro divisor MPEG-2 dá suporte às seguintes interfaces.</span><span class="sxs-lookup"><span data-stu-id="7a8df-126">The MPEG-2 splitter filter supports the following interfaces.</span></span>

-   <span data-ttu-id="7a8df-127">[**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse).</span><span class="sxs-lookup"><span data-stu-id="7a8df-127">[**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse).</span></span> <span data-ttu-id="7a8df-128">Somente fluxo de programa MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="7a8df-128">MPEG-2 program stream only.</span></span>
-   <span data-ttu-id="7a8df-129">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect).</span><span class="sxs-lookup"><span data-stu-id="7a8df-129">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect).</span></span> <span data-ttu-id="7a8df-130">Somente fluxo de programa MPEG-2, somente fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="7a8df-130">MPEG-2 program stream only, audio streams only.</span></span>
-   <span data-ttu-id="7a8df-131">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking).</span><span class="sxs-lookup"><span data-stu-id="7a8df-131">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking).</span></span> <span data-ttu-id="7a8df-132">Inclui o modo de byte que busca.</span><span class="sxs-lookup"><span data-stu-id="7a8df-132">Includes byte mode seeking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a8df-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7a8df-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a8df-134">Suporte a MPEG-2 no DirectShow</span><span class="sxs-lookup"><span data-stu-id="7a8df-134">MPEG-2 Support in DirectShow</span></span>](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



