---
title: Interface IDWriteTextLayout2
description: Representa um bloco de texto após ter sido totalmente analisado e formatado. | Interface IDWriteTextLayout2
ms.assetid: 034D795B-016A-401E-AD75-D5B0D1E87806
keywords:
- Gravação direta da interface IDWriteTextLayout2
- Gravação direta da interface IDWriteTextLayout2, descrita
topic_type:
- apiref
api_name:
- IDWriteTextLayout2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80bb6037a598096109a9255abbb01ef289c5ef99
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298305"
---
# <a name="idwritetextlayout2-interface"></a><span data-ttu-id="59151-106">Interface IDWriteTextLayout2</span><span class="sxs-lookup"><span data-stu-id="59151-106">IDWriteTextLayout2 interface</span></span>

<span data-ttu-id="59151-107">Representa um bloco de texto após ter sido totalmente analisado e formatado.</span><span class="sxs-lookup"><span data-stu-id="59151-107">Represents a block of text after it has been fully analyzed and formatted.</span></span>

## <a name="members"></a><span data-ttu-id="59151-108">Membros</span><span class="sxs-lookup"><span data-stu-id="59151-108">Members</span></span>

<span data-ttu-id="59151-109">A interface **IDWriteTextLayout2** herda de [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1).</span><span class="sxs-lookup"><span data-stu-id="59151-109">The **IDWriteTextLayout2** interface inherits from [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1).</span></span> <span data-ttu-id="59151-110">**IDWriteTextLayout2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="59151-110">**IDWriteTextLayout2** also has these types of members:</span></span>

-   [<span data-ttu-id="59151-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="59151-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="59151-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="59151-112">Methods</span></span>

<span data-ttu-id="59151-113">A interface **IDWriteTextLayout2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="59151-113">The **IDWriteTextLayout2** interface has these methods.</span></span>



| <span data-ttu-id="59151-114">Método</span><span class="sxs-lookup"><span data-stu-id="59151-114">Method</span></span>                                                                                | <span data-ttu-id="59151-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="59151-115">Description</span></span>                                                                                 |
|:--------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59151-116">**GetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="59151-116">**GetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getfontfallback)                         | <span data-ttu-id="59151-117">Obter o objeto de fallback de fonte atual.</span><span class="sxs-lookup"><span data-stu-id="59151-117">Get the current font fallback object.</span></span> <br/>                                           |
| [<span data-ttu-id="59151-118">**GetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="59151-118">**GetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getlastlinewrapping)                 | <span data-ttu-id="59151-119">Veja se a última palavra na última linha está encapsulada ou não.</span><span class="sxs-lookup"><span data-stu-id="59151-119">Get whether or not the last word on the last line is wrapped.</span></span><br/>                    |
| [<span data-ttu-id="59151-120">**Getmetrics**</span><span class="sxs-lookup"><span data-stu-id="59151-120">**GetMetrics**</span></span>](idwritetextlayout2-getmetrics.md)                                   | <span data-ttu-id="59151-121">Recupera as métricas gerais para a cadeia de caracteres formatada.</span><span class="sxs-lookup"><span data-stu-id="59151-121">Retrieves overall metrics for the formatted string.</span></span> <br/>                             |
| [<span data-ttu-id="59151-122">**GetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="59151-122">**GetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getopticalalignment)                 | <span data-ttu-id="59151-123">Saiba como os glifos se alinham com as bordas da margem.</span><span class="sxs-lookup"><span data-stu-id="59151-123">Get how the glyphs align to the edges the margin.</span></span> <br/>                               |
| [<span data-ttu-id="59151-124">**GetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="59151-124">**GetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getverticalglyphorientation) | <span data-ttu-id="59151-125">Obtenha a orientação preferida de glifos ao usar uma direção de leitura vertical.</span><span class="sxs-lookup"><span data-stu-id="59151-125">Get the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/> |
| [<span data-ttu-id="59151-126">**SetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="59151-126">**SetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setfontfallback)                         | <span data-ttu-id="59151-127">Aplicar um fallback de fonte personalizado no layout.</span><span class="sxs-lookup"><span data-stu-id="59151-127">Apply a custom font fallback onto layout.</span></span><br/>                                        |
| [<span data-ttu-id="59151-128">**SetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="59151-128">**SetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setlastlinewrapping)                 | <span data-ttu-id="59151-129">Defina se a última palavra na última linha será encapsulada.</span><span class="sxs-lookup"><span data-stu-id="59151-129">Set whether or not the last word on the last line is wrapped.</span></span> <br/>                   |
| [<span data-ttu-id="59151-130">**SetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="59151-130">**SetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setopticalalignment)                 | <span data-ttu-id="59151-131">Defina como os glifos se alinham com as bordas da margem.</span><span class="sxs-lookup"><span data-stu-id="59151-131">Set how the glyphs align to the edges the margin.</span></span><br/>                                |
| [<span data-ttu-id="59151-132">**SetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="59151-132">**SetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setverticalglyphorientation) | <span data-ttu-id="59151-133">Defina a orientação preferida de glifos ao usar uma direção de leitura vertical.</span><span class="sxs-lookup"><span data-stu-id="59151-133">Set the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="59151-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59151-134">Requirements</span></span>



| <span data-ttu-id="59151-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="59151-135">Requirement</span></span> | <span data-ttu-id="59151-136">Valor</span><span class="sxs-lookup"><span data-stu-id="59151-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59151-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59151-137">Minimum supported client</span></span><br/> | <span data-ttu-id="59151-138">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="59151-138">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="59151-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59151-139">Minimum supported server</span></span><br/> | <span data-ttu-id="59151-140">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="59151-140">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="59151-141">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="59151-141">Minimum supported phone</span></span><br/>  | <span data-ttu-id="59151-142">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="59151-142">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="59151-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59151-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="59151-144"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59151-144"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="59151-145">DLL</span><span class="sxs-lookup"><span data-stu-id="59151-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59151-146"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59151-146"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="59151-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="59151-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59151-148">**IDWriteTextLayout1**</span><span class="sxs-lookup"><span data-stu-id="59151-148">**IDWriteTextLayout1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
</dt> </dl>

 

