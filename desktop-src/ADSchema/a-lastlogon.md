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
# <a name="last-logon-attribute"></a><span data-ttu-id="5cf73-105">Last-Logon atributo</span><span class="sxs-lookup"><span data-stu-id="5cf73-105">Last-Logon attribute</span></span>

<span data-ttu-id="5cf73-106">A última vez que o usuário fez logon.</span><span class="sxs-lookup"><span data-stu-id="5cf73-106">The last time the user logged on.</span></span> <span data-ttu-id="5cf73-107">Esse valor é armazenado como um inteiro grande que representa o número de intervalos de 100 a nanossegundos desde 1º de janeiro de 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="5cf73-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="5cf73-108">Um valor de zero significa que a hora do último logon é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="5cf73-108">A value of zero means that the last logon time is unknown.</span></span>



| <span data-ttu-id="5cf73-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="5cf73-109">Entry</span></span> | <span data-ttu-id="5cf73-110">Valor</span><span class="sxs-lookup"><span data-stu-id="5cf73-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5cf73-111">CN</span><span class="sxs-lookup"><span data-stu-id="5cf73-111">CN</span></span>                | <span data-ttu-id="5cf73-112">Last-Logon</span><span class="sxs-lookup"><span data-stu-id="5cf73-112">Last-Logon</span></span>                           |
| <span data-ttu-id="5cf73-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5cf73-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5cf73-114">lastLogon</span><span class="sxs-lookup"><span data-stu-id="5cf73-114">lastLogon</span></span>                            |
| <span data-ttu-id="5cf73-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="5cf73-115">Size</span></span>              | <span data-ttu-id="5cf73-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="5cf73-116">8 bytes</span></span>                              |
| <span data-ttu-id="5cf73-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="5cf73-117">Update Privilege</span></span>  | <span data-ttu-id="5cf73-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="5cf73-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="5cf73-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="5cf73-119">Update Frequency</span></span>  | <span data-ttu-id="5cf73-120">Cada vez que o usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="5cf73-120">Each time the user logs on.</span></span>          |
| <span data-ttu-id="5cf73-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5cf73-121">Attribute-Id</span></span>      | <span data-ttu-id="5cf73-122">1.2.840.113556.1.4.52</span><span class="sxs-lookup"><span data-stu-id="5cf73-122">1.2.840.113556.1.4.52</span></span>                |
| <span data-ttu-id="5cf73-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5cf73-123">System-Id-Guid</span></span>    | <span data-ttu-id="5cf73-124">bf967997-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="5cf73-124">bf967997-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="5cf73-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cf73-125">Syntax</span></span>            | [<span data-ttu-id="5cf73-126">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="5cf73-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="5cf73-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="5cf73-127">Implementations</span></span>

-   [<span data-ttu-id="5cf73-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5cf73-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5cf73-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5cf73-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5cf73-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5cf73-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5cf73-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5cf73-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5cf73-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5cf73-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5cf73-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5cf73-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5cf73-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5cf73-134">Windows 2000 Server</span></span>



| <span data-ttu-id="5cf73-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="5cf73-135">Entry</span></span> | <span data-ttu-id="5cf73-136">Valor</span><span class="sxs-lookup"><span data-stu-id="5cf73-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="5cf73-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="5cf73-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="5cf73-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cf73-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="5cf73-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cf73-139">System-Only</span></span>            | <span data-ttu-id="5cf73-140">Falso</span><span class="sxs-lookup"><span data-stu-id="5cf73-140">False</span></span>                             |
| <span data-ttu-id="5cf73-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5cf73-141">Is-Single-Valued</span></span>       | <span data-ttu-id="5cf73-142">True</span><span class="sxs-lookup"><span data-stu-id="5cf73-142">True</span></span>                              |
| <span data-ttu-id="5cf73-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="5cf73-143">Is Indexed</span></span>             | <span data-ttu-id="5cf73-144">Falso</span><span class="sxs-lookup"><span data-stu-id="5cf73-144">False</span></span>                             |
| <span data-ttu-id="5cf73-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5cf73-145">In Global Catalog</span></span>      | <span data-ttu-id="5cf73-146">Falso</span><span class="sxs-lookup"><span data-stu-id="5cf73-146">False</span></span>                             |
| <span data-ttu-id="5cf73-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5cf73-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cf73-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5cf73-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="5cf73-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cf73-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="5cf73-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cf73-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="5cf73-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cf73-151">Search-Flags</span></span>           | <span data-ttu-id="5cf73-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cf73-152">0x00000000</span></span>                        |
| <span data-ttu-id="5cf73-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cf73-153">System-Flags</span></span>           | <span data-ttu-id="5cf73-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="5cf73-154">0x00000011</span></span>                        |
| <span data-ttu-id="5cf73-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5cf73-155">Classes used in</span></span>        | [<span data-ttu-id="5cf73-156">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="5cf73-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5cf73-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5cf73-157">Windows Server 2003</span></span>



| <span data-ttu-id="5cf73-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="5cf73-158">Entry</span></span> | <span data-ttu-id="5cf73-159">Valor</span><span class="sxs-lookup"><span data-stu-id="5cf73-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="5cf73-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="5cf73-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="5cf73-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cf73-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="5cf73-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cf73-162">System-Only</span></span>            | <span data-ttu-id="5cf73-163">Falso</span><span class="sxs-lookup"><span data-stu-id="5cf73-163">False</span></span>                             |
| <span data-ttu-id="5cf73-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5cf73-164">Is-Single-Valued</span></span>       | <span data-ttu-id="5cf73-165">True</span><span class="sxs-lookup"><span data-stu-id="5cf73-165">True</span></span>                              |
| <span data-ttu-id="5cf73-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="5cf73-166">Is Indexed</span></span>             | <span data-ttu-id="5cf73-167">Falso</span><span class="sxs-lookup"><span data-stu-id="5cf73-167">False</span></span>                             |
| <span data-ttu-id="5cf73-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5cf73-168">In Global Catalog</span></span>      | <span data-ttu-id="5cf73-169">Falso</span><span class="sxs-lookup"><span data-stu-id="5cf73-169">False</span></span>                             |
| <span data-ttu-id="5cf73-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5cf73-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cf73-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5cf73-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="5cf73-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cf73-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="5cf73-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cf73-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="5cf73-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cf73-174">Search-Flags</span></span>           | <span data-ttu-id="5cf73-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cf73-175">0x00000000</span></span>                        |
| <span data-ttu-id="5cf73-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cf73-176">System-Flags</span></span>           | <span data-ttu-id="5cf73-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="5cf73-177">0x00000011</span></span>                        |
| <span data-ttu-id="5cf73-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5cf73-178">Classes used in</span></span>        | [<span data-ttu-id="5cf73-179">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="5cf73-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5cf73-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5cf73-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5cf73-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="5cf73-181">Entry</span></span> | <span data-ttu-id="5cf73-182">Valor</span><span class="sxs-lookup"><span data-stu-id="5cf73-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="5cf73-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="5cf73-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="5cf73-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cf73-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="5cf73-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cf73-185">System-Only</span></span>            | <span data-ttu-id="5cf73-186">Falso</span><span class="sxs-lookup"><span data-stu-id="5cf73-186">False</span></span>                             |
| <span data-ttu-id="5cf73-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5cf73-187">Is-Single-Valued</span></span>       | <span data-ttu-id="5cf73-188">True</span><span class="sxs-lookup"><span data-stu-id="5cf73-188">True</span></span>                              |
| <span data-ttu-id="5cf73-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="5cf73-189">Is Indexed</span></span>             | <span data-ttu-id="5cf73-190">Falso</span><span class="sxs-lookup"><span data-stu-id="5cf73-190">False</span></span>                             |
| <span data-ttu-id="5cf73-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5cf73-191">In Global Catalog</span></span>      | <span data-ttu-id="5cf73-192">Falso</span><span class="sxs-lookup"><span data-stu-id="5cf73-192">False</span></span>                             |
| <span data-ttu-id="5cf73-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5cf73-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cf73-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5cf73-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="5cf73-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cf73-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="5cf73-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cf73-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="5cf73-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cf73-197">Search-Flags</span></span>           | <span data-ttu-id="5cf73-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cf73-198">0x00000000</span></span>                        |
| <span data-ttu-id="5cf73-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cf73-199">System-Flags</span></span>           | <span data-ttu-id="5cf73-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="5cf73-200">0x00000011</span></span>                        |
| <span data-ttu-id="5cf73-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5cf73-201">Classes used in</span></span>        | [<span data-ttu-id="5cf73-202">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="5cf73-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5cf73-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5cf73-203">Windows Server 2008</span></span>



| <span data-ttu-id="5cf73-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="5cf73-204">Entry</span></span> | <span data-ttu-id="5cf73-205">Valor</span><span class="sxs-lookup"><span data-stu-id="5cf73-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="5cf73-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="5cf73-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="5cf73-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cf73-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="5cf73-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cf73-208">System-Only</span></span>            | <span data-ttu-id="5cf73-209">Falso</span><span class="sxs-lookup"><span data-stu-id="5cf73-209">False</span></span>                             |
| <span data-ttu-id="5cf73-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5cf73-210">Is-Single-Valued</span></span>       | <span data-ttu-id="5cf73-211">True</span><span class="sxs-lookup"><span data-stu-id="5cf73-211">True</span></span>                              |
| <span data-ttu-id="5cf73-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="5cf73-212">Is Indexed</span></span>             | <span data-ttu-id="5cf73-213">Falso</span><span class="sxs-lookup"><span data-stu-id="5cf73-213">False</span></span>                             |
| <span data-ttu-id="5cf73-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5cf73-214">In Global Catalog</span></span>      | <span data-ttu-id="5cf73-215">Falso</span><span class="sxs-lookup"><span data-stu-id="5cf73-215">False</span></span>                             |
| <span data-ttu-id="5cf73-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5cf73-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cf73-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5cf73-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="5cf73-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cf73-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="5cf73-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cf73-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="5cf73-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cf73-220">Search-Flags</span></span>           | <span data-ttu-id="5cf73-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cf73-221">0x00000000</span></span>                        |
| <span data-ttu-id="5cf73-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cf73-222">System-Flags</span></span>           | <span data-ttu-id="5cf73-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="5cf73-223">0x00000011</span></span>                        |
| <span data-ttu-id="5cf73-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5cf73-224">Classes used in</span></span>        | [<span data-ttu-id="5cf73-225">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="5cf73-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5cf73-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5cf73-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5cf73-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="5cf73-227">Entry</span></span> | <span data-ttu-id="5cf73-228">Valor</span><span class="sxs-lookup"><span data-stu-id="5cf73-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="5cf73-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="5cf73-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="5cf73-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cf73-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="5cf73-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cf73-231">System-Only</span></span>            | <span data-ttu-id="5cf73-232">Falso</span><span class="sxs-lookup"><span data-stu-id="5cf73-232">False</span></span>                             |
| <span data-ttu-id="5cf73-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5cf73-233">Is-Single-Valued</span></span>       | <span data-ttu-id="5cf73-234">True</span><span class="sxs-lookup"><span data-stu-id="5cf73-234">True</span></span>                              |
| <span data-ttu-id="5cf73-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="5cf73-235">Is Indexed</span></span>             | <span data-ttu-id="5cf73-236">Falso</span><span class="sxs-lookup"><span data-stu-id="5cf73-236">False</span></span>                             |
| <span data-ttu-id="5cf73-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5cf73-237">In Global Catalog</span></span>      | <span data-ttu-id="5cf73-238">Falso</span><span class="sxs-lookup"><span data-stu-id="5cf73-238">False</span></span>                             |
| <span data-ttu-id="5cf73-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5cf73-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cf73-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5cf73-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="5cf73-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cf73-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="5cf73-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cf73-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="5cf73-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cf73-243">Search-Flags</span></span>           | <span data-ttu-id="5cf73-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cf73-244">0x00000000</span></span>                        |
| <span data-ttu-id="5cf73-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cf73-245">System-Flags</span></span>           | <span data-ttu-id="5cf73-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="5cf73-246">0x00000011</span></span>                        |
| <span data-ttu-id="5cf73-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5cf73-247">Classes used in</span></span>        | [<span data-ttu-id="5cf73-248">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="5cf73-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5cf73-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5cf73-249">Windows Server 2012</span></span>



| <span data-ttu-id="5cf73-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="5cf73-250">Entry</span></span> | <span data-ttu-id="5cf73-251">Valor</span><span class="sxs-lookup"><span data-stu-id="5cf73-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="5cf73-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="5cf73-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="5cf73-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5cf73-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="5cf73-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="5cf73-254">System-Only</span></span>            | <span data-ttu-id="5cf73-255">Falso</span><span class="sxs-lookup"><span data-stu-id="5cf73-255">False</span></span>                             |
| <span data-ttu-id="5cf73-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5cf73-256">Is-Single-Valued</span></span>       | <span data-ttu-id="5cf73-257">True</span><span class="sxs-lookup"><span data-stu-id="5cf73-257">True</span></span>                              |
| <span data-ttu-id="5cf73-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="5cf73-258">Is Indexed</span></span>             | <span data-ttu-id="5cf73-259">Falso</span><span class="sxs-lookup"><span data-stu-id="5cf73-259">False</span></span>                             |
| <span data-ttu-id="5cf73-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5cf73-260">In Global Catalog</span></span>      | <span data-ttu-id="5cf73-261">Falso</span><span class="sxs-lookup"><span data-stu-id="5cf73-261">False</span></span>                             |
| <span data-ttu-id="5cf73-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5cf73-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="5cf73-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5cf73-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="5cf73-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5cf73-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="5cf73-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5cf73-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="5cf73-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5cf73-266">Search-Flags</span></span>           | <span data-ttu-id="5cf73-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5cf73-267">0x00000000</span></span>                        |
| <span data-ttu-id="5cf73-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5cf73-268">System-Flags</span></span>           | <span data-ttu-id="5cf73-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="5cf73-269">0x00000011</span></span>                        |
| <span data-ttu-id="5cf73-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5cf73-270">Classes used in</span></span>        | [<span data-ttu-id="5cf73-271">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="5cf73-271">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="5cf73-272">Comentários</span><span class="sxs-lookup"><span data-stu-id="5cf73-272">Remarks</span></span>

<span data-ttu-id="5cf73-273">A parte superior desse inteiro grande corresponde ao membro **dwHighDateTime** da estrutura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e a parte inferior corresponde ao membro **dwLowDateTime** da estrutura **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="5cf73-273">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="5cf73-274">Esse atributo não é replicado e é mantido separadamente em cada controlador de domínio no domínio.</span><span class="sxs-lookup"><span data-stu-id="5cf73-274">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="5cf73-275">Para obter um valor preciso para o último logon do usuário no domínio, o atributo de **último logon** para o usuário deve ser recuperado de cada controlador de domínio no domínio.</span><span class="sxs-lookup"><span data-stu-id="5cf73-275">To get an accurate value for the user's last logon in the domain, the **Last-Logon** attribute for the user must be retrieved from every domain controller in the domain.</span></span> <span data-ttu-id="5cf73-276">O maior valor recuperado é a hora do último logon real para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="5cf73-276">The largest value that is retrieved is the true last logon time for that user.</span></span>

## <a name="see-also"></a><span data-ttu-id="5cf73-277">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cf73-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cf73-278">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="5cf73-278">**FILETIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> </dl>

 

