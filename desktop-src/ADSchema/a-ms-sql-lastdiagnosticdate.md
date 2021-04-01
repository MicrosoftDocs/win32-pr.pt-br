---
title: Atributo MS-SQL-LastDiagnosticDate
description: A última data em que o DBCC CHECKDB foi executado.
ms.assetid: 7060e111-e4cb-4c5a-bce1-32712cbea00e
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo MS-SQL-LastDiagnosticDate
- Esquema de AD do atributo mS-SQL-LastDiagnosticDate
topic_type:
- apiref
api_name:
- MS-SQL-LastDiagnosticDate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f25b8322a9f83b96c0ab4883478e6c0ffa2f3b49
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645354"
---
# <a name="ms-sql-lastdiagnosticdate-attribute"></a><span data-ttu-id="453cb-105">Atributo MS-SQL-LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="453cb-105">MS-SQL-LastDiagnosticDate attribute</span></span>

<span data-ttu-id="453cb-106">A última data em que o DBCC CHECKDB foi executado.</span><span class="sxs-lookup"><span data-stu-id="453cb-106">The last date that DBCC checkdb was run.</span></span>



| <span data-ttu-id="453cb-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="453cb-107">Entry</span></span> | <span data-ttu-id="453cb-108">Valor</span><span class="sxs-lookup"><span data-stu-id="453cb-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="453cb-109">CN</span><span class="sxs-lookup"><span data-stu-id="453cb-109">CN</span></span>                | <span data-ttu-id="453cb-110">MS-SQL-LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="453cb-110">MS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="453cb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="453cb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="453cb-112">mS-SQL-LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="453cb-112">mS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="453cb-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="453cb-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="453cb-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="453cb-114">Update Privilege</span></span>  | <span data-ttu-id="453cb-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="453cb-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="453cb-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="453cb-116">Update Frequency</span></span>  | <span data-ttu-id="453cb-117">Quando o DBCC CHECKDB é executado.</span><span class="sxs-lookup"><span data-stu-id="453cb-117">When DBCC checkdb is run.</span></span>                   |
| <span data-ttu-id="453cb-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="453cb-118">Attribute-Id</span></span>      | <span data-ttu-id="453cb-119">1.2.840.113556.1.4.1399</span><span class="sxs-lookup"><span data-stu-id="453cb-119">1.2.840.113556.1.4.1399</span></span>                     |
| <span data-ttu-id="453cb-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="453cb-120">System-Id-Guid</span></span>    | <span data-ttu-id="453cb-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="453cb-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="453cb-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="453cb-122">Syntax</span></span>            | [<span data-ttu-id="453cb-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="453cb-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="453cb-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="453cb-124">Implementations</span></span>

-   [<span data-ttu-id="453cb-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="453cb-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="453cb-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="453cb-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="453cb-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="453cb-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="453cb-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="453cb-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="453cb-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="453cb-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="453cb-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="453cb-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="453cb-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="453cb-131">Windows 2000 Server</span></span>



| <span data-ttu-id="453cb-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="453cb-132">Entry</span></span> | <span data-ttu-id="453cb-133">Valor</span><span class="sxs-lookup"><span data-stu-id="453cb-133">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="453cb-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="453cb-134">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="453cb-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="453cb-135">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="453cb-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="453cb-136">System-Only</span></span>            | <span data-ttu-id="453cb-137">Falso</span><span class="sxs-lookup"><span data-stu-id="453cb-137">False</span></span>                                                         |
| <span data-ttu-id="453cb-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="453cb-138">Is-Single-Valued</span></span>       | <span data-ttu-id="453cb-139">True</span><span class="sxs-lookup"><span data-stu-id="453cb-139">True</span></span>                                                          |
| <span data-ttu-id="453cb-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="453cb-140">Is Indexed</span></span>             | <span data-ttu-id="453cb-141">Falso</span><span class="sxs-lookup"><span data-stu-id="453cb-141">False</span></span>                                                         |
| <span data-ttu-id="453cb-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="453cb-142">In Global Catalog</span></span>      | <span data-ttu-id="453cb-143">Falso</span><span class="sxs-lookup"><span data-stu-id="453cb-143">False</span></span>                                                         |
| <span data-ttu-id="453cb-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="453cb-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="453cb-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="453cb-145">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="453cb-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="453cb-146">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="453cb-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="453cb-147">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="453cb-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="453cb-148">Search-Flags</span></span>           | <span data-ttu-id="453cb-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="453cb-149">0x00000000</span></span>                                                    |
| <span data-ttu-id="453cb-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="453cb-150">System-Flags</span></span>           | <span data-ttu-id="453cb-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="453cb-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="453cb-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="453cb-152">Classes used in</span></span>        | [<span data-ttu-id="453cb-153">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="453cb-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="453cb-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="453cb-154">Windows Server 2003</span></span>



| <span data-ttu-id="453cb-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="453cb-155">Entry</span></span> | <span data-ttu-id="453cb-156">Valor</span><span class="sxs-lookup"><span data-stu-id="453cb-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="453cb-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="453cb-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="453cb-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="453cb-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="453cb-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="453cb-159">System-Only</span></span>            | <span data-ttu-id="453cb-160">Falso</span><span class="sxs-lookup"><span data-stu-id="453cb-160">False</span></span>                                                         |
| <span data-ttu-id="453cb-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="453cb-161">Is-Single-Valued</span></span>       | <span data-ttu-id="453cb-162">True</span><span class="sxs-lookup"><span data-stu-id="453cb-162">True</span></span>                                                          |
| <span data-ttu-id="453cb-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="453cb-163">Is Indexed</span></span>             | <span data-ttu-id="453cb-164">Falso</span><span class="sxs-lookup"><span data-stu-id="453cb-164">False</span></span>                                                         |
| <span data-ttu-id="453cb-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="453cb-165">In Global Catalog</span></span>      | <span data-ttu-id="453cb-166">Falso</span><span class="sxs-lookup"><span data-stu-id="453cb-166">False</span></span>                                                         |
| <span data-ttu-id="453cb-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="453cb-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="453cb-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="453cb-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="453cb-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="453cb-169">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="453cb-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="453cb-170">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="453cb-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="453cb-171">Search-Flags</span></span>           | <span data-ttu-id="453cb-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="453cb-172">0x00000000</span></span>                                                    |
| <span data-ttu-id="453cb-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="453cb-173">System-Flags</span></span>           | <span data-ttu-id="453cb-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="453cb-174">0x00000010</span></span>                                                    |
| <span data-ttu-id="453cb-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="453cb-175">Classes used in</span></span>        | [<span data-ttu-id="453cb-176">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="453cb-176">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="453cb-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="453cb-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="453cb-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="453cb-178">Entry</span></span> | <span data-ttu-id="453cb-179">Valor</span><span class="sxs-lookup"><span data-stu-id="453cb-179">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="453cb-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="453cb-180">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="453cb-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="453cb-181">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="453cb-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="453cb-182">System-Only</span></span>            | <span data-ttu-id="453cb-183">Falso</span><span class="sxs-lookup"><span data-stu-id="453cb-183">False</span></span>                                                         |
| <span data-ttu-id="453cb-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="453cb-184">Is-Single-Valued</span></span>       | <span data-ttu-id="453cb-185">True</span><span class="sxs-lookup"><span data-stu-id="453cb-185">True</span></span>                                                          |
| <span data-ttu-id="453cb-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="453cb-186">Is Indexed</span></span>             | <span data-ttu-id="453cb-187">Falso</span><span class="sxs-lookup"><span data-stu-id="453cb-187">False</span></span>                                                         |
| <span data-ttu-id="453cb-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="453cb-188">In Global Catalog</span></span>      | <span data-ttu-id="453cb-189">Falso</span><span class="sxs-lookup"><span data-stu-id="453cb-189">False</span></span>                                                         |
| <span data-ttu-id="453cb-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="453cb-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="453cb-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="453cb-191">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="453cb-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="453cb-192">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="453cb-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="453cb-193">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="453cb-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="453cb-194">Search-Flags</span></span>           | <span data-ttu-id="453cb-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="453cb-195">0x00000000</span></span>                                                    |
| <span data-ttu-id="453cb-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="453cb-196">System-Flags</span></span>           | <span data-ttu-id="453cb-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="453cb-197">0x00000010</span></span>                                                    |
| <span data-ttu-id="453cb-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="453cb-198">Classes used in</span></span>        | [<span data-ttu-id="453cb-199">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="453cb-199">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="453cb-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="453cb-200">Windows Server 2008</span></span>



| <span data-ttu-id="453cb-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="453cb-201">Entry</span></span> | <span data-ttu-id="453cb-202">Valor</span><span class="sxs-lookup"><span data-stu-id="453cb-202">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="453cb-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="453cb-203">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="453cb-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="453cb-204">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="453cb-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="453cb-205">System-Only</span></span>            | <span data-ttu-id="453cb-206">Falso</span><span class="sxs-lookup"><span data-stu-id="453cb-206">False</span></span>                                                         |
| <span data-ttu-id="453cb-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="453cb-207">Is-Single-Valued</span></span>       | <span data-ttu-id="453cb-208">True</span><span class="sxs-lookup"><span data-stu-id="453cb-208">True</span></span>                                                          |
| <span data-ttu-id="453cb-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="453cb-209">Is Indexed</span></span>             | <span data-ttu-id="453cb-210">Falso</span><span class="sxs-lookup"><span data-stu-id="453cb-210">False</span></span>                                                         |
| <span data-ttu-id="453cb-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="453cb-211">In Global Catalog</span></span>      | <span data-ttu-id="453cb-212">Falso</span><span class="sxs-lookup"><span data-stu-id="453cb-212">False</span></span>                                                         |
| <span data-ttu-id="453cb-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="453cb-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="453cb-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="453cb-214">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="453cb-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="453cb-215">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="453cb-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="453cb-216">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="453cb-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="453cb-217">Search-Flags</span></span>           | <span data-ttu-id="453cb-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="453cb-218">0x00000000</span></span>                                                    |
| <span data-ttu-id="453cb-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="453cb-219">System-Flags</span></span>           | <span data-ttu-id="453cb-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="453cb-220">0x00000010</span></span>                                                    |
| <span data-ttu-id="453cb-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="453cb-221">Classes used in</span></span>        | [<span data-ttu-id="453cb-222">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="453cb-222">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="453cb-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="453cb-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="453cb-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="453cb-224">Entry</span></span> | <span data-ttu-id="453cb-225">Valor</span><span class="sxs-lookup"><span data-stu-id="453cb-225">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="453cb-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="453cb-226">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="453cb-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="453cb-227">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="453cb-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="453cb-228">System-Only</span></span>            | <span data-ttu-id="453cb-229">Falso</span><span class="sxs-lookup"><span data-stu-id="453cb-229">False</span></span>                                                         |
| <span data-ttu-id="453cb-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="453cb-230">Is-Single-Valued</span></span>       | <span data-ttu-id="453cb-231">True</span><span class="sxs-lookup"><span data-stu-id="453cb-231">True</span></span>                                                          |
| <span data-ttu-id="453cb-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="453cb-232">Is Indexed</span></span>             | <span data-ttu-id="453cb-233">Falso</span><span class="sxs-lookup"><span data-stu-id="453cb-233">False</span></span>                                                         |
| <span data-ttu-id="453cb-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="453cb-234">In Global Catalog</span></span>      | <span data-ttu-id="453cb-235">Falso</span><span class="sxs-lookup"><span data-stu-id="453cb-235">False</span></span>                                                         |
| <span data-ttu-id="453cb-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="453cb-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="453cb-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="453cb-237">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="453cb-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="453cb-238">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="453cb-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="453cb-239">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="453cb-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="453cb-240">Search-Flags</span></span>           | <span data-ttu-id="453cb-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="453cb-241">0x00000000</span></span>                                                    |
| <span data-ttu-id="453cb-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="453cb-242">System-Flags</span></span>           | <span data-ttu-id="453cb-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="453cb-243">0x00000010</span></span>                                                    |
| <span data-ttu-id="453cb-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="453cb-244">Classes used in</span></span>        | [<span data-ttu-id="453cb-245">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="453cb-245">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="453cb-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="453cb-246">Windows Server 2012</span></span>



| <span data-ttu-id="453cb-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="453cb-247">Entry</span></span> | <span data-ttu-id="453cb-248">Valor</span><span class="sxs-lookup"><span data-stu-id="453cb-248">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="453cb-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="453cb-249">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="453cb-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="453cb-250">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="453cb-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="453cb-251">System-Only</span></span>            | <span data-ttu-id="453cb-252">Falso</span><span class="sxs-lookup"><span data-stu-id="453cb-252">False</span></span>                                                         |
| <span data-ttu-id="453cb-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="453cb-253">Is-Single-Valued</span></span>       | <span data-ttu-id="453cb-254">True</span><span class="sxs-lookup"><span data-stu-id="453cb-254">True</span></span>                                                          |
| <span data-ttu-id="453cb-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="453cb-255">Is Indexed</span></span>             | <span data-ttu-id="453cb-256">Falso</span><span class="sxs-lookup"><span data-stu-id="453cb-256">False</span></span>                                                         |
| <span data-ttu-id="453cb-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="453cb-257">In Global Catalog</span></span>      | <span data-ttu-id="453cb-258">Falso</span><span class="sxs-lookup"><span data-stu-id="453cb-258">False</span></span>                                                         |
| <span data-ttu-id="453cb-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="453cb-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="453cb-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="453cb-260">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="453cb-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="453cb-261">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="453cb-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="453cb-262">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="453cb-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="453cb-263">Search-Flags</span></span>           | <span data-ttu-id="453cb-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="453cb-264">0x00000000</span></span>                                                    |
| <span data-ttu-id="453cb-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="453cb-265">System-Flags</span></span>           | <span data-ttu-id="453cb-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="453cb-266">0x00000010</span></span>                                                    |
| <span data-ttu-id="453cb-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="453cb-267">Classes used in</span></span>        | [<span data-ttu-id="453cb-268">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="453cb-268">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



 

 





