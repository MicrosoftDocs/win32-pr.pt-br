---
description: Carrega uma série de glifos na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.
ms.assetid: df023359-bcb3-4c05-950b-19cdeba97c85
title: 'ID3DXFont: método reloadGlyphs de:P (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadGlyphs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 954d9e8abb310f962f7188720cb32035baf50d3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012172"
---
# <a name="id3dxfontpreloadglyphs-method"></a><span data-ttu-id="fa7ee-103">ID3DXFont: método reloadGlyphs de:P</span><span class="sxs-lookup"><span data-stu-id="fa7ee-103">ID3DXFont::PreloadGlyphs method</span></span>

<span data-ttu-id="fa7ee-104">Carrega uma série de glifos na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa7ee-104">Loads a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa7ee-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa7ee-105">Syntax</span></span>


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="fa7ee-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa7ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa7ee-107">*Primeiro* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa7ee-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa7ee-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa7ee-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fa7ee-109">ID do primeiro glifo a ser carregado na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fa7ee-109">ID of the first glyph to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="fa7ee-110">*Último* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa7ee-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa7ee-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa7ee-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fa7ee-112">ID do último glifo a ser carregado na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fa7ee-112">ID of the last glyph to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa7ee-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa7ee-113">Return value</span></span>

<span data-ttu-id="fa7ee-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fa7ee-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fa7ee-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fa7ee-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="fa7ee-116">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="fa7ee-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa7ee-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa7ee-117">Remarks</span></span>

<span data-ttu-id="fa7ee-118">Esse método gera texturas que contêm os glifos de entrada.</span><span class="sxs-lookup"><span data-stu-id="fa7ee-118">This method generates textures that contain the input glyphs.</span></span> <span data-ttu-id="fa7ee-119">Os glifos são desenhados como uma série de triângulos.</span><span class="sxs-lookup"><span data-stu-id="fa7ee-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="fa7ee-120">Os glifos não serão renderizados para o dispositivo; O [**DrawText**](id3dxfont--drawtext.md) ainda deve ser chamado para renderizar os glifos.</span><span class="sxs-lookup"><span data-stu-id="fa7ee-120">Glyphs will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the glyphs.</span></span> <span data-ttu-id="fa7ee-121">No entanto, ao pré-carregar glifos na memória de vídeo, o **DrawText** usará substancialmente menos recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="fa7ee-121">However, by pre-loading glyphs into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa7ee-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa7ee-122">Requirements</span></span>



| <span data-ttu-id="fa7ee-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa7ee-123">Requirement</span></span> | <span data-ttu-id="fa7ee-124">Valor</span><span class="sxs-lookup"><span data-stu-id="fa7ee-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa7ee-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa7ee-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fa7ee-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa7ee-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="fa7ee-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa7ee-127">Library</span></span><br/> | <dl> <span data-ttu-id="fa7ee-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa7ee-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fa7ee-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa7ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa7ee-130">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="fa7ee-130">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
