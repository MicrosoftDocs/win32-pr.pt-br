---
title: Atributo MS-SQL-ThirdParty
description: Esse atributo indica se os dados de publicação são de uma fonte de dados diferente de SQL Server. Se for de outra fonte, ele será definido como TRUE.
ms.assetid: 84d93b9f-0acc-47da-9f1b-44d8468ad53e
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo MS-SQL-ThirdParty
- Esquema de AD do atributo mS-SQL-ThirdParty
topic_type:
- apiref
api_name:
- MS-SQL-ThirdParty
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc2b60f9589990f6357ee3c4cd24215e8af21df
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645349"
---
# <a name="ms-sql-thirdparty-attribute"></a><span data-ttu-id="6fb93-106">Atributo MS-SQL-ThirdParty</span><span class="sxs-lookup"><span data-stu-id="6fb93-106">MS-SQL-ThirdParty attribute</span></span>

<span data-ttu-id="6fb93-107">Esse atributo indica se os dados de publicação são de uma fonte de dados diferente de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6fb93-107">This attribute indicates whether the publication data is from a data source other than SQL Server.</span></span> <span data-ttu-id="6fb93-108">Se for de outra fonte, ele será definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="6fb93-108">If it is from another source, then it is set to **TRUE**.</span></span>



| <span data-ttu-id="6fb93-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="6fb93-109">Entry</span></span> | <span data-ttu-id="6fb93-110">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb93-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6fb93-111">CN</span><span class="sxs-lookup"><span data-stu-id="6fb93-111">CN</span></span>                | <span data-ttu-id="6fb93-112">MS-SQL-ThirdParty</span><span class="sxs-lookup"><span data-stu-id="6fb93-112">MS-SQL-ThirdParty</span></span>                    |
| <span data-ttu-id="6fb93-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6fb93-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6fb93-114">mS-SQL-ThirdParty</span><span class="sxs-lookup"><span data-stu-id="6fb93-114">mS-SQL-ThirdParty</span></span>                    |
| <span data-ttu-id="6fb93-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="6fb93-115">Size</span></span>              | <span data-ttu-id="6fb93-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="6fb93-116">4 bytes</span></span>                              |
| <span data-ttu-id="6fb93-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="6fb93-117">Update Privilege</span></span>  | <span data-ttu-id="6fb93-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="6fb93-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="6fb93-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="6fb93-119">Update Frequency</span></span>  | <span data-ttu-id="6fb93-120">Quando a replicação é configurada.</span><span class="sxs-lookup"><span data-stu-id="6fb93-120">When replication is setup.</span></span>           |
| <span data-ttu-id="6fb93-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6fb93-121">Attribute-Id</span></span>      | <span data-ttu-id="6fb93-122">1.2.840.113556.1.4.1407</span><span class="sxs-lookup"><span data-stu-id="6fb93-122">1.2.840.113556.1.4.1407</span></span>              |
| <span data-ttu-id="6fb93-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6fb93-123">System-Id-Guid</span></span>    | <span data-ttu-id="6fb93-124">c4e311fc-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="6fb93-124">c4e311fc-d34b-11d2-999a-0000f87a57d4</span></span> |
| <span data-ttu-id="6fb93-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fb93-125">Syntax</span></span>            | [<span data-ttu-id="6fb93-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6fb93-126">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="6fb93-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="6fb93-127">Implementations</span></span>

-   [<span data-ttu-id="6fb93-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6fb93-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6fb93-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6fb93-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6fb93-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6fb93-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6fb93-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6fb93-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6fb93-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6fb93-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6fb93-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6fb93-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6fb93-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6fb93-134">Windows 2000 Server</span></span>



| <span data-ttu-id="6fb93-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="6fb93-135">Entry</span></span> | <span data-ttu-id="6fb93-136">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb93-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6fb93-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="6fb93-137">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6fb93-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fb93-138">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6fb93-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fb93-139">System-Only</span></span>            | <span data-ttu-id="6fb93-140">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb93-140">False</span></span>                                                               |
| <span data-ttu-id="6fb93-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6fb93-141">Is-Single-Valued</span></span>       | <span data-ttu-id="6fb93-142">True</span><span class="sxs-lookup"><span data-stu-id="6fb93-142">True</span></span>                                                                |
| <span data-ttu-id="6fb93-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="6fb93-143">Is Indexed</span></span>             | <span data-ttu-id="6fb93-144">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb93-144">False</span></span>                                                               |
| <span data-ttu-id="6fb93-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6fb93-145">In Global Catalog</span></span>      | <span data-ttu-id="6fb93-146">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb93-146">False</span></span>                                                               |
| <span data-ttu-id="6fb93-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6fb93-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fb93-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6fb93-148">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="6fb93-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fb93-149">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="6fb93-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fb93-150">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="6fb93-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb93-151">Search-Flags</span></span>           | <span data-ttu-id="6fb93-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fb93-152">0x00000000</span></span>                                                          |
| <span data-ttu-id="6fb93-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb93-153">System-Flags</span></span>           | <span data-ttu-id="6fb93-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fb93-154">0x00000010</span></span>                                                          |
| <span data-ttu-id="6fb93-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6fb93-155">Classes used in</span></span>        | [<span data-ttu-id="6fb93-156">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="6fb93-156">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6fb93-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6fb93-157">Windows Server 2003</span></span>



| <span data-ttu-id="6fb93-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="6fb93-158">Entry</span></span> | <span data-ttu-id="6fb93-159">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb93-159">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6fb93-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="6fb93-160">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6fb93-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fb93-161">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6fb93-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fb93-162">System-Only</span></span>            | <span data-ttu-id="6fb93-163">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb93-163">False</span></span>                                                               |
| <span data-ttu-id="6fb93-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6fb93-164">Is-Single-Valued</span></span>       | <span data-ttu-id="6fb93-165">True</span><span class="sxs-lookup"><span data-stu-id="6fb93-165">True</span></span>                                                                |
| <span data-ttu-id="6fb93-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="6fb93-166">Is Indexed</span></span>             | <span data-ttu-id="6fb93-167">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb93-167">False</span></span>                                                               |
| <span data-ttu-id="6fb93-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6fb93-168">In Global Catalog</span></span>      | <span data-ttu-id="6fb93-169">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb93-169">False</span></span>                                                               |
| <span data-ttu-id="6fb93-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6fb93-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fb93-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6fb93-171">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="6fb93-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fb93-172">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="6fb93-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fb93-173">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="6fb93-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb93-174">Search-Flags</span></span>           | <span data-ttu-id="6fb93-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fb93-175">0x00000000</span></span>                                                          |
| <span data-ttu-id="6fb93-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb93-176">System-Flags</span></span>           | <span data-ttu-id="6fb93-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fb93-177">0x00000010</span></span>                                                          |
| <span data-ttu-id="6fb93-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6fb93-178">Classes used in</span></span>        | [<span data-ttu-id="6fb93-179">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="6fb93-179">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6fb93-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6fb93-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6fb93-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="6fb93-181">Entry</span></span> | <span data-ttu-id="6fb93-182">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb93-182">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6fb93-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="6fb93-183">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6fb93-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fb93-184">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6fb93-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fb93-185">System-Only</span></span>            | <span data-ttu-id="6fb93-186">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb93-186">False</span></span>                                                               |
| <span data-ttu-id="6fb93-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6fb93-187">Is-Single-Valued</span></span>       | <span data-ttu-id="6fb93-188">True</span><span class="sxs-lookup"><span data-stu-id="6fb93-188">True</span></span>                                                                |
| <span data-ttu-id="6fb93-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="6fb93-189">Is Indexed</span></span>             | <span data-ttu-id="6fb93-190">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb93-190">False</span></span>                                                               |
| <span data-ttu-id="6fb93-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6fb93-191">In Global Catalog</span></span>      | <span data-ttu-id="6fb93-192">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb93-192">False</span></span>                                                               |
| <span data-ttu-id="6fb93-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6fb93-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fb93-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6fb93-194">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="6fb93-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fb93-195">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="6fb93-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fb93-196">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="6fb93-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb93-197">Search-Flags</span></span>           | <span data-ttu-id="6fb93-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fb93-198">0x00000000</span></span>                                                          |
| <span data-ttu-id="6fb93-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb93-199">System-Flags</span></span>           | <span data-ttu-id="6fb93-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fb93-200">0x00000010</span></span>                                                          |
| <span data-ttu-id="6fb93-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6fb93-201">Classes used in</span></span>        | [<span data-ttu-id="6fb93-202">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="6fb93-202">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6fb93-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fb93-203">Windows Server 2008</span></span>



| <span data-ttu-id="6fb93-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="6fb93-204">Entry</span></span> | <span data-ttu-id="6fb93-205">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb93-205">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6fb93-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="6fb93-206">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6fb93-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fb93-207">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6fb93-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fb93-208">System-Only</span></span>            | <span data-ttu-id="6fb93-209">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb93-209">False</span></span>                                                               |
| <span data-ttu-id="6fb93-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6fb93-210">Is-Single-Valued</span></span>       | <span data-ttu-id="6fb93-211">True</span><span class="sxs-lookup"><span data-stu-id="6fb93-211">True</span></span>                                                                |
| <span data-ttu-id="6fb93-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="6fb93-212">Is Indexed</span></span>             | <span data-ttu-id="6fb93-213">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb93-213">False</span></span>                                                               |
| <span data-ttu-id="6fb93-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6fb93-214">In Global Catalog</span></span>      | <span data-ttu-id="6fb93-215">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb93-215">False</span></span>                                                               |
| <span data-ttu-id="6fb93-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6fb93-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fb93-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6fb93-217">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="6fb93-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fb93-218">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="6fb93-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fb93-219">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="6fb93-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb93-220">Search-Flags</span></span>           | <span data-ttu-id="6fb93-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fb93-221">0x00000000</span></span>                                                          |
| <span data-ttu-id="6fb93-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb93-222">System-Flags</span></span>           | <span data-ttu-id="6fb93-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fb93-223">0x00000010</span></span>                                                          |
| <span data-ttu-id="6fb93-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6fb93-224">Classes used in</span></span>        | [<span data-ttu-id="6fb93-225">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="6fb93-225">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6fb93-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6fb93-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6fb93-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="6fb93-227">Entry</span></span> | <span data-ttu-id="6fb93-228">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb93-228">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6fb93-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="6fb93-229">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6fb93-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fb93-230">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6fb93-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fb93-231">System-Only</span></span>            | <span data-ttu-id="6fb93-232">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb93-232">False</span></span>                                                               |
| <span data-ttu-id="6fb93-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6fb93-233">Is-Single-Valued</span></span>       | <span data-ttu-id="6fb93-234">True</span><span class="sxs-lookup"><span data-stu-id="6fb93-234">True</span></span>                                                                |
| <span data-ttu-id="6fb93-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="6fb93-235">Is Indexed</span></span>             | <span data-ttu-id="6fb93-236">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb93-236">False</span></span>                                                               |
| <span data-ttu-id="6fb93-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6fb93-237">In Global Catalog</span></span>      | <span data-ttu-id="6fb93-238">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb93-238">False</span></span>                                                               |
| <span data-ttu-id="6fb93-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6fb93-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fb93-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6fb93-240">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="6fb93-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fb93-241">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="6fb93-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fb93-242">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="6fb93-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb93-243">Search-Flags</span></span>           | <span data-ttu-id="6fb93-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fb93-244">0x00000000</span></span>                                                          |
| <span data-ttu-id="6fb93-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb93-245">System-Flags</span></span>           | <span data-ttu-id="6fb93-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fb93-246">0x00000010</span></span>                                                          |
| <span data-ttu-id="6fb93-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6fb93-247">Classes used in</span></span>        | [<span data-ttu-id="6fb93-248">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="6fb93-248">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6fb93-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6fb93-249">Windows Server 2012</span></span>



| <span data-ttu-id="6fb93-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="6fb93-250">Entry</span></span> | <span data-ttu-id="6fb93-251">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb93-251">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6fb93-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="6fb93-252">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6fb93-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fb93-253">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6fb93-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fb93-254">System-Only</span></span>            | <span data-ttu-id="6fb93-255">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb93-255">False</span></span>                                                               |
| <span data-ttu-id="6fb93-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6fb93-256">Is-Single-Valued</span></span>       | <span data-ttu-id="6fb93-257">True</span><span class="sxs-lookup"><span data-stu-id="6fb93-257">True</span></span>                                                                |
| <span data-ttu-id="6fb93-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="6fb93-258">Is Indexed</span></span>             | <span data-ttu-id="6fb93-259">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb93-259">False</span></span>                                                               |
| <span data-ttu-id="6fb93-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6fb93-260">In Global Catalog</span></span>      | <span data-ttu-id="6fb93-261">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb93-261">False</span></span>                                                               |
| <span data-ttu-id="6fb93-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6fb93-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fb93-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6fb93-263">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="6fb93-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fb93-264">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="6fb93-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fb93-265">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="6fb93-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb93-266">Search-Flags</span></span>           | <span data-ttu-id="6fb93-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fb93-267">0x00000000</span></span>                                                          |
| <span data-ttu-id="6fb93-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb93-268">System-Flags</span></span>           | <span data-ttu-id="6fb93-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fb93-269">0x00000010</span></span>                                                          |
| <span data-ttu-id="6fb93-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6fb93-270">Classes used in</span></span>        | [<span data-ttu-id="6fb93-271">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="6fb93-271">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





