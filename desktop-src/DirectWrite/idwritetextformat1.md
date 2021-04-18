---
title: Interface IDWriteTextFormat1
description: Descreve as propriedades de fonte e parágrafo usadas para formatar texto e descreve as informações de localidade. | Interface IDWriteTextFormat1
ms.assetid: 15295A17-E542-4071-AE38-02014A1235D5
keywords:
- Gravação direta da interface IDWriteTextFormat1
- Gravação direta da interface IDWriteTextFormat1, descrita
topic_type:
- apiref
api_name:
- IDWriteTextFormat1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796c5f845b5ed0d0522039865f2acb023fc2ab0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105753491"
---
# <a name="idwritetextformat1-interface"></a><span data-ttu-id="ce86e-106">Interface IDWriteTextFormat1</span><span class="sxs-lookup"><span data-stu-id="ce86e-106">IDWriteTextFormat1 interface</span></span>

<span data-ttu-id="ce86e-107">Descreve as propriedades de fonte e parágrafo usadas para formatar texto e descreve as informações de localidade.</span><span class="sxs-lookup"><span data-stu-id="ce86e-107">Describes the font and paragraph properties used to format text, and it describes locale information.</span></span> <span data-ttu-id="ce86e-108">Essa interface tem todos os mesmos métodos que [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e adiciona a capacidade de aplicar uma orientação explícita.</span><span class="sxs-lookup"><span data-stu-id="ce86e-108">This interface has all the same methods as [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and adds the ability for you to apply an explicit orientation.</span></span>

## <a name="members"></a><span data-ttu-id="ce86e-109">Membros</span><span class="sxs-lookup"><span data-stu-id="ce86e-109">Members</span></span>

<span data-ttu-id="ce86e-110">A interface **IDWriteTextFormat1** herda de [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span><span class="sxs-lookup"><span data-stu-id="ce86e-110">The **IDWriteTextFormat1** interface inherits from [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span></span> <span data-ttu-id="ce86e-111">**IDWriteTextFormat1** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ce86e-111">**IDWriteTextFormat1** also has these types of members:</span></span>

-   [<span data-ttu-id="ce86e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce86e-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ce86e-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce86e-113">Methods</span></span>

<span data-ttu-id="ce86e-114">A interface **IDWriteTextFormat1** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ce86e-114">The **IDWriteTextFormat1** interface has these methods.</span></span>



| <span data-ttu-id="ce86e-115">Método</span><span class="sxs-lookup"><span data-stu-id="ce86e-115">Method</span></span>                                                                                | <span data-ttu-id="ce86e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce86e-116">Description</span></span>                                                                                                             |
|:--------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce86e-117">**GetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="ce86e-117">**GetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getfontfallback)                         | <span data-ttu-id="ce86e-118">Obtém o fallback atual.</span><span class="sxs-lookup"><span data-stu-id="ce86e-118">Gets the current fallback.</span></span> <span data-ttu-id="ce86e-119">Se nenhum já tiver sido definido desde a criação do layout, ele será nullptr.</span><span class="sxs-lookup"><span data-stu-id="ce86e-119">If none was ever set since creating the layout, it will be nullptr.</span></span><br/>               |
| [<span data-ttu-id="ce86e-120">**GetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="ce86e-120">**GetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getlastlinewrapping)                 | <span data-ttu-id="ce86e-121">Obtém o modo de disposição da última linha.</span><span class="sxs-lookup"><span data-stu-id="ce86e-121">Gets the wrapping mode of the last line.</span></span><br/>                                                                     |
| [<span data-ttu-id="ce86e-122">**GetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="ce86e-122">**GetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getopticalalignment)                 | <span data-ttu-id="ce86e-123">Obtém o alinhamento da margem óptica para o formato de texto.</span><span class="sxs-lookup"><span data-stu-id="ce86e-123">Gets the optical margin alignment for the text format.</span></span><br/>                                                       |
| [<span data-ttu-id="ce86e-124">**GetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="ce86e-124">**GetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getverticalglyphorientation) | <span data-ttu-id="ce86e-125">Obtenha a orientação preferida de glifos ao usar uma direção de leitura vertical.</span><span class="sxs-lookup"><span data-stu-id="ce86e-125">Get the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/>                             |
| [<span data-ttu-id="ce86e-126">**SetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="ce86e-126">**SetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setfontfallback)                         | <span data-ttu-id="ce86e-127">Aplica o fallback de fonte personalizado no layout.</span><span class="sxs-lookup"><span data-stu-id="ce86e-127">Applies the custom font fallback onto the layout.</span></span> <span data-ttu-id="ce86e-128">Se nenhum for definido, ele usará a lista de fallback do sistema padrão.</span><span class="sxs-lookup"><span data-stu-id="ce86e-128">If none is set, it uses the default system fallback list.</span></span> <br/> |
| [<span data-ttu-id="ce86e-129">**SetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="ce86e-129">**SetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setlastlinewrapping)                   | <span data-ttu-id="ce86e-130">Define o modo de disposição da última linha.</span><span class="sxs-lookup"><span data-stu-id="ce86e-130">Sets the wrapping mode of the last line.</span></span><br/>                                                                     |
| [<span data-ttu-id="ce86e-131">**SetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="ce86e-131">**SetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setopticalalignment)                 | <span data-ttu-id="ce86e-132">Define o alinhamento de margem óptica para o formato de texto.</span><span class="sxs-lookup"><span data-stu-id="ce86e-132">Sets the optical margin alignment for the text format.</span></span><br/>                                                       |
| [<span data-ttu-id="ce86e-133">**SetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="ce86e-133">**SetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setverticalglyphorientation) | <span data-ttu-id="ce86e-134">Define a orientação de um formato de texto.</span><span class="sxs-lookup"><span data-stu-id="ce86e-134">Sets the orientation of a text format.</span></span><br/>                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="ce86e-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce86e-135">Requirements</span></span>



| <span data-ttu-id="ce86e-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce86e-136">Requirement</span></span> | <span data-ttu-id="ce86e-137">Valor</span><span class="sxs-lookup"><span data-stu-id="ce86e-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce86e-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce86e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ce86e-139">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ce86e-139">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="ce86e-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce86e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ce86e-141">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="ce86e-141">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="ce86e-142">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="ce86e-142">Minimum supported phone</span></span><br/>  | <span data-ttu-id="ce86e-143">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="ce86e-143">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="ce86e-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce86e-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce86e-145"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce86e-145"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ce86e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="ce86e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce86e-147"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce86e-147"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ce86e-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce86e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce86e-149">**IDWriteTextFormat**</span><span class="sxs-lookup"><span data-stu-id="ce86e-149">**IDWriteTextFormat**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
</dt> </dl>

 

