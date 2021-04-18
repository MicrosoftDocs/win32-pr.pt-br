---
title: WMT_VIDEOIMAGE_TRANSITION_DIAMOND (Wmsdkidl. h)
description: A transição de losango revela a nova imagem em um losango.
ms.assetid: ff36a64d-62f7-424d-acc9-a7902926a90c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAMOND o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAMOND
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e3abfa337edd58fc536e530eb0ff6473c9a9d28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813218"
---
# <a name="wmt_videoimage_transition_diamond"></a><span data-ttu-id="1dd71-104">\_diamante de \_ transição WMT VIDEOIMAGE \_</span><span class="sxs-lookup"><span data-stu-id="1dd71-104">WMT\_VIDEOIMAGE\_TRANSITION\_DIAMOND</span></span>

<span data-ttu-id="1dd71-105">A transição de losango revela a nova imagem em um losango.</span><span class="sxs-lookup"><span data-stu-id="1dd71-105">The diamond transition reveals the new image in a diamond.</span></span>

## <a name="parameters"></a><span data-ttu-id="1dd71-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1dd71-106">Parameters</span></span>

<span data-ttu-id="1dd71-107">A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="1dd71-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1dd71-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="1dd71-108">Parameter</span></span></th>
<th><span data-ttu-id="1dd71-109">Membro da estrutura</span><span class="sxs-lookup"><span data-stu-id="1dd71-109">Structure member</span></span></th>
<th><span data-ttu-id="1dd71-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="1dd71-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1dd71-111">X central</span><span class="sxs-lookup"><span data-stu-id="1dd71-111">Center X</span></span></td>
<td><span data-ttu-id="1dd71-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="1dd71-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="1dd71-113">Coordenada X, relativa ao quadro de vídeo, do centro do losango.</span><span class="sxs-lookup"><span data-stu-id="1dd71-113">X-coordinate, relative to the video frame, of the center of the diamond.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1dd71-114">Y central</span><span class="sxs-lookup"><span data-stu-id="1dd71-114">Center Y</span></span></td>
<td><span data-ttu-id="1dd71-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="1dd71-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="1dd71-116">Coordenada Y, relativa ao quadro de vídeo, do centro do losango.</span><span class="sxs-lookup"><span data-stu-id="1dd71-116">Y-coordinate, relative to the video frame, of the center of the diamond.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1dd71-117">Largura</span><span class="sxs-lookup"><span data-stu-id="1dd71-117">Width</span></span></td>
<td><span data-ttu-id="1dd71-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="1dd71-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="1dd71-119">Largura do losango em pixels.</span><span class="sxs-lookup"><span data-stu-id="1dd71-119">Width of the diamond in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1dd71-120">Altura</span><span class="sxs-lookup"><span data-stu-id="1dd71-120">Height</span></span></td>
<td><span data-ttu-id="1dd71-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="1dd71-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="1dd71-122">Altura do losango em pixels.</span><span class="sxs-lookup"><span data-stu-id="1dd71-122">Height of the diamond in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1dd71-123">Composição</span><span class="sxs-lookup"><span data-stu-id="1dd71-123">Composition</span></span></td>
<td><span data-ttu-id="1dd71-124"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="1dd71-124"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="1dd71-125">Defina como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="1dd71-125">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="1dd71-126">0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="1dd71-126">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="1dd71-127">1-especifica a composição revertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</span><span class="sxs-lookup"><span data-stu-id="1dd71-127">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="1dd71-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dd71-128">Requirements</span></span>



| <span data-ttu-id="1dd71-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dd71-129">Requirement</span></span> | <span data-ttu-id="1dd71-130">Valor</span><span class="sxs-lookup"><span data-stu-id="1dd71-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd71-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1dd71-131">Header</span></span><br/> | <dl> <span data-ttu-id="1dd71-132"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dd71-132"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dd71-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="1dd71-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dd71-134">**Transições de imagem de vídeo**</span><span class="sxs-lookup"><span data-stu-id="1dd71-134">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





