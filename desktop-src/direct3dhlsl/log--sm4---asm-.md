---
title: log (sm4-ASM)
description: Base do log baseado em componente 2.
ms.assetid: 6D28864A-C2BA-44AF-9E78-7C2B34F5E462
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf99949e278ca302543437da346188b690789604
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006898"
---
# <a name="log-sm4---asm"></a><span data-ttu-id="ac30a-103">log (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ac30a-103">log (sm4 - asm)</span></span>

<span data-ttu-id="ac30a-104">Base do log baseado em componente 2.</span><span class="sxs-lookup"><span data-stu-id="ac30a-104">Component-wise log base 2.</span></span>



| <span data-ttu-id="ac30a-105">log \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle</span><span class="sxs-lookup"><span data-stu-id="ac30a-105">log\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle</span></span> |
|----------------------------------------------------------|



 



| <span data-ttu-id="ac30a-106">Item</span><span class="sxs-lookup"><span data-stu-id="ac30a-106">Item</span></span>                                                            | <span data-ttu-id="ac30a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac30a-107">Description</span></span>                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac30a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ac30a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ac30a-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="ac30a-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="ac30a-110">dest = log2 (src0)</span><span class="sxs-lookup"><span data-stu-id="ac30a-110">dest = log2(src0)</span></span><br/> |
| <span data-ttu-id="ac30a-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ac30a-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ac30a-112">\[no \] valor da operação.</span><span class="sxs-lookup"><span data-stu-id="ac30a-112">\[in\] The value for the operation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="ac30a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac30a-113">Remarks</span></span>

### <a name="restrictions"></a><span data-ttu-id="ac30a-114">Restrições</span><span class="sxs-lookup"><span data-stu-id="ac30a-114">Restrictions</span></span>

-   <span data-ttu-id="ac30a-115">Segue a teoria do limite.</span><span class="sxs-lookup"><span data-stu-id="ac30a-115">Follows limit theory.</span></span>
-   <span data-ttu-id="ac30a-116">Tolerância a erros: se *src0* for \[ 0,5.. 2 \] , o erro Absolue não deverá ser maior que 2-21.</span><span class="sxs-lookup"><span data-stu-id="ac30a-116">Error tolerance: If *src0* is \[0.5..2\], absolue error must be no more than 2-21.</span></span> <span data-ttu-id="ac30a-117">Se *src0* for (0.. 0,5) ou (2.. + inf \] , o erro relativo não deverá ser maior que 2-21.</span><span class="sxs-lookup"><span data-stu-id="ac30a-117">If *src0* is (0..0.5) or (2..+INF\], relative error must be no more than 2-21.</span></span>

<span data-ttu-id="ac30a-118">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="ac30a-118">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="ac30a-119">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="ac30a-119">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="ac30a-120">**src**</span><span class="sxs-lookup"><span data-stu-id="ac30a-120">**src**</span></span>  | <span data-ttu-id="ac30a-121">**-INF**</span><span class="sxs-lookup"><span data-stu-id="ac30a-121">**-inf**</span></span> | <span data-ttu-id="ac30a-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="ac30a-122">**-F**</span></span> | <span data-ttu-id="ac30a-123">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="ac30a-123">**-denorm**</span></span> | <span data-ttu-id="ac30a-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="ac30a-124">**-0**</span></span> | <span data-ttu-id="ac30a-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="ac30a-125">**+0**</span></span> | <span data-ttu-id="ac30a-126">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="ac30a-126">**+denorm**</span></span> | <span data-ttu-id="ac30a-127">**+ F**</span><span class="sxs-lookup"><span data-stu-id="ac30a-127">**+F**</span></span> | <span data-ttu-id="ac30a-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="ac30a-128">**+inf**</span></span> | <span data-ttu-id="ac30a-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="ac30a-129">**NaN**</span></span> |
| <span data-ttu-id="ac30a-130">**dest**</span><span class="sxs-lookup"><span data-stu-id="ac30a-130">**dest**</span></span> | <span data-ttu-id="ac30a-131">NaN</span><span class="sxs-lookup"><span data-stu-id="ac30a-131">NaN</span></span>      | <span data-ttu-id="ac30a-132">NaN</span><span class="sxs-lookup"><span data-stu-id="ac30a-132">NaN</span></span>    | <span data-ttu-id="ac30a-133">-inf</span><span class="sxs-lookup"><span data-stu-id="ac30a-133">-inf</span></span>        | <span data-ttu-id="ac30a-134">-inf</span><span class="sxs-lookup"><span data-stu-id="ac30a-134">-inf</span></span>   | <span data-ttu-id="ac30a-135">-inf</span><span class="sxs-lookup"><span data-stu-id="ac30a-135">-inf</span></span>   | <span data-ttu-id="ac30a-136">-inf</span><span class="sxs-lookup"><span data-stu-id="ac30a-136">-inf</span></span>        | <span data-ttu-id="ac30a-137">F</span><span class="sxs-lookup"><span data-stu-id="ac30a-137">F</span></span>      | <span data-ttu-id="ac30a-138">+inf</span><span class="sxs-lookup"><span data-stu-id="ac30a-138">+inf</span></span>     | <span data-ttu-id="ac30a-139">NaN</span><span class="sxs-lookup"><span data-stu-id="ac30a-139">NaN</span></span>     |



 

<span data-ttu-id="ac30a-140">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="ac30a-140">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ac30a-141">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="ac30a-141">Vertex Shader</span></span> | <span data-ttu-id="ac30a-142">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="ac30a-142">Geometry Shader</span></span> | <span data-ttu-id="ac30a-143">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="ac30a-143">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ac30a-144">x</span><span class="sxs-lookup"><span data-stu-id="ac30a-144">x</span></span>             | <span data-ttu-id="ac30a-145">x</span><span class="sxs-lookup"><span data-stu-id="ac30a-145">x</span></span>               | <span data-ttu-id="ac30a-146">x</span><span class="sxs-lookup"><span data-stu-id="ac30a-146">x</span></span>            |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="ac30a-147">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="ac30a-147">Minimum Shader Model</span></span>

<span data-ttu-id="ac30a-148">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ac30a-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ac30a-149">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="ac30a-149">Shader Model</span></span>                                              | <span data-ttu-id="ac30a-150">Com suporte</span><span class="sxs-lookup"><span data-stu-id="ac30a-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ac30a-151">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ac30a-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ac30a-152">sim</span><span class="sxs-lookup"><span data-stu-id="ac30a-152">yes</span></span>       |
| [<span data-ttu-id="ac30a-153">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="ac30a-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ac30a-154">sim</span><span class="sxs-lookup"><span data-stu-id="ac30a-154">yes</span></span>       |
| [<span data-ttu-id="ac30a-155">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ac30a-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ac30a-156">sim</span><span class="sxs-lookup"><span data-stu-id="ac30a-156">yes</span></span>       |
| [<span data-ttu-id="ac30a-157">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac30a-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ac30a-158">não</span><span class="sxs-lookup"><span data-stu-id="ac30a-158">no</span></span>        |
| [<span data-ttu-id="ac30a-159">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac30a-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ac30a-160">não</span><span class="sxs-lookup"><span data-stu-id="ac30a-160">no</span></span>        |
| [<span data-ttu-id="ac30a-161">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac30a-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ac30a-162">não</span><span class="sxs-lookup"><span data-stu-id="ac30a-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ac30a-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac30a-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac30a-164">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac30a-164">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





