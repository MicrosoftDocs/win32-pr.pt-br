---
title: min (sm4-ASM)
description: Mínimo de float de componente.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e584aee077735b717bf76d148d4d0db4357a7d95
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104084275"
---
# <a name="min-sm4---asm"></a><span data-ttu-id="3cb5e-103">min (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3cb5e-103">min (sm4 - asm)</span></span>

<span data-ttu-id="3cb5e-104">Mínimo de float de componente.</span><span class="sxs-lookup"><span data-stu-id="3cb5e-104">Component-wise float minimum.</span></span>



| <span data-ttu-id="3cb5e-105">o mínimo \[ \_ \] \[ de dest. Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="3cb5e-105">min\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="3cb5e-106">Item</span><span class="sxs-lookup"><span data-stu-id="3cb5e-106">Item</span></span>                                                            | <span data-ttu-id="3cb5e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3cb5e-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cb5e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="3cb5e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="3cb5e-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="3cb5e-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="3cb5e-110">*dest*  =  *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="3cb5e-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="3cb5e-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="3cb5e-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="3cb5e-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="3cb5e-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="3cb5e-113">\[nos \] componentes para comparar com o *src1*.</span><span class="sxs-lookup"><span data-stu-id="3cb5e-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                  |
| <span data-ttu-id="3cb5e-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="3cb5e-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="3cb5e-115">\[nos \] componentes para comparar com o *src0*.</span><span class="sxs-lookup"><span data-stu-id="3cb5e-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="3cb5e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3cb5e-116">Remarks</span></span>

><span data-ttu-id="3cb5e-117">= é usado em vez de > de forma que, se min (x, y) = x, Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="3cb5e-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="3cb5e-118">NaN tem tratamento especial.</span><span class="sxs-lookup"><span data-stu-id="3cb5e-118">NaN has special handling.</span></span> <span data-ttu-id="3cb5e-119">Se um operando de origem for NaN, o outro operando de origem será retornado e a escolha será feita por componente.</span><span class="sxs-lookup"><span data-stu-id="3cb5e-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="3cb5e-120">Se ambos forem NaN, qualquer representação NaN será retornada.</span><span class="sxs-lookup"><span data-stu-id="3cb5e-120">If both are NaN, any NaN representation is returned.</span></span> <span data-ttu-id="3cb5e-121">Isso está em conformidade com as novas regras IEEE 754R.</span><span class="sxs-lookup"><span data-stu-id="3cb5e-121">This conforms to new IEEE 754R rules.</span></span>

<span data-ttu-id="3cb5e-122">As desnormas são liberadas, com o sinal preservado, antes da comparação.</span><span class="sxs-lookup"><span data-stu-id="3cb5e-122">Denorms are flushed, with the sign preserved, before comparison.</span></span> <span data-ttu-id="3cb5e-123">No entanto, o resultado gravado no *dest* pode ou não ser liberado.</span><span class="sxs-lookup"><span data-stu-id="3cb5e-123">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="3cb5e-124">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="3cb5e-124">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="3cb5e-125">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="3cb5e-125">F means finite real number.</span></span>



|                    |          |              |          |         |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="3cb5e-126">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="3cb5e-126">**src0 src1->**</span></span> | <span data-ttu-id="3cb5e-127">**-INF**</span><span class="sxs-lookup"><span data-stu-id="3cb5e-127">**-inf**</span></span> | <span data-ttu-id="3cb5e-128">**F**</span><span class="sxs-lookup"><span data-stu-id="3cb5e-128">**F**</span></span>        | <span data-ttu-id="3cb5e-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="3cb5e-129">**+inf**</span></span> | <span data-ttu-id="3cb5e-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="3cb5e-130">**NaN**</span></span> |
| <span data-ttu-id="3cb5e-131">**-INF**</span><span class="sxs-lookup"><span data-stu-id="3cb5e-131">**-inf**</span></span>           | <span data-ttu-id="3cb5e-132">-inf</span><span class="sxs-lookup"><span data-stu-id="3cb5e-132">-inf</span></span>     | <span data-ttu-id="3cb5e-133">-inf</span><span class="sxs-lookup"><span data-stu-id="3cb5e-133">-inf</span></span>         | <span data-ttu-id="3cb5e-134">-inf</span><span class="sxs-lookup"><span data-stu-id="3cb5e-134">-inf</span></span>     | <span data-ttu-id="3cb5e-135">-inf</span><span class="sxs-lookup"><span data-stu-id="3cb5e-135">-inf</span></span>    |
| <span data-ttu-id="3cb5e-136">**F**</span><span class="sxs-lookup"><span data-stu-id="3cb5e-136">**F**</span></span>              | <span data-ttu-id="3cb5e-137">-inf</span><span class="sxs-lookup"><span data-stu-id="3cb5e-137">-inf</span></span>     | <span data-ttu-id="3cb5e-138">src0 ou src1</span><span class="sxs-lookup"><span data-stu-id="3cb5e-138">src0 or src1</span></span> | <span data-ttu-id="3cb5e-139">src0</span><span class="sxs-lookup"><span data-stu-id="3cb5e-139">src0</span></span>     | <span data-ttu-id="3cb5e-140">src0</span><span class="sxs-lookup"><span data-stu-id="3cb5e-140">src0</span></span>    |
| <span data-ttu-id="3cb5e-141">**-INF**</span><span class="sxs-lookup"><span data-stu-id="3cb5e-141">**-inf**</span></span>           | <span data-ttu-id="3cb5e-142">-inf</span><span class="sxs-lookup"><span data-stu-id="3cb5e-142">-inf</span></span>     | <span data-ttu-id="3cb5e-143">src1</span><span class="sxs-lookup"><span data-stu-id="3cb5e-143">src1</span></span>         | <span data-ttu-id="3cb5e-144">+inf</span><span class="sxs-lookup"><span data-stu-id="3cb5e-144">+inf</span></span>     | <span data-ttu-id="3cb5e-145">+inf</span><span class="sxs-lookup"><span data-stu-id="3cb5e-145">+inf</span></span>    |
| <span data-ttu-id="3cb5e-146">**NaN**</span><span class="sxs-lookup"><span data-stu-id="3cb5e-146">**NaN**</span></span>            | <span data-ttu-id="3cb5e-147">-inf</span><span class="sxs-lookup"><span data-stu-id="3cb5e-147">-inf</span></span>     | <span data-ttu-id="3cb5e-148">src1</span><span class="sxs-lookup"><span data-stu-id="3cb5e-148">src1</span></span>         | <span data-ttu-id="3cb5e-149">+inf</span><span class="sxs-lookup"><span data-stu-id="3cb5e-149">+inf</span></span>     | <span data-ttu-id="3cb5e-150">NaN</span><span class="sxs-lookup"><span data-stu-id="3cb5e-150">NaN</span></span>     |



 

<span data-ttu-id="3cb5e-151">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="3cb5e-151">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3cb5e-152">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="3cb5e-152">Vertex Shader</span></span> | <span data-ttu-id="3cb5e-153">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="3cb5e-153">Geometry Shader</span></span> | <span data-ttu-id="3cb5e-154">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3cb5e-154">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3cb5e-155">x</span><span class="sxs-lookup"><span data-stu-id="3cb5e-155">x</span></span>             | <span data-ttu-id="3cb5e-156">x</span><span class="sxs-lookup"><span data-stu-id="3cb5e-156">x</span></span>               | <span data-ttu-id="3cb5e-157">x</span><span class="sxs-lookup"><span data-stu-id="3cb5e-157">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3cb5e-158">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="3cb5e-158">Minimum Shader Model</span></span>

<span data-ttu-id="3cb5e-159">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3cb5e-159">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3cb5e-160">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="3cb5e-160">Shader Model</span></span>                                              | <span data-ttu-id="3cb5e-161">Com suporte</span><span class="sxs-lookup"><span data-stu-id="3cb5e-161">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3cb5e-162">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3cb5e-162">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3cb5e-163">sim</span><span class="sxs-lookup"><span data-stu-id="3cb5e-163">yes</span></span>       |
| [<span data-ttu-id="3cb5e-164">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="3cb5e-164">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3cb5e-165">sim</span><span class="sxs-lookup"><span data-stu-id="3cb5e-165">yes</span></span>       |
| [<span data-ttu-id="3cb5e-166">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="3cb5e-166">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3cb5e-167">sim</span><span class="sxs-lookup"><span data-stu-id="3cb5e-167">yes</span></span>       |
| [<span data-ttu-id="3cb5e-168">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3cb5e-168">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3cb5e-169">não</span><span class="sxs-lookup"><span data-stu-id="3cb5e-169">no</span></span>        |
| [<span data-ttu-id="3cb5e-170">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3cb5e-170">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3cb5e-171">não</span><span class="sxs-lookup"><span data-stu-id="3cb5e-171">no</span></span>        |
| [<span data-ttu-id="3cb5e-172">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3cb5e-172">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3cb5e-173">não</span><span class="sxs-lookup"><span data-stu-id="3cb5e-173">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3cb5e-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3cb5e-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cb5e-175">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3cb5e-175">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





