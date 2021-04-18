---
description: O codificador do Windows Media Video 9 codificará fluxos de vídeo.
ms.assetid: 1d0a41bc-7f7c-4e25-860c-1108ab292951
title: Codificador do Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36ee5823c585d60ee74e75f99e8ec9b4d91f5cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772717"
---
# <a name="windows-media-video-9-encoder"></a><span data-ttu-id="3d4fa-103">Codificador do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="3d4fa-103">Windows Media Video 9 Encoder</span></span>

<span data-ttu-id="3d4fa-104">O codificador do Windows Media Video 9 codificará fluxos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-104">The Windows Media Video 9 encoder encodes video streams.</span></span> <span data-ttu-id="3d4fa-105">O codificador dá suporte às quatro categorias de saída codificadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-105">The encoder supports the following four categories of encoded output.</span></span>

-   <span data-ttu-id="3d4fa-106">Perfil simples do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="3d4fa-106">Windows Media Video 9 Simple Profile</span></span>
-   <span data-ttu-id="3d4fa-107">Perfil principal do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="3d4fa-107">Windows Media Video 9 Main Profile</span></span>
-   <span data-ttu-id="3d4fa-108">Perfil avançado do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="3d4fa-108">Windows Media Video 9 Advanced Profile</span></span>
-   <span data-ttu-id="3d4fa-109">Imagem do vídeo 9,1 do Windows Media</span><span class="sxs-lookup"><span data-stu-id="3d4fa-109">Windows Media Video 9.1 Image</span></span>

## <a name="class-identifier"></a><span data-ttu-id="3d4fa-110">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="3d4fa-110">Class Identifier</span></span>

<span data-ttu-id="3d4fa-111">O CLSID (identificador de classe) para o codificador de vídeo do Windows Media é representado pela constante **CLSID \_ CWMV9EncMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-111">The class identifier (CLSID) for the Windows Media Video encoder is represented by the constant **CLSID\_CWMV9EncMediaObject**.</span></span> <span data-ttu-id="3d4fa-112">Você pode criar uma instância do codificador de vídeo chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-112">You can create an instance of the video encoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="3d4fa-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="3d4fa-113">Interfaces</span></span>

<span data-ttu-id="3d4fa-114">Um objeto de codificador de vídeo expõe a interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que o objeto possa ser usado como um objeto de mídia do DirectX (DMO) e expõe a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que o objeto possa ser usado como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="3d4fa-114">A video encoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="3d4fa-115">Um codificador de vídeo se comporta como um DMO ou um MFT dependendo de quais interfaces você obtém e qual versão do Windows está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-115">A video encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="3d4fa-116">A tabela a seguir mostra as condições sob as quais um codificador de vídeo se comporta como um DMO ou um MFT.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-116">The following table shows the conditions under which a video encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="3d4fa-117">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="3d4fa-117">Operating system</span></span>            | <span data-ttu-id="3d4fa-118">Comportamento do codificador</span><span class="sxs-lookup"><span data-stu-id="3d4fa-118">Encoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d4fa-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3d4fa-119">Windows XP</span></span>                  | <span data-ttu-id="3d4fa-120">Um codificador de vídeo do Windows Media sempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-120">A Windows Media video encoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="3d4fa-121">Windows Vista e Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d4fa-121">Windows Vista and Windows 7</span></span> | <span data-ttu-id="3d4fa-122">Por padrão, um codificador de vídeo do Windows Media se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-122">By default, a Windows Media video encoder behaves as a DMO.</span></span> <span data-ttu-id="3d4fa-123">Se você obtiver uma interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) em um codificador de vídeo, ela se comporta como um MFT.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-123">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video encoder, it behaves as an MFT.</span></span> |



 

## <a name="input-formats"></a><span data-ttu-id="3d4fa-124">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="3d4fa-124">Input Formats</span></span>

