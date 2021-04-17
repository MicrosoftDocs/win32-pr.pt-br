---
title: Atributo repl-UpToDate-vector
description: Rastreia informações de estado de replicação interna para um NC inteiro. As informações aqui podem ser extraídas em formato público por meio da API DsReplicaGetInfo (). Presente em todos os objetos raiz NC.
ms.assetid: f23d94f8-c31b-447f-98c3-c35a4f5f1d43
ms.tgt_platform: multiple
keywords:
- Repl-UpToDate-esquema de AD do atributo de vetor
- Esquema de AD do atributo replUpToDateVector
topic_type:
- apiref
api_name:
- Repl-UpToDate-Vector
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9263111459d01d99cf5990d1c818b5ff2a7a19be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105762828"
---
# <a name="repl-uptodate-vector-attribute"></a><span data-ttu-id="a1246-107">Atributo repl-UpToDate-vector</span><span class="sxs-lookup"><span data-stu-id="a1246-107">Repl-UpToDate-Vector attribute</span></span>

<span data-ttu-id="a1246-108">Rastreia informações de estado de replicação interna para um NC inteiro.</span><span class="sxs-lookup"><span data-stu-id="a1246-108">Tracks internal replication state information for an entire NC.</span></span> <span data-ttu-id="a1246-109">As informações aqui podem ser extraídas em formato público por meio da API DsReplicaGetInfo ().</span><span class="sxs-lookup"><span data-stu-id="a1246-109">Information here can be extracted in public form through the API DsReplicaGetInfo().</span></span> <span data-ttu-id="a1246-110">Presente em todos os objetos raiz NC.</span><span class="sxs-lookup"><span data-stu-id="a1246-110">Present on all NC root objects.</span></span>



