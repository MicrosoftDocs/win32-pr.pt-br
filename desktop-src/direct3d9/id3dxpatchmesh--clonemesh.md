---
description: Cria uma nova malha de patch com a declaração de vértice especificada.
ms.assetid: cc488cd3-fb38-468f-8aec-17c6ed842582
title: 'Método ID3DXPatchMesh:: CloneMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 249b4282aa84e3f7c5ba619a0b42e8c0b1fdf846
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298514"
---
# <a name="id3dxpatchmeshclonemesh-method"></a><span data-ttu-id="929bd-103">Método ID3DXPatchMesh:: CloneMesh</span><span class="sxs-lookup"><span data-stu-id="929bd-103">ID3DXPatchMesh::CloneMesh method</span></span>

<span data-ttu-id="929bd-104">Cria uma nova malha de patch com a declaração de vértice especificada.</span><span class="sxs-lookup"><span data-stu-id="929bd-104">Creates a new patch mesh with the specified vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="929bd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="929bd-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDecl,
  [out, retval]       LPD3DXPATCHMESH   *pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="929bd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="929bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="929bd-107">*Opções* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="929bd-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="929bd-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="929bd-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="929bd-109">Combinação de um ou mais sinalizadores [**D3DXMESH**](./d3dxmesh.md) que especificam as opções de criação para a malha.</span><span class="sxs-lookup"><span data-stu-id="929bd-109">Combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="929bd-110">*pDecl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="929bd-110">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="929bd-111">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="929bd-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="929bd-112">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) que especificam o formato de vértice para os vértices na malha de saída.</span><span class="sxs-lookup"><span data-stu-id="929bd-112">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements that specify the vertex format for the vertices in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="929bd-113">*pMesh* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="929bd-113">*pMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="929bd-114">Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="929bd-114">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="929bd-115">Endereço de um ponteiro para uma interface [**ID3DXPatchMesh**](id3dxpatchmesh.md) que representa a malha clonada.</span><span class="sxs-lookup"><span data-stu-id="929bd-115">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface that represents the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="929bd-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="929bd-116">Return value</span></span>

<span data-ttu-id="929bd-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="929bd-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="929bd-118">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="929bd-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="929bd-119">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="929bd-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="929bd-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="929bd-120">Remarks</span></span>

<span data-ttu-id="929bd-121">**CloneMesh** converte o buffer de vértice para a nova declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="929bd-121">**CloneMesh** converts the vertex buffer to the new vertex declaration.</span></span> <span data-ttu-id="929bd-122">As entradas na declaração de vértice que são novas na malha original são definidas como 0.</span><span class="sxs-lookup"><span data-stu-id="929bd-122">Entries in the vertex declaration that are new to the original mesh are set to 0.</span></span> <span data-ttu-id="929bd-123">Se a malha atual tiver uma adjacência, a nova malha também terá uma adjacência.</span><span class="sxs-lookup"><span data-stu-id="929bd-123">If the current mesh has adjacency, the new mesh will also have adjacency.</span></span>

## <a name="requirements"></a><span data-ttu-id="929bd-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="929bd-124">Requirements</span></span>



| <span data-ttu-id="929bd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="929bd-125">Requirement</span></span> | <span data-ttu-id="929bd-126">Valor</span><span class="sxs-lookup"><span data-stu-id="929bd-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="929bd-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="929bd-127">Header</span></span><br/>  | <dl> <span data-ttu-id="929bd-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="929bd-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="929bd-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="929bd-129">Library</span></span><br/> | <dl> <span data-ttu-id="929bd-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="929bd-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="929bd-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="929bd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="929bd-132">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="929bd-132">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
