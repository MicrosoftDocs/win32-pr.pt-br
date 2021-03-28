---
title: dmovc (SM5-ASM)
description: Movimentação condicional de componente. | dmovc (SM5-ASM)
ms.assetid: E376FE08-E251-4BE5-9F15-99B3B67A29C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e364e6340733c42ae69412db726851329eb2809d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104370856"
---
# <a name="dmovc-sm5---asm"></a><span data-ttu-id="af44a-104">dmovc (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="af44a-104">dmovc (sm5 - asm)</span></span>

<span data-ttu-id="af44a-105">Movimentação condicional de componente.</span><span class="sxs-lookup"><span data-stu-id="af44a-105">Component-wise conditional move.</span></span>



| <span data-ttu-id="af44a-106">dmovc \[ \_ SAT \] dest \[ . Mask \] , src0 \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="af44a-106">dmovc\[\_sat\] dest\[.mask\], src0\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\],</span></span> |
|-----------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="af44a-107">Item</span><span class="sxs-lookup"><span data-stu-id="af44a-107">Item</span></span>                                                            | <span data-ttu-id="af44a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="af44a-108">Description</span></span>                                                                                              |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af44a-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="af44a-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="af44a-110">\[no \] destino da movimentação.</span><span class="sxs-lookup"><span data-stu-id="af44a-110">\[in\] The move destination.</span></span><br/> <span data-ttu-id="af44a-111">Se *src0*, então *dest*  =  *src1* else   =  *src2*.</span><span class="sxs-lookup"><span data-stu-id="af44a-111">If *src0*, then *dest* = *src1* else *dest* = *src2*.</span></span><br/> |
| <span data-ttu-id="af44a-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="af44a-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="af44a-113">\[nos \] componentes para os quais testar a condição.</span><span class="sxs-lookup"><span data-stu-id="af44a-113">\[in\] The components to test the condition against.</span></span><br/>                                          |
| <span data-ttu-id="af44a-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="af44a-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="af44a-115">\[nos \] componentes a serem movidos, se a condição for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="af44a-115">\[in\] The components to move if the condition is true.</span></span><br/>                                       |
| <span data-ttu-id="af44a-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="af44a-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="af44a-117">\[nos \] componentes a serem movidos, se a condição for falsa.</span><span class="sxs-lookup"><span data-stu-id="af44a-117">\[in\] The components to move if the condition is false.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="af44a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="af44a-118">Remarks</span></span>

<span data-ttu-id="af44a-119">O exemplo a seguir mostra como usar essa instrução.</span><span class="sxs-lookup"><span data-stu-id="af44a-119">The following example shows how to use this instruction.</span></span>

``` syntax
                if(the dest mask contains .xy)
                {
                    if(the first 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the first double from src1 (post swizzle)
                        into dest.xy
                    }
                    else
                    {
                        copy the first double from src2 (post swizzle)
                        into dest.xy
                    }
                }
                if(the dest mask contains .zw)
                {
                    if(the second 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the second double from src1 (post swizzle)
                        into dest.zw
                    }
                    else
                    {
                        copy the second double from src2 (post swizzle)
                        into dest.zw
                    }
                }
```

<span data-ttu-id="af44a-120">As máscaras válidas para dest são. XY,. zw,. xyzw.</span><span class="sxs-lookup"><span data-stu-id="af44a-120">The valid masks for dest are .xy, .zw, .xyzw.</span></span>

<span data-ttu-id="af44a-121">O swizzles válido para *src0* é qualquer coisa.</span><span class="sxs-lookup"><span data-stu-id="af44a-121">The valid swizzles for *src0* are anything.</span></span> <span data-ttu-id="af44a-122">Os dois primeiros componentes swizzle são usados para facilitar valores de condição de 2 32 bits.</span><span class="sxs-lookup"><span data-stu-id="af44a-122">The first two components post-swizzle are used to indentify two 32-bit condition values.</span></span>

<span data-ttu-id="af44a-123">O swizzles válido para *src1* e *src2* contendo duplos são. xyzw,. xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="af44a-123">The valid swizzles for *src1* and *src2* containing doubles are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="af44a-124">são. XY,. zw e. xyzw.</span><span class="sxs-lookup"><span data-stu-id="af44a-124">are .xy, .zw, and .xyzw.</span></span>

