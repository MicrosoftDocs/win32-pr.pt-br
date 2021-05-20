---
description: Esta seção descreve o suporte Media Foundation para arquivos MKV (Contêiner de Mídia Matroska).
title: Suporte ao MKV (Contêiner de Mídia matroska)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdd860f58087bc8a0f3fe95d278bfa81edc412d0
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2021
ms.locfileid: "110154208"
---
# <a name="matroska-media-container-mkv-support"></a><span data-ttu-id="1131d-103">Suporte ao MKV (Contêiner de Mídia matroska)</span><span class="sxs-lookup"><span data-stu-id="1131d-103">Matroska Media Container (MKV) support</span></span>

<span data-ttu-id="1131d-104">Esta seção descreve o suporte Media Foundation para arquivos MKV (Contêiner de Mídia Matroska).</span><span class="sxs-lookup"><span data-stu-id="1131d-104">This section describes the Media Foundation support for Matroska Media Container (MKV) files.</span></span>

<span data-ttu-id="1131d-105">O formato MKV pode dar suporte a vários codecs de áudio e vídeo, como H.264 e áudio AAC.</span><span class="sxs-lookup"><span data-stu-id="1131d-105">The MKV format can support multiple video and audio codecs, such as H.264 and AAC audio.</span></span> <span data-ttu-id="1131d-106">Em geral, os contêineres descrevem como os dados de áudio e vídeo são colocados e quais informações complementares são usadas para descrever esses fluxos A/V.</span><span class="sxs-lookup"><span data-stu-id="1131d-106">In general, containers describe how video and audio data is laid out and what supplementary information is used to describe those A/V streams.</span></span> <span data-ttu-id="1131d-107">Os contêineres também podem incluir dados que complementam fluxos A/V, como o título, idiomas dos fluxos de áudio, faixas de legenda ou legenda, fontes para esses subtítulos, imagens, informações de capítulo e menus.</span><span class="sxs-lookup"><span data-stu-id="1131d-107">Containers can also include data that complements A/V streams, such as the title, languages of the audio streams, subtitle or caption tracks, fonts for those subtitles, images, chapter information, and menus.</span></span> <span data-ttu-id="1131d-108">O MKV é um formato altamente flexível que dá suporte a muitos desses recursos de contêiner.</span><span class="sxs-lookup"><span data-stu-id="1131d-108">MKV is a highly flexible format that supports many of these container features.</span></span> <span data-ttu-id="1131d-109">Para obter mais informações sobre o formato MKV, consulte [https://matroska.org](https://matroska.org/)</span><span class="sxs-lookup"><span data-stu-id="1131d-109">For more info about the MKV format, see [https://matroska.org](https://matroska.org/)</span></span>


## <a name="mkv-container-feature-support"></a><span data-ttu-id="1131d-110">Suporte ao recurso de contêiner MKV</span><span class="sxs-lookup"><span data-stu-id="1131d-110">MKV container feature support</span></span>
<span data-ttu-id="1131d-111">Os recursos de contêiner MKV têm suporte no Media Foundation das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="1131d-111">MKV container features are supported on the by Media Foundation in the following ways:</span></span>
- <span data-ttu-id="1131d-112">Se uma ou mais faixas de vídeo estão presentes, a primeira faixa será tocada.</span><span class="sxs-lookup"><span data-stu-id="1131d-112">If one or more video tracks are present, the first track will be played.</span></span>
- <span data-ttu-id="1131d-113">Se uma ou mais faixas de áudio estão presentes, a primeira faixa será tocada.</span><span class="sxs-lookup"><span data-stu-id="1131d-113">If one or more audio tracks are present, the first track will be played.</span></span>
- <span data-ttu-id="1131d-114">Há suporte para faixas de legenda, mas não são selecionadas (tocadas) por padrão.</span><span class="sxs-lookup"><span data-stu-id="1131d-114">Caption tracks are supported, but are not selected (played) by default.</span></span>
- <span data-ttu-id="1131d-115">Se uma ou mais fontes ou imagens estão presentes, legendas e imagens não serão renderizar, embora o arquivo seja carregado e reproduzindo.</span><span class="sxs-lookup"><span data-stu-id="1131d-115">If one or more fonts or images are present, captions and images won’t render, although the file will load and play.</span></span>
- <span data-ttu-id="1131d-116">Não há suporte para informações de menu e não serão exibidas, mas o arquivo será carregado e reproduzirá.</span><span class="sxs-lookup"><span data-stu-id="1131d-116">Menu information is not supported and won’t be displayed, but the file will load and play.</span></span>
- <span data-ttu-id="1131d-117">Se os arquivos com capítulos se referirem a arquivos complementares, os arquivos complementares não reproduzirão.</span><span class="sxs-lookup"><span data-stu-id="1131d-117">If files with chapters refer to supplemental files, the supplemental files won’t play.</span></span>
- <span data-ttu-id="1131d-118">As imagens em miniatura estão disponíveis ao navegar por arquivos em unidades USB usando o navegador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="1131d-118">Thumbnail images are available when browsing for files on USB drives using the file browser.</span></span>

<span data-ttu-id="1131d-119">Esse conjunto de recursos deve permitir a reprodução da maioria dos arquivos MKV se eles contêm codecs com suporte.</span><span class="sxs-lookup"><span data-stu-id="1131d-119">This set of features should allow playback of most MKV files if they contain supported codecs.</span></span>
<span data-ttu-id="1131d-120">Há suporte para arquivos MKV que contêm faixas de áudio e vídeo codificadas com os codecs listados na seção a seguir.</span><span class="sxs-lookup"><span data-stu-id="1131d-120">MKV files that contain video and audio tracks encoded with the codecs listed in the following section are supported.</span></span>

## <a name="supported-mkv-codecs"></a><span data-ttu-id="1131d-121">Codecs MKV com suporte</span><span class="sxs-lookup"><span data-stu-id="1131d-121">Supported MKV codecs</span></span>

### <a name="video-codec-support-for-mkv"></a><span data-ttu-id="1131d-122">Suporte a codec de vídeo para MKV</span><span class="sxs-lookup"><span data-stu-id="1131d-122">Video codec support for MKV</span></span>

<span data-ttu-id="1131d-123">ID do Matroska: V_MPEG4/ISO/AVC</span><span class="sxs-lookup"><span data-stu-id="1131d-123">Matroska ID: V_MPEG4/ISO/AVC</span></span>

- <span data-ttu-id="1131d-124">MF_MT_SUBTYPE de Media Foundation MSFT: MFVideoFormat_H264</span><span class="sxs-lookup"><span data-stu-id="1131d-124">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_H264</span></span>
- <span data-ttu-id="1131d-125">Descrição: vídeo H. 264</span><span class="sxs-lookup"><span data-stu-id="1131d-125">Description: H.264 video</span></span>
- <span data-ttu-id="1131d-126">Identificadores FourCC ou WAV: H264</span><span class="sxs-lookup"><span data-stu-id="1131d-126">FourCC or WAV identifiers: H264</span></span>

<span data-ttu-id="1131d-127">ID do Matroska: V_MPEG2</span><span class="sxs-lookup"><span data-stu-id="1131d-127">Matroska ID: V_MPEG2</span></span>

- <span data-ttu-id="1131d-128">MF_MT_SUBTYPE de Media Foundation MSFT: MFVideoFormat_MPEG2</span><span class="sxs-lookup"><span data-stu-id="1131d-128">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPEG2</span></span>
- <span data-ttu-id="1131d-129">Descrição: vídeo MPEG-2</span><span class="sxs-lookup"><span data-stu-id="1131d-129">Description: MPEG-2 video</span></span>

<span data-ttu-id="1131d-130">ID do Matroska: V_MPEG1</span><span class="sxs-lookup"><span data-stu-id="1131d-130">Matroska ID: V_MPEG1</span></span>

- <span data-ttu-id="1131d-131">MF_MT_SUBTYPE de Media Foundation MSFT: MFVideoFormat_MPG1</span><span class="sxs-lookup"><span data-stu-id="1131d-131">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPG1</span></span>
- <span data-ttu-id="1131d-132">Descrição: vídeo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="1131d-132">Description: MPEG-1 video</span></span>
- <span data-ttu-id="1131d-133">Identificadores FourCC ou WAV: MPG1</span><span class="sxs-lookup"><span data-stu-id="1131d-133">FourCC or WAV identifiers: MPG1</span></span>

<span data-ttu-id="1131d-134">ID do Matroska: V_MPEG4/MS/V3</span><span class="sxs-lookup"><span data-stu-id="1131d-134">Matroska ID: V_MPEG4/MS/V3</span></span>

- <span data-ttu-id="1131d-135">MF_MT_SUBTYPE de Media Foundation MSFT: MFVideoFormat_MP43</span><span class="sxs-lookup"><span data-stu-id="1131d-135">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP43</span></span>
- <span data-ttu-id="1131d-136">Descrição: Microsoft MPEG 4 codec versão 3</span><span class="sxs-lookup"><span data-stu-id="1131d-136">Description: Microsoft MPEG 4 codec version 3</span></span>
- <span data-ttu-id="1131d-137">Identificadores FourCC ou WAV: MP43</span><span class="sxs-lookup"><span data-stu-id="1131d-137">FourCC or WAV identifiers: MP43</span></span>

<span data-ttu-id="1131d-138">ID do Matroska: V_MPEG4/ISO/ASP</span><span class="sxs-lookup"><span data-stu-id="1131d-138">Matroska ID: V_MPEG4/ISO/ASP</span></span>

- <span data-ttu-id="1131d-139">MF_MT_SUBTYPE de Media Foundation MSFT: MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="1131d-139">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="1131d-140">Descrição: vídeo MPEG-4 parte 2</span><span class="sxs-lookup"><span data-stu-id="1131d-140">Description: MPEG-4 part 2 video</span></span>
- <span data-ttu-id="1131d-141">Identificadores FourCC ou WAV: MP4V</span><span class="sxs-lookup"><span data-stu-id="1131d-141">FourCC or WAV identifiers: MP4V</span></span>

<span data-ttu-id="1131d-142">ID do Matroska: V_MS/VFW/FOURCC</span><span class="sxs-lookup"><span data-stu-id="1131d-142">Matroska ID: V_MS/VFW/FOURCC</span></span>

- <span data-ttu-id="1131d-143">Descrição: mapeia para vários codecs geralmente com suporte no formato AVI que estão disponíveis no console.</span><span class="sxs-lookup"><span data-stu-id="1131d-143">Description: Maps to several codecs usually supported in the AVI format that are available on the console.</span></span>

<span data-ttu-id="1131d-144">ID do Matroska: V_THEORA</span><span class="sxs-lookup"><span data-stu-id="1131d-144">Matroska ID: V_THEORA</span></span>

- <span data-ttu-id="1131d-145">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_Theora</span><span class="sxs-lookup"><span data-stu-id="1131d-145">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_Theora</span></span>
- <span data-ttu-id="1131d-146">Descrição: Theora</span><span class="sxs-lookup"><span data-stu-id="1131d-146">Description: Theora</span></span>
- <span data-ttu-id="1131d-147">Identificadores FourCC ou WAV: theo</span><span class="sxs-lookup"><span data-stu-id="1131d-147">FourCC or WAV identifiers: theo</span></span>

<span data-ttu-id="1131d-148">ID do Matroska: V_MPEG4/ISO/SP</span><span class="sxs-lookup"><span data-stu-id="1131d-148">Matroska ID: V_MPEG4/ISO/SP</span></span>

- <span data-ttu-id="1131d-149">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="1131d-149">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="1131d-150">Descrição: Perfil simples ISO MPEG4 (DivX4)</span><span class="sxs-lookup"><span data-stu-id="1131d-150">Description: MPEG4 ISO simple profile (DivX4)</span></span>
- <span data-ttu-id="1131d-151">Identificadores FourCC ou WAV: MP4V</span><span class="sxs-lookup"><span data-stu-id="1131d-151">FourCC or WAV identifiers: MP4V</span></span>

<span data-ttu-id="1131d-152">ID do Matroska: V_MPEG4/ISO/AP</span><span class="sxs-lookup"><span data-stu-id="1131d-152">Matroska ID: V_MPEG4/ISO/AP</span></span>

- <span data-ttu-id="1131d-153">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="1131d-153">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="1131d-154">Descrição: perfil simples avançado DO ISO MPEG4 (DivX5,Fild, FFMPEG)</span><span class="sxs-lookup"><span data-stu-id="1131d-154">Description: MPEG4 ISO advanced simple profile (DivX5, XviD, FFMPEG)</span></span>
- <span data-ttu-id="1131d-155">Identificadores FourCC ou WAV: MP4V</span><span class="sxs-lookup"><span data-stu-id="1131d-155">FourCC or WAV identifiers: MP4V</span></span>


<span data-ttu-id="1131d-156">ID do Matroska: V_MPEGH/ISO/HEVC</span><span class="sxs-lookup"><span data-stu-id="1131d-156">Matroska ID: V_MPEGH/ISO/HEVC</span></span> 

- <span data-ttu-id="1131d-157">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_HEVC</span><span class="sxs-lookup"><span data-stu-id="1131d-157">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_HEVC</span></span>
- <span data-ttu-id="1131d-158">Descrição: HEVC/H.265</span><span class="sxs-lookup"><span data-stu-id="1131d-158">Description: HEVC/H.265</span></span>
- <span data-ttu-id="1131d-159">Identificadores FourCC ou WAV:</span><span class="sxs-lookup"><span data-stu-id="1131d-159">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="1131d-160">ID do Matroska: V_VP8</span><span class="sxs-lookup"><span data-stu-id="1131d-160">Matroska ID: V_VP8</span></span>

- <span data-ttu-id="1131d-161">MF_MT_SUBTYPE de Media Foundation MSFT: MFVideoFormat_VP80</span><span class="sxs-lookup"><span data-stu-id="1131d-161">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP80</span></span>
- <span data-ttu-id="1131d-162">Descrição: formato de codec VP8</span><span class="sxs-lookup"><span data-stu-id="1131d-162">Description: VP8 Codec format</span></span>
- <span data-ttu-id="1131d-163">Identificadores FourCC ou WAV: VP80</span><span class="sxs-lookup"><span data-stu-id="1131d-163">FourCC or WAV identifiers: VP80</span></span>

<span data-ttu-id="1131d-164">ID do Matroska: V_VP9</span><span class="sxs-lookup"><span data-stu-id="1131d-164">Matroska ID: V_VP9</span></span>

- <span data-ttu-id="1131d-165">MF_MT_SUBTYPE de Media Foundation MSFT: MFVideoFormat_VP90</span><span class="sxs-lookup"><span data-stu-id="1131d-165">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP90</span></span>
- <span data-ttu-id="1131d-166">Descrição: formato de codec VP9</span><span class="sxs-lookup"><span data-stu-id="1131d-166">Description: VP9 Codec format</span></span>
- <span data-ttu-id="1131d-167">Identificadores FourCC ou WAV: VP90</span><span class="sxs-lookup"><span data-stu-id="1131d-167">FourCC or WAV identifiers: VP90</span></span>

<span data-ttu-id="1131d-168">ID do Matroska: V_MJPEG</span><span class="sxs-lookup"><span data-stu-id="1131d-168">Matroska ID: V_MJPEG</span></span>

- <span data-ttu-id="1131d-169">MF_MT_SUBTYPE de Media Foundation MSFT: MFVideoFormat_MJPG</span><span class="sxs-lookup"><span data-stu-id="1131d-169">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MJPG</span></span>
- <span data-ttu-id="1131d-170">Descrição: animação JPEG</span><span class="sxs-lookup"><span data-stu-id="1131d-170">Description: Motion JPEG</span></span>
- <span data-ttu-id="1131d-171">Identificadores FourCC ou WAV: MJPG</span><span class="sxs-lookup"><span data-stu-id="1131d-171">FourCC or WAV identifiers: MJPG</span></span>

<span data-ttu-id="1131d-172">ID do Matroska: V_AV1</span><span class="sxs-lookup"><span data-stu-id="1131d-172">Matroska ID: V_AV1</span></span>

- <span data-ttu-id="1131d-173">MF_MT_SUBTYPE de Media Foundation MSFT: MFVideoFormat_AV1</span><span class="sxs-lookup"><span data-stu-id="1131d-173">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_AV1</span></span>
- <span data-ttu-id="1131d-174">Descrição: vídeo AOMedia 1</span><span class="sxs-lookup"><span data-stu-id="1131d-174">Description: AOMedia Video 1</span></span>
- <span data-ttu-id="1131d-175">Identificadores FourCC ou WAV: AV01</span><span class="sxs-lookup"><span data-stu-id="1131d-175">FourCC or WAV identifiers: AV01</span></span>

### <a name="audio-codec-support-for-mkv"></a><span data-ttu-id="1131d-176">Suporte a codec de áudio para MKV</span><span class="sxs-lookup"><span data-stu-id="1131d-176">Audio codec support for MKV</span></span>

<span data-ttu-id="1131d-177">ID do Matroska: A_AAC</span><span class="sxs-lookup"><span data-stu-id="1131d-177">Matroska ID: A_AAC</span></span>

- <span data-ttu-id="1131d-178">MF_MT_SUBTYPE de Media Foundation MSFT: MFAudioFormat_AAC</span><span class="sxs-lookup"><span data-stu-id="1131d-178">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span></span>
- <span data-ttu-id="1131d-179">Descrição: AAC (codificação de áudio avançada)</span><span class="sxs-lookup"><span data-stu-id="1131d-179">Description: Advanced Audio Coding (AAC)</span></span>
- <span data-ttu-id="1131d-180">Identificadores FourCC ou WAV: WAVE_FORMAT_MPEG_HEAAC</span><span class="sxs-lookup"><span data-stu-id="1131d-180">FourCC or WAV identifiers: WAVE_FORMAT_MPEG_HEAAC</span></span>

<span data-ttu-id="1131d-181">ID do Matroska: A_AC3</span><span class="sxs-lookup"><span data-stu-id="1131d-181">Matroska ID: A_AC3</span></span>

- <span data-ttu-id="1131d-182">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_AC3</span><span class="sxs-lookup"><span data-stu-id="1131d-182">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_AC3</span></span>
- <span data-ttu-id="1131d-183">Descrição: Dolby AC3</span><span class="sxs-lookup"><span data-stu-id="1131d-183">Description: Dolby AC3</span></span>
- <span data-ttu-id="1131d-184">Identificadores FourCC ou WAV: WAVE_FORMAT_DOLBY_AC3_SPDIF</span><span class="sxs-lookup"><span data-stu-id="1131d-184">FourCC or WAV identifiers: WAVE_FORMAT_DOLBY_AC3_SPDIF</span></span>

<span data-ttu-id="1131d-185">ID do Matroska: A_MPEG/L3</span><span class="sxs-lookup"><span data-stu-id="1131d-185">Matroska ID: A_MPEG/L3</span></span>

- <span data-ttu-id="1131d-186">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MP3</span><span class="sxs-lookup"><span data-stu-id="1131d-186">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MP3</span></span>
- <span data-ttu-id="1131d-187">Descrição: MPEG Audio Layer-3 (MP3)</span><span class="sxs-lookup"><span data-stu-id="1131d-187">Description: MPEG Audio Layer-3 (MP3)</span></span>
- <span data-ttu-id="1131d-188">Identificadores FourCC ou WAV: WAVE_FORMAT_MPEGLAYER3</span><span class="sxs-lookup"><span data-stu-id="1131d-188">FourCC or WAV identifiers: WAVE_FORMAT_MPEGLAYER3</span></span>

<span data-ttu-id="1131d-189">ID do Matroska: A_MPEG/L1</span><span class="sxs-lookup"><span data-stu-id="1131d-189">Matroska ID: A_MPEG/L1</span></span>

- <span data-ttu-id="1131d-190">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span><span class="sxs-lookup"><span data-stu-id="1131d-190">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span></span>
- <span data-ttu-id="1131d-191">Descrição: conteúdo de áudio MPEG-1</span><span class="sxs-lookup"><span data-stu-id="1131d-191">Description: MPEG-1 audio payload</span></span>
- <span data-ttu-id="1131d-192">Identificadores FourCC ou WAV: WAVE_FORMAT_MPEG</span><span class="sxs-lookup"><span data-stu-id="1131d-192">FourCC or WAV identifiers: WAVE_FORMAT_MPEG</span></span>

<span data-ttu-id="1131d-193">ID do Matroska: A_PCM/INT/BIG</span><span class="sxs-lookup"><span data-stu-id="1131d-193">Matroska ID: A_PCM/INT/BIG</span></span>

- <span data-ttu-id="1131d-194">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span><span class="sxs-lookup"><span data-stu-id="1131d-194">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span></span>
- <span data-ttu-id="1131d-195">Descrição: áudio PCM descompactado</span><span class="sxs-lookup"><span data-stu-id="1131d-195">Description: Uncompressed PCM audio</span></span>
- <span data-ttu-id="1131d-196">Identificadores FourCC ou WAV: WAVE_FORMAT_PCM</span><span class="sxs-lookup"><span data-stu-id="1131d-196">FourCC or WAV identifiers: WAVE_FORMAT_PCM</span></span>

<span data-ttu-id="1131d-197">ID do Matroska: A_PCM/INT/LIT</span><span class="sxs-lookup"><span data-stu-id="1131d-197">Matroska ID: A_PCM/INT/LIT</span></span>

- <span data-ttu-id="1131d-198">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span><span class="sxs-lookup"><span data-stu-id="1131d-198">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span></span>
- <span data-ttu-id="1131d-199">Descrição: áudio PCM descompactado</span><span class="sxs-lookup"><span data-stu-id="1131d-199">Description: Uncompressed PCM audio</span></span>
- <span data-ttu-id="1131d-200">Identificadores FourCC ou WAV: WAVE_FORMAT_PCM</span><span class="sxs-lookup"><span data-stu-id="1131d-200">FourCC or WAV identifiers: WAVE_FORMAT_PCM</span></span>

<span data-ttu-id="1131d-201">ID do Matroska: A_PCM/FLOAT/IEEE</span><span class="sxs-lookup"><span data-stu-id="1131d-201">Matroska ID: A_PCM/FLOAT/IEEE</span></span>

- <span data-ttu-id="1131d-202">MF_MT_SUBTYPE de Media Foundation MSFT: MFAudioFormat_Float</span><span class="sxs-lookup"><span data-stu-id="1131d-202">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Float</span></span>
- <span data-ttu-id="1131d-203">Descrição: áudio de ponto flutuante de IEEE não compactado</span><span class="sxs-lookup"><span data-stu-id="1131d-203">Description: Uncompressed IEEE floating-point audio</span></span>
- <span data-ttu-id="1131d-204">Identificadores FourCC ou WAV: WAVE_FORMAT_IEEE_FLOAT</span><span class="sxs-lookup"><span data-stu-id="1131d-204">FourCC or WAV identifiers: WAVE_FORMAT_IEEE_FLOAT</span></span>

<span data-ttu-id="1131d-205">ID do Matroska: A_ALAC</span><span class="sxs-lookup"><span data-stu-id="1131d-205">Matroska ID: A_ALAC</span></span>

- <span data-ttu-id="1131d-206">MF_MT_SUBTYPE de Media Foundation MSFT: MFAudioFormat_ALAC</span><span class="sxs-lookup"><span data-stu-id="1131d-206">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_ALAC</span></span>
- <span data-ttu-id="1131d-207">Descrição: codec de áudio do Apple Lossless</span><span class="sxs-lookup"><span data-stu-id="1131d-207">Description: Apple Lossless Audio Codec</span></span>
- <span data-ttu-id="1131d-208">Identificadores FourCC ou WAV:</span><span class="sxs-lookup"><span data-stu-id="1131d-208">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="1131d-209">ID do Matroska: A_MPEG/L2</span><span class="sxs-lookup"><span data-stu-id="1131d-209">Matroska ID: A_MPEG/L2</span></span>

- <span data-ttu-id="1131d-210">MF_MT_SUBTYPE de Media Foundation MSFT: MFAudioFormat_MPEG</span><span class="sxs-lookup"><span data-stu-id="1131d-210">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span></span>
- <span data-ttu-id="1131d-211">Descrição: áudio MPEG 1, 2 camada II</span><span class="sxs-lookup"><span data-stu-id="1131d-211">Description: MPEG Audio 1, 2 Layer II</span></span>
- <span data-ttu-id="1131d-212">Identificadores FourCC ou WAV: WAVE_FORMAT_MPEG</span><span class="sxs-lookup"><span data-stu-id="1131d-212">FourCC or WAV identifiers: WAVE_FORMAT_MPEG</span></span>

<span data-ttu-id="1131d-213">ID do Matroska: A_DTS</span><span class="sxs-lookup"><span data-stu-id="1131d-213">Matroska ID: A_DTS</span></span>

- <span data-ttu-id="1131d-214">MF_MT_SUBTYPE de Media Foundation MSFT: MEDIASUBTYPE_DTS_HD</span><span class="sxs-lookup"><span data-stu-id="1131d-214">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DTS_HD</span></span>
- <span data-ttu-id="1131d-215">Descrição: sistema de teatro digital</span><span class="sxs-lookup"><span data-stu-id="1131d-215">Description: Digital Theatre System</span></span>
- <span data-ttu-id="1131d-216">Identificadores FourCC ou WAV: WAVE_FORMAT_DTS</span><span class="sxs-lookup"><span data-stu-id="1131d-216">FourCC or WAV identifiers: WAVE_FORMAT_DTS</span></span>

<span data-ttu-id="1131d-217">ID do Matroska: A_OPUS</span><span class="sxs-lookup"><span data-stu-id="1131d-217">Matroska ID: A_OPUS</span></span>

- <span data-ttu-id="1131d-218">MF_MT_SUBTYPE de Media Foundation MSFT: MFAudioFormat_Opus</span><span class="sxs-lookup"><span data-stu-id="1131d-218">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Opus</span></span>
- <span data-ttu-id="1131d-219">Descrição: Opus</span><span class="sxs-lookup"><span data-stu-id="1131d-219">Description: Opus</span></span>
- <span data-ttu-id="1131d-220">Identificadores FourCC ou WAV: WAVE_FORMAT_OPUS</span><span class="sxs-lookup"><span data-stu-id="1131d-220">FourCC or WAV identifiers: WAVE_FORMAT_OPUS</span></span>

<span data-ttu-id="1131d-221">ID do Matroska: A_VORBIS</span><span class="sxs-lookup"><span data-stu-id="1131d-221">Matroska ID: A_VORBIS</span></span>

- <span data-ttu-id="1131d-222">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Vorbis</span><span class="sxs-lookup"><span data-stu-id="1131d-222">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Vorbis</span></span>
- <span data-ttu-id="1131d-223">Descrição: Vorbis</span><span class="sxs-lookup"><span data-stu-id="1131d-223">Description: Vorbis</span></span>
- <span data-ttu-id="1131d-224">Identificadores FourCC ou WAV:</span><span class="sxs-lookup"><span data-stu-id="1131d-224">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="1131d-225">ID do Matroska: A_FLAC</span><span class="sxs-lookup"><span data-stu-id="1131d-225">Matroska ID: A_FLAC</span></span>

- <span data-ttu-id="1131d-226">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_FLAC</span><span class="sxs-lookup"><span data-stu-id="1131d-226">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_FLAC</span></span>
- <span data-ttu-id="1131d-227">Descrição: Codec de áudio sem perda gratuita</span><span class="sxs-lookup"><span data-stu-id="1131d-227">Description: Free Lossless Audio Codec</span></span>
- <span data-ttu-id="1131d-228">Identificadores FourCC ou WAV: WAVE_FORMAT_FLAC</span><span class="sxs-lookup"><span data-stu-id="1131d-228">FourCC or WAV identifiers: WAVE_FORMAT_FLAC</span></span>

<span data-ttu-id="1131d-229">ID do Matroska: A_AAC/MAIN</span><span class="sxs-lookup"><span data-stu-id="1131d-229">Matroska ID: A_AAC/MAIN</span></span>

- <span data-ttu-id="1131d-230">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span><span class="sxs-lookup"><span data-stu-id="1131d-230">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span></span>
- <span data-ttu-id="1131d-231">Descrição: Codificação de Áudio Avançada (AAC)</span><span class="sxs-lookup"><span data-stu-id="1131d-231">Description: Advanced Audio Coding (AAC)</span></span>
- <span data-ttu-id="1131d-232">Identificadores FourCC ou WAV: WAVE_FORMAT_MPEG_HEAAC</span><span class="sxs-lookup"><span data-stu-id="1131d-232">FourCC or WAV identifiers: WAVE_FORMAT_MPEG_HEAAC</span></span>

<span data-ttu-id="1131d-233">ID do Matroska: A_EAC3</span><span class="sxs-lookup"><span data-stu-id="1131d-233">Matroska ID: A_EAC3</span></span>

- <span data-ttu-id="1131d-234">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_DDPlus</span><span class="sxs-lookup"><span data-stu-id="1131d-234">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_DDPlus</span></span>
- <span data-ttu-id="1131d-235">Descrição: AC-3 aprimorado</span><span class="sxs-lookup"><span data-stu-id="1131d-235">Description: Enhanced AC-3</span></span>
- <span data-ttu-id="1131d-236">Identificadores FourCC ou WAV:</span><span class="sxs-lookup"><span data-stu-id="1131d-236">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="1131d-237">ID do Matroska: A_TRUEHD</span><span class="sxs-lookup"><span data-stu-id="1131d-237">Matroska ID: A_TRUEHD</span></span>

- <span data-ttu-id="1131d-238">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DOLBY_TRUEHD</span><span class="sxs-lookup"><span data-stu-id="1131d-238">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DOLBY_TRUEHD</span></span>
- <span data-ttu-id="1131d-239">Descrição: Dolby TrueHD</span><span class="sxs-lookup"><span data-stu-id="1131d-239">Description: Dolby TrueHD</span></span>
- <span data-ttu-id="1131d-240">Identificadores FourCC ou WAV:</span><span class="sxs-lookup"><span data-stu-id="1131d-240">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="1131d-241">ID do Matroska: A_MS/ACM</span><span class="sxs-lookup"><span data-stu-id="1131d-241">Matroska ID: A_MS/ACM</span></span>

- <span data-ttu-id="1131d-242">MF_MT_SUBTYPE de Media Foundation MSFT: mapeia para vários tipos de WAVE_FORMAT de áudio definidos em Mmreg. h</span><span class="sxs-lookup"><span data-stu-id="1131d-242">MSFT Media Foundation MF_MT_SUBTYPE: Maps to several WAVE_FORMAT audio types defined in mmreg.h</span></span>


### <a name="subtitles-codec-support-for-mkv"></a><span data-ttu-id="1131d-243">Suporte ao codec de legendas para MKV</span><span class="sxs-lookup"><span data-stu-id="1131d-243">Subtitles codec support for MKV</span></span>

<span data-ttu-id="1131d-244">ID do Matroska: S_TEXT/ASCII</span><span class="sxs-lookup"><span data-stu-id="1131d-244">Matroska ID: S_TEXT/ASCII</span></span>

- <span data-ttu-id="1131d-245">MF_MT_SUBTYPE de Media Foundation MSFT: MFSubtitleFormat_SRT</span><span class="sxs-lookup"><span data-stu-id="1131d-245">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span></span>
- <span data-ttu-id="1131d-246">Descrição: texto ASCII</span><span class="sxs-lookup"><span data-stu-id="1131d-246">Description: ASCII text</span></span>

<span data-ttu-id="1131d-247">ID do Matroska: S_TEXT/UTF8</span><span class="sxs-lookup"><span data-stu-id="1131d-247">Matroska ID: S_TEXT/UTF8</span></span>

- <span data-ttu-id="1131d-248">MF_MT_SUBTYPE de Media Foundation MSFT: MFSubtitleFormat_SRT</span><span class="sxs-lookup"><span data-stu-id="1131d-248">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span></span>
- <span data-ttu-id="1131d-249">Descrição: texto sem formatação UTF-8</span><span class="sxs-lookup"><span data-stu-id="1131d-249">Description: UTF-8 Plain Text</span></span>

<span data-ttu-id="1131d-250">ID do Matroska: S_TEXT/SSA</span><span class="sxs-lookup"><span data-stu-id="1131d-250">Matroska ID: S_TEXT/SSA</span></span>

- <span data-ttu-id="1131d-251">MF_MT_SUBTYPE de Media Foundation MSFT: MFSubtitleFormat_SSA</span><span class="sxs-lookup"><span data-stu-id="1131d-251">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span></span>
- <span data-ttu-id="1131d-252">Descrição: formato de legenda</span><span class="sxs-lookup"><span data-stu-id="1131d-252">Description: Subtitles Format</span></span>

<span data-ttu-id="1131d-253">ID do Matroska: S_TEXT/ASS</span><span class="sxs-lookup"><span data-stu-id="1131d-253">Matroska ID: S_TEXT/ASS</span></span>

- <span data-ttu-id="1131d-254">MF_MT_SUBTYPE de Media Foundation MSFT: MFSubtitleFormat_SSA</span><span class="sxs-lookup"><span data-stu-id="1131d-254">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span></span>
- <span data-ttu-id="1131d-255">Descrição: formato de legendas avançadas</span><span class="sxs-lookup"><span data-stu-id="1131d-255">Description: Advanced Subtitles Format</span></span>

<span data-ttu-id="1131d-256">ID do Matroska: S_VOBSUB</span><span class="sxs-lookup"><span data-stu-id="1131d-256">Matroska ID: S_VOBSUB</span></span>

- <span data-ttu-id="1131d-257">MF_MT_SUBTYPE de Media Foundation MSFT: MFSubtitleFormat_VobSub</span><span class="sxs-lookup"><span data-stu-id="1131d-257">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_VobSub</span></span>
- <span data-ttu-id="1131d-258">Descrição: VobSub legendas</span><span class="sxs-lookup"><span data-stu-id="1131d-258">Description: VobSub subtitles</span></span>

<span data-ttu-id="1131d-259">ID do Matroska: S_HDMV/PGS</span><span class="sxs-lookup"><span data-stu-id="1131d-259">Matroska ID: S_HDMV/PGS</span></span>

- <span data-ttu-id="1131d-260">MF_MT_SUBTYPE de Media Foundation MSFT: MFSubtitleFormat_PGS</span><span class="sxs-lookup"><span data-stu-id="1131d-260">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_PGS</span></span>
- <span data-ttu-id="1131d-261">Descrição: subtítulos de gráficos de apresentação do HDMV (PGS)</span><span class="sxs-lookup"><span data-stu-id="1131d-261">Description: HDMV presentation graphics subtitles (PGS)</span></span>


## <a name="technical-details-regarding-codecs"></a><span data-ttu-id="1131d-262">Detalhes técnicos sobre codecs</span><span class="sxs-lookup"><span data-stu-id="1131d-262">Technical details regarding codecs</span></span>

<span data-ttu-id="1131d-263">Consulte o seguinte para obter detalhes técnicos sobre codecs.</span><span class="sxs-lookup"><span data-stu-id="1131d-263">See the following for technical details regarding codecs.</span></span>

- [<span data-ttu-id="1131d-264">Especificações do Codec matroska</span><span class="sxs-lookup"><span data-stu-id="1131d-264">Matroska Codec Specs</span></span>](http://www.matroska.org/technical/specs/codecid/index.html)
- [<span data-ttu-id="1131d-265">GUIDs de subtipo de áudio</span><span class="sxs-lookup"><span data-stu-id="1131d-265">Audio Subtype GUIDs</span></span>](audio-subtype-guids.md)
- [<span data-ttu-id="1131d-266">GUIDs de subtipo de vídeo</span><span class="sxs-lookup"><span data-stu-id="1131d-266">Video Subtype GUIDs</span></span>](video-subtype-guids.md)


## <a name="related-topics"></a><span data-ttu-id="1131d-267">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1131d-267">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1131d-268">Formatos de mídia compatíveis com o Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1131d-268">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="1131d-269">Guia Media Foundation programação do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1131d-269">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 



