---
description: 'Método ID3DXMesh:: SetAttributeTable – define a tabela de atributos para uma malha e o número de entradas armazenadas na tabela.'
ms.assetid: 22d46708-cffd-48da-bdad-8a43f9076356
title: 'Método ID3DXMesh:: SetAttributeTable (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.SetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4cdb503e934ca00b41482601b59266eee750365
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093344"
---
# <a name="id3dxmeshsetattributetable-method"></a><span data-ttu-id="34d74-103">Método ID3DXMesh:: SetAttributeTable</span><span class="sxs-lookup"><span data-stu-id="34d74-103">ID3DXMesh::SetAttributeTable method</span></span>

<span data-ttu-id="34d74-104">Define a tabela de atributos para uma malha e o número de entradas armazenadas na tabela.</span><span class="sxs-lookup"><span data-stu-id="34d74-104">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="34d74-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34d74-105">Syntax</span></span>


```C++
HRESULT SetAttributeTable(
  [in] const D3DXATTRIBUTERANGE *pAttribTable,
  [in]       DWORD              cAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="34d74-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34d74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34d74-107">*pAttribTable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="34d74-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34d74-108">Tipo: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) \***</span><span class="sxs-lookup"><span data-stu-id="34d74-108">Type: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span></span>

<span data-ttu-id="34d74-109">Ponteiro para uma matriz de estruturas [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) , representando as entradas na tabela de atributos de malha.</span><span class="sxs-lookup"><span data-stu-id="34d74-109">Pointer to an array of [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) structures, representing the entries in the mesh attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="34d74-110">*cAttribTableSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="34d74-110">*cAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34d74-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34d74-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34d74-112">Número de atributos na tabela de atributos de malha.</span><span class="sxs-lookup"><span data-stu-id="34d74-112">Number of attributes in the mesh attribute table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34d74-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="34d74-113">Return value</span></span>

<span data-ttu-id="34d74-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="34d74-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="34d74-115">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="34d74-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="34d74-116">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="34d74-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="34d74-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="34d74-117">Remarks</span></span>

<span data-ttu-id="34d74-118">Se um aplicativo acompanhar as informações em uma tabela de atributos e reorganizar a tabela como resultado de alterações em atributos ou rostos, esse método permitirá que o aplicativo atualize as tabelas de atributos em vez de chamar [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) novamente.</span><span class="sxs-lookup"><span data-stu-id="34d74-118">If an application keeps track of the information in an attribute table, and rearranges the table as a result of changes to attributes or faces, this method allows the application to update the attribute tables instead of calling [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) again.</span></span>

## <a name="requirements"></a><span data-ttu-id="34d74-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34d74-119">Requirements</span></span>



| <span data-ttu-id="34d74-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="34d74-120">Requirement</span></span> | <span data-ttu-id="34d74-121">Valor</span><span class="sxs-lookup"><span data-stu-id="34d74-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34d74-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="34d74-122">Header</span></span><br/>  | <dl> <span data-ttu-id="34d74-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="34d74-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="34d74-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="34d74-124">Library</span></span><br/> | <dl> <span data-ttu-id="34d74-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34d74-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="34d74-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="34d74-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34d74-127">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="34d74-127">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="34d74-128">**ID3DXMesh::LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="34d74-128">**ID3DXMesh::LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

<span data-ttu-id="34d74-129">**ID3DXMesh::LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="34d74-129">**ID3DXMesh::LockAttributeBuffer**</span></span>
</dt> </dl>

 

 
