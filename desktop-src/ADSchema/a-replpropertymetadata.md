---
title: Atributo repl-Property-meta-data
description: Rastreia informações de estado de replicação interna para objetos DS. As informações aqui podem ser extraídas em formato público por meio da API pública DsReplicaGetInfo (). Presente em todos os objetos DS.
ms.assetid: 5776208c-8138-4b0a-855a-8bddcbd2e532
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo repl-Property-meta-data
- Esquema de AD do atributo replPropertyMetaData
topic_type:
- apiref
api_name:
- Repl-Property-Meta-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7639d9bca600457d519862e1f57d9ee698d2a155
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645501"
---
# <a name="repl-property-meta-data-attribute"></a><span data-ttu-id="47c65-107">Atributo repl-Property-meta-data</span><span class="sxs-lookup"><span data-stu-id="47c65-107">Repl-Property-Meta-Data attribute</span></span>

<span data-ttu-id="47c65-108">Rastreia informações de estado de replicação interna para objetos DS.</span><span class="sxs-lookup"><span data-stu-id="47c65-108">Tracks internal replication state information for DS objects.</span></span> <span data-ttu-id="47c65-109">As informações aqui podem ser extraídas em formato público por meio da API pública DsReplicaGetInfo ().</span><span class="sxs-lookup"><span data-stu-id="47c65-109">Information here can be extracted in public form through the public API DsReplicaGetInfo().</span></span> <span data-ttu-id="47c65-110">Presente em todos os objetos DS.</span><span class="sxs-lookup"><span data-stu-id="47c65-110">Present on all DS objects.</span></span>



| <span data-ttu-id="47c65-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="47c65-111">Entry</span></span> | <span data-ttu-id="47c65-112">Valor</span><span class="sxs-lookup"><span data-stu-id="47c65-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="47c65-113">CN</span><span class="sxs-lookup"><span data-stu-id="47c65-113">CN</span></span>                | <span data-ttu-id="47c65-114">Repl-Property-meta-data</span><span class="sxs-lookup"><span data-stu-id="47c65-114">Repl-Property-Meta-Data</span></span>                                                      |
| <span data-ttu-id="47c65-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="47c65-115">Ldap-Display-Name</span></span> | <span data-ttu-id="47c65-116">replPropertyMetaData</span><span class="sxs-lookup"><span data-stu-id="47c65-116">replPropertyMetaData</span></span>                                                         |
| <span data-ttu-id="47c65-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="47c65-117">Size</span></span>              | <span data-ttu-id="47c65-118">Comprimento é proporcional ao número de atributos replicáveis no objeto.</span><span class="sxs-lookup"><span data-stu-id="47c65-118">Length is proportional to the number of replicable attributes on the object.</span></span> |
| <span data-ttu-id="47c65-119">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="47c65-119">Update Privilege</span></span>  | <span data-ttu-id="47c65-120">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="47c65-120">This value is set by the system.</span></span>                                             |
| <span data-ttu-id="47c65-121">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="47c65-121">Update Frequency</span></span>  | <span data-ttu-id="47c65-122">Alterações em resposta a qualquer alteração de replicação no objeto.</span><span class="sxs-lookup"><span data-stu-id="47c65-122">Changes in response to any replicating changes in the object.</span></span>                |
| <span data-ttu-id="47c65-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="47c65-123">Attribute-Id</span></span>      | <span data-ttu-id="47c65-124">1.2.840.113556.1.4.3</span><span class="sxs-lookup"><span data-stu-id="47c65-124">1.2.840.113556.1.4.3</span></span>                                                         |
| <span data-ttu-id="47c65-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="47c65-125">System-Id-Guid</span></span>    | <span data-ttu-id="47c65-126">281416c0-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="47c65-126">281416c0-1968-11d0-a28f-00aa003049e2</span></span>                                         |
| <span data-ttu-id="47c65-127">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47c65-127">Syntax</span></span>            | [<span data-ttu-id="47c65-128">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="47c65-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                        |



