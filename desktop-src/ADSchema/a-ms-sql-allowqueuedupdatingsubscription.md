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
# <a name="ms-sql-allowqueuedupdatingsubscription-attribute"></a><span data-ttu-id="1ed05-105">Atributo MS-SQL-AllowQueuedUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="1ed05-105">MS-SQL-AllowQueuedUpdatingSubscription attribute</span></span>

<span data-ttu-id="1ed05-106">True para permitir transações enfileiradas ao atualizar assinaturas.</span><span class="sxs-lookup"><span data-stu-id="1ed05-106">True to allow queued transactions when updating subscriptions.</span></span>



| <span data-ttu-id="1ed05-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ed05-107">Entry</span></span> | <span data-ttu-id="1ed05-108">Valor</span><span class="sxs-lookup"><span data-stu-id="1ed05-108">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="1ed05-109">CN</span><span class="sxs-lookup"><span data-stu-id="1ed05-109">CN</span></span>                | <span data-ttu-id="1ed05-110">MS-SQL-AllowQueuedUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="1ed05-110">MS-SQL-AllowQueuedUpdatingSubscription</span></span> |
| <span data-ttu-id="1ed05-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1ed05-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1ed05-112">mS-SQL-AllowQueuedUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="1ed05-112">mS-SQL-AllowQueuedUpdatingSubscription</span></span> |
| <span data-ttu-id="1ed05-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="1ed05-113">Size</span></span>              | <span data-ttu-id="1ed05-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="1ed05-114">4 bytes</span></span>                                |
| <span data-ttu-id="1ed05-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="1ed05-115">Update Privilege</span></span>  | <span data-ttu-id="1ed05-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="1ed05-116">This value is set by the system.</span></span>       |
| <span data-ttu-id="1ed05-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="1ed05-117">Update Frequency</span></span>  | <span data-ttu-id="1ed05-118">Quando a replicação é configurada.</span><span class="sxs-lookup"><span data-stu-id="1ed05-118">When replication is setup.</span></span>             |
| <span data-ttu-id="1ed05-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1ed05-119">Attribute-Id</span></span>      | <span data-ttu-id="1ed05-120">1.2.840.113556.1.4.1405</span><span class="sxs-lookup"><span data-stu-id="1ed05-120">1.2.840.113556.1.4.1405</span></span>                |
| <span data-ttu-id="1ed05-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1ed05-121">System-Id-Guid</span></span>    | <span data-ttu-id="1ed05-122">c458ca80-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="1ed05-122">c458ca80-d34b-11d2-999a-0000f87a57d4</span></span>   |
| <span data-ttu-id="1ed05-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ed05-123">Syntax</span></span>            | [<span data-ttu-id="1ed05-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1ed05-124">**Boolean**</span></span>](s-boolean.md)           |



## <a name="implementations"></a><span data-ttu-id="1ed05-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="1ed05-125">Implementations</span></span>

