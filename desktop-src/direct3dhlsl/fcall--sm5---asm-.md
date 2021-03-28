---
title: fcall (SM5-ASM)
description: Chamada de função de interface.
ms.assetid: C21784A0-D2F4-4DDE-9AC4-4F21351BCA6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57ea40fec51cf4155b0932f6ce4a7b80d3180dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365279"
---
# <a name="fcall-sm5---asm"></a><span data-ttu-id="6e953-103">fcall (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6e953-103">fcall (sm5 - asm)</span></span>

<span data-ttu-id="6e953-104">Chamada de função de interface.</span><span class="sxs-lookup"><span data-stu-id="6e953-104">Interface function call.</span></span>



| <span data-ttu-id="6e953-105">fcall FP \# \[ arrayIndex \] \[ chamada\]</span><span class="sxs-lookup"><span data-stu-id="6e953-105">fcall fp\#\[arrayIndex\]\[callSite\]</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="6e953-106">Item</span><span class="sxs-lookup"><span data-stu-id="6e953-106">Item</span></span>                                                                                                           | <span data-ttu-id="6e953-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6e953-107">Description</span></span>                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e953-108"><span id="fp_"></span><span id="FP_"></span>*FP\#*</span><span class="sxs-lookup"><span data-stu-id="6e953-108"><span id="fp_"></span><span id="FP_"></span>*fp\#*</span></span><br/>                                                  | <span data-ttu-id="6e953-109">\[no \] ponteiro de função.</span><span class="sxs-lookup"><span data-stu-id="6e953-109">\[in\] The function pointer.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6e953-110"><span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*</span><span class="sxs-lookup"><span data-stu-id="6e953-110"><span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*</span></span><br/> | <span data-ttu-id="6e953-111">\[em \] opcional.</span><span class="sxs-lookup"><span data-stu-id="6e953-111">\[in\] Optional.</span></span> <span data-ttu-id="6e953-112">Especifica um deslocamento na matriz de ponteiro de função.</span><span class="sxs-lookup"><span data-stu-id="6e953-112">Specifies an offset into the function pointer array.</span></span> <span data-ttu-id="6e953-113">Esse parâmetro deve ser um inteiro não assinado literal se FP \# não tiver sido declarado como indexável.</span><span class="sxs-lookup"><span data-stu-id="6e953-113">This parameter must be a literal unsigned integer if fp\# was not declared as indexable.</span></span> <span data-ttu-id="6e953-114">Caso contrário, arrayIndex pode estar no formato literal base + offset de um registro de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6e953-114">Otherwise, arrayIndex may be of the form literal base + offset from a shader register.</span></span> <span data-ttu-id="6e953-115">Por exemplo, fcall FP1 \[ R1. w + 0 \] \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="6e953-115">For example, fcall fp1\[r1.w + 0\]\[0\] .</span></span><br/> |
| <span data-ttu-id="6e953-116"><span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span>*chamada*</span><span class="sxs-lookup"><span data-stu-id="6e953-116"><span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span> *callSite*</span></span><br/>     | <span data-ttu-id="6e953-117">\[em \] opcional.</span><span class="sxs-lookup"><span data-stu-id="6e953-117">\[in\] Optional.</span></span> <span data-ttu-id="6e953-118">Um deslocamento de inteiro não assinado literal na tabela de funções selecionada, selecionando um corpo de função FB \# a ser executado.</span><span class="sxs-lookup"><span data-stu-id="6e953-118">A literal unsigned integer offset into the selected function table, selecting a function body fb\# to execute.</span></span> <br/>                                                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="6e953-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e953-119">Remarks</span></span>

<span data-ttu-id="6e953-120">*FP \#* \[  \] \[ arrayIndex \] resolve para uma determinada tabela de funções, selecionada na API fora do sombreador das opções de tabela de funções listadas na declaração de *FP \#*.</span><span class="sxs-lookup"><span data-stu-id="6e953-120">*fp\#*\[*arrayIndex*\]\[\] resolves to a particular function table, selected from the API outside the shader from the function table choices listed in the declaration of *fp\#*.</span></span>

<span data-ttu-id="6e953-121">A soma de \# em *FP \#* e *arrayIndex* selecione a tabela de funções.</span><span class="sxs-lookup"><span data-stu-id="6e953-121">The sum of \# in *fp\#* and *arrayIndex* select the function table.</span></span> <span data-ttu-id="6e953-122">Por exemplo, se uma interface for declarada como FP4 \[ 4 \] \[ 3 \] (tamanho da matriz de 4), os seguintes **fcall** s serão equivalentes: fcall FP4 \[ 2 \] \[ 3 \] e FP5 \[ 1 \] \[ 3 \] , pois 4 + 2 = 5 + 1.</span><span class="sxs-lookup"><span data-stu-id="6e953-122">For example, if an interface is declared as fp4\[4\]\[3\] (array size of 4), the following **fcall** s are equivalent: fcall fp4\[2\]\[3\] and fp5\[1\]\[3\], because 4+2 = 5+1.</span></span>

