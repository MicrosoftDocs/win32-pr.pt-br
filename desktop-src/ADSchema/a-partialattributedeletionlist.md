---
title: Atributo parcial-atributo-exclusão-lista
description: Controla o estado de replicação interna de réplicas parciais (ou seja, em GCs). Atributo do objeto NC de réplica parcial. Usado quando o GC está no processo de remover atributos dos objetos em seus NCs de réplica parcial.
ms.assetid: 0084774b-7231-4cfc-8f60-c014006da2b9
ms.tgt_platform: multiple
keywords:
- Atributo do AD de atributos parcial-atributo-exclusão-lista
- Esquema de AD do atributo partialAttributeDeletionList
topic_type:
- apiref
api_name:
- Partial-Attribute-Deletion-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c2c6c0428d71dbba4199eeb441c838fb54a4463
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755216"
---
# <a name="partial-attribute-deletion-list-attribute"></a><span data-ttu-id="0346d-107">Atributo parcial-atributo-exclusão-lista</span><span class="sxs-lookup"><span data-stu-id="0346d-107">Partial-Attribute-Deletion-List attribute</span></span>

<span data-ttu-id="0346d-108">Controla o estado de replicação interna de réplicas parciais (ou seja, em GCs).</span><span class="sxs-lookup"><span data-stu-id="0346d-108">Tracks the internal replication state of partial replicas (that is, on GCs).</span></span> <span data-ttu-id="0346d-109">Atributo do objeto NC de réplica parcial.</span><span class="sxs-lookup"><span data-stu-id="0346d-109">Attribute of the partial replica NC object.</span></span> <span data-ttu-id="0346d-110">Usado quando o GC está no processo de remover atributos dos objetos em seus NCs de réplica parcial.</span><span class="sxs-lookup"><span data-stu-id="0346d-110">Used when the GC is in the process of removing attributes from the objects in its partial replica NCs.</span></span>



| <span data-ttu-id="0346d-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="0346d-111">Entry</span></span> | <span data-ttu-id="0346d-112">Valor</span><span class="sxs-lookup"><span data-stu-id="0346d-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="0346d-113">CN</span><span class="sxs-lookup"><span data-stu-id="0346d-113">CN</span></span>                | <span data-ttu-id="0346d-114">Parcial-atributo-exclusão-lista</span><span class="sxs-lookup"><span data-stu-id="0346d-114">Partial-Attribute-Deletion-List</span></span>                       |
| <span data-ttu-id="0346d-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0346d-115">Ldap-Display-Name</span></span> | <span data-ttu-id="0346d-116">partialAttributeDeletionList</span><span class="sxs-lookup"><span data-stu-id="0346d-116">partialAttributeDeletionList</span></span>                          |
| <span data-ttu-id="0346d-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="0346d-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="0346d-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="0346d-118">Update Privilege</span></span>  | <span data-ttu-id="0346d-119">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="0346d-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="0346d-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="0346d-120">Update Frequency</span></span>  | <span data-ttu-id="0346d-121">Durante a replicação</span><span class="sxs-lookup"><span data-stu-id="0346d-121">During replication</span></span>                                    |
| <span data-ttu-id="0346d-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0346d-122">Attribute-Id</span></span>      | <span data-ttu-id="0346d-123">1.2.840.113556.1.4.663</span><span class="sxs-lookup"><span data-stu-id="0346d-123">1.2.840.113556.1.4.663</span></span>                                |
| <span data-ttu-id="0346d-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0346d-124">System-Id-Guid</span></span>    | <span data-ttu-id="0346d-125">28630ec0-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="0346d-125">28630ec0-41d5-11d1-a9c1-0000f80367c1</span></span>                  |
| <span data-ttu-id="0346d-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="0346d-126">Syntax</span></span>            | [<span data-ttu-id="0346d-127">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="0346d-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="0346d-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="0346d-128">Implementations</span></span>

