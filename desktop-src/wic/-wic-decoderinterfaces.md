---
description: Interfaces do decodificador
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: Interfaces do decodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef90ca2dd521c15460295505a6d5b7ea451c4dba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171525"
---
# <a name="decoder-interfaces"></a><span data-ttu-id="1b3bb-103">Interfaces do decodificador</span><span class="sxs-lookup"><span data-stu-id="1b3bb-103">Decoder Interfaces</span></span>

<span data-ttu-id="1b3bb-104">As tabelas a seguir mostram as interfaces implementadas pelos decodificadores do Windows Imaging Component (WIC) e o diagrama de classe mostra a hierarquia de herança.</span><span class="sxs-lookup"><span data-stu-id="1b3bb-104">The following tables show the interfaces implemented by Windows Imaging Component (WIC) decoders, and the class diagram shows the inheritance hierarchy.</span></span>

<span data-ttu-id="1b3bb-105">Interfaces de decodificador Container-Level</span><span class="sxs-lookup"><span data-stu-id="1b3bb-105">Container-Level Decoder Interfaces</span></span>



| <span data-ttu-id="1b3bb-106">Interface</span><span class="sxs-lookup"><span data-stu-id="1b3bb-106">Interface</span></span>                                                                                       | <span data-ttu-id="1b3bb-107">Responsabilidades</span><span class="sxs-lookup"><span data-stu-id="1b3bb-107">Responsibilities</span></span>                             | <span data-ttu-id="1b3bb-108">Implementação</span><span class="sxs-lookup"><span data-stu-id="1b3bb-108">Implementation</span></span>                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="1b3bb-109">IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="1b3bb-109">IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)                                             | <span data-ttu-id="1b3bb-110">Serviços de nível de contêiner</span><span class="sxs-lookup"><span data-stu-id="1b3bb-110">Container-level services</span></span>                     | <span data-ttu-id="1b3bb-111">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1b3bb-111">Required</span></span>                                                                   |
| [<span data-ttu-id="1b3bb-112">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="1b3bb-112">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | <span data-ttu-id="1b3bb-113">Notificação de progresso & suporte ao cancelamento</span><span class="sxs-lookup"><span data-stu-id="1b3bb-113">Progress notification & cancellation support</span></span> | <span data-ttu-id="1b3bb-114">Recomendadas</span><span class="sxs-lookup"><span data-stu-id="1b3bb-114">Recommended</span></span>                                                                |
| [<span data-ttu-id="1b3bb-115">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="1b3bb-115">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)                                 | <span data-ttu-id="1b3bb-116">Enumeração de metadados</span><span class="sxs-lookup"><span data-stu-id="1b3bb-116">Metadata enumeration</span></span>                         | <span data-ttu-id="1b3bb-117">Opcional (necessário apenas para formatos que dão suporte a metadados em nível de contêiner)</span><span class="sxs-lookup"><span data-stu-id="1b3bb-117">Optional (Required only for formats that support container-level metadata)</span></span> |



 

<span data-ttu-id="1b3bb-118">Interfaces de decodificador Frame-Level</span><span class="sxs-lookup"><span data-stu-id="1b3bb-118">Frame-Level Decoder Interfaces</span></span>



| <span data-ttu-id="1b3bb-119">Interface</span><span class="sxs-lookup"><span data-stu-id="1b3bb-119">Interface</span></span>                                                           | <span data-ttu-id="1b3bb-120">Responsabilidades</span><span class="sxs-lookup"><span data-stu-id="1b3bb-120">Responsibilities</span></span>          | <span data-ttu-id="1b3bb-121">Implementação</span><span class="sxs-lookup"><span data-stu-id="1b3bb-121">Implementation</span></span>                |
|---------------------------------------------------------------------|---------------------------|-------------------------------|
| [<span data-ttu-id="1b3bb-122">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="1b3bb-122">IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)         | <span data-ttu-id="1b3bb-123">Serviços de nível de quadro</span><span class="sxs-lookup"><span data-stu-id="1b3bb-123">Frame-level services</span></span>      | <span data-ttu-id="1b3bb-124">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1b3bb-124">Required</span></span>                      |
| [<span data-ttu-id="1b3bb-125">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="1b3bb-125">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)     | <span data-ttu-id="1b3bb-126">Enumeração de metadados</span><span class="sxs-lookup"><span data-stu-id="1b3bb-126">Metadata enumeration</span></span>      | <span data-ttu-id="1b3bb-127">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1b3bb-127">Required</span></span>                      |
| [<span data-ttu-id="1b3bb-128">IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="1b3bb-128">IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md) | <span data-ttu-id="1b3bb-129">Transformações de decodificador nativo</span><span class="sxs-lookup"><span data-stu-id="1b3bb-129">Native decoder transforms</span></span> | <span data-ttu-id="1b3bb-130">Recomendadas</span><span class="sxs-lookup"><span data-stu-id="1b3bb-130">Recommended</span></span>                   |
| [<span data-ttu-id="1b3bb-131">IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="1b3bb-131">IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)                       | <span data-ttu-id="1b3bb-132">Serviços de processamento bruto</span><span class="sxs-lookup"><span data-stu-id="1b3bb-132">Raw processing services</span></span>   | <span data-ttu-id="1b3bb-133">Necessário somente para formatos brutos</span><span class="sxs-lookup"><span data-stu-id="1b3bb-133">Required for Raw formats only</span></span> |



 

![hierarquia de herança da interface do WIC](graphics/wicinterfaces.png)

## <a name="related-topics"></a><span data-ttu-id="1b3bb-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b3bb-135">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1b3bb-136">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="1b3bb-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1b3bb-137">Implementando um decodificador de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="1b3bb-137">Implementing a WIC-Enabled Decoder</span></span>](-wic-implementingwicdecoder.md)
</dt> <dt>

[<span data-ttu-id="1b3bb-138">Implementando IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="1b3bb-138">Implementing IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[<span data-ttu-id="1b3bb-139">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="1b3bb-139">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="1b3bb-140">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="1b3bb-140">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



