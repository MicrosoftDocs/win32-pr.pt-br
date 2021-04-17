---
description: Armazena uma entrada de tabela de atributo.
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
ms.openlocfilehash: a842bbf41847f4b4e65c975e11f3e160cea1422d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105782383"
---
# <a name="d3dxattributerange-structure"></a><span data-ttu-id="3eb24-103">Estrutura D3DXATTRIBUTERANGE</span><span class="sxs-lookup"><span data-stu-id="3eb24-103">D3DXATTRIBUTERANGE structure</span></span>

<span data-ttu-id="3eb24-104">Armazena uma entrada de tabela de atributo.</span><span class="sxs-lookup"><span data-stu-id="3eb24-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eb24-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3eb24-105">Syntax</span></span>


```C++
typedef struct D3DXATTRIBUTERANGE {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
} D3DXATTRIBUTERANGE, *LPD3DXATTRIBUTERANGE;
```



## <a name="members"></a><span data-ttu-id="3eb24-106">Membros</span><span class="sxs-lookup"><span data-stu-id="3eb24-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3eb24-107">**Atribid**</span><span class="sxs-lookup"><span data-stu-id="3eb24-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="3eb24-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3eb24-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3eb24-109">Identificador de tabela de atributo.</span><span class="sxs-lookup"><span data-stu-id="3eb24-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="3eb24-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="3eb24-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="3eb24-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3eb24-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3eb24-112">Iniciando face.</span><span class="sxs-lookup"><span data-stu-id="3eb24-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="3eb24-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="3eb24-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="3eb24-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3eb24-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3eb24-115">Contagem de face.</span><span class="sxs-lookup"><span data-stu-id="3eb24-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="3eb24-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="3eb24-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="3eb24-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3eb24-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3eb24-118">Iniciando vértice.</span><span class="sxs-lookup"><span data-stu-id="3eb24-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="3eb24-119">**Contagemdevértice**</span><span class="sxs-lookup"><span data-stu-id="3eb24-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="3eb24-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3eb24-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3eb24-121">Contagem de vértices.</span><span class="sxs-lookup"><span data-stu-id="3eb24-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3eb24-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="3eb24-122">Remarks</span></span>

<span data-ttu-id="3eb24-123">Uma tabela de atributos é usada para identificar áreas da malha que precisam ser desenhadas com texturas diferentes, Estados de renderização, materiais e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="3eb24-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="3eb24-124">Além disso, o aplicativo pode usar a tabela de atributos para ocultar partes de uma malha por não desenhar um determinado identificador de atributo (attrib) ao desenhar o quadro.</span><span class="sxs-lookup"><span data-stu-id="3eb24-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="3eb24-125">O tipo LPD3DXATTRIBUTERANGE é definido como um ponteiro para a estrutura **D3DXATTRIBUTERANGE** .</span><span class="sxs-lookup"><span data-stu-id="3eb24-125">The LPD3DXATTRIBUTERANGE type is defined as a pointer to the **D3DXATTRIBUTERANGE** structure.</span></span>


```
typedef D3DXATTRIBUTERANGE* LPD3DXATTRIBUTERANGE;
```



## <a name="requirements"></a><span data-ttu-id="3eb24-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3eb24-126">Requirements</span></span>



| <span data-ttu-id="3eb24-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3eb24-127">Requirement</span></span> | <span data-ttu-id="3eb24-128">Valor</span><span class="sxs-lookup"><span data-stu-id="3eb24-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3eb24-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3eb24-129">Header</span></span><br/> | <dl> <span data-ttu-id="3eb24-130"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3eb24-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3eb24-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="3eb24-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eb24-132">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="3eb24-132">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
