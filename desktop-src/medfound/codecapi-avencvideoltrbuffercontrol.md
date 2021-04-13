---
description: Especifica o número máximo de quadros de referência de longo prazo (LTR) controlados pelo aplicativo.
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: Propriedade CODECAPI_AVEncVideoLTRBufferControl (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33adfc7d0ba2db87c2127489d9496dc5e0bb4158
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501195"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a><span data-ttu-id="472f0-103">\_Propriedade CODECAPI AVEncVideoLTRBufferControl</span><span class="sxs-lookup"><span data-stu-id="472f0-103">CODECAPI\_AVEncVideoLTRBufferControl property</span></span>

<span data-ttu-id="472f0-104">Especifica o número máximo de quadros de referência de longo prazo (LTR) controlados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="472f0-104">Specifies the maximum number of Long Term Reference (LTR) frames controlled by application.</span></span>

## <a name="data-type"></a><span data-ttu-id="472f0-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="472f0-105">Data type</span></span>

<span data-ttu-id="472f0-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="472f0-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="472f0-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="472f0-107">Property GUID</span></span>

<span data-ttu-id="472f0-108">**CODECAPI \_ AVEncVideoLTRBufferControl**</span><span class="sxs-lookup"><span data-stu-id="472f0-108">**CODECAPI\_AVEncVideoLTRBufferControl**</span></span>

## <a name="property-value"></a><span data-ttu-id="472f0-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="472f0-109">Property value</span></span>

<span data-ttu-id="472f0-110">O valor desse controle inclui dois campos, onde cada campo tem 16 bits.</span><span class="sxs-lookup"><span data-stu-id="472f0-110">The value of this control includes two fields, where each field has 16 bits.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="472f0-111">Valor</span><span class="sxs-lookup"><span data-stu-id="472f0-111">Value</span></span></th>
<th><span data-ttu-id="472f0-112">Significado</span><span class="sxs-lookup"><span data-stu-id="472f0-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <span data-ttu-id="472f0-113"><dt><strong>O primeiro bits de campo</strong></dt> <dt>[0.. 15]</dt> </span><span class="sxs-lookup"><span data-stu-id="472f0-113"><dt><strong>The first field</strong></dt> <dt>Bits[0..15]</dt> </span></span></dl></td>
<td><span data-ttu-id="472f0-114">O número de quadros LTR controlados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="472f0-114">The number of LTR frames controlled by the application.</span></span><br/> <span data-ttu-id="472f0-115"><strong>Codificadores H. 264/AVC:</strong></span><span class="sxs-lookup"><span data-stu-id="472f0-115"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="472f0-116">Supondo que o valor seja N e N seja um valor diferente de zero, em cada quadro de IDR, o codificador deve marcar automaticamente os quadros seguindo o quadro IDR (e incluindo o quadro IDR) como quadros EPD, contanto que todos os três dos seguintes se apliquem:</span><span class="sxs-lookup"><span data-stu-id="472f0-116">Assuming the value is N and N is non-zero value, at each IDR frame the encoder must automatically mark the frames following the IDR frame (and including the IDR frame) as LTR frames as long as all 3 of the following apply:</span></span>
<ul>
<li><span data-ttu-id="472f0-117">O quadro já não está definido para ser marcado como um quadro de referência de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="472f0-117">The frame is not already set to be marked as a long term reference frame.</span></span></li>
<li><span data-ttu-id="472f0-118">O quadro é um quadro de camada base.</span><span class="sxs-lookup"><span data-stu-id="472f0-118">The frame is a base layer frame.</span></span> <span data-ttu-id="472f0-119">Por exemplo, o elemento de sintaxe <strong>temporal_id</strong> igual a 0.</span><span class="sxs-lookup"><span data-stu-id="472f0-119">For example, syntax element <strong>temporal_id</strong> equal to 0.</span></span></li>
<li><span data-ttu-id="472f0-120">O número de quadros marcados atualmente como EPD é menor que N.</span><span class="sxs-lookup"><span data-stu-id="472f0-120">The number of frames currently marked as LTR is less than N.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <span data-ttu-id="472f0-121"><dt><strong>O segundo campo</strong></dt> <dt>bits [16.. 31]</dt> </span><span class="sxs-lookup"><span data-stu-id="472f0-121"><dt><strong>The second field</strong></dt> <dt>Bits[16..31]</dt> </span></span></dl></td>
<td><span data-ttu-id="472f0-122">O modo de confiança do controle EPD.</span><span class="sxs-lookup"><span data-stu-id="472f0-122">The trust mode of LTR control.</span></span><br/> <span data-ttu-id="472f0-123"><strong>Codificadores H. 264/AVC:</strong></span><span class="sxs-lookup"><span data-stu-id="472f0-123"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="472f0-124">1 (confiar até) significa que o codificador pode usar um quadro EPD, a menos que o aplicativo invalide-o explicitamente por meio do controle de <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> .</span><span class="sxs-lookup"><span data-stu-id="472f0-124">1 (Trust Until) means the encoder may use an LTR frame unless the app explicitly invalidates it through the <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> control.</span></span> <br/> <span data-ttu-id="472f0-125">Outros valores são inválidos e reservados para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="472f0-125">Other values are invalid and reserved for future use.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="472f0-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="472f0-126">Remarks</span></span>

<span data-ttu-id="472f0-127">Essa é uma API estática.</span><span class="sxs-lookup"><span data-stu-id="472f0-127">This is a static API.</span></span>

<span data-ttu-id="472f0-128">O valor padrão deve ser 0</span><span class="sxs-lookup"><span data-stu-id="472f0-128">Default value shall be 0</span></span>

## <a name="requirements"></a><span data-ttu-id="472f0-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="472f0-129">Requirements</span></span>



| <span data-ttu-id="472f0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="472f0-130">Requirement</span></span> | <span data-ttu-id="472f0-131">Valor</span><span class="sxs-lookup"><span data-stu-id="472f0-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="472f0-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="472f0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="472f0-133">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="472f0-133">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="472f0-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="472f0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="472f0-135">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="472f0-135">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="472f0-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="472f0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="472f0-137"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="472f0-137"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="472f0-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="472f0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="472f0-139">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="472f0-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




