---
description: Gera uma malha com faces e vértices reordenados para otimizar o desempenho do desenho. Esse método reordena a malha existente.
ms.assetid: 2cdaf627-d1d3-44f0-a5ae-9023d4b0de45
title: 'Método ID3DXMesh:: OptimizeInplace (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.OptimizeInplace
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f889e0d3754cc1321ffa59eba294038b87991489
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664090"
---
# <a name="id3dxmeshoptimizeinplace-method"></a><span data-ttu-id="7e81a-104">Método ID3DXMesh:: OptimizeInplace</span><span class="sxs-lookup"><span data-stu-id="7e81a-104">ID3DXMesh::OptimizeInplace method</span></span>

<span data-ttu-id="7e81a-105">Gera uma malha com faces e vértices reordenados para otimizar o desempenho do desenho.</span><span class="sxs-lookup"><span data-stu-id="7e81a-105">Generates a mesh with reordered faces and vertices to optimize drawing performance.</span></span> <span data-ttu-id="7e81a-106">Esse método reordena a malha existente.</span><span class="sxs-lookup"><span data-stu-id="7e81a-106">This method reorders the existing mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e81a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e81a-107">Syntax</span></span>


```C++
HRESULT OptimizeInplace(
  [in]        DWORD        Flags,
  [in]  const DWORD        *pAdjacencyIn,
  [out]       DWORD        *pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="7e81a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e81a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e81a-109">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="7e81a-109">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e81a-110">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7e81a-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7e81a-111">Combinação de um ou mais sinalizadores [**D3DXMESHOPT**](./d3dxmeshopt.md) , especificando o tipo de otimização a ser executado.</span><span class="sxs-lookup"><span data-stu-id="7e81a-111">Combination of one or more [**D3DXMESHOPT**](./d3dxmeshopt.md) flags, specifying the type of optimization to perform.</span></span>

</dd> <dt>

<span data-ttu-id="7e81a-112">*pAdjacencyIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e81a-112">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e81a-113">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="7e81a-113">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7e81a-114">Ponteiro para uma matriz de três DWORDs por face que especifica os três vizinhos para cada face na malha de origem.</span><span class="sxs-lookup"><span data-stu-id="7e81a-114">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="7e81a-115">Se a borda não tiver faces adjacentes, o valor será 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="7e81a-115">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="7e81a-116">*pAdjacencyOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7e81a-116">*pAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e81a-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e81a-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7e81a-118">Ponteiro para uma matriz de três DWORDs por face que especifica os três vizinhos para cada face na malha otimizada.</span><span class="sxs-lookup"><span data-stu-id="7e81a-118">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="7e81a-119">Se a borda não tiver faces adjacentes, o valor será 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="7e81a-119">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="7e81a-120">Se o valor fornecido para esse argumento for **nulo**, os dados de adjacência não serão retornados.</span><span class="sxs-lookup"><span data-stu-id="7e81a-120">If the value supplied for this argument is **NULL**, adjacency data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="7e81a-121">*pFaceRemap* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7e81a-121">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e81a-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e81a-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7e81a-123">Uma matriz de DWORDs, uma por face, que identifica a face de malha original que corresponde a cada face na malha otimizada.</span><span class="sxs-lookup"><span data-stu-id="7e81a-123">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="7e81a-124">Se o valor fornecido para esse argumento for **nulo**, os dados de remapeamento facial não serão retornados.</span><span class="sxs-lookup"><span data-stu-id="7e81a-124">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="7e81a-125">*ppVertexRemap* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7e81a-125">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e81a-126">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e81a-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7e81a-127">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) , que contém um DWORD para cada vértice que especifica como os novos vértices são mapeados para os vértices antigos.</span><span class="sxs-lookup"><span data-stu-id="7e81a-127">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="7e81a-128">Esse remapeamento será útil se você precisar alterar dados externos com base no novo mapeamento de vértice.</span><span class="sxs-lookup"><span data-stu-id="7e81a-128">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="7e81a-129">Se o valor fornecido para esse argumento for **nulo**, os dados de remapeamento de vértice não serão retornados.</span><span class="sxs-lookup"><span data-stu-id="7e81a-129">If the value supplied for this argument is **NULL**, vertex remap data is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e81a-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e81a-130">Return value</span></span>

<span data-ttu-id="7e81a-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7e81a-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7e81a-132">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7e81a-132">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7e81a-133">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7e81a-133">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_CANNOTATTRSORT, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e81a-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e81a-134">Remarks</span></span>

<span data-ttu-id="7e81a-135">Antes de executar **ID3DXMesh:: OptimizeInplace**, um aplicativo deve gerar um buffer de adjacência chamando [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span><span class="sxs-lookup"><span data-stu-id="7e81a-135">Before running **ID3DXMesh::OptimizeInplace**, an application must generate an adjacency buffer by calling [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span></span> <span data-ttu-id="7e81a-136">O buffer de adjacência contém dados de adjacência, como uma lista de bordas e as faces que são adjacentes entre si.</span><span class="sxs-lookup"><span data-stu-id="7e81a-136">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

> [!Note]  
> <span data-ttu-id="7e81a-137">Esse método falhará se a malha estiver compartilhando seu buffer de vértice com outra malha, a menos que D3DXMESHOPT \_ IGNOREVERTS seja definido em sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="7e81a-137">This method will fail if the mesh is sharing its vertex buffer with another mesh, unless the D3DXMESHOPT\_IGNOREVERTS is set in Flags.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7e81a-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e81a-138">Requirements</span></span>



| <span data-ttu-id="7e81a-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e81a-139">Requirement</span></span> | <span data-ttu-id="7e81a-140">Valor</span><span class="sxs-lookup"><span data-stu-id="7e81a-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e81a-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7e81a-141">Header</span></span><br/>  | <dl> <span data-ttu-id="7e81a-142"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e81a-142"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7e81a-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7e81a-143">Library</span></span><br/> | <dl> <span data-ttu-id="7e81a-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e81a-144"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7e81a-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e81a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e81a-146">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="7e81a-146">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="7e81a-147">**ID3DXMesh:: Optimize**</span><span class="sxs-lookup"><span data-stu-id="7e81a-147">**ID3DXMesh::Optimize**</span></span>](id3dxmesh--optimize.md)
</dt> </dl>

 

 
