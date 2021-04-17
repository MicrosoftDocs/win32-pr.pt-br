---
title: WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (Wmsdkidl. h)
description: A transição de rolagem de página transforma a imagem antiga com um efeito de inversão de página, revelando a nova imagem abaixo.
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4167395dbe00242af42f30713438f33e88f2dda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748041"
---
# <a name="wmt_videoimage_transition_page_roll"></a><span data-ttu-id="645fa-104">Roll WMT de \_ \_ página de transição VIDEOIMAGE \_ \_</span><span class="sxs-lookup"><span data-stu-id="645fa-104">WMT\_VIDEOIMAGE\_TRANSITION\_PAGE\_ROLL</span></span>

<span data-ttu-id="645fa-105">A transição de rolagem de página transforma a imagem antiga com um efeito de inversão de página, revelando a nova imagem abaixo.</span><span class="sxs-lookup"><span data-stu-id="645fa-105">The page roll transition transforms the old image with a page-flipping effect, revealing the new image underneath.</span></span>

## <a name="parameters"></a><span data-ttu-id="645fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="645fa-106">Parameters</span></span>

<span data-ttu-id="645fa-107">A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="645fa-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="645fa-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="645fa-108">Parameter</span></span></th>
<th><span data-ttu-id="645fa-109">Membro da estrutura</span><span class="sxs-lookup"><span data-stu-id="645fa-109">Structure member</span></span></th>
<th><span data-ttu-id="645fa-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="645fa-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="645fa-111">Raio</span><span class="sxs-lookup"><span data-stu-id="645fa-111">Radius</span></span></td>
<td><span data-ttu-id="645fa-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="645fa-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="645fa-113">Raio do rolo no efeito de acúmulo de página.</span><span class="sxs-lookup"><span data-stu-id="645fa-113">Radius of the roll in the page roll effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="645fa-114">Distância</span><span class="sxs-lookup"><span data-stu-id="645fa-114">Distance</span></span></td>
<td><span data-ttu-id="645fa-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="645fa-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="645fa-116">A quantidade da nova imagem que é revelada pelo efeito de acúmulo de página, em pixels.</span><span class="sxs-lookup"><span data-stu-id="645fa-116">Amount of the new image that is revealed by the page roll effect, in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="645fa-117">Direção</span><span class="sxs-lookup"><span data-stu-id="645fa-117">Direction</span></span></td>
<td><span data-ttu-id="645fa-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="645fa-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="645fa-119">Canto ou lado do quadro de vídeo, do qual o rolo de página se origina. Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="645fa-119">Corner or side of the video frame, from which the page roll originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="645fa-120">0-lado esquerdo</span><span class="sxs-lookup"><span data-stu-id="645fa-120">0 - Left side</span></span></li>
<li><span data-ttu-id="645fa-121">1-lado direito</span><span class="sxs-lookup"><span data-stu-id="645fa-121">1 - Right side</span></span></li>
<li><span data-ttu-id="645fa-122">2-inferior</span><span class="sxs-lookup"><span data-stu-id="645fa-122">2 - Bottom</span></span></li>
<li><span data-ttu-id="645fa-123">3-superior</span><span class="sxs-lookup"><span data-stu-id="645fa-123">3 - Top</span></span></li>
<li><span data-ttu-id="645fa-124">4-canto inferior esquerdo</span><span class="sxs-lookup"><span data-stu-id="645fa-124">4 - Bottom left corner</span></span></li>
<li><span data-ttu-id="645fa-125">5-canto inferior direito</span><span class="sxs-lookup"><span data-stu-id="645fa-125">5 - Bottom right corner</span></span></li>
<li><span data-ttu-id="645fa-126">6-canto superior esquerdo</span><span class="sxs-lookup"><span data-stu-id="645fa-126">6 - Upper left corner</span></span></li>
<li><span data-ttu-id="645fa-127">7-canto superior direito</span><span class="sxs-lookup"><span data-stu-id="645fa-127">7 - Upper right corner</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="645fa-128">Composição</span><span class="sxs-lookup"><span data-stu-id="645fa-128">Composition</span></span></td>
<td><span data-ttu-id="645fa-129"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="645fa-129"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="645fa-130">Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="645fa-130">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="645fa-131">0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="645fa-131">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="645fa-132">1-especifica a composição revertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</span><span class="sxs-lookup"><span data-stu-id="645fa-132">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="645fa-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="645fa-133">Requirements</span></span>



| <span data-ttu-id="645fa-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="645fa-134">Requirement</span></span> | <span data-ttu-id="645fa-135">Valor</span><span class="sxs-lookup"><span data-stu-id="645fa-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="645fa-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="645fa-136">Header</span></span><br/> | <dl> <span data-ttu-id="645fa-137"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="645fa-137"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="645fa-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="645fa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="645fa-139">**Transições de imagem de vídeo**</span><span class="sxs-lookup"><span data-stu-id="645fa-139">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





