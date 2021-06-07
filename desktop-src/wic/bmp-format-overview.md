---
description: Este tópico fornece informações sobre o codec BMP nativo disponível por meio do WIC (Windows Imaging Component).
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Visão geral do formato BMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975f27af5b731ed1f62f3571109553848705239
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444957"
---
# <a name="bmp-format-overview"></a><span data-ttu-id="a298f-103">Visão geral do formato BMP</span><span class="sxs-lookup"><span data-stu-id="a298f-103">BMP Format Overview</span></span>

<span data-ttu-id="a298f-104">Este tópico fornece informações sobre o codec BMP nativo disponível por meio do WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="a298f-104">This topic provides information about the native BMP codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="a298f-105">Identidade do Codec</span><span class="sxs-lookup"><span data-stu-id="a298f-105">Codec Identity</span></span>

<span data-ttu-id="a298f-106">A tabela a seguir fornece informações de identificação de codec.</span><span class="sxs-lookup"><span data-stu-id="a298f-106">The following table provides codec identification information.</span></span>



| <span data-ttu-id="a298f-107">Componente</span><span class="sxs-lookup"><span data-stu-id="a298f-107">Component</span></span>              | <span data-ttu-id="a298f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a298f-108">Description</span></span>           |
|------------------------|-----------------------|
| <span data-ttu-id="a298f-109">Nomes formais</span><span class="sxs-lookup"><span data-stu-id="a298f-109">Formal Name(s)</span></span>         | <span data-ttu-id="a298f-110">Formato bitmap do Windows</span><span class="sxs-lookup"><span data-stu-id="a298f-110">Windows Bitmap Format</span></span> |
| <span data-ttu-id="a298f-111">Extensões de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="a298f-111">File Name Extension(s)</span></span> | <span data-ttu-id="a298f-112">bmp, dib</span><span class="sxs-lookup"><span data-stu-id="a298f-112">bmp, dib</span></span>              |
| <span data-ttu-id="a298f-113">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="a298f-113">MIME type</span></span>              | <span data-ttu-id="a298f-114">image/bmp</span><span class="sxs-lookup"><span data-stu-id="a298f-114">image/bmp</span></span>             |
| <span data-ttu-id="a298f-115">Suporte à especificação</span><span class="sxs-lookup"><span data-stu-id="a298f-115">Specification Support</span></span>  | <span data-ttu-id="a298f-116">Especificação BMP v5</span><span class="sxs-lookup"><span data-stu-id="a298f-116">BMP Specification v5</span></span>  |



 

<span data-ttu-id="a298f-117">A tabela a seguir lista os GUIDs usados para identificar os componentes nativos do codec BMP.</span><span class="sxs-lookup"><span data-stu-id="a298f-117">The following table lists the GUIDs used to identify the native BMP codec components.</span></span>



| <span data-ttu-id="a298f-118">Componente</span><span class="sxs-lookup"><span data-stu-id="a298f-118">Component</span></span>        | <span data-ttu-id="a298f-119">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="a298f-119">Friendly Name</span></span>            | <span data-ttu-id="a298f-120">GUID</span><span class="sxs-lookup"><span data-stu-id="a298f-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="a298f-121">Formato do contêiner</span><span class="sxs-lookup"><span data-stu-id="a298f-121">Container Format</span></span> | <span data-ttu-id="a298f-122">Contêiner \_ GUIDFormatBmp</span><span class="sxs-lookup"><span data-stu-id="a298f-122">GUID\_ContainerFormatBmp</span></span> | <span data-ttu-id="a298f-123">0af1d87e-fcfe-4188-bdeba7906471cbe3</span><span class="sxs-lookup"><span data-stu-id="a298f-123">0af1d87e-fcfe-4188-bdeba7906471cbe3</span></span> |
| <span data-ttu-id="a298f-124">Decodificador</span><span class="sxs-lookup"><span data-stu-id="a298f-124">Decoder</span></span>          | <span data-ttu-id="a298f-125">CLSID \_ WICBmpDecoder</span><span class="sxs-lookup"><span data-stu-id="a298f-125">CLSID\_WICBmpDecoder</span></span>     | <span data-ttu-id="a298f-126">6b462062-7cbf-400d-9fdb813dd10f2778</span><span class="sxs-lookup"><span data-stu-id="a298f-126">6b462062-7cbf-400d-9fdb813dd10f2778</span></span> |
| <span data-ttu-id="a298f-127">Codificador</span><span class="sxs-lookup"><span data-stu-id="a298f-127">Encoder</span></span>          | <span data-ttu-id="a298f-128">CLSID \_ WICBmpEncoder</span><span class="sxs-lookup"><span data-stu-id="a298f-128">CLSID\_WICBmpEncoder</span></span>     | <span data-ttu-id="a298f-129">69be8bb4-d66d-47c8-865aed1589433782</span><span class="sxs-lookup"><span data-stu-id="a298f-129">69be8bb4-d66d-47c8-865aed1589433782</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="a298f-130">Codificação</span><span class="sxs-lookup"><span data-stu-id="a298f-130">Encoding</span></span>

