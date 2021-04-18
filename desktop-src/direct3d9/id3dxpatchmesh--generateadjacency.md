---
description: Gere uma lista de bordas de malha e os patches que compartilham cada borda.
ms.assetid: 024528c0-2c0d-4448-9b38-05cf8d6ffc63
title: 'Método ID3DXPatchMesh:: GenerateAdjacency (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68de2a77b9d27391c57ec299ceb87d29166ee248
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370924"
---
# <a name="id3dxpatchmeshgenerateadjacency-method"></a><span data-ttu-id="3254c-103">Método ID3DXPatchMesh:: GenerateAdjacency</span><span class="sxs-lookup"><span data-stu-id="3254c-103">ID3DXPatchMesh::GenerateAdjacency method</span></span>

<span data-ttu-id="3254c-104">Gere uma lista de bordas de malha e os patches que compartilham cada borda.</span><span class="sxs-lookup"><span data-stu-id="3254c-104">Generate a list of mesh edges and the patches that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="3254c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3254c-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT fTolerance
);
```



## <a name="parameters"></a><span data-ttu-id="3254c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3254c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3254c-107">*fTolerance* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3254c-107">*fTolerance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3254c-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3254c-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3254c-109">Especifica que os vértices que diferem na posição por menos que a tolerância devem ser tratados como coincidentes.</span><span class="sxs-lookup"><span data-stu-id="3254c-109">Specifies that vertices that differ in position by less than the tolerance should be treated as coincident.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3254c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3254c-110">Return value</span></span>

<span data-ttu-id="3254c-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3254c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3254c-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3254c-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3254c-113">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3254c-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3254c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3254c-114">Remarks</span></span>

<span data-ttu-id="3254c-115">Depois que um aplicativo gera informações de adjacência para uma malha, os dados de malha podem ser otimizados para melhorar o desempenho do desenho.</span><span class="sxs-lookup"><span data-stu-id="3254c-115">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span> <span data-ttu-id="3254c-116">Esse método determina quais patches são adjacentes (dentro da tolerância fornecida).</span><span class="sxs-lookup"><span data-stu-id="3254c-116">This method determines which patches are adjacent (within the provided tolerance).</span></span> <span data-ttu-id="3254c-117">Essas informações são usadas internamente para otimizar o mosaico.</span><span class="sxs-lookup"><span data-stu-id="3254c-117">This information is used internally to optimize tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="3254c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3254c-118">Requirements</span></span>



| <span data-ttu-id="3254c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3254c-119">Requirement</span></span> | <span data-ttu-id="3254c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3254c-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3254c-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3254c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3254c-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3254c-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3254c-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3254c-123">Library</span></span><br/> | <dl> <span data-ttu-id="3254c-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3254c-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3254c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3254c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3254c-126">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="3254c-126">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="3254c-127">**ID3DXPatchMesh:: Optimize**</span><span class="sxs-lookup"><span data-stu-id="3254c-127">**ID3DXPatchMesh::Optimize**</span></span>](id3dxpatchmesh--optimize.md)
</dt> </dl>

 

 
