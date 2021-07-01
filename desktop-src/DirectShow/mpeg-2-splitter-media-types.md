---
description: Tipos de mídia de divisor MPEG-2
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Tipos de mídia de divisor MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4e025fafabdeb8c437cc1d1cd6fbb843cf63e3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119971"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="2bc97-103">Tipos de mídia de divisor MPEG-2</span><span class="sxs-lookup"><span data-stu-id="2bc97-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="2bc97-104">O [filtro divisor MPEG-2](mpeg-2-splitter.md) atualmente dá suporte a áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="2bc97-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="2bc97-105">Há suporte para Dolby AC-3 como um substream conforme definido pelo DVD.</span><span class="sxs-lookup"><span data-stu-id="2bc97-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="2bc97-106">O filtro também dá suporte ao áudio MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="2bc97-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="2bc97-107">Os tipos de mídia dependem se o divisor MPEG-2 está fornecendo pacotes PES ou cargas PES.</span><span class="sxs-lookup"><span data-stu-id="2bc97-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="2bc97-108">Vídeo</span><span class="sxs-lookup"><span data-stu-id="2bc97-108">Video</span></span>

<span data-ttu-id="2bc97-109">Para o vídeo MPEG-2, os tipos de mídia são os a seguir.</span><span class="sxs-lookup"><span data-stu-id="2bc97-109">For MPEG-2 video, the media types are as follows.</span></span>


