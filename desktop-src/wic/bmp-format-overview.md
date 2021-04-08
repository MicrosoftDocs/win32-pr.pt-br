---
description: Este tópico fornece informações sobre o codec BMP nativo disponível por meio do Windows Imaging Component (WIC).
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Visão geral do formato BMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3492189f80b43915bab94a7ea8359f2e5950f7c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662292"
---
# <a name="bmp-format-overview"></a><span data-ttu-id="0968e-103">Visão geral do formato BMP</span><span class="sxs-lookup"><span data-stu-id="0968e-103">BMP Format Overview</span></span>

<span data-ttu-id="0968e-104">Este tópico fornece informações sobre o codec BMP nativo disponível por meio do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="0968e-104">This topic provides information about the native BMP codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="0968e-105">Identidade do codec</span><span class="sxs-lookup"><span data-stu-id="0968e-105">Codec Identity</span></span>

<span data-ttu-id="0968e-106">A tabela a seguir fornece informações de identificação do codec.</span><span class="sxs-lookup"><span data-stu-id="0968e-106">The following table provides codec identification information.</span></span>



|                        |                       |
|------------------------|-----------------------|
| <span data-ttu-id="0968e-107">Nome (s) formal (es)</span><span class="sxs-lookup"><span data-stu-id="0968e-107">Formal Name(s)</span></span>         | <span data-ttu-id="0968e-108">Formato de bitmap do Windows</span><span class="sxs-lookup"><span data-stu-id="0968e-108">Windows Bitmap Format</span></span> |
| <span data-ttu-id="0968e-109">Extensão (s) de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="0968e-109">File Name Extension(s)</span></span> | <span data-ttu-id="0968e-110">BMP, DIB</span><span class="sxs-lookup"><span data-stu-id="0968e-110">bmp, dib</span></span>              |
| <span data-ttu-id="0968e-111">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="0968e-111">MIME type</span></span>              | <span data-ttu-id="0968e-112">image/bmp</span><span class="sxs-lookup"><span data-stu-id="0968e-112">image/bmp</span></span>             |
| <span data-ttu-id="0968e-113">Suporte à especificação</span><span class="sxs-lookup"><span data-stu-id="0968e-113">Specification Support</span></span>  | <span data-ttu-id="0968e-114">Especificação BMP V5</span><span class="sxs-lookup"><span data-stu-id="0968e-114">BMP Specification v5</span></span>  |



 

<span data-ttu-id="0968e-115">A tabela a seguir lista os GUIDs usados para identificar os componentes do codec BMP nativos.</span><span class="sxs-lookup"><span data-stu-id="0968e-115">The following table lists the GUIDs used to identify the native BMP codec components.</span></span>



| <span data-ttu-id="0968e-116">Componente</span><span class="sxs-lookup"><span data-stu-id="0968e-116">Component</span></span>        | <span data-ttu-id="0968e-117">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="0968e-117">Friendly Name</span></span>            | <span data-ttu-id="0968e-118">GUID</span><span class="sxs-lookup"><span data-stu-id="0968e-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="0968e-119">Formato do contêiner</span><span class="sxs-lookup"><span data-stu-id="0968e-119">Container Format</span></span> | <span data-ttu-id="0968e-120">\_CONTAINERFORMATBMP GUID</span><span class="sxs-lookup"><span data-stu-id="0968e-120">GUID\_ContainerFormatBmp</span></span> | <span data-ttu-id="0968e-121">0af1d87e-fcfe-4188-bdeba7906471cbe3</span><span class="sxs-lookup"><span data-stu-id="0968e-121">0af1d87e-fcfe-4188-bdeba7906471cbe3</span></span> |
| <span data-ttu-id="0968e-122">Decodificador</span><span class="sxs-lookup"><span data-stu-id="0968e-122">Decoder</span></span>          | <span data-ttu-id="0968e-123">\_WICBMPDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="0968e-123">CLSID\_WICBmpDecoder</span></span>     | <span data-ttu-id="0968e-124">6b462062-7cbf-400d-9fdb813dd10f2778</span><span class="sxs-lookup"><span data-stu-id="0968e-124">6b462062-7cbf-400d-9fdb813dd10f2778</span></span> |
| <span data-ttu-id="0968e-125">Codificador</span><span class="sxs-lookup"><span data-stu-id="0968e-125">Encoder</span></span>          | <span data-ttu-id="0968e-126">\_WICBMPENCODER CLSID</span><span class="sxs-lookup"><span data-stu-id="0968e-126">CLSID\_WICBmpEncoder</span></span>     | <span data-ttu-id="0968e-127">69be8bb4-d66d-47c8-865aed1589433782</span><span class="sxs-lookup"><span data-stu-id="0968e-127">69be8bb4-d66d-47c8-865aed1589433782</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="0968e-128">Codificação</span><span class="sxs-lookup"><span data-stu-id="0968e-128">Encoding</span></span>

<span data-ttu-id="0968e-129">A API de codificação do WIC é projetada para ser independente de codec e, portanto, a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="0968e-129">The WIC encoding API are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="0968e-130">Para obter mais informações sobre codificação de imagem usando a API do WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="0968e-130">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="0968e-131">Opções de codificador</span><span class="sxs-lookup"><span data-stu-id="0968e-131">Encoder Options</span></span>

