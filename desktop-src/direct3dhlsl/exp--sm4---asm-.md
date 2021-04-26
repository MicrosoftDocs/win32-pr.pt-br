---
title: exp (sm4-ASM)
description: 2exponent por componente.
ms.assetid: 12EB865A-BF71-4B4B-854F-9DA056B18AE0
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b24c74394a5e8ac7a6c945e2c9b63e6f242daa1
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999073"
---
# <a name="exp-sm4---asm"></a><span data-ttu-id="77c00-103">exp (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="77c00-103">exp (sm4 - asm)</span></span>

<span data-ttu-id="77c00-104">2exponent por componente.</span><span class="sxs-lookup"><span data-stu-id="77c00-104">Component-wise 2exponent.</span></span>



| <span data-ttu-id="77c00-105">exp \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="77c00-105">exp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="77c00-106">Item</span><span class="sxs-lookup"><span data-stu-id="77c00-106">Item</span></span>                                                            | <span data-ttu-id="77c00-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="77c00-107">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="77c00-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="77c00-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="77c00-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="77c00-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="77c00-110">*dest* = 2 *src0*</span><span class="sxs-lookup"><span data-stu-id="77c00-110">*dest* = 2 *src0*</span></span><br/> |
| <span data-ttu-id="77c00-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="77c00-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="77c00-112">\[no \] expoente.</span><span class="sxs-lookup"><span data-stu-id="77c00-112">\[in\] The exponent.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="77c00-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="77c00-113">Remarks</span></span>

<span data-ttu-id="77c00-114">Essa instrução segue a teoria do limite.</span><span class="sxs-lookup"><span data-stu-id="77c00-114">This instruction follows limit theory.</span></span> <span data-ttu-id="77c00-115">O erro relativo máximo é 2-21.</span><span class="sxs-lookup"><span data-stu-id="77c00-115">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="77c00-116">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="77c00-116">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="77c00-117">Nesta tabela, F significa um número real finito.</span><span class="sxs-lookup"><span data-stu-id="77c00-117">In this table F means finite-real number.</span></span>



| <span data-ttu-id="77c00-118">**src**</span><span class="sxs-lookup"><span data-stu-id="77c00-118">**src**</span></span>  | <span data-ttu-id="77c00-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="77c00-119">**-inf**</span></span> | <span data-ttu-id="77c00-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="77c00-120">**-F**</span></span> | <span data-ttu-id="77c00-121">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="77c00-121">**-denorm**</span></span> | <span data-ttu-id="77c00-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="77c00-122">**-0**</span></span> | <span data-ttu-id="77c00-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="77c00-123">**+0**</span></span> | <span data-ttu-id="77c00-124">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="77c00-124">**+denorm**</span></span> | <span data-ttu-id="77c00-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="77c00-125">**+F**</span></span> | <span data-ttu-id="77c00-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="77c00-126">**+inf**</span></span> | <span data-ttu-id="77c00-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="77c00-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="77c00-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="77c00-128">**dest**</span></span> | <span data-ttu-id="77c00-129">0</span><span class="sxs-lookup"><span data-stu-id="77c00-129">0</span></span>        | <span data-ttu-id="77c00-130">+ F</span><span class="sxs-lookup"><span data-stu-id="77c00-130">+F</span></span>     | <span data-ttu-id="77c00-131">1</span><span class="sxs-lookup"><span data-stu-id="77c00-131">1</span></span>           | <span data-ttu-id="77c00-132">1</span><span class="sxs-lookup"><span data-stu-id="77c00-132">1</span></span>      | <span data-ttu-id="77c00-133">1</span><span class="sxs-lookup"><span data-stu-id="77c00-133">1</span></span>      | <span data-ttu-id="77c00-134">1</span><span class="sxs-lookup"><span data-stu-id="77c00-134">1</span></span>           | <span data-ttu-id="77c00-135">+ F</span><span class="sxs-lookup"><span data-stu-id="77c00-135">+F</span></span>     | <span data-ttu-id="77c00-136">+inf</span><span class="sxs-lookup"><span data-stu-id="77c00-136">+inf</span></span>     | <span data-ttu-id="77c00-137">NaN</span><span class="sxs-lookup"><span data-stu-id="77c00-137">NaN</span></span>     |



 

<span data-ttu-id="77c00-138">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="77c00-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="77c00-139">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="77c00-139">Vertex Shader</span></span> | <span data-ttu-id="77c00-140">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="77c00-140">Geometry Shader</span></span> | <span data-ttu-id="77c00-141">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="77c00-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="77c00-142">x</span><span class="sxs-lookup"><span data-stu-id="77c00-142">x</span></span>             | <span data-ttu-id="77c00-143">x</span><span class="sxs-lookup"><span data-stu-id="77c00-143">x</span></span>               | <span data-ttu-id="77c00-144">x</span><span class="sxs-lookup"><span data-stu-id="77c00-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="77c00-145">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="77c00-145">Minimum Shader Model</span></span>

<span data-ttu-id="77c00-146">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="77c00-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="77c00-147">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="77c00-147">Shader Model</span></span>                                              | <span data-ttu-id="77c00-148">Suportado</span><span class="sxs-lookup"><span data-stu-id="77c00-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="77c00-149">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="77c00-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="77c00-150">sim</span><span class="sxs-lookup"><span data-stu-id="77c00-150">yes</span></span>       |
| [<span data-ttu-id="77c00-151">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="77c00-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="77c00-152">sim</span><span class="sxs-lookup"><span data-stu-id="77c00-152">yes</span></span>       |
| [<span data-ttu-id="77c00-153">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="77c00-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="77c00-154">sim</span><span class="sxs-lookup"><span data-stu-id="77c00-154">yes</span></span>       |
| [<span data-ttu-id="77c00-155">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="77c00-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="77c00-156">não</span><span class="sxs-lookup"><span data-stu-id="77c00-156">no</span></span>        |
| [<span data-ttu-id="77c00-157">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="77c00-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="77c00-158">não</span><span class="sxs-lookup"><span data-stu-id="77c00-158">no</span></span>        |
| [<span data-ttu-id="77c00-159">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="77c00-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="77c00-160">não</span><span class="sxs-lookup"><span data-stu-id="77c00-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="77c00-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77c00-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77c00-162">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="77c00-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





