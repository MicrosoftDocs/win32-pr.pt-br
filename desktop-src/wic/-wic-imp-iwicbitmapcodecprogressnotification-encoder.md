---
description: Implementando IWICBitmapCodecProgressNotification (codificador)
ms.assetid: d470ec93-d329-48c0-9556-0c15daece491
title: Implementando IWICBitmapCodecProgressNotification (codificador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260fac41068de0695813d569881e4a71938eb83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829498"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-encoder"></a><span data-ttu-id="783dc-103">Implementando IWICBitmapCodecProgressNotification (codificador)</span><span class="sxs-lookup"><span data-stu-id="783dc-103">Implementing IWICBitmapCodecProgressNotification (Encoder)</span></span>

## <a name="iwicbitmapcodecprogressnotification"></a><span data-ttu-id="783dc-104">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="783dc-104">IWICBitmapCodecProgressNotification</span></span>

<span data-ttu-id="783dc-105">Embora a interface [**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification) seja opcional, é recomendável que ela seja implementada na classe de codificador de nível de contêiner.</span><span class="sxs-lookup"><span data-stu-id="783dc-105">Although the [**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification) interface is optional, it is recommended that it be implemented on the container-level encoder class.</span></span> <span data-ttu-id="783dc-106">Essa interface é discutida em mais detalhes na [implementação de IWICBitmapCodecProgressNotification (decodificador)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="783dc-106">This interface is discussed in more details in [Implementing IWICBitmapCodecProgressNotification (Decoder)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md).</span></span> <span data-ttu-id="783dc-107">A implementação é a mesma para o decodificador e o codificador.</span><span class="sxs-lookup"><span data-stu-id="783dc-107">The implementation is the same for either the decoder and the encoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="783dc-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="783dc-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="783dc-109">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="783dc-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="783dc-110">Implementando IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="783dc-110">Implementing IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[<span data-ttu-id="783dc-111">Implementando IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="783dc-111">Implementing IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[<span data-ttu-id="783dc-112">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="783dc-112">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="783dc-113">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="783dc-113">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="783dc-114">Implementando IWICBitmapCodecProgressNotification (decodificador)</span><span class="sxs-lookup"><span data-stu-id="783dc-114">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> </dl>

 

 



