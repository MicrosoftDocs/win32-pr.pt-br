---
description: Este tópico fornece informações sobre o codec JPEG nativo disponível por meio do Windows Imaging Component (WIC).
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Visão geral do formato JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb953d1d6a02e47b41d1b7cf872f3381cd640151
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105792649"
---
# <a name="jpeg-format-overview"></a><span data-ttu-id="4abc1-103">Visão geral do formato JPEG</span><span class="sxs-lookup"><span data-stu-id="4abc1-103">JPEG Format Overview</span></span>

<span data-ttu-id="4abc1-104">Este tópico fornece informações sobre o codec JPEG nativo disponível por meio do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="4abc1-104">This topic provides information about the native JPEG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="4abc1-105">Identidade do codec</span><span class="sxs-lookup"><span data-stu-id="4abc1-105">Codec Identity</span></span>

<span data-ttu-id="4abc1-106">A tabela a seguir fornece informações de identificação do codec.</span><span class="sxs-lookup"><span data-stu-id="4abc1-106">The following table provides codec identification information.</span></span>



|                        |                                         |
|------------------------|-----------------------------------------|
| <span data-ttu-id="4abc1-107">Nome (s) formal (es)</span><span class="sxs-lookup"><span data-stu-id="4abc1-107">Formal Name(s)</span></span>         | <span data-ttu-id="4abc1-108">JPEG</span><span class="sxs-lookup"><span data-stu-id="4abc1-108">Joint Photographic Experts Group (JPEG)</span></span> |
| <span data-ttu-id="4abc1-109">Extensão (s) de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="4abc1-109">File Name Extension(s)</span></span> | <span data-ttu-id="4abc1-110">JPE, JPEG, jpg</span><span class="sxs-lookup"><span data-stu-id="4abc1-110">jpe, jpeg, jpg</span></span>                          |
| <span data-ttu-id="4abc1-111">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="4abc1-111">MIME type</span></span>              | <span data-ttu-id="4abc1-112">imagem/JPEG, imagem/JPE, imagem/jpg</span><span class="sxs-lookup"><span data-stu-id="4abc1-112">image/jpeg, image/jpe, image/jpg</span></span>        |
| <span data-ttu-id="4abc1-113">Suporte à especificação</span><span class="sxs-lookup"><span data-stu-id="4abc1-113">Specification Support</span></span>  | <span data-ttu-id="4abc1-114">Especificação JFIF 1, 2</span><span class="sxs-lookup"><span data-stu-id="4abc1-114">JFIF Specification 1.02</span></span>                 |



 

<span data-ttu-id="4abc1-115">A tabela a seguir lista os GUIDs usados para identificar os componentes do codec JPEG nativo.</span><span class="sxs-lookup"><span data-stu-id="4abc1-115">The following table lists the GUIDs used to identify the native JPEG codec components.</span></span>



| <span data-ttu-id="4abc1-116">Componente</span><span class="sxs-lookup"><span data-stu-id="4abc1-116">Component</span></span>        | <span data-ttu-id="4abc1-117">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="4abc1-117">Friendly Name</span></span>             | <span data-ttu-id="4abc1-118">GUID</span><span class="sxs-lookup"><span data-stu-id="4abc1-118">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="4abc1-119">Formato do contêiner</span><span class="sxs-lookup"><span data-stu-id="4abc1-119">Container Format</span></span> | <span data-ttu-id="4abc1-120">\_CONTAINERFORMATJPEG GUID</span><span class="sxs-lookup"><span data-stu-id="4abc1-120">GUID\_ContainerFormatJpeg</span></span> | <span data-ttu-id="4abc1-121">19e4a5aa-5662-4fc5-a0c01758028e1057</span><span class="sxs-lookup"><span data-stu-id="4abc1-121">19e4a5aa-5662-4fc5-a0c01758028e1057</span></span> |
| <span data-ttu-id="4abc1-122">Decodificador</span><span class="sxs-lookup"><span data-stu-id="4abc1-122">Decoder</span></span>          | <span data-ttu-id="4abc1-123">\_WICJPEGDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="4abc1-123">CLSID\_WICJpegDecoder</span></span>     | <span data-ttu-id="4abc1-124">9456a480-e88b-43ea-9e730b2d9b71b1ca</span><span class="sxs-lookup"><span data-stu-id="4abc1-124">9456a480-e88b-43ea-9e730b2d9b71b1ca</span></span> |
| <span data-ttu-id="4abc1-125">Codificador</span><span class="sxs-lookup"><span data-stu-id="4abc1-125">Encoder</span></span>          | <span data-ttu-id="4abc1-126">\_WICJPEGENCODER CLSID</span><span class="sxs-lookup"><span data-stu-id="4abc1-126">CLSID\_WICJpegEncoder</span></span>     | <span data-ttu-id="4abc1-127">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span><span class="sxs-lookup"><span data-stu-id="4abc1-127">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="4abc1-128">Codificação</span><span class="sxs-lookup"><span data-stu-id="4abc1-128">Encoding</span></span>

