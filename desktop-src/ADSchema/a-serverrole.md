---
title: Server-Role atributo
description: Para compatibilidade com servidores de servidor anteriores ao Windows 2000. Um computador que executa o Windows NT Server pode ser um servidor autônomo, um controlador de domínio primário (PDC) ou um controlador de domínio de backup (BDC).
ms.assetid: 0c2e5b18-14ad-4f77-a62c-eeb95aabbb99
ms.tgt_platform: multiple
keywords:
- Esquema de Server-Role do atributo AD
- Esquema de AD do atributo serverRole
topic_type:
- apiref
api_name:
- Server-Role
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58a127a94cd1ecc2bfce3701c11ee2a5e0c2376c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105756303"
---
# <a name="server-role-attribute"></a><span data-ttu-id="486e9-106">Server-Role atributo</span><span class="sxs-lookup"><span data-stu-id="486e9-106">Server-Role attribute</span></span>

<span data-ttu-id="486e9-107">Para compatibilidade com servidores de servidor anteriores ao Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="486e9-107">For compatibility with pre-Windows 2000 Server servers.</span></span> <span data-ttu-id="486e9-108">Um computador que executa o Windows NT Server pode ser um servidor autônomo, um controlador de domínio primário (PDC) ou um controlador de domínio de backup (BDC).</span><span class="sxs-lookup"><span data-stu-id="486e9-108">A computer running Windows NT Server can be a standalone server, a primary domain controller (PDC), or a backup domain controller (BDC).</span></span>



