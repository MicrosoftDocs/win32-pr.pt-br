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
# <a name="repl-topology-stay-of-execution-attribute"></a><span data-ttu-id="a6fbe-105">Atributo repl-Topology-continue-of-Execution</span><span class="sxs-lookup"><span data-stu-id="a6fbe-105">Repl-Topology-Stay-Of-Execution attribute</span></span>

<span data-ttu-id="a6fbe-106">O atraso entre a exclusão de um objeto de servidor e a remoção permanente da topologia de replicação.</span><span class="sxs-lookup"><span data-stu-id="a6fbe-106">The delay between deleting a server object and it being permanently removed from the replication topology.</span></span>



| <span data-ttu-id="a6fbe-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a6fbe-107">Entry</span></span> | <span data-ttu-id="a6fbe-108">Valor</span><span class="sxs-lookup"><span data-stu-id="a6fbe-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a6fbe-109">CN</span><span class="sxs-lookup"><span data-stu-id="a6fbe-109">CN</span></span>                | <span data-ttu-id="a6fbe-110">Repl-topologia-permanecer de execução</span><span class="sxs-lookup"><span data-stu-id="a6fbe-110">Repl-Topology-Stay-Of-Execution</span></span>      |
| <span data-ttu-id="a6fbe-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a6fbe-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a6fbe-112">replTopologyStayOfExecution</span><span class="sxs-lookup"><span data-stu-id="a6fbe-112">replTopologyStayOfExecution</span></span>          |
| <span data-ttu-id="a6fbe-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a6fbe-113">Size</span></span>              | <span data-ttu-id="a6fbe-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="a6fbe-114">4 bytes</span></span>                              |
| <span data-ttu-id="a6fbe-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a6fbe-115">Update Privilege</span></span>  | <span data-ttu-id="a6fbe-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="a6fbe-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="a6fbe-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a6fbe-117">Update Frequency</span></span>  | <span data-ttu-id="a6fbe-118">Sempre que um objeto de servidor é excluído.</span><span class="sxs-lookup"><span data-stu-id="a6fbe-118">Whenever a server object is deleted.</span></span> |
| <span data-ttu-id="a6fbe-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a6fbe-119">Attribute-Id</span></span>      | <span data-ttu-id="a6fbe-120">1.2.840.113556.1.4.677</span><span class="sxs-lookup"><span data-stu-id="a6fbe-120">1.2.840.113556.1.4.677</span></span>               |
| <span data-ttu-id="a6fbe-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a6fbe-121">System-Id-Guid</span></span>    | <span data-ttu-id="a6fbe-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a6fbe-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="a6fbe-123">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6fbe-123">Syntax</span></span>            | [<span data-ttu-id="a6fbe-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="a6fbe-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="a6fbe-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="a6fbe-125">Implementations</span></span>

-   [<span data-ttu-id="a6fbe-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a6fbe-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a6fbe-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a6fbe-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a6fbe-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a6fbe-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a6fbe-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a6fbe-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a6fbe-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a6fbe-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a6fbe-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a6fbe-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a6fbe-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a6fbe-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a6fbe-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a6fbe-133">Windows 2000 Server</span></span>



| <span data-ttu-id="a6fbe-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="a6fbe-134">Entry</span></span> | <span data-ttu-id="a6fbe-135">Valor</span><span class="sxs-lookup"><span data-stu-id="a6fbe-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a6fbe-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="a6fbe-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a6fbe-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6fbe-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a6fbe-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6fbe-138">System-Only</span></span>            | <span data-ttu-id="a6fbe-139">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-139">False</span></span>                                            |
| <span data-ttu-id="a6fbe-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a6fbe-140">Is-Single-Valued</span></span>       | <span data-ttu-id="a6fbe-141">True</span><span class="sxs-lookup"><span data-stu-id="a6fbe-141">True</span></span>                                             |
| <span data-ttu-id="a6fbe-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="a6fbe-142">Is Indexed</span></span>             | <span data-ttu-id="a6fbe-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-143">False</span></span>                                            |
| <span data-ttu-id="a6fbe-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a6fbe-144">In Global Catalog</span></span>      | <span data-ttu-id="a6fbe-145">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-145">False</span></span>                                            |
| <span data-ttu-id="a6fbe-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a6fbe-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6fbe-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a6fbe-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a6fbe-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6fbe-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a6fbe-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6fbe-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a6fbe-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6fbe-150">Search-Flags</span></span>           | <span data-ttu-id="a6fbe-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6fbe-151">0x00000000</span></span>                                       |
| <span data-ttu-id="a6fbe-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6fbe-152">System-Flags</span></span>           | <span data-ttu-id="a6fbe-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6fbe-153">0x00000010</span></span>                                       |
| <span data-ttu-id="a6fbe-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a6fbe-154">Classes used in</span></span>        | [<span data-ttu-id="a6fbe-155">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="a6fbe-155">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a6fbe-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a6fbe-156">Windows Server 2003</span></span>



| <span data-ttu-id="a6fbe-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="a6fbe-157">Entry</span></span> | <span data-ttu-id="a6fbe-158">Valor</span><span class="sxs-lookup"><span data-stu-id="a6fbe-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a6fbe-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="a6fbe-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a6fbe-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6fbe-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a6fbe-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6fbe-161">System-Only</span></span>            | <span data-ttu-id="a6fbe-162">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-162">False</span></span>                                            |
| <span data-ttu-id="a6fbe-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a6fbe-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a6fbe-164">True</span><span class="sxs-lookup"><span data-stu-id="a6fbe-164">True</span></span>                                             |
| <span data-ttu-id="a6fbe-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="a6fbe-165">Is Indexed</span></span>             | <span data-ttu-id="a6fbe-166">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-166">False</span></span>                                            |
| <span data-ttu-id="a6fbe-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a6fbe-167">In Global Catalog</span></span>      | <span data-ttu-id="a6fbe-168">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-168">False</span></span>                                            |
| <span data-ttu-id="a6fbe-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a6fbe-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6fbe-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a6fbe-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a6fbe-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6fbe-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a6fbe-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6fbe-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a6fbe-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6fbe-173">Search-Flags</span></span>           | <span data-ttu-id="a6fbe-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6fbe-174">0x00000000</span></span>                                       |
| <span data-ttu-id="a6fbe-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6fbe-175">System-Flags</span></span>           | <span data-ttu-id="a6fbe-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6fbe-176">0x00000010</span></span>                                       |
| <span data-ttu-id="a6fbe-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a6fbe-177">Classes used in</span></span>        | [<span data-ttu-id="a6fbe-178">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="a6fbe-178">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a6fbe-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="a6fbe-179">ADAM</span></span>



| <span data-ttu-id="a6fbe-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="a6fbe-180">Entry</span></span> | <span data-ttu-id="a6fbe-181">Valor</span><span class="sxs-lookup"><span data-stu-id="a6fbe-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a6fbe-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="a6fbe-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a6fbe-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6fbe-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a6fbe-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6fbe-184">System-Only</span></span>            | <span data-ttu-id="a6fbe-185">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-185">False</span></span>                                            |
| <span data-ttu-id="a6fbe-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a6fbe-186">Is-Single-Valued</span></span>       | <span data-ttu-id="a6fbe-187">True</span><span class="sxs-lookup"><span data-stu-id="a6fbe-187">True</span></span>                                             |
| <span data-ttu-id="a6fbe-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="a6fbe-188">Is Indexed</span></span>             | <span data-ttu-id="a6fbe-189">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-189">False</span></span>                                            |
| <span data-ttu-id="a6fbe-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a6fbe-190">In Global Catalog</span></span>      | <span data-ttu-id="a6fbe-191">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-191">False</span></span>                                            |
| <span data-ttu-id="a6fbe-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a6fbe-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6fbe-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a6fbe-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a6fbe-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6fbe-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a6fbe-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6fbe-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a6fbe-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6fbe-196">Search-Flags</span></span>           | <span data-ttu-id="a6fbe-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6fbe-197">0x00000000</span></span>                                       |
| <span data-ttu-id="a6fbe-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6fbe-198">System-Flags</span></span>           | <span data-ttu-id="a6fbe-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6fbe-199">0x00000010</span></span>                                       |
| <span data-ttu-id="a6fbe-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a6fbe-200">Classes used in</span></span>        | [<span data-ttu-id="a6fbe-201">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="a6fbe-201">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a6fbe-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a6fbe-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a6fbe-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="a6fbe-203">Entry</span></span> | <span data-ttu-id="a6fbe-204">Valor</span><span class="sxs-lookup"><span data-stu-id="a6fbe-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a6fbe-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="a6fbe-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a6fbe-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6fbe-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a6fbe-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6fbe-207">System-Only</span></span>            | <span data-ttu-id="a6fbe-208">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-208">False</span></span>                                            |
| <span data-ttu-id="a6fbe-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a6fbe-209">Is-Single-Valued</span></span>       | <span data-ttu-id="a6fbe-210">True</span><span class="sxs-lookup"><span data-stu-id="a6fbe-210">True</span></span>                                             |
| <span data-ttu-id="a6fbe-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="a6fbe-211">Is Indexed</span></span>             | <span data-ttu-id="a6fbe-212">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-212">False</span></span>                                            |
| <span data-ttu-id="a6fbe-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a6fbe-213">In Global Catalog</span></span>      | <span data-ttu-id="a6fbe-214">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-214">False</span></span>                                            |
| <span data-ttu-id="a6fbe-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a6fbe-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6fbe-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a6fbe-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a6fbe-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6fbe-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a6fbe-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6fbe-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a6fbe-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6fbe-219">Search-Flags</span></span>           | <span data-ttu-id="a6fbe-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6fbe-220">0x00000000</span></span>                                       |
| <span data-ttu-id="a6fbe-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6fbe-221">System-Flags</span></span>           | <span data-ttu-id="a6fbe-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6fbe-222">0x00000010</span></span>                                       |
| <span data-ttu-id="a6fbe-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a6fbe-223">Classes used in</span></span>        | [<span data-ttu-id="a6fbe-224">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="a6fbe-224">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a6fbe-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6fbe-225">Windows Server 2008</span></span>



| <span data-ttu-id="a6fbe-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="a6fbe-226">Entry</span></span> | <span data-ttu-id="a6fbe-227">Valor</span><span class="sxs-lookup"><span data-stu-id="a6fbe-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a6fbe-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="a6fbe-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a6fbe-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6fbe-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a6fbe-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6fbe-230">System-Only</span></span>            | <span data-ttu-id="a6fbe-231">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-231">False</span></span>                                            |
| <span data-ttu-id="a6fbe-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a6fbe-232">Is-Single-Valued</span></span>       | <span data-ttu-id="a6fbe-233">True</span><span class="sxs-lookup"><span data-stu-id="a6fbe-233">True</span></span>                                             |
| <span data-ttu-id="a6fbe-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="a6fbe-234">Is Indexed</span></span>             | <span data-ttu-id="a6fbe-235">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-235">False</span></span>                                            |
| <span data-ttu-id="a6fbe-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a6fbe-236">In Global Catalog</span></span>      | <span data-ttu-id="a6fbe-237">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-237">False</span></span>                                            |
| <span data-ttu-id="a6fbe-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a6fbe-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6fbe-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a6fbe-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a6fbe-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6fbe-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a6fbe-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6fbe-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a6fbe-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6fbe-242">Search-Flags</span></span>           | <span data-ttu-id="a6fbe-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6fbe-243">0x00000000</span></span>                                       |
| <span data-ttu-id="a6fbe-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6fbe-244">System-Flags</span></span>           | <span data-ttu-id="a6fbe-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6fbe-245">0x00000010</span></span>                                       |
| <span data-ttu-id="a6fbe-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a6fbe-246">Classes used in</span></span>        | [<span data-ttu-id="a6fbe-247">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="a6fbe-247">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a6fbe-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a6fbe-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a6fbe-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="a6fbe-249">Entry</span></span> | <span data-ttu-id="a6fbe-250">Valor</span><span class="sxs-lookup"><span data-stu-id="a6fbe-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a6fbe-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="a6fbe-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a6fbe-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6fbe-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a6fbe-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6fbe-253">System-Only</span></span>            | <span data-ttu-id="a6fbe-254">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-254">False</span></span>                                            |
| <span data-ttu-id="a6fbe-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a6fbe-255">Is-Single-Valued</span></span>       | <span data-ttu-id="a6fbe-256">True</span><span class="sxs-lookup"><span data-stu-id="a6fbe-256">True</span></span>                                             |
| <span data-ttu-id="a6fbe-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="a6fbe-257">Is Indexed</span></span>             | <span data-ttu-id="a6fbe-258">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-258">False</span></span>                                            |
| <span data-ttu-id="a6fbe-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a6fbe-259">In Global Catalog</span></span>      | <span data-ttu-id="a6fbe-260">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-260">False</span></span>                                            |
| <span data-ttu-id="a6fbe-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a6fbe-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6fbe-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a6fbe-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a6fbe-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6fbe-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a6fbe-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6fbe-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a6fbe-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6fbe-265">Search-Flags</span></span>           | <span data-ttu-id="a6fbe-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6fbe-266">0x00000000</span></span>                                       |
| <span data-ttu-id="a6fbe-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6fbe-267">System-Flags</span></span>           | <span data-ttu-id="a6fbe-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6fbe-268">0x00000010</span></span>                                       |
| <span data-ttu-id="a6fbe-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a6fbe-269">Classes used in</span></span>        | [<span data-ttu-id="a6fbe-270">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="a6fbe-270">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a6fbe-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a6fbe-271">Windows Server 2012</span></span>



| <span data-ttu-id="a6fbe-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="a6fbe-272">Entry</span></span> | <span data-ttu-id="a6fbe-273">Valor</span><span class="sxs-lookup"><span data-stu-id="a6fbe-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a6fbe-274">ID do link</span><span class="sxs-lookup"><span data-stu-id="a6fbe-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a6fbe-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6fbe-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a6fbe-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6fbe-276">System-Only</span></span>            | <span data-ttu-id="a6fbe-277">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-277">False</span></span>                                            |
| <span data-ttu-id="a6fbe-278">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a6fbe-278">Is-Single-Valued</span></span>       | <span data-ttu-id="a6fbe-279">True</span><span class="sxs-lookup"><span data-stu-id="a6fbe-279">True</span></span>                                             |
| <span data-ttu-id="a6fbe-280">É indexado</span><span class="sxs-lookup"><span data-stu-id="a6fbe-280">Is Indexed</span></span>             | <span data-ttu-id="a6fbe-281">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-281">False</span></span>                                            |
| <span data-ttu-id="a6fbe-282">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a6fbe-282">In Global Catalog</span></span>      | <span data-ttu-id="a6fbe-283">Falso</span><span class="sxs-lookup"><span data-stu-id="a6fbe-283">False</span></span>                                            |
| <span data-ttu-id="a6fbe-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a6fbe-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6fbe-285">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a6fbe-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a6fbe-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6fbe-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a6fbe-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6fbe-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a6fbe-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6fbe-288">Search-Flags</span></span>           | <span data-ttu-id="a6fbe-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6fbe-289">0x00000000</span></span>                                       |
| <span data-ttu-id="a6fbe-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6fbe-290">System-Flags</span></span>           | <span data-ttu-id="a6fbe-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6fbe-291">0x00000010</span></span>                                       |
| <span data-ttu-id="a6fbe-292">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a6fbe-292">Classes used in</span></span>        | [<span data-ttu-id="a6fbe-293">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="a6fbe-293">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





