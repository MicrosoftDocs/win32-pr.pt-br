---
title: Atributo repl-Topology-continue-of-Execution
description: O atraso entre a exclusão de um objeto de servidor e a remoção permanente da topologia de replicação.
ms.assetid: 770231b0-4886-41c2-a3b5-ac488ac09669
ms.tgt_platform: multiple
keywords:
- Replicação de repl-Topology-continue-of-Execution do esquema do AD
- Esquema de AD do atributo replTopologyStayOfExecution
topic_type:
- apiref
api_name:
- Repl-Topology-Stay-Of-Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51c74c477cce926dd18ea17b8df2b1adcf99df1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645413"
---
# <a name="repl-topology-stay-of-execution-attribute"></a><span data-ttu-id="ff9bc-105">Atributo repl-Topology-continue-of-Execution</span><span class="sxs-lookup"><span data-stu-id="ff9bc-105">Repl-Topology-Stay-Of-Execution attribute</span></span>

<span data-ttu-id="ff9bc-106">O atraso entre a exclusão de um objeto de servidor e a remoção permanente da topologia de replicação.</span><span class="sxs-lookup"><span data-stu-id="ff9bc-106">The delay between deleting a server object and it being permanently removed from the replication topology.</span></span>



| <span data-ttu-id="ff9bc-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff9bc-107">Entry</span></span> | <span data-ttu-id="ff9bc-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ff9bc-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ff9bc-109">CN</span><span class="sxs-lookup"><span data-stu-id="ff9bc-109">CN</span></span>                | <span data-ttu-id="ff9bc-110">Repl-topologia-permanecer de execução</span><span class="sxs-lookup"><span data-stu-id="ff9bc-110">Repl-Topology-Stay-Of-Execution</span></span>      |
| <span data-ttu-id="ff9bc-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ff9bc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ff9bc-112">replTopologyStayOfExecution</span><span class="sxs-lookup"><span data-stu-id="ff9bc-112">replTopologyStayOfExecution</span></span>          |
| <span data-ttu-id="ff9bc-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ff9bc-113">Size</span></span>              | <span data-ttu-id="ff9bc-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="ff9bc-114">4 bytes</span></span>                              |
| <span data-ttu-id="ff9bc-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="ff9bc-115">Update Privilege</span></span>  | <span data-ttu-id="ff9bc-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="ff9bc-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="ff9bc-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="ff9bc-117">Update Frequency</span></span>  | <span data-ttu-id="ff9bc-118">Sempre que um objeto de servidor é excluído.</span><span class="sxs-lookup"><span data-stu-id="ff9bc-118">Whenever a server object is deleted.</span></span> |
| <span data-ttu-id="ff9bc-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ff9bc-119">Attribute-Id</span></span>      | <span data-ttu-id="ff9bc-120">1.2.840.113556.1.4.677</span><span class="sxs-lookup"><span data-stu-id="ff9bc-120">1.2.840.113556.1.4.677</span></span>               |
| <span data-ttu-id="ff9bc-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ff9bc-121">System-Id-Guid</span></span>    | <span data-ttu-id="ff9bc-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ff9bc-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="ff9bc-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff9bc-123">Syntax</span></span>            | [<span data-ttu-id="ff9bc-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="ff9bc-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ff9bc-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="ff9bc-125">Implementations</span></span>

