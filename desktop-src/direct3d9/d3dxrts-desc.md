---
description: Descreve uma superfície de renderização.
ms.assetid: cffa1555-1fa2-427d-8bcb-da0e61d82152
title: Estrutura de D3DXRTS_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 3a0b52f258956f7b62734ca97cc5d1bf5ed00ac3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930585"
---
# <a name="d3dxrts_desc-structure"></a><span data-ttu-id="0612e-103">\_Estrutura desc de D3DXRTS</span><span class="sxs-lookup"><span data-stu-id="0612e-103">D3DXRTS\_DESC structure</span></span>

<span data-ttu-id="0612e-104">Descreve uma superfície de renderização.</span><span class="sxs-lookup"><span data-stu-id="0612e-104">Describes a render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0612e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0612e-105">Syntax</span></span>


```C++
typedef struct D3DXRTS_DESC {
  UINT      Width;
  UINT      Height;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTS_DESC, *LPD3DXRTS_DESC;
```



## <a name="members"></a><span data-ttu-id="0612e-106">Membros</span><span class="sxs-lookup"><span data-stu-id="0612e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0612e-107">**Largura**</span><span class="sxs-lookup"><span data-stu-id="0612e-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="0612e-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0612e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0612e-109">Largura da superfície de renderização, em pixels.</span><span class="sxs-lookup"><span data-stu-id="0612e-109">Width of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0612e-110">**Altura**</span><span class="sxs-lookup"><span data-stu-id="0612e-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="0612e-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0612e-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0612e-112">Altura da superfície de renderização, em pixels.</span><span class="sxs-lookup"><span data-stu-id="0612e-112">Height of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0612e-113">**Formato**</span><span class="sxs-lookup"><span data-stu-id="0612e-113">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="0612e-114">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="0612e-114">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0612e-115">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato de pixel da superfície de renderização.</span><span class="sxs-lookup"><span data-stu-id="0612e-115">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the pixel format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="0612e-116">**DepthStencil**</span><span class="sxs-lookup"><span data-stu-id="0612e-116">**DepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="0612e-117">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0612e-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0612e-118">Se **for true**, a superfície de renderização dará suporte a uma superfície de estêncil de profundidade; caso contrário, esse membro será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="0612e-118">If **TRUE**, the render surface supports a depth-stencil surface; otherwise this member is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0612e-119">**DepthStencilFormat**</span><span class="sxs-lookup"><span data-stu-id="0612e-119">**DepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="0612e-120">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="0612e-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0612e-121">Se DepthStencil for definido como **true**, esse parâmetro será um membro do tipo enumerado [D3DFORMAT](d3dformat.md) , descrevendo o formato de estêncil de profundidade da superfície de renderização.</span><span class="sxs-lookup"><span data-stu-id="0612e-121">If DepthStencil is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the depth-stencil format of the render surface.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0612e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0612e-122">Requirements</span></span>



| <span data-ttu-id="0612e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0612e-123">Requirement</span></span> | <span data-ttu-id="0612e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0612e-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0612e-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0612e-125">Header</span></span><br/> | <dl> <span data-ttu-id="0612e-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0612e-126"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0612e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0612e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0612e-128">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="0612e-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="0612e-129">**ID3DXRenderToSurface:: GetDesc**</span><span class="sxs-lookup"><span data-stu-id="0612e-129">**ID3DXRenderToSurface::GetDesc**</span></span>](id3dxrendertosurface--getdesc.md)
</dt> </dl>

 

 
