---
title: BUTTONelement. cursor
description: O atributo cursor especifica ou recupera o valor do cursor BUTTONelement que aparece quando o mouse está sobre o BOTÃOelement.
ms.assetid: 29e7fadb-30d8-40e4-9a64-6b6f45eac80a
keywords:
- BUTTONelement. cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f267cd54c36ad8f89a7242d7f428fd0d52b75fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783626"
---
# <a name="buttonelementcursor"></a><span data-ttu-id="751d9-104">BUTTONelement. cursor</span><span class="sxs-lookup"><span data-stu-id="751d9-104">BUTTONELEMENT.cursor</span></span>

<span data-ttu-id="751d9-105">O atributo **cursor** especifica ou recupera o valor do cursor **buttonelement** que aparece quando o mouse está sobre o **botãoelement**.</span><span class="sxs-lookup"><span data-stu-id="751d9-105">The **cursor** attribute specifies or retrieves the value of the **BUTTONELEMENT** cursor that appears when the mouse is over the **BUTTONELEMENT**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="751d9-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="751d9-106">Possible Values</span></span>

<span data-ttu-id="751d9-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="751d9-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="751d9-108">Valor</span><span class="sxs-lookup"><span data-stu-id="751d9-108">Value</span></span>            | <span data-ttu-id="751d9-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="751d9-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="751d9-110">sistema</span><span class="sxs-lookup"><span data-stu-id="751d9-110">system</span></span>           | <span data-ttu-id="751d9-111">Padrão.</span><span class="sxs-lookup"><span data-stu-id="751d9-111">Default.</span></span> <span data-ttu-id="751d9-112">Cursor dependente de plataforma (geralmente uma seta).</span><span class="sxs-lookup"><span data-stu-id="751d9-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="751d9-113">existentes</span><span class="sxs-lookup"><span data-stu-id="751d9-113">hand</span></span>             | <span data-ttu-id="751d9-114">Existentes.</span><span class="sxs-lookup"><span data-stu-id="751d9-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="751d9-115">ajuda</span><span class="sxs-lookup"><span data-stu-id="751d9-115">help</span></span>             | <span data-ttu-id="751d9-116">Seta com um ponto de interrogação indicando que a ajuda está disponível.</span><span class="sxs-lookup"><span data-stu-id="751d9-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="751d9-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="751d9-117">sizeall</span></span>          | <span data-ttu-id="751d9-118">Seta de quatro pontas apontando para norte, Sul, leste e oeste.</span><span class="sxs-lookup"><span data-stu-id="751d9-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="751d9-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="751d9-119">sizenesw</span></span>         | <span data-ttu-id="751d9-120">Seta de duas pontas apontando para nordeste e sudoeste.</span><span class="sxs-lookup"><span data-stu-id="751d9-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="751d9-121">sizens</span><span class="sxs-lookup"><span data-stu-id="751d9-121">sizens</span></span>           | <span data-ttu-id="751d9-122">Seta de duas pontas apontando para norte e Sul.</span><span class="sxs-lookup"><span data-stu-id="751d9-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="751d9-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="751d9-123">sizenwse</span></span>         | <span data-ttu-id="751d9-124">Seta de duas pontas apontando para noroeste e sudeste.</span><span class="sxs-lookup"><span data-stu-id="751d9-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="751d9-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="751d9-125">sizewe</span></span>           | <span data-ttu-id="751d9-126">Seta de duas pontas apontando para o oeste e o leste.</span><span class="sxs-lookup"><span data-stu-id="751d9-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="751d9-127">upseta</span><span class="sxs-lookup"><span data-stu-id="751d9-127">uparrow</span></span>          | <span data-ttu-id="751d9-128">Seta vertical apontando para cima.</span><span class="sxs-lookup"><span data-stu-id="751d9-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="751d9-129">\*. ani ou \* . cur</span><span class="sxs-lookup"><span data-stu-id="751d9-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="751d9-130">Qualquer arquivo. ani ou. cur (deve estar no mesmo diretório que o arquivo. WMS ou no arquivo. wmz).</span><span class="sxs-lookup"><span data-stu-id="751d9-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="751d9-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="751d9-131">Remarks</span></span>

<span data-ttu-id="751d9-132">Se um valor inválido for especificado, o valor anterior será mantido.</span><span class="sxs-lookup"><span data-stu-id="751d9-132">If an invalid value is specified, the previous value is maintained.</span></span>

<span data-ttu-id="751d9-133">Os caminhos de nome de arquivo de cursor são ignorados, portanto, o arquivo de cursor deve residir no diretório padrão.</span><span class="sxs-lookup"><span data-stu-id="751d9-133">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="751d9-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="751d9-134">Requirements</span></span>



| <span data-ttu-id="751d9-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="751d9-135">Requirement</span></span> | <span data-ttu-id="751d9-136">Valor</span><span class="sxs-lookup"><span data-stu-id="751d9-136">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="751d9-137">Versão</span><span class="sxs-lookup"><span data-stu-id="751d9-137">Version</span></span><br/> | <span data-ttu-id="751d9-138">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="751d9-138">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="751d9-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="751d9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="751d9-140">**Elemento BUTTONelement**</span><span class="sxs-lookup"><span data-stu-id="751d9-140">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> </dl>

 

 





