---
description: 'Método ID3DXBaseMesh:: GetVertexBuffer – recupera o buffer de vértice associado à malha.'
ms.assetid: 5caa6ce1-feab-4919-944e-f92fad3ad443
title: 'Método ID3DXBaseMesh:: GetVertexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9533188e3e2effe1759b58f70c9f033cc491844c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115364"
---
# <a name="id3dxbasemeshgetvertexbuffer-method"></a><span data-ttu-id="01a97-103">Método ID3DXBaseMesh:: GetVertexBuffer</span><span class="sxs-lookup"><span data-stu-id="01a97-103">ID3DXBaseMesh::GetVertexBuffer method</span></span>

<span data-ttu-id="01a97-104">Recupera o buffer de vértice associado à malha.</span><span class="sxs-lookup"><span data-stu-id="01a97-104">Retrieves the vertex buffer associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="01a97-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01a97-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [out, retval] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a><span data-ttu-id="01a97-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01a97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01a97-107">*ppVB* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="01a97-107">*ppVB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="01a97-108">Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="01a97-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span></span>

<span data-ttu-id="01a97-109">Endereço de um ponteiro para uma interface [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) , que representa o objeto de buffer de vértice associado à malha.</span><span class="sxs-lookup"><span data-stu-id="01a97-109">Address of a pointer to an [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) interface, representing the vertex buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01a97-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="01a97-110">Return value</span></span>

<span data-ttu-id="01a97-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="01a97-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="01a97-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="01a97-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="01a97-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="01a97-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="01a97-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01a97-114">Requirements</span></span>



| <span data-ttu-id="01a97-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="01a97-115">Requirement</span></span> | <span data-ttu-id="01a97-116">Valor</span><span class="sxs-lookup"><span data-stu-id="01a97-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01a97-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01a97-117">Header</span></span><br/>  | <dl> <span data-ttu-id="01a97-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="01a97-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="01a97-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01a97-119">Library</span></span><br/> | <dl> <span data-ttu-id="01a97-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01a97-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="01a97-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="01a97-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a97-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="01a97-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
