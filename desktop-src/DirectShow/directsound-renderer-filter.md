---
description: Filtro de renderizador DirectSound
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: Filtro de renderizador DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae932340ea22213e0f9d7234599742d74208f632
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087267"
---
# <a name="directsound-renderer-filter"></a><span data-ttu-id="7d639-103">Filtro de renderizador DirectSound</span><span class="sxs-lookup"><span data-stu-id="7d639-103">DirectSound Renderer Filter</span></span>

<span data-ttu-id="7d639-104">Esse filtro processa áudio usando DirectSound.</span><span class="sxs-lookup"><span data-stu-id="7d639-104">This filter renders audio using DirectSound.</span></span> <span data-ttu-id="7d639-105">Esse filtro é atualmente o processador de áudio padrão para som de onda.</span><span class="sxs-lookup"><span data-stu-id="7d639-105">This filter is currently the default audio renderer for waveform sound.</span></span>

<span data-ttu-id="7d639-106">Além de seus recursos básicos de renderização de som, esse filtro pode processar chamadas da API DirectSound.</span><span class="sxs-lookup"><span data-stu-id="7d639-106">In addition to its basic sound-rendering capabilities, this filter can process DirectSound API calls.</span></span> <span data-ttu-id="7d639-107">Use os métodos [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) para definir e recuperar a janela que manipulará a reprodução do som.</span><span class="sxs-lookup"><span data-stu-id="7d639-107">Use the [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) methods to set and retrieve the window that will handle the sound playback.</span></span> <span data-ttu-id="7d639-108">O renderizador de áudio do DirectSound é o filtro de renderização de áudio padrão para o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7d639-108">The DirectSound Audio Renderer is the default audio rendering filter for DirectShow.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d639-109">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="7d639-109">Filter Interfaces</span></span></td>
<td><span data-ttu-id="7d639-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d639-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d639-111">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="7d639-111">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="7d639-112">Tipo principal: MEDIATYPE_AudioSubtypes:</span><span class="sxs-lookup"><span data-stu-id="7d639-112">Major Type: MEDIATYPE_AudioSubtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="7d639-113">MEDIASUBTYPE_PCM</span><span class="sxs-lookup"><span data-stu-id="7d639-113">MEDIASUBTYPE_PCM</span></span></li>
<li><span data-ttu-id="7d639-114">MEDIASUBTYPE_IEEE_FLOAT</span><span class="sxs-lookup"><span data-stu-id="7d639-114">MEDIASUBTYPE_IEEE_FLOAT</span></span></li>
<li><span data-ttu-id="7d639-115">MEDIASUBTYPE_DOLBY_AC3_SPDIF</span><span class="sxs-lookup"><span data-stu-id="7d639-115">MEDIASUBTYPE_DOLBY_AC3_SPDIF</span></span></li>
<li><span data-ttu-id="7d639-116">MEDIASUBTYPE_RAW_SPORT</span><span class="sxs-lookup"><span data-stu-id="7d639-116">MEDIASUBTYPE_RAW_SPORT</span></span></li>
<li><span data-ttu-id="7d639-117">MEDIASUBTYPE_SPDIF_TAG_241h</span><span class="sxs-lookup"><span data-stu-id="7d639-117">MEDIASUBTYPE_SPDIF_TAG_241h</span></span></li>
<li><span data-ttu-id="7d639-118">MEDIASUBTYPE_DRM_Audio</span><span class="sxs-lookup"><span data-stu-id="7d639-118">MEDIASUBTYPE_DRM_Audio</span></span></li>
</ul>
<span data-ttu-id="7d639-119">Tipo de formato: FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="7d639-119">Format type: FORMAT_WaveFormatEx</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d639-120">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="7d639-120">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="7d639-121"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d639-121"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d639-122">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="7d639-122">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="7d639-123">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="7d639-123">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d639-124">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="7d639-124">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="7d639-125">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="7d639-125">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d639-126">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="7d639-126">Filter CLSID</span></span></td>
<td><span data-ttu-id="7d639-127">CLSID_DSoundRender</span><span class="sxs-lookup"><span data-stu-id="7d639-127">CLSID_DSoundRender</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d639-128">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="7d639-128">Property Page CLSID</span></span></td>
<td><span data-ttu-id="7d639-129">CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties</span><span class="sxs-lookup"><span data-stu-id="7d639-129">CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d639-130">Executável</span><span class="sxs-lookup"><span data-stu-id="7d639-130">Executable</span></span></td>
<td><span data-ttu-id="7d639-131">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="7d639-131">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d639-132"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="7d639-132"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="7d639-133">MERIT_PREFERRED</span><span class="sxs-lookup"><span data-stu-id="7d639-133">MERIT_PREFERRED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d639-134"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="7d639-134"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="7d639-135">CLSID_AudioRendererCategory</span><span class="sxs-lookup"><span data-stu-id="7d639-135">CLSID_AudioRendererCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="7d639-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d639-136">Remarks</span></span>

