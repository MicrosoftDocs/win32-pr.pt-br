---
description: Recupera o buffer de vértice associado à malha.
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
ms.openlocfilehash: b78db368f2467c25b4bb4218a314a22027d5d3f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105789333"
---
# <a name="id3dx10meshgetvertexbuffer-method"></a><span data-ttu-id="b6670-103">Método ID3DX10Mesh:: GetVertexBuffer</span><span class="sxs-lookup"><span data-stu-id="b6670-103">ID3DX10Mesh::GetVertexBuffer method</span></span>

<span data-ttu-id="b6670-104">Recupera o buffer de vértice associado à malha.</span><span class="sxs-lookup"><span data-stu-id="b6670-104">Retrieves the vertex buffer associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6670-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6670-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [in]  UINT              iBuffer,
  [out] ID3DX10MeshBuffer **ppVertexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="b6670-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6670-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6670-107">*iBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6670-107">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6670-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6670-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6670-109">O buffer de vértice a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="b6670-109">The vertex buffer to get.</span></span> <span data-ttu-id="b6670-110">Este é um valor de índice.</span><span class="sxs-lookup"><span data-stu-id="b6670-110">This is an index value.</span></span>

</dd> <dt>

<span data-ttu-id="b6670-111">*ppVertexBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b6670-111">*ppVertexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6670-112">Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b6670-112">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="b6670-113">O buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="b6670-113">The vertex buffer.</span></span> <span data-ttu-id="b6670-114">Consulte [ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="b6670-114">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6670-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6670-115">Return value</span></span>

<span data-ttu-id="b6670-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b6670-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b6670-117">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b6670-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6670-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6670-118">Requirements</span></span>



| <span data-ttu-id="b6670-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6670-119">Requirement</span></span> | <span data-ttu-id="b6670-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b6670-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6670-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6670-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b6670-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6670-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6670-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b6670-123">Library</span></span><br/> | <dl> <span data-ttu-id="b6670-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6670-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6670-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6670-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6670-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="b6670-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="b6670-127">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="b6670-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
