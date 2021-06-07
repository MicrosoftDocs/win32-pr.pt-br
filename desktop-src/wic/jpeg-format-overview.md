---
description: Este tópico fornece informações sobre o codec JPEG nativo disponível por meio do Windows Imaging Component (WIC).
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Visão geral do formato JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2acc7fcd71fc962d3321112d342f675b878188
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444187"
---
# <a name="jpeg-format-overview"></a><span data-ttu-id="31aa4-103">Visão geral do formato JPEG</span><span class="sxs-lookup"><span data-stu-id="31aa4-103">JPEG Format Overview</span></span>

<span data-ttu-id="31aa4-104">Este tópico fornece informações sobre o codec JPEG nativo disponível por meio do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="31aa4-104">This topic provides information about the native JPEG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="31aa4-105">Identidade do Codec</span><span class="sxs-lookup"><span data-stu-id="31aa4-105">Codec Identity</span></span>

<span data-ttu-id="31aa4-106">A tabela a seguir fornece informações de identificação de codec.</span><span class="sxs-lookup"><span data-stu-id="31aa4-106">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="31aa4-107">Componente</span><span class="sxs-lookup"><span data-stu-id="31aa4-107">Component</span></span>            | <span data-ttu-id="31aa4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="31aa4-108">Description</span></span>                             |
|------------------------|-----------------------------------------|
| <span data-ttu-id="31aa4-109">Nomes formais</span><span class="sxs-lookup"><span data-stu-id="31aa4-109">Formal Name(s)</span></span>         | <span data-ttu-id="31aa4-110">JPEG</span><span class="sxs-lookup"><span data-stu-id="31aa4-110">Joint Photographic Experts Group (JPEG)</span></span> |
| <span data-ttu-id="31aa4-111">Extensões de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="31aa4-111">File Name Extension(s)</span></span> | <span data-ttu-id="31aa4-112">jpe, jpeg, jpg</span><span class="sxs-lookup"><span data-stu-id="31aa4-112">jpe, jpeg, jpg</span></span>                          |
| <span data-ttu-id="31aa4-113">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="31aa4-113">MIME type</span></span>              | <span data-ttu-id="31aa4-114">image/jpeg, image/jpe, image/jpg</span><span class="sxs-lookup"><span data-stu-id="31aa4-114">image/jpeg, image/jpe, image/jpg</span></span>        |
| <span data-ttu-id="31aa4-115">Suporte à especificação</span><span class="sxs-lookup"><span data-stu-id="31aa4-115">Specification Support</span></span>  | <span data-ttu-id="31aa4-116">Especificação 1.02 do JFIF</span><span class="sxs-lookup"><span data-stu-id="31aa4-116">JFIF Specification 1.02</span></span>                 |



 

<span data-ttu-id="31aa4-117">A tabela a seguir lista os GUIDs usados para identificar os componentes nativos do codec JPEG.</span><span class="sxs-lookup"><span data-stu-id="31aa4-117">The following table lists the GUIDs used to identify the native JPEG codec components.</span></span>



