---
title: round_z (sm4-ASM)
description: Ponto flutuante redondo para integral float. | round_z (sm4-ASM)
ms.assetid: 97C0E0F2-2571-4A94-BB04-B0CDBA0B5C0C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc874c6d0a1f26902086af300784c55950b71569
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997123"
---
# <a name="round_z-sm4---asm"></a><span data-ttu-id="dcbbe-104">Round \_ z (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="dcbbe-104">round\_z (sm4 - asm)</span></span>

<span data-ttu-id="dcbbe-105">Ponto flutuante redondo para integral float.</span><span class="sxs-lookup"><span data-stu-id="dcbbe-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="dcbbe-106">ARRED \_ z \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="dcbbe-106">round\_z\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-----------------------------------------------------------------|



 



| <span data-ttu-id="dcbbe-107">Item</span><span class="sxs-lookup"><span data-stu-id="dcbbe-107">Item</span></span>                                                            | <span data-ttu-id="dcbbe-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="dcbbe-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="dcbbe-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="dcbbe-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="dcbbe-110">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="dcbbe-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="dcbbe-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="dcbbe-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="dcbbe-112">\[nos \] componentes na operação.</span><span class="sxs-lookup"><span data-stu-id="dcbbe-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="dcbbe-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="dcbbe-113">Remarks</span></span>

<span data-ttu-id="dcbbe-114">Essa instrução executa uma rodada de ponto flutuante de componente para os valores em *src0*, gravando valores de ponto flutuante integral para *dest*.</span><span class="sxs-lookup"><span data-stu-id="dcbbe-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="dcbbe-115">**arredondar \_ z** Arredonda em direção a zero.</span><span class="sxs-lookup"><span data-stu-id="dcbbe-115">**round\_z** rounds towards zero.</span></span>

<span data-ttu-id="dcbbe-116">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números.</span><span class="sxs-lookup"><span data-stu-id="dcbbe-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



| <span data-ttu-id="dcbbe-117">**src**</span><span class="sxs-lookup"><span data-stu-id="dcbbe-117">**src**</span></span>  | <span data-ttu-id="dcbbe-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="dcbbe-118">**-inf**</span></span> | <span data-ttu-id="dcbbe-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="dcbbe-119">**-F**</span></span> | <span data-ttu-id="dcbbe-120">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="dcbbe-120">**-denorm**</span></span> | <span data-ttu-id="dcbbe-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="dcbbe-121">**-0**</span></span> | <span data-ttu-id="dcbbe-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="dcbbe-122">**+0**</span></span> | <span data-ttu-id="dcbbe-123">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="dcbbe-123">**+denorm**</span></span> | <span data-ttu-id="dcbbe-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="dcbbe-124">**+F**</span></span> | <span data-ttu-id="dcbbe-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="dcbbe-125">**+inf**</span></span> | <span data-ttu-id="dcbbe-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="dcbbe-126">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="dcbbe-127">**dest**</span><span class="sxs-lookup"><span data-stu-id="dcbbe-127">**dest**</span></span> | <span data-ttu-id="dcbbe-128">-inf</span><span class="sxs-lookup"><span data-stu-id="dcbbe-128">-inf</span></span>     | <span data-ttu-id="dcbbe-129">-F</span><span class="sxs-lookup"><span data-stu-id="dcbbe-129">-F</span></span>     | <span data-ttu-id="dcbbe-130">-0</span><span class="sxs-lookup"><span data-stu-id="dcbbe-130">-0</span></span>          | <span data-ttu-id="dcbbe-131">-0</span><span class="sxs-lookup"><span data-stu-id="dcbbe-131">-0</span></span>     | <span data-ttu-id="dcbbe-132">+0</span><span class="sxs-lookup"><span data-stu-id="dcbbe-132">+0</span></span>     | <span data-ttu-id="dcbbe-133">+0</span><span class="sxs-lookup"><span data-stu-id="dcbbe-133">+0</span></span>          | <span data-ttu-id="dcbbe-134">+ F</span><span class="sxs-lookup"><span data-stu-id="dcbbe-134">+F</span></span>     | <span data-ttu-id="dcbbe-135">+inf</span><span class="sxs-lookup"><span data-stu-id="dcbbe-135">+inf</span></span>     | <span data-ttu-id="dcbbe-136">NaN</span><span class="sxs-lookup"><span data-stu-id="dcbbe-136">NaN</span></span>     |



 

<span data-ttu-id="dcbbe-137">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="dcbbe-137">F means finite-real number.</span></span>

<span data-ttu-id="dcbbe-138">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="dcbbe-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="dcbbe-139">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="dcbbe-139">Vertex Shader</span></span> | <span data-ttu-id="dcbbe-140">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="dcbbe-140">Geometry Shader</span></span> | <span data-ttu-id="dcbbe-141">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="dcbbe-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="dcbbe-142">x</span><span class="sxs-lookup"><span data-stu-id="dcbbe-142">x</span></span>             | <span data-ttu-id="dcbbe-143">x</span><span class="sxs-lookup"><span data-stu-id="dcbbe-143">x</span></span>               | <span data-ttu-id="dcbbe-144">x</span><span class="sxs-lookup"><span data-stu-id="dcbbe-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dcbbe-145">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="dcbbe-145">Minimum Shader Model</span></span>

<span data-ttu-id="dcbbe-146">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dcbbe-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dcbbe-147">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="dcbbe-147">Shader Model</span></span>                                              | <span data-ttu-id="dcbbe-148">Suportado</span><span class="sxs-lookup"><span data-stu-id="dcbbe-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="dcbbe-149">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="dcbbe-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="dcbbe-150">sim</span><span class="sxs-lookup"><span data-stu-id="dcbbe-150">yes</span></span>       |
| [<span data-ttu-id="dcbbe-151">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="dcbbe-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="dcbbe-152">sim</span><span class="sxs-lookup"><span data-stu-id="dcbbe-152">yes</span></span>       |
| [<span data-ttu-id="dcbbe-153">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="dcbbe-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="dcbbe-154">sim</span><span class="sxs-lookup"><span data-stu-id="dcbbe-154">yes</span></span>       |
| [<span data-ttu-id="dcbbe-155">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dcbbe-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="dcbbe-156">não</span><span class="sxs-lookup"><span data-stu-id="dcbbe-156">no</span></span>        |
| [<span data-ttu-id="dcbbe-157">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dcbbe-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="dcbbe-158">não</span><span class="sxs-lookup"><span data-stu-id="dcbbe-158">no</span></span>        |
| [<span data-ttu-id="dcbbe-159">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dcbbe-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="dcbbe-160">não</span><span class="sxs-lookup"><span data-stu-id="dcbbe-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="dcbbe-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dcbbe-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcbbe-162">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dcbbe-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





