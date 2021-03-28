---
title: Constantes D3DCOMPILE (D3DCompiler. h)
description: As constantes D3DCOMPILE especificam como o compilador compila o código HLSL.
ms.assetid: 039627DD-D6A4-4EA3-8E91-D2A20770E6FF
topic_type:
- apiref
api_name:
- D3DCOMPILE_DEBUG
- D3DCOMPILE_SKIP_VALIDATION
- D3DCOMPILE_SKIP_OPTIMIZATION
- D3DCOMPILE_PACK_MATRIX_ROW_MAJOR
- D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR
- D3DCOMPILE_PARTIAL_PRECISION
- D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT
- D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT
- D3DCOMPILE_NO_PRESHADER
- D3DCOMPILE_AVOID_FLOW_CONTROL
- D3DCOMPILE_PREFER_FLOW_CONTROL
- D3DCOMPILE_ENABLE_STRICTNESS
- D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY
- D3DCOMPILE_IEEE_STRICTNESS
- D3DCOMPILE_OPTIMIZATION_LEVEL0
- D3DCOMPILE_OPTIMIZATION_LEVEL1
- D3DCOMPILE_OPTIMIZATION_LEVEL2
- D3DCOMPILE_OPTIMIZATION_LEVEL3
- D3DCOMPILE_WARNINGS_ARE_ERRORS
- D3DCOMPILE_RESOURCES_MAY_ALIAS
- D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES
- D3DCOMPILE_ALL_RESOURCES_BOUND
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfd396eef06260ae879a3bb816d0bd89a078ea53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172941"
---
# <a name="d3dcompile-constants"></a><span data-ttu-id="f642c-103">Constantes D3DCOMPILE</span><span class="sxs-lookup"><span data-stu-id="f642c-103">D3DCOMPILE Constants</span></span>

<span data-ttu-id="f642c-104">As constantes D3DCOMPILE especificam como o compilador compila o código HLSL.</span><span class="sxs-lookup"><span data-stu-id="f642c-104">The D3DCOMPILE constants specify how the compiler compiles the HLSL code.</span></span>

<dl> <dt>

