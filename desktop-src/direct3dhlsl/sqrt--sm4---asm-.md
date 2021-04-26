---
title: sqrt (sm4-ASM)
description: Raiz quadrada por componente.
ms.assetid: B860D656-7F01-484F-909F-A5C9A61C52C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 628601e0a3a78784a5fd1a089ef7608a0cf9ca05
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996603"
---
# <a name="sqrt-sm4---asm"></a><span data-ttu-id="4e18e-103">sqrt (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4e18e-103">sqrt (sm4 - asm)</span></span>

<span data-ttu-id="4e18e-104">Raiz quadrada por componente.</span><span class="sxs-lookup"><span data-stu-id="4e18e-104">Component-wise square root.</span></span>



| <span data-ttu-id="4e18e-105">SQRT \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="4e18e-105">sqrt\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="4e18e-106">Item</span><span class="sxs-lookup"><span data-stu-id="4e18e-106">Item</span></span>                                                            | <span data-ttu-id="4e18e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e18e-107">Description</span></span>                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4e18e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="4e18e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="4e18e-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="4e18e-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="4e18e-110">*dest* = sqrt (*src0*)</span><span class="sxs-lookup"><span data-stu-id="4e18e-110">*dest* = sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="4e18e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4e18e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="4e18e-112">\[nos \] componentes para os quais obter a raiz quadrada.</span><span class="sxs-lookup"><span data-stu-id="4e18e-112">\[in\] The components for which to take the square root.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="4e18e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e18e-113">Remarks</span></span>

<span data-ttu-id="4e18e-114">A precisão é 1 ULP.</span><span class="sxs-lookup"><span data-stu-id="4e18e-114">Precision is 1 ulp.</span></span>

<span data-ttu-id="4e18e-115">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="4e18e-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="4e18e-116">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="4e18e-116">F means finite-real number.</span></span>



|          | <span data-ttu-id="4e18e-117">**-INF**</span><span class="sxs-lookup"><span data-stu-id="4e18e-117">**-inf**</span></span> | <span data-ttu-id="4e18e-118">**-F**</span><span class="sxs-lookup"><span data-stu-id="4e18e-118">**-F**</span></span> | <span data-ttu-id="4e18e-119">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="4e18e-119">**-denorm**</span></span> | <span data-ttu-id="4e18e-120">**-0**</span><span class="sxs-lookup"><span data-stu-id="4e18e-120">**-0**</span></span> | <span data-ttu-id="4e18e-121">**+0**</span><span class="sxs-lookup"><span data-stu-id="4e18e-121">**+0**</span></span> | <span data-ttu-id="4e18e-122">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="4e18e-122">**+denorm**</span></span> | <span data-ttu-id="4e18e-123">**+ F**</span><span class="sxs-lookup"><span data-stu-id="4e18e-123">**+F**</span></span> | <span data-ttu-id="4e18e-124">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="4e18e-124">**+inf**</span></span> | <span data-ttu-id="4e18e-125">**NaN**</span><span class="sxs-lookup"><span data-stu-id="4e18e-125">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="4e18e-126">**dest**</span><span class="sxs-lookup"><span data-stu-id="4e18e-126">**dest**</span></span> | <span data-ttu-id="4e18e-127">NaN</span><span class="sxs-lookup"><span data-stu-id="4e18e-127">NaN</span></span>      | <span data-ttu-id="4e18e-128">NaN</span><span class="sxs-lookup"><span data-stu-id="4e18e-128">NaN</span></span>    | <span data-ttu-id="4e18e-129">-0</span><span class="sxs-lookup"><span data-stu-id="4e18e-129">-0</span></span>          | <span data-ttu-id="4e18e-130">-0</span><span class="sxs-lookup"><span data-stu-id="4e18e-130">-0</span></span>     | <span data-ttu-id="4e18e-131">+0</span><span class="sxs-lookup"><span data-stu-id="4e18e-131">+0</span></span>     | <span data-ttu-id="4e18e-132">+0</span><span class="sxs-lookup"><span data-stu-id="4e18e-132">+0</span></span>          | <span data-ttu-id="4e18e-133">+ F</span><span class="sxs-lookup"><span data-stu-id="4e18e-133">+F</span></span>     | <span data-ttu-id="4e18e-134">+inf</span><span class="sxs-lookup"><span data-stu-id="4e18e-134">+inf</span></span>     | <span data-ttu-id="4e18e-135">NaN</span><span class="sxs-lookup"><span data-stu-id="4e18e-135">NaN</span></span>     |



 

<span data-ttu-id="4e18e-136">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="4e18e-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4e18e-137">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="4e18e-137">Vertex Shader</span></span> | <span data-ttu-id="4e18e-138">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="4e18e-138">Geometry Shader</span></span> | <span data-ttu-id="4e18e-139">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="4e18e-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4e18e-140">x</span><span class="sxs-lookup"><span data-stu-id="4e18e-140">x</span></span>             | <span data-ttu-id="4e18e-141">x</span><span class="sxs-lookup"><span data-stu-id="4e18e-141">x</span></span>               | <span data-ttu-id="4e18e-142">x</span><span class="sxs-lookup"><span data-stu-id="4e18e-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4e18e-143">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="4e18e-143">Minimum Shader Model</span></span>

<span data-ttu-id="4e18e-144">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4e18e-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4e18e-145">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="4e18e-145">Shader Model</span></span>                                              | <span data-ttu-id="4e18e-146">Suportado</span><span class="sxs-lookup"><span data-stu-id="4e18e-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4e18e-147">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4e18e-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4e18e-148">sim</span><span class="sxs-lookup"><span data-stu-id="4e18e-148">yes</span></span>       |
| [<span data-ttu-id="4e18e-149">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="4e18e-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4e18e-150">sim</span><span class="sxs-lookup"><span data-stu-id="4e18e-150">yes</span></span>       |
| [<span data-ttu-id="4e18e-151">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="4e18e-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4e18e-152">sim</span><span class="sxs-lookup"><span data-stu-id="4e18e-152">yes</span></span>       |
| [<span data-ttu-id="4e18e-153">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e18e-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4e18e-154">não</span><span class="sxs-lookup"><span data-stu-id="4e18e-154">no</span></span>        |
| [<span data-ttu-id="4e18e-155">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e18e-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4e18e-156">não</span><span class="sxs-lookup"><span data-stu-id="4e18e-156">no</span></span>        |
| [<span data-ttu-id="4e18e-157">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e18e-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4e18e-158">não</span><span class="sxs-lookup"><span data-stu-id="4e18e-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4e18e-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e18e-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e18e-160">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e18e-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





