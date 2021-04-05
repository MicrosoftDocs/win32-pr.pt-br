---
title: Atributo MS-SQL-RegisteredOwner
description: O proprietário registrado da instância atual do SQL Server.
ms.assetid: d07712e8-021d-40db-91ba-0fef7e89bb0f
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo MS-SQL-RegisteredOwner
- Esquema de AD do atributo mS-SQL-RegisteredOwner
topic_type:
- apiref
api_name:
- MS-SQL-RegisteredOwner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e201494afffdfea59b75bc1901a474469871351
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645575"
---
# <a name="ms-sql-registeredowner-attribute"></a><span data-ttu-id="e3299-105">Atributo MS-SQL-RegisteredOwner</span><span class="sxs-lookup"><span data-stu-id="e3299-105">MS-SQL-RegisteredOwner attribute</span></span>

<span data-ttu-id="e3299-106">O proprietário registrado da instância atual do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e3299-106">The registered owner for the current instance of SQL Server.</span></span>



| <span data-ttu-id="e3299-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3299-107">Entry</span></span> | <span data-ttu-id="e3299-108">Valor</span><span class="sxs-lookup"><span data-stu-id="e3299-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e3299-109">CN</span><span class="sxs-lookup"><span data-stu-id="e3299-109">CN</span></span>                | <span data-ttu-id="e3299-110">MS-SQL-RegisteredOwner</span><span class="sxs-lookup"><span data-stu-id="e3299-110">MS-SQL-RegisteredOwner</span></span>                      |
| <span data-ttu-id="e3299-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e3299-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e3299-112">mS-SQL-RegisteredOwner</span><span class="sxs-lookup"><span data-stu-id="e3299-112">mS-SQL-RegisteredOwner</span></span>                      |
| <span data-ttu-id="e3299-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="e3299-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="e3299-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="e3299-114">Update Privilege</span></span>  | <span data-ttu-id="e3299-115">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="e3299-115">Domain administrator</span></span>                        |
| <span data-ttu-id="e3299-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="e3299-116">Update Frequency</span></span>  | <span data-ttu-id="e3299-117">Na configuração do sistema.</span><span class="sxs-lookup"><span data-stu-id="e3299-117">At system setup.</span></span>                            |
| <span data-ttu-id="e3299-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e3299-118">Attribute-Id</span></span>      | <span data-ttu-id="e3299-119">1.2.840.113556.1.4.1364</span><span class="sxs-lookup"><span data-stu-id="e3299-119">1.2.840.113556.1.4.1364</span></span>                     |
| <span data-ttu-id="e3299-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e3299-120">System-Id-Guid</span></span>    | <span data-ttu-id="e3299-121">48fd44ea-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="e3299-121">48fd44ea-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="e3299-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3299-122">Syntax</span></span>            | [<span data-ttu-id="e3299-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e3299-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e3299-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="e3299-124">Implementations</span></span>

-   [<span data-ttu-id="e3299-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e3299-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e3299-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e3299-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e3299-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e3299-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e3299-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e3299-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e3299-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e3299-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e3299-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e3299-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e3299-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e3299-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e3299-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3299-132">Entry</span></span> | <span data-ttu-id="e3299-133">Valor</span><span class="sxs-lookup"><span data-stu-id="e3299-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3299-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="e3299-134">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="e3299-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3299-135">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="e3299-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3299-136">System-Only</span></span>            | <span data-ttu-id="e3299-137">Falso</span><span class="sxs-lookup"><span data-stu-id="e3299-137">False</span></span>                                                                                                                 |
| <span data-ttu-id="e3299-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e3299-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e3299-139">True</span><span class="sxs-lookup"><span data-stu-id="e3299-139">True</span></span>                                                                                                                  |
| <span data-ttu-id="e3299-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="e3299-140">Is Indexed</span></span>             | <span data-ttu-id="e3299-141">Falso</span><span class="sxs-lookup"><span data-stu-id="e3299-141">False</span></span>                                                                                                                 |
| <span data-ttu-id="e3299-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e3299-142">In Global Catalog</span></span>      | <span data-ttu-id="e3299-143">Falso</span><span class="sxs-lookup"><span data-stu-id="e3299-143">False</span></span>                                                                                                                 |
| <span data-ttu-id="e3299-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e3299-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3299-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e3299-145">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="e3299-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3299-146">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="e3299-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3299-147">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="e3299-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3299-148">Search-Flags</span></span>           | <span data-ttu-id="e3299-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3299-149">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="e3299-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3299-150">System-Flags</span></span>           | <span data-ttu-id="e3299-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3299-151">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="e3299-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e3299-152">Classes used in</span></span>        | [<span data-ttu-id="e3299-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e3299-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="e3299-154">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="e3299-154">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e3299-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e3299-155">Windows Server 2003</span></span>



| <span data-ttu-id="e3299-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3299-156">Entry</span></span> | <span data-ttu-id="e3299-157">Valor</span><span class="sxs-lookup"><span data-stu-id="e3299-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3299-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="e3299-158">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="e3299-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3299-159">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="e3299-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3299-160">System-Only</span></span>            | <span data-ttu-id="e3299-161">Falso</span><span class="sxs-lookup"><span data-stu-id="e3299-161">False</span></span>                                                                                                                 |
| <span data-ttu-id="e3299-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e3299-162">Is-Single-Valued</span></span>       | <span data-ttu-id="e3299-163">True</span><span class="sxs-lookup"><span data-stu-id="e3299-163">True</span></span>                                                                                                                  |
| <span data-ttu-id="e3299-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="e3299-164">Is Indexed</span></span>             | <span data-ttu-id="e3299-165">Falso</span><span class="sxs-lookup"><span data-stu-id="e3299-165">False</span></span>                                                                                                                 |
| <span data-ttu-id="e3299-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e3299-166">In Global Catalog</span></span>      | <span data-ttu-id="e3299-167">Falso</span><span class="sxs-lookup"><span data-stu-id="e3299-167">False</span></span>                                                                                                                 |
| <span data-ttu-id="e3299-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e3299-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3299-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e3299-169">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="e3299-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3299-170">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="e3299-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3299-171">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="e3299-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3299-172">Search-Flags</span></span>           | <span data-ttu-id="e3299-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3299-173">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="e3299-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3299-174">System-Flags</span></span>           | <span data-ttu-id="e3299-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3299-175">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="e3299-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e3299-176">Classes used in</span></span>        | [<span data-ttu-id="e3299-177">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e3299-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="e3299-178">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="e3299-178">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e3299-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e3299-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e3299-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3299-180">Entry</span></span> | <span data-ttu-id="e3299-181">Valor</span><span class="sxs-lookup"><span data-stu-id="e3299-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3299-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="e3299-182">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="e3299-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3299-183">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="e3299-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3299-184">System-Only</span></span>            | <span data-ttu-id="e3299-185">Falso</span><span class="sxs-lookup"><span data-stu-id="e3299-185">False</span></span>                                                                                                                 |
| <span data-ttu-id="e3299-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e3299-186">Is-Single-Valued</span></span>       | <span data-ttu-id="e3299-187">True</span><span class="sxs-lookup"><span data-stu-id="e3299-187">True</span></span>                                                                                                                  |
| <span data-ttu-id="e3299-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="e3299-188">Is Indexed</span></span>             | <span data-ttu-id="e3299-189">Falso</span><span class="sxs-lookup"><span data-stu-id="e3299-189">False</span></span>                                                                                                                 |
| <span data-ttu-id="e3299-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e3299-190">In Global Catalog</span></span>      | <span data-ttu-id="e3299-191">Falso</span><span class="sxs-lookup"><span data-stu-id="e3299-191">False</span></span>                                                                                                                 |
| <span data-ttu-id="e3299-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e3299-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3299-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e3299-193">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="e3299-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3299-194">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="e3299-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3299-195">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="e3299-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3299-196">Search-Flags</span></span>           | <span data-ttu-id="e3299-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3299-197">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="e3299-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3299-198">System-Flags</span></span>           | <span data-ttu-id="e3299-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3299-199">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="e3299-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e3299-200">Classes used in</span></span>        | [<span data-ttu-id="e3299-201">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e3299-201">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="e3299-202">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="e3299-202">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e3299-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3299-203">Windows Server 2008</span></span>



| <span data-ttu-id="e3299-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3299-204">Entry</span></span> | <span data-ttu-id="e3299-205">Valor</span><span class="sxs-lookup"><span data-stu-id="e3299-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3299-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="e3299-206">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="e3299-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3299-207">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="e3299-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3299-208">System-Only</span></span>            | <span data-ttu-id="e3299-209">Falso</span><span class="sxs-lookup"><span data-stu-id="e3299-209">False</span></span>                                                                                                                 |
| <span data-ttu-id="e3299-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e3299-210">Is-Single-Valued</span></span>       | <span data-ttu-id="e3299-211">True</span><span class="sxs-lookup"><span data-stu-id="e3299-211">True</span></span>                                                                                                                  |
| <span data-ttu-id="e3299-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="e3299-212">Is Indexed</span></span>             | <span data-ttu-id="e3299-213">Falso</span><span class="sxs-lookup"><span data-stu-id="e3299-213">False</span></span>                                                                                                                 |
| <span data-ttu-id="e3299-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e3299-214">In Global Catalog</span></span>      | <span data-ttu-id="e3299-215">Falso</span><span class="sxs-lookup"><span data-stu-id="e3299-215">False</span></span>                                                                                                                 |
| <span data-ttu-id="e3299-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e3299-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3299-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e3299-217">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="e3299-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3299-218">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="e3299-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3299-219">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="e3299-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3299-220">Search-Flags</span></span>           | <span data-ttu-id="e3299-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3299-221">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="e3299-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3299-222">System-Flags</span></span>           | <span data-ttu-id="e3299-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3299-223">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="e3299-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e3299-224">Classes used in</span></span>        | [<span data-ttu-id="e3299-225">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e3299-225">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="e3299-226">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="e3299-226">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e3299-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e3299-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e3299-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3299-228">Entry</span></span> | <span data-ttu-id="e3299-229">Valor</span><span class="sxs-lookup"><span data-stu-id="e3299-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3299-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="e3299-230">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="e3299-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3299-231">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="e3299-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3299-232">System-Only</span></span>            | <span data-ttu-id="e3299-233">Falso</span><span class="sxs-lookup"><span data-stu-id="e3299-233">False</span></span>                                                                                                                 |
| <span data-ttu-id="e3299-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e3299-234">Is-Single-Valued</span></span>       | <span data-ttu-id="e3299-235">True</span><span class="sxs-lookup"><span data-stu-id="e3299-235">True</span></span>                                                                                                                  |
| <span data-ttu-id="e3299-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="e3299-236">Is Indexed</span></span>             | <span data-ttu-id="e3299-237">Falso</span><span class="sxs-lookup"><span data-stu-id="e3299-237">False</span></span>                                                                                                                 |
| <span data-ttu-id="e3299-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e3299-238">In Global Catalog</span></span>      | <span data-ttu-id="e3299-239">Falso</span><span class="sxs-lookup"><span data-stu-id="e3299-239">False</span></span>                                                                                                                 |
| <span data-ttu-id="e3299-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e3299-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3299-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e3299-241">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="e3299-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3299-242">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="e3299-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3299-243">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="e3299-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3299-244">Search-Flags</span></span>           | <span data-ttu-id="e3299-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3299-245">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="e3299-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3299-246">System-Flags</span></span>           | <span data-ttu-id="e3299-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3299-247">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="e3299-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e3299-248">Classes used in</span></span>        | [<span data-ttu-id="e3299-249">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e3299-249">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="e3299-250">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="e3299-250">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e3299-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e3299-251">Windows Server 2012</span></span>



| <span data-ttu-id="e3299-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3299-252">Entry</span></span> | <span data-ttu-id="e3299-253">Valor</span><span class="sxs-lookup"><span data-stu-id="e3299-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3299-254">ID do link</span><span class="sxs-lookup"><span data-stu-id="e3299-254">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="e3299-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3299-255">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="e3299-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3299-256">System-Only</span></span>            | <span data-ttu-id="e3299-257">Falso</span><span class="sxs-lookup"><span data-stu-id="e3299-257">False</span></span>                                                                                                                 |
| <span data-ttu-id="e3299-258">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e3299-258">Is-Single-Valued</span></span>       | <span data-ttu-id="e3299-259">True</span><span class="sxs-lookup"><span data-stu-id="e3299-259">True</span></span>                                                                                                                  |
| <span data-ttu-id="e3299-260">É indexado</span><span class="sxs-lookup"><span data-stu-id="e3299-260">Is Indexed</span></span>             | <span data-ttu-id="e3299-261">Falso</span><span class="sxs-lookup"><span data-stu-id="e3299-261">False</span></span>                                                                                                                 |
| <span data-ttu-id="e3299-262">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e3299-262">In Global Catalog</span></span>      | <span data-ttu-id="e3299-263">Falso</span><span class="sxs-lookup"><span data-stu-id="e3299-263">False</span></span>                                                                                                                 |
| <span data-ttu-id="e3299-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e3299-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3299-265">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e3299-265">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="e3299-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3299-266">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="e3299-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3299-267">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="e3299-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3299-268">Search-Flags</span></span>           | <span data-ttu-id="e3299-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3299-269">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="e3299-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3299-270">System-Flags</span></span>           | <span data-ttu-id="e3299-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3299-271">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="e3299-272">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e3299-272">Classes used in</span></span>        | [<span data-ttu-id="e3299-273">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e3299-273">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="e3299-274">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="e3299-274">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



 

 





