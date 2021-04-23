---
description: Tipos de mídia de divisor MPEG-2
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Tipos de mídia de divisor MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e878acaea8bc87bee2bf5c46a6f7e66c7aa0a485
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909415"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="bc268-103">Tipos de mídia de divisor MPEG-2</span><span class="sxs-lookup"><span data-stu-id="bc268-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="bc268-104">O filtro [divisor MPEG-2](mpeg-2-splitter.md) atualmente dá suporte a áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="bc268-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="bc268-105">O Dolby AC-3 tem suporte como um subfluxo, conforme definido pelo DVD.</span><span class="sxs-lookup"><span data-stu-id="bc268-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="bc268-106">O filtro também dá suporte a áudio MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="bc268-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="bc268-107">Os tipos de mídia dependem se o divisor MPEG-2 está entregando pacotes PES ou cargas PES.</span><span class="sxs-lookup"><span data-stu-id="bc268-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="bc268-108">Vídeo</span><span class="sxs-lookup"><span data-stu-id="bc268-108">Video</span></span>

<span data-ttu-id="bc268-109">Para vídeo MPEG-2, os tipos de mídia são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="bc268-109">For MPEG-2 video, the media types are as follows.</span></span>



| <span data-ttu-id="bc268-110">Label</span><span class="sxs-lookup"><span data-stu-id="bc268-110">Label</span></span> | <span data-ttu-id="bc268-111">Valor</span><span class="sxs-lookup"><span data-stu-id="bc268-111">Value</span></span> |
|------------------|------------------------------------------|--------------------------------|
|                  | <span data-ttu-id="bc268-112">Saída de PES</span><span class="sxs-lookup"><span data-stu-id="bc268-112">PES output</span></span>                               | <span data-ttu-id="bc268-113">Saída da carga</span><span class="sxs-lookup"><span data-stu-id="bc268-113">Payload output</span></span>                 |
| <span data-ttu-id="bc268-114">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="bc268-114">Major Type</span></span>       | <span data-ttu-id="bc268-115">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="bc268-115">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="bc268-116">**Vídeo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="bc268-116">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="bc268-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="bc268-117">Subtype</span></span>          | <span data-ttu-id="bc268-118">**Vídeo do MEDIASUBTYPE \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="bc268-118">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="bc268-119">**Vídeo do MEDIASUBTYPE \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="bc268-119">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="bc268-120">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="bc268-120">Format Type</span></span>      | <span data-ttu-id="bc268-121">**MPEG2Video de formato \_**</span><span class="sxs-lookup"><span data-stu-id="bc268-121">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="bc268-122">**MPEG2Video de formato \_**</span><span class="sxs-lookup"><span data-stu-id="bc268-122">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="bc268-123">Estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="bc268-123">Format Structure</span></span> | [<span data-ttu-id="bc268-124">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="bc268-124">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="bc268-125">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="bc268-125">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="bc268-126">Áudio AC-3</span><span class="sxs-lookup"><span data-stu-id="bc268-126">AC-3 Audio</span></span>

<span data-ttu-id="bc268-127">Para áudio AC-3, os tipos de mídia são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="bc268-127">For AC-3 audio, the media types are as follows.</span></span>



| <span data-ttu-id="bc268-128">Label</span><span class="sxs-lookup"><span data-stu-id="bc268-128">Label</span></span> | <span data-ttu-id="bc268-129">Valor</span><span class="sxs-lookup"><span data-stu-id="bc268-129">Value</span></span> |
|------------------|--------------------------------------|------------------------------|
|                  | <span data-ttu-id="bc268-130">Saída de PES</span><span class="sxs-lookup"><span data-stu-id="bc268-130">PES output</span></span>                           | <span data-ttu-id="bc268-131">Saída da carga</span><span class="sxs-lookup"><span data-stu-id="bc268-131">Payload output</span></span>               |
| <span data-ttu-id="bc268-132">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="bc268-132">Major Type</span></span>       | <span data-ttu-id="bc268-133">MEDIATYPE \_ MPEG2 \_ PES</span><span class="sxs-lookup"><span data-stu-id="bc268-133">MEDIATYPE\_MPEG2\_PES</span></span>                | <span data-ttu-id="bc268-134">**Áudio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="bc268-134">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="bc268-135">Subtype</span><span class="sxs-lookup"><span data-stu-id="bc268-135">Subtype</span></span>          | <span data-ttu-id="bc268-136">MEDIASUBTYPE \_ Dolby \_ AC3</span><span class="sxs-lookup"><span data-stu-id="bc268-136">MEDIASUBTYPE\_DOLBY\_AC3</span></span>             | <span data-ttu-id="bc268-137">**MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="bc268-137">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="bc268-138">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="bc268-138">Format Type</span></span>      | <span data-ttu-id="bc268-139">WaveFormatEx de formato \_</span><span class="sxs-lookup"><span data-stu-id="bc268-139">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="bc268-140">**WaveFormatEx de formato \_**</span><span class="sxs-lookup"><span data-stu-id="bc268-140">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="bc268-141">Estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="bc268-141">Format Structure</span></span> | <span data-ttu-id="bc268-142">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bc268-142">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="bc268-143">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="bc268-143">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="bc268-144">O membro **wFormatTag** da estrutura **WAVEFORMATEX** para AC-3 atualmente é **um \_ formato Wave \_ desconhecido**, mas isso pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="bc268-144">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="bc268-145">Áudio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="bc268-145">MPEG-2 Audio</span></span>

