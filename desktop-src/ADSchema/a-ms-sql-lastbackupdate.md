---
title: Atributo MS-SQL-LastBackupDate
description: A última data em que foi feito o backup do banco de dados.
ms.assetid: 09bd6c2a-85fe-46af-8569-5bc3cbc8411d
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo MS-SQL-LastBackupDate
- Esquema de AD do atributo mS-SQL-LastBackupDate
topic_type:
- apiref
api_name:
- MS-SQL-LastBackupDate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d91cadf953ab51185882c73d4d999a5ccb3fed9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919641"
---
# <a name="ms-sql-lastbackupdate-attribute"></a><span data-ttu-id="0641c-105">Atributo MS-SQL-LastBackupDate</span><span class="sxs-lookup"><span data-stu-id="0641c-105">MS-SQL-LastBackupDate attribute</span></span>

<span data-ttu-id="0641c-106">A última data em que foi feito o backup do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0641c-106">The last date that the database was backed up.</span></span>



| <span data-ttu-id="0641c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="0641c-107">Entry</span></span> | <span data-ttu-id="0641c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="0641c-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="0641c-109">CN</span><span class="sxs-lookup"><span data-stu-id="0641c-109">CN</span></span>                | <span data-ttu-id="0641c-110">MS-SQL-LastBackupDate</span><span class="sxs-lookup"><span data-stu-id="0641c-110">MS-SQL-LastBackupDate</span></span>                       |
| <span data-ttu-id="0641c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0641c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0641c-112">mS-SQL-LastBackupDate</span><span class="sxs-lookup"><span data-stu-id="0641c-112">mS-SQL-LastBackupDate</span></span>                       |
| <span data-ttu-id="0641c-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="0641c-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="0641c-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="0641c-114">Update Privilege</span></span>  | <span data-ttu-id="0641c-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="0641c-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="0641c-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="0641c-116">Update Frequency</span></span>  | <span data-ttu-id="0641c-117">Quando é feito backup do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0641c-117">When the database is backed up.</span></span>             |
| <span data-ttu-id="0641c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0641c-118">Attribute-Id</span></span>      | <span data-ttu-id="0641c-119">1.2.840.113556.1.4.1398</span><span class="sxs-lookup"><span data-stu-id="0641c-119">1.2.840.113556.1.4.1398</span></span>                     |
| <span data-ttu-id="0641c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0641c-120">System-Id-Guid</span></span>    | <span data-ttu-id="0641c-121">f2b6abca-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="0641c-121">f2b6abca-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="0641c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="0641c-122">Syntax</span></span>            | [<span data-ttu-id="0641c-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="0641c-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="0641c-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="0641c-124">Implementations</span></span>

