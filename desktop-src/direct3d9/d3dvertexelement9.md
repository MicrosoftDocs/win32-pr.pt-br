---
description: Define o layout de dados de vértice. Cada vértice pode conter um ou mais tipos de dados, e cada tipo de dados é descrito por um elemento Vertex.
ms.assetid: 6f3c40a0-b28e-48d6-acad-ef80a919c5d7
title: Estrutura D3DVERTEXELEMENT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXELEMENT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e6c5e9508185124673ca7464b31d741cdf8035c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105769152"
---
# <a name="d3dvertexelement9-structure"></a><span data-ttu-id="d00c6-104">Estrutura D3DVERTEXELEMENT9</span><span class="sxs-lookup"><span data-stu-id="d00c6-104">D3DVERTEXELEMENT9 structure</span></span>

<span data-ttu-id="d00c6-105">Define o layout de dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="d00c6-105">Defines the vertex data layout.</span></span> <span data-ttu-id="d00c6-106">Cada vértice pode conter um ou mais tipos de dados, e cada tipo de dados é descrito por um elemento Vertex.</span><span class="sxs-lookup"><span data-stu-id="d00c6-106">Each vertex can contain one or more data types, and each data type is described by a vertex element.</span></span>

## <a name="syntax"></a><span data-ttu-id="d00c6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d00c6-107">Syntax</span></span>


```C++
typedef struct D3DVERTEXELEMENT9 {
  WORD Stream;
  WORD Offset;
  BYTE Type;
  BYTE Method;
  BYTE Usage;
  BYTE UsageIndex;
} D3DVERTEXELEMENT9, *LPD3DVERTEXELEMENT9;
```



## <a name="members"></a><span data-ttu-id="d00c6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d00c6-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d00c6-109">**Stream**</span><span class="sxs-lookup"><span data-stu-id="d00c6-109">**Stream**</span></span>
</dt> <dd>

<span data-ttu-id="d00c6-110">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d00c6-110">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d00c6-111">Número do fluxo.</span><span class="sxs-lookup"><span data-stu-id="d00c6-111">Stream number.</span></span>

</dd> <dt>

<span data-ttu-id="d00c6-112">**Deslocamento**</span><span class="sxs-lookup"><span data-stu-id="d00c6-112">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="d00c6-113">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d00c6-113">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d00c6-114">Deslocamento do início dos dados de vértice para os dados associados ao tipo de dados específico.</span><span class="sxs-lookup"><span data-stu-id="d00c6-114">Offset from the beginning of the vertex data to the data associated with the particular data type.</span></span>

</dd> <dt>

<span data-ttu-id="d00c6-115">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d00c6-115">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="d00c6-116">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d00c6-116">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d00c6-117">O tipo de dados, especificado como um [**D3DDECLTYPE**](./d3ddecltype.md).</span><span class="sxs-lookup"><span data-stu-id="d00c6-117">The data type, specified as a [**D3DDECLTYPE**](./d3ddecltype.md).</span></span> <span data-ttu-id="d00c6-118">Um dos vários tipos predefinidos que definem o tamanho dos dados.</span><span class="sxs-lookup"><span data-stu-id="d00c6-118">One of several predefined types that define the data size.</span></span> <span data-ttu-id="d00c6-119">Alguns métodos têm um tipo implícito.</span><span class="sxs-lookup"><span data-stu-id="d00c6-119">Some methods have an implied type.</span></span>

</dd> <dt>

<span data-ttu-id="d00c6-120">**Método**</span><span class="sxs-lookup"><span data-stu-id="d00c6-120">**Method**</span></span>
</dt> <dd>

