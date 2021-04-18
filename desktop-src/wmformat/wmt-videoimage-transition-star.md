---
title: WMT_VIDEOIMAGE_TRANSITION_STAR (Wmsdkidl. h)
description: A transição de estrela revela a nova imagem em uma estrela de cinco pontas dentro do quadro.
ms.assetid: d16f73ce-0fa8-47b4-8146-32f276e6d16c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_STAR o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_STAR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af064682c4488153823164433bd432a9080336fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811678"
---
# <a name="wmt_videoimage_transition_star"></a><span data-ttu-id="10f52-104">\_estrela de \_ transição WMT VIDEOIMAGE \_</span><span class="sxs-lookup"><span data-stu-id="10f52-104">WMT\_VIDEOIMAGE\_TRANSITION\_STAR</span></span>

<span data-ttu-id="10f52-105">A transição de estrela revela a nova imagem em uma estrela de cinco pontas dentro do quadro.</span><span class="sxs-lookup"><span data-stu-id="10f52-105">The star transition reveals the new image in a five-pointed star inside the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="10f52-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10f52-106">Parameters</span></span>

<span data-ttu-id="10f52-107">A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="10f52-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="10f52-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="10f52-108">Parameter</span></span></th>
<th><span data-ttu-id="10f52-109">Membro da estrutura</span><span class="sxs-lookup"><span data-stu-id="10f52-109">Structure member</span></span></th>
<th><span data-ttu-id="10f52-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="10f52-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10f52-111">X central</span><span class="sxs-lookup"><span data-stu-id="10f52-111">Center X</span></span></td>
<td><span data-ttu-id="10f52-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="10f52-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="10f52-113">Coordenada X, em relação ao quadro de vídeo, do centro da estrela.</span><span class="sxs-lookup"><span data-stu-id="10f52-113">X-coordinate, relative to the video frame, of the center of the star.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10f52-114">Y central</span><span class="sxs-lookup"><span data-stu-id="10f52-114">Center Y</span></span></td>
<td><span data-ttu-id="10f52-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="10f52-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="10f52-116">Coordenada Y, em relação ao quadro de vídeo, do centro da estrela.</span><span class="sxs-lookup"><span data-stu-id="10f52-116">Y-coordinate, relative to the video frame, of the center of the star.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10f52-117">Raio</span><span class="sxs-lookup"><span data-stu-id="10f52-117">Radius</span></span></td>
<td><span data-ttu-id="10f52-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="10f52-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="10f52-119">Raio, em pixels, do círculo definido pelos pontos da estrela.</span><span class="sxs-lookup"><span data-stu-id="10f52-119">Radius, in pixels, of the circle defined by the points of the star.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10f52-120">Composição</span><span class="sxs-lookup"><span data-stu-id="10f52-120">Composition</span></span></td>
<td><span data-ttu-id="10f52-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="10f52-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="10f52-122">Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="10f52-122">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="10f52-123">0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="10f52-123">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="10f52-124">1-especifica a composição invertida, na qual a imagem atual é a imagem de plano de fundo, e a imagem anterior é o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="10f52-124">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="10f52-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10f52-125">Requirements</span></span>



| <span data-ttu-id="10f52-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="10f52-126">Requirement</span></span> | <span data-ttu-id="10f52-127">Valor</span><span class="sxs-lookup"><span data-stu-id="10f52-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10f52-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="10f52-128">Header</span></span><br/> | <dl> <span data-ttu-id="10f52-129"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="10f52-129"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10f52-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="10f52-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10f52-131">**Transições de imagem de vídeo**</span><span class="sxs-lookup"><span data-stu-id="10f52-131">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





