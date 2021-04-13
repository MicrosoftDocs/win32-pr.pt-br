---
title: Schema-Info atributo
description: Um valor binário interno usado para detectar alterações de esquema entre os DCs e forçar um ciclo de replicação do NC de esquema antes de replicar qualquer outro NC. Usado para resolver Ties quando o esquema FSMO é capturado e uma alteração é feita em mais de um DC.
ms.assetid: 416cef3f-211b-439d-b177-267806c6a5d2
ms.tgt_platform: multiple
keywords:
- Esquema de Schema-Info do atributo AD
- Esquema de AD do atributo schemaInfo
topic_type:
- apiref
api_name:
- Schema-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca55fc8ad3f53709b3819a7333e3470a1ac35cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104500042"
---
# <a name="schema-info-attribute"></a><span data-ttu-id="67589-106">Schema-Info atributo</span><span class="sxs-lookup"><span data-stu-id="67589-106">Schema-Info attribute</span></span>

<span data-ttu-id="67589-107">Um valor binário interno usado para detectar alterações de esquema entre os DCs e forçar um ciclo de replicação do NC de esquema antes de replicar qualquer outro NC.</span><span class="sxs-lookup"><span data-stu-id="67589-107">An internal binary value used to detect schema changes between DCs and force a schema NC replication cycle before replicating any other NC.</span></span> <span data-ttu-id="67589-108">Usado para resolver Ties quando o esquema FSMO é capturado e uma alteração é feita em mais de um DC.</span><span class="sxs-lookup"><span data-stu-id="67589-108">Used to resolve ties when the schema FSMO is seized and a change is made on more than one DC.</span></span>



| <span data-ttu-id="67589-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="67589-109">Entry</span></span> | <span data-ttu-id="67589-110">Valor</span><span class="sxs-lookup"><span data-stu-id="67589-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="67589-111">CN</span><span class="sxs-lookup"><span data-stu-id="67589-111">CN</span></span>                | <span data-ttu-id="67589-112">Schema-Info</span><span class="sxs-lookup"><span data-stu-id="67589-112">Schema-Info</span></span>                                           |
| <span data-ttu-id="67589-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="67589-113">Ldap-Display-Name</span></span> | <span data-ttu-id="67589-114">schemaInfo</span><span class="sxs-lookup"><span data-stu-id="67589-114">schemaInfo</span></span>                                            |
| <span data-ttu-id="67589-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="67589-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="67589-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="67589-116">Update Privilege</span></span>  | <span data-ttu-id="67589-117">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="67589-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="67589-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="67589-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="67589-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="67589-119">Attribute-Id</span></span>      | <span data-ttu-id="67589-120">1.2.840.113556.1.4.1358</span><span class="sxs-lookup"><span data-stu-id="67589-120">1.2.840.113556.1.4.1358</span></span>                               |
| <span data-ttu-id="67589-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="67589-121">System-Id-Guid</span></span>    | <span data-ttu-id="67589-122">f9fb64ae-93b4-11d2-9945-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="67589-122">f9fb64ae-93b4-11d2-9945-0000f87a57d4</span></span>                  |
| <span data-ttu-id="67589-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="67589-123">Syntax</span></span>            | [<span data-ttu-id="67589-124">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="67589-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="67589-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="67589-125">Implementations</span></span>

