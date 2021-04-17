---
title: Atributo MS-SQL-netaccount
description: Uma cadeia de caracteres definida pelo usuário. O padrão é definido como USERACCOUNT.
ms.assetid: 0db095c8-8492-45c0-b509-d4082cec2c13
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo MS-SQL-netaccount
- Esquema de AD do atributo mS-SQL-netaccount
topic_type:
- apiref
api_name:
- MS-SQL-ServiceAccount
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab96de3d56dedd3178e579e100f00b77df4edb7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105748331"
---
# <a name="ms-sql-serviceaccount-attribute"></a><span data-ttu-id="9db82-106">Atributo MS-SQL-netaccount</span><span class="sxs-lookup"><span data-stu-id="9db82-106">MS-SQL-ServiceAccount attribute</span></span>

<span data-ttu-id="9db82-107">Uma cadeia de caracteres definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="9db82-107">A user defined string.</span></span> <span data-ttu-id="9db82-108">O padrão é definido como USERACCOUNT.</span><span class="sxs-lookup"><span data-stu-id="9db82-108">The default is set to ServiceAccount.</span></span>



| <span data-ttu-id="9db82-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="9db82-109">Entry</span></span> | <span data-ttu-id="9db82-110">Valor</span><span class="sxs-lookup"><span data-stu-id="9db82-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9db82-111">CN</span><span class="sxs-lookup"><span data-stu-id="9db82-111">CN</span></span>                | <span data-ttu-id="9db82-112">Conta do MS-SQL-Microsoft</span><span class="sxs-lookup"><span data-stu-id="9db82-112">MS-SQL-ServiceAccount</span></span>                       |
| <span data-ttu-id="9db82-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9db82-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9db82-114">Conta do mS-SQL-Microsoft</span><span class="sxs-lookup"><span data-stu-id="9db82-114">mS-SQL-ServiceAccount</span></span>                       |
| <span data-ttu-id="9db82-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="9db82-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="9db82-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="9db82-116">Update Privilege</span></span>  | <span data-ttu-id="9db82-117">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="9db82-117">Domain administrator</span></span>                        |
| <span data-ttu-id="9db82-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="9db82-118">Update Frequency</span></span>  | <span data-ttu-id="9db82-119">Na configuração do sistema.</span><span class="sxs-lookup"><span data-stu-id="9db82-119">At system setup.</span></span>                            |
| <span data-ttu-id="9db82-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9db82-120">Attribute-Id</span></span>      | <span data-ttu-id="9db82-121">1.2.840.113556.1.4.1369</span><span class="sxs-lookup"><span data-stu-id="9db82-121">1.2.840.113556.1.4.1369</span></span>                     |
| <span data-ttu-id="9db82-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9db82-122">System-Id-Guid</span></span>    | <span data-ttu-id="9db82-123">64933a3e-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="9db82-123">64933a3e-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="9db82-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="9db82-124">Syntax</span></span>            | [<span data-ttu-id="9db82-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9db82-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9db82-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="9db82-126">Implementations</span></span>

