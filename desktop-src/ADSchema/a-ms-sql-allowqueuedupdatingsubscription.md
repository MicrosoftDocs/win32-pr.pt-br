---
title: Atributo MS-SQL-AllowQueuedUpdatingSubscription
description: True para permitir transações enfileiradas ao atualizar assinaturas.
ms.assetid: 132c107f-8586-48db-b70c-027c619aadf7
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo MS-SQL-AllowQueuedUpdatingSubscription
- Esquema de AD do atributo mS-SQL-AllowQueuedUpdatingSubscription
topic_type:
- apiref
api_name:
- MS-SQL-AllowQueuedUpdatingSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2056a04b6e0f155c156cde06975e96eb13f61eb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103824976"
---
# <a name="ms-sql-allowqueuedupdatingsubscription-attribute"></a><span data-ttu-id="f228e-105">Atributo MS-SQL-AllowQueuedUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="f228e-105">MS-SQL-AllowQueuedUpdatingSubscription attribute</span></span>

<span data-ttu-id="f228e-106">True para permitir transações enfileiradas ao atualizar assinaturas.</span><span class="sxs-lookup"><span data-stu-id="f228e-106">True to allow queued transactions when updating subscriptions.</span></span>



| <span data-ttu-id="f228e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f228e-107">Entry</span></span> | <span data-ttu-id="f228e-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f228e-108">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="f228e-109">CN</span><span class="sxs-lookup"><span data-stu-id="f228e-109">CN</span></span>                | <span data-ttu-id="f228e-110">MS-SQL-AllowQueuedUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="f228e-110">MS-SQL-AllowQueuedUpdatingSubscription</span></span> |
| <span data-ttu-id="f228e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f228e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f228e-112">mS-SQL-AllowQueuedUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="f228e-112">mS-SQL-AllowQueuedUpdatingSubscription</span></span> |
| <span data-ttu-id="f228e-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f228e-113">Size</span></span>              | <span data-ttu-id="f228e-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="f228e-114">4 bytes</span></span>                                |
| <span data-ttu-id="f228e-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f228e-115">Update Privilege</span></span>  | <span data-ttu-id="f228e-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="f228e-116">This value is set by the system.</span></span>       |
| <span data-ttu-id="f228e-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f228e-117">Update Frequency</span></span>  | <span data-ttu-id="f228e-118">Quando a replicação é configurada.</span><span class="sxs-lookup"><span data-stu-id="f228e-118">When replication is setup.</span></span>             |
| <span data-ttu-id="f228e-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f228e-119">Attribute-Id</span></span>      | <span data-ttu-id="f228e-120">1.2.840.113556.1.4.1405</span><span class="sxs-lookup"><span data-stu-id="f228e-120">1.2.840.113556.1.4.1405</span></span>                |
| <span data-ttu-id="f228e-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f228e-121">System-Id-Guid</span></span>    | <span data-ttu-id="f228e-122">c458ca80-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="f228e-122">c458ca80-d34b-11d2-999a-0000f87a57d4</span></span>   |
| <span data-ttu-id="f228e-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="f228e-123">Syntax</span></span>            | [<span data-ttu-id="f228e-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f228e-124">**Boolean**</span></span>](s-boolean.md)           |



## <a name="implementations"></a><span data-ttu-id="f228e-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="f228e-125">Implementations</span></span>

