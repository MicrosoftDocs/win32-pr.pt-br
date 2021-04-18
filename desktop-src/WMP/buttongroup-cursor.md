---
title: BOTÃO. cursor
description: O atributo cursor especifica ou recupera o tipo de cursor que aparece quando o mouse está sobre um botão no botão.
ms.assetid: c1b7e3e1-862b-48c1-bd2d-d9abd9ada14c
keywords:
- BOTÃO. cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b3de12950aed383f48dcde5d8978724037f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760462"
---
# <a name="buttongroupcursor"></a><span data-ttu-id="0a5df-104">BOTÃO. cursor</span><span class="sxs-lookup"><span data-stu-id="0a5df-104">BUTTONGROUP.cursor</span></span>

<span data-ttu-id="0a5df-105">O atributo **cursor** especifica ou recupera o tipo de cursor que aparece quando o mouse está sobre um botão no **botão**.</span><span class="sxs-lookup"><span data-stu-id="0a5df-105">The **cursor** attribute specifies or retrieves the type of cursor that appears when the mouse is over a button in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="0a5df-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="0a5df-106">Possible Values</span></span>

<span data-ttu-id="0a5df-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a5df-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="0a5df-108">Valor</span><span class="sxs-lookup"><span data-stu-id="0a5df-108">Value</span></span>            | <span data-ttu-id="0a5df-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a5df-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a5df-110">sistema</span><span class="sxs-lookup"><span data-stu-id="0a5df-110">system</span></span>           | <span data-ttu-id="0a5df-111">Padrão.</span><span class="sxs-lookup"><span data-stu-id="0a5df-111">Default.</span></span> <span data-ttu-id="0a5df-112">Cursor dependente de plataforma (geralmente uma seta).</span><span class="sxs-lookup"><span data-stu-id="0a5df-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="0a5df-113">existentes</span><span class="sxs-lookup"><span data-stu-id="0a5df-113">hand</span></span>             | <span data-ttu-id="0a5df-114">Existentes.</span><span class="sxs-lookup"><span data-stu-id="0a5df-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="0a5df-115">ajuda</span><span class="sxs-lookup"><span data-stu-id="0a5df-115">help</span></span>             | <span data-ttu-id="0a5df-116">Seta com um ponto de interrogação indicando que a ajuda está disponível.</span><span class="sxs-lookup"><span data-stu-id="0a5df-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="0a5df-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="0a5df-117">sizeall</span></span>          | <span data-ttu-id="0a5df-118">Seta de quatro pontas apontando para norte, Sul, leste e oeste.</span><span class="sxs-lookup"><span data-stu-id="0a5df-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="0a5df-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="0a5df-119">sizenesw</span></span>         | <span data-ttu-id="0a5df-120">Seta de duas pontas apontando para nordeste e sudoeste.</span><span class="sxs-lookup"><span data-stu-id="0a5df-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="0a5df-121">sizens</span><span class="sxs-lookup"><span data-stu-id="0a5df-121">sizens</span></span>           | <span data-ttu-id="0a5df-122">Seta de duas pontas apontando para norte e Sul.</span><span class="sxs-lookup"><span data-stu-id="0a5df-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="0a5df-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="0a5df-123">sizenwse</span></span>         | <span data-ttu-id="0a5df-124">Seta de duas pontas apontando para noroeste e sudeste.</span><span class="sxs-lookup"><span data-stu-id="0a5df-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="0a5df-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="0a5df-125">sizewe</span></span>           | <span data-ttu-id="0a5df-126">Seta de duas pontas apontando para o oeste e o leste.</span><span class="sxs-lookup"><span data-stu-id="0a5df-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="0a5df-127">upseta</span><span class="sxs-lookup"><span data-stu-id="0a5df-127">uparrow</span></span>          | <span data-ttu-id="0a5df-128">Seta vertical apontando para cima.</span><span class="sxs-lookup"><span data-stu-id="0a5df-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="0a5df-129">\*. ani ou \* . cur</span><span class="sxs-lookup"><span data-stu-id="0a5df-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="0a5df-130">Qualquer arquivo. ani ou. cur (deve estar no mesmo diretório que o arquivo. WMS ou no arquivo. wmz).</span><span class="sxs-lookup"><span data-stu-id="0a5df-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0a5df-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a5df-131">Remarks</span></span>

<span data-ttu-id="0a5df-132">O cursor especificado se aplica a todos os botões do **botão**.</span><span class="sxs-lookup"><span data-stu-id="0a5df-132">The cursor specified applies to all buttons in the **BUTTONGROUP**.</span></span>

<span data-ttu-id="0a5df-133">Se você especificar um valor de cursor inválido, ele permanecerá no valor definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="0a5df-133">If you specify an invalid cursor value, it remains at the previously set value.</span></span>

<span data-ttu-id="0a5df-134">Os caminhos de nome de arquivo de cursor são ignorados, portanto, o arquivo de cursor deve residir no diretório padrão.</span><span class="sxs-lookup"><span data-stu-id="0a5df-134">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a5df-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a5df-135">Requirements</span></span>



| <span data-ttu-id="0a5df-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a5df-136">Requirement</span></span> | <span data-ttu-id="0a5df-137">Valor</span><span class="sxs-lookup"><span data-stu-id="0a5df-137">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0a5df-138">Versão</span><span class="sxs-lookup"><span data-stu-id="0a5df-138">Version</span></span><br/> | <span data-ttu-id="0a5df-139">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="0a5df-139">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a5df-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a5df-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a5df-141">**Elemento de botão**</span><span class="sxs-lookup"><span data-stu-id="0a5df-141">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> </dl>

 

 