<span data-ttu-id="3d4fa-125">O codificador de vídeo do Windows Media dá suporte aos seguintes subtipos de mídia de entrada quando ele está agindo como DMO.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-125">The Windows Media Video encoder supports the following input media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="3d4fa-126">MEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="3d4fa-126">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="3d4fa-127">MEDIASUBTYPE \_ I420</span><span class="sxs-lookup"><span data-stu-id="3d4fa-127">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="3d4fa-128">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="3d4fa-128">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="3d4fa-129">MEDIASUBTYPE \_ NV11</span><span class="sxs-lookup"><span data-stu-id="3d4fa-129">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="3d4fa-130">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="3d4fa-130">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="3d4fa-131">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="3d4fa-131">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="3d4fa-132">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="3d4fa-132">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="3d4fa-133">MEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="3d4fa-133">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="3d4fa-134">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="3d4fa-134">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="3d4fa-135">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="3d4fa-135">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="3d4fa-136">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="3d4fa-136">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="3d4fa-137">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="3d4fa-137">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="3d4fa-138">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="3d4fa-138">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="3d4fa-139">MEDIASUBTYPE \_ FOTOmotion</span><span class="sxs-lookup"><span data-stu-id="3d4fa-139">MEDIASUBTYPE\_PHOTOMOTION</span></span>

<span data-ttu-id="3d4fa-140">O codificador de vídeo do Windows Media dá suporte aos seguintes subtipos de mídia de entrada quando ele está atuando como um MFT.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-140">The Windows Media Video encoder supports the following input media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="3d4fa-141">MFVideoFormat \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="3d4fa-141">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="3d4fa-142">MFVideoFormat \_ I420</span><span class="sxs-lookup"><span data-stu-id="3d4fa-142">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="3d4fa-143">MFVideoFormat \_ YV12</span><span class="sxs-lookup"><span data-stu-id="3d4fa-143">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="3d4fa-144">MFVideoFormat \_ NV11</span><span class="sxs-lookup"><span data-stu-id="3d4fa-144">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="3d4fa-145">MFVideoFormat \_ NV12</span><span class="sxs-lookup"><span data-stu-id="3d4fa-145">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="3d4fa-146">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="3d4fa-146">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="3d4fa-147">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="3d4fa-147">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="3d4fa-148">MFVideoFormat \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="3d4fa-148">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="3d4fa-149">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="3d4fa-149">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="3d4fa-150">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="3d4fa-150">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="3d4fa-151">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="3d4fa-151">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="3d4fa-152">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="3d4fa-152">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="3d4fa-153">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="3d4fa-153">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="3d4fa-154">MEDIASUBTYPE \_ FOTOmotion</span><span class="sxs-lookup"><span data-stu-id="3d4fa-154">MEDIASUBTYPE\_PHOTOMOTION</span></span>

## <a name="output-formats"></a><span data-ttu-id="3d4fa-155">Formatos de saída</span><span class="sxs-lookup"><span data-stu-id="3d4fa-155">Output Formats</span></span>

<span data-ttu-id="3d4fa-156">A tabela a seguir mostra os códigos de quatro caracteres (FOURCC) que correspondem às categorias de saída codificada.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-156">The following table shows the four-character codes (FOURCCs) that correspond to the categories of encoded output.</span></span>



| <span data-ttu-id="3d4fa-157">Categoria</span><span class="sxs-lookup"><span data-stu-id="3d4fa-157">Category</span></span>                               | <span data-ttu-id="3d4fa-158">FOURCC</span><span class="sxs-lookup"><span data-stu-id="3d4fa-158">FOURCC</span></span>                                   |
|----------------------------------------|------------------------------------------|
| <span data-ttu-id="3d4fa-159">Perfil simples do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="3d4fa-159">Windows Media Video 9 Simple Profile</span></span>   | <span data-ttu-id="3d4fa-160">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="3d4fa-160">"WMV3"</span></span>                                   |
| <span data-ttu-id="3d4fa-161">Perfil principal do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="3d4fa-161">Windows Media Video 9 Main Profile</span></span>     | <span data-ttu-id="3d4fa-162">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="3d4fa-162">"WMV3"</span></span>                                   |
| <span data-ttu-id="3d4fa-163">Perfil avançado do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="3d4fa-163">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="3d4fa-164">"WVC1"</span><span class="sxs-lookup"><span data-stu-id="3d4fa-164">"WVC1"</span></span>                                   |
| <span data-ttu-id="3d4fa-165">Imagem do vídeo 9,1 do Windows Media</span><span class="sxs-lookup"><span data-stu-id="3d4fa-165">Windows Media Video 9.1 Image</span></span>          | <span data-ttu-id="3d4fa-166">"WMVP" para 9,1, "WVP2" para 9,1 versão 2</span><span class="sxs-lookup"><span data-stu-id="3d4fa-166">"WMVP" for 9.1, "WVP2" for 9.1 version 2</span></span> |



 