-   [<span data-ttu-id="0641c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0641c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0641c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0641c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0641c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0641c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0641c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0641c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0641c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0641c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0641c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0641c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0641c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0641c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0641c-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="0641c-132">Entry</span></span> | <span data-ttu-id="0641c-133">Valor</span><span class="sxs-lookup"><span data-stu-id="0641c-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0641c-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="0641c-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0641c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0641c-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0641c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0641c-136">System-Only</span></span>            | <span data-ttu-id="0641c-137">Falso</span><span class="sxs-lookup"><span data-stu-id="0641c-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="0641c-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0641c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0641c-139">True</span><span class="sxs-lookup"><span data-stu-id="0641c-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="0641c-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="0641c-140">Is Indexed</span></span>             | <span data-ttu-id="0641c-141">Falso</span><span class="sxs-lookup"><span data-stu-id="0641c-141">False</span></span>                                                                                                                         |
| <span data-ttu-id="0641c-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0641c-142">In Global Catalog</span></span>      | <span data-ttu-id="0641c-143">Falso</span><span class="sxs-lookup"><span data-stu-id="0641c-143">False</span></span>                                                                                                                         |
| <span data-ttu-id="0641c-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0641c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0641c-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0641c-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="0641c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0641c-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0641c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0641c-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0641c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0641c-148">Search-Flags</span></span>           | <span data-ttu-id="0641c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0641c-149">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="0641c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0641c-150">System-Flags</span></span>           | <span data-ttu-id="0641c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0641c-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="0641c-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0641c-152">Classes used in</span></span>        | [<span data-ttu-id="0641c-153">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="0641c-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="0641c-154">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="0641c-154">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0641c-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0641c-155">Windows Server 2003</span></span>



| <span data-ttu-id="0641c-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="0641c-156">Entry</span></span> | <span data-ttu-id="0641c-157">Valor</span><span class="sxs-lookup"><span data-stu-id="0641c-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0641c-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="0641c-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0641c-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0641c-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0641c-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="0641c-160">System-Only</span></span>            | <span data-ttu-id="0641c-161">Falso</span><span class="sxs-lookup"><span data-stu-id="0641c-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="0641c-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0641c-162">Is-Single-Valued</span></span>       | <span data-ttu-id="0641c-163">True</span><span class="sxs-lookup"><span data-stu-id="0641c-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="0641c-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="0641c-164">Is Indexed</span></span>             | <span data-ttu-id="0641c-165">Falso</span><span class="sxs-lookup"><span data-stu-id="0641c-165">False</span></span>                                                                                                                         |
| <span data-ttu-id="0641c-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0641c-166">In Global Catalog</span></span>      | <span data-ttu-id="0641c-167">Falso</span><span class="sxs-lookup"><span data-stu-id="0641c-167">False</span></span>                                                                                                                         |
| <span data-ttu-id="0641c-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0641c-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="0641c-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0641c-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="0641c-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0641c-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0641c-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0641c-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0641c-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0641c-172">Search-Flags</span></span>           | <span data-ttu-id="0641c-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0641c-173">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="0641c-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0641c-174">System-Flags</span></span>           | <span data-ttu-id="0641c-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0641c-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="0641c-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0641c-176">Classes used in</span></span>        | [<span data-ttu-id="0641c-177">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="0641c-177">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="0641c-178">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="0641c-178">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0641c-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0641c-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0641c-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="0641c-180">Entry</span></span> | <span data-ttu-id="0641c-181">Valor</span><span class="sxs-lookup"><span data-stu-id="0641c-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0641c-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="0641c-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0641c-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0641c-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0641c-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="0641c-184">System-Only</span></span>            | <span data-ttu-id="0641c-185">Falso</span><span class="sxs-lookup"><span data-stu-id="0641c-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="0641c-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0641c-186">Is-Single-Valued</span></span>       | <span data-ttu-id="0641c-187">True</span><span class="sxs-lookup"><span data-stu-id="0641c-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="0641c-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="0641c-188">Is Indexed</span></span>             | <span data-ttu-id="0641c-189">Falso</span><span class="sxs-lookup"><span data-stu-id="0641c-189">False</span></span>                                                                                                                         |
| <span data-ttu-id="0641c-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0641c-190">In Global Catalog</span></span>      | <span data-ttu-id="0641c-191">Falso</span><span class="sxs-lookup"><span data-stu-id="0641c-191">False</span></span>                                                                                                                         |
| <span data-ttu-id="0641c-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0641c-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="0641c-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0641c-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="0641c-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0641c-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0641c-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0641c-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0641c-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0641c-196">Search-Flags</span></span>           | <span data-ttu-id="0641c-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0641c-197">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="0641c-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0641c-198">System-Flags</span></span>           | <span data-ttu-id="0641c-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0641c-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="0641c-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0641c-200">Classes used in</span></span>        | [<span data-ttu-id="0641c-201">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="0641c-201">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="0641c-202">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="0641c-202">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0641c-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0641c-203">Windows Server 2008</span></span>



| <span data-ttu-id="0641c-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="0641c-204">Entry</span></span> | <span data-ttu-id="0641c-205">Valor</span><span class="sxs-lookup"><span data-stu-id="0641c-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0641c-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="0641c-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0641c-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0641c-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0641c-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="0641c-208">System-Only</span></span>            | <span data-ttu-id="0641c-209">Falso</span><span class="sxs-lookup"><span data-stu-id="0641c-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="0641c-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0641c-210">Is-Single-Valued</span></span>       | <span data-ttu-id="0641c-211">True</span><span class="sxs-lookup"><span data-stu-id="0641c-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="0641c-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="0641c-212">Is Indexed</span></span>             | <span data-ttu-id="0641c-213">Falso</span><span class="sxs-lookup"><span data-stu-id="0641c-213">False</span></span>                                                                                                                         |
| <span data-ttu-id="0641c-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0641c-214">In Global Catalog</span></span>      | <span data-ttu-id="0641c-215">Falso</span><span class="sxs-lookup"><span data-stu-id="0641c-215">False</span></span>                                                                                                                         |
| <span data-ttu-id="0641c-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0641c-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="0641c-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0641c-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="0641c-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0641c-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0641c-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0641c-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0641c-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0641c-220">Search-Flags</span></span>           | <span data-ttu-id="0641c-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0641c-221">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="0641c-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0641c-222">System-Flags</span></span>           | <span data-ttu-id="0641c-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0641c-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="0641c-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0641c-224">Classes used in</span></span>        | [<span data-ttu-id="0641c-225">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="0641c-225">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="0641c-226">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="0641c-226">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0641c-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0641c-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0641c-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="0641c-228">Entry</span></span> | <span data-ttu-id="0641c-229">Valor</span><span class="sxs-lookup"><span data-stu-id="0641c-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0641c-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="0641c-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0641c-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0641c-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0641c-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="0641c-232">System-Only</span></span>            | <span data-ttu-id="0641c-233">Falso</span><span class="sxs-lookup"><span data-stu-id="0641c-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="0641c-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0641c-234">Is-Single-Valued</span></span>       | <span data-ttu-id="0641c-235">True</span><span class="sxs-lookup"><span data-stu-id="0641c-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="0641c-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="0641c-236">Is Indexed</span></span>             | <span data-ttu-id="0641c-237">Falso</span><span class="sxs-lookup"><span data-stu-id="0641c-237">False</span></span>                                                                                                                         |
| <span data-ttu-id="0641c-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0641c-238">In Global Catalog</span></span>      | <span data-ttu-id="0641c-239">Falso</span><span class="sxs-lookup"><span data-stu-id="0641c-239">False</span></span>                                                                                                                         |
| <span data-ttu-id="0641c-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0641c-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="0641c-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0641c-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="0641c-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0641c-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0641c-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0641c-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0641c-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0641c-244">Search-Flags</span></span>           | <span data-ttu-id="0641c-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0641c-245">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="0641c-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0641c-246">System-Flags</span></span>           | <span data-ttu-id="0641c-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0641c-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="0641c-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0641c-248">Classes used in</span></span>        | [<span data-ttu-id="0641c-249">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="0641c-249">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="0641c-250">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="0641c-250">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0641c-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0641c-251">Windows Server 2012</span></span>



| <span data-ttu-id="0641c-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="0641c-252">Entry</span></span> | <span data-ttu-id="0641c-253">Valor</span><span class="sxs-lookup"><span data-stu-id="0641c-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0641c-254">ID do link</span><span class="sxs-lookup"><span data-stu-id="0641c-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0641c-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0641c-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0641c-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="0641c-256">System-Only</span></span>            | <span data-ttu-id="0641c-257">Falso</span><span class="sxs-lookup"><span data-stu-id="0641c-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="0641c-258">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0641c-258">Is-Single-Valued</span></span>       | <span data-ttu-id="0641c-259">True</span><span class="sxs-lookup"><span data-stu-id="0641c-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="0641c-260">É indexado</span><span class="sxs-lookup"><span data-stu-id="0641c-260">Is Indexed</span></span>             | <span data-ttu-id="0641c-261">Falso</span><span class="sxs-lookup"><span data-stu-id="0641c-261">False</span></span>                                                                                                                         |
| <span data-ttu-id="0641c-262">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0641c-262">In Global Catalog</span></span>      | <span data-ttu-id="0641c-263">Falso</span><span class="sxs-lookup"><span data-stu-id="0641c-263">False</span></span>                                                                                                                         |
| <span data-ttu-id="0641c-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0641c-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="0641c-265">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0641c-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="0641c-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0641c-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0641c-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0641c-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0641c-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0641c-268">Search-Flags</span></span>           | <span data-ttu-id="0641c-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0641c-269">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="0641c-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0641c-270">System-Flags</span></span>           | <span data-ttu-id="0641c-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0641c-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="0641c-272">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0641c-272">Classes used in</span></span>        | [<span data-ttu-id="0641c-273">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="0641c-273">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="0641c-274">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="0641c-274">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



 

 





