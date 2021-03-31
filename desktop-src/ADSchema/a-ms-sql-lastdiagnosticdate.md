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
# <a name="ms-sql-lastdiagnosticdate-attribute"></a><span data-ttu-id="75c9a-105">Atributo MS-SQL-LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="75c9a-105">MS-SQL-LastDiagnosticDate attribute</span></span>

<span data-ttu-id="75c9a-106">A última data em que o DBCC CHECKDB foi executado.</span><span class="sxs-lookup"><span data-stu-id="75c9a-106">The last date that DBCC checkdb was run.</span></span>



| <span data-ttu-id="75c9a-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="75c9a-107">Entry</span></span> | <span data-ttu-id="75c9a-108">Valor</span><span class="sxs-lookup"><span data-stu-id="75c9a-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="75c9a-109">CN</span><span class="sxs-lookup"><span data-stu-id="75c9a-109">CN</span></span>                | <span data-ttu-id="75c9a-110">MS-SQL-LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="75c9a-110">MS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="75c9a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="75c9a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="75c9a-112">mS-SQL-LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="75c9a-112">mS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="75c9a-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="75c9a-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="75c9a-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="75c9a-114">Update Privilege</span></span>  | <span data-ttu-id="75c9a-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="75c9a-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="75c9a-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="75c9a-116">Update Frequency</span></span>  | <span data-ttu-id="75c9a-117">Quando o DBCC CHECKDB é executado.</span><span class="sxs-lookup"><span data-stu-id="75c9a-117">When DBCC checkdb is run.</span></span>                   |
| <span data-ttu-id="75c9a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="75c9a-118">Attribute-Id</span></span>      | <span data-ttu-id="75c9a-119">1.2.840.113556.1.4.1399</span><span class="sxs-lookup"><span data-stu-id="75c9a-119">1.2.840.113556.1.4.1399</span></span>                     |
| <span data-ttu-id="75c9a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="75c9a-120">System-Id-Guid</span></span>    | <span data-ttu-id="75c9a-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="75c9a-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="75c9a-122">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75c9a-122">Syntax</span></span>            | [<span data-ttu-id="75c9a-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="75c9a-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="75c9a-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="75c9a-124">Implementations</span></span>

-   [<span data-ttu-id="75c9a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="75c9a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="75c9a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="75c9a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="75c9a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="75c9a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="75c9a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="75c9a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="75c9a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="75c9a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="75c9a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="75c9a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="75c9a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="75c9a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="75c9a-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="75c9a-132">Entry</span></span> | <span data-ttu-id="75c9a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="75c9a-133">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="75c9a-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="75c9a-134">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="75c9a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75c9a-135">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="75c9a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="75c9a-136">System-Only</span></span>            | <span data-ttu-id="75c9a-137">Falso</span><span class="sxs-lookup"><span data-stu-id="75c9a-137">False</span></span>                                                         |
| <span data-ttu-id="75c9a-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="75c9a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="75c9a-139">True</span><span class="sxs-lookup"><span data-stu-id="75c9a-139">True</span></span>                                                          |
| <span data-ttu-id="75c9a-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="75c9a-140">Is Indexed</span></span>             | <span data-ttu-id="75c9a-141">Falso</span><span class="sxs-lookup"><span data-stu-id="75c9a-141">False</span></span>                                                         |
| <span data-ttu-id="75c9a-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="75c9a-142">In Global Catalog</span></span>      | <span data-ttu-id="75c9a-143">Falso</span><span class="sxs-lookup"><span data-stu-id="75c9a-143">False</span></span>                                                         |
| <span data-ttu-id="75c9a-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="75c9a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="75c9a-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="75c9a-145">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="75c9a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75c9a-146">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="75c9a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75c9a-147">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="75c9a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75c9a-148">Search-Flags</span></span>           | <span data-ttu-id="75c9a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75c9a-149">0x00000000</span></span>                                                    |
| <span data-ttu-id="75c9a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75c9a-150">System-Flags</span></span>           | <span data-ttu-id="75c9a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75c9a-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="75c9a-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="75c9a-152">Classes used in</span></span>        | [<span data-ttu-id="75c9a-153">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="75c9a-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="75c9a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="75c9a-154">Windows Server 2003</span></span>



| <span data-ttu-id="75c9a-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="75c9a-155">Entry</span></span> | <span data-ttu-id="75c9a-156">Valor</span><span class="sxs-lookup"><span data-stu-id="75c9a-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="75c9a-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="75c9a-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="75c9a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75c9a-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="75c9a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="75c9a-159">System-Only</span></span>            | <span data-ttu-id="75c9a-160">Falso</span><span class="sxs-lookup"><span data-stu-id="75c9a-160">False</span></span>                                                         |
| <span data-ttu-id="75c9a-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="75c9a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="75c9a-162">True</span><span class="sxs-lookup"><span data-stu-id="75c9a-162">True</span></span>                                                          |
| <span data-ttu-id="75c9a-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="75c9a-163">Is Indexed</span></span>             | <span data-ttu-id="75c9a-164">Falso</span><span class="sxs-lookup"><span data-stu-id="75c9a-164">False</span></span>                                                         |
| <span data-ttu-id="75c9a-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="75c9a-165">In Global Catalog</span></span>      | <span data-ttu-id="75c9a-166">Falso</span><span class="sxs-lookup"><span data-stu-id="75c9a-166">False</span></span>                                                         |
| <span data-ttu-id="75c9a-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="75c9a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="75c9a-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="75c9a-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="75c9a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75c9a-169">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="75c9a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75c9a-170">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="75c9a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75c9a-171">Search-Flags</span></span>           | <span data-ttu-id="75c9a-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75c9a-172">0x00000000</span></span>                                                    |
| <span data-ttu-id="75c9a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75c9a-173">System-Flags</span></span>           | <span data-ttu-id="75c9a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75c9a-174">0x00000010</span></span>                                                    |
| <span data-ttu-id="75c9a-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="75c9a-175">Classes used in</span></span>        | [<span data-ttu-id="75c9a-176">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="75c9a-176">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="75c9a-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="75c9a-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="75c9a-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="75c9a-178">Entry</span></span> | <span data-ttu-id="75c9a-179">Valor</span><span class="sxs-lookup"><span data-stu-id="75c9a-179">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="75c9a-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="75c9a-180">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="75c9a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75c9a-181">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="75c9a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="75c9a-182">System-Only</span></span>            | <span data-ttu-id="75c9a-183">Falso</span><span class="sxs-lookup"><span data-stu-id="75c9a-183">False</span></span>                                                         |
| <span data-ttu-id="75c9a-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="75c9a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="75c9a-185">True</span><span class="sxs-lookup"><span data-stu-id="75c9a-185">True</span></span>                                                          |
| <span data-ttu-id="75c9a-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="75c9a-186">Is Indexed</span></span>             | <span data-ttu-id="75c9a-187">Falso</span><span class="sxs-lookup"><span data-stu-id="75c9a-187">False</span></span>                                                         |
| <span data-ttu-id="75c9a-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="75c9a-188">In Global Catalog</span></span>      | <span data-ttu-id="75c9a-189">Falso</span><span class="sxs-lookup"><span data-stu-id="75c9a-189">False</span></span>                                                         |
| <span data-ttu-id="75c9a-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="75c9a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="75c9a-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="75c9a-191">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="75c9a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75c9a-192">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="75c9a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75c9a-193">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="75c9a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75c9a-194">Search-Flags</span></span>           | <span data-ttu-id="75c9a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75c9a-195">0x00000000</span></span>                                                    |
| <span data-ttu-id="75c9a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75c9a-196">System-Flags</span></span>           | <span data-ttu-id="75c9a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75c9a-197">0x00000010</span></span>                                                    |
| <span data-ttu-id="75c9a-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="75c9a-198">Classes used in</span></span>        | [<span data-ttu-id="75c9a-199">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="75c9a-199">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="75c9a-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75c9a-200">Windows Server 2008</span></span>



| <span data-ttu-id="75c9a-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="75c9a-201">Entry</span></span> | <span data-ttu-id="75c9a-202">Valor</span><span class="sxs-lookup"><span data-stu-id="75c9a-202">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="75c9a-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="75c9a-203">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="75c9a-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75c9a-204">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="75c9a-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="75c9a-205">System-Only</span></span>            | <span data-ttu-id="75c9a-206">Falso</span><span class="sxs-lookup"><span data-stu-id="75c9a-206">False</span></span>                                                         |
| <span data-ttu-id="75c9a-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="75c9a-207">Is-Single-Valued</span></span>       | <span data-ttu-id="75c9a-208">True</span><span class="sxs-lookup"><span data-stu-id="75c9a-208">True</span></span>                                                          |
| <span data-ttu-id="75c9a-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="75c9a-209">Is Indexed</span></span>             | <span data-ttu-id="75c9a-210">Falso</span><span class="sxs-lookup"><span data-stu-id="75c9a-210">False</span></span>                                                         |
| <span data-ttu-id="75c9a-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="75c9a-211">In Global Catalog</span></span>      | <span data-ttu-id="75c9a-212">Falso</span><span class="sxs-lookup"><span data-stu-id="75c9a-212">False</span></span>                                                         |
| <span data-ttu-id="75c9a-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="75c9a-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="75c9a-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="75c9a-214">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="75c9a-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75c9a-215">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="75c9a-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75c9a-216">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="75c9a-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75c9a-217">Search-Flags</span></span>           | <span data-ttu-id="75c9a-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75c9a-218">0x00000000</span></span>                                                    |
| <span data-ttu-id="75c9a-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75c9a-219">System-Flags</span></span>           | <span data-ttu-id="75c9a-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75c9a-220">0x00000010</span></span>                                                    |
| <span data-ttu-id="75c9a-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="75c9a-221">Classes used in</span></span>        | [<span data-ttu-id="75c9a-222">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="75c9a-222">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="75c9a-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="75c9a-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="75c9a-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="75c9a-224">Entry</span></span> | <span data-ttu-id="75c9a-225">Valor</span><span class="sxs-lookup"><span data-stu-id="75c9a-225">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="75c9a-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="75c9a-226">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="75c9a-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75c9a-227">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="75c9a-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="75c9a-228">System-Only</span></span>            | <span data-ttu-id="75c9a-229">Falso</span><span class="sxs-lookup"><span data-stu-id="75c9a-229">False</span></span>                                                         |
| <span data-ttu-id="75c9a-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="75c9a-230">Is-Single-Valued</span></span>       | <span data-ttu-id="75c9a-231">True</span><span class="sxs-lookup"><span data-stu-id="75c9a-231">True</span></span>                                                          |
| <span data-ttu-id="75c9a-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="75c9a-232">Is Indexed</span></span>             | <span data-ttu-id="75c9a-233">Falso</span><span class="sxs-lookup"><span data-stu-id="75c9a-233">False</span></span>                                                         |
| <span data-ttu-id="75c9a-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="75c9a-234">In Global Catalog</span></span>      | <span data-ttu-id="75c9a-235">Falso</span><span class="sxs-lookup"><span data-stu-id="75c9a-235">False</span></span>                                                         |
| <span data-ttu-id="75c9a-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="75c9a-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="75c9a-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="75c9a-237">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="75c9a-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75c9a-238">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="75c9a-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75c9a-239">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="75c9a-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75c9a-240">Search-Flags</span></span>           | <span data-ttu-id="75c9a-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75c9a-241">0x00000000</span></span>                                                    |
| <span data-ttu-id="75c9a-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75c9a-242">System-Flags</span></span>           | <span data-ttu-id="75c9a-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75c9a-243">0x00000010</span></span>                                                    |
| <span data-ttu-id="75c9a-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="75c9a-244">Classes used in</span></span>        | [<span data-ttu-id="75c9a-245">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="75c9a-245">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="75c9a-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="75c9a-246">Windows Server 2012</span></span>



| <span data-ttu-id="75c9a-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="75c9a-247">Entry</span></span> | <span data-ttu-id="75c9a-248">Valor</span><span class="sxs-lookup"><span data-stu-id="75c9a-248">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="75c9a-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="75c9a-249">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="75c9a-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75c9a-250">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="75c9a-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="75c9a-251">System-Only</span></span>            | <span data-ttu-id="75c9a-252">Falso</span><span class="sxs-lookup"><span data-stu-id="75c9a-252">False</span></span>                                                         |
| <span data-ttu-id="75c9a-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="75c9a-253">Is-Single-Valued</span></span>       | <span data-ttu-id="75c9a-254">True</span><span class="sxs-lookup"><span data-stu-id="75c9a-254">True</span></span>                                                          |
| <span data-ttu-id="75c9a-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="75c9a-255">Is Indexed</span></span>             | <span data-ttu-id="75c9a-256">Falso</span><span class="sxs-lookup"><span data-stu-id="75c9a-256">False</span></span>                                                         |
| <span data-ttu-id="75c9a-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="75c9a-257">In Global Catalog</span></span>      | <span data-ttu-id="75c9a-258">Falso</span><span class="sxs-lookup"><span data-stu-id="75c9a-258">False</span></span>                                                         |
| <span data-ttu-id="75c9a-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="75c9a-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="75c9a-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="75c9a-260">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="75c9a-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75c9a-261">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="75c9a-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75c9a-262">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="75c9a-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75c9a-263">Search-Flags</span></span>           | <span data-ttu-id="75c9a-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75c9a-264">0x00000000</span></span>                                                    |
| <span data-ttu-id="75c9a-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75c9a-265">System-Flags</span></span>           | <span data-ttu-id="75c9a-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75c9a-266">0x00000010</span></span>                                                    |
| <span data-ttu-id="75c9a-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="75c9a-267">Classes used in</span></span>        | [<span data-ttu-id="75c9a-268">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="75c9a-268">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



 

 





