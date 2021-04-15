---
title: Atributo FRS-Version-GUID
description: Se houver, a alteração desse valor indicará que uma alteração de configuração foi feita nesse conjunto de réplicas.
ms.assetid: 27cd68c5-a8aa-4c14-bf1d-0eb7c4d9cca5
ms.tgt_platform: multiple
keywords:
- FRS-Version-GUID de atributo do AD Schema
- Esquema de AD do atributo fRSVersionGUID
topic_type:
- apiref
api_name:
- FRS-Version-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f12cfadd1086fbb8ee79bafb8d0ee5f947ff503e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104500018"
---
# <a name="frs-version-guid-attribute"></a><span data-ttu-id="f47ec-105">Atributo FRS-Version-GUID</span><span class="sxs-lookup"><span data-stu-id="f47ec-105">FRS-Version-GUID attribute</span></span>

<span data-ttu-id="f47ec-106">Se houver, a alteração desse valor indicará que uma alteração de configuração foi feita nesse conjunto de réplicas.</span><span class="sxs-lookup"><span data-stu-id="f47ec-106">If present, changing this value indicates a configuration change has been made on this replica set.</span></span>



| <span data-ttu-id="f47ec-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f47ec-107">Entry</span></span> | <span data-ttu-id="f47ec-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f47ec-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="f47ec-109">CN</span><span class="sxs-lookup"><span data-stu-id="f47ec-109">CN</span></span>                | <span data-ttu-id="f47ec-110">FRS-Version-GUID</span><span class="sxs-lookup"><span data-stu-id="f47ec-110">FRS-Version-GUID</span></span>                                      |
| <span data-ttu-id="f47ec-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f47ec-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f47ec-112">fRSVersionGUID</span><span class="sxs-lookup"><span data-stu-id="f47ec-112">fRSVersionGUID</span></span>                                        |
| <span data-ttu-id="f47ec-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f47ec-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="f47ec-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f47ec-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="f47ec-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f47ec-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="f47ec-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f47ec-116">Attribute-Id</span></span>      | <span data-ttu-id="f47ec-117">1.2.840.113556.1.4.43</span><span class="sxs-lookup"><span data-stu-id="f47ec-117">1.2.840.113556.1.4.43</span></span>                                 |
| <span data-ttu-id="f47ec-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f47ec-118">System-Id-Guid</span></span>    | <span data-ttu-id="f47ec-119">26d9736c-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="f47ec-119">26d9736c-6070-11d1-a9c6-0000f80367c1</span></span>                  |
| <span data-ttu-id="f47ec-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="f47ec-120">Syntax</span></span>            | [<span data-ttu-id="f47ec-121">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="f47ec-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="f47ec-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="f47ec-122">Implementations</span></span>

