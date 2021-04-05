---
title: Last-Logon atributo
description: A última vez que o usuário fez logon.
ms.assetid: 271f4f38-90f9-4add-a3ed-413c224e1fae
ms.tgt_platform: multiple
keywords:
- Esquema de Last-Logon do atributo AD
- Esquema de AD do atributo lastLogon
topic_type:
- apiref
api_name:
- Last-Logon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae01ffabf2d4862c030607b997a4d9057b934f8f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825239"
---
# <a name="last-logon-attribute"></a><span data-ttu-id="f1674-105">Last-Logon atributo</span><span class="sxs-lookup"><span data-stu-id="f1674-105">Last-Logon attribute</span></span>

<span data-ttu-id="f1674-106">A última vez que o usuário fez logon.</span><span class="sxs-lookup"><span data-stu-id="f1674-106">The last time the user logged on.</span></span> <span data-ttu-id="f1674-107">Esse valor é armazenado como um inteiro grande que representa o número de intervalos de 100 a nanossegundos desde 1º de janeiro de 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="f1674-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="f1674-108">Um valor de zero significa que a hora do último logon é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="f1674-108">A value of zero means that the last logon time is unknown.</span></span>



| <span data-ttu-id="f1674-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1674-109">Entry</span></span> | <span data-ttu-id="f1674-110">Valor</span><span class="sxs-lookup"><span data-stu-id="f1674-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f1674-111">CN</span><span class="sxs-lookup"><span data-stu-id="f1674-111">CN</span></span>                | <span data-ttu-id="f1674-112">Last-Logon</span><span class="sxs-lookup"><span data-stu-id="f1674-112">Last-Logon</span></span>                           |
| <span data-ttu-id="f1674-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f1674-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f1674-114">lastLogon</span><span class="sxs-lookup"><span data-stu-id="f1674-114">lastLogon</span></span>                            |
| <span data-ttu-id="f1674-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f1674-115">Size</span></span>              | <span data-ttu-id="f1674-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="f1674-116">8 bytes</span></span>                              |
| <span data-ttu-id="f1674-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f1674-117">Update Privilege</span></span>  | <span data-ttu-id="f1674-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="f1674-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="f1674-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f1674-119">Update Frequency</span></span>  | <span data-ttu-id="f1674-120">Cada vez que o usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="f1674-120">Each time the user logs on.</span></span>          |
| <span data-ttu-id="f1674-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f1674-121">Attribute-Id</span></span>      | <span data-ttu-id="f1674-122">1.2.840.113556.1.4.52</span><span class="sxs-lookup"><span data-stu-id="f1674-122">1.2.840.113556.1.4.52</span></span>                |
| <span data-ttu-id="f1674-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f1674-123">System-Id-Guid</span></span>    | <span data-ttu-id="f1674-124">bf967997-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f1674-124">bf967997-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="f1674-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1674-125">Syntax</span></span>            | [<span data-ttu-id="f1674-126">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="f1674-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="f1674-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="f1674-127">Implementations</span></span>

