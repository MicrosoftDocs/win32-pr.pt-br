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
# <a name="ms-sql-thirdparty-attribute"></a><span data-ttu-id="a986a-106">Atributo MS-SQL-ThirdParty</span><span class="sxs-lookup"><span data-stu-id="a986a-106">MS-SQL-ThirdParty attribute</span></span>

<span data-ttu-id="a986a-107">Esse atributo indica se os dados de publicação são de uma fonte de dados diferente de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a986a-107">This attribute indicates whether the publication data is from a data source other than SQL Server.</span></span> <span data-ttu-id="a986a-108">Se for de outra fonte, ele será definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="a986a-108">If it is from another source, then it is set to **TRUE**.</span></span>



| <span data-ttu-id="a986a-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="a986a-109">Entry</span></span> | <span data-ttu-id="a986a-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a986a-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a986a-111">CN</span><span class="sxs-lookup"><span data-stu-id="a986a-111">CN</span></span>                | <span data-ttu-id="a986a-112">MS-SQL-ThirdParty</span><span class="sxs-lookup"><span data-stu-id="a986a-112">MS-SQL-ThirdParty</span></span>                    |
| <span data-ttu-id="a986a-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a986a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a986a-114">mS-SQL-ThirdParty</span><span class="sxs-lookup"><span data-stu-id="a986a-114">mS-SQL-ThirdParty</span></span>                    |
| <span data-ttu-id="a986a-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a986a-115">Size</span></span>              | <span data-ttu-id="a986a-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="a986a-116">4 bytes</span></span>                              |
| <span data-ttu-id="a986a-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a986a-117">Update Privilege</span></span>  | <span data-ttu-id="a986a-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="a986a-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="a986a-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a986a-119">Update Frequency</span></span>  | <span data-ttu-id="a986a-120">Quando a replicação é configurada.</span><span class="sxs-lookup"><span data-stu-id="a986a-120">When replication is setup.</span></span>           |
| <span data-ttu-id="a986a-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a986a-121">Attribute-Id</span></span>      | <span data-ttu-id="a986a-122">1.2.840.113556.1.4.1407</span><span class="sxs-lookup"><span data-stu-id="a986a-122">1.2.840.113556.1.4.1407</span></span>              |
| <span data-ttu-id="a986a-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a986a-123">System-Id-Guid</span></span>    | <span data-ttu-id="a986a-124">c4e311fc-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="a986a-124">c4e311fc-d34b-11d2-999a-0000f87a57d4</span></span> |
| <span data-ttu-id="a986a-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="a986a-125">Syntax</span></span>            | [<span data-ttu-id="a986a-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a986a-126">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="a986a-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="a986a-127">Implementations</span></span>

