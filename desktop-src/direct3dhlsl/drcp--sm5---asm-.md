---
title: drcp (SM5-ASM)
description: Computa um recíproco de precisão dupla por componente.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b678f4e8b3464817215de9132298fdde1f6feec
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293577"
---
# <a name="drcp-sm5---asm"></a><span data-ttu-id="de119-103">drcp (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="de119-103">drcp (sm5 - asm)</span></span>

<span data-ttu-id="de119-104">Computa um recíproco de precisão dupla por componente.</span><span class="sxs-lookup"><span data-stu-id="de119-104">Computes a component-wise double-precision reciprocal.</span></span>



| <span data-ttu-id="de119-105">RCP \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="de119-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="de119-106">Item</span><span class="sxs-lookup"><span data-stu-id="de119-106">Item</span></span>                                                            | <span data-ttu-id="de119-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="de119-107">Description</span></span>                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de119-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="de119-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="de119-109">\[no \] endereço dos resultados</span><span class="sxs-lookup"><span data-stu-id="de119-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="de119-110">*dest*  =  **1,0**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="de119-110">*dest* = **1.0** / *src0*.</span></span> <span data-ttu-id="de119-111">O valor do resultado deve ser preciso para o 1,0 ULP</span><span class="sxs-lookup"><span data-stu-id="de119-111">The result value must be accurate to 1.0 ULP</span></span><br/> |
| <span data-ttu-id="de119-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="de119-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="de119-113">\[no \] número para pegar o recíproco de.</span><span class="sxs-lookup"><span data-stu-id="de119-113">\[in\] The number to take the reciprocal of.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="de119-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="de119-114">Remarks</span></span>

<span data-ttu-id="de119-115">A instrução DRCP é emitida pelo compilador HLSL somente quando explicitamente chamado por meio de RCP () intrínseco, quando um Double é usado como o argumento.</span><span class="sxs-lookup"><span data-stu-id="de119-115">The DRCP instruction is emitted by the HLSL compiler only when explicitly called via the rcp() intrinsic, when a double is used as the argument.</span></span> <span data-ttu-id="de119-116">A precisão dessa instrução é necessária para ser 1,0 ULP.</span><span class="sxs-lookup"><span data-stu-id="de119-116">The accuracy of this instruction is required to be 1.0 ULP.</span></span>

<span data-ttu-id="de119-117">Os sombreadores que usam essa instrução serão marcados com um sinalizador de sombreador que fará com que eles não sejam associados, a menos que todas as condições a seguir sejam atendidas.</span><span class="sxs-lookup"><span data-stu-id="de119-117">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="de119-118">O sistema dá suporte ao DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="de119-118">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="de119-119">O sistema inclui um Driver WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="de119-119">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="de119-120">O driver fornece suporte para essa instrução por meio de **Opções de D3D11 de dados de recursos do D3D11 \_ \_ \_ \_ . ExtendedDoublesShaderInstructions** definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="de119-120">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="de119-121">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="de119-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="de119-122">Nesta tabela, F significa um número real finito.</span><span class="sxs-lookup"><span data-stu-id="de119-122">In this table F means finite-real number.</span></span>



