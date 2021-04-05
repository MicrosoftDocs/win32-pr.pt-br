---
title: atributo ms-DS-NC-repl-Outbound-Neighbors
description: Parceiros de replicação para esta partição. Esse servidor envia dados de replicação para esses outros servidores, que atuam como destinos. Esse servidor notificará esses outros servidores quando novos dados estiverem disponíveis.
ms.assetid: 9dcc7485-1999-47ff-bb57-8193768a15a9
ms.tgt_platform: multiple
keywords:
- Esquema de AD do MS-DS-NC-repl-Outbound-Neighbors
- atributo msDS-NCReplOutboundNeighbors do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-NC-Repl-Outbound-Neighbors
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fd37ccab1b3faef6ca2c84a52c05249a52ff38a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825199"
---
# <a name="ms-ds-nc-repl-outbound-neighbors-attribute"></a><span data-ttu-id="69939-107">atributo ms-DS-NC-repl-Outbound-Neighbors</span><span class="sxs-lookup"><span data-stu-id="69939-107">ms-DS-NC-Repl-Outbound-Neighbors attribute</span></span>

<span data-ttu-id="69939-108">Parceiros de replicação para esta partição.</span><span class="sxs-lookup"><span data-stu-id="69939-108">Replication partners for this partition.</span></span> <span data-ttu-id="69939-109">Esse servidor envia dados de replicação para esses outros servidores, que atuam como destinos.</span><span class="sxs-lookup"><span data-stu-id="69939-109">This server sends replication data to these other servers, which act as destinations.</span></span> <span data-ttu-id="69939-110">Esse servidor notificará esses outros servidores quando novos dados estiverem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="69939-110">This server will notify these other servers when new data is available.</span></span>



| <span data-ttu-id="69939-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="69939-111">Entry</span></span> | <span data-ttu-id="69939-112">Valor</span><span class="sxs-lookup"><span data-stu-id="69939-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="69939-113">CN</span><span class="sxs-lookup"><span data-stu-id="69939-113">CN</span></span>                | <span data-ttu-id="69939-114">ms-DS-NC-repl-Bound-Neighbors</span><span class="sxs-lookup"><span data-stu-id="69939-114">ms-DS-NC-Repl-Outbound-Neighbors</span></span>            |
| <span data-ttu-id="69939-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="69939-115">Ldap-Display-Name</span></span> | <span data-ttu-id="69939-116">msDS-NCReplOutboundNeighbors</span><span class="sxs-lookup"><span data-stu-id="69939-116">msDS-NCReplOutboundNeighbors</span></span>                |
| <span data-ttu-id="69939-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="69939-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="69939-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="69939-118">Update Privilege</span></span>  | <span data-ttu-id="69939-119">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="69939-119">This value is set by the system.</span></span>            |
| <span data-ttu-id="69939-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="69939-120">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="69939-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="69939-121">Attribute-Id</span></span>      | <span data-ttu-id="69939-122">1.2.840.113556.1.4.1706</span><span class="sxs-lookup"><span data-stu-id="69939-122">1.2.840.113556.1.4.1706</span></span>                     |
| <span data-ttu-id="69939-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="69939-123">System-Id-Guid</span></span>    | <span data-ttu-id="69939-124">855f2ef5-a1c5-4cc4-ba6d-32522848b61f</span><span class="sxs-lookup"><span data-stu-id="69939-124">855f2ef5-a1c5-4cc4-ba6d-32522848b61f</span></span>        |
| <span data-ttu-id="69939-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="69939-125">Syntax</span></span>            | [<span data-ttu-id="69939-126">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="69939-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="69939-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="69939-127">Implementations</span></span>

