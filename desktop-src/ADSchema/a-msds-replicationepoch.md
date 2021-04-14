---
title: atributo ms-DS-ReplicationEpoch
description: Isso é usado para manter a época sob a qual todos os DCs estão replicando. Uma época é o período de tempo em que um domínio tem um nome específico. Uma nova época começa quando ocorre uma alteração no nome de domínio.
ms.assetid: d8a3c4fd-f416-483f-820f-7b3182d0bfc3
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DS-ReplicationEpoch
- atributo msDS-ReplicationEpoch do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-ReplicationEpoch
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef9aaefefe5cd1ae269508390ae13f67037fdb8a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104499988"
---
# <a name="ms-ds-replicationepoch-attribute"></a><span data-ttu-id="122ed-107">atributo ms-DS-ReplicationEpoch</span><span class="sxs-lookup"><span data-stu-id="122ed-107">ms-DS-ReplicationEpoch attribute</span></span>

<span data-ttu-id="122ed-108">Isso é usado para manter a época sob a qual todos os DCs estão replicando.</span><span class="sxs-lookup"><span data-stu-id="122ed-108">This is used to hold the epoch under which all the DCs are replicating.</span></span> <span data-ttu-id="122ed-109">Uma época é o período de tempo em que um domínio tem um nome específico.</span><span class="sxs-lookup"><span data-stu-id="122ed-109">An epoch is the period of time in which a domain has a specific name.</span></span> <span data-ttu-id="122ed-110">Uma nova época começa quando ocorre uma alteração no nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="122ed-110">A new epoch starts when a domain name change occurs.</span></span>



| <span data-ttu-id="122ed-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="122ed-111">Entry</span></span> | <span data-ttu-id="122ed-112">Valor</span><span class="sxs-lookup"><span data-stu-id="122ed-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="122ed-113">CN</span><span class="sxs-lookup"><span data-stu-id="122ed-113">CN</span></span>                | <span data-ttu-id="122ed-114">ms-DS-ReplicationEpoch</span><span class="sxs-lookup"><span data-stu-id="122ed-114">ms-DS-ReplicationEpoch</span></span>               |
| <span data-ttu-id="122ed-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="122ed-115">Ldap-Display-Name</span></span> | <span data-ttu-id="122ed-116">msDS-ReplicationEpoch</span><span class="sxs-lookup"><span data-stu-id="122ed-116">msDS-ReplicationEpoch</span></span>                |
| <span data-ttu-id="122ed-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="122ed-117">Size</span></span>              | \-                                   |
| <span data-ttu-id="122ed-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="122ed-118">Update Privilege</span></span>  | <span data-ttu-id="122ed-119">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="122ed-119">This value is set by the system.</span></span>     |
| <span data-ttu-id="122ed-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="122ed-120">Update Frequency</span></span>  | <span data-ttu-id="122ed-121">Somente durante a reestruturação do domínio.</span><span class="sxs-lookup"><span data-stu-id="122ed-121">Only during domain restructure.</span></span>      |
| <span data-ttu-id="122ed-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="122ed-122">Attribute-Id</span></span>      | <span data-ttu-id="122ed-123">1.2.840.113556.1.4.1720</span><span class="sxs-lookup"><span data-stu-id="122ed-123">1.2.840.113556.1.4.1720</span></span>              |
| <span data-ttu-id="122ed-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="122ed-124">System-Id-Guid</span></span>    | <span data-ttu-id="122ed-125">08e3aa79-eb1c-45b5-af7b-8f94246c8e41</span><span class="sxs-lookup"><span data-stu-id="122ed-125">08e3aa79-eb1c-45b5-af7b-8f94246c8e41</span></span> |
| <span data-ttu-id="122ed-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="122ed-126">Syntax</span></span>            | [<span data-ttu-id="122ed-127">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="122ed-127">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="122ed-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="122ed-128">Implementations</span></span>

