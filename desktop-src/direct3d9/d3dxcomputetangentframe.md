---
description: Calcule os vetores tangente, binormal e normal para uma malha.
ms.assetid: 54edb9a5-440d-4191-a58f-296e5b804e0c
title: Função D3DXComputeTangentFrame (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrame
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b95d8f046499716a2c7972593093dfb409b11f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815486"
---
# <a name="d3dxcomputetangentframe-function"></a><span data-ttu-id="c5465-103">Função D3DXComputeTangentFrame</span><span class="sxs-lookup"><span data-stu-id="c5465-103">D3DXComputeTangentFrame function</span></span>

<span data-ttu-id="c5465-104">Calcule os vetores tangente, binormal e normal para uma malha.</span><span class="sxs-lookup"><span data-stu-id="c5465-104">Compute tangent, binormal, and normal vectors for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5465-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5465-105">Syntax</span></span>


```C++
HRESULT D3DXComputeTangentFrame(
  _In_ ID3DXMesh *pMesh,
  _In_ DWORD     dwOptions
);
```



## <a name="parameters"></a><span data-ttu-id="c5465-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5465-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5465-107">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5465-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5465-108">Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5465-108">Type: **[**ID3DXMesh**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="c5465-109">Ponteiro para um objeto de malha [**ID3DXMesh**](id3dxmesh.md) de entrada.</span><span class="sxs-lookup"><span data-stu-id="c5465-109">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="c5465-110">*dwOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5465-110">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5465-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5465-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5465-112">Combinação de um ou mais sinalizadores [**D3DXTANGENT**](./d3dxtangent.md) .</span><span class="sxs-lookup"><span data-stu-id="c5465-112">Combination of one or more [**D3DXTANGENT**](./d3dxtangent.md) flags.</span></span>

<span data-ttu-id="c5465-113">Use **NULL** para especificar as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="c5465-113">Use **NULL** to specify the following options:</span></span>

-   <span data-ttu-id="c5465-114">Peso o comprimento normal do vetor pelo ângulo, em radianos, entendeu-se pelas duas bordas deixando o vértice.</span><span class="sxs-lookup"><span data-stu-id="c5465-114">Weight the normal vector length by the angle, in radians, subtended by the two edges leaving the vertex.</span></span>
-   <span data-ttu-id="c5465-115">Calcule coordenadas cartesianas ortogonal das coordenadas de textura UV.</span><span class="sxs-lookup"><span data-stu-id="c5465-115">Compute orthogonal Cartesian coordinates from the UV texture coordinates.</span></span>
-   <span data-ttu-id="c5465-116">As texturas não são encapsuladas nas direções U ou V</span><span class="sxs-lookup"><span data-stu-id="c5465-116">Textures are not wrapped in either U or V directions</span></span>
-   <span data-ttu-id="c5465-117">Derivações parciais em relação às coordenadas de textura são normalizadas.</span><span class="sxs-lookup"><span data-stu-id="c5465-117">Partial derivatives with respect to texture coordinates are normalized.</span></span>
-   <span data-ttu-id="c5465-118">Os vértices são ordenados em uma direção no sentido anti-horário em volta de cada triângulo.</span><span class="sxs-lookup"><span data-stu-id="c5465-118">Vertices are ordered in a counterclockwise direction around each triangle.</span></span>
-   <span data-ttu-id="c5465-119">Use vetores normais por vértice já presentes na malha de entrada.</span><span class="sxs-lookup"><span data-stu-id="c5465-119">Use per-vertex normal vectors already present in the input mesh.</span></span>
-   <span data-ttu-id="c5465-120">Os resultados serão armazenados na malha de entrada original.</span><span class="sxs-lookup"><span data-stu-id="c5465-120">The results will be stored in the original input mesh.</span></span> <span data-ttu-id="c5465-121">A função falhará se novos vértices precisarem ser criados.</span><span class="sxs-lookup"><span data-stu-id="c5465-121">The function will fail if new vertices need to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5465-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c5465-122">Return value</span></span>

<span data-ttu-id="c5465-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5465-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5465-124">Se a função for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c5465-124">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c5465-125">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c5465-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5465-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5465-126">Remarks</span></span>

<span data-ttu-id="c5465-127">Essa função simplesmente chama [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) com os seguintes parâmetros de entrada:</span><span class="sxs-lookup"><span data-stu-id="c5465-127">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx(pMesh, D3DDECLUSAGE_TEXCOORD, 0,   
      D3DDECLUSAGE_BINORMAL, 0, D3DDECLUSAGE_TANGENT, 0, 
      D3DDECLUSAGE_NORMAL, 0, 
      dwOptions | D3DXTANGENT_GENERATE_IN_PLACE,
      NULL, 0.01f, 0.25f, 0.01f, NULL, NULL);
```



<span data-ttu-id="c5465-128">As singularidades são tratadas conforme exigido pelo agrupamento de bordas e divisão de vértices.</span><span class="sxs-lookup"><span data-stu-id="c5465-128">Singularities are handled as required by grouping edges and splitting vertices.</span></span> <span data-ttu-id="c5465-129">Se qualquer vértice precisar ser dividido, a função falhará.</span><span class="sxs-lookup"><span data-stu-id="c5465-129">If any vertices need to be split, the function will fail.</span></span> <span data-ttu-id="c5465-130">O vetor normal calculado em cada vértice é sempre normalizado para ter comprimento de unidade.</span><span class="sxs-lookup"><span data-stu-id="c5465-130">The computed normal vector at each vertex is always normalized to have unit length.</span></span>

<span data-ttu-id="c5465-131">A solução mais robusta para a computação de coordenadas cartesianas ortogonal é não definir sinalizadores D3DXTANGENT \_ ortogonale \_ de \_ você e D3DXTANGENT \_ ortogonalize \_ de \_ V, de forma que as coordenadas ortogonales sejam computadas de ambas as coordenadas de textura UV.</span><span class="sxs-lookup"><span data-stu-id="c5465-131">The most robust solution for computing orthogonal Cartesian coordinates is to not set flags D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V, so that orthogonal coordinates are computed from both UV texture coordinates.</span></span> <span data-ttu-id="c5465-132">No entanto, nesse caso, se U ou V for zero, a função computará coordenadas ortogonal usando D3DXTANGENT \_ ortogonalize \_ de \_ V ou D3DXTANGENT \_ ortogonalize \_ de \_ U, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c5465-132">However, in this case, if either U or V is zero, then the function will compute orthogonal coordinates using D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V or D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5465-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5465-133">Requirements</span></span>



| <span data-ttu-id="c5465-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5465-134">Requirement</span></span> | <span data-ttu-id="c5465-135">Valor</span><span class="sxs-lookup"><span data-stu-id="c5465-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5465-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5465-136">Header</span></span><br/>  | <dl> <span data-ttu-id="c5465-137"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5465-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c5465-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c5465-138">Library</span></span><br/> | <dl> <span data-ttu-id="c5465-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5465-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c5465-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5465-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5465-141">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="c5465-141">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="c5465-142">**D3DXComputeTangentFrameEx**</span><span class="sxs-lookup"><span data-stu-id="c5465-142">**D3DXComputeTangentFrameEx**</span></span>](d3dxcomputetangentframeex.md)
</dt> <dt>

[<span data-ttu-id="c5465-143">**D3DXTANGENT**</span><span class="sxs-lookup"><span data-stu-id="c5465-143">**D3DXTANGENT**</span></span>](./d3dxtangent.md)
</dt> </dl>

 

 
