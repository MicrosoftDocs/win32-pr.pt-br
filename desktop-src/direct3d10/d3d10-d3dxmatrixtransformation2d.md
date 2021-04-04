---
description: Cria uma matriz de transformação 2D que representa as transformações no plano XY. Argumentos nulos são tratados como transformações de identidade.
ms.assetid: 5b894c3b-a532-458a-bcbc-48fcd5c73c34
title: Função D3DXMatrixTransformation2D (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b41d8234dcd9dda1b3735c83460a20c7109e63d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664080"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx10mathh"></a><span data-ttu-id="78ced-104">Função D3DXMatrixTransformation2D (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="78ced-104">D3DXMatrixTransformation2D function (D3DX10Math.h)</span></span>

<span data-ttu-id="78ced-105">Cria uma matriz de transformação 2D que representa as transformações no plano XY.</span><span class="sxs-lookup"><span data-stu-id="78ced-105">Builds a 2D transformation matrix that represents transformations in the xy plane.</span></span> <span data-ttu-id="78ced-106">Argumentos **nulos** são tratados como transformações de identidade.</span><span class="sxs-lookup"><span data-stu-id="78ced-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="78ced-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78ced-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       ScalingRotation,
  _In_    const D3DXVECTOR2 *pScaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="78ced-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78ced-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78ced-109">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="78ced-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78ced-110">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="78ced-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="78ced-111">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que contém o resultado das transformações.</span><span class="sxs-lookup"><span data-stu-id="78ced-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that contains the result of the transformations.</span></span>

</dd> <dt>

<span data-ttu-id="78ced-112">*pScalingCenter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78ced-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78ced-113">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="78ced-113">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="78ced-114">Ponteiro para um [**D3DXVECTOR2**](d3d10-d3dxvector2.md), um ponto que identifica o centro de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="78ced-114">Pointer to a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), a point identifying the scaling center.</span></span> <span data-ttu-id="78ced-115">Se esse argumento for **nulo**, uma matriz <sub>SC</sub> de identidade M será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="78ced-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="78ced-116">*ScalingRotation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78ced-116">*ScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78ced-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78ced-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78ced-118">Ponteiro para o fator de rotação de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="78ced-118">Pointer to the scaling rotation factor.</span></span>

</dd> <dt>

<span data-ttu-id="78ced-119">*pScaling* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78ced-119">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78ced-120">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="78ced-120">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="78ced-121">Ponteiro para uma estrutura D3DXVECTOR2, um ponto que identifica a escala.</span><span class="sxs-lookup"><span data-stu-id="78ced-121">Pointer to a D3DXVECTOR2 structure, a point identifying the scale.</span></span> <span data-ttu-id="78ced-122">Se esse argumento for **nulo**, uma matriz MS de identidade será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="78ced-122">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="78ced-123">*pRotationCenter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78ced-123">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78ced-124">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="78ced-124">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="78ced-125">Ponteiro para uma estrutura D3DXVECTOR2, um ponto que identifica o centro de rotação.</span><span class="sxs-lookup"><span data-stu-id="78ced-125">Pointer to a D3DXVECTOR2 structure, a point identifying the rotation center.</span></span> <span data-ttu-id="78ced-126">Se esse argumento for **nulo**, uma matriz <sub>RC</sub> de identidade M será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="78ced-126">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="78ced-127">*Rotação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78ced-127">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78ced-128">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78ced-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78ced-129">O ângulo de rotação em radianos.</span><span class="sxs-lookup"><span data-stu-id="78ced-129">The angle of rotation in radians.</span></span>

</dd> <dt>

<span data-ttu-id="78ced-130">*pTranslation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78ced-130">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78ced-131">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="78ced-131">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="78ced-132">Ponteiro para uma estrutura D3DXVECTOR2, identificando a tradução.</span><span class="sxs-lookup"><span data-stu-id="78ced-132">Pointer to a D3DXVECTOR2 structure, identifying the translation.</span></span> <span data-ttu-id="78ced-133">Se esse argumento for **nulo**, uma matriz de identidade MT será aplicada à fórmula em comentários.</span><span class="sxs-lookup"><span data-stu-id="78ced-133">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78ced-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="78ced-134">Return value</span></span>

<span data-ttu-id="78ced-135">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="78ced-135">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="78ced-136">Ponteiro para uma estrutura D3DXMATRIX que contém a matriz de transformação.</span><span class="sxs-lookup"><span data-stu-id="78ced-136">Pointer to a D3DXMATRIX structure that contains the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="78ced-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="78ced-137">Remarks</span></span>

<span data-ttu-id="78ced-138">Essa função calcula a matriz de transformação com a seguinte fórmula, com concatenação de matriz avaliada na ordem da esquerda para a direita:</span><span class="sxs-lookup"><span data-stu-id="78ced-138">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="78ced-139">M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>Sr</sub>) ⁻ ¹ \* MS \* m<sub>Sr</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="78ced-139">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹\* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="78ced-140">onde:</span><span class="sxs-lookup"><span data-stu-id="78ced-140">where:</span></span>

<span data-ttu-id="78ced-141">M<sub>out</sub> = matriz de saída (pout)</span><span class="sxs-lookup"><span data-stu-id="78ced-141">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="78ced-142">M<sub>SC</sub> = matriz do centro de dimensionamento (pScalingCenter)</span><span class="sxs-lookup"><span data-stu-id="78ced-142">M<sub>sc</sub> = scaling center matrix (pScalingCenter)</span></span>

<span data-ttu-id="78ced-143">M<sub>Sr</sub> = matriz de rotação de escala (pScalingRotation)</span><span class="sxs-lookup"><span data-stu-id="78ced-143">M<sub>sr</sub> = scaling rotation matrix (pScalingRotation)</span></span>

<span data-ttu-id="78ced-144">MS = matriz de dimensionamento (pScaling)</span><span class="sxs-lookup"><span data-stu-id="78ced-144">Mₛ = scaling matrix (pScaling)</span></span>

<span data-ttu-id="78ced-145">M<sub>RC</sub> = centro da matriz de rotação (pRotationCenter)</span><span class="sxs-lookup"><span data-stu-id="78ced-145">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="78ced-146">M<sub>r</sub> = matriz de rotação (rotação)</span><span class="sxs-lookup"><span data-stu-id="78ced-146">M<sub>r</sub> = rotation matrix (Rotation)</span></span>

<span data-ttu-id="78ced-147">MT = matriz de conversão (pTranslation)</span><span class="sxs-lookup"><span data-stu-id="78ced-147">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="78ced-148">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="78ced-148">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="78ced-149">Dessa forma, a função D3DXMatrixTransformation2D pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="78ced-149">In this way, the D3DXMatrixTransformation2D function can be used as a parameter for another function.</span></span>

<span data-ttu-id="78ced-150">Para transformações 3D, use [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md).</span><span class="sxs-lookup"><span data-stu-id="78ced-150">For 3D transformations, use [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78ced-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78ced-151">Requirements</span></span>



| <span data-ttu-id="78ced-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="78ced-152">Requirement</span></span> | <span data-ttu-id="78ced-153">Valor</span><span class="sxs-lookup"><span data-stu-id="78ced-153">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78ced-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78ced-154">Header</span></span><br/>  | <dl> <span data-ttu-id="78ced-155"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="78ced-155"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="78ced-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="78ced-156">Library</span></span><br/> | <dl> <span data-ttu-id="78ced-157"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78ced-157"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="78ced-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="78ced-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78ced-159">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="78ced-159">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