| <span data-ttu-id="31aa4-118">Componente</span><span class="sxs-lookup"><span data-stu-id="31aa4-118">Component</span></span>        | <span data-ttu-id="31aa4-119">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="31aa4-119">Friendly Name</span></span>             | <span data-ttu-id="31aa4-120">GUID</span><span class="sxs-lookup"><span data-stu-id="31aa4-120">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="31aa4-121">Formato do contêiner</span><span class="sxs-lookup"><span data-stu-id="31aa4-121">Container Format</span></span> | <span data-ttu-id="31aa4-122">Contêiner \_ GUIDFormatJpeg</span><span class="sxs-lookup"><span data-stu-id="31aa4-122">GUID\_ContainerFormatJpeg</span></span> | <span data-ttu-id="31aa4-123">19e4a5aa-5662-4fc5-a0c01758028e1057</span><span class="sxs-lookup"><span data-stu-id="31aa4-123">19e4a5aa-5662-4fc5-a0c01758028e1057</span></span> |
| <span data-ttu-id="31aa4-124">Decodificador</span><span class="sxs-lookup"><span data-stu-id="31aa4-124">Decoder</span></span>          | <span data-ttu-id="31aa4-125">CLSID \_ WICJpegDecoder</span><span class="sxs-lookup"><span data-stu-id="31aa4-125">CLSID\_WICJpegDecoder</span></span>     | <span data-ttu-id="31aa4-126">9456a480-e88b-43ea-9e730b2d9b71b1ca</span><span class="sxs-lookup"><span data-stu-id="31aa4-126">9456a480-e88b-43ea-9e730b2d9b71b1ca</span></span> |
| <span data-ttu-id="31aa4-127">Codificador</span><span class="sxs-lookup"><span data-stu-id="31aa4-127">Encoder</span></span>          | <span data-ttu-id="31aa4-128">CLSID \_ WICJpegEncoder</span><span class="sxs-lookup"><span data-stu-id="31aa4-128">CLSID\_WICJpegEncoder</span></span>     | <span data-ttu-id="31aa4-129">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span><span class="sxs-lookup"><span data-stu-id="31aa4-129">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="31aa4-130">Codificação</span><span class="sxs-lookup"><span data-stu-id="31aa4-130">Encoding</span></span>

<span data-ttu-id="31aa4-131">A API de codificação WIC foi projetada para ser independente de codec e a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="31aa4-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="31aa4-132">Para obter mais informações sobre a codificação de imagem usando a API WIC, consulte a [Visão geral de codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="31aa4-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="31aa4-133">Opções do codificador</span><span class="sxs-lookup"><span data-stu-id="31aa4-133">Encoder Options</span></span>

