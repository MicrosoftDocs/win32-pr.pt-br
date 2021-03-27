---
title: Diferenças de sombreador de vértice
description: Diferenças de sombreador de vértice
ms.assetid: 94fe4033-94c0-4561-b0fd-1fb85d8f796b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c74603f9eab4ea91e9220bbaa172c0262aeda99
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007679"
---
# <a name="vertex-shader-differences"></a><span data-ttu-id="f6b8f-103">Diferenças de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="f6b8f-103">Vertex Shader Differences</span></span>

## <a name="instruction-slots"></a><span data-ttu-id="f6b8f-104">Slots de instrução</span><span class="sxs-lookup"><span data-stu-id="f6b8f-104">Instruction Slots</span></span>

<span data-ttu-id="f6b8f-105">Cada versão dá suporte a um número diferente de Slots de instrução máximos.</span><span class="sxs-lookup"><span data-stu-id="f6b8f-105">Each version supports a differing number of maximum instruction slots.</span></span>



| <span data-ttu-id="f6b8f-106">Versão</span><span class="sxs-lookup"><span data-stu-id="f6b8f-106">Version</span></span>  | <span data-ttu-id="f6b8f-107">Número máximo de Slots de instrução</span><span class="sxs-lookup"><span data-stu-id="f6b8f-107">Maximum number of instruction slots</span></span>                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6b8f-108">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f6b8f-108">vs\_1\_1</span></span> | <span data-ttu-id="f6b8f-109">128</span><span class="sxs-lookup"><span data-stu-id="f6b8f-109">128</span></span>                                                                                                                               |
| <span data-ttu-id="f6b8f-110">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f6b8f-110">vs\_2\_0</span></span> | <span data-ttu-id="f6b8f-111">256</span><span class="sxs-lookup"><span data-stu-id="f6b8f-111">256</span></span>                                                                                                                               |
| <span data-ttu-id="f6b8f-112">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f6b8f-112">vs\_2\_x</span></span> | <span data-ttu-id="f6b8f-113">256</span><span class="sxs-lookup"><span data-stu-id="f6b8f-113">256</span></span>                                                                                                                               |
| <span data-ttu-id="f6b8f-114">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f6b8f-114">vs\_3\_0</span></span> | <span data-ttu-id="f6b8f-115">mínimo de 512 e até o número de Slots em D3DCAPS9. MaxVertexShader30InstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="f6b8f-115">512 minimum, and up to the number of slots in D3DCAPS9.MaxVertexShader30InstructionSlots.</span></span> <span data-ttu-id="f6b8f-116">Consulte [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="f6b8f-116">See [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span></span> |



 

<span data-ttu-id="f6b8f-117">Para obter informações sobre as limitações de sombreadores de software, consulte [sombreadores de software](dx9-graphics-reference-asm-software-shaders.md).</span><span class="sxs-lookup"><span data-stu-id="f6b8f-117">For information about the limitations of software shaders, see [Software Shaders](dx9-graphics-reference-asm-software-shaders.md).</span></span>

## <a name="flow-control-nesting-limits"></a><span data-ttu-id="f6b8f-118">Limites de aninhamento de controle de fluxo</span><span class="sxs-lookup"><span data-stu-id="f6b8f-118">Flow Control Nesting Limits</span></span>

