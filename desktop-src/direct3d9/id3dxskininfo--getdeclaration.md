---
description: 'Método ID3DXSkinInfo:: getdeclaration-Obtém a declaração de vértice.'
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
ms.openlocfilehash: 83554b13fe8e20890b1edecd690c540c2e14d4d7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093134"
---
# <a name="id3dxskininfogetdeclaration-method"></a><span data-ttu-id="2e861-103">Método ID3DXSkinInfo:: getdeclaration</span><span class="sxs-lookup"><span data-stu-id="2e861-103">ID3DXSkinInfo::GetDeclaration method</span></span>

<span data-ttu-id="2e861-104">Obtém a declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="2e861-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e861-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e861-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="2e861-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e861-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e861-107">*Declaração* \[ de entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="2e861-107">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e861-108">Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="2e861-108">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="2e861-109">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) que descreve o formato de vértice dos vértices de malha.</span><span class="sxs-lookup"><span data-stu-id="2e861-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="2e861-110">O limite superior dessa matriz de Declarador é o [**tamanho máximo de \_ \_ DECL \_ FVF**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="2e861-110">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="2e861-111">A matriz do elemento Vertex termina com a macro [**\_ end D3DDECL**](d3ddecl-end.md) .</span><span class="sxs-lookup"><span data-stu-id="2e861-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e861-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2e861-112">Return value</span></span>

<span data-ttu-id="2e861-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2e861-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2e861-114">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2e861-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2e861-115">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2e861-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e861-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e861-116">Remarks</span></span>

<span data-ttu-id="2e861-117">A matriz de elementos inclui a macro [**D3DDECL \_ end**](d3ddecl-end.md) , que encerra a declaração.</span><span class="sxs-lookup"><span data-stu-id="2e861-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e861-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e861-118">Requirements</span></span>



| <span data-ttu-id="2e861-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e861-119">Requirement</span></span> | <span data-ttu-id="2e861-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2e861-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e861-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e861-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2e861-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e861-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2e861-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e861-123">Library</span></span><br/> | <dl> <span data-ttu-id="2e861-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e861-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2e861-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2e861-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e861-126">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="2e861-126">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="2e861-127">**ID3DXSkinInfo:: setdeclaration**</span><span class="sxs-lookup"><span data-stu-id="2e861-127">**ID3DXSkinInfo::SetDeclaration**</span></span>](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 
