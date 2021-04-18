---
description: Cria uma matriz de transformação afim 2D no plano XY. Argumentos nulos são tratados como transformações de identidade.
ms.assetid: 335de919-ae4d-405d-b6bb-ca6bdc2d568a
title: Função D3DXMatrixAffineTransformation2D (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6edd0658eb80ec53d19b6c136a672cb78a2087b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105786279"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx9mathh"></a><span data-ttu-id="75f5b-104">Função D3DXMatrixAffineTransformation2D (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="75f5b-104">D3DXMatrixAffineTransformation2D function (D3dx9math.h)</span></span>

<span data-ttu-id="75f5b-105">Cria uma matriz de transformação afim 2D no plano XY.</span><span class="sxs-lookup"><span data-stu-id="75f5b-105">Builds a 2D affine transformation matrix in the xy plane.</span></span> <span data-ttu-id="75f5b-106">Argumentos **nulos** são tratados como transformações de identidade.</span><span class="sxs-lookup"><span data-stu-id="75f5b-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="75f5b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75f5b-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_          FLOAT       Scaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="75f5b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75f5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75f5b-109">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="75f5b-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="75f5b-110">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="75f5b-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="75f5b-111">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="75f5b-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="75f5b-112">*Dimensionamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75f5b-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75f5b-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75f5b-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75f5b-114">Fator de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="75f5b-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="75f5b-115">*pRotationCenter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75f5b-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75f5b-116">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="75f5b-116">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="75f5b-117">Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) , um ponto que identifica o centro da rotação.</span><span class="sxs-lookup"><span data-stu-id="75f5b-117">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the center of rotation.</span></span> <span data-ttu-id="75f5b-118">Se esse argumento for **nulo**, uma matriz <sub>RC</sub> de identidade M será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="75f5b-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="75f5b-119">*Rotação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75f5b-119">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75f5b-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75f5b-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75f5b-121">O ângulo de rotação.</span><span class="sxs-lookup"><span data-stu-id="75f5b-121">The angle of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="75f5b-122">*pTranslation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75f5b-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75f5b-123">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="75f5b-123">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="75f5b-124">Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) , representando a tradução.</span><span class="sxs-lookup"><span data-stu-id="75f5b-124">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, representing the translation.</span></span> <span data-ttu-id="75f5b-125">Se esse argumento for **nulo**, uma matriz de identidade MT será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="75f5b-125">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75f5b-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75f5b-126">Return value</span></span>

<span data-ttu-id="75f5b-127">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="75f5b-127">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="75f5b-128">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é uma matriz de transformação afim.</span><span class="sxs-lookup"><span data-stu-id="75f5b-128">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="75f5b-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="75f5b-129">Remarks</span></span>

<span data-ttu-id="75f5b-130">Essa função calcula a matriz de transformação afim com a seguinte fórmula, com concatenação de matriz avaliada na ordem da esquerda para a direita:</span><span class="sxs-lookup"><span data-stu-id="75f5b-130">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="75f5b-131">M<sub>out</sub> = MS \* (M<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="75f5b-131">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="75f5b-132">onde:</span><span class="sxs-lookup"><span data-stu-id="75f5b-132">where:</span></span>

<span data-ttu-id="75f5b-133">M <sub>out</sub> = matriz de saída (*pout*)</span><span class="sxs-lookup"><span data-stu-id="75f5b-133">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="75f5b-134">MS = matriz de dimensionamento (*dimensionamento*)</span><span class="sxs-lookup"><span data-stu-id="75f5b-134">Mₛ = scaling matrix (*Scaling*)</span></span>

<span data-ttu-id="75f5b-135">M <sub>RC</sub> = centro da matriz de rotação (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="75f5b-135">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="75f5b-136">M <sub>r</sub> = matriz de rotação (*rotação*)</span><span class="sxs-lookup"><span data-stu-id="75f5b-136">M <sub>r</sub> = rotation matrix (*Rotation*)</span></span>

<span data-ttu-id="75f5b-137">MT = matriz de conversão (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="75f5b-137">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="75f5b-138">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="75f5b-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="75f5b-139">Dessa forma, a função **D3DXMatrixAffineTransformation2D** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="75f5b-139">In this way, the **D3DXMatrixAffineTransformation2D** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="75f5b-140">Para transformações de afinidade 3D, use [**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md).</span><span class="sxs-lookup"><span data-stu-id="75f5b-140">For 3D affine transformations, use [**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75f5b-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75f5b-141">Requirements</span></span>



| <span data-ttu-id="75f5b-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="75f5b-142">Requirement</span></span> | <span data-ttu-id="75f5b-143">Valor</span><span class="sxs-lookup"><span data-stu-id="75f5b-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75f5b-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75f5b-144">Header</span></span><br/>  | <dl> <span data-ttu-id="75f5b-145"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="75f5b-145"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="75f5b-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75f5b-146">Library</span></span><br/> | <dl> <span data-ttu-id="75f5b-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75f5b-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="75f5b-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="75f5b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75f5b-149">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="75f5b-149">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="75f5b-150">**D3DXMatrixTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="75f5b-150">**D3DXMatrixTransformation2D**</span></span>](d3dxmatrixtransformation2d.md)
</dt> <dt>

[<span data-ttu-id="75f5b-151">Transformações (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="75f5b-151">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
