---
description: Clona uma malha usando um Declarador.
ms.assetid: 47e0329a-ea85-478d-af8b-cf85d2a779f6
title: 'Método ID3DXBaseMesh:: CloneMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 421b72a080564886a10c187594223fb58a0b69fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105789392"
---
# <a name="id3dxbasemeshclonemesh-method"></a><span data-ttu-id="d1125-103">Método ID3DXBaseMesh:: CloneMesh</span><span class="sxs-lookup"><span data-stu-id="d1125-103">ID3DXBaseMesh::CloneMesh method</span></span>

<span data-ttu-id="d1125-104">Clona uma malha usando um Declarador.</span><span class="sxs-lookup"><span data-stu-id="d1125-104">Clones a mesh using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1125-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1125-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDeclaration,
  [in]                LPDIRECT3DDEVICE9 pDevice,
  [out, retval]       LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="d1125-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1125-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1125-107">*Opções* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="d1125-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1125-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1125-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d1125-109">Uma combinação de um ou mais sinalizadores [**D3DXMESH**](./d3dxmesh.md) especificando as opções de criação para a malha.</span><span class="sxs-lookup"><span data-stu-id="d1125-109">A combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d1125-110">*pDeclaration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1125-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1125-111">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="d1125-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="d1125-112">Uma matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , que especifica o formato de vértice para os vértices na malha de saída.</span><span class="sxs-lookup"><span data-stu-id="d1125-112">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, which specify the vertex format for the vertices in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d1125-113">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1125-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1125-114">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d1125-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d1125-115">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o objeto de dispositivo associado à malha.</span><span class="sxs-lookup"><span data-stu-id="d1125-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d1125-116">*ppCloneMesh* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d1125-116">*ppCloneMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d1125-117">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="d1125-117">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="d1125-118">Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa a malha clonada.</span><span class="sxs-lookup"><span data-stu-id="d1125-118">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1125-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1125-119">Return value</span></span>

<span data-ttu-id="d1125-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d1125-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d1125-121">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d1125-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d1125-122">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d1125-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1125-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1125-123">Remarks</span></span>

<span data-ttu-id="d1125-124">**ID3DXBaseMesh:: CloneMesh** é usado para reformatar e alterar o layout de dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="d1125-124">**ID3DXBaseMesh::CloneMesh** is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="d1125-125">Isso é feito criando um novo objeto de malha.</span><span class="sxs-lookup"><span data-stu-id="d1125-125">This is done by creating a new mesh object.</span></span> <span data-ttu-id="d1125-126">Por exemplo, use-o para adicionar espaço para normais, coordenadas de textura, cores, pesos, etc. que não estavam presentes antes.</span><span class="sxs-lookup"><span data-stu-id="d1125-126">For example, use it to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="d1125-127">[**ID3DXBaseMesh:: UpdateSemantics**](id3dxbasemesh--updatesemantics.md) atualiza a declaração de vértice com informações semânticas diferentes sem alterar o layout do buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="d1125-127">[**ID3DXBaseMesh::UpdateSemantics**](id3dxbasemesh--updatesemantics.md) updates the vertex declaration with different semantic information without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="d1125-128">Esse método não modifica o conteúdo do buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="d1125-128">This method does not modify the contents of the vertex buffer.</span></span> <span data-ttu-id="d1125-129">Por exemplo, use-o para rerotular uma coordenada de textura 3D como uma binormal ou uma tangente ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="d1125-129">For example, use it to relabel a 3D texture coordinate as a binormal or tangent or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1125-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1125-130">Requirements</span></span>



| <span data-ttu-id="d1125-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1125-131">Requirement</span></span> | <span data-ttu-id="d1125-132">Valor</span><span class="sxs-lookup"><span data-stu-id="d1125-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1125-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1125-133">Header</span></span><br/>  | <dl> <span data-ttu-id="d1125-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1125-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d1125-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1125-135">Library</span></span><br/> | <dl> <span data-ttu-id="d1125-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1125-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d1125-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1125-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1125-138">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="d1125-138">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="d1125-139">**ID3DXBaseMesh::CloneMeshFVF**</span><span class="sxs-lookup"><span data-stu-id="d1125-139">**ID3DXBaseMesh::CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[<span data-ttu-id="d1125-140">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="d1125-140">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
