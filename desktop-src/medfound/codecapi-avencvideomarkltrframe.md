---
description: Marca o quadro atual como um quadro EPD.
ms.assetid: D70A54D6-DA9B-40E5-B130-0AA9C5363DF0
title: Propriedade CODECAPI_AVEncVideoMarkLTRFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a377f30aec049bc5cbc850ea03ace9dcc640bd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501194"
---
# <a name="codecapi_avencvideomarkltrframe-property"></a><span data-ttu-id="69ab3-103">\_Propriedade CODECAPI AVEncVideoMarkLTRFrame</span><span class="sxs-lookup"><span data-stu-id="69ab3-103">CODECAPI\_AVEncVideoMarkLTRFrame property</span></span>

<span data-ttu-id="69ab3-104">Marca o quadro atual como um quadro EPD.</span><span class="sxs-lookup"><span data-stu-id="69ab3-104">Marks the current frame as a LTR frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="69ab3-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="69ab3-105">Data type</span></span>

<span data-ttu-id="69ab3-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="69ab3-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="69ab3-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="69ab3-107">Property GUID</span></span>

<span data-ttu-id="69ab3-108">**CODECAPI \_ AVEncVideoMarkLTRFrame**</span><span class="sxs-lookup"><span data-stu-id="69ab3-108">**CODECAPI\_AVEncVideoMarkLTRFrame**</span></span>

## <a name="remarks"></a><span data-ttu-id="69ab3-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="69ab3-109">Remarks</span></span>

<span data-ttu-id="69ab3-110">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="69ab3-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="69ab3-111">O valor desse controle é o valor da sintaxe H. 264 *LongTermFramIdx* associada ao quadro atual.</span><span class="sxs-lookup"><span data-stu-id="69ab3-111">The value of this control is the value of H.264 syntax *LongTermFramIdx* associated with the current frame.</span></span> <span data-ttu-id="69ab3-112">Se o quadro atual não estiver na camada base, por exemplo, a *\_ ID temporal* do elemento de sintaxe não for igual a 0, essa propriedade se aplicará ao próximo quadro de camada base na ordem de codificação.</span><span class="sxs-lookup"><span data-stu-id="69ab3-112">If the current frame is not in the base layer, for example syntax element *temporal\_id* is not equal to 0, this property applies to the next base layer frame in encoding order.</span></span>

<span data-ttu-id="69ab3-113">Essa propriedade não deverá ser chamada se uma chamada pendente para marcar um quadro EPD tiver sido emitida usando a \_ Propriedade CODECAPI AVEncVideoMarkLTRFrame e o codificador ainda não tiver marcado um quadro como LTR.</span><span class="sxs-lookup"><span data-stu-id="69ab3-113">This property should not be called if a pending call to mark an LTR frame has been issued using the CODECAPI\_AVEncVideoMarkLTRFrame property and the encoder has not yet marked a frame as LTR.</span></span> <span data-ttu-id="69ab3-114">Em outras palavras, o codificador não deve enfileirar \_ as solicitações CODECAPI AVEncVideoMarkLTRFrame.</span><span class="sxs-lookup"><span data-stu-id="69ab3-114">In other words, the encoder should not queue up CODECAPI\_AVEncVideoMarkLTRFrame requests.</span></span> <span data-ttu-id="69ab3-115">Se uma \_ solicitação CODECAPI AVEncVideoMarkLTRFrame for enviada enquanto outra \_ solicitação AVEncVideoMarkLTRFrame CODECAPI ainda estiver pendente, a solicitação mais antiga deverá ser descartada.</span><span class="sxs-lookup"><span data-stu-id="69ab3-115">If a CODECAPI\_AVEncVideoMarkLTRFrame request is submitted while another CODECAPI\_AVEncVideoMarkLTRFrame request is still pending, the older request should be dropped.</span></span>

<span data-ttu-id="69ab3-116">A \_ Propriedade CODECAPI AVEncVideoMarkLTRFrame é dinâmica e pode ser definida durante a sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="69ab3-116">The CODECAPI\_AVEncVideoMarkLTRFrame property is dynamic and can be set during the encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="69ab3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69ab3-117">Requirements</span></span>



| <span data-ttu-id="69ab3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="69ab3-118">Requirement</span></span> | <span data-ttu-id="69ab3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="69ab3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69ab3-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69ab3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="69ab3-121">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="69ab3-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="69ab3-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69ab3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="69ab3-123">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="69ab3-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="69ab3-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69ab3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="69ab3-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="69ab3-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69ab3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="69ab3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69ab3-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="69ab3-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




