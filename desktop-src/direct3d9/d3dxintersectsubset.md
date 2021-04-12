---
description: Cruza o raio especificado com o subconjunto de malha fornecido. Isso fornece uma funcionalidade semelhante ao D3DXIntersect.
ms.assetid: 4a757b9e-18eb-424e-9f3e-cdf917c23787
title: Função D3DXIntersectSubset (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectSubset
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 621f45d7c2a6d8ff162f539ef62153d3ae70f6e9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172997"
---
# <a name="d3dxintersectsubset-function"></a><span data-ttu-id="38721-104">Função D3DXIntersectSubset</span><span class="sxs-lookup"><span data-stu-id="38721-104">D3DXIntersectSubset function</span></span>

<span data-ttu-id="38721-105">Cruza o raio especificado com o subconjunto de malha fornecido.</span><span class="sxs-lookup"><span data-stu-id="38721-105">Intersects the specified ray with the given mesh subset.</span></span> <span data-ttu-id="38721-106">Isso fornece uma funcionalidade semelhante ao [**D3DXIntersect**](d3dxintersect.md).</span><span class="sxs-lookup"><span data-stu-id="38721-106">This provides similar functionality to [**D3DXIntersect**](d3dxintersect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="38721-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38721-107">Syntax</span></span>


```C++
HRESULT D3DXIntersectSubset(
  _In_        LPD3DXBASEMESH pMesh,
  _In_        DWORD          AttribId,
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



## <a name="parameters"></a><span data-ttu-id="38721-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38721-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38721-109">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="38721-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38721-110">Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="38721-110">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="38721-111">Ponteiro para uma interface [**ID3DXBaseMesh**](id3dxbasemesh.md) , representando a malha a ser testada.</span><span class="sxs-lookup"><span data-stu-id="38721-111">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to be tested.</span></span> <span data-ttu-id="38721-112">A malha deve ser classificada como atributo.</span><span class="sxs-lookup"><span data-stu-id="38721-112">The mesh must be attribute sorted.</span></span>

</dd> <dt>

<span data-ttu-id="38721-113">*Atribid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="38721-113">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38721-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38721-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38721-115">Identificador de atributo do subconjunto com o qual Interseccionar.</span><span class="sxs-lookup"><span data-stu-id="38721-115">Attribute identifier of the subset to intersect with.</span></span>

</dd> <dt>

<span data-ttu-id="38721-116">*pRayPos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="38721-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38721-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="38721-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="38721-118">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando o ponto em que o raio começa.</span><span class="sxs-lookup"><span data-stu-id="38721-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="38721-119">*pRayDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="38721-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38721-120">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="38721-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="38721-121">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando a direção do raio.</span><span class="sxs-lookup"><span data-stu-id="38721-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="38721-122">*pHit* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="38721-122">*pHit* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38721-123">Tipo: **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="38721-123">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38721-124">Ponteiro para um BOOL.</span><span class="sxs-lookup"><span data-stu-id="38721-124">Pointer to a BOOL.</span></span> <span data-ttu-id="38721-125">Se Ray Interseccionar uma face triangular na malha, esse valor será definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="38721-125">If the ray intersects a triangular face on the mesh, this value will be set to **TRUE**.</span></span> <span data-ttu-id="38721-126">Caso contrário, esse valor será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="38721-126">Otherwise, this value is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="38721-127">*pFaceIndex* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="38721-127">*pFaceIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38721-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="38721-128">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38721-129">Aponta para um valor de índice da face mais próxima da origem Ray, se pHit for **true**.</span><span class="sxs-lookup"><span data-stu-id="38721-129">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="38721-130">*pU* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="38721-130">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38721-131">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="38721-131">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38721-132">Ponteiro para uma coordenada de pressionamento de barycentric, U.</span><span class="sxs-lookup"><span data-stu-id="38721-132">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="38721-133">*VP* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="38721-133">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38721-134">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="38721-134">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38721-135">Ponteiro para uma coordenada de pressionamento de barycentric, V.</span><span class="sxs-lookup"><span data-stu-id="38721-135">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="38721-136">*pDist* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="38721-136">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38721-137">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="38721-137">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38721-138">Ponteiro para uma distância de parâmetro de interseção de raio.</span><span class="sxs-lookup"><span data-stu-id="38721-138">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="38721-139">*ppAllHits* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="38721-139">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38721-140">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="38721-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="38721-141">Matriz de estruturas [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) , que representa todas as ocorrências, não apenas as ocorrências mais próximas.</span><span class="sxs-lookup"><span data-stu-id="38721-141">Array of [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) structures, representing all hits, not just closest hits.</span></span>

</dd> <dt>

<span data-ttu-id="38721-142">*pCountOfHits* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="38721-142">*pCountOfHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38721-143">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="38721-143">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38721-144">Número de elementos na matriz retornados de ppAllHits.</span><span class="sxs-lookup"><span data-stu-id="38721-144">Number of elements in the array returned from ppAllHits.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38721-145">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38721-145">Return value</span></span>

<span data-ttu-id="38721-146">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="38721-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="38721-147">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="38721-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="38721-148">Se a função falhar, o valor de retorno poderá ser o seguinte valor: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="38721-148">If the function fails, the return value can be the following value: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="38721-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="38721-149">Remarks</span></span>

<span data-ttu-id="38721-150">A função **D3DXIntersectSubset** fornece uma maneira de entender os pontos em um triângulo, independentemente de onde o triângulo realmente está localizado.</span><span class="sxs-lookup"><span data-stu-id="38721-150">The **D3DXIntersectSubset** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="38721-151">Essa função retorna o ponto resultante usando a seguinte equação: v1 + U (v2-v1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="38721-151">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="38721-152">Qualquer ponto no V1V2V3 do plano pode ser representado pela coordenada barycentric (U, V).</span><span class="sxs-lookup"><span data-stu-id="38721-152">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="38721-153">O parâmetro U controla a quantidade de v2 que é ponderada no resultado e o parâmetro V controla a quantidade de v3 ponderada no resultado.</span><span class="sxs-lookup"><span data-stu-id="38721-153">The parameter U controls how much V2 gets weighted into the result and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="38721-154">Por fim, o valor de \[ 1-(U + V) \] controla o quanto v1 é ponderado no resultado.</span><span class="sxs-lookup"><span data-stu-id="38721-154">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="38721-155">As coordenadas de barycentric são uma forma de coordenadas gerais.</span><span class="sxs-lookup"><span data-stu-id="38721-155">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="38721-156">Nesse contexto, o uso de coordenadas barycentric representa uma alteração nos sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="38721-156">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="38721-157">O que se aplica a coordenadas cartesianas é verdadeiro para coordenadas barycentrics.</span><span class="sxs-lookup"><span data-stu-id="38721-157">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="38721-158">As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo.</span><span class="sxs-lookup"><span data-stu-id="38721-158">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="38721-159">Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="38721-159">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="38721-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38721-160">Requirements</span></span>



| <span data-ttu-id="38721-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="38721-161">Requirement</span></span> | <span data-ttu-id="38721-162">Valor</span><span class="sxs-lookup"><span data-stu-id="38721-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="38721-163">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38721-163">Header</span></span><br/>  | <dl> <span data-ttu-id="38721-164"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="38721-164"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="38721-165">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38721-165">Library</span></span><br/> | <dl> <span data-ttu-id="38721-166"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38721-166"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="38721-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="38721-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38721-168">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="38721-168">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