|                | <span data-ttu-id="2bc97-110">Saída do PES</span><span class="sxs-lookup"><span data-stu-id="2bc97-110">PES output</span></span> | <span data-ttu-id="2bc97-111">Saída de payload</span><span class="sxs-lookup"><span data-stu-id="2bc97-111">Payload output</span></span>
|------------------|------------------------------------------|--------------------------------|
| <span data-ttu-id="2bc97-112">**Tipo principal**</span><span class="sxs-lookup"><span data-stu-id="2bc97-112">**Major type**</span></span>       | <span data-ttu-id="2bc97-113">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="2bc97-113">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="2bc97-114">**Vídeo \_ MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="2bc97-114">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="2bc97-115">**Subtipo**</span><span class="sxs-lookup"><span data-stu-id="2bc97-115">**Subtype**</span></span>          | <span data-ttu-id="2bc97-116">**VÍDEO MEDIASUBTYPE \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="2bc97-116">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="2bc97-117">**VÍDEO MEDIASUBTYPE \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="2bc97-117">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="2bc97-118">**Tipo de formato**</span><span class="sxs-lookup"><span data-stu-id="2bc97-118">**Format type**</span></span>      | <span data-ttu-id="2bc97-119">**FORMATO \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="2bc97-119">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="2bc97-120">**FORMATO \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="2bc97-120">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="2bc97-121">**Estrutura de formato**</span><span class="sxs-lookup"><span data-stu-id="2bc97-121">**Format structure**</span></span> | [<span data-ttu-id="2bc97-122">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="2bc97-122">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="2bc97-123">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="2bc97-123">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="2bc97-124">Áudio AC-3</span><span class="sxs-lookup"><span data-stu-id="2bc97-124">AC-3 Audio</span></span>

<span data-ttu-id="2bc97-125">Para áudio AC-3, os tipos de mídia são os a seguir.</span><span class="sxs-lookup"><span data-stu-id="2bc97-125">For AC-3 audio, the media types are as follows.</span></span>

| | <span data-ttu-id="2bc97-126">Saída do PES</span><span class="sxs-lookup"><span data-stu-id="2bc97-126">PES output</span></span> | <span data-ttu-id="2bc97-127">Saída de payload</span><span class="sxs-lookup"><span data-stu-id="2bc97-127">Payload output</span></span> |
|------------------|--------------------------------------|------------------------------|
| <span data-ttu-id="2bc97-128">**Tipo principal**</span><span class="sxs-lookup"><span data-stu-id="2bc97-128">**Major type**</span></span>       | <span data-ttu-id="2bc97-129">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="2bc97-129">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="2bc97-130">**ÁUDIO \_ MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="2bc97-130">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="2bc97-131">**Subtipo**</span><span class="sxs-lookup"><span data-stu-id="2bc97-131">**Subtype**</span></span>          | <span data-ttu-id="2bc97-132">**MEDIASUBTYPE \_ DOLBY \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="2bc97-132">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span>             | <span data-ttu-id="2bc97-133">**MEDIASUBTYPE \_ DOLBY \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="2bc97-133">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="2bc97-134">**Tipo de formato**</span><span class="sxs-lookup"><span data-stu-id="2bc97-134">**Format type**</span></span>      | <span data-ttu-id="2bc97-135">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="2bc97-135">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="2bc97-136">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="2bc97-136">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="2bc97-137">**Estrutura de formato**</span><span class="sxs-lookup"><span data-stu-id="2bc97-137">**Format structure**</span></span> | <span data-ttu-id="2bc97-138">[**Waveformatex**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2bc97-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="2bc97-139">**Waveformatex**</span><span class="sxs-lookup"><span data-stu-id="2bc97-139">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="2bc97-140">O membro **wFormatTag** da estrutura **WAVEFORMATEX** para AC-3 atualmente é **WAVE FORMAT \_ \_ UNKNOWN,** mas isso pode mudar.</span><span class="sxs-lookup"><span data-stu-id="2bc97-140">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="2bc97-141">Áudio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="2bc97-141">MPEG-2 Audio</span></span>

<span data-ttu-id="2bc97-142">Para áudio MPEG-2, os tipos de mídia são os a seguir.</span><span class="sxs-lookup"><span data-stu-id="2bc97-142">For MPEG-2 audio, the media types are as follows.</span></span>



|  | <span data-ttu-id="2bc97-143">Saída do PES</span><span class="sxs-lookup"><span data-stu-id="2bc97-143">PES output</span></span> | <span data-ttu-id="2bc97-144">Saída de payload</span><span class="sxs-lookup"><span data-stu-id="2bc97-144">Payload output</span></span> |
|------------------|-------------------------------|--------------------------------|
| <span data-ttu-id="2bc97-145">**Tipo principal**</span><span class="sxs-lookup"><span data-stu-id="2bc97-145">**Major type**</span></span>       | <span data-ttu-id="2bc97-146">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="2bc97-146">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="2bc97-147">**ÁUDIO \_ MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="2bc97-147">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="2bc97-148">**Subtipo**</span><span class="sxs-lookup"><span data-stu-id="2bc97-148">**Subtype**</span></span>          | <span data-ttu-id="2bc97-149">**MEDIASUBTYE \_ MPEG2 \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="2bc97-149">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="2bc97-150">**ÁUDIO MEDIASUBTYPE \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="2bc97-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="2bc97-151">**Tipo de formato**</span><span class="sxs-lookup"><span data-stu-id="2bc97-151">**Format type**</span></span>      | <span data-ttu-id="2bc97-152">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="2bc97-152">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="2bc97-153">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="2bc97-153">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="2bc97-154">**Estrutura de formato**</span><span class="sxs-lookup"><span data-stu-id="2bc97-154">**Format structure**</span></span> | <span data-ttu-id="2bc97-155">**Waveformatex**</span><span class="sxs-lookup"><span data-stu-id="2bc97-155">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="2bc97-156">**Waveformatex**</span><span class="sxs-lookup"><span data-stu-id="2bc97-156">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="2bc97-157">O membro **wFormatTag** da estrutura **WAVEFORMATEX** para ÁUDIO MPEG-2 atualmente é **WAVE FORMAT \_ \_ UNKNOWN,** mas isso pode mudar.</span><span class="sxs-lookup"><span data-stu-id="2bc97-157">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="2bc97-158">O Divisor MPEG-2 presume que os fluxos D0 a DF são usados para o fluxo de extensão multicanal, como são para áudio MPEG-2 de DVD.</span><span class="sxs-lookup"><span data-stu-id="2bc97-158">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="2bc97-159">Portanto, sempre que o fluxo C *x* é selecionado, o divisor encaminha os pacotes para o fluxo D *x* também.</span><span class="sxs-lookup"><span data-stu-id="2bc97-159">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="2bc97-160">Áudio LPCM</span><span class="sxs-lookup"><span data-stu-id="2bc97-160">LPCM Audio</span></span>

<span data-ttu-id="2bc97-161">Para áudio LPCM, os tipos de mídia são os a seguir.</span><span class="sxs-lookup"><span data-stu-id="2bc97-161">For LPCM audio, the media types are as follows.</span></span>



|  | <span data-ttu-id="2bc97-162">Saída do PES</span><span class="sxs-lookup"><span data-stu-id="2bc97-162">PES output</span></span> | <span data-ttu-id="2bc97-163">Saída de payload</span><span class="sxs-lookup"><span data-stu-id="2bc97-163">Payload output</span></span> |
|------------------|------------------------------------|------------------------------------|
| <span data-ttu-id="2bc97-164">**Tipo principal**</span><span class="sxs-lookup"><span data-stu-id="2bc97-164">**Major type**</span></span>       | <span data-ttu-id="2bc97-165">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="2bc97-165">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="2bc97-166">**ÁUDIO \_ MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="2bc97-166">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="2bc97-167">**Subtipo**</span><span class="sxs-lookup"><span data-stu-id="2bc97-167">**Subtype**</span></span>          | <span data-ttu-id="2bc97-168">**ÁUDIO \_ LPCM DE DVD MEDIASUBTYPE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2bc97-168">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="2bc97-169">**ÁUDIO \_ LPCM DE DVD MEDIASUBTYPE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2bc97-169">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="2bc97-170">**Tipo de formato**</span><span class="sxs-lookup"><span data-stu-id="2bc97-170">**Format type**</span></span>      | <span data-ttu-id="2bc97-171">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="2bc97-171">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="2bc97-172">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="2bc97-172">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="2bc97-173">**Estrutura de formato**</span><span class="sxs-lookup"><span data-stu-id="2bc97-173">**Format structure**</span></span> | <span data-ttu-id="2bc97-174">**Waveformatex**</span><span class="sxs-lookup"><span data-stu-id="2bc97-174">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="2bc97-175">**Waveformatex**</span><span class="sxs-lookup"><span data-stu-id="2bc97-175">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="2bc97-176">O membro **wFormatTag** da estrutura **WAVEFORMATEX** para áudio LPCM atualmente é **WAVE FORMAT \_ \_ UNKNOWN,** mas isso pode mudar.</span><span class="sxs-lookup"><span data-stu-id="2bc97-176">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2bc97-177">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2bc97-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bc97-178">Tipos de mídia MPEG-2</span><span class="sxs-lookup"><span data-stu-id="2bc97-178">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
