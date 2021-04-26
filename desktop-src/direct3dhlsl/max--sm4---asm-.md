---
title: Max (sm4-ASM)
description: Máximo de float de componente.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64d88c581828f2563f6d5d8a6c57de6400f9bbf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994723"
---
# <a name="max-sm4---asm"></a><span data-ttu-id="28914-103">Max (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="28914-103">max (sm4 - asm)</span></span>

<span data-ttu-id="28914-104">Máximo de float de componente.</span><span class="sxs-lookup"><span data-stu-id="28914-104">Component-wise float maximum.</span></span>



| <span data-ttu-id="28914-105">máximo \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="28914-105">max\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="28914-106">Item</span><span class="sxs-lookup"><span data-stu-id="28914-106">Item</span></span>                                                            | <span data-ttu-id="28914-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="28914-107">Description</span></span>                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28914-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="28914-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="28914-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="28914-109">\[in\] The result of the operation.</span></span> <br/> <span data-ttu-id="28914-110">*dest*  =  *src0*  >=  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="28914-110">*dest* = *src0* >= *src1* ?</span></span> <span data-ttu-id="28914-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="28914-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="28914-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="28914-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="28914-113">\[nos \] componentes para comparar com o *src1*.</span><span class="sxs-lookup"><span data-stu-id="28914-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                    |
| <span data-ttu-id="28914-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="28914-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="28914-115">\[nos \] componentes para comparar com o *src0*.</span><span class="sxs-lookup"><span data-stu-id="28914-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="28914-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="28914-116">Remarks</span></span>

><span data-ttu-id="28914-117">= é usado em vez de > de forma que, se min (x, y) = x, Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="28914-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="28914-118">NaN tem tratamento especial.</span><span class="sxs-lookup"><span data-stu-id="28914-118">NaN has special handling.</span></span> <span data-ttu-id="28914-119">Se um operando de origem for NaN, o outro operando de origem será retornado e a escolha será feita por componente.</span><span class="sxs-lookup"><span data-stu-id="28914-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="28914-120">Se ambos forem NaN, qualquer representação NaN será retornada.</span><span class="sxs-lookup"><span data-stu-id="28914-120">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="28914-121">As normas são liberadas com Sign preservado antes da comparação.</span><span class="sxs-lookup"><span data-stu-id="28914-121">Denorms are flushed with sign preserved before the comparison.</span></span> <span data-ttu-id="28914-122">No entanto, o resultado gravado no *dest* pode ou não ser liberado.</span><span class="sxs-lookup"><span data-stu-id="28914-122">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="28914-123">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="28914-123">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="28914-124">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="28914-124">F means finite real number.</span></span>



