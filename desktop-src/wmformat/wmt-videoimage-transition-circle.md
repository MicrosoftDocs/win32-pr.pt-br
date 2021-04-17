---
title: WMT_VIDEOIMAGE_TRANSITION_CIRCLE (Wmsdkidl. h)
description: A transição de círculo revela a nova imagem em um círculo.
ms.assetid: ba3bcf46-1254-4aad-a958-0f9ddb2f40dc
keywords:
- WMT_VIDEOIMAGE_TRANSITION_CIRCLE o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_CIRCLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ccf3a8eff2ca5a5069fa01c4e61bc0735808fd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763149"
---
# <a name="wmt_videoimage_transition_circle"></a><span data-ttu-id="a0d02-104">\_círculo de \_ transição de VIDEOIMAGE WMT \_</span><span class="sxs-lookup"><span data-stu-id="a0d02-104">WMT\_VIDEOIMAGE\_TRANSITION\_CIRCLE</span></span>

<span data-ttu-id="a0d02-105">A transição de círculo revela a nova imagem em um círculo.</span><span class="sxs-lookup"><span data-stu-id="a0d02-105">The circle transition reveals the new image in a circle.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0d02-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0d02-106">Parameters</span></span>

<span data-ttu-id="a0d02-107">A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="a0d02-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0d02-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0d02-108">Parameter</span></span></th>
<th><span data-ttu-id="a0d02-109">Membro da estrutura</span><span class="sxs-lookup"><span data-stu-id="a0d02-109">Structure member</span></span></th>
<th><span data-ttu-id="a0d02-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0d02-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0d02-111">X central</span><span class="sxs-lookup"><span data-stu-id="a0d02-111">Center X</span></span></td>
<td><span data-ttu-id="a0d02-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="a0d02-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="a0d02-113">Coordenada X, em relação ao quadro de vídeo, do centro do círculo.</span><span class="sxs-lookup"><span data-stu-id="a0d02-113">X-coordinate, relative to the video frame, of the center of the circle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0d02-114">Y central</span><span class="sxs-lookup"><span data-stu-id="a0d02-114">Center Y</span></span></td>
<td><span data-ttu-id="a0d02-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="a0d02-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="a0d02-116">Coordenada Y, em relação ao quadro de vídeo, do centro do círculo.</span><span class="sxs-lookup"><span data-stu-id="a0d02-116">Y-coordinate, relative to the video frame, of center of the circle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0d02-117">Raio</span><span class="sxs-lookup"><span data-stu-id="a0d02-117">Radius</span></span></td>
<td><span data-ttu-id="a0d02-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="a0d02-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="a0d02-119">Raio, em pixels, do círculo.</span><span class="sxs-lookup"><span data-stu-id="a0d02-119">Radius, in pixels, of the circle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0d02-120">Composição</span><span class="sxs-lookup"><span data-stu-id="a0d02-120">Composition</span></span></td>
<td><span data-ttu-id="a0d02-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="a0d02-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="a0d02-122">Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="a0d02-122">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="a0d02-123">0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="a0d02-123">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="a0d02-124">1-especifica a composição invertida, na qual a imagem atual é a imagem de plano de fundo, e a imagem anterior é o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="a0d02-124">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="a0d02-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0d02-125">Requirements</span></span>



| <span data-ttu-id="a0d02-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0d02-126">Requirement</span></span> | <span data-ttu-id="a0d02-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a0d02-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0d02-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0d02-128">Header</span></span><br/> | <dl> <span data-ttu-id="a0d02-129"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0d02-129"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0d02-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0d02-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0d02-131">**Transições de imagem de vídeo**</span><span class="sxs-lookup"><span data-stu-id="a0d02-131">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





