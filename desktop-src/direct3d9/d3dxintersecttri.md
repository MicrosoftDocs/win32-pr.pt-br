---
description: Função D3DXIntersectTri (D3DX9Mesh. h) – computa a interseção de um raio e um triângulo.
ms.assetid: f335a71d-7203-4ea1-a6bf-407b28c712e6
title: Função D3DXIntersectTri (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectTri
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33d45beda51a7a2c80debafbab864c2accb33653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098264"
---
# <a name="d3dxintersecttri-function-d3dx9meshh"></a><span data-ttu-id="59c8c-103">Função D3DXIntersectTri (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="59c8c-103">D3DXIntersectTri function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="59c8c-104">Computa a interseção de um raio e um triângulo.</span><span class="sxs-lookup"><span data-stu-id="59c8c-104">Computes the intersection of a ray and a triangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="59c8c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59c8c-105">Syntax</span></span>


```C++
BOOL D3DXIntersectTri(
  _In_  const D3DXVECTOR3 *p0,
  _In_  const D3DXVECTOR3 *p1,
  _In_  const D3DXVECTOR3 *p2,
  _In_  const D3DXVECTOR3 *pRayPos,
  _In_  const D3DXVECTOR3 *pRayDir,
  _Out_       FLOAT       *pU,
  _Out_       FLOAT       *pV,
  _Out_       FLOAT       *pDist
);
```



## <a name="parameters"></a><span data-ttu-id="59c8c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59c8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59c8c-107">*P0* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59c8c-107">*p0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c8c-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="59c8c-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="59c8c-109">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , descrevendo a primeira posição do vértice do triângulo.</span><span class="sxs-lookup"><span data-stu-id="59c8c-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the first triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="59c8c-110">*P1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59c8c-110">*p1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c8c-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="59c8c-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="59c8c-112">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , descrevendo a segunda posição de vértice de triângulo.</span><span class="sxs-lookup"><span data-stu-id="59c8c-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the second triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="59c8c-113">*P2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59c8c-113">*p2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c8c-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="59c8c-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="59c8c-115">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , descrevendo a terceira posição de vértice do triângulo.</span><span class="sxs-lookup"><span data-stu-id="59c8c-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the third triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="59c8c-116">*pRayPos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59c8c-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c8c-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="59c8c-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="59c8c-118">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando o ponto em que o raio começa.</span><span class="sxs-lookup"><span data-stu-id="59c8c-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="59c8c-119">*pRayDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59c8c-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c8c-120">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="59c8c-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="59c8c-121">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando a direção do raio.</span><span class="sxs-lookup"><span data-stu-id="59c8c-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="59c8c-122">*pU* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="59c8c-122">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59c8c-123">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="59c8c-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="59c8c-124">Barycentric as coordenadas de impacto, U.</span><span class="sxs-lookup"><span data-stu-id="59c8c-124">Barycentric hit coordinates, U.</span></span>

</dd> <dt>

<span data-ttu-id="59c8c-125">*VP* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="59c8c-125">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59c8c-126">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="59c8c-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="59c8c-127">Barycentric coordenadas de sucesso, V.</span><span class="sxs-lookup"><span data-stu-id="59c8c-127">Barycentric hit coordinates, V.</span></span>

</dd> <dt>

<span data-ttu-id="59c8c-128">*pDist* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="59c8c-128">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59c8c-129">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="59c8c-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="59c8c-130">Distância do parâmetro Ray-interseção.</span><span class="sxs-lookup"><span data-stu-id="59c8c-130">Ray-intersection parameter distance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59c8c-131">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="59c8c-131">Return value</span></span>

<span data-ttu-id="59c8c-132">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59c8c-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59c8c-133">Retornará **true** se Ray Interseccionar a área do triângulo.</span><span class="sxs-lookup"><span data-stu-id="59c8c-133">Returns **TRUE** if the ray intersects the area of the triangle.</span></span> <span data-ttu-id="59c8c-134">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="59c8c-134">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="59c8c-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="59c8c-135">Remarks</span></span>

<span data-ttu-id="59c8c-136">A função [**D3DXIntersect**](d3dxintersect.md) fornece uma maneira de entender os pontos em um triângulo, independentemente de onde o triângulo realmente está localizado.</span><span class="sxs-lookup"><span data-stu-id="59c8c-136">The [**D3DXIntersect**](d3dxintersect.md) function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="59c8c-137">Essa função retorna o ponto resultante usando a seguinte equação: v1 + U (v2-v1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="59c8c-137">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="59c8c-138">Qualquer ponto no V1V2V3 do plano pode ser representado pela coordenada barycentric (U, V).</span><span class="sxs-lookup"><span data-stu-id="59c8c-138">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="59c8c-139">O parâmetro U controla a quantidade de v2 que é ponderada no resultado, e o parâmetro V controla a quantidade de v3 ponderada no resultado.</span><span class="sxs-lookup"><span data-stu-id="59c8c-139">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="59c8c-140">Por fim, o valor de \[ 1-(U + V) \] controla o quanto v1 é ponderado no resultado.</span><span class="sxs-lookup"><span data-stu-id="59c8c-140">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="59c8c-141">As coordenadas de barycentric são uma forma de coordenadas gerais.</span><span class="sxs-lookup"><span data-stu-id="59c8c-141">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="59c8c-142">Nesse contexto, o uso de coordenadas barycentric representa uma alteração nos sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="59c8c-142">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="59c8c-143">O que se aplica a coordenadas cartesianas é verdadeiro para coordenadas barycentrics.</span><span class="sxs-lookup"><span data-stu-id="59c8c-143">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="59c8c-144">As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo.</span><span class="sxs-lookup"><span data-stu-id="59c8c-144">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="59c8c-145">Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="59c8c-145">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="59c8c-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59c8c-146">Requirements</span></span>



| <span data-ttu-id="59c8c-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="59c8c-147">Requirement</span></span> | <span data-ttu-id="59c8c-148">Valor</span><span class="sxs-lookup"><span data-stu-id="59c8c-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59c8c-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59c8c-149">Header</span></span><br/>  | <dl> <span data-ttu-id="59c8c-150"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="59c8c-150"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="59c8c-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59c8c-151">Library</span></span><br/> | <dl> <span data-ttu-id="59c8c-152"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59c8c-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="59c8c-153">Consulte também</span><span class="sxs-lookup"><span data-stu-id="59c8c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59c8c-154">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="59c8c-154">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
