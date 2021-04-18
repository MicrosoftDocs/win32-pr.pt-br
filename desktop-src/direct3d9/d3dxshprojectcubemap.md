---
description: Projeta uma função representada em um mapa de cubo em harmônicas esféricas (SH).
ms.assetid: da5a3195-801e-4f1c-b52c-9eafc6e2e7b4
title: Função D3DXSHProjectCubeMap (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHProjectCubeMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0e3e45b42907c47d8c7f1b9e5294738b8997cd6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105802111"
---
# <a name="d3dxshprojectcubemap-function"></a><span data-ttu-id="e7bbc-103">Função D3DXSHProjectCubeMap</span><span class="sxs-lookup"><span data-stu-id="e7bbc-103">D3DXSHProjectCubeMap function</span></span>

<span data-ttu-id="e7bbc-104">Projeta uma função representada em um mapa de cubo em harmônicas esféricas (SH).</span><span class="sxs-lookup"><span data-stu-id="e7bbc-104">Projects a function represented on a cube map into spherical harmonics (SH).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7bbc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7bbc-105">Syntax</span></span>


```C++
HRESULT D3DXSHProjectCubeMap(
  _In_ UINT                   Order,
  _In_ LPDIRECT3DCUBETEXTURE9 pCubeMap,
  _In_ FLOAT                  *pROut,
  _In_ FLOAT                  *pGOut,
  _In_ FLOAT                  *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="e7bbc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7bbc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7bbc-107">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7bbc-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bbc-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7bbc-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7bbc-109">Ordem da avaliação harmônica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="e7bbc-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="e7bbc-110">Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="e7bbc-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="e7bbc-111">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="e7bbc-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="e7bbc-112">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="e7bbc-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="e7bbc-113">*pCubeMap* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7bbc-113">*pCubeMap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bbc-114">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="e7bbc-114">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="e7bbc-115">Ponteiro para uma textura de cubo de origem.</span><span class="sxs-lookup"><span data-stu-id="e7bbc-115">Pointer to a source cube texture.</span></span> <span data-ttu-id="e7bbc-116">Consulte [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9).</span><span class="sxs-lookup"><span data-stu-id="e7bbc-116">See [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9).</span></span>

</dd> <dt>

<span data-ttu-id="e7bbc-117">*pROut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7bbc-117">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bbc-118">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7bbc-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e7bbc-119">Ponteiro para o vetor SH de saída para o componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="e7bbc-119">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="e7bbc-120">*pGOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7bbc-120">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bbc-121">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7bbc-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e7bbc-122">Ponteiro para o vetor SH de saída para o componente verde.</span><span class="sxs-lookup"><span data-stu-id="e7bbc-122">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="e7bbc-123">*pBOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7bbc-123">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bbc-124">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7bbc-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e7bbc-125">Ponteiro para o vetor SH de saída para o componente azul.</span><span class="sxs-lookup"><span data-stu-id="e7bbc-125">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7bbc-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7bbc-126">Return value</span></span>

<span data-ttu-id="e7bbc-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7bbc-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7bbc-128">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e7bbc-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e7bbc-129">Se a função falhar, o valor de retorno poderá ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e7bbc-129">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7bbc-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7bbc-130">Requirements</span></span>



| <span data-ttu-id="e7bbc-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7bbc-131">Requirement</span></span> | <span data-ttu-id="e7bbc-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e7bbc-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7bbc-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7bbc-133">Header</span></span><br/>  | <dl> <span data-ttu-id="e7bbc-134"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7bbc-134"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e7bbc-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7bbc-135">Library</span></span><br/> | <dl> <span data-ttu-id="e7bbc-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7bbc-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e7bbc-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7bbc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7bbc-138">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="e7bbc-138">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e7bbc-139">Transferência radiante de computação (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e7bbc-139">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
