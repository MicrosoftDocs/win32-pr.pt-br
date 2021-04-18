---
title: TEXT. cursor
description: O atributo cursor especifica ou recupera um valor que indica qual cursor aparece quando o mouse está sobre o controle de texto.
ms.assetid: 360d4ed1-9c4f-4210-8e77-2dfbe7573869
keywords:
- TEXT. cursor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8cf7b135ed0a99b5c65f760a08e4e7083234674
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791286"
---
# <a name="textcursor"></a><span data-ttu-id="a9346-104">TEXT. cursor</span><span class="sxs-lookup"><span data-stu-id="a9346-104">TEXT.cursor</span></span>

<span data-ttu-id="a9346-105">O atributo **cursor** especifica ou recupera um valor que indica qual cursor aparece quando o mouse está sobre o controle de texto.</span><span class="sxs-lookup"><span data-stu-id="a9346-105">The **cursor** attribute specifies or retrieves a value indicating which cursor appears when the mouse is over the Text control.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="a9346-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="a9346-106">Possible Values</span></span>

<span data-ttu-id="a9346-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a9346-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="a9346-108">Valor</span><span class="sxs-lookup"><span data-stu-id="a9346-108">Value</span></span>            | <span data-ttu-id="a9346-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9346-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9346-110">sistema</span><span class="sxs-lookup"><span data-stu-id="a9346-110">system</span></span>           | <span data-ttu-id="a9346-111">Padrão.</span><span class="sxs-lookup"><span data-stu-id="a9346-111">Default.</span></span> <span data-ttu-id="a9346-112">Cursor dependente de plataforma (geralmente uma seta).</span><span class="sxs-lookup"><span data-stu-id="a9346-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="a9346-113">existentes</span><span class="sxs-lookup"><span data-stu-id="a9346-113">hand</span></span>             | <span data-ttu-id="a9346-114">Existentes.</span><span class="sxs-lookup"><span data-stu-id="a9346-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="a9346-115">ajuda</span><span class="sxs-lookup"><span data-stu-id="a9346-115">help</span></span>             | <span data-ttu-id="a9346-116">Seta com um ponto de interrogação indicando que a ajuda está disponível.</span><span class="sxs-lookup"><span data-stu-id="a9346-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="a9346-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="a9346-117">sizeall</span></span>          | <span data-ttu-id="a9346-118">Seta de quatro pontas apontando para norte, Sul, leste e oeste.</span><span class="sxs-lookup"><span data-stu-id="a9346-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="a9346-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="a9346-119">sizenesw</span></span>         | <span data-ttu-id="a9346-120">Seta de duas pontas apontando para nordeste e sudoeste.</span><span class="sxs-lookup"><span data-stu-id="a9346-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="a9346-121">sizens</span><span class="sxs-lookup"><span data-stu-id="a9346-121">sizens</span></span>           | <span data-ttu-id="a9346-122">Seta de duas pontas apontando para norte e Sul.</span><span class="sxs-lookup"><span data-stu-id="a9346-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="a9346-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="a9346-123">sizenwse</span></span>         | <span data-ttu-id="a9346-124">Seta de duas pontas apontando para noroeste e sudeste.</span><span class="sxs-lookup"><span data-stu-id="a9346-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="a9346-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="a9346-125">sizewe</span></span>           | <span data-ttu-id="a9346-126">Seta de duas pontas apontando para o oeste e o leste.</span><span class="sxs-lookup"><span data-stu-id="a9346-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="a9346-127">upseta</span><span class="sxs-lookup"><span data-stu-id="a9346-127">uparrow</span></span>          | <span data-ttu-id="a9346-128">Seta vertical apontando para cima.</span><span class="sxs-lookup"><span data-stu-id="a9346-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="a9346-129">\*. ani ou \* . cur</span><span class="sxs-lookup"><span data-stu-id="a9346-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="a9346-130">Qualquer arquivo. ani ou. cur (deve estar no mesmo diretório que o arquivo. WMS ou no arquivo. wmz).</span><span class="sxs-lookup"><span data-stu-id="a9346-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

<span data-ttu-id="a9346-131">Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.</span><span class="sxs-lookup"><span data-stu-id="a9346-131">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9346-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9346-132">Requirements</span></span>



| <span data-ttu-id="a9346-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9346-133">Requirement</span></span> | <span data-ttu-id="a9346-134">Valor</span><span class="sxs-lookup"><span data-stu-id="a9346-134">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a9346-135">Versão</span><span class="sxs-lookup"><span data-stu-id="a9346-135">Version</span></span><br/> | <span data-ttu-id="a9346-136">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a9346-136">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a9346-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9346-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9346-138">**Elemento de texto**</span><span class="sxs-lookup"><span data-stu-id="a9346-138">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