<span data-ttu-id="4abc1-129">A API de codificação do WIC é projetada para ser independente de codec e a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="4abc1-129">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="4abc1-130">Para obter mais informações sobre codificação de imagem usando a API do WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="4abc1-130">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="4abc1-131">Opções de codificador</span><span class="sxs-lookup"><span data-stu-id="4abc1-131">Encoder Options</span></span>

<span data-ttu-id="4abc1-132">Os codecs habilitados para WIC diferem no nível de opção de codificação.</span><span class="sxs-lookup"><span data-stu-id="4abc1-132">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="4abc1-133">As opções de codificador refletem os recursos de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador.</span><span class="sxs-lookup"><span data-stu-id="4abc1-133">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="4abc1-134">As opções de codificador podem ser opções básicas compatíveis com o WIC disponíveis para todos os códigos habilitados para WIC (embora não sejam necessariamente suportados) ou opções específicas de codec projetadas pelo codec de formato de imagem.</span><span class="sxs-lookup"><span data-stu-id="4abc1-134">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="4abc1-135">Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4abc1-135">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="4abc1-136">Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="4abc1-136">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="4abc1-137">O codec JPEG usa opções básicas de WIC.</span><span class="sxs-lookup"><span data-stu-id="4abc1-137">The JPEG codec uses basic WIC options.</span></span> <span data-ttu-id="4abc1-138">A tabela a seguir lista as opções de codificador do WIC compatíveis com o codec JPEG nativo.</span><span class="sxs-lookup"><span data-stu-id="4abc1-138">The following table lists the WIC encoder options supported by the native JPEG codec.</span></span>



