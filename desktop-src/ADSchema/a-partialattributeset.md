---
title: Atributo parcial-conjunto de atributos
description: Controla o estado de replicação interna de réplicas parciais (ou seja, em GCs). Atributo do objeto NC de réplica parcial. Define o conjunto de atributos presentes em um NC de réplica parcial específico.
ms.assetid: 2840d2b7-e186-4ef2-9107-f1e5c0c2f760
ms.tgt_platform: multiple
keywords:
- Atributo de AD de atributos de conjunto de atributos parciais
- Esquema de AD do atributo partialAttributeSet
topic_type:
- apiref
api_name:
- Partial-Attribute-Set
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e932c07b0d4a8e3ea8f30f504194093d61912b7b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105749143"
---
# <a name="partial-attribute-set-attribute"></a><span data-ttu-id="74ab1-107">Atributo parcial-conjunto de atributos</span><span class="sxs-lookup"><span data-stu-id="74ab1-107">Partial-Attribute-Set attribute</span></span>

<span data-ttu-id="74ab1-108">Controla o estado de replicação interna de réplicas parciais (ou seja, em GCs).</span><span class="sxs-lookup"><span data-stu-id="74ab1-108">Tracks the internal replication state of partial replicas (that is, on GCs).</span></span> <span data-ttu-id="74ab1-109">Atributo do objeto NC de réplica parcial.</span><span class="sxs-lookup"><span data-stu-id="74ab1-109">Attribute of the partial replica NC object.</span></span> <span data-ttu-id="74ab1-110">Define o conjunto de atributos presentes em um NC de réplica parcial específico.</span><span class="sxs-lookup"><span data-stu-id="74ab1-110">Defines the set of attributes present on a particular partial replica NC.</span></span>



| <span data-ttu-id="74ab1-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="74ab1-111">Entry</span></span> | <span data-ttu-id="74ab1-112">Valor</span><span class="sxs-lookup"><span data-stu-id="74ab1-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="74ab1-113">CN</span><span class="sxs-lookup"><span data-stu-id="74ab1-113">CN</span></span>                | <span data-ttu-id="74ab1-114">Conjunto de atributos parciais</span><span class="sxs-lookup"><span data-stu-id="74ab1-114">Partial-Attribute-Set</span></span>                                 |
| <span data-ttu-id="74ab1-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="74ab1-115">Ldap-Display-Name</span></span> | <span data-ttu-id="74ab1-116">partialAttributeSet</span><span class="sxs-lookup"><span data-stu-id="74ab1-116">partialAttributeSet</span></span>                                   |
| <span data-ttu-id="74ab1-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="74ab1-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="74ab1-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="74ab1-118">Update Privilege</span></span>  | <span data-ttu-id="74ab1-119">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="74ab1-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="74ab1-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="74ab1-120">Update Frequency</span></span>  | <span data-ttu-id="74ab1-121">Durante a replicação</span><span class="sxs-lookup"><span data-stu-id="74ab1-121">During replication</span></span>                                    |
| <span data-ttu-id="74ab1-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="74ab1-122">Attribute-Id</span></span>      | <span data-ttu-id="74ab1-123">1.2.840.113556.1.4.640</span><span class="sxs-lookup"><span data-stu-id="74ab1-123">1.2.840.113556.1.4.640</span></span>                                |
| <span data-ttu-id="74ab1-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="74ab1-124">System-Id-Guid</span></span>    | <span data-ttu-id="74ab1-125">19405b9e-3cfa-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="74ab1-125">19405b9e-3cfa-11d1-a9c0-0000f80367c1</span></span>                  |
| <span data-ttu-id="74ab1-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="74ab1-126">Syntax</span></span>            | [<span data-ttu-id="74ab1-127">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="74ab1-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="74ab1-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="74ab1-128">Implementations</span></span>

