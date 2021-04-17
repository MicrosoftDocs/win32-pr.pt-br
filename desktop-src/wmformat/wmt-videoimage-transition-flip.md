---
title: WMT_VIDEOIMAGE_TRANSITION_FLIP (Wmsdkidl. h)
description: A transição de flip gira a imagem antiga em um eixo y por meio do centro do quadro. A nova imagem é revelada como a parte traseira da imagem antiga.
ms.assetid: ff9990ef-962c-4dbb-b2bc-3bee070d2044
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FLIP o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FLIP
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc92ad1dfffd945b89293dd9207289aa47645d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752732"
---
# <a name="wmt_videoimage_transition_flip"></a><span data-ttu-id="1ba56-105">Inverter WMT de \_ \_ transição VIDEOIMAGE \_</span><span class="sxs-lookup"><span data-stu-id="1ba56-105">WMT\_VIDEOIMAGE\_TRANSITION\_FLIP</span></span>

<span data-ttu-id="1ba56-106">A transição de flip gira a imagem antiga em um eixo y por meio do centro do quadro.</span><span class="sxs-lookup"><span data-stu-id="1ba56-106">The flip transition rotates the old image on a y-axis through the center of the frame.</span></span> <span data-ttu-id="1ba56-107">A nova imagem é revelada como a parte traseira da imagem antiga.</span><span class="sxs-lookup"><span data-stu-id="1ba56-107">The new image is revealed as the back of the old image.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ba56-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ba56-108">Parameters</span></span>

<span data-ttu-id="1ba56-109">A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="1ba56-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1ba56-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ba56-110">Parameter</span></span></th>
<th><span data-ttu-id="1ba56-111">Membro da estrutura</span><span class="sxs-lookup"><span data-stu-id="1ba56-111">Structure member</span></span></th>
<th><span data-ttu-id="1ba56-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ba56-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1ba56-113">Ângulo</span><span class="sxs-lookup"><span data-stu-id="1ba56-113">Angle</span></span></td>
<td><span data-ttu-id="1ba56-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="1ba56-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="1ba56-115">Ângulo da rotação, de 0,0 a 180,0 graus.</span><span class="sxs-lookup"><span data-stu-id="1ba56-115">Angle of the rotation, from 0.0 to 180.0 degrees.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ba56-116">Composição</span><span class="sxs-lookup"><span data-stu-id="1ba56-116">Composition</span></span></td>
<td><span data-ttu-id="1ba56-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="1ba56-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="1ba56-118">Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="1ba56-118">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="1ba56-119">0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="1ba56-119">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="1ba56-120">1-especifica a composição revertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</span><span class="sxs-lookup"><span data-stu-id="1ba56-120">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="1ba56-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ba56-121">Remarks</span></span>

<span data-ttu-id="1ba56-122">Você pode visualizar o efeito dessa transição como se ambas as imagens fossem fotos físicas coladas de volta para trás.</span><span class="sxs-lookup"><span data-stu-id="1ba56-122">You can visualize the effect of this transition as if both images were physical photographs glued together back-to-back.</span></span> <span data-ttu-id="1ba56-123">A transição tem o mesmo efeito que conter duas fotografias no centro da borda inferior e girando-as 180 graus.</span><span class="sxs-lookup"><span data-stu-id="1ba56-123">The transition has the same effect as holding two such photographs at the center of the bottom edge and rotating them 180 degrees.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ba56-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ba56-124">Requirements</span></span>



| <span data-ttu-id="1ba56-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ba56-125">Requirement</span></span> | <span data-ttu-id="1ba56-126">Valor</span><span class="sxs-lookup"><span data-stu-id="1ba56-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ba56-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ba56-127">Header</span></span><br/> | <dl> <span data-ttu-id="1ba56-128"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ba56-128"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ba56-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ba56-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ba56-130">**Transições de imagem de vídeo**</span><span class="sxs-lookup"><span data-stu-id="1ba56-130">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





