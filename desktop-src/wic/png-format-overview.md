---
description: Este tópico fornece informações sobre o codec PNG nativo disponível por meio do Windows Imaging Component (WIC).
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Visão geral do formato PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118d6af831c8fb6f8cacc8407e90f610c0fc426d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765267"
---
# <a name="png-format-overview"></a><span data-ttu-id="eb4d2-103">Visão geral do formato PNG</span><span class="sxs-lookup"><span data-stu-id="eb4d2-103">PNG Format Overview</span></span>

<span data-ttu-id="eb4d2-104">Este tópico fornece informações sobre o codec PNG nativo disponível por meio do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="eb4d2-104">This topic provides information about the native PNG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="eb4d2-105">Identidade do codec</span><span class="sxs-lookup"><span data-stu-id="eb4d2-105">Codec Identity</span></span>

<span data-ttu-id="eb4d2-106">A tabela a seguir fornece informações de identificação do codec.</span><span class="sxs-lookup"><span data-stu-id="eb4d2-106">The following table provides codec identification information.</span></span>



|                        |                                 |
|------------------------|---------------------------------|
| <span data-ttu-id="eb4d2-107">Nome (s) formal (es)</span><span class="sxs-lookup"><span data-stu-id="eb4d2-107">Formal Name(s)</span></span>         | <span data-ttu-id="eb4d2-108">PNG</span><span class="sxs-lookup"><span data-stu-id="eb4d2-108">Portable Network Graphics (PNG)</span></span> |
| <span data-ttu-id="eb4d2-109">Extensão (s) de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="eb4d2-109">File Name Extension(s)</span></span> | <span data-ttu-id="eb4d2-110">png</span><span class="sxs-lookup"><span data-stu-id="eb4d2-110">png</span></span>                             |
| <span data-ttu-id="eb4d2-111">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="eb4d2-111">MIME type</span></span>              | <span data-ttu-id="eb4d2-112">image/png</span><span class="sxs-lookup"><span data-stu-id="eb4d2-112">image/png</span></span>                       |
| <span data-ttu-id="eb4d2-113">Suporte à especificação</span><span class="sxs-lookup"><span data-stu-id="eb4d2-113">Specification Support</span></span>  | <span data-ttu-id="eb4d2-114">Especificação de PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="eb4d2-114">PNG Specification 1.2</span></span>           |



 

<span data-ttu-id="eb4d2-115">A tabela a seguir lista os GUIDs usados para identificar os componentes do codec PNG nativo.</span><span class="sxs-lookup"><span data-stu-id="eb4d2-115">The following table lists the GUIDs used to identify the native PNG codec components.</span></span>



| <span data-ttu-id="eb4d2-116">Componente</span><span class="sxs-lookup"><span data-stu-id="eb4d2-116">Component</span></span>        | <span data-ttu-id="eb4d2-117">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="eb4d2-117">Friendly Name</span></span>            | <span data-ttu-id="eb4d2-118">GUID</span><span class="sxs-lookup"><span data-stu-id="eb4d2-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="eb4d2-119">Formato do contêiner</span><span class="sxs-lookup"><span data-stu-id="eb4d2-119">Container Format</span></span> | <span data-ttu-id="eb4d2-120">\_CONTAINERFORMATPNG GUID</span><span class="sxs-lookup"><span data-stu-id="eb4d2-120">GUID\_ContainerFormatPng</span></span> | <span data-ttu-id="eb4d2-121">1b7cfaf4-713f-473c-bbcd6137425faeaf</span><span class="sxs-lookup"><span data-stu-id="eb4d2-121">1b7cfaf4-713f-473c-bbcd6137425faeaf</span></span> |
| <span data-ttu-id="eb4d2-122">Decodificador</span><span class="sxs-lookup"><span data-stu-id="eb4d2-122">Decoder</span></span>          | <span data-ttu-id="eb4d2-123">\_WICPNGDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="eb4d2-123">CLSID\_WICPngDecoder</span></span>     | <span data-ttu-id="eb4d2-124">389ea17b-5078-4cde-b6ef25c15175c751</span><span class="sxs-lookup"><span data-stu-id="eb4d2-124">389ea17b-5078-4cde-b6ef25c15175c751</span></span> |
| <span data-ttu-id="eb4d2-125">Codificador</span><span class="sxs-lookup"><span data-stu-id="eb4d2-125">Encoder</span></span>          | <span data-ttu-id="eb4d2-126">\_WICPNGENCODER CLSID</span><span class="sxs-lookup"><span data-stu-id="eb4d2-126">CLSID\_WICPngEncoder</span></span>     | <span data-ttu-id="eb4d2-127">27949969-876a-41d7-9447568f6a35a4dc</span><span class="sxs-lookup"><span data-stu-id="eb4d2-127">27949969-876a-41d7-9447568f6a35a4dc</span></span> |



 

### <a name="windows-8-and-later"></a><span data-ttu-id="eb4d2-128">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="eb4d2-128">Windows 8 and later</span></span>

<span data-ttu-id="eb4d2-129">A partir do WIC do Windows 8 fornece um decodificador PNG adicional</span><span class="sxs-lookup"><span data-stu-id="eb4d2-129">Starting with Windows 8 WIC provides an additional PNG decoder</span></span>

## <a name="encoding"></a><span data-ttu-id="eb4d2-130">Codificação</span><span class="sxs-lookup"><span data-stu-id="eb4d2-130">Encoding</span></span>