-   [<span data-ttu-id="f1674-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f1674-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f1674-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f1674-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f1674-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f1674-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f1674-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f1674-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f1674-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f1674-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f1674-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f1674-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f1674-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f1674-134">Windows 2000 Server</span></span>



| <span data-ttu-id="f1674-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1674-135">Entry</span></span> | <span data-ttu-id="f1674-136">Valor</span><span class="sxs-lookup"><span data-stu-id="f1674-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f1674-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1674-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f1674-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1674-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f1674-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1674-139">System-Only</span></span>            | <span data-ttu-id="f1674-140">Falso</span><span class="sxs-lookup"><span data-stu-id="f1674-140">False</span></span>                             |
| <span data-ttu-id="f1674-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1674-141">Is-Single-Valued</span></span>       | <span data-ttu-id="f1674-142">True</span><span class="sxs-lookup"><span data-stu-id="f1674-142">True</span></span>                              |
| <span data-ttu-id="f1674-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1674-143">Is Indexed</span></span>             | <span data-ttu-id="f1674-144">Falso</span><span class="sxs-lookup"><span data-stu-id="f1674-144">False</span></span>                             |
| <span data-ttu-id="f1674-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1674-145">In Global Catalog</span></span>      | <span data-ttu-id="f1674-146">Falso</span><span class="sxs-lookup"><span data-stu-id="f1674-146">False</span></span>                             |
| <span data-ttu-id="f1674-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1674-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1674-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1674-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f1674-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1674-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f1674-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1674-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f1674-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1674-151">Search-Flags</span></span>           | <span data-ttu-id="f1674-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1674-152">0x00000000</span></span>                        |
| <span data-ttu-id="f1674-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1674-153">System-Flags</span></span>           | <span data-ttu-id="f1674-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f1674-154">0x00000011</span></span>                        |
| <span data-ttu-id="f1674-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1674-155">Classes used in</span></span>        | [<span data-ttu-id="f1674-156">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f1674-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f1674-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f1674-157">Windows Server 2003</span></span>



| <span data-ttu-id="f1674-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1674-158">Entry</span></span> | <span data-ttu-id="f1674-159">Valor</span><span class="sxs-lookup"><span data-stu-id="f1674-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f1674-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1674-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f1674-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1674-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f1674-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1674-162">System-Only</span></span>            | <span data-ttu-id="f1674-163">Falso</span><span class="sxs-lookup"><span data-stu-id="f1674-163">False</span></span>                             |
| <span data-ttu-id="f1674-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1674-164">Is-Single-Valued</span></span>       | <span data-ttu-id="f1674-165">True</span><span class="sxs-lookup"><span data-stu-id="f1674-165">True</span></span>                              |
| <span data-ttu-id="f1674-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1674-166">Is Indexed</span></span>             | <span data-ttu-id="f1674-167">Falso</span><span class="sxs-lookup"><span data-stu-id="f1674-167">False</span></span>                             |
| <span data-ttu-id="f1674-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1674-168">In Global Catalog</span></span>      | <span data-ttu-id="f1674-169">Falso</span><span class="sxs-lookup"><span data-stu-id="f1674-169">False</span></span>                             |
| <span data-ttu-id="f1674-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1674-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1674-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1674-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f1674-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1674-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f1674-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1674-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f1674-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1674-174">Search-Flags</span></span>           | <span data-ttu-id="f1674-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1674-175">0x00000000</span></span>                        |
| <span data-ttu-id="f1674-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1674-176">System-Flags</span></span>           | <span data-ttu-id="f1674-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f1674-177">0x00000011</span></span>                        |
| <span data-ttu-id="f1674-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1674-178">Classes used in</span></span>        | [<span data-ttu-id="f1674-179">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f1674-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f1674-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f1674-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f1674-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1674-181">Entry</span></span> | <span data-ttu-id="f1674-182">Valor</span><span class="sxs-lookup"><span data-stu-id="f1674-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f1674-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1674-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f1674-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1674-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f1674-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1674-185">System-Only</span></span>            | <span data-ttu-id="f1674-186">Falso</span><span class="sxs-lookup"><span data-stu-id="f1674-186">False</span></span>                             |
| <span data-ttu-id="f1674-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1674-187">Is-Single-Valued</span></span>       | <span data-ttu-id="f1674-188">True</span><span class="sxs-lookup"><span data-stu-id="f1674-188">True</span></span>                              |
| <span data-ttu-id="f1674-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1674-189">Is Indexed</span></span>             | <span data-ttu-id="f1674-190">Falso</span><span class="sxs-lookup"><span data-stu-id="f1674-190">False</span></span>                             |
| <span data-ttu-id="f1674-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1674-191">In Global Catalog</span></span>      | <span data-ttu-id="f1674-192">Falso</span><span class="sxs-lookup"><span data-stu-id="f1674-192">False</span></span>                             |
| <span data-ttu-id="f1674-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1674-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1674-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1674-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f1674-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1674-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f1674-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1674-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f1674-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1674-197">Search-Flags</span></span>           | <span data-ttu-id="f1674-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1674-198">0x00000000</span></span>                        |
| <span data-ttu-id="f1674-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1674-199">System-Flags</span></span>           | <span data-ttu-id="f1674-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f1674-200">0x00000011</span></span>                        |
| <span data-ttu-id="f1674-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1674-201">Classes used in</span></span>        | [<span data-ttu-id="f1674-202">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f1674-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f1674-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1674-203">Windows Server 2008</span></span>



| <span data-ttu-id="f1674-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1674-204">Entry</span></span> | <span data-ttu-id="f1674-205">Valor</span><span class="sxs-lookup"><span data-stu-id="f1674-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f1674-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1674-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f1674-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1674-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f1674-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1674-208">System-Only</span></span>            | <span data-ttu-id="f1674-209">Falso</span><span class="sxs-lookup"><span data-stu-id="f1674-209">False</span></span>                             |
| <span data-ttu-id="f1674-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1674-210">Is-Single-Valued</span></span>       | <span data-ttu-id="f1674-211">True</span><span class="sxs-lookup"><span data-stu-id="f1674-211">True</span></span>                              |
| <span data-ttu-id="f1674-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1674-212">Is Indexed</span></span>             | <span data-ttu-id="f1674-213">Falso</span><span class="sxs-lookup"><span data-stu-id="f1674-213">False</span></span>                             |
| <span data-ttu-id="f1674-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1674-214">In Global Catalog</span></span>      | <span data-ttu-id="f1674-215">Falso</span><span class="sxs-lookup"><span data-stu-id="f1674-215">False</span></span>                             |
| <span data-ttu-id="f1674-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1674-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1674-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1674-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f1674-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1674-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f1674-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1674-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f1674-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1674-220">Search-Flags</span></span>           | <span data-ttu-id="f1674-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1674-221">0x00000000</span></span>                        |
| <span data-ttu-id="f1674-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1674-222">System-Flags</span></span>           | <span data-ttu-id="f1674-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f1674-223">0x00000011</span></span>                        |
| <span data-ttu-id="f1674-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1674-224">Classes used in</span></span>        | [<span data-ttu-id="f1674-225">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f1674-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f1674-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f1674-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f1674-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1674-227">Entry</span></span> | <span data-ttu-id="f1674-228">Valor</span><span class="sxs-lookup"><span data-stu-id="f1674-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f1674-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1674-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f1674-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1674-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f1674-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1674-231">System-Only</span></span>            | <span data-ttu-id="f1674-232">Falso</span><span class="sxs-lookup"><span data-stu-id="f1674-232">False</span></span>                             |
| <span data-ttu-id="f1674-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1674-233">Is-Single-Valued</span></span>       | <span data-ttu-id="f1674-234">True</span><span class="sxs-lookup"><span data-stu-id="f1674-234">True</span></span>                              |
| <span data-ttu-id="f1674-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1674-235">Is Indexed</span></span>             | <span data-ttu-id="f1674-236">Falso</span><span class="sxs-lookup"><span data-stu-id="f1674-236">False</span></span>                             |
| <span data-ttu-id="f1674-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1674-237">In Global Catalog</span></span>      | <span data-ttu-id="f1674-238">Falso</span><span class="sxs-lookup"><span data-stu-id="f1674-238">False</span></span>                             |
| <span data-ttu-id="f1674-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1674-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1674-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1674-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f1674-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1674-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f1674-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1674-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f1674-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1674-243">Search-Flags</span></span>           | <span data-ttu-id="f1674-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1674-244">0x00000000</span></span>                        |
| <span data-ttu-id="f1674-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1674-245">System-Flags</span></span>           | <span data-ttu-id="f1674-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f1674-246">0x00000011</span></span>                        |
| <span data-ttu-id="f1674-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1674-247">Classes used in</span></span>        | [<span data-ttu-id="f1674-248">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f1674-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f1674-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f1674-249">Windows Server 2012</span></span>



| <span data-ttu-id="f1674-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1674-250">Entry</span></span> | <span data-ttu-id="f1674-251">Valor</span><span class="sxs-lookup"><span data-stu-id="f1674-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f1674-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1674-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f1674-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1674-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f1674-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1674-254">System-Only</span></span>            | <span data-ttu-id="f1674-255">Falso</span><span class="sxs-lookup"><span data-stu-id="f1674-255">False</span></span>                             |
| <span data-ttu-id="f1674-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1674-256">Is-Single-Valued</span></span>       | <span data-ttu-id="f1674-257">True</span><span class="sxs-lookup"><span data-stu-id="f1674-257">True</span></span>                              |
| <span data-ttu-id="f1674-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1674-258">Is Indexed</span></span>             | <span data-ttu-id="f1674-259">Falso</span><span class="sxs-lookup"><span data-stu-id="f1674-259">False</span></span>                             |
| <span data-ttu-id="f1674-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1674-260">In Global Catalog</span></span>      | <span data-ttu-id="f1674-261">Falso</span><span class="sxs-lookup"><span data-stu-id="f1674-261">False</span></span>                             |
| <span data-ttu-id="f1674-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1674-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1674-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1674-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f1674-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1674-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f1674-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1674-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f1674-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1674-266">Search-Flags</span></span>           | <span data-ttu-id="f1674-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1674-267">0x00000000</span></span>                        |
| <span data-ttu-id="f1674-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1674-268">System-Flags</span></span>           | <span data-ttu-id="f1674-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f1674-269">0x00000011</span></span>                        |
| <span data-ttu-id="f1674-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1674-270">Classes used in</span></span>        | [<span data-ttu-id="f1674-271">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f1674-271">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f1674-272">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1674-272">Remarks</span></span>

<span data-ttu-id="f1674-273">A parte superior desse inteiro grande corresponde ao membro **dwHighDateTime** da estrutura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e a parte inferior corresponde ao membro **dwLowDateTime** da estrutura **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="f1674-273">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="f1674-274">Esse atributo não é replicado e é mantido separadamente em cada controlador de domínio no domínio.</span><span class="sxs-lookup"><span data-stu-id="f1674-274">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="f1674-275">Para obter um valor preciso para o último logon do usuário no domínio, o atributo de **último logon** para o usuário deve ser recuperado de cada controlador de domínio no domínio.</span><span class="sxs-lookup"><span data-stu-id="f1674-275">To get an accurate value for the user's last logon in the domain, the **Last-Logon** attribute for the user must be retrieved from every domain controller in the domain.</span></span> <span data-ttu-id="f1674-276">O maior valor recuperado é a hora do último logon real para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="f1674-276">The largest value that is retrieved is the true last logon time for that user.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1674-277">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1674-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1674-278">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="f1674-278">**FILETIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> </dl>

 

