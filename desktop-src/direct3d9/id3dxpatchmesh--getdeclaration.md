---
description: 'Método ID3DXPatchMesh:: getdeclaration-Obtém a declaração de vértice.'
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: 'Método ID3DXPatchMesh:: getdeclaration (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0fde070b1b013e651c84ffea7098eb8225aed8f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093294"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a><span data-ttu-id="687b4-103">Método ID3DXPatchMesh:: getdeclaration</span><span class="sxs-lookup"><span data-stu-id="687b4-103">ID3DXPatchMesh::GetDeclaration method</span></span>

<span data-ttu-id="687b4-104">Obtém a declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="687b4-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="687b4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="687b4-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a><span data-ttu-id="687b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="687b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="687b4-107">*pDeclaration* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="687b4-107">*pDeclaration* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="687b4-108">Tipo: **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="687b4-108">Type: **[**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="687b4-109">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) que descreve o formato de vértice dos vértices de malha.</span><span class="sxs-lookup"><span data-stu-id="687b4-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="687b4-110">A dimensão dessa matriz de Declarador é o [**tamanho máximo de \_ \_ DECL \_ FVF**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="687b4-110">The dimension of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="687b4-111">A matriz do elemento Vertex termina com a macro [**\_ end D3DDECL**](d3ddecl-end.md) .</span><span class="sxs-lookup"><span data-stu-id="687b4-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="687b4-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="687b4-112">Return value</span></span>

<span data-ttu-id="687b4-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="687b4-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="687b4-114">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="687b4-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="687b4-115">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="687b4-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="687b4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="687b4-116">Remarks</span></span>

<span data-ttu-id="687b4-117">A matriz de elementos inclui a macro [**D3DDECL \_ end**](d3ddecl-end.md) , que encerra a declaração.</span><span class="sxs-lookup"><span data-stu-id="687b4-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="687b4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="687b4-118">Requirements</span></span>



| <span data-ttu-id="687b4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="687b4-119">Requirement</span></span> | <span data-ttu-id="687b4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="687b4-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="687b4-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="687b4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="687b4-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="687b4-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="687b4-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="687b4-123">Library</span></span><br/> | <dl> <span data-ttu-id="687b4-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="687b4-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="687b4-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="687b4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="687b4-126">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="687b4-126">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
