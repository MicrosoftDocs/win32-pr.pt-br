---
title: Atributo MS-SQL-AllowAnonymousSubscription
description: True se a publicação permitir que assinantes anônimos se assinem.
ms.assetid: d4ac86ce-d3c5-493e-8212-e9250671a522
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo MS-SQL-AllowAnonymousSubscription
- Esquema de AD do atributo mS-SQL-AllowAnonymousSubscription
topic_type:
- apiref
api_name:
- MS-SQL-AllowAnonymousSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23de7f731ffaca310a39d81d4af80a5b0a23a84
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087120"
---
# <a name="ms-sql-allowanonymoussubscription-attribute"></a><span data-ttu-id="4438b-105">Atributo MS-SQL-AllowAnonymousSubscription</span><span class="sxs-lookup"><span data-stu-id="4438b-105">MS-SQL-AllowAnonymousSubscription attribute</span></span>

<span data-ttu-id="4438b-106">True se a publicação permitir que assinantes anônimos se assinem.</span><span class="sxs-lookup"><span data-stu-id="4438b-106">True if the publication allows anonymous subscribers to subscribe to it.</span></span>



| <span data-ttu-id="4438b-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="4438b-107">Entry</span></span> | <span data-ttu-id="4438b-108">Valor</span><span class="sxs-lookup"><span data-stu-id="4438b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="4438b-109">CN</span><span class="sxs-lookup"><span data-stu-id="4438b-109">CN</span></span>                | <span data-ttu-id="4438b-110">MS-SQL-AllowAnonymousSubscription</span><span class="sxs-lookup"><span data-stu-id="4438b-110">MS-SQL-AllowAnonymousSubscription</span></span>    |
| <span data-ttu-id="4438b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4438b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4438b-112">mS-SQL-AllowAnonymousSubscription</span><span class="sxs-lookup"><span data-stu-id="4438b-112">mS-SQL-AllowAnonymousSubscription</span></span>    |
| <span data-ttu-id="4438b-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="4438b-113">Size</span></span>              | <span data-ttu-id="4438b-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="4438b-114">4 bytes</span></span>                              |
| <span data-ttu-id="4438b-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="4438b-115">Update Privilege</span></span>  | <span data-ttu-id="4438b-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="4438b-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="4438b-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="4438b-117">Update Frequency</span></span>  | <span data-ttu-id="4438b-118">Quando a replicação é configurada.</span><span class="sxs-lookup"><span data-stu-id="4438b-118">When replication is setup.</span></span>           |
| <span data-ttu-id="4438b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4438b-119">Attribute-Id</span></span>      | <span data-ttu-id="4438b-120">1.2.840.113556.1.4.1394</span><span class="sxs-lookup"><span data-stu-id="4438b-120">1.2.840.113556.1.4.1394</span></span>              |
| <span data-ttu-id="4438b-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4438b-121">System-Id-Guid</span></span>    | <span data-ttu-id="4438b-122">db77be4a-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="4438b-122">db77be4a-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="4438b-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="4438b-123">Syntax</span></span>            | [<span data-ttu-id="4438b-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="4438b-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="4438b-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="4438b-125">Implementations</span></span>

