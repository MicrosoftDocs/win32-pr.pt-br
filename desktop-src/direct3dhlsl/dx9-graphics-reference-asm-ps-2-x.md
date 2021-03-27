---
title: ps_2_x
description: Um sombreador de pixel programável é composto de um conjunto de instruções que operam em dados de pixel. Registra dados de transferência dentro e fora da ALU. Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13e5daf7c3a4b41e5b27b1c20f8b1f5f8355c325
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988689"
---
# <a name="ps_2_x"></a><span data-ttu-id="12475-105">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="12475-105">ps\_2\_x</span></span>

<span data-ttu-id="12475-106">Um sombreador de pixel programável é composto de um conjunto de instruções que operam em dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="12475-106">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="12475-107">Registra dados de transferência dentro e fora da ALU.</span><span class="sxs-lookup"><span data-stu-id="12475-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="12475-108">Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.</span><span class="sxs-lookup"><span data-stu-id="12475-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="12475-109">[as \_ instruções do PS 2 \_ x](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contêm uma lista das instruções disponíveis.</span><span class="sxs-lookup"><span data-stu-id="12475-109">[ps\_2\_x Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="12475-110">[os \_ registros PS 2 \_ x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) lista os diferentes tipos de registros usados pela alu do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="12475-110">[ps\_2\_x Registers](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="12475-111">[Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) São usados para modificar a maneira como uma instrução funciona.</span><span class="sxs-lookup"><span data-stu-id="12475-111">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="12475-112">A [máscara de gravação do registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina quais componentes do registro de destino são gravados.</span><span class="sxs-lookup"><span data-stu-id="12475-112">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="12475-113">[Modificadores de registro de origem do sombreador de pixel](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alteram os dados de registro de origem antes da execução da instrução.</span><span class="sxs-lookup"><span data-stu-id="12475-113">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="12475-114">[O Swizzling de registro de origem](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.</span><span class="sxs-lookup"><span data-stu-id="12475-114">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="dynamic-flow-control"></a><span data-ttu-id="12475-115">Controle de fluxo dinâmico</span><span class="sxs-lookup"><span data-stu-id="12475-115">Dynamic Flow Control</span></span>

<span data-ttu-id="12475-116">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) representa a profundidade de aninhamento das instruções de controle de fluxo dinâmico: [If](if-bool---ps.md), If [ \_ comp](if-comp---ps.md), [If \_ Pred](if-pred---ps.md), [Break-PS](break---ps.md)e [Break \_ comp-PS](break-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="12475-116">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of dynamic flow control instructions: [if](if-bool---ps.md), [if\_comp](if-comp---ps.md), [if\_pred](if-pred---ps.md), [break - ps](break---ps.md), and [break\_comp - ps](break-comp---ps.md).</span></span> <span data-ttu-id="12475-117">O valor é igual à profundidade de aninhamento do bloco If \_ comp.</span><span class="sxs-lookup"><span data-stu-id="12475-117">The value is equal to the nesting depth of the if\_comp block.</span></span> <span data-ttu-id="12475-118">Se esse limite for zero, o dispositivo não oferecerá suporte a instruções de controle de fluxo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="12475-118">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

## <a name="number-of-temporary-registers"></a><span data-ttu-id="12475-119">Número de registros temporários</span><span class="sxs-lookup"><span data-stu-id="12475-119">Number of Temporary Registers</span></span>

<span data-ttu-id="12475-120">O número de registros temporários com suporte pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12475-120">The number of temporary registers supported by the device.</span></span> <span data-ttu-id="12475-121">O intervalo é de 12 a 32.</span><span class="sxs-lookup"><span data-stu-id="12475-121">The range is from 12 to 32.</span></span>

## <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="12475-122">Profundidade de aninhamento de controle de fluxo estático</span><span class="sxs-lookup"><span data-stu-id="12475-122">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="12475-123">[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) representa a profundidade de aninhamento de dois tipos de instruções de controle de fluxo estático: Rep- [loop](loop---ps.md)  / [](rep---ps.md) e [chamar](call---ps.md)  / [callnz](callnz-bool---ps.md).</span><span class="sxs-lookup"><span data-stu-id="12475-123">[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of two types of static flow control instructions: [loop](loop---ps.md) /[rep](rep---ps.md) And [call](call---ps.md) /[callnz](callnz-bool---ps.md).</span></span> <span data-ttu-id="12475-124">instruções de/rep de loop podem ser aninhadas até **StaticFlowControlDepth** de profundidade.</span><span class="sxs-lookup"><span data-stu-id="12475-124">loop /rep instructions can be nested up to **StaticFlowControlDepth** deep.</span></span> <span data-ttu-id="12475-125">Independentemente, as instruções Call/callnz podem ser aninhadas até **StaticFlowControlDepth** Deep.</span><span class="sxs-lookup"><span data-stu-id="12475-125">Independently, call /callnz instructions can be nested up to **StaticFlowControlDepth** deep.</span></span>

## <a name="number-of-instruction-slots"></a><span data-ttu-id="12475-126">Número de Slots de instrução</span><span class="sxs-lookup"><span data-stu-id="12475-126">Number of Instruction Slots</span></span>

<span data-ttu-id="12475-127">O número de Slots de instrução pode variar de 96 para um máximo de 512 e é especificado pelo [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span><span class="sxs-lookup"><span data-stu-id="12475-127">The number of instruction slots can range from 96 to a maximum of 512, and is specified by the [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span></span> <span data-ttu-id="12475-128">O número total de instruções que podem ser executadas é definido por **MaxPixelShaderInstructionsExecuted**.</span><span class="sxs-lookup"><span data-stu-id="12475-128">The total number of instructions that can run is defined by **MaxPixelShaderInstructionsExecuted**.</span></span> <span data-ttu-id="12475-129">Isso pode ser maior do que o número de Slots de instrução devido a chamadas de loop e sub-rotina.</span><span class="sxs-lookup"><span data-stu-id="12475-129">This can be larger than the number of instruction slots due to looping and subroutine calls.</span></span>

## <a name="arbitrary-swizzle"></a><span data-ttu-id="12475-130">Swizzle arbitrário</span><span class="sxs-lookup"><span data-stu-id="12475-130">Arbitrary Swizzle</span></span>

<span data-ttu-id="12475-131">Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) for definido, o swizzle arbitrário terá suporte.</span><span class="sxs-lookup"><span data-stu-id="12475-131">If [**D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, arbitrary swizzle is supported.</span></span> <span data-ttu-id="12475-132">Consulte [registro de origem Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="12475-132">See [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span></span>

## <a name="gradient-instructions"></a><span data-ttu-id="12475-133">Instruções de gradiente</span><span class="sxs-lookup"><span data-stu-id="12475-133">Gradient Instructions</span></span>

<span data-ttu-id="12475-134">Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) for definido, as instruções de gradiente serão suportadas.</span><span class="sxs-lookup"><span data-stu-id="12475-134">If [**D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, gradient instructions are supported.</span></span> <span data-ttu-id="12475-135">Consulte [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)e [texldd-PS](texldd---ps.md).</span><span class="sxs-lookup"><span data-stu-id="12475-135">See [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md), and [texldd - ps](texldd---ps.md).</span></span>

## <a name="predication"></a><span data-ttu-id="12475-136">Predicação</span><span class="sxs-lookup"><span data-stu-id="12475-136">Predication</span></span>

<span data-ttu-id="12475-137">Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ predicação**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) for definido, a instrução predicação terá suporte.</span><span class="sxs-lookup"><span data-stu-id="12475-137">If [**D3DD3DPSHADERCAPS2\_0\_PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, instruction predication is supported.</span></span> <span data-ttu-id="12475-138">Consulte [registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="12475-138">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>

## <a name="dependent-read-limit"></a><span data-ttu-id="12475-139">Limite de leitura dependente</span><span class="sxs-lookup"><span data-stu-id="12475-139">Dependent Read Limit</span></span>

<span data-ttu-id="12475-140">Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) for definido, não haverá nenhum limite de leitura dependente.</span><span class="sxs-lookup"><span data-stu-id="12475-140">If [**D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there are no dependent read limits.</span></span>

## <a name="texture-instruction-limit"></a><span data-ttu-id="12475-141">Limite de instrução de textura</span><span class="sxs-lookup"><span data-stu-id="12475-141">Texture Instruction Limit</span></span>

<span data-ttu-id="12475-142">Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) for definido, não haverá limite para instruções de textura.</span><span class="sxs-lookup"><span data-stu-id="12475-142">If [**D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there is no limit on texture instructions.</span></span>

## <a name="sampler-count"></a><span data-ttu-id="12475-143">Contagem de amostras</span><span class="sxs-lookup"><span data-stu-id="12475-143">Sampler Count</span></span>

<span data-ttu-id="12475-144">O número de amostragens de textura disponíveis é 16.</span><span class="sxs-lookup"><span data-stu-id="12475-144">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12475-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12475-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12475-146">Sombreadores de pixel</span><span class="sxs-lookup"><span data-stu-id="12475-146">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 