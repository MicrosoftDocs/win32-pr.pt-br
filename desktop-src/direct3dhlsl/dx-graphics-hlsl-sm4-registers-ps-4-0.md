---
title: Registros-ps_4_0
description: Esta seção contém informações de referência para os registros de entrada e saída implementados pelo pixel shader versão 4 \_ 0.
ms.assetid: 8b83667f-f599-4105-b68c-0d6aa7c528ab
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3dea9606419f32a168c08cc1efbebb5e285d3815
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364055"
---
# <a name="registers---ps_4_0"></a><span data-ttu-id="799b1-103">Registros-PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="799b1-103">Registers - ps\_4\_0</span></span>

<span data-ttu-id="799b1-104">Esta seção contém informações de referência para os registros de entrada e saída implementados pelo pixel shader versão 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="799b1-104">This section contains reference information for the input and output registers implemented by pixel shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="799b1-105">Registros de entrada</span><span class="sxs-lookup"><span data-stu-id="799b1-105">Input Registers</span></span>



| <span data-ttu-id="799b1-106">Registre-se</span><span class="sxs-lookup"><span data-stu-id="799b1-106">Register</span></span>      | <span data-ttu-id="799b1-107">Name</span><span class="sxs-lookup"><span data-stu-id="799b1-107">Name</span></span> | <span data-ttu-id="799b1-108">Contagem</span><span class="sxs-lookup"><span data-stu-id="799b1-108">Count</span></span>              | <span data-ttu-id="799b1-109">R/W</span><span class="sxs-lookup"><span data-stu-id="799b1-109">R/W</span></span> | <span data-ttu-id="799b1-110">Dimensão</span><span class="sxs-lookup"><span data-stu-id="799b1-110">Dimension</span></span> | <span data-ttu-id="799b1-111">Indexável por r\#</span><span class="sxs-lookup"><span data-stu-id="799b1-111">Indexable by r\#</span></span> | <span data-ttu-id="799b1-112">Padrões</span><span class="sxs-lookup"><span data-stu-id="799b1-112">Defaults</span></span> | <span data-ttu-id="799b1-113">Requer DCL</span><span class="sxs-lookup"><span data-stu-id="799b1-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="799b1-114">d\#</span><span class="sxs-lookup"><span data-stu-id="799b1-114">r\#</span></span>           |      | <span data-ttu-id="799b1-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="799b1-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="799b1-116">R/W</span><span class="sxs-lookup"><span data-stu-id="799b1-116">R/W</span></span> | <span data-ttu-id="799b1-117">4</span><span class="sxs-lookup"><span data-stu-id="799b1-117">4</span></span>         | <span data-ttu-id="799b1-118">Não</span><span class="sxs-lookup"><span data-stu-id="799b1-118">No</span></span>               | <span data-ttu-id="799b1-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="799b1-119">None</span></span>     | <span data-ttu-id="799b1-120">Yes</span><span class="sxs-lookup"><span data-stu-id="799b1-120">Yes</span></span>          |
| <span data-ttu-id="799b1-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="799b1-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="799b1-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="799b1-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="799b1-123">R/W</span><span class="sxs-lookup"><span data-stu-id="799b1-123">R/W</span></span> | <span data-ttu-id="799b1-124">4</span><span class="sxs-lookup"><span data-stu-id="799b1-124">4</span></span>         | <span data-ttu-id="799b1-125">Sim</span><span class="sxs-lookup"><span data-stu-id="799b1-125">Yes</span></span>              | <span data-ttu-id="799b1-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="799b1-126">None</span></span>     | <span data-ttu-id="799b1-127">Yes</span><span class="sxs-lookup"><span data-stu-id="799b1-127">Yes</span></span>          |
| <span data-ttu-id="799b1-128">l\#</span><span class="sxs-lookup"><span data-stu-id="799b1-128">v\#</span></span>           |      | <span data-ttu-id="799b1-129">32</span><span class="sxs-lookup"><span data-stu-id="799b1-129">32</span></span>                 | <span data-ttu-id="799b1-130">R</span><span class="sxs-lookup"><span data-stu-id="799b1-130">R</span></span>   | <span data-ttu-id="799b1-131">4</span><span class="sxs-lookup"><span data-stu-id="799b1-131">4</span></span>         | <span data-ttu-id="799b1-132">Sim</span><span class="sxs-lookup"><span data-stu-id="799b1-132">Yes</span></span>              | <span data-ttu-id="799b1-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="799b1-133">None</span></span>     | <span data-ttu-id="799b1-134">Yes</span><span class="sxs-lookup"><span data-stu-id="799b1-134">Yes</span></span>          |
| <span data-ttu-id="799b1-135">t\#</span><span class="sxs-lookup"><span data-stu-id="799b1-135">t\#</span></span>           |      | <span data-ttu-id="799b1-136">128</span><span class="sxs-lookup"><span data-stu-id="799b1-136">128</span></span>                | <span data-ttu-id="799b1-137">R</span><span class="sxs-lookup"><span data-stu-id="799b1-137">R</span></span>   | <span data-ttu-id="799b1-138">1</span><span class="sxs-lookup"><span data-stu-id="799b1-138">1</span></span>         | <span data-ttu-id="799b1-139">Não</span><span class="sxs-lookup"><span data-stu-id="799b1-139">No</span></span>               | <span data-ttu-id="799b1-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="799b1-140">None</span></span>     | <span data-ttu-id="799b1-141">Yes</span><span class="sxs-lookup"><span data-stu-id="799b1-141">Yes</span></span>          |
| <span data-ttu-id="799b1-142">s\#</span><span class="sxs-lookup"><span data-stu-id="799b1-142">s\#</span></span>           |      | <span data-ttu-id="799b1-143">16</span><span class="sxs-lookup"><span data-stu-id="799b1-143">16</span></span>                 | <span data-ttu-id="799b1-144">R</span><span class="sxs-lookup"><span data-stu-id="799b1-144">R</span></span>   | <span data-ttu-id="799b1-145">1</span><span class="sxs-lookup"><span data-stu-id="799b1-145">1</span></span>         | <span data-ttu-id="799b1-146">Não</span><span class="sxs-lookup"><span data-stu-id="799b1-146">No</span></span>               | <span data-ttu-id="799b1-147">Nenhum</span><span class="sxs-lookup"><span data-stu-id="799b1-147">None</span></span>     | <span data-ttu-id="799b1-148">Yes</span><span class="sxs-lookup"><span data-stu-id="799b1-148">Yes</span></span>          |
| <span data-ttu-id="799b1-149">\# \[ índice CB\]</span><span class="sxs-lookup"><span data-stu-id="799b1-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="799b1-150">15</span><span class="sxs-lookup"><span data-stu-id="799b1-150">15</span></span>                 | <span data-ttu-id="799b1-151">R</span><span class="sxs-lookup"><span data-stu-id="799b1-151">R</span></span>   | <span data-ttu-id="799b1-152">4</span><span class="sxs-lookup"><span data-stu-id="799b1-152">4</span></span>         | <span data-ttu-id="799b1-153">Sim (conteúdo)</span><span class="sxs-lookup"><span data-stu-id="799b1-153">Yes(Contents)</span></span>    | <span data-ttu-id="799b1-154">Nenhum</span><span class="sxs-lookup"><span data-stu-id="799b1-154">None</span></span>     | <span data-ttu-id="799b1-155">Yes</span><span class="sxs-lookup"><span data-stu-id="799b1-155">Yes</span></span>          |
| <span data-ttu-id="799b1-156">índice de ICB \[\]</span><span class="sxs-lookup"><span data-stu-id="799b1-156">icb\[index\]</span></span>  |      | <span data-ttu-id="799b1-157">1</span><span class="sxs-lookup"><span data-stu-id="799b1-157">1</span></span>                  | <span data-ttu-id="799b1-158">R</span><span class="sxs-lookup"><span data-stu-id="799b1-158">R</span></span>   | <span data-ttu-id="799b1-159">4</span><span class="sxs-lookup"><span data-stu-id="799b1-159">4</span></span>         | <span data-ttu-id="799b1-160">Sim (conteúdo)</span><span class="sxs-lookup"><span data-stu-id="799b1-160">Yes(Contents)</span></span>    | <span data-ttu-id="799b1-161">Nenhum</span><span class="sxs-lookup"><span data-stu-id="799b1-161">None</span></span>     | <span data-ttu-id="799b1-162">Yes</span><span class="sxs-lookup"><span data-stu-id="799b1-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="799b1-163">Registros de saída</span><span class="sxs-lookup"><span data-stu-id="799b1-163">Output Registers</span></span>



