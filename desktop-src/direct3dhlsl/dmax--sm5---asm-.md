---
title: DMáx (SM5-ASM)
description: Máximo de precisão dupla por componente.
ms.assetid: 34ED8B34-2592-4BBB-BCF0-F2222E4D51D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703b277a98b16570de6f5ab7e0e7643ddfdcc705
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365203"
---
# <a name="dmax-sm5---asm"></a><span data-ttu-id="d7822-103">DMáx (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="d7822-103">dmax (sm5 - asm)</span></span>

<span data-ttu-id="d7822-104">Máximo de precisão dupla por componente.</span><span class="sxs-lookup"><span data-stu-id="d7822-104">Component-wise double-precision maximum.</span></span>



| <span data-ttu-id="d7822-105">DMáx \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d7822-105">dmax\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="d7822-106">Item</span><span class="sxs-lookup"><span data-stu-id="d7822-106">Item</span></span>                                                            | <span data-ttu-id="d7822-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7822-107">Description</span></span>                                                                                                                                                                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7822-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d7822-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d7822-109">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="d7822-109">\[in\] The address of the results of the operation.</span></span><br/> <span data-ttu-id="d7822-110">*dest*  =  *src0*  >=  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="d7822-110">*dest* = *src0* >= *src1* ?</span></span> <span data-ttu-id="d7822-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="d7822-111">*src0* : *src1*</span></span><br/> <span data-ttu-id="d7822-112">>= é usado em vez de > de forma que, se min (x, y) = x, Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="d7822-112">>= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span> <br/> |
| <span data-ttu-id="d7822-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d7822-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d7822-114">\[no \] valor a ser comparado com *src1*.</span><span class="sxs-lookup"><span data-stu-id="d7822-114">\[in\] The value to compare with *src1*.</span></span><br/>                                                                                                                                                           |
| <span data-ttu-id="d7822-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="d7822-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="d7822-116">\[no \] valor a ser comparado com *src0*.</span><span class="sxs-lookup"><span data-stu-id="d7822-116">\[in\] The value to compare with *src0*.</span></span><br/>                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="d7822-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7822-117">Remarks</span></span>

<span data-ttu-id="d7822-118">NaN tem tratamento especial.</span><span class="sxs-lookup"><span data-stu-id="d7822-118">NaN has special handling.</span></span> <span data-ttu-id="d7822-119">Se um operando de origem for NaN, o outro operando de origem será retornado.</span><span class="sxs-lookup"><span data-stu-id="d7822-119">If one source operand is NaN, then the other source operand is returned.</span></span> <span data-ttu-id="d7822-120">A escolha é feita por componente.</span><span class="sxs-lookup"><span data-stu-id="d7822-120">The choice is made per-component.</span></span> <span data-ttu-id="d7822-121">Se ambos forem NaN, qualquer representação NaN será retornada.</span><span class="sxs-lookup"><span data-stu-id="d7822-121">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="d7822-122">O swizzles válido para os parâmetros de origem são. xyzw,. xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="d7822-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="d7822-123">As máscaras de *destino* válidas são. XY,. zw e. xyzw.</span><span class="sxs-lookup"><span data-stu-id="d7822-123">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="d7822-124">Os seguintes mapeamentos *src* são swizzle:</span><span class="sxs-lookup"><span data-stu-id="d7822-124">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="d7822-125">*dest* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="d7822-125">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="d7822-126">*src0* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="d7822-126">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="d7822-127">*src1* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="d7822-127">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="d7822-128">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="d7822-128">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d7822-129">Vértice</span><span class="sxs-lookup"><span data-stu-id="d7822-129">Vertex</span></span> | <span data-ttu-id="d7822-130">Envoltória</span><span class="sxs-lookup"><span data-stu-id="d7822-130">Hull</span></span> | <span data-ttu-id="d7822-131">Domínio</span><span class="sxs-lookup"><span data-stu-id="d7822-131">Domain</span></span> | <span data-ttu-id="d7822-132">Geometria</span><span class="sxs-lookup"><span data-stu-id="d7822-132">Geometry</span></span> | <span data-ttu-id="d7822-133">16x16</span><span class="sxs-lookup"><span data-stu-id="d7822-133">Pixel</span></span> | <span data-ttu-id="d7822-134">Computação</span><span class="sxs-lookup"><span data-stu-id="d7822-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d7822-135">X</span><span class="sxs-lookup"><span data-stu-id="d7822-135">X</span></span>      | <span data-ttu-id="d7822-136">X</span><span class="sxs-lookup"><span data-stu-id="d7822-136">X</span></span>    | <span data-ttu-id="d7822-137">X</span><span class="sxs-lookup"><span data-stu-id="d7822-137">X</span></span>      | <span data-ttu-id="d7822-138">X</span><span class="sxs-lookup"><span data-stu-id="d7822-138">X</span></span>        | <span data-ttu-id="d7822-139">X</span><span class="sxs-lookup"><span data-stu-id="d7822-139">X</span></span>     | <span data-ttu-id="d7822-140">X</span><span class="sxs-lookup"><span data-stu-id="d7822-140">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d7822-141">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="d7822-141">Minimum Shader Model</span></span>

<span data-ttu-id="d7822-142">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="d7822-142">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d7822-143">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="d7822-143">Shader Model</span></span>                                              | <span data-ttu-id="d7822-144">Com suporte</span><span class="sxs-lookup"><span data-stu-id="d7822-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d7822-145">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d7822-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d7822-146">sim</span><span class="sxs-lookup"><span data-stu-id="d7822-146">yes</span></span>       |
| [<span data-ttu-id="d7822-147">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="d7822-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d7822-148">não</span><span class="sxs-lookup"><span data-stu-id="d7822-148">no</span></span>        |
| [<span data-ttu-id="d7822-149">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="d7822-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d7822-150">não</span><span class="sxs-lookup"><span data-stu-id="d7822-150">no</span></span>        |
| [<span data-ttu-id="d7822-151">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7822-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d7822-152">não</span><span class="sxs-lookup"><span data-stu-id="d7822-152">no</span></span>        |
| [<span data-ttu-id="d7822-153">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7822-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d7822-154">não</span><span class="sxs-lookup"><span data-stu-id="d7822-154">no</span></span>        |
| [<span data-ttu-id="d7822-155">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7822-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d7822-156">não</span><span class="sxs-lookup"><span data-stu-id="d7822-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d7822-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7822-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7822-158">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7822-158">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





