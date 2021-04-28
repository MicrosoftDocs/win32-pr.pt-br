---
description: Função D3DXIntersectTri (D3DX10math. h) – computa a interseção de um raio e um triângulo.
ms.assetid: 819f2543-8046-47c9-93b8-7d888264786f
title: Função D3DXIntersectTri (D3DX10math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c8bf502cca48701a7d71a083e515f9988cafe303
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113234"
---
# <a name="d3dxintersecttri-function-d3dx10mathh"></a><span data-ttu-id="feac7-103">Função D3DXIntersectTri (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="feac7-103">D3DXIntersectTri function (D3DX10math.h)</span></span>

<span data-ttu-id="feac7-104">Computa a interseção de um raio e um triângulo.</span><span class="sxs-lookup"><span data-stu-id="feac7-104">Computes the intersection of a ray and a triangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="feac7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="feac7-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="feac7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="feac7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feac7-107">*P0* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="feac7-107">*p0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feac7-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="feac7-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="feac7-109">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , descrevendo a primeira posição do vértice do triângulo.</span><span class="sxs-lookup"><span data-stu-id="feac7-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the first triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="feac7-110">*P1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="feac7-110">*p1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feac7-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="feac7-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="feac7-112">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , descrevendo a segunda posição de vértice de triângulo.</span><span class="sxs-lookup"><span data-stu-id="feac7-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the second triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="feac7-113">*P2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="feac7-113">*p2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feac7-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="feac7-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="feac7-115">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , descrevendo a terceira posição de vértice do triângulo.</span><span class="sxs-lookup"><span data-stu-id="feac7-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the third triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="feac7-116">*pRayPos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="feac7-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feac7-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="feac7-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="feac7-118">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , especificando o ponto em que o raio começa.</span><span class="sxs-lookup"><span data-stu-id="feac7-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="feac7-119">*pRayDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="feac7-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feac7-120">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="feac7-120">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="feac7-121">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , especificando a direção do raio.</span><span class="sxs-lookup"><span data-stu-id="feac7-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="feac7-122">*pU* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="feac7-122">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="feac7-123">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="feac7-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="feac7-124">Barycentric as coordenadas de impacto, U.</span><span class="sxs-lookup"><span data-stu-id="feac7-124">Barycentric hit coordinates, U.</span></span>

</dd> <dt>

<span data-ttu-id="feac7-125">*VP* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="feac7-125">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="feac7-126">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="feac7-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="feac7-127">Barycentric coordenadas de sucesso, V.</span><span class="sxs-lookup"><span data-stu-id="feac7-127">Barycentric hit coordinates, V.</span></span>

</dd> <dt>

<span data-ttu-id="feac7-128">*pDist* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="feac7-128">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="feac7-129">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="feac7-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="feac7-130">Distância do parâmetro Ray-interseção.</span><span class="sxs-lookup"><span data-stu-id="feac7-130">Ray-intersection parameter distance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feac7-131">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="feac7-131">Return value</span></span>

<span data-ttu-id="feac7-132">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="feac7-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="feac7-133">Retornará **true** se Ray Interseccionar a área do triângulo.</span><span class="sxs-lookup"><span data-stu-id="feac7-133">Returns **TRUE** if the ray intersects the area of the triangle.</span></span> <span data-ttu-id="feac7-134">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="feac7-134">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="feac7-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="feac7-135">Remarks</span></span>

<span data-ttu-id="feac7-136">Qualquer ponto no V1V2V3 do plano pode ser representado pela coordenada barycentric (U, V).</span><span class="sxs-lookup"><span data-stu-id="feac7-136">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="feac7-137">O parâmetro U controla a quantidade de v2 que é ponderada no resultado, e o parâmetro V controla a quantidade de v3 ponderada no resultado.</span><span class="sxs-lookup"><span data-stu-id="feac7-137">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="feac7-138">Por fim, o valor de \[ 1-(U + V) \] controla o quanto v1 é ponderado no resultado.</span><span class="sxs-lookup"><span data-stu-id="feac7-138">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="feac7-139">As coordenadas de barycentric são uma forma de coordenadas gerais.</span><span class="sxs-lookup"><span data-stu-id="feac7-139">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="feac7-140">Nesse contexto, o uso de coordenadas barycentric representa uma alteração nos sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="feac7-140">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="feac7-141">O que se aplica a coordenadas cartesianas é verdadeiro para coordenadas barycentrics.</span><span class="sxs-lookup"><span data-stu-id="feac7-141">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="feac7-142">As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo.</span><span class="sxs-lookup"><span data-stu-id="feac7-142">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="feac7-143">Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="feac7-143">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="feac7-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="feac7-144">Requirements</span></span>



| <span data-ttu-id="feac7-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="feac7-145">Requirement</span></span> | <span data-ttu-id="feac7-146">Valor</span><span class="sxs-lookup"><span data-stu-id="feac7-146">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="feac7-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="feac7-147">Header</span></span><br/>  | <dl> <span data-ttu-id="feac7-148"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="feac7-148"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="feac7-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="feac7-149">Library</span></span><br/> | <dl> <span data-ttu-id="feac7-150"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="feac7-150"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="feac7-151">Consulte também</span><span class="sxs-lookup"><span data-stu-id="feac7-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feac7-152">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="feac7-152">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
