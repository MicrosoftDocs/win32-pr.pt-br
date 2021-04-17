---
title: VÍDEO. cursor
description: O atributo cursor especifica ou recupera o valor do cursor que é usado quando o mouse está sobre uma área clicável do vídeo.
ms.assetid: 2faaf9cd-47be-47d5-ad4e-8f3bb322d812
keywords:
- VÍDEO. cursor Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c23ab90b974ad5a7f9cfaf9fcc598371cd0697f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762437"
---
# <a name="videocursor"></a><span data-ttu-id="c6c5b-104">VÍDEO. cursor</span><span class="sxs-lookup"><span data-stu-id="c6c5b-104">VIDEO.cursor</span></span>

<span data-ttu-id="c6c5b-105">O atributo **cursor** especifica ou recupera o valor do cursor que é usado quando o mouse está sobre uma área clicável do vídeo.</span><span class="sxs-lookup"><span data-stu-id="c6c5b-105">The **cursor** attribute specifies or retrieves the cursor value that is used when the mouse is over a clickable area of the video.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="c6c5b-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="c6c5b-106">Possible Values</span></span>

<span data-ttu-id="c6c5b-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c6c5b-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="c6c5b-108">Valor</span><span class="sxs-lookup"><span data-stu-id="c6c5b-108">Value</span></span>            | <span data-ttu-id="c6c5b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6c5b-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c5b-110">sistema</span><span class="sxs-lookup"><span data-stu-id="c6c5b-110">system</span></span>           | <span data-ttu-id="c6c5b-111">Cursor dependente de plataforma (geralmente uma seta).</span><span class="sxs-lookup"><span data-stu-id="c6c5b-111">Platform-dependent cursor (usually an arrow).</span></span>                                               |
| <span data-ttu-id="c6c5b-112">existentes</span><span class="sxs-lookup"><span data-stu-id="c6c5b-112">hand</span></span>             | <span data-ttu-id="c6c5b-113">Existentes.</span><span class="sxs-lookup"><span data-stu-id="c6c5b-113">Hand.</span></span>                                                                                       |
| <span data-ttu-id="c6c5b-114">ajuda</span><span class="sxs-lookup"><span data-stu-id="c6c5b-114">help</span></span>             | <span data-ttu-id="c6c5b-115">Seta com um ponto de interrogação indicando que a ajuda está disponível.</span><span class="sxs-lookup"><span data-stu-id="c6c5b-115">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="c6c5b-116">sizeall</span><span class="sxs-lookup"><span data-stu-id="c6c5b-116">sizeall</span></span>          | <span data-ttu-id="c6c5b-117">Seta de quatro pontas apontando para norte, Sul, leste e oeste.</span><span class="sxs-lookup"><span data-stu-id="c6c5b-117">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="c6c5b-118">sizenesw</span><span class="sxs-lookup"><span data-stu-id="c6c5b-118">sizenesw</span></span>         | <span data-ttu-id="c6c5b-119">Seta de duas pontas apontando para nordeste e sudoeste.</span><span class="sxs-lookup"><span data-stu-id="c6c5b-119">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="c6c5b-120">sizens</span><span class="sxs-lookup"><span data-stu-id="c6c5b-120">sizens</span></span>           | <span data-ttu-id="c6c5b-121">Seta de duas pontas apontando para norte e Sul.</span><span class="sxs-lookup"><span data-stu-id="c6c5b-121">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="c6c5b-122">sizenwse</span><span class="sxs-lookup"><span data-stu-id="c6c5b-122">sizenwse</span></span>         | <span data-ttu-id="c6c5b-123">Seta de duas pontas apontando para noroeste e sudeste.</span><span class="sxs-lookup"><span data-stu-id="c6c5b-123">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="c6c5b-124">sizewe</span><span class="sxs-lookup"><span data-stu-id="c6c5b-124">sizewe</span></span>           | <span data-ttu-id="c6c5b-125">Seta de duas pontas apontando para o oeste e o leste.</span><span class="sxs-lookup"><span data-stu-id="c6c5b-125">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="c6c5b-126">upseta</span><span class="sxs-lookup"><span data-stu-id="c6c5b-126">uparrow</span></span>          | <span data-ttu-id="c6c5b-127">Seta vertical apontando para cima.</span><span class="sxs-lookup"><span data-stu-id="c6c5b-127">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="c6c5b-128">\*. ani ou \* . cur</span><span class="sxs-lookup"><span data-stu-id="c6c5b-128">\*.ani or \*.cur</span></span> | <span data-ttu-id="c6c5b-129">Qualquer arquivo. ani ou. cur (deve estar no mesmo diretório que o arquivo. WMS ou no arquivo. wmz).</span><span class="sxs-lookup"><span data-stu-id="c6c5b-129">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c6c5b-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6c5b-130">Remarks</span></span>

<span data-ttu-id="c6c5b-131">Para fins de renderização, o sistema é o cursor padrão.</span><span class="sxs-lookup"><span data-stu-id="c6c5b-131">For rendering purposes, system is the default cursor.</span></span> <span data-ttu-id="c6c5b-132">O valor padrão recuperado desse atributo é "" (cadeia de caracteres vazia).</span><span class="sxs-lookup"><span data-stu-id="c6c5b-132">The default value retrieved from this attribute is "" (empty string).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6c5b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6c5b-133">Requirements</span></span>



| <span data-ttu-id="c6c5b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6c5b-134">Requirement</span></span> | <span data-ttu-id="c6c5b-135">Valor</span><span class="sxs-lookup"><span data-stu-id="c6c5b-135">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c6c5b-136">Versão</span><span class="sxs-lookup"><span data-stu-id="c6c5b-136">Version</span></span><br/> | <span data-ttu-id="c6c5b-137">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c6c5b-137">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6c5b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6c5b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c5b-139">**Elemento VIDEO**</span><span class="sxs-lookup"><span data-stu-id="c6c5b-139">**VIDEO Element**</span></span>](video-element.md)
</dt> </dl>

 

 