-   [<span data-ttu-id="9db82-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9db82-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9db82-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9db82-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9db82-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9db82-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9db82-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9db82-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9db82-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9db82-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9db82-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9db82-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9db82-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9db82-133">Windows 2000 Server</span></span>



| <span data-ttu-id="9db82-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="9db82-134">Entry</span></span> | <span data-ttu-id="9db82-135">Valor</span><span class="sxs-lookup"><span data-stu-id="9db82-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9db82-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="9db82-136">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9db82-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9db82-137">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9db82-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="9db82-138">System-Only</span></span>            | <span data-ttu-id="9db82-139">Falso</span><span class="sxs-lookup"><span data-stu-id="9db82-139">False</span></span>                                                                                                                 |
| <span data-ttu-id="9db82-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9db82-140">Is-Single-Valued</span></span>       | <span data-ttu-id="9db82-141">True</span><span class="sxs-lookup"><span data-stu-id="9db82-141">True</span></span>                                                                                                                  |
| <span data-ttu-id="9db82-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="9db82-142">Is Indexed</span></span>             | <span data-ttu-id="9db82-143">Falso</span><span class="sxs-lookup"><span data-stu-id="9db82-143">False</span></span>                                                                                                                 |
| <span data-ttu-id="9db82-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9db82-144">In Global Catalog</span></span>      | <span data-ttu-id="9db82-145">Falso</span><span class="sxs-lookup"><span data-stu-id="9db82-145">False</span></span>                                                                                                                 |
| <span data-ttu-id="9db82-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9db82-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="9db82-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9db82-147">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="9db82-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9db82-148">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9db82-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9db82-149">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9db82-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9db82-150">Search-Flags</span></span>           | <span data-ttu-id="9db82-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9db82-151">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="9db82-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9db82-152">System-Flags</span></span>           | <span data-ttu-id="9db82-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9db82-153">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="9db82-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9db82-154">Classes used in</span></span>        | [<span data-ttu-id="9db82-155">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="9db82-155">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="9db82-156">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="9db82-156">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9db82-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9db82-157">Windows Server 2003</span></span>



| <span data-ttu-id="9db82-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="9db82-158">Entry</span></span> | <span data-ttu-id="9db82-159">Valor</span><span class="sxs-lookup"><span data-stu-id="9db82-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9db82-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="9db82-160">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9db82-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9db82-161">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9db82-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="9db82-162">System-Only</span></span>            | <span data-ttu-id="9db82-163">Falso</span><span class="sxs-lookup"><span data-stu-id="9db82-163">False</span></span>                                                                                                                 |
| <span data-ttu-id="9db82-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9db82-164">Is-Single-Valued</span></span>       | <span data-ttu-id="9db82-165">True</span><span class="sxs-lookup"><span data-stu-id="9db82-165">True</span></span>                                                                                                                  |
| <span data-ttu-id="9db82-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="9db82-166">Is Indexed</span></span>             | <span data-ttu-id="9db82-167">Falso</span><span class="sxs-lookup"><span data-stu-id="9db82-167">False</span></span>                                                                                                                 |
| <span data-ttu-id="9db82-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9db82-168">In Global Catalog</span></span>      | <span data-ttu-id="9db82-169">Falso</span><span class="sxs-lookup"><span data-stu-id="9db82-169">False</span></span>                                                                                                                 |
| <span data-ttu-id="9db82-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9db82-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="9db82-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9db82-171">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="9db82-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9db82-172">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9db82-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9db82-173">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9db82-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9db82-174">Search-Flags</span></span>           | <span data-ttu-id="9db82-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9db82-175">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="9db82-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9db82-176">System-Flags</span></span>           | <span data-ttu-id="9db82-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9db82-177">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="9db82-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9db82-178">Classes used in</span></span>        | [<span data-ttu-id="9db82-179">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="9db82-179">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="9db82-180">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="9db82-180">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9db82-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9db82-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9db82-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="9db82-182">Entry</span></span> | <span data-ttu-id="9db82-183">Valor</span><span class="sxs-lookup"><span data-stu-id="9db82-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9db82-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="9db82-184">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9db82-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9db82-185">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9db82-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="9db82-186">System-Only</span></span>            | <span data-ttu-id="9db82-187">Falso</span><span class="sxs-lookup"><span data-stu-id="9db82-187">False</span></span>                                                                                                                 |
| <span data-ttu-id="9db82-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9db82-188">Is-Single-Valued</span></span>       | <span data-ttu-id="9db82-189">True</span><span class="sxs-lookup"><span data-stu-id="9db82-189">True</span></span>                                                                                                                  |
| <span data-ttu-id="9db82-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="9db82-190">Is Indexed</span></span>             | <span data-ttu-id="9db82-191">Falso</span><span class="sxs-lookup"><span data-stu-id="9db82-191">False</span></span>                                                                                                                 |
| <span data-ttu-id="9db82-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9db82-192">In Global Catalog</span></span>      | <span data-ttu-id="9db82-193">Falso</span><span class="sxs-lookup"><span data-stu-id="9db82-193">False</span></span>                                                                                                                 |
| <span data-ttu-id="9db82-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9db82-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="9db82-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9db82-195">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="9db82-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9db82-196">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9db82-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9db82-197">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9db82-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9db82-198">Search-Flags</span></span>           | <span data-ttu-id="9db82-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9db82-199">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="9db82-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9db82-200">System-Flags</span></span>           | <span data-ttu-id="9db82-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9db82-201">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="9db82-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9db82-202">Classes used in</span></span>        | [<span data-ttu-id="9db82-203">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="9db82-203">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="9db82-204">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="9db82-204">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9db82-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9db82-205">Windows Server 2008</span></span>



| <span data-ttu-id="9db82-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="9db82-206">Entry</span></span> | <span data-ttu-id="9db82-207">Valor</span><span class="sxs-lookup"><span data-stu-id="9db82-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9db82-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="9db82-208">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9db82-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9db82-209">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9db82-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="9db82-210">System-Only</span></span>            | <span data-ttu-id="9db82-211">Falso</span><span class="sxs-lookup"><span data-stu-id="9db82-211">False</span></span>                                                                                                                 |
| <span data-ttu-id="9db82-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9db82-212">Is-Single-Valued</span></span>       | <span data-ttu-id="9db82-213">True</span><span class="sxs-lookup"><span data-stu-id="9db82-213">True</span></span>                                                                                                                  |
| <span data-ttu-id="9db82-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="9db82-214">Is Indexed</span></span>             | <span data-ttu-id="9db82-215">Falso</span><span class="sxs-lookup"><span data-stu-id="9db82-215">False</span></span>                                                                                                                 |
| <span data-ttu-id="9db82-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9db82-216">In Global Catalog</span></span>      | <span data-ttu-id="9db82-217">Falso</span><span class="sxs-lookup"><span data-stu-id="9db82-217">False</span></span>                                                                                                                 |
| <span data-ttu-id="9db82-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9db82-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="9db82-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9db82-219">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="9db82-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9db82-220">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9db82-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9db82-221">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9db82-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9db82-222">Search-Flags</span></span>           | <span data-ttu-id="9db82-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9db82-223">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="9db82-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9db82-224">System-Flags</span></span>           | <span data-ttu-id="9db82-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9db82-225">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="9db82-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9db82-226">Classes used in</span></span>        | [<span data-ttu-id="9db82-227">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="9db82-227">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="9db82-228">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="9db82-228">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9db82-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9db82-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9db82-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="9db82-230">Entry</span></span> | <span data-ttu-id="9db82-231">Valor</span><span class="sxs-lookup"><span data-stu-id="9db82-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9db82-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="9db82-232">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9db82-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9db82-233">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9db82-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="9db82-234">System-Only</span></span>            | <span data-ttu-id="9db82-235">Falso</span><span class="sxs-lookup"><span data-stu-id="9db82-235">False</span></span>                                                                                                                 |
| <span data-ttu-id="9db82-236">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9db82-236">Is-Single-Valued</span></span>       | <span data-ttu-id="9db82-237">True</span><span class="sxs-lookup"><span data-stu-id="9db82-237">True</span></span>                                                                                                                  |
| <span data-ttu-id="9db82-238">É indexado</span><span class="sxs-lookup"><span data-stu-id="9db82-238">Is Indexed</span></span>             | <span data-ttu-id="9db82-239">Falso</span><span class="sxs-lookup"><span data-stu-id="9db82-239">False</span></span>                                                                                                                 |
| <span data-ttu-id="9db82-240">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9db82-240">In Global Catalog</span></span>      | <span data-ttu-id="9db82-241">Falso</span><span class="sxs-lookup"><span data-stu-id="9db82-241">False</span></span>                                                                                                                 |
| <span data-ttu-id="9db82-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9db82-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="9db82-243">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9db82-243">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="9db82-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9db82-244">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9db82-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9db82-245">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9db82-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9db82-246">Search-Flags</span></span>           | <span data-ttu-id="9db82-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9db82-247">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="9db82-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9db82-248">System-Flags</span></span>           | <span data-ttu-id="9db82-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9db82-249">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="9db82-250">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9db82-250">Classes used in</span></span>        | [<span data-ttu-id="9db82-251">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="9db82-251">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="9db82-252">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="9db82-252">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9db82-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9db82-253">Windows Server 2012</span></span>



| <span data-ttu-id="9db82-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="9db82-254">Entry</span></span> | <span data-ttu-id="9db82-255">Valor</span><span class="sxs-lookup"><span data-stu-id="9db82-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9db82-256">ID do link</span><span class="sxs-lookup"><span data-stu-id="9db82-256">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9db82-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9db82-257">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9db82-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="9db82-258">System-Only</span></span>            | <span data-ttu-id="9db82-259">Falso</span><span class="sxs-lookup"><span data-stu-id="9db82-259">False</span></span>                                                                                                                 |
| <span data-ttu-id="9db82-260">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9db82-260">Is-Single-Valued</span></span>       | <span data-ttu-id="9db82-261">True</span><span class="sxs-lookup"><span data-stu-id="9db82-261">True</span></span>                                                                                                                  |
| <span data-ttu-id="9db82-262">É indexado</span><span class="sxs-lookup"><span data-stu-id="9db82-262">Is Indexed</span></span>             | <span data-ttu-id="9db82-263">Falso</span><span class="sxs-lookup"><span data-stu-id="9db82-263">False</span></span>                                                                                                                 |
| <span data-ttu-id="9db82-264">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9db82-264">In Global Catalog</span></span>      | <span data-ttu-id="9db82-265">Falso</span><span class="sxs-lookup"><span data-stu-id="9db82-265">False</span></span>                                                                                                                 |
| <span data-ttu-id="9db82-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9db82-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="9db82-267">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9db82-267">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="9db82-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9db82-268">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9db82-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9db82-269">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9db82-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9db82-270">Search-Flags</span></span>           | <span data-ttu-id="9db82-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9db82-271">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="9db82-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9db82-272">System-Flags</span></span>           | <span data-ttu-id="9db82-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9db82-273">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="9db82-274">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9db82-274">Classes used in</span></span>        | [<span data-ttu-id="9db82-275">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="9db82-275">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="9db82-276">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="9db82-276">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



 

 