-   [<span data-ttu-id="74ab1-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="74ab1-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="74ab1-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="74ab1-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="74ab1-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="74ab1-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="74ab1-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="74ab1-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="74ab1-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="74ab1-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="74ab1-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="74ab1-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="74ab1-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="74ab1-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="74ab1-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="74ab1-136">Windows 2000 Server</span></span>



| <span data-ttu-id="74ab1-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="74ab1-137">Entry</span></span> | <span data-ttu-id="74ab1-138">Valor</span><span class="sxs-lookup"><span data-stu-id="74ab1-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="74ab1-139">ID do link</span><span class="sxs-lookup"><span data-stu-id="74ab1-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="74ab1-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74ab1-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="74ab1-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="74ab1-141">System-Only</span></span>            | <span data-ttu-id="74ab1-142">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-142">True</span></span>                            |
| <span data-ttu-id="74ab1-143">É de valor único</span><span class="sxs-lookup"><span data-stu-id="74ab1-143">Is-Single-Valued</span></span>       | <span data-ttu-id="74ab1-144">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-144">True</span></span>                            |
| <span data-ttu-id="74ab1-145">É indexado</span><span class="sxs-lookup"><span data-stu-id="74ab1-145">Is Indexed</span></span>             | <span data-ttu-id="74ab1-146">Falso</span><span class="sxs-lookup"><span data-stu-id="74ab1-146">False</span></span>                           |
| <span data-ttu-id="74ab1-147">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="74ab1-147">In Global Catalog</span></span>      | <span data-ttu-id="74ab1-148">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-148">True</span></span>                            |
| <span data-ttu-id="74ab1-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="74ab1-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="74ab1-150">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="74ab1-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="74ab1-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74ab1-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="74ab1-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74ab1-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="74ab1-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74ab1-153">Search-Flags</span></span>           | <span data-ttu-id="74ab1-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74ab1-154">0x00000000</span></span>                      |
| <span data-ttu-id="74ab1-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74ab1-155">System-Flags</span></span>           | <span data-ttu-id="74ab1-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="74ab1-156">0x00000013</span></span>                      |
| <span data-ttu-id="74ab1-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="74ab1-157">Classes used in</span></span>        | [<span data-ttu-id="74ab1-158">**Início**</span><span class="sxs-lookup"><span data-stu-id="74ab1-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="74ab1-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="74ab1-159">Windows Server 2003</span></span>



| <span data-ttu-id="74ab1-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="74ab1-160">Entry</span></span> | <span data-ttu-id="74ab1-161">Valor</span><span class="sxs-lookup"><span data-stu-id="74ab1-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="74ab1-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="74ab1-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="74ab1-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74ab1-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="74ab1-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="74ab1-164">System-Only</span></span>            | <span data-ttu-id="74ab1-165">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-165">True</span></span>                            |
| <span data-ttu-id="74ab1-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="74ab1-166">Is-Single-Valued</span></span>       | <span data-ttu-id="74ab1-167">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-167">True</span></span>                            |
| <span data-ttu-id="74ab1-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="74ab1-168">Is Indexed</span></span>             | <span data-ttu-id="74ab1-169">Falso</span><span class="sxs-lookup"><span data-stu-id="74ab1-169">False</span></span>                           |
| <span data-ttu-id="74ab1-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="74ab1-170">In Global Catalog</span></span>      | <span data-ttu-id="74ab1-171">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-171">True</span></span>                            |
| <span data-ttu-id="74ab1-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="74ab1-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="74ab1-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="74ab1-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="74ab1-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74ab1-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="74ab1-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74ab1-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="74ab1-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74ab1-176">Search-Flags</span></span>           | <span data-ttu-id="74ab1-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74ab1-177">0x00000000</span></span>                      |
| <span data-ttu-id="74ab1-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74ab1-178">System-Flags</span></span>           | <span data-ttu-id="74ab1-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="74ab1-179">0x00000013</span></span>                      |
| <span data-ttu-id="74ab1-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="74ab1-180">Classes used in</span></span>        | [<span data-ttu-id="74ab1-181">**Início**</span><span class="sxs-lookup"><span data-stu-id="74ab1-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="74ab1-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="74ab1-182">ADAM</span></span>



| <span data-ttu-id="74ab1-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="74ab1-183">Entry</span></span> | <span data-ttu-id="74ab1-184">Valor</span><span class="sxs-lookup"><span data-stu-id="74ab1-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="74ab1-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="74ab1-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="74ab1-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74ab1-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="74ab1-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="74ab1-187">System-Only</span></span>            | <span data-ttu-id="74ab1-188">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-188">True</span></span>                            |
| <span data-ttu-id="74ab1-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="74ab1-189">Is-Single-Valued</span></span>       | <span data-ttu-id="74ab1-190">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-190">True</span></span>                            |
| <span data-ttu-id="74ab1-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="74ab1-191">Is Indexed</span></span>             | <span data-ttu-id="74ab1-192">Falso</span><span class="sxs-lookup"><span data-stu-id="74ab1-192">False</span></span>                           |
| <span data-ttu-id="74ab1-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="74ab1-193">In Global Catalog</span></span>      | <span data-ttu-id="74ab1-194">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-194">True</span></span>                            |
| <span data-ttu-id="74ab1-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="74ab1-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="74ab1-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="74ab1-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="74ab1-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74ab1-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="74ab1-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74ab1-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="74ab1-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74ab1-199">Search-Flags</span></span>           | <span data-ttu-id="74ab1-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74ab1-200">0x00000000</span></span>                      |
| <span data-ttu-id="74ab1-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74ab1-201">System-Flags</span></span>           | <span data-ttu-id="74ab1-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="74ab1-202">0x00000013</span></span>                      |
| <span data-ttu-id="74ab1-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="74ab1-203">Classes used in</span></span>        | [<span data-ttu-id="74ab1-204">**Início**</span><span class="sxs-lookup"><span data-stu-id="74ab1-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="74ab1-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="74ab1-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="74ab1-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="74ab1-206">Entry</span></span> | <span data-ttu-id="74ab1-207">Valor</span><span class="sxs-lookup"><span data-stu-id="74ab1-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="74ab1-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="74ab1-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="74ab1-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74ab1-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="74ab1-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="74ab1-210">System-Only</span></span>            | <span data-ttu-id="74ab1-211">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-211">True</span></span>                            |
| <span data-ttu-id="74ab1-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="74ab1-212">Is-Single-Valued</span></span>       | <span data-ttu-id="74ab1-213">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-213">True</span></span>                            |
| <span data-ttu-id="74ab1-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="74ab1-214">Is Indexed</span></span>             | <span data-ttu-id="74ab1-215">Falso</span><span class="sxs-lookup"><span data-stu-id="74ab1-215">False</span></span>                           |
| <span data-ttu-id="74ab1-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="74ab1-216">In Global Catalog</span></span>      | <span data-ttu-id="74ab1-217">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-217">True</span></span>                            |
| <span data-ttu-id="74ab1-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="74ab1-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="74ab1-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="74ab1-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="74ab1-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74ab1-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="74ab1-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74ab1-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="74ab1-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74ab1-222">Search-Flags</span></span>           | <span data-ttu-id="74ab1-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74ab1-223">0x00000000</span></span>                      |
| <span data-ttu-id="74ab1-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74ab1-224">System-Flags</span></span>           | <span data-ttu-id="74ab1-225">0x00000013</span><span class="sxs-lookup"><span data-stu-id="74ab1-225">0x00000013</span></span>                      |
| <span data-ttu-id="74ab1-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="74ab1-226">Classes used in</span></span>        | [<span data-ttu-id="74ab1-227">**Início**</span><span class="sxs-lookup"><span data-stu-id="74ab1-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="74ab1-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74ab1-228">Windows Server 2008</span></span>



| <span data-ttu-id="74ab1-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="74ab1-229">Entry</span></span> | <span data-ttu-id="74ab1-230">Valor</span><span class="sxs-lookup"><span data-stu-id="74ab1-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="74ab1-231">ID do link</span><span class="sxs-lookup"><span data-stu-id="74ab1-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="74ab1-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74ab1-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="74ab1-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="74ab1-233">System-Only</span></span>            | <span data-ttu-id="74ab1-234">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-234">True</span></span>                            |
| <span data-ttu-id="74ab1-235">É de valor único</span><span class="sxs-lookup"><span data-stu-id="74ab1-235">Is-Single-Valued</span></span>       | <span data-ttu-id="74ab1-236">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-236">True</span></span>                            |
| <span data-ttu-id="74ab1-237">É indexado</span><span class="sxs-lookup"><span data-stu-id="74ab1-237">Is Indexed</span></span>             | <span data-ttu-id="74ab1-238">Falso</span><span class="sxs-lookup"><span data-stu-id="74ab1-238">False</span></span>                           |
| <span data-ttu-id="74ab1-239">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="74ab1-239">In Global Catalog</span></span>      | <span data-ttu-id="74ab1-240">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-240">True</span></span>                            |
| <span data-ttu-id="74ab1-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="74ab1-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="74ab1-242">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="74ab1-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="74ab1-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74ab1-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="74ab1-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74ab1-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="74ab1-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74ab1-245">Search-Flags</span></span>           | <span data-ttu-id="74ab1-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74ab1-246">0x00000000</span></span>                      |
| <span data-ttu-id="74ab1-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74ab1-247">System-Flags</span></span>           | <span data-ttu-id="74ab1-248">0x00000013</span><span class="sxs-lookup"><span data-stu-id="74ab1-248">0x00000013</span></span>                      |
| <span data-ttu-id="74ab1-249">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="74ab1-249">Classes used in</span></span>        | [<span data-ttu-id="74ab1-250">**Início**</span><span class="sxs-lookup"><span data-stu-id="74ab1-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="74ab1-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="74ab1-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="74ab1-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="74ab1-252">Entry</span></span> | <span data-ttu-id="74ab1-253">Valor</span><span class="sxs-lookup"><span data-stu-id="74ab1-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="74ab1-254">ID do link</span><span class="sxs-lookup"><span data-stu-id="74ab1-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="74ab1-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74ab1-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="74ab1-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="74ab1-256">System-Only</span></span>            | <span data-ttu-id="74ab1-257">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-257">True</span></span>                            |
| <span data-ttu-id="74ab1-258">É de valor único</span><span class="sxs-lookup"><span data-stu-id="74ab1-258">Is-Single-Valued</span></span>       | <span data-ttu-id="74ab1-259">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-259">True</span></span>                            |
| <span data-ttu-id="74ab1-260">É indexado</span><span class="sxs-lookup"><span data-stu-id="74ab1-260">Is Indexed</span></span>             | <span data-ttu-id="74ab1-261">Falso</span><span class="sxs-lookup"><span data-stu-id="74ab1-261">False</span></span>                           |
| <span data-ttu-id="74ab1-262">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="74ab1-262">In Global Catalog</span></span>      | <span data-ttu-id="74ab1-263">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-263">True</span></span>                            |
| <span data-ttu-id="74ab1-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="74ab1-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="74ab1-265">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="74ab1-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="74ab1-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74ab1-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="74ab1-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74ab1-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="74ab1-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74ab1-268">Search-Flags</span></span>           | <span data-ttu-id="74ab1-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74ab1-269">0x00000000</span></span>                      |
| <span data-ttu-id="74ab1-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74ab1-270">System-Flags</span></span>           | <span data-ttu-id="74ab1-271">0x00000013</span><span class="sxs-lookup"><span data-stu-id="74ab1-271">0x00000013</span></span>                      |
| <span data-ttu-id="74ab1-272">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="74ab1-272">Classes used in</span></span>        | [<span data-ttu-id="74ab1-273">**Início**</span><span class="sxs-lookup"><span data-stu-id="74ab1-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="74ab1-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="74ab1-274">Windows Server 2012</span></span>



| <span data-ttu-id="74ab1-275">Entrada</span><span class="sxs-lookup"><span data-stu-id="74ab1-275">Entry</span></span> | <span data-ttu-id="74ab1-276">Valor</span><span class="sxs-lookup"><span data-stu-id="74ab1-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="74ab1-277">ID do link</span><span class="sxs-lookup"><span data-stu-id="74ab1-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="74ab1-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74ab1-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="74ab1-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="74ab1-279">System-Only</span></span>            | <span data-ttu-id="74ab1-280">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-280">True</span></span>                            |
| <span data-ttu-id="74ab1-281">É de valor único</span><span class="sxs-lookup"><span data-stu-id="74ab1-281">Is-Single-Valued</span></span>       | <span data-ttu-id="74ab1-282">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-282">True</span></span>                            |
| <span data-ttu-id="74ab1-283">É indexado</span><span class="sxs-lookup"><span data-stu-id="74ab1-283">Is Indexed</span></span>             | <span data-ttu-id="74ab1-284">Falso</span><span class="sxs-lookup"><span data-stu-id="74ab1-284">False</span></span>                           |
| <span data-ttu-id="74ab1-285">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="74ab1-285">In Global Catalog</span></span>      | <span data-ttu-id="74ab1-286">True</span><span class="sxs-lookup"><span data-stu-id="74ab1-286">True</span></span>                            |
| <span data-ttu-id="74ab1-287">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="74ab1-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="74ab1-288">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="74ab1-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="74ab1-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74ab1-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="74ab1-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74ab1-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="74ab1-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74ab1-291">Search-Flags</span></span>           | <span data-ttu-id="74ab1-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74ab1-292">0x00000000</span></span>                      |
| <span data-ttu-id="74ab1-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74ab1-293">System-Flags</span></span>           | <span data-ttu-id="74ab1-294">0x00000013</span><span class="sxs-lookup"><span data-stu-id="74ab1-294">0x00000013</span></span>                      |
| <span data-ttu-id="74ab1-295">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="74ab1-295">Classes used in</span></span>        | [<span data-ttu-id="74ab1-296">**Início**</span><span class="sxs-lookup"><span data-stu-id="74ab1-296">**Top**</span></span>](c-top.md)<br/> |



 

 





