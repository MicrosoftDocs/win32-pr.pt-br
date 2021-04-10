---
description: Interfaces do codificador
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: Interfaces do codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5367a25f1a2a4caf486711f7569312a436f8f474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170306"
---
# <a name="encoder-interfaces"></a><span data-ttu-id="9b0f1-103">Interfaces do codificador</span><span class="sxs-lookup"><span data-stu-id="9b0f1-103">Encoder Interfaces</span></span>


<span data-ttu-id="9b0f1-104">As tabelas a seguir mostram as interfaces implementadas pelos codificadores do Windows Imaging Component (WIC) e o diagrama de classe mostra a hierarquia de herança.</span><span class="sxs-lookup"><span data-stu-id="9b0f1-104">The following tables show the interfaces implemented by Windows Imaging Component (WIC) encoders, and the class diagram shows the inheritance hierarchy.</span></span>

<span data-ttu-id="9b0f1-105">Interfaces do codificador Container-Level</span><span class="sxs-lookup"><span data-stu-id="9b0f1-105">Container-Level Encoder Interfaces</span></span>



| <span data-ttu-id="9b0f1-106">Interface</span><span class="sxs-lookup"><span data-stu-id="9b0f1-106">Interface</span></span>                                                                                       | <span data-ttu-id="9b0f1-107">Responsabilidades</span><span class="sxs-lookup"><span data-stu-id="9b0f1-107">Responsibilities</span></span>                             | <span data-ttu-id="9b0f1-108">Implementação</span><span class="sxs-lookup"><span data-stu-id="9b0f1-108">Implementation</span></span>                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="9b0f1-109">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="9b0f1-109">IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)                                             | <span data-ttu-id="9b0f1-110">Serviços de nível de contêiner</span><span class="sxs-lookup"><span data-stu-id="9b0f1-110">Container-level services</span></span>                     | <span data-ttu-id="9b0f1-111">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9b0f1-111">Required</span></span>                                                                   |
| [<span data-ttu-id="9b0f1-112">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="9b0f1-112">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md) | <span data-ttu-id="9b0f1-113">Notificação de progresso & suporte ao cancelamento</span><span class="sxs-lookup"><span data-stu-id="9b0f1-113">Progress notification & cancellation support</span></span> | <span data-ttu-id="9b0f1-114">Recomendadas</span><span class="sxs-lookup"><span data-stu-id="9b0f1-114">Recommended</span></span>                                                                |
| [<span data-ttu-id="9b0f1-115">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="9b0f1-115">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)                                 | <span data-ttu-id="9b0f1-116">Serviços de serialização de metadados</span><span class="sxs-lookup"><span data-stu-id="9b0f1-116">Metadata serialization services</span></span>              | <span data-ttu-id="9b0f1-117">Opcional (necessário apenas para formatos que dão suporte a metadados em nível de contêiner)</span><span class="sxs-lookup"><span data-stu-id="9b0f1-117">Optional (Required only for formats that support container-level metadata)</span></span> |



 

<span data-ttu-id="9b0f1-118">Interfaces do codificador Frame-Level</span><span class="sxs-lookup"><span data-stu-id="9b0f1-118">Frame-Level Encoder Interfaces</span></span>



| <span data-ttu-id="9b0f1-119">Interface</span><span class="sxs-lookup"><span data-stu-id="9b0f1-119">Interface</span></span>                                                       | <span data-ttu-id="9b0f1-120">Responsabilidades</span><span class="sxs-lookup"><span data-stu-id="9b0f1-120">Responsibilities</span></span>                | <span data-ttu-id="9b0f1-121">Implementação</span><span class="sxs-lookup"><span data-stu-id="9b0f1-121">Implementation</span></span> |
|-----------------------------------------------------------------|---------------------------------|----------------|
| [<span data-ttu-id="9b0f1-122">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="9b0f1-122">IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)     | <span data-ttu-id="9b0f1-123">Serviços de nível de quadro</span><span class="sxs-lookup"><span data-stu-id="9b0f1-123">Frame-level services</span></span>            | <span data-ttu-id="9b0f1-124">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9b0f1-124">Required</span></span>       |
| [<span data-ttu-id="9b0f1-125">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="9b0f1-125">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md) | <span data-ttu-id="9b0f1-126">Serviços de serialização de metadados</span><span class="sxs-lookup"><span data-stu-id="9b0f1-126">Metadata serialization services</span></span> | <span data-ttu-id="9b0f1-127">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9b0f1-127">Required</span></span>       |



 

![hierarquia de herança da interface do codificador WIC](graphics/wicencoderinterfaces.png)

<span data-ttu-id="9b0f1-129">Você observará que as interfaces do codificador são quase imagens espelhadas das interfaces do decodificador e que a maioria dos métodos nessas interfaces correspondem aos métodos nas interfaces do decodificador relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9b0f1-129">You'll notice that the encoder interfaces are almost mirror images of the decoder interfaces, and that most of the methods on these interfaces correspond to methods on the related decoder interfaces.</span></span> <span data-ttu-id="9b0f1-130">Agora que você está familiarizado com a implementação de um decodificador habilitado por WIC, a implementação de um codificador habilitado para WIC também parecerá familiar.</span><span class="sxs-lookup"><span data-stu-id="9b0f1-130">Now that you're familiar with the implementation of a WIC-enabled decoder, the implementation of a WIC-enabled encoder will seem familiar as well.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b0f1-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b0f1-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9b0f1-132">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="9b0f1-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9b0f1-133">Implementando um codificador de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="9b0f1-133">Implementing a WIC-Enabled Encoder</span></span>](-wic-implementingwicencoder.md)
</dt> <dt>

[<span data-ttu-id="9b0f1-134">Implementando IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="9b0f1-134">Implementing IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[<span data-ttu-id="9b0f1-135">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="9b0f1-135">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="9b0f1-136">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="9b0f1-136">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



