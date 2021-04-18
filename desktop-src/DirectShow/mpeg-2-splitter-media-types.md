---
description: Tipos de mídia de divisor MPEG-2
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Tipos de mídia de divisor MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb10310bd126346c8e1558801200682792836d92
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105810489"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="ddfbb-103">Tipos de mídia de divisor MPEG-2</span><span class="sxs-lookup"><span data-stu-id="ddfbb-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="ddfbb-104">O filtro [divisor MPEG-2](mpeg-2-splitter.md) atualmente dá suporte a áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="ddfbb-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="ddfbb-105">O Dolby AC-3 tem suporte como um subfluxo, conforme definido pelo DVD.</span><span class="sxs-lookup"><span data-stu-id="ddfbb-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="ddfbb-106">O filtro também dá suporte a áudio MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="ddfbb-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="ddfbb-107">Os tipos de mídia dependem se o divisor MPEG-2 está entregando pacotes PES ou cargas PES.</span><span class="sxs-lookup"><span data-stu-id="ddfbb-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="ddfbb-108">Vídeo</span><span class="sxs-lookup"><span data-stu-id="ddfbb-108">Video</span></span>

<span data-ttu-id="ddfbb-109">Para vídeo MPEG-2, os tipos de mídia são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="ddfbb-109">For MPEG-2 video, the media types are as follows.</span></span>