<span data-ttu-id="0968e-132">Os codecs habilitados para WIC diferem no nível de opção de codificação.</span><span class="sxs-lookup"><span data-stu-id="0968e-132">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="0968e-133">As opções de codificador refletem os recursos de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador.</span><span class="sxs-lookup"><span data-stu-id="0968e-133">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="0968e-134">As opções de codificador podem ser opções básicas compatíveis com o WIC disponíveis para todos os códigos habilitados para WIC (embora não sejam necessariamente suportados) ou opções específicas de codec projetadas pelo codec de formato de imagem.</span><span class="sxs-lookup"><span data-stu-id="0968e-134">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="0968e-135">Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0968e-135">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="0968e-136">Para obter mais informações sobre como usar a interface **IPropertyBag2** para a codificação WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="0968e-136">For more information about using the **IPropertyBag2** interface for WIC encoding see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="0968e-137">A tabela a seguir lista as opções de codificador do WIC com suporte do codec BMP nativo.</span><span class="sxs-lookup"><span data-stu-id="0968e-137">The following table lists the WIC encoder options supported by the native BMP codec.</span></span>



| <span data-ttu-id="0968e-138">Nome da Propriedade</span><span class="sxs-lookup"><span data-stu-id="0968e-138">Property Name</span></span>               | <span data-ttu-id="0968e-139">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0968e-139">VARTYPE</span></span>      | <span data-ttu-id="0968e-140">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="0968e-140">Value Range</span></span>                      | <span data-ttu-id="0968e-141">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="0968e-141">Default Value</span></span>      |
|-----------------------------|--------------|----------------------------------|--------------------|
| <span data-ttu-id="0968e-142">**EnableV5Header32bppBGRA**</span><span class="sxs-lookup"><span data-stu-id="0968e-142">**EnableV5Header32bppBGRA**</span></span> | <span data-ttu-id="0968e-143">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="0968e-143">**VT\_BOOL**</span></span> | <span data-ttu-id="0968e-144">**VARIANTE \_ true/Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="0968e-144">**VARIANT\_TRUE/VARIANT\_FALSE**</span></span> | <span data-ttu-id="0968e-145">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="0968e-145">**VARIANT\_FALSE**</span></span> |



 

### <a name="enablev5header32bppbgra"></a><span data-ttu-id="0968e-146">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="0968e-146">EnableV5Header32bppBGRA</span></span>

<span data-ttu-id="0968e-147">Especifica se os dados de codificação devem ser permitidos no \_ formato de pixel WICPIXELFORMAT32BPPBGRA GUID.</span><span class="sxs-lookup"><span data-stu-id="0968e-147">Specifies whether to allow encoding data in the GUID\_WICPixelFormat32bppBGRA pixel format.</span></span> <span data-ttu-id="0968e-148">Se essa opção for definida como **Variant \_ true**, o bmp será gravado com um cabeçalho BITMAPV5HEADER.</span><span class="sxs-lookup"><span data-stu-id="0968e-148">If this option is set to **VARIANT\_TRUE**, the BMP will be written out with a BITMAPV5HEADER header.</span></span>

<span data-ttu-id="0968e-149">O valor padrão é **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="0968e-149">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="0968e-150">Se uma opção de codificador estiver presente na lista de opções de IPropertyBag2 para a qual o codec não dá suporte, ela será ignorada.</span><span class="sxs-lookup"><span data-stu-id="0968e-150">If an encoder option is present in the IPropertyBag2 option list that the codec does not support, it is ignored.</span></span>

<span data-ttu-id="0968e-151">Observação para arquivos BMP de 16 bits e de 32 bits do Windows, o codec BMP ignora qualquer canal alfa, pois muitos arquivos de imagem herdados contêm dados inválidos nesse canal extra.</span><span class="sxs-lookup"><span data-stu-id="0968e-151">Note for 16-bit and 32-bit Windows BMP files, the BMP codec ignores any alpha channel, as many legacy image files contain invalid data in this extra channel.</span></span> <span data-ttu-id="0968e-152">A partir do Windows 8, os arquivos BMP de 32 bits do Windows gravados usando o **BITMAPV5HEADER** com conteúdo de canal alfa válido são lidos como WICPixelFormat32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="0968e-152">Starting with Windows 8, 32-bit Windows BMP files written using the **BITMAPV5HEADER** with valid alpha channel content are read as WICPixelFormat32bppBGRA</span></span>

## <a name="decoding"></a><span data-ttu-id="0968e-153">Decodificação</span><span class="sxs-lookup"><span data-stu-id="0968e-153">Decoding</span></span>

<span data-ttu-id="0968e-154">A API de decodificação de WIC é projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="0968e-154">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="0968e-155">Para obter mais informações sobre a decodificação de imagem, consulte a [visão geral da decodificação](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="0968e-155">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="0968e-156">Para obter mais informações sobre como usar dados de imagem decodificados, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="0968e-156">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
