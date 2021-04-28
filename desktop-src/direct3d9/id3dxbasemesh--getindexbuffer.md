---
description: 'Método ID3DXBaseMesh:: GetIndexBuffer – recupera os dados em um buffer de índice.'
ms.assetid: 8e14a047-a8a6-4763-88c7-3b439044eeb4
title: 'Método ID3DXBaseMesh:: GetIndexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 40e57193a2bf9a47ed0c57e6d13644441fbc42ce
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115424"
---
# <a name="id3dxbasemeshgetindexbuffer-method"></a><span data-ttu-id="a3780-103">Método ID3DXBaseMesh:: GetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="a3780-103">ID3DXBaseMesh::GetIndexBuffer method</span></span>

<span data-ttu-id="a3780-104">Recupera os dados em um buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="a3780-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3780-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3780-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a><span data-ttu-id="a3780-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3780-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3780-107">*ppIB* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a3780-107">*ppIB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a3780-108">Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="a3780-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="a3780-109">Endereço de um ponteiro para uma interface [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , representando o objeto de buffer de índice associado à malha.</span><span class="sxs-lookup"><span data-stu-id="a3780-109">Address of a pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing the index buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3780-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a3780-110">Return value</span></span>

<span data-ttu-id="a3780-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a3780-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a3780-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a3780-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a3780-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a3780-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3780-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3780-114">Requirements</span></span>



| <span data-ttu-id="a3780-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3780-115">Requirement</span></span> | <span data-ttu-id="a3780-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a3780-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3780-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a3780-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a3780-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3780-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a3780-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a3780-119">Library</span></span><br/> | <dl> <span data-ttu-id="a3780-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3780-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a3780-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a3780-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3780-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="a3780-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
