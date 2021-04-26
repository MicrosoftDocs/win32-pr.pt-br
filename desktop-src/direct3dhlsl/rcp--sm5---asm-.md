---
title: RCP (SM5-ASM)
description: Recíproco de componente.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa37499a981bae86333b071c2e96a37ccb8ac1a6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998243"
---
# <a name="rcp-sm5---asm"></a><span data-ttu-id="712fa-103">RCP (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="712fa-103">rcp (sm5 - asm)</span></span>

<span data-ttu-id="712fa-104">Recíproco de componente.</span><span class="sxs-lookup"><span data-stu-id="712fa-104">Component-wise reciprocal.</span></span>



| <span data-ttu-id="712fa-105">RCP \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="712fa-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="712fa-106">Item</span><span class="sxs-lookup"><span data-stu-id="712fa-106">Item</span></span>                                                            | <span data-ttu-id="712fa-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="712fa-107">Description</span></span>                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="712fa-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="712fa-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="712fa-109">\[no \] endereço dos resultados</span><span class="sxs-lookup"><span data-stu-id="712fa-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="712fa-110">*dest*  =  **1,0 f**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="712fa-110">*dest* = **1.0f** / *src0*.</span></span><br/> |
| <span data-ttu-id="712fa-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="712fa-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="712fa-112">\[no \] número para pegar o recíproco de.</span><span class="sxs-lookup"><span data-stu-id="712fa-112">\[in\] The number to take the reciprocal of.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="712fa-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="712fa-113">Remarks</span></span>

<span data-ttu-id="712fa-114">Use essa instrução para reduzir a precisão recíproca, independentemente dos requisitos estritos para a divisão.</span><span class="sxs-lookup"><span data-stu-id="712fa-114">Use this instruction for reduced precision reciprocal, independent of the strict requirements for divide.</span></span>

<span data-ttu-id="712fa-115">O erro relativo máximo é 2-21.</span><span class="sxs-lookup"><span data-stu-id="712fa-115">Maximum relative error is 2-21.</span></span> <span data-ttu-id="712fa-116">(A tolerância de erro apenas corresponde a RSQ)</span><span class="sxs-lookup"><span data-stu-id="712fa-116">(The error tolerance just matches rsq)</span></span>

<span data-ttu-id="712fa-117">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números.</span><span class="sxs-lookup"><span data-stu-id="712fa-117">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



| <span data-ttu-id="712fa-118">*src*</span><span class="sxs-lookup"><span data-stu-id="712fa-118">*src*</span></span>  | <span data-ttu-id="712fa-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="712fa-119">**-inf**</span></span> | <span data-ttu-id="712fa-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="712fa-120">**-F**</span></span> | <span data-ttu-id="712fa-121">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="712fa-121">**-denorm**</span></span> | <span data-ttu-id="712fa-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="712fa-122">**-0**</span></span> | <span data-ttu-id="712fa-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="712fa-123">**+0**</span></span> | <span data-ttu-id="712fa-124">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="712fa-124">**+denorm**</span></span> | <span data-ttu-id="712fa-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="712fa-125">**+F**</span></span> | <span data-ttu-id="712fa-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="712fa-126">**+inf**</span></span> | <span data-ttu-id="712fa-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="712fa-127">**NaN**</span></span> |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="712fa-128">*dest*</span><span class="sxs-lookup"><span data-stu-id="712fa-128">*dest*</span></span> | <span data-ttu-id="712fa-129">-0</span><span class="sxs-lookup"><span data-stu-id="712fa-129">-0</span></span>       | <span data-ttu-id="712fa-130">-F</span><span class="sxs-lookup"><span data-stu-id="712fa-130">-F</span></span>     | <span data-ttu-id="712fa-131">-inf</span><span class="sxs-lookup"><span data-stu-id="712fa-131">-inf</span></span>        | <span data-ttu-id="712fa-132">-inf</span><span class="sxs-lookup"><span data-stu-id="712fa-132">-inf</span></span>   | <span data-ttu-id="712fa-133">+inf</span><span class="sxs-lookup"><span data-stu-id="712fa-133">+inf</span></span>   | <span data-ttu-id="712fa-134">+inf</span><span class="sxs-lookup"><span data-stu-id="712fa-134">+inf</span></span>        | <span data-ttu-id="712fa-135">+ F</span><span class="sxs-lookup"><span data-stu-id="712fa-135">+F</span></span>     | <span data-ttu-id="712fa-136">+0</span><span class="sxs-lookup"><span data-stu-id="712fa-136">+0</span></span>       | <span data-ttu-id="712fa-137">NaN</span><span class="sxs-lookup"><span data-stu-id="712fa-137">NaN</span></span>     |



 

