---
title: Atributo MS-SQL-Type
description: O tipo de replicação usado por este SQL Server.
ms.assetid: 8e7fa9ab-9a25-4ee3-9134-68af698a5fb8
ms.tgt_platform: multiple
keywords:
- Atributo AD do MS-SQL-Type
- atributo AD do mS-SQL-Type
topic_type:
- apiref
api_name:
- MS-SQL-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057b85b0c522a891cc31cde699fd062897c54818
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825394"
---
# <a name="ms-sql-type-attribute"></a><span data-ttu-id="f1040-105">Atributo MS-SQL-Type</span><span class="sxs-lookup"><span data-stu-id="f1040-105">MS-SQL-Type attribute</span></span>

<span data-ttu-id="f1040-106">O tipo de replicação usado por este SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f1040-106">The replication type used by this SQL server.</span></span> <span data-ttu-id="f1040-107">Os valores a seguir são os possíveis valores para esse atributo.</span><span class="sxs-lookup"><span data-stu-id="f1040-107">The following values are the possible values for this attribute.</span></span>



| <span data-ttu-id="f1040-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f1040-108">Value</span></span>        | <span data-ttu-id="f1040-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1040-109">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="f1040-110">0</span><span class="sxs-lookup"><span data-stu-id="f1040-110">0</span></span><br/> | <span data-ttu-id="f1040-111">Replicação transacional.</span><span class="sxs-lookup"><span data-stu-id="f1040-111">Transactional replication.</span></span><br/> |
| <span data-ttu-id="f1040-112">1</span><span class="sxs-lookup"><span data-stu-id="f1040-112">1</span></span><br/> | <span data-ttu-id="f1040-113">Replicação de instantâneo</span><span class="sxs-lookup"><span data-stu-id="f1040-113">Snapshot replication.</span></span><br/>      |
| <span data-ttu-id="f1040-114">2</span><span class="sxs-lookup"><span data-stu-id="f1040-114">2</span></span><br/> | <span data-ttu-id="f1040-115">Replicação de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="f1040-115">Merge replication.</span></span><br/>         |



 



