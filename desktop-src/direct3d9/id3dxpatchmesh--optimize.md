---
description: Otimiza a malha de patches para mosaico eficiente.
ms.assetid: 0049e649-5fe5-45b4-9b09-14b7f99b4988
title: 'Método ID3DXPatchMesh:: Optimize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fa66aadd0ef1f9f9f65747694fc311f80172449
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930758"
---
# <a name="id3dxpatchmeshoptimize-method"></a><span data-ttu-id="91e19-103">Método ID3DXPatchMesh:: Optimize</span><span class="sxs-lookup"><span data-stu-id="91e19-103">ID3DXPatchMesh::Optimize method</span></span>

<span data-ttu-id="91e19-104">Otimiza a malha de patches para mosaico eficiente.</span><span class="sxs-lookup"><span data-stu-id="91e19-104">Optimizes the patch mesh for efficient tessellation.</span></span>

## <a name="syntax"></a><span data-ttu-id="91e19-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91e19-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in] DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="91e19-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91e19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91e19-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="91e19-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91e19-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91e19-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91e19-109">Atualmente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="91e19-109">Currently unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91e19-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91e19-110">Return value</span></span>

<span data-ttu-id="91e19-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="91e19-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="91e19-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="91e19-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="91e19-113">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT.</span><span class="sxs-lookup"><span data-stu-id="91e19-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_CANNOTATTRSORT.</span></span>

## <a name="remarks"></a><span data-ttu-id="91e19-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="91e19-114">Remarks</span></span>

<span data-ttu-id="91e19-115">Depois que um aplicativo gera informações de adjacência para uma malha, os dados de malha podem ser otimizados (reordenados) para melhorar o desempenho do desenho.</span><span class="sxs-lookup"><span data-stu-id="91e19-115">After an application generates adjacency information for a mesh, the mesh data can be optimized (reordered) for better drawing performance.</span></span> <span data-ttu-id="91e19-116">Esse método determina quais patches são adjacentes (dentro da tolerância fornecida).</span><span class="sxs-lookup"><span data-stu-id="91e19-116">This method determines which patches are adjacent (within the provided tolerance).</span></span>

<span data-ttu-id="91e19-117">As informações de adjacência também são usadas para otimizar o mosaico.</span><span class="sxs-lookup"><span data-stu-id="91e19-117">Adjacency information is also used to optimize tessellation.</span></span> <span data-ttu-id="91e19-118">Gere informações de adjacência uma vez e incluí repetidamente chamando [**ID3DXPatchMesh:: incluí**](id3dxpatchmesh--tessellate.md).</span><span class="sxs-lookup"><span data-stu-id="91e19-118">Generate adjacency information once and tessellate repeatedly by calling [**ID3DXPatchMesh::Tessellate**](id3dxpatchmesh--tessellate.md).</span></span> <span data-ttu-id="91e19-119">A otimização executada é independente do nível de mosaico real usado.</span><span class="sxs-lookup"><span data-stu-id="91e19-119">The optimization performed is independent of the actual tessellation level used.</span></span> <span data-ttu-id="91e19-120">No entanto, se os vértices de malha forem alterados, você deverá regenerar as informações de adjacência.</span><span class="sxs-lookup"><span data-stu-id="91e19-120">However, if the mesh vertices are changed, you must regenerate the adjacency information.</span></span>

## <a name="requirements"></a><span data-ttu-id="91e19-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91e19-121">Requirements</span></span>



| <span data-ttu-id="91e19-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="91e19-122">Requirement</span></span> | <span data-ttu-id="91e19-123">Valor</span><span class="sxs-lookup"><span data-stu-id="91e19-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91e19-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91e19-124">Header</span></span><br/>  | <dl> <span data-ttu-id="91e19-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="91e19-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="91e19-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="91e19-126">Library</span></span><br/> | <dl> <span data-ttu-id="91e19-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91e19-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="91e19-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="91e19-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91e19-129">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="91e19-129">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="91e19-130">**ID3DXPatchMesh::GenerateAdjacency**</span><span class="sxs-lookup"><span data-stu-id="91e19-130">**ID3DXPatchMesh::GenerateAdjacency**</span></span>](id3dxpatchmesh--generateadjacency.md)
</dt> </dl>

 

 
