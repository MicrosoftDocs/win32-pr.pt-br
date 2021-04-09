---
description: Usa uma função HLSL (linguagem de sombreamento de alto nível) compilada para preencher cada Texel de cada nível de mipmap de uma textura.
ms.assetid: 013660ce-865e-4acf-a1ea-670e70377ff5
title: Função D3DXFillTextureTX (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3605011f7967edec68d13405b4cabbd9c90d4c59
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012094"
---
# <a name="d3dxfilltexturetx-function"></a><span data-ttu-id="c991e-103">Função D3DXFillTextureTX</span><span class="sxs-lookup"><span data-stu-id="c991e-103">D3DXFillTextureTX function</span></span>

<span data-ttu-id="c991e-104">Usa uma função HLSL (linguagem de sombreamento de alto nível) compilada para preencher cada Texel de cada nível de mipmap de uma textura.</span><span class="sxs-lookup"><span data-stu-id="c991e-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c991e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c991e-105">Syntax</span></span>


```C++
HRESULT D3DXFillTextureTX(
  _Inout_ LPDIRECT3DTEXTURE9  pTexture,
  _In_    LPD3DXTEXTURESHADER pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="c991e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c991e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c991e-107">*pTexture* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="c991e-107">*pTexture* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c991e-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="c991e-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="c991e-109">Ponteiro para um objeto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , representando a textura a ser preenchida.</span><span class="sxs-lookup"><span data-stu-id="c991e-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="c991e-110">*pTextureShader* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c991e-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c991e-111">Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="c991e-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="c991e-112">Ponteiro para um objeto sombreador de textura [**ID3DXTextureShader**](id3dxtextureshader.md) .</span><span class="sxs-lookup"><span data-stu-id="c991e-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c991e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c991e-113">Return value</span></span>

<span data-ttu-id="c991e-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c991e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c991e-115">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c991e-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c991e-116">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c991e-116">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c991e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c991e-117">Remarks</span></span>

<span data-ttu-id="c991e-118">O destino de textura deve ser uma função HLSL que contenha a seguinte semântica:</span><span class="sxs-lookup"><span data-stu-id="c991e-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="c991e-119">Um parâmetro de entrada deve usar uma semântica de posição.</span><span class="sxs-lookup"><span data-stu-id="c991e-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="c991e-120">Um parâmetro de entrada deve usar uma semântica PSIZE.</span><span class="sxs-lookup"><span data-stu-id="c991e-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="c991e-121">A função deve retornar um parâmetro que usa a semântica de cor.</span><span class="sxs-lookup"><span data-stu-id="c991e-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="c991e-122">Veja a seguir um exemplo de tal função HLSL:</span><span class="sxs-lookup"><span data-stu-id="c991e-122">The following is an example of such an HLSL function:</span></span>


```
float4 TextureGradientFill(
  float2 vTexCoord : POSITION, 
  float2 vTexelSize : PSIZE) : COLOR 
  {
    float r,g, b, xSq,ySq, a;
    xSq = 2.f*vTexCoord.x-1.f; xSq *= xSq;
    ySq = 2.f*vTexCoord.y-1.f; ySq *= ySq;
    a = sqrt(xSq+ySq);
    if (a > 1.0f) {
        a = 1.0f-(a-1.0f);
    }
    else if (a < 0.2f) {
        a = 0.2f;
    }
    r = 1-vTexCoord.x;
    g = 1-vTexCoord.y;
    b = vTexCoord.x;
    return float4(r, g, b, a);
    
  };
```



<span data-ttu-id="c991e-123">Observe que os parâmetros de entrada podem estar em qualquer ordem, mas a semântica de entrada deve ser representada.</span><span class="sxs-lookup"><span data-stu-id="c991e-123">Note that the input parameters can be in any order, but both input semantics must be represented.</span></span>

## <a name="requirements"></a><span data-ttu-id="c991e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c991e-124">Requirements</span></span>



| <span data-ttu-id="c991e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c991e-125">Requirement</span></span> | <span data-ttu-id="c991e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c991e-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c991e-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c991e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c991e-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="c991e-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c991e-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c991e-129">Library</span></span><br/> | <dl> <span data-ttu-id="c991e-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c991e-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c991e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c991e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c991e-132">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="c991e-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="c991e-133">**D3DXFillCubeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="c991e-133">**D3DXFillCubeTextureTX**</span></span>](d3dxfillcubetexturetx.md)
</dt> <dt>

[<span data-ttu-id="c991e-134">**D3DXFillVolumeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="c991e-134">**D3DXFillVolumeTextureTX**</span></span>](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
