---
title: Diferenças de sombreador de pixel
description: Diferenças de sombreador de pixel
ms.assetid: 11aefb26-eb82-486c-81ff-7c0cfbab1b7a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a74b5cc7588220fdc5173c470f7852ee9ef763d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366201"
---
# <a name="pixel-shader-differences"></a><span data-ttu-id="a7b89-103">Diferenças de sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="a7b89-103">Pixel Shader Differences</span></span>

## <a name="instruction-slots"></a><span data-ttu-id="a7b89-104">Slots de instrução</span><span class="sxs-lookup"><span data-stu-id="a7b89-104">Instruction Slots</span></span>

<span data-ttu-id="a7b89-105">Cada versão dá suporte a um número diferente de Slots de instrução máximos.</span><span class="sxs-lookup"><span data-stu-id="a7b89-105">Each version supports a different number of maximum instruction slots.</span></span>



| <span data-ttu-id="a7b89-106">Versão</span><span class="sxs-lookup"><span data-stu-id="a7b89-106">Version</span></span>  | <span data-ttu-id="a7b89-107">Número máximo de Slots de instrução</span><span class="sxs-lookup"><span data-stu-id="a7b89-107">Maximum number of instruction slots</span></span>                                                                                   |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7b89-108">PS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a7b89-108">ps\_1\_1</span></span> | <span data-ttu-id="a7b89-109">4 texturas aritméticas + 8</span><span class="sxs-lookup"><span data-stu-id="a7b89-109">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="a7b89-110">PS \_ 1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="a7b89-110">ps\_1\_2</span></span> | <span data-ttu-id="a7b89-111">4 texturas aritméticas + 8</span><span class="sxs-lookup"><span data-stu-id="a7b89-111">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="a7b89-112">PS \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a7b89-112">ps\_1\_3</span></span> | <span data-ttu-id="a7b89-113">4 texturas aritméticas + 8</span><span class="sxs-lookup"><span data-stu-id="a7b89-113">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="a7b89-114">PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="a7b89-114">ps\_1\_4</span></span> | <span data-ttu-id="a7b89-115">6 texturas + 8 aritméticas por fase</span><span class="sxs-lookup"><span data-stu-id="a7b89-115">6 texture + 8 arithmetic per phase</span></span>                                                                                    |
| <span data-ttu-id="a7b89-116">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a7b89-116">ps\_2\_0</span></span> | <span data-ttu-id="a7b89-117">32 textura + aritmética de 64</span><span class="sxs-lookup"><span data-stu-id="a7b89-117">32 texture + 64 arithmetic</span></span>                                                                                            |
| <span data-ttu-id="a7b89-118">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a7b89-118">ps\_2\_x</span></span> | <span data-ttu-id="a7b89-119">mínimo de 96 e até o número de Slots em D3DCAPS9. D3DPSHADERCAPS2 \_ 0. NumInstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="a7b89-119">96 minimum, and up to the number of slots in D3DCAPS9.D3DPSHADERCAPS2\_0.NumInstructionSlots.</span></span> <span data-ttu-id="a7b89-120">Consulte D3DPSHADERCAPS2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="a7b89-120">See D3DPSHADERCAPS2\_0.</span></span> |
| <span data-ttu-id="a7b89-121">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a7b89-121">ps\_3\_0</span></span> | <span data-ttu-id="a7b89-122">mínimo de 512 e até o número de Slots em D3DCAPS9. MaxPixelShader30InstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="a7b89-122">512 minimum, and up to the number of slots in D3DCAPS9.MaxPixelShader30InstructionSlots.</span></span> <span data-ttu-id="a7b89-123">Consulte D3DPSHADERCAPS2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="a7b89-123">See D3DPSHADERCAPS2\_0.</span></span>      |



 

<span data-ttu-id="a7b89-124">Para obter informações sobre as limitações de sombreadores de software, consulte [sombreadores de software](dx9-graphics-reference-asm-software-shaders.md).</span><span class="sxs-lookup"><span data-stu-id="a7b89-124">For information about the limitations of software shaders, see [Software Shaders](dx9-graphics-reference-asm-software-shaders.md).</span></span>

## <a name="flow-control-nesting-limits"></a><span data-ttu-id="a7b89-125">Limites de aninhamento de controle de fluxo</span><span class="sxs-lookup"><span data-stu-id="a7b89-125">Flow Control Nesting Limits</span></span>