-   [<span data-ttu-id="122ed-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="122ed-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="122ed-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="122ed-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="122ed-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="122ed-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="122ed-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="122ed-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="122ed-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="122ed-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="122ed-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="122ed-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="122ed-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="122ed-135">Windows Server 2003</span></span>



| <span data-ttu-id="122ed-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="122ed-136">Entry</span></span> | <span data-ttu-id="122ed-137">Valor</span><span class="sxs-lookup"><span data-stu-id="122ed-137">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="122ed-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="122ed-138">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="122ed-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="122ed-139">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="122ed-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="122ed-140">System-Only</span></span>            | <span data-ttu-id="122ed-141">Falso</span><span class="sxs-lookup"><span data-stu-id="122ed-141">False</span></span>                                    |
| <span data-ttu-id="122ed-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="122ed-142">Is-Single-Valued</span></span>       | <span data-ttu-id="122ed-143">True</span><span class="sxs-lookup"><span data-stu-id="122ed-143">True</span></span>                                     |
| <span data-ttu-id="122ed-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="122ed-144">Is Indexed</span></span>             | <span data-ttu-id="122ed-145">Falso</span><span class="sxs-lookup"><span data-stu-id="122ed-145">False</span></span>                                    |
| <span data-ttu-id="122ed-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="122ed-146">In Global Catalog</span></span>      | <span data-ttu-id="122ed-147">Falso</span><span class="sxs-lookup"><span data-stu-id="122ed-147">False</span></span>                                    |
| <span data-ttu-id="122ed-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="122ed-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="122ed-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="122ed-149">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="122ed-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="122ed-150">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="122ed-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="122ed-151">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="122ed-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="122ed-152">Search-Flags</span></span>           | <span data-ttu-id="122ed-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="122ed-153">0x00000000</span></span>                               |
| <span data-ttu-id="122ed-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="122ed-154">System-Flags</span></span>           | <span data-ttu-id="122ed-155">0x00000011</span><span class="sxs-lookup"><span data-stu-id="122ed-155">0x00000011</span></span>                               |
| <span data-ttu-id="122ed-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="122ed-156">Classes used in</span></span>        | [<span data-ttu-id="122ed-157">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="122ed-157">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="122ed-158">ADAM</span><span class="sxs-lookup"><span data-stu-id="122ed-158">ADAM</span></span>



| <span data-ttu-id="122ed-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="122ed-159">Entry</span></span> | <span data-ttu-id="122ed-160">Valor</span><span class="sxs-lookup"><span data-stu-id="122ed-160">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="122ed-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="122ed-161">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="122ed-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="122ed-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="122ed-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="122ed-163">System-Only</span></span>            | <span data-ttu-id="122ed-164">Falso</span><span class="sxs-lookup"><span data-stu-id="122ed-164">False</span></span>                                    |
| <span data-ttu-id="122ed-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="122ed-165">Is-Single-Valued</span></span>       | <span data-ttu-id="122ed-166">True</span><span class="sxs-lookup"><span data-stu-id="122ed-166">True</span></span>                                     |
| <span data-ttu-id="122ed-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="122ed-167">Is Indexed</span></span>             | <span data-ttu-id="122ed-168">Falso</span><span class="sxs-lookup"><span data-stu-id="122ed-168">False</span></span>                                    |
| <span data-ttu-id="122ed-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="122ed-169">In Global Catalog</span></span>      | <span data-ttu-id="122ed-170">Falso</span><span class="sxs-lookup"><span data-stu-id="122ed-170">False</span></span>                                    |
| <span data-ttu-id="122ed-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="122ed-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="122ed-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="122ed-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="122ed-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="122ed-173">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="122ed-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="122ed-174">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="122ed-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="122ed-175">Search-Flags</span></span>           | <span data-ttu-id="122ed-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="122ed-176">0x00000000</span></span>                               |
| <span data-ttu-id="122ed-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="122ed-177">System-Flags</span></span>           | <span data-ttu-id="122ed-178">0x00000011</span><span class="sxs-lookup"><span data-stu-id="122ed-178">0x00000011</span></span>                               |
| <span data-ttu-id="122ed-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="122ed-179">Classes used in</span></span>        | [<span data-ttu-id="122ed-180">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="122ed-180">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="122ed-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="122ed-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="122ed-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="122ed-182">Entry</span></span> | <span data-ttu-id="122ed-183">Valor</span><span class="sxs-lookup"><span data-stu-id="122ed-183">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="122ed-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="122ed-184">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="122ed-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="122ed-185">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="122ed-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="122ed-186">System-Only</span></span>            | <span data-ttu-id="122ed-187">Falso</span><span class="sxs-lookup"><span data-stu-id="122ed-187">False</span></span>                                    |
| <span data-ttu-id="122ed-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="122ed-188">Is-Single-Valued</span></span>       | <span data-ttu-id="122ed-189">True</span><span class="sxs-lookup"><span data-stu-id="122ed-189">True</span></span>                                     |
| <span data-ttu-id="122ed-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="122ed-190">Is Indexed</span></span>             | <span data-ttu-id="122ed-191">Falso</span><span class="sxs-lookup"><span data-stu-id="122ed-191">False</span></span>                                    |
| <span data-ttu-id="122ed-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="122ed-192">In Global Catalog</span></span>      | <span data-ttu-id="122ed-193">Falso</span><span class="sxs-lookup"><span data-stu-id="122ed-193">False</span></span>                                    |
| <span data-ttu-id="122ed-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="122ed-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="122ed-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="122ed-195">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="122ed-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="122ed-196">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="122ed-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="122ed-197">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="122ed-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="122ed-198">Search-Flags</span></span>           | <span data-ttu-id="122ed-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="122ed-199">0x00000000</span></span>                               |
| <span data-ttu-id="122ed-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="122ed-200">System-Flags</span></span>           | <span data-ttu-id="122ed-201">0x00000011</span><span class="sxs-lookup"><span data-stu-id="122ed-201">0x00000011</span></span>                               |
| <span data-ttu-id="122ed-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="122ed-202">Classes used in</span></span>        | [<span data-ttu-id="122ed-203">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="122ed-203">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="122ed-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="122ed-204">Windows Server 2008</span></span>



| <span data-ttu-id="122ed-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="122ed-205">Entry</span></span> | <span data-ttu-id="122ed-206">Valor</span><span class="sxs-lookup"><span data-stu-id="122ed-206">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="122ed-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="122ed-207">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="122ed-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="122ed-208">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="122ed-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="122ed-209">System-Only</span></span>            | <span data-ttu-id="122ed-210">Falso</span><span class="sxs-lookup"><span data-stu-id="122ed-210">False</span></span>                                    |
| <span data-ttu-id="122ed-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="122ed-211">Is-Single-Valued</span></span>       | <span data-ttu-id="122ed-212">True</span><span class="sxs-lookup"><span data-stu-id="122ed-212">True</span></span>                                     |
| <span data-ttu-id="122ed-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="122ed-213">Is Indexed</span></span>             | <span data-ttu-id="122ed-214">Falso</span><span class="sxs-lookup"><span data-stu-id="122ed-214">False</span></span>                                    |
| <span data-ttu-id="122ed-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="122ed-215">In Global Catalog</span></span>      | <span data-ttu-id="122ed-216">Falso</span><span class="sxs-lookup"><span data-stu-id="122ed-216">False</span></span>                                    |
| <span data-ttu-id="122ed-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="122ed-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="122ed-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="122ed-218">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="122ed-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="122ed-219">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="122ed-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="122ed-220">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="122ed-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="122ed-221">Search-Flags</span></span>           | <span data-ttu-id="122ed-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="122ed-222">0x00000000</span></span>                               |
| <span data-ttu-id="122ed-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="122ed-223">System-Flags</span></span>           | <span data-ttu-id="122ed-224">0x00000011</span><span class="sxs-lookup"><span data-stu-id="122ed-224">0x00000011</span></span>                               |
| <span data-ttu-id="122ed-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="122ed-225">Classes used in</span></span>        | [<span data-ttu-id="122ed-226">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="122ed-226">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="122ed-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="122ed-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="122ed-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="122ed-228">Entry</span></span> | <span data-ttu-id="122ed-229">Valor</span><span class="sxs-lookup"><span data-stu-id="122ed-229">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="122ed-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="122ed-230">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="122ed-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="122ed-231">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="122ed-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="122ed-232">System-Only</span></span>            | <span data-ttu-id="122ed-233">Falso</span><span class="sxs-lookup"><span data-stu-id="122ed-233">False</span></span>                                    |
| <span data-ttu-id="122ed-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="122ed-234">Is-Single-Valued</span></span>       | <span data-ttu-id="122ed-235">True</span><span class="sxs-lookup"><span data-stu-id="122ed-235">True</span></span>                                     |
| <span data-ttu-id="122ed-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="122ed-236">Is Indexed</span></span>             | <span data-ttu-id="122ed-237">Falso</span><span class="sxs-lookup"><span data-stu-id="122ed-237">False</span></span>                                    |
| <span data-ttu-id="122ed-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="122ed-238">In Global Catalog</span></span>      | <span data-ttu-id="122ed-239">Falso</span><span class="sxs-lookup"><span data-stu-id="122ed-239">False</span></span>                                    |
| <span data-ttu-id="122ed-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="122ed-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="122ed-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="122ed-241">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="122ed-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="122ed-242">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="122ed-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="122ed-243">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="122ed-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="122ed-244">Search-Flags</span></span>           | <span data-ttu-id="122ed-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="122ed-245">0x00000000</span></span>                               |
| <span data-ttu-id="122ed-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="122ed-246">System-Flags</span></span>           | <span data-ttu-id="122ed-247">0x00000011</span><span class="sxs-lookup"><span data-stu-id="122ed-247">0x00000011</span></span>                               |
| <span data-ttu-id="122ed-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="122ed-248">Classes used in</span></span>        | [<span data-ttu-id="122ed-249">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="122ed-249">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="122ed-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="122ed-250">Windows Server 2012</span></span>



| <span data-ttu-id="122ed-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="122ed-251">Entry</span></span> | <span data-ttu-id="122ed-252">Valor</span><span class="sxs-lookup"><span data-stu-id="122ed-252">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="122ed-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="122ed-253">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="122ed-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="122ed-254">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="122ed-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="122ed-255">System-Only</span></span>            | <span data-ttu-id="122ed-256">Falso</span><span class="sxs-lookup"><span data-stu-id="122ed-256">False</span></span>                                    |
| <span data-ttu-id="122ed-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="122ed-257">Is-Single-Valued</span></span>       | <span data-ttu-id="122ed-258">True</span><span class="sxs-lookup"><span data-stu-id="122ed-258">True</span></span>                                     |
| <span data-ttu-id="122ed-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="122ed-259">Is Indexed</span></span>             | <span data-ttu-id="122ed-260">Falso</span><span class="sxs-lookup"><span data-stu-id="122ed-260">False</span></span>                                    |
| <span data-ttu-id="122ed-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="122ed-261">In Global Catalog</span></span>      | <span data-ttu-id="122ed-262">Falso</span><span class="sxs-lookup"><span data-stu-id="122ed-262">False</span></span>                                    |
| <span data-ttu-id="122ed-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="122ed-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="122ed-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="122ed-264">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="122ed-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="122ed-265">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="122ed-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="122ed-266">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="122ed-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="122ed-267">Search-Flags</span></span>           | <span data-ttu-id="122ed-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="122ed-268">0x00000000</span></span>                               |
| <span data-ttu-id="122ed-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="122ed-269">System-Flags</span></span>           | <span data-ttu-id="122ed-270">0x00000011</span><span class="sxs-lookup"><span data-stu-id="122ed-270">0x00000011</span></span>                               |
| <span data-ttu-id="122ed-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="122ed-271">Classes used in</span></span>        | [<span data-ttu-id="122ed-272">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="122ed-272">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





