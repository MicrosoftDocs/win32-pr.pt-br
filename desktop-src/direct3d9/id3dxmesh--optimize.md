---
description: Gera uma nova malha com faces e vértices reordenados para otimizar o desempenho do desenho.
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: 'Método ID3DXMesh:: Optimize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7752e08236094d7038a5e77ac1a679f787305022
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930762"
---
# <a name="id3dxmeshoptimize-method"></a><span data-ttu-id="52311-103">Método ID3DXMesh:: Optimize</span><span class="sxs-lookup"><span data-stu-id="52311-103">ID3DXMesh::Optimize method</span></span>

<span data-ttu-id="52311-104">Gera uma nova malha com faces e vértices reordenados para otimizar o desempenho do desenho.</span><span class="sxs-lookup"><span data-stu-id="52311-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="52311-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52311-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in]            DWORD        Flags,
  [in]      const DWORD        *pAdjacencyIn,
  [in, out]       DWORD        *pAdjacencyOut,
  [in, out]       DWORD        *pFaceRemap,
  [out]           LPD3DXBUFFER *ppVertexRemap,
  [out]           LPD3DXMESH   *ppOptMesh
);
```



## <a name="parameters"></a><span data-ttu-id="52311-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52311-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52311-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="52311-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52311-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52311-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52311-109">Especifica o tipo de otimização a ser executado.</span><span class="sxs-lookup"><span data-stu-id="52311-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="52311-110">Esse parâmetro pode ser definido como uma combinação de um ou mais sinalizadores de [**D3DXMESHOPT**](./d3dxmeshopt.md) e [**D3DXMESH**](./d3dxmesh.md) (exceto D3DXMESH \_ 32 bits, D3DXMESH \_ IB \_ WriteOnly e D3DXMESH \_ WRITEONLY).</span><span class="sxs-lookup"><span data-stu-id="52311-110">This parameter can be set to a combination of one or more flags from [**D3DXMESHOPT**](./d3dxmeshopt.md) and [**D3DXMESH**](./d3dxmesh.md) (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="52311-111">*pAdjacencyIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="52311-111">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52311-112">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="52311-112">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="52311-113">Ponteiro para uma matriz de três DWORDs por face que especifica os três vizinhos para cada face na malha de origem.</span><span class="sxs-lookup"><span data-stu-id="52311-113">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="52311-114">Se a borda não tiver faces adjacentes, o valor será 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="52311-114">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="52311-115">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="52311-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="52311-116">*pAdjacencyOut* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="52311-116">*pAdjacencyOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="52311-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="52311-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="52311-118">Ponteiro para uma matriz de três DWORDs por face que especifica os três vizinhos para cada face na malha otimizada.</span><span class="sxs-lookup"><span data-stu-id="52311-118">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="52311-119">Se a borda não tiver faces adjacentes, o valor será 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="52311-119">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="52311-120">*pFaceRemap* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="52311-120">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="52311-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="52311-121">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="52311-122">Uma matriz de DWORDs, uma por face, que identifica a face de malha original que corresponde a cada face na malha otimizada.</span><span class="sxs-lookup"><span data-stu-id="52311-122">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="52311-123">Se o valor fornecido para esse argumento for **nulo**, os dados de remapeamento facial não serão retornados.</span><span class="sxs-lookup"><span data-stu-id="52311-123">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="52311-124">*ppVertexRemap* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="52311-124">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52311-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="52311-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="52311-126">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) , que contém um DWORD para cada vértice que especifica como os novos vértices são mapeados para os vértices antigos.</span><span class="sxs-lookup"><span data-stu-id="52311-126">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="52311-127">Esse remapeamento será útil se você precisar alterar dados externos com base no novo mapeamento de vértice.</span><span class="sxs-lookup"><span data-stu-id="52311-127">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> <dt>

<span data-ttu-id="52311-128">*ppOptMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="52311-128">*ppOptMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52311-129">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="52311-129">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="52311-130">Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa a malha otimizada.</span><span class="sxs-lookup"><span data-stu-id="52311-130">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the optimized mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52311-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="52311-131">Return value</span></span>

<span data-ttu-id="52311-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="52311-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="52311-133">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="52311-133">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="52311-134">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="52311-134">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="52311-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="52311-135">Remarks</span></span>

<span data-ttu-id="52311-136">Esse método gera uma nova malha.</span><span class="sxs-lookup"><span data-stu-id="52311-136">This method generates a new mesh.</span></span> <span data-ttu-id="52311-137">Antes de executar Optimize, um aplicativo deve gerar um buffer de adjacência chamando [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span><span class="sxs-lookup"><span data-stu-id="52311-137">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span></span> <span data-ttu-id="52311-138">O buffer de adjacência contém dados de adjacência, como uma lista de bordas e as faces que são adjacentes entre si.</span><span class="sxs-lookup"><span data-stu-id="52311-138">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="52311-139">Esse método é muito semelhante ao método [**ID3DXBaseMesh:: CloneMesh**](id3dxbasemesh--clonemesh.md) , exceto pelo fato de que ele pode executar a otimização ao gerar o novo clone da malha.</span><span class="sxs-lookup"><span data-stu-id="52311-139">This method is very similar to the [**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="52311-140">A malha de saída herda todos os parâmetros de criação da malha de entrada.</span><span class="sxs-lookup"><span data-stu-id="52311-140">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="52311-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52311-141">Requirements</span></span>



| <span data-ttu-id="52311-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="52311-142">Requirement</span></span> | <span data-ttu-id="52311-143">Valor</span><span class="sxs-lookup"><span data-stu-id="52311-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52311-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52311-144">Header</span></span><br/>  | <dl> <span data-ttu-id="52311-145"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="52311-145"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="52311-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52311-146">Library</span></span><br/> | <dl> <span data-ttu-id="52311-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52311-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="52311-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="52311-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52311-149">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="52311-149">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="52311-150">**ID3DXMesh::OptimizeInplace**</span><span class="sxs-lookup"><span data-stu-id="52311-150">**ID3DXMesh::OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
