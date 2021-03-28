---
title: Registros-gs_4_0
description: Esta seção contém informações de referência para os registros de entrada e saída implementados pelo Geometry shader versão 4 \_ 0.
ms.assetid: 1f3ebd71-19de-4e26-87f0-4fb5c8e2a343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c5db86ffb797434af4badd6496b71a4ad684583
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498718"
---
# <a name="registers---gs_4_0"></a><span data-ttu-id="2e12d-103">Registros-GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2e12d-103">Registers - gs\_4\_0</span></span>

<span data-ttu-id="2e12d-104">Esta seção contém informações de referência para os registros de entrada e saída implementados pelo Geometry shader versão 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="2e12d-104">This section contains reference information for the input and output registers implemented by geometry shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="2e12d-105">Registros de entrada</span><span class="sxs-lookup"><span data-stu-id="2e12d-105">Input Registers</span></span>



| <span data-ttu-id="2e12d-106">Registre-se</span><span class="sxs-lookup"><span data-stu-id="2e12d-106">Register</span></span>                 | <span data-ttu-id="2e12d-107">Name</span><span class="sxs-lookup"><span data-stu-id="2e12d-107">Name</span></span> | <span data-ttu-id="2e12d-108">Contagem</span><span class="sxs-lookup"><span data-stu-id="2e12d-108">Count</span></span>              | <span data-ttu-id="2e12d-109">R/W</span><span class="sxs-lookup"><span data-stu-id="2e12d-109">R/W</span></span> | <span data-ttu-id="2e12d-110">Dimensão</span><span class="sxs-lookup"><span data-stu-id="2e12d-110">Dimension</span></span>        | <span data-ttu-id="2e12d-111">Indexável por r\#</span><span class="sxs-lookup"><span data-stu-id="2e12d-111">Indexable by r\#</span></span> | <span data-ttu-id="2e12d-112">Padrões</span><span class="sxs-lookup"><span data-stu-id="2e12d-112">Defaults</span></span> | <span data-ttu-id="2e12d-113">Requer DCL</span><span class="sxs-lookup"><span data-stu-id="2e12d-113">Requires DCL</span></span> |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| <span data-ttu-id="2e12d-114">d\#</span><span class="sxs-lookup"><span data-stu-id="2e12d-114">r\#</span></span>                      |      | <span data-ttu-id="2e12d-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="2e12d-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="2e12d-116">R/W</span><span class="sxs-lookup"><span data-stu-id="2e12d-116">R/W</span></span> | <span data-ttu-id="2e12d-117">4</span><span class="sxs-lookup"><span data-stu-id="2e12d-117">4</span></span>                | <span data-ttu-id="2e12d-118">Não</span><span class="sxs-lookup"><span data-stu-id="2e12d-118">No</span></span>               | <span data-ttu-id="2e12d-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2e12d-119">None</span></span>     | <span data-ttu-id="2e12d-120">Yes</span><span class="sxs-lookup"><span data-stu-id="2e12d-120">Yes</span></span>          |
| <span data-ttu-id="2e12d-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="2e12d-121">x\#\[n\]</span></span>                 |      | <span data-ttu-id="2e12d-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="2e12d-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="2e12d-123">R/W</span><span class="sxs-lookup"><span data-stu-id="2e12d-123">R/W</span></span> | <span data-ttu-id="2e12d-124">4</span><span class="sxs-lookup"><span data-stu-id="2e12d-124">4</span></span>                | <span data-ttu-id="2e12d-125">Sim</span><span class="sxs-lookup"><span data-stu-id="2e12d-125">Yes</span></span>              | <span data-ttu-id="2e12d-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2e12d-126">None</span></span>     | <span data-ttu-id="2e12d-127">Yes</span><span class="sxs-lookup"><span data-stu-id="2e12d-127">Yes</span></span>          |
| <span data-ttu-id="2e12d-128">\# \[ elemento de vértice \] \[ v\]</span><span class="sxs-lookup"><span data-stu-id="2e12d-128">v\#\[vertex\]\[element\]</span></span> |      | <span data-ttu-id="2e12d-129">32</span><span class="sxs-lookup"><span data-stu-id="2e12d-129">32</span></span>                 | <span data-ttu-id="2e12d-130">R</span><span class="sxs-lookup"><span data-stu-id="2e12d-130">R</span></span>   | <span data-ttu-id="2e12d-131">4 (comp.) \* 6 (Vert)</span><span class="sxs-lookup"><span data-stu-id="2e12d-131">4(comp)\*6(vert)</span></span> | <span data-ttu-id="2e12d-132">Yes</span><span class="sxs-lookup"><span data-stu-id="2e12d-132">Yes</span></span>              | <span data-ttu-id="2e12d-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2e12d-133">None</span></span>     | <span data-ttu-id="2e12d-134">Yes</span><span class="sxs-lookup"><span data-stu-id="2e12d-134">Yes</span></span>          |
| <span data-ttu-id="2e12d-135">vprim</span><span class="sxs-lookup"><span data-stu-id="2e12d-135">vprim</span></span>                    |      | <span data-ttu-id="2e12d-136">1</span><span class="sxs-lookup"><span data-stu-id="2e12d-136">1</span></span>                  | <span data-ttu-id="2e12d-137">R</span><span class="sxs-lookup"><span data-stu-id="2e12d-137">R</span></span>   | <span data-ttu-id="2e12d-138">1</span><span class="sxs-lookup"><span data-stu-id="2e12d-138">1</span></span>                | <span data-ttu-id="2e12d-139">Não</span><span class="sxs-lookup"><span data-stu-id="2e12d-139">No</span></span>               | <span data-ttu-id="2e12d-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2e12d-140">None</span></span>     | <span data-ttu-id="2e12d-141">Yes</span><span class="sxs-lookup"><span data-stu-id="2e12d-141">Yes</span></span>          |
| <span data-ttu-id="2e12d-142">t\#</span><span class="sxs-lookup"><span data-stu-id="2e12d-142">t\#</span></span>                      |      | <span data-ttu-id="2e12d-143">128</span><span class="sxs-lookup"><span data-stu-id="2e12d-143">128</span></span>                | <span data-ttu-id="2e12d-144">R</span><span class="sxs-lookup"><span data-stu-id="2e12d-144">R</span></span>   | <span data-ttu-id="2e12d-145">1</span><span class="sxs-lookup"><span data-stu-id="2e12d-145">1</span></span>                | <span data-ttu-id="2e12d-146">Não</span><span class="sxs-lookup"><span data-stu-id="2e12d-146">No</span></span>               | <span data-ttu-id="2e12d-147">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2e12d-147">None</span></span>     | <span data-ttu-id="2e12d-148">Yes</span><span class="sxs-lookup"><span data-stu-id="2e12d-148">Yes</span></span>          |
| <span data-ttu-id="2e12d-149">s\#</span><span class="sxs-lookup"><span data-stu-id="2e12d-149">s\#</span></span>                      |      | <span data-ttu-id="2e12d-150">16</span><span class="sxs-lookup"><span data-stu-id="2e12d-150">16</span></span>                 | <span data-ttu-id="2e12d-151">R</span><span class="sxs-lookup"><span data-stu-id="2e12d-151">R</span></span>   | <span data-ttu-id="2e12d-152">1</span><span class="sxs-lookup"><span data-stu-id="2e12d-152">1</span></span>                | <span data-ttu-id="2e12d-153">Não</span><span class="sxs-lookup"><span data-stu-id="2e12d-153">No</span></span>               | <span data-ttu-id="2e12d-154">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2e12d-154">None</span></span>     | <span data-ttu-id="2e12d-155">Yes</span><span class="sxs-lookup"><span data-stu-id="2e12d-155">Yes</span></span>          |
| <span data-ttu-id="2e12d-156">\# \[ índice CB\]</span><span class="sxs-lookup"><span data-stu-id="2e12d-156">cb\#\[index\]</span></span>            |      | <span data-ttu-id="2e12d-157">15</span><span class="sxs-lookup"><span data-stu-id="2e12d-157">15</span></span>                 | <span data-ttu-id="2e12d-158">R</span><span class="sxs-lookup"><span data-stu-id="2e12d-158">R</span></span>   | <span data-ttu-id="2e12d-159">4</span><span class="sxs-lookup"><span data-stu-id="2e12d-159">4</span></span>                | <span data-ttu-id="2e12d-160">Sim (conteúdo)</span><span class="sxs-lookup"><span data-stu-id="2e12d-160">Yes(Contents)</span></span>    | <span data-ttu-id="2e12d-161">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2e12d-161">None</span></span>     | <span data-ttu-id="2e12d-162">Yes</span><span class="sxs-lookup"><span data-stu-id="2e12d-162">Yes</span></span>          |
| <span data-ttu-id="2e12d-163">índice de ICB \[\]</span><span class="sxs-lookup"><span data-stu-id="2e12d-163">icb\[index\]</span></span>             |      | <span data-ttu-id="2e12d-164">1</span><span class="sxs-lookup"><span data-stu-id="2e12d-164">1</span></span>                  | <span data-ttu-id="2e12d-165">R</span><span class="sxs-lookup"><span data-stu-id="2e12d-165">R</span></span>   | <span data-ttu-id="2e12d-166">4</span><span class="sxs-lookup"><span data-stu-id="2e12d-166">4</span></span>                | <span data-ttu-id="2e12d-167">Sim (conteúdo)</span><span class="sxs-lookup"><span data-stu-id="2e12d-167">Yes(Contents)</span></span>    | <span data-ttu-id="2e12d-168">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2e12d-168">None</span></span>     | <span data-ttu-id="2e12d-169">Yes</span><span class="sxs-lookup"><span data-stu-id="2e12d-169">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="2e12d-170">Registros de saída</span><span class="sxs-lookup"><span data-stu-id="2e12d-170">Output Registers</span></span>