<span data-ttu-id="a298f-131">A API de codificação WIC foi projetada para ser independente de codec e, portanto, a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="a298f-131">The WIC encoding API are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="a298f-132">Para obter mais informações sobre a codificação de imagem usando a API WIC, consulte a [Visão geral de codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="a298f-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="a298f-133">Opções do codificador</span><span class="sxs-lookup"><span data-stu-id="a298f-133">Encoder Options</span></span>

<span data-ttu-id="a298f-134">Os codecs habilitados para WIC diferem no nível da opção de codificação.</span><span class="sxs-lookup"><span data-stu-id="a298f-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="a298f-135">As opções do codificador refletem as funcionalidades de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador.</span><span class="sxs-lookup"><span data-stu-id="a298f-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="a298f-136">As opções de codificador podem ser opções básicas com suporte do WIC disponíveis para todos os códigos habilitados para WIC (embora não necessariamente com suporte) ou opções específicas de codec projetadas pelo codec de formato de imagem.</span><span class="sxs-lookup"><span data-stu-id="a298f-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="a298f-137">Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a298f-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="a298f-138">Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte Visão [geral da codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="a298f-138">For more information about using the **IPropertyBag2** interface for WIC encoding see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="a298f-139">A tabela a seguir lista as opções do codificador WIC com suporte pelo codec BMP nativo.</span><span class="sxs-lookup"><span data-stu-id="a298f-139">The following table lists the WIC encoder options supported by the native BMP codec.</span></span>



| <span data-ttu-id="a298f-140">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="a298f-140">Property Name</span></span>               | <span data-ttu-id="a298f-141">Vartype</span><span class="sxs-lookup"><span data-stu-id="a298f-141">VARTYPE</span></span>      | <span data-ttu-id="a298f-142">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="a298f-142">Value Range</span></span>                      | <span data-ttu-id="a298f-143">Valor Padrão</span><span class="sxs-lookup"><span data-stu-id="a298f-143">Default Value</span></span>      |
|-----------------------------|--------------|----------------------------------|--------------------|
| <span data-ttu-id="a298f-144">**EnableV5Header32bppBGRA**</span><span class="sxs-lookup"><span data-stu-id="a298f-144">**EnableV5Header32bppBGRA**</span></span> | <span data-ttu-id="a298f-145">**BOOL da VT \_**</span><span class="sxs-lookup"><span data-stu-id="a298f-145">**VT\_BOOL**</span></span> | <span data-ttu-id="a298f-146">**VARIANT \_ TRUE/VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="a298f-146">**VARIANT\_TRUE/VARIANT\_FALSE**</span></span> | <span data-ttu-id="a298f-147">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="a298f-147">**VARIANT\_FALSE**</span></span> |



 

### <a name="enablev5header32bppbgra"></a><span data-ttu-id="a298f-148">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="a298f-148">EnableV5Header32bppBGRA</span></span>

<span data-ttu-id="a298f-149">Especifica se é necessário permitir a codificação de dados no formato de \_ pixel WICPixelFormat32bppBGRA de GUID.</span><span class="sxs-lookup"><span data-stu-id="a298f-149">Specifies whether to allow encoding data in the GUID\_WICPixelFormat32bppBGRA pixel format.</span></span> <span data-ttu-id="a298f-150">Se essa opção for definida como **VARIANT \_ TRUE,** o BMP será gravado com um header BITMAPV5HEADER.</span><span class="sxs-lookup"><span data-stu-id="a298f-150">If this option is set to **VARIANT\_TRUE**, the BMP will be written out with a BITMAPV5HEADER header.</span></span>

<span data-ttu-id="a298f-151">O valor padrão é **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="a298f-151">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="a298f-152">Se uma opção de codificador estiver presente na lista de opções IPropertyBag2 à qual o codec não dá suporte, ela será ignorada.</span><span class="sxs-lookup"><span data-stu-id="a298f-152">If an encoder option is present in the IPropertyBag2 option list that the codec does not support, it is ignored.</span></span>

<span data-ttu-id="a298f-153">Observação para arquivos BMP do Windows de 16 bits e 32 bits, o codec BMP ignora qualquer canal alfa, pois muitos arquivos de imagem herdados contêm dados inválidos nesse canal extra.</span><span class="sxs-lookup"><span data-stu-id="a298f-153">Note for 16-bit and 32-bit Windows BMP files, the BMP codec ignores any alpha channel, as many legacy image files contain invalid data in this extra channel.</span></span> <span data-ttu-id="a298f-154">A partir do Windows 8, os arquivos BMP do Windows de 32 bits gravados usando **o BITMAPV5HEADER** com conteúdo de canal alfa válido são lidos como WICPixelFormat32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="a298f-154">Starting with Windows 8, 32-bit Windows BMP files written using the **BITMAPV5HEADER** with valid alpha channel content are read as WICPixelFormat32bppBGRA</span></span>

## <a name="decoding"></a><span data-ttu-id="a298f-155">Decodificação</span><span class="sxs-lookup"><span data-stu-id="a298f-155">Decoding</span></span>

<span data-ttu-id="a298f-156">A API de decodificação do WIC foi projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="a298f-156">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="a298f-157">Para obter mais informações sobre decodificação de imagem, consulte Visão [geral de decodificação.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="a298f-157">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="a298f-158">Para obter mais informações sobre como usar dados de imagem decodificados, consulte Visão geral das [fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="a298f-158">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