-   [<span data-ttu-id="1ed05-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1ed05-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1ed05-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1ed05-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1ed05-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1ed05-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1ed05-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1ed05-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1ed05-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1ed05-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1ed05-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1ed05-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1ed05-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1ed05-132">Windows 2000 Server</span></span>



| <span data-ttu-id="1ed05-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ed05-133">Entry</span></span> | <span data-ttu-id="1ed05-134">Valor</span><span class="sxs-lookup"><span data-stu-id="1ed05-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="1ed05-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="1ed05-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="1ed05-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ed05-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="1ed05-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ed05-137">System-Only</span></span>            | <span data-ttu-id="1ed05-138">Falso</span><span class="sxs-lookup"><span data-stu-id="1ed05-138">False</span></span>                                                               |
| <span data-ttu-id="1ed05-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1ed05-139">Is-Single-Valued</span></span>       | <span data-ttu-id="1ed05-140">True</span><span class="sxs-lookup"><span data-stu-id="1ed05-140">True</span></span>                                                                |
| <span data-ttu-id="1ed05-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="1ed05-141">Is Indexed</span></span>             | <span data-ttu-id="1ed05-142">Falso</span><span class="sxs-lookup"><span data-stu-id="1ed05-142">False</span></span>                                                               |
| <span data-ttu-id="1ed05-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ed05-143">In Global Catalog</span></span>      | <span data-ttu-id="1ed05-144">Falso</span><span class="sxs-lookup"><span data-stu-id="1ed05-144">False</span></span>                                                               |
| <span data-ttu-id="1ed05-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1ed05-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ed05-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1ed05-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="1ed05-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ed05-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="1ed05-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ed05-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="1ed05-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ed05-149">Search-Flags</span></span>           | <span data-ttu-id="1ed05-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ed05-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="1ed05-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ed05-151">System-Flags</span></span>           | <span data-ttu-id="1ed05-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ed05-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="1ed05-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1ed05-153">Classes used in</span></span>        | [<span data-ttu-id="1ed05-154">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="1ed05-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1ed05-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1ed05-155">Windows Server 2003</span></span>



| <span data-ttu-id="1ed05-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ed05-156">Entry</span></span> | <span data-ttu-id="1ed05-157">Valor</span><span class="sxs-lookup"><span data-stu-id="1ed05-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="1ed05-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="1ed05-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="1ed05-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ed05-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="1ed05-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ed05-160">System-Only</span></span>            | <span data-ttu-id="1ed05-161">Falso</span><span class="sxs-lookup"><span data-stu-id="1ed05-161">False</span></span>                                                               |
| <span data-ttu-id="1ed05-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1ed05-162">Is-Single-Valued</span></span>       | <span data-ttu-id="1ed05-163">True</span><span class="sxs-lookup"><span data-stu-id="1ed05-163">True</span></span>                                                                |
| <span data-ttu-id="1ed05-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="1ed05-164">Is Indexed</span></span>             | <span data-ttu-id="1ed05-165">Falso</span><span class="sxs-lookup"><span data-stu-id="1ed05-165">False</span></span>                                                               |
| <span data-ttu-id="1ed05-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ed05-166">In Global Catalog</span></span>      | <span data-ttu-id="1ed05-167">Falso</span><span class="sxs-lookup"><span data-stu-id="1ed05-167">False</span></span>                                                               |
| <span data-ttu-id="1ed05-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1ed05-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ed05-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1ed05-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="1ed05-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ed05-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="1ed05-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ed05-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="1ed05-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ed05-172">Search-Flags</span></span>           | <span data-ttu-id="1ed05-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ed05-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="1ed05-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ed05-174">System-Flags</span></span>           | <span data-ttu-id="1ed05-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ed05-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="1ed05-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1ed05-176">Classes used in</span></span>        | [<span data-ttu-id="1ed05-177">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="1ed05-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1ed05-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1ed05-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1ed05-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ed05-179">Entry</span></span> | <span data-ttu-id="1ed05-180">Valor</span><span class="sxs-lookup"><span data-stu-id="1ed05-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="1ed05-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="1ed05-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="1ed05-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ed05-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="1ed05-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ed05-183">System-Only</span></span>            | <span data-ttu-id="1ed05-184">Falso</span><span class="sxs-lookup"><span data-stu-id="1ed05-184">False</span></span>                                                               |
| <span data-ttu-id="1ed05-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1ed05-185">Is-Single-Valued</span></span>       | <span data-ttu-id="1ed05-186">True</span><span class="sxs-lookup"><span data-stu-id="1ed05-186">True</span></span>                                                                |
| <span data-ttu-id="1ed05-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="1ed05-187">Is Indexed</span></span>             | <span data-ttu-id="1ed05-188">Falso</span><span class="sxs-lookup"><span data-stu-id="1ed05-188">False</span></span>                                                               |
| <span data-ttu-id="1ed05-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ed05-189">In Global Catalog</span></span>      | <span data-ttu-id="1ed05-190">Falso</span><span class="sxs-lookup"><span data-stu-id="1ed05-190">False</span></span>                                                               |
| <span data-ttu-id="1ed05-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1ed05-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ed05-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1ed05-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="1ed05-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ed05-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="1ed05-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ed05-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="1ed05-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ed05-195">Search-Flags</span></span>           | <span data-ttu-id="1ed05-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ed05-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="1ed05-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ed05-197">System-Flags</span></span>           | <span data-ttu-id="1ed05-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ed05-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="1ed05-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1ed05-199">Classes used in</span></span>        | [<span data-ttu-id="1ed05-200">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="1ed05-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1ed05-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ed05-201">Windows Server 2008</span></span>



| <span data-ttu-id="1ed05-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ed05-202">Entry</span></span> | <span data-ttu-id="1ed05-203">Valor</span><span class="sxs-lookup"><span data-stu-id="1ed05-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="1ed05-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="1ed05-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="1ed05-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ed05-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="1ed05-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ed05-206">System-Only</span></span>            | <span data-ttu-id="1ed05-207">Falso</span><span class="sxs-lookup"><span data-stu-id="1ed05-207">False</span></span>                                                               |
| <span data-ttu-id="1ed05-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1ed05-208">Is-Single-Valued</span></span>       | <span data-ttu-id="1ed05-209">True</span><span class="sxs-lookup"><span data-stu-id="1ed05-209">True</span></span>                                                                |
| <span data-ttu-id="1ed05-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="1ed05-210">Is Indexed</span></span>             | <span data-ttu-id="1ed05-211">Falso</span><span class="sxs-lookup"><span data-stu-id="1ed05-211">False</span></span>                                                               |
| <span data-ttu-id="1ed05-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ed05-212">In Global Catalog</span></span>      | <span data-ttu-id="1ed05-213">Falso</span><span class="sxs-lookup"><span data-stu-id="1ed05-213">False</span></span>                                                               |
| <span data-ttu-id="1ed05-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1ed05-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ed05-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1ed05-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="1ed05-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ed05-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="1ed05-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ed05-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="1ed05-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ed05-218">Search-Flags</span></span>           | <span data-ttu-id="1ed05-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ed05-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="1ed05-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ed05-220">System-Flags</span></span>           | <span data-ttu-id="1ed05-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ed05-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="1ed05-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1ed05-222">Classes used in</span></span>        | [<span data-ttu-id="1ed05-223">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="1ed05-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1ed05-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1ed05-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1ed05-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ed05-225">Entry</span></span> | <span data-ttu-id="1ed05-226">Valor</span><span class="sxs-lookup"><span data-stu-id="1ed05-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="1ed05-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="1ed05-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="1ed05-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ed05-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="1ed05-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ed05-229">System-Only</span></span>            | <span data-ttu-id="1ed05-230">Falso</span><span class="sxs-lookup"><span data-stu-id="1ed05-230">False</span></span>                                                               |
| <span data-ttu-id="1ed05-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1ed05-231">Is-Single-Valued</span></span>       | <span data-ttu-id="1ed05-232">True</span><span class="sxs-lookup"><span data-stu-id="1ed05-232">True</span></span>                                                                |
| <span data-ttu-id="1ed05-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="1ed05-233">Is Indexed</span></span>             | <span data-ttu-id="1ed05-234">Falso</span><span class="sxs-lookup"><span data-stu-id="1ed05-234">False</span></span>                                                               |
| <span data-ttu-id="1ed05-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ed05-235">In Global Catalog</span></span>      | <span data-ttu-id="1ed05-236">Falso</span><span class="sxs-lookup"><span data-stu-id="1ed05-236">False</span></span>                                                               |
| <span data-ttu-id="1ed05-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1ed05-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ed05-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1ed05-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="1ed05-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ed05-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="1ed05-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ed05-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="1ed05-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ed05-241">Search-Flags</span></span>           | <span data-ttu-id="1ed05-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ed05-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="1ed05-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ed05-243">System-Flags</span></span>           | <span data-ttu-id="1ed05-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ed05-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="1ed05-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1ed05-245">Classes used in</span></span>        | [<span data-ttu-id="1ed05-246">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="1ed05-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1ed05-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1ed05-247">Windows Server 2012</span></span>



| <span data-ttu-id="1ed05-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ed05-248">Entry</span></span> | <span data-ttu-id="1ed05-249">Valor</span><span class="sxs-lookup"><span data-stu-id="1ed05-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="1ed05-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="1ed05-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="1ed05-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ed05-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="1ed05-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ed05-252">System-Only</span></span>            | <span data-ttu-id="1ed05-253">Falso</span><span class="sxs-lookup"><span data-stu-id="1ed05-253">False</span></span>                                                               |
| <span data-ttu-id="1ed05-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1ed05-254">Is-Single-Valued</span></span>       | <span data-ttu-id="1ed05-255">True</span><span class="sxs-lookup"><span data-stu-id="1ed05-255">True</span></span>                                                                |
| <span data-ttu-id="1ed05-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="1ed05-256">Is Indexed</span></span>             | <span data-ttu-id="1ed05-257">Falso</span><span class="sxs-lookup"><span data-stu-id="1ed05-257">False</span></span>                                                               |
| <span data-ttu-id="1ed05-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ed05-258">In Global Catalog</span></span>      | <span data-ttu-id="1ed05-259">Falso</span><span class="sxs-lookup"><span data-stu-id="1ed05-259">False</span></span>                                                               |
| <span data-ttu-id="1ed05-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1ed05-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ed05-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1ed05-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="1ed05-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ed05-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="1ed05-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ed05-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="1ed05-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ed05-264">Search-Flags</span></span>           | <span data-ttu-id="1ed05-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ed05-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="1ed05-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ed05-266">System-Flags</span></span>           | <span data-ttu-id="1ed05-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ed05-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="1ed05-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1ed05-268">Classes used in</span></span>        | [<span data-ttu-id="1ed05-269">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="1ed05-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





