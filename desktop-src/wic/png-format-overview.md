---
description: Este tópico fornece informações sobre o codec PNG nativo disponível por meio do Windows Imaging Component (WIC).
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Visão geral do formato PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb00b7530a22fcdbcce112053431ace5e553383
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444437"
---
# <a name="png-format-overview"></a><span data-ttu-id="6b11a-103">Visão geral do formato PNG</span><span class="sxs-lookup"><span data-stu-id="6b11a-103">PNG Format Overview</span></span>

<span data-ttu-id="6b11a-104">Este tópico fornece informações sobre o codec PNG nativo disponível por meio do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="6b11a-104">This topic provides information about the native PNG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="6b11a-105">Identidade do codec</span><span class="sxs-lookup"><span data-stu-id="6b11a-105">Codec Identity</span></span>

<span data-ttu-id="6b11a-106">A tabela a seguir fornece informações de identificação do codec.</span><span class="sxs-lookup"><span data-stu-id="6b11a-106">The following table provides codec identification information.</span></span>



|     <span data-ttu-id="6b11a-107">Componente</span><span class="sxs-lookup"><span data-stu-id="6b11a-107">Component</span></span>          | <span data-ttu-id="6b11a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b11a-108">Description</span></span>                     |
|------------------------|---------------------------------|
| <span data-ttu-id="6b11a-109">Nome (s) formal (es)</span><span class="sxs-lookup"><span data-stu-id="6b11a-109">Formal Name(s)</span></span>         | <span data-ttu-id="6b11a-110">PNG</span><span class="sxs-lookup"><span data-stu-id="6b11a-110">Portable Network Graphics (PNG)</span></span> |
| <span data-ttu-id="6b11a-111">Extensão (s) de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="6b11a-111">File Name Extension(s)</span></span> | <span data-ttu-id="6b11a-112">png</span><span class="sxs-lookup"><span data-stu-id="6b11a-112">png</span></span>                             |
| <span data-ttu-id="6b11a-113">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="6b11a-113">MIME type</span></span>              | <span data-ttu-id="6b11a-114">image/png</span><span class="sxs-lookup"><span data-stu-id="6b11a-114">image/png</span></span>                       |
| <span data-ttu-id="6b11a-115">Suporte à especificação</span><span class="sxs-lookup"><span data-stu-id="6b11a-115">Specification Support</span></span>  | <span data-ttu-id="6b11a-116">Especificação de PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="6b11a-116">PNG Specification 1.2</span></span>           |



 

<span data-ttu-id="6b11a-117">A tabela a seguir lista os GUIDs usados para identificar os componentes do codec PNG nativo.</span><span class="sxs-lookup"><span data-stu-id="6b11a-117">The following table lists the GUIDs used to identify the native PNG codec components.</span></span>



| <span data-ttu-id="6b11a-118">Componente</span><span class="sxs-lookup"><span data-stu-id="6b11a-118">Component</span></span>        | <span data-ttu-id="6b11a-119">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="6b11a-119">Friendly Name</span></span>            | <span data-ttu-id="6b11a-120">GUID</span><span class="sxs-lookup"><span data-stu-id="6b11a-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="6b11a-121">Formato do contêiner</span><span class="sxs-lookup"><span data-stu-id="6b11a-121">Container Format</span></span> | <span data-ttu-id="6b11a-122">\_CONTAINERFORMATPNG GUID</span><span class="sxs-lookup"><span data-stu-id="6b11a-122">GUID\_ContainerFormatPng</span></span> | <span data-ttu-id="6b11a-123">1b7cfaf4-713f-473c-bbcd6137425faeaf</span><span class="sxs-lookup"><span data-stu-id="6b11a-123">1b7cfaf4-713f-473c-bbcd6137425faeaf</span></span> |
| <span data-ttu-id="6b11a-124">Decodificador</span><span class="sxs-lookup"><span data-stu-id="6b11a-124">Decoder</span></span>          | <span data-ttu-id="6b11a-125">\_WICPNGDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="6b11a-125">CLSID\_WICPngDecoder</span></span>     | <span data-ttu-id="6b11a-126">389ea17b-5078-4cde-b6ef25c15175c751</span><span class="sxs-lookup"><span data-stu-id="6b11a-126">389ea17b-5078-4cde-b6ef25c15175c751</span></span> |
| <span data-ttu-id="6b11a-127">Codificador</span><span class="sxs-lookup"><span data-stu-id="6b11a-127">Encoder</span></span>          | <span data-ttu-id="6b11a-128">\_WICPNGENCODER CLSID</span><span class="sxs-lookup"><span data-stu-id="6b11a-128">CLSID\_WICPngEncoder</span></span>     | <span data-ttu-id="6b11a-129">27949969-876a-41d7-9447568f6a35a4dc</span><span class="sxs-lookup"><span data-stu-id="6b11a-129">27949969-876a-41d7-9447568f6a35a4dc</span></span> |



 

### <a name="windows-8-and-later"></a><span data-ttu-id="6b11a-130">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="6b11a-130">Windows 8 and later</span></span>

<span data-ttu-id="6b11a-131">A partir do WIC do Windows 8 fornece um decodificador PNG adicional</span><span class="sxs-lookup"><span data-stu-id="6b11a-131">Starting with Windows 8 WIC provides an additional PNG decoder</span></span>

## <a name="encoding"></a><span data-ttu-id="6b11a-132">Codificação</span><span class="sxs-lookup"><span data-stu-id="6b11a-132">Encoding</span></span>

