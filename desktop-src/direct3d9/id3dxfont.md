---
description: A interface ID3DXFont encapsula as texturas e os recursos necessários para processar uma fonte específica em um dispositivo específico.
ms.assetid: ac40b600-3b9f-4e6e-8563-18597b3dd602
title: Interface ID3DXFont (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3b3919e4198feddbe4ac193f58f63d48753aa94d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105796086"
---
# <a name="id3dxfont-interface"></a><span data-ttu-id="fb04e-103">Interface ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="fb04e-103">ID3DXFont interface</span></span>

<span data-ttu-id="fb04e-104">A interface ID3DXFont encapsula as texturas e os recursos necessários para processar uma fonte específica em um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="fb04e-104">The ID3DXFont interface encapsulates the textures and resources needed to render a specific font on a specific device.</span></span>

## <a name="members"></a><span data-ttu-id="fb04e-105">Membros</span><span class="sxs-lookup"><span data-stu-id="fb04e-105">Members</span></span>

<span data-ttu-id="fb04e-106">A interface **ID3DXFont** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fb04e-106">The **ID3DXFont** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fb04e-107">**ID3DXFont** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fb04e-107">**ID3DXFont** also has these types of members:</span></span>

-   [<span data-ttu-id="fb04e-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="fb04e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fb04e-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="fb04e-109">Methods</span></span>

<span data-ttu-id="fb04e-110">A interface **ID3DXFont** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="fb04e-110">The **ID3DXFont** interface has these methods.</span></span>



| <span data-ttu-id="fb04e-111">Método</span><span class="sxs-lookup"><span data-stu-id="fb04e-111">Method</span></span>                                                    | <span data-ttu-id="fb04e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb04e-112">Description</span></span>                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb04e-113">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="fb04e-113">**DrawText**</span></span>](id3dxfont--drawtext.md)                   | <span data-ttu-id="fb04e-114">Desenha texto formatado.</span><span class="sxs-lookup"><span data-stu-id="fb04e-114">Draws formatted text.</span></span> <span data-ttu-id="fb04e-115">Esse método dá suporte a cadeias de caracteres ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="fb04e-115">This method supports ANSI and Unicode strings.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="fb04e-116">**GetDC**</span><span class="sxs-lookup"><span data-stu-id="fb04e-116">**GetDC**</span></span>](id3dxfont--getdc.md)                         | <span data-ttu-id="fb04e-117">Retorna um identificador para um contexto de dispositivo de exibição (DC) que tem o conjunto de fontes.</span><span class="sxs-lookup"><span data-stu-id="fb04e-117">Returns a handle to a display device context (DC) that has the font set.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="fb04e-118">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="fb04e-118">**GetDesc**</span></span>](id3dxfont--getdesc.md)                     | <span data-ttu-id="fb04e-119">Obtém uma descrição do objeto de fonte atual.</span><span class="sxs-lookup"><span data-stu-id="fb04e-119">Gets a description of the current font object.</span></span> <span data-ttu-id="fb04e-120">GetDescW e getdescum são idênticos a esse método, exceto que um ponteiro é retornado para uma estrutura [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) ou **D3DXFONT \_ desca** , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fb04e-120">GetDescW and GetDescA are identical to this method, except that a pointer is returned to a [**D3DXFONT\_DESCW**](d3dxfont-desc.md) or **D3DXFONT\_DESCA** structure, respectively.</span></span><br/> |
| [<span data-ttu-id="fb04e-121">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="fb04e-121">**GetDevice**</span></span>](id3dxfont--getdevice.md)                 | <span data-ttu-id="fb04e-122">Recupera o dispositivo Direct3D associado ao objeto Font.</span><span class="sxs-lookup"><span data-stu-id="fb04e-122">Retrieves the Direct3D device associated with the font object.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="fb04e-123">**GetGlyphData**</span><span class="sxs-lookup"><span data-stu-id="fb04e-123">**GetGlyphData**</span></span>](id3dxfont--getglyphdata.md)           | <span data-ttu-id="fb04e-124">Retorna informações sobre o posicionamento e a orientação de um glifo em uma célula de caractere.</span><span class="sxs-lookup"><span data-stu-id="fb04e-124">Returns information about the placement and orientation of a glyph in a character cell.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="fb04e-125">**GetTextMetrics**</span><span class="sxs-lookup"><span data-stu-id="fb04e-125">**GetTextMetrics**</span></span>](id3dxfont--gettextmetrics.md)       | <span data-ttu-id="fb04e-126">Recupera características de fonte que são identificadas em uma estrutura [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) .</span><span class="sxs-lookup"><span data-stu-id="fb04e-126">Retrieves font characteristics that are identified in a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.</span></span> <span data-ttu-id="fb04e-127">Esse método dá suporte às configurações de compilador ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="fb04e-127">This method supports ANSI and Unicode compiler settings.</span></span><br/>                                                                       |
| [<span data-ttu-id="fb04e-128">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="fb04e-128">**OnLostDevice**</span></span>](id3dxfont--onlostdevice.md)           | <span data-ttu-id="fb04e-129">Use este método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks.</span><span class="sxs-lookup"><span data-stu-id="fb04e-129">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="fb04e-130">Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb04e-130">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/>                                              |
| [<span data-ttu-id="fb04e-131">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="fb04e-131">**OnResetDevice**</span></span>](id3dxfont--onresetdevice.md)         | <span data-ttu-id="fb04e-132">Use este método para readquirir recursos e salvar o estado inicial.</span><span class="sxs-lookup"><span data-stu-id="fb04e-132">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="fb04e-133">**PreloadCharacters**</span><span class="sxs-lookup"><span data-stu-id="fb04e-133">**PreloadCharacters**</span></span>](id3dxfont--preloadcharacters.md) | <span data-ttu-id="fb04e-134">Carrega uma série de caracteres na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb04e-134">Loads a series of characters into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="fb04e-135">**PreloadGlyphs**</span><span class="sxs-lookup"><span data-stu-id="fb04e-135">**PreloadGlyphs**</span></span>](id3dxfont--preloadglyphs.md)         | <span data-ttu-id="fb04e-136">Carrega uma série de glifos na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb04e-136">Loads a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="fb04e-137">**PreloadText**</span><span class="sxs-lookup"><span data-stu-id="fb04e-137">**PreloadText**</span></span>](id3dxfont--preloadtext.md)             | <span data-ttu-id="fb04e-138">Carrega texto formatado em memória de vídeo para melhorar a eficiência da renderização para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb04e-138">Loads formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="fb04e-139">Esse método dá suporte a cadeias de caracteres ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="fb04e-139">This method supports ANSI and Unicode strings.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="fb04e-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb04e-140">Remarks</span></span>