<span data-ttu-id="d00c6-121">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d00c6-121">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d00c6-122">O método especifica o processamento de Tessellator, que determina como o Tessellator interpreta (ou Opera) os dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="d00c6-122">The method specifies the tessellator processing, which determines how the tessellator interprets (or operates on) the vertex data.</span></span> <span data-ttu-id="d00c6-123">Para obter mais informações, consulte [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span><span class="sxs-lookup"><span data-stu-id="d00c6-123">For more information, see [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span></span>

</dd> <dt>

<span data-ttu-id="d00c6-124">**Usage**</span><span class="sxs-lookup"><span data-stu-id="d00c6-124">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="d00c6-125">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d00c6-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d00c6-126">Define para que os dados serão usados; ou seja, a interoperabilidade entre layouts de dados de vértice e sombreadores de vértice.</span><span class="sxs-lookup"><span data-stu-id="d00c6-126">Defines what the data will be used for; that is, the interoperability between vertex data layouts and vertex shaders.</span></span> <span data-ttu-id="d00c6-127">Cada uso atua para associar uma declaração de vértice a um sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="d00c6-127">Each usage acts to bind a vertex declaration to a vertex shader.</span></span> <span data-ttu-id="d00c6-128">Em alguns casos, eles têm uma interpretação especial.</span><span class="sxs-lookup"><span data-stu-id="d00c6-128">In some cases, they have a special interpretation.</span></span> <span data-ttu-id="d00c6-129">Por exemplo, um elemento que especifica \_ a posição D3DDECLUSAGE normal ou D3DDECLUSAGE \_ é usado pelo Tessellator do N-patch para configurar o mosaico.</span><span class="sxs-lookup"><span data-stu-id="d00c6-129">For example, an element that specifies D3DDECLUSAGE\_NORMAL or D3DDECLUSAGE\_POSITION is used by the N-patch tessellator to set up tessellation.</span></span> <span data-ttu-id="d00c6-130">Consulte [**D3DDECLUSAGE**](./d3ddeclusage.md) para obter uma lista da semântica disponível.</span><span class="sxs-lookup"><span data-stu-id="d00c6-130">See [**D3DDECLUSAGE**](./d3ddeclusage.md) for a list of the available semantics.</span></span> <span data-ttu-id="d00c6-131">D3DDECLUSAGE \_ TEXCOORD pode ser usado para campos definidos pelo usuário (que não têm um uso existente definido).</span><span class="sxs-lookup"><span data-stu-id="d00c6-131">D3DDECLUSAGE\_TEXCOORD can be used for user-defined fields (which don't have an existing usage defined).</span></span>

</dd> <dt>

<span data-ttu-id="d00c6-132">**UsageIndex**</span><span class="sxs-lookup"><span data-stu-id="d00c6-132">**UsageIndex**</span></span>
</dt> <dd>

<span data-ttu-id="d00c6-133">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d00c6-133">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d00c6-134">Modifica os dados de uso para permitir que o usuário especifique vários tipos de uso.</span><span class="sxs-lookup"><span data-stu-id="d00c6-134">Modifies the usage data to allow the user to specify multiple usage types.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d00c6-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="d00c6-135">Remarks</span></span>

<span data-ttu-id="d00c6-136">Os dados de vértice são definidos usando uma matriz de estruturas **D3DVERTEXELEMENT9** .</span><span class="sxs-lookup"><span data-stu-id="d00c6-136">Vertex data is defined using an array of **D3DVERTEXELEMENT9** structures.</span></span> <span data-ttu-id="d00c6-137">Use [**D3DDECL \_ end**](d3ddecl-end.md) para declarar o último elemento na declaração.</span><span class="sxs-lookup"><span data-stu-id="d00c6-137">Use [**D3DDECL\_END**](d3ddecl-end.md) to declare the last element in the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d00c6-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d00c6-138">Requirements</span></span>



| <span data-ttu-id="d00c6-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="d00c6-139">Requirement</span></span> | <span data-ttu-id="d00c6-140">Valor</span><span class="sxs-lookup"><span data-stu-id="d00c6-140">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d00c6-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d00c6-141">Header</span></span><br/> | <dl> <span data-ttu-id="d00c6-142"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d00c6-142"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d00c6-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="d00c6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d00c6-144">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="d00c6-144">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="d00c6-145">Declaração de vértice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d00c6-145">Vertex Declaration (Direct3D 9)</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