| <span data-ttu-id="486e9-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="486e9-109">Entry</span></span> | <span data-ttu-id="486e9-110">Valor</span><span class="sxs-lookup"><span data-stu-id="486e9-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="486e9-111">CN</span><span class="sxs-lookup"><span data-stu-id="486e9-111">CN</span></span>                | <span data-ttu-id="486e9-112">Server-Role</span><span class="sxs-lookup"><span data-stu-id="486e9-112">Server-Role</span></span>                          |
| <span data-ttu-id="486e9-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="486e9-113">Ldap-Display-Name</span></span> | <span data-ttu-id="486e9-114">serverRole</span><span class="sxs-lookup"><span data-stu-id="486e9-114">serverRole</span></span>                           |
| <span data-ttu-id="486e9-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="486e9-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="486e9-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="486e9-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="486e9-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="486e9-117">Update Frequency</span></span>  | <span data-ttu-id="486e9-118">4 bytes</span><span class="sxs-lookup"><span data-stu-id="486e9-118">4 bytes</span></span>                              |
| <span data-ttu-id="486e9-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="486e9-119">Attribute-Id</span></span>      | <span data-ttu-id="486e9-120">1.2.840.113556.1.4.157</span><span class="sxs-lookup"><span data-stu-id="486e9-120">1.2.840.113556.1.4.157</span></span>               |
| <span data-ttu-id="486e9-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="486e9-121">System-Id-Guid</span></span>    | <span data-ttu-id="486e9-122">bf967a33-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="486e9-122">bf967a33-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="486e9-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="486e9-123">Syntax</span></span>            | [<span data-ttu-id="486e9-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="486e9-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="486e9-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="486e9-125">Implementations</span></span>

-   [<span data-ttu-id="486e9-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="486e9-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="486e9-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="486e9-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="486e9-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="486e9-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="486e9-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="486e9-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="486e9-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="486e9-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="486e9-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="486e9-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="486e9-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="486e9-132">Windows 2000 Server</span></span>



| <span data-ttu-id="486e9-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="486e9-133">Entry</span></span> | <span data-ttu-id="486e9-134">Valor</span><span class="sxs-lookup"><span data-stu-id="486e9-134">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="486e9-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="486e9-135">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="486e9-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="486e9-136">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="486e9-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="486e9-137">System-Only</span></span>            | <span data-ttu-id="486e9-138">Falso</span><span class="sxs-lookup"><span data-stu-id="486e9-138">False</span></span>                                                 |
| <span data-ttu-id="486e9-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="486e9-139">Is-Single-Valued</span></span>       | <span data-ttu-id="486e9-140">True</span><span class="sxs-lookup"><span data-stu-id="486e9-140">True</span></span>                                                  |
| <span data-ttu-id="486e9-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="486e9-141">Is Indexed</span></span>             | <span data-ttu-id="486e9-142">Falso</span><span class="sxs-lookup"><span data-stu-id="486e9-142">False</span></span>                                                 |
| <span data-ttu-id="486e9-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="486e9-143">In Global Catalog</span></span>      | <span data-ttu-id="486e9-144">Falso</span><span class="sxs-lookup"><span data-stu-id="486e9-144">False</span></span>                                                 |
| <span data-ttu-id="486e9-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="486e9-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="486e9-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="486e9-146">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="486e9-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="486e9-147">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="486e9-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="486e9-148">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="486e9-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="486e9-149">Search-Flags</span></span>           | <span data-ttu-id="486e9-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="486e9-150">0x00000000</span></span>                                            |
| <span data-ttu-id="486e9-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="486e9-151">System-Flags</span></span>           | <span data-ttu-id="486e9-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="486e9-152">0x00000010</span></span>                                            |
| <span data-ttu-id="486e9-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="486e9-153">Classes used in</span></span>        | [<span data-ttu-id="486e9-154">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="486e9-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="486e9-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="486e9-155">Windows Server 2003</span></span>



| <span data-ttu-id="486e9-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="486e9-156">Entry</span></span> | <span data-ttu-id="486e9-157">Valor</span><span class="sxs-lookup"><span data-stu-id="486e9-157">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="486e9-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="486e9-158">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="486e9-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="486e9-159">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="486e9-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="486e9-160">System-Only</span></span>            | <span data-ttu-id="486e9-161">Falso</span><span class="sxs-lookup"><span data-stu-id="486e9-161">False</span></span>                                                 |
| <span data-ttu-id="486e9-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="486e9-162">Is-Single-Valued</span></span>       | <span data-ttu-id="486e9-163">True</span><span class="sxs-lookup"><span data-stu-id="486e9-163">True</span></span>                                                  |
| <span data-ttu-id="486e9-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="486e9-164">Is Indexed</span></span>             | <span data-ttu-id="486e9-165">Falso</span><span class="sxs-lookup"><span data-stu-id="486e9-165">False</span></span>                                                 |
| <span data-ttu-id="486e9-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="486e9-166">In Global Catalog</span></span>      | <span data-ttu-id="486e9-167">Falso</span><span class="sxs-lookup"><span data-stu-id="486e9-167">False</span></span>                                                 |
| <span data-ttu-id="486e9-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="486e9-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="486e9-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="486e9-169">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="486e9-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="486e9-170">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="486e9-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="486e9-171">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="486e9-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="486e9-172">Search-Flags</span></span>           | <span data-ttu-id="486e9-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="486e9-173">0x00000000</span></span>                                            |
| <span data-ttu-id="486e9-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="486e9-174">System-Flags</span></span>           | <span data-ttu-id="486e9-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="486e9-175">0x00000010</span></span>                                            |
| <span data-ttu-id="486e9-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="486e9-176">Classes used in</span></span>        | [<span data-ttu-id="486e9-177">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="486e9-177">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="486e9-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="486e9-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="486e9-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="486e9-179">Entry</span></span> | <span data-ttu-id="486e9-180">Valor</span><span class="sxs-lookup"><span data-stu-id="486e9-180">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="486e9-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="486e9-181">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="486e9-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="486e9-182">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="486e9-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="486e9-183">System-Only</span></span>            | <span data-ttu-id="486e9-184">Falso</span><span class="sxs-lookup"><span data-stu-id="486e9-184">False</span></span>                                                 |
| <span data-ttu-id="486e9-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="486e9-185">Is-Single-Valued</span></span>       | <span data-ttu-id="486e9-186">True</span><span class="sxs-lookup"><span data-stu-id="486e9-186">True</span></span>                                                  |
| <span data-ttu-id="486e9-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="486e9-187">Is Indexed</span></span>             | <span data-ttu-id="486e9-188">Falso</span><span class="sxs-lookup"><span data-stu-id="486e9-188">False</span></span>                                                 |
| <span data-ttu-id="486e9-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="486e9-189">In Global Catalog</span></span>      | <span data-ttu-id="486e9-190">Falso</span><span class="sxs-lookup"><span data-stu-id="486e9-190">False</span></span>                                                 |
| <span data-ttu-id="486e9-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="486e9-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="486e9-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="486e9-192">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="486e9-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="486e9-193">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="486e9-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="486e9-194">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="486e9-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="486e9-195">Search-Flags</span></span>           | <span data-ttu-id="486e9-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="486e9-196">0x00000000</span></span>                                            |
| <span data-ttu-id="486e9-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="486e9-197">System-Flags</span></span>           | <span data-ttu-id="486e9-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="486e9-198">0x00000010</span></span>                                            |
| <span data-ttu-id="486e9-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="486e9-199">Classes used in</span></span>        | [<span data-ttu-id="486e9-200">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="486e9-200">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="486e9-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="486e9-201">Windows Server 2008</span></span>



| <span data-ttu-id="486e9-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="486e9-202">Entry</span></span> | <span data-ttu-id="486e9-203">Valor</span><span class="sxs-lookup"><span data-stu-id="486e9-203">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="486e9-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="486e9-204">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="486e9-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="486e9-205">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="486e9-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="486e9-206">System-Only</span></span>            | <span data-ttu-id="486e9-207">Falso</span><span class="sxs-lookup"><span data-stu-id="486e9-207">False</span></span>                                                 |
| <span data-ttu-id="486e9-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="486e9-208">Is-Single-Valued</span></span>       | <span data-ttu-id="486e9-209">True</span><span class="sxs-lookup"><span data-stu-id="486e9-209">True</span></span>                                                  |
| <span data-ttu-id="486e9-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="486e9-210">Is Indexed</span></span>             | <span data-ttu-id="486e9-211">Falso</span><span class="sxs-lookup"><span data-stu-id="486e9-211">False</span></span>                                                 |
| <span data-ttu-id="486e9-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="486e9-212">In Global Catalog</span></span>      | <span data-ttu-id="486e9-213">Falso</span><span class="sxs-lookup"><span data-stu-id="486e9-213">False</span></span>                                                 |
| <span data-ttu-id="486e9-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="486e9-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="486e9-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="486e9-215">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="486e9-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="486e9-216">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="486e9-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="486e9-217">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="486e9-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="486e9-218">Search-Flags</span></span>           | <span data-ttu-id="486e9-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="486e9-219">0x00000000</span></span>                                            |
| <span data-ttu-id="486e9-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="486e9-220">System-Flags</span></span>           | <span data-ttu-id="486e9-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="486e9-221">0x00000010</span></span>                                            |
| <span data-ttu-id="486e9-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="486e9-222">Classes used in</span></span>        | [<span data-ttu-id="486e9-223">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="486e9-223">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="486e9-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="486e9-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="486e9-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="486e9-225">Entry</span></span> | <span data-ttu-id="486e9-226">Valor</span><span class="sxs-lookup"><span data-stu-id="486e9-226">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="486e9-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="486e9-227">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="486e9-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="486e9-228">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="486e9-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="486e9-229">System-Only</span></span>            | <span data-ttu-id="486e9-230">Falso</span><span class="sxs-lookup"><span data-stu-id="486e9-230">False</span></span>                                                 |
| <span data-ttu-id="486e9-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="486e9-231">Is-Single-Valued</span></span>       | <span data-ttu-id="486e9-232">True</span><span class="sxs-lookup"><span data-stu-id="486e9-232">True</span></span>                                                  |
| <span data-ttu-id="486e9-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="486e9-233">Is Indexed</span></span>             | <span data-ttu-id="486e9-234">Falso</span><span class="sxs-lookup"><span data-stu-id="486e9-234">False</span></span>                                                 |
| <span data-ttu-id="486e9-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="486e9-235">In Global Catalog</span></span>      | <span data-ttu-id="486e9-236">Falso</span><span class="sxs-lookup"><span data-stu-id="486e9-236">False</span></span>                                                 |
| <span data-ttu-id="486e9-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="486e9-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="486e9-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="486e9-238">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="486e9-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="486e9-239">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="486e9-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="486e9-240">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="486e9-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="486e9-241">Search-Flags</span></span>           | <span data-ttu-id="486e9-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="486e9-242">0x00000000</span></span>                                            |
| <span data-ttu-id="486e9-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="486e9-243">System-Flags</span></span>           | <span data-ttu-id="486e9-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="486e9-244">0x00000010</span></span>                                            |
| <span data-ttu-id="486e9-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="486e9-245">Classes used in</span></span>        | [<span data-ttu-id="486e9-246">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="486e9-246">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="486e9-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="486e9-247">Windows Server 2012</span></span>



| <span data-ttu-id="486e9-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="486e9-248">Entry</span></span> | <span data-ttu-id="486e9-249">Valor</span><span class="sxs-lookup"><span data-stu-id="486e9-249">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="486e9-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="486e9-250">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="486e9-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="486e9-251">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="486e9-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="486e9-252">System-Only</span></span>            | <span data-ttu-id="486e9-253">Falso</span><span class="sxs-lookup"><span data-stu-id="486e9-253">False</span></span>                                                 |
| <span data-ttu-id="486e9-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="486e9-254">Is-Single-Valued</span></span>       | <span data-ttu-id="486e9-255">True</span><span class="sxs-lookup"><span data-stu-id="486e9-255">True</span></span>                                                  |
| <span data-ttu-id="486e9-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="486e9-256">Is Indexed</span></span>             | <span data-ttu-id="486e9-257">Falso</span><span class="sxs-lookup"><span data-stu-id="486e9-257">False</span></span>                                                 |
| <span data-ttu-id="486e9-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="486e9-258">In Global Catalog</span></span>      | <span data-ttu-id="486e9-259">Falso</span><span class="sxs-lookup"><span data-stu-id="486e9-259">False</span></span>                                                 |
| <span data-ttu-id="486e9-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="486e9-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="486e9-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="486e9-261">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="486e9-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="486e9-262">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="486e9-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="486e9-263">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="486e9-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="486e9-264">Search-Flags</span></span>           | <span data-ttu-id="486e9-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="486e9-265">0x00000000</span></span>                                            |
| <span data-ttu-id="486e9-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="486e9-266">System-Flags</span></span>           | <span data-ttu-id="486e9-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="486e9-267">0x00000010</span></span>                                            |
| <span data-ttu-id="486e9-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="486e9-268">Classes used in</span></span>        | [<span data-ttu-id="486e9-269">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="486e9-269">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