-   [<span data-ttu-id="f228e-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f228e-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f228e-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f228e-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f228e-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f228e-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f228e-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f228e-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f228e-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f228e-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f228e-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f228e-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f228e-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f228e-132">Windows 2000 Server</span></span>



| <span data-ttu-id="f228e-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="f228e-133">Entry</span></span> | <span data-ttu-id="f228e-134">Valor</span><span class="sxs-lookup"><span data-stu-id="f228e-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f228e-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="f228e-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f228e-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f228e-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f228e-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f228e-137">System-Only</span></span>            | <span data-ttu-id="f228e-138">Falso</span><span class="sxs-lookup"><span data-stu-id="f228e-138">False</span></span>                                                               |
| <span data-ttu-id="f228e-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f228e-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f228e-140">True</span><span class="sxs-lookup"><span data-stu-id="f228e-140">True</span></span>                                                                |
| <span data-ttu-id="f228e-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="f228e-141">Is Indexed</span></span>             | <span data-ttu-id="f228e-142">Falso</span><span class="sxs-lookup"><span data-stu-id="f228e-142">False</span></span>                                                               |
| <span data-ttu-id="f228e-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f228e-143">In Global Catalog</span></span>      | <span data-ttu-id="f228e-144">Falso</span><span class="sxs-lookup"><span data-stu-id="f228e-144">False</span></span>                                                               |
| <span data-ttu-id="f228e-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f228e-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f228e-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f228e-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="f228e-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f228e-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="f228e-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f228e-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="f228e-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f228e-149">Search-Flags</span></span>           | <span data-ttu-id="f228e-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f228e-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="f228e-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f228e-151">System-Flags</span></span>           | <span data-ttu-id="f228e-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f228e-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="f228e-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f228e-153">Classes used in</span></span>        | [<span data-ttu-id="f228e-154">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="f228e-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f228e-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f228e-155">Windows Server 2003</span></span>



| <span data-ttu-id="f228e-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="f228e-156">Entry</span></span> | <span data-ttu-id="f228e-157">Valor</span><span class="sxs-lookup"><span data-stu-id="f228e-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f228e-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="f228e-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f228e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f228e-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f228e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="f228e-160">System-Only</span></span>            | <span data-ttu-id="f228e-161">Falso</span><span class="sxs-lookup"><span data-stu-id="f228e-161">False</span></span>                                                               |
| <span data-ttu-id="f228e-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f228e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="f228e-163">True</span><span class="sxs-lookup"><span data-stu-id="f228e-163">True</span></span>                                                                |
| <span data-ttu-id="f228e-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="f228e-164">Is Indexed</span></span>             | <span data-ttu-id="f228e-165">Falso</span><span class="sxs-lookup"><span data-stu-id="f228e-165">False</span></span>                                                               |
| <span data-ttu-id="f228e-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f228e-166">In Global Catalog</span></span>      | <span data-ttu-id="f228e-167">Falso</span><span class="sxs-lookup"><span data-stu-id="f228e-167">False</span></span>                                                               |
| <span data-ttu-id="f228e-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f228e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="f228e-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f228e-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="f228e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f228e-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="f228e-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f228e-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="f228e-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f228e-172">Search-Flags</span></span>           | <span data-ttu-id="f228e-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f228e-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="f228e-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f228e-174">System-Flags</span></span>           | <span data-ttu-id="f228e-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f228e-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="f228e-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f228e-176">Classes used in</span></span>        | [<span data-ttu-id="f228e-177">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="f228e-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f228e-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f228e-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f228e-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="f228e-179">Entry</span></span> | <span data-ttu-id="f228e-180">Valor</span><span class="sxs-lookup"><span data-stu-id="f228e-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f228e-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="f228e-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f228e-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f228e-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f228e-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="f228e-183">System-Only</span></span>            | <span data-ttu-id="f228e-184">Falso</span><span class="sxs-lookup"><span data-stu-id="f228e-184">False</span></span>                                                               |
| <span data-ttu-id="f228e-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f228e-185">Is-Single-Valued</span></span>       | <span data-ttu-id="f228e-186">True</span><span class="sxs-lookup"><span data-stu-id="f228e-186">True</span></span>                                                                |
| <span data-ttu-id="f228e-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="f228e-187">Is Indexed</span></span>             | <span data-ttu-id="f228e-188">Falso</span><span class="sxs-lookup"><span data-stu-id="f228e-188">False</span></span>                                                               |
| <span data-ttu-id="f228e-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f228e-189">In Global Catalog</span></span>      | <span data-ttu-id="f228e-190">Falso</span><span class="sxs-lookup"><span data-stu-id="f228e-190">False</span></span>                                                               |
| <span data-ttu-id="f228e-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f228e-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="f228e-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f228e-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="f228e-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f228e-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="f228e-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f228e-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="f228e-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f228e-195">Search-Flags</span></span>           | <span data-ttu-id="f228e-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f228e-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="f228e-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f228e-197">System-Flags</span></span>           | <span data-ttu-id="f228e-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f228e-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="f228e-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f228e-199">Classes used in</span></span>        | [<span data-ttu-id="f228e-200">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="f228e-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f228e-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f228e-201">Windows Server 2008</span></span>



| <span data-ttu-id="f228e-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="f228e-202">Entry</span></span> | <span data-ttu-id="f228e-203">Valor</span><span class="sxs-lookup"><span data-stu-id="f228e-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f228e-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="f228e-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f228e-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f228e-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f228e-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="f228e-206">System-Only</span></span>            | <span data-ttu-id="f228e-207">Falso</span><span class="sxs-lookup"><span data-stu-id="f228e-207">False</span></span>                                                               |
| <span data-ttu-id="f228e-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f228e-208">Is-Single-Valued</span></span>       | <span data-ttu-id="f228e-209">True</span><span class="sxs-lookup"><span data-stu-id="f228e-209">True</span></span>                                                                |
| <span data-ttu-id="f228e-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="f228e-210">Is Indexed</span></span>             | <span data-ttu-id="f228e-211">Falso</span><span class="sxs-lookup"><span data-stu-id="f228e-211">False</span></span>                                                               |
| <span data-ttu-id="f228e-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f228e-212">In Global Catalog</span></span>      | <span data-ttu-id="f228e-213">Falso</span><span class="sxs-lookup"><span data-stu-id="f228e-213">False</span></span>                                                               |
| <span data-ttu-id="f228e-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f228e-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="f228e-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f228e-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="f228e-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f228e-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="f228e-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f228e-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="f228e-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f228e-218">Search-Flags</span></span>           | <span data-ttu-id="f228e-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f228e-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="f228e-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f228e-220">System-Flags</span></span>           | <span data-ttu-id="f228e-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f228e-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="f228e-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f228e-222">Classes used in</span></span>        | [<span data-ttu-id="f228e-223">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="f228e-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f228e-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f228e-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f228e-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="f228e-225">Entry</span></span> | <span data-ttu-id="f228e-226">Valor</span><span class="sxs-lookup"><span data-stu-id="f228e-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f228e-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="f228e-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f228e-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f228e-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f228e-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="f228e-229">System-Only</span></span>            | <span data-ttu-id="f228e-230">Falso</span><span class="sxs-lookup"><span data-stu-id="f228e-230">False</span></span>                                                               |
| <span data-ttu-id="f228e-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f228e-231">Is-Single-Valued</span></span>       | <span data-ttu-id="f228e-232">True</span><span class="sxs-lookup"><span data-stu-id="f228e-232">True</span></span>                                                                |
| <span data-ttu-id="f228e-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="f228e-233">Is Indexed</span></span>             | <span data-ttu-id="f228e-234">Falso</span><span class="sxs-lookup"><span data-stu-id="f228e-234">False</span></span>                                                               |
| <span data-ttu-id="f228e-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f228e-235">In Global Catalog</span></span>      | <span data-ttu-id="f228e-236">Falso</span><span class="sxs-lookup"><span data-stu-id="f228e-236">False</span></span>                                                               |
| <span data-ttu-id="f228e-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f228e-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="f228e-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f228e-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="f228e-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f228e-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="f228e-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f228e-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="f228e-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f228e-241">Search-Flags</span></span>           | <span data-ttu-id="f228e-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f228e-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="f228e-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f228e-243">System-Flags</span></span>           | <span data-ttu-id="f228e-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f228e-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="f228e-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f228e-245">Classes used in</span></span>        | [<span data-ttu-id="f228e-246">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="f228e-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f228e-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f228e-247">Windows Server 2012</span></span>



| <span data-ttu-id="f228e-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="f228e-248">Entry</span></span> | <span data-ttu-id="f228e-249">Valor</span><span class="sxs-lookup"><span data-stu-id="f228e-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f228e-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="f228e-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f228e-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f228e-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f228e-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="f228e-252">System-Only</span></span>            | <span data-ttu-id="f228e-253">Falso</span><span class="sxs-lookup"><span data-stu-id="f228e-253">False</span></span>                                                               |
| <span data-ttu-id="f228e-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f228e-254">Is-Single-Valued</span></span>       | <span data-ttu-id="f228e-255">True</span><span class="sxs-lookup"><span data-stu-id="f228e-255">True</span></span>                                                                |
| <span data-ttu-id="f228e-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="f228e-256">Is Indexed</span></span>             | <span data-ttu-id="f228e-257">Falso</span><span class="sxs-lookup"><span data-stu-id="f228e-257">False</span></span>                                                               |
| <span data-ttu-id="f228e-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f228e-258">In Global Catalog</span></span>      | <span data-ttu-id="f228e-259">Falso</span><span class="sxs-lookup"><span data-stu-id="f228e-259">False</span></span>                                                               |
| <span data-ttu-id="f228e-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f228e-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="f228e-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f228e-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="f228e-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f228e-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="f228e-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f228e-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="f228e-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f228e-264">Search-Flags</span></span>           | <span data-ttu-id="f228e-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f228e-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="f228e-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f228e-266">System-Flags</span></span>           | <span data-ttu-id="f228e-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f228e-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="f228e-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f228e-268">Classes used in</span></span>        | [<span data-ttu-id="f228e-269">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="f228e-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





