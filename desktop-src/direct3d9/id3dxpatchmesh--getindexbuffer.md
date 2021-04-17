---
description: Obtém o buffer do índice de malha.
ms.assetid: d9152f3b-c8e6-4def-8cf1-a517ca4d34e7
title: 'Método ID3DXPatchMesh:: GetIndexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c2730b90f77d33db519d2231a68ab7fdc2b520fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791057"
---
# <a name="id3dxpatchmeshgetindexbuffer-method"></a><span data-ttu-id="deb98-103">Método ID3DXPatchMesh:: GetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="deb98-103">ID3DXPatchMesh::GetIndexBuffer method</span></span>

<span data-ttu-id="deb98-104">Obtém o buffer do índice de malha.</span><span class="sxs-lookup"><span data-stu-id="deb98-104">Gets the mesh index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="deb98-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="deb98-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a><span data-ttu-id="deb98-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="deb98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deb98-107">*ppIB* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="deb98-107">*ppIB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="deb98-108">Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="deb98-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="deb98-109">Ponteiro para o buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="deb98-109">Pointer to the index buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deb98-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="deb98-110">Return value</span></span>

<span data-ttu-id="deb98-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="deb98-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="deb98-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="deb98-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="deb98-113">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="deb98-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="deb98-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="deb98-114">Remarks</span></span>

<span data-ttu-id="deb98-115">O buffer de índice contém a ordenação de vértice no buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="deb98-115">The index buffer contains the vertex ordering in the vertex buffer.</span></span> <span data-ttu-id="deb98-116">O buffer de índice é usado para acessar o buffer de vértice quando a malha é renderizada.</span><span class="sxs-lookup"><span data-stu-id="deb98-116">The index buffer is used to access the vertex buffer when the mesh is rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="deb98-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="deb98-117">Requirements</span></span>



| <span data-ttu-id="deb98-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="deb98-118">Requirement</span></span> | <span data-ttu-id="deb98-119">Valor</span><span class="sxs-lookup"><span data-stu-id="deb98-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="deb98-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="deb98-120">Header</span></span><br/>  | <dl> <span data-ttu-id="deb98-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="deb98-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="deb98-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="deb98-122">Library</span></span><br/> | <dl> <span data-ttu-id="deb98-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="deb98-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="deb98-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="deb98-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deb98-125">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="deb98-125">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
