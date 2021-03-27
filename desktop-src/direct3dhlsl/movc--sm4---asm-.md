---
title: movc (sm4-ASM)
description: Movimentação condicional de componente. | movc (sm4-ASM)
ms.assetid: B7F19DF5-282F-41D4-AE2D-6ACF61A42088
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91aa3116b7bc13102386c57c9b8c63d3534147a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989182"
---
# <a name="movc-sm4---asm"></a><span data-ttu-id="84e70-104">movc (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="84e70-104">movc (sm4 - asm)</span></span>

<span data-ttu-id="84e70-105">Movimentação condicional de componente.</span><span class="sxs-lookup"><span data-stu-id="84e70-105">Component-wise conditional move.</span></span>



| <span data-ttu-id="84e70-106">movc \[ \_ SAT \] dest \[ . Mask \] , src0 \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="84e70-106">movc\[\_sat\] dest\[.mask\], src0\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="84e70-107">Item</span><span class="sxs-lookup"><span data-stu-id="84e70-107">Item</span></span>                                                            | <span data-ttu-id="84e70-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="84e70-108">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84e70-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="84e70-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="84e70-110">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="84e70-110">\[in\] The address of the result of the operation.</span></span> <br/> <span data-ttu-id="84e70-111">Se *src0*, então *dest*  =  *src1* else   =  *src2*</span><span class="sxs-lookup"><span data-stu-id="84e70-111">If *src0*, then *dest* = *src1* else *dest* = *src2*</span></span><br/> |
| <span data-ttu-id="84e70-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="84e70-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="84e70-113">\[nos \] componentes nos quais testar a condição.</span><span class="sxs-lookup"><span data-stu-id="84e70-113">\[in\] The components on which to test the condition.</span></span><br/>                                                               |
| <span data-ttu-id="84e70-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="84e70-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="84e70-115">\[nos \] componentes a serem movidos.</span><span class="sxs-lookup"><span data-stu-id="84e70-115">\[in\] The components to move.</span></span> <br/>                                                                                     |
| <span data-ttu-id="84e70-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="84e70-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="84e70-117">\[nos \] componentes a serem movidos.</span><span class="sxs-lookup"><span data-stu-id="84e70-117">\[in\] The components to move.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="84e70-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="84e70-118">Remarks</span></span>

<span data-ttu-id="84e70-119">O exemplo a seguir mostra como usar essa instrução.</span><span class="sxs-lookup"><span data-stu-id="84e70-119">The following example shows how to use this instruction.</span></span>

``` syntax
                for each component in dest[.mask]
                    if the corresponding component in src0 (POS-swizzle)
                       has any bit set
                    {
                        copy this component (POS-swizzle) from src1 into dest
                    }
                    else
                    {
                        copy this component (POS-swizzle) from src2 into dest
                    }
                endfor
```

<span data-ttu-id="84e70-120">Os modificadores em *src1* e *src2*, diferente de swizzle, assumem que os dados são de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="84e70-120">The modifiers on *src1* and *src2*, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="84e70-121">A ausência de modificadores apenas move dados sem alterar bits.</span><span class="sxs-lookup"><span data-stu-id="84e70-121">The absence of modifiers just moves data without altering bits.</span></span>

<span data-ttu-id="84e70-122">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="84e70-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="84e70-123">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="84e70-123">Vertex Shader</span></span> | <span data-ttu-id="84e70-124">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="84e70-124">Geometry Shader</span></span> | <span data-ttu-id="84e70-125">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="84e70-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="84e70-126">x</span><span class="sxs-lookup"><span data-stu-id="84e70-126">x</span></span>             | <span data-ttu-id="84e70-127">x</span><span class="sxs-lookup"><span data-stu-id="84e70-127">x</span></span>               | <span data-ttu-id="84e70-128">x</span><span class="sxs-lookup"><span data-stu-id="84e70-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="84e70-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="84e70-129">Minimum Shader Model</span></span>

<span data-ttu-id="84e70-130">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="84e70-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="84e70-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="84e70-131">Shader Model</span></span>                                              | <span data-ttu-id="84e70-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="84e70-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="84e70-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="84e70-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="84e70-134">sim</span><span class="sxs-lookup"><span data-stu-id="84e70-134">yes</span></span>       |
| [<span data-ttu-id="84e70-135">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="84e70-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="84e70-136">sim</span><span class="sxs-lookup"><span data-stu-id="84e70-136">yes</span></span>       |
| [<span data-ttu-id="84e70-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="84e70-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="84e70-138">sim</span><span class="sxs-lookup"><span data-stu-id="84e70-138">yes</span></span>       |
| [<span data-ttu-id="84e70-139">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="84e70-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="84e70-140">não</span><span class="sxs-lookup"><span data-stu-id="84e70-140">no</span></span>        |
| [<span data-ttu-id="84e70-141">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="84e70-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="84e70-142">não</span><span class="sxs-lookup"><span data-stu-id="84e70-142">no</span></span>        |
| [<span data-ttu-id="84e70-143">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="84e70-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="84e70-144">não</span><span class="sxs-lookup"><span data-stu-id="84e70-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="84e70-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="84e70-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84e70-146">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="84e70-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