| <span data-ttu-id="4abc1-139">Nome da Propriedade</span><span class="sxs-lookup"><span data-stu-id="4abc1-139">Property Name</span></span>                                        | <span data-ttu-id="4abc1-140">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4abc1-140">VARTYPE</span></span>           | <span data-ttu-id="4abc1-141">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="4abc1-141">Value Range</span></span>                                                                       | <span data-ttu-id="4abc1-142">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="4abc1-142">Default Value</span></span>                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="4abc1-143">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="4abc1-143">ImageQuality</span></span>](#imagequality-option)                 | <span data-ttu-id="4abc1-144">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="4abc1-144">VT\_R4</span></span>            | <span data-ttu-id="4abc1-145">0-1,0</span><span class="sxs-lookup"><span data-stu-id="4abc1-145">0 - 1.0</span></span>                                                                           | <span data-ttu-id="4abc1-146">0,9</span><span class="sxs-lookup"><span data-stu-id="4abc1-146">0.9</span></span>                                                                            |
| [<span data-ttu-id="4abc1-147">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="4abc1-147">BitmapTransform</span></span>](#bitmaptransform-option)           | <span data-ttu-id="4abc1-148">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="4abc1-148">VT\_UI1</span></span>           | [<span data-ttu-id="4abc1-149">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="4abc1-149">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [<span data-ttu-id="4abc1-150">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="4abc1-150">**WICBitmapTransformRotate0**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [<span data-ttu-id="4abc1-151">Luminância</span><span class="sxs-lookup"><span data-stu-id="4abc1-151">Luminance</span></span>](#luminance-option)                       | <span data-ttu-id="4abc1-152">\_Matriz VT UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="4abc1-152">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="4abc1-153">64 entradas (DCT)</span><span class="sxs-lookup"><span data-stu-id="4abc1-153">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="4abc1-154">Tabela de luminância padrão.</span><span class="sxs-lookup"><span data-stu-id="4abc1-154">Default luminance table.</span></span>                                                       |
| [<span data-ttu-id="4abc1-155">Crominância</span><span class="sxs-lookup"><span data-stu-id="4abc1-155">Chrominance</span></span>](#chrominance-option)                   | <span data-ttu-id="4abc1-156">\_Matriz VT UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="4abc1-156">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="4abc1-157">64 entradas (DCT)</span><span class="sxs-lookup"><span data-stu-id="4abc1-157">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="4abc1-158">Tabela crominância padrão.</span><span class="sxs-lookup"><span data-stu-id="4abc1-158">Default chrominance table.</span></span>                                                     |
| [<span data-ttu-id="4abc1-159">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="4abc1-159">JpegYCrCbSubsampling</span></span>](#jpegycrcbsubsampling-option) | <span data-ttu-id="4abc1-160">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="4abc1-160">VT\_UI1</span></span>           | [<span data-ttu-id="4abc1-161">**WICJpegYCrCbSubsamplingOption**</span><span class="sxs-lookup"><span data-stu-id="4abc1-161">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [<span data-ttu-id="4abc1-162">**WICJpegYCrCbSubsampling420**</span><span class="sxs-lookup"><span data-stu-id="4abc1-162">**WICJpegYCrCbSubsampling420**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [<span data-ttu-id="4abc1-163">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="4abc1-163">SuppressApp0</span></span>](/windows)                       | <span data-ttu-id="4abc1-164">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="4abc1-164">VT\_BOOL</span></span>          | <span data-ttu-id="4abc1-165">**Verdadeiro** / **Falso**</span><span class="sxs-lookup"><span data-stu-id="4abc1-165">**TRUE**/**FALSE**</span></span>                                                                | <span data-ttu-id="4abc1-166">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="4abc1-166">**FALSE**</span></span>                                                                      |



 

<span data-ttu-id="4abc1-167">Se uma opção de codificador estiver presente na lista de opções de [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) para a qual o codec não dá suporte, ela será ignorada.</span><span class="sxs-lookup"><span data-stu-id="4abc1-167">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="imagequality-option"></a><span data-ttu-id="4abc1-168">Opção ImageQuality</span><span class="sxs-lookup"><span data-stu-id="4abc1-168">ImageQuality Option</span></span>

<span data-ttu-id="4abc1-169">Especifica a fidelidade da imagem desejada.</span><span class="sxs-lookup"><span data-stu-id="4abc1-169">Specifies the desired image fidelity.</span></span> <span data-ttu-id="4abc1-170">0,0 indica a menor fidelidade possível e 1,0 especifica a fidelidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="4abc1-170">0.0 indicates the lowest possible fidelity and 1.0 specifies the highest fidelity.</span></span>

<span data-ttu-id="4abc1-171">O valor padrão é 0,9.</span><span class="sxs-lookup"><span data-stu-id="4abc1-171">The default value is 0.9.</span></span>

### <a name="bitmaptransform-option"></a><span data-ttu-id="4abc1-172">Opção BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="4abc1-172">BitmapTransform Option</span></span>

<span data-ttu-id="4abc1-173">Especifica como a imagem deve ser transformada durante a decodificação de imagem.</span><span class="sxs-lookup"><span data-stu-id="4abc1-173">Specifies how the image is to be transformed during image decoding.</span></span> <span data-ttu-id="4abc1-174">Essa opção deve ser definida como um dos valores de enumeração [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .</span><span class="sxs-lookup"><span data-stu-id="4abc1-174">This option must be set to one of the [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) enumeration values.</span></span>

<span data-ttu-id="4abc1-175">O valor padrão é [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span><span class="sxs-lookup"><span data-stu-id="4abc1-175">The default value is [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span></span>

### <a name="luminance-option"></a><span data-ttu-id="4abc1-176">Opção de luminância</span><span class="sxs-lookup"><span data-stu-id="4abc1-176">Luminance Option</span></span>

<span data-ttu-id="4abc1-177">Especifica a tabela de nível de brilho em escala de cinza a ser usada para codificação.</span><span class="sxs-lookup"><span data-stu-id="4abc1-177">Specifies the grayscale brightness level table to use for encoding.</span></span>

### <a name="chrominance-option"></a><span data-ttu-id="4abc1-178">Opção crominância</span><span class="sxs-lookup"><span data-stu-id="4abc1-178">Chrominance Option</span></span>

<span data-ttu-id="4abc1-179">Especifica a tabela crominância a ser usada para codificação.</span><span class="sxs-lookup"><span data-stu-id="4abc1-179">Specifies the chrominance table to use for encoding.</span></span>

### <a name="jpegycrcbsubsampling-option"></a><span data-ttu-id="4abc1-180">Opção JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="4abc1-180">JpegYCrCbSubsampling Option</span></span>

<span data-ttu-id="4abc1-181">Especifica a taxa de subamostração a ser usada para codificação YCrCb.</span><span class="sxs-lookup"><span data-stu-id="4abc1-181">Specifies the subsampling ratio to use for YCrCb encoding.</span></span>

<span data-ttu-id="4abc1-182">O valor padrão é [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span><span class="sxs-lookup"><span data-stu-id="4abc1-182">The default value is [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span></span>

### <a name="suppressapp0-option"></a><span data-ttu-id="4abc1-183">Opção SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="4abc1-183">SuppressApp0 Option</span></span>

<span data-ttu-id="4abc1-184">Especifica se é para suprimir a gravação de metadados do App0 durante a codificação dos dados da imagem.</span><span class="sxs-lookup"><span data-stu-id="4abc1-184">Specifies whether to suppress the write of App0 metadata while encoding the image data.</span></span>

<span data-ttu-id="4abc1-185">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="4abc1-185">The default value is **FALSE**.</span></span>

## <a name="decoding"></a><span data-ttu-id="4abc1-186">Decodificação</span><span class="sxs-lookup"><span data-stu-id="4abc1-186">Decoding</span></span>

<span data-ttu-id="4abc1-187">A API de decodificação de WIC é projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="4abc1-187">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="4abc1-188">Para obter mais informações sobre a decodificação de imagem, consulte a [visão geral da decodificação](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="4abc1-188">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="4abc1-189">Para obter mais informações sobre como usar dados de imagem decodificados, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="4abc1-189">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="4abc1-190">O codec JPEG nativo também dá suporte ao [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) na decodificação de quadros adicionando opções avançada para decodificar um fluxo de imagem.</span><span class="sxs-lookup"><span data-stu-id="4abc1-190">The native JPEG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advaced options for decoding an image stream.</span></span> <span data-ttu-id="4abc1-191">Para obter mais informações sobre essas opções avançadas, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="4abc1-191">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
