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
# <a name="ms-sql-lastdiagnosticdate-attribute"></a><span data-ttu-id="99f72-105">Atributo MS-SQL-LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="99f72-105">MS-SQL-LastDiagnosticDate attribute</span></span>

<span data-ttu-id="99f72-106">A última data em que o DBCC CHECKDB foi executado.</span><span class="sxs-lookup"><span data-stu-id="99f72-106">The last date that DBCC checkdb was run.</span></span>



| <span data-ttu-id="99f72-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="99f72-107">Entry</span></span> | <span data-ttu-id="99f72-108">Valor</span><span class="sxs-lookup"><span data-stu-id="99f72-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="99f72-109">CN</span><span class="sxs-lookup"><span data-stu-id="99f72-109">CN</span></span>                | <span data-ttu-id="99f72-110">MS-SQL-LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="99f72-110">MS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="99f72-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="99f72-111">Ldap-Display-Name</span></span> | <span data-ttu-id="99f72-112">mS-SQL-LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="99f72-112">mS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="99f72-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="99f72-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="99f72-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="99f72-114">Update Privilege</span></span>  | <span data-ttu-id="99f72-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="99f72-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="99f72-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="99f72-116">Update Frequency</span></span>  | <span data-ttu-id="99f72-117">Quando o DBCC CHECKDB é executado.</span><span class="sxs-lookup"><span data-stu-id="99f72-117">When DBCC checkdb is run.</span></span>                   |
| <span data-ttu-id="99f72-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="99f72-118">Attribute-Id</span></span>      | <span data-ttu-id="99f72-119">1.2.840.113556.1.4.1399</span><span class="sxs-lookup"><span data-stu-id="99f72-119">1.2.840.113556.1.4.1399</span></span>                     |
| <span data-ttu-id="99f72-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="99f72-120">System-Id-Guid</span></span>    | <span data-ttu-id="99f72-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="99f72-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="99f72-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="99f72-122">Syntax</span></span>            | [<span data-ttu-id="99f72-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="99f72-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="99f72-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="99f72-124">Implementations</span></span>

-   [<span data-ttu-id="99f72-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="99f72-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="99f72-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="99f72-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="99f72-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="99f72-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="99f72-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="99f72-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="99f72-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="99f72-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="99f72-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="99f72-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="99f72-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="99f72-131">Windows 2000 Server</span></span>



| <span data-ttu-id="99f72-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="99f72-132">Entry</span></span> | <span data-ttu-id="99f72-133">Valor</span><span class="sxs-lookup"><span data-stu-id="99f72-133">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="99f72-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="99f72-134">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="99f72-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99f72-135">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="99f72-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="99f72-136">System-Only</span></span>            | <span data-ttu-id="99f72-137">Falso</span><span class="sxs-lookup"><span data-stu-id="99f72-137">False</span></span>                                                         |
| <span data-ttu-id="99f72-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="99f72-138">Is-Single-Valued</span></span>       | <span data-ttu-id="99f72-139">True</span><span class="sxs-lookup"><span data-stu-id="99f72-139">True</span></span>                                                          |
| <span data-ttu-id="99f72-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="99f72-140">Is Indexed</span></span>             | <span data-ttu-id="99f72-141">Falso</span><span class="sxs-lookup"><span data-stu-id="99f72-141">False</span></span>                                                         |
| <span data-ttu-id="99f72-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="99f72-142">In Global Catalog</span></span>      | <span data-ttu-id="99f72-143">Falso</span><span class="sxs-lookup"><span data-stu-id="99f72-143">False</span></span>                                                         |
| <span data-ttu-id="99f72-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="99f72-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="99f72-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="99f72-145">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="99f72-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99f72-146">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="99f72-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99f72-147">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="99f72-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99f72-148">Search-Flags</span></span>           | <span data-ttu-id="99f72-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99f72-149">0x00000000</span></span>                                                    |
| <span data-ttu-id="99f72-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99f72-150">System-Flags</span></span>           | <span data-ttu-id="99f72-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99f72-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="99f72-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="99f72-152">Classes used in</span></span>        | [<span data-ttu-id="99f72-153">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="99f72-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="99f72-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="99f72-154">Windows Server 2003</span></span>



| <span data-ttu-id="99f72-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="99f72-155">Entry</span></span> | <span data-ttu-id="99f72-156">Valor</span><span class="sxs-lookup"><span data-stu-id="99f72-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="99f72-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="99f72-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="99f72-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99f72-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="99f72-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="99f72-159">System-Only</span></span>            | <span data-ttu-id="99f72-160">Falso</span><span class="sxs-lookup"><span data-stu-id="99f72-160">False</span></span>                                                         |
| <span data-ttu-id="99f72-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="99f72-161">Is-Single-Valued</span></span>       | <span data-ttu-id="99f72-162">True</span><span class="sxs-lookup"><span data-stu-id="99f72-162">True</span></span>                                                          |
| <span data-ttu-id="99f72-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="99f72-163">Is Indexed</span></span>             | <span data-ttu-id="99f72-164">Falso</span><span class="sxs-lookup"><span data-stu-id="99f72-164">False</span></span>                                                         |
| <span data-ttu-id="99f72-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="99f72-165">In Global Catalog</span></span>      | <span data-ttu-id="99f72-166">Falso</span><span class="sxs-lookup"><span data-stu-id="99f72-166">False</span></span>                                                         |
| <span data-ttu-id="99f72-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="99f72-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="99f72-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="99f72-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="99f72-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99f72-169">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="99f72-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99f72-170">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="99f72-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99f72-171">Search-Flags</span></span>           | <span data-ttu-id="99f72-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99f72-172">0x00000000</span></span>                                                    |
| <span data-ttu-id="99f72-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99f72-173">System-Flags</span></span>           | <span data-ttu-id="99f72-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99f72-174">0x00000010</span></span>                                                    |
| <span data-ttu-id="99f72-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="99f72-175">Classes used in</span></span>        | [<span data-ttu-id="99f72-176">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="99f72-176">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="99f72-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="99f72-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="99f72-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="99f72-178">Entry</span></span> | <span data-ttu-id="99f72-179">Valor</span><span class="sxs-lookup"><span data-stu-id="99f72-179">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="99f72-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="99f72-180">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="99f72-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99f72-181">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="99f72-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="99f72-182">System-Only</span></span>            | <span data-ttu-id="99f72-183">Falso</span><span class="sxs-lookup"><span data-stu-id="99f72-183">False</span></span>                                                         |
| <span data-ttu-id="99f72-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="99f72-184">Is-Single-Valued</span></span>       | <span data-ttu-id="99f72-185">True</span><span class="sxs-lookup"><span data-stu-id="99f72-185">True</span></span>                                                          |
| <span data-ttu-id="99f72-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="99f72-186">Is Indexed</span></span>             | <span data-ttu-id="99f72-187">Falso</span><span class="sxs-lookup"><span data-stu-id="99f72-187">False</span></span>                                                         |
| <span data-ttu-id="99f72-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="99f72-188">In Global Catalog</span></span>      | <span data-ttu-id="99f72-189">Falso</span><span class="sxs-lookup"><span data-stu-id="99f72-189">False</span></span>                                                         |
| <span data-ttu-id="99f72-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="99f72-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="99f72-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="99f72-191">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="99f72-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99f72-192">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="99f72-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99f72-193">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="99f72-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99f72-194">Search-Flags</span></span>           | <span data-ttu-id="99f72-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99f72-195">0x00000000</span></span>                                                    |
| <span data-ttu-id="99f72-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99f72-196">System-Flags</span></span>           | <span data-ttu-id="99f72-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99f72-197">0x00000010</span></span>                                                    |
| <span data-ttu-id="99f72-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="99f72-198">Classes used in</span></span>        | [<span data-ttu-id="99f72-199">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="99f72-199">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="99f72-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99f72-200">Windows Server 2008</span></span>



| <span data-ttu-id="99f72-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="99f72-201">Entry</span></span> | <span data-ttu-id="99f72-202">Valor</span><span class="sxs-lookup"><span data-stu-id="99f72-202">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="99f72-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="99f72-203">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="99f72-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99f72-204">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="99f72-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="99f72-205">System-Only</span></span>            | <span data-ttu-id="99f72-206">Falso</span><span class="sxs-lookup"><span data-stu-id="99f72-206">False</span></span>                                                         |
| <span data-ttu-id="99f72-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="99f72-207">Is-Single-Valued</span></span>       | <span data-ttu-id="99f72-208">True</span><span class="sxs-lookup"><span data-stu-id="99f72-208">True</span></span>                                                          |
| <span data-ttu-id="99f72-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="99f72-209">Is Indexed</span></span>             | <span data-ttu-id="99f72-210">Falso</span><span class="sxs-lookup"><span data-stu-id="99f72-210">False</span></span>                                                         |
| <span data-ttu-id="99f72-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="99f72-211">In Global Catalog</span></span>      | <span data-ttu-id="99f72-212">Falso</span><span class="sxs-lookup"><span data-stu-id="99f72-212">False</span></span>                                                         |
| <span data-ttu-id="99f72-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="99f72-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="99f72-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="99f72-214">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="99f72-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99f72-215">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="99f72-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99f72-216">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="99f72-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99f72-217">Search-Flags</span></span>           | <span data-ttu-id="99f72-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99f72-218">0x00000000</span></span>                                                    |
| <span data-ttu-id="99f72-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99f72-219">System-Flags</span></span>           | <span data-ttu-id="99f72-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99f72-220">0x00000010</span></span>                                                    |
| <span data-ttu-id="99f72-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="99f72-221">Classes used in</span></span>        | [<span data-ttu-id="99f72-222">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="99f72-222">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="99f72-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="99f72-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="99f72-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="99f72-224">Entry</span></span> | <span data-ttu-id="99f72-225">Valor</span><span class="sxs-lookup"><span data-stu-id="99f72-225">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="99f72-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="99f72-226">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="99f72-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99f72-227">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="99f72-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="99f72-228">System-Only</span></span>            | <span data-ttu-id="99f72-229">Falso</span><span class="sxs-lookup"><span data-stu-id="99f72-229">False</span></span>                                                         |
| <span data-ttu-id="99f72-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="99f72-230">Is-Single-Valued</span></span>       | <span data-ttu-id="99f72-231">True</span><span class="sxs-lookup"><span data-stu-id="99f72-231">True</span></span>                                                          |
| <span data-ttu-id="99f72-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="99f72-232">Is Indexed</span></span>             | <span data-ttu-id="99f72-233">Falso</span><span class="sxs-lookup"><span data-stu-id="99f72-233">False</span></span>                                                         |
| <span data-ttu-id="99f72-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="99f72-234">In Global Catalog</span></span>      | <span data-ttu-id="99f72-235">Falso</span><span class="sxs-lookup"><span data-stu-id="99f72-235">False</span></span>                                                         |
| <span data-ttu-id="99f72-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="99f72-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="99f72-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="99f72-237">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="99f72-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99f72-238">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="99f72-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99f72-239">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="99f72-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99f72-240">Search-Flags</span></span>           | <span data-ttu-id="99f72-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99f72-241">0x00000000</span></span>                                                    |
| <span data-ttu-id="99f72-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99f72-242">System-Flags</span></span>           | <span data-ttu-id="99f72-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99f72-243">0x00000010</span></span>                                                    |
| <span data-ttu-id="99f72-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="99f72-244">Classes used in</span></span>        | [<span data-ttu-id="99f72-245">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="99f72-245">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="99f72-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="99f72-246">Windows Server 2012</span></span>



| <span data-ttu-id="99f72-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="99f72-247">Entry</span></span> | <span data-ttu-id="99f72-248">Valor</span><span class="sxs-lookup"><span data-stu-id="99f72-248">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="99f72-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="99f72-249">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="99f72-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99f72-250">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="99f72-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="99f72-251">System-Only</span></span>            | <span data-ttu-id="99f72-252">Falso</span><span class="sxs-lookup"><span data-stu-id="99f72-252">False</span></span>                                                         |
| <span data-ttu-id="99f72-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="99f72-253">Is-Single-Valued</span></span>       | <span data-ttu-id="99f72-254">True</span><span class="sxs-lookup"><span data-stu-id="99f72-254">True</span></span>                                                          |
| <span data-ttu-id="99f72-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="99f72-255">Is Indexed</span></span>             | <span data-ttu-id="99f72-256">Falso</span><span class="sxs-lookup"><span data-stu-id="99f72-256">False</span></span>                                                         |
| <span data-ttu-id="99f72-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="99f72-257">In Global Catalog</span></span>      | <span data-ttu-id="99f72-258">Falso</span><span class="sxs-lookup"><span data-stu-id="99f72-258">False</span></span>                                                         |
| <span data-ttu-id="99f72-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="99f72-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="99f72-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="99f72-260">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="99f72-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99f72-261">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="99f72-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99f72-262">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="99f72-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99f72-263">Search-Flags</span></span>           | <span data-ttu-id="99f72-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99f72-264">0x00000000</span></span>                                                    |
| <span data-ttu-id="99f72-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99f72-265">System-Flags</span></span>           | <span data-ttu-id="99f72-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99f72-266">0x00000010</span></span>                                                    |
| <span data-ttu-id="99f72-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="99f72-267">Classes used in</span></span>        | [<span data-ttu-id="99f72-268">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="99f72-268">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



 

 





