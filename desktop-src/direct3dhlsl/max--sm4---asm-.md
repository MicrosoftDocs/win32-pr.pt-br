---
title: Max (sm4-ASM)
description: Máximo de float de componente.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f24618897eacf250f2b924f6dde3745a32a7172
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365194"
---
# <a name="max-sm4---asm"></a><span data-ttu-id="04830-103">Max (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="04830-103">max (sm4 - asm)</span></span>

<span data-ttu-id="04830-104">Máximo de float de componente.</span><span class="sxs-lookup"><span data-stu-id="04830-104">Component-wise float maximum.</span></span>



| <span data-ttu-id="04830-105">máximo \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="04830-105">max\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="04830-106">Item</span><span class="sxs-lookup"><span data-stu-id="04830-106">Item</span></span>                                                            | <span data-ttu-id="04830-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="04830-107">Description</span></span>                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04830-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="04830-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="04830-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="04830-109">\[in\] The result of the operation.</span></span> <br/> <span data-ttu-id="04830-110">*dest*  =  *src0*  >=  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="04830-110">*dest* = *src0* >= *src1* ?</span></span> <span data-ttu-id="04830-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="04830-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="04830-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="04830-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="04830-113">\[nos \] componentes para comparar com o *src1*.</span><span class="sxs-lookup"><span data-stu-id="04830-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                    |
| <span data-ttu-id="04830-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="04830-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="04830-115">\[nos \] componentes para comparar com o *src0*.</span><span class="sxs-lookup"><span data-stu-id="04830-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="04830-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="04830-116">Remarks</span></span>

><span data-ttu-id="04830-117">= é usado em vez de > de forma que, se min (x, y) = x, Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="04830-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="04830-118">NaN tem tratamento especial.</span><span class="sxs-lookup"><span data-stu-id="04830-118">NaN has special handling.</span></span> <span data-ttu-id="04830-119">Se um operando de origem for NaN, o outro operando de origem será retornado e a escolha será feita por componente.</span><span class="sxs-lookup"><span data-stu-id="04830-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="04830-120">Se ambos forem NaN, qualquer representação NaN será retornada.</span><span class="sxs-lookup"><span data-stu-id="04830-120">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="04830-121">As normas são liberadas com Sign preservado antes da comparação.</span><span class="sxs-lookup"><span data-stu-id="04830-121">Denorms are flushed with sign preserved before the comparison.</span></span> <span data-ttu-id="04830-122">No entanto, o resultado gravado no *dest* pode ou não ser liberado.</span><span class="sxs-lookup"><span data-stu-id="04830-122">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="04830-123">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="04830-123">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="04830-124">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="04830-124">F means finite real number.</span></span>



