---
title: Interface IDWriteTextLayout3
description: Representa um bloco de texto após ter sido totalmente analisado e formatado. | Interface IDWriteTextLayout3
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
keywords:
- Gravação direta da interface IDWriteTextLayout3
- Gravação direta da interface IDWriteTextLayout3, descrita
topic_type:
- apiref
api_name:
- IDWriteTextLayout3
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78a7a9203245939e40b522e0ef5998be0764085a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105759003"
---
# <a name="idwritetextlayout3-interface"></a><span data-ttu-id="046c5-106">Interface IDWriteTextLayout3</span><span class="sxs-lookup"><span data-stu-id="046c5-106">IDWriteTextLayout3 interface</span></span>

<span data-ttu-id="046c5-107">Representa um bloco de texto após ter sido totalmente analisado e formatado.</span><span class="sxs-lookup"><span data-stu-id="046c5-107">Represents a block of text after it has been fully analyzed and formatted.</span></span>

## <a name="members"></a><span data-ttu-id="046c5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="046c5-108">Members</span></span>

<span data-ttu-id="046c5-109">A interface **IDWriteTextLayout3** herda de [**IDWriteTextLayout2**](idwritetextlayout2.md).</span><span class="sxs-lookup"><span data-stu-id="046c5-109">The **IDWriteTextLayout3** interface inherits from [**IDWriteTextLayout2**](idwritetextlayout2.md).</span></span> <span data-ttu-id="046c5-110">**IDWriteTextLayout3** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="046c5-110">**IDWriteTextLayout3** also has these types of members:</span></span>

-   [<span data-ttu-id="046c5-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="046c5-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="046c5-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="046c5-112">Methods</span></span>

<span data-ttu-id="046c5-113">A interface **IDWriteTextLayout3** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="046c5-113">The **IDWriteTextLayout3** interface has these methods.</span></span>



| <span data-ttu-id="046c5-114">Método</span><span class="sxs-lookup"><span data-stu-id="046c5-114">Method</span></span>                                                          | <span data-ttu-id="046c5-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="046c5-115">Description</span></span>                                                                                                                                                                                                                                                          |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="046c5-116">**GetLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="046c5-116">**GetLineMetrics**</span></span>](idwritetextlayout3-getlinemetrics.md)     | <span data-ttu-id="046c5-117">Recupera as propriedades de cada linha.</span><span class="sxs-lookup"><span data-stu-id="046c5-117">Retrieves properties of each line.</span></span><br/>                                                                                                                                                                                                                        |
| [<span data-ttu-id="046c5-118">**GetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="046c5-118">**GetLineSpacing**</span></span>](idwritetextlayout3-getlinespacing.md)     | <span data-ttu-id="046c5-119">Obtém informações de espaçamento de linha.</span><span class="sxs-lookup"><span data-stu-id="046c5-119">Gets line spacing information.</span></span><br/>                                                                                                                                                                                                                            |
| [<span data-ttu-id="046c5-120">**InvalidateLayout**</span><span class="sxs-lookup"><span data-stu-id="046c5-120">**InvalidateLayout**</span></span>](idwritetextlayout3-invalidatelayout.md) | <span data-ttu-id="046c5-121">Invalida o layout, forçando o layout a ser remedido antes de chamar as métricas ou as funções de desenho.</span><span class="sxs-lookup"><span data-stu-id="046c5-121">Invalidates the layout, forcing layout to remeasure before calling the metrics or drawing functions.</span></span> <span data-ttu-id="046c5-122">Isso será útil se a localidade de uma fonte for alterada, e o layout deve ser redesenhado ou se o tamanho de um cliente implementado IDWriteInlineObject for alterado.</span><span class="sxs-lookup"><span data-stu-id="046c5-122">This is useful if the locality of a font changes, and layout should be redrawn, or if the size of a client implemented IDWriteInlineObject changes.</span></span> <br/> |
| [<span data-ttu-id="046c5-123">**SetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="046c5-123">**SetLineSpacing**</span></span>](idwritetextlayout3-setlinespacing.md)     | <span data-ttu-id="046c5-124">Definir espaçamento de linha.</span><span class="sxs-lookup"><span data-stu-id="046c5-124">Set line spacing.</span></span><br/>                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="046c5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="046c5-125">Requirements</span></span>



| <span data-ttu-id="046c5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="046c5-126">Requirement</span></span> | <span data-ttu-id="046c5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="046c5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="046c5-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="046c5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="046c5-129">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="046c5-129">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="046c5-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="046c5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="046c5-131">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="046c5-131">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="046c5-132">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="046c5-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="046c5-133">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="046c5-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="046c5-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="046c5-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="046c5-135"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="046c5-135"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="046c5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="046c5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="046c5-137"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="046c5-137"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="046c5-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="046c5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="046c5-139">**IDWriteTextLayout2**</span><span class="sxs-lookup"><span data-stu-id="046c5-139">**IDWriteTextLayout2**</span></span>](idwritetextlayout2.md)
</dt> </dl>

 

 





