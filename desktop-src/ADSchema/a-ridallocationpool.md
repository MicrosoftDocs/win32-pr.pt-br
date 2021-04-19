---
title: Atributo RID-Allocation-pool
description: Um pool que foi previamente buscado para uso pelo Gerenciador de RID quando o pool de alocação de RID anterior foi usado.
ms.assetid: 6d49b497-322f-424c-badc-4801f51481f3
ms.tgt_platform: multiple
keywords:
- RID-alocação-atributo do pool-esquema do AD
- Esquema de AD do atributo rIDAllocationPool
topic_type:
- apiref
api_name:
- RID-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a035cef460cc3081144d66391db78fb32c61108b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105753856"
---
# <a name="rid-allocation-pool-attribute"></a><span data-ttu-id="884ac-105">Atributo RID-Allocation-pool</span><span class="sxs-lookup"><span data-stu-id="884ac-105">RID-Allocation-Pool attribute</span></span>

<span data-ttu-id="884ac-106">Um pool que foi previamente buscado para uso pelo Gerenciador de RID quando o pool de alocação de RID anterior foi usado.</span><span class="sxs-lookup"><span data-stu-id="884ac-106">A pool that was prefetched for use by the RID manager when the RID-Previous-Allocation-Pool has been used up.</span></span>



