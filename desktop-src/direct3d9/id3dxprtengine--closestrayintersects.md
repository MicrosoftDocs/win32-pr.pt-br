---
description: Usa o rastreamento de raio eficiente em simulações de computação radiante (PRT) para determinar se um raio cruza uma malha.
ms.assetid: e506aed3-bf14-4f29-845b-2091f5b00950
title: 'Método ID3DXPRTEngine:: ClosestRayIntersects (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ClosestRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4fd802f636077c9ec2a9f0f1060ffd43493aabf1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173161"
---
# <a name="id3dxprtengineclosestrayintersects-method"></a><span data-ttu-id="0e78e-103">Método ID3DXPRTEngine:: ClosestRayIntersects</span><span class="sxs-lookup"><span data-stu-id="0e78e-103">ID3DXPRTEngine::ClosestRayIntersects method</span></span>

<span data-ttu-id="0e78e-104">Usa o rastreamento de raio eficiente em simulações de computação radiante (PRT) para determinar se um raio cruza uma malha.</span><span class="sxs-lookup"><span data-stu-id="0e78e-104">Uses efficient ray-tracing in precomputed radiance transfer (PRT) simulations to determine whether a ray intersects a mesh.</span></span> <span data-ttu-id="0e78e-105">Se uma interseção for encontrada, o método retornará o índice da face de malha mais próxima atingida pelas coordenadas Ray e barycentric do ponto de interseção.</span><span class="sxs-lookup"><span data-stu-id="0e78e-105">If an intersection is found, the method returns the index of the closest mesh face hit by the ray and the barycentric coordinates of the intersection point.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e78e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e78e-106">Syntax</span></span>


```C++
BOOL ClosestRayIntersects(
  [in]  const D3DXVECTOR3 *pRayPos,
  [in]  const D3DXVECTOR3 *pRayDir,
  [in]        DWORD       *pFaceIndex,
  [out]       FLOAT       *pU,
  [out]       FLOAT       *pV,
  [out]       FLOAT       *pDist
);
```



## <a name="parameters"></a><span data-ttu-id="0e78e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e78e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e78e-108">*pRayPos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0e78e-108">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e78e-109">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0e78e-109">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0e78e-110">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando o ponto em que o raio começa.</span><span class="sxs-lookup"><span data-stu-id="0e78e-110">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="0e78e-111">*pRayDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0e78e-111">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e78e-112">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0e78e-112">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0e78e-113">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando a direção normalizada do raio.</span><span class="sxs-lookup"><span data-stu-id="0e78e-113">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the normalized direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="0e78e-114">*pFaceIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0e78e-114">*pFaceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e78e-115">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e78e-115">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0e78e-116">Ponteiro para o índice da face de malha atual que é primeiro atingido pelo raio fornecido, com base no empilhamento de todas as faces de malha de bloqueadores na frente da malha atual.</span><span class="sxs-lookup"><span data-stu-id="0e78e-116">Pointer to the index of the current mesh face that is first hit by the given ray, based upon stacking all blocker mesh faces in front of the current mesh.</span></span>

</dd> <dt>

<span data-ttu-id="0e78e-117">*pU* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0e78e-117">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e78e-118">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e78e-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0e78e-119">Ponteiro para uma coordenada de pressionamento de barycentric, U, para o vértice 0 do triângulo.</span><span class="sxs-lookup"><span data-stu-id="0e78e-119">Pointer to a barycentric hit coordinate, U, for vertex 0 of the triangle.</span></span>

</dd> <dt>

<span data-ttu-id="0e78e-120">*VP* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0e78e-120">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e78e-121">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e78e-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0e78e-122">Ponteiro para uma coordenada de pressionamento de barycentric, V, para o vértice 1 do triângulo.</span><span class="sxs-lookup"><span data-stu-id="0e78e-122">Pointer to a barycentric hit coordinate, V, for vertex 1 of the triangle.</span></span>

</dd> <dt>

<span data-ttu-id="0e78e-123">*pDist* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0e78e-123">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e78e-124">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e78e-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0e78e-125">Ponteiro para a distância do ponto de interseção ao longo do raio.</span><span class="sxs-lookup"><span data-stu-id="0e78e-125">Pointer to the distance of the intersection point along the ray.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e78e-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e78e-126">Return value</span></span>

<span data-ttu-id="0e78e-127">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e78e-127">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e78e-128">Retornará **true** se Ray Interseccionar a malha atual; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="0e78e-128">Returns **TRUE** if the ray intersects the current mesh; otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e78e-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e78e-129">Remarks</span></span>

<span data-ttu-id="0e78e-130">Use [**ID3DXPRTEngine:: SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) para definir distâncias mínimas e máximas de interseção com Ray.</span><span class="sxs-lookup"><span data-stu-id="0e78e-130">Use [**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) to set minimum and maximum distances of intersection with the ray.</span></span>

<span data-ttu-id="0e78e-131">A coordenada barycentric do terceiro vértice (vértice 2) do triângulo é 1-(U + V).</span><span class="sxs-lookup"><span data-stu-id="0e78e-131">The barycentric coordinate of the third vertex (vertex 2) of the triangle is 1 - ( U + V ).</span></span>

<span data-ttu-id="0e78e-132">Esse método é executado mais devagar que [**ID3DXPRTEngine:: ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md).</span><span class="sxs-lookup"><span data-stu-id="0e78e-132">This method executes slower than [**ID3DXPRTEngine::ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md).</span></span> <span data-ttu-id="0e78e-133">Use **ID3DXPRTEngine:: ShadowRayIntersects** se o local do ponto de interseção não for necessário.</span><span class="sxs-lookup"><span data-stu-id="0e78e-133">Use **ID3DXPRTEngine::ShadowRayIntersects** if the location of the intersection point is not needed.</span></span>

<span data-ttu-id="0e78e-134">As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo.</span><span class="sxs-lookup"><span data-stu-id="0e78e-134">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="0e78e-135">Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="0e78e-135">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e78e-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e78e-136">Requirements</span></span>



| <span data-ttu-id="0e78e-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e78e-137">Requirement</span></span> | <span data-ttu-id="0e78e-138">Valor</span><span class="sxs-lookup"><span data-stu-id="0e78e-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e78e-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0e78e-139">Header</span></span><br/>  | <dl> <span data-ttu-id="0e78e-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e78e-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0e78e-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0e78e-141">Library</span></span><br/> | <dl> <span data-ttu-id="0e78e-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e78e-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0e78e-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e78e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e78e-144">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="0e78e-144">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="0e78e-145">**ID3DXPRTEngine::ShadowRayIntersects**</span><span class="sxs-lookup"><span data-stu-id="0e78e-145">**ID3DXPRTEngine::ShadowRayIntersects**</span></span>](id3dxprtengine--shadowrayintersects.md)
</dt> <dt>

[<span data-ttu-id="0e78e-146">**ID3DXPRTEngine::SetMinMaxIntersection**</span><span class="sxs-lookup"><span data-stu-id="0e78e-146">**ID3DXPRTEngine::SetMinMaxIntersection**</span></span>](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