| <span data-ttu-id="f1040-116">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1040-116">Entry</span></span> | <span data-ttu-id="f1040-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f1040-117">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f1040-118">CN</span><span class="sxs-lookup"><span data-stu-id="f1040-118">CN</span></span>                | <span data-ttu-id="f1040-119">MS-SQL-Type</span><span class="sxs-lookup"><span data-stu-id="f1040-119">MS-SQL-Type</span></span>                                 |
| <span data-ttu-id="f1040-120">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f1040-120">Ldap-Display-Name</span></span> | <span data-ttu-id="f1040-121">mS-SQL-Type</span><span class="sxs-lookup"><span data-stu-id="f1040-121">mS-SQL-Type</span></span>                                 |
| <span data-ttu-id="f1040-122">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f1040-122">Size</span></span>              | \-                                          |
| <span data-ttu-id="f1040-123">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f1040-123">Update Privilege</span></span>  | <span data-ttu-id="f1040-124">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="f1040-124">Domain administrator</span></span>                        |
| <span data-ttu-id="f1040-125">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f1040-125">Update Frequency</span></span>  | <span data-ttu-id="f1040-126">Quando a replicação é configurada.</span><span class="sxs-lookup"><span data-stu-id="f1040-126">When replication is set up.</span></span>                 |
| <span data-ttu-id="f1040-127">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f1040-127">Attribute-Id</span></span>      | <span data-ttu-id="f1040-128">1.2.840.113556.1.4.1391</span><span class="sxs-lookup"><span data-stu-id="f1040-128">1.2.840.113556.1.4.1391</span></span>                     |
| <span data-ttu-id="f1040-129">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f1040-129">System-Id-Guid</span></span>    | <span data-ttu-id="f1040-130">ca48eba8-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="f1040-130">ca48eba8-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="f1040-131">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1040-131">Syntax</span></span>            | [<span data-ttu-id="f1040-132">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f1040-132">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f1040-133">Implementações</span><span class="sxs-lookup"><span data-stu-id="f1040-133">Implementations</span></span>

-   [<span data-ttu-id="f1040-134">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f1040-134">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f1040-135">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f1040-135">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f1040-136">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f1040-136">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f1040-137">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f1040-137">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f1040-138">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f1040-138">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f1040-139">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f1040-139">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f1040-140">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f1040-140">Windows 2000 Server</span></span>



| <span data-ttu-id="f1040-141">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1040-141">Entry</span></span> | <span data-ttu-id="f1040-142">Valor</span><span class="sxs-lookup"><span data-stu-id="f1040-142">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1040-143">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1040-143">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="f1040-144">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1040-144">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="f1040-145">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1040-145">System-Only</span></span>            | <span data-ttu-id="f1040-146">Falso</span><span class="sxs-lookup"><span data-stu-id="f1040-146">False</span></span>                                                                                                                               |
| <span data-ttu-id="f1040-147">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1040-147">Is-Single-Valued</span></span>       | <span data-ttu-id="f1040-148">True</span><span class="sxs-lookup"><span data-stu-id="f1040-148">True</span></span>                                                                                                                                |
| <span data-ttu-id="f1040-149">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1040-149">Is Indexed</span></span>             | <span data-ttu-id="f1040-150">Falso</span><span class="sxs-lookup"><span data-stu-id="f1040-150">False</span></span>                                                                                                                               |
| <span data-ttu-id="f1040-151">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1040-151">In Global Catalog</span></span>      | <span data-ttu-id="f1040-152">Falso</span><span class="sxs-lookup"><span data-stu-id="f1040-152">False</span></span>                                                                                                                               |
| <span data-ttu-id="f1040-153">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1040-153">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1040-154">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1040-154">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="f1040-155">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1040-155">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="f1040-156">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1040-156">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="f1040-157">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-157">Search-Flags</span></span>           | <span data-ttu-id="f1040-158">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1040-158">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="f1040-159">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-159">System-Flags</span></span>           | <span data-ttu-id="f1040-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1040-160">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="f1040-161">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1040-161">Classes used in</span></span>        | [<span data-ttu-id="f1040-162">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="f1040-162">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="f1040-163">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="f1040-163">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f1040-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f1040-164">Windows Server 2003</span></span>



| <span data-ttu-id="f1040-165">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1040-165">Entry</span></span> | <span data-ttu-id="f1040-166">Valor</span><span class="sxs-lookup"><span data-stu-id="f1040-166">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1040-167">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1040-167">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="f1040-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1040-168">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="f1040-169">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1040-169">System-Only</span></span>            | <span data-ttu-id="f1040-170">Falso</span><span class="sxs-lookup"><span data-stu-id="f1040-170">False</span></span>                                                                                                                               |
| <span data-ttu-id="f1040-171">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1040-171">Is-Single-Valued</span></span>       | <span data-ttu-id="f1040-172">True</span><span class="sxs-lookup"><span data-stu-id="f1040-172">True</span></span>                                                                                                                                |
| <span data-ttu-id="f1040-173">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1040-173">Is Indexed</span></span>             | <span data-ttu-id="f1040-174">Falso</span><span class="sxs-lookup"><span data-stu-id="f1040-174">False</span></span>                                                                                                                               |
| <span data-ttu-id="f1040-175">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1040-175">In Global Catalog</span></span>      | <span data-ttu-id="f1040-176">Falso</span><span class="sxs-lookup"><span data-stu-id="f1040-176">False</span></span>                                                                                                                               |
| <span data-ttu-id="f1040-177">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1040-177">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1040-178">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1040-178">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="f1040-179">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1040-179">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="f1040-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1040-180">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="f1040-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-181">Search-Flags</span></span>           | <span data-ttu-id="f1040-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1040-182">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="f1040-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-183">System-Flags</span></span>           | <span data-ttu-id="f1040-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1040-184">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="f1040-185">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1040-185">Classes used in</span></span>        | [<span data-ttu-id="f1040-186">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="f1040-186">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="f1040-187">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="f1040-187">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f1040-188">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f1040-188">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f1040-189">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1040-189">Entry</span></span> | <span data-ttu-id="f1040-190">Valor</span><span class="sxs-lookup"><span data-stu-id="f1040-190">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1040-191">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1040-191">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="f1040-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1040-192">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="f1040-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1040-193">System-Only</span></span>            | <span data-ttu-id="f1040-194">Falso</span><span class="sxs-lookup"><span data-stu-id="f1040-194">False</span></span>                                                                                                                               |
| <span data-ttu-id="f1040-195">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1040-195">Is-Single-Valued</span></span>       | <span data-ttu-id="f1040-196">True</span><span class="sxs-lookup"><span data-stu-id="f1040-196">True</span></span>                                                                                                                                |
| <span data-ttu-id="f1040-197">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1040-197">Is Indexed</span></span>             | <span data-ttu-id="f1040-198">Falso</span><span class="sxs-lookup"><span data-stu-id="f1040-198">False</span></span>                                                                                                                               |
| <span data-ttu-id="f1040-199">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1040-199">In Global Catalog</span></span>      | <span data-ttu-id="f1040-200">Falso</span><span class="sxs-lookup"><span data-stu-id="f1040-200">False</span></span>                                                                                                                               |
| <span data-ttu-id="f1040-201">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1040-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1040-202">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1040-202">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="f1040-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1040-203">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="f1040-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1040-204">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="f1040-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-205">Search-Flags</span></span>           | <span data-ttu-id="f1040-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1040-206">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="f1040-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-207">System-Flags</span></span>           | <span data-ttu-id="f1040-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1040-208">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="f1040-209">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1040-209">Classes used in</span></span>        | [<span data-ttu-id="f1040-210">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="f1040-210">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="f1040-211">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="f1040-211">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f1040-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1040-212">Windows Server 2008</span></span>



| <span data-ttu-id="f1040-213">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1040-213">Entry</span></span> | <span data-ttu-id="f1040-214">Valor</span><span class="sxs-lookup"><span data-stu-id="f1040-214">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1040-215">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1040-215">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="f1040-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1040-216">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="f1040-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1040-217">System-Only</span></span>            | <span data-ttu-id="f1040-218">Falso</span><span class="sxs-lookup"><span data-stu-id="f1040-218">False</span></span>                                                                                                                               |
| <span data-ttu-id="f1040-219">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1040-219">Is-Single-Valued</span></span>       | <span data-ttu-id="f1040-220">True</span><span class="sxs-lookup"><span data-stu-id="f1040-220">True</span></span>                                                                                                                                |
| <span data-ttu-id="f1040-221">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1040-221">Is Indexed</span></span>             | <span data-ttu-id="f1040-222">Falso</span><span class="sxs-lookup"><span data-stu-id="f1040-222">False</span></span>                                                                                                                               |
| <span data-ttu-id="f1040-223">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1040-223">In Global Catalog</span></span>      | <span data-ttu-id="f1040-224">Falso</span><span class="sxs-lookup"><span data-stu-id="f1040-224">False</span></span>                                                                                                                               |
| <span data-ttu-id="f1040-225">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1040-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1040-226">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1040-226">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="f1040-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1040-227">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="f1040-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1040-228">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="f1040-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-229">Search-Flags</span></span>           | <span data-ttu-id="f1040-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1040-230">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="f1040-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-231">System-Flags</span></span>           | <span data-ttu-id="f1040-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1040-232">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="f1040-233">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1040-233">Classes used in</span></span>        | [<span data-ttu-id="f1040-234">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="f1040-234">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="f1040-235">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="f1040-235">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f1040-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f1040-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f1040-237">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1040-237">Entry</span></span> | <span data-ttu-id="f1040-238">Valor</span><span class="sxs-lookup"><span data-stu-id="f1040-238">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1040-239">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1040-239">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="f1040-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1040-240">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="f1040-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1040-241">System-Only</span></span>            | <span data-ttu-id="f1040-242">Falso</span><span class="sxs-lookup"><span data-stu-id="f1040-242">False</span></span>                                                                                                                               |
| <span data-ttu-id="f1040-243">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1040-243">Is-Single-Valued</span></span>       | <span data-ttu-id="f1040-244">True</span><span class="sxs-lookup"><span data-stu-id="f1040-244">True</span></span>                                                                                                                                |
| <span data-ttu-id="f1040-245">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1040-245">Is Indexed</span></span>             | <span data-ttu-id="f1040-246">Falso</span><span class="sxs-lookup"><span data-stu-id="f1040-246">False</span></span>                                                                                                                               |
| <span data-ttu-id="f1040-247">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1040-247">In Global Catalog</span></span>      | <span data-ttu-id="f1040-248">Falso</span><span class="sxs-lookup"><span data-stu-id="f1040-248">False</span></span>                                                                                                                               |
| <span data-ttu-id="f1040-249">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1040-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1040-250">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1040-250">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="f1040-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1040-251">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="f1040-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1040-252">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="f1040-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-253">Search-Flags</span></span>           | <span data-ttu-id="f1040-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1040-254">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="f1040-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-255">System-Flags</span></span>           | <span data-ttu-id="f1040-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1040-256">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="f1040-257">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1040-257">Classes used in</span></span>        | [<span data-ttu-id="f1040-258">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="f1040-258">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="f1040-259">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="f1040-259">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f1040-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f1040-260">Windows Server 2012</span></span>



| <span data-ttu-id="f1040-261">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1040-261">Entry</span></span> | <span data-ttu-id="f1040-262">Valor</span><span class="sxs-lookup"><span data-stu-id="f1040-262">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1040-263">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1040-263">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="f1040-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1040-264">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="f1040-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1040-265">System-Only</span></span>            | <span data-ttu-id="f1040-266">Falso</span><span class="sxs-lookup"><span data-stu-id="f1040-266">False</span></span>                                                                                                                               |
| <span data-ttu-id="f1040-267">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1040-267">Is-Single-Valued</span></span>       | <span data-ttu-id="f1040-268">True</span><span class="sxs-lookup"><span data-stu-id="f1040-268">True</span></span>                                                                                                                                |
| <span data-ttu-id="f1040-269">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1040-269">Is Indexed</span></span>             | <span data-ttu-id="f1040-270">Falso</span><span class="sxs-lookup"><span data-stu-id="f1040-270">False</span></span>                                                                                                                               |
| <span data-ttu-id="f1040-271">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1040-271">In Global Catalog</span></span>      | <span data-ttu-id="f1040-272">Falso</span><span class="sxs-lookup"><span data-stu-id="f1040-272">False</span></span>                                                                                                                               |
| <span data-ttu-id="f1040-273">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1040-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1040-274">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1040-274">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="f1040-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1040-275">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="f1040-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1040-276">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="f1040-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-277">Search-Flags</span></span>           | <span data-ttu-id="f1040-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1040-278">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="f1040-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1040-279">System-Flags</span></span>           | <span data-ttu-id="f1040-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1040-280">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="f1040-281">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1040-281">Classes used in</span></span>        | [<span data-ttu-id="f1040-282">**MS-SQL-sqlpublication**</span><span class="sxs-lookup"><span data-stu-id="f1040-282">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="f1040-283">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="f1040-283">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



 

 





