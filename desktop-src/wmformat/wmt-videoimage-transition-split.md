---
title: WMT_VIDEOIMAGE_TRANSITION_SPLIT (Wmsdkidl. h)
description: A transição de divisão revela a nova imagem, dividindo a imagem antiga. A divisão aparece ao longo de uma linha reta horizontal ou vertical começando dentro do quadro.
ms.assetid: ad777bfb-29a7-441f-8399-e462639450eb
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05df253c730b85c4bef8cf18d05ed98fcbd78f35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747258"
---
# <a name="wmt_videoimage_transition_split"></a><span data-ttu-id="5bee4-105">\_divisão de \_ transição WMT VIDEOIMAGE \_</span><span class="sxs-lookup"><span data-stu-id="5bee4-105">WMT\_VIDEOIMAGE\_TRANSITION\_SPLIT</span></span>

<span data-ttu-id="5bee4-106">A transição de divisão revela a nova imagem, dividindo a imagem antiga.</span><span class="sxs-lookup"><span data-stu-id="5bee4-106">The split transition reveals the new image by splitting the old image.</span></span> <span data-ttu-id="5bee4-107">A divisão aparece ao longo de uma linha reta horizontal ou vertical começando dentro do quadro.</span><span class="sxs-lookup"><span data-stu-id="5bee4-107">The split appears along a straight horizontal or vertical line starting inside the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="5bee4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bee4-108">Parameters</span></span>

<span data-ttu-id="5bee4-109">A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="5bee4-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5bee4-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5bee4-110">Parameter</span></span></th>
<th><span data-ttu-id="5bee4-111">Membro da estrutura</span><span class="sxs-lookup"><span data-stu-id="5bee4-111">Structure member</span></span></th>
<th><span data-ttu-id="5bee4-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5bee4-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5bee4-113">X central</span><span class="sxs-lookup"><span data-stu-id="5bee4-113">Center X</span></span></td>
<td><span data-ttu-id="5bee4-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="5bee4-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="5bee4-115">Coordenada X, em relação ao quadro de vídeo, da linha de origem da divisão.</span><span class="sxs-lookup"><span data-stu-id="5bee4-115">X-coordinate, relative to the video frame, of the origin line of the split.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5bee4-116">Y central</span><span class="sxs-lookup"><span data-stu-id="5bee4-116">Center Y</span></span></td>
<td><span data-ttu-id="5bee4-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="5bee4-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="5bee4-118">Coordenada Y, em relação ao quadro de vídeo, da linha de origem da divisão.</span><span class="sxs-lookup"><span data-stu-id="5bee4-118">Y-coordinate, relative to the video frame, of the origin line of the split.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5bee4-119">Distância</span><span class="sxs-lookup"><span data-stu-id="5bee4-119">Distance</span></span></td>
<td><span data-ttu-id="5bee4-120"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="5bee4-120"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="5bee4-121">Largura da divisão em pixels.</span><span class="sxs-lookup"><span data-stu-id="5bee4-121">Width of the split in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5bee4-122">Direção</span><span class="sxs-lookup"><span data-stu-id="5bee4-122">Direction</span></span></td>
<td><span data-ttu-id="5bee4-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="5bee4-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="5bee4-124">Orientação da divisão. Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="5bee4-124">Orientation of the split.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="5bee4-125">0-divide ao longo de uma linha horizontal.</span><span class="sxs-lookup"><span data-stu-id="5bee4-125">0 - Splits along a horizontal line.</span></span></li>
<li><span data-ttu-id="5bee4-126">1-divide ao longo de uma linha vertical.</span><span class="sxs-lookup"><span data-stu-id="5bee4-126">1 - Splits along a vertical line.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5bee4-127">Composição</span><span class="sxs-lookup"><span data-stu-id="5bee4-127">Composition</span></span></td>
<td><span data-ttu-id="5bee4-128"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="5bee4-128"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="5bee4-129">Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="5bee4-129">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="5bee4-130">0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="5bee4-130">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="5bee4-131">1-especifica a composição revertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</span><span class="sxs-lookup"><span data-stu-id="5bee4-131">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="5bee4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bee4-132">Requirements</span></span>



| <span data-ttu-id="5bee4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bee4-133">Requirement</span></span> | <span data-ttu-id="5bee4-134">Valor</span><span class="sxs-lookup"><span data-stu-id="5bee4-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5bee4-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5bee4-135">Header</span></span><br/> | <dl> <span data-ttu-id="5bee4-136"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bee4-136"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bee4-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bee4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bee4-138">**Transições de imagem de vídeo**</span><span class="sxs-lookup"><span data-stu-id="5bee4-138">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





