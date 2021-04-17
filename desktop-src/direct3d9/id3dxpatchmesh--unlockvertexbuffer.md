---
description: Desbloqueie o buffer de vértice.
ms.assetid: 98b82fd1-56e8-45f3-bf26-a1e3b54c2979
title: 'Método ID3DXPatchMesh:: UnlockVertexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c6d4b6a55281048b303733e1addf2ab4636f74ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105770595"
---
# <a name="id3dxpatchmeshunlockvertexbuffer-method"></a><span data-ttu-id="81243-103">Método ID3DXPatchMesh:: UnlockVertexBuffer</span><span class="sxs-lookup"><span data-stu-id="81243-103">ID3DXPatchMesh::UnlockVertexBuffer method</span></span>

<span data-ttu-id="81243-104">Desbloqueie o buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="81243-104">Unlock the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="81243-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81243-105">Syntax</span></span>


```C++
HRESULT UnlockVertexBuffer();
```



## <a name="parameters"></a><span data-ttu-id="81243-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81243-106">Parameters</span></span>

<span data-ttu-id="81243-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="81243-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81243-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="81243-108">Return value</span></span>

<span data-ttu-id="81243-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="81243-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="81243-110">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="81243-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="81243-111">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="81243-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="81243-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="81243-112">Remarks</span></span>

<span data-ttu-id="81243-113">O buffer de vértice é geralmente bloqueado, gravado e, em seguida, desbloqueado para leitura.</span><span class="sxs-lookup"><span data-stu-id="81243-113">The vertex buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="81243-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81243-114">Requirements</span></span>



| <span data-ttu-id="81243-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="81243-115">Requirement</span></span> | <span data-ttu-id="81243-116">Valor</span><span class="sxs-lookup"><span data-stu-id="81243-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81243-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81243-117">Header</span></span><br/>  | <dl> <span data-ttu-id="81243-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="81243-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="81243-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81243-119">Library</span></span><br/> | <dl> <span data-ttu-id="81243-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81243-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="81243-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="81243-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81243-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="81243-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




