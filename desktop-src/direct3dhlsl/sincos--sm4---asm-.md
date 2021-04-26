---
title: Sincos (sm4-ASM)
description: Meio do componente (teta) e cos (teta) para teta em radianos.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c03118ff9a1fc2d958eaa6eb1a550a6dbf672a2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997013"
---
# <a name="sincos-sm4---asm"></a><span data-ttu-id="8f0d8-103">Sincos (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8f0d8-103">sincos (sm4 - asm)</span></span>

<span data-ttu-id="8f0d8-104">Meio do componente (teta) e cos (teta) para teta em radianos.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-104">Component-wise sin(theta) and cos(theta) for theta in radians.</span></span>



| <span data-ttu-id="8f0d8-105">Sincos \[ \_ SAT \] destSIN \[ . Mask \] , destCOS \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="8f0d8-105">sincos\[\_sat\] destSIN\[.mask\], destCOS\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------------|



 



| <span data-ttu-id="8f0d8-106">Item</span><span class="sxs-lookup"><span data-stu-id="8f0d8-106">Item</span></span>                                                                                               | <span data-ttu-id="8f0d8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f0d8-107">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="8f0d8-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span><span class="sxs-lookup"><span data-stu-id="8f0d8-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span></span><br/> | <span data-ttu-id="8f0d8-109">\[no \] endereço do sin (*src0*), calculado por componente.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-109">\[in\] The address of sin(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="8f0d8-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span><span class="sxs-lookup"><span data-stu-id="8f0d8-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span></span><br/> | <span data-ttu-id="8f0d8-111">\[no \] endereço de cos (*src0*), calculado por componente.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-111">\[in\] The address of cos(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="8f0d8-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="8f0d8-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                    | <span data-ttu-id="8f0d8-113">\[nos \] componentes para os quais computar Sin e cos.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-113">\[in\] The components for which to compute sin and cos.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="8f0d8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f0d8-114">Remarks</span></span>

<span data-ttu-id="8f0d8-115">Se o resultado não for necessário, você poderá especificar *destSIN* e *destCOS* como NULL em vez de especificar um registro.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-115">If the result is not needed, you can specify *destSIN* and *destCOS* as NULL instead of specifying a register.</span></span>

<span data-ttu-id="8f0d8-116">Os valores de teta podem ser quaisquer valores de ponto flutuante de IEEE 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-116">Theta values can be any IEEE 32-bit floating point values.</span></span>

<span data-ttu-id="8f0d8-117">O erro absoluto máximo é 0, 8 no intervalo de-100 \* PI a + 100 \* PI.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-117">The maximum absolute error is 0.0008 in the interval from -100\*Pi to +100\*Pi.</span></span>

<span data-ttu-id="8f0d8-118">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-118">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="8f0d8-119">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-119">F means finite-real number.</span></span>



| <span data-ttu-id="8f0d8-120">**src**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-120">**src**</span></span>     | <span data-ttu-id="8f0d8-121">**-INF**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-121">**-inf**</span></span> | <span data-ttu-id="8f0d8-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-122">**-F**</span></span>       | <span data-ttu-id="8f0d8-123">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-123">**-denorm**</span></span> | <span data-ttu-id="8f0d8-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-124">**-0**</span></span> | <span data-ttu-id="8f0d8-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-125">**+0**</span></span> | <span data-ttu-id="8f0d8-126">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-126">**+denorm**</span></span> | <span data-ttu-id="8f0d8-127">**+ F**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-127">**+F**</span></span>       | <span data-ttu-id="8f0d8-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-128">**+inf**</span></span> | <span data-ttu-id="8f0d8-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-129">**NaN**</span></span> |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| <span data-ttu-id="8f0d8-130">**destSIN**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-130">**destSIN**</span></span> | <span data-ttu-id="8f0d8-131">NaN</span><span class="sxs-lookup"><span data-stu-id="8f0d8-131">NaN</span></span>      | <span data-ttu-id="8f0d8-132">\[-1 a + 1\]</span><span class="sxs-lookup"><span data-stu-id="8f0d8-132">\[-1 to +1\]</span></span> | <span data-ttu-id="8f0d8-133">-0</span><span class="sxs-lookup"><span data-stu-id="8f0d8-133">-0</span></span>          | <span data-ttu-id="8f0d8-134">-0</span><span class="sxs-lookup"><span data-stu-id="8f0d8-134">-0</span></span>     | <span data-ttu-id="8f0d8-135">+0</span><span class="sxs-lookup"><span data-stu-id="8f0d8-135">+0</span></span>     | <span data-ttu-id="8f0d8-136">+0</span><span class="sxs-lookup"><span data-stu-id="8f0d8-136">+0</span></span>          | <span data-ttu-id="8f0d8-137">\[-1 a + 1\]</span><span class="sxs-lookup"><span data-stu-id="8f0d8-137">\[-1 to +1\]</span></span> | <span data-ttu-id="8f0d8-138">NaN</span><span class="sxs-lookup"><span data-stu-id="8f0d8-138">NaN</span></span>      | <span data-ttu-id="8f0d8-139">NaN</span><span class="sxs-lookup"><span data-stu-id="8f0d8-139">NaN</span></span>     |
| <span data-ttu-id="8f0d8-140">**destCOS**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-140">**destCOS**</span></span> | <span data-ttu-id="8f0d8-141">NaN</span><span class="sxs-lookup"><span data-stu-id="8f0d8-141">NaN</span></span>      | <span data-ttu-id="8f0d8-142">\[-1 a + 1\]</span><span class="sxs-lookup"><span data-stu-id="8f0d8-142">\[-1 to +1\]</span></span> | <span data-ttu-id="8f0d8-143">+1</span><span class="sxs-lookup"><span data-stu-id="8f0d8-143">+1</span></span>          | <span data-ttu-id="8f0d8-144">+1</span><span class="sxs-lookup"><span data-stu-id="8f0d8-144">+1</span></span>     | <span data-ttu-id="8f0d8-145">+1</span><span class="sxs-lookup"><span data-stu-id="8f0d8-145">+1</span></span>     | <span data-ttu-id="8f0d8-146">+1</span><span class="sxs-lookup"><span data-stu-id="8f0d8-146">+1</span></span>          | <span data-ttu-id="8f0d8-147">\[-1 a + 1\]</span><span class="sxs-lookup"><span data-stu-id="8f0d8-147">\[-1 to +1\]</span></span> | <span data-ttu-id="8f0d8-148">NaN</span><span class="sxs-lookup"><span data-stu-id="8f0d8-148">NaN</span></span>      | <span data-ttu-id="8f0d8-149">NaN</span><span class="sxs-lookup"><span data-stu-id="8f0d8-149">NaN</span></span>     |



 

<span data-ttu-id="8f0d8-150">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="8f0d8-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8f0d8-151">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="8f0d8-151">Vertex Shader</span></span> | <span data-ttu-id="8f0d8-152">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="8f0d8-152">Geometry Shader</span></span> | <span data-ttu-id="8f0d8-153">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="8f0d8-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8f0d8-154">x</span><span class="sxs-lookup"><span data-stu-id="8f0d8-154">x</span></span>             | <span data-ttu-id="8f0d8-155">x</span><span class="sxs-lookup"><span data-stu-id="8f0d8-155">x</span></span>               | <span data-ttu-id="8f0d8-156">x</span><span class="sxs-lookup"><span data-stu-id="8f0d8-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8f0d8-157">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="8f0d8-157">Minimum Shader Model</span></span>

<span data-ttu-id="8f0d8-158">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8f0d8-159">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="8f0d8-159">Shader Model</span></span>                                              | <span data-ttu-id="8f0d8-160">Suportado</span><span class="sxs-lookup"><span data-stu-id="8f0d8-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8f0d8-161">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8f0d8-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8f0d8-162">sim</span><span class="sxs-lookup"><span data-stu-id="8f0d8-162">yes</span></span>       |
| [<span data-ttu-id="8f0d8-163">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="8f0d8-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8f0d8-164">sim</span><span class="sxs-lookup"><span data-stu-id="8f0d8-164">yes</span></span>       |
| [<span data-ttu-id="8f0d8-165">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="8f0d8-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8f0d8-166">sim</span><span class="sxs-lookup"><span data-stu-id="8f0d8-166">yes</span></span>       |
| [<span data-ttu-id="8f0d8-167">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f0d8-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8f0d8-168">não</span><span class="sxs-lookup"><span data-stu-id="8f0d8-168">no</span></span>        |
| [<span data-ttu-id="8f0d8-169">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f0d8-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8f0d8-170">não</span><span class="sxs-lookup"><span data-stu-id="8f0d8-170">no</span></span>        |
| [<span data-ttu-id="8f0d8-171">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f0d8-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8f0d8-172">não</span><span class="sxs-lookup"><span data-stu-id="8f0d8-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8f0d8-173">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f0d8-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f0d8-174">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f0d8-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