-   [<span data-ttu-id="0346d-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0346d-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0346d-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0346d-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0346d-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="0346d-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0346d-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0346d-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0346d-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0346d-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0346d-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0346d-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0346d-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0346d-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0346d-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0346d-136">Windows 2000 Server</span></span>



| <span data-ttu-id="0346d-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="0346d-137">Entry</span></span> | <span data-ttu-id="0346d-138">Valor</span><span class="sxs-lookup"><span data-stu-id="0346d-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0346d-139">ID do link</span><span class="sxs-lookup"><span data-stu-id="0346d-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0346d-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0346d-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0346d-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="0346d-141">System-Only</span></span>            | <span data-ttu-id="0346d-142">True</span><span class="sxs-lookup"><span data-stu-id="0346d-142">True</span></span>                            |
| <span data-ttu-id="0346d-143">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0346d-143">Is-Single-Valued</span></span>       | <span data-ttu-id="0346d-144">True</span><span class="sxs-lookup"><span data-stu-id="0346d-144">True</span></span>                            |
| <span data-ttu-id="0346d-145">É indexado</span><span class="sxs-lookup"><span data-stu-id="0346d-145">Is Indexed</span></span>             | <span data-ttu-id="0346d-146">Falso</span><span class="sxs-lookup"><span data-stu-id="0346d-146">False</span></span>                           |
| <span data-ttu-id="0346d-147">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0346d-147">In Global Catalog</span></span>      | <span data-ttu-id="0346d-148">True</span><span class="sxs-lookup"><span data-stu-id="0346d-148">True</span></span>                            |
| <span data-ttu-id="0346d-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0346d-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="0346d-150">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0346d-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0346d-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0346d-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0346d-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0346d-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0346d-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0346d-153">Search-Flags</span></span>           | <span data-ttu-id="0346d-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0346d-154">0x00000000</span></span>                      |
| <span data-ttu-id="0346d-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0346d-155">System-Flags</span></span>           | <span data-ttu-id="0346d-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0346d-156">0x00000013</span></span>                      |
| <span data-ttu-id="0346d-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0346d-157">Classes used in</span></span>        | [<span data-ttu-id="0346d-158">**Início**</span><span class="sxs-lookup"><span data-stu-id="0346d-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0346d-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0346d-159">Windows Server 2003</span></span>



| <span data-ttu-id="0346d-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="0346d-160">Entry</span></span> | <span data-ttu-id="0346d-161">Valor</span><span class="sxs-lookup"><span data-stu-id="0346d-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0346d-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="0346d-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0346d-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0346d-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0346d-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="0346d-164">System-Only</span></span>            | <span data-ttu-id="0346d-165">True</span><span class="sxs-lookup"><span data-stu-id="0346d-165">True</span></span>                            |
| <span data-ttu-id="0346d-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0346d-166">Is-Single-Valued</span></span>       | <span data-ttu-id="0346d-167">True</span><span class="sxs-lookup"><span data-stu-id="0346d-167">True</span></span>                            |
| <span data-ttu-id="0346d-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="0346d-168">Is Indexed</span></span>             | <span data-ttu-id="0346d-169">Falso</span><span class="sxs-lookup"><span data-stu-id="0346d-169">False</span></span>                           |
| <span data-ttu-id="0346d-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0346d-170">In Global Catalog</span></span>      | <span data-ttu-id="0346d-171">True</span><span class="sxs-lookup"><span data-stu-id="0346d-171">True</span></span>                            |
| <span data-ttu-id="0346d-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0346d-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="0346d-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0346d-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0346d-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0346d-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0346d-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0346d-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0346d-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0346d-176">Search-Flags</span></span>           | <span data-ttu-id="0346d-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0346d-177">0x00000000</span></span>                      |
| <span data-ttu-id="0346d-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0346d-178">System-Flags</span></span>           | <span data-ttu-id="0346d-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0346d-179">0x00000013</span></span>                      |
| <span data-ttu-id="0346d-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0346d-180">Classes used in</span></span>        | [<span data-ttu-id="0346d-181">**Início**</span><span class="sxs-lookup"><span data-stu-id="0346d-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0346d-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="0346d-182">ADAM</span></span>



| <span data-ttu-id="0346d-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="0346d-183">Entry</span></span> | <span data-ttu-id="0346d-184">Valor</span><span class="sxs-lookup"><span data-stu-id="0346d-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0346d-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="0346d-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0346d-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0346d-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0346d-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="0346d-187">System-Only</span></span>            | <span data-ttu-id="0346d-188">True</span><span class="sxs-lookup"><span data-stu-id="0346d-188">True</span></span>                            |
| <span data-ttu-id="0346d-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0346d-189">Is-Single-Valued</span></span>       | <span data-ttu-id="0346d-190">True</span><span class="sxs-lookup"><span data-stu-id="0346d-190">True</span></span>                            |
| <span data-ttu-id="0346d-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="0346d-191">Is Indexed</span></span>             | <span data-ttu-id="0346d-192">Falso</span><span class="sxs-lookup"><span data-stu-id="0346d-192">False</span></span>                           |
| <span data-ttu-id="0346d-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0346d-193">In Global Catalog</span></span>      | <span data-ttu-id="0346d-194">True</span><span class="sxs-lookup"><span data-stu-id="0346d-194">True</span></span>                            |
| <span data-ttu-id="0346d-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0346d-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="0346d-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0346d-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0346d-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0346d-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0346d-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0346d-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0346d-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0346d-199">Search-Flags</span></span>           | <span data-ttu-id="0346d-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0346d-200">0x00000000</span></span>                      |
| <span data-ttu-id="0346d-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0346d-201">System-Flags</span></span>           | <span data-ttu-id="0346d-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0346d-202">0x00000013</span></span>                      |
| <span data-ttu-id="0346d-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0346d-203">Classes used in</span></span>        | [<span data-ttu-id="0346d-204">**Início**</span><span class="sxs-lookup"><span data-stu-id="0346d-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0346d-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0346d-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0346d-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="0346d-206">Entry</span></span> | <span data-ttu-id="0346d-207">Valor</span><span class="sxs-lookup"><span data-stu-id="0346d-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0346d-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="0346d-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0346d-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0346d-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0346d-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="0346d-210">System-Only</span></span>            | <span data-ttu-id="0346d-211">True</span><span class="sxs-lookup"><span data-stu-id="0346d-211">True</span></span>                            |
| <span data-ttu-id="0346d-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0346d-212">Is-Single-Valued</span></span>       | <span data-ttu-id="0346d-213">True</span><span class="sxs-lookup"><span data-stu-id="0346d-213">True</span></span>                            |
| <span data-ttu-id="0346d-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="0346d-214">Is Indexed</span></span>             | <span data-ttu-id="0346d-215">Falso</span><span class="sxs-lookup"><span data-stu-id="0346d-215">False</span></span>                           |
| <span data-ttu-id="0346d-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0346d-216">In Global Catalog</span></span>      | <span data-ttu-id="0346d-217">True</span><span class="sxs-lookup"><span data-stu-id="0346d-217">True</span></span>                            |
| <span data-ttu-id="0346d-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0346d-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="0346d-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0346d-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0346d-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0346d-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0346d-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0346d-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0346d-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0346d-222">Search-Flags</span></span>           | <span data-ttu-id="0346d-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0346d-223">0x00000000</span></span>                      |
| <span data-ttu-id="0346d-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0346d-224">System-Flags</span></span>           | <span data-ttu-id="0346d-225">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0346d-225">0x00000013</span></span>                      |
| <span data-ttu-id="0346d-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0346d-226">Classes used in</span></span>        | [<span data-ttu-id="0346d-227">**Início**</span><span class="sxs-lookup"><span data-stu-id="0346d-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0346d-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0346d-228">Windows Server 2008</span></span>



| <span data-ttu-id="0346d-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="0346d-229">Entry</span></span> | <span data-ttu-id="0346d-230">Valor</span><span class="sxs-lookup"><span data-stu-id="0346d-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0346d-231">ID do link</span><span class="sxs-lookup"><span data-stu-id="0346d-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0346d-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0346d-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0346d-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="0346d-233">System-Only</span></span>            | <span data-ttu-id="0346d-234">True</span><span class="sxs-lookup"><span data-stu-id="0346d-234">True</span></span>                            |
| <span data-ttu-id="0346d-235">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0346d-235">Is-Single-Valued</span></span>       | <span data-ttu-id="0346d-236">True</span><span class="sxs-lookup"><span data-stu-id="0346d-236">True</span></span>                            |
| <span data-ttu-id="0346d-237">É indexado</span><span class="sxs-lookup"><span data-stu-id="0346d-237">Is Indexed</span></span>             | <span data-ttu-id="0346d-238">Falso</span><span class="sxs-lookup"><span data-stu-id="0346d-238">False</span></span>                           |
| <span data-ttu-id="0346d-239">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0346d-239">In Global Catalog</span></span>      | <span data-ttu-id="0346d-240">True</span><span class="sxs-lookup"><span data-stu-id="0346d-240">True</span></span>                            |
| <span data-ttu-id="0346d-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0346d-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="0346d-242">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0346d-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0346d-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0346d-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0346d-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0346d-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0346d-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0346d-245">Search-Flags</span></span>           | <span data-ttu-id="0346d-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0346d-246">0x00000000</span></span>                      |
| <span data-ttu-id="0346d-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0346d-247">System-Flags</span></span>           | <span data-ttu-id="0346d-248">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0346d-248">0x00000013</span></span>                      |
| <span data-ttu-id="0346d-249">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0346d-249">Classes used in</span></span>        | [<span data-ttu-id="0346d-250">**Início**</span><span class="sxs-lookup"><span data-stu-id="0346d-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0346d-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0346d-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0346d-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="0346d-252">Entry</span></span> | <span data-ttu-id="0346d-253">Valor</span><span class="sxs-lookup"><span data-stu-id="0346d-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0346d-254">ID do link</span><span class="sxs-lookup"><span data-stu-id="0346d-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0346d-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0346d-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0346d-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="0346d-256">System-Only</span></span>            | <span data-ttu-id="0346d-257">True</span><span class="sxs-lookup"><span data-stu-id="0346d-257">True</span></span>                            |
| <span data-ttu-id="0346d-258">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0346d-258">Is-Single-Valued</span></span>       | <span data-ttu-id="0346d-259">True</span><span class="sxs-lookup"><span data-stu-id="0346d-259">True</span></span>                            |
| <span data-ttu-id="0346d-260">É indexado</span><span class="sxs-lookup"><span data-stu-id="0346d-260">Is Indexed</span></span>             | <span data-ttu-id="0346d-261">Falso</span><span class="sxs-lookup"><span data-stu-id="0346d-261">False</span></span>                           |
| <span data-ttu-id="0346d-262">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0346d-262">In Global Catalog</span></span>      | <span data-ttu-id="0346d-263">True</span><span class="sxs-lookup"><span data-stu-id="0346d-263">True</span></span>                            |
| <span data-ttu-id="0346d-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0346d-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="0346d-265">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0346d-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0346d-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0346d-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0346d-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0346d-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0346d-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0346d-268">Search-Flags</span></span>           | <span data-ttu-id="0346d-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0346d-269">0x00000000</span></span>                      |
| <span data-ttu-id="0346d-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0346d-270">System-Flags</span></span>           | <span data-ttu-id="0346d-271">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0346d-271">0x00000013</span></span>                      |
| <span data-ttu-id="0346d-272">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0346d-272">Classes used in</span></span>        | [<span data-ttu-id="0346d-273">**Início**</span><span class="sxs-lookup"><span data-stu-id="0346d-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0346d-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0346d-274">Windows Server 2012</span></span>



| <span data-ttu-id="0346d-275">Entrada</span><span class="sxs-lookup"><span data-stu-id="0346d-275">Entry</span></span> | <span data-ttu-id="0346d-276">Valor</span><span class="sxs-lookup"><span data-stu-id="0346d-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0346d-277">ID do link</span><span class="sxs-lookup"><span data-stu-id="0346d-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0346d-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0346d-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0346d-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="0346d-279">System-Only</span></span>            | <span data-ttu-id="0346d-280">True</span><span class="sxs-lookup"><span data-stu-id="0346d-280">True</span></span>                            |
| <span data-ttu-id="0346d-281">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0346d-281">Is-Single-Valued</span></span>       | <span data-ttu-id="0346d-282">True</span><span class="sxs-lookup"><span data-stu-id="0346d-282">True</span></span>                            |
| <span data-ttu-id="0346d-283">É indexado</span><span class="sxs-lookup"><span data-stu-id="0346d-283">Is Indexed</span></span>             | <span data-ttu-id="0346d-284">Falso</span><span class="sxs-lookup"><span data-stu-id="0346d-284">False</span></span>                           |
| <span data-ttu-id="0346d-285">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0346d-285">In Global Catalog</span></span>      | <span data-ttu-id="0346d-286">True</span><span class="sxs-lookup"><span data-stu-id="0346d-286">True</span></span>                            |
| <span data-ttu-id="0346d-287">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0346d-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="0346d-288">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0346d-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0346d-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0346d-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0346d-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0346d-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0346d-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0346d-291">Search-Flags</span></span>           | <span data-ttu-id="0346d-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0346d-292">0x00000000</span></span>                      |
| <span data-ttu-id="0346d-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0346d-293">System-Flags</span></span>           | <span data-ttu-id="0346d-294">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0346d-294">0x00000013</span></span>                      |
| <span data-ttu-id="0346d-295">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0346d-295">Classes used in</span></span>        | [<span data-ttu-id="0346d-296">**Início**</span><span class="sxs-lookup"><span data-stu-id="0346d-296">**Top**</span></span>](c-top.md)<br/> |



 

 