<span data-ttu-id="7d639-137">Esse filtro atua como um wrapper para um dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="7d639-137">This filter acts as a wrapper for an audio device.</span></span> <span data-ttu-id="7d639-138">Para enumerar os dispositivos de áudio disponíveis no sistema do usuário, use a interface [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) com a categoria de processador de áudio (CLSID \_ AudioRendererCategory).</span><span class="sxs-lookup"><span data-stu-id="7d639-138">To enumerate the audio devices available on the user's system, use the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface with the audio renderer category (CLSID\_AudioRendererCategory).</span></span> <span data-ttu-id="7d639-139">Para cada dispositivo de áudio, a categoria de processador de áudio contém duas instâncias de filtro.</span><span class="sxs-lookup"><span data-stu-id="7d639-139">For each audio device, the audio renderer category contains two filter instances.</span></span> <span data-ttu-id="7d639-140">Um deles corresponde ao renderizador do DirectSound e o outro corresponde ao filtro do [processador de áudio (WaveOut)](audio-renderer--waveout--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="7d639-140">One of these corresponds to the DirectSound Renderer, and the other corresponds to the [Audio Renderer (WaveOut)](audio-renderer--waveout--filter.md) filter.</span></span> <span data-ttu-id="7d639-141">A instância do DirectSound tem o nome amigável "DirectSound: *DeviceName*", em que *DeviceName* é o nome do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7d639-141">The DirectSound instance has the friendly name "DirectSound: *DeviceName*," where *DeviceName* is the name of the device.</span></span> <span data-ttu-id="7d639-142">A instância de WaveOut tem o nome amigável *DeviceName*.</span><span class="sxs-lookup"><span data-stu-id="7d639-142">The WaveOut instance has the friendly name *DeviceName*.</span></span>

<span data-ttu-id="7d639-143">A categoria de processador de áudio contém duas instâncias de filtro adicionais, chamadas "dispositivo DirectSound padrão" e "dispositivo wave out padrão".</span><span class="sxs-lookup"><span data-stu-id="7d639-143">The audio renderer category contains two additional filter instances, named "Default DirectSound Device" and "Default WaveOut Device."</span></span> <span data-ttu-id="7d639-144">Eles correspondem ao dispositivo de som padrão, conforme escolhido pelo usuário por meio do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="7d639-144">These correspond to the default sound device, as chosen by the user through the Control Panel.</span></span> <span data-ttu-id="7d639-145">Eles são, na verdade, mapeamentos para um dos pares descritos no parágrafo anterior.</span><span class="sxs-lookup"><span data-stu-id="7d639-145">They are actually mappings to one of the pairs described in the previous paragraph.</span></span> <span data-ttu-id="7d639-146">Por exemplo, se o sistema tiver dois dispositivos de áudio, o dispositivo A e o dispositivo B, a categoria de processador de áudio conterá o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7d639-146">For example, if the system has two audio devices, Device A and Device B, the audio renderer category will contain the following:</span></span>

