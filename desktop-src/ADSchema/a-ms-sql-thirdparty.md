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
# <a name="ms-sql-thirdparty-attribute"></a><span data-ttu-id="64043-106">Atributo MS-SQL-ThirdParty</span><span class="sxs-lookup"><span data-stu-id="64043-106">MS-SQL-ThirdParty attribute</span></span>

<span data-ttu-id="64043-107">Esse atributo indica se os dados de publicação são de uma fonte de dados diferente de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="64043-107">This attribute indicates whether the publication data is from a data source other than SQL Server.</span></span> <span data-ttu-id="64043-108">Se for de outra fonte, ele será definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="64043-108">If it is from another source, then it is set to **TRUE**.</span></span>



| <span data-ttu-id="64043-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="64043-109">Entry</span></span> | <span data-ttu-id="64043-110">Valor</span><span class="sxs-lookup"><span data-stu-id="64043-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="64043-111">CN</span><span class="sxs-lookup"><span data-stu-id="64043-111">CN</span></span>                | <span data-ttu-id="64043-112">MS-SQL-ThirdParty</span><span class="sxs-lookup"><span data-stu-id="64043-112">MS-SQL-ThirdParty</span></span>                    |
| <span data-ttu-id="64043-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="64043-113">Ldap-Display-Name</span></span> | <span data-ttu-id="64043-114">mS-SQL-ThirdParty</span><span class="sxs-lookup"><span data-stu-id="64043-114">mS-SQL-ThirdParty</span></span>                    |
| <span data-ttu-id="64043-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="64043-115">Size</span></span>              | <span data-ttu-id="64043-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="64043-116">4 bytes</span></span>                              |
| <span data-ttu-id="64043-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="64043-117">Update Privilege</span></span>  | <span data-ttu-id="64043-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="64043-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="64043-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="64043-119">Update Frequency</span></span>  | <span data-ttu-id="64043-120">Quando a replicação é configurada.</span><span class="sxs-lookup"><span data-stu-id="64043-120">When replication is setup.</span></span>           |
| <span data-ttu-id="64043-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="64043-121">Attribute-Id</span></span>      | <span data-ttu-id="64043-122">1.2.840.113556.1.4.1407</span><span class="sxs-lookup"><span data-stu-id="64043-122">1.2.840.113556.1.4.1407</span></span>              |
| <span data-ttu-id="64043-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="64043-123">System-Id-Guid</span></span>    | <span data-ttu-id="64043-124">c4e311fc-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="64043-124">c4e311fc-d34b-11d2-999a-0000f87a57d4</span></span> |
| <span data-ttu-id="64043-125">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64043-125">Syntax</span></span>            | [<span data-ttu-id="64043-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="64043-126">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="64043-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="64043-127">Implementations</span></span>