-   [<span data-ttu-id="ff9bc-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ff9bc-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ff9bc-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ff9bc-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ff9bc-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ff9bc-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ff9bc-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ff9bc-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ff9bc-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ff9bc-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ff9bc-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ff9bc-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ff9bc-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ff9bc-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ff9bc-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ff9bc-133">Windows 2000 Server</span></span>



| <span data-ttu-id="ff9bc-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff9bc-134">Entry</span></span> | <span data-ttu-id="ff9bc-135">Valor</span><span class="sxs-lookup"><span data-stu-id="ff9bc-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ff9bc-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="ff9bc-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ff9bc-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff9bc-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ff9bc-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff9bc-138">System-Only</span></span>            | <span data-ttu-id="ff9bc-139">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-139">False</span></span>                                            |
| <span data-ttu-id="ff9bc-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ff9bc-140">Is-Single-Valued</span></span>       | <span data-ttu-id="ff9bc-141">True</span><span class="sxs-lookup"><span data-stu-id="ff9bc-141">True</span></span>                                             |
| <span data-ttu-id="ff9bc-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="ff9bc-142">Is Indexed</span></span>             | <span data-ttu-id="ff9bc-143">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-143">False</span></span>                                            |
| <span data-ttu-id="ff9bc-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff9bc-144">In Global Catalog</span></span>      | <span data-ttu-id="ff9bc-145">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-145">False</span></span>                                            |
| <span data-ttu-id="ff9bc-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ff9bc-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff9bc-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ff9bc-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ff9bc-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff9bc-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ff9bc-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff9bc-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ff9bc-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff9bc-150">Search-Flags</span></span>           | <span data-ttu-id="ff9bc-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff9bc-151">0x00000000</span></span>                                       |
| <span data-ttu-id="ff9bc-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff9bc-152">System-Flags</span></span>           | <span data-ttu-id="ff9bc-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff9bc-153">0x00000010</span></span>                                       |
| <span data-ttu-id="ff9bc-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ff9bc-154">Classes used in</span></span>        | [<span data-ttu-id="ff9bc-155">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="ff9bc-155">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ff9bc-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ff9bc-156">Windows Server 2003</span></span>



| <span data-ttu-id="ff9bc-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff9bc-157">Entry</span></span> | <span data-ttu-id="ff9bc-158">Valor</span><span class="sxs-lookup"><span data-stu-id="ff9bc-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ff9bc-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="ff9bc-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ff9bc-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff9bc-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ff9bc-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff9bc-161">System-Only</span></span>            | <span data-ttu-id="ff9bc-162">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-162">False</span></span>                                            |
| <span data-ttu-id="ff9bc-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ff9bc-163">Is-Single-Valued</span></span>       | <span data-ttu-id="ff9bc-164">True</span><span class="sxs-lookup"><span data-stu-id="ff9bc-164">True</span></span>                                             |
| <span data-ttu-id="ff9bc-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="ff9bc-165">Is Indexed</span></span>             | <span data-ttu-id="ff9bc-166">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-166">False</span></span>                                            |
| <span data-ttu-id="ff9bc-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff9bc-167">In Global Catalog</span></span>      | <span data-ttu-id="ff9bc-168">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-168">False</span></span>                                            |
| <span data-ttu-id="ff9bc-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ff9bc-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff9bc-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ff9bc-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ff9bc-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff9bc-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ff9bc-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff9bc-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ff9bc-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff9bc-173">Search-Flags</span></span>           | <span data-ttu-id="ff9bc-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff9bc-174">0x00000000</span></span>                                       |
| <span data-ttu-id="ff9bc-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff9bc-175">System-Flags</span></span>           | <span data-ttu-id="ff9bc-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff9bc-176">0x00000010</span></span>                                       |
| <span data-ttu-id="ff9bc-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ff9bc-177">Classes used in</span></span>        | [<span data-ttu-id="ff9bc-178">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="ff9bc-178">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ff9bc-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="ff9bc-179">ADAM</span></span>



| <span data-ttu-id="ff9bc-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff9bc-180">Entry</span></span> | <span data-ttu-id="ff9bc-181">Valor</span><span class="sxs-lookup"><span data-stu-id="ff9bc-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ff9bc-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="ff9bc-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ff9bc-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff9bc-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ff9bc-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff9bc-184">System-Only</span></span>            | <span data-ttu-id="ff9bc-185">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-185">False</span></span>                                            |
| <span data-ttu-id="ff9bc-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ff9bc-186">Is-Single-Valued</span></span>       | <span data-ttu-id="ff9bc-187">True</span><span class="sxs-lookup"><span data-stu-id="ff9bc-187">True</span></span>                                             |
| <span data-ttu-id="ff9bc-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="ff9bc-188">Is Indexed</span></span>             | <span data-ttu-id="ff9bc-189">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-189">False</span></span>                                            |
| <span data-ttu-id="ff9bc-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff9bc-190">In Global Catalog</span></span>      | <span data-ttu-id="ff9bc-191">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-191">False</span></span>                                            |
| <span data-ttu-id="ff9bc-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ff9bc-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff9bc-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ff9bc-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ff9bc-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff9bc-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ff9bc-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff9bc-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ff9bc-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff9bc-196">Search-Flags</span></span>           | <span data-ttu-id="ff9bc-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff9bc-197">0x00000000</span></span>                                       |
| <span data-ttu-id="ff9bc-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff9bc-198">System-Flags</span></span>           | <span data-ttu-id="ff9bc-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff9bc-199">0x00000010</span></span>                                       |
| <span data-ttu-id="ff9bc-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ff9bc-200">Classes used in</span></span>        | [<span data-ttu-id="ff9bc-201">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="ff9bc-201">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ff9bc-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ff9bc-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ff9bc-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff9bc-203">Entry</span></span> | <span data-ttu-id="ff9bc-204">Valor</span><span class="sxs-lookup"><span data-stu-id="ff9bc-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ff9bc-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="ff9bc-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ff9bc-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff9bc-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ff9bc-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff9bc-207">System-Only</span></span>            | <span data-ttu-id="ff9bc-208">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-208">False</span></span>                                            |
| <span data-ttu-id="ff9bc-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ff9bc-209">Is-Single-Valued</span></span>       | <span data-ttu-id="ff9bc-210">True</span><span class="sxs-lookup"><span data-stu-id="ff9bc-210">True</span></span>                                             |
| <span data-ttu-id="ff9bc-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="ff9bc-211">Is Indexed</span></span>             | <span data-ttu-id="ff9bc-212">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-212">False</span></span>                                            |
| <span data-ttu-id="ff9bc-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff9bc-213">In Global Catalog</span></span>      | <span data-ttu-id="ff9bc-214">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-214">False</span></span>                                            |
| <span data-ttu-id="ff9bc-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ff9bc-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff9bc-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ff9bc-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ff9bc-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff9bc-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ff9bc-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff9bc-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ff9bc-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff9bc-219">Search-Flags</span></span>           | <span data-ttu-id="ff9bc-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff9bc-220">0x00000000</span></span>                                       |
| <span data-ttu-id="ff9bc-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff9bc-221">System-Flags</span></span>           | <span data-ttu-id="ff9bc-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff9bc-222">0x00000010</span></span>                                       |
| <span data-ttu-id="ff9bc-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ff9bc-223">Classes used in</span></span>        | [<span data-ttu-id="ff9bc-224">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="ff9bc-224">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ff9bc-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff9bc-225">Windows Server 2008</span></span>



| <span data-ttu-id="ff9bc-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff9bc-226">Entry</span></span> | <span data-ttu-id="ff9bc-227">Valor</span><span class="sxs-lookup"><span data-stu-id="ff9bc-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ff9bc-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="ff9bc-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ff9bc-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff9bc-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ff9bc-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff9bc-230">System-Only</span></span>            | <span data-ttu-id="ff9bc-231">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-231">False</span></span>                                            |
| <span data-ttu-id="ff9bc-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ff9bc-232">Is-Single-Valued</span></span>       | <span data-ttu-id="ff9bc-233">True</span><span class="sxs-lookup"><span data-stu-id="ff9bc-233">True</span></span>                                             |
| <span data-ttu-id="ff9bc-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="ff9bc-234">Is Indexed</span></span>             | <span data-ttu-id="ff9bc-235">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-235">False</span></span>                                            |
| <span data-ttu-id="ff9bc-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff9bc-236">In Global Catalog</span></span>      | <span data-ttu-id="ff9bc-237">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-237">False</span></span>                                            |
| <span data-ttu-id="ff9bc-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ff9bc-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff9bc-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ff9bc-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ff9bc-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff9bc-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ff9bc-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff9bc-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ff9bc-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff9bc-242">Search-Flags</span></span>           | <span data-ttu-id="ff9bc-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff9bc-243">0x00000000</span></span>                                       |
| <span data-ttu-id="ff9bc-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff9bc-244">System-Flags</span></span>           | <span data-ttu-id="ff9bc-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff9bc-245">0x00000010</span></span>                                       |
| <span data-ttu-id="ff9bc-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ff9bc-246">Classes used in</span></span>        | [<span data-ttu-id="ff9bc-247">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="ff9bc-247">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ff9bc-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ff9bc-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ff9bc-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff9bc-249">Entry</span></span> | <span data-ttu-id="ff9bc-250">Valor</span><span class="sxs-lookup"><span data-stu-id="ff9bc-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ff9bc-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="ff9bc-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ff9bc-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff9bc-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ff9bc-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff9bc-253">System-Only</span></span>            | <span data-ttu-id="ff9bc-254">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-254">False</span></span>                                            |
| <span data-ttu-id="ff9bc-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ff9bc-255">Is-Single-Valued</span></span>       | <span data-ttu-id="ff9bc-256">True</span><span class="sxs-lookup"><span data-stu-id="ff9bc-256">True</span></span>                                             |
| <span data-ttu-id="ff9bc-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="ff9bc-257">Is Indexed</span></span>             | <span data-ttu-id="ff9bc-258">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-258">False</span></span>                                            |
| <span data-ttu-id="ff9bc-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff9bc-259">In Global Catalog</span></span>      | <span data-ttu-id="ff9bc-260">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-260">False</span></span>                                            |
| <span data-ttu-id="ff9bc-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ff9bc-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff9bc-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ff9bc-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ff9bc-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff9bc-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ff9bc-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff9bc-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ff9bc-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff9bc-265">Search-Flags</span></span>           | <span data-ttu-id="ff9bc-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff9bc-266">0x00000000</span></span>                                       |
| <span data-ttu-id="ff9bc-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff9bc-267">System-Flags</span></span>           | <span data-ttu-id="ff9bc-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff9bc-268">0x00000010</span></span>                                       |
| <span data-ttu-id="ff9bc-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ff9bc-269">Classes used in</span></span>        | [<span data-ttu-id="ff9bc-270">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="ff9bc-270">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ff9bc-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ff9bc-271">Windows Server 2012</span></span>



| <span data-ttu-id="ff9bc-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff9bc-272">Entry</span></span> | <span data-ttu-id="ff9bc-273">Valor</span><span class="sxs-lookup"><span data-stu-id="ff9bc-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ff9bc-274">ID do link</span><span class="sxs-lookup"><span data-stu-id="ff9bc-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ff9bc-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff9bc-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ff9bc-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff9bc-276">System-Only</span></span>            | <span data-ttu-id="ff9bc-277">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-277">False</span></span>                                            |
| <span data-ttu-id="ff9bc-278">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ff9bc-278">Is-Single-Valued</span></span>       | <span data-ttu-id="ff9bc-279">True</span><span class="sxs-lookup"><span data-stu-id="ff9bc-279">True</span></span>                                             |
| <span data-ttu-id="ff9bc-280">É indexado</span><span class="sxs-lookup"><span data-stu-id="ff9bc-280">Is Indexed</span></span>             | <span data-ttu-id="ff9bc-281">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-281">False</span></span>                                            |
| <span data-ttu-id="ff9bc-282">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff9bc-282">In Global Catalog</span></span>      | <span data-ttu-id="ff9bc-283">Falso</span><span class="sxs-lookup"><span data-stu-id="ff9bc-283">False</span></span>                                            |
| <span data-ttu-id="ff9bc-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ff9bc-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff9bc-285">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ff9bc-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ff9bc-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff9bc-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ff9bc-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff9bc-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ff9bc-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff9bc-288">Search-Flags</span></span>           | <span data-ttu-id="ff9bc-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff9bc-289">0x00000000</span></span>                                       |
| <span data-ttu-id="ff9bc-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff9bc-290">System-Flags</span></span>           | <span data-ttu-id="ff9bc-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff9bc-291">0x00000010</span></span>                                       |
| <span data-ttu-id="ff9bc-292">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ff9bc-292">Classes used in</span></span>        | [<span data-ttu-id="ff9bc-293">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="ff9bc-293">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





