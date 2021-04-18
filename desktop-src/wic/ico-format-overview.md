---
description: Este tópico fornece informações sobre o codec do Native ICO disponível por meio do Windows Imaging Component (WIC).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Visão geral do formato ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d370497e9231d6deb8d1793a26a53565b5cd99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763068"
---
# <a name="ico-format-overview"></a><span data-ttu-id="36884-103">Visão geral do formato ICO</span><span class="sxs-lookup"><span data-stu-id="36884-103">ICO Format Overview</span></span>

<span data-ttu-id="36884-104">Este tópico fornece informações sobre o codec do Native ICO disponível por meio do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="36884-104">This topic provides information about the native ICO codec available through Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="36884-105">Identidade do codec</span><span class="sxs-lookup"><span data-stu-id="36884-105">Codec Identity</span></span>

<span data-ttu-id="36884-106">A tabela a seguir fornece informações de identificação do codec.</span><span class="sxs-lookup"><span data-stu-id="36884-106">The following table provides codec identification information.</span></span>



|                        |                   |
|------------------------|-------------------|
| <span data-ttu-id="36884-107">Nome (s) formal (es)</span><span class="sxs-lookup"><span data-stu-id="36884-107">Formal Name(s)</span></span>         | <span data-ttu-id="36884-108">Formato de ícone (ICO)</span><span class="sxs-lookup"><span data-stu-id="36884-108">Icon Format (ICO)</span></span> |
| <span data-ttu-id="36884-109">Extensão (s) de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="36884-109">File Name Extension(s)</span></span> | <span data-ttu-id="36884-110">ico</span><span class="sxs-lookup"><span data-stu-id="36884-110">ico</span></span>               |
| <span data-ttu-id="36884-111">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="36884-111">MIME type</span></span>              | <span data-ttu-id="36884-112">imagem/ico</span><span class="sxs-lookup"><span data-stu-id="36884-112">image/ico</span></span>         |
| <span data-ttu-id="36884-113">Suporte à especificação</span><span class="sxs-lookup"><span data-stu-id="36884-113">Specification Support</span></span>  |                   |



 

<span data-ttu-id="36884-114">A tabela a seguir lista os GUIDs usados para identificar os componentes do codec do Native ICO.</span><span class="sxs-lookup"><span data-stu-id="36884-114">The following table lists the GUIDs used to identify the native ICO codec components.</span></span>



| <span data-ttu-id="36884-115">Componente</span><span class="sxs-lookup"><span data-stu-id="36884-115">Component</span></span>        | <span data-ttu-id="36884-116">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="36884-116">Friendly Name</span></span>            | <span data-ttu-id="36884-117">GUID</span><span class="sxs-lookup"><span data-stu-id="36884-117">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="36884-118">Formato do contêiner</span><span class="sxs-lookup"><span data-stu-id="36884-118">Container Format</span></span> | <span data-ttu-id="36884-119">\_CONTAINERFORMATICO GUID</span><span class="sxs-lookup"><span data-stu-id="36884-119">GUID\_ContainerFormatIco</span></span> | <span data-ttu-id="36884-120">a3a860c4-338f-4c17-919afba4b5628f21</span><span class="sxs-lookup"><span data-stu-id="36884-120">a3a860c4-338f-4c17-919afba4b5628f21</span></span> |
| <span data-ttu-id="36884-121">Decodificador</span><span class="sxs-lookup"><span data-stu-id="36884-121">Decoder</span></span>          | <span data-ttu-id="36884-122">\_WICICODECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="36884-122">CLSID\_WICIcoDecoder</span></span>     | <span data-ttu-id="36884-123">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span><span class="sxs-lookup"><span data-stu-id="36884-123">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span></span> |
| <span data-ttu-id="36884-124">Codificador</span><span class="sxs-lookup"><span data-stu-id="36884-124">Encoder</span></span>          | <span data-ttu-id="36884-125">NÃO DISPONÍVEL</span><span class="sxs-lookup"><span data-stu-id="36884-125">NOT AVAILABLE</span></span>            | <span data-ttu-id="36884-126">NÃO DISPONÍVEL</span><span class="sxs-lookup"><span data-stu-id="36884-126">NOT AVAILABLE</span></span>                       |



 

## <a name="encoding"></a><span data-ttu-id="36884-127">Codificação</span><span class="sxs-lookup"><span data-stu-id="36884-127">Encoding</span></span>

<span data-ttu-id="36884-128">O WIC não fornece um codificador de imagem ICO nativo.</span><span class="sxs-lookup"><span data-stu-id="36884-128">WIC does not provide a native ICO image encoder.</span></span>

## <a name="decoding"></a><span data-ttu-id="36884-129">Decodificação</span><span class="sxs-lookup"><span data-stu-id="36884-129">Decoding</span></span>

<span data-ttu-id="36884-130">A API de decodificação de WIC é projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma.</span><span class="sxs-lookup"><span data-stu-id="36884-130">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="36884-131">Para obter mais informações sobre a decodificação de imagem, consulte a [visão geral da decodificação](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="36884-131">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="36884-132">Para obter mais informações sobre como usar dados de imagem decodificados, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="36884-132">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 



