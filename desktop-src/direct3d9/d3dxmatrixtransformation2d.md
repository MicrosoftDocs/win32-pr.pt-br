---
description: Cria uma matriz de transformação 2D que representa as transformações no plano XY. Argumentos nulos são tratados como transformações de identidade.
ms.assetid: 671d3d67-b474-4fc1-9913-d21f05d66d9a
title: Função D3DXMatrixTransformation2D (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation2D
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ead4d403917b5328776b33563bc477c28983d6ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811984"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx9mathh"></a><span data-ttu-id="f7a51-104">Função D3DXMatrixTransformation2D (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f7a51-104">D3DXMatrixTransformation2D function (D3dx9math.h)</span></span>

<span data-ttu-id="f7a51-105">Cria uma matriz de transformação 2D que representa as transformações no plano XY.</span><span class="sxs-lookup"><span data-stu-id="f7a51-105">Builds a 2D transformation matrix that represents transformations in the xy plane.</span></span> <span data-ttu-id="f7a51-106">Argumentos **nulos** são tratados como transformações de identidade.</span><span class="sxs-lookup"><span data-stu-id="f7a51-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7a51-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7a51-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       pScalingRotation,
  _In_    const D3DXVECTOR2 *pScaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="f7a51-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7a51-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7a51-109">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f7a51-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a51-110">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f7a51-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f7a51-111">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que contém o resultado das transformações.</span><span class="sxs-lookup"><span data-stu-id="f7a51-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that contains the result of the transformations.</span></span>

</dd> <dt>

<span data-ttu-id="f7a51-112">*pScalingCenter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7a51-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a51-113">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="f7a51-113">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f7a51-114">Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) , um ponto que identifica o centro de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="f7a51-114">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the scaling center.</span></span> <span data-ttu-id="f7a51-115">Se esse argumento for **nulo**, uma matriz <sub>SC</sub> de identidade M será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="f7a51-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f7a51-116">*pScalingRotation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7a51-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a51-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7a51-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f7a51-118">O fator de rotação de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="f7a51-118">The scaling rotation factor.</span></span>

</dd> <dt>

<span data-ttu-id="f7a51-119">*pScaling* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7a51-119">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a51-120">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="f7a51-120">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f7a51-121">Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) , um ponto que identifica a escala.</span><span class="sxs-lookup"><span data-stu-id="f7a51-121">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the scale.</span></span> <span data-ttu-id="f7a51-122">Se esse argumento for **nulo**, uma matriz MS de identidade será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="f7a51-122">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f7a51-123">*pRotationCenter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7a51-123">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a51-124">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="f7a51-124">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f7a51-125">Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) , um ponto que identifica o centro de rotação.</span><span class="sxs-lookup"><span data-stu-id="f7a51-125">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the rotation center.</span></span> <span data-ttu-id="f7a51-126">Se esse argumento for **nulo**, uma matriz <sub>RC</sub> de identidade M será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="f7a51-126">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f7a51-127">*Rotação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7a51-127">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a51-128">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7a51-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f7a51-129">O ângulo de rotação em radianos.</span><span class="sxs-lookup"><span data-stu-id="f7a51-129">The angle of rotation in radians.</span></span>

</dd> <dt>

<span data-ttu-id="f7a51-130">*pTranslation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7a51-130">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a51-131">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="f7a51-131">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f7a51-132">Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) , identificando a tradução.</span><span class="sxs-lookup"><span data-stu-id="f7a51-132">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, identifying the translation.</span></span> <span data-ttu-id="f7a51-133">Se esse argumento for **nulo**, uma matriz de identidade MT será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="f7a51-133">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7a51-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f7a51-134">Return value</span></span>

<span data-ttu-id="f7a51-135">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f7a51-135">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f7a51-136">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que contém a matriz de transformação.</span><span class="sxs-lookup"><span data-stu-id="f7a51-136">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that contains the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7a51-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7a51-137">Remarks</span></span>

<span data-ttu-id="f7a51-138">Essa função calcula a matriz de transformação com a seguinte fórmula, com concatenação de matriz avaliada na ordem da esquerda para a direita:</span><span class="sxs-lookup"><span data-stu-id="f7a51-138">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="f7a51-139">M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>Sr</sub>) ⁻ ¹ \* MS \* m<sub>Sr</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="f7a51-139">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹\* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="f7a51-140">onde:</span><span class="sxs-lookup"><span data-stu-id="f7a51-140">where:</span></span>

<span data-ttu-id="f7a51-141">M <sub>out</sub> = matriz de saída (*pout*)</span><span class="sxs-lookup"><span data-stu-id="f7a51-141">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="f7a51-142">M <sub>SC</sub> = matriz do centro de dimensionamento (*pScalingCenter*)</span><span class="sxs-lookup"><span data-stu-id="f7a51-142">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="f7a51-143">M <sub>Sr</sub> = matriz de rotação de escala (*pScalingRotation*)</span><span class="sxs-lookup"><span data-stu-id="f7a51-143">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="f7a51-144">MS = matriz de dimensionamento (*pScaling*)</span><span class="sxs-lookup"><span data-stu-id="f7a51-144">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="f7a51-145">M <sub>RC</sub> = centro da matriz de rotação (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="f7a51-145">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="f7a51-146">M <sub>r</sub> = matriz de rotação (*rotação*)</span><span class="sxs-lookup"><span data-stu-id="f7a51-146">M <sub>r</sub> = rotation matrix (*Rotation*)</span></span>

<span data-ttu-id="f7a51-147">MT = matriz de conversão (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="f7a51-147">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="f7a51-148">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="f7a51-148">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f7a51-149">Dessa forma, a função **D3DXMatrixTransformation2D** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="f7a51-149">In this way, the **D3DXMatrixTransformation2D** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f7a51-150">Para transformações 3D, use [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).</span><span class="sxs-lookup"><span data-stu-id="f7a51-150">For 3D transformations, use [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7a51-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7a51-151">Requirements</span></span>



| <span data-ttu-id="f7a51-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7a51-152">Requirement</span></span> | <span data-ttu-id="f7a51-153">Valor</span><span class="sxs-lookup"><span data-stu-id="f7a51-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7a51-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f7a51-154">Header</span></span><br/>  | <dl> <span data-ttu-id="f7a51-155"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7a51-155"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f7a51-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f7a51-156">Library</span></span><br/> | <dl> <span data-ttu-id="f7a51-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7a51-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f7a51-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7a51-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7a51-159">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="f7a51-159">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f7a51-160">**D3DXMatrixAffineTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="f7a51-160">**D3DXMatrixAffineTransformation2D**</span></span>](d3dxmatrixaffinetransformation2d.md)
</dt> <dt>

[<span data-ttu-id="f7a51-161">Transformações (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f7a51-161">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
