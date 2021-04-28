---
description: Estrutura D3DXATTRIBUTERANGE – armazena uma entrada de tabela de atributo.
ms.assetid: b9f13b12-35ba-4e4c-93ac-3dd44d611b47
title: Estrutura D3DXATTRIBUTERANGE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTERANGE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7dfdf15f653fda77b1ca8c9a14cd32decee9658e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116004"
---
# <a name="d3dxattributerange-structure"></a><span data-ttu-id="18edb-103">Estrutura D3DXATTRIBUTERANGE</span><span class="sxs-lookup"><span data-stu-id="18edb-103">D3DXATTRIBUTERANGE structure</span></span>

<span data-ttu-id="18edb-104">Armazena uma entrada de tabela de atributo.</span><span class="sxs-lookup"><span data-stu-id="18edb-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="18edb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18edb-105">Syntax</span></span>


```C++
typedef struct D3DXATTRIBUTERANGE {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
} D3DXATTRIBUTERANGE, *LPD3DXATTRIBUTERANGE;
```



## <a name="members"></a><span data-ttu-id="18edb-106">Membros</span><span class="sxs-lookup"><span data-stu-id="18edb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="18edb-107">**Atribid**</span><span class="sxs-lookup"><span data-stu-id="18edb-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="18edb-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18edb-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="18edb-109">Identificador de tabela de atributo.</span><span class="sxs-lookup"><span data-stu-id="18edb-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="18edb-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="18edb-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="18edb-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18edb-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="18edb-112">Iniciando face.</span><span class="sxs-lookup"><span data-stu-id="18edb-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="18edb-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="18edb-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="18edb-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18edb-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="18edb-115">Contagem de face.</span><span class="sxs-lookup"><span data-stu-id="18edb-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="18edb-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="18edb-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="18edb-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18edb-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="18edb-118">Iniciando vértice.</span><span class="sxs-lookup"><span data-stu-id="18edb-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="18edb-119">**Contagemdevértice**</span><span class="sxs-lookup"><span data-stu-id="18edb-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="18edb-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18edb-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="18edb-121">Contagem de vértices.</span><span class="sxs-lookup"><span data-stu-id="18edb-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18edb-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="18edb-122">Remarks</span></span>

<span data-ttu-id="18edb-123">Uma tabela de atributos é usada para identificar áreas da malha que precisam ser desenhadas com texturas diferentes, Estados de renderização, materiais e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="18edb-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="18edb-124">Além disso, o aplicativo pode usar a tabela de atributos para ocultar partes de uma malha por não desenhar um determinado identificador de atributo (attrib) ao desenhar o quadro.</span><span class="sxs-lookup"><span data-stu-id="18edb-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="18edb-125">O tipo LPD3DXATTRIBUTERANGE é definido como um ponteiro para a estrutura **D3DXATTRIBUTERANGE** .</span><span class="sxs-lookup"><span data-stu-id="18edb-125">The LPD3DXATTRIBUTERANGE type is defined as a pointer to the **D3DXATTRIBUTERANGE** structure.</span></span>


```
typedef D3DXATTRIBUTERANGE* LPD3DXATTRIBUTERANGE;
```



## <a name="requirements"></a><span data-ttu-id="18edb-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18edb-126">Requirements</span></span>



| <span data-ttu-id="18edb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="18edb-127">Requirement</span></span> | <span data-ttu-id="18edb-128">Valor</span><span class="sxs-lookup"><span data-stu-id="18edb-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18edb-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="18edb-129">Header</span></span><br/> | <dl> <span data-ttu-id="18edb-130"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="18edb-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18edb-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="18edb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18edb-132">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="18edb-132">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
