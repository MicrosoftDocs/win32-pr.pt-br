---
description: Este tópico fornece informações sobre o codec DNG nativo disponível por meio Windows Imaging Component (WIC).
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Visão geral do formato DNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0815d6a24bb8e57e6c64b90f9e9068765838e148
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444927"
---
# <a name="dng-format-overview"></a><span data-ttu-id="dcad0-103">Visão geral do formato DNG</span><span class="sxs-lookup"><span data-stu-id="dcad0-103">DNG Format Overview</span></span>

<span data-ttu-id="dcad0-104">\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="dcad0-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dcad0-105">A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]</span><span class="sxs-lookup"><span data-stu-id="dcad0-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dcad0-106">Este tópico fornece informações sobre o codec DNG nativo disponível por meio Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="dcad0-106">This topic provides information about the native DNG codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="dcad0-107">Identidade do Codec</span><span class="sxs-lookup"><span data-stu-id="dcad0-107">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="dcad0-108">Decodificação</span><span class="sxs-lookup"><span data-stu-id="dcad0-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="dcad0-109">Identidade do Codec</span><span class="sxs-lookup"><span data-stu-id="dcad0-109">Codec Identity</span></span>

<span data-ttu-id="dcad0-110">A tabela a seguir fornece informações de identificação de codec.</span><span class="sxs-lookup"><span data-stu-id="dcad0-110">The following table provides codec identification information.</span></span>



|     <span data-ttu-id="dcad0-111">Componente</span><span class="sxs-lookup"><span data-stu-id="dcad0-111">Component</span></span>          |  <span data-ttu-id="dcad0-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="dcad0-112">Description</span></span>                                         |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="dcad0-113">Nomes formais</span><span class="sxs-lookup"><span data-stu-id="dcad0-113">Formal Name(s)</span></span>         | <span data-ttu-id="dcad0-114">DNG (Digital Negative)</span><span class="sxs-lookup"><span data-stu-id="dcad0-114">Digital Negative (DNG)</span></span>                               |
| <span data-ttu-id="dcad0-115">Extensões de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="dcad0-115">File Name Extension(s)</span></span> | <span data-ttu-id="dcad0-116">.dng</span><span class="sxs-lookup"><span data-stu-id="dcad0-116">.dng</span></span>                                                 |
| <span data-ttu-id="dcad0-117">Tipos MIME</span><span class="sxs-lookup"><span data-stu-id="dcad0-117">MIME type(s)</span></span>           | <span data-ttu-id="dcad0-118">image/DNG</span><span class="sxs-lookup"><span data-stu-id="dcad0-118">image/DNG</span></span>                                            |
| <span data-ttu-id="dcad0-119">Suporte à especificação</span><span class="sxs-lookup"><span data-stu-id="dcad0-119">Specification Support</span></span>  | <span data-ttu-id="dcad0-120">Especificação DNG (Digital Negative) Versão 1.4.0.0</span><span class="sxs-lookup"><span data-stu-id="dcad0-120">Digital Negative (DNG) Specification Version 1.4.0.0</span></span> |



 

<span data-ttu-id="dcad0-121">A tabela a seguir lista os GUIDs usados para identificar os componentes nativos do codec DNG.</span><span class="sxs-lookup"><span data-stu-id="dcad0-121">The following table lists the GUIDs used to identify the native DNG codec components.</span></span>



| <span data-ttu-id="dcad0-122">Componente</span><span class="sxs-lookup"><span data-stu-id="dcad0-122">Component</span></span>        | <span data-ttu-id="dcad0-123">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="dcad0-123">Friendly Name</span></span>             | <span data-ttu-id="dcad0-124">GUID</span><span class="sxs-lookup"><span data-stu-id="dcad0-124">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="dcad0-125">Formato do contêiner</span><span class="sxs-lookup"><span data-stu-id="dcad0-125">Container Format</span></span> | <span data-ttu-id="dcad0-126">GUID \_ ContainerFormatAdng</span><span class="sxs-lookup"><span data-stu-id="dcad0-126">GUID\_ContainerFormatAdng</span></span> | <span data-ttu-id="dcad0-127">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span><span class="sxs-lookup"><span data-stu-id="dcad0-127">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span></span> |
| <span data-ttu-id="dcad0-128">Decodificador</span><span class="sxs-lookup"><span data-stu-id="dcad0-128">Decoder</span></span>          | <span data-ttu-id="dcad0-129">CLSID \_ WICAdngDecoder</span><span class="sxs-lookup"><span data-stu-id="dcad0-129">CLSID\_WICAdngDecoder</span></span>     | <span data-ttu-id="dcad0-130">981d9411-909e-42a7-8f5da747ff052edb</span><span class="sxs-lookup"><span data-stu-id="dcad0-130">981d9411-909e-42a7-8f5da747ff052edb</span></span> |



 

## <a name="decoding"></a><span data-ttu-id="dcad0-131">Decodificação</span><span class="sxs-lookup"><span data-stu-id="dcad0-131">Decoding</span></span>

<span data-ttu-id="dcad0-132">A API de decodificação do WIC foi projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="dcad0-132">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="dcad0-133">Para obter mais informações sobre decodificação de imagem, consulte Visão [geral de decodificação.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="dcad0-133">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="dcad0-134">Para obter mais informações sobre como usar dados de imagem decodificados, consulte Visão geral das [fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="dcad0-134">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="dcad0-135">O decodificador não dá suporte à decodificação de dados brutos do sensor e só dá suporte a arquivos com uma representação de imagem não bruta inserida em um IFD com NewSubFileType igual a 1.</span><span class="sxs-lookup"><span data-stu-id="dcad0-135">The decoder does not support decoding raw sensor data and only supports files with a non-raw image representation embedded in an IFD with NewSubFileType equal to 1.</span></span>

 

 



