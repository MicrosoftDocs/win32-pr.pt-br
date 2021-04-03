---
description: Esta seção descreve os aplicativos de exemplo que demonstram como usar os tópicos Media Foundation. Encoding SamplesPlayback SamplesPlug-InsSource Reader SamplesVideo CaptureMiscellaneous SamplesDeprecated ou obsoletos SamplesRelated
ms.assetid: 9d460107-ec12-4df5-a7a9-d19943685599
title: Exemplos de SDK do Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f335b5ba744b098efdb7570aa861ad36fc9216cf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103663795"
---
# <a name="media-foundation-sdk-samples"></a><span data-ttu-id="f410f-103">Exemplos de SDK do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f410f-103">Media Foundation SDK Samples</span></span>

<span data-ttu-id="f410f-104">Esta seção descreve os aplicativos de exemplo que demonstram como usar Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f410f-104">This section describes sample applications that demonstrate how to use Media Foundation.</span></span>

-   [<span data-ttu-id="f410f-105">Exemplos de codificação</span><span class="sxs-lookup"><span data-stu-id="f410f-105">Encoding Samples</span></span>](#encoding-samples)
-   [<span data-ttu-id="f410f-106">Exemplos de reprodução</span><span class="sxs-lookup"><span data-stu-id="f410f-106">Playback Samples</span></span>](#playback-samples)
-   [<span data-ttu-id="f410f-107">Plug-ins</span><span class="sxs-lookup"><span data-stu-id="f410f-107">Plug-Ins</span></span>](#plug-ins)
-   [<span data-ttu-id="f410f-108">Amostras do leitor de origem</span><span class="sxs-lookup"><span data-stu-id="f410f-108">Source Reader Samples</span></span>](#source-reader-samples)
-   [<span data-ttu-id="f410f-109">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="f410f-109">Video Capture</span></span>](#video-capture)
-   [<span data-ttu-id="f410f-110">Exemplos diversos</span><span class="sxs-lookup"><span data-stu-id="f410f-110">Miscellaneous Samples</span></span>](#miscellaneous-samples)
-   [<span data-ttu-id="f410f-111">Amostras preteridas ou obsoletas</span><span class="sxs-lookup"><span data-stu-id="f410f-111">Deprecated or Obsolete Samples</span></span>](#deprecated-or-obsolete-samples)
-   [<span data-ttu-id="f410f-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f410f-112">Related topics</span></span>](#related-topics)

## <a name="encoding-samples"></a><span data-ttu-id="f410f-113">Exemplos de codificação</span><span class="sxs-lookup"><span data-stu-id="f410f-113">Encoding Samples</span></span>



| <span data-ttu-id="f410f-114">Amostra</span><span class="sxs-lookup"><span data-stu-id="f410f-114">Sample</span></span>                            | <span data-ttu-id="f410f-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f410f-115">Description</span></span>                                                 |
|-----------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="f410f-116">Codificação</span><span class="sxs-lookup"><span data-stu-id="f410f-116">Transcode</span></span>](transcode-sample.md) | <span data-ttu-id="f410f-117">Mostra como recodificar um arquivo de mídia para o formato de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="f410f-117">Shows how to reencode a media file to Windows Media format.</span></span> |



 

## <a name="playback-samples"></a><span data-ttu-id="f410f-118">Exemplos de reprodução</span><span class="sxs-lookup"><span data-stu-id="f410f-118">Playback Samples</span></span>



| <span data-ttu-id="f410f-119">Amostra</span><span class="sxs-lookup"><span data-stu-id="f410f-119">Sample</span></span>                                            | <span data-ttu-id="f410f-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="f410f-120">Description</span></span>                                                                                                                                                                                                     |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f410f-121">[BasicPlayback](/previous-versions//bb970475(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f410f-121">[BasicPlayback](/previous-versions//bb970475(v=vs.85))</span></span>          | <span data-ttu-id="f410f-122">Reproduz arquivos de áudio e vídeo usando a [sessão de mídia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="f410f-122">Plays audio and video files by using the [Media Session](media-session.md).</span></span> <span data-ttu-id="f410f-123">Este exemplo demonstra como criar topologias de reprodução, controlar a sessão de mídia e receber eventos de sessão durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="f410f-123">This sample demonstrates how to create playback topologies, control the Media Session, and receive session events during playback.</span></span> |
| <span data-ttu-id="f410f-124">[MFPlayer](/previous-versions//bb970516(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f410f-124">[MFPlayer](/previous-versions//bb970516(v=vs.85))</span></span>                    | <span data-ttu-id="f410f-125">Demonstra algumas funções de reprodução que não estão incluídas no exemplo [BasicPlayback](/previous-versions//bb970475(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f410f-125">Demonstrates some playback functions that are not included in the [BasicPlayback](/previous-versions//bb970475(v=vs.85)) sample.</span></span>                                                                                              |
| [<span data-ttu-id="f410f-126">ProtectedPlayback</span><span class="sxs-lookup"><span data-stu-id="f410f-126">ProtectedPlayback</span></span>](protectedplayback-sample.md) | <span data-ttu-id="f410f-127">Reproduz arquivos de áudio e vídeo protegidos.</span><span class="sxs-lookup"><span data-stu-id="f410f-127">Plays protected audio and video files.</span></span> <span data-ttu-id="f410f-128">Este exemplo mostra como usar a sessão do caminho de mídia protegida (PMP) e como usar objetos de habilitação de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="f410f-128">This sample shows how to use the protected media path (PMP) session and how to use content enabler objects.</span></span>                                                              |



 

## <a name="plug-ins"></a><span data-ttu-id="f410f-129">Plug-Ins</span><span class="sxs-lookup"><span data-stu-id="f410f-129">Plug-Ins</span></span>



| <span data-ttu-id="f410f-130">Amostra</span><span class="sxs-lookup"><span data-stu-id="f410f-130">Sample</span></span>                                       | <span data-ttu-id="f410f-131">Sub-Area</span><span class="sxs-lookup"><span data-stu-id="f410f-131">Sub-Area</span></span>                         | <span data-ttu-id="f410f-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="f410f-132">Description</span></span>                                                                                            |
|----------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f410f-133">Decodificador</span><span class="sxs-lookup"><span data-stu-id="f410f-133">Decoder</span></span>](decoder-sample.md)                | <span data-ttu-id="f410f-134">Media Foundation transformação (MFT)</span><span class="sxs-lookup"><span data-stu-id="f410f-134">Media Foundation transform (MFT)</span></span> | <span data-ttu-id="f410f-135">Decodificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f410f-135">Video decoder.</span></span>                                                                                         |
| [<span data-ttu-id="f410f-136">EVRPresenter</span><span class="sxs-lookup"><span data-stu-id="f410f-136">EVRPresenter</span></span>](evrpresenter-sample.md)      | <span data-ttu-id="f410f-137">Diversos</span><span class="sxs-lookup"><span data-stu-id="f410f-137">Miscellaneous</span></span>                    | <span data-ttu-id="f410f-138">Apresentador personalizado para o [processador de vídeo avançado](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="f410f-138">Custom presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span>                 |
| [<span data-ttu-id="f410f-139">\_AUDIODELAY MFT</span><span class="sxs-lookup"><span data-stu-id="f410f-139">MFT\_AudioDelay</span></span>](mft-audiodelay-sample.md) | <span data-ttu-id="f410f-140">MFT</span><span class="sxs-lookup"><span data-stu-id="f410f-140">MFT</span></span>                              | <span data-ttu-id="f410f-141">Transformação de efeito de áudio.</span><span class="sxs-lookup"><span data-stu-id="f410f-141">Audio effect transform.</span></span> <span data-ttu-id="f410f-142">Mostra como gravar um MFT básico para processamento de áudio.</span><span class="sxs-lookup"><span data-stu-id="f410f-142">Shows how to write a basic MFT for audio processing.</span></span>                           |
| [<span data-ttu-id="f410f-143">Escala de cinza da MFT \_</span><span class="sxs-lookup"><span data-stu-id="f410f-143">MFT\_Grayscale</span></span>](mft-grayscale-sample.md)   | <span data-ttu-id="f410f-144">MFT</span><span class="sxs-lookup"><span data-stu-id="f410f-144">MFT</span></span>                              | <span data-ttu-id="f410f-145">Efeito de vídeo em escala de cinza.</span><span class="sxs-lookup"><span data-stu-id="f410f-145">Grayscale video effect.</span></span> <span data-ttu-id="f410f-146">Mostra como gravar um MFT básico para processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f410f-146">Shows how to write a basic MFT for video processing.</span></span>                           |
| [<span data-ttu-id="f410f-147">MPEG1Source</span><span class="sxs-lookup"><span data-stu-id="f410f-147">MPEG1Source</span></span>](mpeg1source-sample.md)        | <span data-ttu-id="f410f-148">Origem da mídia</span><span class="sxs-lookup"><span data-stu-id="f410f-148">Media source</span></span>                     | <span data-ttu-id="f410f-149">Analisa os fluxos de camada de sistemas MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="f410f-149">Parses MPEG-1 systems-layer streams.</span></span> <span data-ttu-id="f410f-150">Mostra como gravar uma fonte de mídia personalizada e um manipulador de fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="f410f-150">Shows how to write a custom media source and byte-stream handler.</span></span> |
| [<span data-ttu-id="f410f-151">WavSink</span><span class="sxs-lookup"><span data-stu-id="f410f-151">WavSink</span></span>](wavsink-sample.md)                | <span data-ttu-id="f410f-152">Coletor de mídia</span><span class="sxs-lookup"><span data-stu-id="f410f-152">Media sink</span></span>                       | <span data-ttu-id="f410f-153">Um coletor de arquivo que grava arquivos. wav.</span><span class="sxs-lookup"><span data-stu-id="f410f-153">An archive sink that writes .wav files.</span></span> <span data-ttu-id="f410f-154">Mostra como gravar um coletor de mídia personalizado.</span><span class="sxs-lookup"><span data-stu-id="f410f-154">Shows how to write a custom media sink.</span></span>                        |
| [<span data-ttu-id="f410f-155">WavSource</span><span class="sxs-lookup"><span data-stu-id="f410f-155">WavSource</span></span>](wavsource-sample.md)            | <span data-ttu-id="f410f-156">Origem da mídia</span><span class="sxs-lookup"><span data-stu-id="f410f-156">Media source</span></span>                     | <span data-ttu-id="f410f-157">Analisa arquivos. wav.</span><span class="sxs-lookup"><span data-stu-id="f410f-157">Parses .wav files.</span></span> <span data-ttu-id="f410f-158">Mostra como gravar uma fonte de mídia personalizada e um manipulador de fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="f410f-158">Shows how to write a custom media source and byte-stream handler.</span></span>                   |



 

## <a name="source-reader-samples"></a><span data-ttu-id="f410f-159">Amostras do leitor de origem</span><span class="sxs-lookup"><span data-stu-id="f410f-159">Source Reader Samples</span></span>



| <span data-ttu-id="f410f-160">Amostra</span><span class="sxs-lookup"><span data-stu-id="f410f-160">Sample</span></span>                                      | <span data-ttu-id="f410f-161">Descrição</span><span class="sxs-lookup"><span data-stu-id="f410f-161">Description</span></span>                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="f410f-162">Clipe de áudio</span><span class="sxs-lookup"><span data-stu-id="f410f-162">Audio Clip</span></span>](audio-clip-sample.md)         | <span data-ttu-id="f410f-163">Usa o [leitor de origem](source-reader.md) para decodificar áudio de um arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="f410f-163">Uses the [Source Reader](source-reader.md) to decode audio from a media file.</span></span>      |
| [<span data-ttu-id="f410f-164">VideoThumbnail</span><span class="sxs-lookup"><span data-stu-id="f410f-164">VideoThumbnail</span></span>](videothumbnail-sample.md) | <span data-ttu-id="f410f-165">Usa o [leitor de origem](source-reader.md) para obter quadros únicos de um arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f410f-165">Uses the [Source Reader](source-reader.md) to get single frames from a video file.</span></span> |



 

## <a name="video-capture"></a><span data-ttu-id="f410f-166">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="f410f-166">Video Capture</span></span>



| <span data-ttu-id="f410f-167">Amostra</span><span class="sxs-lookup"><span data-stu-id="f410f-167">Sample</span></span>                                        | <span data-ttu-id="f410f-168">Descrição</span><span class="sxs-lookup"><span data-stu-id="f410f-168">Description</span></span>                                                                                 |
|-----------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f410f-169">MFCaptureD3D</span><span class="sxs-lookup"><span data-stu-id="f410f-169">MFCaptureD3D</span></span>](mfcaptured3d-sample.md)       | <span data-ttu-id="f410f-170">Mostra como visualizar o vídeo de um dispositivo de captura de vídeo, usando o Direct3D para renderizar o vídeo.</span><span class="sxs-lookup"><span data-stu-id="f410f-170">Shows how to preview video from a video capture device, using Direct3D to render the video.</span></span> |
| [<span data-ttu-id="f410f-171">MFCaptureToFile</span><span class="sxs-lookup"><span data-stu-id="f410f-171">MFCaptureToFile</span></span>](mfcapturetofile-sample.md) | <span data-ttu-id="f410f-172">Mostra como capturar vídeo de uma câmera de vídeo para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f410f-172">Shows how to capture video from a video camera to a file.</span></span>                                   |



 

## <a name="miscellaneous-samples"></a><span data-ttu-id="f410f-173">Exemplos diversos</span><span class="sxs-lookup"><span data-stu-id="f410f-173">Miscellaneous Samples</span></span>



| <span data-ttu-id="f410f-174">Amostra</span><span class="sxs-lookup"><span data-stu-id="f410f-174">Sample</span></span>                                         | <span data-ttu-id="f410f-175">Descrição</span><span class="sxs-lookup"><span data-stu-id="f410f-175">Description</span></span>                                                                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f410f-176">ASFParser</span><span class="sxs-lookup"><span data-stu-id="f410f-176">ASFParser</span></span>](asfparser-sample.md)              | <span data-ttu-id="f410f-177">Mostra como analisar dados de um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="f410f-177">Shows how to parse data from an Advanced Systems Format (ASF) file.</span></span>                                                                                   |
| [<span data-ttu-id="f410f-178">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="f410f-178">DXVA-HD</span></span>](dxva-hd-sample.md)                  | <span data-ttu-id="f410f-179">Mostra como usar o Microsoft DirectX vídeo Acceleration High Definition (DXVA-HD).</span><span class="sxs-lookup"><span data-stu-id="f410f-179">Shows how to use Microsoft DirectX Video Acceleration High Definition (DXVA-HD).</span></span>                                                                      |
| [<span data-ttu-id="f410f-180">DXVA2 \_ VideoProc</span><span class="sxs-lookup"><span data-stu-id="f410f-180">DXVA2\_VideoProc</span></span>](dxva2-videoproc-sample.md) | <span data-ttu-id="f410f-181">Usa a DXVA (DirectX Video Acceleration) 2,0 para criar um fluxo de vídeo YUV de 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="f410f-181">Uses DirectX Video Acceleration (DXVA) 2.0 to create a stream of 4:2:2 YUV video.</span></span> <span data-ttu-id="f410f-182">Este exemplo mostra como usar os recursos de processamento de vídeo do DXVA.</span><span class="sxs-lookup"><span data-stu-id="f410f-182">This sample shows how to use the video processing features of DXVA.</span></span> |



 

## <a name="deprecated-or-obsolete-samples"></a><span data-ttu-id="f410f-183">Amostras preteridas ou obsoletas</span><span class="sxs-lookup"><span data-stu-id="f410f-183">Deprecated or Obsolete Samples</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f410f-184">Amostra</span><span class="sxs-lookup"><span data-stu-id="f410f-184">Sample</span></span></th>
<th><span data-ttu-id="f410f-185">Descrição</span><span class="sxs-lookup"><span data-stu-id="f410f-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f410f-186"><a href="mfplayer2-sample.md">MFPlayer2</a></span><span class="sxs-lookup"><span data-stu-id="f410f-186"><a href="mfplayer2-sample.md">MFPlayer2</a></span></span></td>
<td><span data-ttu-id="f410f-187">Demonstra alguns recursos avançados de reprodução da API do <a href="using-mfplay-for-audio-video-playback.md">MFPlay</a> .</span><span class="sxs-lookup"><span data-stu-id="f410f-187">Demonstrates some advanced playback features of the <a href="using-mfplay-for-audio-video-playback.md">MFPlay</a> API.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f410f-188"><a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a></span><span class="sxs-lookup"><span data-stu-id="f410f-188"><a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a></span></span></td>
<td><span data-ttu-id="f410f-189">Aplica um efeito de escala de cinza ao vídeo.</span><span class="sxs-lookup"><span data-stu-id="f410f-189">Applies a grayscale effect to video.</span></span> <span data-ttu-id="f410f-190">Mostra como inserir MFTs em uma topologia de reprodução.</span><span class="sxs-lookup"><span data-stu-id="f410f-190">Shows how to insert MFTs into a playback topology.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f410f-191">Este exemplo não está mais incluído no SDK.</span><span class="sxs-lookup"><span data-stu-id="f410f-191">This sample is no longer included in the SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f410f-192"><a href="playlist-sample.md">7.1</a></span><span class="sxs-lookup"><span data-stu-id="f410f-192"><a href="playlist-sample.md">Playlist</a></span></span></td>
<td><span data-ttu-id="f410f-193">Reproduz uma sequência de arquivos de áudio usando a origem do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="f410f-193">Plays a sequence of audio files using the sequencer source.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f410f-194">Este exemplo não está mais incluído no SDK.</span><span class="sxs-lookup"><span data-stu-id="f410f-194">This sample is no longer included in the SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f410f-195"><a href="simplecapture-sample.md">SimpleCapture</a></span><span class="sxs-lookup"><span data-stu-id="f410f-195"><a href="simplecapture-sample.md">SimpleCapture</a></span></span></td>
<td><span data-ttu-id="f410f-196">Mostra como visualizar o vídeo de um dispositivo de captura de vídeo usando a API MFPlay.</span><span class="sxs-lookup"><span data-stu-id="f410f-196">Shows how to preview video from a video capture device, using the MFPlay API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f410f-197"><a href="simpleplay-sample.md">SimplePlay</a></span><span class="sxs-lookup"><span data-stu-id="f410f-197"><a href="simpleplay-sample.md">SimplePlay</a></span></span></td>
<td><span data-ttu-id="f410f-198">Mostra como reproduzir um arquivo de mídia usando a API MFPlay.</span><span class="sxs-lookup"><span data-stu-id="f410f-198">Shows how to play a media file using the MFPlay API.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f410f-199">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f410f-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f410f-200">Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f410f-200">Microsoft Media Foundation</span></span>](microsoft-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="f410f-201">Sobre o Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f410f-201">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 
