---
title: WMT_VIDEOIMAGE_TRANSITION_INSET (Wmsdkidl. h)
description: A transição de inserção revela a nova imagem em um retângulo originado de um canto do quadro.
ms.assetid: fd8bc4b7-0546-4897-ab7b-a320bbd126ef
keywords:
- WMT_VIDEOIMAGE_TRANSITION_INSET o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_INSET
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd41887fafaae2756e2dafe3d57d4f1a86edf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749672"
---
# <a name="wmt_videoimage_transition_inset"></a><span data-ttu-id="08c65-104">\_inserção de \_ transição WMT VIDEOIMAGE \_</span><span class="sxs-lookup"><span data-stu-id="08c65-104">WMT\_VIDEOIMAGE\_TRANSITION\_INSET</span></span>

<span data-ttu-id="08c65-105">A transição de inserção revela a nova imagem em um retângulo originado de um canto do quadro.</span><span class="sxs-lookup"><span data-stu-id="08c65-105">The inset transition reveals the new image in a rectangle originating from one corner of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="08c65-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08c65-106">Parameters</span></span>

<span data-ttu-id="08c65-107">A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="08c65-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08c65-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="08c65-108">Parameter</span></span></th>
<th><span data-ttu-id="08c65-109">Membro da estrutura</span><span class="sxs-lookup"><span data-stu-id="08c65-109">Structure member</span></span></th>
<th><span data-ttu-id="08c65-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="08c65-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="08c65-111">Largura</span><span class="sxs-lookup"><span data-stu-id="08c65-111">Width</span></span></td>
<td><span data-ttu-id="08c65-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="08c65-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="08c65-113">Largura da margem interna em pixels.</span><span class="sxs-lookup"><span data-stu-id="08c65-113">Width of the inset in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08c65-114">Altura</span><span class="sxs-lookup"><span data-stu-id="08c65-114">Height</span></span></td>
<td><span data-ttu-id="08c65-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="08c65-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="08c65-116">Altura da margem interna em pixels.</span><span class="sxs-lookup"><span data-stu-id="08c65-116">Height of the inset in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08c65-117">Direção</span><span class="sxs-lookup"><span data-stu-id="08c65-117">Direction</span></span></td>
<td><span data-ttu-id="08c65-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="08c65-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="08c65-119">Canto do qual a margem interna se origina. Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="08c65-119">Corner from which the inset originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="08c65-120">0-inferior esquerdo</span><span class="sxs-lookup"><span data-stu-id="08c65-120">0 - Lower left</span></span></li>
<li><span data-ttu-id="08c65-121">1-inferior direito</span><span class="sxs-lookup"><span data-stu-id="08c65-121">1 - Lower right</span></span></li>
<li><span data-ttu-id="08c65-122">2-superior esquerdo</span><span class="sxs-lookup"><span data-stu-id="08c65-122">2 - Upper left</span></span></li>
<li><span data-ttu-id="08c65-123">3-superior direito</span><span class="sxs-lookup"><span data-stu-id="08c65-123">3 - Upper right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08c65-124">Composição</span><span class="sxs-lookup"><span data-stu-id="08c65-124">Composition</span></span></td>
<td><span data-ttu-id="08c65-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="08c65-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="08c65-126">Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="08c65-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="08c65-127">0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="08c65-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="08c65-128">1-especifica a composição revertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</span><span class="sxs-lookup"><span data-stu-id="08c65-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="08c65-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08c65-129">Requirements</span></span>



| <span data-ttu-id="08c65-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="08c65-130">Requirement</span></span> | <span data-ttu-id="08c65-131">Valor</span><span class="sxs-lookup"><span data-stu-id="08c65-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08c65-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="08c65-132">Header</span></span><br/> | <dl> <span data-ttu-id="08c65-133"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="08c65-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08c65-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="08c65-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08c65-135">**Transições de imagem de vídeo**</span><span class="sxs-lookup"><span data-stu-id="08c65-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





