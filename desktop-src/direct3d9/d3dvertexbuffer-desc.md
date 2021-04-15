---
description: Descreve um buffer de vértice.
ms.assetid: 0ae8f976-d0ca-4d55-b6db-5be85fa3c799
title: Estrutura de D3DVERTEXBUFFER_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b2c0838743f8190eeb0e5c825e7125d2e48c0b6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506505"
---
# <a name="d3dvertexbuffer_desc-structure"></a><span data-ttu-id="b7586-103">\_Estrutura desc de D3DVERTEXBUFFER</span><span class="sxs-lookup"><span data-stu-id="b7586-103">D3DVERTEXBUFFER\_DESC structure</span></span>

<span data-ttu-id="b7586-104">Descreve um buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="b7586-104">Describes a vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7586-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7586-105">Syntax</span></span>


```C++
typedef struct D3DVERTEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
  DWORD           FVF;
} D3DVERTEXBUFFER_DESC, *LPD3DVERTEXBUFFER_DESC;
```



## <a name="members"></a><span data-ttu-id="b7586-106">Membros</span><span class="sxs-lookup"><span data-stu-id="b7586-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b7586-107">**Formato**</span><span class="sxs-lookup"><span data-stu-id="b7586-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="b7586-108">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="b7586-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b7586-109">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato da superfície dos dados do buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="b7586-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the vertex buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="b7586-110">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b7586-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="b7586-111">Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="b7586-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b7586-112">Membro do tipo enumerado [**D3DRESOURCETYPE**](./d3dresourcetype.md) , identificando esse recurso como um buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="b7586-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b7586-113">**Usage**</span><span class="sxs-lookup"><span data-stu-id="b7586-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="b7586-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7586-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b7586-115">Combinação de um ou mais sinalizadores [**D3DUSAGE**](d3dusage.md) .</span><span class="sxs-lookup"><span data-stu-id="b7586-115">Combination of one or more [**D3DUSAGE**](d3dusage.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="b7586-116">**Pool**</span><span class="sxs-lookup"><span data-stu-id="b7586-116">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="b7586-117">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="b7586-117">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b7586-118">Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , especificando a classe de memória alocada para este buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="b7586-118">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b7586-119">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="b7586-119">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="b7586-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7586-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b7586-121">Tamanho do buffer de vértice, em bytes.</span><span class="sxs-lookup"><span data-stu-id="b7586-121">Size of the vertex buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b7586-122">**FVF**</span><span class="sxs-lookup"><span data-stu-id="b7586-122">**FVF**</span></span>
</dt> <dd>

<span data-ttu-id="b7586-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7586-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b7586-124">Combinação de [D3DFVF](d3dfvf.md) que descreve o formato de vértice dos vértices nesse buffer.</span><span class="sxs-lookup"><span data-stu-id="b7586-124">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format of the vertices in this buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7586-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7586-125">Requirements</span></span>



| <span data-ttu-id="b7586-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7586-126">Requirement</span></span> | <span data-ttu-id="b7586-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b7586-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7586-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7586-128">Header</span></span><br/> | <dl> <span data-ttu-id="b7586-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7586-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7586-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7586-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7586-131">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="b7586-131">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="b7586-132">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="b7586-132">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-getdesc)
</dt> <dt>

[<span data-ttu-id="b7586-133">Buffers de vértice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b7586-133">Vertex Buffers (Direct3D 9)</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
