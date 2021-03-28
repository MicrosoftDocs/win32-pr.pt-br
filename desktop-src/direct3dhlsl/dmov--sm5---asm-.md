---
title: dmov (SM5-ASM)
description: Movimentação por componentes. | dmov (SM5-ASM)
ms.assetid: 05DBB9E2-10EC-4324-BB8F-1A9E315DE90C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b7d9c5ca0da1671ddf30fb9746333617f7688a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930518"
---
# <a name="dmov-sm5---asm"></a><span data-ttu-id="2b86e-104">dmov (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2b86e-104">dmov (sm5 - asm)</span></span>

<span data-ttu-id="2b86e-105">Movimentação por componentes.</span><span class="sxs-lookup"><span data-stu-id="2b86e-105">Component-wise move.</span></span>



| <span data-ttu-id="2b86e-106">dmov \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="2b86e-106">dmov\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="2b86e-107">Item</span><span class="sxs-lookup"><span data-stu-id="2b86e-107">Item</span></span>                                                            | <span data-ttu-id="2b86e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b86e-108">Description</span></span>                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="2b86e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2b86e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2b86e-110">\[no \] destino da movimentação.</span><span class="sxs-lookup"><span data-stu-id="2b86e-110">\[in\] The move destination.</span></span> <span data-ttu-id="2b86e-111">*dest*  =  *src0*.</span><span class="sxs-lookup"><span data-stu-id="2b86e-111">*dest* = *src0*.</span></span><br/> |
| <span data-ttu-id="2b86e-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2b86e-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2b86e-113">\[nos \] componentes a serem movidos.</span><span class="sxs-lookup"><span data-stu-id="2b86e-113">\[in\] The components to be moved.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="2b86e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b86e-114">Remarks</span></span>

<span data-ttu-id="2b86e-115">Os modificadores, exceto swizzle, assumem que os dados são de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="2b86e-115">The modifiers, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="2b86e-116">A ausência de modificadores move dados sem alterar bits.</span><span class="sxs-lookup"><span data-stu-id="2b86e-116">The absence of modifiers moves data without altering bits.</span></span>

<span data-ttu-id="2b86e-117">O swizzles válido para os parâmetros de origem são. xyzw,. xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="2b86e-117">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="2b86e-118">Os seguintes mapeamentos *src* são swizzle:</span><span class="sxs-lookup"><span data-stu-id="2b86e-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="2b86e-119">*src0* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="2b86e-119">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="2b86e-120">*src1* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="2b86e-120">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="2b86e-121">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="2b86e-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2b86e-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="2b86e-122">Vertex</span></span> | <span data-ttu-id="2b86e-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="2b86e-123">Hull</span></span> | <span data-ttu-id="2b86e-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="2b86e-124">Domain</span></span> | <span data-ttu-id="2b86e-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="2b86e-125">Geometry</span></span> | <span data-ttu-id="2b86e-126">16x16</span><span class="sxs-lookup"><span data-stu-id="2b86e-126">Pixel</span></span> | <span data-ttu-id="2b86e-127">Computação</span><span class="sxs-lookup"><span data-stu-id="2b86e-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2b86e-128">X</span><span class="sxs-lookup"><span data-stu-id="2b86e-128">X</span></span>      | <span data-ttu-id="2b86e-129">X</span><span class="sxs-lookup"><span data-stu-id="2b86e-129">X</span></span>    | <span data-ttu-id="2b86e-130">X</span><span class="sxs-lookup"><span data-stu-id="2b86e-130">X</span></span>      | <span data-ttu-id="2b86e-131">X</span><span class="sxs-lookup"><span data-stu-id="2b86e-131">X</span></span>        | <span data-ttu-id="2b86e-132">X</span><span class="sxs-lookup"><span data-stu-id="2b86e-132">X</span></span>     | <span data-ttu-id="2b86e-133">X</span><span class="sxs-lookup"><span data-stu-id="2b86e-133">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2b86e-134">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="2b86e-134">Minimum Shader Model</span></span>

<span data-ttu-id="2b86e-135">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="2b86e-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2b86e-136">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="2b86e-136">Shader Model</span></span>                                              | <span data-ttu-id="2b86e-137">Com suporte</span><span class="sxs-lookup"><span data-stu-id="2b86e-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2b86e-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2b86e-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2b86e-139">sim</span><span class="sxs-lookup"><span data-stu-id="2b86e-139">yes</span></span>       |
| [<span data-ttu-id="2b86e-140">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="2b86e-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2b86e-141">não</span><span class="sxs-lookup"><span data-stu-id="2b86e-141">no</span></span>        |
| [<span data-ttu-id="2b86e-142">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="2b86e-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2b86e-143">não</span><span class="sxs-lookup"><span data-stu-id="2b86e-143">no</span></span>        |
| [<span data-ttu-id="2b86e-144">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b86e-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2b86e-145">não</span><span class="sxs-lookup"><span data-stu-id="2b86e-145">no</span></span>        |
| [<span data-ttu-id="2b86e-146">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b86e-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2b86e-147">não</span><span class="sxs-lookup"><span data-stu-id="2b86e-147">no</span></span>        |
| [<span data-ttu-id="2b86e-148">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b86e-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2b86e-149">não</span><span class="sxs-lookup"><span data-stu-id="2b86e-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2b86e-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b86e-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b86e-151">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b86e-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





