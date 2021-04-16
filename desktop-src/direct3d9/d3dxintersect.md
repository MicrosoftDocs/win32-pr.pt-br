---
description: Determina se um raio intersecciona com uma malha.
ms.assetid: 325f5b40-80ba-4400-a143-bae41146ab07
title: Função D3DXIntersect (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc877fb1301e01b05184625ba2e92a2c680cfa9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105773003"
---
# <a name="d3dxintersect-function"></a><span data-ttu-id="214a1-103">Função D3DXIntersect</span><span class="sxs-lookup"><span data-stu-id="214a1-103">D3DXIntersect function</span></span>

<span data-ttu-id="214a1-104">Determina se um raio intersecciona com uma malha.</span><span class="sxs-lookup"><span data-stu-id="214a1-104">Determines if a ray intersects with a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="214a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="214a1-105">Syntax</span></span>


```C++
HRESULT D3DXIntersect(
  _In_        LPD3DXBASEMESH pMesh,
  _In_  const D3DXVECTOR3    *pRayPos,
  _In_  const D3DXVECTOR3    *pRayDir,
  _Out_       BOOL           *pHit,
  _Out_       DWORD          *pFaceIndex,
  _Out_       FLOAT          *pU,
  _Out_       FLOAT          *pV,
  _Out_       FLOAT          *pDist,
  _Out_       LPD3DXBUFFER   *ppAllHits,
  _Out_       DWORD          *pCountOfHits
);
```



## <a name="parameters"></a><span data-ttu-id="214a1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="214a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="214a1-107">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="214a1-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="214a1-108">Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="214a1-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="214a1-109">Ponteiro para uma interface [**ID3DXBaseMesh**](id3dxbasemesh.md) , representando a malha a ser testada.</span><span class="sxs-lookup"><span data-stu-id="214a1-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="214a1-110">*pRayPos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="214a1-110">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="214a1-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="214a1-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="214a1-112">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando o ponto em que o raio começa.</span><span class="sxs-lookup"><span data-stu-id="214a1-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="214a1-113">*pRayDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="214a1-113">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="214a1-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="214a1-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="214a1-115">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando a direção do raio.</span><span class="sxs-lookup"><span data-stu-id="214a1-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="214a1-116">*pHit* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="214a1-116">*pHit* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="214a1-117">Tipo: **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="214a1-117">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="214a1-118">Ponteiro para um BOOL.</span><span class="sxs-lookup"><span data-stu-id="214a1-118">Pointer to a BOOL.</span></span> <span data-ttu-id="214a1-119">Se Ray Interseccionar uma face triangular na malha, esse valor será definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="214a1-119">If the ray intersects a triangular face on the mesh, this value will be set to **TRUE**.</span></span> <span data-ttu-id="214a1-120">Caso contrário, esse valor será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="214a1-120">Otherwise, this value is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="214a1-121">*pFaceIndex* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="214a1-121">*pFaceIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="214a1-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="214a1-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="214a1-123">Aponta para um valor de índice da face mais próxima da origem Ray, se pHit for **true**.</span><span class="sxs-lookup"><span data-stu-id="214a1-123">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="214a1-124">*pU* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="214a1-124">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="214a1-125">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="214a1-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="214a1-126">Ponteiro para uma coordenada de pressionamento de barycentric, U.</span><span class="sxs-lookup"><span data-stu-id="214a1-126">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="214a1-127">*VP* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="214a1-127">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="214a1-128">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="214a1-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="214a1-129">Ponteiro para uma coordenada de pressionamento de barycentric, V.</span><span class="sxs-lookup"><span data-stu-id="214a1-129">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="214a1-130">*pDist* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="214a1-130">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="214a1-131">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="214a1-131">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="214a1-132">Ponteiro para uma distância de parâmetro de interseção de raio.</span><span class="sxs-lookup"><span data-stu-id="214a1-132">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="214a1-133">*ppAllHits* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="214a1-133">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="214a1-134">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="214a1-134">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="214a1-135">Ponteiro para um objeto [**ID3DXBuffer**](id3dxbuffer.md) , que contém uma matriz de estruturas [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="214a1-135">Pointer to an [**ID3DXBuffer**](id3dxbuffer.md) object, containing an array of [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="214a1-136">*pCountOfHits* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="214a1-136">*pCountOfHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="214a1-137">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="214a1-137">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="214a1-138">Ponteiro para um DWORD que contém o número de entradas na matriz ppAllHits.</span><span class="sxs-lookup"><span data-stu-id="214a1-138">Pointer to a DWORD that contains the number of entries in the ppAllHits array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="214a1-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="214a1-139">Return value</span></span>

<span data-ttu-id="214a1-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="214a1-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="214a1-141">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="214a1-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="214a1-142">Se a função falhar, o valor de retorno poderá ser: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="214a1-142">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="214a1-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="214a1-143">Remarks</span></span>

<span data-ttu-id="214a1-144">A função **D3DXIntersect** fornece uma maneira de entender os pontos em um triângulo, independentemente de onde o triângulo realmente está localizado.</span><span class="sxs-lookup"><span data-stu-id="214a1-144">The **D3DXIntersect** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="214a1-145">Essa função retorna o ponto resultante usando a seguinte equação: v1 + U (v2-v1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="214a1-145">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="214a1-146">Qualquer ponto no V1V2V3 do plano pode ser representado pela coordenada barycentric (U, V).</span><span class="sxs-lookup"><span data-stu-id="214a1-146">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="214a1-147">O parâmetro U controla a quantidade de v2 que é ponderada no resultado, e o parâmetro V controla a quantidade de v3 ponderada no resultado.</span><span class="sxs-lookup"><span data-stu-id="214a1-147">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="214a1-148">Por fim, o valor de \[ 1-(U + V) \] controla o quanto v1 é ponderado no resultado.</span><span class="sxs-lookup"><span data-stu-id="214a1-148">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="214a1-149">As coordenadas de barycentric são uma forma de coordenadas gerais.</span><span class="sxs-lookup"><span data-stu-id="214a1-149">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="214a1-150">Nesse contexto, o uso de coordenadas barycentric representa uma alteração nos sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="214a1-150">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="214a1-151">O que se aplica a coordenadas cartesianas é verdadeiro para coordenadas barycentrics.</span><span class="sxs-lookup"><span data-stu-id="214a1-151">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="214a1-152">As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo.</span><span class="sxs-lookup"><span data-stu-id="214a1-152">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="214a1-153">Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="214a1-153">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="214a1-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="214a1-154">Requirements</span></span>



| <span data-ttu-id="214a1-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="214a1-155">Requirement</span></span> | <span data-ttu-id="214a1-156">Valor</span><span class="sxs-lookup"><span data-stu-id="214a1-156">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="214a1-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="214a1-157">Header</span></span><br/>  | <dl> <span data-ttu-id="214a1-158"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="214a1-158"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="214a1-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="214a1-159">Library</span></span><br/> | <dl> <span data-ttu-id="214a1-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="214a1-160"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="214a1-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="214a1-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="214a1-162">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="214a1-162">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
