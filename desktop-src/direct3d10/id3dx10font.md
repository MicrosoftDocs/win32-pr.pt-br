---
description: A interface ID3DX10Font encapsula as texturas e os recursos necessários para processar uma fonte específica em um dispositivo específico.
ms.assetid: 81f4ffe3-f50d-47ce-ae85-15a2a19cacbd
title: Interface ID3DX10Font (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7d7c9fb1daa0934b5e6b3147f60803be5c0b5c07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173022"
---
# <a name="id3dx10font-interface"></a><span data-ttu-id="8d9f7-103">Interface ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="8d9f7-103">ID3DX10Font interface</span></span>

<span data-ttu-id="8d9f7-104">A interface ID3DX10Font encapsula as texturas e os recursos necessários para processar uma fonte específica em um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-104">The ID3DX10Font interface encapsulates the textures and resources needed to render a specific font on a specific device.</span></span>

## <a name="members"></a><span data-ttu-id="8d9f7-105">Membros</span><span class="sxs-lookup"><span data-stu-id="8d9f7-105">Members</span></span>

<span data-ttu-id="8d9f7-106">A interface **ID3DX10Font** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8d9f7-106">The **ID3DX10Font** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8d9f7-107">**ID3DX10Font** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8d9f7-107">**ID3DX10Font** also has these types of members:</span></span>

-   [<span data-ttu-id="8d9f7-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="8d9f7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8d9f7-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="8d9f7-109">Methods</span></span>

<span data-ttu-id="8d9f7-110">A interface **ID3DX10Font** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-110">The **ID3DX10Font** interface has these methods.</span></span>



| <span data-ttu-id="8d9f7-111">Método</span><span class="sxs-lookup"><span data-stu-id="8d9f7-111">Method</span></span>                                                     | <span data-ttu-id="8d9f7-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d9f7-112">Description</span></span>                                                                                                                                           |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d9f7-113">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="8d9f7-113">**DrawText**</span></span>](id3dx10font-drawtext.md)                   | <span data-ttu-id="8d9f7-114">Desenhar texto formatado.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-114">Draw formatted text.</span></span> <span data-ttu-id="8d9f7-115">Esse método dá suporte a cadeias de caracteres ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-115">This method supports ANSI and Unicode strings.</span></span><br/>                                                                        |
| [<span data-ttu-id="8d9f7-116">**GetDC**</span><span class="sxs-lookup"><span data-stu-id="8d9f7-116">**GetDC**</span></span>](id3dx10font-getdc.md)                         | <span data-ttu-id="8d9f7-117">Retorna um identificador para um contexto de dispositivo de vídeo (DC) que tem a fonte definida para ele.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-117">Return a handle to a display device context (DC) that has the font set onto it.</span></span><br/>                                                            |
| [<span data-ttu-id="8d9f7-118">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="8d9f7-118">**GetDesc**</span></span>](id3dx10font-getdesc.md)                     | <span data-ttu-id="8d9f7-119">Obtenha uma descrição do objeto de fonte atual.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-119">Get a description of the current font object.</span></span><br/>                                                                                              |
| [<span data-ttu-id="8d9f7-120">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="8d9f7-120">**GetDevice**</span></span>](id3dx10font-getdevice.md)                 | <span data-ttu-id="8d9f7-121">Recupere o dispositivo Direct3D associado ao objeto Font.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-121">Retrieve the Direct3D device associated with the font object.</span></span><br/>                                                                              |
| [<span data-ttu-id="8d9f7-122">**GetGlyphData**</span><span class="sxs-lookup"><span data-stu-id="8d9f7-122">**GetGlyphData**</span></span>](id3dx10font-getglyphdata.md)           | <span data-ttu-id="8d9f7-123">Retorna informações sobre o posicionamento e a orientação de um glifo em uma célula de caractere.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-123">Return information about the placement and orientation of a glyph in a character cell.</span></span><br/>                                                     |
| [<span data-ttu-id="8d9f7-124">**GetTextMetrics**</span><span class="sxs-lookup"><span data-stu-id="8d9f7-124">**GetTextMetrics**</span></span>](id3dx10font-gettextmetrics.md)       | <span data-ttu-id="8d9f7-125">Recuperar características de fonte.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-125">Retrieve font characteristics.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="8d9f7-126">**PreloadCharacters**</span><span class="sxs-lookup"><span data-stu-id="8d9f7-126">**PreloadCharacters**</span></span>](id3dx10font-preloadcharacters.md) | <span data-ttu-id="8d9f7-127">Carregue uma série de caracteres na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-127">Load a series of characters into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                        |
| [<span data-ttu-id="8d9f7-128">**PreloadGlyphs**</span><span class="sxs-lookup"><span data-stu-id="8d9f7-128">**PreloadGlyphs**</span></span>](id3dx10font-preloadglyphs.md)         | <span data-ttu-id="8d9f7-129">Carregue uma série de glifos na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-129">Load a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                            |
| [<span data-ttu-id="8d9f7-130">**PreloadText**</span><span class="sxs-lookup"><span data-stu-id="8d9f7-130">**PreloadText**</span></span>](id3dx10font-preloadtext.md)             | <span data-ttu-id="8d9f7-131">Carregue o texto formatado na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-131">Load formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="8d9f7-132">Esse método dá suporte a cadeias de caracteres ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-132">This method supports ANSI and Unicode strings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8d9f7-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d9f7-133">Remarks</span></span>

<span data-ttu-id="8d9f7-134">A interface ID3DX10Font é obtida chamando [**D3DX10CreateFont**](d3dx10createfont.md) ou [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md).</span><span class="sxs-lookup"><span data-stu-id="8d9f7-134">The ID3DX10Font interface is obtained by calling [**D3DX10CreateFont**](d3dx10createfont.md) or [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md).</span></span>

<span data-ttu-id="8d9f7-135">O tipo LPD3DX10FONT é definido como um ponteiro para a interface ID3DX10Font.</span><span class="sxs-lookup"><span data-stu-id="8d9f7-135">The LPD3DX10FONT type is defined as a pointer to the ID3DX10Font interface.</span></span>


```
typedef interface ID3DX10Font ID3DX10Font;
typedef interface ID3DX10Font *LPD3DX10FONT;
```



## <a name="requirements"></a><span data-ttu-id="8d9f7-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d9f7-136">Requirements</span></span>



| <span data-ttu-id="8d9f7-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d9f7-137">Requirement</span></span> | <span data-ttu-id="8d9f7-138">Valor</span><span class="sxs-lookup"><span data-stu-id="8d9f7-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d9f7-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d9f7-139">Header</span></span><br/>  | <dl> <span data-ttu-id="8d9f7-140"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d9f7-140"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d9f7-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d9f7-141">Library</span></span><br/> | <dl> <span data-ttu-id="8d9f7-142"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d9f7-142"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d9f7-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d9f7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d9f7-144">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="8d9f7-144">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
