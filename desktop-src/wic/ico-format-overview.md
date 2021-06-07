---
description: Este tópico fornece informações sobre o codec de ICO nativo disponível por meio Windows Imaging Component (WIC).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Visão geral do formato ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329a53a3b5d386c5e5386141162c608dc9db1ec0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444459"
---
# <a name="ico-format-overview"></a><span data-ttu-id="e0d01-103">Visão geral do formato ICO</span><span class="sxs-lookup"><span data-stu-id="e0d01-103">ICO Format Overview</span></span>

<span data-ttu-id="e0d01-104">Este tópico fornece informações sobre o codec de ICO nativo disponível por meio Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="e0d01-104">This topic provides information about the native ICO codec available through Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="e0d01-105">Identidade do Codec</span><span class="sxs-lookup"><span data-stu-id="e0d01-105">Codec Identity</span></span>

<span data-ttu-id="e0d01-106">A tabela a seguir fornece informações de identificação de codec.</span><span class="sxs-lookup"><span data-stu-id="e0d01-106">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="e0d01-107">Componente</span><span class="sxs-lookup"><span data-stu-id="e0d01-107">Component</span></span>            | <span data-ttu-id="e0d01-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0d01-108">Description</span></span>       |
|------------------------|-------------------|
| <span data-ttu-id="e0d01-109">Nomes formais</span><span class="sxs-lookup"><span data-stu-id="e0d01-109">Formal Name(s)</span></span>         | <span data-ttu-id="e0d01-110">Formato de ícone (ICO)</span><span class="sxs-lookup"><span data-stu-id="e0d01-110">Icon Format (ICO)</span></span> |
| <span data-ttu-id="e0d01-111">Extensões de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="e0d01-111">File Name Extension(s)</span></span> | <span data-ttu-id="e0d01-112">Ico</span><span class="sxs-lookup"><span data-stu-id="e0d01-112">ico</span></span>               |
| <span data-ttu-id="e0d01-113">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="e0d01-113">MIME type</span></span>              | <span data-ttu-id="e0d01-114">image/ico</span><span class="sxs-lookup"><span data-stu-id="e0d01-114">image/ico</span></span>         |
| <span data-ttu-id="e0d01-115">Suporte à especificação</span><span class="sxs-lookup"><span data-stu-id="e0d01-115">Specification Support</span></span>  |                   |



 

<span data-ttu-id="e0d01-116">A tabela a seguir lista os GUIDs usados para identificar os componentes de codec de ICO nativos.</span><span class="sxs-lookup"><span data-stu-id="e0d01-116">The following table lists the GUIDs used to identify the native ICO codec components.</span></span>



| <span data-ttu-id="e0d01-117">Componente</span><span class="sxs-lookup"><span data-stu-id="e0d01-117">Component</span></span>        | <span data-ttu-id="e0d01-118">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="e0d01-118">Friendly Name</span></span>            | <span data-ttu-id="e0d01-119">GUID</span><span class="sxs-lookup"><span data-stu-id="e0d01-119">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="e0d01-120">Formato do contêiner</span><span class="sxs-lookup"><span data-stu-id="e0d01-120">Container Format</span></span> | <span data-ttu-id="e0d01-121">Contêiner \_ GUIDFormatIco</span><span class="sxs-lookup"><span data-stu-id="e0d01-121">GUID\_ContainerFormatIco</span></span> | <span data-ttu-id="e0d01-122">a3a860c4-338f-4c17-919afba4b5628f21</span><span class="sxs-lookup"><span data-stu-id="e0d01-122">a3a860c4-338f-4c17-919afba4b5628f21</span></span> |
| <span data-ttu-id="e0d01-123">Decodificador</span><span class="sxs-lookup"><span data-stu-id="e0d01-123">Decoder</span></span>          | <span data-ttu-id="e0d01-124">CLSID \_ WICIcoDecoder</span><span class="sxs-lookup"><span data-stu-id="e0d01-124">CLSID\_WICIcoDecoder</span></span>     | <span data-ttu-id="e0d01-125">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span><span class="sxs-lookup"><span data-stu-id="e0d01-125">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span></span> |
| <span data-ttu-id="e0d01-126">Codificador</span><span class="sxs-lookup"><span data-stu-id="e0d01-126">Encoder</span></span>          | <span data-ttu-id="e0d01-127">NÃO DISPONÍVEL</span><span class="sxs-lookup"><span data-stu-id="e0d01-127">NOT AVAILABLE</span></span>            | <span data-ttu-id="e0d01-128">NÃO DISPONÍVEL</span><span class="sxs-lookup"><span data-stu-id="e0d01-128">NOT AVAILABLE</span></span>                       |



 

## <a name="encoding"></a><span data-ttu-id="e0d01-129">Codificação</span><span class="sxs-lookup"><span data-stu-id="e0d01-129">Encoding</span></span>

<span data-ttu-id="e0d01-130">O WIC não fornece um codificador de imagem de ICO nativo.</span><span class="sxs-lookup"><span data-stu-id="e0d01-130">WIC does not provide a native ICO image encoder.</span></span>

## <a name="decoding"></a><span data-ttu-id="e0d01-131">Decodificação</span><span class="sxs-lookup"><span data-stu-id="e0d01-131">Decoding</span></span>

<span data-ttu-id="e0d01-132">A API de decodificação do WIC foi projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="e0d01-132">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="e0d01-133">Para obter mais informações sobre decodificação de imagem, consulte Visão [geral de decodificação.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="e0d01-133">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="e0d01-134">Para obter mais informações sobre como usar dados de imagem decodificados, consulte Visão geral das [fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="e0d01-134">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 