|                  |                                          |                                |
|------------------|------------------------------------------|--------------------------------|
|                  | <span data-ttu-id="ddfbb-110">Saída de PES</span><span class="sxs-lookup"><span data-stu-id="ddfbb-110">PES output</span></span>                               | <span data-ttu-id="ddfbb-111">Saída da carga</span><span class="sxs-lookup"><span data-stu-id="ddfbb-111">Payload output</span></span>                 |
| <span data-ttu-id="ddfbb-112">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="ddfbb-112">Major Type</span></span>       | <span data-ttu-id="ddfbb-113">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-113">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="ddfbb-114">**Vídeo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-114">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="ddfbb-115">Subtype</span><span class="sxs-lookup"><span data-stu-id="ddfbb-115">Subtype</span></span>          | <span data-ttu-id="ddfbb-116">**Vídeo do MEDIASUBTYPE \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-116">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="ddfbb-117">**Vídeo do MEDIASUBTYPE \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-117">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="ddfbb-118">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="ddfbb-118">Format Type</span></span>      | <span data-ttu-id="ddfbb-119">**MPEG2Video de formato \_**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-119">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="ddfbb-120">**MPEG2Video de formato \_**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-120">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="ddfbb-121">Estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="ddfbb-121">Format Structure</span></span> | [<span data-ttu-id="ddfbb-122">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-122">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="ddfbb-123">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-123">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="ddfbb-124">Áudio AC-3</span><span class="sxs-lookup"><span data-stu-id="ddfbb-124">AC-3 Audio</span></span>

<span data-ttu-id="ddfbb-125">Para áudio AC-3, os tipos de mídia são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="ddfbb-125">For AC-3 audio, the media types are as follows.</span></span>



|                  |                                      |                              |
|------------------|--------------------------------------|------------------------------|
|                  | <span data-ttu-id="ddfbb-126">Saída de PES</span><span class="sxs-lookup"><span data-stu-id="ddfbb-126">PES output</span></span>                           | <span data-ttu-id="ddfbb-127">Saída da carga</span><span class="sxs-lookup"><span data-stu-id="ddfbb-127">Payload output</span></span>               |
| <span data-ttu-id="ddfbb-128">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="ddfbb-128">Major Type</span></span>       | <span data-ttu-id="ddfbb-129">MEDIATYPE \_ MPEG2 \_ PES</span><span class="sxs-lookup"><span data-stu-id="ddfbb-129">MEDIATYPE\_MPEG2\_PES</span></span>                | <span data-ttu-id="ddfbb-130">**Áudio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-130">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="ddfbb-131">Subtype</span><span class="sxs-lookup"><span data-stu-id="ddfbb-131">Subtype</span></span>          | <span data-ttu-id="ddfbb-132">MEDIASUBTYPE \_ Dolby \_ AC3</span><span class="sxs-lookup"><span data-stu-id="ddfbb-132">MEDIASUBTYPE\_DOLBY\_AC3</span></span>             | <span data-ttu-id="ddfbb-133">**MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-133">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="ddfbb-134">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="ddfbb-134">Format Type</span></span>      | <span data-ttu-id="ddfbb-135">WaveFormatEx de formato \_</span><span class="sxs-lookup"><span data-stu-id="ddfbb-135">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="ddfbb-136">**WaveFormatEx de formato \_**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-136">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="ddfbb-137">Estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="ddfbb-137">Format Structure</span></span> | <span data-ttu-id="ddfbb-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ddfbb-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="ddfbb-139">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-139">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="ddfbb-140">O membro **wFormatTag** da estrutura **WAVEFORMATEX** para AC-3 atualmente é **um \_ formato Wave \_ desconhecido**, mas isso pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="ddfbb-140">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="ddfbb-141">Áudio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="ddfbb-141">MPEG-2 Audio</span></span>

<span data-ttu-id="ddfbb-142">Para áudio MPEG-2, os tipos de mídia são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="ddfbb-142">For MPEG-2 audio, the media types are as follows.</span></span>



|                  |                               |                                |
|------------------|-------------------------------|--------------------------------|
|                  | <span data-ttu-id="ddfbb-143">Saída de PES</span><span class="sxs-lookup"><span data-stu-id="ddfbb-143">PES output</span></span>                    | <span data-ttu-id="ddfbb-144">Saída da carga</span><span class="sxs-lookup"><span data-stu-id="ddfbb-144">Payload output</span></span>                 |
| <span data-ttu-id="ddfbb-145">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="ddfbb-145">Major Type</span></span>       | <span data-ttu-id="ddfbb-146">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-146">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="ddfbb-147">**Áudio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-147">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="ddfbb-148">Subtype</span><span class="sxs-lookup"><span data-stu-id="ddfbb-148">Subtype</span></span>          | <span data-ttu-id="ddfbb-149">**\_Áudio MEDIASUBTYE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-149">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="ddfbb-150">**\_Áudio MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="ddfbb-151">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="ddfbb-151">Format Type</span></span>      | <span data-ttu-id="ddfbb-152">**WaveFormatEx de formato \_**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-152">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="ddfbb-153">**WaveFormatEx de formato \_**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-153">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="ddfbb-154">Estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="ddfbb-154">Format Structure</span></span> | <span data-ttu-id="ddfbb-155">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-155">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="ddfbb-156">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-156">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="ddfbb-157">O membro **wFormatTag** da estrutura **WAVEFORMATEX** para áudio MPEG-2 está no **\_ formato Wave \_ desconhecido** no momento, mas isso pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="ddfbb-157">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="ddfbb-158">O divisor MPEG-2 pressupõe que fluxos D0 por meio de DF são usados para o fluxo de extensão multicanal, como são para áudio MPEG-2 de DVD.</span><span class="sxs-lookup"><span data-stu-id="ddfbb-158">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="ddfbb-159">Portanto, sempre que o fluxo C *x* é selecionado, o divisor encaminha os pacotes para o fluxo D *x* também.</span><span class="sxs-lookup"><span data-stu-id="ddfbb-159">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="ddfbb-160">Áudio LPCM</span><span class="sxs-lookup"><span data-stu-id="ddfbb-160">LPCM Audio</span></span>

<span data-ttu-id="ddfbb-161">Para áudio LPCM, os tipos de mídia são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="ddfbb-161">For LPCM audio, the media types are as follows.</span></span>



|                  |                                    |                                    |
|------------------|------------------------------------|------------------------------------|
|                  | <span data-ttu-id="ddfbb-162">Saída de PES</span><span class="sxs-lookup"><span data-stu-id="ddfbb-162">PES output</span></span>                         | <span data-ttu-id="ddfbb-163">Saída da carga</span><span class="sxs-lookup"><span data-stu-id="ddfbb-163">Payload output</span></span>                     |
| <span data-ttu-id="ddfbb-164">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="ddfbb-164">Major Type</span></span>       | <span data-ttu-id="ddfbb-165">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-165">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="ddfbb-166">**Áudio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-166">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="ddfbb-167">Subtype</span><span class="sxs-lookup"><span data-stu-id="ddfbb-167">Subtype</span></span>          | <span data-ttu-id="ddfbb-168">**\_áudio MEDIASUBTYPE DVD \_ LPCM \_**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-168">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="ddfbb-169">**\_áudio MEDIASUBTYPE DVD \_ LPCM \_**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-169">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="ddfbb-170">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="ddfbb-170">Format Type</span></span>      | <span data-ttu-id="ddfbb-171">**WaveFormatEx de formato \_**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-171">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="ddfbb-172">**WaveFormatEx de formato \_**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-172">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="ddfbb-173">Estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="ddfbb-173">Format Structure</span></span> | <span data-ttu-id="ddfbb-174">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-174">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="ddfbb-175">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="ddfbb-175">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="ddfbb-176">Atualmente, o membro **wFormatTag** da estrutura **WAVEFORMATEX** para áudio LPCM **é \_ \_ desconhecido no formato Wave**, mas isso pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="ddfbb-176">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ddfbb-177">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ddfbb-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddfbb-178">Tipos de mídia MPEG-2</span><span class="sxs-lookup"><span data-stu-id="ddfbb-178">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
