---
description: O decodificador Windows Media Video 9 decodifica fluxos de vídeo que foram codificados pelo codificador de vídeo do Windows Media.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Decodificador do Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d89e05f82ce503016a10d5591a23bc673d0db5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798232"
---
# <a name="windows-media-video-9-decoder"></a><span data-ttu-id="fdd9c-103">Decodificador do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="fdd9c-103">Windows Media Video 9 Decoder</span></span>

<span data-ttu-id="fdd9c-104">O decodificador Windows Media Video 9 decodifica fluxos de vídeo que foram codificados pelo [**codificador de vídeo do Windows Media**](windowsmediavideo9encoder.md).</span><span class="sxs-lookup"><span data-stu-id="fdd9c-104">The Windows Media Video 9 decoder decodes video streams that were encoded by the [**Windows Media Video Encoder**](windowsmediavideo9encoder.md).</span></span> <span data-ttu-id="fdd9c-105">O codificador e o decodificador dão suporte às quatro categorias de vídeo codificadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-105">The encoder and decoder support the following four categories of encoded video.</span></span>

-   <span data-ttu-id="fdd9c-106">Perfil simples do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="fdd9c-106">Windows Media Video 9 Simple Profile</span></span>
-   <span data-ttu-id="fdd9c-107">Perfil principal do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="fdd9c-107">Windows Media Video 9 Main Profile</span></span>
-   <span data-ttu-id="fdd9c-108">Perfil avançado do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="fdd9c-108">Windows Media Video 9 Advanced Profile</span></span>
-   <span data-ttu-id="fdd9c-109">Imagem do vídeo 9,1 do Windows Media</span><span class="sxs-lookup"><span data-stu-id="fdd9c-109">Windows Media Video 9.1 Image</span></span>

## <a name="class-identifier"></a><span data-ttu-id="fdd9c-110">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="fdd9c-110">Class Identifier</span></span>

<span data-ttu-id="fdd9c-111">O CLSID (identificador de classe) para o decodificador de vídeo do Windows Media é representado pela constante **CLSID \_ CWMVDecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-111">The class identifier (CLSID) for the Windows Media Video decoder is represented by the constant **CLSID\_CWMVDecMediaObject**.</span></span> <span data-ttu-id="fdd9c-112">Você pode criar uma instância do decodificador de vídeo chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-112">You can create an instance of the video decoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="fdd9c-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="fdd9c-113">Interfaces</span></span>

<span data-ttu-id="fdd9c-114">Um objeto de decodificador de vídeo expõe a interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que o objeto possa ser usado como um objeto de mídia DirectX (DMO) e expõe a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que o objeto possa ser usado como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="fdd9c-114">A video decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="fdd9c-115">Um decodificador de vídeo se comporta como um DMO ou um MFT dependendo de quais interfaces você obtém e qual versão do Windows está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-115">A video decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="fdd9c-116">A tabela a seguir mostra as condições sob as quais um decodificador de vídeo se comporta como um DMO ou um MFT.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-116">The following table shows the conditions under which a video decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="fdd9c-117">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="fdd9c-117">Operating system</span></span>            | <span data-ttu-id="fdd9c-118">Comportamento do decodificador</span><span class="sxs-lookup"><span data-stu-id="fdd9c-118">Decoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd9c-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fdd9c-119">Windows XP</span></span>                  | <span data-ttu-id="fdd9c-120">Um decodificador de vídeo do Windows Media sempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-120">A Windows Media video decoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="fdd9c-121">Windows Vista e Windows 7</span><span class="sxs-lookup"><span data-stu-id="fdd9c-121">Windows Vista and Windows 7</span></span> | <span data-ttu-id="fdd9c-122">Por padrão, um decodificador de vídeo do Windows Media se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-122">By default, a Windows Media video decoder behaves as a DMO.</span></span> <span data-ttu-id="fdd9c-123">Se você obtiver uma interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) em um decodificador de vídeo, ele se comporta como um MFT.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-123">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="fdd9c-124">A partir do Windows 7, o decodificador de vídeo do Windows Media implementa a interface [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) .</span><span class="sxs-lookup"><span data-stu-id="fdd9c-124">Beginning with Windows 7, the Windows Media Video decoder implements the [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) interface.</span></span>

