---
title: Atributo FRS-réplica-set-type
description: Este é um código que indica se este é um conjunto de réplicas do SYSVOL, um conjunto de réplicas DFS ou outro conjunto de réplicas.
ms.assetid: 687a854f-ffa1-41f4-a515-5224759696ab
ms.tgt_platform: multiple
keywords:
- FRS-réplica-set-type atributo AD Schema
- Esquema de AD do atributo fRSReplicaSetType
topic_type:
- apiref
api_name:
- FRS-Replica-Set-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18046c9b4edb794687d275af52e35416419c7e2d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103824952"
---
# <a name="frs-replica-set-type-attribute"></a><span data-ttu-id="8805b-105">Atributo FRS-réplica-set-type</span><span class="sxs-lookup"><span data-stu-id="8805b-105">FRS-Replica-Set-Type attribute</span></span>

<span data-ttu-id="8805b-106">Este é um código que indica se este é um conjunto de réplicas do SYSVOL, um conjunto de réplicas DFS ou outro conjunto de réplicas.</span><span class="sxs-lookup"><span data-stu-id="8805b-106">This is a code that indicates whether this is a sysvol replica set, a DFS replica set, or other replica set.</span></span>



| <span data-ttu-id="8805b-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="8805b-107">Entry</span></span> | <span data-ttu-id="8805b-108">Valor</span><span class="sxs-lookup"><span data-stu-id="8805b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8805b-109">CN</span><span class="sxs-lookup"><span data-stu-id="8805b-109">CN</span></span>                | <span data-ttu-id="8805b-110">FRS-réplica-set-type</span><span class="sxs-lookup"><span data-stu-id="8805b-110">FRS-Replica-Set-Type</span></span>                 |
| <span data-ttu-id="8805b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8805b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8805b-112">fRSReplicaSetType</span><span class="sxs-lookup"><span data-stu-id="8805b-112">fRSReplicaSetType</span></span>                    |
| <span data-ttu-id="8805b-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="8805b-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="8805b-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="8805b-114">Update Privilege</span></span>  | <span data-ttu-id="8805b-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="8805b-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="8805b-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="8805b-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8805b-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8805b-117">Attribute-Id</span></span>      | <span data-ttu-id="8805b-118">1.2.840.113556.1.4.31</span><span class="sxs-lookup"><span data-stu-id="8805b-118">1.2.840.113556.1.4.31</span></span>                |
| <span data-ttu-id="8805b-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8805b-119">System-Id-Guid</span></span>    | <span data-ttu-id="8805b-120">26d9736b-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8805b-120">26d9736b-6070-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="8805b-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="8805b-121">Syntax</span></span>            | [<span data-ttu-id="8805b-122">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="8805b-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="8805b-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="8805b-123">Implementations</span></span>

-   [<span data-ttu-id="8805b-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8805b-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8805b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8805b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8805b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8805b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8805b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8805b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8805b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8805b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8805b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8805b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8805b-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8805b-130">Windows 2000 Server</span></span>



| <span data-ttu-id="8805b-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="8805b-131">Entry</span></span> | <span data-ttu-id="8805b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="8805b-132">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8805b-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="8805b-133">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8805b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8805b-134">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8805b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="8805b-135">System-Only</span></span>            | <span data-ttu-id="8805b-136">Falso</span><span class="sxs-lookup"><span data-stu-id="8805b-136">False</span></span>                                                     |
| <span data-ttu-id="8805b-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8805b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="8805b-138">True</span><span class="sxs-lookup"><span data-stu-id="8805b-138">True</span></span>                                                      |
| <span data-ttu-id="8805b-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="8805b-139">Is Indexed</span></span>             | <span data-ttu-id="8805b-140">Falso</span><span class="sxs-lookup"><span data-stu-id="8805b-140">False</span></span>                                                     |
| <span data-ttu-id="8805b-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8805b-141">In Global Catalog</span></span>      | <span data-ttu-id="8805b-142">Falso</span><span class="sxs-lookup"><span data-stu-id="8805b-142">False</span></span>                                                     |
| <span data-ttu-id="8805b-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8805b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="8805b-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8805b-144">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8805b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8805b-145">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8805b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8805b-146">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8805b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8805b-147">Search-Flags</span></span>           | <span data-ttu-id="8805b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8805b-148">0x00000000</span></span>                                                |
| <span data-ttu-id="8805b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8805b-149">System-Flags</span></span>           | <span data-ttu-id="8805b-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8805b-150">0x00000010</span></span>                                                |
| <span data-ttu-id="8805b-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8805b-151">Classes used in</span></span>        | [<span data-ttu-id="8805b-152">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="8805b-152">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8805b-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8805b-153">Windows Server 2003</span></span>



| <span data-ttu-id="8805b-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="8805b-154">Entry</span></span> | <span data-ttu-id="8805b-155">Valor</span><span class="sxs-lookup"><span data-stu-id="8805b-155">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8805b-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="8805b-156">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8805b-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8805b-157">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8805b-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="8805b-158">System-Only</span></span>            | <span data-ttu-id="8805b-159">Falso</span><span class="sxs-lookup"><span data-stu-id="8805b-159">False</span></span>                                                     |
| <span data-ttu-id="8805b-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8805b-160">Is-Single-Valued</span></span>       | <span data-ttu-id="8805b-161">True</span><span class="sxs-lookup"><span data-stu-id="8805b-161">True</span></span>                                                      |
| <span data-ttu-id="8805b-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="8805b-162">Is Indexed</span></span>             | <span data-ttu-id="8805b-163">Falso</span><span class="sxs-lookup"><span data-stu-id="8805b-163">False</span></span>                                                     |
| <span data-ttu-id="8805b-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8805b-164">In Global Catalog</span></span>      | <span data-ttu-id="8805b-165">Falso</span><span class="sxs-lookup"><span data-stu-id="8805b-165">False</span></span>                                                     |
| <span data-ttu-id="8805b-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8805b-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="8805b-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8805b-167">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8805b-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8805b-168">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8805b-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8805b-169">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8805b-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8805b-170">Search-Flags</span></span>           | <span data-ttu-id="8805b-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8805b-171">0x00000000</span></span>                                                |
| <span data-ttu-id="8805b-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8805b-172">System-Flags</span></span>           | <span data-ttu-id="8805b-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8805b-173">0x00000010</span></span>                                                |
| <span data-ttu-id="8805b-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8805b-174">Classes used in</span></span>        | [<span data-ttu-id="8805b-175">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="8805b-175">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8805b-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8805b-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8805b-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="8805b-177">Entry</span></span> | <span data-ttu-id="8805b-178">Valor</span><span class="sxs-lookup"><span data-stu-id="8805b-178">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8805b-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="8805b-179">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8805b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8805b-180">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8805b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="8805b-181">System-Only</span></span>            | <span data-ttu-id="8805b-182">Falso</span><span class="sxs-lookup"><span data-stu-id="8805b-182">False</span></span>                                                     |
| <span data-ttu-id="8805b-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8805b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="8805b-184">True</span><span class="sxs-lookup"><span data-stu-id="8805b-184">True</span></span>                                                      |
| <span data-ttu-id="8805b-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="8805b-185">Is Indexed</span></span>             | <span data-ttu-id="8805b-186">Falso</span><span class="sxs-lookup"><span data-stu-id="8805b-186">False</span></span>                                                     |
| <span data-ttu-id="8805b-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8805b-187">In Global Catalog</span></span>      | <span data-ttu-id="8805b-188">Falso</span><span class="sxs-lookup"><span data-stu-id="8805b-188">False</span></span>                                                     |
| <span data-ttu-id="8805b-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8805b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="8805b-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8805b-190">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8805b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8805b-191">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8805b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8805b-192">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8805b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8805b-193">Search-Flags</span></span>           | <span data-ttu-id="8805b-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8805b-194">0x00000000</span></span>                                                |
| <span data-ttu-id="8805b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8805b-195">System-Flags</span></span>           | <span data-ttu-id="8805b-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8805b-196">0x00000010</span></span>                                                |
| <span data-ttu-id="8805b-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8805b-197">Classes used in</span></span>        | [<span data-ttu-id="8805b-198">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="8805b-198">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8805b-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8805b-199">Windows Server 2008</span></span>



| <span data-ttu-id="8805b-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="8805b-200">Entry</span></span> | <span data-ttu-id="8805b-201">Valor</span><span class="sxs-lookup"><span data-stu-id="8805b-201">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8805b-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="8805b-202">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8805b-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8805b-203">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8805b-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="8805b-204">System-Only</span></span>            | <span data-ttu-id="8805b-205">Falso</span><span class="sxs-lookup"><span data-stu-id="8805b-205">False</span></span>                                                     |
| <span data-ttu-id="8805b-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8805b-206">Is-Single-Valued</span></span>       | <span data-ttu-id="8805b-207">True</span><span class="sxs-lookup"><span data-stu-id="8805b-207">True</span></span>                                                      |
| <span data-ttu-id="8805b-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="8805b-208">Is Indexed</span></span>             | <span data-ttu-id="8805b-209">Falso</span><span class="sxs-lookup"><span data-stu-id="8805b-209">False</span></span>                                                     |
| <span data-ttu-id="8805b-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8805b-210">In Global Catalog</span></span>      | <span data-ttu-id="8805b-211">Falso</span><span class="sxs-lookup"><span data-stu-id="8805b-211">False</span></span>                                                     |
| <span data-ttu-id="8805b-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8805b-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="8805b-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8805b-213">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8805b-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8805b-214">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8805b-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8805b-215">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8805b-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8805b-216">Search-Flags</span></span>           | <span data-ttu-id="8805b-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8805b-217">0x00000000</span></span>                                                |
| <span data-ttu-id="8805b-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8805b-218">System-Flags</span></span>           | <span data-ttu-id="8805b-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8805b-219">0x00000010</span></span>                                                |
| <span data-ttu-id="8805b-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8805b-220">Classes used in</span></span>        | [<span data-ttu-id="8805b-221">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="8805b-221">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8805b-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8805b-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8805b-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="8805b-223">Entry</span></span> | <span data-ttu-id="8805b-224">Valor</span><span class="sxs-lookup"><span data-stu-id="8805b-224">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8805b-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="8805b-225">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8805b-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8805b-226">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8805b-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="8805b-227">System-Only</span></span>            | <span data-ttu-id="8805b-228">Falso</span><span class="sxs-lookup"><span data-stu-id="8805b-228">False</span></span>                                                     |
| <span data-ttu-id="8805b-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8805b-229">Is-Single-Valued</span></span>       | <span data-ttu-id="8805b-230">True</span><span class="sxs-lookup"><span data-stu-id="8805b-230">True</span></span>                                                      |
| <span data-ttu-id="8805b-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="8805b-231">Is Indexed</span></span>             | <span data-ttu-id="8805b-232">Falso</span><span class="sxs-lookup"><span data-stu-id="8805b-232">False</span></span>                                                     |
| <span data-ttu-id="8805b-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8805b-233">In Global Catalog</span></span>      | <span data-ttu-id="8805b-234">Falso</span><span class="sxs-lookup"><span data-stu-id="8805b-234">False</span></span>                                                     |
| <span data-ttu-id="8805b-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8805b-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="8805b-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8805b-236">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8805b-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8805b-237">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8805b-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8805b-238">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8805b-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8805b-239">Search-Flags</span></span>           | <span data-ttu-id="8805b-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8805b-240">0x00000000</span></span>                                                |
| <span data-ttu-id="8805b-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8805b-241">System-Flags</span></span>           | <span data-ttu-id="8805b-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8805b-242">0x00000010</span></span>                                                |
| <span data-ttu-id="8805b-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8805b-243">Classes used in</span></span>        | [<span data-ttu-id="8805b-244">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="8805b-244">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8805b-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8805b-245">Windows Server 2012</span></span>



| <span data-ttu-id="8805b-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="8805b-246">Entry</span></span> | <span data-ttu-id="8805b-247">Valor</span><span class="sxs-lookup"><span data-stu-id="8805b-247">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8805b-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="8805b-248">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8805b-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8805b-249">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8805b-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="8805b-250">System-Only</span></span>            | <span data-ttu-id="8805b-251">Falso</span><span class="sxs-lookup"><span data-stu-id="8805b-251">False</span></span>                                                     |
| <span data-ttu-id="8805b-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8805b-252">Is-Single-Valued</span></span>       | <span data-ttu-id="8805b-253">True</span><span class="sxs-lookup"><span data-stu-id="8805b-253">True</span></span>                                                      |
| <span data-ttu-id="8805b-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="8805b-254">Is Indexed</span></span>             | <span data-ttu-id="8805b-255">Falso</span><span class="sxs-lookup"><span data-stu-id="8805b-255">False</span></span>                                                     |
| <span data-ttu-id="8805b-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8805b-256">In Global Catalog</span></span>      | <span data-ttu-id="8805b-257">Falso</span><span class="sxs-lookup"><span data-stu-id="8805b-257">False</span></span>                                                     |
| <span data-ttu-id="8805b-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8805b-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="8805b-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8805b-259">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8805b-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8805b-260">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8805b-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8805b-261">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8805b-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8805b-262">Search-Flags</span></span>           | <span data-ttu-id="8805b-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8805b-263">0x00000000</span></span>                                                |
| <span data-ttu-id="8805b-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8805b-264">System-Flags</span></span>           | <span data-ttu-id="8805b-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8805b-265">0x00000010</span></span>                                                |
| <span data-ttu-id="8805b-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8805b-266">Classes used in</span></span>        | [<span data-ttu-id="8805b-267">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="8805b-267">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





