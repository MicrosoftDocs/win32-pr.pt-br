---
title: RCP (SM5-ASM)
description: Recíproco de componente.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbaa2ffc29a4c3373009d9dec1b895710186e67
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104498952"
---
# <a name="rcp-sm5---asm"></a><span data-ttu-id="a2eb0-103">RCP (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a2eb0-103">rcp (sm5 - asm)</span></span>

<span data-ttu-id="a2eb0-104">Recíproco de componente.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-104">Component-wise reciprocal.</span></span>



| <span data-ttu-id="a2eb0-105">RCP \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="a2eb0-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="a2eb0-106">Item</span><span class="sxs-lookup"><span data-stu-id="a2eb0-106">Item</span></span>                                                            | <span data-ttu-id="a2eb0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2eb0-107">Description</span></span>                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a2eb0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a2eb0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a2eb0-109">\[no \] endereço dos resultados</span><span class="sxs-lookup"><span data-stu-id="a2eb0-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="a2eb0-110">*dest*  =  **1,0 f**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-110">*dest* = **1.0f** / *src0*.</span></span><br/> |
| <span data-ttu-id="a2eb0-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a2eb0-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a2eb0-112">\[no \] número para pegar o recíproco de.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-112">\[in\] The number to take the reciprocal of.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="a2eb0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2eb0-113">Remarks</span></span>

<span data-ttu-id="a2eb0-114">Use essa instrução para reduzir a precisão recíproca, independentemente dos requisitos estritos para a divisão.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-114">Use this instruction for reduced precision reciprocal, independent of the strict requirements for divide.</span></span>

<span data-ttu-id="a2eb0-115">O erro relativo máximo é 2-21.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-115">Maximum relative error is 2-21.</span></span> <span data-ttu-id="a2eb0-116">(A tolerância de erro apenas corresponde a RSQ)</span><span class="sxs-lookup"><span data-stu-id="a2eb0-116">(The error tolerance just matches rsq)</span></span>

<span data-ttu-id="a2eb0-117">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-117">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



|        |          |        |             |        |        |             |        |          |         |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="a2eb0-118">*src*</span><span class="sxs-lookup"><span data-stu-id="a2eb0-118">*src*</span></span>  | <span data-ttu-id="a2eb0-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="a2eb0-119">**-inf**</span></span> | <span data-ttu-id="a2eb0-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="a2eb0-120">**-F**</span></span> | <span data-ttu-id="a2eb0-121">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="a2eb0-121">**-denorm**</span></span> | <span data-ttu-id="a2eb0-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="a2eb0-122">**-0**</span></span> | <span data-ttu-id="a2eb0-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="a2eb0-123">**+0**</span></span> | <span data-ttu-id="a2eb0-124">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="a2eb0-124">**+denorm**</span></span> | <span data-ttu-id="a2eb0-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="a2eb0-125">**+F**</span></span> | <span data-ttu-id="a2eb0-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="a2eb0-126">**+inf**</span></span> | <span data-ttu-id="a2eb0-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a2eb0-127">**NaN**</span></span> |
| <span data-ttu-id="a2eb0-128">*dest*</span><span class="sxs-lookup"><span data-stu-id="a2eb0-128">*dest*</span></span> | <span data-ttu-id="a2eb0-129">-0</span><span class="sxs-lookup"><span data-stu-id="a2eb0-129">-0</span></span>       | <span data-ttu-id="a2eb0-130">-F</span><span class="sxs-lookup"><span data-stu-id="a2eb0-130">-F</span></span>     | <span data-ttu-id="a2eb0-131">-inf</span><span class="sxs-lookup"><span data-stu-id="a2eb0-131">-inf</span></span>        | <span data-ttu-id="a2eb0-132">-inf</span><span class="sxs-lookup"><span data-stu-id="a2eb0-132">-inf</span></span>   | <span data-ttu-id="a2eb0-133">+inf</span><span class="sxs-lookup"><span data-stu-id="a2eb0-133">+inf</span></span>   | <span data-ttu-id="a2eb0-134">+inf</span><span class="sxs-lookup"><span data-stu-id="a2eb0-134">+inf</span></span>        | <span data-ttu-id="a2eb0-135">+ F</span><span class="sxs-lookup"><span data-stu-id="a2eb0-135">+F</span></span>     | <span data-ttu-id="a2eb0-136">+0</span><span class="sxs-lookup"><span data-stu-id="a2eb0-136">+0</span></span>       | <span data-ttu-id="a2eb0-137">NaN</span><span class="sxs-lookup"><span data-stu-id="a2eb0-137">NaN</span></span>     |



 

