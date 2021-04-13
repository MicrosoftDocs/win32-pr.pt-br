---
description: Cria uma matriz de transformação afim 3D. Argumentos nulos são tratados como transformações de identidade.
ms.assetid: 54eac78f-57be-4a24-8dfb-0b519e97d6ca
title: Função D3DXMatrixAffineTransformation (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 025485f0015e6f2d85851c8f0919f5462b2bdc3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298737"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx9mathh"></a><span data-ttu-id="ea499-104">Função D3DXMatrixAffineTransformation (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="ea499-104">D3DXMatrixAffineTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="ea499-105">Cria uma matriz de transformação afim 3D.</span><span class="sxs-lookup"><span data-stu-id="ea499-105">Builds a 3D affine transformation matrix.</span></span> <span data-ttu-id="ea499-106">Argumentos **nulos** são tratados como transformações de identidade.</span><span class="sxs-lookup"><span data-stu-id="ea499-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea499-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea499-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_          FLOAT          Scaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="ea499-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea499-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea499-109">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ea499-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea499-110">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea499-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ea499-111">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="ea499-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ea499-112">*Dimensionamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea499-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea499-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea499-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea499-114">Fator de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="ea499-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="ea499-115">*pRotationCenter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea499-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea499-116">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ea499-116">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ea499-117">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , um ponto que identifica o centro da rotação.</span><span class="sxs-lookup"><span data-stu-id="ea499-117">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point identifying the center of rotation.</span></span> <span data-ttu-id="ea499-118">Se esse argumento for **nulo**, uma matriz <sub>RC</sub> de identidade M será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="ea499-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ea499-119">*protação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea499-119">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea499-120">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ea499-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ea499-121">Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que especifica a rotação.</span><span class="sxs-lookup"><span data-stu-id="ea499-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="ea499-122">Se esse argumento for **nulo**, uma matriz <sub>r</sub> de identidade M será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="ea499-122">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ea499-123">*pTranslation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea499-123">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea499-124">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ea499-124">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ea499-125">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) que representa a tradução.</span><span class="sxs-lookup"><span data-stu-id="ea499-125">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure representing the translation.</span></span> <span data-ttu-id="ea499-126">Se esse argumento for **nulo**, uma matriz de identidade MT será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="ea499-126">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea499-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea499-127">Return value</span></span>

<span data-ttu-id="ea499-128">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea499-128">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ea499-129">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é uma matriz de transformação afim.</span><span class="sxs-lookup"><span data-stu-id="ea499-129">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea499-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea499-130">Remarks</span></span>

<span data-ttu-id="ea499-131">Essa função calcula a matriz de transformação afim com a seguinte fórmula, com concatenação de matriz avaliada na ordem da esquerda para a direita:</span><span class="sxs-lookup"><span data-stu-id="ea499-131">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="ea499-132">M<sub>out</sub> = MS \* (M<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="ea499-132">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="ea499-133">onde:</span><span class="sxs-lookup"><span data-stu-id="ea499-133">where:</span></span>

<span data-ttu-id="ea499-134">M <sub>out</sub> = matriz de saída (*pout*)</span><span class="sxs-lookup"><span data-stu-id="ea499-134">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="ea499-135">MS = matriz de dimensionamento (*dimensionamento*)</span><span class="sxs-lookup"><span data-stu-id="ea499-135">Mₛ = scaling matrix (*Scaling*)</span></span>

<span data-ttu-id="ea499-136">M <sub>RC</sub> = centro da matriz de rotação (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="ea499-136">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="ea499-137">M <sub>r</sub> = matriz de rotação (*protação*)</span><span class="sxs-lookup"><span data-stu-id="ea499-137">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="ea499-138">MT = matriz de conversão (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="ea499-138">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="ea499-139">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="ea499-139">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ea499-140">Dessa forma, a função **D3DXMatrixAffineTransformation** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="ea499-140">In this way, the **D3DXMatrixAffineTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ea499-141">Para transformações de afinidade 2D, use [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).</span><span class="sxs-lookup"><span data-stu-id="ea499-141">For 2D affine transformations, use [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea499-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea499-142">Requirements</span></span>



| <span data-ttu-id="ea499-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea499-143">Requirement</span></span> | <span data-ttu-id="ea499-144">Valor</span><span class="sxs-lookup"><span data-stu-id="ea499-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea499-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea499-145">Header</span></span><br/>  | <dl> <span data-ttu-id="ea499-146"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea499-146"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ea499-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea499-147">Library</span></span><br/> | <dl> <span data-ttu-id="ea499-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea499-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ea499-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea499-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea499-150">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="ea499-150">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ea499-151">**D3DXMatrixTransformation**</span><span class="sxs-lookup"><span data-stu-id="ea499-151">**D3DXMatrixTransformation**</span></span>](d3dxmatrixtransformation.md)
</dt> <dt>

[<span data-ttu-id="ea499-152">Transformações (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ea499-152">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
