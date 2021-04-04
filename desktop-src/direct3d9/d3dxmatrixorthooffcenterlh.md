---
description: Cria uma matriz de projeção ortográfica personalizada de mão esquerda.
ms.assetid: e4f087e5-63d9-49ca-9d8e-3a25070e1a51
title: Função D3DXMatrixOrthoOffCenterLH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1e286197233b2abb2b19138b8fc9d154df355a6a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930686"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx9mathh"></a><span data-ttu-id="c2dfb-103">Função D3DXMatrixOrthoOffCenterLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c2dfb-103">D3DXMatrixOrthoOffCenterLH function (D3dx9math.h)</span></span>

<span data-ttu-id="c2dfb-104">Cria uma matriz de projeção ortográfica personalizada de mão esquerda.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-104">Builds a customized, left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2dfb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2dfb-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="c2dfb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2dfb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2dfb-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="c2dfb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2dfb-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c2dfb-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c2dfb-109">Ponteiro para o [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2dfb-110">*l* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="c2dfb-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2dfb-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2dfb-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2dfb-112">Valor x mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c2dfb-113">*r* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="c2dfb-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2dfb-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2dfb-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2dfb-115">Valor x máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c2dfb-116">*b* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="c2dfb-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2dfb-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2dfb-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2dfb-118">Valor y mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c2dfb-119">*t* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="c2dfb-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2dfb-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2dfb-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2dfb-121">Valor y máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c2dfb-122">*Zn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2dfb-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2dfb-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2dfb-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2dfb-124">Valor z mínimo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c2dfb-125">*ZF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2dfb-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2dfb-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2dfb-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2dfb-127">Valor z máximo do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2dfb-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2dfb-128">Return value</span></span>

<span data-ttu-id="c2dfb-129">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c2dfb-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c2dfb-130">Ponteiro para o [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-130">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c2dfb-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2dfb-131">Remarks</span></span>

<span data-ttu-id="c2dfb-132">A função [**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md) é um caso especial da função **D3DXMatrixOrthoOffCenterLH** .</span><span class="sxs-lookup"><span data-stu-id="c2dfb-132">The [**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md) function is a special case of the **D3DXMatrixOrthoOffCenterLH** function.</span></span> <span data-ttu-id="c2dfb-133">Para criar a mesma projeção usando **D3DXMatrixOrthoOffCenterLH**, use os seguintes valores: l =-w/2, r = w/2, b =-h/2 e t = h/2.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-133">To create the same projection using **D3DXMatrixOrthoOffCenterLH**, use the following values: l = -w/2, r = w/2, b = -h/2, and t = h/2.</span></span>

<span data-ttu-id="c2dfb-134">Todos os parâmetros da função **D3DXMatrixOrthoOffCenterLH** são distâncias no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-134">All the parameters of the **D3DXMatrixOrthoOffCenterLH** function are distances in camera space.</span></span> <span data-ttu-id="c2dfb-135">Os parâmetros descrevem as dimensões do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-135">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="c2dfb-136">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="c2dfb-136">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c2dfb-137">Dessa forma, a função **D3DXMatrixOrthoOffCenterLH** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-137">In this way, the **D3DXMatrixOrthoOffCenterLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c2dfb-138">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-138">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="c2dfb-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2dfb-139">Requirements</span></span>



| <span data-ttu-id="c2dfb-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2dfb-140">Requirement</span></span> | <span data-ttu-id="c2dfb-141">Valor</span><span class="sxs-lookup"><span data-stu-id="c2dfb-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2dfb-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2dfb-142">Header</span></span><br/>  | <dl> <span data-ttu-id="c2dfb-143"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2dfb-143"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c2dfb-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c2dfb-144">Library</span></span><br/> | <dl> <span data-ttu-id="c2dfb-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2dfb-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c2dfb-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2dfb-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2dfb-147">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="c2dfb-147">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c2dfb-148">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="c2dfb-148">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="c2dfb-149">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="c2dfb-149">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="c2dfb-150">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="c2dfb-150">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> </dl>

 

 