-   [<span data-ttu-id="67589-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="67589-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="67589-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="67589-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="67589-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="67589-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="67589-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="67589-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="67589-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="67589-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="67589-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="67589-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="67589-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="67589-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="67589-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="67589-133">Windows 2000 Server</span></span>



| <span data-ttu-id="67589-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="67589-134">Entry</span></span> | <span data-ttu-id="67589-135">Valor</span><span class="sxs-lookup"><span data-stu-id="67589-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="67589-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="67589-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="67589-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67589-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="67589-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="67589-138">System-Only</span></span>            | <span data-ttu-id="67589-139">True</span><span class="sxs-lookup"><span data-stu-id="67589-139">True</span></span>                            |
| <span data-ttu-id="67589-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="67589-140">Is-Single-Valued</span></span>       | <span data-ttu-id="67589-141">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-141">False</span></span>                           |
| <span data-ttu-id="67589-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="67589-142">Is Indexed</span></span>             | <span data-ttu-id="67589-143">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-143">False</span></span>                           |
| <span data-ttu-id="67589-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="67589-144">In Global Catalog</span></span>      | <span data-ttu-id="67589-145">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-145">False</span></span>                           |
| <span data-ttu-id="67589-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="67589-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="67589-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="67589-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="67589-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67589-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="67589-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67589-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="67589-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67589-150">Search-Flags</span></span>           | <span data-ttu-id="67589-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67589-151">0x00000000</span></span>                      |
| <span data-ttu-id="67589-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67589-152">System-Flags</span></span>           | <span data-ttu-id="67589-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67589-153">0x00000010</span></span>                      |
| <span data-ttu-id="67589-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="67589-154">Classes used in</span></span>        | [<span data-ttu-id="67589-155">**DMD**</span><span class="sxs-lookup"><span data-stu-id="67589-155">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="67589-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="67589-156">Windows Server 2003</span></span>



| <span data-ttu-id="67589-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="67589-157">Entry</span></span> | <span data-ttu-id="67589-158">Valor</span><span class="sxs-lookup"><span data-stu-id="67589-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="67589-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="67589-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="67589-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67589-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="67589-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="67589-161">System-Only</span></span>            | <span data-ttu-id="67589-162">True</span><span class="sxs-lookup"><span data-stu-id="67589-162">True</span></span>                            |
| <span data-ttu-id="67589-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="67589-163">Is-Single-Valued</span></span>       | <span data-ttu-id="67589-164">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-164">False</span></span>                           |
| <span data-ttu-id="67589-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="67589-165">Is Indexed</span></span>             | <span data-ttu-id="67589-166">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-166">False</span></span>                           |
| <span data-ttu-id="67589-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="67589-167">In Global Catalog</span></span>      | <span data-ttu-id="67589-168">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-168">False</span></span>                           |
| <span data-ttu-id="67589-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="67589-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="67589-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="67589-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="67589-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67589-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="67589-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67589-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="67589-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67589-173">Search-Flags</span></span>           | <span data-ttu-id="67589-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67589-174">0x00000000</span></span>                      |
| <span data-ttu-id="67589-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67589-175">System-Flags</span></span>           | <span data-ttu-id="67589-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67589-176">0x00000010</span></span>                      |
| <span data-ttu-id="67589-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="67589-177">Classes used in</span></span>        | [<span data-ttu-id="67589-178">**DMD**</span><span class="sxs-lookup"><span data-stu-id="67589-178">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="adam"></a><span data-ttu-id="67589-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="67589-179">ADAM</span></span>



| <span data-ttu-id="67589-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="67589-180">Entry</span></span> | <span data-ttu-id="67589-181">Valor</span><span class="sxs-lookup"><span data-stu-id="67589-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="67589-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="67589-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="67589-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67589-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="67589-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="67589-184">System-Only</span></span>            | <span data-ttu-id="67589-185">True</span><span class="sxs-lookup"><span data-stu-id="67589-185">True</span></span>                            |
| <span data-ttu-id="67589-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="67589-186">Is-Single-Valued</span></span>       | <span data-ttu-id="67589-187">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-187">False</span></span>                           |
| <span data-ttu-id="67589-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="67589-188">Is Indexed</span></span>             | <span data-ttu-id="67589-189">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-189">False</span></span>                           |
| <span data-ttu-id="67589-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="67589-190">In Global Catalog</span></span>      | <span data-ttu-id="67589-191">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-191">False</span></span>                           |
| <span data-ttu-id="67589-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="67589-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="67589-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="67589-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="67589-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67589-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="67589-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67589-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="67589-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67589-196">Search-Flags</span></span>           | <span data-ttu-id="67589-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67589-197">0x00000000</span></span>                      |
| <span data-ttu-id="67589-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67589-198">System-Flags</span></span>           | <span data-ttu-id="67589-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67589-199">0x00000010</span></span>                      |
| <span data-ttu-id="67589-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="67589-200">Classes used in</span></span>        | [<span data-ttu-id="67589-201">**DMD**</span><span class="sxs-lookup"><span data-stu-id="67589-201">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="67589-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="67589-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="67589-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="67589-203">Entry</span></span> | <span data-ttu-id="67589-204">Valor</span><span class="sxs-lookup"><span data-stu-id="67589-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="67589-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="67589-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="67589-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67589-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="67589-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="67589-207">System-Only</span></span>            | <span data-ttu-id="67589-208">True</span><span class="sxs-lookup"><span data-stu-id="67589-208">True</span></span>                            |
| <span data-ttu-id="67589-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="67589-209">Is-Single-Valued</span></span>       | <span data-ttu-id="67589-210">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-210">False</span></span>                           |
| <span data-ttu-id="67589-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="67589-211">Is Indexed</span></span>             | <span data-ttu-id="67589-212">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-212">False</span></span>                           |
| <span data-ttu-id="67589-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="67589-213">In Global Catalog</span></span>      | <span data-ttu-id="67589-214">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-214">False</span></span>                           |
| <span data-ttu-id="67589-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="67589-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="67589-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="67589-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="67589-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67589-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="67589-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67589-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="67589-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67589-219">Search-Flags</span></span>           | <span data-ttu-id="67589-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67589-220">0x00000000</span></span>                      |
| <span data-ttu-id="67589-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67589-221">System-Flags</span></span>           | <span data-ttu-id="67589-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67589-222">0x00000010</span></span>                      |
| <span data-ttu-id="67589-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="67589-223">Classes used in</span></span>        | [<span data-ttu-id="67589-224">**DMD**</span><span class="sxs-lookup"><span data-stu-id="67589-224">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="67589-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67589-225">Windows Server 2008</span></span>



| <span data-ttu-id="67589-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="67589-226">Entry</span></span> | <span data-ttu-id="67589-227">Valor</span><span class="sxs-lookup"><span data-stu-id="67589-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="67589-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="67589-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="67589-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67589-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="67589-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="67589-230">System-Only</span></span>            | <span data-ttu-id="67589-231">True</span><span class="sxs-lookup"><span data-stu-id="67589-231">True</span></span>                            |
| <span data-ttu-id="67589-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="67589-232">Is-Single-Valued</span></span>       | <span data-ttu-id="67589-233">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-233">False</span></span>                           |
| <span data-ttu-id="67589-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="67589-234">Is Indexed</span></span>             | <span data-ttu-id="67589-235">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-235">False</span></span>                           |
| <span data-ttu-id="67589-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="67589-236">In Global Catalog</span></span>      | <span data-ttu-id="67589-237">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-237">False</span></span>                           |
| <span data-ttu-id="67589-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="67589-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="67589-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="67589-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="67589-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67589-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="67589-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67589-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="67589-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67589-242">Search-Flags</span></span>           | <span data-ttu-id="67589-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67589-243">0x00000000</span></span>                      |
| <span data-ttu-id="67589-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67589-244">System-Flags</span></span>           | <span data-ttu-id="67589-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67589-245">0x00000010</span></span>                      |
| <span data-ttu-id="67589-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="67589-246">Classes used in</span></span>        | [<span data-ttu-id="67589-247">**DMD**</span><span class="sxs-lookup"><span data-stu-id="67589-247">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="67589-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="67589-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="67589-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="67589-249">Entry</span></span> | <span data-ttu-id="67589-250">Valor</span><span class="sxs-lookup"><span data-stu-id="67589-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="67589-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="67589-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="67589-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67589-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="67589-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="67589-253">System-Only</span></span>            | <span data-ttu-id="67589-254">True</span><span class="sxs-lookup"><span data-stu-id="67589-254">True</span></span>                            |
| <span data-ttu-id="67589-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="67589-255">Is-Single-Valued</span></span>       | <span data-ttu-id="67589-256">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-256">False</span></span>                           |
| <span data-ttu-id="67589-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="67589-257">Is Indexed</span></span>             | <span data-ttu-id="67589-258">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-258">False</span></span>                           |
| <span data-ttu-id="67589-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="67589-259">In Global Catalog</span></span>      | <span data-ttu-id="67589-260">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-260">False</span></span>                           |
| <span data-ttu-id="67589-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="67589-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="67589-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="67589-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="67589-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67589-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="67589-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67589-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="67589-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67589-265">Search-Flags</span></span>           | <span data-ttu-id="67589-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67589-266">0x00000000</span></span>                      |
| <span data-ttu-id="67589-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67589-267">System-Flags</span></span>           | <span data-ttu-id="67589-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67589-268">0x00000010</span></span>                      |
| <span data-ttu-id="67589-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="67589-269">Classes used in</span></span>        | [<span data-ttu-id="67589-270">**DMD**</span><span class="sxs-lookup"><span data-stu-id="67589-270">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="67589-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="67589-271">Windows Server 2012</span></span>



| <span data-ttu-id="67589-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="67589-272">Entry</span></span> | <span data-ttu-id="67589-273">Valor</span><span class="sxs-lookup"><span data-stu-id="67589-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="67589-274">ID do link</span><span class="sxs-lookup"><span data-stu-id="67589-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="67589-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67589-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="67589-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="67589-276">System-Only</span></span>            | <span data-ttu-id="67589-277">True</span><span class="sxs-lookup"><span data-stu-id="67589-277">True</span></span>                            |
| <span data-ttu-id="67589-278">É de valor único</span><span class="sxs-lookup"><span data-stu-id="67589-278">Is-Single-Valued</span></span>       | <span data-ttu-id="67589-279">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-279">False</span></span>                           |
| <span data-ttu-id="67589-280">É indexado</span><span class="sxs-lookup"><span data-stu-id="67589-280">Is Indexed</span></span>             | <span data-ttu-id="67589-281">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-281">False</span></span>                           |
| <span data-ttu-id="67589-282">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="67589-282">In Global Catalog</span></span>      | <span data-ttu-id="67589-283">Falso</span><span class="sxs-lookup"><span data-stu-id="67589-283">False</span></span>                           |
| <span data-ttu-id="67589-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="67589-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="67589-285">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="67589-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="67589-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67589-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="67589-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67589-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="67589-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67589-288">Search-Flags</span></span>           | <span data-ttu-id="67589-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67589-289">0x00000000</span></span>                      |
| <span data-ttu-id="67589-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67589-290">System-Flags</span></span>           | <span data-ttu-id="67589-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67589-291">0x00000010</span></span>                      |
| <span data-ttu-id="67589-292">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="67589-292">Classes used in</span></span>        | [<span data-ttu-id="67589-293">**DMD**</span><span class="sxs-lookup"><span data-stu-id="67589-293">**DMD**</span></span>](c-dmd.md)<br/> |



 

 





