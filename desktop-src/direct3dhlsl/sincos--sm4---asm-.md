---
title: Sincos (sm4-ASM)
description: Meio do componente (teta) e cos (teta) para teta em radianos.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2dd8fc3b011758f071cdcd273e34eb8a7f6421f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988561"
---
# <a name="sincos-sm4---asm"></a><span data-ttu-id="8f6a4-103">Sincos (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8f6a4-103">sincos (sm4 - asm)</span></span>

<span data-ttu-id="8f6a4-104">Meio do componente (teta) e cos (teta) para teta em radianos.</span><span class="sxs-lookup"><span data-stu-id="8f6a4-104">Component-wise sin(theta) and cos(theta) for theta in radians.</span></span>



| <span data-ttu-id="8f6a4-105">Sincos \[ \_ SAT \] destSIN \[ . Mask \] , destCOS \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="8f6a4-105">sincos\[\_sat\] destSIN\[.mask\], destCOS\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------------|



 



| <span data-ttu-id="8f6a4-106">Item</span><span class="sxs-lookup"><span data-stu-id="8f6a4-106">Item</span></span>                                                                                               | <span data-ttu-id="8f6a4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f6a4-107">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="8f6a4-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span><span class="sxs-lookup"><span data-stu-id="8f6a4-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span></span><br/> | <span data-ttu-id="8f6a4-109">\[no \] endereço do sin (*src0*), calculado por componente.</span><span class="sxs-lookup"><span data-stu-id="8f6a4-109">\[in\] The address of sin(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="8f6a4-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span><span class="sxs-lookup"><span data-stu-id="8f6a4-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span></span><br/> | <span data-ttu-id="8f6a4-111">\[no \] endereço de cos (*src0*), calculado por componente.</span><span class="sxs-lookup"><span data-stu-id="8f6a4-111">\[in\] The address of cos(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="8f6a4-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="8f6a4-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                    | <span data-ttu-id="8f6a4-113">\[nos \] componentes para os quais computar Sin e cos.</span><span class="sxs-lookup"><span data-stu-id="8f6a4-113">\[in\] The components for which to compute sin and cos.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="8f6a4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f6a4-114">Remarks</span></span>

<span data-ttu-id="8f6a4-115">Se o resultado não for necessário, você poderá especificar *destSIN* e *destCOS* como NULL em vez de especificar um registro.</span><span class="sxs-lookup"><span data-stu-id="8f6a4-115">If the result is not needed, you can specify *destSIN* and *destCOS* as NULL instead of specifying a register.</span></span>

<span data-ttu-id="8f6a4-116">Os valores de teta podem ser quaisquer valores de ponto flutuante de IEEE 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8f6a4-116">Theta values can be any IEEE 32-bit floating point values.</span></span>

<span data-ttu-id="8f6a4-117">O erro absoluto máximo é 0, 8 no intervalo de-100 \* PI a + 100 \* PI.</span><span class="sxs-lookup"><span data-stu-id="8f6a4-117">The maximum absolute error is 0.0008 in the interval from -100\*Pi to +100\*Pi.</span></span>

<span data-ttu-id="8f6a4-118">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números.</span><span class="sxs-lookup"><span data-stu-id="8f6a4-118">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="8f6a4-119">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="8f6a4-119">F means finite-real number.</span></span>



|             |          |              |             |        |        |             |              |          |         |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| <span data-ttu-id="8f6a4-120">**src**</span><span class="sxs-lookup"><span data-stu-id="8f6a4-120">**src**</span></span>     | <span data-ttu-id="8f6a4-121">**-INF**</span><span class="sxs-lookup"><span data-stu-id="8f6a4-121">**-inf**</span></span> | <span data-ttu-id="8f6a4-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="8f6a4-122">**-F**</span></span>       | <span data-ttu-id="8f6a4-123">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="8f6a4-123">**-denorm**</span></span> | <span data-ttu-id="8f6a4-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="8f6a4-124">**-0**</span></span> | <span data-ttu-id="8f6a4-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="8f6a4-125">**+0**</span></span> | <span data-ttu-id="8f6a4-126">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="8f6a4-126">**+denorm**</span></span> | <span data-ttu-id="8f6a4-127">**+ F**</span><span class="sxs-lookup"><span data-stu-id="8f6a4-127">**+F**</span></span>       | <span data-ttu-id="8f6a4-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="8f6a4-128">**+inf**</span></span> | <span data-ttu-id="8f6a4-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="8f6a4-129">**NaN**</span></span> |
| <span data-ttu-id="8f6a4-130">**destSIN**</span><span class="sxs-lookup"><span data-stu-id="8f6a4-130">**destSIN**</span></span> | <span data-ttu-id="8f6a4-131">NaN</span><span class="sxs-lookup"><span data-stu-id="8f6a4-131">NaN</span></span>      | <span data-ttu-id="8f6a4-132">\[-1 a + 1\]</span><span class="sxs-lookup"><span data-stu-id="8f6a4-132">\[-1 to +1\]</span></span> | <span data-ttu-id="8f6a4-133">-0</span><span class="sxs-lookup"><span data-stu-id="8f6a4-133">-0</span></span>          | <span data-ttu-id="8f6a4-134">-0</span><span class="sxs-lookup"><span data-stu-id="8f6a4-134">-0</span></span>     | <span data-ttu-id="8f6a4-135">+0</span><span class="sxs-lookup"><span data-stu-id="8f6a4-135">+0</span></span>     | <span data-ttu-id="8f6a4-136">+0</span><span class="sxs-lookup"><span data-stu-id="8f6a4-136">+0</span></span>          | <span data-ttu-id="8f6a4-137">\[-1 a + 1\]</span><span class="sxs-lookup"><span data-stu-id="8f6a4-137">\[-1 to +1\]</span></span> | <span data-ttu-id="8f6a4-138">NaN</span><span class="sxs-lookup"><span data-stu-id="8f6a4-138">NaN</span></span>      | <span data-ttu-id="8f6a4-139">NaN</span><span class="sxs-lookup"><span data-stu-id="8f6a4-139">NaN</span></span>     |
| <span data-ttu-id="8f6a4-140">**destCOS**</span><span class="sxs-lookup"><span data-stu-id="8f6a4-140">**destCOS**</span></span> | <span data-ttu-id="8f6a4-141">NaN</span><span class="sxs-lookup"><span data-stu-id="8f6a4-141">NaN</span></span>      | <span data-ttu-id="8f6a4-142">\[-1 a + 1\]</span><span class="sxs-lookup"><span data-stu-id="8f6a4-142">\[-1 to +1\]</span></span> | <span data-ttu-id="8f6a4-143">+1</span><span class="sxs-lookup"><span data-stu-id="8f6a4-143">+1</span></span>          | <span data-ttu-id="8f6a4-144">+1</span><span class="sxs-lookup"><span data-stu-id="8f6a4-144">+1</span></span>     | <span data-ttu-id="8f6a4-145">+1</span><span class="sxs-lookup"><span data-stu-id="8f6a4-145">+1</span></span>     | <span data-ttu-id="8f6a4-146">+1</span><span class="sxs-lookup"><span data-stu-id="8f6a4-146">+1</span></span>          | <span data-ttu-id="8f6a4-147">\[-1 a + 1\]</span><span class="sxs-lookup"><span data-stu-id="8f6a4-147">\[-1 to +1\]</span></span> | <span data-ttu-id="8f6a4-148">NaN</span><span class="sxs-lookup"><span data-stu-id="8f6a4-148">NaN</span></span>      | <span data-ttu-id="8f6a4-149">NaN</span><span class="sxs-lookup"><span data-stu-id="8f6a4-149">NaN</span></span>     |



 

<span data-ttu-id="8f6a4-150">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="8f6a4-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8f6a4-151">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="8f6a4-151">Vertex Shader</span></span> | <span data-ttu-id="8f6a4-152">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="8f6a4-152">Geometry Shader</span></span> | <span data-ttu-id="8f6a4-153">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="8f6a4-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8f6a4-154">x</span><span class="sxs-lookup"><span data-stu-id="8f6a4-154">x</span></span>             | <span data-ttu-id="8f6a4-155">x</span><span class="sxs-lookup"><span data-stu-id="8f6a4-155">x</span></span>               | <span data-ttu-id="8f6a4-156">x</span><span class="sxs-lookup"><span data-stu-id="8f6a4-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8f6a4-157">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="8f6a4-157">Minimum Shader Model</span></span>

<span data-ttu-id="8f6a4-158">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8f6a4-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8f6a4-159">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="8f6a4-159">Shader Model</span></span>                                              | <span data-ttu-id="8f6a4-160">Com suporte</span><span class="sxs-lookup"><span data-stu-id="8f6a4-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8f6a4-161">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8f6a4-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8f6a4-162">sim</span><span class="sxs-lookup"><span data-stu-id="8f6a4-162">yes</span></span>       |
| [<span data-ttu-id="8f6a4-163">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="8f6a4-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8f6a4-164">sim</span><span class="sxs-lookup"><span data-stu-id="8f6a4-164">yes</span></span>       |
| [<span data-ttu-id="8f6a4-165">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="8f6a4-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8f6a4-166">sim</span><span class="sxs-lookup"><span data-stu-id="8f6a4-166">yes</span></span>       |
| [<span data-ttu-id="8f6a4-167">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f6a4-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8f6a4-168">não</span><span class="sxs-lookup"><span data-stu-id="8f6a4-168">no</span></span>        |
| [<span data-ttu-id="8f6a4-169">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f6a4-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8f6a4-170">não</span><span class="sxs-lookup"><span data-stu-id="8f6a4-170">no</span></span>        |
| [<span data-ttu-id="8f6a4-171">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f6a4-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8f6a4-172">não</span><span class="sxs-lookup"><span data-stu-id="8f6a4-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8f6a4-173">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f6a4-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f6a4-174">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f6a4-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





