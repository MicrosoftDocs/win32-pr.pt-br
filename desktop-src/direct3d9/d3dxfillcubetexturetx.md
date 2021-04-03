---
description: Usa uma função HLSL (linguagem de sombreamento de alto nível) compilada para preencher cada Texel de cada nível de mipmap de uma textura.
ms.assetid: a0c36967-57e6-4771-8e9f-f32949c12001
title: Função D3DXFillCubeTextureTX (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 37a831ef95d50f9b0389be0f1c9937e46748f6d3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664005"
---
# <a name="d3dxfillcubetexturetx-function"></a><span data-ttu-id="6154e-103">Função D3DXFillCubeTextureTX</span><span class="sxs-lookup"><span data-stu-id="6154e-103">D3DXFillCubeTextureTX function</span></span>

<span data-ttu-id="6154e-104">Usa uma função HLSL (linguagem de sombreamento de alto nível) compilada para preencher cada Texel de cada nível de mipmap de uma textura.</span><span class="sxs-lookup"><span data-stu-id="6154e-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="6154e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6154e-105">Syntax</span></span>


```C++
HRESULT D3DXFillCubeTextureTX(
  _In_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER    pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="6154e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6154e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6154e-107">*pTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6154e-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6154e-108">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="6154e-108">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="6154e-109">Ponteiro para um objeto [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , representando a textura a ser preenchida.</span><span class="sxs-lookup"><span data-stu-id="6154e-109">Pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="6154e-110">*pTextureShader* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6154e-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6154e-111">Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="6154e-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="6154e-112">Ponteiro para um objeto sombreador de textura [**ID3DXTextureShader**](id3dxtextureshader.md) .</span><span class="sxs-lookup"><span data-stu-id="6154e-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6154e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6154e-113">Return value</span></span>

<span data-ttu-id="6154e-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6154e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6154e-115">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6154e-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6154e-116">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6154e-116">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6154e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6154e-117">Remarks</span></span>

<span data-ttu-id="6154e-118">O destino de textura deve ser uma função HLSL que contenha a seguinte semântica:</span><span class="sxs-lookup"><span data-stu-id="6154e-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="6154e-119">Um parâmetro de entrada deve usar uma semântica de posição.</span><span class="sxs-lookup"><span data-stu-id="6154e-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="6154e-120">Um parâmetro de entrada deve usar uma semântica PSIZE.</span><span class="sxs-lookup"><span data-stu-id="6154e-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="6154e-121">A função deve retornar um parâmetro que usa a semântica de cor.</span><span class="sxs-lookup"><span data-stu-id="6154e-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="6154e-122">Os parâmetros de entrada podem estar em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="6154e-122">The input parameters can be in any order.</span></span> <span data-ttu-id="6154e-123">Para obter um exemplo, consulte [ **D3DXFillTextureTX**](d3dxfilltexturetx.md)</span><span class="sxs-lookup"><span data-stu-id="6154e-123">For an example, see [**D3DXFillTextureTX**](d3dxfilltexturetx.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="6154e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6154e-124">Requirements</span></span>



| <span data-ttu-id="6154e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6154e-125">Requirement</span></span> | <span data-ttu-id="6154e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6154e-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6154e-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6154e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6154e-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6154e-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6154e-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6154e-129">Library</span></span><br/> | <dl> <span data-ttu-id="6154e-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6154e-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6154e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="6154e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6154e-132">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="6154e-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="6154e-133">**D3DXFillVolumeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="6154e-133">**D3DXFillVolumeTextureTX**</span></span>](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
