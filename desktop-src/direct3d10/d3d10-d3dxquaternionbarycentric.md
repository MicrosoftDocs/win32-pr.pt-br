---
description: Retorna um Quaternion nas coordenadas de barycentric.
ms.assetid: 0a8d8d5a-f486-4457-86e9-27e76eaf1bc4
title: Função D3DXQuaternionBaryCentric (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionBaryCentric
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f7cdfcf5b8e7052fcbea72f12123a0ea44422853
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812808"
---
# <a name="d3dxquaternionbarycentric-function-d3dx10mathh"></a><span data-ttu-id="b3272-103">Função D3DXQuaternionBaryCentric (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b3272-103">D3DXQuaternionBaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="b3272-104">Retorna um Quaternion nas coordenadas de barycentric.</span><span class="sxs-lookup"><span data-stu-id="b3272-104">Returns a quaternion in barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3272-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3272-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionBaryCentric(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_    const D3DXQUATERNION *pQ3,
  _In_          FLOAT          f,
  _In_          FLOAT          g
);
```



## <a name="parameters"></a><span data-ttu-id="b3272-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3272-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3272-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b3272-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3272-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3272-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b3272-109">Ponteiro para o [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="b3272-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b3272-110">*pQ1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3272-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3272-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3272-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b3272-112">Ponteiro para uma estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="b3272-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="b3272-113">*pQ2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3272-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3272-114">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3272-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b3272-115">Ponteiro para uma estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="b3272-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="b3272-116">*pQ3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3272-116">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3272-117">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3272-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b3272-118">Ponteiro para uma estrutura de D3DXQUATERNION de origem.</span><span class="sxs-lookup"><span data-stu-id="b3272-118">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="b3272-119">*f* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="b3272-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3272-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3272-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3272-121">Fator de ponderação.</span><span class="sxs-lookup"><span data-stu-id="b3272-121">Weighting factor.</span></span> <span data-ttu-id="b3272-122">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="b3272-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b3272-123">*g* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="b3272-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3272-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3272-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3272-125">Fator de ponderação.</span><span class="sxs-lookup"><span data-stu-id="b3272-125">Weighting factor.</span></span> <span data-ttu-id="b3272-126">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="b3272-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3272-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3272-127">Return value</span></span>

<span data-ttu-id="b3272-128">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3272-128">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b3272-129">Ponteiro para uma estrutura D3DXQUATERNION em coordenadas barycentric.</span><span class="sxs-lookup"><span data-stu-id="b3272-129">Pointer to a D3DXQUATERNION structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3272-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3272-130">Remarks</span></span>

<span data-ttu-id="b3272-131">Para computar as coordenadas barycentric, a função D3DXQuaternionBaryCentric implementa a seguinte série de operações de interpolação linear esférica:</span><span class="sxs-lookup"><span data-stu-id="b3272-131">To compute the barycentric coordinates, the D3DXQuaternionBaryCentric function implements the following series of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(Q1, Q2, f+g), Slerp(Q1, Q3, f+g), g/(f+g))
```



<span data-ttu-id="b3272-132">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="b3272-132">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b3272-133">Dessa forma, a função D3DXQuaternionBaryCentric pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="b3272-133">In this way, the D3DXQuaternionBaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b3272-134">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="b3272-134">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

<span data-ttu-id="b3272-135">As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo.</span><span class="sxs-lookup"><span data-stu-id="b3272-135">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="b3272-136">Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="b3272-136">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3272-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3272-137">Requirements</span></span>



| <span data-ttu-id="b3272-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3272-138">Requirement</span></span> | <span data-ttu-id="b3272-139">Valor</span><span class="sxs-lookup"><span data-stu-id="b3272-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3272-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3272-140">Header</span></span><br/>  | <dl> <span data-ttu-id="b3272-141"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3272-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b3272-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3272-142">Library</span></span><br/> | <dl> <span data-ttu-id="b3272-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3272-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b3272-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3272-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3272-145">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="b3272-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
