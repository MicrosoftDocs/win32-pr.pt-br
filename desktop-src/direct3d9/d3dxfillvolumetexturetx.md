---
description: Usa uma função HLSL (linguagem de sombreamento de alto nível) compilada para preencher cada Texel de cada nível de mipmap de uma textura.
ms.assetid: f082e1d2-c433-482c-9288-58e5c558cdc5
title: Função D3DXFillVolumeTextureTX (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de310ee6171924a5d2b61071d47c421739f15833
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785327"
---
# <a name="d3dxfillvolumetexturetx-function"></a><span data-ttu-id="e5367-103">Função D3DXFillVolumeTextureTX</span><span class="sxs-lookup"><span data-stu-id="e5367-103">D3DXFillVolumeTextureTX function</span></span>

<span data-ttu-id="e5367-104">Usa uma função HLSL (linguagem de sombreamento de alto nível) compilada para preencher cada Texel de cada nível de mipmap de uma textura.</span><span class="sxs-lookup"><span data-stu-id="e5367-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5367-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5367-105">Syntax</span></span>


```C++
HRESULT D3DXFillVolumeTextureTX(
  _In_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER      pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="e5367-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5367-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5367-107">*pTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5367-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5367-108">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="e5367-108">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="e5367-109">Ponteiro para um objeto [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , representando a textura a ser preenchida.</span><span class="sxs-lookup"><span data-stu-id="e5367-109">Pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="e5367-110">*pTextureShader* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5367-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5367-111">Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="e5367-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="e5367-112">Ponteiro para um objeto sombreador de textura [**ID3DXTextureShader**](id3dxtextureshader.md) .</span><span class="sxs-lookup"><span data-stu-id="e5367-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5367-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e5367-113">Return value</span></span>

<span data-ttu-id="e5367-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e5367-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e5367-115">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e5367-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e5367-116">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e5367-116">If the function fails, the return value can be one of the following:D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5367-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5367-117">Remarks</span></span>

<span data-ttu-id="e5367-118">O destino de textura deve ser uma função HLSL que contenha a seguinte semântica:</span><span class="sxs-lookup"><span data-stu-id="e5367-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="e5367-119">Um parâmetro de entrada deve usar uma semântica de posição.</span><span class="sxs-lookup"><span data-stu-id="e5367-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="e5367-120">Um parâmetro de entrada deve usar uma semântica PSIZE.</span><span class="sxs-lookup"><span data-stu-id="e5367-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="e5367-121">A função deve retornar um parâmetro que usa a semântica de cor.</span><span class="sxs-lookup"><span data-stu-id="e5367-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="e5367-122">Os parâmetros de entrada podem estar em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="e5367-122">The input parameters can be in any order.</span></span> <span data-ttu-id="e5367-123">Para obter um exemplo, consulte [ **D3DXFillTextureTX**](d3dxfilltexturetx.md)</span><span class="sxs-lookup"><span data-stu-id="e5367-123">For an example, see [**D3DXFillTextureTX**](d3dxfilltexturetx.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="e5367-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5367-124">Requirements</span></span>



| <span data-ttu-id="e5367-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5367-125">Requirement</span></span> | <span data-ttu-id="e5367-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e5367-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5367-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5367-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e5367-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5367-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e5367-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e5367-129">Library</span></span><br/> | <dl> <span data-ttu-id="e5367-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5367-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e5367-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5367-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5367-132">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="e5367-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="e5367-133">**D3DXFillTextureTX**</span><span class="sxs-lookup"><span data-stu-id="e5367-133">**D3DXFillTextureTX**</span></span>](d3dxfilltexturetx.md)
</dt> <dt>

[<span data-ttu-id="e5367-134">**D3DXFillCubeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="e5367-134">**D3DXFillCubeTextureTX**</span></span>](d3dxfillcubetexturetx.md)
</dt> </dl>

 

 
