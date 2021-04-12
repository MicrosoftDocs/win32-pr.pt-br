---
description: Especifica os tipos de modos de exibição a serem filtrados.
ms.assetid: 4a03d0f0-dec5-4209-8c99-b58cc13064f5
title: Estrutura D3DDISPLAYMODEFILTER (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEFILTER
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b60c283405bead7b2618b91d6de76158841ff27f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298542"
---
# <a name="d3ddisplaymodefilter-structure"></a><span data-ttu-id="a801c-103">Estrutura D3DDISPLAYMODEFILTER</span><span class="sxs-lookup"><span data-stu-id="a801c-103">D3DDISPLAYMODEFILTER structure</span></span>

<span data-ttu-id="a801c-104">Especifica os tipos de modos de exibição a serem filtrados.</span><span class="sxs-lookup"><span data-stu-id="a801c-104">Specifies types of display modes to filter out.</span></span>

## <a name="syntax"></a><span data-ttu-id="a801c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a801c-105">Syntax</span></span>


```C++
typedef struct {
  UINT                Size;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEFILTER;
```



## <a name="members"></a><span data-ttu-id="a801c-106">Membros</span><span class="sxs-lookup"><span data-stu-id="a801c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a801c-107">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="a801c-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="a801c-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a801c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a801c-109">O tamanho desta estrutura.</span><span class="sxs-lookup"><span data-stu-id="a801c-109">The size of this structure.</span></span> <span data-ttu-id="a801c-110">Isso deve sempre ser definido como sizeof (D3DDISPLAYMODEFILTER).</span><span class="sxs-lookup"><span data-stu-id="a801c-110">This should always be set to sizeof(D3DDISPLAYMODEFILTER).</span></span>

</dd> <dt>

<span data-ttu-id="a801c-111">**Formato**</span><span class="sxs-lookup"><span data-stu-id="a801c-111">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="a801c-112">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="a801c-112">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a801c-113">O formato do modo de exibição a ser filtrado. Consulte [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="a801c-113">The display mode format to filter out. See [D3DFORMAT](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="a801c-114">**ScanLineOrdering**</span><span class="sxs-lookup"><span data-stu-id="a801c-114">**ScanLineOrdering**</span></span>
</dt> <dd>

<span data-ttu-id="a801c-115">Tipo: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span><span class="sxs-lookup"><span data-stu-id="a801c-115">Type: **[**D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a801c-116">Se a ordenação de varredura é entrelaçada ou progressiva.</span><span class="sxs-lookup"><span data-stu-id="a801c-116">Whether the scanline ordering is interlaced or progressive.</span></span> <span data-ttu-id="a801c-117">Consulte [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span><span class="sxs-lookup"><span data-stu-id="a801c-117">See [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a801c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a801c-118">Requirements</span></span>



| <span data-ttu-id="a801c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a801c-119">Requirement</span></span> | <span data-ttu-id="a801c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a801c-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a801c-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a801c-121">Header</span></span><br/> | <dl> <span data-ttu-id="a801c-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a801c-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a801c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="a801c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a801c-124">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="a801c-124">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
