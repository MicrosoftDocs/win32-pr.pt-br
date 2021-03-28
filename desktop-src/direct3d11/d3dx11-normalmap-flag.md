---
title: Enumeração de D3DX11_NORMALMAP_FLAG (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Opções de mapa normais. Você pode combinar qualquer número desses sinalizadores usando uma operação OR bit a bit.
ms.assetid: cc9c8a54-be1e-4594-8274-9955562a6fa8
keywords:
- Enumeração D3DX11_NORMALMAP_FLAG Direct3D 11
- Ponteiro de enumeração LPD3DX11_NORMALMAP_FLAG Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_NORMALMAP_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f5d9669370e6df03d783ae1cb82a5eeb5a9142
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173188"
---
# <a name="d3dx11_normalmap_flag-enumeration"></a><span data-ttu-id="11dd0-107">\_Enumeração de \_ sinalizador D3DX11 NormalMap</span><span class="sxs-lookup"><span data-stu-id="11dd0-107">D3DX11\_NORMALMAP\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="11dd0-108">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="11dd0-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="11dd0-109">Opções de mapa normais.</span><span class="sxs-lookup"><span data-stu-id="11dd0-109">Normal map options.</span></span> <span data-ttu-id="11dd0-110">Você pode combinar qualquer número desses sinalizadores usando uma operação OR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="11dd0-110">You can combine any number of these flags by using a bitwise OR operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="11dd0-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="11dd0-111">Syntax</span></span>


```C++
typedef enum D3DX11_NORMALMAP_FLAG { 
  D3DX11_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX11_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX11_NORMALMAP_MIRROR             = (3 << 16),
  D3DX11_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX11_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX11_NORMALMAP_FLAG, *LPD3DX11_NORMALMAP_FLAG;
```



## <a name="constants"></a><span data-ttu-id="11dd0-112">Constantes</span><span class="sxs-lookup"><span data-stu-id="11dd0-112">Constants</span></span>

<dl> <dt>

<span data-ttu-id="11dd0-113"><span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**D3DX11 \_ NormalMap \_ Mirror \_ U**</span><span class="sxs-lookup"><span data-stu-id="11dd0-113"><span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**D3DX11\_NORMALMAP\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="11dd0-114">Indica que os pixels da borda da textura no eixo U devem ser espelhados, não encapsulados.</span><span class="sxs-lookup"><span data-stu-id="11dd0-114">Indicates that pixels off the edge of the texture on the U-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="11dd0-115"><span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11 \_ NormalMap \_ Mirror \_ V**</span><span class="sxs-lookup"><span data-stu-id="11dd0-115"><span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11\_NORMALMAP\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="11dd0-116">Indica que os pixels da borda da textura no eixo V devem ser espelhados, não encapsulados.</span><span class="sxs-lookup"><span data-stu-id="11dd0-116">Indicates that pixels off the edge of the texture on the V-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="11dd0-117"><span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**D3DX11 \_ NormalMap \_ Mirror**</span><span class="sxs-lookup"><span data-stu-id="11dd0-117"><span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**D3DX11\_NORMALMAP\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="11dd0-118">O mesmo que D3DX11 \_ NormalMap \_ espelho \_ U \| D3DX11 \_ NormalMap \_ Mirror \_ V.</span><span class="sxs-lookup"><span data-stu-id="11dd0-118">Same as D3DX11\_NORMALMAP\_MIRROR\_U \| D3DX11\_NORMALMAP\_MIRROR\_V.</span></span>

</dd> <dt>

<span data-ttu-id="11dd0-119"><span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11 \_ NormalMap \_ INVERTSIGN**</span><span class="sxs-lookup"><span data-stu-id="11dd0-119"><span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11\_NORMALMAP\_INVERTSIGN**</span></span>
</dt> <dd>

<span data-ttu-id="11dd0-120">Inverte a direção de cada normal.</span><span class="sxs-lookup"><span data-stu-id="11dd0-120">Inverts the direction of each normal.</span></span>

</dd> <dt>

<span data-ttu-id="11dd0-121"><span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**D3DX11 \_ NormalMap \_ \_ oclusão Compute**</span><span class="sxs-lookup"><span data-stu-id="11dd0-121"><span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**D3DX11\_NORMALMAP\_COMPUTE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="11dd0-122">Computa o termo por pixel oclusão e o codifica no Alpha.</span><span class="sxs-lookup"><span data-stu-id="11dd0-122">Computes the per pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="11dd0-123">Um alfa de 1 significa que o pixel não é obscurecido de nenhuma forma e um alfa de 0 significaria que o pixel fosse completamente obscurecido.</span><span class="sxs-lookup"><span data-stu-id="11dd0-123">An Alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 would mean that the pixel is completely obscured.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11dd0-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="11dd0-124">Remarks</span></span>

<span data-ttu-id="11dd0-125">Esses sinalizadores são usados pelo [**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md).</span><span class="sxs-lookup"><span data-stu-id="11dd0-125">These flags are used by [**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11dd0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11dd0-126">Requirements</span></span>



| <span data-ttu-id="11dd0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="11dd0-127">Requirement</span></span> | <span data-ttu-id="11dd0-128">Valor</span><span class="sxs-lookup"><span data-stu-id="11dd0-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11dd0-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11dd0-129">Header</span></span><br/> | <dl> <span data-ttu-id="11dd0-130"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="11dd0-130"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11dd0-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="11dd0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11dd0-132">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="11dd0-132">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





