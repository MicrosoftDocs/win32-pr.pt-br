---
title: deriv_rty_fine (SM5-ASM)
description: Computa a taxa de alteração de componentes. | deriv_rty_fine (SM5-ASM)
ms.assetid: 7C5769A6-443C-4208-BD09-3DF3C5902624
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f0274fd04ae88ee412c95947691628754ba197
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989185"
---
# <a name="deriv_rty_fine-sm5---asm"></a><span data-ttu-id="22baf-104">derivar \_ rty \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="22baf-104">deriv\_rty\_fine (sm5 - asm)</span></span>

<span data-ttu-id="22baf-105">Computa a taxa de alteração de componentes.</span><span class="sxs-lookup"><span data-stu-id="22baf-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="22baf-106">deriva \_ rty \_ de \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="22baf-106">deriv\_rty\_fine\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="22baf-107">Item</span><span class="sxs-lookup"><span data-stu-id="22baf-107">Item</span></span>                                                            | <span data-ttu-id="22baf-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="22baf-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="22baf-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="22baf-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="22baf-110">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="22baf-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="22baf-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="22baf-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="22baf-112">\[nos \] componentes na operação.</span><span class="sxs-lookup"><span data-stu-id="22baf-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="22baf-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="22baf-113">Remarks</span></span>

<span data-ttu-id="22baf-114">Para obter mais informações, consulte [derivar \_ RTX \_ .](deriv-rtx-fine--sm5---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="22baf-114">For more information, see [deriv\_rtx\_fine.](deriv-rtx-fine--sm5---asm-.md)</span></span>

<span data-ttu-id="22baf-115">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="22baf-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="22baf-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="22baf-116">Vertex</span></span> | <span data-ttu-id="22baf-117">Envoltória</span><span class="sxs-lookup"><span data-stu-id="22baf-117">Hull</span></span> | <span data-ttu-id="22baf-118">Domínio</span><span class="sxs-lookup"><span data-stu-id="22baf-118">Domain</span></span> | <span data-ttu-id="22baf-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="22baf-119">Geometry</span></span> | <span data-ttu-id="22baf-120">16x16</span><span class="sxs-lookup"><span data-stu-id="22baf-120">Pixel</span></span> | <span data-ttu-id="22baf-121">Computação</span><span class="sxs-lookup"><span data-stu-id="22baf-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="22baf-122">X</span><span class="sxs-lookup"><span data-stu-id="22baf-122">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="22baf-123">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="22baf-123">Minimum Shader Model</span></span>

<span data-ttu-id="22baf-124">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="22baf-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="22baf-125">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="22baf-125">Shader Model</span></span>                                              | <span data-ttu-id="22baf-126">Com suporte</span><span class="sxs-lookup"><span data-stu-id="22baf-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="22baf-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="22baf-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="22baf-128">sim</span><span class="sxs-lookup"><span data-stu-id="22baf-128">yes</span></span>       |
| [<span data-ttu-id="22baf-129">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="22baf-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="22baf-130">não</span><span class="sxs-lookup"><span data-stu-id="22baf-130">no</span></span>        |
| [<span data-ttu-id="22baf-131">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="22baf-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="22baf-132">não</span><span class="sxs-lookup"><span data-stu-id="22baf-132">no</span></span>        |
| [<span data-ttu-id="22baf-133">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="22baf-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="22baf-134">não</span><span class="sxs-lookup"><span data-stu-id="22baf-134">no</span></span>        |
| [<span data-ttu-id="22baf-135">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="22baf-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="22baf-136">não</span><span class="sxs-lookup"><span data-stu-id="22baf-136">no</span></span>        |
| [<span data-ttu-id="22baf-137">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="22baf-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="22baf-138">não</span><span class="sxs-lookup"><span data-stu-id="22baf-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="22baf-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22baf-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22baf-140">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="22baf-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