### <a name="restrictions"></a><span data-ttu-id="6e953-123">Restrições</span><span class="sxs-lookup"><span data-stu-id="6e953-123">Restrictions</span></span>

-   <span data-ttu-id="6e953-124">Se *arrayIndex* usar a indexação dinâmica, o comportamento será indefinido se *arrayIndex* divergir em invocações de sombreador adjacentes, que poderia estar em execução em atrelada.</span><span class="sxs-lookup"><span data-stu-id="6e953-124">If *arrayIndex* uses dynamic indexing, behavior is undefined if *arrayIndex* diverges on adjacent shader invocations, which could be executing in lockstep.</span></span> <span data-ttu-id="6e953-125">O compilador HLSL tentará não permitir esse caso.</span><span class="sxs-lookup"><span data-stu-id="6e953-125">The HLSL compiler will attempt to disallow this case.</span></span>

    <span data-ttu-id="6e953-126">As invocações adjacentes podem ficar inativas devido ao controle de fluxo, pois ele não interrompe a execução de atrelada.</span><span class="sxs-lookup"><span data-stu-id="6e953-126">Adjacent invocations can be inactive due to flow control, because it doesn t break lockstep execution.</span></span>

-   <span data-ttu-id="6e953-127">Se *FP \#*  +  *arrayIndex* especificar um índice fora dos limites, o comportamento será indefinido.</span><span class="sxs-lookup"><span data-stu-id="6e953-127">If *fp\#* + *arrayIndex* specifies an out of bounds index, behavior is undefined.</span></span>
-   <span data-ttu-id="6e953-128">Para os casos indefinidos descritos aqui, isso significa que o comportamento do dispositivo D3D atual se torna indefinido, incluindo a possibilidade de perda do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6e953-128">For the undefined cases described here, it means the behavior of the current D3D device becomes undefined, including the possibility of Device Lost.</span></span> <span data-ttu-id="6e953-129">No entanto, nenhuma memória fora do dispositivo D3D atual será acessada ou executada como código.</span><span class="sxs-lookup"><span data-stu-id="6e953-129">However no memory outside the current D3D device will be accessed or executed as code.</span></span>

<span data-ttu-id="6e953-130">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="6e953-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6e953-131">Vértice</span><span class="sxs-lookup"><span data-stu-id="6e953-131">Vertex</span></span> | <span data-ttu-id="6e953-132">Envoltória</span><span class="sxs-lookup"><span data-stu-id="6e953-132">Hull</span></span> | <span data-ttu-id="6e953-133">Domínio</span><span class="sxs-lookup"><span data-stu-id="6e953-133">Domain</span></span> | <span data-ttu-id="6e953-134">Geometria</span><span class="sxs-lookup"><span data-stu-id="6e953-134">Geometry</span></span> | <span data-ttu-id="6e953-135">16x16</span><span class="sxs-lookup"><span data-stu-id="6e953-135">Pixel</span></span> | <span data-ttu-id="6e953-136">Computação</span><span class="sxs-lookup"><span data-stu-id="6e953-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6e953-137">X</span><span class="sxs-lookup"><span data-stu-id="6e953-137">X</span></span>      | <span data-ttu-id="6e953-138">X</span><span class="sxs-lookup"><span data-stu-id="6e953-138">X</span></span>    | <span data-ttu-id="6e953-139">X</span><span class="sxs-lookup"><span data-stu-id="6e953-139">X</span></span>      | <span data-ttu-id="6e953-140">X</span><span class="sxs-lookup"><span data-stu-id="6e953-140">X</span></span>        | <span data-ttu-id="6e953-141">X</span><span class="sxs-lookup"><span data-stu-id="6e953-141">X</span></span>     | <span data-ttu-id="6e953-142">X</span><span class="sxs-lookup"><span data-stu-id="6e953-142">X</span></span>       |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="6e953-143">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="6e953-143">Minimum Shader Model</span></span>

<span data-ttu-id="6e953-144">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="6e953-144">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6e953-145">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="6e953-145">Shader Model</span></span>                                              | <span data-ttu-id="6e953-146">Com suporte</span><span class="sxs-lookup"><span data-stu-id="6e953-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6e953-147">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6e953-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6e953-148">sim</span><span class="sxs-lookup"><span data-stu-id="6e953-148">yes</span></span>       |
| [<span data-ttu-id="6e953-149">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="6e953-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6e953-150">não</span><span class="sxs-lookup"><span data-stu-id="6e953-150">no</span></span>        |
| [<span data-ttu-id="6e953-151">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6e953-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6e953-152">não</span><span class="sxs-lookup"><span data-stu-id="6e953-152">no</span></span>        |
| [<span data-ttu-id="6e953-153">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e953-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6e953-154">não</span><span class="sxs-lookup"><span data-stu-id="6e953-154">no</span></span>        |
| [<span data-ttu-id="6e953-155">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e953-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6e953-156">não</span><span class="sxs-lookup"><span data-stu-id="6e953-156">no</span></span>        |
| [<span data-ttu-id="6e953-157">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e953-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6e953-158">não</span><span class="sxs-lookup"><span data-stu-id="6e953-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6e953-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6e953-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e953-160">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e953-160">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





