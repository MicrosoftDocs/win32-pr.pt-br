---
description: O codificador do Windows Media Video 7/8 implementa versões anteriores do codificador de vídeo do Windows Media.
ms.assetid: c4165614-b9ec-4216-b36c-f57bc05e3a8e
title: Codificador de vídeo 7/8 do Windows Media (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5467d02681ef319a508f6f6581e1f3c0191950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763489"
---
# <a name="windows-media-video-78-encoder"></a><span data-ttu-id="5073f-103">Codificador de vídeo 7/8 do Windows Media</span><span class="sxs-lookup"><span data-stu-id="5073f-103">Windows Media Video 7/8 Encoder</span></span>

<span data-ttu-id="5073f-104">O codificador do Windows Media Video 7/8 implementa versões anteriores do codificador de vídeo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5073f-104">The Windows Media Video 7/8 encoder implements previous versions of the Windows Media Video encoder.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="5073f-105">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="5073f-105">Class Identifier</span></span>

<span data-ttu-id="5073f-106">O CLSID (identificador de classe) do Windows Media Video 7/8 Encoder é **CLSID \_ CWMVXEncMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="5073f-106">The class identifier (CLSID) for the Windows Media Video 7/8 encoder is **CLSID\_CWMVXEncMediaObject**.</span></span> <span data-ttu-id="5073f-107">Você pode criar uma instância do codificador chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="5073f-107">You can create an instance of the encoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="5073f-108">Interfaces</span><span class="sxs-lookup"><span data-stu-id="5073f-108">Interfaces</span></span>

<span data-ttu-id="5073f-109">Um objeto de codificador de vídeo expõe a interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que o objeto possa ser usado como um objeto de mídia do DirectX (DMO) e expõe a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que o objeto possa ser usado como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="5073f-109">A video encoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="5073f-110">Um codificador de vídeo se comporta como um DMO ou um MFT dependendo de quais interfaces você obtém e qual versão do Windows está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="5073f-110">A video encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="5073f-111">A tabela a seguir mostra as condições sob as quais um codificador de vídeo se comporta como um DMO ou um MFT.</span><span class="sxs-lookup"><span data-stu-id="5073f-111">The following table shows the conditions under which a video encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="5073f-112">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="5073f-112">Operating system</span></span>            | <span data-ttu-id="5073f-113">Comportamento do codificador</span><span class="sxs-lookup"><span data-stu-id="5073f-113">Encoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5073f-114">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5073f-114">Windows XP</span></span>                  | <span data-ttu-id="5073f-115">Um codificador de vídeo do Windows Media sempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="5073f-115">A Windows Media video encoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="5073f-116">Windows Vista e Windows 7</span><span class="sxs-lookup"><span data-stu-id="5073f-116">Windows Vista and Windows 7</span></span> | <span data-ttu-id="5073f-117">Por padrão, um codificador de vídeo do Windows Media se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="5073f-117">By default, a Windows Media video encoder behaves as a DMO.</span></span> <span data-ttu-id="5073f-118">Se você obtiver uma interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) em um codificador de vídeo, ela se comporta como um MFT.</span><span class="sxs-lookup"><span data-stu-id="5073f-118">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video encoder, it behaves as an MFT.</span></span> |



 

## <a name="input-formats"></a><span data-ttu-id="5073f-119">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="5073f-119">Input Formats</span></span>

<span data-ttu-id="5073f-120">O codificador de vídeo do Windows Media dá suporte aos seguintes subtipos de mídia de entrada quando ele está agindo como DMO.</span><span class="sxs-lookup"><span data-stu-id="5073f-120">The Windows Media Video encoder supports the following input media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="5073f-121">MEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="5073f-121">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="5073f-122">MEDIASUBTYPE \_ I420</span><span class="sxs-lookup"><span data-stu-id="5073f-122">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="5073f-123">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="5073f-123">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="5073f-124">MEDIASUBTYPE \_ NV11</span><span class="sxs-lookup"><span data-stu-id="5073f-124">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="5073f-125">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="5073f-125">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="5073f-126">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="5073f-126">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="5073f-127">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="5073f-127">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="5073f-128">MEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="5073f-128">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="5073f-129">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="5073f-129">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="5073f-130">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="5073f-130">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="5073f-131">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="5073f-131">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="5073f-132">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="5073f-132">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="5073f-133">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="5073f-133">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="5073f-134">MEDIASUBTYPE \_ FOTOmotion</span><span class="sxs-lookup"><span data-stu-id="5073f-134">MEDIASUBTYPE\_PHOTOMOTION</span></span>

