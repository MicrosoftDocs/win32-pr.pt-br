---
description: Especifica que o quadro atual é codificado usando um ou vários quadros EPD.
ms.assetid: 51FD6E36-9CDF-4005-942F-7A92CA706F38
title: Propriedade CODECAPI_AVEncVideoUseLTRFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252933180e8212c94c3c2b2442397c53d0f9c559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646613"
---
# <a name="codecapi_avencvideouseltrframe-property"></a><span data-ttu-id="35d12-103">\_Propriedade CODECAPI AVEncVideoUseLTRFrame</span><span class="sxs-lookup"><span data-stu-id="35d12-103">CODECAPI\_AVEncVideoUseLTRFrame property</span></span>

<span data-ttu-id="35d12-104">Especifica que o quadro atual é codificado usando um ou vários quadros EPD.</span><span class="sxs-lookup"><span data-stu-id="35d12-104">Specifies that the current frame is encoded using one or multiple LTR frames.</span></span>

## <a name="data-type"></a><span data-ttu-id="35d12-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="35d12-105">Data type</span></span>

<span data-ttu-id="35d12-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="35d12-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="35d12-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="35d12-107">Property GUID</span></span>

<span data-ttu-id="35d12-108">**CODECAPI \_ AVEncVideoUseLTRFrame**</span><span class="sxs-lookup"><span data-stu-id="35d12-108">**CODECAPI\_AVEncVideoUseLTRFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="35d12-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="35d12-109">Property value</span></span>

<span data-ttu-id="35d12-110">O valor desse controle inclui dois campos, onde cada campo tem 16 bits.</span><span class="sxs-lookup"><span data-stu-id="35d12-110">The value of this control includes two fields, where each field has 16 bits.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35d12-111">Valor</span><span class="sxs-lookup"><span data-stu-id="35d12-111">Value</span></span></th>
<th><span data-ttu-id="35d12-112">Significado</span><span class="sxs-lookup"><span data-stu-id="35d12-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <span data-ttu-id="35d12-113"><dt><strong>O primeiro bits de campo</strong></dt> <dt>[0.. 15]</dt> </span><span class="sxs-lookup"><span data-stu-id="35d12-113"><dt><strong>The first field</strong></dt> <dt>Bits[0..15]</dt> </span></span></dl></td>
<td><span data-ttu-id="35d12-114">Indica quais quadros EPD são permitidos para codificar o quadro atual.</span><span class="sxs-lookup"><span data-stu-id="35d12-114">Indicates which LTR frame(s) are allowed for encoding the current frame.</span></span> <br/> <span data-ttu-id="35d12-115"><strong>Codificadores H. 264/AVC:</strong></span><span class="sxs-lookup"><span data-stu-id="35d12-115"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="35d12-116">Este é um bitmap que indica quais quadros EPD podem ser usados como uma referência para esse quadro.</span><span class="sxs-lookup"><span data-stu-id="35d12-116">This is a bitmap that indicates which LTR frames can be used as a reference for this frame.</span></span> <span data-ttu-id="35d12-117">O bit menos significativo corresponde ao índice LTR 0, o segundo bit menos significativo corresponde ao índice EPD 1, etc.</span><span class="sxs-lookup"><span data-stu-id="35d12-117">The least significant bit corresponds to LTR index 0, the second least significant bit corresponds to LTR index 1, etc.</span></span><br/> <span data-ttu-id="35d12-118">Esse valor não deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="35d12-118">This value shall not be 0.</span></span><br/> <span data-ttu-id="35d12-119">O índice mais alto especificado por esse valor não deve ser maior que o número máximo de quadros EPD especificados na propriedade <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> menos um.</span><span class="sxs-lookup"><span data-stu-id="35d12-119">The highest index specified by this value shall not be greater than the maximum number of LTR frames specified in the <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> property less one.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <span data-ttu-id="35d12-120"><dt><strong>O segundo campo</strong></dt> <dt>bits [16.. 31]</dt> </span><span class="sxs-lookup"><span data-stu-id="35d12-120"><dt><strong>The second field</strong></dt> <dt>Bits[16..31]</dt> </span></span></dl></td>
<td><span data-ttu-id="35d12-121">Sinalizador que indica se são necessárias limitações adicionais para a codificação de quadros subsequentes.</span><span class="sxs-lookup"><span data-stu-id="35d12-121">Flag that indicates whether additional limitations are required for encoding subsequent frames.</span></span> <br/> <span data-ttu-id="35d12-122"><strong>Codificadores H. 264/AVC:</strong></span><span class="sxs-lookup"><span data-stu-id="35d12-122"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="35d12-123">1 está no único valor válido para este campo.</span><span class="sxs-lookup"><span data-stu-id="35d12-123">1 is on the only valid value for this field.</span></span> <span data-ttu-id="35d12-124">Todos os outros valores são inválidos e reservados para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="35d12-124">All other values are invalid and reserved for future use.</span></span><br/> <span data-ttu-id="35d12-125">Quando o sinalizador for 1, o codificador deverá codificar os quadros subsequentes na ordem de codificação, sujeito às seguintes restrições:</span><span class="sxs-lookup"><span data-stu-id="35d12-125">When the flag is 1, the encoder shall encode subsequent frames in encoding order subject to the following constraints:</span></span><br/>
<ul>
<li><span data-ttu-id="35d12-126">Ele não deve usar quadros de referência de curto prazo na ordem de codificação mais antiga do que o quadro atual ou a codificação futura na ordem de codificação.</span><span class="sxs-lookup"><span data-stu-id="35d12-126">It shall not use short term reference frames in encoding order older than the current frame or future encoding in encoding order.</span></span></li>
<li><span data-ttu-id="35d12-127">Ele não deve usar quadros LTR não descritos pelo controle de CODECAPI_AVEncVideoUseLTRFrame mais recente.</span><span class="sxs-lookup"><span data-stu-id="35d12-127">It shall not use LTR frames not described by the most recent CODECAPI_AVEncVideoUseLTRFrame control.</span></span></li>
<li><span data-ttu-id="35d12-128">Ele pode usar quadros LTR atualizados após o quadro atual.</span><span class="sxs-lookup"><span data-stu-id="35d12-128">It may use LTR frames updated after the current frame.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="35d12-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="35d12-129">Remarks</span></span>

