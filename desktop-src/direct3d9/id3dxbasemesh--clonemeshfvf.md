---
description: Clona uma malha usando um código de formato de vértice flexível (FVF).
ms.assetid: b7d23ea9-1a2f-46e3-bcb5-82040d2a1e12
title: 'Método ID3DXBaseMesh:: CloneMeshFVF (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMeshFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4cb3b0ad33e54e79464949f441842173fb48a180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807934"
---
# <a name="id3dxbasemeshclonemeshfvf-method"></a><span data-ttu-id="efde3-103">Método ID3DXBaseMesh:: CloneMeshFVF</span><span class="sxs-lookup"><span data-stu-id="efde3-103">ID3DXBaseMesh::CloneMeshFVF method</span></span>

<span data-ttu-id="efde3-104">Clona uma malha usando um código de formato de vértice flexível (FVF).</span><span class="sxs-lookup"><span data-stu-id="efde3-104">Clones a mesh using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="efde3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efde3-105">Syntax</span></span>


```C++
HRESULT CloneMeshFVF(
  [in]          DWORD             Options,
  [in]          DWORD             FVF,
  [in]          LPDIRECT3DDEVICE9 pDevice,
  [out, retval] LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="efde3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efde3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efde3-107">*Opções* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="efde3-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efde3-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="efde3-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="efde3-109">Uma combinação de um ou mais sinalizadores [**D3DXMESH**](./d3dxmesh.md) especificando as opções de criação para a malha.</span><span class="sxs-lookup"><span data-stu-id="efde3-109">A combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="efde3-110">*FVF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="efde3-110">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efde3-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="efde3-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="efde3-112">Combinação de códigos FVF, que especifica o formato de vértice para os vértices na malha de saída.</span><span class="sxs-lookup"><span data-stu-id="efde3-112">Combination of FVF codes, which specifies the vertex format for the vertices in the output mesh.</span></span> <span data-ttu-id="efde3-113">Para obter os valores dos códigos, consulte [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="efde3-113">For the values of the codes, see [D3DFVF](d3dfvf.md).</span></span>

</dd> <dt>

<span data-ttu-id="efde3-114">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="efde3-114">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efde3-115">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="efde3-115">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="efde3-116">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa o objeto de dispositivo associado à malha.</span><span class="sxs-lookup"><span data-stu-id="efde3-116">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="efde3-117">*ppCloneMesh* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="efde3-117">*ppCloneMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="efde3-118">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="efde3-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="efde3-119">Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa a malha clonada.</span><span class="sxs-lookup"><span data-stu-id="efde3-119">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efde3-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="efde3-120">Return value</span></span>

<span data-ttu-id="efde3-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="efde3-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="efde3-122">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="efde3-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="efde3-123">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="efde3-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="efde3-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="efde3-124">Remarks</span></span>

<span data-ttu-id="efde3-125">**ID3DXBaseMesh:: CloneMeshFVF** é usado para reformatar e alterar o layout de dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="efde3-125">**ID3DXBaseMesh::CloneMeshFVF** is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="efde3-126">Isso é feito criando um novo objeto de malha.</span><span class="sxs-lookup"><span data-stu-id="efde3-126">This is done by creating a new mesh object.</span></span> <span data-ttu-id="efde3-127">Por exemplo, use-o para adicionar espaço para Normals, coordenadas de textura, cores, pesos, etc. que não estavam presentes antes.</span><span class="sxs-lookup"><span data-stu-id="efde3-127">For example, use it to to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="efde3-128">[**ID3DXBaseMesh:: UpdateSemantics**](id3dxbasemesh--updatesemantics.md) atualiza a declaração de vértice com informações semânticas diferentes sem alterar o layout do buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="efde3-128">[**ID3DXBaseMesh::UpdateSemantics**](id3dxbasemesh--updatesemantics.md) updates the vertex declaration with different semantic information without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="efde3-129">Esse método não modifica o conteúdo do buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="efde3-129">This method does not modify the contents of the vertex buffer.</span></span> <span data-ttu-id="efde3-130">Por exemplo, use-o para rerotular uma coordenada de textura 3D como uma binormal ou uma tangente ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="efde3-130">For example, use it to relabel a 3D texture coordinate as a binormal or tangent or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="efde3-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efde3-131">Requirements</span></span>



| <span data-ttu-id="efde3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="efde3-132">Requirement</span></span> | <span data-ttu-id="efde3-133">Valor</span><span class="sxs-lookup"><span data-stu-id="efde3-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="efde3-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="efde3-134">Header</span></span><br/>  | <dl> <span data-ttu-id="efde3-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="efde3-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="efde3-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="efde3-136">Library</span></span><br/> | <dl> <span data-ttu-id="efde3-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efde3-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="efde3-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="efde3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efde3-139">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="efde3-139">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="efde3-140">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="efde3-140">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
