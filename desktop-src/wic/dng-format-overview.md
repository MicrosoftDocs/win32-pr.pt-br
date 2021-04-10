---
description: Este tópico fornece informações sobre o codec DNG nativo disponível por meio do Windows Imaging Component (WIC).
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Visão geral do formato DNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f766356f7c13d7b2bb25adab5411ae55c2735f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296812"
---
# <a name="dng-format-overview"></a><span data-ttu-id="d250f-103">Visão geral do formato DNG</span><span class="sxs-lookup"><span data-stu-id="d250f-103">DNG Format Overview</span></span>

<span data-ttu-id="d250f-104">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="d250f-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d250f-105">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="d250f-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d250f-106">Este tópico fornece informações sobre o codec DNG nativo disponível por meio do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="d250f-106">This topic provides information about the native DNG codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="d250f-107">Identidade do codec</span><span class="sxs-lookup"><span data-stu-id="d250f-107">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="d250f-108">Decodificação</span><span class="sxs-lookup"><span data-stu-id="d250f-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="d250f-109">Identidade do codec</span><span class="sxs-lookup"><span data-stu-id="d250f-109">Codec Identity</span></span>

<span data-ttu-id="d250f-110">A tabela a seguir fornece informações de identificação do codec.</span><span class="sxs-lookup"><span data-stu-id="d250f-110">The following table provides codec identification information.</span></span>



|                        |                                                      |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d250f-111">Nome (s) formal (es)</span><span class="sxs-lookup"><span data-stu-id="d250f-111">Formal Name(s)</span></span>         | <span data-ttu-id="d250f-112">Negativo digital (DNG)</span><span class="sxs-lookup"><span data-stu-id="d250f-112">Digital Negative (DNG)</span></span>                               |
| <span data-ttu-id="d250f-113">Extensão (s) de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="d250f-113">File Name Extension(s)</span></span> | <span data-ttu-id="d250f-114">.dng</span><span class="sxs-lookup"><span data-stu-id="d250f-114">.dng</span></span>                                                 |
| <span data-ttu-id="d250f-115">Tipo (s) MIME</span><span class="sxs-lookup"><span data-stu-id="d250f-115">MIME type(s)</span></span>           | <span data-ttu-id="d250f-116">imagem/DNG</span><span class="sxs-lookup"><span data-stu-id="d250f-116">image/DNG</span></span>                                            |
| <span data-ttu-id="d250f-117">Suporte à especificação</span><span class="sxs-lookup"><span data-stu-id="d250f-117">Specification Support</span></span>  | <span data-ttu-id="d250f-118">Especificação de DNG (digital negativo) versão 1.4.0.0</span><span class="sxs-lookup"><span data-stu-id="d250f-118">Digital Negative (DNG) Specification Version 1.4.0.0</span></span> |



 

<span data-ttu-id="d250f-119">A tabela a seguir lista os GUIDs usados para identificar os componentes nativos do codec DNG.</span><span class="sxs-lookup"><span data-stu-id="d250f-119">The following table lists the GUIDs used to identify the native DNG codec components.</span></span>



| <span data-ttu-id="d250f-120">Componente</span><span class="sxs-lookup"><span data-stu-id="d250f-120">Component</span></span>        | <span data-ttu-id="d250f-121">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="d250f-121">Friendly Name</span></span>             | <span data-ttu-id="d250f-122">GUID</span><span class="sxs-lookup"><span data-stu-id="d250f-122">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="d250f-123">Formato do contêiner</span><span class="sxs-lookup"><span data-stu-id="d250f-123">Container Format</span></span> | <span data-ttu-id="d250f-124">\_CONTAINERFORMATADNG GUID</span><span class="sxs-lookup"><span data-stu-id="d250f-124">GUID\_ContainerFormatAdng</span></span> | <span data-ttu-id="d250f-125">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span><span class="sxs-lookup"><span data-stu-id="d250f-125">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span></span> |
| <span data-ttu-id="d250f-126">Decodificador</span><span class="sxs-lookup"><span data-stu-id="d250f-126">Decoder</span></span>          | <span data-ttu-id="d250f-127">\_WICADNGDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="d250f-127">CLSID\_WICAdngDecoder</span></span>     | <span data-ttu-id="d250f-128">981d9411-909e-42a7-8f5da747ff052edb</span><span class="sxs-lookup"><span data-stu-id="d250f-128">981d9411-909e-42a7-8f5da747ff052edb</span></span> |



 

## <a name="decoding"></a><span data-ttu-id="d250f-129">Decodificação</span><span class="sxs-lookup"><span data-stu-id="d250f-129">Decoding</span></span>

<span data-ttu-id="d250f-130">A API de decodificação de WIC é projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="d250f-130">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="d250f-131">Para obter mais informações sobre a decodificação de imagem, consulte a [visão geral da decodificação](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="d250f-131">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="d250f-132">Para obter mais informações sobre como usar dados de imagem decodificados, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="d250f-132">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="d250f-133">O decodificador não dá suporte à decodificação de dados de sensor bruto e só dá suporte a arquivos com uma representação de imagem não bruta inserida em uma IFD com NewSubFileType igual a 1.</span><span class="sxs-lookup"><span data-stu-id="d250f-133">The decoder does not support decoding raw sensor data and only supports files with a non-raw image representation embedded in an IFD with NewSubFileType equal to 1.</span></span>

 

 



