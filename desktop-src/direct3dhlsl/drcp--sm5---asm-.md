---
title: drcp (SM5-ASM)
description: Computa um recíproco de precisão dupla por componente.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 770159f5007b08f5482ba8b58634b44e7f3e6ef0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998333"
---
# <a name="drcp-sm5---asm"></a><span data-ttu-id="10b4f-103">drcp (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="10b4f-103">drcp (sm5 - asm)</span></span>

<span data-ttu-id="10b4f-104">Computa um recíproco de precisão dupla por componente.</span><span class="sxs-lookup"><span data-stu-id="10b4f-104">Computes a component-wise double-precision reciprocal.</span></span>



| <span data-ttu-id="10b4f-105">RCP \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="10b4f-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="10b4f-106">Item</span><span class="sxs-lookup"><span data-stu-id="10b4f-106">Item</span></span>                                                            | <span data-ttu-id="10b4f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="10b4f-107">Description</span></span>                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10b4f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="10b4f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="10b4f-109">\[no \] endereço dos resultados</span><span class="sxs-lookup"><span data-stu-id="10b4f-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="10b4f-110">*dest*  =  **1,0**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="10b4f-110">*dest* = **1.0** / *src0*.</span></span> <span data-ttu-id="10b4f-111">O valor do resultado deve ser preciso para o 1,0 ULP</span><span class="sxs-lookup"><span data-stu-id="10b4f-111">The result value must be accurate to 1.0 ULP</span></span><br/> |
| <span data-ttu-id="10b4f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="10b4f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="10b4f-113">\[no \] número para pegar o recíproco de.</span><span class="sxs-lookup"><span data-stu-id="10b4f-113">\[in\] The number to take the reciprocal of.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="10b4f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="10b4f-114">Remarks</span></span>

<span data-ttu-id="10b4f-115">A instrução DRCP é emitida pelo compilador HLSL somente quando explicitamente chamado por meio de RCP () intrínseco, quando um Double é usado como o argumento.</span><span class="sxs-lookup"><span data-stu-id="10b4f-115">The DRCP instruction is emitted by the HLSL compiler only when explicitly called via the rcp() intrinsic, when a double is used as the argument.</span></span> <span data-ttu-id="10b4f-116">A precisão dessa instrução é necessária para ser 1,0 ULP.</span><span class="sxs-lookup"><span data-stu-id="10b4f-116">The accuracy of this instruction is required to be 1.0 ULP.</span></span>

<span data-ttu-id="10b4f-117">Os sombreadores que usam essa instrução serão marcados com um sinalizador de sombreador que fará com que eles não sejam associados, a menos que todas as condições a seguir sejam atendidas.</span><span class="sxs-lookup"><span data-stu-id="10b4f-117">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="10b4f-118">O sistema dá suporte ao DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="10b4f-118">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="10b4f-119">O sistema inclui um Driver WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="10b4f-119">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="10b4f-120">O driver fornece suporte para essa instrução por meio de **Opções de D3D11 de dados de recursos do D3D11 \_ \_ \_ \_ . ExtendedDoublesShaderInstructions** definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="10b4f-120">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="10b4f-121">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="10b4f-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="10b4f-122">Nesta tabela, F significa um número real finito.</span><span class="sxs-lookup"><span data-stu-id="10b4f-122">In this table F means finite-real number.</span></span>