<span data-ttu-id="5073f-135">O codificador de vídeo do Windows Media dá suporte aos seguintes subtipos de mídia de entrada quando ele está atuando como um MFT.</span><span class="sxs-lookup"><span data-stu-id="5073f-135">The Windows Media Video encoder supports the following input media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="5073f-136">MFVideoFormat \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="5073f-136">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="5073f-137">MFVideoFormat \_ I420</span><span class="sxs-lookup"><span data-stu-id="5073f-137">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="5073f-138">MFVideoFormat \_ YV12</span><span class="sxs-lookup"><span data-stu-id="5073f-138">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="5073f-139">MFVideoFormat \_ NV11</span><span class="sxs-lookup"><span data-stu-id="5073f-139">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="5073f-140">MFVideoFormat \_ NV12</span><span class="sxs-lookup"><span data-stu-id="5073f-140">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="5073f-141">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="5073f-141">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="5073f-142">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="5073f-142">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="5073f-143">MFVideoFormat \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="5073f-143">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="5073f-144">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="5073f-144">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="5073f-145">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="5073f-145">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="5073f-146">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="5073f-146">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="5073f-147">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="5073f-147">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="5073f-148">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="5073f-148">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="5073f-149">MEDIASUBTYPE \_ FOTOmotion</span><span class="sxs-lookup"><span data-stu-id="5073f-149">MEDIASUBTYPE\_PHOTOMOTION</span></span>

## <a name="output-formats"></a><span data-ttu-id="5073f-150">Formatos de saída</span><span class="sxs-lookup"><span data-stu-id="5073f-150">Output Formats</span></span>

<span data-ttu-id="5073f-151">A tabela a seguir mostra os códigos de quatro caracteres (FOURCC) para os tipos de saída com suporte no codificador de vídeo 7/8 do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5073f-151">The following table shows the four-character codes (FOURCCs) for the output types supported by the Windows Media Video 7/8 encoder.</span></span>



| <span data-ttu-id="5073f-152">Category</span><span class="sxs-lookup"><span data-stu-id="5073f-152">Category</span></span>              | <span data-ttu-id="5073f-153">FOURCC</span><span class="sxs-lookup"><span data-stu-id="5073f-153">FOURCC</span></span> |
|-----------------------|--------|
| <span data-ttu-id="5073f-154">Windows Media Video 7</span><span class="sxs-lookup"><span data-stu-id="5073f-154">Windows Media Video 7</span></span> | <span data-ttu-id="5073f-155">"WMV1"</span><span class="sxs-lookup"><span data-stu-id="5073f-155">"WMV1"</span></span> |
| <span data-ttu-id="5073f-156">Vídeo do Windows Media 8</span><span class="sxs-lookup"><span data-stu-id="5073f-156">Windows Media Video 8</span></span> | <span data-ttu-id="5073f-157">"WMV2"</span><span class="sxs-lookup"><span data-stu-id="5073f-157">"WMV2"</span></span> |



 

## <a name="properties"></a><span data-ttu-id="5073f-158">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5073f-158">Properties</span></span>

