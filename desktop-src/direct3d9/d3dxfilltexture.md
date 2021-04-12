---
description: Usa uma função fornecida pelo usuário para preencher cada Texel de cada nível de MIP de uma determinada textura.
ms.assetid: 9c822472-2bbf-4629-bdb3-6491573e8de2
title: Função D3DXFillTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20790a9e4c1a9ce242a5e067dd617c7871a70b7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298622"
---
# <a name="d3dxfilltexture-function"></a><span data-ttu-id="443d1-103">Função D3DXFillTexture</span><span class="sxs-lookup"><span data-stu-id="443d1-103">D3DXFillTexture function</span></span>

<span data-ttu-id="443d1-104">Usa uma função fornecida pelo usuário para preencher cada Texel de cada nível de MIP de uma determinada textura.</span><span class="sxs-lookup"><span data-stu-id="443d1-104">Uses a user-provided function to fill each texel of each mip level of a given texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="443d1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="443d1-105">Syntax</span></span>


```C++
HRESULT D3DXFillTexture(
  _Out_ LPDIRECT3DTEXTURE9 pTexture,
  _In_  LPD3DXFILL2D       pFunction,
  _In_  LPVOID             pData
);
```



## <a name="parameters"></a><span data-ttu-id="443d1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="443d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="443d1-107">*pTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="443d1-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="443d1-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="443d1-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="443d1-109">Ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , representando a textura preenchida.</span><span class="sxs-lookup"><span data-stu-id="443d1-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="443d1-110">*pFunction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="443d1-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="443d1-111">Tipo: **[LPD3DXFILL2D](lpd3dxfill2d.md)**</span><span class="sxs-lookup"><span data-stu-id="443d1-111">Type: **[LPD3DXFILL2D](lpd3dxfill2d.md)**</span></span>

<span data-ttu-id="443d1-112">Ponteiro para uma função de avaliador fornecida pelo usuário, que será usada para calcular o valor de cada Texel.</span><span class="sxs-lookup"><span data-stu-id="443d1-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="443d1-113">A função segue o protótipo de [LPD3DXFILL2D](lpd3dxfill2d.md).</span><span class="sxs-lookup"><span data-stu-id="443d1-113">The function follows the prototype of [LPD3DXFILL2D](lpd3dxfill2d.md).</span></span>

</dd> <dt>

<span data-ttu-id="443d1-114">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="443d1-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="443d1-115">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="443d1-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="443d1-116">Ponteiro para um bloco arbitrário de dados definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="443d1-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="443d1-117">Esse ponteiro será passado para a função fornecida em *pFunction*.</span><span class="sxs-lookup"><span data-stu-id="443d1-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="443d1-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="443d1-118">Return value</span></span>

<span data-ttu-id="443d1-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="443d1-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="443d1-120">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="443d1-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="443d1-121">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="443d1-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="443d1-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="443d1-122">Remarks</span></span>

<span data-ttu-id="443d1-123">Aqui está um exemplo que cria uma função chamada ColorFill, que se baseia em D3DXFillTexture.</span><span class="sxs-lookup"><span data-stu-id="443d1-123">Here is an example that creates a function called ColorFill, which relies on D3DXFillTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorFill (D3DXVECTOR4* pOut, const D3DXVECTOR2* pTexCoord, 
const D3DXVECTOR2* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, 0.0f, 0.0f);
}
    
    
// Fill the texture using D3DXFillTexture
if (FAILED (hr = D3DXFillTexture (m_pTexture, ColorFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="443d1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="443d1-124">Requirements</span></span>



| <span data-ttu-id="443d1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="443d1-125">Requirement</span></span> | <span data-ttu-id="443d1-126">Valor</span><span class="sxs-lookup"><span data-stu-id="443d1-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="443d1-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="443d1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="443d1-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="443d1-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="443d1-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="443d1-129">Library</span></span><br/> | <dl> <span data-ttu-id="443d1-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="443d1-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="443d1-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="443d1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="443d1-132">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="443d1-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