<span data-ttu-id="bc268-146">Para áudio MPEG-2, os tipos de mídia são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="bc268-146">For MPEG-2 audio, the media types are as follows.</span></span>



| <span data-ttu-id="bc268-147">Label</span><span class="sxs-lookup"><span data-stu-id="bc268-147">Label</span></span> | <span data-ttu-id="bc268-148">Valor</span><span class="sxs-lookup"><span data-stu-id="bc268-148">Value</span></span> |
|------------------|-------------------------------|--------------------------------|
|                  | <span data-ttu-id="bc268-149">Saída de PES</span><span class="sxs-lookup"><span data-stu-id="bc268-149">PES output</span></span>                    | <span data-ttu-id="bc268-150">Saída da carga</span><span class="sxs-lookup"><span data-stu-id="bc268-150">Payload output</span></span>                 |
| <span data-ttu-id="bc268-151">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="bc268-151">Major Type</span></span>       | <span data-ttu-id="bc268-152">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="bc268-152">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="bc268-153">**Áudio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="bc268-153">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="bc268-154">Subtype</span><span class="sxs-lookup"><span data-stu-id="bc268-154">Subtype</span></span>          | <span data-ttu-id="bc268-155">**\_Áudio MEDIASUBTYE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="bc268-155">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="bc268-156">**\_Áudio MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="bc268-156">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="bc268-157">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="bc268-157">Format Type</span></span>      | <span data-ttu-id="bc268-158">**WaveFormatEx de formato \_**</span><span class="sxs-lookup"><span data-stu-id="bc268-158">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="bc268-159">**WaveFormatEx de formato \_**</span><span class="sxs-lookup"><span data-stu-id="bc268-159">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="bc268-160">Estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="bc268-160">Format Structure</span></span> | <span data-ttu-id="bc268-161">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="bc268-161">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="bc268-162">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="bc268-162">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="bc268-163">O membro **wFormatTag** da estrutura **WAVEFORMATEX** para áudio MPEG-2 está no **\_ formato Wave \_ desconhecido** no momento, mas isso pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="bc268-163">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="bc268-164">O divisor MPEG-2 pressupõe que fluxos D0 por meio de DF são usados para o fluxo de extensão multicanal, como são para áudio MPEG-2 de DVD.</span><span class="sxs-lookup"><span data-stu-id="bc268-164">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="bc268-165">Portanto, sempre que o fluxo C *x* é selecionado, o divisor encaminha os pacotes para o fluxo D *x* também.</span><span class="sxs-lookup"><span data-stu-id="bc268-165">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="bc268-166">Áudio LPCM</span><span class="sxs-lookup"><span data-stu-id="bc268-166">LPCM Audio</span></span>

<span data-ttu-id="bc268-167">Para áudio LPCM, os tipos de mídia são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="bc268-167">For LPCM audio, the media types are as follows.</span></span>



| <span data-ttu-id="bc268-168">Label</span><span class="sxs-lookup"><span data-stu-id="bc268-168">Label</span></span> | <span data-ttu-id="bc268-169">Valor</span><span class="sxs-lookup"><span data-stu-id="bc268-169">Value</span></span> |
|------------------|------------------------------------|------------------------------------|
|                  | <span data-ttu-id="bc268-170">Saída de PES</span><span class="sxs-lookup"><span data-stu-id="bc268-170">PES output</span></span>                         | <span data-ttu-id="bc268-171">Saída da carga</span><span class="sxs-lookup"><span data-stu-id="bc268-171">Payload output</span></span>                     |
| <span data-ttu-id="bc268-172">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="bc268-172">Major Type</span></span>       | <span data-ttu-id="bc268-173">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="bc268-173">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="bc268-174">**Áudio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="bc268-174">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="bc268-175">Subtype</span><span class="sxs-lookup"><span data-stu-id="bc268-175">Subtype</span></span>          | <span data-ttu-id="bc268-176">**\_áudio MEDIASUBTYPE DVD \_ LPCM \_**</span><span class="sxs-lookup"><span data-stu-id="bc268-176">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="bc268-177">**\_áudio MEDIASUBTYPE DVD \_ LPCM \_**</span><span class="sxs-lookup"><span data-stu-id="bc268-177">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="bc268-178">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="bc268-178">Format Type</span></span>      | <span data-ttu-id="bc268-179">**WaveFormatEx de formato \_**</span><span class="sxs-lookup"><span data-stu-id="bc268-179">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="bc268-180">**WaveFormatEx de formato \_**</span><span class="sxs-lookup"><span data-stu-id="bc268-180">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="bc268-181">Estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="bc268-181">Format Structure</span></span> | <span data-ttu-id="bc268-182">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="bc268-182">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="bc268-183">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="bc268-183">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="bc268-184">Atualmente, o membro **wFormatTag** da estrutura **WAVEFORMATEX** para áudio LPCM **é \_ \_ desconhecido no formato Wave**, mas isso pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="bc268-184">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc268-185">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc268-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc268-186">Tipos de mídia MPEG-2</span><span class="sxs-lookup"><span data-stu-id="bc268-186">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
