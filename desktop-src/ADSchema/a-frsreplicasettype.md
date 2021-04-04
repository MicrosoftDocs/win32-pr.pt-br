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
# <a name="frs-replica-set-type-attribute"></a><span data-ttu-id="48f6f-105">Atributo FRS-réplica-set-type</span><span class="sxs-lookup"><span data-stu-id="48f6f-105">FRS-Replica-Set-Type attribute</span></span>

<span data-ttu-id="48f6f-106">Este é um código que indica se este é um conjunto de réplicas do SYSVOL, um conjunto de réplicas DFS ou outro conjunto de réplicas.</span><span class="sxs-lookup"><span data-stu-id="48f6f-106">This is a code that indicates whether this is a sysvol replica set, a DFS replica set, or other replica set.</span></span>



| <span data-ttu-id="48f6f-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="48f6f-107">Entry</span></span> | <span data-ttu-id="48f6f-108">Valor</span><span class="sxs-lookup"><span data-stu-id="48f6f-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="48f6f-109">CN</span><span class="sxs-lookup"><span data-stu-id="48f6f-109">CN</span></span>                | <span data-ttu-id="48f6f-110">FRS-réplica-set-type</span><span class="sxs-lookup"><span data-stu-id="48f6f-110">FRS-Replica-Set-Type</span></span>                 |
| <span data-ttu-id="48f6f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="48f6f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="48f6f-112">fRSReplicaSetType</span><span class="sxs-lookup"><span data-stu-id="48f6f-112">fRSReplicaSetType</span></span>                    |
| <span data-ttu-id="48f6f-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="48f6f-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="48f6f-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="48f6f-114">Update Privilege</span></span>  | <span data-ttu-id="48f6f-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="48f6f-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="48f6f-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="48f6f-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="48f6f-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="48f6f-117">Attribute-Id</span></span>      | <span data-ttu-id="48f6f-118">1.2.840.113556.1.4.31</span><span class="sxs-lookup"><span data-stu-id="48f6f-118">1.2.840.113556.1.4.31</span></span>                |
| <span data-ttu-id="48f6f-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="48f6f-119">System-Id-Guid</span></span>    | <span data-ttu-id="48f6f-120">26d9736b-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="48f6f-120">26d9736b-6070-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="48f6f-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="48f6f-121">Syntax</span></span>            | [<span data-ttu-id="48f6f-122">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="48f6f-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="48f6f-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="48f6f-123">Implementations</span></span>

-   [<span data-ttu-id="48f6f-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="48f6f-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="48f6f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="48f6f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="48f6f-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="48f6f-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="48f6f-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="48f6f-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="48f6f-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="48f6f-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="48f6f-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="48f6f-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="48f6f-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="48f6f-130">Windows 2000 Server</span></span>



| <span data-ttu-id="48f6f-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="48f6f-131">Entry</span></span> | <span data-ttu-id="48f6f-132">Valor</span><span class="sxs-lookup"><span data-stu-id="48f6f-132">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="48f6f-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="48f6f-133">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="48f6f-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48f6f-134">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="48f6f-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="48f6f-135">System-Only</span></span>            | <span data-ttu-id="48f6f-136">Falso</span><span class="sxs-lookup"><span data-stu-id="48f6f-136">False</span></span>                                                     |
| <span data-ttu-id="48f6f-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="48f6f-137">Is-Single-Valued</span></span>       | <span data-ttu-id="48f6f-138">True</span><span class="sxs-lookup"><span data-stu-id="48f6f-138">True</span></span>                                                      |
| <span data-ttu-id="48f6f-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="48f6f-139">Is Indexed</span></span>             | <span data-ttu-id="48f6f-140">Falso</span><span class="sxs-lookup"><span data-stu-id="48f6f-140">False</span></span>                                                     |
| <span data-ttu-id="48f6f-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="48f6f-141">In Global Catalog</span></span>      | <span data-ttu-id="48f6f-142">Falso</span><span class="sxs-lookup"><span data-stu-id="48f6f-142">False</span></span>                                                     |
| <span data-ttu-id="48f6f-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="48f6f-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="48f6f-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="48f6f-144">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="48f6f-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48f6f-145">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="48f6f-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48f6f-146">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="48f6f-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48f6f-147">Search-Flags</span></span>           | <span data-ttu-id="48f6f-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48f6f-148">0x00000000</span></span>                                                |
| <span data-ttu-id="48f6f-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48f6f-149">System-Flags</span></span>           | <span data-ttu-id="48f6f-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48f6f-150">0x00000010</span></span>                                                |
| <span data-ttu-id="48f6f-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="48f6f-151">Classes used in</span></span>        | [<span data-ttu-id="48f6f-152">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="48f6f-152">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="48f6f-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="48f6f-153">Windows Server 2003</span></span>



| <span data-ttu-id="48f6f-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="48f6f-154">Entry</span></span> | <span data-ttu-id="48f6f-155">Valor</span><span class="sxs-lookup"><span data-stu-id="48f6f-155">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="48f6f-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="48f6f-156">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="48f6f-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48f6f-157">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="48f6f-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="48f6f-158">System-Only</span></span>            | <span data-ttu-id="48f6f-159">Falso</span><span class="sxs-lookup"><span data-stu-id="48f6f-159">False</span></span>                                                     |
| <span data-ttu-id="48f6f-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="48f6f-160">Is-Single-Valued</span></span>       | <span data-ttu-id="48f6f-161">True</span><span class="sxs-lookup"><span data-stu-id="48f6f-161">True</span></span>                                                      |
| <span data-ttu-id="48f6f-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="48f6f-162">Is Indexed</span></span>             | <span data-ttu-id="48f6f-163">Falso</span><span class="sxs-lookup"><span data-stu-id="48f6f-163">False</span></span>                                                     |
| <span data-ttu-id="48f6f-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="48f6f-164">In Global Catalog</span></span>      | <span data-ttu-id="48f6f-165">Falso</span><span class="sxs-lookup"><span data-stu-id="48f6f-165">False</span></span>                                                     |
| <span data-ttu-id="48f6f-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="48f6f-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="48f6f-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="48f6f-167">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="48f6f-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48f6f-168">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="48f6f-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48f6f-169">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="48f6f-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48f6f-170">Search-Flags</span></span>           | <span data-ttu-id="48f6f-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48f6f-171">0x00000000</span></span>                                                |
| <span data-ttu-id="48f6f-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48f6f-172">System-Flags</span></span>           | <span data-ttu-id="48f6f-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48f6f-173">0x00000010</span></span>                                                |
| <span data-ttu-id="48f6f-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="48f6f-174">Classes used in</span></span>        | [<span data-ttu-id="48f6f-175">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="48f6f-175">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="48f6f-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="48f6f-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="48f6f-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="48f6f-177">Entry</span></span> | <span data-ttu-id="48f6f-178">Valor</span><span class="sxs-lookup"><span data-stu-id="48f6f-178">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="48f6f-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="48f6f-179">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="48f6f-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48f6f-180">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="48f6f-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="48f6f-181">System-Only</span></span>            | <span data-ttu-id="48f6f-182">Falso</span><span class="sxs-lookup"><span data-stu-id="48f6f-182">False</span></span>                                                     |
| <span data-ttu-id="48f6f-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="48f6f-183">Is-Single-Valued</span></span>       | <span data-ttu-id="48f6f-184">True</span><span class="sxs-lookup"><span data-stu-id="48f6f-184">True</span></span>                                                      |
| <span data-ttu-id="48f6f-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="48f6f-185">Is Indexed</span></span>             | <span data-ttu-id="48f6f-186">Falso</span><span class="sxs-lookup"><span data-stu-id="48f6f-186">False</span></span>                                                     |
| <span data-ttu-id="48f6f-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="48f6f-187">In Global Catalog</span></span>      | <span data-ttu-id="48f6f-188">Falso</span><span class="sxs-lookup"><span data-stu-id="48f6f-188">False</span></span>                                                     |
| <span data-ttu-id="48f6f-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="48f6f-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="48f6f-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="48f6f-190">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="48f6f-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48f6f-191">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="48f6f-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48f6f-192">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="48f6f-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48f6f-193">Search-Flags</span></span>           | <span data-ttu-id="48f6f-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48f6f-194">0x00000000</span></span>                                                |
| <span data-ttu-id="48f6f-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48f6f-195">System-Flags</span></span>           | <span data-ttu-id="48f6f-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48f6f-196">0x00000010</span></span>                                                |
| <span data-ttu-id="48f6f-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="48f6f-197">Classes used in</span></span>        | [<span data-ttu-id="48f6f-198">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="48f6f-198">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="48f6f-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48f6f-199">Windows Server 2008</span></span>



| <span data-ttu-id="48f6f-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="48f6f-200">Entry</span></span> | <span data-ttu-id="48f6f-201">Valor</span><span class="sxs-lookup"><span data-stu-id="48f6f-201">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="48f6f-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="48f6f-202">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="48f6f-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48f6f-203">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="48f6f-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="48f6f-204">System-Only</span></span>            | <span data-ttu-id="48f6f-205">Falso</span><span class="sxs-lookup"><span data-stu-id="48f6f-205">False</span></span>                                                     |
| <span data-ttu-id="48f6f-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="48f6f-206">Is-Single-Valued</span></span>       | <span data-ttu-id="48f6f-207">True</span><span class="sxs-lookup"><span data-stu-id="48f6f-207">True</span></span>                                                      |
| <span data-ttu-id="48f6f-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="48f6f-208">Is Indexed</span></span>             | <span data-ttu-id="48f6f-209">Falso</span><span class="sxs-lookup"><span data-stu-id="48f6f-209">False</span></span>                                                     |
| <span data-ttu-id="48f6f-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="48f6f-210">In Global Catalog</span></span>      | <span data-ttu-id="48f6f-211">Falso</span><span class="sxs-lookup"><span data-stu-id="48f6f-211">False</span></span>                                                     |
| <span data-ttu-id="48f6f-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="48f6f-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="48f6f-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="48f6f-213">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="48f6f-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48f6f-214">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="48f6f-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48f6f-215">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="48f6f-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48f6f-216">Search-Flags</span></span>           | <span data-ttu-id="48f6f-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48f6f-217">0x00000000</span></span>                                                |
| <span data-ttu-id="48f6f-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48f6f-218">System-Flags</span></span>           | <span data-ttu-id="48f6f-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48f6f-219">0x00000010</span></span>                                                |
| <span data-ttu-id="48f6f-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="48f6f-220">Classes used in</span></span>        | [<span data-ttu-id="48f6f-221">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="48f6f-221">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="48f6f-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="48f6f-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="48f6f-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="48f6f-223">Entry</span></span> | <span data-ttu-id="48f6f-224">Valor</span><span class="sxs-lookup"><span data-stu-id="48f6f-224">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="48f6f-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="48f6f-225">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="48f6f-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48f6f-226">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="48f6f-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="48f6f-227">System-Only</span></span>            | <span data-ttu-id="48f6f-228">Falso</span><span class="sxs-lookup"><span data-stu-id="48f6f-228">False</span></span>                                                     |
| <span data-ttu-id="48f6f-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="48f6f-229">Is-Single-Valued</span></span>       | <span data-ttu-id="48f6f-230">True</span><span class="sxs-lookup"><span data-stu-id="48f6f-230">True</span></span>                                                      |
| <span data-ttu-id="48f6f-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="48f6f-231">Is Indexed</span></span>             | <span data-ttu-id="48f6f-232">Falso</span><span class="sxs-lookup"><span data-stu-id="48f6f-232">False</span></span>                                                     |
| <span data-ttu-id="48f6f-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="48f6f-233">In Global Catalog</span></span>      | <span data-ttu-id="48f6f-234">Falso</span><span class="sxs-lookup"><span data-stu-id="48f6f-234">False</span></span>                                                     |
| <span data-ttu-id="48f6f-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="48f6f-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="48f6f-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="48f6f-236">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="48f6f-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48f6f-237">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="48f6f-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48f6f-238">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="48f6f-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48f6f-239">Search-Flags</span></span>           | <span data-ttu-id="48f6f-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48f6f-240">0x00000000</span></span>                                                |
| <span data-ttu-id="48f6f-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48f6f-241">System-Flags</span></span>           | <span data-ttu-id="48f6f-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48f6f-242">0x00000010</span></span>                                                |
| <span data-ttu-id="48f6f-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="48f6f-243">Classes used in</span></span>        | [<span data-ttu-id="48f6f-244">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="48f6f-244">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="48f6f-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="48f6f-245">Windows Server 2012</span></span>



| <span data-ttu-id="48f6f-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="48f6f-246">Entry</span></span> | <span data-ttu-id="48f6f-247">Valor</span><span class="sxs-lookup"><span data-stu-id="48f6f-247">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="48f6f-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="48f6f-248">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="48f6f-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48f6f-249">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="48f6f-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="48f6f-250">System-Only</span></span>            | <span data-ttu-id="48f6f-251">Falso</span><span class="sxs-lookup"><span data-stu-id="48f6f-251">False</span></span>                                                     |
| <span data-ttu-id="48f6f-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="48f6f-252">Is-Single-Valued</span></span>       | <span data-ttu-id="48f6f-253">True</span><span class="sxs-lookup"><span data-stu-id="48f6f-253">True</span></span>                                                      |
| <span data-ttu-id="48f6f-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="48f6f-254">Is Indexed</span></span>             | <span data-ttu-id="48f6f-255">Falso</span><span class="sxs-lookup"><span data-stu-id="48f6f-255">False</span></span>                                                     |
| <span data-ttu-id="48f6f-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="48f6f-256">In Global Catalog</span></span>      | <span data-ttu-id="48f6f-257">Falso</span><span class="sxs-lookup"><span data-stu-id="48f6f-257">False</span></span>                                                     |
| <span data-ttu-id="48f6f-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="48f6f-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="48f6f-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="48f6f-259">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="48f6f-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48f6f-260">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="48f6f-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48f6f-261">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="48f6f-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48f6f-262">Search-Flags</span></span>           | <span data-ttu-id="48f6f-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48f6f-263">0x00000000</span></span>                                                |
| <span data-ttu-id="48f6f-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48f6f-264">System-Flags</span></span>           | <span data-ttu-id="48f6f-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48f6f-265">0x00000010</span></span>                                                |
| <span data-ttu-id="48f6f-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="48f6f-266">Classes used in</span></span>        | [<span data-ttu-id="48f6f-267">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="48f6f-267">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





