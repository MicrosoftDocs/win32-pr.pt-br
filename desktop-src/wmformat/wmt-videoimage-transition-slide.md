---
title: WMT_VIDEOIMAGE_TRANSITION_SLIDE (Wmsdkidl. h)
description: A transição de slides revela a nova imagem deslizando a imagem antiga para fora do quadro.
ms.assetid: 925bcf92-5608-48ca-9bdc-dd08bcd8b8d5
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26caaadc268e823734c2bcf4a7899e6bb5399192
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747632"
---
# <a name="wmt_videoimage_transition_slide"></a><span data-ttu-id="16728-104">SLIDE de transição do WMT \_ VIDEOIMAGE \_ \_</span><span class="sxs-lookup"><span data-stu-id="16728-104">WMT\_VIDEOIMAGE\_TRANSITION\_SLIDE</span></span>

<span data-ttu-id="16728-105">A transição de slides revela a nova imagem deslizando a imagem antiga para fora do quadro.</span><span class="sxs-lookup"><span data-stu-id="16728-105">The slide transition reveals the new image by sliding the old image out of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="16728-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16728-106">Parameters</span></span>

<span data-ttu-id="16728-107">A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="16728-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="16728-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="16728-108">Parameter</span></span></th>
<th><span data-ttu-id="16728-109">Membro da estrutura</span><span class="sxs-lookup"><span data-stu-id="16728-109">Structure member</span></span></th>
<th><span data-ttu-id="16728-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="16728-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="16728-111">Distância</span><span class="sxs-lookup"><span data-stu-id="16728-111">Distance</span></span></td>
<td><span data-ttu-id="16728-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="16728-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="16728-113">Distância, em pixels, que a imagem antiga desliza para fora do quadro.</span><span class="sxs-lookup"><span data-stu-id="16728-113">Distance, in pixels, that the old image slides out of the frame.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16728-114">Direção</span><span class="sxs-lookup"><span data-stu-id="16728-114">Direction</span></span></td>
<td><span data-ttu-id="16728-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="16728-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="16728-116">Direção na qual os slides da imagem antiga. Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="16728-116">Direction in which the old image slides.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="16728-117">0 – deslize para a direita.</span><span class="sxs-lookup"><span data-stu-id="16728-117">0 - Slide to the right.</span></span></li>
<li><span data-ttu-id="16728-118">1-slide à esquerda.</span><span class="sxs-lookup"><span data-stu-id="16728-118">1 - Slide to the left.</span></span></li>
<li><span data-ttu-id="16728-119">2-Deslize para cima.</span><span class="sxs-lookup"><span data-stu-id="16728-119">2 - Slide upward.</span></span></li>
<li><span data-ttu-id="16728-120">3-deslizar para baixo.</span><span class="sxs-lookup"><span data-stu-id="16728-120">3 - Slide downward.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16728-121">Composição</span><span class="sxs-lookup"><span data-stu-id="16728-121">Composition</span></span></td>
<td><span data-ttu-id="16728-122"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="16728-122"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="16728-123">Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="16728-123">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="16728-124">0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="16728-124">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="16728-125">1-especifica a composição revertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</span><span class="sxs-lookup"><span data-stu-id="16728-125">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="16728-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16728-126">Requirements</span></span>



| <span data-ttu-id="16728-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="16728-127">Requirement</span></span> | <span data-ttu-id="16728-128">Valor</span><span class="sxs-lookup"><span data-stu-id="16728-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16728-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16728-129">Header</span></span><br/> | <dl> <span data-ttu-id="16728-130"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="16728-130"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16728-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="16728-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16728-132">**Transições de imagem de vídeo**</span><span class="sxs-lookup"><span data-stu-id="16728-132">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





