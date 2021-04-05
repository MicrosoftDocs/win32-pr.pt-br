---
title: Atributo LM-pwd-History
description: O histórico de senha do usuário no formato unidirecional do LM (LAN Manager) (). O LM OWF é usado para compatibilidade com clientes do LAN Manager 2. x, Windows 95 e Windows 98.
ms.assetid: c4cb2e74-b37d-4c76-8d21-d71bc9c19a4a
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo LM-pwd-History
- Esquema de AD do atributo lmPwdHistory
topic_type:
- apiref
api_name:
- Lm-Pwd-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28f5c73b35bb0ea2cae9d01324d82e1568485541
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825237"
---
# <a name="lm-pwd-history-attribute"></a><span data-ttu-id="40862-106">Atributo LM-pwd-History</span><span class="sxs-lookup"><span data-stu-id="40862-106">Lm-Pwd-History attribute</span></span>

<span data-ttu-id="40862-107">O histórico de senha do usuário no formato unidirecional do LM (LAN Manager) ().</span><span class="sxs-lookup"><span data-stu-id="40862-107">The password history of the user in LAN Manager (LM) one-way format (OWF).</span></span> <span data-ttu-id="40862-108">O LM OWF é usado para compatibilidade com o LAN Manager 2. *x* clients, Windows 95 e Windows 98.</span><span class="sxs-lookup"><span data-stu-id="40862-108">The LM OWF is used for compatibility with LAN Manager 2.*x* clients, Windows 95, and Windows 98.</span></span>



