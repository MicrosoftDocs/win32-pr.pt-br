---
description: Este tópico fornece informações sobre o codec TIFF nativo disponível por meio do Windows Imaging Component (WIC).
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Visão geral do formato TIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db603857da892d4b699bb7df7d8b3e2ee5566326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781448"
---
# <a name="tiff-format-overview"></a><span data-ttu-id="643d6-103">Visão geral do formato TIFF</span><span class="sxs-lookup"><span data-stu-id="643d6-103">TIFF Format Overview</span></span>

<span data-ttu-id="643d6-104">Este tópico fornece informações sobre o codec TIFF nativo disponível por meio do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="643d6-104">This topic provides information about the native TIFF codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="643d6-105">Identidade do codec</span><span class="sxs-lookup"><span data-stu-id="643d6-105">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="643d6-106">Codificação</span><span class="sxs-lookup"><span data-stu-id="643d6-106">Encoding</span></span>](#encoding)
    -   [<span data-ttu-id="643d6-107">Opções de codificador</span><span class="sxs-lookup"><span data-stu-id="643d6-107">Encoder Options</span></span>](#encoder-options)
-   [<span data-ttu-id="643d6-108">Decodificação</span><span class="sxs-lookup"><span data-stu-id="643d6-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="643d6-109">Identidade do codec</span><span class="sxs-lookup"><span data-stu-id="643d6-109">Codec Identity</span></span>

<span data-ttu-id="643d6-110">A tabela a seguir fornece informações de identificação do codec.</span><span class="sxs-lookup"><span data-stu-id="643d6-110">The following table provides codec identification information.</span></span>



|                        |                                 |
|------------------------|---------------------------------|
| <span data-ttu-id="643d6-111">Nome (s) formal (es)</span><span class="sxs-lookup"><span data-stu-id="643d6-111">Formal Name(s)</span></span>         | <span data-ttu-id="643d6-112">TIFF</span><span class="sxs-lookup"><span data-stu-id="643d6-112">Tagged Image File Format (TIFF)</span></span> |
| <span data-ttu-id="643d6-113">Extensão (s) de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="643d6-113">File Name Extension(s)</span></span> | <span data-ttu-id="643d6-114">TIFF, TIF</span><span class="sxs-lookup"><span data-stu-id="643d6-114">tiff, tif</span></span>                       |
| <span data-ttu-id="643d6-115">Tipo (s) MIME</span><span class="sxs-lookup"><span data-stu-id="643d6-115">MIME type(s)</span></span>           | <span data-ttu-id="643d6-116">imagem/TIFF, imagem/TIF</span><span class="sxs-lookup"><span data-stu-id="643d6-116">image/tiff, image/tif</span></span>           |
| <span data-ttu-id="643d6-117">Suporte à especificação</span><span class="sxs-lookup"><span data-stu-id="643d6-117">Specification Support</span></span>  | <span data-ttu-id="643d6-118">Especificação TIFF 6,0</span><span class="sxs-lookup"><span data-stu-id="643d6-118">TIFF Specification 6.0</span></span>          |



 

<span data-ttu-id="643d6-119">A tabela a seguir lista os GUIDs usados para identificar os componentes do codec TIFF nativo.</span><span class="sxs-lookup"><span data-stu-id="643d6-119">The following table lists the GUIDs used to identify the native TIFF codec components.</span></span>



| <span data-ttu-id="643d6-120">Componente</span><span class="sxs-lookup"><span data-stu-id="643d6-120">Component</span></span>        | <span data-ttu-id="643d6-121">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="643d6-121">Friendly Name</span></span>             | <span data-ttu-id="643d6-122">GUID</span><span class="sxs-lookup"><span data-stu-id="643d6-122">GUID</span></span>                                 |
|------------------|---------------------------|--------------------------------------|
| <span data-ttu-id="643d6-123">Formato do contêiner</span><span class="sxs-lookup"><span data-stu-id="643d6-123">Container Format</span></span> | <span data-ttu-id="643d6-124">\_CONTAINERFORMATTIFF GUID</span><span class="sxs-lookup"><span data-stu-id="643d6-124">GUID\_ContainerFormatTiff</span></span> | <span data-ttu-id="643d6-125">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span><span class="sxs-lookup"><span data-stu-id="643d6-125">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span></span>  |
| <span data-ttu-id="643d6-126">Decodificador</span><span class="sxs-lookup"><span data-stu-id="643d6-126">Decoder</span></span>          | <span data-ttu-id="643d6-127">\_WICTIFFDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="643d6-127">CLSID\_WICTiffDecoder</span></span>     | <span data-ttu-id="643d6-128">b54e85d9-fe23-499f-8b886acea7137502b</span><span class="sxs-lookup"><span data-stu-id="643d6-128">b54e85d9-fe23-499f-8b886acea7137502b</span></span> |
| <span data-ttu-id="643d6-129">Codificador</span><span class="sxs-lookup"><span data-stu-id="643d6-129">Encoder</span></span>          | <span data-ttu-id="643d6-130">\_WICTIFFENCODER CLSID</span><span class="sxs-lookup"><span data-stu-id="643d6-130">CLSID\_WICTiffEncoder</span></span>     | <span data-ttu-id="643d6-131">0131be10-2001-4c5f-a9b0cc88fab64ce8</span><span class="sxs-lookup"><span data-stu-id="643d6-131">0131be10-2001-4c5f-a9b0cc88fab64ce8</span></span>  |



 

## <a name="encoding"></a><span data-ttu-id="643d6-132">Codificação</span><span class="sxs-lookup"><span data-stu-id="643d6-132">Encoding</span></span>

<span data-ttu-id="643d6-133">A API de codificação do WIC é projetada para ser independente de codec e a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="643d6-133">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="643d6-134">Para obter mais informações sobre codificação de imagem usando a API do WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="643d6-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="643d6-135">Opções de codificador</span><span class="sxs-lookup"><span data-stu-id="643d6-135">Encoder Options</span></span>

<span data-ttu-id="643d6-136">Os codecs habilitados para WIC diferem no nível de opção de codificação.</span><span class="sxs-lookup"><span data-stu-id="643d6-136">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="643d6-137">As opções de codificador refletem os recursos de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador.</span><span class="sxs-lookup"><span data-stu-id="643d6-137">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="643d6-138">As opções de codificador podem ser opções básicas compatíveis com o WIC disponíveis para todos os códigos habilitados para WIC (embora não sejam necessariamente suportados) ou opções específicas de codec projetadas pelo codec de formato de imagem.</span><span class="sxs-lookup"><span data-stu-id="643d6-138">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="643d6-139">Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="643d6-139">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="643d6-140">Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="643d6-140">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="643d6-141">O codec TIFF usa opções básicas de WIC.</span><span class="sxs-lookup"><span data-stu-id="643d6-141">The TIFF codec uses basic WIC options.</span></span> <span data-ttu-id="643d6-142">A tabela a seguir lista as opções de codificador do WIC com suporte do codec TIFF nativo.</span><span class="sxs-lookup"><span data-stu-id="643d6-142">The following table lists the WIC encoder options supported by the native TIFF codec.</span></span>

| <span data-ttu-id="643d6-143">Nome da Propriedade</span><span class="sxs-lookup"><span data-stu-id="643d6-143">Property Name</span></span>         | <span data-ttu-id="643d6-144">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="643d6-144">VARTYPE</span></span> | <span data-ttu-id="643d6-145">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="643d6-145">Value Range</span></span> | <span data-ttu-id="643d6-146">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="643d6-146">Default Value</span></span>    |
|-----------------------|---------|-------------|------------------|
| <span data-ttu-id="643d6-147">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="643d6-147">CompressionQuality</span></span>    | <span data-ttu-id="643d6-148">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="643d6-148">VT\_R4</span></span>  | <span data-ttu-id="643d6-149">0-1,0</span><span class="sxs-lookup"><span data-stu-id="643d6-149">0 - 1.0</span></span>     | <span data-ttu-id="643d6-150">0</span><span class="sxs-lookup"><span data-stu-id="643d6-150">0</span></span>                |
| <span data-ttu-id="643d6-151">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="643d6-151">TiffCompressionMethod</span></span> | <span data-ttu-id="643d6-152">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="643d6-152">VT\_UI1</span></span> | [<span data-ttu-id="643d6-153">**WICTiffCompressionOption**</span><span class="sxs-lookup"><span data-stu-id="643d6-153">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [<span data-ttu-id="643d6-154">**WICTiffCompressionDontCare**</span><span class="sxs-lookup"><span data-stu-id="643d6-154">**WICTiffCompressionDontCare**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

<span data-ttu-id="643d6-155">Se uma opção de codificador estiver presente na lista de opções de [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) para a qual o codec não dá suporte, ela será ignorada.</span><span class="sxs-lookup"><span data-stu-id="643d6-155">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="compressionquality-option"></a><span data-ttu-id="643d6-156">Opção CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="643d6-156">CompressionQuality Option</span></span>

<span data-ttu-id="643d6-157">Especifica a qualidade de compactação desejada.</span><span class="sxs-lookup"><span data-stu-id="643d6-157">Specifies the desired compression quality.</span></span> <span data-ttu-id="643d6-158">0,0 indica o esquema de compactação menos eficiente disponível.</span><span class="sxs-lookup"><span data-stu-id="643d6-158">0.0 indicates the least efficient compression scheme available.</span></span> <span data-ttu-id="643d6-159">Normalmente, esse esquema resulta em uma codificação mais rápida, mas uma saída maior.</span><span class="sxs-lookup"><span data-stu-id="643d6-159">Typically, this scheme results in a faster encode but larger output.</span></span> <span data-ttu-id="643d6-160">Um valor de 1,0 especifica o esquema de compactação mais eficiente disponível.</span><span class="sxs-lookup"><span data-stu-id="643d6-160">A value of 1.0 specifies the most efficient compression scheme available.</span></span> <span data-ttu-id="643d6-161">Normalmente, esse esquema resulta em uma codificação mais longa, mas produz uma saída menor.</span><span class="sxs-lookup"><span data-stu-id="643d6-161">Typically, this scheme results in a longer encode but produces smaller output.</span></span>

<span data-ttu-id="643d6-162">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="643d6-162">The default value is 0.</span></span>

### <a name="tiffcompressionmethod-option"></a><span data-ttu-id="643d6-163">Opção TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="643d6-163">TiffCompressionMethod Option</span></span>

<span data-ttu-id="643d6-164">Especifica o método de compactação TIFF.</span><span class="sxs-lookup"><span data-stu-id="643d6-164">Specifies the TIFF compression method.</span></span>

<span data-ttu-id="643d6-165">O valor padrão é [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span><span class="sxs-lookup"><span data-stu-id="643d6-165">The default value is [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span></span>

## <a name="decoding"></a><span data-ttu-id="643d6-166">Decodificação</span><span class="sxs-lookup"><span data-stu-id="643d6-166">Decoding</span></span>

<span data-ttu-id="643d6-167">As APIs de decodificação de WIC são projetadas para serem independentes de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="643d6-167">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="643d6-168">Para obter mais informações sobre a decodificação de imagem, consulte a [visão geral da decodificação](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="643d6-168">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="643d6-169">Para obter mais informações sobre como usar dados de imagem decodificados, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="643d6-169">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
