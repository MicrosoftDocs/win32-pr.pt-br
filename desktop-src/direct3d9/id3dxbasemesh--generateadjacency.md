---
description: Gere uma lista de bordas de malha, bem como uma lista de faces que compartilham cada borda.
ms.assetid: 9d52290f-1c9e-43a7-b239-35cd54e36466
title: 'Método ID3DXBaseMesh:: GenerateAdjacency (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5b1d304878a4977bb14d6ef98ad7256b6c3181f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370988"
---
# <a name="id3dxbasemeshgenerateadjacency-method"></a><span data-ttu-id="33d1b-103">Método ID3DXBaseMesh:: GenerateAdjacency</span><span class="sxs-lookup"><span data-stu-id="33d1b-103">ID3DXBaseMesh::GenerateAdjacency method</span></span>

<span data-ttu-id="33d1b-104">Gere uma lista de bordas de malha, bem como uma lista de faces que compartilham cada borda.</span><span class="sxs-lookup"><span data-stu-id="33d1b-104">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="33d1b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33d1b-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT Epsilon,
  [in] DWORD *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="33d1b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33d1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33d1b-107">*Épsilon* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33d1b-107">*Epsilon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33d1b-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33d1b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33d1b-109">Especifica que os vértices que diferem na posição por menos de Épsilon devem ser tratados como coincidentes.</span><span class="sxs-lookup"><span data-stu-id="33d1b-109">Specifies that vertices that differ in position by less than epsilon should be treated as coincident.</span></span>

</dd> <dt>

<span data-ttu-id="33d1b-110">*pAdjacency* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33d1b-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33d1b-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="33d1b-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="33d1b-112">Ponteiro para uma matriz de três DWORDs por face a ser preenchida com os índices de faces adjacentes.</span><span class="sxs-lookup"><span data-stu-id="33d1b-112">Pointer to an array of three DWORDs per face to be filled with the indices of adjacent faces.</span></span> <span data-ttu-id="33d1b-113">O número de bytes nessa matriz deve ser pelo menos 3 \* [**ID3DXBaseMesh:: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="33d1b-113">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33d1b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33d1b-114">Return value</span></span>

<span data-ttu-id="33d1b-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="33d1b-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="33d1b-116">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="33d1b-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="33d1b-117">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="33d1b-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="33d1b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="33d1b-118">Remarks</span></span>

<span data-ttu-id="33d1b-119">Depois que um aplicativo gera informações de adjacência para uma malha, os dados de malha podem ser otimizados para melhorar o desempenho do desenho.</span><span class="sxs-lookup"><span data-stu-id="33d1b-119">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span>

<span data-ttu-id="33d1b-120">A ordem das entradas no buffer de adjacência é determinada pela ordem dos índices de vértice no buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="33d1b-120">The order of the entries in the adjacency buffer is determined by the order of the vertex indices in the index buffer.</span></span> <span data-ttu-id="33d1b-121">O triângulo adjacente 0 sempre corresponde à borda entre os índices dos cantos 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="33d1b-121">The adjacent triangle 0 always corresponds to the edge between the indices of the corners 0 and 1.</span></span> <span data-ttu-id="33d1b-122">O triângulo adjacente 1 sempre corresponde à borda entre os índices dos cantos 1 e 2, enquanto o triângulo adjacente 2 corresponde à borda entre os índices dos cantos 2 e 0.</span><span class="sxs-lookup"><span data-stu-id="33d1b-122">The adjacent triangle 1 always corresponds to the edge between the indices of the corners 1 and 2 while the adjacent triangle 2 corresponds to the edge between the indices of the corners 2 and 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="33d1b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33d1b-123">Requirements</span></span>



| <span data-ttu-id="33d1b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="33d1b-124">Requirement</span></span> | <span data-ttu-id="33d1b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="33d1b-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33d1b-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33d1b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="33d1b-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="33d1b-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="33d1b-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33d1b-128">Library</span></span><br/> | <dl> <span data-ttu-id="33d1b-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33d1b-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="33d1b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="33d1b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33d1b-131">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="33d1b-131">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="33d1b-132">**ID3DXMesh:: Optimize**</span><span class="sxs-lookup"><span data-stu-id="33d1b-132">**ID3DXMesh::Optimize**</span></span>](id3dxmesh--optimize.md)
</dt> <dt>

[<span data-ttu-id="33d1b-133">**ID3DXMesh::OptimizeInplace**</span><span class="sxs-lookup"><span data-stu-id="33d1b-133">**ID3DXMesh::OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
