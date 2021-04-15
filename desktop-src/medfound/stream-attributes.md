---
description: Atributos de fluxo
ms.assetid: 83b64ad8-2552-41d1-bc61-20361831020b
title: Atributos de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a25de9ae6cf769268b3868d36bac2e293cfd8d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502246"
---
# <a name="stream-attributes"></a><span data-ttu-id="a3b32-103">Atributos de fluxo</span><span class="sxs-lookup"><span data-stu-id="a3b32-103">Stream Attributes</span></span>

<span data-ttu-id="a3b32-104">Os atributos a seguir se aplicam a fluxos de mídia.</span><span class="sxs-lookup"><span data-stu-id="a3b32-104">The following attributes apply to media streams.</span></span> <span data-ttu-id="a3b32-105">Para obter os atributos de um exemplo de mídia, use o método [**IMFMediaSourceEx:: Getstreamattributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) .</span><span class="sxs-lookup"><span data-stu-id="a3b32-105">To get the attributes from a media sample, use the [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) method.</span></span>



| <span data-ttu-id="a3b32-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="a3b32-106">Attribute</span></span>                                                                                   | <span data-ttu-id="a3b32-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3b32-107">Description</span></span>                                   |
|---------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="a3b32-108">MFStreamExtension \_ CameraExtrinsics</span><span class="sxs-lookup"><span data-stu-id="a3b32-108">MFStreamExtension\_CameraExtrinsics</span></span>](mfstreamextension-cameraextrinsics.md)               | <span data-ttu-id="a3b32-109">A câmera é extrínsecos para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="a3b32-109">The camera extrinsics for the stream.</span></span>         |
| [<span data-ttu-id="a3b32-110">MFStreamExtension \_ PinholeCameraIntrinsics</span><span class="sxs-lookup"><span data-stu-id="a3b32-110">MFStreamExtension\_PinholeCameraIntrinsics</span></span>](mfstreamextension-pinholecameraintrinsics.md) | <span data-ttu-id="a3b32-111">A câmera pinhole é intrínseca para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="a3b32-111">The pinhole camera intrinsics for the stream.</span></span> |



 

<span data-ttu-id="a3b32-112">Nem todo fluxo de mídia contém todos os atributos listados aqui.</span><span class="sxs-lookup"><span data-stu-id="a3b32-112">Not every media stream contains every attribute listed here.</span></span> <span data-ttu-id="a3b32-113">Em alguns casos, um atributo se aplica somente a determinados tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="a3b32-113">In some cases, an attribute applies only to certain kinds of data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3b32-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3b32-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3b32-115">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="a3b32-115">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="a3b32-116">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a3b32-116">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a3b32-117">Amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="a3b32-117">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 



