---
description: Este tópico fornece informações sobre o codec de GIF nativo disponível por meio do Windows Imaging Component (WIC).
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: Visão geral do formato GIF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f592b50300edf79c71ff4050a2c0d5aeba8b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170452"
---
# <a name="gif-format-overview"></a><span data-ttu-id="b3f68-103">Visão geral do formato GIF</span><span class="sxs-lookup"><span data-stu-id="b3f68-103">GIF Format Overview</span></span>

<span data-ttu-id="b3f68-104">Este tópico fornece informações sobre o codec de GIF nativo disponível por meio do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="b3f68-104">This topic provides information about the native GIF codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="b3f68-105">Identidade do codec</span><span class="sxs-lookup"><span data-stu-id="b3f68-105">Codec Identity</span></span>

<span data-ttu-id="b3f68-106">A tabela a seguir fornece informações de identificação do codec.</span><span class="sxs-lookup"><span data-stu-id="b3f68-106">The following table provides codec identification information.</span></span>



|                        |                                       |
|------------------------|---------------------------------------|
| <span data-ttu-id="b3f68-107">Nome (s) formal (es)</span><span class="sxs-lookup"><span data-stu-id="b3f68-107">Formal Name(s)</span></span>         | <span data-ttu-id="b3f68-108">Graphics Interchange Format 89A (GIF)</span><span class="sxs-lookup"><span data-stu-id="b3f68-108">Graphics Interchange Format 89a (GIF)</span></span> |
| <span data-ttu-id="b3f68-109">Extensão (s) de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="b3f68-109">File Name Extension(s)</span></span> | <span data-ttu-id="b3f68-110">GIF</span><span class="sxs-lookup"><span data-stu-id="b3f68-110">gif</span></span>                                   |
| <span data-ttu-id="b3f68-111">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="b3f68-111">MIME type</span></span>              | <span data-ttu-id="b3f68-112">image/gif</span><span class="sxs-lookup"><span data-stu-id="b3f68-112">image/gif</span></span>                             |
| <span data-ttu-id="b3f68-113">Suporte à especificação</span><span class="sxs-lookup"><span data-stu-id="b3f68-113">Specification Support</span></span>  | <span data-ttu-id="b3f68-114">Especificação de GIF 89A/89m</span><span class="sxs-lookup"><span data-stu-id="b3f68-114">GIF Specification 89a/89m</span></span>             |



 

<span data-ttu-id="b3f68-115">A tabela a seguir lista os GUIDs usados para identificar os componentes do codec GIF nativo.</span><span class="sxs-lookup"><span data-stu-id="b3f68-115">The following table lists the GUIDs used to identify the native GIF codec components.</span></span>



| <span data-ttu-id="b3f68-116">Componente</span><span class="sxs-lookup"><span data-stu-id="b3f68-116">Component</span></span>        | <span data-ttu-id="b3f68-117">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="b3f68-117">Friendly Name</span></span>            | <span data-ttu-id="b3f68-118">GUID</span><span class="sxs-lookup"><span data-stu-id="b3f68-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="b3f68-119">Formato do contêiner</span><span class="sxs-lookup"><span data-stu-id="b3f68-119">Container Format</span></span> | <span data-ttu-id="b3f68-120">\_CONTAINERFORMATGIF GUID</span><span class="sxs-lookup"><span data-stu-id="b3f68-120">GUID\_ContainerFormatGif</span></span> | <span data-ttu-id="b3f68-121">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span><span class="sxs-lookup"><span data-stu-id="b3f68-121">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span></span> |
| <span data-ttu-id="b3f68-122">Decodificador</span><span class="sxs-lookup"><span data-stu-id="b3f68-122">Decoder</span></span>          | <span data-ttu-id="b3f68-123">\_WICGIFDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="b3f68-123">CLSID\_WICGifDecoder</span></span>     | <span data-ttu-id="b3f68-124">381dda3c-9ce9-4834-a23e1f98f8fc52be</span><span class="sxs-lookup"><span data-stu-id="b3f68-124">381dda3c-9ce9-4834-a23e1f98f8fc52be</span></span> |
| <span data-ttu-id="b3f68-125">Codificador</span><span class="sxs-lookup"><span data-stu-id="b3f68-125">Encoder</span></span>          | <span data-ttu-id="b3f68-126">\_WICGIFENCODER CLSID</span><span class="sxs-lookup"><span data-stu-id="b3f68-126">CLSID\_WICGifEncoder</span></span>     | <span data-ttu-id="b3f68-127">114f5598-0b22-40a0-86a1c83ea495adbd</span><span class="sxs-lookup"><span data-stu-id="b3f68-127">114f5598-0b22-40a0-86a1c83ea495adbd</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="b3f68-128">Codificação</span><span class="sxs-lookup"><span data-stu-id="b3f68-128">Encoding</span></span>

<span data-ttu-id="b3f68-129">A API de codificação do WIC é projetada para ser independente de codec e a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="b3f68-129">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="b3f68-130">Para obter mais informações sobre codificação de imagem usando a API do WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="b3f68-130">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="b3f68-131">Opções de codificador</span><span class="sxs-lookup"><span data-stu-id="b3f68-131">Encoder Options</span></span>

<span data-ttu-id="b3f68-132">Os codecs habilitados para WIC diferem no nível de opção de codificação.</span><span class="sxs-lookup"><span data-stu-id="b3f68-132">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="b3f68-133">As opções de codificador refletem os recursos de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador.</span><span class="sxs-lookup"><span data-stu-id="b3f68-133">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="b3f68-134">As opções de codificador podem ser opções básicas compatíveis com o WIC disponíveis para todos os códigos habilitados para WIC (embora não sejam necessariamente suportados) ou opções específicas de codec projetadas pelo codec de formato de imagem.</span><span class="sxs-lookup"><span data-stu-id="b3f68-134">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="b3f68-135">Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b3f68-135">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="b3f68-136">Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="b3f68-136">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="b3f68-137">O codificador GIF não oferece suporte a nenhuma opção básica de WIC e não fornece opções de codificador personalizadas.</span><span class="sxs-lookup"><span data-stu-id="b3f68-137">The GIF encoder does not support any basic WIC options and does not provide custom encoder options.</span></span> <span data-ttu-id="b3f68-138">Se uma opção de codificador estiver na lista de opções [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) , ela será ignorada.</span><span class="sxs-lookup"><span data-stu-id="b3f68-138">If an encoder option is in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list, it is ignored.</span></span>

## <a name="decoding"></a><span data-ttu-id="b3f68-139">Decodificação</span><span class="sxs-lookup"><span data-stu-id="b3f68-139">Decoding</span></span>

<span data-ttu-id="b3f68-140">A API de decodificação de WIC é projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="b3f68-140">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="b3f68-141">Para obter mais informações sobre a decodificação de imagem, consulte a [visão geral da decodificação](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="b3f68-141">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="b3f68-142">Para obter mais informações sobre como usar dados de imagem decodificados, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="b3f68-142">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
