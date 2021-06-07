---
description: Este tópico fornece informações sobre o codec GIF nativo disponível por meio do Windows Imaging Component (WIC).
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: Visão geral do formato GIF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf7e9924c921b7944de114f5fe667cb2aa33cae
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444447"
---
# <a name="gif-format-overview"></a><span data-ttu-id="8a93a-103">Visão geral do formato GIF</span><span class="sxs-lookup"><span data-stu-id="8a93a-103">GIF Format Overview</span></span>

<span data-ttu-id="8a93a-104">Este tópico fornece informações sobre o codec GIF nativo disponível por meio do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="8a93a-104">This topic provides information about the native GIF codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="8a93a-105">Identidade do Codec</span><span class="sxs-lookup"><span data-stu-id="8a93a-105">Codec Identity</span></span>

<span data-ttu-id="8a93a-106">A tabela a seguir fornece informações de identificação de codec.</span><span class="sxs-lookup"><span data-stu-id="8a93a-106">The following table provides codec identification information.</span></span>



|  <span data-ttu-id="8a93a-107">Componente</span><span class="sxs-lookup"><span data-stu-id="8a93a-107">Component</span></span>             | <span data-ttu-id="8a93a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a93a-108">Description</span></span>                           |
|------------------------|---------------------------------------|
| <span data-ttu-id="8a93a-109">Nomes formais</span><span class="sxs-lookup"><span data-stu-id="8a93a-109">Formal Name(s)</span></span>         | <span data-ttu-id="8a93a-110">Graphics Interchange Format 89a (GIF)</span><span class="sxs-lookup"><span data-stu-id="8a93a-110">Graphics Interchange Format 89a (GIF)</span></span> |
| <span data-ttu-id="8a93a-111">Extensões de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="8a93a-111">File Name Extension(s)</span></span> | <span data-ttu-id="8a93a-112">GIF</span><span class="sxs-lookup"><span data-stu-id="8a93a-112">gif</span></span>                                   |
| <span data-ttu-id="8a93a-113">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="8a93a-113">MIME type</span></span>              | <span data-ttu-id="8a93a-114">image/gif</span><span class="sxs-lookup"><span data-stu-id="8a93a-114">image/gif</span></span>                             |
| <span data-ttu-id="8a93a-115">Suporte à especificação</span><span class="sxs-lookup"><span data-stu-id="8a93a-115">Specification Support</span></span>  | <span data-ttu-id="8a93a-116">Especificação GIF 89a/89m</span><span class="sxs-lookup"><span data-stu-id="8a93a-116">GIF Specification 89a/89m</span></span>             |



 

<span data-ttu-id="8a93a-117">A tabela a seguir lista os GUIDs usados para identificar os componentes nativos de codec gif.</span><span class="sxs-lookup"><span data-stu-id="8a93a-117">The following table lists the GUIDs used to identify the native GIF codec components.</span></span>



| <span data-ttu-id="8a93a-118">Componente</span><span class="sxs-lookup"><span data-stu-id="8a93a-118">Component</span></span>        | <span data-ttu-id="8a93a-119">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="8a93a-119">Friendly Name</span></span>            | <span data-ttu-id="8a93a-120">GUID</span><span class="sxs-lookup"><span data-stu-id="8a93a-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="8a93a-121">Formato do contêiner</span><span class="sxs-lookup"><span data-stu-id="8a93a-121">Container Format</span></span> | <span data-ttu-id="8a93a-122">Contêiner \_ GUIDFormatGif</span><span class="sxs-lookup"><span data-stu-id="8a93a-122">GUID\_ContainerFormatGif</span></span> | <span data-ttu-id="8a93a-123">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span><span class="sxs-lookup"><span data-stu-id="8a93a-123">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span></span> |
| <span data-ttu-id="8a93a-124">Decodificador</span><span class="sxs-lookup"><span data-stu-id="8a93a-124">Decoder</span></span>          | <span data-ttu-id="8a93a-125">CLSID \_ WICGifDecoder</span><span class="sxs-lookup"><span data-stu-id="8a93a-125">CLSID\_WICGifDecoder</span></span>     | <span data-ttu-id="8a93a-126">381dda3c-9ce9-4834-a23e1f98f8fc52be</span><span class="sxs-lookup"><span data-stu-id="8a93a-126">381dda3c-9ce9-4834-a23e1f98f8fc52be</span></span> |
| <span data-ttu-id="8a93a-127">Codificador</span><span class="sxs-lookup"><span data-stu-id="8a93a-127">Encoder</span></span>          | <span data-ttu-id="8a93a-128">CLSID \_ WICGifEncoder</span><span class="sxs-lookup"><span data-stu-id="8a93a-128">CLSID\_WICGifEncoder</span></span>     | <span data-ttu-id="8a93a-129">114f5598-0b22-40a0-86a1c83ea495adbd</span><span class="sxs-lookup"><span data-stu-id="8a93a-129">114f5598-0b22-40a0-86a1c83ea495adbd</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="8a93a-130">Codificação</span><span class="sxs-lookup"><span data-stu-id="8a93a-130">Encoding</span></span>

<span data-ttu-id="8a93a-131">A API de codificação WIC foi projetada para ser independente de codec e a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="8a93a-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="8a93a-132">Para obter mais informações sobre a codificação de imagem usando a API WIC, consulte a [Visão geral de codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="8a93a-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="8a93a-133">Opções do codificador</span><span class="sxs-lookup"><span data-stu-id="8a93a-133">Encoder Options</span></span>

<span data-ttu-id="8a93a-134">Os codecs habilitados para WIC diferem no nível da opção de codificação.</span><span class="sxs-lookup"><span data-stu-id="8a93a-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="8a93a-135">As opções do codificador refletem as funcionalidades de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador.</span><span class="sxs-lookup"><span data-stu-id="8a93a-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="8a93a-136">As opções de codificador podem ser opções básicas com suporte do WIC disponíveis para todos os códigos habilitados para WIC (embora não necessariamente com suporte) ou opções específicas de codec projetadas pelo codec de formato de imagem.</span><span class="sxs-lookup"><span data-stu-id="8a93a-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="8a93a-137">Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8a93a-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="8a93a-138">Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte a Visão geral [de codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="8a93a-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="8a93a-139">O codificador GIF não dá suporte a nenhuma opção básica do WIC e não fornece opções de codificador personalizadas.</span><span class="sxs-lookup"><span data-stu-id="8a93a-139">The GIF encoder does not support any basic WIC options and does not provide custom encoder options.</span></span> <span data-ttu-id="8a93a-140">Se uma opção de codificador estiver na [**lista de opções IPropertyBag2,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) ela será ignorada.</span><span class="sxs-lookup"><span data-stu-id="8a93a-140">If an encoder option is in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list, it is ignored.</span></span>

## <a name="decoding"></a><span data-ttu-id="8a93a-141">Decodificação</span><span class="sxs-lookup"><span data-stu-id="8a93a-141">Decoding</span></span>

<span data-ttu-id="8a93a-142">A API de decodificação do WIC foi projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="8a93a-142">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="8a93a-143">Para obter mais informações sobre decodificação de imagem, consulte Visão [geral de decodificação.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="8a93a-143">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="8a93a-144">Para obter mais informações sobre como usar dados de imagem decodificados, consulte Visão geral das [fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="8a93a-144">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