|               |          |        |        |        |        |          |         |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| <span data-ttu-id="de119-123">**orig**-></span><span class="sxs-lookup"><span data-stu-id="de119-123">**src**-></span></span>  | <span data-ttu-id="de119-124">**-INF**</span><span class="sxs-lookup"><span data-stu-id="de119-124">**-inf**</span></span> | <span data-ttu-id="de119-125">**-F**</span><span class="sxs-lookup"><span data-stu-id="de119-125">**-F**</span></span> | <span data-ttu-id="de119-126">**-0**</span><span class="sxs-lookup"><span data-stu-id="de119-126">**-0**</span></span> | <span data-ttu-id="de119-127">**+0**</span><span class="sxs-lookup"><span data-stu-id="de119-127">**+0**</span></span> | <span data-ttu-id="de119-128">**+ F**</span><span class="sxs-lookup"><span data-stu-id="de119-128">**+F**</span></span> | <span data-ttu-id="de119-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="de119-129">**+inf**</span></span> | <span data-ttu-id="de119-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="de119-130">**NaN**</span></span> |
| <span data-ttu-id="de119-131">**dest**-></span><span class="sxs-lookup"><span data-stu-id="de119-131">**dest**-></span></span> | <span data-ttu-id="de119-132">-0</span><span class="sxs-lookup"><span data-stu-id="de119-132">-0</span></span>       | <span data-ttu-id="de119-133">-F</span><span class="sxs-lookup"><span data-stu-id="de119-133">-F</span></span>     | <span data-ttu-id="de119-134">-inf</span><span class="sxs-lookup"><span data-stu-id="de119-134">-inf</span></span>   | <span data-ttu-id="de119-135">+inf</span><span class="sxs-lookup"><span data-stu-id="de119-135">+inf</span></span>   | <span data-ttu-id="de119-136">+ F</span><span class="sxs-lookup"><span data-stu-id="de119-136">+F</span></span>     | <span data-ttu-id="de119-137">+0</span><span class="sxs-lookup"><span data-stu-id="de119-137">+0</span></span>       | <span data-ttu-id="de119-138">NaN</span><span class="sxs-lookup"><span data-stu-id="de119-138">NaN</span></span>     |



 

<span data-ttu-id="de119-139">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="de119-139">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="de119-140">Vértice</span><span class="sxs-lookup"><span data-stu-id="de119-140">Vertex</span></span> | <span data-ttu-id="de119-141">Envoltória</span><span class="sxs-lookup"><span data-stu-id="de119-141">Hull</span></span> | <span data-ttu-id="de119-142">Domínio</span><span class="sxs-lookup"><span data-stu-id="de119-142">Domain</span></span> | <span data-ttu-id="de119-143">Geometria</span><span class="sxs-lookup"><span data-stu-id="de119-143">Geometry</span></span> | <span data-ttu-id="de119-144">16x16</span><span class="sxs-lookup"><span data-stu-id="de119-144">Pixel</span></span> | <span data-ttu-id="de119-145">Computação</span><span class="sxs-lookup"><span data-stu-id="de119-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="de119-146">X</span><span class="sxs-lookup"><span data-stu-id="de119-146">X</span></span>      | <span data-ttu-id="de119-147">X</span><span class="sxs-lookup"><span data-stu-id="de119-147">X</span></span>    | <span data-ttu-id="de119-148">X</span><span class="sxs-lookup"><span data-stu-id="de119-148">X</span></span>      | <span data-ttu-id="de119-149">X</span><span class="sxs-lookup"><span data-stu-id="de119-149">X</span></span>        | <span data-ttu-id="de119-150">X</span><span class="sxs-lookup"><span data-stu-id="de119-150">X</span></span>     | <span data-ttu-id="de119-151">X</span><span class="sxs-lookup"><span data-stu-id="de119-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="de119-152">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="de119-152">Minimum Shader Model</span></span>

<span data-ttu-id="de119-153">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="de119-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="de119-154">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="de119-154">Shader Model</span></span>                                              | <span data-ttu-id="de119-155">Com suporte</span><span class="sxs-lookup"><span data-stu-id="de119-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="de119-156">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="de119-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="de119-157">sim</span><span class="sxs-lookup"><span data-stu-id="de119-157">yes</span></span>       |
| [<span data-ttu-id="de119-158">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="de119-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="de119-159">não</span><span class="sxs-lookup"><span data-stu-id="de119-159">no</span></span>        |
| [<span data-ttu-id="de119-160">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="de119-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="de119-161">não</span><span class="sxs-lookup"><span data-stu-id="de119-161">no</span></span>        |
| [<span data-ttu-id="de119-162">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de119-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="de119-163">não</span><span class="sxs-lookup"><span data-stu-id="de119-163">no</span></span>        |
| [<span data-ttu-id="de119-164">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de119-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="de119-165">não</span><span class="sxs-lookup"><span data-stu-id="de119-165">no</span></span>        |
| [<span data-ttu-id="de119-166">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de119-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="de119-167">não</span><span class="sxs-lookup"><span data-stu-id="de119-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="de119-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="de119-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de119-169">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de119-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





