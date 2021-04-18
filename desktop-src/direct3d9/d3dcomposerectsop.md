---
description: Especifica como combinar os dados de glifo das superfícies de origem e de destino em uma chamada para ComposeRects.
ms.assetid: 4b0e6e48-48e0-4955-bb20-f953fdce785c
title: Enumeração D3DCOMPOSERECTSOP (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTSOP
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cd47cb14ab129bf27a4b59ba07e0be12d144fb8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105787635"
---
# <a name="d3dcomposerectsop-enumeration"></a><span data-ttu-id="7a238-103">Enumeração D3DCOMPOSERECTSOP</span><span class="sxs-lookup"><span data-stu-id="7a238-103">D3DCOMPOSERECTSOP enumeration</span></span>

<span data-ttu-id="7a238-104">Especifica como combinar os dados de glifo das superfícies de origem e de destino em uma chamada para [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects).</span><span class="sxs-lookup"><span data-stu-id="7a238-104">Specifies how to combine the glyph data from the source and destination surfaces in a call to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a238-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a238-105">Syntax</span></span>


```C++
typedef enum _D3DCOMPOSERECTSOP { 
  D3DCOMPOSERECTS_COPY         = 1,
  D3DCOMPOSERECTS_OR           = 2,
  D3DCOMPOSERECTS_AND          = 3,
  D3DCOMPOSERECTS_NEG          = 4,
  D3DCOMPOSERECTS_FORCE_DWORD  = 0x7fffffff
} D3DCOMPOSERECTSOP;
```



## <a name="constants"></a><span data-ttu-id="7a238-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="7a238-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7a238-107"><span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**\_Cópia D3DCOMPOSERECTS**</span><span class="sxs-lookup"><span data-stu-id="7a238-107"><span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**D3DCOMPOSERECTS\_COPY**</span></span>
</dt> <dd>

<span data-ttu-id="7a238-108">Copie a origem para o destino.</span><span class="sxs-lookup"><span data-stu-id="7a238-108">Copy the source to the destination.</span></span>

</dd> <dt>

<span data-ttu-id="7a238-109"><span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS \_ ou**</span><span class="sxs-lookup"><span data-stu-id="7a238-109"><span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS\_OR**</span></span>
</dt> <dd>

<span data-ttu-id="7a238-110">OU a origem e o destino.</span><span class="sxs-lookup"><span data-stu-id="7a238-110">Bitwise OR the source and the destination.</span></span>

</dd> <dt>

<span data-ttu-id="7a238-111"><span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS \_ e**</span><span class="sxs-lookup"><span data-stu-id="7a238-111"><span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS\_AND**</span></span>
</dt> <dd>

<span data-ttu-id="7a238-112">E-bit e a origem e o destino.</span><span class="sxs-lookup"><span data-stu-id="7a238-112">Bitwise AND the source and the destination.</span></span>

</dd> <dt>

<span data-ttu-id="7a238-113"><span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS \_ neg**</span><span class="sxs-lookup"><span data-stu-id="7a238-113"><span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS\_NEG**</span></span>
</dt> <dd>

<span data-ttu-id="7a238-114">Copie a origem negada para o destino (DST & ~ src).</span><span class="sxs-lookup"><span data-stu-id="7a238-114">Copy the negated source to the destination (Dst & ~Src).</span></span>

</dd> <dt>

<span data-ttu-id="7a238-115"><span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="7a238-115"><span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="7a238-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="7a238-116">Reserved.</span></span> <span data-ttu-id="7a238-117">Usado para forçar a enumeração a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="7a238-117">Used to force enumeration to 32-bits in size.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a238-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a238-118">Requirements</span></span>



| <span data-ttu-id="7a238-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a238-119">Requirement</span></span> | <span data-ttu-id="7a238-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7a238-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a238-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a238-121">Header</span></span><br/> | <dl> <span data-ttu-id="7a238-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a238-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a238-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a238-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a238-124">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="7a238-124">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




