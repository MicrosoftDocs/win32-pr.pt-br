---
title: Registros-gs_4_1
description: Esta seção contém informações de referência para os registros de entrada e saída implementados pelo Geometry Shader versões 4 \_ 0 e 4 \_ 1.
ms.assetid: 0312707D-11D0-45D0-9E8C-8BD2BC65352C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a01f200bd4183843b1cfd2892fde5da442ca8d36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159999"
---
# <a name="registers---gs_4_1"></a><span data-ttu-id="c1d49-103">Registros-GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="c1d49-103">Registers - gs\_4\_1</span></span>

<span data-ttu-id="c1d49-104">Esta seção contém informações de referência para os registros de entrada e saída implementados pelo Geometry Shader versões 4 \_ 0 e 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="c1d49-104">This section contains reference information for the input and output registers implemented by geometry shader versions 4\_0 and 4\_1.</span></span>

## <a name="input-registers"></a><span data-ttu-id="c1d49-105">Registros de entrada</span><span class="sxs-lookup"><span data-stu-id="c1d49-105">Input Registers</span></span>



| <span data-ttu-id="c1d49-106">Registre-se</span><span class="sxs-lookup"><span data-stu-id="c1d49-106">Register</span></span>                 | <span data-ttu-id="c1d49-107">Name</span><span class="sxs-lookup"><span data-stu-id="c1d49-107">Name</span></span> | <span data-ttu-id="c1d49-108">Contagem</span><span class="sxs-lookup"><span data-stu-id="c1d49-108">Count</span></span>              | <span data-ttu-id="c1d49-109">R/W</span><span class="sxs-lookup"><span data-stu-id="c1d49-109">R/W</span></span> | <span data-ttu-id="c1d49-110">Dimensão</span><span class="sxs-lookup"><span data-stu-id="c1d49-110">Dimension</span></span>        | <span data-ttu-id="c1d49-111">Indexável por r\#</span><span class="sxs-lookup"><span data-stu-id="c1d49-111">Indexable by r\#</span></span> | <span data-ttu-id="c1d49-112">Padrões</span><span class="sxs-lookup"><span data-stu-id="c1d49-112">Defaults</span></span> | <span data-ttu-id="c1d49-113">Requer DCL</span><span class="sxs-lookup"><span data-stu-id="c1d49-113">Requires DCL</span></span> |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| <span data-ttu-id="c1d49-114">d\#</span><span class="sxs-lookup"><span data-stu-id="c1d49-114">r\#</span></span>                      |      | <span data-ttu-id="c1d49-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="c1d49-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="c1d49-116">R/W</span><span class="sxs-lookup"><span data-stu-id="c1d49-116">R/W</span></span> | <span data-ttu-id="c1d49-117">4</span><span class="sxs-lookup"><span data-stu-id="c1d49-117">4</span></span>                | <span data-ttu-id="c1d49-118">Não</span><span class="sxs-lookup"><span data-stu-id="c1d49-118">No</span></span>               | <span data-ttu-id="c1d49-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c1d49-119">None</span></span>     | <span data-ttu-id="c1d49-120">Yes</span><span class="sxs-lookup"><span data-stu-id="c1d49-120">Yes</span></span>          |
| <span data-ttu-id="c1d49-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="c1d49-121">x\#\[n\]</span></span>                 |      | <span data-ttu-id="c1d49-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="c1d49-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="c1d49-123">R/W</span><span class="sxs-lookup"><span data-stu-id="c1d49-123">R/W</span></span> | <span data-ttu-id="c1d49-124">4</span><span class="sxs-lookup"><span data-stu-id="c1d49-124">4</span></span>                | <span data-ttu-id="c1d49-125">Sim</span><span class="sxs-lookup"><span data-stu-id="c1d49-125">Yes</span></span>              | <span data-ttu-id="c1d49-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c1d49-126">None</span></span>     | <span data-ttu-id="c1d49-127">Yes</span><span class="sxs-lookup"><span data-stu-id="c1d49-127">Yes</span></span>          |
| <span data-ttu-id="c1d49-128">\# \[ elemento de vértice \] \[ v\]</span><span class="sxs-lookup"><span data-stu-id="c1d49-128">v\#\[vertex\]\[element\]</span></span> |      | <span data-ttu-id="c1d49-129">32</span><span class="sxs-lookup"><span data-stu-id="c1d49-129">32</span></span>                 | <span data-ttu-id="c1d49-130">R</span><span class="sxs-lookup"><span data-stu-id="c1d49-130">R</span></span>   | <span data-ttu-id="c1d49-131">4 (comp.) \* 6 (Vert)</span><span class="sxs-lookup"><span data-stu-id="c1d49-131">4(comp)\*6(vert)</span></span> | <span data-ttu-id="c1d49-132">Yes</span><span class="sxs-lookup"><span data-stu-id="c1d49-132">Yes</span></span>              | <span data-ttu-id="c1d49-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c1d49-133">None</span></span>     | <span data-ttu-id="c1d49-134">Yes</span><span class="sxs-lookup"><span data-stu-id="c1d49-134">Yes</span></span>          |
| <span data-ttu-id="c1d49-135">vprim</span><span class="sxs-lookup"><span data-stu-id="c1d49-135">vprim</span></span>                    |      | <span data-ttu-id="c1d49-136">1</span><span class="sxs-lookup"><span data-stu-id="c1d49-136">1</span></span>                  | <span data-ttu-id="c1d49-137">R</span><span class="sxs-lookup"><span data-stu-id="c1d49-137">R</span></span>   | <span data-ttu-id="c1d49-138">1</span><span class="sxs-lookup"><span data-stu-id="c1d49-138">1</span></span>                | <span data-ttu-id="c1d49-139">Não</span><span class="sxs-lookup"><span data-stu-id="c1d49-139">No</span></span>               | <span data-ttu-id="c1d49-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c1d49-140">None</span></span>     | <span data-ttu-id="c1d49-141">Yes</span><span class="sxs-lookup"><span data-stu-id="c1d49-141">Yes</span></span>          |
| <span data-ttu-id="c1d49-142">t\#</span><span class="sxs-lookup"><span data-stu-id="c1d49-142">t\#</span></span>                      |      | <span data-ttu-id="c1d49-143">128</span><span class="sxs-lookup"><span data-stu-id="c1d49-143">128</span></span>                | <span data-ttu-id="c1d49-144">R</span><span class="sxs-lookup"><span data-stu-id="c1d49-144">R</span></span>   | <span data-ttu-id="c1d49-145">1</span><span class="sxs-lookup"><span data-stu-id="c1d49-145">1</span></span>                | <span data-ttu-id="c1d49-146">Não</span><span class="sxs-lookup"><span data-stu-id="c1d49-146">No</span></span>               | <span data-ttu-id="c1d49-147">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c1d49-147">None</span></span>     | <span data-ttu-id="c1d49-148">Yes</span><span class="sxs-lookup"><span data-stu-id="c1d49-148">Yes</span></span>          |
| <span data-ttu-id="c1d49-149">s\#</span><span class="sxs-lookup"><span data-stu-id="c1d49-149">s\#</span></span>                      |      | <span data-ttu-id="c1d49-150">16</span><span class="sxs-lookup"><span data-stu-id="c1d49-150">16</span></span>                 | <span data-ttu-id="c1d49-151">R</span><span class="sxs-lookup"><span data-stu-id="c1d49-151">R</span></span>   | <span data-ttu-id="c1d49-152">1</span><span class="sxs-lookup"><span data-stu-id="c1d49-152">1</span></span>                | <span data-ttu-id="c1d49-153">Não</span><span class="sxs-lookup"><span data-stu-id="c1d49-153">No</span></span>               | <span data-ttu-id="c1d49-154">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c1d49-154">None</span></span>     | <span data-ttu-id="c1d49-155">Yes</span><span class="sxs-lookup"><span data-stu-id="c1d49-155">Yes</span></span>          |
| <span data-ttu-id="c1d49-156">\# \[ índice CB\]</span><span class="sxs-lookup"><span data-stu-id="c1d49-156">cb\#\[index\]</span></span>            |      | <span data-ttu-id="c1d49-157">15</span><span class="sxs-lookup"><span data-stu-id="c1d49-157">15</span></span>                 | <span data-ttu-id="c1d49-158">R</span><span class="sxs-lookup"><span data-stu-id="c1d49-158">R</span></span>   | <span data-ttu-id="c1d49-159">4</span><span class="sxs-lookup"><span data-stu-id="c1d49-159">4</span></span>                | <span data-ttu-id="c1d49-160">Sim (conteúdo)</span><span class="sxs-lookup"><span data-stu-id="c1d49-160">Yes(Contents)</span></span>    | <span data-ttu-id="c1d49-161">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c1d49-161">None</span></span>     | <span data-ttu-id="c1d49-162">Yes</span><span class="sxs-lookup"><span data-stu-id="c1d49-162">Yes</span></span>          |
| <span data-ttu-id="c1d49-163">índice de ICB \[\]</span><span class="sxs-lookup"><span data-stu-id="c1d49-163">icb\[index\]</span></span>             |      | <span data-ttu-id="c1d49-164">1</span><span class="sxs-lookup"><span data-stu-id="c1d49-164">1</span></span>                  | <span data-ttu-id="c1d49-165">R</span><span class="sxs-lookup"><span data-stu-id="c1d49-165">R</span></span>   | <span data-ttu-id="c1d49-166">4</span><span class="sxs-lookup"><span data-stu-id="c1d49-166">4</span></span>                | <span data-ttu-id="c1d49-167">Sim (conteúdo)</span><span class="sxs-lookup"><span data-stu-id="c1d49-167">Yes(Contents)</span></span>    | <span data-ttu-id="c1d49-168">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c1d49-168">None</span></span>     | <span data-ttu-id="c1d49-169">Yes</span><span class="sxs-lookup"><span data-stu-id="c1d49-169">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="c1d49-170">Registros de saída</span><span class="sxs-lookup"><span data-stu-id="c1d49-170">Output Registers</span></span>



