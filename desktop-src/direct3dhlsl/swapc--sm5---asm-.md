---
title: swapc (SM5-ASM)
description: Executa uma troca condicional inteligente de componentes dos valores entre dois registros de entrada.
ms.assetid: 3DFCEB82-076E-4AFA-915F-47390A355B7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d2ee674a1cb1067594b0e96c739ff8df73b152
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988585"
---
# <a name="swapc-sm5---asm"></a><span data-ttu-id="bf48d-103">swapc (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="bf48d-103">swapc (sm5 - asm)</span></span>

<span data-ttu-id="bf48d-104">Executa uma troca condicional inteligente de componentes dos valores entre dois registros de entrada.</span><span class="sxs-lookup"><span data-stu-id="bf48d-104">Performs a component-wise conditional swap of the values between two input registers.</span></span>



| <span data-ttu-id="bf48d-105">swapc dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle \] , src2 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="bf48d-105">swapc dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="bf48d-106">Item</span><span class="sxs-lookup"><span data-stu-id="bf48d-106">Item</span></span>                                                               | <span data-ttu-id="bf48d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf48d-107">Description</span></span>                                                                                     |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf48d-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="bf48d-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="bf48d-109">\[em \] registrar com máscaras de gravação não vazias arbitrárias.</span><span class="sxs-lookup"><span data-stu-id="bf48d-109">\[in\] Register with arbitrary nonempty write masks.</span></span> <span data-ttu-id="bf48d-110">Deve ser diferente de *dest1*.</span><span class="sxs-lookup"><span data-stu-id="bf48d-110">Must be different than *dest1*.</span></span><br/> |
| <span data-ttu-id="bf48d-111"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="bf48d-111"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="bf48d-112">\[em \] registrar com máscaras de gravação não vazias arbitrárias.</span><span class="sxs-lookup"><span data-stu-id="bf48d-112">\[in\] Register with arbitrary nonempty write masks.</span></span> <span data-ttu-id="bf48d-113">Deve ser diferente de *dest0*.</span><span class="sxs-lookup"><span data-stu-id="bf48d-113">Must be different than *dest0*.</span></span><br/> |
| <span data-ttu-id="bf48d-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="bf48d-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="bf48d-115">\[o no \] fornece 4 condições.</span><span class="sxs-lookup"><span data-stu-id="bf48d-115">\[in\] Provides 4 conditions.</span></span> <span data-ttu-id="bf48d-116">Um valor inteiro diferente de zero significa **true**.</span><span class="sxs-lookup"><span data-stu-id="bf48d-116">A nonzero integer value means **true**.</span></span> <br/>               |
| <span data-ttu-id="bf48d-117"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="bf48d-117"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="bf48d-118">\[em \] um dos valores a serem trocados.</span><span class="sxs-lookup"><span data-stu-id="bf48d-118">\[in\] One of the values to be swapped.</span></span><br/>                                              |
| <span data-ttu-id="bf48d-119"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="bf48d-119"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/>    | <span data-ttu-id="bf48d-120">\[em \] um dos valores a serem trocados.</span><span class="sxs-lookup"><span data-stu-id="bf48d-120">\[in\] One of the values to be swapped.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="bf48d-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf48d-121">Remarks</span></span>

<span data-ttu-id="bf48d-122">A codificação dessa instrução tenta expressar compactar várias trocas condicionais paralelas de escalares entre os registros de 2 4 componentes, com flexibilidade secundária na disposição dos pares de números envolvidos na troca.</span><span class="sxs-lookup"><span data-stu-id="bf48d-122">The encoding of this instruction attempts to compactly express multiple parallel conditional swaps of scalars across two 4-component registers, with minor flexibility in the arrangement of the pairs of numbers involved in swapping.</span></span>