<span data-ttu-id="a2eb0-138">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a2eb0-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a2eb0-139">Vértice</span><span class="sxs-lookup"><span data-stu-id="a2eb0-139">Vertex</span></span> | <span data-ttu-id="a2eb0-140">Envoltória</span><span class="sxs-lookup"><span data-stu-id="a2eb0-140">Hull</span></span> | <span data-ttu-id="a2eb0-141">Domínio</span><span class="sxs-lookup"><span data-stu-id="a2eb0-141">Domain</span></span> | <span data-ttu-id="a2eb0-142">Geometria</span><span class="sxs-lookup"><span data-stu-id="a2eb0-142">Geometry</span></span> | <span data-ttu-id="a2eb0-143">16x16</span><span class="sxs-lookup"><span data-stu-id="a2eb0-143">Pixel</span></span> | <span data-ttu-id="a2eb0-144">Computação</span><span class="sxs-lookup"><span data-stu-id="a2eb0-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a2eb0-145">X</span><span class="sxs-lookup"><span data-stu-id="a2eb0-145">X</span></span>      | <span data-ttu-id="a2eb0-146">X</span><span class="sxs-lookup"><span data-stu-id="a2eb0-146">X</span></span>    | <span data-ttu-id="a2eb0-147">X</span><span class="sxs-lookup"><span data-stu-id="a2eb0-147">X</span></span>      | <span data-ttu-id="a2eb0-148">X</span><span class="sxs-lookup"><span data-stu-id="a2eb0-148">X</span></span>        | <span data-ttu-id="a2eb0-149">X</span><span class="sxs-lookup"><span data-stu-id="a2eb0-149">X</span></span>     | <span data-ttu-id="a2eb0-150">X</span><span class="sxs-lookup"><span data-stu-id="a2eb0-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a2eb0-151">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="a2eb0-151">Minimum Shader Model</span></span>

<span data-ttu-id="a2eb0-152">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a2eb0-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a2eb0-153">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="a2eb0-153">Shader Model</span></span>                                              | <span data-ttu-id="a2eb0-154">Com suporte</span><span class="sxs-lookup"><span data-stu-id="a2eb0-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a2eb0-155">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a2eb0-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a2eb0-156">sim</span><span class="sxs-lookup"><span data-stu-id="a2eb0-156">yes</span></span>       |
| [<span data-ttu-id="a2eb0-157">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a2eb0-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a2eb0-158">não</span><span class="sxs-lookup"><span data-stu-id="a2eb0-158">no</span></span>        |
| [<span data-ttu-id="a2eb0-159">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a2eb0-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a2eb0-160">não</span><span class="sxs-lookup"><span data-stu-id="a2eb0-160">no</span></span>        |
| [<span data-ttu-id="a2eb0-161">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a2eb0-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a2eb0-162">não</span><span class="sxs-lookup"><span data-stu-id="a2eb0-162">no</span></span>        |
| [<span data-ttu-id="a2eb0-163">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a2eb0-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a2eb0-164">não</span><span class="sxs-lookup"><span data-stu-id="a2eb0-164">no</span></span>        |
| [<span data-ttu-id="a2eb0-165">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a2eb0-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a2eb0-166">não</span><span class="sxs-lookup"><span data-stu-id="a2eb0-166">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a2eb0-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2eb0-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2eb0-168">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a2eb0-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





