---
title: WMT_VIDEOIMAGE_TRANSITION_BOW_TIE (Wmsdkidl. h)
description: A transição de gravata de arco revela a nova imagem em um conjunto de triângulos nos lados opostos do quadro.
ms.assetid: d98da767-eea7-460c-ae5f-6bef9d93ad9d
keywords:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd4d426c335a30853085a2501206ccd6e7efc7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766282"
---
# <a name="wmt_videoimage_transition_bow_tie"></a><span data-ttu-id="6968d-104">gravata WMT de \_ transição de VIDEOIMAGE \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6968d-104">WMT\_VIDEOIMAGE\_TRANSITION\_BOW\_TIE</span></span>

<span data-ttu-id="6968d-105">A transição de gravata de arco revela a nova imagem em um conjunto de triângulos nos lados opostos do quadro.</span><span class="sxs-lookup"><span data-stu-id="6968d-105">The bow tie transition reveals the new image in a set of triangles on opposite sides of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="6968d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6968d-106">Parameters</span></span>

<span data-ttu-id="6968d-107">A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="6968d-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6968d-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="6968d-108">Parameter</span></span></th>
<th><span data-ttu-id="6968d-109">Membro da estrutura</span><span class="sxs-lookup"><span data-stu-id="6968d-109">Structure member</span></span></th>
<th><span data-ttu-id="6968d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6968d-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6968d-111">Largura</span><span class="sxs-lookup"><span data-stu-id="6968d-111">Width</span></span></td>
<td><span data-ttu-id="6968d-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="6968d-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="6968d-113">Largura de cada lado triangular do gravata de arco.</span><span class="sxs-lookup"><span data-stu-id="6968d-113">Width of each triangular side of the bow tie.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6968d-114">Altura</span><span class="sxs-lookup"><span data-stu-id="6968d-114">Height</span></span></td>
<td><span data-ttu-id="6968d-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="6968d-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="6968d-116">Altura de cada lado triangular da gravata de curva.</span><span class="sxs-lookup"><span data-stu-id="6968d-116">Height of each triangular side of the bow tie.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6968d-117">Direção</span><span class="sxs-lookup"><span data-stu-id="6968d-117">Direction</span></span></td>
<td><span data-ttu-id="6968d-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="6968d-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="6968d-119">Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="6968d-119">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="6968d-120">0-especifica o efeito de vínculo de arco horizontal, no qual os triângulos entram nos lados direito e esquerdo do quadro.</span><span class="sxs-lookup"><span data-stu-id="6968d-120">0 - Specifies horizontal bow tie effect, in which the triangles enter from the right and left sides of the frame.</span></span></li>
<li><span data-ttu-id="6968d-121">1-especifica o efeito de vínculo de arco vertical, no qual os triângulos entram na parte superior e inferior do quadro.</span><span class="sxs-lookup"><span data-stu-id="6968d-121">1 - Specifies vertical bow tie effect, in which the triangles enter from the top and bottom of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6968d-122">Composição</span><span class="sxs-lookup"><span data-stu-id="6968d-122">Composition</span></span></td>
<td><span data-ttu-id="6968d-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="6968d-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="6968d-124">Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="6968d-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="6968d-125">0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="6968d-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="6968d-126">1-especifica a composição invertida, na qual a imagem atual é a imagem de plano de fundo, e a imagem anterior é o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="6968d-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="6968d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6968d-127">Requirements</span></span>



| <span data-ttu-id="6968d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6968d-128">Requirement</span></span> | <span data-ttu-id="6968d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6968d-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6968d-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6968d-130">Header</span></span><br/> | <dl> <span data-ttu-id="6968d-131"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6968d-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6968d-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="6968d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6968d-133">**Transições de imagem de vídeo**</span><span class="sxs-lookup"><span data-stu-id="6968d-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