-   [<span data-ttu-id="64043-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="64043-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="64043-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="64043-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="64043-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="64043-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="64043-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="64043-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="64043-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="64043-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="64043-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="64043-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="64043-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="64043-134">Windows 2000 Server</span></span>



| <span data-ttu-id="64043-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="64043-135">Entry</span></span> | <span data-ttu-id="64043-136">Valor</span><span class="sxs-lookup"><span data-stu-id="64043-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="64043-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="64043-137">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="64043-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64043-138">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="64043-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="64043-139">System-Only</span></span>            | <span data-ttu-id="64043-140">Falso</span><span class="sxs-lookup"><span data-stu-id="64043-140">False</span></span>                                                               |
| <span data-ttu-id="64043-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64043-141">Is-Single-Valued</span></span>       | <span data-ttu-id="64043-142">True</span><span class="sxs-lookup"><span data-stu-id="64043-142">True</span></span>                                                                |
| <span data-ttu-id="64043-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="64043-143">Is Indexed</span></span>             | <span data-ttu-id="64043-144">Falso</span><span class="sxs-lookup"><span data-stu-id="64043-144">False</span></span>                                                               |
| <span data-ttu-id="64043-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64043-145">In Global Catalog</span></span>      | <span data-ttu-id="64043-146">Falso</span><span class="sxs-lookup"><span data-stu-id="64043-146">False</span></span>                                                               |
| <span data-ttu-id="64043-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64043-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="64043-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64043-148">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="64043-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64043-149">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="64043-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64043-150">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="64043-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64043-151">Search-Flags</span></span>           | <span data-ttu-id="64043-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64043-152">0x00000000</span></span>                                                          |
| <span data-ttu-id="64043-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64043-153">System-Flags</span></span>           | <span data-ttu-id="64043-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64043-154">0x00000010</span></span>                                                          |
| <span data-ttu-id="64043-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64043-155">Classes used in</span></span>        | [<span data-ttu-id="64043-156">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="64043-156">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="64043-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="64043-157">Windows Server 2003</span></span>



| <span data-ttu-id="64043-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="64043-158">Entry</span></span> | <span data-ttu-id="64043-159">Valor</span><span class="sxs-lookup"><span data-stu-id="64043-159">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="64043-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="64043-160">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="64043-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64043-161">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="64043-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="64043-162">System-Only</span></span>            | <span data-ttu-id="64043-163">Falso</span><span class="sxs-lookup"><span data-stu-id="64043-163">False</span></span>                                                               |
| <span data-ttu-id="64043-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64043-164">Is-Single-Valued</span></span>       | <span data-ttu-id="64043-165">True</span><span class="sxs-lookup"><span data-stu-id="64043-165">True</span></span>                                                                |
| <span data-ttu-id="64043-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="64043-166">Is Indexed</span></span>             | <span data-ttu-id="64043-167">Falso</span><span class="sxs-lookup"><span data-stu-id="64043-167">False</span></span>                                                               |
| <span data-ttu-id="64043-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64043-168">In Global Catalog</span></span>      | <span data-ttu-id="64043-169">Falso</span><span class="sxs-lookup"><span data-stu-id="64043-169">False</span></span>                                                               |
| <span data-ttu-id="64043-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64043-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="64043-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64043-171">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="64043-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64043-172">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="64043-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64043-173">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="64043-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64043-174">Search-Flags</span></span>           | <span data-ttu-id="64043-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64043-175">0x00000000</span></span>                                                          |
| <span data-ttu-id="64043-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64043-176">System-Flags</span></span>           | <span data-ttu-id="64043-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64043-177">0x00000010</span></span>                                                          |
| <span data-ttu-id="64043-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64043-178">Classes used in</span></span>        | [<span data-ttu-id="64043-179">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="64043-179">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="64043-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="64043-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="64043-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="64043-181">Entry</span></span> | <span data-ttu-id="64043-182">Valor</span><span class="sxs-lookup"><span data-stu-id="64043-182">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="64043-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="64043-183">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="64043-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64043-184">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="64043-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="64043-185">System-Only</span></span>            | <span data-ttu-id="64043-186">Falso</span><span class="sxs-lookup"><span data-stu-id="64043-186">False</span></span>                                                               |
| <span data-ttu-id="64043-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64043-187">Is-Single-Valued</span></span>       | <span data-ttu-id="64043-188">True</span><span class="sxs-lookup"><span data-stu-id="64043-188">True</span></span>                                                                |
| <span data-ttu-id="64043-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="64043-189">Is Indexed</span></span>             | <span data-ttu-id="64043-190">Falso</span><span class="sxs-lookup"><span data-stu-id="64043-190">False</span></span>                                                               |
| <span data-ttu-id="64043-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64043-191">In Global Catalog</span></span>      | <span data-ttu-id="64043-192">Falso</span><span class="sxs-lookup"><span data-stu-id="64043-192">False</span></span>                                                               |
| <span data-ttu-id="64043-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64043-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="64043-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64043-194">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="64043-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64043-195">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="64043-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64043-196">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="64043-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64043-197">Search-Flags</span></span>           | <span data-ttu-id="64043-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64043-198">0x00000000</span></span>                                                          |
| <span data-ttu-id="64043-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64043-199">System-Flags</span></span>           | <span data-ttu-id="64043-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64043-200">0x00000010</span></span>                                                          |
| <span data-ttu-id="64043-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64043-201">Classes used in</span></span>        | [<span data-ttu-id="64043-202">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="64043-202">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="64043-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64043-203">Windows Server 2008</span></span>



| <span data-ttu-id="64043-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="64043-204">Entry</span></span> | <span data-ttu-id="64043-205">Valor</span><span class="sxs-lookup"><span data-stu-id="64043-205">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="64043-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="64043-206">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="64043-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64043-207">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="64043-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="64043-208">System-Only</span></span>            | <span data-ttu-id="64043-209">Falso</span><span class="sxs-lookup"><span data-stu-id="64043-209">False</span></span>                                                               |
| <span data-ttu-id="64043-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64043-210">Is-Single-Valued</span></span>       | <span data-ttu-id="64043-211">True</span><span class="sxs-lookup"><span data-stu-id="64043-211">True</span></span>                                                                |
| <span data-ttu-id="64043-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="64043-212">Is Indexed</span></span>             | <span data-ttu-id="64043-213">Falso</span><span class="sxs-lookup"><span data-stu-id="64043-213">False</span></span>                                                               |
| <span data-ttu-id="64043-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64043-214">In Global Catalog</span></span>      | <span data-ttu-id="64043-215">Falso</span><span class="sxs-lookup"><span data-stu-id="64043-215">False</span></span>                                                               |
| <span data-ttu-id="64043-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64043-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="64043-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64043-217">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="64043-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64043-218">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="64043-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64043-219">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="64043-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64043-220">Search-Flags</span></span>           | <span data-ttu-id="64043-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64043-221">0x00000000</span></span>                                                          |
| <span data-ttu-id="64043-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64043-222">System-Flags</span></span>           | <span data-ttu-id="64043-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64043-223">0x00000010</span></span>                                                          |
| <span data-ttu-id="64043-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64043-224">Classes used in</span></span>        | [<span data-ttu-id="64043-225">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="64043-225">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="64043-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="64043-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="64043-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="64043-227">Entry</span></span> | <span data-ttu-id="64043-228">Valor</span><span class="sxs-lookup"><span data-stu-id="64043-228">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="64043-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="64043-229">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="64043-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64043-230">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="64043-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="64043-231">System-Only</span></span>            | <span data-ttu-id="64043-232">Falso</span><span class="sxs-lookup"><span data-stu-id="64043-232">False</span></span>                                                               |
| <span data-ttu-id="64043-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64043-233">Is-Single-Valued</span></span>       | <span data-ttu-id="64043-234">True</span><span class="sxs-lookup"><span data-stu-id="64043-234">True</span></span>                                                                |
| <span data-ttu-id="64043-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="64043-235">Is Indexed</span></span>             | <span data-ttu-id="64043-236">Falso</span><span class="sxs-lookup"><span data-stu-id="64043-236">False</span></span>                                                               |
| <span data-ttu-id="64043-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64043-237">In Global Catalog</span></span>      | <span data-ttu-id="64043-238">Falso</span><span class="sxs-lookup"><span data-stu-id="64043-238">False</span></span>                                                               |
| <span data-ttu-id="64043-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64043-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="64043-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64043-240">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="64043-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64043-241">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="64043-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64043-242">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="64043-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64043-243">Search-Flags</span></span>           | <span data-ttu-id="64043-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64043-244">0x00000000</span></span>                                                          |
| <span data-ttu-id="64043-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64043-245">System-Flags</span></span>           | <span data-ttu-id="64043-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64043-246">0x00000010</span></span>                                                          |
| <span data-ttu-id="64043-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64043-247">Classes used in</span></span>        | [<span data-ttu-id="64043-248">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="64043-248">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="64043-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="64043-249">Windows Server 2012</span></span>



| <span data-ttu-id="64043-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="64043-250">Entry</span></span> | <span data-ttu-id="64043-251">Valor</span><span class="sxs-lookup"><span data-stu-id="64043-251">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="64043-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="64043-252">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="64043-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64043-253">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="64043-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="64043-254">System-Only</span></span>            | <span data-ttu-id="64043-255">Falso</span><span class="sxs-lookup"><span data-stu-id="64043-255">False</span></span>                                                               |
| <span data-ttu-id="64043-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64043-256">Is-Single-Valued</span></span>       | <span data-ttu-id="64043-257">True</span><span class="sxs-lookup"><span data-stu-id="64043-257">True</span></span>                                                                |
| <span data-ttu-id="64043-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="64043-258">Is Indexed</span></span>             | <span data-ttu-id="64043-259">Falso</span><span class="sxs-lookup"><span data-stu-id="64043-259">False</span></span>                                                               |
| <span data-ttu-id="64043-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64043-260">In Global Catalog</span></span>      | <span data-ttu-id="64043-261">Falso</span><span class="sxs-lookup"><span data-stu-id="64043-261">False</span></span>                                                               |
| <span data-ttu-id="64043-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64043-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="64043-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64043-263">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="64043-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64043-264">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="64043-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64043-265">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="64043-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64043-266">Search-Flags</span></span>           | <span data-ttu-id="64043-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64043-267">0x00000000</span></span>                                                          |
| <span data-ttu-id="64043-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64043-268">System-Flags</span></span>           | <span data-ttu-id="64043-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64043-269">0x00000010</span></span>                                                          |
| <span data-ttu-id="64043-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64043-270">Classes used in</span></span>        | [<span data-ttu-id="64043-271">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="64043-271">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