| <span data-ttu-id="a1246-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1246-111">Entry</span></span> | <span data-ttu-id="a1246-112">Valor</span><span class="sxs-lookup"><span data-stu-id="a1246-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a1246-113">CN</span><span class="sxs-lookup"><span data-stu-id="a1246-113">CN</span></span>                | <span data-ttu-id="a1246-114">Repl-UpToDate-vector</span><span class="sxs-lookup"><span data-stu-id="a1246-114">Repl-UpToDate-Vector</span></span>                                                           |
| <span data-ttu-id="a1246-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a1246-115">Ldap-Display-Name</span></span> | <span data-ttu-id="a1246-116">replUpToDateVector</span><span class="sxs-lookup"><span data-stu-id="a1246-116">replUpToDateVector</span></span>                                                             |
| <span data-ttu-id="a1246-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a1246-117">Size</span></span>              | <span data-ttu-id="a1246-118">O comprimento é proporcional ao número de réplicas (passado e presente) do NC.</span><span class="sxs-lookup"><span data-stu-id="a1246-118">Length is proportional to the number of replicas (past and present) of the NC.</span></span> |
| <span data-ttu-id="a1246-119">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a1246-119">Update Privilege</span></span>  | <span data-ttu-id="a1246-120">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="a1246-120">This value is set by the system.</span></span>                                               |
| <span data-ttu-id="a1246-121">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a1246-121">Update Frequency</span></span>  | <span data-ttu-id="a1246-122">Alterações em resposta a ciclos de replicação de entrada concluídos.</span><span class="sxs-lookup"><span data-stu-id="a1246-122">Changes in response to completed inbound replication cycles.</span></span>                   |
| <span data-ttu-id="a1246-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a1246-123">Attribute-Id</span></span>      | <span data-ttu-id="a1246-124">1.2.840.113556.1.4.4</span><span class="sxs-lookup"><span data-stu-id="a1246-124">1.2.840.113556.1.4.4</span></span>                                                           |
| <span data-ttu-id="a1246-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a1246-125">System-Id-Guid</span></span>    | <span data-ttu-id="a1246-126">bf967a16-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a1246-126">bf967a16-0de6-11d0-a285-00aa003049e2</span></span>                                           |
| <span data-ttu-id="a1246-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1246-127">Syntax</span></span>            | [<span data-ttu-id="a1246-128">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="a1246-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                          |



## <a name="implementations"></a><span data-ttu-id="a1246-129">Implementações</span><span class="sxs-lookup"><span data-stu-id="a1246-129">Implementations</span></span>

-   [<span data-ttu-id="a1246-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a1246-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a1246-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a1246-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a1246-132">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a1246-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a1246-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a1246-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a1246-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a1246-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a1246-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a1246-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a1246-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a1246-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a1246-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a1246-137">Windows 2000 Server</span></span>



| <span data-ttu-id="a1246-138">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1246-138">Entry</span></span> | <span data-ttu-id="a1246-139">Valor</span><span class="sxs-lookup"><span data-stu-id="a1246-139">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a1246-140">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1246-140">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a1246-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1246-141">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a1246-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1246-142">System-Only</span></span>            | <span data-ttu-id="a1246-143">True</span><span class="sxs-lookup"><span data-stu-id="a1246-143">True</span></span>                            |
| <span data-ttu-id="a1246-144">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1246-144">Is-Single-Valued</span></span>       | <span data-ttu-id="a1246-145">True</span><span class="sxs-lookup"><span data-stu-id="a1246-145">True</span></span>                            |
| <span data-ttu-id="a1246-146">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1246-146">Is Indexed</span></span>             | <span data-ttu-id="a1246-147">Falso</span><span class="sxs-lookup"><span data-stu-id="a1246-147">False</span></span>                           |
| <span data-ttu-id="a1246-148">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1246-148">In Global Catalog</span></span>      | <span data-ttu-id="a1246-149">True</span><span class="sxs-lookup"><span data-stu-id="a1246-149">True</span></span>                            |
| <span data-ttu-id="a1246-150">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1246-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1246-151">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1246-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a1246-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1246-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a1246-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1246-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a1246-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1246-154">Search-Flags</span></span>           | <span data-ttu-id="a1246-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1246-155">0x00000000</span></span>                      |
| <span data-ttu-id="a1246-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1246-156">System-Flags</span></span>           | <span data-ttu-id="a1246-157">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a1246-157">0x00000013</span></span>                      |
| <span data-ttu-id="a1246-158">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1246-158">Classes used in</span></span>        | [<span data-ttu-id="a1246-159">**Início**</span><span class="sxs-lookup"><span data-stu-id="a1246-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a1246-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a1246-160">Windows Server 2003</span></span>



| <span data-ttu-id="a1246-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1246-161">Entry</span></span> | <span data-ttu-id="a1246-162">Valor</span><span class="sxs-lookup"><span data-stu-id="a1246-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a1246-163">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1246-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a1246-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1246-164">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a1246-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1246-165">System-Only</span></span>            | <span data-ttu-id="a1246-166">True</span><span class="sxs-lookup"><span data-stu-id="a1246-166">True</span></span>                            |
| <span data-ttu-id="a1246-167">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1246-167">Is-Single-Valued</span></span>       | <span data-ttu-id="a1246-168">True</span><span class="sxs-lookup"><span data-stu-id="a1246-168">True</span></span>                            |
| <span data-ttu-id="a1246-169">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1246-169">Is Indexed</span></span>             | <span data-ttu-id="a1246-170">Falso</span><span class="sxs-lookup"><span data-stu-id="a1246-170">False</span></span>                           |
| <span data-ttu-id="a1246-171">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1246-171">In Global Catalog</span></span>      | <span data-ttu-id="a1246-172">True</span><span class="sxs-lookup"><span data-stu-id="a1246-172">True</span></span>                            |
| <span data-ttu-id="a1246-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1246-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1246-174">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1246-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a1246-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1246-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a1246-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1246-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a1246-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1246-177">Search-Flags</span></span>           | <span data-ttu-id="a1246-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1246-178">0x00000000</span></span>                      |
| <span data-ttu-id="a1246-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1246-179">System-Flags</span></span>           | <span data-ttu-id="a1246-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a1246-180">0x00000013</span></span>                      |
| <span data-ttu-id="a1246-181">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1246-181">Classes used in</span></span>        | [<span data-ttu-id="a1246-182">**Início**</span><span class="sxs-lookup"><span data-stu-id="a1246-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a1246-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="a1246-183">ADAM</span></span>



| <span data-ttu-id="a1246-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1246-184">Entry</span></span> | <span data-ttu-id="a1246-185">Valor</span><span class="sxs-lookup"><span data-stu-id="a1246-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a1246-186">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1246-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a1246-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1246-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a1246-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1246-188">System-Only</span></span>            | <span data-ttu-id="a1246-189">True</span><span class="sxs-lookup"><span data-stu-id="a1246-189">True</span></span>                            |
| <span data-ttu-id="a1246-190">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1246-190">Is-Single-Valued</span></span>       | <span data-ttu-id="a1246-191">True</span><span class="sxs-lookup"><span data-stu-id="a1246-191">True</span></span>                            |
| <span data-ttu-id="a1246-192">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1246-192">Is Indexed</span></span>             | <span data-ttu-id="a1246-193">Falso</span><span class="sxs-lookup"><span data-stu-id="a1246-193">False</span></span>                           |
| <span data-ttu-id="a1246-194">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1246-194">In Global Catalog</span></span>      | <span data-ttu-id="a1246-195">True</span><span class="sxs-lookup"><span data-stu-id="a1246-195">True</span></span>                            |
| <span data-ttu-id="a1246-196">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1246-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1246-197">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1246-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a1246-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1246-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a1246-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1246-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a1246-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1246-200">Search-Flags</span></span>           | <span data-ttu-id="a1246-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1246-201">0x00000000</span></span>                      |
| <span data-ttu-id="a1246-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1246-202">System-Flags</span></span>           | <span data-ttu-id="a1246-203">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a1246-203">0x00000013</span></span>                      |
| <span data-ttu-id="a1246-204">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1246-204">Classes used in</span></span>        | [<span data-ttu-id="a1246-205">**Início**</span><span class="sxs-lookup"><span data-stu-id="a1246-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a1246-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a1246-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a1246-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1246-207">Entry</span></span> | <span data-ttu-id="a1246-208">Valor</span><span class="sxs-lookup"><span data-stu-id="a1246-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a1246-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1246-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a1246-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1246-210">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a1246-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1246-211">System-Only</span></span>            | <span data-ttu-id="a1246-212">True</span><span class="sxs-lookup"><span data-stu-id="a1246-212">True</span></span>                            |
| <span data-ttu-id="a1246-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1246-213">Is-Single-Valued</span></span>       | <span data-ttu-id="a1246-214">True</span><span class="sxs-lookup"><span data-stu-id="a1246-214">True</span></span>                            |
| <span data-ttu-id="a1246-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1246-215">Is Indexed</span></span>             | <span data-ttu-id="a1246-216">Falso</span><span class="sxs-lookup"><span data-stu-id="a1246-216">False</span></span>                           |
| <span data-ttu-id="a1246-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1246-217">In Global Catalog</span></span>      | <span data-ttu-id="a1246-218">True</span><span class="sxs-lookup"><span data-stu-id="a1246-218">True</span></span>                            |
| <span data-ttu-id="a1246-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1246-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1246-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1246-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a1246-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1246-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a1246-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1246-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a1246-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1246-223">Search-Flags</span></span>           | <span data-ttu-id="a1246-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1246-224">0x00000000</span></span>                      |
| <span data-ttu-id="a1246-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1246-225">System-Flags</span></span>           | <span data-ttu-id="a1246-226">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a1246-226">0x00000013</span></span>                      |
| <span data-ttu-id="a1246-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1246-227">Classes used in</span></span>        | [<span data-ttu-id="a1246-228">**Início**</span><span class="sxs-lookup"><span data-stu-id="a1246-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a1246-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1246-229">Windows Server 2008</span></span>



| <span data-ttu-id="a1246-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1246-230">Entry</span></span> | <span data-ttu-id="a1246-231">Valor</span><span class="sxs-lookup"><span data-stu-id="a1246-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a1246-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1246-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a1246-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1246-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a1246-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1246-234">System-Only</span></span>            | <span data-ttu-id="a1246-235">True</span><span class="sxs-lookup"><span data-stu-id="a1246-235">True</span></span>                            |
| <span data-ttu-id="a1246-236">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1246-236">Is-Single-Valued</span></span>       | <span data-ttu-id="a1246-237">True</span><span class="sxs-lookup"><span data-stu-id="a1246-237">True</span></span>                            |
| <span data-ttu-id="a1246-238">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1246-238">Is Indexed</span></span>             | <span data-ttu-id="a1246-239">Falso</span><span class="sxs-lookup"><span data-stu-id="a1246-239">False</span></span>                           |
| <span data-ttu-id="a1246-240">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1246-240">In Global Catalog</span></span>      | <span data-ttu-id="a1246-241">True</span><span class="sxs-lookup"><span data-stu-id="a1246-241">True</span></span>                            |
| <span data-ttu-id="a1246-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1246-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1246-243">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1246-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a1246-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1246-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a1246-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1246-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a1246-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1246-246">Search-Flags</span></span>           | <span data-ttu-id="a1246-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1246-247">0x00000000</span></span>                      |
| <span data-ttu-id="a1246-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1246-248">System-Flags</span></span>           | <span data-ttu-id="a1246-249">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a1246-249">0x00000013</span></span>                      |
| <span data-ttu-id="a1246-250">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1246-250">Classes used in</span></span>        | [<span data-ttu-id="a1246-251">**Início**</span><span class="sxs-lookup"><span data-stu-id="a1246-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a1246-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a1246-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a1246-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1246-253">Entry</span></span> | <span data-ttu-id="a1246-254">Valor</span><span class="sxs-lookup"><span data-stu-id="a1246-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a1246-255">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1246-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a1246-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1246-256">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a1246-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1246-257">System-Only</span></span>            | <span data-ttu-id="a1246-258">True</span><span class="sxs-lookup"><span data-stu-id="a1246-258">True</span></span>                            |
| <span data-ttu-id="a1246-259">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1246-259">Is-Single-Valued</span></span>       | <span data-ttu-id="a1246-260">True</span><span class="sxs-lookup"><span data-stu-id="a1246-260">True</span></span>                            |
| <span data-ttu-id="a1246-261">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1246-261">Is Indexed</span></span>             | <span data-ttu-id="a1246-262">Falso</span><span class="sxs-lookup"><span data-stu-id="a1246-262">False</span></span>                           |
| <span data-ttu-id="a1246-263">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1246-263">In Global Catalog</span></span>      | <span data-ttu-id="a1246-264">True</span><span class="sxs-lookup"><span data-stu-id="a1246-264">True</span></span>                            |
| <span data-ttu-id="a1246-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1246-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1246-266">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1246-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a1246-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1246-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a1246-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1246-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a1246-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1246-269">Search-Flags</span></span>           | <span data-ttu-id="a1246-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1246-270">0x00000000</span></span>                      |
| <span data-ttu-id="a1246-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1246-271">System-Flags</span></span>           | <span data-ttu-id="a1246-272">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a1246-272">0x00000013</span></span>                      |
| <span data-ttu-id="a1246-273">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1246-273">Classes used in</span></span>        | [<span data-ttu-id="a1246-274">**Início**</span><span class="sxs-lookup"><span data-stu-id="a1246-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a1246-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a1246-275">Windows Server 2012</span></span>



| <span data-ttu-id="a1246-276">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1246-276">Entry</span></span> | <span data-ttu-id="a1246-277">Valor</span><span class="sxs-lookup"><span data-stu-id="a1246-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a1246-278">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1246-278">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a1246-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1246-279">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a1246-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1246-280">System-Only</span></span>            | <span data-ttu-id="a1246-281">True</span><span class="sxs-lookup"><span data-stu-id="a1246-281">True</span></span>                            |
| <span data-ttu-id="a1246-282">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1246-282">Is-Single-Valued</span></span>       | <span data-ttu-id="a1246-283">True</span><span class="sxs-lookup"><span data-stu-id="a1246-283">True</span></span>                            |
| <span data-ttu-id="a1246-284">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1246-284">Is Indexed</span></span>             | <span data-ttu-id="a1246-285">Falso</span><span class="sxs-lookup"><span data-stu-id="a1246-285">False</span></span>                           |
| <span data-ttu-id="a1246-286">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1246-286">In Global Catalog</span></span>      | <span data-ttu-id="a1246-287">True</span><span class="sxs-lookup"><span data-stu-id="a1246-287">True</span></span>                            |
| <span data-ttu-id="a1246-288">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1246-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1246-289">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1246-289">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a1246-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1246-290">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a1246-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1246-291">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a1246-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1246-292">Search-Flags</span></span>           | <span data-ttu-id="a1246-293">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1246-293">0x00000000</span></span>                      |
| <span data-ttu-id="a1246-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1246-294">System-Flags</span></span>           | <span data-ttu-id="a1246-295">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a1246-295">0x00000013</span></span>                      |
| <span data-ttu-id="a1246-296">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1246-296">Classes used in</span></span>        | [<span data-ttu-id="a1246-297">**Início**</span><span class="sxs-lookup"><span data-stu-id="a1246-297">**Top**</span></span>](c-top.md)<br/> |



 

 





