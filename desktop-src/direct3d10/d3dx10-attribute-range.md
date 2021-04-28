---
description: Estrutura de D3DX10_ATTRIBUTE_RANGE – armazena uma entrada de tabela de atributo.
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
ms.openlocfilehash: 3e2954483da53c77ebef57f9cf2de104734caba2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094364"
---
# <a name="d3dx10_attribute_range-structure"></a><span data-ttu-id="b0922-103">Estrutura do intervalo de \_ atributos D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="b0922-103">D3DX10\_ATTRIBUTE\_RANGE structure</span></span>

<span data-ttu-id="b0922-104">Armazena uma entrada de tabela de atributo.</span><span class="sxs-lookup"><span data-stu-id="b0922-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0922-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0922-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_RANGE {
  UINT AttribId;
  UINT FaceStart;
  UINT FaceCount;
  UINT VertexStart;
  UINT VertexCount;
} D3DX10_ATTRIBUTE_RANGE, *LPD3DX10_ATTRIBUTE_RANGE;
```



## <a name="members"></a><span data-ttu-id="b0922-106">Membros</span><span class="sxs-lookup"><span data-stu-id="b0922-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b0922-107">**Atribid**</span><span class="sxs-lookup"><span data-stu-id="b0922-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="b0922-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0922-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b0922-109">Identificador de tabela de atributo.</span><span class="sxs-lookup"><span data-stu-id="b0922-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b0922-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="b0922-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="b0922-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0922-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b0922-112">Iniciando face.</span><span class="sxs-lookup"><span data-stu-id="b0922-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="b0922-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="b0922-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="b0922-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0922-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b0922-115">Contagem de face.</span><span class="sxs-lookup"><span data-stu-id="b0922-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="b0922-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="b0922-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="b0922-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0922-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b0922-118">Iniciando vértice.</span><span class="sxs-lookup"><span data-stu-id="b0922-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="b0922-119">**Contagemdevértice**</span><span class="sxs-lookup"><span data-stu-id="b0922-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="b0922-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0922-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b0922-121">Contagem de vértices.</span><span class="sxs-lookup"><span data-stu-id="b0922-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0922-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0922-122">Remarks</span></span>

<span data-ttu-id="b0922-123">Uma tabela de atributos é usada para identificar áreas da malha que precisam ser desenhadas com texturas diferentes, Estados de renderização, materiais e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b0922-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="b0922-124">Além disso, o aplicativo pode usar a tabela de atributos para ocultar partes de uma malha por não desenhar um determinado identificador de atributo (attrib) ao desenhar o quadro.</span><span class="sxs-lookup"><span data-stu-id="b0922-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="b0922-125">O \_ tipo de intervalo de atributo LPD3DX \_ é definido como um ponteiro para a \_ estrutura do intervalo de atributos D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="b0922-125">The LPD3DX\_ATTRIBUTE\_RANGE type is defined as a pointer to the D3DX\_ATTRIBUTE\_RANGE structure.</span></span>


```
typedef D3DX_ATTRIBUTE_RANGE* LPD3DX_ATTRIBUTE_RANGE;
```



## <a name="requirements"></a><span data-ttu-id="b0922-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0922-126">Requirements</span></span>



| <span data-ttu-id="b0922-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0922-127">Requirement</span></span> | <span data-ttu-id="b0922-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b0922-128">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b0922-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0922-129">Header</span></span><br/> | <dl> <span data-ttu-id="b0922-130"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0922-130"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0922-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b0922-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0922-132">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="b0922-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