<span data-ttu-id="f642c-105"><span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**\_Depuração D3DCOMPILE**</span><span class="sxs-lookup"><span data-stu-id="f642c-105"><span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**D3DCOMPILE\_DEBUG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-106">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="f642c-106">(1 << 0)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-107">Direciona o compilador para inserir informações de arquivo/linha/tipo/símbolo de depuração no código de saída.</span><span class="sxs-lookup"><span data-stu-id="f642c-107">Directs the compiler to insert debug file/line/type/symbol information into the output code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-108"><span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE \_ ignorar \_ validação**</span><span class="sxs-lookup"><span data-stu-id="f642c-108"><span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE\_SKIP\_VALIDATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-109">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="f642c-109">(1 << 1)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-110">Instrui o compilador a não validar o código gerado em relação a recursos e restrições conhecidos.</span><span class="sxs-lookup"><span data-stu-id="f642c-110">Directs the compiler not to validate the generated code against known capabilities and constraints.</span></span> <span data-ttu-id="f642c-111">É recomendável que você use essa constante apenas com sombreadores que foram compilados com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="f642c-111">We recommend that you use this constant only with shaders that have been successfully compiled in the past.</span></span> <span data-ttu-id="f642c-112">O DirectX sempre valida os sombreadores antes de defini-los para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f642c-112">DirectX always validates shaders before it sets them to a device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-113"><span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**D3DCOMPILE \_ ignorar \_ otimização**</span><span class="sxs-lookup"><span data-stu-id="f642c-113"><span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**D3DCOMPILE\_SKIP\_OPTIMIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-114">(1 << 2)</span><span class="sxs-lookup"><span data-stu-id="f642c-114">(1 << 2)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-115">Direciona o compilador para ignorar as etapas de otimização durante a geração de código.</span><span class="sxs-lookup"><span data-stu-id="f642c-115">Directs the compiler to skip optimization steps during code generation.</span></span> <span data-ttu-id="f642c-116">É recomendável que você defina essa constante somente para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="f642c-116">We recommend that you set this constant for debug purposes only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-117"><span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**Linha de matriz do pacote de D3DCOMPILE \_ \_ \_ \_ principal**</span><span class="sxs-lookup"><span data-stu-id="f642c-117"><span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**D3DCOMPILE\_PACK\_MATRIX\_ROW\_MAJOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-118">(1 << 3)</span><span class="sxs-lookup"><span data-stu-id="f642c-118">(1 << 3)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-119">Direciona o compilador para pacotes de matrizes em ordem de linha principal na entrada e na saída do sombreador.</span><span class="sxs-lookup"><span data-stu-id="f642c-119">Directs the compiler to pack matrices in row-major order on input and output from the shader.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-120"><span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**\_Coluna de matriz de pacote D3DCOMPILE \_ \_ \_ principal**</span><span class="sxs-lookup"><span data-stu-id="f642c-120"><span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**D3DCOMPILE\_PACK\_MATRIX\_COLUMN\_MAJOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-121">(1 << 4)</span><span class="sxs-lookup"><span data-stu-id="f642c-121">(1 << 4)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-122">Direciona o compilador para pacotes de matrizes na ordem principal da coluna na entrada e na saída do sombreador.</span><span class="sxs-lookup"><span data-stu-id="f642c-122">Directs the compiler to pack matrices in column-major order on input and output from the shader.</span></span> <span data-ttu-id="f642c-123">Esse tipo de empacotamento é geralmente mais eficiente, pois uma série de produtos de ponto pode executar a multiplicação de matriz de vetor.</span><span class="sxs-lookup"><span data-stu-id="f642c-123">This type of packing is generally more efficient because a series of dot-products can then perform vector-matrix multiplication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-124"><span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**\_Precisão parcial do D3DCOMPILE \_**</span><span class="sxs-lookup"><span data-stu-id="f642c-124"><span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**D3DCOMPILE\_PARTIAL\_PRECISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-125">(1 << 5)</span><span class="sxs-lookup"><span data-stu-id="f642c-125">(1 << 5)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-126">Direciona o compilador para executar todos os cálculos com precisão parcial.</span><span class="sxs-lookup"><span data-stu-id="f642c-126">Directs the compiler to perform all computations with partial precision.</span></span> <span data-ttu-id="f642c-127">Se você definir essa constante, o código compilado poderá ser executado mais rapidamente em algum hardware.</span><span class="sxs-lookup"><span data-stu-id="f642c-127">If you set this constant, the compiled code might run faster on some hardware.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-128"><span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE \_ Force \_ vs \_ software \_ sem \_ aceitar**</span><span class="sxs-lookup"><span data-stu-id="f642c-128"><span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE\_FORCE\_VS\_SOFTWARE\_NO\_OPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-129">(1 << 6)</span><span class="sxs-lookup"><span data-stu-id="f642c-129">(1 << 6)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-130">Direciona o compilador para compilar um sombreador de vértice para o próximo perfil de sombreador mais alto.</span><span class="sxs-lookup"><span data-stu-id="f642c-130">Directs the compiler to compile a vertex shader for the next highest shader profile.</span></span> <span data-ttu-id="f642c-131">Essa constante ativa a depuração e otimizações.</span><span class="sxs-lookup"><span data-stu-id="f642c-131">This constant turns debugging on and optimizations off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-132"><span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE \_ forçar \_ o \_ software PS \_ não \_ aceitar**</span><span class="sxs-lookup"><span data-stu-id="f642c-132"><span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE\_FORCE\_PS\_SOFTWARE\_NO\_OPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-133">(1 << 7)</span><span class="sxs-lookup"><span data-stu-id="f642c-133">(1 << 7)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-134">Direciona o compilador para compilar um sombreador de pixel para o próximo perfil de sombreador mais alto.</span><span class="sxs-lookup"><span data-stu-id="f642c-134">Directs the compiler to compile a pixel shader for the next highest shader profile.</span></span> <span data-ttu-id="f642c-135">Essa constante também ativa a depuração e otimizações.</span><span class="sxs-lookup"><span data-stu-id="f642c-135">This constant also turns debugging on and optimizations off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-136"><span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE \_ sem \_ preshadr**</span><span class="sxs-lookup"><span data-stu-id="f642c-136"><span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE\_NO\_PRESHADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-137">(1 << 8)</span><span class="sxs-lookup"><span data-stu-id="f642c-137">(1 << 8)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-138">Direciona o compilador para desabilitar os preshaders.</span><span class="sxs-lookup"><span data-stu-id="f642c-138">Directs the compiler to disable Preshaders.</span></span> <span data-ttu-id="f642c-139">Se você definir essa constante, o compilador não extrairá a expressão estática para avaliação.</span><span class="sxs-lookup"><span data-stu-id="f642c-139">If you set this constant, the compiler does not pull out static expression for evaluation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-140"><span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE \_ evitar \_ controle de fluxo \_**</span><span class="sxs-lookup"><span data-stu-id="f642c-140"><span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE\_AVOID\_FLOW\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-141">(1 << 9)</span><span class="sxs-lookup"><span data-stu-id="f642c-141">(1 << 9)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-142">Instrui o compilador a não usar construções de controle de fluxo sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="f642c-142">Directs the compiler to not use flow-control constructs where possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-143"><span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE \_ prefiro \_ o \_ controle de fluxo**</span><span class="sxs-lookup"><span data-stu-id="f642c-143"><span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE\_PREFER\_FLOW\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-144">(1 << 10)</span><span class="sxs-lookup"><span data-stu-id="f642c-144">(1 << 10)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-145">Instrui o compilador a usar construções de controle de fluxo sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="f642c-145">Directs the compiler to use flow-control constructs where possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-146"><span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE \_ habilitar \_ restrição**</span><span class="sxs-lookup"><span data-stu-id="f642c-146"><span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE\_ENABLE\_STRICTNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-147">(1 << 11)</span><span class="sxs-lookup"><span data-stu-id="f642c-147">(1 << 11)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-148">Força a compilação estrita, que pode não permitir a sintaxe herdada.</span><span class="sxs-lookup"><span data-stu-id="f642c-148">Forces strict compile, which might not allow for legacy syntax.</span></span>

