---
title: deriv_rtx_fine (SM5-ASM)
description: Computa a taxa de alteração de componentes. | deriv_rtx_fine (SM5-ASM)
ms.assetid: 5752C85B-2965-489C-BF27-968FAF5EAA52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73061e3220704cf2c19e28b4d6d434fda43fb941
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989215"
---
# <a name="deriv_rtx_fine-sm5---asm"></a><span data-ttu-id="efe1e-104">derivar \_ RTX \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="efe1e-104">deriv\_rtx\_fine (sm5 - asm)</span></span>

<span data-ttu-id="efe1e-105">Computa a taxa de alteração de componentes.</span><span class="sxs-lookup"><span data-stu-id="efe1e-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="efe1e-106">deriva \_ RTX \_ de \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="efe1e-106">deriv\_rtx\_fine\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="efe1e-107">Item</span><span class="sxs-lookup"><span data-stu-id="efe1e-107">Item</span></span>                                                            | <span data-ttu-id="efe1e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="efe1e-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="efe1e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="efe1e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="efe1e-110">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="efe1e-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="efe1e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="efe1e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="efe1e-112">\[nos \] componentes na operação.</span><span class="sxs-lookup"><span data-stu-id="efe1e-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="efe1e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="efe1e-113">Remarks</span></span>

<span data-ttu-id="efe1e-114">Essa instrução computa a taxa de alteração de conteúdo de cada componente float32 de *src0* (post-swizzle), com relação à direção de renderTarget x (RTX) ou à direção de renderTarget y (Confira [derivação \_ rty \_ boa](deriv-rty-fine--sm5---asm-.md)).</span><span class="sxs-lookup"><span data-stu-id="efe1e-114">This instruction computes the rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction (see [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md)).</span></span> <span data-ttu-id="efe1e-115">Cada pixel no carimbo 2x2 Obtém um par exclusivo de cálculos derivativos x/y</span><span class="sxs-lookup"><span data-stu-id="efe1e-115">Each pixel in the 2x2 stamp gets a unique pair of x/y derivative calculations</span></span>

<span data-ttu-id="efe1e-116">Os dados na invocação do sombreador de pixel atual sempre participam do cálculo do derivativo solicitado.</span><span class="sxs-lookup"><span data-stu-id="efe1e-116">The data in the current pixel shader invocation always participates in the calculation of the requested derivative.</span></span> <span data-ttu-id="efe1e-117">No meio do 2x2 pixel em que o pixel atual cai, a derivada x é o Delta da linha de 2 pixels, incluindo o pixel atual.</span><span class="sxs-lookup"><span data-stu-id="efe1e-117">In the 2x2 pixel quad the current pixel falls within, the x derivative is the delta of the row of 2 pixels including the current pixel.</span></span> <span data-ttu-id="efe1e-118">A derivada y é o Delta da coluna de 2 pixels, incluindo o pixel atual.</span><span class="sxs-lookup"><span data-stu-id="efe1e-118">The y derivative is the delta of the column of 2 pixels including the current pixel.</span></span> <span data-ttu-id="efe1e-119">Não há nenhuma especificação que informando como os quatro de 2x2 serão alinhados ou colocados em um primitivo.</span><span class="sxs-lookup"><span data-stu-id="efe1e-119">There is no specification dictating how the 2x2 quads will be aligned or tiled over a primitive.</span></span>

<span data-ttu-id="efe1e-120">Os derivativos são calculados em um nível refinado (cálculo exclusivo do par derivado x/y para cada pixel em um 2x2 Quad).</span><span class="sxs-lookup"><span data-stu-id="efe1e-120">Derivatives are calculated at a fine level (unique calculation of the x/y derivative pair for each pixel in a 2x2 quad).</span></span> <span data-ttu-id="efe1e-121">Essa instrução e [o \_ rty \_ de derivação](deriv-rty-fine--sm5---asm-.md) são alternativas para [derivar \_ RTX \_ ](deriv-rtx-coarse--sm5---asm-.md) e derivar [ \_ rty \_ grande](deriv-rty-coarse--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="efe1e-121">This instruction and [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md) are alternatives to [deriv\_rtx\_coarse](deriv-rtx-coarse--sm5---asm-.md) and [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md).</span></span> <span data-ttu-id="efe1e-122">Essas \_ \_ instruções derivadas mais altas e refinadas são uma substituição para **derivar \_ RTX** essas \_ \_ instruções derivativas e exfinadas são uma substituição para **derivar \_ RTX** e **derivar \_ rty** de modelos de sombreador anteriores.</span><span class="sxs-lookup"><span data-stu-id="efe1e-122">These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtx** These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtx** and **deriv\_rty** from previous shader models.</span></span>

<span data-ttu-id="efe1e-123">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="efe1e-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="efe1e-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="efe1e-124">Vertex</span></span> | <span data-ttu-id="efe1e-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="efe1e-125">Hull</span></span> | <span data-ttu-id="efe1e-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="efe1e-126">Domain</span></span> | <span data-ttu-id="efe1e-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="efe1e-127">Geometry</span></span> | <span data-ttu-id="efe1e-128">16x16</span><span class="sxs-lookup"><span data-stu-id="efe1e-128">Pixel</span></span> | <span data-ttu-id="efe1e-129">Computação</span><span class="sxs-lookup"><span data-stu-id="efe1e-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="efe1e-130">X</span><span class="sxs-lookup"><span data-stu-id="efe1e-130">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="efe1e-131">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="efe1e-131">Minimum Shader Model</span></span>

<span data-ttu-id="efe1e-132">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="efe1e-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="efe1e-133">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="efe1e-133">Shader Model</span></span>                                              | <span data-ttu-id="efe1e-134">Com suporte</span><span class="sxs-lookup"><span data-stu-id="efe1e-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="efe1e-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="efe1e-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="efe1e-136">sim</span><span class="sxs-lookup"><span data-stu-id="efe1e-136">yes</span></span>       |
| [<span data-ttu-id="efe1e-137">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="efe1e-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="efe1e-138">não</span><span class="sxs-lookup"><span data-stu-id="efe1e-138">no</span></span>        |
| [<span data-ttu-id="efe1e-139">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="efe1e-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="efe1e-140">não</span><span class="sxs-lookup"><span data-stu-id="efe1e-140">no</span></span>        |
| [<span data-ttu-id="efe1e-141">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="efe1e-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="efe1e-142">não</span><span class="sxs-lookup"><span data-stu-id="efe1e-142">no</span></span>        |
| [<span data-ttu-id="efe1e-143">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="efe1e-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="efe1e-144">não</span><span class="sxs-lookup"><span data-stu-id="efe1e-144">no</span></span>        |
| [<span data-ttu-id="efe1e-145">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="efe1e-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="efe1e-146">não</span><span class="sxs-lookup"><span data-stu-id="efe1e-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="efe1e-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="efe1e-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efe1e-148">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="efe1e-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