## <a name="input-formats"></a><span data-ttu-id="fdd9c-125">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="fdd9c-125">Input Formats</span></span>

<span data-ttu-id="fdd9c-126">A tabela a seguir mostra os códigos de quatro caracteres (FOURCC) que correspondem às categorias de entrada codificada que são suportadas pelo decodificador de vídeo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-126">The following table shows the four-character codes (FOURCCs) that correspond to the categories of encoded input that are supported by the Windows Media Video decoder.</span></span>



| <span data-ttu-id="fdd9c-127">Categoria</span><span class="sxs-lookup"><span data-stu-id="fdd9c-127">Category</span></span>                               | <span data-ttu-id="fdd9c-128">FOURCC</span><span class="sxs-lookup"><span data-stu-id="fdd9c-128">FOURCC</span></span>                                   |
|----------------------------------------|------------------------------------------|
| <span data-ttu-id="fdd9c-129">Perfil simples do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="fdd9c-129">Windows Media Video 9 Simple Profile</span></span>   | <span data-ttu-id="fdd9c-130">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="fdd9c-130">"WMV3"</span></span>                                   |
| <span data-ttu-id="fdd9c-131">Perfil principal do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="fdd9c-131">Windows Media Video 9 Main Profile</span></span>     | <span data-ttu-id="fdd9c-132">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="fdd9c-132">"WMV3"</span></span>                                   |
| <span data-ttu-id="fdd9c-133">Perfil avançado do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="fdd9c-133">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="fdd9c-134">"WVC1"</span><span class="sxs-lookup"><span data-stu-id="fdd9c-134">"WVC1"</span></span>                                   |
| <span data-ttu-id="fdd9c-135">Imagem do vídeo 9,1 do Windows Media</span><span class="sxs-lookup"><span data-stu-id="fdd9c-135">Windows Media Video 9.1 Image</span></span>          | <span data-ttu-id="fdd9c-136">"WMVP" para 9,1, "WVP2" para 9,1 versão 2</span><span class="sxs-lookup"><span data-stu-id="fdd9c-136">"WMVP" for 9.1, "WVP2" for 9.1 version 2</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="fdd9c-137">Formatos de saída</span><span class="sxs-lookup"><span data-stu-id="fdd9c-137">Output Formats</span></span>

<span data-ttu-id="fdd9c-138">O decodificador de vídeo do Windows Media dá suporte aos seguintes subtipos de mídia de saída quando ele está atuando como um DMO.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-138">The Windows Media Video decoder supports the following output media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="fdd9c-139">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="fdd9c-139">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="fdd9c-140">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="fdd9c-140">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="fdd9c-141">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="fdd9c-141">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="fdd9c-142">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="fdd9c-142">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="fdd9c-143">MEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="fdd9c-143">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="fdd9c-144">MEDIASUBTYPE \_ NV11</span><span class="sxs-lookup"><span data-stu-id="fdd9c-144">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="fdd9c-145">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="fdd9c-145">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="fdd9c-146">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="fdd9c-146">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="fdd9c-147">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="fdd9c-147">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="fdd9c-148">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="fdd9c-148">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="fdd9c-149">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="fdd9c-149">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="fdd9c-150">O decodificador de vídeo do Windows Media dá suporte aos seguintes subtipos de mídia de saída quando ele está atuando como um MFT.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-150">The Windows Media Video decoder supports the following output media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="fdd9c-151">MFVideoFormat \_ NV12</span><span class="sxs-lookup"><span data-stu-id="fdd9c-151">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="fdd9c-152">MFVideoFormat \_ YV12</span><span class="sxs-lookup"><span data-stu-id="fdd9c-152">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="fdd9c-153">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="fdd9c-153">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="fdd9c-154">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="fdd9c-154">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="fdd9c-155">MFVideoFormat \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="fdd9c-155">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="fdd9c-156">MFVideoFormat \_ NV11</span><span class="sxs-lookup"><span data-stu-id="fdd9c-156">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="fdd9c-157">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="fdd9c-157">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="fdd9c-158">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="fdd9c-158">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="fdd9c-159">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="fdd9c-159">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="fdd9c-160">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="fdd9c-160">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="fdd9c-161">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="fdd9c-161">MFVideoFormat\_RGB8</span></span>