<span data-ttu-id="5073f-159">O codificador do Windows Media Video 7/8 dá suporte às seguintes propriedades.</span><span class="sxs-lookup"><span data-stu-id="5073f-159">The Windows Media Video 7/8 encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5073f-160">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5073f-160">Property</span></span></th>
<th><span data-ttu-id="5073f-161">Descrição</span><span class="sxs-lookup"><span data-stu-id="5073f-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5073f-162"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-162"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="5073f-163">Especifica a sobrecarga, em bytes por pacote, necessária para o contêiner usado para armazenar o conteúdo compactado.</span><span class="sxs-lookup"><span data-stu-id="5073f-163">Specifies the overhead, in bytes per packet, required for the container used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="5073f-164">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-164">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-165">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="5073f-165">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5073f-166"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-166"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="5073f-167">Especifica a taxa média de quadros do conteúdo do vídeo, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="5073f-167">Specifies the average frame rate of video content, in frames per second.</span></span><br/> <dl> <span data-ttu-id="5073f-168">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-168">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-169">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5073f-169">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5073f-170"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-170"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="5073f-171">Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits variável restrita (VBR) em sua taxa média de bits (especificada por <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="5073f-171">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span></span><br/> <dl> <span data-ttu-id="5073f-172">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-172">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-173">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5073f-173">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5073f-174"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-174"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="5073f-175">Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits variável restrita (VBR) em sua taxa de bits de pico (especificada por <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="5073f-175">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span></span><br/> <dl> <span data-ttu-id="5073f-176">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-176">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-177">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5073f-177">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5073f-178"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-178"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span></span></td>
<td><span data-ttu-id="5073f-179">Especifica se o fluxo de bits de vídeo codificado contém um valor de total de buffer com cada quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="5073f-179">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="5073f-180">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-180">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-181">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5073f-181">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5073f-182"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-182"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="5073f-183">Especifica o número de quadros de vídeo codificados pelo codec.</span><span class="sxs-lookup"><span data-stu-id="5073f-183">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="5073f-184">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-184">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-185">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5073f-185">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5073f-186"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-186"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="5073f-187">Especifica o número de quadros de vídeo codificados pelo codec que realmente contêm dados.</span><span class="sxs-lookup"><span data-stu-id="5073f-187">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="5073f-188">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-188">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-189">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5073f-189">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5073f-190"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-190"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="5073f-191">Essa propriedade é substituída por <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5073f-191">This property is superseded by <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5073f-192"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-192"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span></span></td>
<td><span data-ttu-id="5073f-193">Especifica a complexidade do algoritmo do codificador.</span><span class="sxs-lookup"><span data-stu-id="5073f-193">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="5073f-194">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-194">Windows Vista and later.</span></span><br />
<span data-ttu-id="5073f-195">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="5073f-195">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5073f-196"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-196"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span></span></td>
<td><span data-ttu-id="5073f-197">Especifica uma representação numérica da compensação entre a suavidade de movimento e a qualidade da imagem na saída do codec.</span><span class="sxs-lookup"><span data-stu-id="5073f-197">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="5073f-198">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-198">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-199">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="5073f-199">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5073f-200"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-200"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="5073f-201">Especifica o modelo de conformidade do dispositivo para o qual o conteúdo codificado está em conformidade.</span><span class="sxs-lookup"><span data-stu-id="5073f-201">Specifies the device conformance template to which the encoded content conforms.</span></span><br/> <dl> <span data-ttu-id="5073f-202">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-202">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-203">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5073f-203">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5073f-204"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-204"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span></span></td>
<td><span data-ttu-id="5073f-205">Especifica o modelo de conformidade do dispositivo que você deseja usar para a codificação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5073f-205">Specifies the device conformance template that you want to use for video encoding.</span></span><br/> <dl> <span data-ttu-id="5073f-206">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-206">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-207">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="5073f-207">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5073f-208"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-208"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="5073f-209">Especifica o número de quadros de vídeo removidos durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="5073f-209">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="5073f-210">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-210">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-211">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5073f-211">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5073f-212"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-212"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="5073f-213">Especifica o fim de uma passagem de codificação.</span><span class="sxs-lookup"><span data-stu-id="5073f-213">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="5073f-214">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-214">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-215">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="5073f-215">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5073f-216"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-216"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span></span></td>
<td><span data-ttu-id="5073f-217">Especifica o FOURCC que identifica o codificador que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="5073f-217">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="5073f-218">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-218">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-219">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="5073f-219">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5073f-220"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-220"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span></span></td>
<td><span data-ttu-id="5073f-221">Especifica se a saída do codec será entrelaçada.</span><span class="sxs-lookup"><span data-stu-id="5073f-221">Specifies whether the codec output will be interlaced.</span></span><br/> <dl> <span data-ttu-id="5073f-222">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-222">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-223">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="5073f-223">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5073f-224"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-224"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span></span></td>
<td><span data-ttu-id="5073f-225">Especifica o tempo máximo, em milissegundos, entre os quadros-chave na saída do codec.</span><span class="sxs-lookup"><span data-stu-id="5073f-225">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="5073f-226">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-226">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-227">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="5073f-227">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5073f-228"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-228"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="5073f-229">Especifica o número máximo de passagens aceitas pelo codec.</span><span class="sxs-lookup"><span data-stu-id="5073f-229">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="5073f-230">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-230">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-231">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5073f-231">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5073f-232"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-232"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="5073f-233">Especifica o número de passagens que o codec usará para codificar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5073f-233">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="5073f-234">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-234">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-235">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5073f-235">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5073f-236"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-236"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="5073f-237">Especifica se o codificador produz entradas de quadro fictícias no fluxo de bits para quadros duplicados.</span><span class="sxs-lookup"><span data-stu-id="5073f-237">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span><br/> <dl> <span data-ttu-id="5073f-238">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-238">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-239">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="5073f-239">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5073f-240"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-240"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="5073f-241">Especifica QP.</span><span class="sxs-lookup"><span data-stu-id="5073f-241">Specifies QP.</span></span><br/> <dl> <span data-ttu-id="5073f-242">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-242">Windows Vista and later.</span></span><br />
<span data-ttu-id="5073f-243">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="5073f-243">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5073f-244"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-244"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="5073f-245">Especifica a taxa média de bits, em bits por segundo, usada para codificação de taxa de bits de variável (VBR) de 2 passagens.</span><span class="sxs-lookup"><span data-stu-id="5073f-245">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="5073f-246">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-246">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-247">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5073f-247">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5073f-248"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-248"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="5073f-249">Especifica a taxa de bits de pico, em bits por segundo, usada para taxa de bits variável restrita de 2 passagens (VBR).</span><span class="sxs-lookup"><span data-stu-id="5073f-249">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR).</span></span><br/> <dl> <span data-ttu-id="5073f-250">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-250">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-251">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5073f-251">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5073f-252"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-252"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="5073f-253">Especifica o número de quadros de vídeo passados para o codificador durante o processo de codificação.</span><span class="sxs-lookup"><span data-stu-id="5073f-253">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="5073f-254">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-254">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-255">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5073f-255">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5073f-256"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-256"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="5073f-257">Especifica se o codec usará a codificação de taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="5073f-257">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="5073f-258">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-258">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-259">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5073f-259">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5073f-260"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-260"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="5073f-261">Especifica o nível de qualidade real para codificação de taxa de bits de variável (VBR) com base na qualidade (1-passagem).</span><span class="sxs-lookup"><span data-stu-id="5073f-261">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="5073f-262">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-262">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-263">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="5073f-263">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5073f-264"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-264"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span></span></td>
<td><span data-ttu-id="5073f-265">Especifica a quantidade de conteúdo, em milissegundos, que pode caber no buffer de modelo.</span><span class="sxs-lookup"><span data-stu-id="5073f-265">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="5073f-266">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-266">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-267">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="5073f-267">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5073f-268"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="5073f-268"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="5073f-269">Especifica o número de quadros de vídeo que foram ignorados porque eles eram duplicatas de quadros anteriores.</span><span class="sxs-lookup"><span data-stu-id="5073f-269">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="5073f-270">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="5073f-270">Windows XP and later.</span></span><br />
<span data-ttu-id="5073f-271">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5073f-271">Read-only</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="5073f-272">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5073f-272">Requirements</span></span>



| <span data-ttu-id="5073f-273">Requisito</span><span class="sxs-lookup"><span data-stu-id="5073f-273">Requirement</span></span> | <span data-ttu-id="5073f-274">Valor</span><span class="sxs-lookup"><span data-stu-id="5073f-274">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5073f-275">Cliente</span><span class="sxs-lookup"><span data-stu-id="5073f-275">Client</span></span><br/> | <span data-ttu-id="5073f-276">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="5073f-276">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="5073f-277">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5073f-277">Header</span></span><br/> | <dl> <span data-ttu-id="5073f-278"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5073f-278"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="5073f-279">DLL</span><span class="sxs-lookup"><span data-stu-id="5073f-279">DLL</span></span><br/>    | <dl> <span data-ttu-id="5073f-280"><dt>Wmvxencd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5073f-280"><dt>Wmvxencd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5073f-281">Confira também</span><span class="sxs-lookup"><span data-stu-id="5073f-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5073f-282">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="5073f-282">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="5073f-283">Implementação de codec</span><span class="sxs-lookup"><span data-stu-id="5073f-283">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="5073f-284">GUIDs de subtipo de vídeo</span><span class="sxs-lookup"><span data-stu-id="5073f-284">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 
