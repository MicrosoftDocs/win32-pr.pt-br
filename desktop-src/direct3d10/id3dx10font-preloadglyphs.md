---
description: Carregue uma série de glifos na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.
ms.assetid: 7d063d52-af2c-44a6-9019-3d546acfbd4a
title: 'ID3DX10Font: método reloadGlyphs de:P (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadGlyphs
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fdb67b8a25912c6efc49ef27082d3b6b4e843b33
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760677"
---
# <a name="id3dx10fontpreloadglyphs-method"></a><span data-ttu-id="f836c-103">ID3DX10Font: método reloadGlyphs de:P</span><span class="sxs-lookup"><span data-stu-id="f836c-103">ID3DX10Font::PreloadGlyphs method</span></span>

<span data-ttu-id="f836c-104">Carregue uma série de glifos na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f836c-104">Load a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="f836c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f836c-105">Syntax</span></span>


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="f836c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f836c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f836c-107">*Primeiro* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f836c-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f836c-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f836c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f836c-109">ID do primeiro glifo a ser carregado na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f836c-109">ID of the first glyph to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="f836c-110">*Último* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f836c-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f836c-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f836c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f836c-112">ID do último glifo a ser carregado na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f836c-112">ID of the last glyph to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f836c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f836c-113">Return value</span></span>

<span data-ttu-id="f836c-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f836c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f836c-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f836c-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f836c-116">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="f836c-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="f836c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f836c-117">Remarks</span></span>

<span data-ttu-id="f836c-118">Esse método gera texturas que contêm os glifos de entrada.</span><span class="sxs-lookup"><span data-stu-id="f836c-118">This method generates textures that contain the input glyphs.</span></span> <span data-ttu-id="f836c-119">Os glifos são desenhados como uma série de triângulos.</span><span class="sxs-lookup"><span data-stu-id="f836c-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="f836c-120">Os glifos não serão renderizados para o dispositivo; ID3DX10Font::D rawText ainda deve ser chamado para renderizar os glifos.</span><span class="sxs-lookup"><span data-stu-id="f836c-120">Glyphs will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the glyphs.</span></span> <span data-ttu-id="f836c-121">No entanto, ao pré-carregar glifos na memória de vídeo, ID3DX10Font::D rawText usará substancialmente menos recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="f836c-121">However, by pre-loading glyphs into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="f836c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f836c-122">Requirements</span></span>



| <span data-ttu-id="f836c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f836c-123">Requirement</span></span> | <span data-ttu-id="f836c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f836c-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f836c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f836c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f836c-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f836c-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f836c-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f836c-127">Library</span></span><br/> | <dl> <span data-ttu-id="f836c-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f836c-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f836c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f836c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f836c-130">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="f836c-130">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="f836c-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="f836c-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
