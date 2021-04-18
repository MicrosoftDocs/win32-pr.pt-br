---
description: Esta seção lista os tipos de mídia usados para dados MPEG-1.
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: Tipos de mídia MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d1ff7c121c52db39d574f9bbae3650b04312e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105784115"
---
# <a name="mpeg-1-media-types"></a><span data-ttu-id="5835f-103">Tipos de mídia MPEG-1</span><span class="sxs-lookup"><span data-stu-id="5835f-103">MPEG-1 Media Types</span></span>

<span data-ttu-id="5835f-104">Esta seção lista os tipos de mídia usados para dados MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="5835f-104">This section lists the media types used for MPEG-1 data.</span></span>

## <a name="mpeg-1-system-stream"></a><span data-ttu-id="5835f-105">MPEG-1 System Stream</span><span class="sxs-lookup"><span data-stu-id="5835f-105">MPEG-1 System Stream</span></span>



|                       |                                                 |
|-----------------------|-------------------------------------------------|
| <span data-ttu-id="5835f-106">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="5835f-106">Major type</span></span>            | <span data-ttu-id="5835f-107">Fluxo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="5835f-107">MEDIATYPE\_Stream</span></span>                               |
| <span data-ttu-id="5835f-108">Subtype</span><span class="sxs-lookup"><span data-stu-id="5835f-108">Subtype</span></span>               | <span data-ttu-id="5835f-109">MEDIASUBTYPE \_ MPEG1System</span><span class="sxs-lookup"><span data-stu-id="5835f-109">MEDIASUBTYPE\_MPEG1System</span></span>                       |
| <span data-ttu-id="5835f-110">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="5835f-110">Format Type</span></span>           | <span data-ttu-id="5835f-111">MPEGStreams de formato \_</span><span class="sxs-lookup"><span data-stu-id="5835f-111">FORMAT\_MPEGStreams</span></span>                             |
| <span data-ttu-id="5835f-112">Estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="5835f-112">Format Structure</span></span>      | [<span data-ttu-id="5835f-113">**AM \_ MPEGSYSTEMTYPE**</span><span class="sxs-lookup"><span data-stu-id="5835f-113">**AM\_MPEGSYSTEMTYPE**</span></span>](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| <span data-ttu-id="5835f-114">Conteúdo de exemplo de mídia</span><span class="sxs-lookup"><span data-stu-id="5835f-114">Media Sample Contents</span></span> | <span data-ttu-id="5835f-115">Fluxo de bytes; sem alinhamento</span><span class="sxs-lookup"><span data-stu-id="5835f-115">Byte stream; no alignment</span></span>                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a><span data-ttu-id="5835f-116">Fluxo do sistema MPEG-1 do CD de vídeo</span><span class="sxs-lookup"><span data-stu-id="5835f-116">MPEG-1 System Stream from Video CD</span></span>



|                       |                            |
|-----------------------|----------------------------|
| <span data-ttu-id="5835f-117">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="5835f-117">Major type</span></span>            | <span data-ttu-id="5835f-118">Fluxo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="5835f-118">MEDIATYPE\_Stream</span></span>          |
| <span data-ttu-id="5835f-119">Subtype</span><span class="sxs-lookup"><span data-stu-id="5835f-119">Subtype</span></span>               | <span data-ttu-id="5835f-120">MEDIASUBTYPE \_ MPEG1VideoCD</span><span class="sxs-lookup"><span data-stu-id="5835f-120">MEDIASUBTYPE\_MPEG1VideoCD</span></span> |
| <span data-ttu-id="5835f-121">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="5835f-121">Format Type</span></span>           | <span data-ttu-id="5835f-122">GUID \_ nulo</span><span class="sxs-lookup"><span data-stu-id="5835f-122">GUID\_NULL</span></span>                 |
| <span data-ttu-id="5835f-123">Estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="5835f-123">Format Structure</span></span>      | <span data-ttu-id="5835f-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5835f-124">None</span></span>                       |
| <span data-ttu-id="5835f-125">Conteúdo de exemplo de mídia</span><span class="sxs-lookup"><span data-stu-id="5835f-125">Media Sample Contents</span></span> | <span data-ttu-id="5835f-126">Fluxo de bytes; sem alinhamento.</span><span class="sxs-lookup"><span data-stu-id="5835f-126">Byte stream; no alignment.</span></span> |



 

## <a name="mpeg-1-audio-packet"></a><span data-ttu-id="5835f-127">Pacote de áudio MPEG-1</span><span class="sxs-lookup"><span data-stu-id="5835f-127">MPEG-1 Audio Packet</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="5835f-128">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="5835f-128">Major type</span></span>            | <span data-ttu-id="5835f-129">Áudio de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="5835f-129">MEDIATYPE\_Audio</span></span>                               |
| <span data-ttu-id="5835f-130">Subtype</span><span class="sxs-lookup"><span data-stu-id="5835f-130">Subtype</span></span>               | <span data-ttu-id="5835f-131">MEDIASUBTYPE \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="5835f-131">MEDIASUBTYPE\_MPEG1Packet</span></span>                      |
| <span data-ttu-id="5835f-132">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="5835f-132">Format Type</span></span>           | <span data-ttu-id="5835f-133">WaveFormatEx de formato \_</span><span class="sxs-lookup"><span data-stu-id="5835f-133">FORMAT\_WaveFormatEx</span></span>                           |
| <span data-ttu-id="5835f-134">Estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="5835f-134">Format Structure</span></span>      | [<span data-ttu-id="5835f-135">**MPEG1WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="5835f-135">**MPEG1WAVEFORMAT**</span></span>](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| <span data-ttu-id="5835f-136">Conteúdo de exemplo de mídia</span><span class="sxs-lookup"><span data-stu-id="5835f-136">Media Sample Contents</span></span> | <span data-ttu-id="5835f-137">Pacote único MPEG-1, incluindo o cabeçalho do pacote.</span><span class="sxs-lookup"><span data-stu-id="5835f-137">Single MPEG-1 packet, including packet header.</span></span> |



 

## <a name="mpeg-1-audio-payload"></a><span data-ttu-id="5835f-138">Carga de áudio MPEG-1</span><span class="sxs-lookup"><span data-stu-id="5835f-138">MPEG-1 Audio Payload</span></span>



|                       |                                            |
|-----------------------|--------------------------------------------|
| <span data-ttu-id="5835f-139">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="5835f-139">Major type</span></span>            | <span data-ttu-id="5835f-140">Áudio de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="5835f-140">MEDIATYPE\_Audio</span></span>                           |
| <span data-ttu-id="5835f-141">Subtype</span><span class="sxs-lookup"><span data-stu-id="5835f-141">Subtype</span></span>               | <span data-ttu-id="5835f-142">MEDIASUBTYPE \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="5835f-142">MEDIASUBTYPE\_MPEG1Payload</span></span>                 |
| <span data-ttu-id="5835f-143">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="5835f-143">Format Type</span></span>           | <span data-ttu-id="5835f-144">WaveFormatEx de formato \_</span><span class="sxs-lookup"><span data-stu-id="5835f-144">FORMAT\_WaveFormatEx</span></span>                       |
| <span data-ttu-id="5835f-145">Estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="5835f-145">Format Structure</span></span>      | [<span data-ttu-id="5835f-146">**MPEG1WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="5835f-146">**MPEG1WAVEFORMAT**</span></span>](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| <span data-ttu-id="5835f-147">Conteúdo de exemplo de mídia</span><span class="sxs-lookup"><span data-stu-id="5835f-147">Media Sample Contents</span></span> | <span data-ttu-id="5835f-148">Dados de áudio MPEG-1 alinhados em byte.</span><span class="sxs-lookup"><span data-stu-id="5835f-148">Byte-aligned MPEG-1 audio data.</span></span>            |



 

## <a name="mpeg-1-video-packet"></a><span data-ttu-id="5835f-149">Pacote de vídeo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="5835f-149">MPEG-1 Video Packet</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="5835f-150">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="5835f-150">Major type</span></span>            | <span data-ttu-id="5835f-151">Vídeo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="5835f-151">MEDIATYPE\_Video</span></span>                               |
| <span data-ttu-id="5835f-152">Subtype</span><span class="sxs-lookup"><span data-stu-id="5835f-152">Subtype</span></span>               | <span data-ttu-id="5835f-153">MEDIASUBTYPE \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="5835f-153">MEDIASUBTYPE\_MPEG1Packet</span></span>                      |
| <span data-ttu-id="5835f-154">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="5835f-154">Format Type</span></span>           | <span data-ttu-id="5835f-155">MPEGVideo de formato \_</span><span class="sxs-lookup"><span data-stu-id="5835f-155">FORMAT\_MPEGVideo</span></span>                              |
| <span data-ttu-id="5835f-156">Estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="5835f-156">Format Structure</span></span>      | [<span data-ttu-id="5835f-157">**MPEG1VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="5835f-157">**MPEG1VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| <span data-ttu-id="5835f-158">Conteúdo de exemplo de mídia</span><span class="sxs-lookup"><span data-stu-id="5835f-158">Media Sample Contents</span></span> | <span data-ttu-id="5835f-159">Pacote único MPEG-1, incluindo o cabeçalho do pacote.</span><span class="sxs-lookup"><span data-stu-id="5835f-159">Single MPEG-1 packet, including packet header.</span></span> |



 

## <a name="mpeg-1-video-payload"></a><span data-ttu-id="5835f-160">Carga de vídeo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="5835f-160">MPEG-1 Video payload</span></span>



|                       |                                          |
|-----------------------|------------------------------------------|
| <span data-ttu-id="5835f-161">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="5835f-161">Major type</span></span>            | <span data-ttu-id="5835f-162">Vídeo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="5835f-162">MEDIATYPE\_Video</span></span>                         |
| <span data-ttu-id="5835f-163">Subtype</span><span class="sxs-lookup"><span data-stu-id="5835f-163">Subtype</span></span>               | <span data-ttu-id="5835f-164">MEDIASUBTYPE \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="5835f-164">MEDIASUBTYPE\_MPEG1Payload</span></span>               |
| <span data-ttu-id="5835f-165">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="5835f-165">Format Type</span></span>           | <span data-ttu-id="5835f-166">MPEGVideo de formato \_</span><span class="sxs-lookup"><span data-stu-id="5835f-166">FORMAT\_MPEGVideo</span></span>                        |
| <span data-ttu-id="5835f-167">Estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="5835f-167">Format Structure</span></span>      | [<span data-ttu-id="5835f-168">**MPEG1VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="5835f-168">**MPEG1VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| <span data-ttu-id="5835f-169">Conteúdo de exemplo de mídia</span><span class="sxs-lookup"><span data-stu-id="5835f-169">Media Sample Contents</span></span> | <span data-ttu-id="5835f-170">Dados de vídeo MPEG-1 alinhados em byte.</span><span class="sxs-lookup"><span data-stu-id="5835f-170">Byte-aligned MPEG-1 video data.</span></span>          |



 

## <a name="mpeg-1-native-video-stream"></a><span data-ttu-id="5835f-171">Fluxo de vídeo nativo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="5835f-171">MPEG-1 Native Video Stream</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="5835f-172">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="5835f-172">Major type</span></span>            | <span data-ttu-id="5835f-173">Fluxo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="5835f-173">MEDIATYPE\_Stream</span></span>                              |
| <span data-ttu-id="5835f-174">Subtype</span><span class="sxs-lookup"><span data-stu-id="5835f-174">Subtype</span></span>               | <span data-ttu-id="5835f-175">MEDIASUBTYPE \_ MPEG1Video</span><span class="sxs-lookup"><span data-stu-id="5835f-175">MEDIASUBTYPE\_ MPEG1Video</span></span>                      |
| <span data-ttu-id="5835f-176">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="5835f-176">Format Type</span></span>           | <span data-ttu-id="5835f-177">GUID \_ nulo</span><span class="sxs-lookup"><span data-stu-id="5835f-177">GUID\_NULL</span></span>                                     |
| <span data-ttu-id="5835f-178">Estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="5835f-178">Format Structure</span></span>      | <span data-ttu-id="5835f-179">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5835f-179">None</span></span>                                           |
| <span data-ttu-id="5835f-180">Conteúdo de exemplo de mídia</span><span class="sxs-lookup"><span data-stu-id="5835f-180">Media Sample Contents</span></span> | <span data-ttu-id="5835f-181">Matriz de bytes de fluxo de vídeo (sem camada do sistema).</span><span class="sxs-lookup"><span data-stu-id="5835f-181">Array of video stream bytes (no system layer).</span></span> |



 

## <a name="mpeg-1-native-audio-stream"></a><span data-ttu-id="5835f-182">Fluxo de áudio nativo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="5835f-182">MPEG-1 Native Audio Stream</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="5835f-183">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="5835f-183">Major type</span></span>            | <span data-ttu-id="5835f-184">Fluxo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="5835f-184">MEDIATYPE\_Stream</span></span>                              |
| <span data-ttu-id="5835f-185">Subtype</span><span class="sxs-lookup"><span data-stu-id="5835f-185">Subtype</span></span>               | <span data-ttu-id="5835f-186">MEDIASUBTYPE \_ MPEG1Audio</span><span class="sxs-lookup"><span data-stu-id="5835f-186">MEDIASUBTYPE\_ MPEG1Audio</span></span>                      |
| <span data-ttu-id="5835f-187">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="5835f-187">Format Type</span></span>           | <span data-ttu-id="5835f-188">GUID \_ nulo</span><span class="sxs-lookup"><span data-stu-id="5835f-188">GUID\_NULL</span></span>                                     |
| <span data-ttu-id="5835f-189">Estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="5835f-189">Format Structure</span></span>      | <span data-ttu-id="5835f-190">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5835f-190">None</span></span>                                           |
| <span data-ttu-id="5835f-191">Conteúdo de exemplo de mídia</span><span class="sxs-lookup"><span data-stu-id="5835f-191">Media Sample Contents</span></span> | <span data-ttu-id="5835f-192">Matriz de bytes de fluxo de áudio (sem camada do sistema).</span><span class="sxs-lookup"><span data-stu-id="5835f-192">Array of audio stream bytes (no system layer).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5835f-193">Comentários</span><span class="sxs-lookup"><span data-stu-id="5835f-193">Remarks</span></span>

<span data-ttu-id="5835f-194">Os filtros MPEG-1 do DirectShow dão suporte a esses tipos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="5835f-194">The DirectShow MPEG-1 filters support these types as follows.</span></span>



| <span data-ttu-id="5835f-195">Filtrar</span><span class="sxs-lookup"><span data-stu-id="5835f-195">Filter</span></span>               | <span data-ttu-id="5835f-196">Direção</span><span class="sxs-lookup"><span data-stu-id="5835f-196">Direction</span></span> | <span data-ttu-id="5835f-197">Tipos de mídia com suporte</span><span class="sxs-lookup"><span data-stu-id="5835f-197">Supported media types</span></span>                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5835f-198">Divisor MPEG-1</span><span class="sxs-lookup"><span data-stu-id="5835f-198">MPEG-1 Splitter</span></span>      | <span data-ttu-id="5835f-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="5835f-199">Input</span></span>     | <span data-ttu-id="5835f-200">Fluxo do sistema streamMPEG-1 do sistema MPEG-1 do CD de vídeo</span><span class="sxs-lookup"><span data-stu-id="5835f-200">MPEG-1 system streamMPEG-1 system stream from Video CD</span></span><br/>                                                 |
| <span data-ttu-id="5835f-201">Divisor MPEG-1</span><span class="sxs-lookup"><span data-stu-id="5835f-201">MPEG-1 Splitter</span></span>      | <span data-ttu-id="5835f-202">Saída</span><span class="sxs-lookup"><span data-stu-id="5835f-202">Output</span></span>    | <span data-ttu-id="5835f-203">Carga de áudio MPEG-1 audio packetMPEG-1</span><span class="sxs-lookup"><span data-stu-id="5835f-203">MPEG-1 Audio packetMPEG-1 Audio payload</span></span><br/> <span data-ttu-id="5835f-204">Pacote de vídeo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="5835f-204">MPEG-1 Video packet</span></span><br/> <span data-ttu-id="5835f-205">Carga de vídeo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="5835f-205">MPEG-1 Video payload</span></span><br/> |
| <span data-ttu-id="5835f-206">Codec de áudio de software</span><span class="sxs-lookup"><span data-stu-id="5835f-206">Software Audio Codec</span></span> | <span data-ttu-id="5835f-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="5835f-207">Input</span></span>     | <span data-ttu-id="5835f-208">Carga de áudio MPEG-1 audio packetMPEG-1</span><span class="sxs-lookup"><span data-stu-id="5835f-208">MPEG-1 Audio packetMPEG-1 Audio payload</span></span><br/>                                                                |
| <span data-ttu-id="5835f-209">Codec de vídeo de software</span><span class="sxs-lookup"><span data-stu-id="5835f-209">Software Video Codec</span></span> | <span data-ttu-id="5835f-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="5835f-210">Input</span></span>     | <span data-ttu-id="5835f-211">Carga de vídeo MPEG-1 Video packetMPEG-1</span><span class="sxs-lookup"><span data-stu-id="5835f-211">MPEG-1 Video packetMPEG-1 Video payload</span></span><br/>                                                                |
| <span data-ttu-id="5835f-212">Codec de áudio de software</span><span class="sxs-lookup"><span data-stu-id="5835f-212">Software Audio Codec</span></span> | <span data-ttu-id="5835f-213">Saída</span><span class="sxs-lookup"><span data-stu-id="5835f-213">Output</span></span>    | <span data-ttu-id="5835f-214">Áudio PCM</span><span class="sxs-lookup"><span data-stu-id="5835f-214">PCM audio</span></span>                                                                                                         |
| <span data-ttu-id="5835f-215">Codec de vídeo de software</span><span class="sxs-lookup"><span data-stu-id="5835f-215">Software Video Codec</span></span> | <span data-ttu-id="5835f-216">Saída</span><span class="sxs-lookup"><span data-stu-id="5835f-216">Output</span></span>    | <span data-ttu-id="5835f-217">Vídeo descompactado (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)</span><span class="sxs-lookup"><span data-stu-id="5835f-217">Uncompressed video (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)</span></span>                                    |



 

<span data-ttu-id="5835f-218">O pacote de vídeo MPEG-1 e os tipos de mídia de carga contêm um cabeçalho de sequência completo para que os dados possam ser reproduzidos do meio de um arquivo sem precisar de um cabeçalho de sequência para inicializar a reprodução do vídeo.</span><span class="sxs-lookup"><span data-stu-id="5835f-218">MPEG-1 Video packet and payload media types contain a complete sequence header so that data can be played from the middle of a file without needing a sequence header to initialize the video playback.</span></span>

<span data-ttu-id="5835f-219">O cabeçalho de sequência de vídeo é anexado ao tipo de dados vídeo para vídeo MPEG para que a reprodução possa começar do meio de um fluxo.</span><span class="sxs-lookup"><span data-stu-id="5835f-219">The video sequence header is appended to the video data type for MPEG video so that play can begin from the middle of a stream.</span></span> <span data-ttu-id="5835f-220">O comprimento deste campo é de até 140 bytes; Ele inclui o código de início do cabeçalho de sequência (0x000001B3) no início, juntamente com todas as matrizes de quantização encontradas no primeiro cabeçalho de sequência encontrado.</span><span class="sxs-lookup"><span data-stu-id="5835f-220">The length of this field is up to 140 bytes; it includes the sequence header start code (0x000001B3) at the start, along with any quantization matrices found in the first sequence header encountered.</span></span>

 

 




