---
title: Interface IDWriteTextFormat2
description: Descreve as propriedades de fonte e parágrafo usadas para formatar texto e descreve as informações de localidade. | Interface IDWriteTextFormat2
ms.assetid: 4396d2b0-240f-ee8b-1d21-c4294fb29b51
keywords:
- Gravação direta da interface IDWriteTextFormat2
- Gravação direta da interface IDWriteTextFormat2, descrita
topic_type:
- apiref
api_name:
- IDWriteTextFormat2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06abf78095953f684ed6ec3fd241c699b2b37db4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105778776"
---
# <a name="idwritetextformat2-interface"></a><span data-ttu-id="4437b-106">Interface IDWriteTextFormat2</span><span class="sxs-lookup"><span data-stu-id="4437b-106">IDWriteTextFormat2 interface</span></span>

<span data-ttu-id="4437b-107">Descreve as propriedades de fonte e parágrafo usadas para formatar texto e descreve as informações de localidade.</span><span class="sxs-lookup"><span data-stu-id="4437b-107">Describes the font and paragraph properties used to format text, and it describes locale information.</span></span>

## <a name="members"></a><span data-ttu-id="4437b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4437b-108">Members</span></span>

<span data-ttu-id="4437b-109">A interface **IDWriteTextFormat2** herda de [**IDWriteTextFormat1**](idwritetextformat1.md).</span><span class="sxs-lookup"><span data-stu-id="4437b-109">The **IDWriteTextFormat2** interface inherits from [**IDWriteTextFormat1**](idwritetextformat1.md).</span></span> <span data-ttu-id="4437b-110">**IDWriteTextFormat2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4437b-110">**IDWriteTextFormat2** also has these types of members:</span></span>

-   [<span data-ttu-id="4437b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4437b-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4437b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4437b-112">Methods</span></span>

<span data-ttu-id="4437b-113">A interface **IDWriteTextFormat2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4437b-113">The **IDWriteTextFormat2** interface has these methods.</span></span>



| <span data-ttu-id="4437b-114">Método</span><span class="sxs-lookup"><span data-stu-id="4437b-114">Method</span></span>                                                      | <span data-ttu-id="4437b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="4437b-115">Description</span></span>                                                                      |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="4437b-116">**GetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="4437b-116">**GetLineSpacing**</span></span>](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritetextformat2-getlinespacing) | <span data-ttu-id="4437b-117">Obtém o ajuste de espaçamento de linha definido para um parágrafo de texto multilinha.</span><span class="sxs-lookup"><span data-stu-id="4437b-117">Gets the line spacing adjustment set for a multiline text paragraph.</span></span> <br/> |
| [<span data-ttu-id="4437b-118">**SetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="4437b-118">**SetLineSpacing**</span></span>](idwritetextformat2-setlinespacing.md) | <span data-ttu-id="4437b-119">Definir espaçamento de linha.</span><span class="sxs-lookup"><span data-stu-id="4437b-119">Set line spacing.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="4437b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4437b-120">Requirements</span></span>



| <span data-ttu-id="4437b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4437b-121">Requirement</span></span> | <span data-ttu-id="4437b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4437b-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4437b-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4437b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4437b-124">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4437b-124">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="4437b-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4437b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4437b-126">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="4437b-126">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="4437b-127">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="4437b-127">Minimum supported phone</span></span><br/>  | <span data-ttu-id="4437b-128">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="4437b-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="4437b-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4437b-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="4437b-130"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4437b-130"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4437b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4437b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4437b-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4437b-132"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4437b-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="4437b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4437b-134">**IDWriteTextFormat1**</span><span class="sxs-lookup"><span data-stu-id="4437b-134">**IDWriteTextFormat1**</span></span>](idwritetextformat1.md)
</dt> </dl>

 

