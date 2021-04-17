---
description: 'Esse filtro decodifica os seguintes formatos de áudio:'
ms.assetid: 2fd14296-9eed-4e25-b140-6281c707fdb7
title: Decodificador de áudio do Microsoft MPEG-1/DD/AAC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a685fa2be32dd963cdc7de08ec716117e6a7016e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105779921"
---
# <a name="microsoft-mpeg-1ddaac-audio-decoder"></a><span data-ttu-id="3d2a5-103">Decodificador de áudio do Microsoft MPEG-1/DD/AAC</span><span class="sxs-lookup"><span data-stu-id="3d2a5-103">Microsoft MPEG-1/DD/AAC Audio Decoder</span></span>

<span data-ttu-id="3d2a5-104">Esse filtro decodifica os seguintes formatos de áudio:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-104">This filter decodes the following audio formats:</span></span>

-   <span data-ttu-id="3d2a5-105">Camadas de áudio MPEG-1 I e II.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-105">MPEG-1 audio layers I and II.</span></span>
-   <span data-ttu-id="3d2a5-106">Áudio MPEG-2 compatível com versões anteriores, camadas I e II (ISO/IEC 13818-3), mono e estéreo somente.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-106">Backward-compatible MPEG-2 audio, layers I and II (ISO/IEC 13818-3), mono and stereo only.</span></span>
-   <span data-ttu-id="3d2a5-107">Perfil de LC (codificação de áudio avançado) (AAC) de baixa complexidade.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-107">Advanced Audio Coding (AAC) Low Complexity (LC) profile.</span></span>
-   <span data-ttu-id="3d2a5-108">High-Efficiency AAC (HE-AAC) versão 1 e versão 2.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-108">High-Efficiency AAC (HE-AAC) version 1 and version 2.</span></span>
-   <span data-ttu-id="3d2a5-109">DTS (Digital Theater Systems) de passagem para saída digital.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-109">Pass-through Digital Theater Systems (DTS) for digital output.</span></span>
-   <span data-ttu-id="3d2a5-110">Somente LPCM, mono e estéreo, com ou sem cabeçalhos do PES.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-110">LPCM, mono and stereo only, with or without PES headers.</span></span>
-   <span data-ttu-id="3d2a5-111">Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-111">Dolby Digital.</span></span>
-   <span data-ttu-id="3d2a5-112">Dolby Digital Plus, incluindo conversão de Dolby Digital Plus para Dolby Digital para saída digital.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-112">Dolby Digital Plus, including conversion from Dolby Digital Plus to Dolby Digital for digital output.</span></span>

> [!Note]  
> <span data-ttu-id="3d2a5-113">A implementação da tecnologia Dolby Digital da Microsoft é restrita em termos do programa de licenciamento do Dolby Digital para uso pelos aplicativos da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-113">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

> [!Note]  
> <span data-ttu-id="3d2a5-114">Não há suporte para esse filtro em plataformas baseadas em IA-64.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-114">This filter is not supported on IA-64-based platforms.</span></span>

 

<span data-ttu-id="3d2a5-115">A decodificação dos formatos Dolby Digital Plus, AAC e HE-AAC requer o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-115">Decoding of Dolby Digital Plus, AAC, and HE-AAC formats requires Windows 7.</span></span> <span data-ttu-id="3d2a5-116">Não há suporte para a decodificação de Dolby Digital ou Dolby Digital Plus no Windows 7 Home Basic ou no Windows 7 Starter.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-116">Decoding of Dolby Digital or Dolby Digital Plus is not supported on Windows 7 Home Basic or Windows 7 Starter.</span></span>

<span data-ttu-id="3d2a5-117">No registro, o nome amigável desse filtro é "decodificador de áudio do Microsoft DTV-DVD".</span><span class="sxs-lookup"><span data-stu-id="3d2a5-117">In the registry, the friendly name of this filter is "Microsoft DTV-DVD Audio Decoder".</span></span>



<span data-ttu-id="3d2a5-118">Informações de filtro</span><span class="sxs-lookup"><span data-stu-id="3d2a5-118">Filter Information</span></span>

