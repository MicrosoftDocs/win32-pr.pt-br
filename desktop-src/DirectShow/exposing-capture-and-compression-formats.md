---
description: Expondo os formatos de captura e compactação
ms.assetid: f7466cfe-b13e-4ee9-82f9-0528ed97bf99
title: Expondo os formatos de captura e compactação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02051d9e68b3ad919b96dca53b674305787b3186
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646184"
---
# <a name="exposing-capture-and-compression-formats"></a><span data-ttu-id="15028-103">Expondo os formatos de captura e compactação</span><span class="sxs-lookup"><span data-stu-id="15028-103">Exposing Capture and Compression Formats</span></span>

<span data-ttu-id="15028-104">Este artigo descreve como retornar formatos de captura e compactação usando o método [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) .</span><span class="sxs-lookup"><span data-stu-id="15028-104">This article describes how to return capture and compression formats by using the [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="15028-105">Esse método pode obter mais informações sobre os tipos de mídia aceitos do que a maneira tradicional de enumerar os tipos de mídia de um PIN, de modo que ele normalmente deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="15028-105">This method can get more information about accepted media types than the traditional way of enumerating a pin's media types, so it should typically be used instead.</span></span> <span data-ttu-id="15028-106">**GetStreamCaps** pode retornar informações sobre os tipos de formatos permitidos para áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="15028-106">**GetStreamCaps** can return information about the kinds of formats allowed for audio or video.</span></span> <span data-ttu-id="15028-107">Além disso, este artigo fornece um código de exemplo que demonstra como reconectar o PIN de entrada de um filtro de transformação para garantir que o filtro possa produzir uma saída específica.</span><span class="sxs-lookup"><span data-stu-id="15028-107">Additionally, this article provides some sample code that demonstrates how to reconnect the input pin of a transform filter to ensure your filter can produce a particular output.</span></span>

<span data-ttu-id="15028-108">O método **GetStreamCaps** retorna uma matriz de pares de estruturas de tipo e recursos de mídia.</span><span class="sxs-lookup"><span data-stu-id="15028-108">The **GetStreamCaps** method returns an array of pairs of media type and capabilities structures.</span></span> <span data-ttu-id="15028-109">O tipo de mídia é uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) e os recursos são representados por uma estrutura de Caps de configuração de fluxo de áudio ou uma estrutura de [**Caps de configuração de fluxo de vídeo \_ \_ \_**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) . [**\_ \_ \_**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps)</span><span class="sxs-lookup"><span data-stu-id="15028-109">The media type is an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure and the capabilities are represented either by an [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structure or a [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure.</span></span> <span data-ttu-id="15028-110">A primeira seção deste artigo apresenta um exemplo de vídeo e o segundo apresenta um exemplo de áudio.</span><span class="sxs-lookup"><span data-stu-id="15028-110">The first section in this article presents a video example and the second presents an audio example.</span></span>

<span data-ttu-id="15028-111">Este artigo contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="15028-111">This article contains the following topics:</span></span>

-   [<span data-ttu-id="15028-112">Recursos de vídeo</span><span class="sxs-lookup"><span data-stu-id="15028-112">Video Capabilities</span></span>](video-capabilities.md)
-   [<span data-ttu-id="15028-113">Recursos de áudio</span><span class="sxs-lookup"><span data-stu-id="15028-113">Audio Capabilities</span></span>](audio-capabilities.md)
-   [<span data-ttu-id="15028-114">Reconectando sua entrada para garantir tipos de saída específicos</span><span class="sxs-lookup"><span data-stu-id="15028-114">Reconnecting Your Input to Ensure Specific Output Types</span></span>](reconnecting-your-input-to-ensure-specific-output-types.md)

## <a name="related-topics"></a><span data-ttu-id="15028-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15028-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15028-116">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="15028-116">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



