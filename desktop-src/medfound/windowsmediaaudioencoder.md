---
description: 'O codificador de áudio do Windows Media codificará os fluxos de áudio. O codificador dá suporte a três categorias de saída codificada: Windows Media Audio Standard, Windows Media Audio Professional e Windows Media Audio sem perdas.'
ms.assetid: 1f6a3a9f-b534-4a6b-b773-0315c759624e
title: Codificador de áudio do Windows Media (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f1d5b9e5f890a43958bcc304dd2d305844fdb4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798048"
---
# <a name="windows-media-audio-encoder"></a><span data-ttu-id="391e8-104">Codificador de áudio do Windows Media</span><span class="sxs-lookup"><span data-stu-id="391e8-104">Windows Media Audio Encoder</span></span>

<span data-ttu-id="391e8-105">O codificador de áudio do Windows Media codificará os fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="391e8-105">The Windows Media Audio encoder encodes audio streams.</span></span> <span data-ttu-id="391e8-106">O codificador dá suporte a três categorias de saída codificada: Windows Media Audio Standard, Windows Media Audio Professional e Windows Media Audio sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-106">The encoder supports three categories of encoded output: Windows Media Audio Standard, Windows Media Audio Professional, and Windows Media Audio Lossless.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="391e8-107">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="391e8-107">Class Identifier</span></span>

<span data-ttu-id="391e8-108">O CLSID (identificador de classe) para o codificador de áudio do Windows Media é representado pela constante **CLSID \_ CWMAEncMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="391e8-108">The class identifier (CLSID) for the Windows Media Audio Encoder is represented by the constant **CLSID\_CWMAEncMediaObject**.</span></span> <span data-ttu-id="391e8-109">Você pode criar uma instância do codificador de áudio chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="391e8-109">You can create an instance of the audio encoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="391e8-110">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="391e8-110">Input Formats</span></span>

<span data-ttu-id="391e8-111">A tabela a seguir mostra as marcas de formato de áudio que representam as categorias de entrada com suporte pelo codificador de áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="391e8-111">The following table shows the audio format tags that represent the input categories supported by the Windows Media Audio encoder.</span></span> <span data-ttu-id="391e8-112">Para obter informações sobre como definir os tipos de entrada e saída para o codificador, consulte [Configurando a codificação de áudio](configuringaudioencoding.md).</span><span class="sxs-lookup"><span data-stu-id="391e8-112">For information about how to set the input and output types for the encoder, see [Configuring Audio Encoding](configuringaudioencoding.md).</span></span>



| <span data-ttu-id="391e8-113">Formatar constante de marca</span><span class="sxs-lookup"><span data-stu-id="391e8-113">Format tag constant</span></span>       | <span data-ttu-id="391e8-114">Formatar valor da marca</span><span class="sxs-lookup"><span data-stu-id="391e8-114">Format tag value</span></span> | <span data-ttu-id="391e8-115">Formato de áudio</span><span class="sxs-lookup"><span data-stu-id="391e8-115">Audio format</span></span>                                          |
|---------------------------|------------------|-------------------------------------------------------|
| <span data-ttu-id="391e8-116">\_PCM de formato Wave \_</span><span class="sxs-lookup"><span data-stu-id="391e8-116">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="391e8-117">0x0001</span><span class="sxs-lookup"><span data-stu-id="391e8-117">0x0001</span></span>           | <span data-ttu-id="391e8-118">Formato PCM</span><span class="sxs-lookup"><span data-stu-id="391e8-118">PCM format</span></span>                                            |
| <span data-ttu-id="391e8-119">\_formato Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="391e8-119">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="391e8-120">0x0003</span><span class="sxs-lookup"><span data-stu-id="391e8-120">0x0003</span></span>           | <span data-ttu-id="391e8-121">Ponto flutuante IEEE</span><span class="sxs-lookup"><span data-stu-id="391e8-121">IEEE floating point</span></span>                                   |
| <span data-ttu-id="391e8-122">\_formato Wave \_ extensível</span><span class="sxs-lookup"><span data-stu-id="391e8-122">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="391e8-123">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="391e8-123">0xFFFE</span></span>           | <span data-ttu-id="391e8-124">Formato PCM/IEEE na estrutura **WAVEFORMATEXTENSIBLE**</span><span class="sxs-lookup"><span data-stu-id="391e8-124">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="391e8-125">Formatos de saída</span><span class="sxs-lookup"><span data-stu-id="391e8-125">Output Formats</span></span>

<span data-ttu-id="391e8-126">A tabela a seguir mostra as marcas de formato de áudio que representam as categorias de saída com suporte pelo codificador de áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="391e8-126">The following table shows the audio format tags that represent the output categories supported by the Windows Media Audio encoder.</span></span>



| <span data-ttu-id="391e8-127">Formatar constante de marca</span><span class="sxs-lookup"><span data-stu-id="391e8-127">Format tag constant</span></span>             | <span data-ttu-id="391e8-128">Formatar valor da marca</span><span class="sxs-lookup"><span data-stu-id="391e8-128">Format tag value</span></span> | <span data-ttu-id="391e8-129">Formato de áudio</span><span class="sxs-lookup"><span data-stu-id="391e8-129">Audio format</span></span>                     |
|---------------------------------|------------------|----------------------------------|
| <span data-ttu-id="391e8-130">\_WMAUDIO2 de formato Wave \_</span><span class="sxs-lookup"><span data-stu-id="391e8-130">WAVE\_FORMAT\_WMAUDIO2</span></span>          | <span data-ttu-id="391e8-131">0x0161</span><span class="sxs-lookup"><span data-stu-id="391e8-131">0x0161</span></span>           | <span data-ttu-id="391e8-132">Padrão de áudio do Windows Media</span><span class="sxs-lookup"><span data-stu-id="391e8-132">Windows Media Audio Standard</span></span>     |
| <span data-ttu-id="391e8-133">\_WMAUDIO3 de formato Wave \_</span><span class="sxs-lookup"><span data-stu-id="391e8-133">WAVE\_FORMAT\_WMAUDIO3</span></span>          | <span data-ttu-id="391e8-134">0x0162</span><span class="sxs-lookup"><span data-stu-id="391e8-134">0x0162</span></span>           | <span data-ttu-id="391e8-135">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="391e8-135">Windows Media Audio Professional</span></span> |
| <span data-ttu-id="391e8-136">\_formato Wave \_ WMAUDIO \_ Lossless</span><span class="sxs-lookup"><span data-stu-id="391e8-136">WAVE\_FORMAT\_WMAUDIO\_LOSSLESS</span></span> | <span data-ttu-id="391e8-137">0x0163</span><span class="sxs-lookup"><span data-stu-id="391e8-137">0x0163</span></span>           | <span data-ttu-id="391e8-138">Windows Media Audio sem perdas</span><span class="sxs-lookup"><span data-stu-id="391e8-138">Windows Media Audio Lossless</span></span>     |



 

## <a name="interfaces"></a><span data-ttu-id="391e8-139">Interfaces</span><span class="sxs-lookup"><span data-stu-id="391e8-139">Interfaces</span></span>

<span data-ttu-id="391e8-140">Um objeto endoder de áudio expõe a interface **IMediaObject** para que o objeto possa ser usado como um objeto de mídia do DirectX (DMO) e expõe a interface **IMFTransform** para que o objeto possa ser usado como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="391e8-140">An audio endoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="391e8-141">Um codificador de áudio do Windows Media se comporta como DMO ou MFT dependendo de quais interfaces você obtém e qual versão do Windows está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="391e8-141">A Windows Media Audio encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="391e8-142">A tabela a seguir mostra as condições sob as quais um codificador de áudio se comporta como um DMO ou um MFT.</span><span class="sxs-lookup"><span data-stu-id="391e8-142">The following table shows the conditions under which an audio encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="391e8-143">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="391e8-143">Operating system</span></span> | <span data-ttu-id="391e8-144">Comportamento do codificador</span><span class="sxs-lookup"><span data-stu-id="391e8-144">Encoder behavior</span></span>                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="391e8-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="391e8-145">Windows XP</span></span>       | <span data-ttu-id="391e8-146">Um codificador de áudio do Windows Media sempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="391e8-146">A Windows Media Audio encoder always behaves as a DMO.</span></span>                                                                                                                                |
| <span data-ttu-id="391e8-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="391e8-147">Windows Vista</span></span>    | <span data-ttu-id="391e8-148">Por padrão, um codificador de áudio do Windows Media se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="391e8-148">By default, a Windows Media Audio encoder behaves as a DMO.</span></span> <span data-ttu-id="391e8-149">Se você obtiver uma interface **IMFTransform** ou uma interface **IPropertyStore** em um codificador de áudio, ela se comporta como um MFT.</span><span class="sxs-lookup"><span data-stu-id="391e8-149">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on an audio encoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="391e8-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="391e8-150">Windows 7</span></span>        | <span data-ttu-id="391e8-151">Por padrão, um codificador de áudio do Windows Media se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="391e8-151">By default, a Windows Media Audio encoder behaves as a DMO.</span></span> <span data-ttu-id="391e8-152">Se você obtiver uma interface **IMFTransform** em um codificador de áudio, ele se comporta como um MFT.</span><span class="sxs-lookup"><span data-stu-id="391e8-152">If you obtain an **IMFTransform** interface on an audio encoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="encoder-properties"></a><span data-ttu-id="391e8-153">Propriedades do codificador</span><span class="sxs-lookup"><span data-stu-id="391e8-153">Encoder Properties</span></span>

<span data-ttu-id="391e8-154">O codificador de áudio do Windows Media dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="391e8-154">The Windows Media Audio encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="391e8-155">Propriedade</span><span class="sxs-lookup"><span data-stu-id="391e8-155">Property</span></span></th>
<th><span data-ttu-id="391e8-156">Descrição</span><span class="sxs-lookup"><span data-stu-id="391e8-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="391e8-157"><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-157"><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></span></span></td>
<td><span data-ttu-id="391e8-158">Especifica se o codificador usa a codificação de VBR média controlável.</span><span class="sxs-lookup"><span data-stu-id="391e8-158">Specifies whether the encoder uses average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="391e8-159">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-160">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-160">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-161">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-161">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-162"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-162"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="391e8-163">Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits variável restrita (VBR) em sua taxa de bits de pico.</span><span class="sxs-lookup"><span data-stu-id="391e8-163">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate.</span></span><br/> <dl> <span data-ttu-id="391e8-164">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-164">Windows XP and later.</span></span><br />
<span data-ttu-id="391e8-165">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="391e8-165">Standard, Professional.</span></span><br />
<span data-ttu-id="391e8-166">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-166">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-167"><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-167"><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></span></span></td>
<td><span data-ttu-id="391e8-168">Especifica se o codificador deve verificar a consistência dos dados entre as passagens ao executar a codificação de VBR de duas passagens.</span><span class="sxs-lookup"><span data-stu-id="391e8-168">Specifies whether whether the encoder should check for data consistency across passes when performing two-pass VBR encoding.</span></span> <br/> <dl> <span data-ttu-id="391e8-169">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-169">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-170">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-170">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-171">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="391e8-171">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-172"><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-172"><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></span></span></td>
<td><span data-ttu-id="391e8-173">Especifica se o codificador é restrito por um requisito de latência de decodificador máximo.</span><span class="sxs-lookup"><span data-stu-id="391e8-173">Specifies whether the encoder is constrained by a maximum decoder latency requirement.</span></span><br/> <dl> <span data-ttu-id="391e8-174">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-174">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-175">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-175">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-176">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-176">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-177"><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-177"><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="391e8-178">Especifica se a complexidade do algoritmo de codificação é restrita.</span><span class="sxs-lookup"><span data-stu-id="391e8-178">Specifies whether the complexity of the encoding algorithm is constrained.</span></span><br/> <dl> <span data-ttu-id="391e8-179">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-179">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-180">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-180">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-181">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-181">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-182"><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-182"><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></span></span></td>
<td><span data-ttu-id="391e8-183">Especifica se o codificador é restrito por um requisito de latência máxima.</span><span class="sxs-lookup"><span data-stu-id="391e8-183">Specifies whether the encoder is constrained by a maximum latency requirement.</span></span><br/> <dl> <span data-ttu-id="391e8-184">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-184">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-185">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-185">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-186">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-186">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-187"><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-187"><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="391e8-188">Especifica se os modos enumerados pelo codificador são limitados àqueles que atendem a um requisito de qualidade.</span><span class="sxs-lookup"><span data-stu-id="391e8-188">Specifies whether modes enumerated by the encoder are limited to those that meet a quality requirement.</span></span><br/> <dl> <span data-ttu-id="391e8-189">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-189">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-190">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-190">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-191">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-191">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-192"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-192"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="391e8-193">Especifica o perfil de complexidade do conteúdo codificado.</span><span class="sxs-lookup"><span data-stu-id="391e8-193">Specifies the complexity profile of the encoded content.</span></span><br/> <dl> <span data-ttu-id="391e8-194">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-194">Windows XP and later.</span></span><br />
<span data-ttu-id="391e8-195">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-195">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-196">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="391e8-196">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-197"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-197"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="391e8-198">Especifica o nível de qualidade desejado para a codificação de VBR.</span><span class="sxs-lookup"><span data-stu-id="391e8-198">Specifies the desired quality level for VBR encoding.</span></span><br/> <dl> <span data-ttu-id="391e8-199">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-199">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-200">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-200">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-201">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-201">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-202"><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-202"><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></span></span></td>
<td><span data-ttu-id="391e8-203">Especifica se o codificador usa substituição de ruído.</span><span class="sxs-lookup"><span data-stu-id="391e8-203">Specifies whether the encoder uses noise substitution.</span></span><br/> <dl> <span data-ttu-id="391e8-204">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-204">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-205">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-205">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-206">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-206">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-207"><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-207"><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></span></span></td>
<td><span data-ttu-id="391e8-208">Especifica se o codificador usa a limitação de intervalo PCM.</span><span class="sxs-lookup"><span data-stu-id="391e8-208">Specifies whether the encoder uses PCM range limiting.</span></span><br/> <dl> <span data-ttu-id="391e8-209">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-209">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-210">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-210">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-211">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-211">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-212"><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-212"><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></span></span></td>
<td><span data-ttu-id="391e8-213">Especifica a largura de banda máxima codificada permitida pelo truncamento de banda no codificador.</span><span class="sxs-lookup"><span data-stu-id="391e8-213">Specifies the maximum coded bandwidth allowed by band truncation in the encoder.</span></span><br/> <dl> <span data-ttu-id="391e8-214">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-214">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-215">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-215">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-216">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-216">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-217"><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-217"><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></span></span></td>
<td><span data-ttu-id="391e8-218">Especifica a largura de banda mínima codificada permitida pelo truncamento de banda no codificador.</span><span class="sxs-lookup"><span data-stu-id="391e8-218">Specifies the minimum coded bandwidth allowed by band truncation in the encoder.</span></span><br/> <dl> <span data-ttu-id="391e8-219">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-219">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-220">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-220">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-221">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-221">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-222"><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-222"><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></span></span></td>
<td><span data-ttu-id="391e8-223">Especifica a qualidade na qual a largura de banda mínima codificada é permitida.</span><span class="sxs-lookup"><span data-stu-id="391e8-223">Specifies the quality at which minimum coded bandwidth is allowed.</span></span> <br/> <dl> <span data-ttu-id="391e8-224">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-224">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-225">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-225">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-226">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-226">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-227"><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-227"><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></span></span></td>
<td><span data-ttu-id="391e8-228">Especifica a qualidade na qual a largura de banda máxima codificada é permitida.</span><span class="sxs-lookup"><span data-stu-id="391e8-228">Specifies the quality at which maximum coded bandwidth is allowed.</span></span><br/> <dl> <span data-ttu-id="391e8-229">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-229">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-230">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-230">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-231">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-231">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-232"><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-232"><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></span></span></td>
<td><span data-ttu-id="391e8-233">Especifica se o codificador executa o truncamento de banda.</span><span class="sxs-lookup"><span data-stu-id="391e8-233">Specifies whether the encoder performs band truncation.</span></span><br/> <dl> <span data-ttu-id="391e8-234">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-234">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-235">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-235">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-236">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-236">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-237"><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-237"><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></span></span></td>
<td><span data-ttu-id="391e8-238">Especifica se o codificador usa o estilo de computação de máscara executado pela versão 7 do codificador de áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="391e8-238">Specifies whether the encoder uses the style of mask computation performed by version 7 of the Windows Media Audio encoder.</span></span><br/> <dl> <span data-ttu-id="391e8-239">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-239">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-240">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-240">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-241">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-241">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-242"><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-242"><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></span></span></td>
<td><span data-ttu-id="391e8-243">Especifica se o codificador executa o processamento de imagens estéreo.</span><span class="sxs-lookup"><span data-stu-id="391e8-243">Specifies whether the encoder performs stereo image processing.</span></span> <br/> <dl> <span data-ttu-id="391e8-244">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-244">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-245">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-245">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-246">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-246">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-247"><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-247"><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="391e8-248">Especifica a janela de buffer, em milissegundos, para um codificador configurado para usar a codificação de VBR média controlável.</span><span class="sxs-lookup"><span data-stu-id="391e8-248">Specifies the buffer window, in milliseconds, for an encoder that is configured to use average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="391e8-249">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-249">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-250">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-250">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-251">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-251">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-252"><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-252"><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="391e8-253">Especifica a taxa média de bits, em bits por segundo, para um codificador configurado para usar a codificação de VBR média controlável.</span><span class="sxs-lookup"><span data-stu-id="391e8-253">Specifies the average bit rate, in bits per second, for an encoder that is configured to use average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="391e8-254">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-254">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-255">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-255">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-256">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-256">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-257"><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-257"><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="391e8-258">Especifica a complexidade do algoritmo de codificação.</span><span class="sxs-lookup"><span data-stu-id="391e8-258">Specifies the complexity of the encoding algorithm.</span></span><br/> <dl> <span data-ttu-id="391e8-259">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-259">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-260">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-260">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-261">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-261">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-262"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-262"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="391e8-263">Especifica o fim de uma passagem de codificação.</span><span class="sxs-lookup"><span data-stu-id="391e8-263">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="391e8-264">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-264">Windows XP and later.</span></span><br />
<span data-ttu-id="391e8-265">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="391e8-265">Standard, Professional.</span></span><br />
<span data-ttu-id="391e8-266">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-266">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-267"><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-267"><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></span></span></td>
<td><span data-ttu-id="391e8-268">Especifica se o codificador principal usa &quot; o &quot; recurso Plus.</span><span class="sxs-lookup"><span data-stu-id="391e8-268">Specifies whether the core encoder uses the &quot;Plus&quot; feature.</span></span><br/> <dl> <span data-ttu-id="391e8-269">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-269">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-270">Professional.</span><span class="sxs-lookup"><span data-stu-id="391e8-270">Professional.</span></span><br />
<span data-ttu-id="391e8-271">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-271">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-272"><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-272"><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></span></span></td>
<td><span data-ttu-id="391e8-273">Especifica a latência máxima para o decodificador, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="391e8-273">Specifies the maximum latency for the decoder, in milliseconds.</span></span><br/> <dl> <span data-ttu-id="391e8-274">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-274">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-275">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-275">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-276">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-276">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-277"><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-277"><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></span></span></td>
<td><span data-ttu-id="391e8-278">Especifica a latência máxima para o codificador, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="391e8-278">Specifies the maximum latency for the encoder, in milliseconds.</span></span><br/> <dl> <span data-ttu-id="391e8-279">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-279">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-280">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-280">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-281">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-281">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-282"><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-282"><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="391e8-283">Especifica o nível de qualidade de VBR do tipo de saída enumerado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="391e8-283">Specifies the VBR quality level of the most recently enumerated output type.</span></span><br/> <dl> <span data-ttu-id="391e8-284">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-284">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-285">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-285">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-286">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="391e8-286">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-287"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-287"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="391e8-288">Especifica o número máximo de passagens aceitas pelo codificador.</span><span class="sxs-lookup"><span data-stu-id="391e8-288">Specifies the maximum number of passes supported by the encoder.</span></span><br/> <dl> <span data-ttu-id="391e8-289">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-289">Windows XP and later.</span></span><br />
<span data-ttu-id="391e8-290">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-290">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-291">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="391e8-291">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-292"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-292"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="391e8-293">Especifica o número de passagens que o codificador usará para codificar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="391e8-293">Specifies the number of passes that the encoder will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="391e8-294">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-294">Windows XP and later.</span></span><br />
<span data-ttu-id="391e8-295">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-295">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-296">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-296">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-297"><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-297"><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></span></span></td>
<td><span data-ttu-id="391e8-298">Especifica se o codificador é restrito por uma taxa de bits de pico.</span><span class="sxs-lookup"><span data-stu-id="391e8-298">Specifies whether the encoder is constrained by a peak bit rate.</span></span><br/> <dl> <span data-ttu-id="391e8-299">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-299">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-300">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="391e8-300">Standard, Professional.</span></span><br />
<span data-ttu-id="391e8-301">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-301">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-302"><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-302"><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></span></span></td>
<td><span data-ttu-id="391e8-303">Especifica o número preferencial de amostras por quadro.</span><span class="sxs-lookup"><span data-stu-id="391e8-303">Specifies the preferred number of samples per frame.</span></span><br/> <dl> <span data-ttu-id="391e8-304">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-304">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-305">Professional.</span><span class="sxs-lookup"><span data-stu-id="391e8-305">Professional.</span></span><br />
<span data-ttu-id="391e8-306">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-306">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-307"><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-307"><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></span></span></td>
<td><span data-ttu-id="391e8-308">Especifica se o codificador deve usar um tamanho de quadro preferencial.</span><span class="sxs-lookup"><span data-stu-id="391e8-308">Specifies whether the encoder should use a preferred frame size.</span></span><br/> <dl> <span data-ttu-id="391e8-309">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-309">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-310">Professional.</span><span class="sxs-lookup"><span data-stu-id="391e8-310">Professional.</span></span><br />
<span data-ttu-id="391e8-311">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-311">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-312"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-312"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="391e8-313">Especifica a taxa de bits de pico, em bits por segundo, usada para codificação de taxa de bits de variável (VBR) restrita de 2 passagens.</span><span class="sxs-lookup"><span data-stu-id="391e8-313">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) encoding.</span></span> <br/> <dl> <span data-ttu-id="391e8-314">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-314">Windows XP and later.</span></span><br />
<span data-ttu-id="391e8-315">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="391e8-315">Standard, Professional.</span></span><br />
<span data-ttu-id="391e8-316">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-316">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-317"><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-317"><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="391e8-318">Especifica a janela de buffer médio, em milissegundos, de um fluxo codificado.</span><span class="sxs-lookup"><span data-stu-id="391e8-318">Specifies the average buffer window, in milliseconds, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="391e8-319">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-319">Windows XP and later.</span></span><br />
<span data-ttu-id="391e8-320">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-320">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-321">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="391e8-321">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-322"><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-322"><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="391e8-323">Especifica a janela de buffer máximo, em milissegundos, de um fluxo codificado.</span><span class="sxs-lookup"><span data-stu-id="391e8-323">Specifies the maximum buffer window, in milliseconds, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="391e8-324">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-324">Windows XP and later.</span></span><br />
<span data-ttu-id="391e8-325">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-325">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-326">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="391e8-326">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-327"><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-327"><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="391e8-328">Especifica a taxa média de bits, em bits por segundo, de um fluxo codificado.</span><span class="sxs-lookup"><span data-stu-id="391e8-328">Specifies the average bit rate, in bits per second, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="391e8-329">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-329">Windows XP and later.</span></span><br />
<span data-ttu-id="391e8-330">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-330">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-331">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="391e8-331">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-332"><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-332"><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="391e8-333">Especifica a taxa de bits máxima, em bits por segundo, de um fluxo codificado.</span><span class="sxs-lookup"><span data-stu-id="391e8-333">Specifies the maximum bit rate, in bits per second, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="391e8-334">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-334">Windows XP and later.</span></span><br />
<span data-ttu-id="391e8-335">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-335">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-336">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="391e8-336">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-337"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-337"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="391e8-338">Especifica se o codificador usa a codificação VBR.</span><span class="sxs-lookup"><span data-stu-id="391e8-338">Specifies whether the encoder uses VBR encoding.</span></span><br/> <dl> <span data-ttu-id="391e8-339">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-339">Windows XP and later.</span></span><br />
<span data-ttu-id="391e8-340">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-340">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-341">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-341">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-342"><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-342"><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></span></span></td>
<td><span data-ttu-id="391e8-343">Essa propriedade não é usada no momento pelo codec de áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="391e8-343">This property is currently not used by the Windows Media Audio codec.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-344"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-344"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span></span></td>
<td><span data-ttu-id="391e8-345">Especifica o nível médio de volume de conteúdo de áudio.</span><span class="sxs-lookup"><span data-stu-id="391e8-345">Specifies the average volume level of audio content.</span></span><br/> <dl> <span data-ttu-id="391e8-346">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-346">Windows XP and later.</span></span><br />
<span data-ttu-id="391e8-347">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-347">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-348">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="391e8-348">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-349"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-349"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span></span></td>
<td><span data-ttu-id="391e8-350">Especifica o nível de volume mais alto que ocorre no conteúdo de áudio.</span><span class="sxs-lookup"><span data-stu-id="391e8-350">Specifies the highest volume level occurring in audio content.</span></span><br/> <dl> <span data-ttu-id="391e8-351">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-351">Windows XP and later.</span></span><br />
<span data-ttu-id="391e8-352">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-352">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-353">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="391e8-353">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-354"><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-354"><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></span></span></td>
<td><span data-ttu-id="391e8-355">Especifica a média de bytes por segundo para áudio de VBR codificado.</span><span class="sxs-lookup"><span data-stu-id="391e8-355">Specifies the average bytes per second for VBR encoded audio.</span></span><br/> <dl> <span data-ttu-id="391e8-356">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-356">Windows XP and later.</span></span><br />
<span data-ttu-id="391e8-357">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-357">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-358">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="391e8-358">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-359"><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-359"><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></span></span></td>
<td><span data-ttu-id="391e8-360">Especifica se o codificador deve produzir 1 pacote WMA por quadro.</span><span class="sxs-lookup"><span data-stu-id="391e8-360">Specifies whether the encoder should produce 1 WMA packet per frame.</span></span><br/> <dl> <span data-ttu-id="391e8-361">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-361">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-362">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-362">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-363">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-363">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-364"><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-364"><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></span></span></td>
<td><span data-ttu-id="391e8-365">Especifica se o codificador deve gerar parâmetros de controle de intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="391e8-365">Specifies whether the encoder should generate dynamic range control parameters.</span></span><br/> <dl> <span data-ttu-id="391e8-366">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-366">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-367">Standard, Professional, sem perdas.</span><span class="sxs-lookup"><span data-stu-id="391e8-367">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="391e8-368">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-368">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="391e8-369"><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-369"><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></span></span></td>
<td><span data-ttu-id="391e8-370">Especifica a estrutura <strong>WAVEFORMATEX</strong> que descreve o conteúdo de áudio de entrada.</span><span class="sxs-lookup"><span data-stu-id="391e8-370">Specifies the <strong>WAVEFORMATEX</strong> structure describing the input audio content.</span></span><br/> <dl> <span data-ttu-id="391e8-371">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-371">Windows XP and later.</span></span><br />
<span data-ttu-id="391e8-372">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="391e8-372">Standard, Professional.</span></span><br />
<span data-ttu-id="391e8-373">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-373">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="391e8-374"><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></span><span class="sxs-lookup"><span data-stu-id="391e8-374"><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></span></span></td>
<td><span data-ttu-id="391e8-375">Especifica se o codificador deve habilitar a codificação S/PDIF em tempo real.</span><span class="sxs-lookup"><span data-stu-id="391e8-375">Specifies whether the encoder should enable real-time S/PDIF encoding .</span></span><br/> <dl> <span data-ttu-id="391e8-376">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="391e8-376">Windows Vista and later.</span></span><br />
<span data-ttu-id="391e8-377">Professional.</span><span class="sxs-lookup"><span data-stu-id="391e8-377">Professional.</span></span><br />
<span data-ttu-id="391e8-378">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="391e8-378">Read/write.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="391e8-379">Requisitos</span><span class="sxs-lookup"><span data-stu-id="391e8-379">Requirements</span></span>



| <span data-ttu-id="391e8-380">Requisito</span><span class="sxs-lookup"><span data-stu-id="391e8-380">Requirement</span></span> | <span data-ttu-id="391e8-381">Valor</span><span class="sxs-lookup"><span data-stu-id="391e8-381">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="391e8-382">Cliente</span><span class="sxs-lookup"><span data-stu-id="391e8-382">Client</span></span><br/> | <span data-ttu-id="391e8-383">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="391e8-383">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="391e8-384">parâmetro</span><span class="sxs-lookup"><span data-stu-id="391e8-384">Header</span></span><br/> | <dl> <span data-ttu-id="391e8-385"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="391e8-385"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="391e8-386">DLL</span><span class="sxs-lookup"><span data-stu-id="391e8-386">DLL</span></span><br/>    | <dl> <span data-ttu-id="391e8-387"><dt>Wmadmoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="391e8-387"><dt>Wmadmoe.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="391e8-388">Confira também</span><span class="sxs-lookup"><span data-stu-id="391e8-388">See also</span></span>

<dl> <dt>

[<span data-ttu-id="391e8-389">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="391e8-389">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="391e8-390">Implementação de codec</span><span class="sxs-lookup"><span data-stu-id="391e8-390">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 