| <span data-ttu-id="10b4f-123">**orig**-></span><span class="sxs-lookup"><span data-stu-id="10b4f-123">**src**-></span></span>  | <span data-ttu-id="10b4f-124">**-INF**</span><span class="sxs-lookup"><span data-stu-id="10b4f-124">**-inf**</span></span> | <span data-ttu-id="10b4f-125">**-F**</span><span class="sxs-lookup"><span data-stu-id="10b4f-125">**-F**</span></span> | <span data-ttu-id="10b4f-126">**-0**</span><span class="sxs-lookup"><span data-stu-id="10b4f-126">**-0**</span></span> | <span data-ttu-id="10b4f-127">**+0**</span><span class="sxs-lookup"><span data-stu-id="10b4f-127">**+0**</span></span> | <span data-ttu-id="10b4f-128">**+ F**</span><span class="sxs-lookup"><span data-stu-id="10b4f-128">**+F**</span></span> | <span data-ttu-id="10b4f-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="10b4f-129">**+inf**</span></span> | <span data-ttu-id="10b4f-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="10b4f-130">**NaN**</span></span> |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| <span data-ttu-id="10b4f-131">**dest**-></span><span class="sxs-lookup"><span data-stu-id="10b4f-131">**dest**-></span></span> | <span data-ttu-id="10b4f-132">-0</span><span class="sxs-lookup"><span data-stu-id="10b4f-132">-0</span></span>       | <span data-ttu-id="10b4f-133">-F</span><span class="sxs-lookup"><span data-stu-id="10b4f-133">-F</span></span>     | <span data-ttu-id="10b4f-134">-inf</span><span class="sxs-lookup"><span data-stu-id="10b4f-134">-inf</span></span>   | <span data-ttu-id="10b4f-135">+inf</span><span class="sxs-lookup"><span data-stu-id="10b4f-135">+inf</span></span>   | <span data-ttu-id="10b4f-136">+ F</span><span class="sxs-lookup"><span data-stu-id="10b4f-136">+F</span></span>     | <span data-ttu-id="10b4f-137">+0</span><span class="sxs-lookup"><span data-stu-id="10b4f-137">+0</span></span>       | <span data-ttu-id="10b4f-138">NaN</span><span class="sxs-lookup"><span data-stu-id="10b4f-138">NaN</span></span>     |



 

<span data-ttu-id="10b4f-139">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="10b4f-139">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="10b4f-140">Vértice</span><span class="sxs-lookup"><span data-stu-id="10b4f-140">Vertex</span></span> | <span data-ttu-id="10b4f-141">Envoltória</span><span class="sxs-lookup"><span data-stu-id="10b4f-141">Hull</span></span> | <span data-ttu-id="10b4f-142">Domain</span><span class="sxs-lookup"><span data-stu-id="10b4f-142">Domain</span></span> | <span data-ttu-id="10b4f-143">Geometria</span><span class="sxs-lookup"><span data-stu-id="10b4f-143">Geometry</span></span> | <span data-ttu-id="10b4f-144">16x16</span><span class="sxs-lookup"><span data-stu-id="10b4f-144">Pixel</span></span> | <span data-ttu-id="10b4f-145">Computação</span><span class="sxs-lookup"><span data-stu-id="10b4f-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="10b4f-146">X</span><span class="sxs-lookup"><span data-stu-id="10b4f-146">X</span></span>      | <span data-ttu-id="10b4f-147">X</span><span class="sxs-lookup"><span data-stu-id="10b4f-147">X</span></span>    | <span data-ttu-id="10b4f-148">X</span><span class="sxs-lookup"><span data-stu-id="10b4f-148">X</span></span>      | <span data-ttu-id="10b4f-149">X</span><span class="sxs-lookup"><span data-stu-id="10b4f-149">X</span></span>        | <span data-ttu-id="10b4f-150">X</span><span class="sxs-lookup"><span data-stu-id="10b4f-150">X</span></span>     | <span data-ttu-id="10b4f-151">X</span><span class="sxs-lookup"><span data-stu-id="10b4f-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="10b4f-152">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="10b4f-152">Minimum Shader Model</span></span>

<span data-ttu-id="10b4f-153">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="10b4f-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="10b4f-154">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="10b4f-154">Shader Model</span></span>                                              | <span data-ttu-id="10b4f-155">Suportado</span><span class="sxs-lookup"><span data-stu-id="10b4f-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="10b4f-156">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="10b4f-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="10b4f-157">sim</span><span class="sxs-lookup"><span data-stu-id="10b4f-157">yes</span></span>       |
| [<span data-ttu-id="10b4f-158">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="10b4f-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="10b4f-159">não</span><span class="sxs-lookup"><span data-stu-id="10b4f-159">no</span></span>        |
| [<span data-ttu-id="10b4f-160">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="10b4f-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="10b4f-161">não</span><span class="sxs-lookup"><span data-stu-id="10b4f-161">no</span></span>        |
| [<span data-ttu-id="10b4f-162">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="10b4f-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="10b4f-163">não</span><span class="sxs-lookup"><span data-stu-id="10b4f-163">no</span></span>        |
| [<span data-ttu-id="10b4f-164">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="10b4f-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="10b4f-165">não</span><span class="sxs-lookup"><span data-stu-id="10b4f-165">no</span></span>        |
| [<span data-ttu-id="10b4f-166">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="10b4f-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="10b4f-167">não</span><span class="sxs-lookup"><span data-stu-id="10b4f-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="10b4f-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="10b4f-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10b4f-169">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="10b4f-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