-   <span data-ttu-id="f6b8f-119">Consulte [limites de aninhamento de controle de fluxo](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="f6b8f-119">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>

## <a name="vs_1_1-features"></a><span data-ttu-id="f6b8f-120">vs \_ 1 \_ 1 recursos</span><span class="sxs-lookup"><span data-stu-id="f6b8f-120">vs\_1\_1 Features</span></span>

<span data-ttu-id="f6b8f-121">Novas instruções:</span><span class="sxs-lookup"><span data-stu-id="f6b8f-121">New instructions:</span></span>

<span data-ttu-id="f6b8f-122">Consulte [as instruções – vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).</span><span class="sxs-lookup"><span data-stu-id="f6b8f-122">See [Instructions - vs\_1\_1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).</span></span>

<span data-ttu-id="f6b8f-123">Novos registros:</span><span class="sxs-lookup"><span data-stu-id="f6b8f-123">New registers:</span></span>

<span data-ttu-id="f6b8f-124">Consulte [registros-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).</span><span class="sxs-lookup"><span data-stu-id="f6b8f-124">See [Registers - vs\_1\_1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).</span></span>

## <a name="vs_2_0-features"></a><span data-ttu-id="f6b8f-125">Recursos do vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f6b8f-125">vs\_2\_0 Features</span></span>

<span data-ttu-id="f6b8f-126">Novos recursos:</span><span class="sxs-lookup"><span data-stu-id="f6b8f-126">New features:</span></span>

-   <span data-ttu-id="f6b8f-127">Controle de fluxo estático</span><span class="sxs-lookup"><span data-stu-id="f6b8f-127">Static flow control</span></span>
-   <span data-ttu-id="f6b8f-128">Todos os quatro componentes do [registro de endereço](dx9-graphics-reference-asm-vs-registers-address.md) (a0) estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f6b8f-128">All four components of the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md) (a0) are available.</span></span>

<span data-ttu-id="f6b8f-129">Novas instruções:</span><span class="sxs-lookup"><span data-stu-id="f6b8f-129">New instructions:</span></span>

-   <span data-ttu-id="f6b8f-130">Instruções de instalação- [DEFB-vs](defb---vs.md), [defi-vs](defi---vs.md)</span><span class="sxs-lookup"><span data-stu-id="f6b8f-130">Setup instructions - [defb - vs](defb---vs.md), [defi - vs](defi---vs.md)</span></span>
-   <span data-ttu-id="f6b8f-131">Instruções aritméticas- [ABS-vs](abs---vs.md), [CRS-vs](crs---vs.md), [LRP-vs](lrp---vs.md), [mova-vs](mova---vs.md), [NRM-vs](nrm---vs.md), [pow-vs](pow---vs.md), [sgn-vs](sgn---vs.md), [Sincos-vs](sincos---vs.md)</span><span class="sxs-lookup"><span data-stu-id="f6b8f-131">Arithmetic instructions - [abs - vs](abs---vs.md), [crs - vs](crs---vs.md), [lrp - vs](lrp---vs.md), [mova - vs](mova---vs.md), [nrm - vs](nrm---vs.md), [pow - vs](pow---vs.md), [sgn - vs](sgn---vs.md), [sincos - vs](sincos---vs.md)</span></span>
-   <span data-ttu-id="f6b8f-132">Instruções de controle de fluxo estático- [Call-vs](call---vs.md), [callnz bool-vs](callnz-bool---vs.md), [senão-vs](else---vs.md), [endif-vs](endif---vs.md), [ENDLOOP-vs](endloop---vs.md), [endrep-vs](endrep---vs.md), [se bool-vs](if-bool---vs.md), [Label-](label---vs.md)vs, [loop](loop---vs.md)-vs, [Rep-vs](rep---vs.md), [RET-vs](ret---vs.md)</span><span class="sxs-lookup"><span data-stu-id="f6b8f-132">Static flow control instructions - [call - vs](call---vs.md), [callnz bool - vs](callnz-bool---vs.md), [else - vs](else---vs.md), [endif - vs](endif---vs.md), [endloop - vs](endloop---vs.md), [endrep - vs](endrep---vs.md), [if bool - vs](if-bool---vs.md), [label - vs](label---vs.md), [loop - vs](loop---vs.md), [rep - vs](rep---vs.md), [ret - vs](ret---vs.md)</span></span>

<span data-ttu-id="f6b8f-133">Novos registros:</span><span class="sxs-lookup"><span data-stu-id="f6b8f-133">New registers:</span></span>

-   <span data-ttu-id="f6b8f-134">[Registro booliano constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b \# )</span><span class="sxs-lookup"><span data-stu-id="f6b8f-134">[Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b\#)</span></span>
-   <span data-ttu-id="f6b8f-135">[Registro de inteiro constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i \# )</span><span class="sxs-lookup"><span data-stu-id="f6b8f-135">[Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i\#)</span></span>
-   <span data-ttu-id="f6b8f-136">[Registro do contador de loop](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al)</span><span class="sxs-lookup"><span data-stu-id="f6b8f-136">[Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL)</span></span>

## <a name="vs_2_x-features"></a><span data-ttu-id="f6b8f-137">Recursos do vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f6b8f-137">vs\_2\_x Features</span></span>

<span data-ttu-id="f6b8f-138">Novos recursos (D3DCAPS9. VS20Caps):</span><span class="sxs-lookup"><span data-stu-id="f6b8f-138">New features (D3DCAPS9.VS20Caps):</span></span>

-   <span data-ttu-id="f6b8f-139">Controle de fluxo dinâmico</span><span class="sxs-lookup"><span data-stu-id="f6b8f-139">Dynamic flow control</span></span>
-   <span data-ttu-id="f6b8f-140">Aninhamento de instruções de controle de fluxo dinâmicos e estáticas</span><span class="sxs-lookup"><span data-stu-id="f6b8f-140">Nesting for dynamic and static flow control instructions</span></span>
-   <span data-ttu-id="f6b8f-141">Número de s de [registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# ) aumentado</span><span class="sxs-lookup"><span data-stu-id="f6b8f-141">Number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s (r\#) increased</span></span>
-   <span data-ttu-id="f6b8f-142">Predicação</span><span class="sxs-lookup"><span data-stu-id="f6b8f-142">Predication</span></span>

<span data-ttu-id="f6b8f-143">Novas instruções:</span><span class="sxs-lookup"><span data-stu-id="f6b8f-143">New Instructions:</span></span>

-   <span data-ttu-id="f6b8f-144">Instruções de controle de fluxo dinâmico- [Break-vs](break---vs.md), [Break \_ comp-vs](break-comp---vs.md), [breakp-vs](breakp---vs.md), [callnz Pred-vs](callnz-pred---vs.md), [se \_ comp-vs](if-comp---vs.md), [se Pred-vs](if-pred---vs.md), [setp \_ comp-vs](setp-comp---vs.md)</span><span class="sxs-lookup"><span data-stu-id="f6b8f-144">Dynamic flow control instructions - [break - vs](break---vs.md), [break\_comp - vs](break-comp---vs.md), [breakp - vs](breakp---vs.md), [callnz pred - vs](callnz-pred---vs.md), [if\_comp - vs](if-comp---vs.md), [if pred - vs](if-pred---vs.md), [setp\_comp - vs](setp-comp---vs.md)</span></span>

<span data-ttu-id="f6b8f-145">Novos registros:</span><span class="sxs-lookup"><span data-stu-id="f6b8f-145">New registers:</span></span>

-   <span data-ttu-id="f6b8f-146">[Registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0)</span><span class="sxs-lookup"><span data-stu-id="f6b8f-146">[Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0)</span></span>

## <a name="vs_3_0-features"></a><span data-ttu-id="f6b8f-147">Recursos do vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f6b8f-147">vs\_3\_0 Features</span></span>

<span data-ttu-id="f6b8f-148">Novos recursos:</span><span class="sxs-lookup"><span data-stu-id="f6b8f-148">New features :</span></span>

-   <span data-ttu-id="f6b8f-149">Pesquisa de textura</span><span class="sxs-lookup"><span data-stu-id="f6b8f-149">Texture lookup</span></span>
-   <span data-ttu-id="f6b8f-150">Registros de [saída](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) indexáveis (o \# )</span><span class="sxs-lookup"><span data-stu-id="f6b8f-150">Indexable [Output Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#)</span></span>
-   <span data-ttu-id="f6b8f-151">Número de s de [registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# ) aumentado para 32</span><span class="sxs-lookup"><span data-stu-id="f6b8f-151">Number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s (r\#) increased to 32</span></span>

<span data-ttu-id="f6b8f-152">Novas instruções:</span><span class="sxs-lookup"><span data-stu-id="f6b8f-152">New instructions:</span></span>

-   <span data-ttu-id="f6b8f-153">Instrução de instalação [- \_ defaultsampletype (SM3-vs ASM)](dcl-samplertype---vs.md)</span><span class="sxs-lookup"><span data-stu-id="f6b8f-153">Setup instruction - [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md)</span></span>
-   <span data-ttu-id="f6b8f-154">Instrução de textura- [texldl-vs](texldl---vs.md)</span><span class="sxs-lookup"><span data-stu-id="f6b8f-154">Texture instruction - [texldl - vs](texldl---vs.md)</span></span>

<span data-ttu-id="f6b8f-155">Novos registros:</span><span class="sxs-lookup"><span data-stu-id="f6b8f-155">New registers:</span></span>

-   <span data-ttu-id="f6b8f-156">[Amostra (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s \# )</span><span class="sxs-lookup"><span data-stu-id="f6b8f-156">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s\#)</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6b8f-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6b8f-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6b8f-158">Sombreadores de vértice</span><span class="sxs-lookup"><span data-stu-id="f6b8f-158">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 