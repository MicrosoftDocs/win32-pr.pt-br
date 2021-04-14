---
title: Logon-Hours atributo
description: As horas em que o usuário tem permissão para fazer logon no domínio.
ms.assetid: b97cc8b0-7f26-45c1-b1c9-bae6467bdfb6
ms.tgt_platform: multiple
keywords:
- Esquema de Logon-Hours do atributo AD
- Esquema de AD do atributo logonHours
topic_type:
- apiref
api_name:
- Logon-Hours
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f764192ac57efdb1f14d55f691183240f0eddfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456136"
---
# <a name="logon-hours-attribute"></a><span data-ttu-id="23f07-105">Logon-Hours atributo</span><span class="sxs-lookup"><span data-stu-id="23f07-105">Logon-Hours attribute</span></span>

<span data-ttu-id="23f07-106">As horas em que o usuário tem permissão para fazer logon no domínio.</span><span class="sxs-lookup"><span data-stu-id="23f07-106">The hours that the user is allowed to logon to the domain.</span></span>



| <span data-ttu-id="23f07-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="23f07-107">Entry</span></span> | <span data-ttu-id="23f07-108">Valor</span><span class="sxs-lookup"><span data-stu-id="23f07-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="23f07-109">CN</span><span class="sxs-lookup"><span data-stu-id="23f07-109">CN</span></span>                | <span data-ttu-id="23f07-110">Logon-Hours</span><span class="sxs-lookup"><span data-stu-id="23f07-110">Logon-Hours</span></span>                                           |
| <span data-ttu-id="23f07-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="23f07-111">Ldap-Display-Name</span></span> | <span data-ttu-id="23f07-112">logonHours</span><span class="sxs-lookup"><span data-stu-id="23f07-112">logonHours</span></span>                                            |
| <span data-ttu-id="23f07-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="23f07-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="23f07-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="23f07-114">Update Privilege</span></span>  | <span data-ttu-id="23f07-115">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="23f07-115">Domain administrator</span></span>                                  |
| <span data-ttu-id="23f07-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="23f07-116">Update Frequency</span></span>  | <span data-ttu-id="23f07-117">Sempre que o horário de logon da conta precisar ser alterado.</span><span class="sxs-lookup"><span data-stu-id="23f07-117">Whenever the account's logon hours needs to change.</span></span>   |
| <span data-ttu-id="23f07-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="23f07-118">Attribute-Id</span></span>      | <span data-ttu-id="23f07-119">1.2.840.113556.1.4.64</span><span class="sxs-lookup"><span data-stu-id="23f07-119">1.2.840.113556.1.4.64</span></span>                                 |
| <span data-ttu-id="23f07-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="23f07-120">System-Id-Guid</span></span>    | <span data-ttu-id="23f07-121">bf9679ab-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="23f07-121">bf9679ab-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="23f07-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="23f07-122">Syntax</span></span>            | [<span data-ttu-id="23f07-123">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="23f07-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="23f07-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="23f07-124">Implementations</span></span>

-   [<span data-ttu-id="23f07-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="23f07-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="23f07-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="23f07-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="23f07-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="23f07-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="23f07-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="23f07-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="23f07-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="23f07-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="23f07-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="23f07-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="23f07-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="23f07-131">Windows 2000 Server</span></span>



| <span data-ttu-id="23f07-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="23f07-132">Entry</span></span> | <span data-ttu-id="23f07-133">Valor</span><span class="sxs-lookup"><span data-stu-id="23f07-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="23f07-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="23f07-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="23f07-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23f07-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="23f07-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="23f07-136">System-Only</span></span>            | <span data-ttu-id="23f07-137">Falso</span><span class="sxs-lookup"><span data-stu-id="23f07-137">False</span></span>                             |
| <span data-ttu-id="23f07-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="23f07-138">Is-Single-Valued</span></span>       | <span data-ttu-id="23f07-139">True</span><span class="sxs-lookup"><span data-stu-id="23f07-139">True</span></span>                              |
| <span data-ttu-id="23f07-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="23f07-140">Is Indexed</span></span>             | <span data-ttu-id="23f07-141">Falso</span><span class="sxs-lookup"><span data-stu-id="23f07-141">False</span></span>                             |
| <span data-ttu-id="23f07-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="23f07-142">In Global Catalog</span></span>      | <span data-ttu-id="23f07-143">Falso</span><span class="sxs-lookup"><span data-stu-id="23f07-143">False</span></span>                             |
| <span data-ttu-id="23f07-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="23f07-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="23f07-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="23f07-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="23f07-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23f07-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="23f07-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23f07-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="23f07-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23f07-148">Search-Flags</span></span>           | <span data-ttu-id="23f07-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23f07-149">0x00000010</span></span>                        |
| <span data-ttu-id="23f07-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23f07-150">System-Flags</span></span>           | <span data-ttu-id="23f07-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23f07-151">0x00000010</span></span>                        |
| <span data-ttu-id="23f07-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="23f07-152">Classes used in</span></span>        | [<span data-ttu-id="23f07-153">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="23f07-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="23f07-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="23f07-154">Windows Server 2003</span></span>



| <span data-ttu-id="23f07-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="23f07-155">Entry</span></span> | <span data-ttu-id="23f07-156">Valor</span><span class="sxs-lookup"><span data-stu-id="23f07-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="23f07-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="23f07-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="23f07-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23f07-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="23f07-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="23f07-159">System-Only</span></span>            | <span data-ttu-id="23f07-160">Falso</span><span class="sxs-lookup"><span data-stu-id="23f07-160">False</span></span>                             |
| <span data-ttu-id="23f07-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="23f07-161">Is-Single-Valued</span></span>       | <span data-ttu-id="23f07-162">True</span><span class="sxs-lookup"><span data-stu-id="23f07-162">True</span></span>                              |
| <span data-ttu-id="23f07-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="23f07-163">Is Indexed</span></span>             | <span data-ttu-id="23f07-164">Falso</span><span class="sxs-lookup"><span data-stu-id="23f07-164">False</span></span>                             |
| <span data-ttu-id="23f07-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="23f07-165">In Global Catalog</span></span>      | <span data-ttu-id="23f07-166">Falso</span><span class="sxs-lookup"><span data-stu-id="23f07-166">False</span></span>                             |
| <span data-ttu-id="23f07-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="23f07-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="23f07-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="23f07-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="23f07-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23f07-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="23f07-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23f07-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="23f07-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23f07-171">Search-Flags</span></span>           | <span data-ttu-id="23f07-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23f07-172">0x00000010</span></span>                        |
| <span data-ttu-id="23f07-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23f07-173">System-Flags</span></span>           | <span data-ttu-id="23f07-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23f07-174">0x00000010</span></span>                        |
| <span data-ttu-id="23f07-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="23f07-175">Classes used in</span></span>        | [<span data-ttu-id="23f07-176">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="23f07-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="23f07-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="23f07-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="23f07-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="23f07-178">Entry</span></span> | <span data-ttu-id="23f07-179">Valor</span><span class="sxs-lookup"><span data-stu-id="23f07-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="23f07-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="23f07-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="23f07-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23f07-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="23f07-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="23f07-182">System-Only</span></span>            | <span data-ttu-id="23f07-183">Falso</span><span class="sxs-lookup"><span data-stu-id="23f07-183">False</span></span>                             |
| <span data-ttu-id="23f07-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="23f07-184">Is-Single-Valued</span></span>       | <span data-ttu-id="23f07-185">True</span><span class="sxs-lookup"><span data-stu-id="23f07-185">True</span></span>                              |
| <span data-ttu-id="23f07-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="23f07-186">Is Indexed</span></span>             | <span data-ttu-id="23f07-187">Falso</span><span class="sxs-lookup"><span data-stu-id="23f07-187">False</span></span>                             |
| <span data-ttu-id="23f07-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="23f07-188">In Global Catalog</span></span>      | <span data-ttu-id="23f07-189">Falso</span><span class="sxs-lookup"><span data-stu-id="23f07-189">False</span></span>                             |
| <span data-ttu-id="23f07-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="23f07-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="23f07-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="23f07-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="23f07-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23f07-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="23f07-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23f07-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="23f07-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23f07-194">Search-Flags</span></span>           | <span data-ttu-id="23f07-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23f07-195">0x00000010</span></span>                        |
| <span data-ttu-id="23f07-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23f07-196">System-Flags</span></span>           | <span data-ttu-id="23f07-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23f07-197">0x00000010</span></span>                        |
| <span data-ttu-id="23f07-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="23f07-198">Classes used in</span></span>        | [<span data-ttu-id="23f07-199">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="23f07-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="23f07-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23f07-200">Windows Server 2008</span></span>



| <span data-ttu-id="23f07-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="23f07-201">Entry</span></span> | <span data-ttu-id="23f07-202">Valor</span><span class="sxs-lookup"><span data-stu-id="23f07-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="23f07-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="23f07-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="23f07-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23f07-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="23f07-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="23f07-205">System-Only</span></span>            | <span data-ttu-id="23f07-206">Falso</span><span class="sxs-lookup"><span data-stu-id="23f07-206">False</span></span>                             |
| <span data-ttu-id="23f07-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="23f07-207">Is-Single-Valued</span></span>       | <span data-ttu-id="23f07-208">True</span><span class="sxs-lookup"><span data-stu-id="23f07-208">True</span></span>                              |
| <span data-ttu-id="23f07-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="23f07-209">Is Indexed</span></span>             | <span data-ttu-id="23f07-210">Falso</span><span class="sxs-lookup"><span data-stu-id="23f07-210">False</span></span>                             |
| <span data-ttu-id="23f07-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="23f07-211">In Global Catalog</span></span>      | <span data-ttu-id="23f07-212">Falso</span><span class="sxs-lookup"><span data-stu-id="23f07-212">False</span></span>                             |
| <span data-ttu-id="23f07-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="23f07-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="23f07-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="23f07-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="23f07-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23f07-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="23f07-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23f07-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="23f07-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23f07-217">Search-Flags</span></span>           | <span data-ttu-id="23f07-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23f07-218">0x00000010</span></span>                        |
| <span data-ttu-id="23f07-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23f07-219">System-Flags</span></span>           | <span data-ttu-id="23f07-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23f07-220">0x00000010</span></span>                        |
| <span data-ttu-id="23f07-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="23f07-221">Classes used in</span></span>        | [<span data-ttu-id="23f07-222">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="23f07-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="23f07-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="23f07-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="23f07-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="23f07-224">Entry</span></span> | <span data-ttu-id="23f07-225">Valor</span><span class="sxs-lookup"><span data-stu-id="23f07-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="23f07-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="23f07-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="23f07-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23f07-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="23f07-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="23f07-228">System-Only</span></span>            | <span data-ttu-id="23f07-229">Falso</span><span class="sxs-lookup"><span data-stu-id="23f07-229">False</span></span>                             |
| <span data-ttu-id="23f07-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="23f07-230">Is-Single-Valued</span></span>       | <span data-ttu-id="23f07-231">True</span><span class="sxs-lookup"><span data-stu-id="23f07-231">True</span></span>                              |
| <span data-ttu-id="23f07-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="23f07-232">Is Indexed</span></span>             | <span data-ttu-id="23f07-233">Falso</span><span class="sxs-lookup"><span data-stu-id="23f07-233">False</span></span>                             |
| <span data-ttu-id="23f07-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="23f07-234">In Global Catalog</span></span>      | <span data-ttu-id="23f07-235">Falso</span><span class="sxs-lookup"><span data-stu-id="23f07-235">False</span></span>                             |
| <span data-ttu-id="23f07-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="23f07-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="23f07-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="23f07-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="23f07-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23f07-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="23f07-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23f07-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="23f07-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23f07-240">Search-Flags</span></span>           | <span data-ttu-id="23f07-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23f07-241">0x00000010</span></span>                        |
| <span data-ttu-id="23f07-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23f07-242">System-Flags</span></span>           | <span data-ttu-id="23f07-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23f07-243">0x00000010</span></span>                        |
| <span data-ttu-id="23f07-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="23f07-244">Classes used in</span></span>        | [<span data-ttu-id="23f07-245">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="23f07-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="23f07-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="23f07-246">Windows Server 2012</span></span>



| <span data-ttu-id="23f07-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="23f07-247">Entry</span></span> | <span data-ttu-id="23f07-248">Valor</span><span class="sxs-lookup"><span data-stu-id="23f07-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="23f07-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="23f07-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="23f07-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23f07-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="23f07-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="23f07-251">System-Only</span></span>            | <span data-ttu-id="23f07-252">Falso</span><span class="sxs-lookup"><span data-stu-id="23f07-252">False</span></span>                             |
| <span data-ttu-id="23f07-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="23f07-253">Is-Single-Valued</span></span>       | <span data-ttu-id="23f07-254">True</span><span class="sxs-lookup"><span data-stu-id="23f07-254">True</span></span>                              |
| <span data-ttu-id="23f07-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="23f07-255">Is Indexed</span></span>             | <span data-ttu-id="23f07-256">Falso</span><span class="sxs-lookup"><span data-stu-id="23f07-256">False</span></span>                             |
| <span data-ttu-id="23f07-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="23f07-257">In Global Catalog</span></span>      | <span data-ttu-id="23f07-258">Falso</span><span class="sxs-lookup"><span data-stu-id="23f07-258">False</span></span>                             |
| <span data-ttu-id="23f07-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="23f07-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="23f07-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="23f07-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="23f07-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23f07-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="23f07-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23f07-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="23f07-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23f07-263">Search-Flags</span></span>           | <span data-ttu-id="23f07-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23f07-264">0x00000010</span></span>                        |
| <span data-ttu-id="23f07-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23f07-265">System-Flags</span></span>           | <span data-ttu-id="23f07-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23f07-266">0x00000010</span></span>                        |
| <span data-ttu-id="23f07-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="23f07-267">Classes used in</span></span>        | [<span data-ttu-id="23f07-268">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="23f07-268">**User**</span></span>](c-user.md)<br/> |



 

 





