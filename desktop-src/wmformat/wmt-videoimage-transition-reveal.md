---
title: WMT_VIDEOIMAGE_TRANSITION_REVEAL (Wmsdkidl. h)
description: A transição Reveal revela a nova imagem ao longo de uma linha reta originada de um lado do quadro.
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9aa385912cf106955dd33e06824d0b3668fcd97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751304"
---
# <a name="wmt_videoimage_transition_reveal"></a><span data-ttu-id="2aab2-104">WMT \_ de \_ transição VIDEOIMAGE \_ revela</span><span class="sxs-lookup"><span data-stu-id="2aab2-104">WMT\_VIDEOIMAGE\_TRANSITION\_REVEAL</span></span>

<span data-ttu-id="2aab2-105">A transição Reveal revela a nova imagem ao longo de uma linha reta originada de um lado do quadro.</span><span class="sxs-lookup"><span data-stu-id="2aab2-105">The reveal transition reveals the new image along a straight line originating from one side of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="2aab2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2aab2-106">Parameters</span></span>

<span data-ttu-id="2aab2-107">A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="2aab2-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2aab2-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="2aab2-108">Parameter</span></span></th>
<th><span data-ttu-id="2aab2-109">Membro da estrutura</span><span class="sxs-lookup"><span data-stu-id="2aab2-109">Structure member</span></span></th>
<th><span data-ttu-id="2aab2-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="2aab2-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2aab2-111">Distância</span><span class="sxs-lookup"><span data-stu-id="2aab2-111">Distance</span></span></td>
<td><span data-ttu-id="2aab2-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="2aab2-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="2aab2-113">A quantidade da nova imagem revelada, em pixels.</span><span class="sxs-lookup"><span data-stu-id="2aab2-113">Amount of the new image revealed, in pixels.</span></span> <span data-ttu-id="2aab2-114">Esse valor é relativo ao lado de origem do quadro.</span><span class="sxs-lookup"><span data-stu-id="2aab2-114">This value is relative to the originating side of the frame.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2aab2-115">Direção</span><span class="sxs-lookup"><span data-stu-id="2aab2-115">Direction</span></span></td>
<td><span data-ttu-id="2aab2-116"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="2aab2-116"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="2aab2-117">Direção da revelação. Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="2aab2-117">Direction of the revealing.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="2aab2-118">0-revelar à direita; origine do lado esquerdo do quadro.</span><span class="sxs-lookup"><span data-stu-id="2aab2-118">0 - Reveal to the right; originate from the left side of the frame.</span></span></li>
<li><span data-ttu-id="2aab2-119">1-revelar à esquerda; origine do lado direito do quadro.</span><span class="sxs-lookup"><span data-stu-id="2aab2-119">1 - Reveal to the left; originate from the right side of the frame.</span></span></li>
<li><span data-ttu-id="2aab2-120">2-revelar para cima; originar-se da parte inferior do quadro.</span><span class="sxs-lookup"><span data-stu-id="2aab2-120">2 - Reveal upward; originate from the bottom of the frame.</span></span></li>
<li><span data-ttu-id="2aab2-121">3-revelar para baixo; origine da parte superior do quadro.</span><span class="sxs-lookup"><span data-stu-id="2aab2-121">3 - Reveal downward; originate from the top of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2aab2-122">Composição</span><span class="sxs-lookup"><span data-stu-id="2aab2-122">Composition</span></span></td>
<td><span data-ttu-id="2aab2-123"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="2aab2-123"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="2aab2-124">Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="2aab2-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="2aab2-125">0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="2aab2-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="2aab2-126">1-especifica a composição revertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</span><span class="sxs-lookup"><span data-stu-id="2aab2-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="2aab2-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2aab2-127">Requirements</span></span>



| <span data-ttu-id="2aab2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2aab2-128">Requirement</span></span> | <span data-ttu-id="2aab2-129">Valor</span><span class="sxs-lookup"><span data-stu-id="2aab2-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2aab2-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2aab2-130">Header</span></span><br/> | <dl> <span data-ttu-id="2aab2-131"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2aab2-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2aab2-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="2aab2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aab2-133">**Transições de imagem de vídeo**</span><span class="sxs-lookup"><span data-stu-id="2aab2-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





