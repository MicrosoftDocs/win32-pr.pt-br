---
description: Limpa uma malha, preparando-a para simplificação.
ms.assetid: 2b586ecc-db87-4b20-a4fc-c8b547bebf65
title: Função D3DXCleanMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCleanMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5565978dc1ad0e80c33718275ea65080930ce7cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105752162"
---
# <a name="d3dxcleanmesh-function"></a><span data-ttu-id="0f8f5-103">Função D3DXCleanMesh</span><span class="sxs-lookup"><span data-stu-id="0f8f5-103">D3DXCleanMesh function</span></span>

<span data-ttu-id="0f8f5-104">Limpa uma malha, preparando-a para simplificação.</span><span class="sxs-lookup"><span data-stu-id="0f8f5-104">Cleans a mesh, preparing it for simplification.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f8f5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f8f5-105">Syntax</span></span>


```C++
HRESULT D3DXCleanMesh(
  _In_        D3DXCLEANTYPE CleanType,
  _In_        LPD3DXMESH    pMeshIn,
  _In_  const DWORD         *pAdjacencyIn,
  _Out_       LPD3DXMESH    *ppMeshOut,
  _Out_       DWORD         *pAdjacencyOut,
  _Out_       LPD3DXBUFFER  *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="0f8f5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f8f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f8f5-107">*Limpartype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0f8f5-107">*CleanType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f8f5-108">Tipo: **[ **D3DXCLEANTYPE**](./d3dxcleantype.md)**</span><span class="sxs-lookup"><span data-stu-id="0f8f5-108">Type: **[**D3DXCLEANTYPE**](./d3dxcleantype.md)**</span></span>

<span data-ttu-id="0f8f5-109">Operações de vértice a serem executadas na preparação para limpeza de malha.</span><span class="sxs-lookup"><span data-stu-id="0f8f5-109">Vertex operations to perform in preparation for mesh cleaning.</span></span> <span data-ttu-id="0f8f5-110">Consulte [**D3DXCLEANTYPE**](./d3dxcleantype.md).</span><span class="sxs-lookup"><span data-stu-id="0f8f5-110">See [**D3DXCLEANTYPE**](./d3dxcleantype.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f8f5-111">*pMeshIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0f8f5-111">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f8f5-112">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="0f8f5-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="0f8f5-113">Ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , representando a malha a ser limpa.</span><span class="sxs-lookup"><span data-stu-id="0f8f5-113">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to be cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="0f8f5-114">*pAdjacencyIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0f8f5-114">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f8f5-115">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0f8f5-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0f8f5-116">Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha a ser limpa.</span><span class="sxs-lookup"><span data-stu-id="0f8f5-116">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="0f8f5-117">*ppMeshOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0f8f5-117">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f8f5-118">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="0f8f5-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="0f8f5-119">Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa a malha limpa retornada.</span><span class="sxs-lookup"><span data-stu-id="0f8f5-119">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned cleaned mesh.</span></span> <span data-ttu-id="0f8f5-120">A mesma malha é retornada, que foi passada se nenhuma limpeza fosse necessária.</span><span class="sxs-lookup"><span data-stu-id="0f8f5-120">The same mesh is returned that was passed in if no cleaning was necessary.</span></span>

</dd> <dt>

<span data-ttu-id="0f8f5-121">*pAdjacencyOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0f8f5-121">*pAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f8f5-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0f8f5-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0f8f5-123">Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha de saída.</span><span class="sxs-lookup"><span data-stu-id="0f8f5-123">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="0f8f5-124">*ppErrorsAndWarnings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0f8f5-124">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f8f5-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0f8f5-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0f8f5-126">Retorna um buffer que contém uma cadeia de caracteres de erros e avisos, que explicam os problemas encontrados na malha.</span><span class="sxs-lookup"><span data-stu-id="0f8f5-126">Returns a buffer containing a string of errors and warnings, which explain the problems found in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f8f5-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f8f5-127">Return value</span></span>

<span data-ttu-id="0f8f5-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0f8f5-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0f8f5-129">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0f8f5-129">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0f8f5-130">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0f8f5-130">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f8f5-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f8f5-131">Remarks</span></span>

<span data-ttu-id="0f8f5-132">Essa função limpa uma malha usando o método de limpeza e as opções especificadas no parâmetro Cleantype.</span><span class="sxs-lookup"><span data-stu-id="0f8f5-132">This function cleans a mesh using the cleaning method and options specified in the CleanType parameter.</span></span> <span data-ttu-id="0f8f5-133">Consulte a enumeração [**D3DXCLEANTYPE**](./d3dxcleantype.md) para obter uma descrição das opções disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0f8f5-133">See the [**D3DXCLEANTYPE**](./d3dxcleantype.md) enumeration for a description of the available options.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f8f5-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f8f5-134">Requirements</span></span>



| <span data-ttu-id="0f8f5-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f8f5-135">Requirement</span></span> | <span data-ttu-id="0f8f5-136">Valor</span><span class="sxs-lookup"><span data-stu-id="0f8f5-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f8f5-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0f8f5-137">Header</span></span><br/>  | <dl> <span data-ttu-id="0f8f5-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f8f5-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0f8f5-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f8f5-139">Library</span></span><br/> | <dl> <span data-ttu-id="0f8f5-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f8f5-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0f8f5-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f8f5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f8f5-142">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="0f8f5-142">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
