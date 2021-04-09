---
description: Cria uma matriz de transformação. Argumentos nulos são tratados como transformações de identidade.
ms.assetid: 39042fc6-f489-4e44-ad3f-858ca395575d
title: Função D3DXMatrixTransformation (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2174329e01e3e624ef27608ca56b33181b770db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012074"
---
# <a name="d3dxmatrixtransformation-function-d3dx9mathh"></a><span data-ttu-id="42d11-104">Função D3DXMatrixTransformation (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="42d11-104">D3DXMatrixTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="42d11-105">Cria uma matriz de transformação.</span><span class="sxs-lookup"><span data-stu-id="42d11-105">Builds a transformation matrix.</span></span> <span data-ttu-id="42d11-106">Argumentos **nulos** são tratados como transformações de identidade.</span><span class="sxs-lookup"><span data-stu-id="42d11-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="42d11-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42d11-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXVECTOR3    *pScalingCenter,
  _In_    const D3DXQUATERNION *pScalingRotation,
  _In_    const D3DXVECTOR3    *pScaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="42d11-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42d11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42d11-109">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="42d11-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="42d11-110">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="42d11-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="42d11-111">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="42d11-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="42d11-112">*pScalingCenter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42d11-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42d11-113">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="42d11-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="42d11-114">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , identificando o ponto central de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="42d11-114">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, identifying the scaling center point.</span></span> <span data-ttu-id="42d11-115">Se esse argumento for **nulo**, uma matriz <sub>SC</sub> de identidade M será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="42d11-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="42d11-116">*pScalingRotation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42d11-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42d11-117">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="42d11-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="42d11-118">Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que especifica a rotação de escala.</span><span class="sxs-lookup"><span data-stu-id="42d11-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the scaling rotation.</span></span> <span data-ttu-id="42d11-119">Se esse argumento for **nulo**, uma matriz <sub>Sr</sub> de identidade M será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="42d11-119">If this argument is **NULL**, an identity M<sub>sr</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="42d11-120">*pScaling* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42d11-120">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42d11-121">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="42d11-121">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="42d11-122">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , o vetor de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="42d11-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, the scaling vector.</span></span> <span data-ttu-id="42d11-123">Se esse argumento for **nulo**, uma matriz MS de identidade será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="42d11-123">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="42d11-124">*pRotationCenter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42d11-124">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42d11-125">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="42d11-125">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="42d11-126">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , um ponto que identifica o centro da rotação.</span><span class="sxs-lookup"><span data-stu-id="42d11-126">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point that identifies the center of rotation.</span></span> <span data-ttu-id="42d11-127">Se esse argumento for **nulo**, uma matriz <sub>RC</sub> de identidade M será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="42d11-127">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="42d11-128">*protação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42d11-128">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42d11-129">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="42d11-129">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="42d11-130">Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que especifica a rotação.</span><span class="sxs-lookup"><span data-stu-id="42d11-130">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="42d11-131">Se esse argumento for **nulo**, uma matriz <sub>r</sub> de identidade M será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="42d11-131">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="42d11-132">*pTranslation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42d11-132">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42d11-133">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="42d11-133">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="42d11-134">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , representando a tradução.</span><span class="sxs-lookup"><span data-stu-id="42d11-134">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, representing the translation.</span></span> <span data-ttu-id="42d11-135">Se esse argumento for **nulo**, uma matriz de identidade MT será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="42d11-135">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42d11-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="42d11-136">Return value</span></span>

<span data-ttu-id="42d11-137">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="42d11-137">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="42d11-138">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é a matriz de transformação.</span><span class="sxs-lookup"><span data-stu-id="42d11-138">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="42d11-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="42d11-139">Remarks</span></span>

<span data-ttu-id="42d11-140">Essa função calcula a matriz de transformação com a seguinte fórmula, com concatenação de matriz avaliada na ordem da esquerda para a direita:</span><span class="sxs-lookup"><span data-stu-id="42d11-140">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="42d11-141">M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>Sr</sub>) ⁻ ¹ \* MS \* m<sub>Sr</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="42d11-141">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span></span>

<span data-ttu-id="42d11-142">onde:</span><span class="sxs-lookup"><span data-stu-id="42d11-142">where:</span></span>

<span data-ttu-id="42d11-143">M <sub>out</sub> = matriz de saída (*pout*)</span><span class="sxs-lookup"><span data-stu-id="42d11-143">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="42d11-144">M <sub>SC</sub> = matriz do centro de dimensionamento (*pScalingCenter*)</span><span class="sxs-lookup"><span data-stu-id="42d11-144">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="42d11-145">M <sub>Sr</sub> = matriz de rotação de escala (*pScalingRotation*)</span><span class="sxs-lookup"><span data-stu-id="42d11-145">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="42d11-146">MS = matriz de dimensionamento (*pScaling*)</span><span class="sxs-lookup"><span data-stu-id="42d11-146">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="42d11-147">M <sub>RC</sub> = centro da matriz de rotação (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="42d11-147">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="42d11-148">M <sub>r</sub> = matriz de rotação (*protação*)</span><span class="sxs-lookup"><span data-stu-id="42d11-148">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="42d11-149">MT = matriz de conversão (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="42d11-149">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="42d11-150">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="42d11-150">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="42d11-151">Dessa forma, a função **D3DXMatrixTransformation** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="42d11-151">In this way, the **D3DXMatrixTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="42d11-152">Para transformações 2D, use [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).</span><span class="sxs-lookup"><span data-stu-id="42d11-152">For 2D transformations, use [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42d11-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42d11-153">Requirements</span></span>



| <span data-ttu-id="42d11-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="42d11-154">Requirement</span></span> | <span data-ttu-id="42d11-155">Valor</span><span class="sxs-lookup"><span data-stu-id="42d11-155">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42d11-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="42d11-156">Header</span></span><br/>  | <dl> <span data-ttu-id="42d11-157"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="42d11-157"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="42d11-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="42d11-158">Library</span></span><br/> | <dl> <span data-ttu-id="42d11-159"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42d11-159"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="42d11-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="42d11-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42d11-161">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="42d11-161">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="42d11-162">**D3DXMatrixAffineTransformation**</span><span class="sxs-lookup"><span data-stu-id="42d11-162">**D3DXMatrixAffineTransformation**</span></span>](d3dxmatrixaffinetransformation.md)
</dt> <dt>

[<span data-ttu-id="42d11-163">Transformações (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="42d11-163">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 




