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
# <a name="repl-property-meta-data-attribute"></a><span data-ttu-id="a3e88-107">Atributo repl-Property-meta-data</span><span class="sxs-lookup"><span data-stu-id="a3e88-107">Repl-Property-Meta-Data attribute</span></span>

<span data-ttu-id="a3e88-108">Rastreia informações de estado de replicação interna para objetos DS.</span><span class="sxs-lookup"><span data-stu-id="a3e88-108">Tracks internal replication state information for DS objects.</span></span> <span data-ttu-id="a3e88-109">As informações aqui podem ser extraídas em formato público por meio da API pública DsReplicaGetInfo ().</span><span class="sxs-lookup"><span data-stu-id="a3e88-109">Information here can be extracted in public form through the public API DsReplicaGetInfo().</span></span> <span data-ttu-id="a3e88-110">Presente em todos os objetos DS.</span><span class="sxs-lookup"><span data-stu-id="a3e88-110">Present on all DS objects.</span></span>



| <span data-ttu-id="a3e88-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3e88-111">Entry</span></span> | <span data-ttu-id="a3e88-112">Valor</span><span class="sxs-lookup"><span data-stu-id="a3e88-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a3e88-113">CN</span><span class="sxs-lookup"><span data-stu-id="a3e88-113">CN</span></span>                | <span data-ttu-id="a3e88-114">Repl-Property-meta-data</span><span class="sxs-lookup"><span data-stu-id="a3e88-114">Repl-Property-Meta-Data</span></span>                                                      |
| <span data-ttu-id="a3e88-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a3e88-115">Ldap-Display-Name</span></span> | <span data-ttu-id="a3e88-116">replPropertyMetaData</span><span class="sxs-lookup"><span data-stu-id="a3e88-116">replPropertyMetaData</span></span>                                                         |
| <span data-ttu-id="a3e88-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a3e88-117">Size</span></span>              | <span data-ttu-id="a3e88-118">Comprimento é proporcional ao número de atributos replicáveis no objeto.</span><span class="sxs-lookup"><span data-stu-id="a3e88-118">Length is proportional to the number of replicable attributes on the object.</span></span> |
| <span data-ttu-id="a3e88-119">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a3e88-119">Update Privilege</span></span>  | <span data-ttu-id="a3e88-120">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="a3e88-120">This value is set by the system.</span></span>                                             |
| <span data-ttu-id="a3e88-121">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a3e88-121">Update Frequency</span></span>  | <span data-ttu-id="a3e88-122">Alterações em resposta a qualquer alteração de replicação no objeto.</span><span class="sxs-lookup"><span data-stu-id="a3e88-122">Changes in response to any replicating changes in the object.</span></span>                |
| <span data-ttu-id="a3e88-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a3e88-123">Attribute-Id</span></span>      | <span data-ttu-id="a3e88-124">1.2.840.113556.1.4.3</span><span class="sxs-lookup"><span data-stu-id="a3e88-124">1.2.840.113556.1.4.3</span></span>                                                         |
| <span data-ttu-id="a3e88-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a3e88-125">System-Id-Guid</span></span>    | <span data-ttu-id="a3e88-126">281416c0-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a3e88-126">281416c0-1968-11d0-a28f-00aa003049e2</span></span>                                         |
| <span data-ttu-id="a3e88-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3e88-127">Syntax</span></span>            | [<span data-ttu-id="a3e88-128">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="a3e88-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                        |



## <a name="implementations"></a><span data-ttu-id="a3e88-129">Implementações</span><span class="sxs-lookup"><span data-stu-id="a3e88-129">Implementations</span></span>

-   [<span data-ttu-id="a3e88-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a3e88-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a3e88-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a3e88-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a3e88-132">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a3e88-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a3e88-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a3e88-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a3e88-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a3e88-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a3e88-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a3e88-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a3e88-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a3e88-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a3e88-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a3e88-137">Windows 2000 Server</span></span>



| <span data-ttu-id="a3e88-138">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3e88-138">Entry</span></span> | <span data-ttu-id="a3e88-139">Valor</span><span class="sxs-lookup"><span data-stu-id="a3e88-139">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a3e88-140">ID do link</span><span class="sxs-lookup"><span data-stu-id="a3e88-140">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a3e88-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3e88-141">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a3e88-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3e88-142">System-Only</span></span>            | <span data-ttu-id="a3e88-143">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-143">True</span></span>                            |
| <span data-ttu-id="a3e88-144">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a3e88-144">Is-Single-Valued</span></span>       | <span data-ttu-id="a3e88-145">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-145">True</span></span>                            |
| <span data-ttu-id="a3e88-146">É indexado</span><span class="sxs-lookup"><span data-stu-id="a3e88-146">Is Indexed</span></span>             | <span data-ttu-id="a3e88-147">Falso</span><span class="sxs-lookup"><span data-stu-id="a3e88-147">False</span></span>                           |
| <span data-ttu-id="a3e88-148">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3e88-148">In Global Catalog</span></span>      | <span data-ttu-id="a3e88-149">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-149">True</span></span>                            |
| <span data-ttu-id="a3e88-150">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a3e88-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3e88-151">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a3e88-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a3e88-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3e88-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a3e88-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3e88-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a3e88-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3e88-154">Search-Flags</span></span>           | <span data-ttu-id="a3e88-155">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a3e88-155">0x00000008</span></span>                      |
| <span data-ttu-id="a3e88-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3e88-156">System-Flags</span></span>           | <span data-ttu-id="a3e88-157">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a3e88-157">0x00000013</span></span>                      |
| <span data-ttu-id="a3e88-158">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a3e88-158">Classes used in</span></span>        | [<span data-ttu-id="a3e88-159">**Início**</span><span class="sxs-lookup"><span data-stu-id="a3e88-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a3e88-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3e88-160">Windows Server 2003</span></span>



| <span data-ttu-id="a3e88-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3e88-161">Entry</span></span> | <span data-ttu-id="a3e88-162">Valor</span><span class="sxs-lookup"><span data-stu-id="a3e88-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a3e88-163">ID do link</span><span class="sxs-lookup"><span data-stu-id="a3e88-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a3e88-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3e88-164">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a3e88-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3e88-165">System-Only</span></span>            | <span data-ttu-id="a3e88-166">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-166">True</span></span>                            |
| <span data-ttu-id="a3e88-167">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a3e88-167">Is-Single-Valued</span></span>       | <span data-ttu-id="a3e88-168">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-168">True</span></span>                            |
| <span data-ttu-id="a3e88-169">É indexado</span><span class="sxs-lookup"><span data-stu-id="a3e88-169">Is Indexed</span></span>             | <span data-ttu-id="a3e88-170">Falso</span><span class="sxs-lookup"><span data-stu-id="a3e88-170">False</span></span>                           |
| <span data-ttu-id="a3e88-171">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3e88-171">In Global Catalog</span></span>      | <span data-ttu-id="a3e88-172">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-172">True</span></span>                            |
| <span data-ttu-id="a3e88-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a3e88-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3e88-174">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a3e88-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a3e88-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3e88-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a3e88-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3e88-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a3e88-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3e88-177">Search-Flags</span></span>           | <span data-ttu-id="a3e88-178">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a3e88-178">0x00000008</span></span>                      |
| <span data-ttu-id="a3e88-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3e88-179">System-Flags</span></span>           | <span data-ttu-id="a3e88-180">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="a3e88-180">0x0000001B</span></span>                      |
| <span data-ttu-id="a3e88-181">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a3e88-181">Classes used in</span></span>        | [<span data-ttu-id="a3e88-182">**Início**</span><span class="sxs-lookup"><span data-stu-id="a3e88-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a3e88-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="a3e88-183">ADAM</span></span>



| <span data-ttu-id="a3e88-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3e88-184">Entry</span></span> | <span data-ttu-id="a3e88-185">Valor</span><span class="sxs-lookup"><span data-stu-id="a3e88-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a3e88-186">ID do link</span><span class="sxs-lookup"><span data-stu-id="a3e88-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a3e88-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3e88-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a3e88-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3e88-188">System-Only</span></span>            | <span data-ttu-id="a3e88-189">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-189">True</span></span>                            |
| <span data-ttu-id="a3e88-190">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a3e88-190">Is-Single-Valued</span></span>       | <span data-ttu-id="a3e88-191">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-191">True</span></span>                            |
| <span data-ttu-id="a3e88-192">É indexado</span><span class="sxs-lookup"><span data-stu-id="a3e88-192">Is Indexed</span></span>             | <span data-ttu-id="a3e88-193">Falso</span><span class="sxs-lookup"><span data-stu-id="a3e88-193">False</span></span>                           |
| <span data-ttu-id="a3e88-194">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3e88-194">In Global Catalog</span></span>      | <span data-ttu-id="a3e88-195">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-195">True</span></span>                            |
| <span data-ttu-id="a3e88-196">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a3e88-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3e88-197">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a3e88-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a3e88-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3e88-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a3e88-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3e88-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a3e88-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3e88-200">Search-Flags</span></span>           | <span data-ttu-id="a3e88-201">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a3e88-201">0x00000008</span></span>                      |
| <span data-ttu-id="a3e88-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3e88-202">System-Flags</span></span>           | <span data-ttu-id="a3e88-203">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="a3e88-203">0x0000001B</span></span>                      |
| <span data-ttu-id="a3e88-204">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a3e88-204">Classes used in</span></span>        | [<span data-ttu-id="a3e88-205">**Início**</span><span class="sxs-lookup"><span data-stu-id="a3e88-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a3e88-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a3e88-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a3e88-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3e88-207">Entry</span></span> | <span data-ttu-id="a3e88-208">Valor</span><span class="sxs-lookup"><span data-stu-id="a3e88-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a3e88-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="a3e88-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a3e88-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3e88-210">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a3e88-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3e88-211">System-Only</span></span>            | <span data-ttu-id="a3e88-212">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-212">True</span></span>                            |
| <span data-ttu-id="a3e88-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a3e88-213">Is-Single-Valued</span></span>       | <span data-ttu-id="a3e88-214">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-214">True</span></span>                            |
| <span data-ttu-id="a3e88-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="a3e88-215">Is Indexed</span></span>             | <span data-ttu-id="a3e88-216">Falso</span><span class="sxs-lookup"><span data-stu-id="a3e88-216">False</span></span>                           |
| <span data-ttu-id="a3e88-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3e88-217">In Global Catalog</span></span>      | <span data-ttu-id="a3e88-218">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-218">True</span></span>                            |
| <span data-ttu-id="a3e88-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a3e88-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3e88-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a3e88-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a3e88-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3e88-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a3e88-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3e88-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a3e88-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3e88-223">Search-Flags</span></span>           | <span data-ttu-id="a3e88-224">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a3e88-224">0x00000008</span></span>                      |
| <span data-ttu-id="a3e88-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3e88-225">System-Flags</span></span>           | <span data-ttu-id="a3e88-226">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="a3e88-226">0x0000001B</span></span>                      |
| <span data-ttu-id="a3e88-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a3e88-227">Classes used in</span></span>        | [<span data-ttu-id="a3e88-228">**Início**</span><span class="sxs-lookup"><span data-stu-id="a3e88-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a3e88-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3e88-229">Windows Server 2008</span></span>



| <span data-ttu-id="a3e88-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3e88-230">Entry</span></span> | <span data-ttu-id="a3e88-231">Valor</span><span class="sxs-lookup"><span data-stu-id="a3e88-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a3e88-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="a3e88-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a3e88-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3e88-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a3e88-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3e88-234">System-Only</span></span>            | <span data-ttu-id="a3e88-235">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-235">True</span></span>                            |
| <span data-ttu-id="a3e88-236">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a3e88-236">Is-Single-Valued</span></span>       | <span data-ttu-id="a3e88-237">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-237">True</span></span>                            |
| <span data-ttu-id="a3e88-238">É indexado</span><span class="sxs-lookup"><span data-stu-id="a3e88-238">Is Indexed</span></span>             | <span data-ttu-id="a3e88-239">Falso</span><span class="sxs-lookup"><span data-stu-id="a3e88-239">False</span></span>                           |
| <span data-ttu-id="a3e88-240">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3e88-240">In Global Catalog</span></span>      | <span data-ttu-id="a3e88-241">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-241">True</span></span>                            |
| <span data-ttu-id="a3e88-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a3e88-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3e88-243">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a3e88-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a3e88-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3e88-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a3e88-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3e88-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a3e88-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3e88-246">Search-Flags</span></span>           | <span data-ttu-id="a3e88-247">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a3e88-247">0x00000008</span></span>                      |
| <span data-ttu-id="a3e88-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3e88-248">System-Flags</span></span>           | <span data-ttu-id="a3e88-249">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="a3e88-249">0x0000001B</span></span>                      |
| <span data-ttu-id="a3e88-250">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a3e88-250">Classes used in</span></span>        | [<span data-ttu-id="a3e88-251">**Início**</span><span class="sxs-lookup"><span data-stu-id="a3e88-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a3e88-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a3e88-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a3e88-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3e88-253">Entry</span></span> | <span data-ttu-id="a3e88-254">Valor</span><span class="sxs-lookup"><span data-stu-id="a3e88-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a3e88-255">ID do link</span><span class="sxs-lookup"><span data-stu-id="a3e88-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a3e88-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3e88-256">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a3e88-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3e88-257">System-Only</span></span>            | <span data-ttu-id="a3e88-258">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-258">True</span></span>                            |
| <span data-ttu-id="a3e88-259">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a3e88-259">Is-Single-Valued</span></span>       | <span data-ttu-id="a3e88-260">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-260">True</span></span>                            |
| <span data-ttu-id="a3e88-261">É indexado</span><span class="sxs-lookup"><span data-stu-id="a3e88-261">Is Indexed</span></span>             | <span data-ttu-id="a3e88-262">Falso</span><span class="sxs-lookup"><span data-stu-id="a3e88-262">False</span></span>                           |
| <span data-ttu-id="a3e88-263">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3e88-263">In Global Catalog</span></span>      | <span data-ttu-id="a3e88-264">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-264">True</span></span>                            |
| <span data-ttu-id="a3e88-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a3e88-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3e88-266">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a3e88-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a3e88-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3e88-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a3e88-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3e88-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a3e88-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3e88-269">Search-Flags</span></span>           | <span data-ttu-id="a3e88-270">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a3e88-270">0x00000008</span></span>                      |
| <span data-ttu-id="a3e88-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3e88-271">System-Flags</span></span>           | <span data-ttu-id="a3e88-272">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="a3e88-272">0x0000001B</span></span>                      |
| <span data-ttu-id="a3e88-273">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a3e88-273">Classes used in</span></span>        | [<span data-ttu-id="a3e88-274">**Início**</span><span class="sxs-lookup"><span data-stu-id="a3e88-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a3e88-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3e88-275">Windows Server 2012</span></span>



| <span data-ttu-id="a3e88-276">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3e88-276">Entry</span></span> | <span data-ttu-id="a3e88-277">Valor</span><span class="sxs-lookup"><span data-stu-id="a3e88-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a3e88-278">ID do link</span><span class="sxs-lookup"><span data-stu-id="a3e88-278">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a3e88-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3e88-279">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a3e88-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3e88-280">System-Only</span></span>            | <span data-ttu-id="a3e88-281">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-281">True</span></span>                            |
| <span data-ttu-id="a3e88-282">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a3e88-282">Is-Single-Valued</span></span>       | <span data-ttu-id="a3e88-283">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-283">True</span></span>                            |
| <span data-ttu-id="a3e88-284">É indexado</span><span class="sxs-lookup"><span data-stu-id="a3e88-284">Is Indexed</span></span>             | <span data-ttu-id="a3e88-285">Falso</span><span class="sxs-lookup"><span data-stu-id="a3e88-285">False</span></span>                           |
| <span data-ttu-id="a3e88-286">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3e88-286">In Global Catalog</span></span>      | <span data-ttu-id="a3e88-287">True</span><span class="sxs-lookup"><span data-stu-id="a3e88-287">True</span></span>                            |
| <span data-ttu-id="a3e88-288">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a3e88-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3e88-289">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a3e88-289">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a3e88-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3e88-290">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a3e88-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3e88-291">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a3e88-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3e88-292">Search-Flags</span></span>           | <span data-ttu-id="a3e88-293">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a3e88-293">0x00000008</span></span>                      |
| <span data-ttu-id="a3e88-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3e88-294">System-Flags</span></span>           | <span data-ttu-id="a3e88-295">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="a3e88-295">0x0000001B</span></span>                      |
| <span data-ttu-id="a3e88-296">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a3e88-296">Classes used in</span></span>        | [<span data-ttu-id="a3e88-297">**Início**</span><span class="sxs-lookup"><span data-stu-id="a3e88-297">**Top**</span></span>](c-top.md)<br/> |



 

 





