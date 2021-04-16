---
title: WMT_VIDEOIMAGE_TRANSITION_IRIS (Wmsdkidl. h)
description: A transição íris revela a nova imagem ao longo de um eixo x e um eixo y. O efeito visual dessa transição é que a nova imagem aparece em um alcance cruzado ampliando para todos os lados do quadro.
ms.assetid: 7390d959-a566-43e7-937d-1e617bc98a6e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_IRIS o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_IRIS
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd216c7387f850f317417717c50216dd63449843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750080"
---
# <a name="wmt_videoimage_transition_iris"></a><span data-ttu-id="1c87f-105">\_íris de \_ transição WMT VIDEOIMAGE \_</span><span class="sxs-lookup"><span data-stu-id="1c87f-105">WMT\_VIDEOIMAGE\_TRANSITION\_IRIS</span></span>

<span data-ttu-id="1c87f-106">A transição íris revela a nova imagem ao longo de um eixo x e um eixo y.</span><span class="sxs-lookup"><span data-stu-id="1c87f-106">The iris transition reveals the new image along an x-axis and a y-axis.</span></span> <span data-ttu-id="1c87f-107">O efeito visual dessa transição é que a nova imagem aparece em um alcance cruzado ampliando para todos os lados do quadro.</span><span class="sxs-lookup"><span data-stu-id="1c87f-107">The visual effect of this transition is that the new image appears in a widening cross reaching to all sides of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="1c87f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c87f-108">Parameters</span></span>

<span data-ttu-id="1c87f-109">A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="1c87f-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c87f-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="1c87f-110">Parameter</span></span></th>
<th><span data-ttu-id="1c87f-111">Membro da estrutura</span><span class="sxs-lookup"><span data-stu-id="1c87f-111">Structure member</span></span></th>
<th><span data-ttu-id="1c87f-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c87f-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c87f-113">X central</span><span class="sxs-lookup"><span data-stu-id="1c87f-113">Center X</span></span></td>
<td><span data-ttu-id="1c87f-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="1c87f-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="1c87f-115">Coordenada X, em relação ao quadro de vídeo, do centro do efeito de íris.</span><span class="sxs-lookup"><span data-stu-id="1c87f-115">X-coordinate, relative to the video frame, of the center of the iris effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c87f-116">Y central</span><span class="sxs-lookup"><span data-stu-id="1c87f-116">Center Y</span></span></td>
<td><span data-ttu-id="1c87f-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="1c87f-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="1c87f-118">Coordenada Y, em relação ao quadro de vídeo, do centro do efeito de íris.</span><span class="sxs-lookup"><span data-stu-id="1c87f-118">Y-coordinate, relative to the video frame, of the center of the iris effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c87f-119">Largura</span><span class="sxs-lookup"><span data-stu-id="1c87f-119">Width</span></span></td>
<td><span data-ttu-id="1c87f-120"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="1c87f-120"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="1c87f-121">Largura da linha vertical que revela a nova imagem, em pixels.</span><span class="sxs-lookup"><span data-stu-id="1c87f-121">Width of the vertical line revealing the new image, in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c87f-122">Altura</span><span class="sxs-lookup"><span data-stu-id="1c87f-122">Height</span></span></td>
<td><span data-ttu-id="1c87f-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="1c87f-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="1c87f-124">Altura da linha horizontal que revela a nova imagem, em pixels.</span><span class="sxs-lookup"><span data-stu-id="1c87f-124">Height of the horizontal line revealing the new image, in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c87f-125">Composição</span><span class="sxs-lookup"><span data-stu-id="1c87f-125">Composition</span></span></td>
<td><span data-ttu-id="1c87f-126"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="1c87f-126"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="1c87f-127">Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="1c87f-127">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="1c87f-128">0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="1c87f-128">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="1c87f-129">1-especifica a composição revertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</span><span class="sxs-lookup"><span data-stu-id="1c87f-129">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="1c87f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c87f-130">Requirements</span></span>



| <span data-ttu-id="1c87f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c87f-131">Requirement</span></span> | <span data-ttu-id="1c87f-132">Valor</span><span class="sxs-lookup"><span data-stu-id="1c87f-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c87f-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1c87f-133">Header</span></span><br/> | <dl> <span data-ttu-id="1c87f-134"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c87f-134"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c87f-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c87f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c87f-136">**Transições de imagem de vídeo**</span><span class="sxs-lookup"><span data-stu-id="1c87f-136">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