## <a name="properties"></a><span data-ttu-id="fdd9c-162">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fdd9c-162">Properties</span></span>

<span data-ttu-id="fdd9c-163">O decodificador de vídeo do Windows Media dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-163">The Windows Media Video decoder supports the following properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fdd9c-164">Propriedade</span><span class="sxs-lookup"><span data-stu-id="fdd9c-164">Property</span></span></th>
<th><span data-ttu-id="fdd9c-165">Descrição</span><span class="sxs-lookup"><span data-stu-id="fdd9c-165">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fdd9c-166"><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></span><span class="sxs-lookup"><span data-stu-id="fdd9c-166"><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></span></span></td>
<td><span data-ttu-id="fdd9c-167">Especifica se o codec decodifica quadros de vídeo entrelaçados do fluxo compactado como quadros progressivos.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-167">Specifies whether the codec decodes interlaced video frames from the compressed stream as progressive frames.</span></span><br/> <dl> <span data-ttu-id="fdd9c-168">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-168">Windows XP and later.</span></span><br />
<span data-ttu-id="fdd9c-169">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-169">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="fdd9c-170">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-170">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdd9c-171"><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></span><span class="sxs-lookup"><span data-stu-id="fdd9c-171"><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></span></span></td>
<td><span data-ttu-id="fdd9c-172">Especifica se o decodificador usará o hardware de aceleração de vídeo do DirectX, se disponível.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-172">Specifies whether the decoder will use DirectX video acceleration hardware, if available.</span></span><br/> <dl> <span data-ttu-id="fdd9c-173">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-173">Windows XP and later.</span></span><br />
<span data-ttu-id="fdd9c-174">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-174">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="fdd9c-175">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-175">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdd9c-176"><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></span><span class="sxs-lookup"><span data-stu-id="fdd9c-176"><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></span></span></td>
<td><span data-ttu-id="fdd9c-177">Especifica o nível de energia para o decodificador.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-177">Specifies the power level for the decoder.</span></span><br/> <dl> <span data-ttu-id="fdd9c-178">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-178">Windows 7.</span></span><br />
<span data-ttu-id="fdd9c-179">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-179">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="fdd9c-180">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-180">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdd9c-181"><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></span><span class="sxs-lookup"><span data-stu-id="fdd9c-181"><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></span></span></td>
<td><span data-ttu-id="fdd9c-182">Especifica se o decodificador deve usar a interpolação de quadros.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-182">Specifies whether the decoder should use frame interpolation.</span></span><br/> <dl> <span data-ttu-id="fdd9c-183">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-183">Windows XP and later.</span></span><br />
<span data-ttu-id="fdd9c-184">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-184">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="fdd9c-185">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-185">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdd9c-186"><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></span><span class="sxs-lookup"><span data-stu-id="fdd9c-186"><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></span></span></td>
<td><span data-ttu-id="fdd9c-187">Especifica se o decodificador dá suporte à interpolação de quadros.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-187">Specifies whether the decoder supports frame interpolation.</span></span><br/> <dl> <span data-ttu-id="fdd9c-188">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-188">Windows XP and later.</span></span><br />
<span data-ttu-id="fdd9c-189">Perfil simples, perfil principal, perfil avançado, imagem</span><span class="sxs-lookup"><span data-stu-id="fdd9c-189">Simple Profile, Main Profile, Advanced Profile, Image</span></span><br />
<span data-ttu-id="fdd9c-190">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-190">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdd9c-191"><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></span><span class="sxs-lookup"><span data-stu-id="fdd9c-191"><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></span></span></td>
<td><span data-ttu-id="fdd9c-192">Especifica o número de threads que o decodificador usará.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-192">Specifies the number of threads that the decoder will use.</span></span><br/> <dl> <span data-ttu-id="fdd9c-193">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-193">Windows Vista and later.</span></span><br />
<span data-ttu-id="fdd9c-194">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-194">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="fdd9c-195">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-195">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdd9c-196"><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></span><span class="sxs-lookup"><span data-stu-id="fdd9c-196"><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></span></span></td>
<td><span data-ttu-id="fdd9c-197">Especifica o modo de pós-processamento do decodificador.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-197">Specifies the post processing mode for the decoder.</span></span><br/> <dl> <span data-ttu-id="fdd9c-198">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-198">Windows Vista and later.</span></span><br />
<span data-ttu-id="fdd9c-199">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-199">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="fdd9c-200">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-200">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdd9c-201"><strong>g_wszWMVCNeedsDrain</strong></span><span class="sxs-lookup"><span data-stu-id="fdd9c-201"><strong>g_wszWMVCNeedsDrain</strong></span></span></td>
<td><span data-ttu-id="fdd9c-202">Especifica se o decodificador deve ser drenado.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-202">Specifies whether the decoder should be drained.</span></span><br/> <dl> <span data-ttu-id="fdd9c-203">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fdd9c-203">Windows 8</span></span><br />
<span data-ttu-id="fdd9c-204">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-204">Read-only.</span></span><br />
</dl> <span data-ttu-id="fdd9c-205">Essa propriedade é usada pelo tempo de execução do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-205">This property is used by the Windows Media Format runtime.</span></span> <span data-ttu-id="fdd9c-206">O tipo de propriedade é <strong>VARIANT_BOOL</strong>.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-206">The property type is <strong>VARIANT_BOOL</strong>.</span></span> <span data-ttu-id="fdd9c-207">Se o valor for <strong>VARIANT_TRUE</strong>, o decodificador deverá ser esgotado após uma descontinuidade.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-207">If the value is <strong>VARIANT_TRUE</strong>, the decoder should be drained after a discontinuity.</span></span> <span data-ttu-id="fdd9c-208">Para obter mais informações sobre como descarregar uma MFT, consulte <a href="basic-mft-processing-model.md">modelo básico de processamento de MFT</a>.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-208">For more information about draining an MFT, see <a href="basic-mft-processing-model.md">Basic MFT Processing Model</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fdd9c-209">Para consultar essa propriedade, use a interface <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="fdd9c-209">To query this property, use the <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> interface.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="fdd9c-210">Comentários</span><span class="sxs-lookup"><span data-stu-id="fdd9c-210">Remarks</span></span>

