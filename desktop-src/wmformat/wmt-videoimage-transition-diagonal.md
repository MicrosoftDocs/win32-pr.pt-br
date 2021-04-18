---
title: WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (Wmsdkidl. h)
description: A transição diagonal revela a nova imagem ao longo de uma linha diagonal originada em um canto do quadro.
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6affa3e0727972e66e1ab6584c94ec233a11655
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788082"
---
# <a name="wmt_videoimage_transition_diagonal"></a><span data-ttu-id="94fd4-104">\_diagonal de \_ transição WMT VIDEOIMAGE \_</span><span class="sxs-lookup"><span data-stu-id="94fd4-104">WMT\_VIDEOIMAGE\_TRANSITION\_DIAGONAL</span></span>

<span data-ttu-id="94fd4-105">A transição diagonal revela a nova imagem ao longo de uma linha diagonal originada em um canto do quadro.</span><span class="sxs-lookup"><span data-stu-id="94fd4-105">The diagonal transition reveals the new image along a diagonal line originating in one corner of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="94fd4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94fd4-106">Parameters</span></span>

<span data-ttu-id="94fd4-107">A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="94fd4-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="94fd4-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="94fd4-108">Parameter</span></span></th>
<th><span data-ttu-id="94fd4-109">Membro da estrutura</span><span class="sxs-lookup"><span data-stu-id="94fd4-109">Structure member</span></span></th>
<th><span data-ttu-id="94fd4-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="94fd4-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="94fd4-111">Largura</span><span class="sxs-lookup"><span data-stu-id="94fd4-111">Width</span></span></td>
<td><span data-ttu-id="94fd4-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="94fd4-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="94fd4-113">Largura da seção diagonal em pixels.</span><span class="sxs-lookup"><span data-stu-id="94fd4-113">Width of the diagonal section in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94fd4-114">Altura</span><span class="sxs-lookup"><span data-stu-id="94fd4-114">Height</span></span></td>
<td><span data-ttu-id="94fd4-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="94fd4-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="94fd4-116">Altura da seção diagonal em pixels.</span><span class="sxs-lookup"><span data-stu-id="94fd4-116">Height of the diagonal section in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="94fd4-117">Direção</span><span class="sxs-lookup"><span data-stu-id="94fd4-117">Direction</span></span></td>
<td><span data-ttu-id="94fd4-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="94fd4-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="94fd4-119">Determina o canto do qual a transição se origina. Defina como um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="94fd4-119">Determines the corner from which the transition originates.Set to one of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="94fd4-120">0-superior direito</span><span class="sxs-lookup"><span data-stu-id="94fd4-120">0 - Upper right</span></span></li>
<li><span data-ttu-id="94fd4-121">1-superior esquerdo</span><span class="sxs-lookup"><span data-stu-id="94fd4-121">1 - Upper left</span></span></li>
<li><span data-ttu-id="94fd4-122">2-inferior direito</span><span class="sxs-lookup"><span data-stu-id="94fd4-122">2 - Lower right</span></span></li>
<li><span data-ttu-id="94fd4-123">3-inferior esquerdo</span><span class="sxs-lookup"><span data-stu-id="94fd4-123">3 - Lower left</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94fd4-124">Composição</span><span class="sxs-lookup"><span data-stu-id="94fd4-124">Composition</span></span></td>
<td><span data-ttu-id="94fd4-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="94fd4-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="94fd4-126">Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="94fd4-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="94fd4-127">0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="94fd4-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="94fd4-128">1-especifica a composição invertida, na qual a imagem atual é a imagem de plano de fundo, e a imagem anterior é o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="94fd4-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="94fd4-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94fd4-129">Requirements</span></span>



| <span data-ttu-id="94fd4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="94fd4-130">Requirement</span></span> | <span data-ttu-id="94fd4-131">Valor</span><span class="sxs-lookup"><span data-stu-id="94fd4-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94fd4-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="94fd4-132">Header</span></span><br/> | <dl> <span data-ttu-id="94fd4-133"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="94fd4-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94fd4-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="94fd4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94fd4-135">**Transições de imagem de vídeo**</span><span class="sxs-lookup"><span data-stu-id="94fd4-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





