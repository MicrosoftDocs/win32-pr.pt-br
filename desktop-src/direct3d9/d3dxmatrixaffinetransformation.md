---
description: Função D3DXMatrixAffineTransformation (D3dx9math. h) – compila uma matriz de transformação afim 3D. Argumentos nulos são tratados como transformações de identidade.
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
ms.openlocfilehash: 7329ffbffe5ffd89ed64e5386246f39699618960
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094164"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx9mathh"></a><span data-ttu-id="7931a-104">Função D3DXMatrixAffineTransformation (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="7931a-104">D3DXMatrixAffineTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="7931a-105">Cria uma matriz de transformação afim 3D.</span><span class="sxs-lookup"><span data-stu-id="7931a-105">Builds a 3D affine transformation matrix.</span></span> <span data-ttu-id="7931a-106">Argumentos **nulos** são tratados como transformações de identidade.</span><span class="sxs-lookup"><span data-stu-id="7931a-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="7931a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7931a-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_          FLOAT          Scaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="7931a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7931a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7931a-109">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7931a-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7931a-110">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7931a-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7931a-111">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="7931a-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7931a-112">*Dimensionamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7931a-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7931a-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7931a-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7931a-114">Fator de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="7931a-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="7931a-115">*pRotationCenter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7931a-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7931a-116">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7931a-116">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7931a-117">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , um ponto que identifica o centro da rotação.</span><span class="sxs-lookup"><span data-stu-id="7931a-117">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point identifying the center of rotation.</span></span> <span data-ttu-id="7931a-118">Se esse argumento for **nulo**, uma matriz <sub>RC</sub> de identidade M será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="7931a-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7931a-119">*protação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7931a-119">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7931a-120">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="7931a-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7931a-121">Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que especifica a rotação.</span><span class="sxs-lookup"><span data-stu-id="7931a-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="7931a-122">Se esse argumento for **nulo**, uma matriz <sub>r</sub> de identidade M será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="7931a-122">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7931a-123">*pTranslation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7931a-123">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7931a-124">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7931a-124">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7931a-125">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) que representa a tradução.</span><span class="sxs-lookup"><span data-stu-id="7931a-125">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure representing the translation.</span></span> <span data-ttu-id="7931a-126">Se esse argumento for **nulo**, uma matriz de identidade MT será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="7931a-126">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7931a-127">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7931a-127">Return value</span></span>

<span data-ttu-id="7931a-128">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7931a-128">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7931a-129">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é uma matriz de transformação afim.</span><span class="sxs-lookup"><span data-stu-id="7931a-129">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="7931a-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="7931a-130">Remarks</span></span>

<span data-ttu-id="7931a-131">Essa função calcula a matriz de transformação afim com a seguinte fórmula, com concatenação de matriz avaliada na ordem da esquerda para a direita:</span><span class="sxs-lookup"><span data-stu-id="7931a-131">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="7931a-132">M<sub>out</sub> = MS \* (M<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="7931a-132">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="7931a-133">em que:</span><span class="sxs-lookup"><span data-stu-id="7931a-133">where:</span></span>

<span data-ttu-id="7931a-134">M <sub>out</sub> = matriz de saída (*pout*)</span><span class="sxs-lookup"><span data-stu-id="7931a-134">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="7931a-135">MS = matriz de dimensionamento (*dimensionamento*)</span><span class="sxs-lookup"><span data-stu-id="7931a-135">Mₛ = scaling matrix (*Scaling*)</span></span>

<span data-ttu-id="7931a-136">M <sub>RC</sub> = centro da matriz de rotação (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="7931a-136">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="7931a-137">M <sub>r</sub> = matriz de rotação (*protação*)</span><span class="sxs-lookup"><span data-stu-id="7931a-137">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="7931a-138">MT = matriz de conversão (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="7931a-138">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="7931a-139">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="7931a-139">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="7931a-140">Dessa forma, a função **D3DXMatrixAffineTransformation** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="7931a-140">In this way, the **D3DXMatrixAffineTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="7931a-141">Para transformações de afinidade 2D, use [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).</span><span class="sxs-lookup"><span data-stu-id="7931a-141">For 2D affine transformations, use [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7931a-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7931a-142">Requirements</span></span>



| <span data-ttu-id="7931a-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="7931a-143">Requirement</span></span> | <span data-ttu-id="7931a-144">Valor</span><span class="sxs-lookup"><span data-stu-id="7931a-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7931a-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7931a-145">Header</span></span><br/>  | <dl> <span data-ttu-id="7931a-146"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7931a-146"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7931a-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7931a-147">Library</span></span><br/> | <dl> <span data-ttu-id="7931a-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7931a-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7931a-149">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7931a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7931a-150">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="7931a-150">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7931a-151">**D3DXMatrixTransformation**</span><span class="sxs-lookup"><span data-stu-id="7931a-151">**D3DXMatrixTransformation**</span></span>](d3dxmatrixtransformation.md)
</dt> <dt>

[<span data-ttu-id="7931a-152">Transformações (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7931a-152">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