<span data-ttu-id="f642c-149">Por padrão, o compilador desabilita a restrição na sintaxe preterida.</span><span class="sxs-lookup"><span data-stu-id="f642c-149">By default, the compiler disables strictness on deprecated syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-150"><span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE \_ habilitar a \_ compatibilidade com versões anteriores \_**</span><span class="sxs-lookup"><span data-stu-id="f642c-150"><span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE\_ENABLE\_BACKWARDS\_COMPATIBILITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-151">(1 << 12)</span><span class="sxs-lookup"><span data-stu-id="f642c-151">(1 << 12)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-152">Direciona o compilador para permitir que os sombreadores mais antigos sejam compilados em destinos de 5 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="f642c-152">Directs the compiler to enable older shaders to compile to 5\_0 targets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-153"><span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE \_ IEEE \_ Strict**</span><span class="sxs-lookup"><span data-stu-id="f642c-153"><span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE\_IEEE\_STRICTNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-154">(1 << 13)</span><span class="sxs-lookup"><span data-stu-id="f642c-154">(1 << 13)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-155">Força a compilação IEEE estrita.</span><span class="sxs-lookup"><span data-stu-id="f642c-155">Forces the IEEE strict compile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-156"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**D3DCOMPILE \_ otimização \_ LEVEL0**</span><span class="sxs-lookup"><span data-stu-id="f642c-156"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-157">(1 << 14)</span><span class="sxs-lookup"><span data-stu-id="f642c-157">(1 << 14)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-158">Direciona o compilador para usar o nível de otimização mais baixo.</span><span class="sxs-lookup"><span data-stu-id="f642c-158">Directs the compiler to use the lowest optimization level.</span></span> <span data-ttu-id="f642c-159">Se você definir essa constante, o compilador poderá produzir um código mais lento, mas produzirá o código mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="f642c-159">If you set this constant, the compiler might produce slower code but produces the code more quickly.</span></span> <span data-ttu-id="f642c-160">Defina essa constante ao desenvolver o sombreador iterativamente.</span><span class="sxs-lookup"><span data-stu-id="f642c-160">Set this constant when you develop the shader iteratively.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-161"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**D3DCOMPILE \_ otimização \_ LEVEL1**</span><span class="sxs-lookup"><span data-stu-id="f642c-161"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-162">0</span><span class="sxs-lookup"><span data-stu-id="f642c-162">0</span></span>
</dt> <dt>



<span data-ttu-id="f642c-163">Direciona o compilador para usar o segundo nível de otimização mais baixo.</span><span class="sxs-lookup"><span data-stu-id="f642c-163">Directs the compiler to use the second lowest optimization level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-164"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**D3DCOMPILE \_ otimização \_ LEVEL2**</span><span class="sxs-lookup"><span data-stu-id="f642c-164"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-165">((1 << 14) \| (1 << 15))</span><span class="sxs-lookup"><span data-stu-id="f642c-165">((1 << 14) \| (1 << 15))</span></span>
</dt> <dt>