| <span data-ttu-id="28914-125">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="28914-125">**src0 src1->**</span></span> | <span data-ttu-id="28914-126">**-INF**</span><span class="sxs-lookup"><span data-stu-id="28914-126">**-inf**</span></span> | <span data-ttu-id="28914-127">**F**</span><span class="sxs-lookup"><span data-stu-id="28914-127">**F**</span></span>        | <span data-ttu-id="28914-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="28914-128">**+inf**</span></span> | <span data-ttu-id="28914-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="28914-129">**NaN**</span></span> |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="28914-130">**-INF**</span><span class="sxs-lookup"><span data-stu-id="28914-130">**-inf**</span></span>           | <span data-ttu-id="28914-131">-inf</span><span class="sxs-lookup"><span data-stu-id="28914-131">-inf</span></span>     | <span data-ttu-id="28914-132">src1</span><span class="sxs-lookup"><span data-stu-id="28914-132">src1</span></span>         | <span data-ttu-id="28914-133">+inf</span><span class="sxs-lookup"><span data-stu-id="28914-133">+inf</span></span>     | <span data-ttu-id="28914-134">-inf</span><span class="sxs-lookup"><span data-stu-id="28914-134">-inf</span></span>    |
| <span data-ttu-id="28914-135">**F**</span><span class="sxs-lookup"><span data-stu-id="28914-135">**F**</span></span>              | <span data-ttu-id="28914-136">src0</span><span class="sxs-lookup"><span data-stu-id="28914-136">src0</span></span>     | <span data-ttu-id="28914-137">src0 ou src1</span><span class="sxs-lookup"><span data-stu-id="28914-137">src0 or src1</span></span> | <span data-ttu-id="28914-138">+inf</span><span class="sxs-lookup"><span data-stu-id="28914-138">+inf</span></span>     | <span data-ttu-id="28914-139">src0</span><span class="sxs-lookup"><span data-stu-id="28914-139">src0</span></span>    |
| <span data-ttu-id="28914-140">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="28914-140">**+inf**</span></span>           | <span data-ttu-id="28914-141">+inf</span><span class="sxs-lookup"><span data-stu-id="28914-141">+inf</span></span>     | <span data-ttu-id="28914-142">+inf</span><span class="sxs-lookup"><span data-stu-id="28914-142">+inf</span></span>         | <span data-ttu-id="28914-143">+inf</span><span class="sxs-lookup"><span data-stu-id="28914-143">+inf</span></span>     | <span data-ttu-id="28914-144">+inf</span><span class="sxs-lookup"><span data-stu-id="28914-144">+inf</span></span>    |
| <span data-ttu-id="28914-145">**NaN**</span><span class="sxs-lookup"><span data-stu-id="28914-145">**NaN**</span></span>            | <span data-ttu-id="28914-146">-inf</span><span class="sxs-lookup"><span data-stu-id="28914-146">-inf</span></span>     | <span data-ttu-id="28914-147">src1</span><span class="sxs-lookup"><span data-stu-id="28914-147">src1</span></span>         | <span data-ttu-id="28914-148">+inf</span><span class="sxs-lookup"><span data-stu-id="28914-148">+inf</span></span>     | <span data-ttu-id="28914-149">NaN</span><span class="sxs-lookup"><span data-stu-id="28914-149">NaN</span></span>     |



 

<span data-ttu-id="28914-150">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="28914-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="28914-151">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="28914-151">Vertex Shader</span></span> | <span data-ttu-id="28914-152">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="28914-152">Geometry Shader</span></span> | <span data-ttu-id="28914-153">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="28914-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="28914-154">x</span><span class="sxs-lookup"><span data-stu-id="28914-154">x</span></span>             | <span data-ttu-id="28914-155">x</span><span class="sxs-lookup"><span data-stu-id="28914-155">x</span></span>               | <span data-ttu-id="28914-156">x</span><span class="sxs-lookup"><span data-stu-id="28914-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="28914-157">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="28914-157">Minimum Shader Model</span></span>

<span data-ttu-id="28914-158">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="28914-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="28914-159">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="28914-159">Shader Model</span></span>                                              | <span data-ttu-id="28914-160">Suportado</span><span class="sxs-lookup"><span data-stu-id="28914-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="28914-161">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="28914-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="28914-162">sim</span><span class="sxs-lookup"><span data-stu-id="28914-162">yes</span></span>       |
| [<span data-ttu-id="28914-163">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="28914-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="28914-164">sim</span><span class="sxs-lookup"><span data-stu-id="28914-164">yes</span></span>       |
| [<span data-ttu-id="28914-165">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="28914-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="28914-166">sim</span><span class="sxs-lookup"><span data-stu-id="28914-166">yes</span></span>       |
| [<span data-ttu-id="28914-167">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="28914-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="28914-168">não</span><span class="sxs-lookup"><span data-stu-id="28914-168">no</span></span>        |
| [<span data-ttu-id="28914-169">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="28914-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="28914-170">não</span><span class="sxs-lookup"><span data-stu-id="28914-170">no</span></span>        |
| [<span data-ttu-id="28914-171">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="28914-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="28914-172">não</span><span class="sxs-lookup"><span data-stu-id="28914-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="28914-173">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28914-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28914-174">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="28914-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