-   [<span data-ttu-id="f47ec-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f47ec-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f47ec-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f47ec-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f47ec-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f47ec-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f47ec-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f47ec-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f47ec-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f47ec-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f47ec-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f47ec-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f47ec-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f47ec-129">Windows 2000 Server</span></span>



| <span data-ttu-id="f47ec-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="f47ec-130">Entry</span></span> | <span data-ttu-id="f47ec-131">Valor</span><span class="sxs-lookup"><span data-stu-id="f47ec-131">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f47ec-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="f47ec-132">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f47ec-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f47ec-133">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f47ec-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f47ec-134">System-Only</span></span>            | <span data-ttu-id="f47ec-135">Falso</span><span class="sxs-lookup"><span data-stu-id="f47ec-135">False</span></span>                                                     |
| <span data-ttu-id="f47ec-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f47ec-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f47ec-137">True</span><span class="sxs-lookup"><span data-stu-id="f47ec-137">True</span></span>                                                      |
| <span data-ttu-id="f47ec-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="f47ec-138">Is Indexed</span></span>             | <span data-ttu-id="f47ec-139">Falso</span><span class="sxs-lookup"><span data-stu-id="f47ec-139">False</span></span>                                                     |
| <span data-ttu-id="f47ec-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f47ec-140">In Global Catalog</span></span>      | <span data-ttu-id="f47ec-141">Falso</span><span class="sxs-lookup"><span data-stu-id="f47ec-141">False</span></span>                                                     |
| <span data-ttu-id="f47ec-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f47ec-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f47ec-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f47ec-143">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f47ec-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f47ec-144">Range-Lower</span></span>            | <span data-ttu-id="f47ec-145">16</span><span class="sxs-lookup"><span data-stu-id="f47ec-145">16</span></span>                                                        |
| <span data-ttu-id="f47ec-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f47ec-146">Range-Upper</span></span>            | <span data-ttu-id="f47ec-147">16</span><span class="sxs-lookup"><span data-stu-id="f47ec-147">16</span></span>                                                        |
| <span data-ttu-id="f47ec-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f47ec-148">Search-Flags</span></span>           | <span data-ttu-id="f47ec-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f47ec-149">0x00000000</span></span>                                                |
| <span data-ttu-id="f47ec-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f47ec-150">System-Flags</span></span>           | <span data-ttu-id="f47ec-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f47ec-151">0x00000010</span></span>                                                |
| <span data-ttu-id="f47ec-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f47ec-152">Classes used in</span></span>        | [<span data-ttu-id="f47ec-153">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="f47ec-153">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f47ec-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f47ec-154">Windows Server 2003</span></span>



| <span data-ttu-id="f47ec-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="f47ec-155">Entry</span></span> | <span data-ttu-id="f47ec-156">Valor</span><span class="sxs-lookup"><span data-stu-id="f47ec-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f47ec-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="f47ec-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f47ec-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f47ec-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f47ec-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="f47ec-159">System-Only</span></span>            | <span data-ttu-id="f47ec-160">Falso</span><span class="sxs-lookup"><span data-stu-id="f47ec-160">False</span></span>                                                     |
| <span data-ttu-id="f47ec-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f47ec-161">Is-Single-Valued</span></span>       | <span data-ttu-id="f47ec-162">True</span><span class="sxs-lookup"><span data-stu-id="f47ec-162">True</span></span>                                                      |
| <span data-ttu-id="f47ec-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="f47ec-163">Is Indexed</span></span>             | <span data-ttu-id="f47ec-164">Falso</span><span class="sxs-lookup"><span data-stu-id="f47ec-164">False</span></span>                                                     |
| <span data-ttu-id="f47ec-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f47ec-165">In Global Catalog</span></span>      | <span data-ttu-id="f47ec-166">Falso</span><span class="sxs-lookup"><span data-stu-id="f47ec-166">False</span></span>                                                     |
| <span data-ttu-id="f47ec-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f47ec-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="f47ec-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f47ec-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f47ec-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f47ec-169">Range-Lower</span></span>            | <span data-ttu-id="f47ec-170">16</span><span class="sxs-lookup"><span data-stu-id="f47ec-170">16</span></span>                                                        |
| <span data-ttu-id="f47ec-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f47ec-171">Range-Upper</span></span>            | <span data-ttu-id="f47ec-172">16</span><span class="sxs-lookup"><span data-stu-id="f47ec-172">16</span></span>                                                        |
| <span data-ttu-id="f47ec-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f47ec-173">Search-Flags</span></span>           | <span data-ttu-id="f47ec-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f47ec-174">0x00000000</span></span>                                                |
| <span data-ttu-id="f47ec-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f47ec-175">System-Flags</span></span>           | <span data-ttu-id="f47ec-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f47ec-176">0x00000010</span></span>                                                |
| <span data-ttu-id="f47ec-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f47ec-177">Classes used in</span></span>        | [<span data-ttu-id="f47ec-178">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="f47ec-178">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f47ec-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f47ec-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f47ec-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="f47ec-180">Entry</span></span> | <span data-ttu-id="f47ec-181">Valor</span><span class="sxs-lookup"><span data-stu-id="f47ec-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f47ec-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="f47ec-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f47ec-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f47ec-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f47ec-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="f47ec-184">System-Only</span></span>            | <span data-ttu-id="f47ec-185">Falso</span><span class="sxs-lookup"><span data-stu-id="f47ec-185">False</span></span>                                                     |
| <span data-ttu-id="f47ec-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f47ec-186">Is-Single-Valued</span></span>       | <span data-ttu-id="f47ec-187">True</span><span class="sxs-lookup"><span data-stu-id="f47ec-187">True</span></span>                                                      |
| <span data-ttu-id="f47ec-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="f47ec-188">Is Indexed</span></span>             | <span data-ttu-id="f47ec-189">Falso</span><span class="sxs-lookup"><span data-stu-id="f47ec-189">False</span></span>                                                     |
| <span data-ttu-id="f47ec-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f47ec-190">In Global Catalog</span></span>      | <span data-ttu-id="f47ec-191">Falso</span><span class="sxs-lookup"><span data-stu-id="f47ec-191">False</span></span>                                                     |
| <span data-ttu-id="f47ec-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f47ec-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="f47ec-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f47ec-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f47ec-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f47ec-194">Range-Lower</span></span>            | <span data-ttu-id="f47ec-195">16</span><span class="sxs-lookup"><span data-stu-id="f47ec-195">16</span></span>                                                        |
| <span data-ttu-id="f47ec-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f47ec-196">Range-Upper</span></span>            | <span data-ttu-id="f47ec-197">16</span><span class="sxs-lookup"><span data-stu-id="f47ec-197">16</span></span>                                                        |
| <span data-ttu-id="f47ec-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f47ec-198">Search-Flags</span></span>           | <span data-ttu-id="f47ec-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f47ec-199">0x00000000</span></span>                                                |
| <span data-ttu-id="f47ec-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f47ec-200">System-Flags</span></span>           | <span data-ttu-id="f47ec-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f47ec-201">0x00000010</span></span>                                                |
| <span data-ttu-id="f47ec-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f47ec-202">Classes used in</span></span>        | [<span data-ttu-id="f47ec-203">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="f47ec-203">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f47ec-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f47ec-204">Windows Server 2008</span></span>



| <span data-ttu-id="f47ec-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="f47ec-205">Entry</span></span> | <span data-ttu-id="f47ec-206">Valor</span><span class="sxs-lookup"><span data-stu-id="f47ec-206">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f47ec-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="f47ec-207">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f47ec-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f47ec-208">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f47ec-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="f47ec-209">System-Only</span></span>            | <span data-ttu-id="f47ec-210">Falso</span><span class="sxs-lookup"><span data-stu-id="f47ec-210">False</span></span>                                                     |
| <span data-ttu-id="f47ec-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f47ec-211">Is-Single-Valued</span></span>       | <span data-ttu-id="f47ec-212">True</span><span class="sxs-lookup"><span data-stu-id="f47ec-212">True</span></span>                                                      |
| <span data-ttu-id="f47ec-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="f47ec-213">Is Indexed</span></span>             | <span data-ttu-id="f47ec-214">Falso</span><span class="sxs-lookup"><span data-stu-id="f47ec-214">False</span></span>                                                     |
| <span data-ttu-id="f47ec-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f47ec-215">In Global Catalog</span></span>      | <span data-ttu-id="f47ec-216">Falso</span><span class="sxs-lookup"><span data-stu-id="f47ec-216">False</span></span>                                                     |
| <span data-ttu-id="f47ec-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f47ec-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="f47ec-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f47ec-218">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f47ec-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f47ec-219">Range-Lower</span></span>            | <span data-ttu-id="f47ec-220">16</span><span class="sxs-lookup"><span data-stu-id="f47ec-220">16</span></span>                                                        |
| <span data-ttu-id="f47ec-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f47ec-221">Range-Upper</span></span>            | <span data-ttu-id="f47ec-222">16</span><span class="sxs-lookup"><span data-stu-id="f47ec-222">16</span></span>                                                        |
| <span data-ttu-id="f47ec-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f47ec-223">Search-Flags</span></span>           | <span data-ttu-id="f47ec-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f47ec-224">0x00000000</span></span>                                                |
| <span data-ttu-id="f47ec-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f47ec-225">System-Flags</span></span>           | <span data-ttu-id="f47ec-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f47ec-226">0x00000010</span></span>                                                |
| <span data-ttu-id="f47ec-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f47ec-227">Classes used in</span></span>        | [<span data-ttu-id="f47ec-228">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="f47ec-228">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f47ec-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f47ec-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f47ec-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="f47ec-230">Entry</span></span> | <span data-ttu-id="f47ec-231">Valor</span><span class="sxs-lookup"><span data-stu-id="f47ec-231">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f47ec-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="f47ec-232">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f47ec-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f47ec-233">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f47ec-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="f47ec-234">System-Only</span></span>            | <span data-ttu-id="f47ec-235">Falso</span><span class="sxs-lookup"><span data-stu-id="f47ec-235">False</span></span>                                                     |
| <span data-ttu-id="f47ec-236">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f47ec-236">Is-Single-Valued</span></span>       | <span data-ttu-id="f47ec-237">True</span><span class="sxs-lookup"><span data-stu-id="f47ec-237">True</span></span>                                                      |
| <span data-ttu-id="f47ec-238">É indexado</span><span class="sxs-lookup"><span data-stu-id="f47ec-238">Is Indexed</span></span>             | <span data-ttu-id="f47ec-239">Falso</span><span class="sxs-lookup"><span data-stu-id="f47ec-239">False</span></span>                                                     |
| <span data-ttu-id="f47ec-240">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f47ec-240">In Global Catalog</span></span>      | <span data-ttu-id="f47ec-241">Falso</span><span class="sxs-lookup"><span data-stu-id="f47ec-241">False</span></span>                                                     |
| <span data-ttu-id="f47ec-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f47ec-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="f47ec-243">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f47ec-243">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f47ec-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f47ec-244">Range-Lower</span></span>            | <span data-ttu-id="f47ec-245">16</span><span class="sxs-lookup"><span data-stu-id="f47ec-245">16</span></span>                                                        |
| <span data-ttu-id="f47ec-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f47ec-246">Range-Upper</span></span>            | <span data-ttu-id="f47ec-247">16</span><span class="sxs-lookup"><span data-stu-id="f47ec-247">16</span></span>                                                        |
| <span data-ttu-id="f47ec-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f47ec-248">Search-Flags</span></span>           | <span data-ttu-id="f47ec-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f47ec-249">0x00000000</span></span>                                                |
| <span data-ttu-id="f47ec-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f47ec-250">System-Flags</span></span>           | <span data-ttu-id="f47ec-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f47ec-251">0x00000010</span></span>                                                |
| <span data-ttu-id="f47ec-252">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f47ec-252">Classes used in</span></span>        | [<span data-ttu-id="f47ec-253">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="f47ec-253">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f47ec-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f47ec-254">Windows Server 2012</span></span>



| <span data-ttu-id="f47ec-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="f47ec-255">Entry</span></span> | <span data-ttu-id="f47ec-256">Valor</span><span class="sxs-lookup"><span data-stu-id="f47ec-256">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f47ec-257">ID do link</span><span class="sxs-lookup"><span data-stu-id="f47ec-257">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f47ec-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f47ec-258">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f47ec-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="f47ec-259">System-Only</span></span>            | <span data-ttu-id="f47ec-260">Falso</span><span class="sxs-lookup"><span data-stu-id="f47ec-260">False</span></span>                                                     |
| <span data-ttu-id="f47ec-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f47ec-261">Is-Single-Valued</span></span>       | <span data-ttu-id="f47ec-262">True</span><span class="sxs-lookup"><span data-stu-id="f47ec-262">True</span></span>                                                      |
| <span data-ttu-id="f47ec-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="f47ec-263">Is Indexed</span></span>             | <span data-ttu-id="f47ec-264">Falso</span><span class="sxs-lookup"><span data-stu-id="f47ec-264">False</span></span>                                                     |
| <span data-ttu-id="f47ec-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f47ec-265">In Global Catalog</span></span>      | <span data-ttu-id="f47ec-266">Falso</span><span class="sxs-lookup"><span data-stu-id="f47ec-266">False</span></span>                                                     |
| <span data-ttu-id="f47ec-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f47ec-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="f47ec-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f47ec-268">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f47ec-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f47ec-269">Range-Lower</span></span>            | <span data-ttu-id="f47ec-270">16</span><span class="sxs-lookup"><span data-stu-id="f47ec-270">16</span></span>                                                        |
| <span data-ttu-id="f47ec-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f47ec-271">Range-Upper</span></span>            | <span data-ttu-id="f47ec-272">16</span><span class="sxs-lookup"><span data-stu-id="f47ec-272">16</span></span>                                                        |
| <span data-ttu-id="f47ec-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f47ec-273">Search-Flags</span></span>           | <span data-ttu-id="f47ec-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f47ec-274">0x00000000</span></span>                                                |
| <span data-ttu-id="f47ec-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f47ec-275">System-Flags</span></span>           | <span data-ttu-id="f47ec-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f47ec-276">0x00000010</span></span>                                                |
| <span data-ttu-id="f47ec-277">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f47ec-277">Classes used in</span></span>        | [<span data-ttu-id="f47ec-278">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="f47ec-278">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