-   [<span data-ttu-id="4438b-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4438b-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4438b-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4438b-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4438b-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4438b-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4438b-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4438b-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4438b-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4438b-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4438b-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4438b-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4438b-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4438b-132">Windows 2000 Server</span></span>



| <span data-ttu-id="4438b-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="4438b-133">Entry</span></span> | <span data-ttu-id="4438b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="4438b-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="4438b-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="4438b-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="4438b-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4438b-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="4438b-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="4438b-137">System-Only</span></span>            | <span data-ttu-id="4438b-138">Falso</span><span class="sxs-lookup"><span data-stu-id="4438b-138">False</span></span>                                                               |
| <span data-ttu-id="4438b-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4438b-139">Is-Single-Valued</span></span>       | <span data-ttu-id="4438b-140">True</span><span class="sxs-lookup"><span data-stu-id="4438b-140">True</span></span>                                                                |
| <span data-ttu-id="4438b-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="4438b-141">Is Indexed</span></span>             | <span data-ttu-id="4438b-142">Falso</span><span class="sxs-lookup"><span data-stu-id="4438b-142">False</span></span>                                                               |
| <span data-ttu-id="4438b-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4438b-143">In Global Catalog</span></span>      | <span data-ttu-id="4438b-144">Falso</span><span class="sxs-lookup"><span data-stu-id="4438b-144">False</span></span>                                                               |
| <span data-ttu-id="4438b-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4438b-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="4438b-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4438b-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="4438b-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4438b-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="4438b-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4438b-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="4438b-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4438b-149">Search-Flags</span></span>           | <span data-ttu-id="4438b-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4438b-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="4438b-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4438b-151">System-Flags</span></span>           | <span data-ttu-id="4438b-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4438b-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="4438b-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4438b-153">Classes used in</span></span>        | [<span data-ttu-id="4438b-154">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="4438b-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4438b-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4438b-155">Windows Server 2003</span></span>



| <span data-ttu-id="4438b-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="4438b-156">Entry</span></span> | <span data-ttu-id="4438b-157">Valor</span><span class="sxs-lookup"><span data-stu-id="4438b-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="4438b-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="4438b-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="4438b-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4438b-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="4438b-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="4438b-160">System-Only</span></span>            | <span data-ttu-id="4438b-161">Falso</span><span class="sxs-lookup"><span data-stu-id="4438b-161">False</span></span>                                                               |
| <span data-ttu-id="4438b-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4438b-162">Is-Single-Valued</span></span>       | <span data-ttu-id="4438b-163">True</span><span class="sxs-lookup"><span data-stu-id="4438b-163">True</span></span>                                                                |
| <span data-ttu-id="4438b-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="4438b-164">Is Indexed</span></span>             | <span data-ttu-id="4438b-165">Falso</span><span class="sxs-lookup"><span data-stu-id="4438b-165">False</span></span>                                                               |
| <span data-ttu-id="4438b-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4438b-166">In Global Catalog</span></span>      | <span data-ttu-id="4438b-167">Falso</span><span class="sxs-lookup"><span data-stu-id="4438b-167">False</span></span>                                                               |
| <span data-ttu-id="4438b-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4438b-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="4438b-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4438b-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="4438b-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4438b-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="4438b-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4438b-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="4438b-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4438b-172">Search-Flags</span></span>           | <span data-ttu-id="4438b-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4438b-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="4438b-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4438b-174">System-Flags</span></span>           | <span data-ttu-id="4438b-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4438b-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="4438b-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4438b-176">Classes used in</span></span>        | [<span data-ttu-id="4438b-177">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="4438b-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4438b-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4438b-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4438b-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="4438b-179">Entry</span></span> | <span data-ttu-id="4438b-180">Valor</span><span class="sxs-lookup"><span data-stu-id="4438b-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="4438b-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="4438b-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="4438b-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4438b-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="4438b-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="4438b-183">System-Only</span></span>            | <span data-ttu-id="4438b-184">Falso</span><span class="sxs-lookup"><span data-stu-id="4438b-184">False</span></span>                                                               |
| <span data-ttu-id="4438b-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4438b-185">Is-Single-Valued</span></span>       | <span data-ttu-id="4438b-186">True</span><span class="sxs-lookup"><span data-stu-id="4438b-186">True</span></span>                                                                |
| <span data-ttu-id="4438b-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="4438b-187">Is Indexed</span></span>             | <span data-ttu-id="4438b-188">Falso</span><span class="sxs-lookup"><span data-stu-id="4438b-188">False</span></span>                                                               |
| <span data-ttu-id="4438b-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4438b-189">In Global Catalog</span></span>      | <span data-ttu-id="4438b-190">Falso</span><span class="sxs-lookup"><span data-stu-id="4438b-190">False</span></span>                                                               |
| <span data-ttu-id="4438b-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4438b-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="4438b-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4438b-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="4438b-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4438b-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="4438b-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4438b-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="4438b-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4438b-195">Search-Flags</span></span>           | <span data-ttu-id="4438b-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4438b-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="4438b-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4438b-197">System-Flags</span></span>           | <span data-ttu-id="4438b-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4438b-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="4438b-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4438b-199">Classes used in</span></span>        | [<span data-ttu-id="4438b-200">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="4438b-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4438b-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4438b-201">Windows Server 2008</span></span>



| <span data-ttu-id="4438b-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="4438b-202">Entry</span></span> | <span data-ttu-id="4438b-203">Valor</span><span class="sxs-lookup"><span data-stu-id="4438b-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="4438b-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="4438b-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="4438b-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4438b-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="4438b-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="4438b-206">System-Only</span></span>            | <span data-ttu-id="4438b-207">Falso</span><span class="sxs-lookup"><span data-stu-id="4438b-207">False</span></span>                                                               |
| <span data-ttu-id="4438b-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4438b-208">Is-Single-Valued</span></span>       | <span data-ttu-id="4438b-209">True</span><span class="sxs-lookup"><span data-stu-id="4438b-209">True</span></span>                                                                |
| <span data-ttu-id="4438b-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="4438b-210">Is Indexed</span></span>             | <span data-ttu-id="4438b-211">Falso</span><span class="sxs-lookup"><span data-stu-id="4438b-211">False</span></span>                                                               |
| <span data-ttu-id="4438b-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4438b-212">In Global Catalog</span></span>      | <span data-ttu-id="4438b-213">Falso</span><span class="sxs-lookup"><span data-stu-id="4438b-213">False</span></span>                                                               |
| <span data-ttu-id="4438b-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4438b-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="4438b-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4438b-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="4438b-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4438b-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="4438b-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4438b-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="4438b-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4438b-218">Search-Flags</span></span>           | <span data-ttu-id="4438b-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4438b-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="4438b-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4438b-220">System-Flags</span></span>           | <span data-ttu-id="4438b-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4438b-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="4438b-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4438b-222">Classes used in</span></span>        | [<span data-ttu-id="4438b-223">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="4438b-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4438b-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4438b-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4438b-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="4438b-225">Entry</span></span> | <span data-ttu-id="4438b-226">Valor</span><span class="sxs-lookup"><span data-stu-id="4438b-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="4438b-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="4438b-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="4438b-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4438b-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="4438b-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="4438b-229">System-Only</span></span>            | <span data-ttu-id="4438b-230">Falso</span><span class="sxs-lookup"><span data-stu-id="4438b-230">False</span></span>                                                               |
| <span data-ttu-id="4438b-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4438b-231">Is-Single-Valued</span></span>       | <span data-ttu-id="4438b-232">True</span><span class="sxs-lookup"><span data-stu-id="4438b-232">True</span></span>                                                                |
| <span data-ttu-id="4438b-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="4438b-233">Is Indexed</span></span>             | <span data-ttu-id="4438b-234">Falso</span><span class="sxs-lookup"><span data-stu-id="4438b-234">False</span></span>                                                               |
| <span data-ttu-id="4438b-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4438b-235">In Global Catalog</span></span>      | <span data-ttu-id="4438b-236">Falso</span><span class="sxs-lookup"><span data-stu-id="4438b-236">False</span></span>                                                               |
| <span data-ttu-id="4438b-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4438b-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="4438b-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4438b-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="4438b-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4438b-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="4438b-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4438b-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="4438b-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4438b-241">Search-Flags</span></span>           | <span data-ttu-id="4438b-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4438b-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="4438b-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4438b-243">System-Flags</span></span>           | <span data-ttu-id="4438b-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4438b-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="4438b-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4438b-245">Classes used in</span></span>        | [<span data-ttu-id="4438b-246">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="4438b-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4438b-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4438b-247">Windows Server 2012</span></span>



| <span data-ttu-id="4438b-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="4438b-248">Entry</span></span> | <span data-ttu-id="4438b-249">Valor</span><span class="sxs-lookup"><span data-stu-id="4438b-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="4438b-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="4438b-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="4438b-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4438b-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="4438b-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="4438b-252">System-Only</span></span>            | <span data-ttu-id="4438b-253">Falso</span><span class="sxs-lookup"><span data-stu-id="4438b-253">False</span></span>                                                               |
| <span data-ttu-id="4438b-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4438b-254">Is-Single-Valued</span></span>       | <span data-ttu-id="4438b-255">True</span><span class="sxs-lookup"><span data-stu-id="4438b-255">True</span></span>                                                                |
| <span data-ttu-id="4438b-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="4438b-256">Is Indexed</span></span>             | <span data-ttu-id="4438b-257">Falso</span><span class="sxs-lookup"><span data-stu-id="4438b-257">False</span></span>                                                               |
| <span data-ttu-id="4438b-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4438b-258">In Global Catalog</span></span>      | <span data-ttu-id="4438b-259">Falso</span><span class="sxs-lookup"><span data-stu-id="4438b-259">False</span></span>                                                               |
| <span data-ttu-id="4438b-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4438b-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="4438b-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4438b-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="4438b-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4438b-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="4438b-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4438b-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="4438b-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4438b-264">Search-Flags</span></span>           | <span data-ttu-id="4438b-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4438b-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="4438b-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4438b-266">System-Flags</span></span>           | <span data-ttu-id="4438b-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4438b-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="4438b-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4438b-268">Classes used in</span></span>        | [<span data-ttu-id="4438b-269">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="4438b-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