-   <span data-ttu-id="7d639-147">Dispositivo A</span><span class="sxs-lookup"><span data-stu-id="7d639-147">Device A</span></span>
-   <span data-ttu-id="7d639-148">DirectSound: dispositivo A</span><span class="sxs-lookup"><span data-stu-id="7d639-148">DirectSound: Device A</span></span>
-   <span data-ttu-id="7d639-149">Dispositivo B</span><span class="sxs-lookup"><span data-stu-id="7d639-149">Device B</span></span>
-   <span data-ttu-id="7d639-150">DirectSound: dispositivo B</span><span class="sxs-lookup"><span data-stu-id="7d639-150">DirectSound: Device B</span></span>
-   <span data-ttu-id="7d639-151">Dispositivo DirectSound padrão</span><span class="sxs-lookup"><span data-stu-id="7d639-151">Default DirectSound Device</span></span>
-   <span data-ttu-id="7d639-152">Dispositivo wave out padrão</span><span class="sxs-lookup"><span data-stu-id="7d639-152">Default WaveOut Device</span></span>

<span data-ttu-id="7d639-153">Se o usuário selecionou o dispositivo A como o dispositivo padrão, "dispositivo DirectSound padrão" é equivalente a "DirectSound: dispositivo A" e "dispositivo wave out padrão" é equivalente a "dispositivo A".</span><span class="sxs-lookup"><span data-stu-id="7d639-153">If the user selected Device A as the default device, then "Default DirectSound Device" is equivalent to "DirectSound: Device A," and "Default WaveOut Device" is equivalent to "Device A."</span></span> <span data-ttu-id="7d639-154">Se o usuário selecionar o dispositivo B como o dispositivo padrão, esses mapeamentos serão alterados.</span><span class="sxs-lookup"><span data-stu-id="7d639-154">If the user selects Device B as the default device, these mappings will change.</span></span>

<span data-ttu-id="7d639-155">"Dispositivo DirectSound padrão" é atribuído a um mérito de um mérito \_ preferido.</span><span class="sxs-lookup"><span data-stu-id="7d639-155">"Default DirectSound Device" is assigned a merit of MERIT\_PREFERRED.</span></span> <span data-ttu-id="7d639-156">Os outros têm mérito de \_ mérito \_ não \_ usam.</span><span class="sxs-lookup"><span data-stu-id="7d639-156">The others have merit MERIT\_DO\_NOT\_USE.</span></span> <span data-ttu-id="7d639-157">Portanto, o Intelligent Connect sempre escolherá o dispositivo DirectSound padrão.</span><span class="sxs-lookup"><span data-stu-id="7d639-157">Therefore, Intelligent Connect will always choose the default DirectSound device.</span></span>

<span data-ttu-id="7d639-158">O filtro do processador DirectSound dá suporte ao som 3D por meio das interfaces **IDirectSound3DBuffer** e **IDirectSound3dListener** do DirectSound.</span><span class="sxs-lookup"><span data-stu-id="7d639-158">The DirectSound Renderer filter supports 3D sound through the DirectSound **IDirectSound3DBuffer** and **IDirectSound3dListener** interfaces.</span></span> <span data-ttu-id="7d639-159">Você também pode consultar o filtro para as versões atuais dessas interfaces, **IDirectSound3DBuffer8** e **IDirectSound3dListener8**.</span><span class="sxs-lookup"><span data-stu-id="7d639-159">You can also query the filter for the current versions of these interfaces, **IDirectSound3DBuffer8** and **IDirectSound3dListener8**.</span></span> <span data-ttu-id="7d639-160">Execute o grafo antes de chamar métodos nessas interfaces.</span><span class="sxs-lookup"><span data-stu-id="7d639-160">Run the graph before calling methods on these interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d639-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d639-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d639-162">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="7d639-162">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




