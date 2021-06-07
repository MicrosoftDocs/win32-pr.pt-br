---
description: Este tópico fornece informações sobre o codec TIFF nativo disponível por meio Windows Imaging Component (WIC).
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Visão geral do formato TIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b28dfcc85dac21e95e6c76118d2db57cb74a08
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444417"
---
# <a name="tiff-format-overview"></a><span data-ttu-id="3b96e-103">Visão geral do formato TIFF</span><span class="sxs-lookup"><span data-stu-id="3b96e-103">TIFF Format Overview</span></span>

<span data-ttu-id="3b96e-104">Este tópico fornece informações sobre o codec TIFF nativo disponível por meio Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="3b96e-104">This topic provides information about the native TIFF codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="3b96e-105">Identidade do Codec</span><span class="sxs-lookup"><span data-stu-id="3b96e-105">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="3b96e-106">Codificação</span><span class="sxs-lookup"><span data-stu-id="3b96e-106">Encoding</span></span>](#encoding)
    -   [<span data-ttu-id="3b96e-107">Opções do codificador</span><span class="sxs-lookup"><span data-stu-id="3b96e-107">Encoder Options</span></span>](#encoder-options)
-   [<span data-ttu-id="3b96e-108">Decodificação</span><span class="sxs-lookup"><span data-stu-id="3b96e-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="3b96e-109">Identidade do Codec</span><span class="sxs-lookup"><span data-stu-id="3b96e-109">Codec Identity</span></span>

<span data-ttu-id="3b96e-110">A tabela a seguir fornece informações de identificação de codec.</span><span class="sxs-lookup"><span data-stu-id="3b96e-110">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="3b96e-111">Componente</span><span class="sxs-lookup"><span data-stu-id="3b96e-111">Component</span></span>            |   <span data-ttu-id="3b96e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b96e-112">Description</span></span>                   |
|------------------------|---------------------------------|
| <span data-ttu-id="3b96e-113">Nomes formais</span><span class="sxs-lookup"><span data-stu-id="3b96e-113">Formal Name(s)</span></span>         | <span data-ttu-id="3b96e-114">TIFF</span><span class="sxs-lookup"><span data-stu-id="3b96e-114">Tagged Image File Format (TIFF)</span></span> |
| <span data-ttu-id="3b96e-115">Extensões de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="3b96e-115">File Name Extension(s)</span></span> | <span data-ttu-id="3b96e-116">tiff, tif</span><span class="sxs-lookup"><span data-stu-id="3b96e-116">tiff, tif</span></span>                       |
| <span data-ttu-id="3b96e-117">Tipos MIME</span><span class="sxs-lookup"><span data-stu-id="3b96e-117">MIME type(s)</span></span>           | <span data-ttu-id="3b96e-118">image/tiff, image/tif</span><span class="sxs-lookup"><span data-stu-id="3b96e-118">image/tiff, image/tif</span></span>           |
| <span data-ttu-id="3b96e-119">Suporte à especificação</span><span class="sxs-lookup"><span data-stu-id="3b96e-119">Specification Support</span></span>  | <span data-ttu-id="3b96e-120">Especificação TIFF 6.0</span><span class="sxs-lookup"><span data-stu-id="3b96e-120">TIFF Specification 6.0</span></span>          |



 

<span data-ttu-id="3b96e-121">A tabela a seguir lista os GUIDs usados para identificar os componentes de codec TIFF nativos.</span><span class="sxs-lookup"><span data-stu-id="3b96e-121">The following table lists the GUIDs used to identify the native TIFF codec components.</span></span>



| <span data-ttu-id="3b96e-122">Componente</span><span class="sxs-lookup"><span data-stu-id="3b96e-122">Component</span></span>        | <span data-ttu-id="3b96e-123">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="3b96e-123">Friendly Name</span></span>             | <span data-ttu-id="3b96e-124">GUID</span><span class="sxs-lookup"><span data-stu-id="3b96e-124">GUID</span></span>                                 |
|------------------|---------------------------|--------------------------------------|
| <span data-ttu-id="3b96e-125">Formato do contêiner</span><span class="sxs-lookup"><span data-stu-id="3b96e-125">Container Format</span></span> | <span data-ttu-id="3b96e-126">Contêiner \_ GUIDFormatTiff</span><span class="sxs-lookup"><span data-stu-id="3b96e-126">GUID\_ContainerFormatTiff</span></span> | <span data-ttu-id="3b96e-127">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span><span class="sxs-lookup"><span data-stu-id="3b96e-127">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span></span>  |
| <span data-ttu-id="3b96e-128">Decodificador</span><span class="sxs-lookup"><span data-stu-id="3b96e-128">Decoder</span></span>          | <span data-ttu-id="3b96e-129">CLSID \_ WICTiffDecoder</span><span class="sxs-lookup"><span data-stu-id="3b96e-129">CLSID\_WICTiffDecoder</span></span>     | <span data-ttu-id="3b96e-130">b54e85d9-fe23-499f-8b886es7137502b</span><span class="sxs-lookup"><span data-stu-id="3b96e-130">b54e85d9-fe23-499f-8b886acea7137502b</span></span> |
| <span data-ttu-id="3b96e-131">Codificador</span><span class="sxs-lookup"><span data-stu-id="3b96e-131">Encoder</span></span>          | <span data-ttu-id="3b96e-132">CLSID \_ WICTiffEncoder</span><span class="sxs-lookup"><span data-stu-id="3b96e-132">CLSID\_WICTiffEncoder</span></span>     | <span data-ttu-id="3b96e-133">0131be10-2001-4c5f-a9b0cc88fab64ce8</span><span class="sxs-lookup"><span data-stu-id="3b96e-133">0131be10-2001-4c5f-a9b0cc88fab64ce8</span></span>  |



 

## <a name="encoding"></a><span data-ttu-id="3b96e-134">Codificação</span><span class="sxs-lookup"><span data-stu-id="3b96e-134">Encoding</span></span>

<span data-ttu-id="3b96e-135">A API de codificação WIC foi projetada para ser independente de codec e a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="3b96e-135">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="3b96e-136">Para obter mais informações sobre a codificação de imagem usando a API WIC, consulte a [Visão geral de codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="3b96e-136">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="3b96e-137">Opções do codificador</span><span class="sxs-lookup"><span data-stu-id="3b96e-137">Encoder Options</span></span>

<span data-ttu-id="3b96e-138">Os codecs habilitados para WIC diferem no nível da opção de codificação.</span><span class="sxs-lookup"><span data-stu-id="3b96e-138">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="3b96e-139">As opções do codificador refletem as funcionalidades de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador.</span><span class="sxs-lookup"><span data-stu-id="3b96e-139">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="3b96e-140">As opções de codificador podem ser opções básicas com suporte do WIC disponíveis para todos os códigos habilitados para WIC (embora não necessariamente com suporte) ou opções específicas de codec projetadas pelo codec de formato de imagem.</span><span class="sxs-lookup"><span data-stu-id="3b96e-140">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="3b96e-141">Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3b96e-141">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="3b96e-142">Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte a Visão geral [de codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="3b96e-142">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="3b96e-143">O codec TIFF usa opções básicas do WIC.</span><span class="sxs-lookup"><span data-stu-id="3b96e-143">The TIFF codec uses basic WIC options.</span></span> <span data-ttu-id="3b96e-144">A tabela a seguir lista as opções do codificador WIC com suporte pelo codec TIFF nativo.</span><span class="sxs-lookup"><span data-stu-id="3b96e-144">The following table lists the WIC encoder options supported by the native TIFF codec.</span></span>

| <span data-ttu-id="3b96e-145">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="3b96e-145">Property Name</span></span>         | <span data-ttu-id="3b96e-146">Vartype</span><span class="sxs-lookup"><span data-stu-id="3b96e-146">VARTYPE</span></span> | <span data-ttu-id="3b96e-147">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="3b96e-147">Value Range</span></span> | <span data-ttu-id="3b96e-148">Valor Padrão</span><span class="sxs-lookup"><span data-stu-id="3b96e-148">Default Value</span></span>    |
|-----------------------|---------|-------------|------------------|
| <span data-ttu-id="3b96e-149">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="3b96e-149">CompressionQuality</span></span>    | <span data-ttu-id="3b96e-150">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="3b96e-150">VT\_R4</span></span>  | <span data-ttu-id="3b96e-151">0 - 1.0</span><span class="sxs-lookup"><span data-stu-id="3b96e-151">0 - 1.0</span></span>     | <span data-ttu-id="3b96e-152">0</span><span class="sxs-lookup"><span data-stu-id="3b96e-152">0</span></span>                |
| <span data-ttu-id="3b96e-153">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="3b96e-153">TiffCompressionMethod</span></span> | <span data-ttu-id="3b96e-154">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="3b96e-154">VT\_UI1</span></span> | [<span data-ttu-id="3b96e-155">**WICTiffCompressionOption**</span><span class="sxs-lookup"><span data-stu-id="3b96e-155">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [<span data-ttu-id="3b96e-156">**WICTiffCompressionDontCare**</span><span class="sxs-lookup"><span data-stu-id="3b96e-156">**WICTiffCompressionDontCare**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

<span data-ttu-id="3b96e-157">Se uma opção de codificador estiver presente na lista de opções [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) à qual o codec não dá suporte, ela será ignorada.</span><span class="sxs-lookup"><span data-stu-id="3b96e-157">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="compressionquality-option"></a><span data-ttu-id="3b96e-158">Opção CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="3b96e-158">CompressionQuality Option</span></span>

<span data-ttu-id="3b96e-159">Especifica a qualidade de compactação desejada.</span><span class="sxs-lookup"><span data-stu-id="3b96e-159">Specifies the desired compression quality.</span></span> <span data-ttu-id="3b96e-160">0.0 indica o esquema de compactação menos eficiente disponível.</span><span class="sxs-lookup"><span data-stu-id="3b96e-160">0.0 indicates the least efficient compression scheme available.</span></span> <span data-ttu-id="3b96e-161">Normalmente, esse esquema resulta em uma codificação mais rápida, mas em uma saída maior.</span><span class="sxs-lookup"><span data-stu-id="3b96e-161">Typically, this scheme results in a faster encode but larger output.</span></span> <span data-ttu-id="3b96e-162">Um valor de 1,0 especifica o esquema de compactação mais eficiente disponível.</span><span class="sxs-lookup"><span data-stu-id="3b96e-162">A value of 1.0 specifies the most efficient compression scheme available.</span></span> <span data-ttu-id="3b96e-163">Normalmente, esse esquema resulta em uma codificação mais longa, mas produz uma saída menor.</span><span class="sxs-lookup"><span data-stu-id="3b96e-163">Typically, this scheme results in a longer encode but produces smaller output.</span></span>

<span data-ttu-id="3b96e-164">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="3b96e-164">The default value is 0.</span></span>

### <a name="tiffcompressionmethod-option"></a><span data-ttu-id="3b96e-165">Opção TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="3b96e-165">TiffCompressionMethod Option</span></span>

<span data-ttu-id="3b96e-166">Especifica o método de compactação TIFF.</span><span class="sxs-lookup"><span data-stu-id="3b96e-166">Specifies the TIFF compression method.</span></span>

<span data-ttu-id="3b96e-167">O valor padrão é [**WICTiffCompressionDontCare.**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)</span><span class="sxs-lookup"><span data-stu-id="3b96e-167">The default value is [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span></span>

## <a name="decoding"></a><span data-ttu-id="3b96e-168">Decodificação</span><span class="sxs-lookup"><span data-stu-id="3b96e-168">Decoding</span></span>

<span data-ttu-id="3b96e-169">As APIs de decodificação do WIC foram projetadas para serem independentes de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="3b96e-169">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="3b96e-170">Para obter mais informações sobre decodificação de imagem, consulte Visão [geral de decodificação.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="3b96e-170">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="3b96e-171">Para obter mais informações sobre como usar dados de imagem decodificados, consulte Visão geral das [fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="3b96e-171">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
