---
description: Habilita ou desabilita a aceleração de hardware para decodificação de vídeo H. 264.
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: Propriedade AVDecVideoAcceleration_H264 (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbcedf2d038c010ee781030baf0a8289e68eab4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825962"
---
# <a name="avdecvideoacceleration_h264-property"></a><span data-ttu-id="2ca6f-103">\_Propriedade AVDecVideoAcceleration H264</span><span class="sxs-lookup"><span data-stu-id="2ca6f-103">AVDecVideoAcceleration\_H264 property</span></span>

<span data-ttu-id="2ca6f-104">Habilita ou desabilita a aceleração de hardware para decodificação de vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="2ca6f-104">Enables or disables hardware acceleration for H.264 video decoding.</span></span>

<span data-ttu-id="2ca6f-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2ca6f-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="2ca6f-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2ca6f-106">Data type</span></span>

<span data-ttu-id="2ca6f-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="2ca6f-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="2ca6f-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="2ca6f-108">Property GUID</span></span>

<span data-ttu-id="2ca6f-109">**CODECAPI \_ AVDecVideoAcceleration \_ H264**</span><span class="sxs-lookup"><span data-stu-id="2ca6f-109">**CODECAPI\_AVDecVideoAcceleration\_H264**</span></span>

## <a name="remarks"></a><span data-ttu-id="2ca6f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ca6f-110">Remarks</span></span>

<span data-ttu-id="2ca6f-111">Se o valor for zero, o decodificador não usará a DXVA (aceleração de vídeo do DirectX) para decodificação de vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="2ca6f-111">If the value is zero, the decoder does not use DirectX Video Acceleration (DXVA) for H.264 video decoding.</span></span> <span data-ttu-id="2ca6f-112">Para filtros do DirectShow, defina essa propriedade antes que o pino de saída do decodificador seja conectado.</span><span class="sxs-lookup"><span data-stu-id="2ca6f-112">For DirectShow filters, set this property before the decoder's output pin is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ca6f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ca6f-113">Requirements</span></span>



| <span data-ttu-id="2ca6f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ca6f-114">Requirement</span></span> | <span data-ttu-id="2ca6f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="2ca6f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca6f-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ca6f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2ca6f-117">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2ca6f-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="2ca6f-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ca6f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2ca6f-119">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2ca6f-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2ca6f-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ca6f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ca6f-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ca6f-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ca6f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ca6f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ca6f-123">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="2ca6f-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="2ca6f-124">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="2ca6f-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




