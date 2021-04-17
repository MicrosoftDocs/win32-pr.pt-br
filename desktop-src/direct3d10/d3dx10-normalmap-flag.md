---
description: Esses sinalizadores são usados para controlar como o D3DX10ComputeNormalMap gera mapas normais. Qualquer número desses sinalizadores pode estar ou juntos em qualquer combinação.
ms.assetid: 307936c1-3137-41fe-8bea-7a82e6db0867
title: Enumeração de D3DX10_NORMALMAP_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_NORMALMAP_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: c4b6962561007fbc3e64b471c045e98b2f8328b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812130"
---
# <a name="d3dx10_normalmap_flag-enumeration"></a><span data-ttu-id="b223b-104">\_Enumeração de \_ sinalizador D3DX10 NormalMap</span><span class="sxs-lookup"><span data-stu-id="b223b-104">D3DX10\_NORMALMAP\_FLAG enumeration</span></span>

<span data-ttu-id="b223b-105">Esses sinalizadores são usados para controlar como o [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) gera mapas normais.</span><span class="sxs-lookup"><span data-stu-id="b223b-105">These flags are used to control how [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) generates normal maps.</span></span> <span data-ttu-id="b223b-106">Qualquer número desses sinalizadores pode estar ou juntos em qualquer combinação.</span><span class="sxs-lookup"><span data-stu-id="b223b-106">Any number of these flags may be OR'd together in any combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="b223b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b223b-107">Syntax</span></span>


```C++
typedef enum D3DX10_NORMALMAP_FLAG { 
  D3DX10_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX10_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX10_NORMALMAP_MIRROR             = (3 << 16),
  D3DX10_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX10_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX10_NORMALMAP_FLAG, *LPD3DX10_NORMALMAP_FLAG;
```



## <a name="constants"></a><span data-ttu-id="b223b-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="b223b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b223b-109"><span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3DX10 \_ NormalMap \_ Mirror \_ U**</span><span class="sxs-lookup"><span data-stu-id="b223b-109"><span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3DX10\_NORMALMAP\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="b223b-110">Indica que os pixels da borda da textura no eixo U devem ser espelhados, não encapsulados.</span><span class="sxs-lookup"><span data-stu-id="b223b-110">Indicates that pixels off the edge of the texture on the U-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="b223b-111"><span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10 \_ NormalMap \_ Mirror \_ V**</span><span class="sxs-lookup"><span data-stu-id="b223b-111"><span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10\_NORMALMAP\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="b223b-112">Indica que os pixels da borda da textura no eixo V devem ser espelhados, não encapsulados.</span><span class="sxs-lookup"><span data-stu-id="b223b-112">Indicates that pixels off the edge of the texture on the V-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="b223b-113"><span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**D3DX10 \_ NormalMap \_ Mirror**</span><span class="sxs-lookup"><span data-stu-id="b223b-113"><span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**D3DX10\_NORMALMAP\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="b223b-114">O mesmo que D3DX10 \_ NormalMap \_ espelho \_ U \| D3DX10 \_ NormalMap \_ Mirror \_ V.</span><span class="sxs-lookup"><span data-stu-id="b223b-114">Same as D3DX10\_NORMALMAP\_MIRROR\_U \| D3DX10\_NORMALMAP\_MIRROR\_V.</span></span>

</dd> <dt>

<span data-ttu-id="b223b-115"><span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10 \_ NormalMap \_ INVERTSIGN**</span><span class="sxs-lookup"><span data-stu-id="b223b-115"><span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10\_NORMALMAP\_INVERTSIGN**</span></span>
</dt> <dd>

<span data-ttu-id="b223b-116">Inverte a direção de cada normal.</span><span class="sxs-lookup"><span data-stu-id="b223b-116">Inverts the direction of each normal.</span></span>

</dd> <dt>

<span data-ttu-id="b223b-117"><span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**D3DX10 \_ NormalMap \_ \_ oclusão Compute**</span><span class="sxs-lookup"><span data-stu-id="b223b-117"><span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**D3DX10\_NORMALMAP\_COMPUTE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="b223b-118">Computa o termo por pixel oclusão e o codifica no Alpha.</span><span class="sxs-lookup"><span data-stu-id="b223b-118">Computes the per pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="b223b-119">Um alfa de 1 significa que o pixel não é obscurecido de nenhuma forma e um alfa de 0 significaria que o pixel fosse completamente obscurecido.</span><span class="sxs-lookup"><span data-stu-id="b223b-119">An Alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 would mean that the pixel is completely obscured.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b223b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b223b-120">Requirements</span></span>



| <span data-ttu-id="b223b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b223b-121">Requirement</span></span> | <span data-ttu-id="b223b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b223b-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b223b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b223b-123">Header</span></span><br/> | <dl> <span data-ttu-id="b223b-124"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b223b-124"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b223b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b223b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b223b-126">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="b223b-126">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




