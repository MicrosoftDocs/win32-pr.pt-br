---
description: Armazena uma entrada de tabela de atributo.
ms.assetid: 81c77dc9-e078-46a1-a435-4b241e36ec13
title: Estrutura de D3DX10_ATTRIBUTE_RANGE (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_RANGE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: ddf7f10882e08232467130b3abbc6fb723a843ed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771351"
---
# <a name="d3dx10_attribute_range-structure"></a><span data-ttu-id="1d6d2-103">Estrutura do intervalo de \_ atributos D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="1d6d2-103">D3DX10\_ATTRIBUTE\_RANGE structure</span></span>

<span data-ttu-id="1d6d2-104">Armazena uma entrada de tabela de atributo.</span><span class="sxs-lookup"><span data-stu-id="1d6d2-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d6d2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d6d2-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_RANGE {
  UINT AttribId;
  UINT FaceStart;
  UINT FaceCount;
  UINT VertexStart;
  UINT VertexCount;
} D3DX10_ATTRIBUTE_RANGE, *LPD3DX10_ATTRIBUTE_RANGE;
```



## <a name="members"></a><span data-ttu-id="1d6d2-106">Membros</span><span class="sxs-lookup"><span data-stu-id="1d6d2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1d6d2-107">**Atribid**</span><span class="sxs-lookup"><span data-stu-id="1d6d2-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="1d6d2-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d6d2-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1d6d2-109">Identificador de tabela de atributo.</span><span class="sxs-lookup"><span data-stu-id="1d6d2-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1d6d2-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="1d6d2-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="1d6d2-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d6d2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1d6d2-112">Iniciando face.</span><span class="sxs-lookup"><span data-stu-id="1d6d2-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="1d6d2-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="1d6d2-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="1d6d2-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d6d2-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1d6d2-115">Contagem de face.</span><span class="sxs-lookup"><span data-stu-id="1d6d2-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="1d6d2-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="1d6d2-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="1d6d2-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d6d2-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1d6d2-118">Iniciando vértice.</span><span class="sxs-lookup"><span data-stu-id="1d6d2-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="1d6d2-119">**Contagemdevértice**</span><span class="sxs-lookup"><span data-stu-id="1d6d2-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="1d6d2-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d6d2-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1d6d2-121">Contagem de vértices.</span><span class="sxs-lookup"><span data-stu-id="1d6d2-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d6d2-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d6d2-122">Remarks</span></span>

<span data-ttu-id="1d6d2-123">Uma tabela de atributos é usada para identificar áreas da malha que precisam ser desenhadas com texturas diferentes, Estados de renderização, materiais e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="1d6d2-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="1d6d2-124">Além disso, o aplicativo pode usar a tabela de atributos para ocultar partes de uma malha por não desenhar um determinado identificador de atributo (attrib) ao desenhar o quadro.</span><span class="sxs-lookup"><span data-stu-id="1d6d2-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="1d6d2-125">O \_ tipo de intervalo de atributo LPD3DX \_ é definido como um ponteiro para a \_ estrutura do intervalo de atributos D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="1d6d2-125">The LPD3DX\_ATTRIBUTE\_RANGE type is defined as a pointer to the D3DX\_ATTRIBUTE\_RANGE structure.</span></span>


```
typedef D3DX_ATTRIBUTE_RANGE* LPD3DX_ATTRIBUTE_RANGE;
```



## <a name="requirements"></a><span data-ttu-id="1d6d2-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d6d2-126">Requirements</span></span>



| <span data-ttu-id="1d6d2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d6d2-127">Requirement</span></span> | <span data-ttu-id="1d6d2-128">Valor</span><span class="sxs-lookup"><span data-stu-id="1d6d2-128">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1d6d2-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d6d2-129">Header</span></span><br/> | <dl> <span data-ttu-id="1d6d2-130"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d6d2-130"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d6d2-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d6d2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d6d2-132">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="1d6d2-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