| <span data-ttu-id="c1d49-171">Registre-se</span><span class="sxs-lookup"><span data-stu-id="c1d49-171">Register</span></span> | <span data-ttu-id="c1d49-172">Name</span><span class="sxs-lookup"><span data-stu-id="c1d49-172">Name</span></span>            | <span data-ttu-id="c1d49-173">Contagem</span><span class="sxs-lookup"><span data-stu-id="c1d49-173">Count</span></span> | <span data-ttu-id="c1d49-174">R/W</span><span class="sxs-lookup"><span data-stu-id="c1d49-174">R/W</span></span> | <span data-ttu-id="c1d49-175">Dimensão</span><span class="sxs-lookup"><span data-stu-id="c1d49-175">Dimension</span></span> | <span data-ttu-id="c1d49-176">Indexável por r\#</span><span class="sxs-lookup"><span data-stu-id="c1d49-176">Indexable by r\#</span></span> | <span data-ttu-id="c1d49-177">Padrões</span><span class="sxs-lookup"><span data-stu-id="c1d49-177">Defaults</span></span> | <span data-ttu-id="c1d49-178">Requer DCL</span><span class="sxs-lookup"><span data-stu-id="c1d49-178">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="c1d49-179">NULO</span><span class="sxs-lookup"><span data-stu-id="c1d49-179">NULL</span></span>     | <span data-ttu-id="c1d49-180">Descartar resultado</span><span class="sxs-lookup"><span data-stu-id="c1d49-180">Discard Result</span></span>  | <span data-ttu-id="c1d49-181">N/D</span><span class="sxs-lookup"><span data-stu-id="c1d49-181">N/A</span></span>   | <span data-ttu-id="c1d49-182">W</span><span class="sxs-lookup"><span data-stu-id="c1d49-182">W</span></span>   | <span data-ttu-id="c1d49-183">N/D</span><span class="sxs-lookup"><span data-stu-id="c1d49-183">N/A</span></span>       | <span data-ttu-id="c1d49-184">N/D</span><span class="sxs-lookup"><span data-stu-id="c1d49-184">N/A</span></span>              | <span data-ttu-id="c1d49-185">N/D</span><span class="sxs-lookup"><span data-stu-id="c1d49-185">N/A</span></span>      | <span data-ttu-id="c1d49-186">Não</span><span class="sxs-lookup"><span data-stu-id="c1d49-186">No</span></span>           |
| <span data-ttu-id="c1d49-187">minúscula\#</span><span class="sxs-lookup"><span data-stu-id="c1d49-187">o\#</span></span>      | <span data-ttu-id="c1d49-188">Registro de saída</span><span class="sxs-lookup"><span data-stu-id="c1d49-188">Output Register</span></span> | <span data-ttu-id="c1d49-189">32</span><span class="sxs-lookup"><span data-stu-id="c1d49-189">32</span></span>    | <span data-ttu-id="c1d49-190">W</span><span class="sxs-lookup"><span data-stu-id="c1d49-190">W</span></span>   | <span data-ttu-id="c1d49-191">N/D</span><span class="sxs-lookup"><span data-stu-id="c1d49-191">N/A</span></span>       | <span data-ttu-id="c1d49-192">N/D</span><span class="sxs-lookup"><span data-stu-id="c1d49-192">N/A</span></span>              | <span data-ttu-id="c1d49-193">4</span><span class="sxs-lookup"><span data-stu-id="c1d49-193">4</span></span>        | <span data-ttu-id="c1d49-194">Sim</span><span class="sxs-lookup"><span data-stu-id="c1d49-194">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="c1d49-195">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1d49-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1d49-196">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c1d49-196">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