<span data-ttu-id="31aa4-134">Os codecs habilitados para WIC diferem no nível da opção de codificação.</span><span class="sxs-lookup"><span data-stu-id="31aa4-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="31aa4-135">As opções do codificador refletem as funcionalidades de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador.</span><span class="sxs-lookup"><span data-stu-id="31aa4-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="31aa4-136">As opções de codificador podem ser opções básicas com suporte do WIC disponíveis para todos os códigos habilitados para WIC (embora não necessariamente com suporte) ou opções específicas de codec projetadas pelo codec de formato de imagem.</span><span class="sxs-lookup"><span data-stu-id="31aa4-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="31aa4-137">Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="31aa4-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="31aa4-138">Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte a Visão geral [de codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="31aa4-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="31aa4-139">O codec JPEG usa opções básicas do WIC.</span><span class="sxs-lookup"><span data-stu-id="31aa4-139">The JPEG codec uses basic WIC options.</span></span> <span data-ttu-id="31aa4-140">A tabela a seguir lista as opções do codificador WIC com suporte pelo codec jpeg nativo.</span><span class="sxs-lookup"><span data-stu-id="31aa4-140">The following table lists the WIC encoder options supported by the native JPEG codec.</span></span>



| <span data-ttu-id="31aa4-141">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="31aa4-141">Property Name</span></span>                                        | <span data-ttu-id="31aa4-142">Vartype</span><span class="sxs-lookup"><span data-stu-id="31aa4-142">VARTYPE</span></span>           | <span data-ttu-id="31aa4-143">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="31aa4-143">Value Range</span></span>                                                                       | <span data-ttu-id="31aa4-144">Valor Padrão</span><span class="sxs-lookup"><span data-stu-id="31aa4-144">Default Value</span></span>                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="31aa4-145">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="31aa4-145">ImageQuality</span></span>](#imagequality-option)                 | <span data-ttu-id="31aa4-146">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="31aa4-146">VT\_R4</span></span>            | <span data-ttu-id="31aa4-147">0 - 1.0</span><span class="sxs-lookup"><span data-stu-id="31aa4-147">0 - 1.0</span></span>                                                                           | <span data-ttu-id="31aa4-148">0,9</span><span class="sxs-lookup"><span data-stu-id="31aa4-148">0.9</span></span>                                                                            |
| [<span data-ttu-id="31aa4-149">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="31aa4-149">BitmapTransform</span></span>](#bitmaptransform-option)           | <span data-ttu-id="31aa4-150">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="31aa4-150">VT\_UI1</span></span>           | [<span data-ttu-id="31aa4-151">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="31aa4-151">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [<span data-ttu-id="31aa4-152">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="31aa4-152">**WICBitmapTransformRotate0**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [<span data-ttu-id="31aa4-153">Luminância</span><span class="sxs-lookup"><span data-stu-id="31aa4-153">Luminance</span></span>](#luminance-option)                       | <span data-ttu-id="31aa4-154">MATRIZ VT \_ UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="31aa4-154">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="31aa4-155">64 entradas (DCT)</span><span class="sxs-lookup"><span data-stu-id="31aa4-155">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="31aa4-156">Tabela de luminância padrão.</span><span class="sxs-lookup"><span data-stu-id="31aa4-156">Default luminance table.</span></span>                                                       |
| [<span data-ttu-id="31aa4-157">Crominância</span><span class="sxs-lookup"><span data-stu-id="31aa4-157">Chrominance</span></span>](#chrominance-option)                   | <span data-ttu-id="31aa4-158">MATRIZ VT \_ UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="31aa4-158">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="31aa4-159">64 entradas (DCT)</span><span class="sxs-lookup"><span data-stu-id="31aa4-159">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="31aa4-160">Tabela de chrominance padrão.</span><span class="sxs-lookup"><span data-stu-id="31aa4-160">Default chrominance table.</span></span>                                                     |
| [<span data-ttu-id="31aa4-161">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="31aa4-161">JpegYCrCbSubsampling</span></span>](#jpegycrcbsubsampling-option) | <span data-ttu-id="31aa4-162">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="31aa4-162">VT\_UI1</span></span>           | [<span data-ttu-id="31aa4-163">**WICJpegYCrCbSubsamplingOption**</span><span class="sxs-lookup"><span data-stu-id="31aa4-163">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [<span data-ttu-id="31aa4-164">**WICJpegYCrCbSubsampling420**</span><span class="sxs-lookup"><span data-stu-id="31aa4-164">**WICJpegYCrCbSubsampling420**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [<span data-ttu-id="31aa4-165">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="31aa4-165">SuppressApp0</span></span>](/windows)                       | <span data-ttu-id="31aa4-166">BOOL da VT \_</span><span class="sxs-lookup"><span data-stu-id="31aa4-166">VT\_BOOL</span></span>          | <span data-ttu-id="31aa4-167">**TRUE** / **FALSE**</span><span class="sxs-lookup"><span data-stu-id="31aa4-167">**TRUE**/**FALSE**</span></span>                                                                | <span data-ttu-id="31aa4-168">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="31aa4-168">**FALSE**</span></span>                                                                      |



 

<span data-ttu-id="31aa4-169">Se uma opção de codificador estiver presente na lista de opções [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) à qual o codec não dá suporte, ela será ignorada.</span><span class="sxs-lookup"><span data-stu-id="31aa4-169">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="imagequality-option"></a><span data-ttu-id="31aa4-170">Opção ImageQuality</span><span class="sxs-lookup"><span data-stu-id="31aa4-170">ImageQuality Option</span></span>

<span data-ttu-id="31aa4-171">Especifica a fidelidade da imagem desejada.</span><span class="sxs-lookup"><span data-stu-id="31aa4-171">Specifies the desired image fidelity.</span></span> <span data-ttu-id="31aa4-172">0,0 indica a fidelidade mais baixa possível e 1,0 especifica a fidelidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="31aa4-172">0.0 indicates the lowest possible fidelity and 1.0 specifies the highest fidelity.</span></span>

<span data-ttu-id="31aa4-173">O valor padrão é 0,9.</span><span class="sxs-lookup"><span data-stu-id="31aa4-173">The default value is 0.9.</span></span>

### <a name="bitmaptransform-option"></a><span data-ttu-id="31aa4-174">Opção BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="31aa4-174">BitmapTransform Option</span></span>

<span data-ttu-id="31aa4-175">Especifica como a imagem deve ser transformada durante a decodificação da imagem.</span><span class="sxs-lookup"><span data-stu-id="31aa4-175">Specifies how the image is to be transformed during image decoding.</span></span> <span data-ttu-id="31aa4-176">Essa opção deve ser definida como um dos valores de enumeração [**WICBitmapTransformOptions.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)</span><span class="sxs-lookup"><span data-stu-id="31aa4-176">This option must be set to one of the [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) enumeration values.</span></span>

<span data-ttu-id="31aa4-177">O valor padrão é [**WICBitmapTransformRotate0.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)</span><span class="sxs-lookup"><span data-stu-id="31aa4-177">The default value is [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span></span>

### <a name="luminance-option"></a><span data-ttu-id="31aa4-178">Opção Luminance</span><span class="sxs-lookup"><span data-stu-id="31aa4-178">Luminance Option</span></span>

<span data-ttu-id="31aa4-179">Especifica a tabela de nível de brilho de escala de cinza a ser usada para codificação.</span><span class="sxs-lookup"><span data-stu-id="31aa4-179">Specifies the grayscale brightness level table to use for encoding.</span></span>

### <a name="chrominance-option"></a><span data-ttu-id="31aa4-180">Opção Chrominance</span><span class="sxs-lookup"><span data-stu-id="31aa4-180">Chrominance Option</span></span>

<span data-ttu-id="31aa4-181">Especifica a tabela de chrominance a ser usada para codificação.</span><span class="sxs-lookup"><span data-stu-id="31aa4-181">Specifies the chrominance table to use for encoding.</span></span>

### <a name="jpegycrcbsubsampling-option"></a><span data-ttu-id="31aa4-182">Opção JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="31aa4-182">JpegYCrCbSubsampling Option</span></span>

<span data-ttu-id="31aa4-183">Especifica a taxa de subampling a ser usada para codificação YCrCb.</span><span class="sxs-lookup"><span data-stu-id="31aa4-183">Specifies the subsampling ratio to use for YCrCb encoding.</span></span>

<span data-ttu-id="31aa4-184">O valor padrão é [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span><span class="sxs-lookup"><span data-stu-id="31aa4-184">The default value is [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span></span>

### <a name="suppressapp0-option"></a><span data-ttu-id="31aa4-185">Opção SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="31aa4-185">SuppressApp0 Option</span></span>

<span data-ttu-id="31aa4-186">Especifica se a gravação de metadados do App0 deve ser suprimida durante a codificação dos dados da imagem.</span><span class="sxs-lookup"><span data-stu-id="31aa4-186">Specifies whether to suppress the write of App0 metadata while encoding the image data.</span></span>

<span data-ttu-id="31aa4-187">O valor padrão é **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="31aa4-187">The default value is **FALSE**.</span></span>

## <a name="decoding"></a><span data-ttu-id="31aa4-188">Decodificação</span><span class="sxs-lookup"><span data-stu-id="31aa4-188">Decoding</span></span>

<span data-ttu-id="31aa4-189">A API de decodificação do WIC foi projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="31aa4-189">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="31aa4-190">Para obter mais informações sobre decodificação de imagem, consulte Visão [geral de decodificação.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="31aa4-190">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="31aa4-191">Para obter mais informações sobre como usar dados de imagem decodificados, consulte Visão geral das [fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="31aa4-191">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="31aa4-192">O codec jpeg nativo também dá suporte ao [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) na decodificação de quadro adicionando opções de suporte para decodificar um fluxo de imagem.</span><span class="sxs-lookup"><span data-stu-id="31aa4-192">The native JPEG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advaced options for decoding an image stream.</span></span> <span data-ttu-id="31aa4-193">Para obter mais informações sobre essas opções avançadas, consulte Visão geral das [fontes de bitmap.](-wic-bitmapsources.md)</span><span class="sxs-lookup"><span data-stu-id="31aa4-193">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
