---
description: Função D3DXVec2BaryCentric (D3DX10Math. h) – retorna um ponto em coordenadas barycentric, usando os vetores 2D especificados.
ms.assetid: 8eceb2c0-26a0-4a7f-9830-85327dcb31ab
title: Função D3DXVec2BaryCentric (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2BaryCentric
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5b78d08c67fed04af9ef0d54d0c6895106b99208
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108437"
---
# <a name="d3dxvec2barycentric-function-d3dx10mathh"></a><span data-ttu-id="16cc4-103">Função D3DXVec2BaryCentric (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="16cc4-103">D3DXVec2BaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="16cc4-104">Retorna um ponto em coordenadas barycentric, usando os vetores 2D especificados.</span><span class="sxs-lookup"><span data-stu-id="16cc4-104">Returns a point in Barycentric coordinates, using the specified 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="16cc4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16cc4-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2BaryCentric(
  _In_       D3DXVECTOR2 *pOut,
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2,
  _In_ const D3DXVECTOR2 *pV3,
  _In_       FLOAT       f,
  _In_       FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="16cc4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16cc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16cc4-107">*pout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16cc4-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16cc4-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="16cc4-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="16cc4-109">Ponteiro para o [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="16cc4-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="16cc4-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16cc4-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16cc4-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="16cc4-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="16cc4-112">Ponteiro para uma estrutura de D3DXVECTOR2 de origem.</span><span class="sxs-lookup"><span data-stu-id="16cc4-112">Pointer to a source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="16cc4-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16cc4-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16cc4-114">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="16cc4-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="16cc4-115">Ponteiro para uma estrutura de D3DXVECTOR2 de origem.</span><span class="sxs-lookup"><span data-stu-id="16cc4-115">Pointer to a source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="16cc4-116">*pV3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16cc4-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16cc4-117">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="16cc4-117">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="16cc4-118">Ponteiro para uma estrutura de D3DXVECTOR2 de origem.</span><span class="sxs-lookup"><span data-stu-id="16cc4-118">Pointer to a source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="16cc4-119">*f* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="16cc4-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16cc4-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16cc4-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16cc4-121">Fator de ponderação.</span><span class="sxs-lookup"><span data-stu-id="16cc4-121">Weighting factor.</span></span> <span data-ttu-id="16cc4-122">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="16cc4-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="16cc4-123">*g* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="16cc4-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16cc4-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16cc4-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16cc4-125">Fator de ponderação.</span><span class="sxs-lookup"><span data-stu-id="16cc4-125">Weighting factor.</span></span> <span data-ttu-id="16cc4-126">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="16cc4-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16cc4-127">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="16cc4-127">Return value</span></span>

<span data-ttu-id="16cc4-128">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="16cc4-128">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="16cc4-129">Ponteiro para uma estrutura D3DXVECTOR2 em coordenadas barycentric.</span><span class="sxs-lookup"><span data-stu-id="16cc4-129">Pointer to a D3DXVECTOR2 structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="16cc4-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="16cc4-130">Remarks</span></span>

<span data-ttu-id="16cc4-131">A função D3DXVec2BaryCentric fornece uma maneira de entender os pontos em um triângulo, independentemente de onde o triângulo realmente está localizado.</span><span class="sxs-lookup"><span data-stu-id="16cc4-131">The D3DXVec2BaryCentric function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="16cc4-132">Essa função retorna o ponto resultante usando a seguinte equação: v1 + f (v2-v1) + g (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="16cc4-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="16cc4-133">Qualquer ponto no V1V2V3 do plano pode ser representado pela coordenada barycentric (f, g). O parâmetro f controla a quantidade de v2 que é ponderada no resultado, e o parâmetro g controla a quantidade de v3 ponderada no resultado.</span><span class="sxs-lookup"><span data-stu-id="16cc4-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter f controls how much V2 gets weighted into the result, and the parameter g controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="16cc4-134">Por fim, 1-f-g controla o quanto v1 é ponderado no resultado.</span><span class="sxs-lookup"><span data-stu-id="16cc4-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="16cc4-135">Observe as seguintes relações.</span><span class="sxs-lookup"><span data-stu-id="16cc4-135">Note the following relations.</span></span>

-   <span data-ttu-id="16cc4-136">Se (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), o ponto estará dentro do triângulo V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="16cc4-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="16cc4-137">Se (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), o ponto estará na linha V1V3.</span><span class="sxs-lookup"><span data-stu-id="16cc4-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="16cc4-138">Se (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), o ponto estará na linha V1V2.</span><span class="sxs-lookup"><span data-stu-id="16cc4-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="16cc4-139">Se (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), o ponto estará na linha V2V3.</span><span class="sxs-lookup"><span data-stu-id="16cc4-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="16cc4-140">As coordenadas de barycentric são uma forma de coordenadas gerais.</span><span class="sxs-lookup"><span data-stu-id="16cc4-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="16cc4-141">Nesse contexto, o uso de coordenadas barycentric representa uma alteração nos sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="16cc4-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="16cc4-142">O que se aplica a coordenadas cartesianas é verdadeiro para coordenadas Barycentrics.</span><span class="sxs-lookup"><span data-stu-id="16cc4-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="16cc4-143">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="16cc4-143">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="16cc4-144">Dessa forma, a função D3DXVec2BaryCentric pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="16cc4-144">In this way, the D3DXVec2BaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="16cc4-145">As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo.</span><span class="sxs-lookup"><span data-stu-id="16cc4-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="16cc4-146">Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="16cc4-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="16cc4-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16cc4-147">Requirements</span></span>



| <span data-ttu-id="16cc4-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="16cc4-148">Requirement</span></span> | <span data-ttu-id="16cc4-149">Valor</span><span class="sxs-lookup"><span data-stu-id="16cc4-149">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16cc4-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16cc4-150">Header</span></span><br/>  | <dl> <span data-ttu-id="16cc4-151"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="16cc4-151"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="16cc4-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16cc4-152">Library</span></span><br/> | <dl> <span data-ttu-id="16cc4-153"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16cc4-153"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="16cc4-154">Consulte também</span><span class="sxs-lookup"><span data-stu-id="16cc4-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16cc4-155">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="16cc4-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
