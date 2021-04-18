---
description: Define o uso de vídeo para um codificador de vídeo.
ms.assetid: 2A6941A3-CCA0-467C-AC8A-DADC2CD1D405
title: Propriedade CODECAPI_AVEncVideoUsage (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27568412613702846e99d0ca556cc59cdc4fc77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749548"
---
# <a name="codecapi_avencvideousage-property"></a><span data-ttu-id="4da6c-103">\_Propriedade CODECAPI AVEncVideoUsage</span><span class="sxs-lookup"><span data-stu-id="4da6c-103">CODECAPI\_AVEncVideoUsage property</span></span>

<span data-ttu-id="4da6c-104">Define o uso de vídeo para um codificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4da6c-104">Sets the video usage for a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="4da6c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4da6c-105">Data type</span></span>

<span data-ttu-id="4da6c-106">**ULONG (VT \_ UI4)**</span><span class="sxs-lookup"><span data-stu-id="4da6c-106">**ULONG (VT\_UI4)**</span></span>

## <a name="property-guid"></a><span data-ttu-id="4da6c-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="4da6c-107">Property GUID</span></span>

<span data-ttu-id="4da6c-108">**CODECAPI \_ AVEncVideoUsage**</span><span class="sxs-lookup"><span data-stu-id="4da6c-108">**CODECAPI\_AVEncVideoUsage**</span></span>

## <a name="remarks"></a><span data-ttu-id="4da6c-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="4da6c-109">Remarks</span></span>

<span data-ttu-id="4da6c-110">Essa propriedade também é usada com [codificadores de câmera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="4da6c-110">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="4da6c-111">[CODECAPI \_ AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md), CODECAPI \_ AVEncVideoUsage e [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) são propriedades de codificador estáticos.</span><span class="sxs-lookup"><span data-stu-id="4da6c-111">[CODECAPI\_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md), CODECAPI\_AVEncVideoUsage, and [CODECAPI\_AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) are static encoder properties.</span></span> <span data-ttu-id="4da6c-112">Uma vez definido, eles só terão efeito depois que um tipo de mídia definido for chamado no pino de saída da câmera.</span><span class="sxs-lookup"><span data-stu-id="4da6c-112">Once set, these will only take effect after a set media type is called on the camera s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="4da6c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4da6c-113">Requirements</span></span>



| <span data-ttu-id="4da6c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4da6c-114">Requirement</span></span> | <span data-ttu-id="4da6c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4da6c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4da6c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4da6c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4da6c-117">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4da6c-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="4da6c-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4da6c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4da6c-119">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4da6c-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="4da6c-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4da6c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4da6c-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4da6c-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4da6c-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="4da6c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4da6c-123">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4da6c-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

