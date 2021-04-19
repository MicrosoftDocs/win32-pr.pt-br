---
title: deriv_rtx_coarse (SM5-ASM)
description: Computa a taxa de alteração de componentes. | deriv_rtx_coarse (SM5-ASM)
ms.assetid: 57743BB2-251C-4EA7-BDA9-70B2ECEE3B3F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2355b6db6aef9e85959d6359053fea76b48af0a5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989162"
---
# <a name="deriv_rtx_coarse-sm5---asm"></a><span data-ttu-id="96daf-104">derivar \_ RTX \_ grande (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="96daf-104">deriv\_rtx\_coarse (sm5 - asm)</span></span>

<span data-ttu-id="96daf-105">Computa a taxa de alteração de componentes.</span><span class="sxs-lookup"><span data-stu-id="96daf-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="96daf-106">deriva \_ RTX \_ de \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="96daf-106">deriv\_rtx\_coarse\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------|



 



| <span data-ttu-id="96daf-107">Item</span><span class="sxs-lookup"><span data-stu-id="96daf-107">Item</span></span>                                                            | <span data-ttu-id="96daf-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="96daf-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="96daf-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="96daf-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="96daf-110">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="96daf-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="96daf-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="96daf-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="96daf-112">\[nos \] componentes na operação.</span><span class="sxs-lookup"><span data-stu-id="96daf-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="96daf-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="96daf-113">Remarks</span></span>

<span data-ttu-id="96daf-114">Essa instrução computa a taxa de alteração de conteúdo de cada componente float32 de *src0* (post-swizzle), com relação à direção de renderTarget x (RTX) ou à direção de renderTarget y (Confira [derivação de \_ rty \_ grande](deriv-rty-coarse--sm5---asm-.md)).</span><span class="sxs-lookup"><span data-stu-id="96daf-114">This instruction computes the rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction (see [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md)).</span></span> <span data-ttu-id="96daf-115">Apenas um único par derivado x, y é calculado para cada carimbo 2x2 de pixels.</span><span class="sxs-lookup"><span data-stu-id="96daf-115">Only a single x,y derivative pair is computed for each 2x2 stamp of pixels.</span></span>

<span data-ttu-id="96daf-116">Os dados na invocação do sombreador de pixel atual podem ou não participar do cálculo da derivação solicitada, porque o derivativo será calculado apenas uma vez por 2x2 Quad.</span><span class="sxs-lookup"><span data-stu-id="96daf-116">The data in the current pixel shader invocation may or may not participate in the calculation of the requested derivative, because the derivative will be calculated only once per 2x2 quad.</span></span> <span data-ttu-id="96daf-117">Por exemplo, a derivação x pode ser um Delta da linha superior de pixels e a direção y ([derivada de \_ rty \_ ](deriv-rty-coarse--sm5---asm-.md)) poderia ser um Delta da coluna esquerda de pixels.</span><span class="sxs-lookup"><span data-stu-id="96daf-117">For example, the x derivative could be a delta from the top row of pixels, and the y direction ([deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md)) could be a delta from the left column of pixels.</span></span> <span data-ttu-id="96daf-118">O cálculo exato é até o fornecedor do hardware.</span><span class="sxs-lookup"><span data-stu-id="96daf-118">The exact calculation is up to the hardware vendor.</span></span> <span data-ttu-id="96daf-119">Também não há nenhuma especificação que determine como as quatro quádruplas de 2x2 serão alinhadas ou colocadas em um primitivo.</span><span class="sxs-lookup"><span data-stu-id="96daf-119">There is also no specification dictating how the 2x2 quads will be aligned or tiled over a primitive.</span></span>

<span data-ttu-id="96daf-120">Os derivativos são calculados em um nível mais baixo, uma vez por quatro por 2x2 pixels.</span><span class="sxs-lookup"><span data-stu-id="96daf-120">Derivatives are calculated at a coarse level, once per 2x2 pixel quad.</span></span> <span data-ttu-id="96daf-121">Essa instrução e [o \_ rty \_ de derivação](deriv-rty-coarse--sm5---asm-.md) são alternativas para [derivar \_ RTX \_ bem](deriv-rtx-fine--sm5---asm-.md) e [derivar \_ rty \_ ](deriv-rty-fine--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="96daf-121">This instruction and [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md) are alternatives to [deriv\_rtx\_fine](deriv-rtx-fine--sm5---asm-.md) and [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md).</span></span> <span data-ttu-id="96daf-122">Essas \_ \_ instruções derivadas mais altas e finas são uma substituição para **derivar \_ rtxderiv \_ rty** de modelos de sombreador anteriores.</span><span class="sxs-lookup"><span data-stu-id="96daf-122">These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtxderiv\_rty** from previous shader models .</span></span>

<span data-ttu-id="96daf-123">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="96daf-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="96daf-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="96daf-124">Vertex</span></span> | <span data-ttu-id="96daf-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="96daf-125">Hull</span></span> | <span data-ttu-id="96daf-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="96daf-126">Domain</span></span> | <span data-ttu-id="96daf-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="96daf-127">Geometry</span></span> | <span data-ttu-id="96daf-128">16x16</span><span class="sxs-lookup"><span data-stu-id="96daf-128">Pixel</span></span> | <span data-ttu-id="96daf-129">Computação</span><span class="sxs-lookup"><span data-stu-id="96daf-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="96daf-130">X</span><span class="sxs-lookup"><span data-stu-id="96daf-130">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="96daf-131">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="96daf-131">Minimum Shader Model</span></span>

<span data-ttu-id="96daf-132">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="96daf-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="96daf-133">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="96daf-133">Shader Model</span></span>                                              | <span data-ttu-id="96daf-134">Com suporte</span><span class="sxs-lookup"><span data-stu-id="96daf-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="96daf-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="96daf-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="96daf-136">sim</span><span class="sxs-lookup"><span data-stu-id="96daf-136">yes</span></span>       |
| [<span data-ttu-id="96daf-137">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="96daf-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="96daf-138">não</span><span class="sxs-lookup"><span data-stu-id="96daf-138">no</span></span>        |
| [<span data-ttu-id="96daf-139">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="96daf-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="96daf-140">não</span><span class="sxs-lookup"><span data-stu-id="96daf-140">no</span></span>        |
| [<span data-ttu-id="96daf-141">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="96daf-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="96daf-142">não</span><span class="sxs-lookup"><span data-stu-id="96daf-142">no</span></span>        |
| [<span data-ttu-id="96daf-143">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="96daf-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="96daf-144">não</span><span class="sxs-lookup"><span data-stu-id="96daf-144">no</span></span>        |
| [<span data-ttu-id="96daf-145">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="96daf-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="96daf-146">não</span><span class="sxs-lookup"><span data-stu-id="96daf-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="96daf-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="96daf-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96daf-148">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="96daf-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





