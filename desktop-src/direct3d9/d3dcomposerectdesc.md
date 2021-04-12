---
description: Especifica o retângulo usado para incluir glifos em uma superfície monocromática.
ms.assetid: ce5d492f-38d1-4e7b-a9c2-68c791c84d0c
title: Estrutura D3DCOMPOSERECTDESC (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cf9ad5f1c075f4dc52d68b894b37c7d0f0a7b310
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370930"
---
# <a name="d3dcomposerectdesc-structure"></a><span data-ttu-id="c893c-103">Estrutura D3DCOMPOSERECTDESC</span><span class="sxs-lookup"><span data-stu-id="c893c-103">D3DCOMPOSERECTDESC structure</span></span>

<span data-ttu-id="c893c-104">Especifica o retângulo usado para incluir glifos em uma superfície monocromática.</span><span class="sxs-lookup"><span data-stu-id="c893c-104">Specifies the rectangle used to enclose glyphs on a monochrome surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c893c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c893c-105">Syntax</span></span>


```C++
typedef struct _D3DCOMPOSERECTDESC {
  USHORT X;
  USHORT Y;
  USHORT Width;
  USHORT Height;
} D3DCOMPOSERECTDESC;
```



## <a name="members"></a><span data-ttu-id="c893c-106">Membros</span><span class="sxs-lookup"><span data-stu-id="c893c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c893c-107">**X**</span><span class="sxs-lookup"><span data-stu-id="c893c-107">**X**</span></span>
</dt> <dd>

<span data-ttu-id="c893c-108">Tipo: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c893c-108">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c893c-109">Coordenada esquerda para iniciar a cópia em.</span><span class="sxs-lookup"><span data-stu-id="c893c-109">Left coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="c893c-110">**S**</span><span class="sxs-lookup"><span data-stu-id="c893c-110">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="c893c-111">Tipo: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c893c-111">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c893c-112">Coordenada superior para iniciar a cópia em.</span><span class="sxs-lookup"><span data-stu-id="c893c-112">Top coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="c893c-113">**Largura**</span><span class="sxs-lookup"><span data-stu-id="c893c-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="c893c-114">Tipo: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c893c-114">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c893c-115">Número de texels da coordenada esquerda.</span><span class="sxs-lookup"><span data-stu-id="c893c-115">Number of texels from left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="c893c-116">**Altura**</span><span class="sxs-lookup"><span data-stu-id="c893c-116">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="c893c-117">Tipo: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c893c-117">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c893c-118">Número de texels da coordenada superior.</span><span class="sxs-lookup"><span data-stu-id="c893c-118">Number of texels from the top coordinate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c893c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="c893c-119">Remarks</span></span>

<span data-ttu-id="c893c-120">Essa estrutura é usada em chamadas para [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) para incluir glifos na superfície de origem.</span><span class="sxs-lookup"><span data-stu-id="c893c-120">This structure is used in calls to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) to enclose glyphs on the source surface.</span></span> <span data-ttu-id="c893c-121">Um buffer de vértice (consulte [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) preenchido com essas estruturas é criado para conter os locais de glifo.</span><span class="sxs-lookup"><span data-stu-id="c893c-121">A vertex buffer (see [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) filled with these structures are created to contain the glyph locations.</span></span> <span data-ttu-id="c893c-122">Os membros USHORT são usados para reduzir o volume de memória o máximo possível.</span><span class="sxs-lookup"><span data-stu-id="c893c-122">USHORT members are used to reduce the memory footprint as much as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="c893c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c893c-123">Requirements</span></span>



| <span data-ttu-id="c893c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c893c-124">Requirement</span></span> | <span data-ttu-id="c893c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="c893c-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c893c-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c893c-126">Header</span></span><br/> | <dl> <span data-ttu-id="c893c-127"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c893c-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c893c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c893c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c893c-129">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="c893c-129">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
