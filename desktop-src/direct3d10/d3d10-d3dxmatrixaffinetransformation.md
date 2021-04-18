---
description: Cria uma matriz de transformação afim 3D. Argumentos nulos são tratados como transformações de identidade.
ms.assetid: 36044272-a8ce-47db-8f52-30dc680f8174
title: Função D3DXMatrixAffineTransformation (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 27fee5a620d75c3930b1bc2f8a85415db1320a47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781145"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx10mathh"></a><span data-ttu-id="b400e-104">Função D3DXMatrixAffineTransformation (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b400e-104">D3DXMatrixAffineTransformation function (D3DX10Math.h)</span></span>

<span data-ttu-id="b400e-105">Cria uma matriz de transformação afim 3D.</span><span class="sxs-lookup"><span data-stu-id="b400e-105">Builds a 3D affine transformation matrix.</span></span> <span data-ttu-id="b400e-106">Argumentos **nulos** são tratados como transformações de identidade.</span><span class="sxs-lookup"><span data-stu-id="b400e-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="b400e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b400e-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _In_       D3DXMATRIX     *pOut,
  _In_       FLOAT          Scaling,
  _In_ const D3DXVECTOR3    *pRotationCenter,
  _In_ const D3DXQUATERNION *pRotation,
  _In_ const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="b400e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b400e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b400e-109">*pout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b400e-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b400e-110">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b400e-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b400e-111">Ponteiro para o [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="b400e-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b400e-112">*Dimensionamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b400e-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b400e-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b400e-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b400e-114">Fator de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="b400e-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="b400e-115">*pRotationCenter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b400e-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b400e-116">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b400e-116">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b400e-117">Ponteiro para um [**D3DXVECTOR3**](d3d10-d3dxvector3.md), um ponto que identifica o centro da rotação.</span><span class="sxs-lookup"><span data-stu-id="b400e-117">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), a point identifying the center of rotation.</span></span> <span data-ttu-id="b400e-118">Se esse argumento for **nulo**, uma matriz <sub>RC</sub> de identidade M será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="b400e-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b400e-119">*protação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b400e-119">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b400e-120">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="b400e-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b400e-121">Ponteiro para um [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que especifica a rotação.</span><span class="sxs-lookup"><span data-stu-id="b400e-121">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that specifies the rotation.</span></span> <span data-ttu-id="b400e-122">Se esse argumento for **nulo**, uma matriz <sub>r</sub> de identidade M será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="b400e-122">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b400e-123">*pTranslation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b400e-123">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b400e-124">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b400e-124">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b400e-125">Ponteiro para uma estrutura D3DXVECTOR3 que representa a tradução.</span><span class="sxs-lookup"><span data-stu-id="b400e-125">Pointer to a D3DXVECTOR3 structure representing the translation.</span></span> <span data-ttu-id="b400e-126">Se esse argumento for **nulo**, uma matriz de identidade MT será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="b400e-126">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b400e-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b400e-127">Return value</span></span>

<span data-ttu-id="b400e-128">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b400e-128">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b400e-129">Ponteiro para uma estrutura D3DXMATRIX que é uma matriz de transformação afim.</span><span class="sxs-lookup"><span data-stu-id="b400e-129">Pointer to a D3DXMATRIX structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="b400e-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="b400e-130">Remarks</span></span>

<span data-ttu-id="b400e-131">Essa função calcula a matriz de transformação afim com a seguinte fórmula, com concatenação de matriz avaliada na ordem da esquerda para a direita:</span><span class="sxs-lookup"><span data-stu-id="b400e-131">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="b400e-132">M<sub>out</sub> = MS \* (M<sub>RC</sub>)-1 \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="b400e-132">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="b400e-133">onde:</span><span class="sxs-lookup"><span data-stu-id="b400e-133">where:</span></span>

<span data-ttu-id="b400e-134">M<sub>out</sub> = matriz de saída (pout)</span><span class="sxs-lookup"><span data-stu-id="b400e-134">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="b400e-135">MS = matriz de dimensionamento (dimensionamento)</span><span class="sxs-lookup"><span data-stu-id="b400e-135">Mₛ = scaling matrix (Scaling)</span></span>

<span data-ttu-id="b400e-136">M<sub>RC</sub> = centro da matriz de rotação (pRotationCenter)</span><span class="sxs-lookup"><span data-stu-id="b400e-136">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="b400e-137">M<sub>r</sub> = matriz de rotação (protação)</span><span class="sxs-lookup"><span data-stu-id="b400e-137">M<sub>r</sub> = rotation matrix (pRotation)</span></span>

<span data-ttu-id="b400e-138">MT = matriz de conversão (pTranslation)</span><span class="sxs-lookup"><span data-stu-id="b400e-138">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="b400e-139">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="b400e-139">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b400e-140">Dessa forma, a função D3DXMatrixAffineTransformation pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="b400e-140">In this way, the D3DXMatrixAffineTransformation function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b400e-141">Para transformações de afinidade 2D, use D3DXMatrixAffineTransformation2D.</span><span class="sxs-lookup"><span data-stu-id="b400e-141">For 2D affine transformations, use D3DXMatrixAffineTransformation2D.</span></span>

## <a name="requirements"></a><span data-ttu-id="b400e-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b400e-142">Requirements</span></span>



| <span data-ttu-id="b400e-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b400e-143">Requirement</span></span> | <span data-ttu-id="b400e-144">Valor</span><span class="sxs-lookup"><span data-stu-id="b400e-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b400e-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b400e-145">Header</span></span><br/>  | <dl> <span data-ttu-id="b400e-146"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b400e-146"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b400e-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b400e-147">Library</span></span><br/> | <dl> <span data-ttu-id="b400e-148"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b400e-148"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b400e-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="b400e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b400e-150">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="b400e-150">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
