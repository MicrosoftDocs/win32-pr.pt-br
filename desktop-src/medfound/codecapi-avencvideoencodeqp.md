---
description: Especifica o parâmetro de quantificação (QP) para codificação de vídeo.
ms.assetid: 9E3B5E2D-3583-4C89-BC2A-4AC3C5545673
title: Propriedade CODECAPI_AVEncVideoEncodeQP (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec6c746f2f3c902ca416097571abaf5953956cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814126"
---
# <a name="codecapi_avencvideoencodeqp-property"></a><span data-ttu-id="cacb5-103">\_Propriedade CODECAPI AVEncVideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="cacb5-103">CODECAPI\_AVEncVideoEncodeQP property</span></span>

<span data-ttu-id="cacb5-104">Especifica o parâmetro de quantificação (QP) para codificação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cacb5-104">Specifies the quantization parameter (QP) for video encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="cacb5-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="cacb5-105">Data type</span></span>

<span data-ttu-id="cacb5-106">**ULONGLONG** (VT \_ UI8)</span><span class="sxs-lookup"><span data-stu-id="cacb5-106">**ULONGLONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="cacb5-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="cacb5-107">Property GUID</span></span>

<span data-ttu-id="cacb5-108">**CODECAPI \_ AVEncVideoEncodeQP**</span><span class="sxs-lookup"><span data-stu-id="cacb5-108">**CODECAPI\_AVEncVideoEncodeQP**</span></span>

## <a name="property-value"></a><span data-ttu-id="cacb5-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="cacb5-109">Property value</span></span>

<span data-ttu-id="cacb5-110">Um conjunto de campos de 4 16 bits usado para especificar o quadro QPs na codificação de QP fixa.</span><span class="sxs-lookup"><span data-stu-id="cacb5-110">A set of four 16-bit fields used to specify the frame QPs in fixed-QP encoding.</span></span>

<span data-ttu-id="cacb5-111">Os campos são:</span><span class="sxs-lookup"><span data-stu-id="cacb5-111">The fields are:</span></span>

-   <span data-ttu-id="cacb5-112">Bits 0-15: QP padrão</span><span class="sxs-lookup"><span data-stu-id="cacb5-112">Bits 0-15: Default QP</span></span>
-   <span data-ttu-id="cacb5-113">Bits 16-31: QP usado para quadros I</span><span class="sxs-lookup"><span data-stu-id="cacb5-113">Bits 16-31: QP used for I frames</span></span>
-   <span data-ttu-id="cacb5-114">Bits 32-47: QP usado para quadros P</span><span class="sxs-lookup"><span data-stu-id="cacb5-114">Bits 32-47: QP used for P frames</span></span>
-   <span data-ttu-id="cacb5-115">Bits 48-63: QP usado para quadros B</span><span class="sxs-lookup"><span data-stu-id="cacb5-115">Bits 48-63: QP used for B frames</span></span>

## <a name="remarks"></a><span data-ttu-id="cacb5-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="cacb5-116">Remarks</span></span>

<span data-ttu-id="cacb5-117">Essa propriedade também é usada com [codificadores de câmera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="cacb5-117">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="cacb5-118">Para garantir o uso consistente em codificadores diferentes, você deve assumir que os codificadores só verão a QP padrão e podem ignorar valores de QP para imagens I/P/B.</span><span class="sxs-lookup"><span data-stu-id="cacb5-118">To insure consistent usage across different encoders, you should assume encoders will only look at the default QP and can ignore QP values for I/P/B pictures.</span></span>

## <a name="requirements"></a><span data-ttu-id="cacb5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cacb5-119">Requirements</span></span>



| <span data-ttu-id="cacb5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cacb5-120">Requirement</span></span> | <span data-ttu-id="cacb5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="cacb5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cacb5-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cacb5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cacb5-123">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cacb5-123">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="cacb5-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cacb5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cacb5-125">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cacb5-125">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="cacb5-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cacb5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cacb5-127"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cacb5-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cacb5-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="cacb5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cacb5-129">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cacb5-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="cacb5-130">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="cacb5-130">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

