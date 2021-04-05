---
description: Define a contagem de camadas temporais de vídeo para um codificador de vídeo.
ms.assetid: 36E1C86B-86D0-40CB-8F96-061FC653E9C3
title: Propriedade CODECAPI_AVEncVideoTemporalLayerCount (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85402b57c0eaf5c5fe61290eabdfd3e34a64ca4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457223"
---
# <a name="codecapi_avencvideotemporallayercount-property"></a><span data-ttu-id="c8065-103">\_Propriedade CODECAPI AVEncVideoTemporalLayerCount</span><span class="sxs-lookup"><span data-stu-id="c8065-103">CODECAPI\_AVEncVideoTemporalLayerCount property</span></span>

<span data-ttu-id="c8065-104">Define a contagem de camadas temporais de vídeo para um codificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c8065-104">Sets the video temporal layer count for a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="c8065-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c8065-105">Data type</span></span>

<span data-ttu-id="c8065-106">**ULONG (VT \_ UI4)**</span><span class="sxs-lookup"><span data-stu-id="c8065-106">**ULONG (VT\_UI4)**</span></span>

## <a name="property-guid"></a><span data-ttu-id="c8065-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="c8065-107">Property GUID</span></span>

<span data-ttu-id="c8065-108">**CODECAPI \_ AVEncVideoTemporalLayerCount**</span><span class="sxs-lookup"><span data-stu-id="c8065-108">**CODECAPI\_AVEncVideoTemporalLayerCount**</span></span>

## <a name="remarks"></a><span data-ttu-id="c8065-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8065-109">Remarks</span></span>

<span data-ttu-id="c8065-110">Essa propriedade também é usada com [codificadores de câmera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="c8065-110">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="c8065-111">CODECAPI \_ AVEncVideoTemporalLayerCount, [CODECAPI \_ AVEncVideoUsage](codecapi-avencvideousage.md)e [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) são propriedades de codificador estáticos.</span><span class="sxs-lookup"><span data-stu-id="c8065-111">CODECAPI\_AVEncVideoTemporalLayerCount, [CODECAPI\_AVEncVideoUsage](codecapi-avencvideousage.md), and [CODECAPI\_AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) are static encoder properties.</span></span> <span data-ttu-id="c8065-112">Uma vez definido, eles só terão efeito depois que um tipo de mídia definido for chamado no pino de saída da câmera.</span><span class="sxs-lookup"><span data-stu-id="c8065-112">Once set, these will only take effect after a set media type is called on the camera s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8065-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8065-113">Requirements</span></span>



| <span data-ttu-id="c8065-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8065-114">Requirement</span></span> | <span data-ttu-id="c8065-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c8065-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8065-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8065-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c8065-117">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c8065-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="c8065-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8065-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c8065-119">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c8065-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c8065-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c8065-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8065-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8065-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8065-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8065-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8065-123">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c8065-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

