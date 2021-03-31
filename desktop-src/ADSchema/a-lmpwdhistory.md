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
# <a name="lm-pwd-history-attribute"></a><span data-ttu-id="afc5b-106">Atributo LM-pwd-History</span><span class="sxs-lookup"><span data-stu-id="afc5b-106">Lm-Pwd-History attribute</span></span>

<span data-ttu-id="afc5b-107">O histórico de senha do usuário no formato unidirecional do LM (LAN Manager) ().</span><span class="sxs-lookup"><span data-stu-id="afc5b-107">The password history of the user in LAN Manager (LM) one-way format (OWF).</span></span> <span data-ttu-id="afc5b-108">O LM OWF é usado para compatibilidade com o LAN Manager 2. *x* clients, Windows 95 e Windows 98.</span><span class="sxs-lookup"><span data-stu-id="afc5b-108">The LM OWF is used for compatibility with LAN Manager 2.*x* clients, Windows 95, and Windows 98.</span></span>



| <span data-ttu-id="afc5b-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="afc5b-109">Entry</span></span> | <span data-ttu-id="afc5b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="afc5b-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="afc5b-111">CN</span><span class="sxs-lookup"><span data-stu-id="afc5b-111">CN</span></span>                | <span data-ttu-id="afc5b-112">LM-pwd-History</span><span class="sxs-lookup"><span data-stu-id="afc5b-112">Lm-Pwd-History</span></span>                                        |
| <span data-ttu-id="afc5b-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="afc5b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="afc5b-114">lmPwdHistory</span><span class="sxs-lookup"><span data-stu-id="afc5b-114">lmPwdHistory</span></span>                                          |
| <span data-ttu-id="afc5b-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="afc5b-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="afc5b-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="afc5b-116">Update Privilege</span></span>  | <span data-ttu-id="afc5b-117">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="afc5b-117">Domain administrator</span></span>                                  |
| <span data-ttu-id="afc5b-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="afc5b-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="afc5b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="afc5b-119">Attribute-Id</span></span>      | <span data-ttu-id="afc5b-120">1.2.840.113556.1.4.160</span><span class="sxs-lookup"><span data-stu-id="afc5b-120">1.2.840.113556.1.4.160</span></span>                                |
| <span data-ttu-id="afc5b-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="afc5b-121">System-Id-Guid</span></span>    | <span data-ttu-id="afc5b-122">bf96799d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="afc5b-122">bf96799d-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="afc5b-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="afc5b-123">Syntax</span></span>            | [<span data-ttu-id="afc5b-124">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="afc5b-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="afc5b-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="afc5b-125">Implementations</span></span>

-   [<span data-ttu-id="afc5b-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="afc5b-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="afc5b-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="afc5b-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="afc5b-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="afc5b-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="afc5b-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="afc5b-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="afc5b-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="afc5b-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="afc5b-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="afc5b-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="afc5b-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="afc5b-132">Windows 2000 Server</span></span>



| <span data-ttu-id="afc5b-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="afc5b-133">Entry</span></span> | <span data-ttu-id="afc5b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="afc5b-134">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="afc5b-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="afc5b-135">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="afc5b-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afc5b-136">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="afc5b-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="afc5b-137">System-Only</span></span>            | <span data-ttu-id="afc5b-138">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-138">False</span></span>                             |
| <span data-ttu-id="afc5b-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="afc5b-139">Is-Single-Valued</span></span>       | <span data-ttu-id="afc5b-140">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-140">False</span></span>                             |
| <span data-ttu-id="afc5b-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="afc5b-141">Is Indexed</span></span>             | <span data-ttu-id="afc5b-142">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-142">False</span></span>                             |
| <span data-ttu-id="afc5b-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="afc5b-143">In Global Catalog</span></span>      | <span data-ttu-id="afc5b-144">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-144">False</span></span>                             |
| <span data-ttu-id="afc5b-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="afc5b-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="afc5b-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="afc5b-146">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="afc5b-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afc5b-147">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="afc5b-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afc5b-148">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="afc5b-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afc5b-149">Search-Flags</span></span>           | <span data-ttu-id="afc5b-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afc5b-150">0x00000000</span></span>                        |
| <span data-ttu-id="afc5b-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afc5b-151">System-Flags</span></span>           | <span data-ttu-id="afc5b-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afc5b-152">0x00000010</span></span>                        |
| <span data-ttu-id="afc5b-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="afc5b-153">Classes used in</span></span>        | [<span data-ttu-id="afc5b-154">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="afc5b-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="afc5b-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="afc5b-155">Windows Server 2003</span></span>



| <span data-ttu-id="afc5b-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="afc5b-156">Entry</span></span> | <span data-ttu-id="afc5b-157">Valor</span><span class="sxs-lookup"><span data-stu-id="afc5b-157">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="afc5b-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="afc5b-158">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="afc5b-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afc5b-159">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="afc5b-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="afc5b-160">System-Only</span></span>            | <span data-ttu-id="afc5b-161">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-161">False</span></span>                             |
| <span data-ttu-id="afc5b-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="afc5b-162">Is-Single-Valued</span></span>       | <span data-ttu-id="afc5b-163">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-163">False</span></span>                             |
| <span data-ttu-id="afc5b-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="afc5b-164">Is Indexed</span></span>             | <span data-ttu-id="afc5b-165">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-165">False</span></span>                             |
| <span data-ttu-id="afc5b-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="afc5b-166">In Global Catalog</span></span>      | <span data-ttu-id="afc5b-167">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-167">False</span></span>                             |
| <span data-ttu-id="afc5b-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="afc5b-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="afc5b-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="afc5b-169">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="afc5b-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afc5b-170">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="afc5b-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afc5b-171">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="afc5b-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afc5b-172">Search-Flags</span></span>           | <span data-ttu-id="afc5b-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afc5b-173">0x00000000</span></span>                        |
| <span data-ttu-id="afc5b-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afc5b-174">System-Flags</span></span>           | <span data-ttu-id="afc5b-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afc5b-175">0x00000010</span></span>                        |
| <span data-ttu-id="afc5b-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="afc5b-176">Classes used in</span></span>        | [<span data-ttu-id="afc5b-177">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="afc5b-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="afc5b-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="afc5b-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="afc5b-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="afc5b-179">Entry</span></span> | <span data-ttu-id="afc5b-180">Valor</span><span class="sxs-lookup"><span data-stu-id="afc5b-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="afc5b-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="afc5b-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="afc5b-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afc5b-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="afc5b-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="afc5b-183">System-Only</span></span>            | <span data-ttu-id="afc5b-184">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-184">False</span></span>                             |
| <span data-ttu-id="afc5b-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="afc5b-185">Is-Single-Valued</span></span>       | <span data-ttu-id="afc5b-186">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-186">False</span></span>                             |
| <span data-ttu-id="afc5b-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="afc5b-187">Is Indexed</span></span>             | <span data-ttu-id="afc5b-188">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-188">False</span></span>                             |
| <span data-ttu-id="afc5b-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="afc5b-189">In Global Catalog</span></span>      | <span data-ttu-id="afc5b-190">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-190">False</span></span>                             |
| <span data-ttu-id="afc5b-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="afc5b-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="afc5b-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="afc5b-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="afc5b-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afc5b-193">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="afc5b-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afc5b-194">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="afc5b-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afc5b-195">Search-Flags</span></span>           | <span data-ttu-id="afc5b-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afc5b-196">0x00000000</span></span>                        |
| <span data-ttu-id="afc5b-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afc5b-197">System-Flags</span></span>           | <span data-ttu-id="afc5b-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afc5b-198">0x00000010</span></span>                        |
| <span data-ttu-id="afc5b-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="afc5b-199">Classes used in</span></span>        | [<span data-ttu-id="afc5b-200">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="afc5b-200">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="afc5b-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afc5b-201">Windows Server 2008</span></span>



| <span data-ttu-id="afc5b-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="afc5b-202">Entry</span></span> | <span data-ttu-id="afc5b-203">Valor</span><span class="sxs-lookup"><span data-stu-id="afc5b-203">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="afc5b-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="afc5b-204">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="afc5b-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afc5b-205">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="afc5b-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="afc5b-206">System-Only</span></span>            | <span data-ttu-id="afc5b-207">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-207">False</span></span>                             |
| <span data-ttu-id="afc5b-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="afc5b-208">Is-Single-Valued</span></span>       | <span data-ttu-id="afc5b-209">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-209">False</span></span>                             |
| <span data-ttu-id="afc5b-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="afc5b-210">Is Indexed</span></span>             | <span data-ttu-id="afc5b-211">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-211">False</span></span>                             |
| <span data-ttu-id="afc5b-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="afc5b-212">In Global Catalog</span></span>      | <span data-ttu-id="afc5b-213">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-213">False</span></span>                             |
| <span data-ttu-id="afc5b-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="afc5b-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="afc5b-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="afc5b-215">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="afc5b-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afc5b-216">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="afc5b-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afc5b-217">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="afc5b-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afc5b-218">Search-Flags</span></span>           | <span data-ttu-id="afc5b-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afc5b-219">0x00000000</span></span>                        |
| <span data-ttu-id="afc5b-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afc5b-220">System-Flags</span></span>           | <span data-ttu-id="afc5b-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afc5b-221">0x00000010</span></span>                        |
| <span data-ttu-id="afc5b-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="afc5b-222">Classes used in</span></span>        | [<span data-ttu-id="afc5b-223">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="afc5b-223">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="afc5b-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="afc5b-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="afc5b-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="afc5b-225">Entry</span></span> | <span data-ttu-id="afc5b-226">Valor</span><span class="sxs-lookup"><span data-stu-id="afc5b-226">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="afc5b-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="afc5b-227">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="afc5b-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afc5b-228">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="afc5b-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="afc5b-229">System-Only</span></span>            | <span data-ttu-id="afc5b-230">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-230">False</span></span>                             |
| <span data-ttu-id="afc5b-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="afc5b-231">Is-Single-Valued</span></span>       | <span data-ttu-id="afc5b-232">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-232">False</span></span>                             |
| <span data-ttu-id="afc5b-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="afc5b-233">Is Indexed</span></span>             | <span data-ttu-id="afc5b-234">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-234">False</span></span>                             |
| <span data-ttu-id="afc5b-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="afc5b-235">In Global Catalog</span></span>      | <span data-ttu-id="afc5b-236">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-236">False</span></span>                             |
| <span data-ttu-id="afc5b-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="afc5b-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="afc5b-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="afc5b-238">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="afc5b-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afc5b-239">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="afc5b-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afc5b-240">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="afc5b-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afc5b-241">Search-Flags</span></span>           | <span data-ttu-id="afc5b-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afc5b-242">0x00000000</span></span>                        |
| <span data-ttu-id="afc5b-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afc5b-243">System-Flags</span></span>           | <span data-ttu-id="afc5b-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afc5b-244">0x00000010</span></span>                        |
| <span data-ttu-id="afc5b-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="afc5b-245">Classes used in</span></span>        | [<span data-ttu-id="afc5b-246">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="afc5b-246">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="afc5b-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="afc5b-247">Windows Server 2012</span></span>



| <span data-ttu-id="afc5b-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="afc5b-248">Entry</span></span> | <span data-ttu-id="afc5b-249">Valor</span><span class="sxs-lookup"><span data-stu-id="afc5b-249">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="afc5b-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="afc5b-250">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="afc5b-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afc5b-251">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="afc5b-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="afc5b-252">System-Only</span></span>            | <span data-ttu-id="afc5b-253">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-253">False</span></span>                             |
| <span data-ttu-id="afc5b-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="afc5b-254">Is-Single-Valued</span></span>       | <span data-ttu-id="afc5b-255">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-255">False</span></span>                             |
| <span data-ttu-id="afc5b-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="afc5b-256">Is Indexed</span></span>             | <span data-ttu-id="afc5b-257">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-257">False</span></span>                             |
| <span data-ttu-id="afc5b-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="afc5b-258">In Global Catalog</span></span>      | <span data-ttu-id="afc5b-259">Falso</span><span class="sxs-lookup"><span data-stu-id="afc5b-259">False</span></span>                             |
| <span data-ttu-id="afc5b-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="afc5b-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="afc5b-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="afc5b-261">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="afc5b-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afc5b-262">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="afc5b-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afc5b-263">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="afc5b-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afc5b-264">Search-Flags</span></span>           | <span data-ttu-id="afc5b-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afc5b-265">0x00000000</span></span>                        |
| <span data-ttu-id="afc5b-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afc5b-266">System-Flags</span></span>           | <span data-ttu-id="afc5b-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afc5b-267">0x00000010</span></span>                        |
| <span data-ttu-id="afc5b-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="afc5b-268">Classes used in</span></span>        | [<span data-ttu-id="afc5b-269">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="afc5b-269">**User**</span></span>](c-user.md)<br/> |



 

 