<span data-ttu-id="fb04e-141">A interface **ID3DXFont** é obtida chamando [**D3DXCreateFont**](d3dxcreatefont.md) ou [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md).</span><span class="sxs-lookup"><span data-stu-id="fb04e-141">The **ID3DXFont** interface is obtained by calling [**D3DXCreateFont**](d3dxcreatefont.md) or [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md).</span></span>

<span data-ttu-id="fb04e-142">O tipo LPD3DXFONT é definido como um ponteiro para a interface **ID3DXFont** .</span><span class="sxs-lookup"><span data-stu-id="fb04e-142">The LPD3DXFONT type is defined as a pointer to the **ID3DXFont** interface.</span></span>


```
typedef interface ID3DXFont ID3DXFont;
typedef interface ID3DXFont *LPD3DXFONT;
```



## <a name="requirements"></a><span data-ttu-id="fb04e-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb04e-143">Requirements</span></span>



| <span data-ttu-id="fb04e-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb04e-144">Requirement</span></span> | <span data-ttu-id="fb04e-145">Valor</span><span class="sxs-lookup"><span data-stu-id="fb04e-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb04e-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb04e-146">Header</span></span><br/>  | <dl> <span data-ttu-id="fb04e-147"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb04e-147"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="fb04e-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb04e-148">Library</span></span><br/> | <dl> <span data-ttu-id="fb04e-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb04e-149"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fb04e-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb04e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb04e-151">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="fb04e-151">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
