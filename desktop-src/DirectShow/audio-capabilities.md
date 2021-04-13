---
description: Recursos de áudio
ms.assetid: de96f6ee-b526-4ac2-93ac-a731f86ef5d5
title: Recursos de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2cf02927b69d807f400c4185a7d4ddbdd14322
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500669"
---
# <a name="audio-capabilities"></a><span data-ttu-id="5f235-103">Recursos de áudio</span><span class="sxs-lookup"><span data-stu-id="5f235-103">Audio Capabilities</span></span>

<span data-ttu-id="5f235-104">Para recursos de áudio, [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) retorna uma matriz de pares das estruturas de [**Caps de \_ \_ configuração de \_ fluxo de áudio**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) e de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="5f235-104">For audio capabilities, [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) returns an array of pairs of [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) and [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structures.</span></span> <span data-ttu-id="5f235-105">Assim como acontece com o vídeo, você pode usar isso para expor todos os tipos de recursos de áudio no PIN, como a taxa de dados e se ele dá suporte a mono ou estéreo.</span><span class="sxs-lookup"><span data-stu-id="5f235-105">As with video, you can use this to expose all kinds of audio capabilities on the pin, such as data rate and whether it supports mono or stereo.</span></span>

<span data-ttu-id="5f235-106">Para obter exemplos de vídeo relacionados ao GetStreamCaps, consulte [recursos de vídeo](video-capabilities.md).</span><span class="sxs-lookup"><span data-stu-id="5f235-106">For video-related examples relating to GetStreamCaps, see [Video Capabilities](video-capabilities.md).</span></span>

<span data-ttu-id="5f235-107">Suponha que você ofereça suporte ao formato Wave de codificação de código de pulso (PCM) (conforme representado pela estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) ) em taxas de amostragem de 11.025, 22.050 e 44.100 amostras por segundo, tudo em mono ou estéreo de 8 ou 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5f235-107">Suppose you support pulse code modulation (PCM) wave format (as represented by the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure) at sampling rates of 11,025, 22,050, and 44,100 samples per second, all at 8- or 16-bit mono or stereo.</span></span> <span data-ttu-id="5f235-108">Nesse caso, você ofereceria dois pares de estruturas.</span><span class="sxs-lookup"><span data-stu-id="5f235-108">In this case, you would offer two pairs of structures.</span></span> <span data-ttu-id="5f235-109">O primeiro par teria uma estrutura de capacidade de configuração de fluxo de áudio, dizendo que você dá suporte a um mínimo de 11.025 a um máximo de 22.050 amostras por segundo com uma granularidade de 11.025 amostras por segundo (a granularidade é a diferença entre os valores com suporte); um mínimo de 8 bits para um máximo de bits de 16 bits por amostra com uma granularidade de 8 bits por amostra; e o máximo de um canal e mínimo de dois canais. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f235-109">The first pair would have an **AUDIO\_STREAM\_CONFIG\_CAPS** capability structure saying you support a minimum of 11,025 to a maximum of 22,050 samples per second with a granularity of 11,025 samples per second (granularity is the difference between supported values); an 8-bit minimum to a 16-bit maximum bits per sample with a granularity of 8 bits per sample; and one-channel minimum and two-channel maximum.</span></span> <span data-ttu-id="5f235-110">O tipo de mídia do primeiro par seria o formato PCM padrão nesse intervalo, talvez 22 kilohertz (kHz), estéreo de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5f235-110">The first pair's media type would be your default PCM format in that range, perhaps 22 kilohertz (kHz), 16-bit stereo.</span></span> <span data-ttu-id="5f235-111">Seu segundo par seria um recurso que mostra 44.100 para os exemplos mínimo e máximo por segundo; bits de 8 bits (mínimo) e 16 bits (máximo) por amostra, com uma granularidade de 8 bits por amostra; e o mínimo de um canal e o máximo de dois canais.</span><span class="sxs-lookup"><span data-stu-id="5f235-111">Your second pair would be a capability showing 44,100 for both minimum and maximum samples per second; 8-bit (minimum) and 16-bit (maximum) bits per sample, with a granularity of 8 bits per sample; and one-channel minimum and two-channel maximum.</span></span> <span data-ttu-id="5f235-112">O tipo de mídia seria o formato padrão de 44 kHz, talvez 44 kHz de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5f235-112">The media type would be your default 44 kHz format, perhaps 44 kHz 16-bit stereo.</span></span>

<span data-ttu-id="5f235-113">Se você der suporte a formatos Wave não PCM, o tipo de mídia retornado por esse método poderá mostrar a quais formatos não PCM são suportados (com uma taxa de amostragem padrão, taxa de bits e canais) e a estrutura de recursos que acompanha esse tipo de mídia pode descrever quais outras taxas de amostra, taxas de bits e canais são suportados.</span><span class="sxs-lookup"><span data-stu-id="5f235-113">If you support non-PCM wave formats, the media type returned by this method can show which non-PCM formats you support (with a default sample rate, bit rate, and channels) and the capabilities structure accompanying that media type can describe which other sample rates, bit rates, and channels you support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f235-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f235-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f235-115">Expondo os formatos de captura e compactação</span><span class="sxs-lookup"><span data-stu-id="5f235-115">Exposing Capture and Compression Formats</span></span>](exposing-capture-and-compression-formats.md)
</dt> </dl>

 

 
