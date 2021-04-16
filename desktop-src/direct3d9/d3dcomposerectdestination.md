---
description: Especifica o glifo de origem e o local em uma superfície monocromática para copiar glifos.
ms.assetid: eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1
title: Estrutura D3DCOMPOSERECTDESTINATION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESTINATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 56843bc78943a4c76fe4fe0f5e18242728a979c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105768371"
---
# <a name="d3dcomposerectdestination-structure"></a><span data-ttu-id="fa570-103">Estrutura D3DCOMPOSERECTDESTINATION</span><span class="sxs-lookup"><span data-stu-id="fa570-103">D3DCOMPOSERECTDESTINATION structure</span></span>

<span data-ttu-id="fa570-104">Especifica o glifo de origem e o local em uma superfície monocromática para copiar glifos.</span><span class="sxs-lookup"><span data-stu-id="fa570-104">Specifies the source glyph and location in a monochrome surface to copy glyphs into.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa570-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa570-105">Syntax</span></span>


```C++
typedef struct _D3DCOMPOSERECTDESTINATION {
  USHORT SrcRectIndex;
  USHORT Reserved;
  USHORT X;
  USHORT Y;
} D3DCOMPOSERECTDESTINATION;
```



## <a name="members"></a><span data-ttu-id="fa570-106">Membros</span><span class="sxs-lookup"><span data-stu-id="fa570-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fa570-107">**SrcRectIndex**</span><span class="sxs-lookup"><span data-stu-id="fa570-107">**SrcRectIndex**</span></span>
</dt> <dd>

<span data-ttu-id="fa570-108">Tipo: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa570-108">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fa570-109">Um glifo específico de índice do buffer de vértices que contém estruturas [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) .</span><span class="sxs-lookup"><span data-stu-id="fa570-109">Index particular glyph from vertex buffer containing [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="fa570-110">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="fa570-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="fa570-111">Tipo: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa570-111">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fa570-112">Reservado para fins de alinhamento.</span><span class="sxs-lookup"><span data-stu-id="fa570-112">Reserved for alignment purposes.</span></span>

</dd> <dt>

<span data-ttu-id="fa570-113">**X**</span><span class="sxs-lookup"><span data-stu-id="fa570-113">**X**</span></span>
</dt> <dd>

<span data-ttu-id="fa570-114">Tipo: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa570-114">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fa570-115">Coordenada esquerda para iniciar a cópia em.</span><span class="sxs-lookup"><span data-stu-id="fa570-115">Left coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="fa570-116">**S**</span><span class="sxs-lookup"><span data-stu-id="fa570-116">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="fa570-117">Tipo: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa570-117">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fa570-118">Coordenada superior para iniciar a cópia em.</span><span class="sxs-lookup"><span data-stu-id="fa570-118">Top coordinate to begin copy at.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa570-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa570-119">Remarks</span></span>

<span data-ttu-id="fa570-120">Essa estrutura é usada em chamadas para [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) para indicar que os glifos de local devem ser copiados para e qual glifo específico deve ser copiado.</span><span class="sxs-lookup"><span data-stu-id="fa570-120">This structure is used in calls to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) to indicate the location glyphs should be copied to and which particular glyph should be copied.</span></span> <span data-ttu-id="fa570-121">Um buffer de vértice (consulte [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) preenchido com essas estruturas é criado para conter os locais de glifo.</span><span class="sxs-lookup"><span data-stu-id="fa570-121">A vertex buffer (see [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) filled with these structures are created to contain the glyph locations.</span></span> <span data-ttu-id="fa570-122">Os membros USHORT são usados para reduzir o volume de memória o máximo possível.</span><span class="sxs-lookup"><span data-stu-id="fa570-122">USHORT members are used to reduce the memory footprint as much as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa570-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa570-123">Requirements</span></span>



| <span data-ttu-id="fa570-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa570-124">Requirement</span></span> | <span data-ttu-id="fa570-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fa570-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa570-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa570-126">Header</span></span><br/> | <dl> <span data-ttu-id="fa570-127"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa570-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa570-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa570-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa570-129">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="fa570-129">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
