---
title: RSQ (sm4-ASM)
description: Raiz quadrada recíproca de componente.
ms.assetid: CDA3C2DF-2793-4CE3-87CE-4E0AA945A1BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc274f927151938be055150d5b17287f9be0004d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006914"
---
# <a name="rsq-sm4---asm"></a><span data-ttu-id="d5b5a-103">RSQ (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d5b5a-103">rsq (sm4 - asm)</span></span>

<span data-ttu-id="d5b5a-104">Raiz quadrada recíproca de componente.</span><span class="sxs-lookup"><span data-stu-id="d5b5a-104">Component-wise reciprocal square root.</span></span>



| <span data-ttu-id="d5b5a-105">RSQ \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d5b5a-105">rsq\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="d5b5a-106">Item</span><span class="sxs-lookup"><span data-stu-id="d5b5a-106">Item</span></span>                                                            | <span data-ttu-id="d5b5a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5b5a-107">Description</span></span>                                                                                      |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5b5a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d5b5a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d5b5a-109">\[in \] contém os resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="d5b5a-109">\[in\] Contains the results of the operation.</span></span><br/> <span data-ttu-id="d5b5a-110">*dest* = 1,0 f/sqrt (*src0*)</span><span class="sxs-lookup"><span data-stu-id="d5b5a-110">*dest* = 1.0f / sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="d5b5a-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d5b5a-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d5b5a-112">\[nos \] componentes para a operação.</span><span class="sxs-lookup"><span data-stu-id="d5b5a-112">\[in\] The components for the operation.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="d5b5a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5b5a-113">Remarks</span></span>

<span data-ttu-id="d5b5a-114">O erro relativo máximo é 2-21.</span><span class="sxs-lookup"><span data-stu-id="d5b5a-114">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="d5b5a-115">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="d5b5a-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="d5b5a-116">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="d5b5a-116">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="d5b5a-117">**src**</span><span class="sxs-lookup"><span data-stu-id="d5b5a-117">**src**</span></span>  | <span data-ttu-id="d5b5a-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="d5b5a-118">**-inf**</span></span> | <span data-ttu-id="d5b5a-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="d5b5a-119">**-F**</span></span> | <span data-ttu-id="d5b5a-120">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="d5b5a-120">**-denorm**</span></span> | <span data-ttu-id="d5b5a-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="d5b5a-121">**-0**</span></span> | <span data-ttu-id="d5b5a-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="d5b5a-122">**+0**</span></span> | <span data-ttu-id="d5b5a-123">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="d5b5a-123">**+denorm**</span></span> | <span data-ttu-id="d5b5a-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="d5b5a-124">**+F**</span></span> | <span data-ttu-id="d5b5a-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="d5b5a-125">**+inf**</span></span> | <span data-ttu-id="d5b5a-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="d5b5a-126">**NaN**</span></span> |
| <span data-ttu-id="d5b5a-127">**dest**</span><span class="sxs-lookup"><span data-stu-id="d5b5a-127">**dest**</span></span> | <span data-ttu-id="d5b5a-128">NaN</span><span class="sxs-lookup"><span data-stu-id="d5b5a-128">NaN</span></span>      | <span data-ttu-id="d5b5a-129">NaN</span><span class="sxs-lookup"><span data-stu-id="d5b5a-129">NaN</span></span>    | <span data-ttu-id="d5b5a-130">-inf</span><span class="sxs-lookup"><span data-stu-id="d5b5a-130">-inf</span></span>        | <span data-ttu-id="d5b5a-131">-inf</span><span class="sxs-lookup"><span data-stu-id="d5b5a-131">-inf</span></span>   | <span data-ttu-id="d5b5a-132">+inf</span><span class="sxs-lookup"><span data-stu-id="d5b5a-132">+inf</span></span>   | <span data-ttu-id="d5b5a-133">+inf</span><span class="sxs-lookup"><span data-stu-id="d5b5a-133">+inf</span></span>        | <span data-ttu-id="d5b5a-134">+ F</span><span class="sxs-lookup"><span data-stu-id="d5b5a-134">+F</span></span>     | <span data-ttu-id="d5b5a-135">+0</span><span class="sxs-lookup"><span data-stu-id="d5b5a-135">+0</span></span>       | <span data-ttu-id="d5b5a-136">NaN</span><span class="sxs-lookup"><span data-stu-id="d5b5a-136">NaN</span></span>     |



 

<span data-ttu-id="d5b5a-137">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="d5b5a-137">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d5b5a-138">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="d5b5a-138">Vertex Shader</span></span> | <span data-ttu-id="d5b5a-139">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="d5b5a-139">Geometry Shader</span></span> | <span data-ttu-id="d5b5a-140">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="d5b5a-140">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d5b5a-141">x</span><span class="sxs-lookup"><span data-stu-id="d5b5a-141">x</span></span>             | <span data-ttu-id="d5b5a-142">x</span><span class="sxs-lookup"><span data-stu-id="d5b5a-142">x</span></span>               | <span data-ttu-id="d5b5a-143">x</span><span class="sxs-lookup"><span data-stu-id="d5b5a-143">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d5b5a-144">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="d5b5a-144">Minimum Shader Model</span></span>

<span data-ttu-id="d5b5a-145">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d5b5a-145">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d5b5a-146">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="d5b5a-146">Shader Model</span></span>                                              | <span data-ttu-id="d5b5a-147">Com suporte</span><span class="sxs-lookup"><span data-stu-id="d5b5a-147">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d5b5a-148">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d5b5a-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d5b5a-149">sim</span><span class="sxs-lookup"><span data-stu-id="d5b5a-149">yes</span></span>       |
| [<span data-ttu-id="d5b5a-150">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="d5b5a-150">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d5b5a-151">sim</span><span class="sxs-lookup"><span data-stu-id="d5b5a-151">yes</span></span>       |
| [<span data-ttu-id="d5b5a-152">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="d5b5a-152">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d5b5a-153">sim</span><span class="sxs-lookup"><span data-stu-id="d5b5a-153">yes</span></span>       |
| [<span data-ttu-id="d5b5a-154">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5b5a-154">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d5b5a-155">não</span><span class="sxs-lookup"><span data-stu-id="d5b5a-155">no</span></span>        |
| [<span data-ttu-id="d5b5a-156">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5b5a-156">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d5b5a-157">não</span><span class="sxs-lookup"><span data-stu-id="d5b5a-157">no</span></span>        |
| [<span data-ttu-id="d5b5a-158">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5b5a-158">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d5b5a-159">não</span><span class="sxs-lookup"><span data-stu-id="d5b5a-159">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d5b5a-160">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5b5a-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5b5a-161">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5b5a-161">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





