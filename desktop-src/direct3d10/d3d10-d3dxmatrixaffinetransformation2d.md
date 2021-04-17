---
description: Cria uma matriz de transformação afim 2D no plano x-y. Argumentos nulos são tratados como transformações de identidade.
ms.assetid: f46a307c-4566-42c8-8def-fb189116144e
title: Função D3DXMatrixAffineTransformation2D (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation2D
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 223ef5d2d9a68c993553d52f5d4cf63e8b95dd3b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763195"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx10mathh"></a><span data-ttu-id="6d5be-104">Função D3DXMatrixAffineTransformation2D (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="6d5be-104">D3DXMatrixAffineTransformation2D function (D3DX10Math.h)</span></span>

<span data-ttu-id="6d5be-105">Cria uma matriz de transformação afim 2D no plano x-y.</span><span class="sxs-lookup"><span data-stu-id="6d5be-105">Builds a 2D affine transformation matrix in the x-y plane.</span></span> <span data-ttu-id="6d5be-106">Argumentos **nulos** são tratados como transformações de identidade.</span><span class="sxs-lookup"><span data-stu-id="6d5be-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d5be-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d5be-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _In_       D3DXMATRIX  *pOut,
  _In_       FLOAT       Scaling,
  _In_ const D3DXVECTOR2 *pRotationCenter,
  _In_       FLOAT       Rotation,
  _In_ const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="6d5be-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d5be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d5be-109">*pout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d5be-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5be-110">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6d5be-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6d5be-111">Ponteiro para o [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="6d5be-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6d5be-112">*Dimensionamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d5be-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5be-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d5be-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6d5be-114">Fator de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="6d5be-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="6d5be-115">*pRotationCenter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d5be-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5be-116">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="6d5be-116">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="6d5be-117">Ponteiro para um [**D3DXVECTOR2**](d3d10-d3dxvector2.md), um ponto que identifica o centro da rotação.</span><span class="sxs-lookup"><span data-stu-id="6d5be-117">Pointer to a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), a point identifying the center of rotation.</span></span> <span data-ttu-id="6d5be-118">Se esse argumento for **nulo**, uma matriz <sub>RC</sub> de identidade M será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="6d5be-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6d5be-119">*Rotação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d5be-119">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5be-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d5be-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6d5be-121">O ângulo de rotação.</span><span class="sxs-lookup"><span data-stu-id="6d5be-121">The angle of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="6d5be-122">*pTranslation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d5be-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d5be-123">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="6d5be-123">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="6d5be-124">Ponteiro para um [**D3DXVECTOR2**](d3d10-d3dxvector2.md), que representa a tradução.</span><span class="sxs-lookup"><span data-stu-id="6d5be-124">Pointer to a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), representing the translation.</span></span> <span data-ttu-id="6d5be-125">Se esse argumento for **nulo**, uma matriz de identidade MT será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="6d5be-125">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d5be-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d5be-126">Return value</span></span>

<span data-ttu-id="6d5be-127">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6d5be-127">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6d5be-128">Ponteiro para uma estrutura D3DXMATRIX que é uma matriz de transformação afim.</span><span class="sxs-lookup"><span data-stu-id="6d5be-128">Pointer to a D3DXMATRIX structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d5be-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d5be-129">Remarks</span></span>

<span data-ttu-id="6d5be-130">Essa função calcula a matriz de transformação afim com a seguinte fórmula, com concatenação de matriz avaliada na ordem da esquerda para a direita:</span><span class="sxs-lookup"><span data-stu-id="6d5be-130">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="6d5be-131">M<sub>out</sub> = MS \* (M<sub>RC</sub>)-1 \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="6d5be-131">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="6d5be-132">onde:</span><span class="sxs-lookup"><span data-stu-id="6d5be-132">where:</span></span>

<span data-ttu-id="6d5be-133">M<sub>out</sub> = matriz de saída (pout)</span><span class="sxs-lookup"><span data-stu-id="6d5be-133">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="6d5be-134">MS = matriz de dimensionamento (dimensionamento)</span><span class="sxs-lookup"><span data-stu-id="6d5be-134">Mₛ = scaling matrix (Scaling)</span></span>

<span data-ttu-id="6d5be-135">M<sub>RC</sub> = centro da matriz de rotação (pRotationCenter)</span><span class="sxs-lookup"><span data-stu-id="6d5be-135">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="6d5be-136">M<sub>r</sub> = matriz de rotação (rotação)</span><span class="sxs-lookup"><span data-stu-id="6d5be-136">M<sub>r</sub> = rotation matrix (Rotation)</span></span>

<span data-ttu-id="6d5be-137">MT = matriz de conversão (pTranslation)</span><span class="sxs-lookup"><span data-stu-id="6d5be-137">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="6d5be-138">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="6d5be-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6d5be-139">Dessa forma, a função D3DXMatrixAffineTransformation2D pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="6d5be-139">In this way, the D3DXMatrixAffineTransformation2D function can be used as a parameter for another function.</span></span>

<span data-ttu-id="6d5be-140">Para transformações de afinidade 3D, use D3DXMatrixAffineTransformation.</span><span class="sxs-lookup"><span data-stu-id="6d5be-140">For 3D affine transformations, use D3DXMatrixAffineTransformation.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d5be-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d5be-141">Requirements</span></span>



| <span data-ttu-id="6d5be-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d5be-142">Requirement</span></span> | <span data-ttu-id="6d5be-143">Valor</span><span class="sxs-lookup"><span data-stu-id="6d5be-143">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d5be-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d5be-144">Header</span></span><br/>  | <dl> <span data-ttu-id="6d5be-145"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d5be-145"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="6d5be-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d5be-146">Library</span></span><br/> | <dl> <span data-ttu-id="6d5be-147"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d5be-147"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6d5be-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d5be-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d5be-149">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="6d5be-149">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
