---
description: Executa mosaico adaptável com base no critério de mosaico adaptável baseado em z.
ms.assetid: 9f8f5c18-e866-4893-ba07-2a3c0d26c028
title: 'Método ID3DXPatchMesh:: TessellateAdaptive (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.TessellateAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4cc6c6b7ff7b0cdb99e56386df49529f26c9166
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105749421"
---
# <a name="id3dxpatchmeshtessellateadaptive-method"></a><span data-ttu-id="8087d-103">Método ID3DXPatchMesh:: TessellateAdaptive</span><span class="sxs-lookup"><span data-stu-id="8087d-103">ID3DXPatchMesh::TessellateAdaptive method</span></span>

<span data-ttu-id="8087d-104">Executa mosaico adaptável com base no critério de mosaico adaptável baseado em z.</span><span class="sxs-lookup"><span data-stu-id="8087d-104">Performs adaptive tessellation based on the z-based adaptive tessellation criterion.</span></span>

## <a name="syntax"></a><span data-ttu-id="8087d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8087d-105">Syntax</span></span>


```C++
HRESULT TessellateAdaptive(
  [in] const D3DXVECTOR4 *pTrans,
  [in]       DWORD       dwMaxTessLevel,
  [in]       DWORD       dwMinTessLevel,
  [in]       LPD3DXMESH  pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="8087d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8087d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8087d-107">*pTrans* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8087d-107">*pTrans* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8087d-108">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="8087d-108">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8087d-109">Especifica um vetor 4D que é pontilhado com os vértices para obter a quantidade de mosaico adaptável por vértice.</span><span class="sxs-lookup"><span data-stu-id="8087d-109">Specifies a 4D vector that is dotted with the vertices to get the per-vertex adaptive tessellation amount.</span></span> <span data-ttu-id="8087d-110">Cada borda é mosaico ao valor médio dos níveis de mosaico para os dois vértices que ele conecta.</span><span class="sxs-lookup"><span data-stu-id="8087d-110">Each edge is tessellated to the average value of the tessellation levels for the two vertices it connects.</span></span>

</dd> <dt>

<span data-ttu-id="8087d-111">*dwMaxTessLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8087d-111">*dwMaxTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8087d-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8087d-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8087d-113">Limite máximo para mosaico adaptável.</span><span class="sxs-lookup"><span data-stu-id="8087d-113">Maximum limit for adaptive tessellation.</span></span> <span data-ttu-id="8087d-114">Este é o número de vértices introduzidos entre os vértices existentes.</span><span class="sxs-lookup"><span data-stu-id="8087d-114">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="8087d-115">Esse valor inteiro pode variar de 1 a 32, inclusive.</span><span class="sxs-lookup"><span data-stu-id="8087d-115">This integer value can range from 1 to 32, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="8087d-116">*dwMinTessLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8087d-116">*dwMinTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8087d-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8087d-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8087d-118">Limite mínimo para mosaico adaptável.</span><span class="sxs-lookup"><span data-stu-id="8087d-118">Minimum limit for adaptive tessellation.</span></span> <span data-ttu-id="8087d-119">Este é o número de vértices introduzidos entre os vértices existentes.</span><span class="sxs-lookup"><span data-stu-id="8087d-119">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="8087d-120">Esse valor inteiro pode variar de 1 a 32, inclusive.</span><span class="sxs-lookup"><span data-stu-id="8087d-120">This integer value can range from 1 to 32, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="8087d-121">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8087d-121">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8087d-122">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="8087d-122">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="8087d-123">Malha mosaico resultante.</span><span class="sxs-lookup"><span data-stu-id="8087d-123">Resulting tessellated mesh.</span></span> <span data-ttu-id="8087d-124">Consulte [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="8087d-124">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8087d-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8087d-125">Return value</span></span>

<span data-ttu-id="8087d-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8087d-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8087d-127">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8087d-127">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8087d-128">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8087d-128">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8087d-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="8087d-129">Remarks</span></span>

<span data-ttu-id="8087d-130">Essa função será executada com mais eficiência se a malha de patches tiver sido otimizada usando [**ID3DXPatchMesh:: Optimize**](id3dxpatchmesh--optimize.md).</span><span class="sxs-lookup"><span data-stu-id="8087d-130">This function will perform more efficiently if the patch mesh has been optimized using [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8087d-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8087d-131">Requirements</span></span>



| <span data-ttu-id="8087d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8087d-132">Requirement</span></span> | <span data-ttu-id="8087d-133">Valor</span><span class="sxs-lookup"><span data-stu-id="8087d-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8087d-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8087d-134">Header</span></span><br/>  | <dl> <span data-ttu-id="8087d-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8087d-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8087d-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8087d-136">Library</span></span><br/> | <dl> <span data-ttu-id="8087d-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8087d-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8087d-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="8087d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8087d-139">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="8087d-139">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
