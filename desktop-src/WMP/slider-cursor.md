---
title: SLIDER. cursor
description: O atributo cursor especifica ou recupera um valor que indica qual cursor aparece quando o mouse está sobre o controle deslizante.
ms.assetid: 5b96a20c-b3a6-4e08-95b2-32937bb15cc6
keywords:
- Controle deslizante. cursor do Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc8f581d7d087545e666565dd03f649112064d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749401"
---
# <a name="slidercursor"></a><span data-ttu-id="0310a-104">SLIDER. cursor</span><span class="sxs-lookup"><span data-stu-id="0310a-104">SLIDER.cursor</span></span>

<span data-ttu-id="0310a-105">O atributo **cursor** especifica ou recupera um valor que indica qual cursor aparece quando o mouse está sobre o controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="0310a-105">The **cursor** attribute specifies or retrieves a value indicating which cursor appears when the mouse is over the slider control.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="0310a-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="0310a-106">Possible Values</span></span>

<span data-ttu-id="0310a-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0310a-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="0310a-108">Valor</span><span class="sxs-lookup"><span data-stu-id="0310a-108">Value</span></span>            | <span data-ttu-id="0310a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0310a-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0310a-110">sistema</span><span class="sxs-lookup"><span data-stu-id="0310a-110">system</span></span>           | <span data-ttu-id="0310a-111">Cursor dependente de plataforma (geralmente uma seta).</span><span class="sxs-lookup"><span data-stu-id="0310a-111">Platform-dependent cursor (usually an arrow).</span></span>                                               |
| <span data-ttu-id="0310a-112">existentes</span><span class="sxs-lookup"><span data-stu-id="0310a-112">hand</span></span>             | <span data-ttu-id="0310a-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="0310a-113">Default.</span></span> <span data-ttu-id="0310a-114">Existentes.</span><span class="sxs-lookup"><span data-stu-id="0310a-114">Hand.</span></span>                                                                              |
| <span data-ttu-id="0310a-115">ajuda</span><span class="sxs-lookup"><span data-stu-id="0310a-115">help</span></span>             | <span data-ttu-id="0310a-116">Seta com um ponto de interrogação indicando que a ajuda está disponível.</span><span class="sxs-lookup"><span data-stu-id="0310a-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="0310a-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="0310a-117">sizeall</span></span>          | <span data-ttu-id="0310a-118">Seta de quatro pontas apontando para norte, Sul, leste e oeste.</span><span class="sxs-lookup"><span data-stu-id="0310a-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="0310a-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="0310a-119">sizenesw</span></span>         | <span data-ttu-id="0310a-120">Seta de duas pontas apontando para nordeste e sudoeste.</span><span class="sxs-lookup"><span data-stu-id="0310a-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="0310a-121">sizens</span><span class="sxs-lookup"><span data-stu-id="0310a-121">sizens</span></span>           | <span data-ttu-id="0310a-122">Seta de duas pontas apontando para norte e Sul.</span><span class="sxs-lookup"><span data-stu-id="0310a-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="0310a-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="0310a-123">sizenwse</span></span>         | <span data-ttu-id="0310a-124">Seta de duas pontas apontando para noroeste e sudeste.</span><span class="sxs-lookup"><span data-stu-id="0310a-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="0310a-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="0310a-125">sizewe</span></span>           | <span data-ttu-id="0310a-126">Seta de duas pontas apontando para o oeste e o leste.</span><span class="sxs-lookup"><span data-stu-id="0310a-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="0310a-127">upseta</span><span class="sxs-lookup"><span data-stu-id="0310a-127">uparrow</span></span>          | <span data-ttu-id="0310a-128">Seta vertical apontando para cima.</span><span class="sxs-lookup"><span data-stu-id="0310a-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="0310a-129">\*. ani ou \* . cur</span><span class="sxs-lookup"><span data-stu-id="0310a-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="0310a-130">Qualquer arquivo. ani ou. cur (deve estar no mesmo diretório que o arquivo. WMS ou no arquivo. wmz).</span><span class="sxs-lookup"><span data-stu-id="0310a-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0310a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0310a-131">Requirements</span></span>



| <span data-ttu-id="0310a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0310a-132">Requirement</span></span> | <span data-ttu-id="0310a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="0310a-133">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0310a-134">Versão</span><span class="sxs-lookup"><span data-stu-id="0310a-134">Version</span></span><br/> | <span data-ttu-id="0310a-135">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="0310a-135">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0310a-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="0310a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0310a-137">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="0310a-137">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 





