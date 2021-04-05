---
title: Atributo MS-SQL-Version
description: A versão da instância atual do SQL Server.
ms.assetid: 0003892c-906d-429b-bc98-bbc441b2d58b
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo MS-SQL-Version
- Esquema de AD do atributo mS-SQL-Version
topic_type:
- apiref
api_name:
- MS-SQL-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446a436a30311f5696d8ed63334b0cf796eb2767
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825393"
---
# <a name="ms-sql-version-attribute"></a><span data-ttu-id="7d893-105">Atributo MS-SQL-Version</span><span class="sxs-lookup"><span data-stu-id="7d893-105">MS-SQL-Version attribute</span></span>

<span data-ttu-id="7d893-106">A versão da instância atual do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7d893-106">The version for the current instance of SQL Server.</span></span>



| <span data-ttu-id="7d893-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="7d893-107">Entry</span></span> | <span data-ttu-id="7d893-108">Valor</span><span class="sxs-lookup"><span data-stu-id="7d893-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="7d893-109">CN</span><span class="sxs-lookup"><span data-stu-id="7d893-109">CN</span></span>                | <span data-ttu-id="7d893-110">Versão do MS-SQL</span><span class="sxs-lookup"><span data-stu-id="7d893-110">MS-SQL-Version</span></span>                              |
| <span data-ttu-id="7d893-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7d893-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7d893-112">Versão do mS-SQL</span><span class="sxs-lookup"><span data-stu-id="7d893-112">mS-SQL-Version</span></span>                              |
| <span data-ttu-id="7d893-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="7d893-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="7d893-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="7d893-114">Update Privilege</span></span>  | <span data-ttu-id="7d893-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="7d893-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="7d893-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="7d893-116">Update Frequency</span></span>  | <span data-ttu-id="7d893-117">Na configuração do sistema.</span><span class="sxs-lookup"><span data-stu-id="7d893-117">At system setup.</span></span>                            |
| <span data-ttu-id="7d893-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7d893-118">Attribute-Id</span></span>      | <span data-ttu-id="7d893-119">1.2.840.113556.1.4.1388</span><span class="sxs-lookup"><span data-stu-id="7d893-119">1.2.840.113556.1.4.1388</span></span>                     |
| <span data-ttu-id="7d893-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7d893-120">System-Id-Guid</span></span>    | <span data-ttu-id="7d893-121">c07cc1d0-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="7d893-121">c07cc1d0-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="7d893-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d893-122">Syntax</span></span>            | [<span data-ttu-id="7d893-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7d893-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="7d893-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="7d893-124">Implementations</span></span>

-   [<span data-ttu-id="7d893-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7d893-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7d893-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7d893-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7d893-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7d893-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7d893-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7d893-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7d893-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7d893-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7d893-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7d893-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7d893-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7d893-131">Windows 2000 Server</span></span>



| <span data-ttu-id="7d893-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="7d893-132">Entry</span></span> | <span data-ttu-id="7d893-133">Valor</span><span class="sxs-lookup"><span data-stu-id="7d893-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d893-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="7d893-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7d893-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d893-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7d893-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d893-136">System-Only</span></span>            | <span data-ttu-id="7d893-137">Falso</span><span class="sxs-lookup"><span data-stu-id="7d893-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="7d893-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7d893-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7d893-139">True</span><span class="sxs-lookup"><span data-stu-id="7d893-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="7d893-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="7d893-140">Is Indexed</span></span>             | <span data-ttu-id="7d893-141">True</span><span class="sxs-lookup"><span data-stu-id="7d893-141">True</span></span>                                                                                                                          |
| <span data-ttu-id="7d893-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7d893-142">In Global Catalog</span></span>      | <span data-ttu-id="7d893-143">True</span><span class="sxs-lookup"><span data-stu-id="7d893-143">True</span></span>                                                                                                                          |
| <span data-ttu-id="7d893-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7d893-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d893-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7d893-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="7d893-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d893-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7d893-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d893-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7d893-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d893-148">Search-Flags</span></span>           | <span data-ttu-id="7d893-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7d893-149">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="7d893-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d893-150">System-Flags</span></span>           | <span data-ttu-id="7d893-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d893-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="7d893-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7d893-152">Classes used in</span></span>        | [<span data-ttu-id="7d893-153">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="7d893-153">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="7d893-154">**MS-SQL-sqlrepository**</span><span class="sxs-lookup"><span data-stu-id="7d893-154">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7d893-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7d893-155">Windows Server 2003</span></span>



| <span data-ttu-id="7d893-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="7d893-156">Entry</span></span> | <span data-ttu-id="7d893-157">Valor</span><span class="sxs-lookup"><span data-stu-id="7d893-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d893-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="7d893-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7d893-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d893-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7d893-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d893-160">System-Only</span></span>            | <span data-ttu-id="7d893-161">Falso</span><span class="sxs-lookup"><span data-stu-id="7d893-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="7d893-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7d893-162">Is-Single-Valued</span></span>       | <span data-ttu-id="7d893-163">True</span><span class="sxs-lookup"><span data-stu-id="7d893-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="7d893-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="7d893-164">Is Indexed</span></span>             | <span data-ttu-id="7d893-165">True</span><span class="sxs-lookup"><span data-stu-id="7d893-165">True</span></span>                                                                                                                          |
| <span data-ttu-id="7d893-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7d893-166">In Global Catalog</span></span>      | <span data-ttu-id="7d893-167">True</span><span class="sxs-lookup"><span data-stu-id="7d893-167">True</span></span>                                                                                                                          |
| <span data-ttu-id="7d893-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7d893-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d893-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7d893-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="7d893-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d893-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7d893-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d893-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7d893-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d893-172">Search-Flags</span></span>           | <span data-ttu-id="7d893-173">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7d893-173">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="7d893-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d893-174">System-Flags</span></span>           | <span data-ttu-id="7d893-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d893-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="7d893-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7d893-176">Classes used in</span></span>        | [<span data-ttu-id="7d893-177">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="7d893-177">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="7d893-178">**MS-SQL-sqlrepository**</span><span class="sxs-lookup"><span data-stu-id="7d893-178">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7d893-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7d893-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7d893-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="7d893-180">Entry</span></span> | <span data-ttu-id="7d893-181">Valor</span><span class="sxs-lookup"><span data-stu-id="7d893-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d893-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="7d893-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7d893-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d893-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7d893-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d893-184">System-Only</span></span>            | <span data-ttu-id="7d893-185">Falso</span><span class="sxs-lookup"><span data-stu-id="7d893-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="7d893-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7d893-186">Is-Single-Valued</span></span>       | <span data-ttu-id="7d893-187">True</span><span class="sxs-lookup"><span data-stu-id="7d893-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="7d893-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="7d893-188">Is Indexed</span></span>             | <span data-ttu-id="7d893-189">True</span><span class="sxs-lookup"><span data-stu-id="7d893-189">True</span></span>                                                                                                                          |
| <span data-ttu-id="7d893-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7d893-190">In Global Catalog</span></span>      | <span data-ttu-id="7d893-191">True</span><span class="sxs-lookup"><span data-stu-id="7d893-191">True</span></span>                                                                                                                          |
| <span data-ttu-id="7d893-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7d893-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d893-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7d893-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="7d893-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d893-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7d893-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d893-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7d893-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d893-196">Search-Flags</span></span>           | <span data-ttu-id="7d893-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7d893-197">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="7d893-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d893-198">System-Flags</span></span>           | <span data-ttu-id="7d893-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d893-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="7d893-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7d893-200">Classes used in</span></span>        | [<span data-ttu-id="7d893-201">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="7d893-201">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="7d893-202">**MS-SQL-sqlrepository**</span><span class="sxs-lookup"><span data-stu-id="7d893-202">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7d893-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d893-203">Windows Server 2008</span></span>



| <span data-ttu-id="7d893-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="7d893-204">Entry</span></span> | <span data-ttu-id="7d893-205">Valor</span><span class="sxs-lookup"><span data-stu-id="7d893-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d893-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="7d893-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7d893-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d893-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7d893-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d893-208">System-Only</span></span>            | <span data-ttu-id="7d893-209">Falso</span><span class="sxs-lookup"><span data-stu-id="7d893-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="7d893-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7d893-210">Is-Single-Valued</span></span>       | <span data-ttu-id="7d893-211">True</span><span class="sxs-lookup"><span data-stu-id="7d893-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="7d893-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="7d893-212">Is Indexed</span></span>             | <span data-ttu-id="7d893-213">True</span><span class="sxs-lookup"><span data-stu-id="7d893-213">True</span></span>                                                                                                                          |
| <span data-ttu-id="7d893-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7d893-214">In Global Catalog</span></span>      | <span data-ttu-id="7d893-215">True</span><span class="sxs-lookup"><span data-stu-id="7d893-215">True</span></span>                                                                                                                          |
| <span data-ttu-id="7d893-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7d893-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d893-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7d893-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="7d893-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d893-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7d893-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d893-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7d893-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d893-220">Search-Flags</span></span>           | <span data-ttu-id="7d893-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7d893-221">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="7d893-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d893-222">System-Flags</span></span>           | <span data-ttu-id="7d893-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d893-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="7d893-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7d893-224">Classes used in</span></span>        | [<span data-ttu-id="7d893-225">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="7d893-225">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="7d893-226">**MS-SQL-sqlrepository**</span><span class="sxs-lookup"><span data-stu-id="7d893-226">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7d893-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7d893-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7d893-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="7d893-228">Entry</span></span> | <span data-ttu-id="7d893-229">Valor</span><span class="sxs-lookup"><span data-stu-id="7d893-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d893-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="7d893-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7d893-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d893-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7d893-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d893-232">System-Only</span></span>            | <span data-ttu-id="7d893-233">Falso</span><span class="sxs-lookup"><span data-stu-id="7d893-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="7d893-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7d893-234">Is-Single-Valued</span></span>       | <span data-ttu-id="7d893-235">True</span><span class="sxs-lookup"><span data-stu-id="7d893-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="7d893-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="7d893-236">Is Indexed</span></span>             | <span data-ttu-id="7d893-237">True</span><span class="sxs-lookup"><span data-stu-id="7d893-237">True</span></span>                                                                                                                          |
| <span data-ttu-id="7d893-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7d893-238">In Global Catalog</span></span>      | <span data-ttu-id="7d893-239">True</span><span class="sxs-lookup"><span data-stu-id="7d893-239">True</span></span>                                                                                                                          |
| <span data-ttu-id="7d893-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7d893-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d893-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7d893-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="7d893-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d893-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7d893-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d893-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7d893-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d893-244">Search-Flags</span></span>           | <span data-ttu-id="7d893-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7d893-245">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="7d893-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d893-246">System-Flags</span></span>           | <span data-ttu-id="7d893-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d893-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="7d893-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7d893-248">Classes used in</span></span>        | [<span data-ttu-id="7d893-249">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="7d893-249">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="7d893-250">**MS-SQL-sqlrepository**</span><span class="sxs-lookup"><span data-stu-id="7d893-250">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7d893-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7d893-251">Windows Server 2012</span></span>



| <span data-ttu-id="7d893-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="7d893-252">Entry</span></span> | <span data-ttu-id="7d893-253">Valor</span><span class="sxs-lookup"><span data-stu-id="7d893-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d893-254">ID do link</span><span class="sxs-lookup"><span data-stu-id="7d893-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7d893-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d893-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7d893-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d893-256">System-Only</span></span>            | <span data-ttu-id="7d893-257">Falso</span><span class="sxs-lookup"><span data-stu-id="7d893-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="7d893-258">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7d893-258">Is-Single-Valued</span></span>       | <span data-ttu-id="7d893-259">True</span><span class="sxs-lookup"><span data-stu-id="7d893-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="7d893-260">É indexado</span><span class="sxs-lookup"><span data-stu-id="7d893-260">Is Indexed</span></span>             | <span data-ttu-id="7d893-261">True</span><span class="sxs-lookup"><span data-stu-id="7d893-261">True</span></span>                                                                                                                          |
| <span data-ttu-id="7d893-262">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7d893-262">In Global Catalog</span></span>      | <span data-ttu-id="7d893-263">True</span><span class="sxs-lookup"><span data-stu-id="7d893-263">True</span></span>                                                                                                                          |
| <span data-ttu-id="7d893-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7d893-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d893-265">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7d893-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="7d893-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d893-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7d893-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d893-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7d893-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d893-268">Search-Flags</span></span>           | <span data-ttu-id="7d893-269">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7d893-269">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="7d893-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d893-270">System-Flags</span></span>           | <span data-ttu-id="7d893-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d893-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="7d893-272">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7d893-272">Classes used in</span></span>        | [<span data-ttu-id="7d893-273">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="7d893-273">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="7d893-274">**MS-SQL-sqlrepository**</span><span class="sxs-lookup"><span data-stu-id="7d893-274">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



 

 