| <span data-ttu-id="40862-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="40862-109">Entry</span></span> | <span data-ttu-id="40862-110">Valor</span><span class="sxs-lookup"><span data-stu-id="40862-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="40862-111">CN</span><span class="sxs-lookup"><span data-stu-id="40862-111">CN</span></span>                | <span data-ttu-id="40862-112">LM-pwd-History</span><span class="sxs-lookup"><span data-stu-id="40862-112">Lm-Pwd-History</span></span>                                        |
| <span data-ttu-id="40862-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="40862-113">Ldap-Display-Name</span></span> | <span data-ttu-id="40862-114">lmPwdHistory</span><span class="sxs-lookup"><span data-stu-id="40862-114">lmPwdHistory</span></span>                                          |
| <span data-ttu-id="40862-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="40862-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="40862-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="40862-116">Update Privilege</span></span>  | <span data-ttu-id="40862-117">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="40862-117">Domain administrator</span></span>                                  |
| <span data-ttu-id="40862-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="40862-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="40862-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="40862-119">Attribute-Id</span></span>      | <span data-ttu-id="40862-120">1.2.840.113556.1.4.160</span><span class="sxs-lookup"><span data-stu-id="40862-120">1.2.840.113556.1.4.160</span></span>                                |
| <span data-ttu-id="40862-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="40862-121">System-Id-Guid</span></span>    | <span data-ttu-id="40862-122">bf96799d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="40862-122">bf96799d-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="40862-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="40862-123">Syntax</span></span>            | [<span data-ttu-id="40862-124">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="40862-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="40862-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="40862-125">Implementations</span></span>

-   [<span data-ttu-id="40862-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="40862-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="40862-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="40862-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="40862-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="40862-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="40862-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="40862-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="40862-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="40862-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="40862-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="40862-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="40862-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="40862-132">Windows 2000 Server</span></span>



| <span data-ttu-id="40862-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="40862-133">Entry</span></span> | <span data-ttu-id="40862-134">Valor</span><span class="sxs-lookup"><span data-stu-id="40862-134">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="40862-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="40862-135">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="40862-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40862-136">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="40862-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="40862-137">System-Only</span></span>            | <span data-ttu-id="40862-138">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-138">False</span></span>                             |
| <span data-ttu-id="40862-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="40862-139">Is-Single-Valued</span></span>       | <span data-ttu-id="40862-140">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-140">False</span></span>                             |
| <span data-ttu-id="40862-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="40862-141">Is Indexed</span></span>             | <span data-ttu-id="40862-142">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-142">False</span></span>                             |
| <span data-ttu-id="40862-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="40862-143">In Global Catalog</span></span>      | <span data-ttu-id="40862-144">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-144">False</span></span>                             |
| <span data-ttu-id="40862-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="40862-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="40862-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="40862-146">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="40862-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40862-147">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="40862-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40862-148">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="40862-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40862-149">Search-Flags</span></span>           | <span data-ttu-id="40862-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40862-150">0x00000000</span></span>                        |
| <span data-ttu-id="40862-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40862-151">System-Flags</span></span>           | <span data-ttu-id="40862-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40862-152">0x00000010</span></span>                        |
| <span data-ttu-id="40862-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="40862-153">Classes used in</span></span>        | [<span data-ttu-id="40862-154">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="40862-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="40862-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="40862-155">Windows Server 2003</span></span>



| <span data-ttu-id="40862-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="40862-156">Entry</span></span> | <span data-ttu-id="40862-157">Valor</span><span class="sxs-lookup"><span data-stu-id="40862-157">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="40862-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="40862-158">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="40862-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40862-159">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="40862-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="40862-160">System-Only</span></span>            | <span data-ttu-id="40862-161">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-161">False</span></span>                             |
| <span data-ttu-id="40862-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="40862-162">Is-Single-Valued</span></span>       | <span data-ttu-id="40862-163">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-163">False</span></span>                             |
| <span data-ttu-id="40862-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="40862-164">Is Indexed</span></span>             | <span data-ttu-id="40862-165">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-165">False</span></span>                             |
| <span data-ttu-id="40862-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="40862-166">In Global Catalog</span></span>      | <span data-ttu-id="40862-167">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-167">False</span></span>                             |
| <span data-ttu-id="40862-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="40862-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="40862-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="40862-169">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="40862-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40862-170">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="40862-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40862-171">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="40862-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40862-172">Search-Flags</span></span>           | <span data-ttu-id="40862-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40862-173">0x00000000</span></span>                        |
| <span data-ttu-id="40862-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40862-174">System-Flags</span></span>           | <span data-ttu-id="40862-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40862-175">0x00000010</span></span>                        |
| <span data-ttu-id="40862-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="40862-176">Classes used in</span></span>        | [<span data-ttu-id="40862-177">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="40862-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="40862-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="40862-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="40862-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="40862-179">Entry</span></span> | <span data-ttu-id="40862-180">Valor</span><span class="sxs-lookup"><span data-stu-id="40862-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="40862-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="40862-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="40862-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40862-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="40862-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="40862-183">System-Only</span></span>            | <span data-ttu-id="40862-184">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-184">False</span></span>                             |
| <span data-ttu-id="40862-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="40862-185">Is-Single-Valued</span></span>       | <span data-ttu-id="40862-186">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-186">False</span></span>                             |
| <span data-ttu-id="40862-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="40862-187">Is Indexed</span></span>             | <span data-ttu-id="40862-188">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-188">False</span></span>                             |
| <span data-ttu-id="40862-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="40862-189">In Global Catalog</span></span>      | <span data-ttu-id="40862-190">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-190">False</span></span>                             |
| <span data-ttu-id="40862-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="40862-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="40862-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="40862-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="40862-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40862-193">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="40862-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40862-194">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="40862-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40862-195">Search-Flags</span></span>           | <span data-ttu-id="40862-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40862-196">0x00000000</span></span>                        |
| <span data-ttu-id="40862-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40862-197">System-Flags</span></span>           | <span data-ttu-id="40862-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40862-198">0x00000010</span></span>                        |
| <span data-ttu-id="40862-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="40862-199">Classes used in</span></span>        | [<span data-ttu-id="40862-200">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="40862-200">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="40862-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40862-201">Windows Server 2008</span></span>



| <span data-ttu-id="40862-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="40862-202">Entry</span></span> | <span data-ttu-id="40862-203">Valor</span><span class="sxs-lookup"><span data-stu-id="40862-203">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="40862-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="40862-204">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="40862-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40862-205">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="40862-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="40862-206">System-Only</span></span>            | <span data-ttu-id="40862-207">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-207">False</span></span>                             |
| <span data-ttu-id="40862-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="40862-208">Is-Single-Valued</span></span>       | <span data-ttu-id="40862-209">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-209">False</span></span>                             |
| <span data-ttu-id="40862-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="40862-210">Is Indexed</span></span>             | <span data-ttu-id="40862-211">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-211">False</span></span>                             |
| <span data-ttu-id="40862-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="40862-212">In Global Catalog</span></span>      | <span data-ttu-id="40862-213">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-213">False</span></span>                             |
| <span data-ttu-id="40862-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="40862-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="40862-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="40862-215">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="40862-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40862-216">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="40862-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40862-217">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="40862-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40862-218">Search-Flags</span></span>           | <span data-ttu-id="40862-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40862-219">0x00000000</span></span>                        |
| <span data-ttu-id="40862-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40862-220">System-Flags</span></span>           | <span data-ttu-id="40862-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40862-221">0x00000010</span></span>                        |
| <span data-ttu-id="40862-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="40862-222">Classes used in</span></span>        | [<span data-ttu-id="40862-223">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="40862-223">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="40862-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="40862-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="40862-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="40862-225">Entry</span></span> | <span data-ttu-id="40862-226">Valor</span><span class="sxs-lookup"><span data-stu-id="40862-226">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="40862-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="40862-227">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="40862-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40862-228">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="40862-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="40862-229">System-Only</span></span>            | <span data-ttu-id="40862-230">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-230">False</span></span>                             |
| <span data-ttu-id="40862-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="40862-231">Is-Single-Valued</span></span>       | <span data-ttu-id="40862-232">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-232">False</span></span>                             |
| <span data-ttu-id="40862-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="40862-233">Is Indexed</span></span>             | <span data-ttu-id="40862-234">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-234">False</span></span>                             |
| <span data-ttu-id="40862-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="40862-235">In Global Catalog</span></span>      | <span data-ttu-id="40862-236">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-236">False</span></span>                             |
| <span data-ttu-id="40862-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="40862-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="40862-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="40862-238">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="40862-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40862-239">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="40862-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40862-240">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="40862-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40862-241">Search-Flags</span></span>           | <span data-ttu-id="40862-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40862-242">0x00000000</span></span>                        |
| <span data-ttu-id="40862-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40862-243">System-Flags</span></span>           | <span data-ttu-id="40862-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40862-244">0x00000010</span></span>                        |
| <span data-ttu-id="40862-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="40862-245">Classes used in</span></span>        | [<span data-ttu-id="40862-246">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="40862-246">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="40862-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="40862-247">Windows Server 2012</span></span>



| <span data-ttu-id="40862-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="40862-248">Entry</span></span> | <span data-ttu-id="40862-249">Valor</span><span class="sxs-lookup"><span data-stu-id="40862-249">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="40862-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="40862-250">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="40862-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="40862-251">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="40862-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="40862-252">System-Only</span></span>            | <span data-ttu-id="40862-253">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-253">False</span></span>                             |
| <span data-ttu-id="40862-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="40862-254">Is-Single-Valued</span></span>       | <span data-ttu-id="40862-255">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-255">False</span></span>                             |
| <span data-ttu-id="40862-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="40862-256">Is Indexed</span></span>             | <span data-ttu-id="40862-257">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-257">False</span></span>                             |
| <span data-ttu-id="40862-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="40862-258">In Global Catalog</span></span>      | <span data-ttu-id="40862-259">Falso</span><span class="sxs-lookup"><span data-stu-id="40862-259">False</span></span>                             |
| <span data-ttu-id="40862-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="40862-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="40862-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="40862-261">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="40862-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="40862-262">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="40862-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="40862-263">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="40862-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="40862-264">Search-Flags</span></span>           | <span data-ttu-id="40862-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="40862-265">0x00000000</span></span>                        |
| <span data-ttu-id="40862-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="40862-266">System-Flags</span></span>           | <span data-ttu-id="40862-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40862-267">0x00000010</span></span>                        |
| <span data-ttu-id="40862-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="40862-268">Classes used in</span></span>        | [<span data-ttu-id="40862-269">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="40862-269">**User**</span></span>](c-user.md)<br/> |



 

 





