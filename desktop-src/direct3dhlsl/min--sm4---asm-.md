---
title: min (sm4-ASM)
description: Mínimo de float de componente.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8791589b77edc66eeab4b48f10f4a9b16b5cb2d9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993893"
---
# <a name="min-sm4---asm"></a><span data-ttu-id="1c800-103">min (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1c800-103">min (sm4 - asm)</span></span>

<span data-ttu-id="1c800-104">Mínimo de float de componente.</span><span class="sxs-lookup"><span data-stu-id="1c800-104">Component-wise float minimum.</span></span>



| <span data-ttu-id="1c800-105">o mínimo \[ \_ \] \[ de dest. Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="1c800-105">min\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="1c800-106">Item</span><span class="sxs-lookup"><span data-stu-id="1c800-106">Item</span></span>                                                            | <span data-ttu-id="1c800-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c800-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c800-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1c800-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1c800-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="1c800-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="1c800-110">*dest*  =  *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="1c800-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="1c800-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="1c800-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="1c800-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1c800-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1c800-113">\[nos \] componentes para comparar com o *src1*.</span><span class="sxs-lookup"><span data-stu-id="1c800-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                  |
| <span data-ttu-id="1c800-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="1c800-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="1c800-115">\[nos \] componentes para comparar com o *src0*.</span><span class="sxs-lookup"><span data-stu-id="1c800-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="1c800-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c800-116">Remarks</span></span>

><span data-ttu-id="1c800-117">= é usado em vez de > de forma que, se min (x, y) = x, Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="1c800-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="1c800-118">NaN tem tratamento especial.</span><span class="sxs-lookup"><span data-stu-id="1c800-118">NaN has special handling.</span></span> <span data-ttu-id="1c800-119">Se um operando de origem for NaN, o outro operando de origem será retornado e a escolha será feita por componente.</span><span class="sxs-lookup"><span data-stu-id="1c800-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="1c800-120">Se ambos forem NaN, qualquer representação NaN será retornada.</span><span class="sxs-lookup"><span data-stu-id="1c800-120">If both are NaN, any NaN representation is returned.</span></span> <span data-ttu-id="1c800-121">Isso está em conformidade com as novas regras IEEE 754R.</span><span class="sxs-lookup"><span data-stu-id="1c800-121">This conforms to new IEEE 754R rules.</span></span>

<span data-ttu-id="1c800-122">As desnormas são liberadas, com o sinal preservado, antes da comparação.</span><span class="sxs-lookup"><span data-stu-id="1c800-122">Denorms are flushed, with the sign preserved, before comparison.</span></span> <span data-ttu-id="1c800-123">No entanto, o resultado gravado no *dest* pode ou não ser liberado.</span><span class="sxs-lookup"><span data-stu-id="1c800-123">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="1c800-124">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="1c800-124">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="1c800-125">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="1c800-125">F means finite real number.</span></span>



| <span data-ttu-id="1c800-126">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="1c800-126">**src0 src1->**</span></span> | <span data-ttu-id="1c800-127">**-INF**</span><span class="sxs-lookup"><span data-stu-id="1c800-127">**-inf**</span></span> | <span data-ttu-id="1c800-128">**F**</span><span class="sxs-lookup"><span data-stu-id="1c800-128">**F**</span></span>        | <span data-ttu-id="1c800-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="1c800-129">**+inf**</span></span> | <span data-ttu-id="1c800-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="1c800-130">**NaN**</span></span> |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="1c800-131">**-INF**</span><span class="sxs-lookup"><span data-stu-id="1c800-131">**-inf**</span></span>           | <span data-ttu-id="1c800-132">-inf</span><span class="sxs-lookup"><span data-stu-id="1c800-132">-inf</span></span>     | <span data-ttu-id="1c800-133">-inf</span><span class="sxs-lookup"><span data-stu-id="1c800-133">-inf</span></span>         | <span data-ttu-id="1c800-134">-inf</span><span class="sxs-lookup"><span data-stu-id="1c800-134">-inf</span></span>     | <span data-ttu-id="1c800-135">-inf</span><span class="sxs-lookup"><span data-stu-id="1c800-135">-inf</span></span>    |
| <span data-ttu-id="1c800-136">**F**</span><span class="sxs-lookup"><span data-stu-id="1c800-136">**F**</span></span>              | <span data-ttu-id="1c800-137">-inf</span><span class="sxs-lookup"><span data-stu-id="1c800-137">-inf</span></span>     | <span data-ttu-id="1c800-138">src0 ou src1</span><span class="sxs-lookup"><span data-stu-id="1c800-138">src0 or src1</span></span> | <span data-ttu-id="1c800-139">src0</span><span class="sxs-lookup"><span data-stu-id="1c800-139">src0</span></span>     | <span data-ttu-id="1c800-140">src0</span><span class="sxs-lookup"><span data-stu-id="1c800-140">src0</span></span>    |
| <span data-ttu-id="1c800-141">**-INF**</span><span class="sxs-lookup"><span data-stu-id="1c800-141">**-inf**</span></span>           | <span data-ttu-id="1c800-142">-inf</span><span class="sxs-lookup"><span data-stu-id="1c800-142">-inf</span></span>     | <span data-ttu-id="1c800-143">src1</span><span class="sxs-lookup"><span data-stu-id="1c800-143">src1</span></span>         | <span data-ttu-id="1c800-144">+inf</span><span class="sxs-lookup"><span data-stu-id="1c800-144">+inf</span></span>     | <span data-ttu-id="1c800-145">+inf</span><span class="sxs-lookup"><span data-stu-id="1c800-145">+inf</span></span>    |
| <span data-ttu-id="1c800-146">**NaN**</span><span class="sxs-lookup"><span data-stu-id="1c800-146">**NaN**</span></span>            | <span data-ttu-id="1c800-147">-inf</span><span class="sxs-lookup"><span data-stu-id="1c800-147">-inf</span></span>     | <span data-ttu-id="1c800-148">src1</span><span class="sxs-lookup"><span data-stu-id="1c800-148">src1</span></span>         | <span data-ttu-id="1c800-149">+inf</span><span class="sxs-lookup"><span data-stu-id="1c800-149">+inf</span></span>     | <span data-ttu-id="1c800-150">NaN</span><span class="sxs-lookup"><span data-stu-id="1c800-150">NaN</span></span>     |



 

<span data-ttu-id="1c800-151">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="1c800-151">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1c800-152">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="1c800-152">Vertex Shader</span></span> | <span data-ttu-id="1c800-153">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="1c800-153">Geometry Shader</span></span> | <span data-ttu-id="1c800-154">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="1c800-154">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1c800-155">x</span><span class="sxs-lookup"><span data-stu-id="1c800-155">x</span></span>             | <span data-ttu-id="1c800-156">x</span><span class="sxs-lookup"><span data-stu-id="1c800-156">x</span></span>               | <span data-ttu-id="1c800-157">x</span><span class="sxs-lookup"><span data-stu-id="1c800-157">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1c800-158">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="1c800-158">Minimum Shader Model</span></span>

<span data-ttu-id="1c800-159">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1c800-159">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1c800-160">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="1c800-160">Shader Model</span></span>                                              | <span data-ttu-id="1c800-161">Suportado</span><span class="sxs-lookup"><span data-stu-id="1c800-161">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1c800-162">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="1c800-162">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1c800-163">sim</span><span class="sxs-lookup"><span data-stu-id="1c800-163">yes</span></span>       |
| [<span data-ttu-id="1c800-164">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="1c800-164">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1c800-165">sim</span><span class="sxs-lookup"><span data-stu-id="1c800-165">yes</span></span>       |
| [<span data-ttu-id="1c800-166">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="1c800-166">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1c800-167">sim</span><span class="sxs-lookup"><span data-stu-id="1c800-167">yes</span></span>       |
| [<span data-ttu-id="1c800-168">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c800-168">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1c800-169">não</span><span class="sxs-lookup"><span data-stu-id="1c800-169">no</span></span>        |
| [<span data-ttu-id="1c800-170">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c800-170">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1c800-171">não</span><span class="sxs-lookup"><span data-stu-id="1c800-171">no</span></span>        |
| [<span data-ttu-id="1c800-172">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c800-172">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1c800-173">não</span><span class="sxs-lookup"><span data-stu-id="1c800-173">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1c800-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c800-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c800-175">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c800-175">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