| <span data-ttu-id="799b1-164">Registre-se</span><span class="sxs-lookup"><span data-stu-id="799b1-164">Register</span></span> | <span data-ttu-id="799b1-165">Name</span><span class="sxs-lookup"><span data-stu-id="799b1-165">Name</span></span>            | <span data-ttu-id="799b1-166">Contagem</span><span class="sxs-lookup"><span data-stu-id="799b1-166">Count</span></span> | <span data-ttu-id="799b1-167">R/W</span><span class="sxs-lookup"><span data-stu-id="799b1-167">R/W</span></span> | <span data-ttu-id="799b1-168">Dimensão</span><span class="sxs-lookup"><span data-stu-id="799b1-168">Dimension</span></span> | <span data-ttu-id="799b1-169">Indexável por r\#</span><span class="sxs-lookup"><span data-stu-id="799b1-169">Indexable by r\#</span></span> | <span data-ttu-id="799b1-170">Padrões</span><span class="sxs-lookup"><span data-stu-id="799b1-170">Defaults</span></span> | <span data-ttu-id="799b1-171">Requer DCL</span><span class="sxs-lookup"><span data-stu-id="799b1-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="799b1-172">NULO</span><span class="sxs-lookup"><span data-stu-id="799b1-172">NULL</span></span>     | <span data-ttu-id="799b1-173">Descartar resultado</span><span class="sxs-lookup"><span data-stu-id="799b1-173">Discard Result</span></span>  | <span data-ttu-id="799b1-174">N/D</span><span class="sxs-lookup"><span data-stu-id="799b1-174">N/A</span></span>   | <span data-ttu-id="799b1-175">W</span><span class="sxs-lookup"><span data-stu-id="799b1-175">W</span></span>   | <span data-ttu-id="799b1-176">N/D</span><span class="sxs-lookup"><span data-stu-id="799b1-176">N/A</span></span>       | <span data-ttu-id="799b1-177">N/D</span><span class="sxs-lookup"><span data-stu-id="799b1-177">N/A</span></span>              | <span data-ttu-id="799b1-178">N/D</span><span class="sxs-lookup"><span data-stu-id="799b1-178">N/A</span></span>      | <span data-ttu-id="799b1-179">Não</span><span class="sxs-lookup"><span data-stu-id="799b1-179">No</span></span>           |
| <span data-ttu-id="799b1-180">minúscula\#</span><span class="sxs-lookup"><span data-stu-id="799b1-180">o\#</span></span>      | <span data-ttu-id="799b1-181">Registro de saída</span><span class="sxs-lookup"><span data-stu-id="799b1-181">Output Register</span></span> | <span data-ttu-id="799b1-182">8</span><span class="sxs-lookup"><span data-stu-id="799b1-182">8</span></span>     | <span data-ttu-id="799b1-183">W</span><span class="sxs-lookup"><span data-stu-id="799b1-183">W</span></span>   | <span data-ttu-id="799b1-184">N/D</span><span class="sxs-lookup"><span data-stu-id="799b1-184">N/A</span></span>       | <span data-ttu-id="799b1-185">N/D</span><span class="sxs-lookup"><span data-stu-id="799b1-185">N/A</span></span>              | <span data-ttu-id="799b1-186">4</span><span class="sxs-lookup"><span data-stu-id="799b1-186">4</span></span>        | <span data-ttu-id="799b1-187">Não</span><span class="sxs-lookup"><span data-stu-id="799b1-187">No</span></span>           |
| <span data-ttu-id="799b1-188">oDepth</span><span class="sxs-lookup"><span data-stu-id="799b1-188">oDepth</span></span>   | <span data-ttu-id="799b1-189">Profundidade de saída</span><span class="sxs-lookup"><span data-stu-id="799b1-189">Output Depth</span></span>    | <span data-ttu-id="799b1-190">1</span><span class="sxs-lookup"><span data-stu-id="799b1-190">1</span></span>     | <span data-ttu-id="799b1-191">W</span><span class="sxs-lookup"><span data-stu-id="799b1-191">W</span></span>   | <span data-ttu-id="799b1-192">N/D</span><span class="sxs-lookup"><span data-stu-id="799b1-192">N/A</span></span>       | <span data-ttu-id="799b1-193">N/D</span><span class="sxs-lookup"><span data-stu-id="799b1-193">N/A</span></span>              | <span data-ttu-id="799b1-194">1</span><span class="sxs-lookup"><span data-stu-id="799b1-194">1</span></span>        | <span data-ttu-id="799b1-195">N/D</span><span class="sxs-lookup"><span data-stu-id="799b1-195">N/A</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="799b1-196">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="799b1-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="799b1-197">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="799b1-197">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




