---
title: vs_2_x
description: Saiba mais sobre vs_2_x, um sombreador de vértice programável, que é composto de um conjunto de instruções que operam em dados de vértice.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3449ae4c1e1eb3b977916f6fb1d19303e9d21a4e
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010710"
---
# <a name="vs_2_x"></a><span data-ttu-id="3296c-103">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3296c-103">vs\_2\_x</span></span>

<span data-ttu-id="3296c-104">Um sombreador de vértice programável é composto de um conjunto de instruções que operam em dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="3296c-104">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="3296c-105">Registra dados de transferência dentro e fora da ALU.</span><span class="sxs-lookup"><span data-stu-id="3296c-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="3296c-106">Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.</span><span class="sxs-lookup"><span data-stu-id="3296c-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="3296c-107">A versão do sombreador de vértice vs \_ 2 \_ x estende o conjunto de recursos com suporte do vs \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="3296c-107">Vertex shader version vs\_2\_x extends the feature set supported by vs\_2\_0.</span></span> <span data-ttu-id="3296c-108">Cada recurso adicional é representado por uma Cap correspondente na estrutura [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) dentro de [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps).</span><span class="sxs-lookup"><span data-stu-id="3296c-108">Each additional feature is represented by a corresponding cap in the [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) structure within [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps).</span></span> <span data-ttu-id="3296c-109">Para usar qualquer um dos recursos aprimorados representados por esses limites, a versão do sombreador de vértice deve ser especificada como vs \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="3296c-109">To use any of the enhanced features represented by these caps, the vertex shader version must be specified as vs\_2\_x.</span></span>