<span data-ttu-id="712fa-138">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="712fa-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="712fa-139">Vértice</span><span class="sxs-lookup"><span data-stu-id="712fa-139">Vertex</span></span> | <span data-ttu-id="712fa-140">Envoltória</span><span class="sxs-lookup"><span data-stu-id="712fa-140">Hull</span></span> | <span data-ttu-id="712fa-141">Domain</span><span class="sxs-lookup"><span data-stu-id="712fa-141">Domain</span></span> | <span data-ttu-id="712fa-142">Geometria</span><span class="sxs-lookup"><span data-stu-id="712fa-142">Geometry</span></span> | <span data-ttu-id="712fa-143">16x16</span><span class="sxs-lookup"><span data-stu-id="712fa-143">Pixel</span></span> | <span data-ttu-id="712fa-144">Computação</span><span class="sxs-lookup"><span data-stu-id="712fa-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="712fa-145">X</span><span class="sxs-lookup"><span data-stu-id="712fa-145">X</span></span>      | <span data-ttu-id="712fa-146">X</span><span class="sxs-lookup"><span data-stu-id="712fa-146">X</span></span>    | <span data-ttu-id="712fa-147">X</span><span class="sxs-lookup"><span data-stu-id="712fa-147">X</span></span>      | <span data-ttu-id="712fa-148">X</span><span class="sxs-lookup"><span data-stu-id="712fa-148">X</span></span>        | <span data-ttu-id="712fa-149">X</span><span class="sxs-lookup"><span data-stu-id="712fa-149">X</span></span>     | <span data-ttu-id="712fa-150">X</span><span class="sxs-lookup"><span data-stu-id="712fa-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="712fa-151">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="712fa-151">Minimum Shader Model</span></span>

<span data-ttu-id="712fa-152">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="712fa-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="712fa-153">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="712fa-153">Shader Model</span></span>                                              | <span data-ttu-id="712fa-154">Suportado</span><span class="sxs-lookup"><span data-stu-id="712fa-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="712fa-155">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="712fa-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="712fa-156">sim</span><span class="sxs-lookup"><span data-stu-id="712fa-156">yes</span></span>       |
| [<span data-ttu-id="712fa-157">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="712fa-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="712fa-158">não</span><span class="sxs-lookup"><span data-stu-id="712fa-158">no</span></span>        |
| [<span data-ttu-id="712fa-159">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="712fa-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="712fa-160">não</span><span class="sxs-lookup"><span data-stu-id="712fa-160">no</span></span>        |
| [<span data-ttu-id="712fa-161">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="712fa-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="712fa-162">não</span><span class="sxs-lookup"><span data-stu-id="712fa-162">no</span></span>        |
| [<span data-ttu-id="712fa-163">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="712fa-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="712fa-164">não</span><span class="sxs-lookup"><span data-stu-id="712fa-164">no</span></span>        |
| [<span data-ttu-id="712fa-165">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="712fa-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="712fa-166">não</span><span class="sxs-lookup"><span data-stu-id="712fa-166">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="712fa-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="712fa-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="712fa-168">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="712fa-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





