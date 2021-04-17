---
description: Habilita ou desabilita a aceleração de hardware para decodificação de vídeo VC-1.
ms.assetid: eee85330-098e-4f21-81b7-a493abbd599b
title: Propriedade AVDecVideoAcceleration_VC1 (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fcdbe265f5a65212a2846b724f570b024ea0ab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105755400"
---
# <a name="avdecvideoacceleration_vc1-property"></a><span data-ttu-id="e84da-103">\_Propriedade AVDecVideoAcceleration VC1</span><span class="sxs-lookup"><span data-stu-id="e84da-103">AVDecVideoAcceleration\_VC1 property</span></span>

<span data-ttu-id="e84da-104">Habilita ou desabilita a aceleração de hardware para decodificação de vídeo VC-1.</span><span class="sxs-lookup"><span data-stu-id="e84da-104">Enables or disables hardware acceleration for VC-1 video decoding.</span></span>

<span data-ttu-id="e84da-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e84da-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="e84da-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e84da-106">Data type</span></span>

<span data-ttu-id="e84da-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="e84da-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="e84da-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="e84da-108">Property GUID</span></span>

<span data-ttu-id="e84da-109">**CODECAPI \_ AVDecVideoAcceleration \_ VC1**</span><span class="sxs-lookup"><span data-stu-id="e84da-109">**CODECAPI\_AVDecVideoAcceleration\_VC1**</span></span>

## <a name="remarks"></a><span data-ttu-id="e84da-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e84da-110">Remarks</span></span>

<span data-ttu-id="e84da-111">Se o valor for zero, o decodificador não usará a DXVA (aceleração de vídeo do DirectX) para decodificação de vídeo VC-1.</span><span class="sxs-lookup"><span data-stu-id="e84da-111">If the value is zero, the decoder does not use DirectX Video Acceleration (DXVA) for VC-1 video decoding.</span></span> <span data-ttu-id="e84da-112">Para filtros do DirectShow, defina essa propriedade antes que o pino de saída do decodificador seja conectado.</span><span class="sxs-lookup"><span data-stu-id="e84da-112">For DirectShow filters, set this property before the decoder's output pin is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="e84da-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e84da-113">Requirements</span></span>



| <span data-ttu-id="e84da-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e84da-114">Requirement</span></span> | <span data-ttu-id="e84da-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e84da-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e84da-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e84da-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e84da-117">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e84da-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="e84da-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e84da-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e84da-119">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e84da-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e84da-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e84da-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e84da-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e84da-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e84da-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="e84da-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e84da-123">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="e84da-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="e84da-124">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="e84da-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




