---
title: exp (sm4-ASM)
description: 2exponent por componente.
ms.assetid: 12EB865A-BF71-4B4B-854F-9DA056B18AE0
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 774be1230bdb02a6179ea5662ca2237c2cefc200
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006866"
---
# <a name="exp-sm4---asm"></a><span data-ttu-id="2b9e0-103">exp (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2b9e0-103">exp (sm4 - asm)</span></span>

<span data-ttu-id="2b9e0-104">2exponent por componente.</span><span class="sxs-lookup"><span data-stu-id="2b9e0-104">Component-wise 2exponent.</span></span>



| <span data-ttu-id="2b9e0-105">exp \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="2b9e0-105">exp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="2b9e0-106">Item</span><span class="sxs-lookup"><span data-stu-id="2b9e0-106">Item</span></span>                                                            | <span data-ttu-id="2b9e0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b9e0-107">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="2b9e0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2b9e0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2b9e0-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="2b9e0-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="2b9e0-110">*dest* = 2 *src0*</span><span class="sxs-lookup"><span data-stu-id="2b9e0-110">*dest* = 2 *src0*</span></span><br/> |
| <span data-ttu-id="2b9e0-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2b9e0-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2b9e0-112">\[no \] expoente.</span><span class="sxs-lookup"><span data-stu-id="2b9e0-112">\[in\] The exponent.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="2b9e0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b9e0-113">Remarks</span></span>

<span data-ttu-id="2b9e0-114">Essa instrução segue a teoria do limite.</span><span class="sxs-lookup"><span data-stu-id="2b9e0-114">This instruction follows limit theory.</span></span> <span data-ttu-id="2b9e0-115">O erro relativo máximo é 2-21.</span><span class="sxs-lookup"><span data-stu-id="2b9e0-115">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="2b9e0-116">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="2b9e0-116">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="2b9e0-117">Nesta tabela, F significa um número real finito.</span><span class="sxs-lookup"><span data-stu-id="2b9e0-117">In this table F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="2b9e0-118">**src**</span><span class="sxs-lookup"><span data-stu-id="2b9e0-118">**src**</span></span>  | <span data-ttu-id="2b9e0-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="2b9e0-119">**-inf**</span></span> | <span data-ttu-id="2b9e0-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="2b9e0-120">**-F**</span></span> | <span data-ttu-id="2b9e0-121">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="2b9e0-121">**-denorm**</span></span> | <span data-ttu-id="2b9e0-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="2b9e0-122">**-0**</span></span> | <span data-ttu-id="2b9e0-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="2b9e0-123">**+0**</span></span> | <span data-ttu-id="2b9e0-124">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="2b9e0-124">**+denorm**</span></span> | <span data-ttu-id="2b9e0-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="2b9e0-125">**+F**</span></span> | <span data-ttu-id="2b9e0-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="2b9e0-126">**+inf**</span></span> | <span data-ttu-id="2b9e0-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="2b9e0-127">**NaN**</span></span> |
| <span data-ttu-id="2b9e0-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="2b9e0-128">**dest**</span></span> | <span data-ttu-id="2b9e0-129">0</span><span class="sxs-lookup"><span data-stu-id="2b9e0-129">0</span></span>        | <span data-ttu-id="2b9e0-130">+ F</span><span class="sxs-lookup"><span data-stu-id="2b9e0-130">+F</span></span>     | <span data-ttu-id="2b9e0-131">1</span><span class="sxs-lookup"><span data-stu-id="2b9e0-131">1</span></span>           | <span data-ttu-id="2b9e0-132">1</span><span class="sxs-lookup"><span data-stu-id="2b9e0-132">1</span></span>      | <span data-ttu-id="2b9e0-133">1</span><span class="sxs-lookup"><span data-stu-id="2b9e0-133">1</span></span>      | <span data-ttu-id="2b9e0-134">1</span><span class="sxs-lookup"><span data-stu-id="2b9e0-134">1</span></span>           | <span data-ttu-id="2b9e0-135">+ F</span><span class="sxs-lookup"><span data-stu-id="2b9e0-135">+F</span></span>     | <span data-ttu-id="2b9e0-136">+inf</span><span class="sxs-lookup"><span data-stu-id="2b9e0-136">+inf</span></span>     | <span data-ttu-id="2b9e0-137">NaN</span><span class="sxs-lookup"><span data-stu-id="2b9e0-137">NaN</span></span>     |



 

<span data-ttu-id="2b9e0-138">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="2b9e0-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2b9e0-139">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="2b9e0-139">Vertex Shader</span></span> | <span data-ttu-id="2b9e0-140">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="2b9e0-140">Geometry Shader</span></span> | <span data-ttu-id="2b9e0-141">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="2b9e0-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2b9e0-142">x</span><span class="sxs-lookup"><span data-stu-id="2b9e0-142">x</span></span>             | <span data-ttu-id="2b9e0-143">x</span><span class="sxs-lookup"><span data-stu-id="2b9e0-143">x</span></span>               | <span data-ttu-id="2b9e0-144">x</span><span class="sxs-lookup"><span data-stu-id="2b9e0-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2b9e0-145">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="2b9e0-145">Minimum Shader Model</span></span>

<span data-ttu-id="2b9e0-146">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2b9e0-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2b9e0-147">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="2b9e0-147">Shader Model</span></span>                                              | <span data-ttu-id="2b9e0-148">Com suporte</span><span class="sxs-lookup"><span data-stu-id="2b9e0-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2b9e0-149">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2b9e0-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2b9e0-150">sim</span><span class="sxs-lookup"><span data-stu-id="2b9e0-150">yes</span></span>       |
| [<span data-ttu-id="2b9e0-151">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="2b9e0-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2b9e0-152">sim</span><span class="sxs-lookup"><span data-stu-id="2b9e0-152">yes</span></span>       |
| [<span data-ttu-id="2b9e0-153">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="2b9e0-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2b9e0-154">sim</span><span class="sxs-lookup"><span data-stu-id="2b9e0-154">yes</span></span>       |
| [<span data-ttu-id="2b9e0-155">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b9e0-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2b9e0-156">não</span><span class="sxs-lookup"><span data-stu-id="2b9e0-156">no</span></span>        |
| [<span data-ttu-id="2b9e0-157">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b9e0-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2b9e0-158">não</span><span class="sxs-lookup"><span data-stu-id="2b9e0-158">no</span></span>        |
| [<span data-ttu-id="2b9e0-159">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b9e0-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2b9e0-160">não</span><span class="sxs-lookup"><span data-stu-id="2b9e0-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2b9e0-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b9e0-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b9e0-162">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b9e0-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





