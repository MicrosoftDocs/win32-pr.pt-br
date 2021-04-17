---
title: Política-replicação-atributo de sinalizadores
description: Determina quais propriedades LSA são replicadas para os clientes.
ms.assetid: 2dadd659-c834-4105-ab3e-8ce0b8811212
ms.tgt_platform: multiple
keywords:
- Policy-Replication-Flag atributo AD Schema
- Esquema de AD do atributo policyReplicationFlags
topic_type:
- apiref
api_name:
- Policy-Replication-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42da6509662d11c4a069ba58dff5f648e7ab2261
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105753013"
---
# <a name="policy-replication-flags-attribute"></a><span data-ttu-id="36b21-105">Política-replicação-atributo de sinalizadores</span><span class="sxs-lookup"><span data-stu-id="36b21-105">Policy-Replication-Flags attribute</span></span>

<span data-ttu-id="36b21-106">Determina quais propriedades LSA são replicadas para os clientes.</span><span class="sxs-lookup"><span data-stu-id="36b21-106">Determines which LSA properties are replicated to clients.</span></span>



| <span data-ttu-id="36b21-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="36b21-107">Entry</span></span> | <span data-ttu-id="36b21-108">Valor</span><span class="sxs-lookup"><span data-stu-id="36b21-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="36b21-109">CN</span><span class="sxs-lookup"><span data-stu-id="36b21-109">CN</span></span>                | <span data-ttu-id="36b21-110">Política-replicação-sinalizadores</span><span class="sxs-lookup"><span data-stu-id="36b21-110">Policy-Replication-Flags</span></span>             |
| <span data-ttu-id="36b21-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="36b21-111">Ldap-Display-Name</span></span> | <span data-ttu-id="36b21-112">policyReplicationFlags</span><span class="sxs-lookup"><span data-stu-id="36b21-112">policyReplicationFlags</span></span>               |
| <span data-ttu-id="36b21-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="36b21-113">Size</span></span>              | <span data-ttu-id="36b21-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="36b21-114">4 bytes</span></span>                              |
| <span data-ttu-id="36b21-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="36b21-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="36b21-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="36b21-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="36b21-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="36b21-117">Attribute-Id</span></span>      | <span data-ttu-id="36b21-118">1.2.840.113556.1.4.633</span><span class="sxs-lookup"><span data-stu-id="36b21-118">1.2.840.113556.1.4.633</span></span>               |
| <span data-ttu-id="36b21-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="36b21-119">System-Id-Guid</span></span>    | <span data-ttu-id="36b21-120">19405b96-3cfa-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="36b21-120">19405b96-3cfa-11d1-a9c0-0000f80367c1</span></span> |
| <span data-ttu-id="36b21-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="36b21-121">Syntax</span></span>            | [<span data-ttu-id="36b21-122">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="36b21-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="36b21-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="36b21-123">Implementations</span></span>

