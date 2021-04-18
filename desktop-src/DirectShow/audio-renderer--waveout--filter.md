---
description: Filtro de processador de áudio (WaveOut)
ms.assetid: a3f2776b-974b-4886-82a3-38e00b607a07
title: Filtro de processador de áudio (WaveOut)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f47018d22bcbbdcf884f5eb4356d1d0b3fe60d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105760100"
---
# <a name="audio-renderer-waveout-filter"></a><span data-ttu-id="6fe1e-103">Filtro de processador de áudio (WaveOut)</span><span class="sxs-lookup"><span data-stu-id="6fe1e-103">Audio Renderer (WaveOut) Filter</span></span>

<span data-ttu-id="6fe1e-104">Esse filtro usa a API de WaveOut \* para renderizar áudio de onda.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-104">This filter uses the waveOut\* API to render waveform audio.</span></span> <span data-ttu-id="6fe1e-105">No entanto, o [filtro de processamento do DirectSound](directsound-renderer-filter.md) fornece a mesma funcionalidade usando o DirectSound.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-105">However, the [DirectSound Renderer Filter](directsound-renderer-filter.md) provides the same functionality using DirectSound.</span></span> <span data-ttu-id="6fe1e-106">Por padrão, o Gerenciador de gráfico de filtro usa o renderizador DirectSound em vez desse filtro.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-106">By default, the Filter Graph Manager uses the DirectSound Renderer instead of this filter.</span></span> <span data-ttu-id="6fe1e-107">A mixagem de áudio está desabilitada no processador de áudio de onda e, portanto, se você precisar misturar vários fluxos de áudio durante a reprodução, use o renderizador DirectSound.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-107">Audio mixing is disabled in the waveOut Audio Renderer, so if you need to mix multiple audio streams during playback, use the DirectSound renderer.</span></span>

<span data-ttu-id="6fe1e-108">Esse filtro não verifica o subtipo do fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-108">This filter does not check the audio stream's subtype.</span></span> <span data-ttu-id="6fe1e-109">A estrutura [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) ou [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) passada no formato contém as informações necessárias para a conexão.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-109">The [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) or [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure passed in the format contains the information needed for the connection.</span></span>

<span data-ttu-id="6fe1e-110">Esse filtro oferece suporte a um intervalo de taxas de exemplo que depende do driver de áudio.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-110">This filter supports a range of sample rates that depends on the audio driver.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6fe1e-111">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="6fe1e-111">Filter Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="6fe1e-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fe1e-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></span></span></li>
<li><span data-ttu-id="6fe1e-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fe1e-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></span></span></li>
<li><span data-ttu-id="6fe1e-114"><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fe1e-114"><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></span></span></li>
<li><span data-ttu-id="6fe1e-115"><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fe1e-115"><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></span></span></li>
<li><span data-ttu-id="6fe1e-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fe1e-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="6fe1e-117"><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fe1e-117"><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></span></span></li>
<li><span data-ttu-id="6fe1e-118"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fe1e-118"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span></span></li>
<li><span data-ttu-id="6fe1e-119"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fe1e-119"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="6fe1e-120">IPersistPropertyBag</span><span class="sxs-lookup"><span data-stu-id="6fe1e-120">IPersistPropertyBag</span></span></li>
<li><span data-ttu-id="6fe1e-121">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="6fe1e-121">IPersistStream</span></span></li>
<li><span data-ttu-id="6fe1e-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fe1e-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="6fe1e-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fe1e-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fe1e-124">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="6fe1e-124">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="6fe1e-125"><strong>MEDIATYPE_Audio</strong></span><span class="sxs-lookup"><span data-stu-id="6fe1e-125"><strong>MEDIATYPE_Audio</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fe1e-126">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="6fe1e-126">Input Pin Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="6fe1e-127"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fe1e-127"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="6fe1e-128"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fe1e-128"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="6fe1e-129"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fe1e-129"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fe1e-130">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="6fe1e-130">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="6fe1e-131">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-131">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fe1e-132">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="6fe1e-132">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="6fe1e-133">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-133">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fe1e-134">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="6fe1e-134">Filter CLSID</span></span></td>
<td><span data-ttu-id="6fe1e-135"><strong>CLSID_AudioRender</strong></span><span class="sxs-lookup"><span data-stu-id="6fe1e-135"><strong>CLSID_AudioRender</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fe1e-136">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="6fe1e-136">Property Page CLSID</span></span></td>
<td><span data-ttu-id="6fe1e-137"><strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong></span><span class="sxs-lookup"><span data-stu-id="6fe1e-137"><strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fe1e-138">Executável</span><span class="sxs-lookup"><span data-stu-id="6fe1e-138">Executable</span></span></td>
<td><span data-ttu-id="6fe1e-139">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="6fe1e-139">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fe1e-140"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="6fe1e-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="6fe1e-141"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="6fe1e-141"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fe1e-142"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="6fe1e-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="6fe1e-143"><strong>CLSID_AudioRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="6fe1e-143"><strong>CLSID_AudioRendererCategory</strong></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="6fe1e-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6fe1e-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fe1e-145">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="6fe1e-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
