---
description: Obtém o buffer de vértice de malha.
ms.assetid: 4ea4e99b-5c2c-467b-8b5d-8174c446680a
title: 'Método ID3DXPatchMesh:: GetVertexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b8c3bb79d4c04db072adef857de195df7a0f0fff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793891"
---
# <a name="id3dxpatchmeshgetvertexbuffer-method"></a><span data-ttu-id="d86f9-103">Método ID3DXPatchMesh:: GetVertexBuffer</span><span class="sxs-lookup"><span data-stu-id="d86f9-103">ID3DXPatchMesh::GetVertexBuffer method</span></span>

<span data-ttu-id="d86f9-104">Obtém o buffer de vértice de malha.</span><span class="sxs-lookup"><span data-stu-id="d86f9-104">Gets the mesh vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d86f9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d86f9-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [out] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a><span data-ttu-id="d86f9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d86f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d86f9-107">*ppVB* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d86f9-107">*ppVB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d86f9-108">Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="d86f9-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span></span>

<span data-ttu-id="d86f9-109">Ponteiro para o buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="d86f9-109">Pointer to the vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d86f9-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d86f9-110">Return value</span></span>

<span data-ttu-id="d86f9-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d86f9-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d86f9-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d86f9-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d86f9-113">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d86f9-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d86f9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d86f9-114">Remarks</span></span>

<span data-ttu-id="d86f9-115">Esse método pressupõe mosaico uniforme.</span><span class="sxs-lookup"><span data-stu-id="d86f9-115">This method assumes uniform tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="d86f9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d86f9-116">Requirements</span></span>



| <span data-ttu-id="d86f9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d86f9-117">Requirement</span></span> | <span data-ttu-id="d86f9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d86f9-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d86f9-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d86f9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d86f9-120"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d86f9-120"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d86f9-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d86f9-121">Library</span></span><br/> | <dl> <span data-ttu-id="d86f9-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d86f9-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d86f9-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d86f9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d86f9-124">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="d86f9-124">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