## <a name="implementations"></a><span data-ttu-id="47c65-129">Implementações</span><span class="sxs-lookup"><span data-stu-id="47c65-129">Implementations</span></span>

-   [<span data-ttu-id="47c65-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="47c65-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="47c65-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="47c65-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="47c65-132">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="47c65-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="47c65-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="47c65-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="47c65-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="47c65-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="47c65-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="47c65-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="47c65-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="47c65-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="47c65-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="47c65-137">Windows 2000 Server</span></span>



| <span data-ttu-id="47c65-138">Entrada</span><span class="sxs-lookup"><span data-stu-id="47c65-138">Entry</span></span> | <span data-ttu-id="47c65-139">Valor</span><span class="sxs-lookup"><span data-stu-id="47c65-139">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47c65-140">ID do link</span><span class="sxs-lookup"><span data-stu-id="47c65-140">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47c65-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47c65-141">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47c65-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="47c65-142">System-Only</span></span>            | <span data-ttu-id="47c65-143">True</span><span class="sxs-lookup"><span data-stu-id="47c65-143">True</span></span>                            |
| <span data-ttu-id="47c65-144">É de valor único</span><span class="sxs-lookup"><span data-stu-id="47c65-144">Is-Single-Valued</span></span>       | <span data-ttu-id="47c65-145">True</span><span class="sxs-lookup"><span data-stu-id="47c65-145">True</span></span>                            |
| <span data-ttu-id="47c65-146">É indexado</span><span class="sxs-lookup"><span data-stu-id="47c65-146">Is Indexed</span></span>             | <span data-ttu-id="47c65-147">Falso</span><span class="sxs-lookup"><span data-stu-id="47c65-147">False</span></span>                           |
| <span data-ttu-id="47c65-148">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="47c65-148">In Global Catalog</span></span>      | <span data-ttu-id="47c65-149">True</span><span class="sxs-lookup"><span data-stu-id="47c65-149">True</span></span>                            |
| <span data-ttu-id="47c65-150">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47c65-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="47c65-151">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="47c65-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47c65-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47c65-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47c65-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47c65-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47c65-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47c65-154">Search-Flags</span></span>           | <span data-ttu-id="47c65-155">0x00000008</span><span class="sxs-lookup"><span data-stu-id="47c65-155">0x00000008</span></span>                      |
| <span data-ttu-id="47c65-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47c65-156">System-Flags</span></span>           | <span data-ttu-id="47c65-157">0x00000013</span><span class="sxs-lookup"><span data-stu-id="47c65-157">0x00000013</span></span>                      |
| <span data-ttu-id="47c65-158">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="47c65-158">Classes used in</span></span>        | [<span data-ttu-id="47c65-159">**Início**</span><span class="sxs-lookup"><span data-stu-id="47c65-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="47c65-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="47c65-160">Windows Server 2003</span></span>



| <span data-ttu-id="47c65-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="47c65-161">Entry</span></span> | <span data-ttu-id="47c65-162">Valor</span><span class="sxs-lookup"><span data-stu-id="47c65-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47c65-163">ID do link</span><span class="sxs-lookup"><span data-stu-id="47c65-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47c65-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47c65-164">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47c65-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="47c65-165">System-Only</span></span>            | <span data-ttu-id="47c65-166">True</span><span class="sxs-lookup"><span data-stu-id="47c65-166">True</span></span>                            |
| <span data-ttu-id="47c65-167">É de valor único</span><span class="sxs-lookup"><span data-stu-id="47c65-167">Is-Single-Valued</span></span>       | <span data-ttu-id="47c65-168">True</span><span class="sxs-lookup"><span data-stu-id="47c65-168">True</span></span>                            |
| <span data-ttu-id="47c65-169">É indexado</span><span class="sxs-lookup"><span data-stu-id="47c65-169">Is Indexed</span></span>             | <span data-ttu-id="47c65-170">Falso</span><span class="sxs-lookup"><span data-stu-id="47c65-170">False</span></span>                           |
| <span data-ttu-id="47c65-171">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="47c65-171">In Global Catalog</span></span>      | <span data-ttu-id="47c65-172">True</span><span class="sxs-lookup"><span data-stu-id="47c65-172">True</span></span>                            |
| <span data-ttu-id="47c65-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47c65-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="47c65-174">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="47c65-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47c65-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47c65-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47c65-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47c65-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47c65-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47c65-177">Search-Flags</span></span>           | <span data-ttu-id="47c65-178">0x00000008</span><span class="sxs-lookup"><span data-stu-id="47c65-178">0x00000008</span></span>                      |
| <span data-ttu-id="47c65-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47c65-179">System-Flags</span></span>           | <span data-ttu-id="47c65-180">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="47c65-180">0x0000001B</span></span>                      |
| <span data-ttu-id="47c65-181">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="47c65-181">Classes used in</span></span>        | [<span data-ttu-id="47c65-182">**Início**</span><span class="sxs-lookup"><span data-stu-id="47c65-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="47c65-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="47c65-183">ADAM</span></span>



| <span data-ttu-id="47c65-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="47c65-184">Entry</span></span> | <span data-ttu-id="47c65-185">Valor</span><span class="sxs-lookup"><span data-stu-id="47c65-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47c65-186">ID do link</span><span class="sxs-lookup"><span data-stu-id="47c65-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47c65-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47c65-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47c65-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="47c65-188">System-Only</span></span>            | <span data-ttu-id="47c65-189">True</span><span class="sxs-lookup"><span data-stu-id="47c65-189">True</span></span>                            |
| <span data-ttu-id="47c65-190">É de valor único</span><span class="sxs-lookup"><span data-stu-id="47c65-190">Is-Single-Valued</span></span>       | <span data-ttu-id="47c65-191">True</span><span class="sxs-lookup"><span data-stu-id="47c65-191">True</span></span>                            |
| <span data-ttu-id="47c65-192">É indexado</span><span class="sxs-lookup"><span data-stu-id="47c65-192">Is Indexed</span></span>             | <span data-ttu-id="47c65-193">Falso</span><span class="sxs-lookup"><span data-stu-id="47c65-193">False</span></span>                           |
| <span data-ttu-id="47c65-194">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="47c65-194">In Global Catalog</span></span>      | <span data-ttu-id="47c65-195">True</span><span class="sxs-lookup"><span data-stu-id="47c65-195">True</span></span>                            |
| <span data-ttu-id="47c65-196">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47c65-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="47c65-197">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="47c65-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47c65-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47c65-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47c65-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47c65-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47c65-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47c65-200">Search-Flags</span></span>           | <span data-ttu-id="47c65-201">0x00000008</span><span class="sxs-lookup"><span data-stu-id="47c65-201">0x00000008</span></span>                      |
| <span data-ttu-id="47c65-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47c65-202">System-Flags</span></span>           | <span data-ttu-id="47c65-203">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="47c65-203">0x0000001B</span></span>                      |
| <span data-ttu-id="47c65-204">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="47c65-204">Classes used in</span></span>        | [<span data-ttu-id="47c65-205">**Início**</span><span class="sxs-lookup"><span data-stu-id="47c65-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="47c65-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="47c65-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="47c65-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="47c65-207">Entry</span></span> | <span data-ttu-id="47c65-208">Valor</span><span class="sxs-lookup"><span data-stu-id="47c65-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47c65-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="47c65-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47c65-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47c65-210">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47c65-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="47c65-211">System-Only</span></span>            | <span data-ttu-id="47c65-212">True</span><span class="sxs-lookup"><span data-stu-id="47c65-212">True</span></span>                            |
| <span data-ttu-id="47c65-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="47c65-213">Is-Single-Valued</span></span>       | <span data-ttu-id="47c65-214">True</span><span class="sxs-lookup"><span data-stu-id="47c65-214">True</span></span>                            |
| <span data-ttu-id="47c65-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="47c65-215">Is Indexed</span></span>             | <span data-ttu-id="47c65-216">Falso</span><span class="sxs-lookup"><span data-stu-id="47c65-216">False</span></span>                           |
| <span data-ttu-id="47c65-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="47c65-217">In Global Catalog</span></span>      | <span data-ttu-id="47c65-218">True</span><span class="sxs-lookup"><span data-stu-id="47c65-218">True</span></span>                            |
| <span data-ttu-id="47c65-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47c65-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="47c65-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="47c65-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47c65-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47c65-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47c65-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47c65-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47c65-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47c65-223">Search-Flags</span></span>           | <span data-ttu-id="47c65-224">0x00000008</span><span class="sxs-lookup"><span data-stu-id="47c65-224">0x00000008</span></span>                      |
| <span data-ttu-id="47c65-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47c65-225">System-Flags</span></span>           | <span data-ttu-id="47c65-226">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="47c65-226">0x0000001B</span></span>                      |
| <span data-ttu-id="47c65-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="47c65-227">Classes used in</span></span>        | [<span data-ttu-id="47c65-228">**Início**</span><span class="sxs-lookup"><span data-stu-id="47c65-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="47c65-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47c65-229">Windows Server 2008</span></span>



| <span data-ttu-id="47c65-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="47c65-230">Entry</span></span> | <span data-ttu-id="47c65-231">Valor</span><span class="sxs-lookup"><span data-stu-id="47c65-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47c65-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="47c65-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47c65-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47c65-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47c65-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="47c65-234">System-Only</span></span>            | <span data-ttu-id="47c65-235">True</span><span class="sxs-lookup"><span data-stu-id="47c65-235">True</span></span>                            |
| <span data-ttu-id="47c65-236">É de valor único</span><span class="sxs-lookup"><span data-stu-id="47c65-236">Is-Single-Valued</span></span>       | <span data-ttu-id="47c65-237">True</span><span class="sxs-lookup"><span data-stu-id="47c65-237">True</span></span>                            |
| <span data-ttu-id="47c65-238">É indexado</span><span class="sxs-lookup"><span data-stu-id="47c65-238">Is Indexed</span></span>             | <span data-ttu-id="47c65-239">Falso</span><span class="sxs-lookup"><span data-stu-id="47c65-239">False</span></span>                           |
| <span data-ttu-id="47c65-240">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="47c65-240">In Global Catalog</span></span>      | <span data-ttu-id="47c65-241">True</span><span class="sxs-lookup"><span data-stu-id="47c65-241">True</span></span>                            |
| <span data-ttu-id="47c65-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47c65-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="47c65-243">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="47c65-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47c65-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47c65-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47c65-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47c65-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47c65-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47c65-246">Search-Flags</span></span>           | <span data-ttu-id="47c65-247">0x00000008</span><span class="sxs-lookup"><span data-stu-id="47c65-247">0x00000008</span></span>                      |
| <span data-ttu-id="47c65-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47c65-248">System-Flags</span></span>           | <span data-ttu-id="47c65-249">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="47c65-249">0x0000001B</span></span>                      |
| <span data-ttu-id="47c65-250">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="47c65-250">Classes used in</span></span>        | [<span data-ttu-id="47c65-251">**Início**</span><span class="sxs-lookup"><span data-stu-id="47c65-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="47c65-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="47c65-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="47c65-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="47c65-253">Entry</span></span> | <span data-ttu-id="47c65-254">Valor</span><span class="sxs-lookup"><span data-stu-id="47c65-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47c65-255">ID do link</span><span class="sxs-lookup"><span data-stu-id="47c65-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47c65-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47c65-256">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47c65-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="47c65-257">System-Only</span></span>            | <span data-ttu-id="47c65-258">True</span><span class="sxs-lookup"><span data-stu-id="47c65-258">True</span></span>                            |
| <span data-ttu-id="47c65-259">É de valor único</span><span class="sxs-lookup"><span data-stu-id="47c65-259">Is-Single-Valued</span></span>       | <span data-ttu-id="47c65-260">True</span><span class="sxs-lookup"><span data-stu-id="47c65-260">True</span></span>                            |
| <span data-ttu-id="47c65-261">É indexado</span><span class="sxs-lookup"><span data-stu-id="47c65-261">Is Indexed</span></span>             | <span data-ttu-id="47c65-262">Falso</span><span class="sxs-lookup"><span data-stu-id="47c65-262">False</span></span>                           |
| <span data-ttu-id="47c65-263">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="47c65-263">In Global Catalog</span></span>      | <span data-ttu-id="47c65-264">True</span><span class="sxs-lookup"><span data-stu-id="47c65-264">True</span></span>                            |
| <span data-ttu-id="47c65-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47c65-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="47c65-266">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="47c65-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47c65-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47c65-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47c65-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47c65-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47c65-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47c65-269">Search-Flags</span></span>           | <span data-ttu-id="47c65-270">0x00000008</span><span class="sxs-lookup"><span data-stu-id="47c65-270">0x00000008</span></span>                      |
| <span data-ttu-id="47c65-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47c65-271">System-Flags</span></span>           | <span data-ttu-id="47c65-272">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="47c65-272">0x0000001B</span></span>                      |
| <span data-ttu-id="47c65-273">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="47c65-273">Classes used in</span></span>        | [<span data-ttu-id="47c65-274">**Início**</span><span class="sxs-lookup"><span data-stu-id="47c65-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="47c65-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="47c65-275">Windows Server 2012</span></span>



| <span data-ttu-id="47c65-276">Entrada</span><span class="sxs-lookup"><span data-stu-id="47c65-276">Entry</span></span> | <span data-ttu-id="47c65-277">Valor</span><span class="sxs-lookup"><span data-stu-id="47c65-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47c65-278">ID do link</span><span class="sxs-lookup"><span data-stu-id="47c65-278">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47c65-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47c65-279">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47c65-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="47c65-280">System-Only</span></span>            | <span data-ttu-id="47c65-281">True</span><span class="sxs-lookup"><span data-stu-id="47c65-281">True</span></span>                            |
| <span data-ttu-id="47c65-282">É de valor único</span><span class="sxs-lookup"><span data-stu-id="47c65-282">Is-Single-Valued</span></span>       | <span data-ttu-id="47c65-283">True</span><span class="sxs-lookup"><span data-stu-id="47c65-283">True</span></span>                            |
| <span data-ttu-id="47c65-284">É indexado</span><span class="sxs-lookup"><span data-stu-id="47c65-284">Is Indexed</span></span>             | <span data-ttu-id="47c65-285">Falso</span><span class="sxs-lookup"><span data-stu-id="47c65-285">False</span></span>                           |
| <span data-ttu-id="47c65-286">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="47c65-286">In Global Catalog</span></span>      | <span data-ttu-id="47c65-287">True</span><span class="sxs-lookup"><span data-stu-id="47c65-287">True</span></span>                            |
| <span data-ttu-id="47c65-288">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="47c65-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="47c65-289">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="47c65-289">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47c65-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47c65-290">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47c65-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47c65-291">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47c65-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47c65-292">Search-Flags</span></span>           | <span data-ttu-id="47c65-293">0x00000008</span><span class="sxs-lookup"><span data-stu-id="47c65-293">0x00000008</span></span>                      |
| <span data-ttu-id="47c65-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47c65-294">System-Flags</span></span>           | <span data-ttu-id="47c65-295">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="47c65-295">0x0000001B</span></span>                      |
| <span data-ttu-id="47c65-296">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="47c65-296">Classes used in</span></span>        | [<span data-ttu-id="47c65-297">**Início**</span><span class="sxs-lookup"><span data-stu-id="47c65-297">**Top**</span></span>](c-top.md)<br/> |



 

 