<span data-ttu-id="eb4d2-131">A API de codificação do WIC é projetada para ser independente de codec e a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="eb4d2-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="eb4d2-132">Para obter mais informações sobre codificação de imagem usando a API do WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="eb4d2-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="eb4d2-133">Opções de codificador</span><span class="sxs-lookup"><span data-stu-id="eb4d2-133">Encoder Options</span></span>

<span data-ttu-id="eb4d2-134">Os codecs habilitados para WIC diferem no nível de opção de codificação.</span><span class="sxs-lookup"><span data-stu-id="eb4d2-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="eb4d2-135">As opções de codificador refletem os recursos de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador.</span><span class="sxs-lookup"><span data-stu-id="eb4d2-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="eb4d2-136">As opções de codificador podem ser opções básicas compatíveis com o WIC disponíveis para todos os códigos habilitados para WIC (embora não sejam necessariamente suportados) ou opções específicas de codec projetadas pelo codec de formato de imagem.</span><span class="sxs-lookup"><span data-stu-id="eb4d2-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="eb4d2-137">Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="eb4d2-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="eb4d2-138">Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="eb4d2-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="eb4d2-139">O codec PNG usa opções básicas de codificador de WIC.</span><span class="sxs-lookup"><span data-stu-id="eb4d2-139">The PNG codec uses basic WIC encoder options.</span></span> <span data-ttu-id="eb4d2-140">A tabela a seguir lista as opções de codificador do WIC compatíveis com o codec PNG nativo.</span><span class="sxs-lookup"><span data-stu-id="eb4d2-140">The following table lists the WIC encoder options supported by the native PNG codec.</span></span>



| <span data-ttu-id="eb4d2-141">Nome da Propriedade</span><span class="sxs-lookup"><span data-stu-id="eb4d2-141">Property Name</span></span>   | <span data-ttu-id="eb4d2-142">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="eb4d2-142">VARTYPE</span></span>  | <span data-ttu-id="eb4d2-143">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="eb4d2-143">Value Range</span></span>                                                 | <span data-ttu-id="eb4d2-144">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="eb4d2-144">Default Value</span></span>                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="eb4d2-145">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="eb4d2-145">InterlaceOption</span></span> | <span data-ttu-id="eb4d2-146">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="eb4d2-146">VT\_BOOL</span></span> | <span data-ttu-id="eb4d2-147">**Verdadeiro** / **Falso**</span><span class="sxs-lookup"><span data-stu-id="eb4d2-147">**TRUE**/**FALSE**</span></span>                                          | <span data-ttu-id="eb4d2-148">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="eb4d2-148">**FALSE**</span></span>                                                        |
| <span data-ttu-id="eb4d2-149">FilterOption</span><span class="sxs-lookup"><span data-stu-id="eb4d2-149">FilterOption</span></span>    | <span data-ttu-id="eb4d2-150">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="eb4d2-150">VT\_UI1</span></span>  | [<span data-ttu-id="eb4d2-151">**WICPngFilterOption**</span><span class="sxs-lookup"><span data-stu-id="eb4d2-151">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [<span data-ttu-id="eb4d2-152">**WICPngFilterUnspecified**</span><span class="sxs-lookup"><span data-stu-id="eb4d2-152">**WICPngFilterUnspecified**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

<span data-ttu-id="eb4d2-153">Se uma opção de codificador estiver presente na lista de opções de [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) para a qual o codec não dá suporte, ela será ignorada.</span><span class="sxs-lookup"><span data-stu-id="eb4d2-153">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="interlaceoption"></a><span data-ttu-id="eb4d2-154">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="eb4d2-154">InterlaceOption</span></span>

<span data-ttu-id="eb4d2-155">Especifica se os dados da imagem devem ser codificados como entrelaçados.</span><span class="sxs-lookup"><span data-stu-id="eb4d2-155">Specifies whether to encode the image data as interlaced.</span></span>

<span data-ttu-id="eb4d2-156">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="eb4d2-156">The default value is **FALSE**.</span></span>

### <a name="filteroption"></a><span data-ttu-id="eb4d2-157">FilterOption</span><span class="sxs-lookup"><span data-stu-id="eb4d2-157">FilterOption</span></span>

<span data-ttu-id="eb4d2-158">Especifica a opção de filtro a ser usada para compactação de imagem.</span><span class="sxs-lookup"><span data-stu-id="eb4d2-158">Specifies the filter option to use for image compression.</span></span>

<span data-ttu-id="eb4d2-159">O valor padrão é [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span><span class="sxs-lookup"><span data-stu-id="eb4d2-159">The default value is [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span></span>

## <a name="decoding"></a><span data-ttu-id="eb4d2-160">Decodificação</span><span class="sxs-lookup"><span data-stu-id="eb4d2-160">Decoding</span></span>

<span data-ttu-id="eb4d2-161">A API de decodificação de WIC é projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="eb4d2-161">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="eb4d2-162">Para obter mais informações sobre a decodificação de imagem, consulte a [visão geral da decodificação](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="eb4d2-162">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="eb4d2-163">Para obter mais informações sobre como usar dados de imagem decodificados, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="eb4d2-163">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="eb4d2-164">O codec PNG nativo também dá suporte ao [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) na decodificação de quadros adicionando opções avançadas para decodificar um fluxo de imagem.</span><span class="sxs-lookup"><span data-stu-id="eb4d2-164">The native PNG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advanced options for decoding an image stream.</span></span> <span data-ttu-id="eb4d2-165">Para obter mais informações sobre essas opções avançadas, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="eb4d2-165">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