<span data-ttu-id="35d12-130">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="35d12-130">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="35d12-131">Esta propriedade não deverá ser chamada se uma chamada pendente para usar um quadro EPD tiver sido emitida usando a \_ Propriedade CODECAPI AVEncVideoUseLTRFrame e o codificador ainda não tiver gerado um quadro que tenha usado o ltr.</span><span class="sxs-lookup"><span data-stu-id="35d12-131">This property should not be called if a pending call to use an LTR frame has been issued using the CODECAPI\_AVEncVideoUseLTRFrame property and the encoder has not yet generated a frame that has used the LTR.</span></span> <span data-ttu-id="35d12-132">Em outras palavras, o codificador não deve enfileirar \_ as solicitações CODECAPI AVEncVideoUseLTRFrame.</span><span class="sxs-lookup"><span data-stu-id="35d12-132">In other words, the encoder should not queue up CODECAPI\_AVEncVideoUseLTRFrame requests.</span></span>

<span data-ttu-id="35d12-133">Se uma \_ solicitação CODECAPI AVEncVideoUseLTRFrame for enviada enquanto outra \_ solicitação AVEncVideoUseLTRFrame CODECAPI ainda estiver pendente, a solicitação mais antiga deverá ser descartada.</span><span class="sxs-lookup"><span data-stu-id="35d12-133">If a CODECAPI\_AVEncVideoUseLTRFrame request is submitted while another CODECAPI\_AVEncVideoUseLTRFrame request is still pending, then the older request should be dropped.</span></span>

<span data-ttu-id="35d12-134">Chamar CODECAPI \_ AVEncVideoUseLTRFrame em um quadro de camada não base é válido e deve ser aplicado ao quadro de camada não base, sem atraso em um quadro de camada de base.</span><span class="sxs-lookup"><span data-stu-id="35d12-134">Calling CODECAPI\_AVEncVideoUseLTRFrame on a non-base layer frame is valid and shall apply to the non-base layer frame, without delay to a base layer frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="35d12-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35d12-135">Requirements</span></span>



| <span data-ttu-id="35d12-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="35d12-136">Requirement</span></span> | <span data-ttu-id="35d12-137">Valor</span><span class="sxs-lookup"><span data-stu-id="35d12-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35d12-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35d12-138">Minimum supported client</span></span><br/> | <span data-ttu-id="35d12-139">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="35d12-139">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="35d12-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35d12-140">Minimum supported server</span></span><br/> | <span data-ttu-id="35d12-141">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="35d12-141">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="35d12-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35d12-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="35d12-143"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="35d12-143"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35d12-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="35d12-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35d12-145">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="35d12-145">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