<span data-ttu-id="6b11a-133">A API de codificação do WIC é projetada para ser independente de codec e a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="6b11a-133">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="6b11a-134">Para obter mais informações sobre codificação de imagem usando a API do WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="6b11a-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="6b11a-135">Opções de codificador</span><span class="sxs-lookup"><span data-stu-id="6b11a-135">Encoder Options</span></span>

<span data-ttu-id="6b11a-136">Os codecs habilitados para WIC diferem no nível de opção de codificação.</span><span class="sxs-lookup"><span data-stu-id="6b11a-136">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="6b11a-137">As opções de codificador refletem os recursos de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador.</span><span class="sxs-lookup"><span data-stu-id="6b11a-137">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="6b11a-138">As opções de codificador podem ser opções básicas compatíveis com o WIC disponíveis para todos os códigos habilitados para WIC (embora não sejam necessariamente suportados) ou opções específicas de codec projetadas pelo codec de formato de imagem.</span><span class="sxs-lookup"><span data-stu-id="6b11a-138">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="6b11a-139">Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6b11a-139">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="6b11a-140">Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="6b11a-140">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="6b11a-141">O codec PNG usa opções básicas de codificador de WIC.</span><span class="sxs-lookup"><span data-stu-id="6b11a-141">The PNG codec uses basic WIC encoder options.</span></span> <span data-ttu-id="6b11a-142">A tabela a seguir lista as opções de codificador do WIC compatíveis com o codec PNG nativo.</span><span class="sxs-lookup"><span data-stu-id="6b11a-142">The following table lists the WIC encoder options supported by the native PNG codec.</span></span>



| <span data-ttu-id="6b11a-143">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="6b11a-143">Property Name</span></span>   | <span data-ttu-id="6b11a-144">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6b11a-144">VARTYPE</span></span>  | <span data-ttu-id="6b11a-145">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="6b11a-145">Value Range</span></span>                                                 | <span data-ttu-id="6b11a-146">Valor Padrão</span><span class="sxs-lookup"><span data-stu-id="6b11a-146">Default Value</span></span>                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="6b11a-147">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="6b11a-147">InterlaceOption</span></span> | <span data-ttu-id="6b11a-148">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="6b11a-148">VT\_BOOL</span></span> | <span data-ttu-id="6b11a-149">**Verdadeiro** / **Falso**</span><span class="sxs-lookup"><span data-stu-id="6b11a-149">**TRUE**/**FALSE**</span></span>                                          | <span data-ttu-id="6b11a-150">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="6b11a-150">**FALSE**</span></span>                                                        |
| <span data-ttu-id="6b11a-151">FilterOption</span><span class="sxs-lookup"><span data-stu-id="6b11a-151">FilterOption</span></span>    | <span data-ttu-id="6b11a-152">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="6b11a-152">VT\_UI1</span></span>  | [<span data-ttu-id="6b11a-153">**WICPngFilterOption**</span><span class="sxs-lookup"><span data-stu-id="6b11a-153">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [<span data-ttu-id="6b11a-154">**WICPngFilterUnspecified**</span><span class="sxs-lookup"><span data-stu-id="6b11a-154">**WICPngFilterUnspecified**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

<span data-ttu-id="6b11a-155">Se uma opção de codificador estiver presente na lista de opções de [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) para a qual o codec não dá suporte, ela será ignorada.</span><span class="sxs-lookup"><span data-stu-id="6b11a-155">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="interlaceoption"></a><span data-ttu-id="6b11a-156">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="6b11a-156">InterlaceOption</span></span>

<span data-ttu-id="6b11a-157">Especifica se os dados da imagem devem ser codificados como entrelaçados.</span><span class="sxs-lookup"><span data-stu-id="6b11a-157">Specifies whether to encode the image data as interlaced.</span></span>

<span data-ttu-id="6b11a-158">O valor padrão é **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="6b11a-158">The default value is **FALSE**.</span></span>

### <a name="filteroption"></a><span data-ttu-id="6b11a-159">FilterOption</span><span class="sxs-lookup"><span data-stu-id="6b11a-159">FilterOption</span></span>

<span data-ttu-id="6b11a-160">Especifica a opção de filtro a ser usada para compactação de imagem.</span><span class="sxs-lookup"><span data-stu-id="6b11a-160">Specifies the filter option to use for image compression.</span></span>

<span data-ttu-id="6b11a-161">O valor padrão é [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span><span class="sxs-lookup"><span data-stu-id="6b11a-161">The default value is [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span></span>

## <a name="decoding"></a><span data-ttu-id="6b11a-162">Decodificação</span><span class="sxs-lookup"><span data-stu-id="6b11a-162">Decoding</span></span>

<span data-ttu-id="6b11a-163">A API de decodificação de WIC é projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="6b11a-163">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="6b11a-164">Para obter mais informações sobre a decodificação de imagem, consulte a [visão geral da decodificação](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="6b11a-164">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="6b11a-165">Para obter mais informações sobre como usar dados de imagem decodificados, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="6b11a-165">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="6b11a-166">O codec PNG nativo também dá suporte ao [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) na decodificação de quadros adicionando opções avançadas para decodificar um fluxo de imagem.</span><span class="sxs-lookup"><span data-stu-id="6b11a-166">The native PNG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advanced options for decoding an image stream.</span></span> <span data-ttu-id="6b11a-167">Para obter mais informações sobre essas opções avançadas, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="6b11a-167">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
