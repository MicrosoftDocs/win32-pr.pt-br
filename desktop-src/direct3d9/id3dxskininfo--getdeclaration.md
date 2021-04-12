---
description: Obtém a declaração de vértice.
ms.assetid: 49738e9b-09cb-489f-b9af-32d220fbede8
title: 'Método ID3DXSkinInfo:: getdeclaration (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de80694bbbb6eea29f391b3b39cff9caacd4791c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298462"
---
# <a name="id3dxskininfogetdeclaration-method"></a><span data-ttu-id="2570a-103">Método ID3DXSkinInfo:: getdeclaration</span><span class="sxs-lookup"><span data-stu-id="2570a-103">ID3DXSkinInfo::GetDeclaration method</span></span>

<span data-ttu-id="2570a-104">Obtém a declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="2570a-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="2570a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2570a-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="2570a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2570a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2570a-107">*Declaração* \[ de entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="2570a-107">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2570a-108">Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="2570a-108">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="2570a-109">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) que descreve o formato de vértice dos vértices de malha.</span><span class="sxs-lookup"><span data-stu-id="2570a-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="2570a-110">O limite superior dessa matriz de Declarador é o [**tamanho máximo de \_ \_ DECL \_ FVF**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="2570a-110">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="2570a-111">A matriz do elemento Vertex termina com a macro [**\_ end D3DDECL**](d3ddecl-end.md) .</span><span class="sxs-lookup"><span data-stu-id="2570a-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2570a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2570a-112">Return value</span></span>

<span data-ttu-id="2570a-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2570a-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2570a-114">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2570a-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2570a-115">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2570a-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2570a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2570a-116">Remarks</span></span>

<span data-ttu-id="2570a-117">A matriz de elementos inclui a macro [**D3DDECL \_ end**](d3ddecl-end.md) , que encerra a declaração.</span><span class="sxs-lookup"><span data-stu-id="2570a-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="2570a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2570a-118">Requirements</span></span>



| <span data-ttu-id="2570a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2570a-119">Requirement</span></span> | <span data-ttu-id="2570a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2570a-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2570a-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2570a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2570a-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2570a-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2570a-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2570a-123">Library</span></span><br/> | <dl> <span data-ttu-id="2570a-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2570a-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2570a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2570a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2570a-126">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="2570a-126">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="2570a-127">**ID3DXSkinInfo:: setdeclaration**</span><span class="sxs-lookup"><span data-stu-id="2570a-127">**ID3DXSkinInfo::SetDeclaration**</span></span>](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 