| <span data-ttu-id="884ac-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="884ac-107">Entry</span></span> | <span data-ttu-id="884ac-108">Valor</span><span class="sxs-lookup"><span data-stu-id="884ac-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="884ac-109">CN</span><span class="sxs-lookup"><span data-stu-id="884ac-109">CN</span></span>                | <span data-ttu-id="884ac-110">RID – pool de alocação</span><span class="sxs-lookup"><span data-stu-id="884ac-110">RID-Allocation-Pool</span></span>                  |
| <span data-ttu-id="884ac-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="884ac-111">Ldap-Display-Name</span></span> | <span data-ttu-id="884ac-112">rIDAllocationPool</span><span class="sxs-lookup"><span data-stu-id="884ac-112">rIDAllocationPool</span></span>                    |
| <span data-ttu-id="884ac-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="884ac-113">Size</span></span>              | <span data-ttu-id="884ac-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="884ac-114">8 bytes</span></span>                              |
| <span data-ttu-id="884ac-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="884ac-115">Update Privilege</span></span>  | <span data-ttu-id="884ac-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="884ac-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="884ac-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="884ac-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="884ac-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="884ac-118">Attribute-Id</span></span>      | <span data-ttu-id="884ac-119">1.2.840.113556.1.4.371</span><span class="sxs-lookup"><span data-stu-id="884ac-119">1.2.840.113556.1.4.371</span></span>               |
| <span data-ttu-id="884ac-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="884ac-120">System-Id-Guid</span></span>    | <span data-ttu-id="884ac-121">66171889-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="884ac-121">66171889-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="884ac-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="884ac-122">Syntax</span></span>            | [<span data-ttu-id="884ac-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="884ac-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="884ac-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="884ac-124">Implementations</span></span>

-   [<span data-ttu-id="884ac-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="884ac-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="884ac-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="884ac-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="884ac-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="884ac-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="884ac-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="884ac-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="884ac-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="884ac-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="884ac-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="884ac-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="884ac-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="884ac-131">Windows 2000 Server</span></span>



| <span data-ttu-id="884ac-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="884ac-132">Entry</span></span> | <span data-ttu-id="884ac-133">Valor</span><span class="sxs-lookup"><span data-stu-id="884ac-133">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="884ac-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="884ac-134">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="884ac-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="884ac-135">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="884ac-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="884ac-136">System-Only</span></span>            | <span data-ttu-id="884ac-137">True</span><span class="sxs-lookup"><span data-stu-id="884ac-137">True</span></span>                                   |
| <span data-ttu-id="884ac-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="884ac-138">Is-Single-Valued</span></span>       | <span data-ttu-id="884ac-139">True</span><span class="sxs-lookup"><span data-stu-id="884ac-139">True</span></span>                                   |
| <span data-ttu-id="884ac-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="884ac-140">Is Indexed</span></span>             | <span data-ttu-id="884ac-141">Falso</span><span class="sxs-lookup"><span data-stu-id="884ac-141">False</span></span>                                  |
| <span data-ttu-id="884ac-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="884ac-142">In Global Catalog</span></span>      | <span data-ttu-id="884ac-143">Falso</span><span class="sxs-lookup"><span data-stu-id="884ac-143">False</span></span>                                  |
| <span data-ttu-id="884ac-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="884ac-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="884ac-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="884ac-145">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="884ac-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="884ac-146">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="884ac-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="884ac-147">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="884ac-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="884ac-148">Search-Flags</span></span>           | <span data-ttu-id="884ac-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="884ac-149">0x00000000</span></span>                             |
| <span data-ttu-id="884ac-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="884ac-150">System-Flags</span></span>           | <span data-ttu-id="884ac-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="884ac-151">0x00000010</span></span>                             |
| <span data-ttu-id="884ac-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="884ac-152">Classes used in</span></span>        | [<span data-ttu-id="884ac-153">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="884ac-153">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="884ac-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="884ac-154">Windows Server 2003</span></span>



| <span data-ttu-id="884ac-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="884ac-155">Entry</span></span> | <span data-ttu-id="884ac-156">Valor</span><span class="sxs-lookup"><span data-stu-id="884ac-156">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="884ac-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="884ac-157">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="884ac-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="884ac-158">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="884ac-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="884ac-159">System-Only</span></span>            | <span data-ttu-id="884ac-160">True</span><span class="sxs-lookup"><span data-stu-id="884ac-160">True</span></span>                                   |
| <span data-ttu-id="884ac-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="884ac-161">Is-Single-Valued</span></span>       | <span data-ttu-id="884ac-162">True</span><span class="sxs-lookup"><span data-stu-id="884ac-162">True</span></span>                                   |
| <span data-ttu-id="884ac-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="884ac-163">Is Indexed</span></span>             | <span data-ttu-id="884ac-164">Falso</span><span class="sxs-lookup"><span data-stu-id="884ac-164">False</span></span>                                  |
| <span data-ttu-id="884ac-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="884ac-165">In Global Catalog</span></span>      | <span data-ttu-id="884ac-166">Falso</span><span class="sxs-lookup"><span data-stu-id="884ac-166">False</span></span>                                  |
| <span data-ttu-id="884ac-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="884ac-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="884ac-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="884ac-168">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="884ac-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="884ac-169">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="884ac-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="884ac-170">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="884ac-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="884ac-171">Search-Flags</span></span>           | <span data-ttu-id="884ac-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="884ac-172">0x00000000</span></span>                             |
| <span data-ttu-id="884ac-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="884ac-173">System-Flags</span></span>           | <span data-ttu-id="884ac-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="884ac-174">0x00000010</span></span>                             |
| <span data-ttu-id="884ac-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="884ac-175">Classes used in</span></span>        | [<span data-ttu-id="884ac-176">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="884ac-176">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="884ac-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="884ac-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="884ac-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="884ac-178">Entry</span></span> | <span data-ttu-id="884ac-179">Valor</span><span class="sxs-lookup"><span data-stu-id="884ac-179">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="884ac-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="884ac-180">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="884ac-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="884ac-181">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="884ac-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="884ac-182">System-Only</span></span>            | <span data-ttu-id="884ac-183">True</span><span class="sxs-lookup"><span data-stu-id="884ac-183">True</span></span>                                   |
| <span data-ttu-id="884ac-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="884ac-184">Is-Single-Valued</span></span>       | <span data-ttu-id="884ac-185">True</span><span class="sxs-lookup"><span data-stu-id="884ac-185">True</span></span>                                   |
| <span data-ttu-id="884ac-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="884ac-186">Is Indexed</span></span>             | <span data-ttu-id="884ac-187">Falso</span><span class="sxs-lookup"><span data-stu-id="884ac-187">False</span></span>                                  |
| <span data-ttu-id="884ac-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="884ac-188">In Global Catalog</span></span>      | <span data-ttu-id="884ac-189">Falso</span><span class="sxs-lookup"><span data-stu-id="884ac-189">False</span></span>                                  |
| <span data-ttu-id="884ac-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="884ac-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="884ac-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="884ac-191">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="884ac-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="884ac-192">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="884ac-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="884ac-193">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="884ac-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="884ac-194">Search-Flags</span></span>           | <span data-ttu-id="884ac-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="884ac-195">0x00000000</span></span>                             |
| <span data-ttu-id="884ac-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="884ac-196">System-Flags</span></span>           | <span data-ttu-id="884ac-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="884ac-197">0x00000010</span></span>                             |
| <span data-ttu-id="884ac-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="884ac-198">Classes used in</span></span>        | [<span data-ttu-id="884ac-199">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="884ac-199">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="884ac-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="884ac-200">Windows Server 2008</span></span>



| <span data-ttu-id="884ac-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="884ac-201">Entry</span></span> | <span data-ttu-id="884ac-202">Valor</span><span class="sxs-lookup"><span data-stu-id="884ac-202">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="884ac-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="884ac-203">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="884ac-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="884ac-204">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="884ac-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="884ac-205">System-Only</span></span>            | <span data-ttu-id="884ac-206">True</span><span class="sxs-lookup"><span data-stu-id="884ac-206">True</span></span>                                   |
| <span data-ttu-id="884ac-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="884ac-207">Is-Single-Valued</span></span>       | <span data-ttu-id="884ac-208">True</span><span class="sxs-lookup"><span data-stu-id="884ac-208">True</span></span>                                   |
| <span data-ttu-id="884ac-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="884ac-209">Is Indexed</span></span>             | <span data-ttu-id="884ac-210">Falso</span><span class="sxs-lookup"><span data-stu-id="884ac-210">False</span></span>                                  |
| <span data-ttu-id="884ac-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="884ac-211">In Global Catalog</span></span>      | <span data-ttu-id="884ac-212">Falso</span><span class="sxs-lookup"><span data-stu-id="884ac-212">False</span></span>                                  |
| <span data-ttu-id="884ac-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="884ac-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="884ac-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="884ac-214">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="884ac-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="884ac-215">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="884ac-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="884ac-216">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="884ac-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="884ac-217">Search-Flags</span></span>           | <span data-ttu-id="884ac-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="884ac-218">0x00000000</span></span>                             |
| <span data-ttu-id="884ac-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="884ac-219">System-Flags</span></span>           | <span data-ttu-id="884ac-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="884ac-220">0x00000010</span></span>                             |
| <span data-ttu-id="884ac-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="884ac-221">Classes used in</span></span>        | [<span data-ttu-id="884ac-222">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="884ac-222">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="884ac-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="884ac-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="884ac-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="884ac-224">Entry</span></span> | <span data-ttu-id="884ac-225">Valor</span><span class="sxs-lookup"><span data-stu-id="884ac-225">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="884ac-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="884ac-226">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="884ac-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="884ac-227">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="884ac-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="884ac-228">System-Only</span></span>            | <span data-ttu-id="884ac-229">True</span><span class="sxs-lookup"><span data-stu-id="884ac-229">True</span></span>                                   |
| <span data-ttu-id="884ac-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="884ac-230">Is-Single-Valued</span></span>       | <span data-ttu-id="884ac-231">True</span><span class="sxs-lookup"><span data-stu-id="884ac-231">True</span></span>                                   |
| <span data-ttu-id="884ac-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="884ac-232">Is Indexed</span></span>             | <span data-ttu-id="884ac-233">Falso</span><span class="sxs-lookup"><span data-stu-id="884ac-233">False</span></span>                                  |
| <span data-ttu-id="884ac-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="884ac-234">In Global Catalog</span></span>      | <span data-ttu-id="884ac-235">Falso</span><span class="sxs-lookup"><span data-stu-id="884ac-235">False</span></span>                                  |
| <span data-ttu-id="884ac-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="884ac-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="884ac-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="884ac-237">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="884ac-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="884ac-238">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="884ac-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="884ac-239">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="884ac-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="884ac-240">Search-Flags</span></span>           | <span data-ttu-id="884ac-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="884ac-241">0x00000000</span></span>                             |
| <span data-ttu-id="884ac-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="884ac-242">System-Flags</span></span>           | <span data-ttu-id="884ac-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="884ac-243">0x00000010</span></span>                             |
| <span data-ttu-id="884ac-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="884ac-244">Classes used in</span></span>        | [<span data-ttu-id="884ac-245">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="884ac-245">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="884ac-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="884ac-246">Windows Server 2012</span></span>



| <span data-ttu-id="884ac-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="884ac-247">Entry</span></span> | <span data-ttu-id="884ac-248">Valor</span><span class="sxs-lookup"><span data-stu-id="884ac-248">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="884ac-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="884ac-249">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="884ac-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="884ac-250">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="884ac-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="884ac-251">System-Only</span></span>            | <span data-ttu-id="884ac-252">True</span><span class="sxs-lookup"><span data-stu-id="884ac-252">True</span></span>                                   |
| <span data-ttu-id="884ac-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="884ac-253">Is-Single-Valued</span></span>       | <span data-ttu-id="884ac-254">True</span><span class="sxs-lookup"><span data-stu-id="884ac-254">True</span></span>                                   |
| <span data-ttu-id="884ac-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="884ac-255">Is Indexed</span></span>             | <span data-ttu-id="884ac-256">Falso</span><span class="sxs-lookup"><span data-stu-id="884ac-256">False</span></span>                                  |
| <span data-ttu-id="884ac-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="884ac-257">In Global Catalog</span></span>      | <span data-ttu-id="884ac-258">Falso</span><span class="sxs-lookup"><span data-stu-id="884ac-258">False</span></span>                                  |
| <span data-ttu-id="884ac-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="884ac-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="884ac-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="884ac-260">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="884ac-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="884ac-261">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="884ac-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="884ac-262">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="884ac-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="884ac-263">Search-Flags</span></span>           | <span data-ttu-id="884ac-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="884ac-264">0x00000000</span></span>                             |
| <span data-ttu-id="884ac-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="884ac-265">System-Flags</span></span>           | <span data-ttu-id="884ac-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="884ac-266">0x00000010</span></span>                             |
| <span data-ttu-id="884ac-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="884ac-267">Classes used in</span></span>        | [<span data-ttu-id="884ac-268">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="884ac-268">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





