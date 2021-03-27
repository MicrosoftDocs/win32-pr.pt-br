---
title: round_z (sm4-ASM)
description: Ponto flutuante redondo para integral float. | round_z (sm4-ASM)
ms.assetid: 97C0E0F2-2571-4A94-BB04-B0CDBA0B5C0C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ed79a60bf122163b49411a3b3197ccdacba1311
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837741"
---
# <a name="round_z-sm4---asm"></a><span data-ttu-id="44f5a-104">Round \_ z (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="44f5a-104">round\_z (sm4 - asm)</span></span>

<span data-ttu-id="44f5a-105">Ponto flutuante redondo para integral float.</span><span class="sxs-lookup"><span data-stu-id="44f5a-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="44f5a-106">ARRED \_ z \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="44f5a-106">round\_z\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-----------------------------------------------------------------|



 



| <span data-ttu-id="44f5a-107">Item</span><span class="sxs-lookup"><span data-stu-id="44f5a-107">Item</span></span>                                                            | <span data-ttu-id="44f5a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="44f5a-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="44f5a-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="44f5a-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="44f5a-110">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="44f5a-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="44f5a-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="44f5a-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="44f5a-112">\[nos \] componentes na operação.</span><span class="sxs-lookup"><span data-stu-id="44f5a-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="44f5a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="44f5a-113">Remarks</span></span>

<span data-ttu-id="44f5a-114">Essa instrução executa uma rodada de ponto flutuante de componente para os valores em *src0*, gravando valores de ponto flutuante integral para *dest*.</span><span class="sxs-lookup"><span data-stu-id="44f5a-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="44f5a-115">**arredondar \_ z** Arredonda em direção a zero.</span><span class="sxs-lookup"><span data-stu-id="44f5a-115">**round\_z** rounds towards zero.</span></span>

<span data-ttu-id="44f5a-116">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números.</span><span class="sxs-lookup"><span data-stu-id="44f5a-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="44f5a-117">**src**</span><span class="sxs-lookup"><span data-stu-id="44f5a-117">**src**</span></span>  | <span data-ttu-id="44f5a-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="44f5a-118">**-inf**</span></span> | <span data-ttu-id="44f5a-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="44f5a-119">**-F**</span></span> | <span data-ttu-id="44f5a-120">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="44f5a-120">**-denorm**</span></span> | <span data-ttu-id="44f5a-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="44f5a-121">**-0**</span></span> | <span data-ttu-id="44f5a-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="44f5a-122">**+0**</span></span> | <span data-ttu-id="44f5a-123">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="44f5a-123">**+denorm**</span></span> | <span data-ttu-id="44f5a-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="44f5a-124">**+F**</span></span> | <span data-ttu-id="44f5a-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="44f5a-125">**+inf**</span></span> | <span data-ttu-id="44f5a-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="44f5a-126">**NaN**</span></span> |
| <span data-ttu-id="44f5a-127">**dest**</span><span class="sxs-lookup"><span data-stu-id="44f5a-127">**dest**</span></span> | <span data-ttu-id="44f5a-128">-inf</span><span class="sxs-lookup"><span data-stu-id="44f5a-128">-inf</span></span>     | <span data-ttu-id="44f5a-129">-F</span><span class="sxs-lookup"><span data-stu-id="44f5a-129">-F</span></span>     | <span data-ttu-id="44f5a-130">-0</span><span class="sxs-lookup"><span data-stu-id="44f5a-130">-0</span></span>          | <span data-ttu-id="44f5a-131">-0</span><span class="sxs-lookup"><span data-stu-id="44f5a-131">-0</span></span>     | <span data-ttu-id="44f5a-132">+0</span><span class="sxs-lookup"><span data-stu-id="44f5a-132">+0</span></span>     | <span data-ttu-id="44f5a-133">+0</span><span class="sxs-lookup"><span data-stu-id="44f5a-133">+0</span></span>          | <span data-ttu-id="44f5a-134">+ F</span><span class="sxs-lookup"><span data-stu-id="44f5a-134">+F</span></span>     | <span data-ttu-id="44f5a-135">+inf</span><span class="sxs-lookup"><span data-stu-id="44f5a-135">+inf</span></span>     | <span data-ttu-id="44f5a-136">NaN</span><span class="sxs-lookup"><span data-stu-id="44f5a-136">NaN</span></span>     |



 

<span data-ttu-id="44f5a-137">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="44f5a-137">F means finite-real number.</span></span>

<span data-ttu-id="44f5a-138">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="44f5a-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="44f5a-139">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="44f5a-139">Vertex Shader</span></span> | <span data-ttu-id="44f5a-140">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="44f5a-140">Geometry Shader</span></span> | <span data-ttu-id="44f5a-141">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="44f5a-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="44f5a-142">x</span><span class="sxs-lookup"><span data-stu-id="44f5a-142">x</span></span>             | <span data-ttu-id="44f5a-143">x</span><span class="sxs-lookup"><span data-stu-id="44f5a-143">x</span></span>               | <span data-ttu-id="44f5a-144">x</span><span class="sxs-lookup"><span data-stu-id="44f5a-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="44f5a-145">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="44f5a-145">Minimum Shader Model</span></span>

<span data-ttu-id="44f5a-146">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="44f5a-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="44f5a-147">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="44f5a-147">Shader Model</span></span>                                              | <span data-ttu-id="44f5a-148">Com suporte</span><span class="sxs-lookup"><span data-stu-id="44f5a-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="44f5a-149">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="44f5a-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="44f5a-150">sim</span><span class="sxs-lookup"><span data-stu-id="44f5a-150">yes</span></span>       |
| [<span data-ttu-id="44f5a-151">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="44f5a-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="44f5a-152">sim</span><span class="sxs-lookup"><span data-stu-id="44f5a-152">yes</span></span>       |
| [<span data-ttu-id="44f5a-153">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="44f5a-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="44f5a-154">sim</span><span class="sxs-lookup"><span data-stu-id="44f5a-154">yes</span></span>       |
| [<span data-ttu-id="44f5a-155">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="44f5a-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="44f5a-156">não</span><span class="sxs-lookup"><span data-stu-id="44f5a-156">no</span></span>        |
| [<span data-ttu-id="44f5a-157">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="44f5a-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="44f5a-158">não</span><span class="sxs-lookup"><span data-stu-id="44f5a-158">no</span></span>        |
| [<span data-ttu-id="44f5a-159">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="44f5a-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="44f5a-160">não</span><span class="sxs-lookup"><span data-stu-id="44f5a-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="44f5a-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="44f5a-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44f5a-162">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="44f5a-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





