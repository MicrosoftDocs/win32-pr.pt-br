---
title: round_pi (sm4-ASM)
description: Ponto flutuante redondo para integral float. | round_pi (sm4-ASM)
ms.assetid: AA4E4C2E-A4B0-4892-8660-1EF57767F4C4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b61282078b3639681eed756e2899d06744f0369e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997103"
---
# <a name="round_pi-sm4---asm"></a><span data-ttu-id="c7a0e-104">arredondar \_ PI (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c7a0e-104">round\_pi (sm4 - asm)</span></span>

<span data-ttu-id="c7a0e-105">Ponto flutuante redondo para integral float.</span><span class="sxs-lookup"><span data-stu-id="c7a0e-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="c7a0e-106">arredondar \_ PI \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c7a0e-106">round\_pi\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="c7a0e-107">Item</span><span class="sxs-lookup"><span data-stu-id="c7a0e-107">Item</span></span>                                                            | <span data-ttu-id="c7a0e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7a0e-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="c7a0e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c7a0e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c7a0e-110">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="c7a0e-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="c7a0e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c7a0e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c7a0e-112">\[nos \] componentes na operação.</span><span class="sxs-lookup"><span data-stu-id="c7a0e-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="c7a0e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7a0e-113">Remarks</span></span>

<span data-ttu-id="c7a0e-114">Essa instrução executa uma rodada de ponto flutuante de componente para os valores em *src0*, gravando valores de ponto flutuante integral para *dest*.</span><span class="sxs-lookup"><span data-stu-id="c7a0e-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="c7a0e-115">**o \_ PI redondo** Arredonda em direção a + infinito, normalmente conhecido como ceil ().</span><span class="sxs-lookup"><span data-stu-id="c7a0e-115">**round\_pi** rounds towards +infinity, commonly known as ceil().</span></span>

<span data-ttu-id="c7a0e-116">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números.</span><span class="sxs-lookup"><span data-stu-id="c7a0e-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="c7a0e-117">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="c7a0e-117">F means finite-real number.</span></span>



| <span data-ttu-id="c7a0e-118">**src**</span><span class="sxs-lookup"><span data-stu-id="c7a0e-118">**src**</span></span>  | <span data-ttu-id="c7a0e-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="c7a0e-119">**-inf**</span></span> | <span data-ttu-id="c7a0e-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="c7a0e-120">**-F**</span></span> | <span data-ttu-id="c7a0e-121">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="c7a0e-121">**-denorm**</span></span> | <span data-ttu-id="c7a0e-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="c7a0e-122">**-0**</span></span> | <span data-ttu-id="c7a0e-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="c7a0e-123">**+0**</span></span> | <span data-ttu-id="c7a0e-124">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="c7a0e-124">**+denorm**</span></span> | <span data-ttu-id="c7a0e-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="c7a0e-125">**+F**</span></span> | <span data-ttu-id="c7a0e-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="c7a0e-126">**+inf**</span></span> | <span data-ttu-id="c7a0e-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="c7a0e-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="c7a0e-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="c7a0e-128">**dest**</span></span> | <span data-ttu-id="c7a0e-129">-inf</span><span class="sxs-lookup"><span data-stu-id="c7a0e-129">-inf</span></span>     | <span data-ttu-id="c7a0e-130">-F</span><span class="sxs-lookup"><span data-stu-id="c7a0e-130">-F</span></span>     | <span data-ttu-id="c7a0e-131">-0</span><span class="sxs-lookup"><span data-stu-id="c7a0e-131">-0</span></span>          | <span data-ttu-id="c7a0e-132">-0</span><span class="sxs-lookup"><span data-stu-id="c7a0e-132">-0</span></span>     | <span data-ttu-id="c7a0e-133">+0</span><span class="sxs-lookup"><span data-stu-id="c7a0e-133">+0</span></span>     | <span data-ttu-id="c7a0e-134">+0</span><span class="sxs-lookup"><span data-stu-id="c7a0e-134">+0</span></span>          | <span data-ttu-id="c7a0e-135">+ F</span><span class="sxs-lookup"><span data-stu-id="c7a0e-135">+F</span></span>     | <span data-ttu-id="c7a0e-136">+inf</span><span class="sxs-lookup"><span data-stu-id="c7a0e-136">+inf</span></span>     | <span data-ttu-id="c7a0e-137">NaN</span><span class="sxs-lookup"><span data-stu-id="c7a0e-137">NaN</span></span>     |



 

<span data-ttu-id="c7a0e-138">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="c7a0e-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c7a0e-139">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="c7a0e-139">Vertex Shader</span></span> | <span data-ttu-id="c7a0e-140">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="c7a0e-140">Geometry Shader</span></span> | <span data-ttu-id="c7a0e-141">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c7a0e-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c7a0e-142">x</span><span class="sxs-lookup"><span data-stu-id="c7a0e-142">x</span></span>             | <span data-ttu-id="c7a0e-143">x</span><span class="sxs-lookup"><span data-stu-id="c7a0e-143">x</span></span>               | <span data-ttu-id="c7a0e-144">x</span><span class="sxs-lookup"><span data-stu-id="c7a0e-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c7a0e-145">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c7a0e-145">Minimum Shader Model</span></span>

<span data-ttu-id="c7a0e-146">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c7a0e-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c7a0e-147">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c7a0e-147">Shader Model</span></span>                                              | <span data-ttu-id="c7a0e-148">Suportado</span><span class="sxs-lookup"><span data-stu-id="c7a0e-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c7a0e-149">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c7a0e-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c7a0e-150">sim</span><span class="sxs-lookup"><span data-stu-id="c7a0e-150">yes</span></span>       |
| [<span data-ttu-id="c7a0e-151">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c7a0e-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c7a0e-152">sim</span><span class="sxs-lookup"><span data-stu-id="c7a0e-152">yes</span></span>       |
| [<span data-ttu-id="c7a0e-153">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c7a0e-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c7a0e-154">sim</span><span class="sxs-lookup"><span data-stu-id="c7a0e-154">yes</span></span>       |
| [<span data-ttu-id="c7a0e-155">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7a0e-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c7a0e-156">não</span><span class="sxs-lookup"><span data-stu-id="c7a0e-156">no</span></span>        |
| [<span data-ttu-id="c7a0e-157">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7a0e-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c7a0e-158">não</span><span class="sxs-lookup"><span data-stu-id="c7a0e-158">no</span></span>        |
| [<span data-ttu-id="c7a0e-159">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7a0e-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c7a0e-160">não</span><span class="sxs-lookup"><span data-stu-id="c7a0e-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c7a0e-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7a0e-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7a0e-162">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7a0e-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





