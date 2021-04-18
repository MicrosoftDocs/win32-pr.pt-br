---
description: Filtro de invólucro do ACM
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: Filtro de invólucro do ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da0c1283ac6d4980f51d40001b38c719f5e31c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105792570"
---
# <a name="acm-wrapper-filter"></a><span data-ttu-id="0bf76-103">Filtro de invólucro do ACM</span><span class="sxs-lookup"><span data-stu-id="0bf76-103">ACM Wrapper Filter</span></span>

<span data-ttu-id="0bf76-104">O filtro de invólucro do ACM permite que os codecs do ACM (Gerenciador de compactação de áudio) ingressem em um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="0bf76-104">The ACM Wrapper filter enables Audio Compression Manager (ACM) codecs to join a filter graph.</span></span> <span data-ttu-id="0bf76-105">Ele pode atuar como um filtro de descompactação ou como um filtro de compactação.</span><span class="sxs-lookup"><span data-stu-id="0bf76-105">It can act either as a decompression filter or as a compression filter.</span></span>

<span data-ttu-id="0bf76-106">Como um filtro de descompactação, o invólucro do ACM aparece na categoria "filtros do DirectShow" (CLSID \_ LegacyAmFilterCategory) e tem um mérito de mérito \_ normal.</span><span class="sxs-lookup"><span data-stu-id="0bf76-106">As a decompression filter, the ACM Wrapper appears in the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory) and has a merit of MERIT\_NORMAL.</span></span> <span data-ttu-id="0bf76-107">O tipo de mídia de conexão no PIN de entrada determina qual codec o filtro usa.</span><span class="sxs-lookup"><span data-stu-id="0bf76-107">The connection media type on the input pin determines which codec the filter uses.</span></span> <span data-ttu-id="0bf76-108">Normalmente, o aplicativo não precisa adicionar o filtro ao grafo de filtro; Ele é retirado automaticamente pelo Gerenciador de gráficos de filtro quando necessário.</span><span class="sxs-lookup"><span data-stu-id="0bf76-108">Typically, the application does not need to add the filter to the filter graph; it is pulled in automatically by the Filter Graph Manager when needed.</span></span> <span data-ttu-id="0bf76-109">A descompactação é apenas para áudio PCM.</span><span class="sxs-lookup"><span data-stu-id="0bf76-109">Decompression is only to PCM audio.</span></span>

<span data-ttu-id="0bf76-110">Como um filtro de compactação, o invólucro do ACM aparece na categoria "compactadores de áudio" (CLSID \_ AudioCompressorCategory) e tem um mérito de mérito \_ \_ não \_ usar.</span><span class="sxs-lookup"><span data-stu-id="0bf76-110">As a compression filter, the ACM Wrapper appears in the "Audio Compressors" category (CLSID\_AudioCompressorCategory) and has a merit of MERIT\_DO\_NOT\_USE.</span></span> <span data-ttu-id="0bf76-111">Cada codec aparece como uma instância separada.</span><span class="sxs-lookup"><span data-stu-id="0bf76-111">Each codec appears as a separate instance.</span></span> <span data-ttu-id="0bf76-112">Para compactação, você não pode criar o filtro diretamente com CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="0bf76-112">For compression, you cannot directly create the filter with CoCreateInstance.</span></span> <span data-ttu-id="0bf76-113">Em vez disso, você deve usar o enumerador de dispositivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="0bf76-113">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="0bf76-114">Para obter mais informações, consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="0bf76-114">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0bf76-115">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="0bf76-115">Filter interfaces</span></span></td>
<td><span data-ttu-id="0bf76-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, IPersist, IPersistPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0bf76-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, IPersist, IPersistPropertyBag</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0bf76-117">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="0bf76-117">Input pin media types</span></span></td>
<td><span data-ttu-id="0bf76-118">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="0bf76-118">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0bf76-119">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="0bf76-119">Input pin interfaces</span></span></td>
<td><span data-ttu-id="0bf76-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf76-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0bf76-121">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="0bf76-121">Output pin media types</span></span></td>
<td><span data-ttu-id="0bf76-122">MEDIATYPE_Audio, MEDIASUBTYPE_PCM FORMAT_WaveFormatEx. qualquer combinação dos seguintes é possível:</span><span class="sxs-lookup"><span data-stu-id="0bf76-122">MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx.Any combination of the following are possible:</span></span><br/>
<ul>
<li><span data-ttu-id="0bf76-123">Exemplos por segundo (kHz): 44,1, 22, 5, 11, 25 ou 8,0.</span><span class="sxs-lookup"><span data-stu-id="0bf76-123">Samples per second (kHz): 44.1, 22.05, 11.025, or 8.0.</span></span></li>
<li><span data-ttu-id="0bf76-124">Canais: estéreo ou mono.</span><span class="sxs-lookup"><span data-stu-id="0bf76-124">Channels: Stereo or mono.</span></span></li>
<li><span data-ttu-id="0bf76-125">Bits por amostra: 8 ou 16.</span><span class="sxs-lookup"><span data-stu-id="0bf76-125">Bits per sample: 8 or 16.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0bf76-126">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="0bf76-126">Output pin interfaces</span></span></td>
<td><span data-ttu-id="0bf76-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf76-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0bf76-128">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="0bf76-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="0bf76-129">CLSID_ACMWrapper</span><span class="sxs-lookup"><span data-stu-id="0bf76-129">CLSID_ACMWrapper</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0bf76-130">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="0bf76-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="0bf76-131">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="0bf76-131">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0bf76-132">Executável</span><span class="sxs-lookup"><span data-stu-id="0bf76-132">Executable</span></span></td>
<td><span data-ttu-id="0bf76-133">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="0bf76-133">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0bf76-134"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="0bf76-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="0bf76-135">MERIT_NORMAL ou MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="0bf76-135">MERIT_NORMAL or MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0bf76-136"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="0bf76-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="0bf76-137">CLSID_LegacyAmFilterCategory ou CLSID_AudioCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="0bf76-137">CLSID_LegacyAmFilterCategory or CLSID_AudioCompressorCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="0bf76-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0bf76-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bf76-139">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="0bf76-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