-   [<span data-ttu-id="69939-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="69939-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="69939-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="69939-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="69939-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="69939-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="69939-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="69939-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="69939-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="69939-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="69939-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="69939-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="69939-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="69939-134">Windows Server 2003</span></span>



| <span data-ttu-id="69939-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="69939-135">Entry</span></span> | <span data-ttu-id="69939-136">Valor</span><span class="sxs-lookup"><span data-stu-id="69939-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="69939-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="69939-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="69939-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69939-138">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="69939-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="69939-139">System-Only</span></span>            | <span data-ttu-id="69939-140">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-140">False</span></span>                           |
| <span data-ttu-id="69939-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="69939-141">Is-Single-Valued</span></span>       | <span data-ttu-id="69939-142">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-142">False</span></span>                           |
| <span data-ttu-id="69939-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="69939-143">Is Indexed</span></span>             | <span data-ttu-id="69939-144">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-144">False</span></span>                           |
| <span data-ttu-id="69939-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="69939-145">In Global Catalog</span></span>      | <span data-ttu-id="69939-146">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-146">False</span></span>                           |
| <span data-ttu-id="69939-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69939-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="69939-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="69939-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="69939-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69939-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="69939-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69939-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="69939-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69939-151">Search-Flags</span></span>           | <span data-ttu-id="69939-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69939-152">0x00000000</span></span>                      |
| <span data-ttu-id="69939-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69939-153">System-Flags</span></span>           | <span data-ttu-id="69939-154">0x00000014</span><span class="sxs-lookup"><span data-stu-id="69939-154">0x00000014</span></span>                      |
| <span data-ttu-id="69939-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="69939-155">Classes used in</span></span>        | [<span data-ttu-id="69939-156">**Início**</span><span class="sxs-lookup"><span data-stu-id="69939-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="69939-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="69939-157">ADAM</span></span>



| <span data-ttu-id="69939-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="69939-158">Entry</span></span> | <span data-ttu-id="69939-159">Valor</span><span class="sxs-lookup"><span data-stu-id="69939-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="69939-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="69939-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="69939-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69939-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="69939-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="69939-162">System-Only</span></span>            | <span data-ttu-id="69939-163">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-163">False</span></span>                           |
| <span data-ttu-id="69939-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="69939-164">Is-Single-Valued</span></span>       | <span data-ttu-id="69939-165">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-165">False</span></span>                           |
| <span data-ttu-id="69939-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="69939-166">Is Indexed</span></span>             | <span data-ttu-id="69939-167">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-167">False</span></span>                           |
| <span data-ttu-id="69939-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="69939-168">In Global Catalog</span></span>      | <span data-ttu-id="69939-169">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-169">False</span></span>                           |
| <span data-ttu-id="69939-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69939-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="69939-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="69939-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="69939-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69939-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="69939-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69939-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="69939-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69939-174">Search-Flags</span></span>           | <span data-ttu-id="69939-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69939-175">0x00000000</span></span>                      |
| <span data-ttu-id="69939-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69939-176">System-Flags</span></span>           | <span data-ttu-id="69939-177">0x00000014</span><span class="sxs-lookup"><span data-stu-id="69939-177">0x00000014</span></span>                      |
| <span data-ttu-id="69939-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="69939-178">Classes used in</span></span>        | [<span data-ttu-id="69939-179">**Início**</span><span class="sxs-lookup"><span data-stu-id="69939-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="69939-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="69939-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="69939-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="69939-181">Entry</span></span> | <span data-ttu-id="69939-182">Valor</span><span class="sxs-lookup"><span data-stu-id="69939-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="69939-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="69939-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="69939-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69939-184">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="69939-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="69939-185">System-Only</span></span>            | <span data-ttu-id="69939-186">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-186">False</span></span>                           |
| <span data-ttu-id="69939-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="69939-187">Is-Single-Valued</span></span>       | <span data-ttu-id="69939-188">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-188">False</span></span>                           |
| <span data-ttu-id="69939-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="69939-189">Is Indexed</span></span>             | <span data-ttu-id="69939-190">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-190">False</span></span>                           |
| <span data-ttu-id="69939-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="69939-191">In Global Catalog</span></span>      | <span data-ttu-id="69939-192">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-192">False</span></span>                           |
| <span data-ttu-id="69939-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69939-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="69939-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="69939-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="69939-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69939-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="69939-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69939-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="69939-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69939-197">Search-Flags</span></span>           | <span data-ttu-id="69939-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69939-198">0x00000000</span></span>                      |
| <span data-ttu-id="69939-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69939-199">System-Flags</span></span>           | <span data-ttu-id="69939-200">0x00000014</span><span class="sxs-lookup"><span data-stu-id="69939-200">0x00000014</span></span>                      |
| <span data-ttu-id="69939-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="69939-201">Classes used in</span></span>        | [<span data-ttu-id="69939-202">**Início**</span><span class="sxs-lookup"><span data-stu-id="69939-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="69939-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69939-203">Windows Server 2008</span></span>



| <span data-ttu-id="69939-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="69939-204">Entry</span></span> | <span data-ttu-id="69939-205">Valor</span><span class="sxs-lookup"><span data-stu-id="69939-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="69939-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="69939-206">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="69939-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69939-207">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="69939-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="69939-208">System-Only</span></span>            | <span data-ttu-id="69939-209">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-209">False</span></span>                           |
| <span data-ttu-id="69939-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="69939-210">Is-Single-Valued</span></span>       | <span data-ttu-id="69939-211">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-211">False</span></span>                           |
| <span data-ttu-id="69939-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="69939-212">Is Indexed</span></span>             | <span data-ttu-id="69939-213">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-213">False</span></span>                           |
| <span data-ttu-id="69939-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="69939-214">In Global Catalog</span></span>      | <span data-ttu-id="69939-215">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-215">False</span></span>                           |
| <span data-ttu-id="69939-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69939-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="69939-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="69939-217">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="69939-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69939-218">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="69939-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69939-219">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="69939-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69939-220">Search-Flags</span></span>           | <span data-ttu-id="69939-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69939-221">0x00000000</span></span>                      |
| <span data-ttu-id="69939-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69939-222">System-Flags</span></span>           | <span data-ttu-id="69939-223">0x00000014</span><span class="sxs-lookup"><span data-stu-id="69939-223">0x00000014</span></span>                      |
| <span data-ttu-id="69939-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="69939-224">Classes used in</span></span>        | [<span data-ttu-id="69939-225">**Início**</span><span class="sxs-lookup"><span data-stu-id="69939-225">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="69939-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="69939-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="69939-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="69939-227">Entry</span></span> | <span data-ttu-id="69939-228">Valor</span><span class="sxs-lookup"><span data-stu-id="69939-228">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="69939-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="69939-229">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="69939-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69939-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="69939-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="69939-231">System-Only</span></span>            | <span data-ttu-id="69939-232">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-232">False</span></span>                           |
| <span data-ttu-id="69939-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="69939-233">Is-Single-Valued</span></span>       | <span data-ttu-id="69939-234">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-234">False</span></span>                           |
| <span data-ttu-id="69939-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="69939-235">Is Indexed</span></span>             | <span data-ttu-id="69939-236">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-236">False</span></span>                           |
| <span data-ttu-id="69939-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="69939-237">In Global Catalog</span></span>      | <span data-ttu-id="69939-238">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-238">False</span></span>                           |
| <span data-ttu-id="69939-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69939-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="69939-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="69939-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="69939-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69939-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="69939-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69939-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="69939-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69939-243">Search-Flags</span></span>           | <span data-ttu-id="69939-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69939-244">0x00000000</span></span>                      |
| <span data-ttu-id="69939-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69939-245">System-Flags</span></span>           | <span data-ttu-id="69939-246">0x00000014</span><span class="sxs-lookup"><span data-stu-id="69939-246">0x00000014</span></span>                      |
| <span data-ttu-id="69939-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="69939-247">Classes used in</span></span>        | [<span data-ttu-id="69939-248">**Início**</span><span class="sxs-lookup"><span data-stu-id="69939-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="69939-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="69939-249">Windows Server 2012</span></span>



| <span data-ttu-id="69939-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="69939-250">Entry</span></span> | <span data-ttu-id="69939-251">Valor</span><span class="sxs-lookup"><span data-stu-id="69939-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="69939-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="69939-252">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="69939-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69939-253">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="69939-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="69939-254">System-Only</span></span>            | <span data-ttu-id="69939-255">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-255">False</span></span>                           |
| <span data-ttu-id="69939-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="69939-256">Is-Single-Valued</span></span>       | <span data-ttu-id="69939-257">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-257">False</span></span>                           |
| <span data-ttu-id="69939-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="69939-258">Is Indexed</span></span>             | <span data-ttu-id="69939-259">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-259">False</span></span>                           |
| <span data-ttu-id="69939-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="69939-260">In Global Catalog</span></span>      | <span data-ttu-id="69939-261">Falso</span><span class="sxs-lookup"><span data-stu-id="69939-261">False</span></span>                           |
| <span data-ttu-id="69939-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69939-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="69939-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="69939-263">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="69939-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69939-264">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="69939-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69939-265">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="69939-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69939-266">Search-Flags</span></span>           | <span data-ttu-id="69939-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69939-267">0x00000000</span></span>                      |
| <span data-ttu-id="69939-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69939-268">System-Flags</span></span>           | <span data-ttu-id="69939-269">0x00000014</span><span class="sxs-lookup"><span data-stu-id="69939-269">0x00000014</span></span>                      |
| <span data-ttu-id="69939-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="69939-270">Classes used in</span></span>        | [<span data-ttu-id="69939-271">**Início**</span><span class="sxs-lookup"><span data-stu-id="69939-271">**Top**</span></span>](c-top.md)<br/> |



 

 





