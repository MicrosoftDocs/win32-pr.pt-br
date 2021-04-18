---
title: BOTÃO. cursor
description: O atributo cursor especifica ou recupera o cursor que aparece quando o ponteiro do mouse passa sobre o botão.
ms.assetid: 19bdbb23-00e2-45cf-b67d-9ada036b9c3b
keywords:
- BOTÃO. cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2641491a5a73498da2c43fd74d4187b5594e177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760464"
---
# <a name="buttoncursor"></a><span data-ttu-id="4c7b7-104">BOTÃO. cursor</span><span class="sxs-lookup"><span data-stu-id="4c7b7-104">BUTTON.cursor</span></span>

<span data-ttu-id="4c7b7-105">O atributo **cursor** especifica ou recupera o cursor que aparece quando o ponteiro do mouse passa sobre o **botão**.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-105">The **cursor** attribute specifies or retrieves the cursor that appears when the mouse pointer hovers over the **BUTTON**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="4c7b7-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="4c7b7-106">Possible Values</span></span>

<span data-ttu-id="4c7b7-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="4c7b7-108">Valor</span><span class="sxs-lookup"><span data-stu-id="4c7b7-108">Value</span></span>            | <span data-ttu-id="4c7b7-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c7b7-109">Description</span></span>                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c7b7-110">sistema</span><span class="sxs-lookup"><span data-stu-id="4c7b7-110">system</span></span>           | <span data-ttu-id="4c7b7-111">Padrão.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-111">Default.</span></span> <span data-ttu-id="4c7b7-112">Cursor dependente de plataforma (geralmente uma seta).</span><span class="sxs-lookup"><span data-stu-id="4c7b7-112">Platform-dependent cursor (usually an arrow).</span></span>                                     |
| <span data-ttu-id="4c7b7-113">existentes</span><span class="sxs-lookup"><span data-stu-id="4c7b7-113">hand</span></span>             | <span data-ttu-id="4c7b7-114">Existentes.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-114">Hand.</span></span>                                                                                      |
| <span data-ttu-id="4c7b7-115">ajuda</span><span class="sxs-lookup"><span data-stu-id="4c7b7-115">help</span></span>             | <span data-ttu-id="4c7b7-116">Seta com um ponto de interrogação indicando que a ajuda está disponível.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-116">Arrow with question mark indicating Help is available.</span></span>                                     |
| <span data-ttu-id="4c7b7-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="4c7b7-117">sizeall</span></span>          | <span data-ttu-id="4c7b7-118">Seta de quatro pontas apontando para norte, Sul, leste e oeste.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                  |
| <span data-ttu-id="4c7b7-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="4c7b7-119">sizenesw</span></span>         | <span data-ttu-id="4c7b7-120">Seta de duas pontas apontando para nordeste e sudoeste.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                     |
| <span data-ttu-id="4c7b7-121">sizens</span><span class="sxs-lookup"><span data-stu-id="4c7b7-121">sizens</span></span>           | <span data-ttu-id="4c7b7-122">Seta de duas pontas apontando para norte e Sul.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-122">Double-pointed arrow pointing north and south.</span></span>                                             |
| <span data-ttu-id="4c7b7-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="4c7b7-123">sizenwse</span></span>         | <span data-ttu-id="4c7b7-124">Seta de duas pontas apontando para noroeste e sudeste.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                     |
| <span data-ttu-id="4c7b7-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="4c7b7-125">sizewe</span></span>           | <span data-ttu-id="4c7b7-126">Seta de duas pontas apontando para o oeste e o leste.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-126">Double-pointed arrow pointing west and east.</span></span>                                               |
| <span data-ttu-id="4c7b7-127">upseta</span><span class="sxs-lookup"><span data-stu-id="4c7b7-127">uparrow</span></span>          | <span data-ttu-id="4c7b7-128">Seta vertical apontando para cima.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-128">Vertical arrow pointing upward.</span></span>                                                            |
| <span data-ttu-id="4c7b7-129">\*. ani ou \* . cur</span><span class="sxs-lookup"><span data-stu-id="4c7b7-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="4c7b7-130">Qualquer arquivo. ani ou. cur (deve estar no mesmo diretório que o arquivo. WMS ou no arquivo. wmz)</span><span class="sxs-lookup"><span data-stu-id="4c7b7-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4c7b7-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c7b7-131">Remarks</span></span>

<span data-ttu-id="4c7b7-132">Se o sistema não reconhecer o valor do cursor especificado, o valor do cursor permanecerá no valor definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-132">If the system does not recognize the cursor value specified, the cursor value remains at the previously set value.</span></span>

<span data-ttu-id="4c7b7-133">Os caminhos de nome de arquivo de cursor são ignorados, portanto, o arquivo de cursor deve residir no diretório padrão.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-133">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c7b7-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c7b7-134">Requirements</span></span>



| <span data-ttu-id="4c7b7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c7b7-135">Requirement</span></span> | <span data-ttu-id="4c7b7-136">Valor</span><span class="sxs-lookup"><span data-stu-id="4c7b7-136">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4c7b7-137">Versão</span><span class="sxs-lookup"><span data-stu-id="4c7b7-137">Version</span></span><br/> | <span data-ttu-id="4c7b7-138">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="4c7b7-138">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4c7b7-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c7b7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c7b7-140">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="4c7b7-140">**BUTTON Element**</span></span>](button-element.md)
</dt> </dl>

 

 





