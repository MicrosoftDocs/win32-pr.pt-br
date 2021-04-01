---
description: Especifica os tipos de quadro (I, P ou B) aos quais o parâmetro de quantificação (QP) é aplicado.
ms.assetid: 6331033F-7EEB-41B3-B166-29686D4AADB6
title: Propriedade CODECAPI_AVEncVideoEncodeFrameTypeQP (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76e68e0cb6cbdc076dbf523f3ae9dfd7b5870f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089784"
---
# <a name="codecapi_avencvideoencodeframetypeqp-property"></a><span data-ttu-id="d9998-103">\_Propriedade CODECAPI AVEncVideoEncodeFrameTypeQP</span><span class="sxs-lookup"><span data-stu-id="d9998-103">CODECAPI\_AVEncVideoEncodeFrameTypeQP property</span></span>

<span data-ttu-id="d9998-104">Especifica os tipos de quadro (I, P ou B) aos quais o parâmetro de quantificação (QP) é aplicado.</span><span class="sxs-lookup"><span data-stu-id="d9998-104">Specifies the frame types (I, P, or B) that the quantization parameter (QP) is applied to.</span></span>

## <a name="data-type"></a><span data-ttu-id="d9998-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d9998-105">Data type</span></span>

<span data-ttu-id="d9998-106">**ULONGULONG** (VT \_ UI8)</span><span class="sxs-lookup"><span data-stu-id="d9998-106">**ULONGULONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d9998-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="d9998-107">Property GUID</span></span>

<span data-ttu-id="d9998-108">**CODECAPI \_ AVEncVideoEncodeFrameTypeQP**</span><span class="sxs-lookup"><span data-stu-id="d9998-108">**CODECAPI\_AVEncVideoEncodeFrameTypeQP**</span></span>

## <a name="remarks"></a><span data-ttu-id="d9998-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9998-109">Remarks</span></span>

<span data-ttu-id="d9998-110">Para codificadores que dão suporte à definição de um parâmetro de quantificação (QP) para tipos de quadro diferentes (I, P, B), eles devem expor essa API além de [CODECAPI \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md).</span><span class="sxs-lookup"><span data-stu-id="d9998-110">For encoders which support setting a quantization parameter (QP) for different frame types (I, P, B), they shall expose this API in addition to [CODECAPI\_AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md).</span></span> <span data-ttu-id="d9998-111">Se um codificador oferecer suporte a apenas uma única QP para todos os tipos de quadro, ele deverá dar suporte apenas a CODECAPI \_ AVEncVideoEncodeQP.</span><span class="sxs-lookup"><span data-stu-id="d9998-111">If an encoder supports only a single QP for all frame types, they shall support only CODECAPI\_AVEncVideoEncodeQP.</span></span>

<span data-ttu-id="d9998-112">Essa é uma propriedade de codificação dinâmica que significa que um novo valor pode ser definido a qualquer momento durante a sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="d9998-112">This is a dynamic encoding property meaning that a new value can be set any time during the encoding session.</span></span>

<span data-ttu-id="d9998-113">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="d9998-113">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="d9998-114">O codificador deve dar suporte a [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**DefinirValor**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="d9998-114">Encoder shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="d9998-115">Um conjunto de campos de 4 16 bits é usado para especificar o quadro QPs na codificação de QP fixa.</span><span class="sxs-lookup"><span data-stu-id="d9998-115">A set of four 16-bit fields are used to specify the frame QPs in fixed-QP encoding.</span></span> <span data-ttu-id="d9998-116">Os campos são:</span><span class="sxs-lookup"><span data-stu-id="d9998-116">The fields are:</span></span>

-   <span data-ttu-id="d9998-117">**Bits 0-15:** QP usado para quadros I, intervalo válido \[ 0, 51 \] .</span><span class="sxs-lookup"><span data-stu-id="d9998-117">**Bits 0-15:** QP used for I frames, valid range \[0, 51\].</span></span>
-   <span data-ttu-id="d9998-118">**Bits 16-31:** QP usado para quadros P, intervalo válido \[ 0, 51 \] .</span><span class="sxs-lookup"><span data-stu-id="d9998-118">**Bits 16-31:** QP used for P frames, valid range \[0, 51\].</span></span>
-   <span data-ttu-id="d9998-119">**Bits 32-47:** QP usado para quadros B, intervalo válido \[ 0, 51\]</span><span class="sxs-lookup"><span data-stu-id="d9998-119">**Bits 32-47:** QP used for B frames, valid range \[0, 51\]</span></span>
-   <span data-ttu-id="d9998-120">**Bits 48-63:** reservado</span><span class="sxs-lookup"><span data-stu-id="d9998-120">**Bits 48-63:** reserved</span></span>

<span data-ttu-id="d9998-121">Quando esse CodecAPI tem suporte, os codificadores devem dar suporte à configuração de QP no tipo de quadro de I, P e B.</span><span class="sxs-lookup"><span data-stu-id="d9998-121">When this CodecAPI is supported, encoders shall support QP setting on frame type of I, P, and B.</span></span>

<span data-ttu-id="d9998-122">O valor padrão deve ser 0x0000001a001a001a.</span><span class="sxs-lookup"><span data-stu-id="d9998-122">Default value shall be 0x0000001a001a001a.</span></span> <span data-ttu-id="d9998-123">QP igual a 26 para I, P e B.</span><span class="sxs-lookup"><span data-stu-id="d9998-123">QP equal to 26 for I, P and B.</span></span>

<span data-ttu-id="d9998-124">Quando [CODECAPI \_ AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) seleciona uma camada temporal específica, [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) of CODECAPI \_ AVEncVideoEncodeFrameTypeQP deve definir QP para os quadros I, P e B nessa camada temporal.</span><span class="sxs-lookup"><span data-stu-id="d9998-124">When [CODECAPI\_AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) selects a specific temporal layer, [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) of CODECAPI\_AVEncVideoEncodeFrameTypeQP shall set QP for I, P, and B frames on that temporal layer.</span></span> <span data-ttu-id="d9998-125">Por padrão, ele define QP para quadros I, P e B na camada temporal de camada temporal base 0.</span><span class="sxs-lookup"><span data-stu-id="d9998-125">By default, it sets QP for I, P, and B frames on base temporal layer temporal layer 0.</span></span>

<span data-ttu-id="d9998-126">[CODECAPI \_ AVEncVideoMaxQP](codecapi-avencvideomaxqp.md) e [CODECAPI \_ AVEncVideoMinQP](codecapi-avencvideominqp.md) devem ser usados para definir e limitar o intervalo de QP para qps de todos os tipos de imagem, I, P e B.</span><span class="sxs-lookup"><span data-stu-id="d9998-126">[CODECAPI\_AVEncVideoMaxQP](codecapi-avencvideomaxqp.md) and [CODECAPI\_AVEncVideoMinQP](codecapi-avencvideominqp.md) shall be used to define and limit the QP range for QPs of all picture types, I, P and B.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9998-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9998-127">Requirements</span></span>



| <span data-ttu-id="d9998-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9998-128">Requirement</span></span> | <span data-ttu-id="d9998-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d9998-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9998-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9998-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d9998-131">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d9998-131">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="d9998-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9998-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d9998-133">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="d9998-133">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d9998-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d9998-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9998-135"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9998-135"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9998-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9998-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9998-137">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d9998-137">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

