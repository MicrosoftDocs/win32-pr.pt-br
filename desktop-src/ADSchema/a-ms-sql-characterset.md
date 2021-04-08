---
title: Atributo MS-SQL-CharacterSet
description: O conjunto de caracteres da instância atual do SQL Server.
ms.assetid: 5c45058f-e883-455c-8e18-415ddae149f8
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo MS-SQL-CharacterSet
- Esquema de AD do atributo mS-SQL-CharacterSet
topic_type:
- apiref
api_name:
- MS-SQL-CharacterSet
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f2f3718c9e47393498e42c4091283ea768d5072
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825401"
---
# <a name="ms-sql-characterset-attribute"></a><span data-ttu-id="9c56a-105">Atributo MS-SQL-CharacterSet</span><span class="sxs-lookup"><span data-stu-id="9c56a-105">MS-SQL-CharacterSet attribute</span></span>

<span data-ttu-id="9c56a-106">O conjunto de caracteres da instância atual do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9c56a-106">The character set for the current instance of SQL Server.</span></span>



| <span data-ttu-id="9c56a-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="9c56a-107">Entry</span></span> | <span data-ttu-id="9c56a-108">Valor</span><span class="sxs-lookup"><span data-stu-id="9c56a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9c56a-109">CN</span><span class="sxs-lookup"><span data-stu-id="9c56a-109">CN</span></span>                | <span data-ttu-id="9c56a-110">MS-SQL-CharacterSet</span><span class="sxs-lookup"><span data-stu-id="9c56a-110">MS-SQL-CharacterSet</span></span>                  |
| <span data-ttu-id="9c56a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9c56a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9c56a-112">mS-SQL-CharacterSet</span><span class="sxs-lookup"><span data-stu-id="9c56a-112">mS-SQL-CharacterSet</span></span>                  |
| <span data-ttu-id="9c56a-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="9c56a-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="9c56a-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="9c56a-114">Update Privilege</span></span>  | <span data-ttu-id="9c56a-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="9c56a-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="9c56a-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="9c56a-116">Update Frequency</span></span>  | <span data-ttu-id="9c56a-117">Na inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="9c56a-117">At system startup.</span></span>                   |
| <span data-ttu-id="9c56a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9c56a-118">Attribute-Id</span></span>      | <span data-ttu-id="9c56a-119">1.2.840.113556.1.4.1370</span><span class="sxs-lookup"><span data-stu-id="9c56a-119">1.2.840.113556.1.4.1370</span></span>              |
| <span data-ttu-id="9c56a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9c56a-120">System-Id-Guid</span></span>    | <span data-ttu-id="9c56a-121">696177a6-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="9c56a-121">696177a6-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="9c56a-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c56a-122">Syntax</span></span>            | [<span data-ttu-id="9c56a-123">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="9c56a-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="9c56a-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="9c56a-124">Implementations</span></span>

-   [<span data-ttu-id="9c56a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9c56a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9c56a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9c56a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9c56a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9c56a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9c56a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9c56a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9c56a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9c56a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9c56a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9c56a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9c56a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9c56a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="9c56a-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="9c56a-132">Entry</span></span> | <span data-ttu-id="9c56a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="9c56a-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9c56a-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="9c56a-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9c56a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c56a-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9c56a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c56a-136">System-Only</span></span>            | <span data-ttu-id="9c56a-137">Falso</span><span class="sxs-lookup"><span data-stu-id="9c56a-137">False</span></span>                                                     |
| <span data-ttu-id="9c56a-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9c56a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9c56a-139">True</span><span class="sxs-lookup"><span data-stu-id="9c56a-139">True</span></span>                                                      |
| <span data-ttu-id="9c56a-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="9c56a-140">Is Indexed</span></span>             | <span data-ttu-id="9c56a-141">Falso</span><span class="sxs-lookup"><span data-stu-id="9c56a-141">False</span></span>                                                     |
| <span data-ttu-id="9c56a-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9c56a-142">In Global Catalog</span></span>      | <span data-ttu-id="9c56a-143">Falso</span><span class="sxs-lookup"><span data-stu-id="9c56a-143">False</span></span>                                                     |
| <span data-ttu-id="9c56a-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9c56a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c56a-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9c56a-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="9c56a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c56a-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="9c56a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c56a-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="9c56a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c56a-148">Search-Flags</span></span>           | <span data-ttu-id="9c56a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c56a-149">0x00000000</span></span>                                                |
| <span data-ttu-id="9c56a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c56a-150">System-Flags</span></span>           | <span data-ttu-id="9c56a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c56a-151">0x00000010</span></span>                                                |
| <span data-ttu-id="9c56a-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9c56a-152">Classes used in</span></span>        | [<span data-ttu-id="9c56a-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="9c56a-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9c56a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9c56a-154">Windows Server 2003</span></span>



| <span data-ttu-id="9c56a-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="9c56a-155">Entry</span></span> | <span data-ttu-id="9c56a-156">Valor</span><span class="sxs-lookup"><span data-stu-id="9c56a-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9c56a-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="9c56a-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9c56a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c56a-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9c56a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c56a-159">System-Only</span></span>            | <span data-ttu-id="9c56a-160">Falso</span><span class="sxs-lookup"><span data-stu-id="9c56a-160">False</span></span>                                                     |
| <span data-ttu-id="9c56a-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9c56a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9c56a-162">True</span><span class="sxs-lookup"><span data-stu-id="9c56a-162">True</span></span>                                                      |
| <span data-ttu-id="9c56a-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="9c56a-163">Is Indexed</span></span>             | <span data-ttu-id="9c56a-164">Falso</span><span class="sxs-lookup"><span data-stu-id="9c56a-164">False</span></span>                                                     |
| <span data-ttu-id="9c56a-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9c56a-165">In Global Catalog</span></span>      | <span data-ttu-id="9c56a-166">Falso</span><span class="sxs-lookup"><span data-stu-id="9c56a-166">False</span></span>                                                     |
| <span data-ttu-id="9c56a-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9c56a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c56a-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9c56a-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="9c56a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c56a-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="9c56a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c56a-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="9c56a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c56a-171">Search-Flags</span></span>           | <span data-ttu-id="9c56a-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c56a-172">0x00000000</span></span>                                                |
| <span data-ttu-id="9c56a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c56a-173">System-Flags</span></span>           | <span data-ttu-id="9c56a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c56a-174">0x00000010</span></span>                                                |
| <span data-ttu-id="9c56a-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9c56a-175">Classes used in</span></span>        | [<span data-ttu-id="9c56a-176">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="9c56a-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9c56a-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9c56a-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9c56a-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="9c56a-178">Entry</span></span> | <span data-ttu-id="9c56a-179">Valor</span><span class="sxs-lookup"><span data-stu-id="9c56a-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9c56a-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="9c56a-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9c56a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c56a-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9c56a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c56a-182">System-Only</span></span>            | <span data-ttu-id="9c56a-183">Falso</span><span class="sxs-lookup"><span data-stu-id="9c56a-183">False</span></span>                                                     |
| <span data-ttu-id="9c56a-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9c56a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9c56a-185">True</span><span class="sxs-lookup"><span data-stu-id="9c56a-185">True</span></span>                                                      |
| <span data-ttu-id="9c56a-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="9c56a-186">Is Indexed</span></span>             | <span data-ttu-id="9c56a-187">Falso</span><span class="sxs-lookup"><span data-stu-id="9c56a-187">False</span></span>                                                     |
| <span data-ttu-id="9c56a-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9c56a-188">In Global Catalog</span></span>      | <span data-ttu-id="9c56a-189">Falso</span><span class="sxs-lookup"><span data-stu-id="9c56a-189">False</span></span>                                                     |
| <span data-ttu-id="9c56a-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9c56a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c56a-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9c56a-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="9c56a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c56a-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="9c56a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c56a-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="9c56a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c56a-194">Search-Flags</span></span>           | <span data-ttu-id="9c56a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c56a-195">0x00000000</span></span>                                                |
| <span data-ttu-id="9c56a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c56a-196">System-Flags</span></span>           | <span data-ttu-id="9c56a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c56a-197">0x00000010</span></span>                                                |
| <span data-ttu-id="9c56a-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9c56a-198">Classes used in</span></span>        | [<span data-ttu-id="9c56a-199">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="9c56a-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9c56a-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c56a-200">Windows Server 2008</span></span>



| <span data-ttu-id="9c56a-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="9c56a-201">Entry</span></span> | <span data-ttu-id="9c56a-202">Valor</span><span class="sxs-lookup"><span data-stu-id="9c56a-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9c56a-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="9c56a-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9c56a-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c56a-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9c56a-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c56a-205">System-Only</span></span>            | <span data-ttu-id="9c56a-206">Falso</span><span class="sxs-lookup"><span data-stu-id="9c56a-206">False</span></span>                                                     |
| <span data-ttu-id="9c56a-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9c56a-207">Is-Single-Valued</span></span>       | <span data-ttu-id="9c56a-208">True</span><span class="sxs-lookup"><span data-stu-id="9c56a-208">True</span></span>                                                      |
| <span data-ttu-id="9c56a-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="9c56a-209">Is Indexed</span></span>             | <span data-ttu-id="9c56a-210">Falso</span><span class="sxs-lookup"><span data-stu-id="9c56a-210">False</span></span>                                                     |
| <span data-ttu-id="9c56a-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9c56a-211">In Global Catalog</span></span>      | <span data-ttu-id="9c56a-212">Falso</span><span class="sxs-lookup"><span data-stu-id="9c56a-212">False</span></span>                                                     |
| <span data-ttu-id="9c56a-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9c56a-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c56a-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9c56a-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="9c56a-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c56a-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="9c56a-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c56a-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="9c56a-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c56a-217">Search-Flags</span></span>           | <span data-ttu-id="9c56a-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c56a-218">0x00000000</span></span>                                                |
| <span data-ttu-id="9c56a-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c56a-219">System-Flags</span></span>           | <span data-ttu-id="9c56a-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c56a-220">0x00000010</span></span>                                                |
| <span data-ttu-id="9c56a-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9c56a-221">Classes used in</span></span>        | [<span data-ttu-id="9c56a-222">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="9c56a-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9c56a-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9c56a-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9c56a-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="9c56a-224">Entry</span></span> | <span data-ttu-id="9c56a-225">Valor</span><span class="sxs-lookup"><span data-stu-id="9c56a-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9c56a-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="9c56a-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9c56a-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c56a-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9c56a-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c56a-228">System-Only</span></span>            | <span data-ttu-id="9c56a-229">Falso</span><span class="sxs-lookup"><span data-stu-id="9c56a-229">False</span></span>                                                     |
| <span data-ttu-id="9c56a-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9c56a-230">Is-Single-Valued</span></span>       | <span data-ttu-id="9c56a-231">True</span><span class="sxs-lookup"><span data-stu-id="9c56a-231">True</span></span>                                                      |
| <span data-ttu-id="9c56a-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="9c56a-232">Is Indexed</span></span>             | <span data-ttu-id="9c56a-233">Falso</span><span class="sxs-lookup"><span data-stu-id="9c56a-233">False</span></span>                                                     |
| <span data-ttu-id="9c56a-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9c56a-234">In Global Catalog</span></span>      | <span data-ttu-id="9c56a-235">Falso</span><span class="sxs-lookup"><span data-stu-id="9c56a-235">False</span></span>                                                     |
| <span data-ttu-id="9c56a-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9c56a-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c56a-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9c56a-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="9c56a-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c56a-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="9c56a-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c56a-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="9c56a-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c56a-240">Search-Flags</span></span>           | <span data-ttu-id="9c56a-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c56a-241">0x00000000</span></span>                                                |
| <span data-ttu-id="9c56a-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c56a-242">System-Flags</span></span>           | <span data-ttu-id="9c56a-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c56a-243">0x00000010</span></span>                                                |
| <span data-ttu-id="9c56a-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9c56a-244">Classes used in</span></span>        | [<span data-ttu-id="9c56a-245">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="9c56a-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9c56a-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c56a-246">Windows Server 2012</span></span>



| <span data-ttu-id="9c56a-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="9c56a-247">Entry</span></span> | <span data-ttu-id="9c56a-248">Valor</span><span class="sxs-lookup"><span data-stu-id="9c56a-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9c56a-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="9c56a-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9c56a-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c56a-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9c56a-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c56a-251">System-Only</span></span>            | <span data-ttu-id="9c56a-252">Falso</span><span class="sxs-lookup"><span data-stu-id="9c56a-252">False</span></span>                                                     |
| <span data-ttu-id="9c56a-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9c56a-253">Is-Single-Valued</span></span>       | <span data-ttu-id="9c56a-254">True</span><span class="sxs-lookup"><span data-stu-id="9c56a-254">True</span></span>                                                      |
| <span data-ttu-id="9c56a-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="9c56a-255">Is Indexed</span></span>             | <span data-ttu-id="9c56a-256">Falso</span><span class="sxs-lookup"><span data-stu-id="9c56a-256">False</span></span>                                                     |
| <span data-ttu-id="9c56a-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9c56a-257">In Global Catalog</span></span>      | <span data-ttu-id="9c56a-258">Falso</span><span class="sxs-lookup"><span data-stu-id="9c56a-258">False</span></span>                                                     |
| <span data-ttu-id="9c56a-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9c56a-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c56a-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9c56a-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="9c56a-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c56a-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="9c56a-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c56a-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="9c56a-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c56a-263">Search-Flags</span></span>           | <span data-ttu-id="9c56a-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c56a-264">0x00000000</span></span>                                                |
| <span data-ttu-id="9c56a-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c56a-265">System-Flags</span></span>           | <span data-ttu-id="9c56a-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c56a-266">0x00000010</span></span>                                                |
| <span data-ttu-id="9c56a-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9c56a-267">Classes used in</span></span>        | [<span data-ttu-id="9c56a-268">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="9c56a-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