<span data-ttu-id="3d2a5-119">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="3d2a5-119">Filter Interfaces</span></span>

[<span data-ttu-id="3d2a5-120">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-120">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="3d2a5-121">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-121">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

<span data-ttu-id="3d2a5-122">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="3d2a5-122">Input Pin Media Types</span></span>

<span data-ttu-id="3d2a5-123">No Windows Vista e posterior, o filtro dá suporte aos seguintes tipos de entrada:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-123">In Windows Vista and later, the filter supports the following input types:</span></span><br/>

-   <span data-ttu-id="3d2a5-124">**MediaType \_ Áudio**, **MEDIASUBTYPE \_ Dolby \_ AC3** (veja a observação 1).</span><span class="sxs-lookup"><span data-stu-id="3d2a5-124">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="3d2a5-125">**MediaType \_ Áudio**, **MEDIASUBTYPE \_ MPEG1Audio**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-125">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1Audio**</span></span>
-   <span data-ttu-id="3d2a5-126">**MediaType \_ Áudio**, **MEDIASUBTYPE \_ MPEG1Payload**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-126">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1Payload**</span></span>
-   <span data-ttu-id="3d2a5-127">**MediaType \_ Áudio**, **\_ \_ áudio MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-127">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="3d2a5-128">**MediaType \_ DVD \_ ENCRYPTED \_ Pack**, **MEDIASUBTYPE \_ Dolby \_ AC3** (veja a observação 1).</span><span class="sxs-lookup"><span data-stu-id="3d2a5-128">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="3d2a5-129">**MediaType \_ \_ \_ Pacote de DVD criptografado**, **MEDIASUBTYPE \_ DTS** (consulte a observação 2.)</span><span class="sxs-lookup"><span data-stu-id="3d2a5-129">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DTS** (See Note 2.)</span></span>
-   <span data-ttu-id="3d2a5-130">**MediaType \_ DVD \_ ENCRYPTED \_ Pack**, **\_ \_ \_ áudio MEDIASUBTYPE DVD LPCM**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-130">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="3d2a5-131">**MediaType \_ DVD \_ ENCRYPTED \_ Pack**, **\_ \_ áudio MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-131">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="3d2a5-132">**MediaType \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ Dolby \_ AC3** (consulte a observação 1.)</span><span class="sxs-lookup"><span data-stu-id="3d2a5-132">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="3d2a5-133">**MediaType \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ DTS** (consulte a observação 2.)</span><span class="sxs-lookup"><span data-stu-id="3d2a5-133">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DTS** (See Note 2.)</span></span>
-   <span data-ttu-id="3d2a5-134">**MediaType \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-134">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="3d2a5-135">**MediaType \_ MPEG2 \_ PES**, **\_ \_ áudio MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-135">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="3d2a5-136">**MediaType \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ AC3** (consulte a observação 1.)</span><span class="sxs-lookup"><span data-stu-id="3d2a5-136">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="3d2a5-137">**MediaType \_ Stream**, **MEDIASUBTYPE \_ MPEG1Audio**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-137">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG1Audio**</span></span>
-   <span data-ttu-id="3d2a5-138">**MediaType \_ Fluxo**, **\_ \_ áudio MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-138">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>

<span data-ttu-id="3d2a5-139">A partir do Windows 7, o filtro também oferece suporte aos seguintes tipos de entrada:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-139">Starting in Windows 7, the filter also supports the following input types:</span></span><br/>

-   <span data-ttu-id="3d2a5-140">**MediaType \_ Áudio**, **MEDIASUBTYPE \_ Dolby \_ DDPLUS** (veja a observação 1).</span><span class="sxs-lookup"><span data-stu-id="3d2a5-140">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_DDPLUS** (See Note 1.)</span></span>
-   <span data-ttu-id="3d2a5-141">**MediaType \_ Áudio**, **MEDIASUBTYPE \_ DTS2** (consulte a observação 2.)</span><span class="sxs-lookup"><span data-stu-id="3d2a5-141">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DTS2** (See Note 2.)</span></span>
-   <span data-ttu-id="3d2a5-142">**MediaType \_ Áudio**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-142">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="3d2a5-143">**MediaType \_ Áudio**, **MEDIASUBTYPE \_ DVM** (consulte a observação 1).</span><span class="sxs-lookup"><span data-stu-id="3d2a5-143">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DVM** (See Note 1.)</span></span>
-   <span data-ttu-id="3d2a5-144">**MediaType \_ Áudio**, **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-144">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG\_ADTS\_AAC**</span></span>
-   <span data-ttu-id="3d2a5-145">**MediaType \_ Áudio**, **MEDIASUBTYPE \_ MPEG \_ loas**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-145">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG\_LOAS**</span></span>
-   <span data-ttu-id="3d2a5-146">**MediaType \_ Áudio**, **MEDIASUBTYPE \_ MPEG1AudioPayload**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-146">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1AudioPayload**</span></span>
-   <span data-ttu-id="3d2a5-147">**MediaType \_ Áudio**, **MEDIASUBTYPE \_ RAW \_ AAC1**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-147">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_RAW\_AAC1**</span></span>
-   <span data-ttu-id="3d2a5-148">**MediaType \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ DDPLUS** (consulte a observação 1.)</span><span class="sxs-lookup"><span data-stu-id="3d2a5-148">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_DDPLUS** (See Note 1.)</span></span>
-   <span data-ttu-id="3d2a5-149">**MediaType \_ Stream**, **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-149">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG\_ADTS\_AAC**</span></span>
-   <span data-ttu-id="3d2a5-150">**MediaType \_ Stream**, **MEDIASUBTYPE \_ MPEG \_ loas**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-150">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG\_LOAS**</span></span>

<span data-ttu-id="3d2a5-151">O tipo de entrada pode ser alterado dinamicamente durante o streaming.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-151">The input type can change dynamically during streaming.</span></span><br/> <span data-ttu-id="3d2a5-152">Para obter mais informações sobre esses tipos de mídia, consulte [**subtipos de áudio**](audio-subtypes.md).</span><span class="sxs-lookup"><span data-stu-id="3d2a5-152">For more information about these media types, see [**Audio Subtypes**](audio-subtypes.md).</span></span><br/>

> [!Note]  
> 1. <span data-ttu-id="3d2a5-153">A implementação da tecnologia Dolby Digital da Microsoft é restrita em termos do programa de licenciamento do Dolby Digital para uso pelos aplicativos da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-153">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

<br/>

> [!Note]  
> 2. <span data-ttu-id="3d2a5-154">Para a entrada de DTS (Digital Theater Systems), somente a saída de S/PDIF é suportada (DTS over S/PDIF).</span><span class="sxs-lookup"><span data-stu-id="3d2a5-154">For Digital Theater Systems (DTS) input, only S/PDIF output is supported (DTS over S/PDIF).</span></span> <span data-ttu-id="3d2a5-155">Não há suporte para a decodificação de áudio.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-155">Audio decoding is not supported.</span></span>

<br/>

<span data-ttu-id="3d2a5-156">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="3d2a5-156">Input Pin Interfaces</span></span>

[<span data-ttu-id="3d2a5-157">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-157">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [<span data-ttu-id="3d2a5-158">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-158">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="3d2a5-159">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-159">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="3d2a5-160">**IPin**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-160">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="3d2a5-161">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-161">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="3d2a5-162">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="3d2a5-162">Output Pin Media Types</span></span>

<span data-ttu-id="3d2a5-163">No Windows Vista e posterior, o filtro dá suporte aos seguintes tipos de saída:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-163">In Windows Vista and later, the filter supports the following output types:</span></span><br/>

-   <span data-ttu-id="3d2a5-164">**MediaType \_ Áudio**, **MEDIASUBTYPE \_ Dolby \_ AC3 \_ SPDIF** (igual ao **KSDATAFORMAT \_ subtipo \_ IEC61937 \_ Dolby \_ digital**)</span><span class="sxs-lookup"><span data-stu-id="3d2a5-164">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3\_SPDIF** (same as **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL**)</span></span>
-   <span data-ttu-id="3d2a5-165">**MediaType \_ Áudio**, **MEDIASUBTYPE \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-165">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span>

<span data-ttu-id="3d2a5-166">A partir do Windows 7, o filtro também oferece suporte aos seguintes tipos de saída:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-166">Starting in Windows 7, the filter also supports the following output types:</span></span><br/>

-   <span data-ttu-id="3d2a5-167">**MediaType \_ Áudio**, **KSDATAFORMAT \_ subtipo \_ IEC61937 \_ DTS**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-167">**MEDIATYPE\_Audio**, **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTS**</span></span>
-   <span data-ttu-id="3d2a5-168">**MediaType \_ Áudio**, **MEDIASUBTYPE \_ IEEE \_ float**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-168">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_IEEE\_FLOAT**</span></span>

<span data-ttu-id="3d2a5-169">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="3d2a5-169">Output Pin Interfaces</span></span>

[<span data-ttu-id="3d2a5-170">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-170">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="3d2a5-171">**IPin**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-171">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="3d2a5-172">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-172">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="3d2a5-173">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="3d2a5-173">Filter CLSID</span></span>

<span data-ttu-id="3d2a5-174">**CLSID \_ do CMPEG2AudDecoderDS** (declarado em wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="3d2a5-174">**CLSID\_CMPEG2AudDecoderDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="3d2a5-175">Executável</span><span class="sxs-lookup"><span data-stu-id="3d2a5-175">Executable</span></span>

<span data-ttu-id="3d2a5-176">msmpeg2adec.dll</span><span class="sxs-lookup"><span data-stu-id="3d2a5-176">msmpeg2adec.dll</span></span>

[<span data-ttu-id="3d2a5-177">Núcleo</span><span class="sxs-lookup"><span data-stu-id="3d2a5-177">Merit</span></span>](merit.md)

<span data-ttu-id="3d2a5-178">**Mérito \_ NORMAL** -1</span><span class="sxs-lookup"><span data-stu-id="3d2a5-178">**MERIT\_NORMAL** - 1</span></span>

[<span data-ttu-id="3d2a5-179">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="3d2a5-179">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="3d2a5-180">**\_LEGACYAMFILTERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-180">**CLSID\_LegacyAmFilterCategory**</span></span>



 

> [!Note]  
> <span data-ttu-id="3d2a5-181">Uma versão anterior da documentação declarava que esse filtro pode decodificar "áudio MPEG-2".</span><span class="sxs-lookup"><span data-stu-id="3d2a5-181">An earlier version of the documentation stated that this filter can decode "MPEG-2 audio."</span></span> <span data-ttu-id="3d2a5-182">O filtro decodifica apenas áudio MPEG-2 compatível com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-182">The filter decodes only backward-compatible MPEG-2 audio.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="3d2a5-183">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d2a5-183">Remarks</span></span>

<span data-ttu-id="3d2a5-184">Os fluxos mono sempre são decodificados para estéreo.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-184">Mono streams are always decoded to stereo.</span></span>

<span data-ttu-id="3d2a5-185">Para fluxos com uma configuração de canal de dois ou mais alto-falantes, o decodificador faz um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-185">For streams with a channel configuration of two or more speakers, the decoder does one of the following:</span></span>

-   <span data-ttu-id="3d2a5-186">Combina até seis canais, usando a configuração de alto-falante 5,1 comum.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-186">Up-mixes to six channels, using the common 5.1 speaker configuration.</span></span>
-   <span data-ttu-id="3d2a5-187">Downmixes para estéreo.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-187">Downmixes to stereo.</span></span>

<span data-ttu-id="3d2a5-188">Para selecionar entre essas duas opções, use a interface [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) para definir a propriedade [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) , antes de conectar os Pins.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-188">To select between these two options, use the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface to set the [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) property, before connecting the pins.</span></span> <span data-ttu-id="3d2a5-189">Como alternativa, quando o aplicativo cria o grafo de filtro, ele pode definir o tipo de mídia desejado no pino de saída.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-189">Alternatively, when the application builds the filter graph, it can set the desired media type on the output pin.</span></span>

### <a name="aac-decoding"></a><span data-ttu-id="3d2a5-190">Decodificação AAC</span><span class="sxs-lookup"><span data-stu-id="3d2a5-190">AAC Decoding</span></span>

<span data-ttu-id="3d2a5-191">Para o AAC, o decodificador tem determinadas restrições de formato na entrada AAC compactada.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-191">For AAC, the decoder has certain format constraints on the compressed AAC input.</span></span> <span data-ttu-id="3d2a5-192">Essas restrições de formato são as mesmas que o [**decodificador AAC**](../medfound/aac-decoder.md)Media Foundation e estão documentadas na seção "[**restrições de formato**](../medfound/aac-decoder.md)".</span><span class="sxs-lookup"><span data-stu-id="3d2a5-192">These format constraints are the same as the Media Foundation [**AAC Decoder**](../medfound/aac-decoder.md), and are documented in the section "[**Format Constraints**](../medfound/aac-decoder.md)".</span></span>

<span data-ttu-id="3d2a5-193">O decodificador do DirectShow também aceita tipos de entrada diferentes do decodificador de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-193">The DirectShow decoder also accepts different input types than the Media Foundation decoder.</span></span> <span data-ttu-id="3d2a5-194">O decodificador do DirectShow dá suporte aos seguintes tipos de entrada AAC:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-194">The DirectShow decoder supports the following AAC input types:</span></span>

-   <span data-ttu-id="3d2a5-195">**MEDIASUBTYPE \_ \_AAC1 bruto**: AAC bruto, normalmente encontrado em AVI ou Matroska (. MKV) arquivos.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-195">**MEDIASUBTYPE\_RAW\_AAC1**: Raw AAC, typically found in AVI or Matroska (.MKV) files.</span></span>
-   <span data-ttu-id="3d2a5-196">**MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**: AAC em um fluxo de transporte de dados de áudio (ADTS) para streaming.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-196">**MEDIASUBTYPE\_MPEG\_ADTS\_AAC**: AAC in an Audio Data Transport Stream (ADTS) for streaming.</span></span>
-   <span data-ttu-id="3d2a5-197">**MEDIASUBTYPE \_ MPEG \_ loas**: fluxo de transporte com uma camada de sincronização (loas) e uma camada de MULTIPLEX (LATM).</span><span class="sxs-lookup"><span data-stu-id="3d2a5-197">**MEDIASUBTYPE\_MPEG\_LOAS**: Transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span>

<span data-ttu-id="3d2a5-198">O decodificador Media Foundation dá suporte aos seguintes tipos de entrada AAC:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-198">The Media Foundation decoder supports the following AAC input types:</span></span>

-   <span data-ttu-id="3d2a5-199">MFAudioFormat \_ AAC (igual a **MEDIASUBTYPE \_ MPEG \_ HEAAC**) para reprodução de arquivo MP4.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-199">MFAudioFormat\_AAC (same as **MEDIASUBTYPE\_MPEG\_HEAAC**) for MP4 file playback.</span></span>
-   <span data-ttu-id="3d2a5-200">**MEDIASUBTYPE \_ \_AAC1 brutos**.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-200">**MEDIASUBTYPE\_RAW\_AAC1**.</span></span>

### <a name="property-sets"></a><span data-ttu-id="3d2a5-201">Conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="3d2a5-201">Property Sets</span></span>

<span data-ttu-id="3d2a5-202">O PIN de entrada do decodificador dá suporte aos seguintes conjuntos de propriedades por meio de [**IKsPropertySet**](ikspropertyset.md):</span><span class="sxs-lookup"><span data-stu-id="3d2a5-202">The decoder's input pin supports the following property sets through [**IKsPropertySet**](ikspropertyset.md):</span></span>

-   [<span data-ttu-id="3d2a5-203">**Conjunto de propriedades da proteção contra cópia de DVD**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-203">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   <span data-ttu-id="3d2a5-204">[**Taxa-alteração de propriedade definida**](rate-change-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="3d2a5-204">[**Rate-Change Property Set**](rate-change-property-set.md).</span></span>

> [!Note]  
> <span data-ttu-id="3d2a5-205">A partir do Windows 7, o decodificador dá suporte ao modo de truque por meio do conjunto de propriedades de alteração de taxa.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-205">Starting in Windows 7, the decoder supports trick mode through the rate-change property set.</span></span> <span data-ttu-id="3d2a5-206">Ele dá suporte a taxas de reprodução no intervalo de \[ 0,501 a 2,0 \] , em que 1,0 é taxa de reprodução normal e 2,0 é o dobro da taxa normal.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-206">It supports playback rates in the range \[0.501 – 2.0\], where 1.0 is normal playback rate, and 2.0 is twice the normal rate.</span></span>

 

### <a name="codec-properties"></a><span data-ttu-id="3d2a5-207">Propriedades do codec</span><span class="sxs-lookup"><span data-stu-id="3d2a5-207">Codec Properties</span></span>

<span data-ttu-id="3d2a5-208">O PIN de entrada do decodificador dá suporte às seguintes propriedades por meio de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="3d2a5-208">The decoder's input pin supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="3d2a5-209">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3d2a5-209">Property</span></span>                                                          | <span data-ttu-id="3d2a5-210">Exige</span><span class="sxs-lookup"><span data-stu-id="3d2a5-210">Requires</span></span>                                                 |
|-------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="3d2a5-211">**AVAudioChannelConfig**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-211">**AVAudioChannelConfig**</span></span>](avaudiochannelconfig-property.md)     | <span data-ttu-id="3d2a5-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d2a5-212">Windows Vista</span></span>                                            |
| [<span data-ttu-id="3d2a5-213">**AVAudioChannelCount**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-213">**AVAudioChannelCount**</span></span>](avaudiochannelcount-property.md)       | <span data-ttu-id="3d2a5-214">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d2a5-214">Windows Vista</span></span>                                            |
| [<span data-ttu-id="3d2a5-215">**AVAudioSampleRate**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-215">**AVAudioSampleRate**</span></span>](avaudiosamplerate-property.md)           | <span data-ttu-id="3d2a5-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d2a5-216">Windows Vista</span></span>                                            |
| [<span data-ttu-id="3d2a5-217">**AVDDSurroundMode**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-217">**AVDDSurroundMode**</span></span>](avddsurroundmode-property.md)             | <span data-ttu-id="3d2a5-218">Somente Windows Vista; sem suporte no Windows 7 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-218">Windows Vista only; not supported in Windows 7 or later.</span></span> |
| [<span data-ttu-id="3d2a5-219">**AVDecAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-219">**AVDecAudioDualMono**</span></span>](avdecaudiodualmono-property.md)         | <span data-ttu-id="3d2a5-220">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d2a5-220">Windows Vista</span></span>                                            |
| [<span data-ttu-id="3d2a5-221">**AVDecCommonInputFormat**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-221">**AVDecCommonInputFormat**</span></span>](avdeccommoninputformat-property.md) | <span data-ttu-id="3d2a5-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d2a5-222">Windows Vista</span></span>                                            |
| [<span data-ttu-id="3d2a5-223">**AVDecCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-223">**AVDecCommonMeanBitRate**</span></span>](avdeccommonmeanbitrate.md)          | <span data-ttu-id="3d2a5-224">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d2a5-224">Windows 7</span></span>                                                |



 

<span data-ttu-id="3d2a5-225">O filtro oferece suporte às seguintes propriedades por meio de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="3d2a5-225">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="3d2a5-226">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3d2a5-226">Property</span></span>                                                                          | <span data-ttu-id="3d2a5-227">Exige</span><span class="sxs-lookup"><span data-stu-id="3d2a5-227">Requires</span></span>      |
|-----------------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="3d2a5-228">**AVDecAACDownmixMode**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-228">**AVDecAACDownmixMode**</span></span>](avdecaacdownmixmode-property.md)                       | <span data-ttu-id="3d2a5-229">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d2a5-229">Windows 7</span></span>     |
| [<span data-ttu-id="3d2a5-230">**AVDecAudioDualMonoReproMode**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-230">**AVDecAudioDualMonoReproMode**</span></span>](avdecaudiodualmonorepromode-property.md)       | <span data-ttu-id="3d2a5-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d2a5-231">Windows Vista</span></span> |
| <span data-ttu-id="3d2a5-232">[**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (veja a observação 3.)</span><span class="sxs-lookup"><span data-stu-id="3d2a5-232">[**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (See Note 3.)</span></span> | <span data-ttu-id="3d2a5-233">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d2a5-233">Windows Vista</span></span> |
| [<span data-ttu-id="3d2a5-234">**AVDecDDDynamicRangeScaleHigh**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-234">**AVDecDDDynamicRangeScaleHigh**</span></span>](avdecdddynamicrangescalehigh-property.md)     | <span data-ttu-id="3d2a5-235">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d2a5-235">Windows Vista</span></span> |
| [<span data-ttu-id="3d2a5-236">**AVDecDDDynamicRangeScaleLow**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-236">**AVDecDDDynamicRangeScaleLow**</span></span>](avdecdddynamicrangescalelow-property.md)       | <span data-ttu-id="3d2a5-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d2a5-237">Windows Vista</span></span> |
| [<span data-ttu-id="3d2a5-238">**AVDecDDOperationalMode**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-238">**AVDecDDOperationalMode**</span></span>](avdecddoperationalmode-property.md)                 | <span data-ttu-id="3d2a5-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d2a5-239">Windows Vista</span></span> |
| [<span data-ttu-id="3d2a5-240">**AVDecMmcssClass**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-240">**AVDecMmcssClass**</span></span>](avdecmmcss-property.md)                                    | <span data-ttu-id="3d2a5-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d2a5-241">Windows Vista</span></span> |
| [<span data-ttu-id="3d2a5-242">**AVDSPLoudnessEqualization**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-242">**AVDSPLoudnessEqualization**</span></span>](avdsploudnessequalization-property.md)           | <span data-ttu-id="3d2a5-243">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d2a5-243">Windows 7</span></span>     |
| [<span data-ttu-id="3d2a5-244">**AVDSPSpeakerFill**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-244">**AVDSPSpeakerFill**</span></span>](avdspspeakerfill-property.md)                             | <span data-ttu-id="3d2a5-245">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d2a5-245">Windows 7</span></span>     |



 

> [!Note]  
> 3. <span data-ttu-id="3d2a5-246">A propriedade [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) deve ser definida antes do pino de saída do decodificador ser conectado.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-246">The [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) property must be set before the decoder's output pin is connected.</span></span> <span data-ttu-id="3d2a5-247">Caso contrário, a alteração não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-247">Otherwise, the change has no effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3d2a5-248">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d2a5-248">Requirements</span></span>



| <span data-ttu-id="3d2a5-249">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d2a5-249">Requirement</span></span> | <span data-ttu-id="3d2a5-250">Valor</span><span class="sxs-lookup"><span data-stu-id="3d2a5-250">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d2a5-251">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d2a5-251">Minimum supported client</span></span><br/> | <span data-ttu-id="3d2a5-252">Windows Vista Home Premium, Windows Vista Ultimate, aplicativos de área de trabalho do Windows 7 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="3d2a5-252">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3d2a5-253">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d2a5-253">Minimum supported server</span></span><br/> | <span data-ttu-id="3d2a5-254">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3d2a5-254">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3d2a5-255">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3d2a5-255">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d2a5-256"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d2a5-256"><dt>Wmcodecdsp.h</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="3d2a5-257">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d2a5-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d2a5-258">**Subtipos de áudio**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-258">**Audio Subtypes**</span></span>](audio-subtypes.md)
</dt> <dt>

[<span data-ttu-id="3d2a5-259">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="3d2a5-259">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="3d2a5-260">**Tipos de mídia de DVD**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-260">**DVD Media Types**</span></span>](dvd-media-types.md)
</dt> </dl>

 

 