-   <span data-ttu-id="3296c-110">[Instruções – vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contém uma lista das instruções disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3296c-110">[Instructions - vs\_2\_x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="3296c-111">[Registros-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) lista os diferentes tipos de registros usados pela alu do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="3296c-111">[Registers - vs\_2\_x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="3296c-112">Os [modificadores de registro do sombreador de vértice](dx9-graphics-reference-asm-vs-registers-modifiers.md) são usados para modificar a maneira como uma instrução funciona.</span><span class="sxs-lookup"><span data-stu-id="3296c-112">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="3296c-113">[Modificadores de registro de origem do sombreador de vértice](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alteram os dados de registro de origem antes da execução da instrução.</span><span class="sxs-lookup"><span data-stu-id="3296c-113">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="3296c-114">[O Swizzling de registro de origem](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.</span><span class="sxs-lookup"><span data-stu-id="3296c-114">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="3296c-115">O [mascaramento do registro de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina quais componentes do registro de destino são gravados.</span><span class="sxs-lookup"><span data-stu-id="3296c-115">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="3296c-116">Novos recursos</span><span class="sxs-lookup"><span data-stu-id="3296c-116">New Features</span></span>

<span data-ttu-id="3296c-117">Os novos recursos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="3296c-117">New features are as follows:</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="3296c-118">Controle de fluxo dinâmico</span><span class="sxs-lookup"><span data-stu-id="3296c-118">Dynamic Flow Control</span></span>

<span data-ttu-id="3296c-119">Se [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, as instruções de controle de fluxo dinâmico a seguir têm suporte:</span><span class="sxs-lookup"><span data-stu-id="3296c-119">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, then the following dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="3296c-120">Se \_ comp-vs</span><span class="sxs-lookup"><span data-stu-id="3296c-120">if\_comp - vs</span></span>](if-comp---vs.md)
-   [<span data-ttu-id="3296c-121">interrupção vs</span><span class="sxs-lookup"><span data-stu-id="3296c-121">break - vs</span></span>](break---vs.md)
-   [<span data-ttu-id="3296c-122">interromper \_ comp-vs</span><span class="sxs-lookup"><span data-stu-id="3296c-122">break\_comp - vs</span></span>](break-comp---vs.md)

<span data-ttu-id="3296c-123">Se [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) também for definido, as seguintes instruções adicionais de controle de fluxo têm suporte:</span><span class="sxs-lookup"><span data-stu-id="3296c-123">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is also set, the following additional flow control instructions are supported:</span></span>

-   [<span data-ttu-id="3296c-124">setp \_ comp-vs</span><span class="sxs-lookup"><span data-stu-id="3296c-124">setp\_comp - vs</span></span>](setp-comp---vs.md)
-   [<span data-ttu-id="3296c-125">se Pred-vs</span><span class="sxs-lookup"><span data-stu-id="3296c-125">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="3296c-126">callnz Pred – vs</span><span class="sxs-lookup"><span data-stu-id="3296c-126">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="3296c-127">breakp-vs</span><span class="sxs-lookup"><span data-stu-id="3296c-127">breakp - vs</span></span>](breakp---vs.md)

<span data-ttu-id="3296c-128">O intervalo de valores para a profundidade do controle de fluxo dinâmico é de 0 a 24 e é igual à profundidade de aninhamento das instruções de controle de fluxo dinâmico (consulte [limites de aninhamento de controle de fluxo](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="3296c-128">The range of values for dynamic flow control depth is 0 to 24 and is equal to the nesting depth of the dynamic flow control instructions (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span> <span data-ttu-id="3296c-129">Se esse limite for zero, o dispositivo não oferecerá suporte a instruções de controle de fluxo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="3296c-129">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

### <a name="number-of-temporary-registers"></a><span data-ttu-id="3296c-130">Número de registros temporários</span><span class="sxs-lookup"><span data-stu-id="3296c-130">Number of Temporary Registers</span></span>

<span data-ttu-id="3296c-131">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) representa o número de s de [registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md)com suporte no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3296c-131">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s supported by the device.</span></span> <span data-ttu-id="3296c-132">O intervalo de valores para esse limite é de 12 a 32.</span><span class="sxs-lookup"><span data-stu-id="3296c-132">The range of values for this cap is 12 to 32.</span></span>

### <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="3296c-133">Profundidade de aninhamento de controle de fluxo estático</span><span class="sxs-lookup"><span data-stu-id="3296c-133">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="3296c-134">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) representa a profundidade de aninhamento de dois tipos de instruções de controle de fluxo estático: [loop-](loop---vs.md)vs e Call-vs-vs / [](rep---vs.md) [](call---vs.md) / [callnz bool-](callnz-bool---vs.md)vs / [se bool-vs](if-bool---vs.md). loop-vs/Rep-vs as instruções podem ser aninhadas até D3DVS20CAPS Deep.</span><span class="sxs-lookup"><span data-stu-id="3296c-134">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the nesting depth of two types of static flow control instructions: [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) and [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[if bool - vs](if-bool---vs.md). loop - vs/rep - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="3296c-135">Independentemente, as instruções de Call-vs/callnz bool-vs podem ser aninhadas até D3DVS20CAPS Deep.</span><span class="sxs-lookup"><span data-stu-id="3296c-135">Independently, call - vs/callnz bool - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="3296c-136">Se D3DVS20CAPS também for definido, [callnz Pred-vs](callnz-pred---vs.md) será contado em direção à profundidade de aninhamento de Call-vs/callnz bool-vs/If bool-vs (consulte [limites de aninhamento de controle de fluxo](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="3296c-136">If D3DVS20CAPS is also set, then [callnz pred - vs](callnz-pred---vs.md) is counted toward the nesting depth of call - vs/callnz bool - vs/if bool - vs (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span>

### <a name="predication"></a><span data-ttu-id="3296c-137">Predicação</span><span class="sxs-lookup"><span data-stu-id="3296c-137">Predication</span></span>

<span data-ttu-id="3296c-138">Se [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) for definido, o dispositivo dará suporte a [setp \_ comp-vs](setp-comp---vs.md) e predicação de instrução.</span><span class="sxs-lookup"><span data-stu-id="3296c-138">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is set, the device supports [setp\_comp - vs](setp-comp---vs.md) and instruction predication.</span></span> <span data-ttu-id="3296c-139">Se D3DVS20CAPS também for maior que 0, as instruções de controle de fluxo dinâmico adicionais a seguir têm suporte:</span><span class="sxs-lookup"><span data-stu-id="3296c-139">If D3DVS20CAPS is also greater than 0, then the following additional dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="3296c-140">se Pred-vs</span><span class="sxs-lookup"><span data-stu-id="3296c-140">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="3296c-141">callnz Pred – vs</span><span class="sxs-lookup"><span data-stu-id="3296c-141">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="3296c-142">breakp-vs</span><span class="sxs-lookup"><span data-stu-id="3296c-142">breakp - vs</span></span>](breakp---vs.md)

### <a name="instruction-count"></a><span data-ttu-id="3296c-143">Contagem de instruções</span><span class="sxs-lookup"><span data-stu-id="3296c-143">Instruction Count</span></span>

<span data-ttu-id="3296c-144">Cada sombreador de vértice pode ter até 256 instruções armazenadas.</span><span class="sxs-lookup"><span data-stu-id="3296c-144">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="3296c-145">O número de instruções executadas pode ser muito maior (devido ao suporte de loop/Rep) e é limitado por [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), que deve ser pelo menos 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="3296c-145">The number of instructions run can be much higher (because of the loop/rep support), and is capped by [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3296c-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3296c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3296c-147">Sombreadores de vértice</span><span class="sxs-lookup"><span data-stu-id="3296c-147">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 