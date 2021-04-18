---
title: WMT_VIDEOIMAGE_TRANSITION_FILLED_V (Wmsdkidl. h)
description: A transição de V preenchida revela a nova imagem em um triângulo proveniente de um lado do quadro.
ms.assetid: d256178f-cb1d-4d36-9d30-e6dd6b3b23ec
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfe229657dfd29d3cb9d83a8a4853e2e89a7a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781083"
---
# <a name="wmt_videoimage_transition_filled_v"></a><span data-ttu-id="86ae4-104">transição de WMT \_ VIDEOIMAGE \_ \_ preenchida \_</span><span class="sxs-lookup"><span data-stu-id="86ae4-104">WMT\_VIDEOIMAGE\_TRANSITION\_FILLED\_V</span></span>

<span data-ttu-id="86ae4-105">A transição de V preenchida revela a nova imagem em um triângulo proveniente de um lado do quadro.</span><span class="sxs-lookup"><span data-stu-id="86ae4-105">The filled V transition reveals the new image in a triangle originating from one side of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="86ae4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86ae4-106">Parameters</span></span>

<span data-ttu-id="86ae4-107">A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="86ae4-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="86ae4-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="86ae4-108">Parameter</span></span></th>
<th><span data-ttu-id="86ae4-109">Membro da estrutura</span><span class="sxs-lookup"><span data-stu-id="86ae4-109">Structure member</span></span></th>
<th><span data-ttu-id="86ae4-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="86ae4-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="86ae4-111">Largura</span><span class="sxs-lookup"><span data-stu-id="86ae4-111">Width</span></span></td>
<td><span data-ttu-id="86ae4-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="86ae4-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="86ae4-113">Largura do V preenchido em pixels.</span><span class="sxs-lookup"><span data-stu-id="86ae4-113">Width of the filled V in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86ae4-114">Altura</span><span class="sxs-lookup"><span data-stu-id="86ae4-114">Height</span></span></td>
<td><span data-ttu-id="86ae4-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="86ae4-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="86ae4-116">Altura do V preenchido em pixels.</span><span class="sxs-lookup"><span data-stu-id="86ae4-116">Height of the filled V in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="86ae4-117">Direção</span><span class="sxs-lookup"><span data-stu-id="86ae4-117">Direction</span></span></td>
<td><span data-ttu-id="86ae4-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="86ae4-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="86ae4-119">Direção da qual o V preenchido é originado. Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="86ae4-119">Direction from which the filled V originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="86ae4-120">0-entra no lado esquerdo do quadro.</span><span class="sxs-lookup"><span data-stu-id="86ae4-120">0 - Enters from the left side of the frame.</span></span></li>
<li><span data-ttu-id="86ae4-121">1-insere do lado direito do quadro.</span><span class="sxs-lookup"><span data-stu-id="86ae4-121">1 - Enters from the right side of the frame.</span></span></li>
<li><span data-ttu-id="86ae4-122">2-entra na parte inferior do quadro.</span><span class="sxs-lookup"><span data-stu-id="86ae4-122">2 - Enters from the bottom of the frame.</span></span></li>
<li><span data-ttu-id="86ae4-123">3-entra na parte superior do quadro.</span><span class="sxs-lookup"><span data-stu-id="86ae4-123">3 - Enters from the top of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86ae4-124">Composição</span><span class="sxs-lookup"><span data-stu-id="86ae4-124">Composition</span></span></td>
<td><span data-ttu-id="86ae4-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="86ae4-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="86ae4-126">Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="86ae4-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="86ae4-127">0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="86ae4-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="86ae4-128">1-especifica a composição revertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</span><span class="sxs-lookup"><span data-stu-id="86ae4-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="86ae4-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86ae4-129">Requirements</span></span>



| <span data-ttu-id="86ae4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="86ae4-130">Requirement</span></span> | <span data-ttu-id="86ae4-131">Valor</span><span class="sxs-lookup"><span data-stu-id="86ae4-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86ae4-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="86ae4-132">Header</span></span><br/> | <dl> <span data-ttu-id="86ae4-133"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="86ae4-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86ae4-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="86ae4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86ae4-135">**Transições de imagem de vídeo**</span><span class="sxs-lookup"><span data-stu-id="86ae4-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





