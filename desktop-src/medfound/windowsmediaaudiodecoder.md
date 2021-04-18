---
description: O decodificador de áudio do Windows Media decodifica os fluxos de áudio que foram codificados pelo codificador de áudio do Windows Media.
ms.assetid: 2d8e4a97-34a7-4eee-9567-7ae98fa282b9
title: Decodificador de áudio do Windows Media (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70f11242f237b8d9709baea6d445a8426236913c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781374"
---
# <a name="windows-media-audio-decoder"></a><span data-ttu-id="b6d51-103">Decodificador de áudio do Windows Media</span><span class="sxs-lookup"><span data-stu-id="b6d51-103">Windows Media Audio Decoder</span></span>

<span data-ttu-id="b6d51-104">O decodificador de áudio do Windows Media decodifica os fluxos de áudio que foram codificados pelo [**codificador de áudio do Windows Media**](windowsmediaaudioencoder.md).</span><span class="sxs-lookup"><span data-stu-id="b6d51-104">The Windows Media Audio decoder decodes audio streams that were encoded by the [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md).</span></span> <span data-ttu-id="b6d51-105">O codificador e o decodificador dão suporte a três categorias de áudio codificado: Windows Media Audio Standard, Windows Media Audio Professional e Windows Media Audio Lossless.</span><span class="sxs-lookup"><span data-stu-id="b6d51-105">The encoder and decoder support three categories of encoded audio: Windows Media Audio Standard, Windows Media Audio Professional, and Windows Media Audio Lossless.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="b6d51-106">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="b6d51-106">Class Identifier</span></span>

<span data-ttu-id="b6d51-107">O CLSID (identificador de classe) para o decodificador de áudio do Windows Media é representado pela constante **CLSID \_ CWMADecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="b6d51-107">The class identifier (CLSID) for the Windows Media Audio decoder is represented by the constant **CLSID\_CWMADecMediaObject**.</span></span> <span data-ttu-id="b6d51-108">Você pode criar uma instância do decodificador de áudio chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="b6d51-108">You can create an instance of the audio decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="b6d51-109">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="b6d51-109">Input Formats</span></span>

<span data-ttu-id="b6d51-110">A tabela a seguir mostra as marcas de formato de áudio que representam as categorias de entrada com suporte pelo decodificador de áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b6d51-110">The following table shows the audio format tags that represent the input categories supported by the Windows Media Audio decoder.</span></span> <span data-ttu-id="b6d51-111">Para obter informações sobre como definir os tipos de entrada e saída para o decodificador, consulte [Configurando a decodificação de áudio](configuringaudiodecoding.md).</span><span class="sxs-lookup"><span data-stu-id="b6d51-111">For information about how to set the input and output types for the decoder, see [Configuring Audio Decoding](configuringaudiodecoding.md).</span></span>



| <span data-ttu-id="b6d51-112">Formatar constante de marca</span><span class="sxs-lookup"><span data-stu-id="b6d51-112">Format tag constant</span></span>             | <span data-ttu-id="b6d51-113">Formatar valor da marca</span><span class="sxs-lookup"><span data-stu-id="b6d51-113">Format tag value</span></span> | <span data-ttu-id="b6d51-114">Formato de áudio</span><span class="sxs-lookup"><span data-stu-id="b6d51-114">Audio format</span></span>                     |
|---------------------------------|------------------|----------------------------------|
| <span data-ttu-id="b6d51-115">\_WMAUDIO2 de formato Wave \_</span><span class="sxs-lookup"><span data-stu-id="b6d51-115">WAVE\_FORMAT\_WMAUDIO2</span></span>          | <span data-ttu-id="b6d51-116">0x0161</span><span class="sxs-lookup"><span data-stu-id="b6d51-116">0x0161</span></span>           | <span data-ttu-id="b6d51-117">Padrão de áudio do Windows Media</span><span class="sxs-lookup"><span data-stu-id="b6d51-117">Windows Media Audio Standard</span></span>     |
| <span data-ttu-id="b6d51-118">\_WMAUDIO3 de formato Wave \_</span><span class="sxs-lookup"><span data-stu-id="b6d51-118">WAVE\_FORMAT\_WMAUDIO3</span></span>          | <span data-ttu-id="b6d51-119">0x0162</span><span class="sxs-lookup"><span data-stu-id="b6d51-119">0x0162</span></span>           | <span data-ttu-id="b6d51-120">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="b6d51-120">Windows Media Audio Professional</span></span> |
| <span data-ttu-id="b6d51-121">\_formato Wave \_ WMAUDIO \_ Lossless</span><span class="sxs-lookup"><span data-stu-id="b6d51-121">WAVE\_FORMAT\_WMAUDIO\_LOSSLESS</span></span> | <span data-ttu-id="b6d51-122">0x0163</span><span class="sxs-lookup"><span data-stu-id="b6d51-122">0x0163</span></span>           | <span data-ttu-id="b6d51-123">Windows Media Audio sem perdas</span><span class="sxs-lookup"><span data-stu-id="b6d51-123">Windows Media Audio Lossless</span></span>     |



 

## <a name="output-formats"></a><span data-ttu-id="b6d51-124">Formatos de saída</span><span class="sxs-lookup"><span data-stu-id="b6d51-124">Output Formats</span></span>

<span data-ttu-id="b6d51-125">A tabela a seguir mostra as marcas de formato de áudio que representam os tipos de saída com suporte pelo **decodificador de áudio do Windows Media**.</span><span class="sxs-lookup"><span data-stu-id="b6d51-125">The following table shows the audio format tags that represent the output types supported by the **Windows Media Audio Decoder**.</span></span> <span data-ttu-id="b6d51-126">Para obter informações sobre como definir os tipos de entrada e saída para o decodificador, consulte [Configurando a codificação de áudio](configuringaudioencoding.md).</span><span class="sxs-lookup"><span data-stu-id="b6d51-126">For information about how to set the input and output types for the decoder, see [Configuring Audio Encoding](configuringaudioencoding.md).</span></span>



| <span data-ttu-id="b6d51-127">Formatar constante de marca</span><span class="sxs-lookup"><span data-stu-id="b6d51-127">Format tag constant</span></span>       | <span data-ttu-id="b6d51-128">Formatar valor da marca</span><span class="sxs-lookup"><span data-stu-id="b6d51-128">Format tag value</span></span> | <span data-ttu-id="b6d51-129">Formato de áudio</span><span class="sxs-lookup"><span data-stu-id="b6d51-129">Audio format</span></span>                                          |
|---------------------------|------------------|-------------------------------------------------------|
| <span data-ttu-id="b6d51-130">\_PCM de formato Wave \_</span><span class="sxs-lookup"><span data-stu-id="b6d51-130">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="b6d51-131">0x0001</span><span class="sxs-lookup"><span data-stu-id="b6d51-131">0x0001</span></span>           | <span data-ttu-id="b6d51-132">Formato PCM</span><span class="sxs-lookup"><span data-stu-id="b6d51-132">PCM format</span></span>                                            |
| <span data-ttu-id="b6d51-133">\_formato Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="b6d51-133">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="b6d51-134">0x0003</span><span class="sxs-lookup"><span data-stu-id="b6d51-134">0x0003</span></span>           | <span data-ttu-id="b6d51-135">Ponto flutuante IEEE</span><span class="sxs-lookup"><span data-stu-id="b6d51-135">IEEE floating point</span></span>                                   |
| <span data-ttu-id="b6d51-136">\_formato Wave \_ extensível</span><span class="sxs-lookup"><span data-stu-id="b6d51-136">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="b6d51-137">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="b6d51-137">0xFFFE</span></span>           | <span data-ttu-id="b6d51-138">Formato PCM/IEEE na estrutura **WAVEFORMATEXTENSIBLE**</span><span class="sxs-lookup"><span data-stu-id="b6d51-138">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="b6d51-139">Interfaces</span><span class="sxs-lookup"><span data-stu-id="b6d51-139">Interfaces</span></span>

<span data-ttu-id="b6d51-140">Um objeto decodificador de áudio expõe a interface **IMediaObject** para que o objeto possa ser usado como um objeto de mídia do DirectX (DMO) e expõe a interface **IMFTransform** para que o objeto possa ser usado como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="b6d51-140">An audio decoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="b6d51-141">Um decodificador de áudio do Windows Media se comporta como DMO ou MFT dependendo de quais interfaces você obtém e qual versão do Windows está em execução.</span><span class="sxs-lookup"><span data-stu-id="b6d51-141">A Windows Media Audio decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="b6d51-142">A tabela a seguir mostra as condições sob as quais um decodificador de áudio se comporta como um DMO ou um MFT.</span><span class="sxs-lookup"><span data-stu-id="b6d51-142">The following table shows the conditions under which an audio decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="b6d51-143">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="b6d51-143">Operating system</span></span> | <span data-ttu-id="b6d51-144">Comportamento do decodificador</span><span class="sxs-lookup"><span data-stu-id="b6d51-144">Decoder behavior</span></span>                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6d51-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b6d51-145">Windows XP</span></span>       | <span data-ttu-id="b6d51-146">Um decodificador de áudio do Windows Media sempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="b6d51-146">A Windows Media Audio decoder always behaves as a DMO.</span></span>                                                                                                                                |
| <span data-ttu-id="b6d51-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6d51-147">Windows Vista</span></span>    | <span data-ttu-id="b6d51-148">Por padrão, um decodificador de áudio do Windows Media se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="b6d51-148">By default, a Windows Media Audio decoder behaves as a DMO.</span></span> <span data-ttu-id="b6d51-149">Se você obter uma interface **IMFTransform** ou uma interface **IPropertyStore** em um decodificador de áudio, ela se comporta como um MFT.</span><span class="sxs-lookup"><span data-stu-id="b6d51-149">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on an audio decoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="b6d51-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b6d51-150">Windows 7</span></span>        | <span data-ttu-id="b6d51-151">Por padrão, um decodificador de áudio do Windows Media se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="b6d51-151">By default, a Windows Media Audio decoder behaves as a DMO.</span></span> <span data-ttu-id="b6d51-152">Se você obtiver uma interface **IMFTransform** em um decodificador de áudio, ele se comporta como um MFT.</span><span class="sxs-lookup"><span data-stu-id="b6d51-152">If you obtain an **IMFTransform** interface on an audio decoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="properties"></a><span data-ttu-id="b6d51-153">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b6d51-153">Properties</span></span>

<span data-ttu-id="b6d51-154">O decodificador de áudio do Windows Media dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6d51-154">The Windows Media Audio decoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b6d51-155">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b6d51-155">Property</span></span></th>
<th><span data-ttu-id="b6d51-156">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6d51-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b6d51-157"><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6d51-157"><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></span></span></td>
<td><span data-ttu-id="b6d51-158">Especifica o número máximo de amostras de PCM adicionais que podem ser retornadas ao final da decodificação de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b6d51-158">Specifies the maximum number of additional PCM samples that might be returned at the end of decoding a file.</span></span><br/> <dl> <span data-ttu-id="b6d51-159">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="b6d51-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="b6d51-160">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="b6d51-160">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b6d51-161">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b6d51-161">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6d51-162"><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6d51-162"><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></span></span></td>
<td><span data-ttu-id="b6d51-163">Especifica o modo de controle de intervalo dinâmico que o decodificador de áudio usará.</span><span class="sxs-lookup"><span data-stu-id="b6d51-163">Specifies the dynamic-range control mode that the audio decoder will use.</span></span><br/> <dl> <span data-ttu-id="b6d51-164">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="b6d51-164">Windows XP and later.</span></span><br />
<span data-ttu-id="b6d51-165">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="b6d51-165">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="b6d51-166">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="b6d51-166">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6d51-167"><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6d51-167"><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></span></span></td>
<td><span data-ttu-id="b6d51-168">Especifica os coeficientes de dobra fornecidos pelo autor para decodificação de áudio multicanal para menos canais do que o fluxo codificado contém.</span><span class="sxs-lookup"><span data-stu-id="b6d51-168">Specifies the author-supplied fold-down coefficients for decoding multichannel audio for fewer channels than the encoded stream contains.</span></span> <br/> <dl> <span data-ttu-id="b6d51-169">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="b6d51-169">Windows XP and later.</span></span><br />
<span data-ttu-id="b6d51-170">Professional</span><span class="sxs-lookup"><span data-stu-id="b6d51-170">Professional</span></span><br />
<span data-ttu-id="b6d51-171">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="b6d51-171">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6d51-172"><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6d51-172"><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></span></span></td>
<td><span data-ttu-id="b6d51-173">Especifica se o decodificador de áudio deve fornecer saída de alta resolução.</span><span class="sxs-lookup"><span data-stu-id="b6d51-173">Specifies whether the audio decoder should deliver high-resolution output.</span></span><br/> <dl> <span data-ttu-id="b6d51-174">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="b6d51-174">Windows XP and later.</span></span><br />
<span data-ttu-id="b6d51-175">Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="b6d51-175">Professional, Lossless.</span></span><br />
<span data-ttu-id="b6d51-176">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="b6d51-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6d51-177"><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6d51-177"><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></span></span></td>
<td><span data-ttu-id="b6d51-178">Especifica se o decodificador de áudio deve executar Lt-Rt dobra para baixo.</span><span class="sxs-lookup"><span data-stu-id="b6d51-178">Specifies whether the audio decoder should perform Lt-Rt fold down.</span></span><br/> <dl> <span data-ttu-id="b6d51-179">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="b6d51-179">Windows Vista and later.</span></span><br />
<span data-ttu-id="b6d51-180">Professional.</span><span class="sxs-lookup"><span data-stu-id="b6d51-180">Professional.</span></span><br />
<span data-ttu-id="b6d51-181">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="b6d51-181">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6d51-182"><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6d51-182"><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></span></span></td>
<td><span data-ttu-id="b6d51-183">Especifica a configuração do alto-falante no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="b6d51-183">Specifies the speaker configuration on the client computer.</span></span><br/> <dl> <span data-ttu-id="b6d51-184">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="b6d51-184">Windows XP and later.</span></span><br />
<span data-ttu-id="b6d51-185">Professional.</span><span class="sxs-lookup"><span data-stu-id="b6d51-185">Professional.</span></span><br />
<span data-ttu-id="b6d51-186">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="b6d51-186">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6d51-187"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6d51-187"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span></span></td>
<td><span data-ttu-id="b6d51-188">Especifica o nível médio de volume de conteúdo de áudio.</span><span class="sxs-lookup"><span data-stu-id="b6d51-188">Specifies the average volume level of audio content.</span></span><br/> <dl> <span data-ttu-id="b6d51-189">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="b6d51-189">Windows XP and later.</span></span><br />
<span data-ttu-id="b6d51-190">Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="b6d51-190">Professional, Lossless.</span></span><br />
<span data-ttu-id="b6d51-191">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b6d51-191">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6d51-192"><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6d51-192"><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></span></span></td>
<td><span data-ttu-id="b6d51-193">Especifica o nível de volume médio desejado de conteúdo de áudio de saída.</span><span class="sxs-lookup"><span data-stu-id="b6d51-193">Specifies the desired average volume level of output audio content.</span></span><br/> <dl> <span data-ttu-id="b6d51-194">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="b6d51-194">Windows XP and later.</span></span><br />
<span data-ttu-id="b6d51-195">Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="b6d51-195">Professional, Lossless.</span></span><br />
<span data-ttu-id="b6d51-196">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="b6d51-196">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6d51-197"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6d51-197"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span></span></td>
<td><span data-ttu-id="b6d51-198">Especifica o nível de volume mais alto que ocorre no conteúdo de áudio.</span><span class="sxs-lookup"><span data-stu-id="b6d51-198">Specifies the highest volume level occurring in audio content.</span></span><br/> <dl> <span data-ttu-id="b6d51-199">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="b6d51-199">Windows XP and later.</span></span><br />
<span data-ttu-id="b6d51-200">Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="b6d51-200">Professional, Lossless.</span></span><br />
<span data-ttu-id="b6d51-201">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b6d51-201">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6d51-202"><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6d51-202"><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></span></span></td>
<td><span data-ttu-id="b6d51-203">Especifica o nível máximo de volume desejado de conteúdo de áudio de saída.</span><span class="sxs-lookup"><span data-stu-id="b6d51-203">Specifies the desired maximum volume level of output audio content.</span></span><br/> <dl> <span data-ttu-id="b6d51-204">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="b6d51-204">Windows XP and later.</span></span><br />
<span data-ttu-id="b6d51-205">Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="b6d51-205">Professional, Lossless.</span></span><br />
<span data-ttu-id="b6d51-206">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="b6d51-206">Write-only.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="b6d51-207">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6d51-207">Requirements</span></span>



| <span data-ttu-id="b6d51-208">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6d51-208">Requirement</span></span> | <span data-ttu-id="b6d51-209">Valor</span><span class="sxs-lookup"><span data-stu-id="b6d51-209">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6d51-210">Cliente</span><span class="sxs-lookup"><span data-stu-id="b6d51-210">Client</span></span><br/> | <span data-ttu-id="b6d51-211">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="b6d51-211">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="b6d51-212">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6d51-212">Header</span></span><br/> | <dl> <span data-ttu-id="b6d51-213"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6d51-213"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="b6d51-214">DLL</span><span class="sxs-lookup"><span data-stu-id="b6d51-214">DLL</span></span><br/>    | <dl> <span data-ttu-id="b6d51-215"><dt>Wmadmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6d51-215"><dt>Wmadmod.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b6d51-216">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6d51-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6d51-217">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="b6d51-217">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="b6d51-218">Implementação de codec</span><span class="sxs-lookup"><span data-stu-id="b6d51-218">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 




