---
title: round_pi (sm4-ASM)
description: Ponto flutuante redondo para integral float. | round_pi (sm4-ASM)
ms.assetid: AA4E4C2E-A4B0-4892-8660-1EF57767F4C4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6016cc03f28852c938b1be62d3aaca39dae5dcfb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989223"
---
# <a name="round_pi-sm4---asm"></a><span data-ttu-id="512b7-104">arredondar \_ PI (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="512b7-104">round\_pi (sm4 - asm)</span></span>

<span data-ttu-id="512b7-105">Ponto flutuante redondo para integral float.</span><span class="sxs-lookup"><span data-stu-id="512b7-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="512b7-106">arredondar \_ PI \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="512b7-106">round\_pi\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="512b7-107">Item</span><span class="sxs-lookup"><span data-stu-id="512b7-107">Item</span></span>                                                            | <span data-ttu-id="512b7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="512b7-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="512b7-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="512b7-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="512b7-110">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="512b7-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="512b7-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="512b7-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="512b7-112">\[nos \] componentes na operação.</span><span class="sxs-lookup"><span data-stu-id="512b7-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="512b7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="512b7-113">Remarks</span></span>

<span data-ttu-id="512b7-114">Essa instrução executa uma rodada de ponto flutuante de componente para os valores em *src0*, gravando valores de ponto flutuante integral para *dest*.</span><span class="sxs-lookup"><span data-stu-id="512b7-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="512b7-115">**o \_ PI redondo** Arredonda em direção a + infinito, normalmente conhecido como ceil ().</span><span class="sxs-lookup"><span data-stu-id="512b7-115">**round\_pi** rounds towards +infinity, commonly known as ceil().</span></span>

<span data-ttu-id="512b7-116">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números.</span><span class="sxs-lookup"><span data-stu-id="512b7-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="512b7-117">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="512b7-117">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="512b7-118">**src**</span><span class="sxs-lookup"><span data-stu-id="512b7-118">**src**</span></span>  | <span data-ttu-id="512b7-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="512b7-119">**-inf**</span></span> | <span data-ttu-id="512b7-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="512b7-120">**-F**</span></span> | <span data-ttu-id="512b7-121">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="512b7-121">**-denorm**</span></span> | <span data-ttu-id="512b7-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="512b7-122">**-0**</span></span> | <span data-ttu-id="512b7-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="512b7-123">**+0**</span></span> | <span data-ttu-id="512b7-124">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="512b7-124">**+denorm**</span></span> | <span data-ttu-id="512b7-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="512b7-125">**+F**</span></span> | <span data-ttu-id="512b7-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="512b7-126">**+inf**</span></span> | <span data-ttu-id="512b7-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="512b7-127">**NaN**</span></span> |
| <span data-ttu-id="512b7-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="512b7-128">**dest**</span></span> | <span data-ttu-id="512b7-129">-inf</span><span class="sxs-lookup"><span data-stu-id="512b7-129">-inf</span></span>     | <span data-ttu-id="512b7-130">-F</span><span class="sxs-lookup"><span data-stu-id="512b7-130">-F</span></span>     | <span data-ttu-id="512b7-131">-0</span><span class="sxs-lookup"><span data-stu-id="512b7-131">-0</span></span>          | <span data-ttu-id="512b7-132">-0</span><span class="sxs-lookup"><span data-stu-id="512b7-132">-0</span></span>     | <span data-ttu-id="512b7-133">+0</span><span class="sxs-lookup"><span data-stu-id="512b7-133">+0</span></span>     | <span data-ttu-id="512b7-134">+0</span><span class="sxs-lookup"><span data-stu-id="512b7-134">+0</span></span>          | <span data-ttu-id="512b7-135">+ F</span><span class="sxs-lookup"><span data-stu-id="512b7-135">+F</span></span>     | <span data-ttu-id="512b7-136">+inf</span><span class="sxs-lookup"><span data-stu-id="512b7-136">+inf</span></span>     | <span data-ttu-id="512b7-137">NaN</span><span class="sxs-lookup"><span data-stu-id="512b7-137">NaN</span></span>     |



 

<span data-ttu-id="512b7-138">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="512b7-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="512b7-139">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="512b7-139">Vertex Shader</span></span> | <span data-ttu-id="512b7-140">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="512b7-140">Geometry Shader</span></span> | <span data-ttu-id="512b7-141">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="512b7-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="512b7-142">x</span><span class="sxs-lookup"><span data-stu-id="512b7-142">x</span></span>             | <span data-ttu-id="512b7-143">x</span><span class="sxs-lookup"><span data-stu-id="512b7-143">x</span></span>               | <span data-ttu-id="512b7-144">x</span><span class="sxs-lookup"><span data-stu-id="512b7-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="512b7-145">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="512b7-145">Minimum Shader Model</span></span>

<span data-ttu-id="512b7-146">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="512b7-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="512b7-147">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="512b7-147">Shader Model</span></span>                                              | <span data-ttu-id="512b7-148">Com suporte</span><span class="sxs-lookup"><span data-stu-id="512b7-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="512b7-149">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="512b7-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="512b7-150">sim</span><span class="sxs-lookup"><span data-stu-id="512b7-150">yes</span></span>       |
| [<span data-ttu-id="512b7-151">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="512b7-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="512b7-152">sim</span><span class="sxs-lookup"><span data-stu-id="512b7-152">yes</span></span>       |
| [<span data-ttu-id="512b7-153">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="512b7-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="512b7-154">sim</span><span class="sxs-lookup"><span data-stu-id="512b7-154">yes</span></span>       |
| [<span data-ttu-id="512b7-155">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="512b7-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="512b7-156">não</span><span class="sxs-lookup"><span data-stu-id="512b7-156">no</span></span>        |
| [<span data-ttu-id="512b7-157">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="512b7-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="512b7-158">não</span><span class="sxs-lookup"><span data-stu-id="512b7-158">no</span></span>        |
| [<span data-ttu-id="512b7-159">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="512b7-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="512b7-160">não</span><span class="sxs-lookup"><span data-stu-id="512b7-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="512b7-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="512b7-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="512b7-162">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="512b7-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





