---
title: WMT_VIDEOIMAGE_TRANSITION_WHEEL (Wmsdkidl. h)
description: A transição da roda revela a nova imagem girando quatro linhas em um ponto dinâmico comum, como os spokes de uma roda.
ms.assetid: 426217be-789b-4b78-b0ea-de9629ecd46c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f39d3355cfce3397c379bf7edafaae77ccfafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747666"
---
# <a name="wmt_videoimage_transition_wheel"></a><span data-ttu-id="09640-104">\_roda de \_ transição WMT VIDEOIMAGE \_</span><span class="sxs-lookup"><span data-stu-id="09640-104">WMT\_VIDEOIMAGE\_TRANSITION\_WHEEL</span></span>

<span data-ttu-id="09640-105">A transição da roda revela a nova imagem girando quatro linhas em um ponto dinâmico comum, como os spokes de uma roda.</span><span class="sxs-lookup"><span data-stu-id="09640-105">The wheel transition reveals the new image by rotating four lines around a common pivot point, like the spokes of a wheel.</span></span>

## <a name="parameters"></a><span data-ttu-id="09640-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09640-106">Parameters</span></span>

<span data-ttu-id="09640-107">A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="09640-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09640-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="09640-108">Parameter</span></span></th>
<th><span data-ttu-id="09640-109">Membro da estrutura</span><span class="sxs-lookup"><span data-stu-id="09640-109">Structure member</span></span></th>
<th><span data-ttu-id="09640-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="09640-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="09640-111">X central</span><span class="sxs-lookup"><span data-stu-id="09640-111">Center X</span></span></td>
<td><span data-ttu-id="09640-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="09640-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="09640-113">Coordenada X, em relação ao quadro de vídeo, do centro do efeito de roda.</span><span class="sxs-lookup"><span data-stu-id="09640-113">X-coordinate, relative to the video frame, of the center of the wheel effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09640-114">Y central</span><span class="sxs-lookup"><span data-stu-id="09640-114">Center Y</span></span></td>
<td><span data-ttu-id="09640-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="09640-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="09640-116">Coordenada Y, em relação ao quadro de vídeo, do centro do efeito de roda.</span><span class="sxs-lookup"><span data-stu-id="09640-116">Y-coordinate, relative to the video frame, of the center of the wheel effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09640-117">Ângulo</span><span class="sxs-lookup"><span data-stu-id="09640-117">Angle</span></span></td>
<td><span data-ttu-id="09640-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="09640-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="09640-119">Ângulo de rotação, em graus, dos spokes do efeito de roda.</span><span class="sxs-lookup"><span data-stu-id="09640-119">Angle of rotation, in degrees, of the spokes of the wheel effect.</span></span> <span data-ttu-id="09640-120">Um valor de 0,0 indica a imagem antiga sem qualquer uma das novas imagens reveladas.</span><span class="sxs-lookup"><span data-stu-id="09640-120">A value of 0.0 indicates the old image without any of the new image revealed.</span></span> <span data-ttu-id="09640-121">Um valor de 90,0 indica a nova imagem totalmente revelada. A movimentação de 0,0 para 90,0 aparece como rotação horária dos spokes.</span><span class="sxs-lookup"><span data-stu-id="09640-121">A value of 90.0 indicates the new image fully revealed.Movement from 0.0 to 90.0 appears as clockwise rotation of the spokes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09640-122">Composição</span><span class="sxs-lookup"><span data-stu-id="09640-122">Composition</span></span></td>
<td><span data-ttu-id="09640-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="09640-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="09640-124">Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="09640-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="09640-125">0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="09640-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="09640-126">1-especifica a composição revertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</span><span class="sxs-lookup"><span data-stu-id="09640-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="09640-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09640-127">Requirements</span></span>



| <span data-ttu-id="09640-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="09640-128">Requirement</span></span> | <span data-ttu-id="09640-129">Valor</span><span class="sxs-lookup"><span data-stu-id="09640-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09640-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="09640-130">Header</span></span><br/> | <dl> <span data-ttu-id="09640-131"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="09640-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09640-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="09640-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09640-133">**Transições de imagem de vídeo**</span><span class="sxs-lookup"><span data-stu-id="09640-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