-   [<span data-ttu-id="36b21-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="36b21-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="36b21-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="36b21-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="36b21-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="36b21-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="36b21-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="36b21-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="36b21-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="36b21-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="36b21-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="36b21-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="36b21-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="36b21-130">Windows 2000 Server</span></span>



| <span data-ttu-id="36b21-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="36b21-131">Entry</span></span> | <span data-ttu-id="36b21-132">Valor</span><span class="sxs-lookup"><span data-stu-id="36b21-132">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="36b21-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="36b21-133">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="36b21-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36b21-134">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="36b21-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="36b21-135">System-Only</span></span>            | <span data-ttu-id="36b21-136">Falso</span><span class="sxs-lookup"><span data-stu-id="36b21-136">False</span></span>                                     |
| <span data-ttu-id="36b21-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="36b21-137">Is-Single-Valued</span></span>       | <span data-ttu-id="36b21-138">True</span><span class="sxs-lookup"><span data-stu-id="36b21-138">True</span></span>                                      |
| <span data-ttu-id="36b21-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="36b21-139">Is Indexed</span></span>             | <span data-ttu-id="36b21-140">Falso</span><span class="sxs-lookup"><span data-stu-id="36b21-140">False</span></span>                                     |
| <span data-ttu-id="36b21-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="36b21-141">In Global Catalog</span></span>      | <span data-ttu-id="36b21-142">Falso</span><span class="sxs-lookup"><span data-stu-id="36b21-142">False</span></span>                                     |
| <span data-ttu-id="36b21-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="36b21-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="36b21-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="36b21-144">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="36b21-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36b21-145">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="36b21-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36b21-146">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="36b21-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36b21-147">Search-Flags</span></span>           | <span data-ttu-id="36b21-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36b21-148">0x00000000</span></span>                                |
| <span data-ttu-id="36b21-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36b21-149">System-Flags</span></span>           | <span data-ttu-id="36b21-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36b21-150">0x00000010</span></span>                                |
| <span data-ttu-id="36b21-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="36b21-151">Classes used in</span></span>        | [<span data-ttu-id="36b21-152">**Computador**</span><span class="sxs-lookup"><span data-stu-id="36b21-152">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="36b21-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="36b21-153">Windows Server 2003</span></span>



| <span data-ttu-id="36b21-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="36b21-154">Entry</span></span> | <span data-ttu-id="36b21-155">Valor</span><span class="sxs-lookup"><span data-stu-id="36b21-155">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="36b21-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="36b21-156">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="36b21-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36b21-157">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="36b21-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="36b21-158">System-Only</span></span>            | <span data-ttu-id="36b21-159">Falso</span><span class="sxs-lookup"><span data-stu-id="36b21-159">False</span></span>                                     |
| <span data-ttu-id="36b21-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="36b21-160">Is-Single-Valued</span></span>       | <span data-ttu-id="36b21-161">True</span><span class="sxs-lookup"><span data-stu-id="36b21-161">True</span></span>                                      |
| <span data-ttu-id="36b21-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="36b21-162">Is Indexed</span></span>             | <span data-ttu-id="36b21-163">Falso</span><span class="sxs-lookup"><span data-stu-id="36b21-163">False</span></span>                                     |
| <span data-ttu-id="36b21-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="36b21-164">In Global Catalog</span></span>      | <span data-ttu-id="36b21-165">Falso</span><span class="sxs-lookup"><span data-stu-id="36b21-165">False</span></span>                                     |
| <span data-ttu-id="36b21-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="36b21-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="36b21-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="36b21-167">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="36b21-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36b21-168">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="36b21-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36b21-169">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="36b21-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36b21-170">Search-Flags</span></span>           | <span data-ttu-id="36b21-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36b21-171">0x00000000</span></span>                                |
| <span data-ttu-id="36b21-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36b21-172">System-Flags</span></span>           | <span data-ttu-id="36b21-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36b21-173">0x00000010</span></span>                                |
| <span data-ttu-id="36b21-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="36b21-174">Classes used in</span></span>        | [<span data-ttu-id="36b21-175">**Computador**</span><span class="sxs-lookup"><span data-stu-id="36b21-175">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="36b21-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="36b21-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="36b21-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="36b21-177">Entry</span></span> | <span data-ttu-id="36b21-178">Valor</span><span class="sxs-lookup"><span data-stu-id="36b21-178">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="36b21-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="36b21-179">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="36b21-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36b21-180">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="36b21-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="36b21-181">System-Only</span></span>            | <span data-ttu-id="36b21-182">Falso</span><span class="sxs-lookup"><span data-stu-id="36b21-182">False</span></span>                                     |
| <span data-ttu-id="36b21-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="36b21-183">Is-Single-Valued</span></span>       | <span data-ttu-id="36b21-184">True</span><span class="sxs-lookup"><span data-stu-id="36b21-184">True</span></span>                                      |
| <span data-ttu-id="36b21-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="36b21-185">Is Indexed</span></span>             | <span data-ttu-id="36b21-186">Falso</span><span class="sxs-lookup"><span data-stu-id="36b21-186">False</span></span>                                     |
| <span data-ttu-id="36b21-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="36b21-187">In Global Catalog</span></span>      | <span data-ttu-id="36b21-188">Falso</span><span class="sxs-lookup"><span data-stu-id="36b21-188">False</span></span>                                     |
| <span data-ttu-id="36b21-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="36b21-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="36b21-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="36b21-190">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="36b21-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36b21-191">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="36b21-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36b21-192">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="36b21-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36b21-193">Search-Flags</span></span>           | <span data-ttu-id="36b21-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36b21-194">0x00000000</span></span>                                |
| <span data-ttu-id="36b21-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36b21-195">System-Flags</span></span>           | <span data-ttu-id="36b21-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36b21-196">0x00000010</span></span>                                |
| <span data-ttu-id="36b21-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="36b21-197">Classes used in</span></span>        | [<span data-ttu-id="36b21-198">**Computador**</span><span class="sxs-lookup"><span data-stu-id="36b21-198">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="36b21-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36b21-199">Windows Server 2008</span></span>



| <span data-ttu-id="36b21-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="36b21-200">Entry</span></span> | <span data-ttu-id="36b21-201">Valor</span><span class="sxs-lookup"><span data-stu-id="36b21-201">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="36b21-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="36b21-202">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="36b21-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36b21-203">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="36b21-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="36b21-204">System-Only</span></span>            | <span data-ttu-id="36b21-205">Falso</span><span class="sxs-lookup"><span data-stu-id="36b21-205">False</span></span>                                     |
| <span data-ttu-id="36b21-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="36b21-206">Is-Single-Valued</span></span>       | <span data-ttu-id="36b21-207">True</span><span class="sxs-lookup"><span data-stu-id="36b21-207">True</span></span>                                      |
| <span data-ttu-id="36b21-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="36b21-208">Is Indexed</span></span>             | <span data-ttu-id="36b21-209">Falso</span><span class="sxs-lookup"><span data-stu-id="36b21-209">False</span></span>                                     |
| <span data-ttu-id="36b21-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="36b21-210">In Global Catalog</span></span>      | <span data-ttu-id="36b21-211">Falso</span><span class="sxs-lookup"><span data-stu-id="36b21-211">False</span></span>                                     |
| <span data-ttu-id="36b21-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="36b21-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="36b21-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="36b21-213">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="36b21-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36b21-214">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="36b21-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36b21-215">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="36b21-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36b21-216">Search-Flags</span></span>           | <span data-ttu-id="36b21-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36b21-217">0x00000000</span></span>                                |
| <span data-ttu-id="36b21-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36b21-218">System-Flags</span></span>           | <span data-ttu-id="36b21-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36b21-219">0x00000010</span></span>                                |
| <span data-ttu-id="36b21-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="36b21-220">Classes used in</span></span>        | [<span data-ttu-id="36b21-221">**Computador**</span><span class="sxs-lookup"><span data-stu-id="36b21-221">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="36b21-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="36b21-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="36b21-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="36b21-223">Entry</span></span> | <span data-ttu-id="36b21-224">Valor</span><span class="sxs-lookup"><span data-stu-id="36b21-224">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="36b21-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="36b21-225">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="36b21-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36b21-226">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="36b21-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="36b21-227">System-Only</span></span>            | <span data-ttu-id="36b21-228">Falso</span><span class="sxs-lookup"><span data-stu-id="36b21-228">False</span></span>                                     |
| <span data-ttu-id="36b21-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="36b21-229">Is-Single-Valued</span></span>       | <span data-ttu-id="36b21-230">True</span><span class="sxs-lookup"><span data-stu-id="36b21-230">True</span></span>                                      |
| <span data-ttu-id="36b21-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="36b21-231">Is Indexed</span></span>             | <span data-ttu-id="36b21-232">Falso</span><span class="sxs-lookup"><span data-stu-id="36b21-232">False</span></span>                                     |
| <span data-ttu-id="36b21-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="36b21-233">In Global Catalog</span></span>      | <span data-ttu-id="36b21-234">Falso</span><span class="sxs-lookup"><span data-stu-id="36b21-234">False</span></span>                                     |
| <span data-ttu-id="36b21-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="36b21-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="36b21-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="36b21-236">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="36b21-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36b21-237">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="36b21-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36b21-238">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="36b21-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36b21-239">Search-Flags</span></span>           | <span data-ttu-id="36b21-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36b21-240">0x00000000</span></span>                                |
| <span data-ttu-id="36b21-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36b21-241">System-Flags</span></span>           | <span data-ttu-id="36b21-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36b21-242">0x00000010</span></span>                                |
| <span data-ttu-id="36b21-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="36b21-243">Classes used in</span></span>        | [<span data-ttu-id="36b21-244">**Computador**</span><span class="sxs-lookup"><span data-stu-id="36b21-244">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="36b21-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="36b21-245">Windows Server 2012</span></span>



| <span data-ttu-id="36b21-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="36b21-246">Entry</span></span> | <span data-ttu-id="36b21-247">Valor</span><span class="sxs-lookup"><span data-stu-id="36b21-247">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="36b21-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="36b21-248">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="36b21-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36b21-249">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="36b21-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="36b21-250">System-Only</span></span>            | <span data-ttu-id="36b21-251">Falso</span><span class="sxs-lookup"><span data-stu-id="36b21-251">False</span></span>                                     |
| <span data-ttu-id="36b21-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="36b21-252">Is-Single-Valued</span></span>       | <span data-ttu-id="36b21-253">True</span><span class="sxs-lookup"><span data-stu-id="36b21-253">True</span></span>                                      |
| <span data-ttu-id="36b21-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="36b21-254">Is Indexed</span></span>             | <span data-ttu-id="36b21-255">Falso</span><span class="sxs-lookup"><span data-stu-id="36b21-255">False</span></span>                                     |
| <span data-ttu-id="36b21-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="36b21-256">In Global Catalog</span></span>      | <span data-ttu-id="36b21-257">Falso</span><span class="sxs-lookup"><span data-stu-id="36b21-257">False</span></span>                                     |
| <span data-ttu-id="36b21-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="36b21-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="36b21-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="36b21-259">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="36b21-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36b21-260">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="36b21-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36b21-261">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="36b21-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36b21-262">Search-Flags</span></span>           | <span data-ttu-id="36b21-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36b21-263">0x00000000</span></span>                                |
| <span data-ttu-id="36b21-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36b21-264">System-Flags</span></span>           | <span data-ttu-id="36b21-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36b21-265">0x00000010</span></span>                                |
| <span data-ttu-id="36b21-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="36b21-266">Classes used in</span></span>        | [<span data-ttu-id="36b21-267">**Computador**</span><span class="sxs-lookup"><span data-stu-id="36b21-267">**Computer**</span></span>](c-computer.md)<br/> |



 

 





