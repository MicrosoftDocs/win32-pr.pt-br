---
description: Determina se um raio intersecciona com essa malha.
ms.assetid: 74565d4a-94e6-4faa-bf70-9c1b35e5e5d8
title: Método ID3DX10Mesh::Intersect (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Intersect
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8ceed03ab21debf61371da9e53b5150d2dc83e4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105750535"
---
# <a name="id3dx10meshintersect-method"></a><span data-ttu-id="ded40-103">Método ID3DX10Mesh:: Intersect</span><span class="sxs-lookup"><span data-stu-id="ded40-103">ID3DX10Mesh::Intersect method</span></span>

<span data-ttu-id="ded40-104">Determina se um raio intersecciona com essa malha.</span><span class="sxs-lookup"><span data-stu-id="ded40-104">Determines if a ray intersects with this mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ded40-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ded40-105">Syntax</span></span>


```C++
HRESULT Intersect(
  [in]  D3DXVECTOR3 *pRayPos,
  [in]  D3DXVECTOR3 *pRayDir,
  [in]  UINT        *pHitCount,
  [in]  UINT        *pFaceIndex,
  [in]  float       *pU,
  [in]  float       *pV,
  [in]  float       *pDist,
  [out] ID3D10Blob  **ppAllHits
);
```



## <a name="parameters"></a><span data-ttu-id="ded40-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ded40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ded40-107">*pRayPos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ded40-107">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ded40-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ded40-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ded40-109">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , especificando o ponto em que o raio começa.</span><span class="sxs-lookup"><span data-stu-id="ded40-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="ded40-110">*pRayDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ded40-110">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ded40-111">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ded40-111">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ded40-112">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , especificando a direção do raio.</span><span class="sxs-lookup"><span data-stu-id="ded40-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="ded40-113">*pHitCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ded40-113">*pHitCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ded40-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ded40-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ded40-115">O número de vezes que Ray interseccionado com a malha.</span><span class="sxs-lookup"><span data-stu-id="ded40-115">The number of times the ray intersected with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ded40-116">*pFaceIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ded40-116">*pFaceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ded40-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ded40-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ded40-118">Aponta para um valor de índice da face mais próxima da origem Ray, se pHit for **true**.</span><span class="sxs-lookup"><span data-stu-id="ded40-118">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="ded40-119">*pU* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ded40-119">*pU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ded40-120">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="ded40-120">Type: **float\***</span></span>

<span data-ttu-id="ded40-121">Ponteiro para uma coordenada de pressionamento de barycentric, U.</span><span class="sxs-lookup"><span data-stu-id="ded40-121">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="ded40-122">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ded40-122">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ded40-123">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="ded40-123">Type: **float\***</span></span>

<span data-ttu-id="ded40-124">Ponteiro para uma coordenada de pressionamento de barycentric, V.</span><span class="sxs-lookup"><span data-stu-id="ded40-124">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="ded40-125">*pDist* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ded40-125">*pDist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ded40-126">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="ded40-126">Type: **float\***</span></span>

<span data-ttu-id="ded40-127">Ponteiro para uma distância de parâmetro de interseção de raio.</span><span class="sxs-lookup"><span data-stu-id="ded40-127">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="ded40-128">*ppAllHits* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ded40-128">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ded40-129">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="ded40-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="ded40-130">Ponteiro para uma [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), contendo uma matriz de estruturas de [**\_ \_ informações de interseção D3DX10**](d3dx10-intersect-info.md) .</span><span class="sxs-lookup"><span data-stu-id="ded40-130">Pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), containing an array of [**D3DX10\_INTERSECT\_INFO**](d3dx10-intersect-info.md) structures.</span></span> <span data-ttu-id="ded40-131">Esta é uma lista de todas as ocorrências que ocorreram no teste de interseção.</span><span class="sxs-lookup"><span data-stu-id="ded40-131">This is a list of all the hits that occurred in the intersection test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ded40-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ded40-132">Return value</span></span>

<span data-ttu-id="ded40-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ded40-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ded40-134">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ded40-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ded40-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="ded40-135">Remarks</span></span>

<span data-ttu-id="ded40-136">Essa API fornece uma maneira de entender os pontos em um triângulo, independentemente de onde o triângulo realmente está localizado.</span><span class="sxs-lookup"><span data-stu-id="ded40-136">This API provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="ded40-137">Essa função retorna o ponto resultante usando a seguinte equação: v1 + U (v2-v1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="ded40-137">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="ded40-138">Qualquer ponto no V1V2V3 do plano pode ser representado pela coordenada barycentric (U, V).</span><span class="sxs-lookup"><span data-stu-id="ded40-138">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="ded40-139">O parâmetro U controla a quantidade de v2 que é ponderada no resultado, e o parâmetro V controla a quantidade de v3 ponderada no resultado.</span><span class="sxs-lookup"><span data-stu-id="ded40-139">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="ded40-140">Por fim, o valor de \[ 1-(U + V) \] controla o quanto v1 é ponderado no resultado.</span><span class="sxs-lookup"><span data-stu-id="ded40-140">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="ded40-141">As coordenadas de barycentric são uma forma de coordenadas gerais.</span><span class="sxs-lookup"><span data-stu-id="ded40-141">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="ded40-142">Nesse contexto, o uso de coordenadas barycentric representa uma alteração nos sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="ded40-142">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="ded40-143">O que se aplica a coordenadas cartesianas é verdadeiro para coordenadas barycentrics.</span><span class="sxs-lookup"><span data-stu-id="ded40-143">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="ded40-144">As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo.</span><span class="sxs-lookup"><span data-stu-id="ded40-144">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="ded40-145">Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="ded40-145">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="ded40-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ded40-146">Requirements</span></span>



| <span data-ttu-id="ded40-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="ded40-147">Requirement</span></span> | <span data-ttu-id="ded40-148">Valor</span><span class="sxs-lookup"><span data-stu-id="ded40-148">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ded40-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ded40-149">Header</span></span><br/>  | <dl> <span data-ttu-id="ded40-150"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ded40-150"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ded40-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ded40-151">Library</span></span><br/> | <dl> <span data-ttu-id="ded40-152"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ded40-152"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ded40-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="ded40-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ded40-154">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="ded40-154">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="ded40-155">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="ded40-155">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