<span data-ttu-id="f642c-166">Direciona o compilador para usar o segundo nível de otimização mais alto.</span><span class="sxs-lookup"><span data-stu-id="f642c-166">Directs the compiler to use the second highest optimization level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-167"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**D3DCOMPILE \_ otimização \_ LEVEL3**</span><span class="sxs-lookup"><span data-stu-id="f642c-167"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-168">(1 << 15)</span><span class="sxs-lookup"><span data-stu-id="f642c-168">(1 << 15)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-169">Direciona o compilador para usar o nível de otimização mais alto.</span><span class="sxs-lookup"><span data-stu-id="f642c-169">Directs the compiler to use the highest optimization level.</span></span> <span data-ttu-id="f642c-170">Se você definir essa constante, o compilador produzirá o melhor código possível, mas poderá levar muito mais tempo para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="f642c-170">If you set this constant, the compiler produces the best possible code but might take significantly longer to do so.</span></span> <span data-ttu-id="f642c-171">Defina essa constante para as compilações finais de um aplicativo quando o desempenho for o fator mais importante.</span><span class="sxs-lookup"><span data-stu-id="f642c-171">Set this constant for final builds of an application when performance is the most important factor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-172"><span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**\_Avisos D3DCOMPILE \_ são \_ erros**</span><span class="sxs-lookup"><span data-stu-id="f642c-172"><span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**D3DCOMPILE\_WARNINGS\_ARE\_ERRORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-173">(1 << 18)</span><span class="sxs-lookup"><span data-stu-id="f642c-173">(1 << 18)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-174">Direciona o compilador para tratar todos os avisos como erros ao compilar o código do sombreador.</span><span class="sxs-lookup"><span data-stu-id="f642c-174">Directs the compiler to treat all warnings as errors when it compiles the shader code.</span></span> <span data-ttu-id="f642c-175">Recomendamos que você use essa constante para o novo código de sombreador, para que você possa resolver todos os avisos e reduzir o número de defeitos de código difíceis de encontrar.</span><span class="sxs-lookup"><span data-stu-id="f642c-175">We recommend that you use this constant for new shader code, so that you can resolve all warnings and lower the number of hard-to-find code defects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-176"><span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**D3DCOMPILE de \_ recursos \_ podem \_ alias**</span><span class="sxs-lookup"><span data-stu-id="f642c-176"><span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**D3DCOMPILE\_RESOURCES\_MAY\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-177">(1 << 19)</span><span class="sxs-lookup"><span data-stu-id="f642c-177">(1 << 19)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-178">Direciona o compilador para pressupor que os modos de exibição de acesso não ordenados (UAVs) e do Shader Resource views (SRVs) podem ser alias para cs \_ 5 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="f642c-178">Directs the compiler to assume that unordered access views (UAVs) and shader resource views (SRVs) may alias for cs\_5\_0.</span></span>

> [!Note]  
> <span data-ttu-id="f642c-179">Essa constante do compilador é nova começando com o \_47.dll D3dcompiler.</span><span class="sxs-lookup"><span data-stu-id="f642c-179">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-180"><span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE \_ habilitar \_ \_ tabelas de DESCRITOr não associado \_**</span><span class="sxs-lookup"><span data-stu-id="f642c-180"><span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE\_ENABLE\_UNBOUNDED\_DESCRIPTOR\_TABLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-181">(1 << 20)</span><span class="sxs-lookup"><span data-stu-id="f642c-181">(1 << 20)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-182">Direciona o compilador para habilitar tabelas de descritor não associadas.</span><span class="sxs-lookup"><span data-stu-id="f642c-182">Directs the compiler to enable unbounded descriptor tables.</span></span>

> [!Note]  
> <span data-ttu-id="f642c-183">Essa constante do compilador é nova começando com o \_47.dll D3dcompiler.</span><span class="sxs-lookup"><span data-stu-id="f642c-183">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="f642c-184"><span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE \_ todos os \_ recursos \_ associados**</span><span class="sxs-lookup"><span data-stu-id="f642c-184"><span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE\_ALL\_RESOURCES\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f642c-185">(1 << 21)</span><span class="sxs-lookup"><span data-stu-id="f642c-185">(1 << 21)</span></span>
</dt> <dt>



<span data-ttu-id="f642c-186">Direciona o compilador para garantir que todos os recursos estejam associados.</span><span class="sxs-lookup"><span data-stu-id="f642c-186">Directs the compiler to ensure all resources are bound.</span></span>

> [!Note]  
> <span data-ttu-id="f642c-187">Essa constante do compilador é nova começando com o \_47.dll D3dcompiler.</span><span class="sxs-lookup"><span data-stu-id="f642c-187">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f642c-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f642c-188">Requirements</span></span>



| <span data-ttu-id="f642c-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="f642c-189">Requirement</span></span> | <span data-ttu-id="f642c-190">Valor</span><span class="sxs-lookup"><span data-stu-id="f642c-190">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f642c-191">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f642c-191">Header</span></span><br/> | <dl> <span data-ttu-id="f642c-192"><dt>D3DCompiler. h</dt></span><span class="sxs-lookup"><span data-stu-id="f642c-192"><dt>D3DCompiler.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f642c-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="f642c-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f642c-194">Constantes D3DCompiler</span><span class="sxs-lookup"><span data-stu-id="f642c-194">D3DCompiler Constants</span></span>](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

 