<span data-ttu-id="fdd9c-211">A resolução máxima permitida pelo decodificador do Windows Media Video 9 é 4096x4096.</span><span class="sxs-lookup"><span data-stu-id="fdd9c-211">The maximum resolution allowed by the Windows Media Video 9 decoder is 4096x4096.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdd9c-212">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdd9c-212">Requirements</span></span>



| <span data-ttu-id="fdd9c-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdd9c-213">Requirement</span></span> | <span data-ttu-id="fdd9c-214">Valor</span><span class="sxs-lookup"><span data-stu-id="fdd9c-214">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd9c-215">Cliente</span><span class="sxs-lookup"><span data-stu-id="fdd9c-215">Client</span></span><br/> | <span data-ttu-id="fdd9c-216">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="fdd9c-216">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="fdd9c-217">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fdd9c-217">Header</span></span><br/> | <dl> <span data-ttu-id="fdd9c-218"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdd9c-218"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="fdd9c-219">DLL</span><span class="sxs-lookup"><span data-stu-id="fdd9c-219">DLL</span></span><br/>    | <dl> <span data-ttu-id="fdd9c-220"><dt>Wmvdecod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdd9c-220"><dt>Wmvdecod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdd9c-221">Confira também</span><span class="sxs-lookup"><span data-stu-id="fdd9c-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdd9c-222">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="fdd9c-222">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="fdd9c-223">Implementação de codec</span><span class="sxs-lookup"><span data-stu-id="fdd9c-223">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 