|                    |          |              |          |         |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="04830-125">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="04830-125">**src0 src1->**</span></span> | <span data-ttu-id="04830-126">**-INF**</span><span class="sxs-lookup"><span data-stu-id="04830-126">**-inf**</span></span> | <span data-ttu-id="04830-127">**F**</span><span class="sxs-lookup"><span data-stu-id="04830-127">**F**</span></span>        | <span data-ttu-id="04830-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="04830-128">**+inf**</span></span> | <span data-ttu-id="04830-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="04830-129">**NaN**</span></span> |
| <span data-ttu-id="04830-130">**-INF**</span><span class="sxs-lookup"><span data-stu-id="04830-130">**-inf**</span></span>           | <span data-ttu-id="04830-131">-inf</span><span class="sxs-lookup"><span data-stu-id="04830-131">-inf</span></span>     | <span data-ttu-id="04830-132">src1</span><span class="sxs-lookup"><span data-stu-id="04830-132">src1</span></span>         | <span data-ttu-id="04830-133">+inf</span><span class="sxs-lookup"><span data-stu-id="04830-133">+inf</span></span>     | <span data-ttu-id="04830-134">-inf</span><span class="sxs-lookup"><span data-stu-id="04830-134">-inf</span></span>    |
| <span data-ttu-id="04830-135">**F**</span><span class="sxs-lookup"><span data-stu-id="04830-135">**F**</span></span>              | <span data-ttu-id="04830-136">src0</span><span class="sxs-lookup"><span data-stu-id="04830-136">src0</span></span>     | <span data-ttu-id="04830-137">src0 ou src1</span><span class="sxs-lookup"><span data-stu-id="04830-137">src0 or src1</span></span> | <span data-ttu-id="04830-138">+inf</span><span class="sxs-lookup"><span data-stu-id="04830-138">+inf</span></span>     | <span data-ttu-id="04830-139">src0</span><span class="sxs-lookup"><span data-stu-id="04830-139">src0</span></span>    |
| <span data-ttu-id="04830-140">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="04830-140">**+inf**</span></span>           | <span data-ttu-id="04830-141">+inf</span><span class="sxs-lookup"><span data-stu-id="04830-141">+inf</span></span>     | <span data-ttu-id="04830-142">+inf</span><span class="sxs-lookup"><span data-stu-id="04830-142">+inf</span></span>         | <span data-ttu-id="04830-143">+inf</span><span class="sxs-lookup"><span data-stu-id="04830-143">+inf</span></span>     | <span data-ttu-id="04830-144">+inf</span><span class="sxs-lookup"><span data-stu-id="04830-144">+inf</span></span>    |
| <span data-ttu-id="04830-145">**NaN**</span><span class="sxs-lookup"><span data-stu-id="04830-145">**NaN**</span></span>            | <span data-ttu-id="04830-146">-inf</span><span class="sxs-lookup"><span data-stu-id="04830-146">-inf</span></span>     | <span data-ttu-id="04830-147">src1</span><span class="sxs-lookup"><span data-stu-id="04830-147">src1</span></span>         | <span data-ttu-id="04830-148">+inf</span><span class="sxs-lookup"><span data-stu-id="04830-148">+inf</span></span>     | <span data-ttu-id="04830-149">NaN</span><span class="sxs-lookup"><span data-stu-id="04830-149">NaN</span></span>     |



 

<span data-ttu-id="04830-150">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="04830-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="04830-151">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="04830-151">Vertex Shader</span></span> | <span data-ttu-id="04830-152">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="04830-152">Geometry Shader</span></span> | <span data-ttu-id="04830-153">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="04830-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="04830-154">x</span><span class="sxs-lookup"><span data-stu-id="04830-154">x</span></span>             | <span data-ttu-id="04830-155">x</span><span class="sxs-lookup"><span data-stu-id="04830-155">x</span></span>               | <span data-ttu-id="04830-156">x</span><span class="sxs-lookup"><span data-stu-id="04830-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="04830-157">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="04830-157">Minimum Shader Model</span></span>

<span data-ttu-id="04830-158">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="04830-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="04830-159">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="04830-159">Shader Model</span></span>                                              | <span data-ttu-id="04830-160">Com suporte</span><span class="sxs-lookup"><span data-stu-id="04830-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="04830-161">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="04830-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="04830-162">sim</span><span class="sxs-lookup"><span data-stu-id="04830-162">yes</span></span>       |
| [<span data-ttu-id="04830-163">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="04830-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="04830-164">sim</span><span class="sxs-lookup"><span data-stu-id="04830-164">yes</span></span>       |
| [<span data-ttu-id="04830-165">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="04830-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="04830-166">sim</span><span class="sxs-lookup"><span data-stu-id="04830-166">yes</span></span>       |
| [<span data-ttu-id="04830-167">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="04830-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="04830-168">não</span><span class="sxs-lookup"><span data-stu-id="04830-168">no</span></span>        |
| [<span data-ttu-id="04830-169">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="04830-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="04830-170">não</span><span class="sxs-lookup"><span data-stu-id="04830-170">no</span></span>        |
| [<span data-ttu-id="04830-171">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="04830-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="04830-172">não</span><span class="sxs-lookup"><span data-stu-id="04830-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="04830-173">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="04830-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04830-174">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="04830-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





