---
description: 'Método ID3DX10Mesh:: GetVertexBuffer – recupera o buffer de vértice associado à malha.'
ms.assetid: c69a712b-8964-4a5b-a136-3f24060b7fd8
title: 'Método ID3DX10Mesh:: GetVertexBuffer (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a63b08cf978a65e1fa9999c79b8033436b41fa2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108074"
---
# <a name="id3dx10meshgetvertexbuffer-method"></a><span data-ttu-id="ce15b-103">Método ID3DX10Mesh:: GetVertexBuffer</span><span class="sxs-lookup"><span data-stu-id="ce15b-103">ID3DX10Mesh::GetVertexBuffer method</span></span>

<span data-ttu-id="ce15b-104">Recupera o buffer de vértice associado à malha.</span><span class="sxs-lookup"><span data-stu-id="ce15b-104">Retrieves the vertex buffer associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce15b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce15b-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [in]  UINT              iBuffer,
  [out] ID3DX10MeshBuffer **ppVertexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="ce15b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce15b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce15b-107">*iBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce15b-107">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce15b-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce15b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce15b-109">O buffer de vértice a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="ce15b-109">The vertex buffer to get.</span></span> <span data-ttu-id="ce15b-110">Este é um valor de índice.</span><span class="sxs-lookup"><span data-stu-id="ce15b-110">This is an index value.</span></span>

</dd> <dt>

<span data-ttu-id="ce15b-111">*ppVertexBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ce15b-111">*ppVertexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce15b-112">Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ce15b-112">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="ce15b-113">O buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="ce15b-113">The vertex buffer.</span></span> <span data-ttu-id="ce15b-114">Consulte [ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="ce15b-114">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce15b-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ce15b-115">Return value</span></span>

<span data-ttu-id="ce15b-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce15b-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce15b-117">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ce15b-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce15b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce15b-118">Requirements</span></span>



| <span data-ttu-id="ce15b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce15b-119">Requirement</span></span> | <span data-ttu-id="ce15b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ce15b-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce15b-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce15b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ce15b-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce15b-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ce15b-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce15b-123">Library</span></span><br/> | <dl> <span data-ttu-id="ce15b-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce15b-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce15b-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ce15b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce15b-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="ce15b-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="ce15b-127">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="ce15b-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