<span data-ttu-id="3d4fa-167">Para distinguir entre perfil simples e perfil principal, defina a propriedade [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="3d4fa-167">To distinguish between Simple Profile and Main Profile, set the [**MFPKEY\_DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) property.</span></span>

## <a name="properties"></a><span data-ttu-id="3d4fa-168">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3d4fa-168">Properties</span></span>

<span data-ttu-id="3d4fa-169">O codificador do Windows Media Video 9 dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-169">The Windows Media Video 9 encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3d4fa-170">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3d4fa-170">Property</span></span></th>
<th><span data-ttu-id="3d4fa-171">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d4fa-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d4fa-172"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-172"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-173">Especifica a sobrecarga, em bytes por pacote, necessária para o contêiner usado para armazenar o conteúdo compactado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-173">Specifies the overhead, in bytes per packet, required for the container used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="3d4fa-174">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-174">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-175">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-175">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-176">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-177"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-177"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-178">Especifica a taxa média de quadros do conteúdo do vídeo, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-178">Specifies the average frame rate of video content, in frames per second.</span></span><br/> <dl> <span data-ttu-id="3d4fa-179">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-179">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-180">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-180">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-181">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-181">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-182"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-182"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-183">Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits variável restrita (VBR) em sua taxa média de bits (especificada por <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="3d4fa-183">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span></span><br/> <dl> <span data-ttu-id="3d4fa-184">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-184">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-185">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-185">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-186">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-186">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-187"><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-187"><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-188">Especifica o aumento Delta entre a imagem quantizador do quadro âncora e a quantizador da imagem do quadro B.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-188">Specifies the delta increase between the picture quantizer of the anchor frame and the picture quantizer of the B-frame.</span></span><br/> <dl> <span data-ttu-id="3d4fa-189">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-189">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-190">Perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-190">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-191">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-191">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-192"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-192"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-193">Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits variável restrita (VBR) em sua taxa de bits de pico (especificada por <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="3d4fa-193">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span></span><br/> <dl> <span data-ttu-id="3d4fa-194">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-194">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-195">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-195">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-196">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-196">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-197"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-197"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-198">Especifica se o fluxo de bits de vídeo codificado contém um valor de total de buffer com cada quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-198">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="3d4fa-199">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-199">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-200">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-200">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-201">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-201">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-202"><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-202"><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-203">Especifica o padrão de codificação a ser usado no início de um grupo de imagens.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-203">Specifies the encoding pattern to use at the beginning of a group of pictures.</span></span><br/> <dl> <span data-ttu-id="3d4fa-204">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-204">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d4fa-205">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-205">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-206">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-206">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-207"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-207"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-208">Especifica o número de quadros de vídeo codificados pelo codec.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-208">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="3d4fa-209">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-209">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-210">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-210">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-211">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-211">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-212"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-212"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-213">Especifica o número de quadros de vídeo codificados pelo codec que realmente contêm dados.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-213">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="3d4fa-214">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-214">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-215">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-215">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-216">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-216">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-217"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-217"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-218">Essa propriedade é substituída por <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-218">This property is superseded by <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-219"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-219"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-220">Especifica a complexidade do algoritmo do codificador.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-220">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="3d4fa-221">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-221">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d4fa-222">Perfil simples, perfil principal.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-222">Simple Profile, Main Profile.</span></span> <span data-ttu-id="3d4fa-223">Perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-223">Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-224">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-224">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-225"><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-225"><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-226">Especifica o tipo de otimização a ser usado para o codec de perfil avançado do Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-226">Specifies the type of optimization to use for the Windows Media Video 9 Advanced Profile codec.</span></span><br/> <dl> <span data-ttu-id="3d4fa-227">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-227">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-228">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-228">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-229">Gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-229">Write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-230"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-230"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-231">Especifica uma representação numérica da compensação entre a suavidade de movimento e a qualidade da imagem na saída do codec.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-231">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="3d4fa-232">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-232">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-233">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-233">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-234">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-234">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-235"><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-235"><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-236">Não usado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-236">Not used.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-237"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-237"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-238">Especifica o modelo de conformidade do dispositivo para o qual o conteúdo codificado está em conformidade.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-238">Specifies the device conformance template to which the encoded content conforms.</span></span><br/> <dl> <span data-ttu-id="3d4fa-239">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-239">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-240">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-240">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-241">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-241">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-242"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-242"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-243">Especifica o modelo de conformidade do dispositivo que você deseja usar para a codificação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-243">Specifies the device conformance template that you want to use for video encoding.</span></span><br/> <dl> <span data-ttu-id="3d4fa-244">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-244">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-245">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-245">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-246">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-246">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-247"><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-247"><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-248">Especifica o método usado para codificar as informações de vetor de movimento.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-248">Specifies the method used to encode the motion vector information.</span></span><br/> <dl> <span data-ttu-id="3d4fa-249">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-249">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-250">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-250">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-251">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-251">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-252"><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-252"><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-253">Especifica se o codec usará o filtro de ruído durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-253">Specifies whether the codec will use the noise filter when encoding.</span></span><br/> <dl> <span data-ttu-id="3d4fa-254">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-254">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-255">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-255">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-256">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-256">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-257"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-257"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-258">Especifica o nível de qualidade desejado para codificação de taxa de bits de variável (VBR) com base na qualidade (1-passagem).</span><span class="sxs-lookup"><span data-stu-id="3d4fa-258">Specifies the desired quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="3d4fa-259">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-259">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d4fa-260">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-260">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-261">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-261">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-262"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-262"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-263">Especifica o número de quadros de vídeo removidos durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-263">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="3d4fa-264">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-264">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-265">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-265">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-266">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-266">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-267"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-267"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-268">Especifica o fim de uma passagem de codificação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-268">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="3d4fa-269">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-269">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-270">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-270">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-271">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-271">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-272"><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-272"><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-273">Especifica uma altura intermediária de quadro para vídeo codificado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-273">Specifies an intermediate frame height for encoded video.</span></span><br/> <dl> <span data-ttu-id="3d4fa-274">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-274">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-275">Perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-275">Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-276">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-276">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-277"><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-277"><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-278">Especifica uma largura de quadro intermediária para o vídeo codificado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-278">Specifies an intermediate frame width for encoded video.</span></span><br/> <dl> <span data-ttu-id="3d4fa-279">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-279">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-280">Perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-280">Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-281">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-281">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-282"><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-282"><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-283">Especifica se o codec deve usar a filtragem mediana durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-283">Specifies whether the codec should use median filtering during encoding.</span></span><br/> <dl> <span data-ttu-id="3d4fa-284">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-284">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-285">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-285">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-286">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-286">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-287"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-287"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-288">Especifica o FOURCC que identifica o codificador que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-288">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="3d4fa-289">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-289">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-290">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-290">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-291">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-291">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-292"><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-292"><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-293">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-293">Obsolete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-294"><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-294"><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-295">Especifica se o codificador tem permissão para descartar quadros.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-295">Specifies whether the encoder is allowed to drop frames.</span></span><br/> <dl> <span data-ttu-id="3d4fa-296">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-296">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-297">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-297">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-298">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-298">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-299"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-299"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-300">Especifica se a saída do codec será entrelaçada.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-300">Specifies whether the codec output will be interlaced.</span></span><br/> <dl> <span data-ttu-id="3d4fa-301">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-301">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-302">Perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-302">Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-303">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-303">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-304"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-304"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-305">Especifica o tempo máximo, em milissegundos, entre os quadros-chave na saída do codec.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-305">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="3d4fa-306">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-306">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-307">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-307">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-308">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-308">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-309"><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-309"><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-310">Não usado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-310">Not used.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-311"><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-311"><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-312">Especifica o número de quadros após o quadro atual que o codec avaliará antes de codificar o quadro atual.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-312">Specifies the number of frames after the current frame that the codec will evaluate before encoding the current frame.</span></span><br/> <dl> <span data-ttu-id="3d4fa-313">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-313">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-314">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-314">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-315">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-315">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-316"><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-316"><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-317">Especifica se o codec deve usar o filtro de desbloqueio no loop durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-317">Specifies whether the codec should use the in-loop deblocking filter during encoding.</span></span><br/> <dl> <span data-ttu-id="3d4fa-318">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-318">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-319">Perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-319">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-320">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-320">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-321"><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-321"><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-322">Especifica o método de custo usado pelo codec para determinar qual modo de macrobloco usar.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-322">Specifies the cost method used by the codec to determine which macroblock mode to use.</span></span><br/> <dl> <span data-ttu-id="3d4fa-323">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-323">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-324">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-324">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-325">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-325">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-326"><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-326"><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-327">Especifica o método a ser usado para a correspondência de movimento.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-327">Specifies the method to use for motion matching.</span></span><br/> <dl> <span data-ttu-id="3d4fa-328">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-328">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-329">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-329">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-330">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-330">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-331"><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-331"><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-332">Especifica os tipos de informações de vídeo que são usadas em operações de pesquisa de movimento.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-332">Specifies the types of video information that are used in motion search operations.</span></span><br/> <dl> <span data-ttu-id="3d4fa-333">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-333">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-334">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-334">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-335">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-335">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-336"><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-336"><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-337">Especifica o intervalo usado em pesquisas de movimento.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-337">Specifies the range used in motion searches.</span></span><br/> <dl> <span data-ttu-id="3d4fa-338">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-338">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-339">Perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-339">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-340">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-340">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-341"><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-341"><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-342">Especifica se o codec deve tentar detectar bordas de quadro ruidosas e removê-las.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-342">Specifies whether the codec should attempt to detect noisy frame edges and remove them.</span></span><br/> <dl> <span data-ttu-id="3d4fa-343">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-343">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-344">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-344">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-345">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-345">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-346"><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-346"><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-347">Especifica o número de quadros de previsão bidirecionais (quadros B).</span><span class="sxs-lookup"><span data-stu-id="3d4fa-347">Specifies the number of bidirectional predictive frames (B-frames).</span></span><br/> <dl> <span data-ttu-id="3d4fa-348">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-348">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-349">Perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-349">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-350">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-350">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-351"><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-351"><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-352">Especifica o número de threads que o codec usará para codificação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-352">Specifies the number of threads that the codec will use for encoding.</span></span><br/> <dl> <span data-ttu-id="3d4fa-353">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-353">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-354">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-354">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-355">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-355">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-356"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-356"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-357">Especifica o número máximo de passagens aceitas pelo codec.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-357">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="3d4fa-358">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-358">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-359">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-359">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-360">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-360">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-361"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-361"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-362">Especifica o número de passagens que o codec usará para codificar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-362">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="3d4fa-363">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-363">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-364">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-364">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-365">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-365">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-366"><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-366"><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-367">Especifica se o codec deve usar a otimização de perceptiva conservadora durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-367">Specifies whether the codec should use conservative perceptual optimization when encoding.</span></span><br/> <dl> <span data-ttu-id="3d4fa-368">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-368">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-369">Perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-369">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-370">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-370">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-371"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-371"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-372">Especifica se o codificador produz entradas de quadro fictícias no fluxo de bits para quadros duplicados.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-372">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span><br/> <dl> <span data-ttu-id="3d4fa-373">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-373">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-374">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-374">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-375">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-375">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-376"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-376"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-377">Especifica QP.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-377">Specifies QP.</span></span><br/> <dl> <span data-ttu-id="3d4fa-378">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-378">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d4fa-379">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-379">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-380">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-380">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-381"><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-381"><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-382">Especifica o grau para o qual o codec deve reduzir o intervalo de cores efetivo do vídeo.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-382">Specifies the degree to which the codec should reduce the effective color range of the video.</span></span><br/> <dl> <span data-ttu-id="3d4fa-383">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-383">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-384">Perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-384">Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-385">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-385">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-386"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-386"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-387">Especifica a taxa média de bits, em bits por segundo, usada para codificação de taxa de bits de variável (VBR) de 2 passagens.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-387">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="3d4fa-388">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-388">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-389">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-389">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-390">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-390">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-391"><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-391"><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-392">Especifica se o codificador usa a pesquisa MV de sub-pixel baseada em RD.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-392">Specifies whether the encoder uses RD-based sub-pixel MV search.</span></span> <br/> <dl> <span data-ttu-id="3d4fa-393">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-393">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-394">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-394">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-395">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-395">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-396"><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-396"><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-397">Para nova codificação de segmento, especifica o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-397">For segment re-encoding, specifies the buffer size.</span></span><br/> <dl> <span data-ttu-id="3d4fa-398">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-398">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d4fa-399">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-399">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-400">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-400">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-401"><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-401"><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-402">Para a recodificação de segmento, especifica a duração do segmento a ser codificado novamente.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-402">For segment re-encoding, specifies the duration of the segment to be re-encoded.</span></span><br/> <dl> <span data-ttu-id="3d4fa-403">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-403">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d4fa-404">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-404">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-405">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-405">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-406"><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-406"><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-407">Para a recodificação de segmento, especifica o quantizador do quadro antes do segmento inicial.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-407">For segment re-encoding, specifies the quantizer of the frame prior to the starting segment.</span></span><br/> <dl> <span data-ttu-id="3d4fa-408">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-408">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d4fa-409">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-409">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-410">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-410">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-411"><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-411"><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-412">Para a recodificação de segmento, especifica a totalidade do buffer inicial.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-412">For segment re-encoding, specifies the starting buffer fullness.</span></span><br/> <dl> <span data-ttu-id="3d4fa-413">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-413">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d4fa-414">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-414">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-415">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-415">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-416"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-416"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-417">Especifica a taxa de bits de pico, em bits por segundo, usada para taxa de bits variável restrita de 2 passagens (VBR).</span><span class="sxs-lookup"><span data-stu-id="3d4fa-417">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR).</span></span><br/> <dl> <span data-ttu-id="3d4fa-418">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-418">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-419">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-419">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-420">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-420">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-421"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-421"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-422">Especifica o número de quadros de vídeo passados para o codificador durante o processo de codificação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-422">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="3d4fa-423">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-423">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-424">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-424">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-425">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-425">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-426"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-426"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-427">Especifica se o codec usará a codificação de taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="3d4fa-427">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="3d4fa-428">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-428">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-429">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-429">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-430">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-430">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-431"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-431"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-432">Especifica o nível de qualidade real para codificação de taxa de bits de variável (VBR) com base na qualidade (1-passagem).</span><span class="sxs-lookup"><span data-stu-id="3d4fa-432">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="3d4fa-433">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-433">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-434">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-434">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-435">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-435">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-436"><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-436"><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-437">Especifica se o codec usará a otimização de escala de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-437">Specifies whether the codec will use video scaling optimization.</span></span><br/> <dl> <span data-ttu-id="3d4fa-438">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-438">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-439">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-439">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-440">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-440">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-441"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-441"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-442">Especifica a quantidade de conteúdo, em milissegundos, que pode caber no buffer de modelo.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-442">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="3d4fa-443">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-443">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-444">Perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-444">Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-445">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-445">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-446"><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-446"><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-447">Para a recodificação de segmento, especifica os dados privados do codec do arquivo que está sendo codificado novamente.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-447">For segment re-encoding, specifies the codec private data of the file that is being re-encoded.</span></span><br/> <dl> <span data-ttu-id="3d4fa-448">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-448">Windows Vista and later.</span></span><br />
<span data-ttu-id="3d4fa-449">Perfil simples, perfil principal, perfil avançado, imagem.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-449">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="3d4fa-450">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-450">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d4fa-451"><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-451"><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-452">Especifica o tipo de lógica que o codec usará para detectar o vídeo de origem entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-452">Specifies the type of logic that the codec will use to detect interlaced source video.</span></span><br/> <dl> <span data-ttu-id="3d4fa-453">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-453">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-454">Perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-454">Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-455">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-455">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d4fa-456"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d4fa-456"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="3d4fa-457">Especifica o número de quadros de vídeo que foram ignorados porque eles eram duplicatas de quadros anteriores.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-457">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="3d4fa-458">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-458">Windows XP and later.</span></span><br />
<span data-ttu-id="3d4fa-459">Perfil simples, perfil principal, perfil avançado.</span><span class="sxs-lookup"><span data-stu-id="3d4fa-459">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="3d4fa-460">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d4fa-460">Read-only</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="3d4fa-461">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d4fa-461">Requirements</span></span>



| <span data-ttu-id="3d4fa-462">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d4fa-462">Requirement</span></span> | <span data-ttu-id="3d4fa-463">Valor</span><span class="sxs-lookup"><span data-stu-id="3d4fa-463">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d4fa-464">Cliente</span><span class="sxs-lookup"><span data-stu-id="3d4fa-464">Client</span></span><br/> | <span data-ttu-id="3d4fa-465">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d4fa-465">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="3d4fa-466">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3d4fa-466">Header</span></span><br/> | <dl> <span data-ttu-id="3d4fa-467"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d4fa-467"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="3d4fa-468">DLL</span><span class="sxs-lookup"><span data-stu-id="3d4fa-468">DLL</span></span><br/>    | <dl> <span data-ttu-id="3d4fa-469"><dt>Wmvencod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d4fa-469"><dt>Wmvencod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d4fa-470">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d4fa-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d4fa-471">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="3d4fa-471">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="3d4fa-472">Implementação de codec</span><span class="sxs-lookup"><span data-stu-id="3d4fa-472">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 