| <span data-ttu-id="2e12d-171">Registre-se</span><span class="sxs-lookup"><span data-stu-id="2e12d-171">Register</span></span> | <span data-ttu-id="2e12d-172">Name</span><span class="sxs-lookup"><span data-stu-id="2e12d-172">Name</span></span>            | <span data-ttu-id="2e12d-173">Contagem</span><span class="sxs-lookup"><span data-stu-id="2e12d-173">Count</span></span> | <span data-ttu-id="2e12d-174">R/W</span><span class="sxs-lookup"><span data-stu-id="2e12d-174">R/W</span></span> | <span data-ttu-id="2e12d-175">Dimensão</span><span class="sxs-lookup"><span data-stu-id="2e12d-175">Dimension</span></span> | <span data-ttu-id="2e12d-176">Indexável por r\#</span><span class="sxs-lookup"><span data-stu-id="2e12d-176">Indexable by r\#</span></span> | <span data-ttu-id="2e12d-177">Padrões</span><span class="sxs-lookup"><span data-stu-id="2e12d-177">Defaults</span></span> | <span data-ttu-id="2e12d-178">Requer DCL</span><span class="sxs-lookup"><span data-stu-id="2e12d-178">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="2e12d-179">NULO</span><span class="sxs-lookup"><span data-stu-id="2e12d-179">NULL</span></span>     | <span data-ttu-id="2e12d-180">Descartar resultado</span><span class="sxs-lookup"><span data-stu-id="2e12d-180">Discard Result</span></span>  | <span data-ttu-id="2e12d-181">N/D</span><span class="sxs-lookup"><span data-stu-id="2e12d-181">N/A</span></span>   | <span data-ttu-id="2e12d-182">W</span><span class="sxs-lookup"><span data-stu-id="2e12d-182">W</span></span>   | <span data-ttu-id="2e12d-183">N/D</span><span class="sxs-lookup"><span data-stu-id="2e12d-183">N/A</span></span>       | <span data-ttu-id="2e12d-184">N/D</span><span class="sxs-lookup"><span data-stu-id="2e12d-184">N/A</span></span>              | <span data-ttu-id="2e12d-185">N/D</span><span class="sxs-lookup"><span data-stu-id="2e12d-185">N/A</span></span>      | <span data-ttu-id="2e12d-186">Não</span><span class="sxs-lookup"><span data-stu-id="2e12d-186">No</span></span>           |
| <span data-ttu-id="2e12d-187">minúscula\#</span><span class="sxs-lookup"><span data-stu-id="2e12d-187">o\#</span></span>      | <span data-ttu-id="2e12d-188">Registro de saída</span><span class="sxs-lookup"><span data-stu-id="2e12d-188">Output Register</span></span> | <span data-ttu-id="2e12d-189">32</span><span class="sxs-lookup"><span data-stu-id="2e12d-189">32</span></span>    | <span data-ttu-id="2e12d-190">W</span><span class="sxs-lookup"><span data-stu-id="2e12d-190">W</span></span>   | <span data-ttu-id="2e12d-191">N/D</span><span class="sxs-lookup"><span data-stu-id="2e12d-191">N/A</span></span>       | <span data-ttu-id="2e12d-192">N/D</span><span class="sxs-lookup"><span data-stu-id="2e12d-192">N/A</span></span>              | <span data-ttu-id="2e12d-193">4</span><span class="sxs-lookup"><span data-stu-id="2e12d-193">4</span></span>        | <span data-ttu-id="2e12d-194">Sim</span><span class="sxs-lookup"><span data-stu-id="2e12d-194">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="2e12d-195">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e12d-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e12d-196">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="2e12d-196">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




