---
title: Logon-Count atributo
description: O número de vezes que a conta foi conectada com êxito. Um valor de 0 indica que o valor é desconhecido.
ms.assetid: 8b12bea7-dfc3-46e3-a4a2-92b5f1239b98
ms.tgt_platform: multiple
keywords:
- Esquema de Logon-Count do atributo AD
- Esquema de AD do atributo logonCount
topic_type:
- apiref
api_name:
- Logon-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ba7865cb3b90f42ede71b169f98f8ce45e722d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825235"
---
# <a name="logon-count-attribute"></a><span data-ttu-id="e177c-106">Logon-Count atributo</span><span class="sxs-lookup"><span data-stu-id="e177c-106">Logon-Count attribute</span></span>

<span data-ttu-id="e177c-107">O número de vezes que a conta foi conectada com êxito.</span><span class="sxs-lookup"><span data-stu-id="e177c-107">The number of times the account has successfully logged on.</span></span> <span data-ttu-id="e177c-108">Um valor de 0 indica que o valor é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e177c-108">A value of 0 indicates that the value is unknown.</span></span>



| <span data-ttu-id="e177c-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="e177c-109">Entry</span></span> | <span data-ttu-id="e177c-110">Valor</span><span class="sxs-lookup"><span data-stu-id="e177c-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e177c-111">CN</span><span class="sxs-lookup"><span data-stu-id="e177c-111">CN</span></span>                | <span data-ttu-id="e177c-112">Logon-Count</span><span class="sxs-lookup"><span data-stu-id="e177c-112">Logon-Count</span></span>                          |
| <span data-ttu-id="e177c-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e177c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e177c-114">logonCount</span><span class="sxs-lookup"><span data-stu-id="e177c-114">logonCount</span></span>                           |
| <span data-ttu-id="e177c-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="e177c-115">Size</span></span>              | <span data-ttu-id="e177c-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="e177c-116">4 bytes</span></span>                              |
| <span data-ttu-id="e177c-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="e177c-117">Update Privilege</span></span>  | <span data-ttu-id="e177c-118">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="e177c-118">Domain administrator</span></span>                 |
| <span data-ttu-id="e177c-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="e177c-119">Update Frequency</span></span>  | <span data-ttu-id="e177c-120">Cada vez que o usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="e177c-120">Each time the user logs on.</span></span>          |
| <span data-ttu-id="e177c-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e177c-121">Attribute-Id</span></span>      | <span data-ttu-id="e177c-122">1.2.840.113556.1.4.169</span><span class="sxs-lookup"><span data-stu-id="e177c-122">1.2.840.113556.1.4.169</span></span>               |
| <span data-ttu-id="e177c-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e177c-123">System-Id-Guid</span></span>    | <span data-ttu-id="e177c-124">bf9679aa-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e177c-124">bf9679aa-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="e177c-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="e177c-125">Syntax</span></span>            | [<span data-ttu-id="e177c-126">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="e177c-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="e177c-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="e177c-127">Implementations</span></span>

-   [<span data-ttu-id="e177c-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e177c-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e177c-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e177c-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e177c-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e177c-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e177c-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e177c-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e177c-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e177c-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e177c-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e177c-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e177c-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e177c-134">Windows 2000 Server</span></span>



| <span data-ttu-id="e177c-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="e177c-135">Entry</span></span> | <span data-ttu-id="e177c-136">Valor</span><span class="sxs-lookup"><span data-stu-id="e177c-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e177c-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="e177c-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e177c-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e177c-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e177c-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="e177c-139">System-Only</span></span>            | <span data-ttu-id="e177c-140">Falso</span><span class="sxs-lookup"><span data-stu-id="e177c-140">False</span></span>                             |
| <span data-ttu-id="e177c-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e177c-141">Is-Single-Valued</span></span>       | <span data-ttu-id="e177c-142">True</span><span class="sxs-lookup"><span data-stu-id="e177c-142">True</span></span>                              |
| <span data-ttu-id="e177c-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="e177c-143">Is Indexed</span></span>             | <span data-ttu-id="e177c-144">Falso</span><span class="sxs-lookup"><span data-stu-id="e177c-144">False</span></span>                             |
| <span data-ttu-id="e177c-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e177c-145">In Global Catalog</span></span>      | <span data-ttu-id="e177c-146">Falso</span><span class="sxs-lookup"><span data-stu-id="e177c-146">False</span></span>                             |
| <span data-ttu-id="e177c-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e177c-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="e177c-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e177c-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e177c-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e177c-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e177c-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e177c-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e177c-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e177c-151">Search-Flags</span></span>           | <span data-ttu-id="e177c-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e177c-152">0x00000000</span></span>                        |
| <span data-ttu-id="e177c-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e177c-153">System-Flags</span></span>           | <span data-ttu-id="e177c-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e177c-154">0x00000011</span></span>                        |
| <span data-ttu-id="e177c-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e177c-155">Classes used in</span></span>        | [<span data-ttu-id="e177c-156">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="e177c-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e177c-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e177c-157">Windows Server 2003</span></span>



| <span data-ttu-id="e177c-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="e177c-158">Entry</span></span> | <span data-ttu-id="e177c-159">Valor</span><span class="sxs-lookup"><span data-stu-id="e177c-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e177c-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="e177c-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e177c-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e177c-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e177c-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="e177c-162">System-Only</span></span>            | <span data-ttu-id="e177c-163">Falso</span><span class="sxs-lookup"><span data-stu-id="e177c-163">False</span></span>                             |
| <span data-ttu-id="e177c-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e177c-164">Is-Single-Valued</span></span>       | <span data-ttu-id="e177c-165">True</span><span class="sxs-lookup"><span data-stu-id="e177c-165">True</span></span>                              |
| <span data-ttu-id="e177c-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="e177c-166">Is Indexed</span></span>             | <span data-ttu-id="e177c-167">Falso</span><span class="sxs-lookup"><span data-stu-id="e177c-167">False</span></span>                             |
| <span data-ttu-id="e177c-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e177c-168">In Global Catalog</span></span>      | <span data-ttu-id="e177c-169">Falso</span><span class="sxs-lookup"><span data-stu-id="e177c-169">False</span></span>                             |
| <span data-ttu-id="e177c-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e177c-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="e177c-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e177c-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e177c-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e177c-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e177c-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e177c-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e177c-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e177c-174">Search-Flags</span></span>           | <span data-ttu-id="e177c-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e177c-175">0x00000000</span></span>                        |
| <span data-ttu-id="e177c-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e177c-176">System-Flags</span></span>           | <span data-ttu-id="e177c-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e177c-177">0x00000011</span></span>                        |
| <span data-ttu-id="e177c-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e177c-178">Classes used in</span></span>        | [<span data-ttu-id="e177c-179">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="e177c-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e177c-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e177c-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e177c-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="e177c-181">Entry</span></span> | <span data-ttu-id="e177c-182">Valor</span><span class="sxs-lookup"><span data-stu-id="e177c-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e177c-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="e177c-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e177c-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e177c-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e177c-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="e177c-185">System-Only</span></span>            | <span data-ttu-id="e177c-186">Falso</span><span class="sxs-lookup"><span data-stu-id="e177c-186">False</span></span>                             |
| <span data-ttu-id="e177c-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e177c-187">Is-Single-Valued</span></span>       | <span data-ttu-id="e177c-188">True</span><span class="sxs-lookup"><span data-stu-id="e177c-188">True</span></span>                              |
| <span data-ttu-id="e177c-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="e177c-189">Is Indexed</span></span>             | <span data-ttu-id="e177c-190">Falso</span><span class="sxs-lookup"><span data-stu-id="e177c-190">False</span></span>                             |
| <span data-ttu-id="e177c-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e177c-191">In Global Catalog</span></span>      | <span data-ttu-id="e177c-192">Falso</span><span class="sxs-lookup"><span data-stu-id="e177c-192">False</span></span>                             |
| <span data-ttu-id="e177c-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e177c-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="e177c-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e177c-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e177c-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e177c-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e177c-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e177c-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e177c-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e177c-197">Search-Flags</span></span>           | <span data-ttu-id="e177c-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e177c-198">0x00000000</span></span>                        |
| <span data-ttu-id="e177c-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e177c-199">System-Flags</span></span>           | <span data-ttu-id="e177c-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e177c-200">0x00000011</span></span>                        |
| <span data-ttu-id="e177c-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e177c-201">Classes used in</span></span>        | [<span data-ttu-id="e177c-202">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="e177c-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e177c-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e177c-203">Windows Server 2008</span></span>



| <span data-ttu-id="e177c-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="e177c-204">Entry</span></span> | <span data-ttu-id="e177c-205">Valor</span><span class="sxs-lookup"><span data-stu-id="e177c-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e177c-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="e177c-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e177c-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e177c-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e177c-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="e177c-208">System-Only</span></span>            | <span data-ttu-id="e177c-209">Falso</span><span class="sxs-lookup"><span data-stu-id="e177c-209">False</span></span>                             |
| <span data-ttu-id="e177c-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e177c-210">Is-Single-Valued</span></span>       | <span data-ttu-id="e177c-211">True</span><span class="sxs-lookup"><span data-stu-id="e177c-211">True</span></span>                              |
| <span data-ttu-id="e177c-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="e177c-212">Is Indexed</span></span>             | <span data-ttu-id="e177c-213">Falso</span><span class="sxs-lookup"><span data-stu-id="e177c-213">False</span></span>                             |
| <span data-ttu-id="e177c-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e177c-214">In Global Catalog</span></span>      | <span data-ttu-id="e177c-215">Falso</span><span class="sxs-lookup"><span data-stu-id="e177c-215">False</span></span>                             |
| <span data-ttu-id="e177c-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e177c-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="e177c-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e177c-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e177c-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e177c-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e177c-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e177c-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e177c-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e177c-220">Search-Flags</span></span>           | <span data-ttu-id="e177c-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e177c-221">0x00000000</span></span>                        |
| <span data-ttu-id="e177c-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e177c-222">System-Flags</span></span>           | <span data-ttu-id="e177c-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e177c-223">0x00000011</span></span>                        |
| <span data-ttu-id="e177c-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e177c-224">Classes used in</span></span>        | [<span data-ttu-id="e177c-225">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="e177c-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e177c-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e177c-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e177c-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="e177c-227">Entry</span></span> | <span data-ttu-id="e177c-228">Valor</span><span class="sxs-lookup"><span data-stu-id="e177c-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e177c-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="e177c-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e177c-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e177c-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e177c-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="e177c-231">System-Only</span></span>            | <span data-ttu-id="e177c-232">Falso</span><span class="sxs-lookup"><span data-stu-id="e177c-232">False</span></span>                             |
| <span data-ttu-id="e177c-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e177c-233">Is-Single-Valued</span></span>       | <span data-ttu-id="e177c-234">True</span><span class="sxs-lookup"><span data-stu-id="e177c-234">True</span></span>                              |
| <span data-ttu-id="e177c-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="e177c-235">Is Indexed</span></span>             | <span data-ttu-id="e177c-236">Falso</span><span class="sxs-lookup"><span data-stu-id="e177c-236">False</span></span>                             |
| <span data-ttu-id="e177c-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e177c-237">In Global Catalog</span></span>      | <span data-ttu-id="e177c-238">Falso</span><span class="sxs-lookup"><span data-stu-id="e177c-238">False</span></span>                             |
| <span data-ttu-id="e177c-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e177c-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="e177c-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e177c-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e177c-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e177c-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e177c-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e177c-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e177c-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e177c-243">Search-Flags</span></span>           | <span data-ttu-id="e177c-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e177c-244">0x00000000</span></span>                        |
| <span data-ttu-id="e177c-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e177c-245">System-Flags</span></span>           | <span data-ttu-id="e177c-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e177c-246">0x00000011</span></span>                        |
| <span data-ttu-id="e177c-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e177c-247">Classes used in</span></span>        | [<span data-ttu-id="e177c-248">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="e177c-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e177c-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e177c-249">Windows Server 2012</span></span>



| <span data-ttu-id="e177c-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="e177c-250">Entry</span></span> | <span data-ttu-id="e177c-251">Valor</span><span class="sxs-lookup"><span data-stu-id="e177c-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e177c-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="e177c-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e177c-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e177c-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e177c-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="e177c-254">System-Only</span></span>            | <span data-ttu-id="e177c-255">Falso</span><span class="sxs-lookup"><span data-stu-id="e177c-255">False</span></span>                             |
| <span data-ttu-id="e177c-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e177c-256">Is-Single-Valued</span></span>       | <span data-ttu-id="e177c-257">True</span><span class="sxs-lookup"><span data-stu-id="e177c-257">True</span></span>                              |
| <span data-ttu-id="e177c-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="e177c-258">Is Indexed</span></span>             | <span data-ttu-id="e177c-259">Falso</span><span class="sxs-lookup"><span data-stu-id="e177c-259">False</span></span>                             |
| <span data-ttu-id="e177c-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e177c-260">In Global Catalog</span></span>      | <span data-ttu-id="e177c-261">Falso</span><span class="sxs-lookup"><span data-stu-id="e177c-261">False</span></span>                             |
| <span data-ttu-id="e177c-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e177c-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="e177c-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e177c-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e177c-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e177c-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e177c-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e177c-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e177c-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e177c-266">Search-Flags</span></span>           | <span data-ttu-id="e177c-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e177c-267">0x00000000</span></span>                        |
| <span data-ttu-id="e177c-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e177c-268">System-Flags</span></span>           | <span data-ttu-id="e177c-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e177c-269">0x00000011</span></span>                        |
| <span data-ttu-id="e177c-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e177c-270">Classes used in</span></span>        | [<span data-ttu-id="e177c-271">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="e177c-271">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e177c-272">Comentários</span><span class="sxs-lookup"><span data-stu-id="e177c-272">Remarks</span></span>

<span data-ttu-id="e177c-273">Esse atributo não é replicado e é mantido em cada controlador de domínio no domínio.</span><span class="sxs-lookup"><span data-stu-id="e177c-273">This attribute is not replicated and is maintained on each domain controller in the domain.</span></span> <span data-ttu-id="e177c-274">Para obter um valor preciso para o número total de tentativas de logon bem-sucedidas do usuário no domínio, cada controlador de domínio no domínio deve ser consultado e a soma dos valores deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="e177c-274">To get an accurate value for the user's total number of successful logon attempts in the domain, each domain controller in the domain must be queried and the sum of the values should be used.</span></span> <span data-ttu-id="e177c-275">Lembre-se de que o atributo não é replicado, portanto, os controladores de domínio que são desativados também podem ter os logons contados para o usuário, e eles ficarão ausentes da contagem.</span><span class="sxs-lookup"><span data-stu-id="e177c-275">Keep in mind that the attribute is not replicated, therefore domain controllers that are retired may have counted logons for the user as well, and these will be missing from the count.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e177c-276">Devido à compatibilidade com as versões de 16 bits do LAN Manager, o atributo tem um limite superior de 65535.</span><span class="sxs-lookup"><span data-stu-id="e177c-276">Due to compatibility with 16-bit versions of LAN Manager, the attribute has an upper limit of 65535.</span></span> <span data-ttu-id="e177c-277">Depois que esse limite for atingido, você não poderá usá-lo como um indicador de atividade do usuário nesse controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="e177c-277">After this limit has been reached, you cannot use it as an indicator of user activity on this domain controller.</span></span>

 

 

 





