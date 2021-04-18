---
description: Recupera o buffer de vértice associado à malha.
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
ms.openlocfilehash: 2098d97c1b7a685e9bd68cb3a6ac4feb6b949d2a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781142"
---
# <a name="id3dxbasemeshgetvertexbuffer-method"></a><span data-ttu-id="1031e-103">Método ID3DXBaseMesh:: GetVertexBuffer</span><span class="sxs-lookup"><span data-stu-id="1031e-103">ID3DXBaseMesh::GetVertexBuffer method</span></span>

<span data-ttu-id="1031e-104">Recupera o buffer de vértice associado à malha.</span><span class="sxs-lookup"><span data-stu-id="1031e-104">Retrieves the vertex buffer associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="1031e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1031e-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [out, retval] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a><span data-ttu-id="1031e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1031e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1031e-107">*ppVB* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1031e-107">*ppVB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1031e-108">Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="1031e-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span></span>

<span data-ttu-id="1031e-109">Endereço de um ponteiro para uma interface [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) , que representa o objeto de buffer de vértice associado à malha.</span><span class="sxs-lookup"><span data-stu-id="1031e-109">Address of a pointer to an [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) interface, representing the vertex buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1031e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1031e-110">Return value</span></span>

<span data-ttu-id="1031e-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1031e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1031e-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1031e-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1031e-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1031e-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1031e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1031e-114">Requirements</span></span>



| <span data-ttu-id="1031e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1031e-115">Requirement</span></span> | <span data-ttu-id="1031e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1031e-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1031e-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1031e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1031e-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1031e-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1031e-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1031e-119">Library</span></span><br/> | <dl> <span data-ttu-id="1031e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1031e-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1031e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="1031e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1031e-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="1031e-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