<span data-ttu-id="bf48d-123">A escolha de Register e Value para *src0*, *src1* e *src2* não são restringidas de forma alguma, como [movc](movc--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="bf48d-123">The choice of register and value for *src0*, *src1*, and *src2* are unconstrained in any way, like [movc](movc--sm4---asm-.md).</span></span>

<span data-ttu-id="bf48d-124">A semântica dessa instrução pode ser descrita pelas operações equivalentes com a instrução **movc** .</span><span class="sxs-lookup"><span data-stu-id="bf48d-124">The semantics of this instruction can be described by the equivalent operations with the **movc** instruction.</span></span> <span data-ttu-id="bf48d-125">O pior caso é mostrado no exemplo a seguir, garantindo que os registros de destino não sejam atualizados até o final.</span><span class="sxs-lookup"><span data-stu-id="bf48d-125">The worst case is shown in the following example, making sure destination registers are not updated until the end.</span></span>

``` syntax
                swapc dest0[.mask], 
                      dest1[.mask],
                      src0[.swizzle],
                      src1[.swizzle],
                      src2[.swizzle]

                expands to:

                movc temp[dest0 s mask], 
                     src0[.swizzle], 
                     src2[.swizzle], src1[.swizzle]

                movc dest1[.mask], 
                     src0[.swizzle], 
                     src1[.swizzle], src2[.swizzle]

                mov  dest0.mask, temp
```

<span data-ttu-id="bf48d-126">Você pode escolher como lidar com a tarefa, se não diretamente.</span><span class="sxs-lookup"><span data-stu-id="bf48d-126">You can choose how to tackle the task, if not directly.</span></span> <span data-ttu-id="bf48d-127">Por exemplo, o mesmo efeito pode ser obtido por uma sequência de até quatro trocas condicionais simples, ou como acima, duas instruções de **movc** de vetor, além de qualquer sobrecarga para garantir que os valores de origem não sejam sobrescritodos por operações anteriores no meio da expansão.</span><span class="sxs-lookup"><span data-stu-id="bf48d-127">For example, the same effect can be achieved by a sequence of up to 4 simple scalar conditional swaps, or as above, two vector **movc** instructions, plus any overhead to make sure the source values are not clobbered by earlier operations in the midst of the expansion.</span></span>

<span data-ttu-id="bf48d-128">Use esta instrução para classificação.</span><span class="sxs-lookup"><span data-stu-id="bf48d-128">Use this instruction for sorting.</span></span>

<span data-ttu-id="bf48d-129">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="bf48d-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bf48d-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="bf48d-130">Vertex</span></span> | <span data-ttu-id="bf48d-131">Envoltória</span><span class="sxs-lookup"><span data-stu-id="bf48d-131">Hull</span></span> | <span data-ttu-id="bf48d-132">Domínio</span><span class="sxs-lookup"><span data-stu-id="bf48d-132">Domain</span></span> | <span data-ttu-id="bf48d-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="bf48d-133">Geometry</span></span> | <span data-ttu-id="bf48d-134">16x16</span><span class="sxs-lookup"><span data-stu-id="bf48d-134">Pixel</span></span> | <span data-ttu-id="bf48d-135">Computação</span><span class="sxs-lookup"><span data-stu-id="bf48d-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bf48d-136">X</span><span class="sxs-lookup"><span data-stu-id="bf48d-136">X</span></span>      | <span data-ttu-id="bf48d-137">X</span><span class="sxs-lookup"><span data-stu-id="bf48d-137">X</span></span>    | <span data-ttu-id="bf48d-138">X</span><span class="sxs-lookup"><span data-stu-id="bf48d-138">X</span></span>      | <span data-ttu-id="bf48d-139">X</span><span class="sxs-lookup"><span data-stu-id="bf48d-139">X</span></span>        | <span data-ttu-id="bf48d-140">X</span><span class="sxs-lookup"><span data-stu-id="bf48d-140">X</span></span>     | <span data-ttu-id="bf48d-141">X</span><span class="sxs-lookup"><span data-stu-id="bf48d-141">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bf48d-142">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="bf48d-142">Minimum Shader Model</span></span>

<span data-ttu-id="bf48d-143">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="bf48d-143">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="bf48d-144">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="bf48d-144">Shader Model</span></span>                                              | <span data-ttu-id="bf48d-145">Com suporte</span><span class="sxs-lookup"><span data-stu-id="bf48d-145">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bf48d-146">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="bf48d-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bf48d-147">sim</span><span class="sxs-lookup"><span data-stu-id="bf48d-147">yes</span></span>       |
| [<span data-ttu-id="bf48d-148">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="bf48d-148">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bf48d-149">não</span><span class="sxs-lookup"><span data-stu-id="bf48d-149">no</span></span>        |
| [<span data-ttu-id="bf48d-150">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="bf48d-150">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bf48d-151">não</span><span class="sxs-lookup"><span data-stu-id="bf48d-151">no</span></span>        |
| [<span data-ttu-id="bf48d-152">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf48d-152">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bf48d-153">não</span><span class="sxs-lookup"><span data-stu-id="bf48d-153">no</span></span>        |
| [<span data-ttu-id="bf48d-154">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf48d-154">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bf48d-155">não</span><span class="sxs-lookup"><span data-stu-id="bf48d-155">no</span></span>        |
| [<span data-ttu-id="bf48d-156">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf48d-156">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bf48d-157">não</span><span class="sxs-lookup"><span data-stu-id="bf48d-157">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bf48d-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf48d-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf48d-159">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf48d-159">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





