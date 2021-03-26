---
title: vs_3_0
description: Um sombreador de vértice programável é composto de um conjunto de instruções que operam em dados de vértice. Registra dados de transferência dentro e fora da ALU. Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 22a0e6e84aff34dcec44713dc4382e391ad05c2b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103824041"
---
# <a name="vs_3_0"></a><span data-ttu-id="ee9cc-105">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ee9cc-105">vs\_3\_0</span></span>

<span data-ttu-id="ee9cc-106">Um sombreador de vértice programável é composto de um conjunto de instruções que operam em dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-106">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="ee9cc-107">Registra dados de transferência dentro e fora da ALU.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="ee9cc-108">Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="ee9cc-109">A versão do sombreador de vértice vs \_ 3 \_ 0 estende o conjunto de recursos com suporte do vs \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-109">Vertex shader version vs\_3\_0 extends the feature set supported by vs\_2\_x.</span></span> <span data-ttu-id="ee9cc-110">Cada um dos recursos do vs \_ 2 \_ X que exige um limite definido, está disponível no vs \_ 3 \_ 0 sem a necessidade do limite.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-110">Each of the features in vs\_2\_X that requires a cap to be set, is available in vs\_3\_0 without requiring the cap.</span></span>

-   <span data-ttu-id="ee9cc-111">[Instruções – vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contém uma lista das instruções disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-111">[Instructions - vs\_3\_0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="ee9cc-112">[Registros-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) lista os diferentes tipos de registros usados pela alu do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-112">[Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="ee9cc-113">Os [modificadores de registro do sombreador de vértice](dx9-graphics-reference-asm-vs-registers-modifiers.md) são usados para modificar a maneira como uma instrução funciona.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-113">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="ee9cc-114">[Modificadores de registro de origem do sombreador de vértice](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alteram os dados de registro de origem antes da execução da instrução.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-114">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="ee9cc-115">[O Swizzling de registro de origem](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-115">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="ee9cc-116">O [mascaramento do registro de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina quais componentes do registro de destino são gravados.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-116">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="ee9cc-117">Novos recursos</span><span class="sxs-lookup"><span data-stu-id="ee9cc-117">New Features</span></span>

<span data-ttu-id="ee9cc-118">Os novos recursos da versão do sombreador de vértice vs \_ 3 \_ 0 estão listados nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-118">New features of vertex shader version vs\_3\_0 are listed in the following sections.</span></span>

### <a name="indexing-registers"></a><span data-ttu-id="ee9cc-119">Registros de indexação</span><span class="sxs-lookup"><span data-stu-id="ee9cc-119">Indexing Registers</span></span>

<span data-ttu-id="ee9cc-120">Nos modelos de sombreador anteriores, somente o banco de registro constante pode ser indexado.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-120">In the earlier shader models, only the constant register bank could be indexed.</span></span> <span data-ttu-id="ee9cc-121">Nesse modelo, os seguintes bancos de registro podem ser indexados, usando o registro do contador de loop (aL):</span><span class="sxs-lookup"><span data-stu-id="ee9cc-121">In this model, the following register banks can be indexed, using the loop counter register (aL):</span></span>

-   <span data-ttu-id="ee9cc-122">Registro de entrada (v \# )</span><span class="sxs-lookup"><span data-stu-id="ee9cc-122">Input register (v\#)</span></span>
-   <span data-ttu-id="ee9cc-123">Registro de saída (o \# )</span><span class="sxs-lookup"><span data-stu-id="ee9cc-123">Output register (o\#)</span></span>

### <a name="vertex-textures"></a><span data-ttu-id="ee9cc-124">Texturas de vértice</span><span class="sxs-lookup"><span data-stu-id="ee9cc-124">Vertex Textures</span></span>

<span data-ttu-id="ee9cc-125">Este modelo de sombreador dá suporte à pesquisa de textura no sombreador de vértice usando texldl.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-125">This shader model supports texture lookup in the vertex shader using texldl.</span></span> <span data-ttu-id="ee9cc-126">O mecanismo de vértice tem quatro estágios de amostra de textura (distintos da amostra de mapa de deslocamento e dos exemplos de textura no mecanismo de pixel) que podem ser usados para exemplos de texturas definidas nesses estágios.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-126">The vertex engine has four texture sampler stages (distinct from the displacement map sampler and the texture samplers in the pixel engine) that can be used to sample textures set at those stages.</span></span> <span data-ttu-id="ee9cc-127">Confira [texturas de vértice no vs \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).</span><span class="sxs-lookup"><span data-stu-id="ee9cc-127">See [Vertex Textures in vs\_3\_0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).</span></span>

### <a name="vertex-stream-frequency"></a><span data-ttu-id="ee9cc-128">Frequência de fluxo de vértice</span><span class="sxs-lookup"><span data-stu-id="ee9cc-128">Vertex Stream Frequency</span></span>

<span data-ttu-id="ee9cc-129">Esse recurso permite que um subconjunto dos registros de entrada seja inicializado a uma taxa diferente de uma vez por vértice.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-129">This feature allows a subset of the input registers to be initialized at a rate different from once per vertex.</span></span> <span data-ttu-id="ee9cc-130">Consulte [desenho de geometria não indexada](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).</span><span class="sxs-lookup"><span data-stu-id="ee9cc-130">See [Drawing Non-Indexed Geometry](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).</span></span>

### <a name="shader-output"></a><span data-ttu-id="ee9cc-131">Saída de sombreador</span><span class="sxs-lookup"><span data-stu-id="ee9cc-131">Shader Output</span></span>

<span data-ttu-id="ee9cc-132">Semelhante ao vs \_ 2 \_ 0, a saída do sombreador pode variar com o controle de fluxo estático.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-132">Similar to vs\_2\_0, the output of the shader can vary with static flow control.</span></span> <span data-ttu-id="ee9cc-133">Tenha cuidado com a ramificação dinâmica, pois isso pode fazer com que as saídas de sombreador variem por vértice.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-133">Be careful with dynamic branching as this can cause shader outputs to vary per vertex.</span></span> <span data-ttu-id="ee9cc-134">Isso produzirá resultados imprevisíveis em hardwares diferentes.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-134">This will produce unpredictable results on different hardware.</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="ee9cc-135">Controle de fluxo dinâmico</span><span class="sxs-lookup"><span data-stu-id="ee9cc-135">Dynamic flow control</span></span>

<span data-ttu-id="ee9cc-136">Todas as instruções de controle de fluxo dinâmico têm suporte.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-136">All dynamic flow control instructions are supported.</span></span> <span data-ttu-id="ee9cc-137">O valor máximo de profundidade de aninhamento permitido é 24.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-137">The maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="ee9cc-138">(Consulte [limites de aninhamento de controle de fluxo](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para obter detalhes.)</span><span class="sxs-lookup"><span data-stu-id="ee9cc-138">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="temporary-registers"></a><span data-ttu-id="ee9cc-139">Registros temporários</span><span class="sxs-lookup"><span data-stu-id="ee9cc-139">Temporary Registers</span></span>

<span data-ttu-id="ee9cc-140">Há suporte para um total de 32 registros temporários (r \# ).</span><span class="sxs-lookup"><span data-stu-id="ee9cc-140">A total of 32 temporary registers (r\#) is supported.</span></span>

### <a name="static-flow-control"></a><span data-ttu-id="ee9cc-141">Controle de fluxo estático</span><span class="sxs-lookup"><span data-stu-id="ee9cc-141">Static Flow Control</span></span>

<span data-ttu-id="ee9cc-142">A profundidade máxima de aninhamento para [loop – vs](loop---vs.md) / [Rep-vs](rep---vs.md) é 4.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-142">The maximum nesting depth for [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) is 4.</span></span> <span data-ttu-id="ee9cc-143">A profundidade máxima de aninhamento para [Call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [callnz Pred-vs](callnz-pred---vs.md) é 4.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-143">The maximum nesting depth for [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[callnz pred - vs](callnz-pred---vs.md) is 4.</span></span> <span data-ttu-id="ee9cc-144">Para [se bool-vs](if-bool---vs.md), o valor máximo de profundidade de aninhamento permitido é 24.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-144">For [if bool - vs](if-bool---vs.md), the maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="ee9cc-145">(Consulte [limites de aninhamento de controle de fluxo](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para obter detalhes.)</span><span class="sxs-lookup"><span data-stu-id="ee9cc-145">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="predication"></a><span data-ttu-id="ee9cc-146">Predicação</span><span class="sxs-lookup"><span data-stu-id="ee9cc-146">Predication</span></span>

<span data-ttu-id="ee9cc-147">Há suporte para predicação de instrução.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-147">Instruction predication is supported.</span></span> <span data-ttu-id="ee9cc-148">Use [setp \_ comp-vs](setp-comp---vs.md) para definir o registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-148">Use [setp\_comp - vs](setp-comp---vs.md) to set the predicate register.</span></span>

### <a name="instruction-count"></a><span data-ttu-id="ee9cc-149">Contagem de instruções</span><span class="sxs-lookup"><span data-stu-id="ee9cc-149">Instruction Count</span></span>

<span data-ttu-id="ee9cc-150">Cada sombreador de vértice é permitido em qualquer lugar de 512 até o número de Slots em MaxVertexShader30InstructionSlots em [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="ee9cc-150">Each vertex shader is allowed anywhere from 512 up to the number of slots in MaxVertexShader30InstructionSlots in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span></span> <span data-ttu-id="ee9cc-151">O número de instruções executadas pode ser muito maior devido ao suporte de loop/representante; no entanto, isso é limitado por MaxVShaderInstructionsExecuted no D3DCAPS9 que deve ser pelo menos 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-151">The number of instructions run can be much higher because of the loop/rep support; however, this is capped by MaxVShaderInstructionsExecuted in D3DCAPS9 which should be at least 0xFFFF.</span></span>

### <a name="device-caps"></a><span data-ttu-id="ee9cc-152">Limites do dispositivo</span><span class="sxs-lookup"><span data-stu-id="ee9cc-152">Device Caps</span></span>

<span data-ttu-id="ee9cc-153">Se houver \_ suporte para o sombreador de vértice 3 0, as seguintes caps têm suporte no hardware (no mínimo):</span><span class="sxs-lookup"><span data-stu-id="ee9cc-153">If Vertex Shader 3\_0 is supported, the following caps are supported in hardware (at a minimum):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee9cc-154">Tampa</span><span class="sxs-lookup"><span data-stu-id="ee9cc-154">Cap</span></span></th>
<th><span data-ttu-id="ee9cc-155">Funcionalidade</span><span class="sxs-lookup"><span data-stu-id="ee9cc-155">Capability</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee9cc-156">Limites de sombreador</span><span class="sxs-lookup"><span data-stu-id="ee9cc-156">Shader caps</span></span></td>
<td><ul>
<li><span data-ttu-id="ee9cc-157">DynamicFlowControlDepth é 24</span><span class="sxs-lookup"><span data-stu-id="ee9cc-157">DynamicFlowControlDepth is 24</span></span></li>
<li><span data-ttu-id="ee9cc-158">NumTemps é 32</span><span class="sxs-lookup"><span data-stu-id="ee9cc-158">NumTemps is 32</span></span></li>
<li><span data-ttu-id="ee9cc-159">StaticFlowControlDepth é 4</span><span class="sxs-lookup"><span data-stu-id="ee9cc-159">StaticFlowControlDepth is 4</span></span></li>
<li><span data-ttu-id="ee9cc-160">Predicação tem suporte.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-160">Predication is supported.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee9cc-161">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span><span class="sxs-lookup"><span data-stu-id="ee9cc-161">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span></span></td>
<td><span data-ttu-id="ee9cc-162">8 K</span><span class="sxs-lookup"><span data-stu-id="ee9cc-162">8K</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee9cc-163">VertexShaderVersion</span><span class="sxs-lookup"><span data-stu-id="ee9cc-163">VertexShaderVersion</span></span></td>
<td><span data-ttu-id="ee9cc-164">3_0</span><span class="sxs-lookup"><span data-stu-id="ee9cc-164">3_0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee9cc-165">MaxVertexShaderConst</span><span class="sxs-lookup"><span data-stu-id="ee9cc-165">MaxVertexShaderConst</span></span></td>
<td><span data-ttu-id="ee9cc-166">256</span><span class="sxs-lookup"><span data-stu-id="ee9cc-166">256</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee9cc-167">MaxVertexShader30InstructionSlots</span><span class="sxs-lookup"><span data-stu-id="ee9cc-167">MaxVertexShader30InstructionSlots</span></span></td>
<td><span data-ttu-id="ee9cc-168">512</span><span class="sxs-lookup"><span data-stu-id="ee9cc-168">512</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee9cc-169">Suporte de neblina</span><span class="sxs-lookup"><span data-stu-id="ee9cc-169">Fog support</span></span></td>
<td><span data-ttu-id="ee9cc-170">D3DPRASTERCAPS_FOGVERTEX</span><span class="sxs-lookup"><span data-stu-id="ee9cc-170">D3DPRASTERCAPS_FOGVERTEX</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee9cc-171">VertexTextureFilterCaps</span><span class="sxs-lookup"><span data-stu-id="ee9cc-171">VertexTextureFilterCaps</span></span></td>
<td><ul>
<li><span data-ttu-id="ee9cc-172"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="ee9cc-172"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span></span></li>
<li><span data-ttu-id="ee9cc-173"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="ee9cc-173"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee9cc-174"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span><span class="sxs-lookup"><span data-stu-id="ee9cc-174"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span></span></td>
<td><span data-ttu-id="ee9cc-175">Os elementos de vértice em uma declaração de vértice podem compartilhar o mesmo deslocamento de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ee9cc-175">Vertex elements in a vertex declaration can share the same stream offset.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee9cc-176">Formatos de vértice</span><span class="sxs-lookup"><span data-stu-id="ee9cc-176">Vertex formats</span></span></td>
<td><ul>
<li><span data-ttu-id="ee9cc-177">D3DDECLTYPE_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="ee9cc-177">D3DDECLTYPE_UBYTE4</span></span></li>
<li><span data-ttu-id="ee9cc-178">D3DDECLTYPE_UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="ee9cc-178">D3DDECLTYPE_UBYTE4N</span></span></li>
<li><span data-ttu-id="ee9cc-179">D3DDECLTYPE_SHORT2N</span><span class="sxs-lookup"><span data-stu-id="ee9cc-179">D3DDECLTYPE_SHORT2N</span></span></li>
<li><span data-ttu-id="ee9cc-180">D3DDECLTYPE_SHORT4N</span><span class="sxs-lookup"><span data-stu-id="ee9cc-180">D3DDECLTYPE_SHORT4N</span></span></li>
<li><span data-ttu-id="ee9cc-181">D3DDECLTYPE_FLOAT16_2</span><span class="sxs-lookup"><span data-stu-id="ee9cc-181">D3DDECLTYPE_FLOAT16_2</span></span></li>
<li><span data-ttu-id="ee9cc-182">D3DDECLTYPE_FLOAT16_4</span><span class="sxs-lookup"><span data-stu-id="ee9cc-182">D3DDECLTYPE_FLOAT16_4</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ee9cc-183">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee9cc-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee9cc-184">Sombreadores de vértice</span><span class="sxs-lookup"><span data-stu-id="ee9cc-184">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 