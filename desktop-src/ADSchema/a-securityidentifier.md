---
title: Security-Identifier atributo
description: Um valor exclusivo de comprimento variável usado para identificar uma conta de usuário, uma conta de grupo ou uma sessão de logon à qual uma ACE se aplica.
ms.assetid: bb6a16f6-d2c1-48f1-af9a-40fe2a59f281
ms.tgt_platform: multiple
keywords:
- Esquema de Security-Identifier do atributo AD
- Esquema de AD do atributo securityIdentifier
topic_type:
- apiref
api_name:
- Security-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd921d0bcba08c2174475007476add8e8787456
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645407"
---
# <a name="security-identifier-attribute"></a><span data-ttu-id="96919-105">Security-Identifier atributo</span><span class="sxs-lookup"><span data-stu-id="96919-105">Security-Identifier attribute</span></span>

<span data-ttu-id="96919-106">Um valor exclusivo de comprimento variável usado para identificar uma conta de usuário, uma conta de grupo ou uma sessão de logon à qual uma ACE se aplica.</span><span class="sxs-lookup"><span data-stu-id="96919-106">A unique value of variable length used to identify a user account, group account, or logon session to which an ACE applies.</span></span>



| <span data-ttu-id="96919-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="96919-107">Entry</span></span> | <span data-ttu-id="96919-108">Valor</span><span class="sxs-lookup"><span data-stu-id="96919-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="96919-109">CN</span><span class="sxs-lookup"><span data-stu-id="96919-109">CN</span></span>                | <span data-ttu-id="96919-110">Security-Identifier</span><span class="sxs-lookup"><span data-stu-id="96919-110">Security-Identifier</span></span>                  |
| <span data-ttu-id="96919-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="96919-111">Ldap-Display-Name</span></span> | <span data-ttu-id="96919-112">securityIdentifier</span><span class="sxs-lookup"><span data-stu-id="96919-112">securityIdentifier</span></span>                   |
| <span data-ttu-id="96919-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="96919-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="96919-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="96919-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="96919-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="96919-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="96919-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="96919-116">Attribute-Id</span></span>      | <span data-ttu-id="96919-117">1.2.840.113556.1.4.121</span><span class="sxs-lookup"><span data-stu-id="96919-117">1.2.840.113556.1.4.121</span></span>               |
| <span data-ttu-id="96919-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="96919-118">System-Id-Guid</span></span>    | <span data-ttu-id="96919-119">bf967a2f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="96919-119">bf967a2f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="96919-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="96919-120">Syntax</span></span>            | [<span data-ttu-id="96919-121">**Cadeia de caracteres (SID)**</span><span class="sxs-lookup"><span data-stu-id="96919-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="96919-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="96919-122">Implementations</span></span>

-   [<span data-ttu-id="96919-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="96919-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="96919-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="96919-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="96919-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="96919-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="96919-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="96919-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="96919-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="96919-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="96919-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="96919-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="96919-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="96919-129">Windows 2000 Server</span></span>



| <span data-ttu-id="96919-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="96919-130">Entry</span></span> | <span data-ttu-id="96919-131">Valor</span><span class="sxs-lookup"><span data-stu-id="96919-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96919-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="96919-132">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="96919-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96919-133">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="96919-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="96919-134">System-Only</span></span>            | <span data-ttu-id="96919-135">Falso</span><span class="sxs-lookup"><span data-stu-id="96919-135">False</span></span>                                                                                                             |
| <span data-ttu-id="96919-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="96919-136">Is-Single-Valued</span></span>       | <span data-ttu-id="96919-137">True</span><span class="sxs-lookup"><span data-stu-id="96919-137">True</span></span>                                                                                                              |
| <span data-ttu-id="96919-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="96919-138">Is Indexed</span></span>             | <span data-ttu-id="96919-139">Falso</span><span class="sxs-lookup"><span data-stu-id="96919-139">False</span></span>                                                                                                             |
| <span data-ttu-id="96919-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="96919-140">In Global Catalog</span></span>      | <span data-ttu-id="96919-141">Falso</span><span class="sxs-lookup"><span data-stu-id="96919-141">False</span></span>                                                                                                             |
| <span data-ttu-id="96919-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96919-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="96919-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="96919-143">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="96919-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96919-144">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="96919-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96919-145">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="96919-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96919-146">Search-Flags</span></span>           | <span data-ttu-id="96919-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96919-147">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="96919-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96919-148">System-Flags</span></span>           | <span data-ttu-id="96919-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96919-149">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="96919-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="96919-150">Classes used in</span></span>        | [<span data-ttu-id="96919-151">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="96919-151">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="96919-152">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="96919-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="96919-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="96919-153">Windows Server 2003</span></span>



| <span data-ttu-id="96919-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="96919-154">Entry</span></span> | <span data-ttu-id="96919-155">Valor</span><span class="sxs-lookup"><span data-stu-id="96919-155">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96919-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="96919-156">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="96919-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96919-157">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="96919-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="96919-158">System-Only</span></span>            | <span data-ttu-id="96919-159">Falso</span><span class="sxs-lookup"><span data-stu-id="96919-159">False</span></span>                                                                                                             |
| <span data-ttu-id="96919-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="96919-160">Is-Single-Valued</span></span>       | <span data-ttu-id="96919-161">True</span><span class="sxs-lookup"><span data-stu-id="96919-161">True</span></span>                                                                                                              |
| <span data-ttu-id="96919-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="96919-162">Is Indexed</span></span>             | <span data-ttu-id="96919-163">Falso</span><span class="sxs-lookup"><span data-stu-id="96919-163">False</span></span>                                                                                                             |
| <span data-ttu-id="96919-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="96919-164">In Global Catalog</span></span>      | <span data-ttu-id="96919-165">True</span><span class="sxs-lookup"><span data-stu-id="96919-165">True</span></span>                                                                                                              |
| <span data-ttu-id="96919-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96919-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="96919-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="96919-167">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="96919-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96919-168">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="96919-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96919-169">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="96919-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96919-170">Search-Flags</span></span>           | <span data-ttu-id="96919-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96919-171">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="96919-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96919-172">System-Flags</span></span>           | <span data-ttu-id="96919-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96919-173">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="96919-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="96919-174">Classes used in</span></span>        | [<span data-ttu-id="96919-175">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="96919-175">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="96919-176">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="96919-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="96919-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="96919-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="96919-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="96919-178">Entry</span></span> | <span data-ttu-id="96919-179">Valor</span><span class="sxs-lookup"><span data-stu-id="96919-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96919-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="96919-180">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="96919-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96919-181">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="96919-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="96919-182">System-Only</span></span>            | <span data-ttu-id="96919-183">Falso</span><span class="sxs-lookup"><span data-stu-id="96919-183">False</span></span>                                                                                                             |
| <span data-ttu-id="96919-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="96919-184">Is-Single-Valued</span></span>       | <span data-ttu-id="96919-185">True</span><span class="sxs-lookup"><span data-stu-id="96919-185">True</span></span>                                                                                                              |
| <span data-ttu-id="96919-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="96919-186">Is Indexed</span></span>             | <span data-ttu-id="96919-187">Falso</span><span class="sxs-lookup"><span data-stu-id="96919-187">False</span></span>                                                                                                             |
| <span data-ttu-id="96919-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="96919-188">In Global Catalog</span></span>      | <span data-ttu-id="96919-189">True</span><span class="sxs-lookup"><span data-stu-id="96919-189">True</span></span>                                                                                                              |
| <span data-ttu-id="96919-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96919-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="96919-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="96919-191">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="96919-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96919-192">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="96919-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96919-193">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="96919-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96919-194">Search-Flags</span></span>           | <span data-ttu-id="96919-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96919-195">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="96919-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96919-196">System-Flags</span></span>           | <span data-ttu-id="96919-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96919-197">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="96919-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="96919-198">Classes used in</span></span>        | [<span data-ttu-id="96919-199">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="96919-199">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="96919-200">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="96919-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="96919-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96919-201">Windows Server 2008</span></span>



| <span data-ttu-id="96919-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="96919-202">Entry</span></span> | <span data-ttu-id="96919-203">Valor</span><span class="sxs-lookup"><span data-stu-id="96919-203">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96919-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="96919-204">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="96919-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96919-205">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="96919-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="96919-206">System-Only</span></span>            | <span data-ttu-id="96919-207">Falso</span><span class="sxs-lookup"><span data-stu-id="96919-207">False</span></span>                                                                                                             |
| <span data-ttu-id="96919-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="96919-208">Is-Single-Valued</span></span>       | <span data-ttu-id="96919-209">True</span><span class="sxs-lookup"><span data-stu-id="96919-209">True</span></span>                                                                                                              |
| <span data-ttu-id="96919-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="96919-210">Is Indexed</span></span>             | <span data-ttu-id="96919-211">Falso</span><span class="sxs-lookup"><span data-stu-id="96919-211">False</span></span>                                                                                                             |
| <span data-ttu-id="96919-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="96919-212">In Global Catalog</span></span>      | <span data-ttu-id="96919-213">True</span><span class="sxs-lookup"><span data-stu-id="96919-213">True</span></span>                                                                                                              |
| <span data-ttu-id="96919-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96919-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="96919-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="96919-215">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="96919-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96919-216">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="96919-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96919-217">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="96919-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96919-218">Search-Flags</span></span>           | <span data-ttu-id="96919-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96919-219">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="96919-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96919-220">System-Flags</span></span>           | <span data-ttu-id="96919-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96919-221">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="96919-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="96919-222">Classes used in</span></span>        | [<span data-ttu-id="96919-223">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="96919-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="96919-224">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="96919-224">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="96919-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="96919-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="96919-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="96919-226">Entry</span></span> | <span data-ttu-id="96919-227">Valor</span><span class="sxs-lookup"><span data-stu-id="96919-227">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96919-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="96919-228">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="96919-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96919-229">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="96919-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="96919-230">System-Only</span></span>            | <span data-ttu-id="96919-231">Falso</span><span class="sxs-lookup"><span data-stu-id="96919-231">False</span></span>                                                                                                             |
| <span data-ttu-id="96919-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="96919-232">Is-Single-Valued</span></span>       | <span data-ttu-id="96919-233">True</span><span class="sxs-lookup"><span data-stu-id="96919-233">True</span></span>                                                                                                              |
| <span data-ttu-id="96919-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="96919-234">Is Indexed</span></span>             | <span data-ttu-id="96919-235">Falso</span><span class="sxs-lookup"><span data-stu-id="96919-235">False</span></span>                                                                                                             |
| <span data-ttu-id="96919-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="96919-236">In Global Catalog</span></span>      | <span data-ttu-id="96919-237">True</span><span class="sxs-lookup"><span data-stu-id="96919-237">True</span></span>                                                                                                              |
| <span data-ttu-id="96919-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96919-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="96919-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="96919-239">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="96919-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96919-240">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="96919-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96919-241">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="96919-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96919-242">Search-Flags</span></span>           | <span data-ttu-id="96919-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96919-243">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="96919-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96919-244">System-Flags</span></span>           | <span data-ttu-id="96919-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96919-245">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="96919-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="96919-246">Classes used in</span></span>        | [<span data-ttu-id="96919-247">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="96919-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="96919-248">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="96919-248">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="96919-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="96919-249">Windows Server 2012</span></span>



| <span data-ttu-id="96919-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="96919-250">Entry</span></span> | <span data-ttu-id="96919-251">Valor</span><span class="sxs-lookup"><span data-stu-id="96919-251">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96919-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="96919-252">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="96919-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96919-253">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="96919-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="96919-254">System-Only</span></span>            | <span data-ttu-id="96919-255">Falso</span><span class="sxs-lookup"><span data-stu-id="96919-255">False</span></span>                                                                                                             |
| <span data-ttu-id="96919-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="96919-256">Is-Single-Valued</span></span>       | <span data-ttu-id="96919-257">True</span><span class="sxs-lookup"><span data-stu-id="96919-257">True</span></span>                                                                                                              |
| <span data-ttu-id="96919-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="96919-258">Is Indexed</span></span>             | <span data-ttu-id="96919-259">Falso</span><span class="sxs-lookup"><span data-stu-id="96919-259">False</span></span>                                                                                                             |
| <span data-ttu-id="96919-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="96919-260">In Global Catalog</span></span>      | <span data-ttu-id="96919-261">True</span><span class="sxs-lookup"><span data-stu-id="96919-261">True</span></span>                                                                                                              |
| <span data-ttu-id="96919-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96919-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="96919-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="96919-263">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="96919-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96919-264">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="96919-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96919-265">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="96919-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96919-266">Search-Flags</span></span>           | <span data-ttu-id="96919-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96919-267">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="96919-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96919-268">System-Flags</span></span>           | <span data-ttu-id="96919-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96919-269">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="96919-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="96919-270">Classes used in</span></span>        | [<span data-ttu-id="96919-271">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="96919-271">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="96919-272">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="96919-272">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





