---
description: Usa uma função fornecida pelo usuário para preencher cada Texel de cada nível de MIP de uma determinada textura de volume.
ms.assetid: cc9eb051-8a62-4e35-87df-c255f10e94d8
title: Função D3DXFillVolumeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d817470f0f0617001fd83054e24e8881ac9a3a1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298621"
---
# <a name="d3dxfillvolumetexture-function"></a><span data-ttu-id="99b7f-103">Função D3DXFillVolumeTexture</span><span class="sxs-lookup"><span data-stu-id="99b7f-103">D3DXFillVolumeTexture function</span></span>

<span data-ttu-id="99b7f-104">Usa uma função fornecida pelo usuário para preencher cada Texel de cada nível de MIP de uma determinada textura de volume.</span><span class="sxs-lookup"><span data-stu-id="99b7f-104">Uses a user-provided function to fill each texel of each mip level of a given volume texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="99b7f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99b7f-105">Syntax</span></span>


```C++
HRESULT D3DXFillVolumeTexture(
  _Out_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D             pFunction,
  _In_  LPVOID                   pData
);
```



## <a name="parameters"></a><span data-ttu-id="99b7f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99b7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b7f-107">*pTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="99b7f-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99b7f-108">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="99b7f-108">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="99b7f-109">Ponteiro para uma interface [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , representando a textura preenchida.</span><span class="sxs-lookup"><span data-stu-id="99b7f-109">Pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="99b7f-110">*pFunction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99b7f-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b7f-111">Tipo: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span><span class="sxs-lookup"><span data-stu-id="99b7f-111">Type: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span></span>

<span data-ttu-id="99b7f-112">Ponteiro para uma função de avaliador fornecida pelo usuário, que será usada para calcular o valor de cada Texel.</span><span class="sxs-lookup"><span data-stu-id="99b7f-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="99b7f-113">A função segue o protótipo de [LPD3DXFILL3D](lpd3dxfill3d.md).</span><span class="sxs-lookup"><span data-stu-id="99b7f-113">The function follows the prototype of [LPD3DXFILL3D](lpd3dxfill3d.md).</span></span>

</dd> <dt>

<span data-ttu-id="99b7f-114">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99b7f-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b7f-115">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99b7f-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99b7f-116">Ponteiro para um bloco arbitrário de dados definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="99b7f-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="99b7f-117">Esse ponteiro será passado para a função fornecida em *pFunction*.</span><span class="sxs-lookup"><span data-stu-id="99b7f-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99b7f-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99b7f-118">Return value</span></span>

<span data-ttu-id="99b7f-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99b7f-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99b7f-120">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99b7f-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="99b7f-121">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="99b7f-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="99b7f-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="99b7f-122">Remarks</span></span>

<span data-ttu-id="99b7f-123">Se o volume for não dinâmico (porque o uso está definido como 0 quando é criado) e localizado na memória de vídeo (o pool de memória definido como D3DPOOL \_ padrão), **D3DXFillVolumeTexture** falhará porque o volume não pode ser bloqueado.</span><span class="sxs-lookup"><span data-stu-id="99b7f-123">If the volume is non-dynamic (because usage is set to 0 when it is created), and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), **D3DXFillVolumeTexture** will fail because the volume cannot be locked.</span></span>

<span data-ttu-id="99b7f-124">Este exemplo cria uma função chamada ColorVolumeFill, que se baseia em D3DXFillVolumeTexture.</span><span class="sxs-lookup"><span data-stu-id="99b7f-124">This example creates a function called ColorVolumeFill, which relies on D3DXFillVolumeTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorVolumeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
   *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill volume texture
if (FAILED (hr = D3DXFillVolumeTexture (m_pTexture, ColorVolumeFill, NULL)))
{
       return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="99b7f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99b7f-125">Requirements</span></span>



| <span data-ttu-id="99b7f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="99b7f-126">Requirement</span></span> | <span data-ttu-id="99b7f-127">Valor</span><span class="sxs-lookup"><span data-stu-id="99b7f-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99b7f-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="99b7f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="99b7f-129"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="99b7f-129"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="99b7f-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99b7f-130">Library</span></span><br/> | <dl> <span data-ttu-id="99b7f-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99b7f-131"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="99b7f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="99b7f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b7f-133">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="99b7f-133">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