<span data-ttu-id="af44a-125">Os seguintes mapeamentos *src* abaixo são swizzle:</span><span class="sxs-lookup"><span data-stu-id="af44a-125">The following *src* mappings below are post-swizzle:</span></span>

-   <span data-ttu-id="af44a-126">*dest* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="af44a-126">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="af44a-127">*src0* é um vec2 de 32 bits/componente entre x e y (ZW ignorado).</span><span class="sxs-lookup"><span data-stu-id="af44a-127">*src0* is a 32bit/component vec2 across x and y (zw ignored).</span></span>
-   <span data-ttu-id="af44a-128">*src1* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="af44a-128">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="af44a-129">*src2* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="af44a-129">*src2* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="af44a-130">Os modificadores em *src1* e *src2*, diferente de swizzle, assumem que os dados são duplos.</span><span class="sxs-lookup"><span data-stu-id="af44a-130">The modifiers on *src1* and *src2*, other than swizzle, assume the data is double.</span></span> <span data-ttu-id="af44a-131">A ausência de modificadores move dados sem alterar bits.</span><span class="sxs-lookup"><span data-stu-id="af44a-131">The absence of modifiers moves data without altering bits.</span></span>

<span data-ttu-id="af44a-132">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="af44a-132">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="af44a-133">Vértice</span><span class="sxs-lookup"><span data-stu-id="af44a-133">Vertex</span></span> | <span data-ttu-id="af44a-134">Envoltória</span><span class="sxs-lookup"><span data-stu-id="af44a-134">Hull</span></span> | <span data-ttu-id="af44a-135">Domínio</span><span class="sxs-lookup"><span data-stu-id="af44a-135">Domain</span></span> | <span data-ttu-id="af44a-136">Geometria</span><span class="sxs-lookup"><span data-stu-id="af44a-136">Geometry</span></span> | <span data-ttu-id="af44a-137">16x16</span><span class="sxs-lookup"><span data-stu-id="af44a-137">Pixel</span></span> | <span data-ttu-id="af44a-138">Computação</span><span class="sxs-lookup"><span data-stu-id="af44a-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="af44a-139">X</span><span class="sxs-lookup"><span data-stu-id="af44a-139">X</span></span>      | <span data-ttu-id="af44a-140">X</span><span class="sxs-lookup"><span data-stu-id="af44a-140">X</span></span>    | <span data-ttu-id="af44a-141">X</span><span class="sxs-lookup"><span data-stu-id="af44a-141">X</span></span>      | <span data-ttu-id="af44a-142">X</span><span class="sxs-lookup"><span data-stu-id="af44a-142">X</span></span>        | <span data-ttu-id="af44a-143">X</span><span class="sxs-lookup"><span data-stu-id="af44a-143">X</span></span>     | <span data-ttu-id="af44a-144">X</span><span class="sxs-lookup"><span data-stu-id="af44a-144">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="af44a-145">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="af44a-145">Minimum Shader Model</span></span>

<span data-ttu-id="af44a-146">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="af44a-146">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="af44a-147">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="af44a-147">Shader Model</span></span>                                              | <span data-ttu-id="af44a-148">Com suporte</span><span class="sxs-lookup"><span data-stu-id="af44a-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="af44a-149">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="af44a-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="af44a-150">sim</span><span class="sxs-lookup"><span data-stu-id="af44a-150">yes</span></span>       |
| [<span data-ttu-id="af44a-151">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="af44a-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="af44a-152">não</span><span class="sxs-lookup"><span data-stu-id="af44a-152">no</span></span>        |
| [<span data-ttu-id="af44a-153">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="af44a-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="af44a-154">não</span><span class="sxs-lookup"><span data-stu-id="af44a-154">no</span></span>        |
| [<span data-ttu-id="af44a-155">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af44a-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="af44a-156">não</span><span class="sxs-lookup"><span data-stu-id="af44a-156">no</span></span>        |
| [<span data-ttu-id="af44a-157">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af44a-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="af44a-158">não</span><span class="sxs-lookup"><span data-stu-id="af44a-158">no</span></span>        |
| [<span data-ttu-id="af44a-159">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af44a-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="af44a-160">não</span><span class="sxs-lookup"><span data-stu-id="af44a-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="af44a-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="af44a-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af44a-162">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af44a-162">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





