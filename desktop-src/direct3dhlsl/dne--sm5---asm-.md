---
title: DNE (SM5-ASM)
description: Não há comparação de precisão dupla por componente.
ms.assetid: 7C69A86D-0820-4640-AF5A-2993EC77D2AA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae00e0e5f4c0269b14a7a0f330d5af8760a1312f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365238"
---
# <a name="dne-sm5---asm"></a><span data-ttu-id="11ce0-103">DNE (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="11ce0-103">dne (sm5 - asm)</span></span>

<span data-ttu-id="11ce0-104">Não há comparação de precisão dupla por componente.</span><span class="sxs-lookup"><span data-stu-id="11ce0-104">Component-wise double-precision not equality comparison.</span></span>



| <span data-ttu-id="11ce0-105">DNE \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="11ce0-105">dne\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="11ce0-106">Item</span><span class="sxs-lookup"><span data-stu-id="11ce0-106">Item</span></span>                                                            | <span data-ttu-id="11ce0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="11ce0-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="11ce0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="11ce0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="11ce0-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="11ce0-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="11ce0-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="11ce0-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="11ce0-111">\[nos \] componentes para comparar com *src1*.</span><span class="sxs-lookup"><span data-stu-id="11ce0-111">\[in\] The components to compare with *src1*.</span></span><br/>      |
| <span data-ttu-id="11ce0-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="11ce0-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="11ce0-113">\[nos \] componentes para comparar com *src0*.</span><span class="sxs-lookup"><span data-stu-id="11ce0-113">\[in\] The components to compare with *src0*.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="11ce0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="11ce0-114">Remarks</span></span>

<span data-ttu-id="11ce0-115">Essa instrução executa a comparação de ponto flutuante de precisão dupla (*src0* ! = *src1*) para cada componente e grava o resultado em *dest*.</span><span class="sxs-lookup"><span data-stu-id="11ce0-115">This instruction performs the double-precision floating-point comparison (*src0* != *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="11ce0-116">Se a comparação for verdadeira, 32-bit 0xFFFFFFFF será retornado para esse componente.</span><span class="sxs-lookup"><span data-stu-id="11ce0-116">If the comparison is true, then 32-bit 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="11ce0-117">Caso contrário, 32 bits 0x00000000 será retornado.</span><span class="sxs-lookup"><span data-stu-id="11ce0-117">Otherwise 32-bit 0x00000000 is returned.</span></span>

<span data-ttu-id="11ce0-118">A comparação com NaN retorna true.</span><span class="sxs-lookup"><span data-stu-id="11ce0-118">Comparison with NaN returns true.</span></span>

<span data-ttu-id="11ce0-119">As máscaras de *destino* válidas são um ou dois componentes.</span><span class="sxs-lookup"><span data-stu-id="11ce0-119">The valid *dest* masks are any one or two components.</span></span> <span data-ttu-id="11ce0-120">Isto é:. x,. y,. z,. w,. XY,. XZ,. XW,. yz,. YW,. zw o primeiro componente de *destino* na máscara recebe o resultado de 32 bits para a primeira comparação dupla.</span><span class="sxs-lookup"><span data-stu-id="11ce0-120">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The first *dest* component in the mask receives the 32-bit result for the first double comparison.</span></span> <span data-ttu-id="11ce0-121">O segundo componente na máscara, se presente, recebe o resultado de 32 bits para a segunda comparação dupla.</span><span class="sxs-lookup"><span data-stu-id="11ce0-121">The second component in the mask, if present, receives the 32-bit result for the second double comparison.</span></span>

<span data-ttu-id="11ce0-122">O swizzles válido para os parâmetros de origem são. xyzw,. xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="11ce0-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="11ce0-123">Os seguintes mapeamentos *src* são swizzle:</span><span class="sxs-lookup"><span data-stu-id="11ce0-123">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="11ce0-124">*src0* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="11ce0-124">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="11ce0-125">*src1* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="11ce0-125">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="11ce0-126">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="11ce0-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="11ce0-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="11ce0-127">Vertex</span></span> | <span data-ttu-id="11ce0-128">Envoltória</span><span class="sxs-lookup"><span data-stu-id="11ce0-128">Hull</span></span> | <span data-ttu-id="11ce0-129">Domínio</span><span class="sxs-lookup"><span data-stu-id="11ce0-129">Domain</span></span> | <span data-ttu-id="11ce0-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="11ce0-130">Geometry</span></span> | <span data-ttu-id="11ce0-131">16x16</span><span class="sxs-lookup"><span data-stu-id="11ce0-131">Pixel</span></span> | <span data-ttu-id="11ce0-132">Computação</span><span class="sxs-lookup"><span data-stu-id="11ce0-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="11ce0-133">X</span><span class="sxs-lookup"><span data-stu-id="11ce0-133">X</span></span>      | <span data-ttu-id="11ce0-134">X</span><span class="sxs-lookup"><span data-stu-id="11ce0-134">X</span></span>    | <span data-ttu-id="11ce0-135">X</span><span class="sxs-lookup"><span data-stu-id="11ce0-135">X</span></span>      | <span data-ttu-id="11ce0-136">X</span><span class="sxs-lookup"><span data-stu-id="11ce0-136">X</span></span>        | <span data-ttu-id="11ce0-137">X</span><span class="sxs-lookup"><span data-stu-id="11ce0-137">X</span></span>     | <span data-ttu-id="11ce0-138">X</span><span class="sxs-lookup"><span data-stu-id="11ce0-138">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="11ce0-139">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="11ce0-139">Minimum Shader Model</span></span>

<span data-ttu-id="11ce0-140">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="11ce0-140">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="11ce0-141">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="11ce0-141">Shader Model</span></span>                                              | <span data-ttu-id="11ce0-142">Com suporte</span><span class="sxs-lookup"><span data-stu-id="11ce0-142">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="11ce0-143">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="11ce0-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="11ce0-144">sim</span><span class="sxs-lookup"><span data-stu-id="11ce0-144">yes</span></span>       |
| [<span data-ttu-id="11ce0-145">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="11ce0-145">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="11ce0-146">não</span><span class="sxs-lookup"><span data-stu-id="11ce0-146">no</span></span>        |
| [<span data-ttu-id="11ce0-147">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="11ce0-147">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="11ce0-148">não</span><span class="sxs-lookup"><span data-stu-id="11ce0-148">no</span></span>        |
| [<span data-ttu-id="11ce0-149">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11ce0-149">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="11ce0-150">não</span><span class="sxs-lookup"><span data-stu-id="11ce0-150">no</span></span>        |
| [<span data-ttu-id="11ce0-151">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11ce0-151">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="11ce0-152">não</span><span class="sxs-lookup"><span data-stu-id="11ce0-152">no</span></span>        |
| [<span data-ttu-id="11ce0-153">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11ce0-153">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="11ce0-154">não</span><span class="sxs-lookup"><span data-stu-id="11ce0-154">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="11ce0-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11ce0-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11ce0-156">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11ce0-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