-   <span data-ttu-id="a7b89-126">Consulte [limitações de controle de fluxo](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="a7b89-126">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>

## <a name="ps_1_x-features"></a><span data-ttu-id="a7b89-127">\_recursos PS 1 \_ x</span><span class="sxs-lookup"><span data-stu-id="a7b89-127">ps\_1\_x Features</span></span>

<span data-ttu-id="a7b89-128">Novas instruções:</span><span class="sxs-lookup"><span data-stu-id="a7b89-128">New instructions:</span></span>

<span data-ttu-id="a7b89-129">Consulte [ \_ \_ as instruções PS 1 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="a7b89-129">See [ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md).</span></span>

<span data-ttu-id="a7b89-130">Novos registros:</span><span class="sxs-lookup"><span data-stu-id="a7b89-130">New registers:</span></span>

<span data-ttu-id="a7b89-131">Consulte [PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 PS 1 \_ \_ \_ \_ 3 \_ \_ PS \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="a7b89-131">See [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="ps_2_0-features"></a><span data-ttu-id="a7b89-132">Recursos do PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a7b89-132">ps\_2\_0 Features</span></span>

<span data-ttu-id="a7b89-133">Novos recursos:</span><span class="sxs-lookup"><span data-stu-id="a7b89-133">New features:</span></span>

-   <span data-ttu-id="a7b89-134">Três novas swizzles-. yzxw,. zxyw,. wzyx</span><span class="sxs-lookup"><span data-stu-id="a7b89-134">Three new swizzles - .yzxw, .zxyw, .wzyx</span></span>
-   <span data-ttu-id="a7b89-135">Número de [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) aumentado para 12</span><span class="sxs-lookup"><span data-stu-id="a7b89-135">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) increased to 12</span></span>
-   <span data-ttu-id="a7b89-136">Número de registros de [registro float de constante](dx9-graphics-reference-asm-ps-registers-constant-float.md) (c \# ) aumentado para 32</span><span class="sxs-lookup"><span data-stu-id="a7b89-136">Number of [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md) registers (c\#) increased to 32</span></span>
-   <span data-ttu-id="a7b89-137">Número de s (t) [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) \# aumentado para 8</span><span class="sxs-lookup"><span data-stu-id="a7b89-137">Number of [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)s (t\#) increased to 8</span></span>

<span data-ttu-id="a7b89-138">Novas instruções:</span><span class="sxs-lookup"><span data-stu-id="a7b89-138">New instructions:</span></span>

-   <span data-ttu-id="a7b89-139">Instruções de instalação- [DCL-(SM2, SM3-PS ASM)](dcl---ps.md), [DCL \_ SampleType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)</span><span class="sxs-lookup"><span data-stu-id="a7b89-139">Setup instructions - [dcl - (sm2, sm3 - ps asm)](dcl---ps.md), [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)</span></span>
-   <span data-ttu-id="a7b89-140">Instruções aritméticas [-ABS-PS](abs---ps.md), [CRS-PS](crs---ps.md), [dp2add-PS](dp2add---ps.md), [exp-PS](exp---ps.md), [FRC-PS](frc---ps.md), [log-PS](log---ps.md), [M3X2-PS](m3x2---ps.md), [m3x3-PS](m3x3---ps.md), [M3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md), [m4x4-](m4x4---ps.md)PS, [Max-](max---ps.md)PS, [min-PS](min---ps.md), [NRM-PS](nrm---ps.md), [pow-PS](pow---ps.md), [rcp-PS](rcp---ps.md), [RSQ-PS](rsq---ps.md), [Sincos-PS](sincos---ps.md)</span><span class="sxs-lookup"><span data-stu-id="a7b89-140">Arithmetic instructions - [abs - ps](abs---ps.md), [crs - ps](crs---ps.md), [dp2add - ps](dp2add---ps.md), [exp - ps](exp---ps.md), [frc - ps](frc---ps.md), [log - ps](log---ps.md), [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), [m4x4 - ps](m4x4---ps.md), [max - ps](max---ps.md), [min - ps](min---ps.md), [nrm - ps](nrm---ps.md), [pow - ps](pow---ps.md), [rcp - ps](rcp---ps.md), [rsq - ps](rsq---ps.md), [sincos - ps](sincos---ps.md)</span></span>
-   <span data-ttu-id="a7b89-141">Instruções de textura- [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md) (sintaxe diferente), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)</span><span class="sxs-lookup"><span data-stu-id="a7b89-141">Texture instructions - [texld - ps\_2\_0 and up](texld---ps-2-0.md) (different syntax), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)</span></span>

<span data-ttu-id="a7b89-142">Novos registros:</span><span class="sxs-lookup"><span data-stu-id="a7b89-142">New registers:</span></span>

-   <span data-ttu-id="a7b89-143">[Amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# )</span><span class="sxs-lookup"><span data-stu-id="a7b89-143">[Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#)</span></span>

## <a name="ps_2_x-features"></a><span data-ttu-id="a7b89-144">Recursos do PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a7b89-144">ps\_2\_x Features</span></span>

<span data-ttu-id="a7b89-145">Novos recursos (consulte [**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).):</span><span class="sxs-lookup"><span data-stu-id="a7b89-145">New features (See [**D3DPSHADERCAPS2\_0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).):</span></span>

-   <span data-ttu-id="a7b89-146">Controle de fluxo dinâmico</span><span class="sxs-lookup"><span data-stu-id="a7b89-146">Dynamic flow control</span></span>
-   <span data-ttu-id="a7b89-147">Controle de fluxo estático</span><span class="sxs-lookup"><span data-stu-id="a7b89-147">Static flow control</span></span>
-   <span data-ttu-id="a7b89-148">Aninhamento de instruções de controle de fluxo dinâmicos e estáticas</span><span class="sxs-lookup"><span data-stu-id="a7b89-148">Nesting for dynamic and static flow control instructions</span></span>
-   <span data-ttu-id="a7b89-149">Número de s de [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md)(r \# ) aumentado</span><span class="sxs-lookup"><span data-stu-id="a7b89-149">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md)s (r\#) increased</span></span>
-   <span data-ttu-id="a7b89-150">Swizzle de origem arbitrária</span><span class="sxs-lookup"><span data-stu-id="a7b89-150">Arbitrary source swizzle</span></span>
-   <span data-ttu-id="a7b89-151">Instruções de gradiente</span><span class="sxs-lookup"><span data-stu-id="a7b89-151">Gradient instructions</span></span>
-   <span data-ttu-id="a7b89-152">Predicação</span><span class="sxs-lookup"><span data-stu-id="a7b89-152">Predication</span></span>
-   <span data-ttu-id="a7b89-153">Nenhum limite de leitura de textura dependente</span><span class="sxs-lookup"><span data-stu-id="a7b89-153">No dependent texture read limit</span></span>
-   <span data-ttu-id="a7b89-154">Nenhum limite de instrução de textura</span><span class="sxs-lookup"><span data-stu-id="a7b89-154">No texture instruction limit</span></span>

<span data-ttu-id="a7b89-155">Novas instruções:</span><span class="sxs-lookup"><span data-stu-id="a7b89-155">New instructions:</span></span>

-   <span data-ttu-id="a7b89-156">Instruções de controle de fluxo estático- [se bool-PS](if-bool---ps.md), [Call-PS](call---ps.md), [callnz bool-PS](callnz-bool---ps.md), [else-PS](else---ps.md), [endif-PS](endif---ps.md), [Rep-PS](rep---ps.md), [endrep-PS](endrep---ps.md), [rótulo-PS](label---ps.md), [RET-PS](ret---ps.md)</span><span class="sxs-lookup"><span data-stu-id="a7b89-156">Static flow control instructions - [if bool - ps](if-bool---ps.md), [call - ps](call---ps.md), [callnz bool - ps](callnz-bool---ps.md), [else - ps](else---ps.md), [endif - ps](endif---ps.md), [rep - ps](rep---ps.md), [endrep - ps](endrep---ps.md), [label - ps](label---ps.md), [ret - ps](ret---ps.md)</span></span>
-   <span data-ttu-id="a7b89-157">Instruções de controle de fluxo dinâmico- [Break-PS](break---ps.md), [Break \_ comp-PS](break-comp---ps.md), [breakp-PS](break-p---ps.md), [callnz Pred-PS](callnz-pred---ps.md), [se \_ comp-PS](if-comp---ps.md), [se for Pred-PS](if-pred---ps.md), [setp \_ comp-PS](setp-comp---ps.md)</span><span class="sxs-lookup"><span data-stu-id="a7b89-157">Dynamic flow control instructions - [break - ps](break---ps.md), [break\_comp - ps](break-comp---ps.md), [breakp - ps](break-p---ps.md), [callnz pred - ps](callnz-pred---ps.md), [if\_comp - ps](if-comp---ps.md), [if pred - ps](if-pred---ps.md), [setp\_comp - ps](setp-comp---ps.md)</span></span>
-   <span data-ttu-id="a7b89-158">Instruções aritméticas- [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)</span><span class="sxs-lookup"><span data-stu-id="a7b89-158">Arithmetic instructions - [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)</span></span>
-   <span data-ttu-id="a7b89-159">Instrução de textura- [texldd-PS](texldd---ps.md)</span><span class="sxs-lookup"><span data-stu-id="a7b89-159">Texture instruction - [texldd - ps](texldd---ps.md)</span></span>

<span data-ttu-id="a7b89-160">Novos registros:</span><span class="sxs-lookup"><span data-stu-id="a7b89-160">New registers:</span></span>

-   <span data-ttu-id="a7b89-161">[Registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0)</span><span class="sxs-lookup"><span data-stu-id="a7b89-161">[Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0)</span></span>

## <a name="ps_3_0-features"></a><span data-ttu-id="a7b89-162">Recursos do PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a7b89-162">ps\_3\_0 Features</span></span>

<span data-ttu-id="a7b89-163">Novos recursos:</span><span class="sxs-lookup"><span data-stu-id="a7b89-163">New features:</span></span>

-   <span data-ttu-id="a7b89-164">10 [registros de entrada](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)consolidados s (v \# )</span><span class="sxs-lookup"><span data-stu-id="a7b89-164">Consolidated 10 [Input Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)s (v\#)</span></span>
-   <span data-ttu-id="a7b89-165">Registro de [cor de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) indexável (v \# ) com o [registro do contador de loop](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al)</span><span class="sxs-lookup"><span data-stu-id="a7b89-165">Indexable [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) with the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL)</span></span>
-   <span data-ttu-id="a7b89-166">Número de s de [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md)(r \# ) aumentado para 32</span><span class="sxs-lookup"><span data-stu-id="a7b89-166">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md)s (r\#) increased to 32</span></span>
-   <span data-ttu-id="a7b89-167">Número de [registros float de constante](dx9-graphics-reference-asm-ps-registers-constant-float.md)(c \# ) aumentados para 224</span><span class="sxs-lookup"><span data-stu-id="a7b89-167">Number of [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c\#) increased to 224</span></span>

<span data-ttu-id="a7b89-168">Novas instruções:</span><span class="sxs-lookup"><span data-stu-id="a7b89-168">New instructions:</span></span>

-   <span data-ttu-id="a7b89-169">Instrução de instalação [- \_ semântica DCL (SM3-PS ASM)](dcl-usage---ps.md)</span><span class="sxs-lookup"><span data-stu-id="a7b89-169">Setup instruction - [dcl\_semantics (sm3 - ps asm)](dcl-usage---ps.md)</span></span>
-   <span data-ttu-id="a7b89-170">Instruções de fluxo estático- [loop-PS](loop---ps.md), [ENDLOOP-PS](endloop---ps.md)</span><span class="sxs-lookup"><span data-stu-id="a7b89-170">Static flow instructions - [loop - ps](loop---ps.md), [endloop - ps](endloop---ps.md)</span></span>
-   <span data-ttu-id="a7b89-171">Instrução aritmética- [Sincos-PS](sincos---ps.md) (nova sintaxe)</span><span class="sxs-lookup"><span data-stu-id="a7b89-171">Arithmetic instruction - [sincos - ps](sincos---ps.md) (new syntax)</span></span>
-   <span data-ttu-id="a7b89-172">Instrução de textura- [texldl-PS](texldl---ps.md)</span><span class="sxs-lookup"><span data-stu-id="a7b89-172">Texture instruction - [texldl - ps](texldl---ps.md)</span></span>

<span data-ttu-id="a7b89-173">Novos registros:</span><span class="sxs-lookup"><span data-stu-id="a7b89-173">New registers:</span></span>

-   <span data-ttu-id="a7b89-174">[Registro de entrada](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# )</span><span class="sxs-lookup"><span data-stu-id="a7b89-174">[Input Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v\#)</span></span>
-   <span data-ttu-id="a7b89-175">[Registro de posição](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vPos)</span><span class="sxs-lookup"><span data-stu-id="a7b89-175">[Position Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vPos)</span></span>
-   <span data-ttu-id="a7b89-176">[Registro facial](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vFace)</span><span class="sxs-lookup"><span data-stu-id="a7b89-176">[Face Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vFace)</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7b89-177">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7b89-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7b89-178">Sombreadores de pixel</span><span class="sxs-lookup"><span data-stu-id="a7b89-178">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 