-   [<span data-ttu-id="a986a-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a986a-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a986a-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a986a-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a986a-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a986a-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a986a-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a986a-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a986a-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a986a-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a986a-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a986a-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a986a-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a986a-134">Windows 2000 Server</span></span>



| <span data-ttu-id="a986a-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="a986a-135">Entry</span></span> | <span data-ttu-id="a986a-136">Valor</span><span class="sxs-lookup"><span data-stu-id="a986a-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a986a-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="a986a-137">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a986a-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a986a-138">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a986a-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="a986a-139">System-Only</span></span>            | <span data-ttu-id="a986a-140">Falso</span><span class="sxs-lookup"><span data-stu-id="a986a-140">False</span></span>                                                               |
| <span data-ttu-id="a986a-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a986a-141">Is-Single-Valued</span></span>       | <span data-ttu-id="a986a-142">True</span><span class="sxs-lookup"><span data-stu-id="a986a-142">True</span></span>                                                                |
| <span data-ttu-id="a986a-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="a986a-143">Is Indexed</span></span>             | <span data-ttu-id="a986a-144">Falso</span><span class="sxs-lookup"><span data-stu-id="a986a-144">False</span></span>                                                               |
| <span data-ttu-id="a986a-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a986a-145">In Global Catalog</span></span>      | <span data-ttu-id="a986a-146">Falso</span><span class="sxs-lookup"><span data-stu-id="a986a-146">False</span></span>                                                               |
| <span data-ttu-id="a986a-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a986a-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="a986a-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a986a-148">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a986a-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a986a-149">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a986a-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a986a-150">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a986a-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a986a-151">Search-Flags</span></span>           | <span data-ttu-id="a986a-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a986a-152">0x00000000</span></span>                                                          |
| <span data-ttu-id="a986a-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a986a-153">System-Flags</span></span>           | <span data-ttu-id="a986a-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a986a-154">0x00000010</span></span>                                                          |
| <span data-ttu-id="a986a-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a986a-155">Classes used in</span></span>        | [<span data-ttu-id="a986a-156">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="a986a-156">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a986a-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a986a-157">Windows Server 2003</span></span>



| <span data-ttu-id="a986a-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="a986a-158">Entry</span></span> | <span data-ttu-id="a986a-159">Valor</span><span class="sxs-lookup"><span data-stu-id="a986a-159">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a986a-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="a986a-160">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a986a-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a986a-161">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a986a-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="a986a-162">System-Only</span></span>            | <span data-ttu-id="a986a-163">Falso</span><span class="sxs-lookup"><span data-stu-id="a986a-163">False</span></span>                                                               |
| <span data-ttu-id="a986a-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a986a-164">Is-Single-Valued</span></span>       | <span data-ttu-id="a986a-165">True</span><span class="sxs-lookup"><span data-stu-id="a986a-165">True</span></span>                                                                |
| <span data-ttu-id="a986a-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="a986a-166">Is Indexed</span></span>             | <span data-ttu-id="a986a-167">Falso</span><span class="sxs-lookup"><span data-stu-id="a986a-167">False</span></span>                                                               |
| <span data-ttu-id="a986a-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a986a-168">In Global Catalog</span></span>      | <span data-ttu-id="a986a-169">Falso</span><span class="sxs-lookup"><span data-stu-id="a986a-169">False</span></span>                                                               |
| <span data-ttu-id="a986a-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a986a-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="a986a-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a986a-171">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a986a-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a986a-172">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a986a-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a986a-173">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a986a-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a986a-174">Search-Flags</span></span>           | <span data-ttu-id="a986a-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a986a-175">0x00000000</span></span>                                                          |
| <span data-ttu-id="a986a-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a986a-176">System-Flags</span></span>           | <span data-ttu-id="a986a-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a986a-177">0x00000010</span></span>                                                          |
| <span data-ttu-id="a986a-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a986a-178">Classes used in</span></span>        | [<span data-ttu-id="a986a-179">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="a986a-179">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a986a-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a986a-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a986a-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="a986a-181">Entry</span></span> | <span data-ttu-id="a986a-182">Valor</span><span class="sxs-lookup"><span data-stu-id="a986a-182">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a986a-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="a986a-183">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a986a-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a986a-184">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a986a-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="a986a-185">System-Only</span></span>            | <span data-ttu-id="a986a-186">Falso</span><span class="sxs-lookup"><span data-stu-id="a986a-186">False</span></span>                                                               |
| <span data-ttu-id="a986a-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a986a-187">Is-Single-Valued</span></span>       | <span data-ttu-id="a986a-188">True</span><span class="sxs-lookup"><span data-stu-id="a986a-188">True</span></span>                                                                |
| <span data-ttu-id="a986a-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="a986a-189">Is Indexed</span></span>             | <span data-ttu-id="a986a-190">Falso</span><span class="sxs-lookup"><span data-stu-id="a986a-190">False</span></span>                                                               |
| <span data-ttu-id="a986a-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a986a-191">In Global Catalog</span></span>      | <span data-ttu-id="a986a-192">Falso</span><span class="sxs-lookup"><span data-stu-id="a986a-192">False</span></span>                                                               |
| <span data-ttu-id="a986a-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a986a-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="a986a-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a986a-194">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a986a-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a986a-195">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a986a-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a986a-196">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a986a-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a986a-197">Search-Flags</span></span>           | <span data-ttu-id="a986a-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a986a-198">0x00000000</span></span>                                                          |
| <span data-ttu-id="a986a-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a986a-199">System-Flags</span></span>           | <span data-ttu-id="a986a-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a986a-200">0x00000010</span></span>                                                          |
| <span data-ttu-id="a986a-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a986a-201">Classes used in</span></span>        | [<span data-ttu-id="a986a-202">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="a986a-202">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a986a-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a986a-203">Windows Server 2008</span></span>



| <span data-ttu-id="a986a-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="a986a-204">Entry</span></span> | <span data-ttu-id="a986a-205">Valor</span><span class="sxs-lookup"><span data-stu-id="a986a-205">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a986a-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="a986a-206">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a986a-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a986a-207">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a986a-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="a986a-208">System-Only</span></span>            | <span data-ttu-id="a986a-209">Falso</span><span class="sxs-lookup"><span data-stu-id="a986a-209">False</span></span>                                                               |
| <span data-ttu-id="a986a-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a986a-210">Is-Single-Valued</span></span>       | <span data-ttu-id="a986a-211">True</span><span class="sxs-lookup"><span data-stu-id="a986a-211">True</span></span>                                                                |
| <span data-ttu-id="a986a-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="a986a-212">Is Indexed</span></span>             | <span data-ttu-id="a986a-213">Falso</span><span class="sxs-lookup"><span data-stu-id="a986a-213">False</span></span>                                                               |
| <span data-ttu-id="a986a-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a986a-214">In Global Catalog</span></span>      | <span data-ttu-id="a986a-215">Falso</span><span class="sxs-lookup"><span data-stu-id="a986a-215">False</span></span>                                                               |
| <span data-ttu-id="a986a-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a986a-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="a986a-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a986a-217">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a986a-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a986a-218">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a986a-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a986a-219">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a986a-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a986a-220">Search-Flags</span></span>           | <span data-ttu-id="a986a-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a986a-221">0x00000000</span></span>                                                          |
| <span data-ttu-id="a986a-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a986a-222">System-Flags</span></span>           | <span data-ttu-id="a986a-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a986a-223">0x00000010</span></span>                                                          |
| <span data-ttu-id="a986a-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a986a-224">Classes used in</span></span>        | [<span data-ttu-id="a986a-225">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="a986a-225">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a986a-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a986a-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a986a-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="a986a-227">Entry</span></span> | <span data-ttu-id="a986a-228">Valor</span><span class="sxs-lookup"><span data-stu-id="a986a-228">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a986a-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="a986a-229">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a986a-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a986a-230">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a986a-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="a986a-231">System-Only</span></span>            | <span data-ttu-id="a986a-232">Falso</span><span class="sxs-lookup"><span data-stu-id="a986a-232">False</span></span>                                                               |
| <span data-ttu-id="a986a-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a986a-233">Is-Single-Valued</span></span>       | <span data-ttu-id="a986a-234">True</span><span class="sxs-lookup"><span data-stu-id="a986a-234">True</span></span>                                                                |
| <span data-ttu-id="a986a-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="a986a-235">Is Indexed</span></span>             | <span data-ttu-id="a986a-236">Falso</span><span class="sxs-lookup"><span data-stu-id="a986a-236">False</span></span>                                                               |
| <span data-ttu-id="a986a-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a986a-237">In Global Catalog</span></span>      | <span data-ttu-id="a986a-238">Falso</span><span class="sxs-lookup"><span data-stu-id="a986a-238">False</span></span>                                                               |
| <span data-ttu-id="a986a-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a986a-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="a986a-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a986a-240">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a986a-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a986a-241">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a986a-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a986a-242">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a986a-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a986a-243">Search-Flags</span></span>           | <span data-ttu-id="a986a-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a986a-244">0x00000000</span></span>                                                          |
| <span data-ttu-id="a986a-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a986a-245">System-Flags</span></span>           | <span data-ttu-id="a986a-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a986a-246">0x00000010</span></span>                                                          |
| <span data-ttu-id="a986a-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a986a-247">Classes used in</span></span>        | [<span data-ttu-id="a986a-248">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="a986a-248">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a986a-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a986a-249">Windows Server 2012</span></span>



| <span data-ttu-id="a986a-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="a986a-250">Entry</span></span> | <span data-ttu-id="a986a-251">Valor</span><span class="sxs-lookup"><span data-stu-id="a986a-251">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a986a-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="a986a-252">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a986a-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a986a-253">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a986a-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="a986a-254">System-Only</span></span>            | <span data-ttu-id="a986a-255">Falso</span><span class="sxs-lookup"><span data-stu-id="a986a-255">False</span></span>                                                               |
| <span data-ttu-id="a986a-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a986a-256">Is-Single-Valued</span></span>       | <span data-ttu-id="a986a-257">True</span><span class="sxs-lookup"><span data-stu-id="a986a-257">True</span></span>                                                                |
| <span data-ttu-id="a986a-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="a986a-258">Is Indexed</span></span>             | <span data-ttu-id="a986a-259">Falso</span><span class="sxs-lookup"><span data-stu-id="a986a-259">False</span></span>                                                               |
| <span data-ttu-id="a986a-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a986a-260">In Global Catalog</span></span>      | <span data-ttu-id="a986a-261">Falso</span><span class="sxs-lookup"><span data-stu-id="a986a-261">False</span></span>                                                               |
| <span data-ttu-id="a986a-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a986a-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="a986a-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a986a-263">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a986a-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a986a-264">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a986a-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a986a-265">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a986a-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a986a-266">Search-Flags</span></span>           | <span data-ttu-id="a986a-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a986a-267">0x00000000</span></span>                                                          |
| <span data-ttu-id="a986a-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a986a-268">System-Flags</span></span>           | <span data-ttu-id="a986a-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a986a-269">0x00000010</span></span>                                                          |
| <span data-ttu-id="a986a-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a986a-270">Classes used in</span></span>        | [<span data-ttu-id="a986a-271">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="a986a-271">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





