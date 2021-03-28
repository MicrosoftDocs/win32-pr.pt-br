---
title: round_ni (sm4-ASM)
description: Ponto flutuante redondo para integral float. | round_ni (sm4-ASM)
ms.assetid: 6DEF818B-AFF9-4B44-950E-320EACE1CAC4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3daafd64e76bd8c04acf7812b096f7374befef6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104012028"
---
# <a name="round_ni-sm4---asm"></a><span data-ttu-id="ac9ed-104">Round \_ Ni (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ac9ed-104">round\_ni (sm4 - asm)</span></span>

<span data-ttu-id="ac9ed-105">Ponto flutuante redondo para integral float.</span><span class="sxs-lookup"><span data-stu-id="ac9ed-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="ac9ed-106">ARRED \_ Ni \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="ac9ed-106">round\_ni\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="ac9ed-107">Item</span><span class="sxs-lookup"><span data-stu-id="ac9ed-107">Item</span></span>                                                            | <span data-ttu-id="ac9ed-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac9ed-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="ac9ed-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ac9ed-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ac9ed-110">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="ac9ed-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="ac9ed-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ac9ed-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ac9ed-112">\[nos \] componentes na operação.</span><span class="sxs-lookup"><span data-stu-id="ac9ed-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="ac9ed-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac9ed-113">Remarks</span></span>

<span data-ttu-id="ac9ed-114">Essa instrução executa uma rodada de ponto flutuante de componente para os valores em *src0*, gravando valores de ponto flutuante integral para *dest*.</span><span class="sxs-lookup"><span data-stu-id="ac9ed-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span> <span data-ttu-id="ac9ed-115">**Round \_ Ni** Arredonda em direção ao infinito, normalmente conhecido como Floor ().</span><span class="sxs-lookup"><span data-stu-id="ac9ed-115">**round\_ni** rounds toward -infinity, commonly known as floor().</span></span>

<span data-ttu-id="ac9ed-116">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números.</span><span class="sxs-lookup"><span data-stu-id="ac9ed-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="ac9ed-117">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="ac9ed-117">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="ac9ed-118">**src**</span><span class="sxs-lookup"><span data-stu-id="ac9ed-118">**src**</span></span>  | <span data-ttu-id="ac9ed-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="ac9ed-119">**-inf**</span></span> | <span data-ttu-id="ac9ed-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="ac9ed-120">**-F**</span></span> | <span data-ttu-id="ac9ed-121">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="ac9ed-121">**-denorm**</span></span> | <span data-ttu-id="ac9ed-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="ac9ed-122">**-0**</span></span> | <span data-ttu-id="ac9ed-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="ac9ed-123">**+0**</span></span> | <span data-ttu-id="ac9ed-124">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="ac9ed-124">**+denorm**</span></span> | <span data-ttu-id="ac9ed-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="ac9ed-125">**+F**</span></span> | <span data-ttu-id="ac9ed-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="ac9ed-126">**+inf**</span></span> | <span data-ttu-id="ac9ed-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="ac9ed-127">**NaN**</span></span> |
| <span data-ttu-id="ac9ed-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="ac9ed-128">**dest**</span></span> | <span data-ttu-id="ac9ed-129">-inf</span><span class="sxs-lookup"><span data-stu-id="ac9ed-129">-inf</span></span>     | <span data-ttu-id="ac9ed-130">-F</span><span class="sxs-lookup"><span data-stu-id="ac9ed-130">-F</span></span>     | <span data-ttu-id="ac9ed-131">-0</span><span class="sxs-lookup"><span data-stu-id="ac9ed-131">-0</span></span>          | <span data-ttu-id="ac9ed-132">-0</span><span class="sxs-lookup"><span data-stu-id="ac9ed-132">-0</span></span>     | <span data-ttu-id="ac9ed-133">+0</span><span class="sxs-lookup"><span data-stu-id="ac9ed-133">+0</span></span>     | <span data-ttu-id="ac9ed-134">+0</span><span class="sxs-lookup"><span data-stu-id="ac9ed-134">+0</span></span>          | <span data-ttu-id="ac9ed-135">+ F</span><span class="sxs-lookup"><span data-stu-id="ac9ed-135">+F</span></span>     | <span data-ttu-id="ac9ed-136">+inf</span><span class="sxs-lookup"><span data-stu-id="ac9ed-136">+inf</span></span>     | <span data-ttu-id="ac9ed-137">NaN</span><span class="sxs-lookup"><span data-stu-id="ac9ed-137">NaN</span></span>     |



 

<span data-ttu-id="ac9ed-138">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="ac9ed-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ac9ed-139">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="ac9ed-139">Vertex Shader</span></span> | <span data-ttu-id="ac9ed-140">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="ac9ed-140">Geometry Shader</span></span> | <span data-ttu-id="ac9ed-141">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="ac9ed-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ac9ed-142">x</span><span class="sxs-lookup"><span data-stu-id="ac9ed-142">x</span></span>             | <span data-ttu-id="ac9ed-143">x</span><span class="sxs-lookup"><span data-stu-id="ac9ed-143">x</span></span>               | <span data-ttu-id="ac9ed-144">x</span><span class="sxs-lookup"><span data-stu-id="ac9ed-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ac9ed-145">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="ac9ed-145">Minimum Shader Model</span></span>

<span data-ttu-id="ac9ed-146">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ac9ed-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ac9ed-147">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="ac9ed-147">Shader Model</span></span>                                              | <span data-ttu-id="ac9ed-148">Com suporte</span><span class="sxs-lookup"><span data-stu-id="ac9ed-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ac9ed-149">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ac9ed-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ac9ed-150">sim</span><span class="sxs-lookup"><span data-stu-id="ac9ed-150">yes</span></span>       |
| [<span data-ttu-id="ac9ed-151">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="ac9ed-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ac9ed-152">sim</span><span class="sxs-lookup"><span data-stu-id="ac9ed-152">yes</span></span>       |
| [<span data-ttu-id="ac9ed-153">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ac9ed-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ac9ed-154">sim</span><span class="sxs-lookup"><span data-stu-id="ac9ed-154">yes</span></span>       |
| [<span data-ttu-id="ac9ed-155">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac9ed-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ac9ed-156">não</span><span class="sxs-lookup"><span data-stu-id="ac9ed-156">no</span></span>        |
| [<span data-ttu-id="ac9ed-157">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac9ed-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ac9ed-158">não</span><span class="sxs-lookup"><span data-stu-id="ac9ed-158">no</span></span>        |
| [<span data-ttu-id="ac9ed-159">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac9ed-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ac9ed-160">não</span><span class="sxs-lookup"><span data-stu-id="ac9ed-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ac9ed-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac9ed-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac9ed-162">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac9ed-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





