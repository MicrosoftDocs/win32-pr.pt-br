---
title: Atributo ALT-Security-Identitiess
description: Contém mapeamentos para certificados X. 509 ou contas de usuário Kerberos externas para esse usuário para fins de autenticação.
ms.assetid: 40b2af9c-fd4f-4883-8494-2b64682ee50c
ms.tgt_platform: multiple
keywords:
- Atributo ALT-Security-Identities do AD Schema
- Esquema de AD do atributo altSecurityIdentities
topic_type:
- apiref
api_name:
- Alt-Security-Identities
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2548e337f29778400bb173a8c15d928d7b06d988
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919373"
---
# <a name="alt-security-identities-attribute"></a><span data-ttu-id="b1a07-105">Atributo ALT-Security-Identitiess</span><span class="sxs-lookup"><span data-stu-id="b1a07-105">Alt-Security-Identities attribute</span></span>

<span data-ttu-id="b1a07-106">Contém mapeamentos para certificados X. 509 ou contas de usuário Kerberos externas para esse usuário para fins de autenticação.</span><span class="sxs-lookup"><span data-stu-id="b1a07-106">Contains mappings for X.509 certificates or external Kerberos user accounts to this user for the purpose of authentication.</span></span>



| <span data-ttu-id="b1a07-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1a07-107">Entry</span></span> | <span data-ttu-id="b1a07-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b1a07-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="b1a07-109">CN</span><span class="sxs-lookup"><span data-stu-id="b1a07-109">CN</span></span>                | <span data-ttu-id="b1a07-110">Alt-segurança-identidades</span><span class="sxs-lookup"><span data-stu-id="b1a07-110">Alt-Security-Identities</span></span>                             |
| <span data-ttu-id="b1a07-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b1a07-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b1a07-112">altSecurityIdentities</span><span class="sxs-lookup"><span data-stu-id="b1a07-112">altSecurityIdentities</span></span>                               |
| <span data-ttu-id="b1a07-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b1a07-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="b1a07-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="b1a07-114">Update Privilege</span></span>  | <span data-ttu-id="b1a07-115">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="b1a07-115">Domain administrator</span></span>                                |
| <span data-ttu-id="b1a07-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="b1a07-116">Update Frequency</span></span>  | <span data-ttu-id="b1a07-117">Cada vez que um novo mecanismo de autenticação é necessário.</span><span class="sxs-lookup"><span data-stu-id="b1a07-117">Each time a new authentication mechanism is needed.</span></span> |
| <span data-ttu-id="b1a07-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b1a07-118">Attribute-Id</span></span>      | <span data-ttu-id="b1a07-119">1.2.840.113556.1.4.867</span><span class="sxs-lookup"><span data-stu-id="b1a07-119">1.2.840.113556.1.4.867</span></span>                              |
| <span data-ttu-id="b1a07-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b1a07-120">System-Id-Guid</span></span>    | <span data-ttu-id="b1a07-121">00fbf30c-91fe-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="b1a07-121">00fbf30c-91fe-11d1-aebc-0000f80367c1</span></span>                |
| <span data-ttu-id="b1a07-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1a07-122">Syntax</span></span>            | [<span data-ttu-id="b1a07-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b1a07-123">**String(Unicode)**</span></span>](s-string-unicode.md)         |



## <a name="implementations"></a><span data-ttu-id="b1a07-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="b1a07-124">Implementations</span></span>

-   [<span data-ttu-id="b1a07-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b1a07-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b1a07-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b1a07-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b1a07-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b1a07-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b1a07-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b1a07-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b1a07-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b1a07-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b1a07-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b1a07-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b1a07-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b1a07-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b1a07-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1a07-132">Entry</span></span> | <span data-ttu-id="b1a07-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b1a07-133">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b1a07-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="b1a07-134">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b1a07-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1a07-135">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b1a07-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1a07-136">System-Only</span></span>            | <span data-ttu-id="b1a07-137">Falso</span><span class="sxs-lookup"><span data-stu-id="b1a07-137">False</span></span>                                                        |
| <span data-ttu-id="b1a07-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b1a07-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b1a07-139">Falso</span><span class="sxs-lookup"><span data-stu-id="b1a07-139">False</span></span>                                                        |
| <span data-ttu-id="b1a07-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="b1a07-140">Is Indexed</span></span>             | <span data-ttu-id="b1a07-141">True</span><span class="sxs-lookup"><span data-stu-id="b1a07-141">True</span></span>                                                         |
| <span data-ttu-id="b1a07-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b1a07-142">In Global Catalog</span></span>      | <span data-ttu-id="b1a07-143">True</span><span class="sxs-lookup"><span data-stu-id="b1a07-143">True</span></span>                                                         |
| <span data-ttu-id="b1a07-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b1a07-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1a07-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b1a07-145">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b1a07-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1a07-146">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b1a07-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1a07-147">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b1a07-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1a07-148">Search-Flags</span></span>           | <span data-ttu-id="b1a07-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b1a07-149">0x00000001</span></span>                                                   |
| <span data-ttu-id="b1a07-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1a07-150">System-Flags</span></span>           | <span data-ttu-id="b1a07-151">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b1a07-151">0x00000012</span></span>                                                   |
| <span data-ttu-id="b1a07-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b1a07-152">Classes used in</span></span>        | [<span data-ttu-id="b1a07-153">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="b1a07-153">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b1a07-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1a07-154">Windows Server 2003</span></span>



| <span data-ttu-id="b1a07-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1a07-155">Entry</span></span> | <span data-ttu-id="b1a07-156">Valor</span><span class="sxs-lookup"><span data-stu-id="b1a07-156">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b1a07-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="b1a07-157">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b1a07-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1a07-158">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b1a07-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1a07-159">System-Only</span></span>            | <span data-ttu-id="b1a07-160">Falso</span><span class="sxs-lookup"><span data-stu-id="b1a07-160">False</span></span>                                                        |
| <span data-ttu-id="b1a07-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b1a07-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b1a07-162">Falso</span><span class="sxs-lookup"><span data-stu-id="b1a07-162">False</span></span>                                                        |
| <span data-ttu-id="b1a07-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="b1a07-163">Is Indexed</span></span>             | <span data-ttu-id="b1a07-164">True</span><span class="sxs-lookup"><span data-stu-id="b1a07-164">True</span></span>                                                         |
| <span data-ttu-id="b1a07-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b1a07-165">In Global Catalog</span></span>      | <span data-ttu-id="b1a07-166">True</span><span class="sxs-lookup"><span data-stu-id="b1a07-166">True</span></span>                                                         |
| <span data-ttu-id="b1a07-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b1a07-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1a07-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b1a07-168">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b1a07-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1a07-169">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b1a07-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1a07-170">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b1a07-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1a07-171">Search-Flags</span></span>           | <span data-ttu-id="b1a07-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b1a07-172">0x00000001</span></span>                                                   |
| <span data-ttu-id="b1a07-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1a07-173">System-Flags</span></span>           | <span data-ttu-id="b1a07-174">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b1a07-174">0x00000012</span></span>                                                   |
| <span data-ttu-id="b1a07-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b1a07-175">Classes used in</span></span>        | [<span data-ttu-id="b1a07-176">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="b1a07-176">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b1a07-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b1a07-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b1a07-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1a07-178">Entry</span></span> | <span data-ttu-id="b1a07-179">Valor</span><span class="sxs-lookup"><span data-stu-id="b1a07-179">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b1a07-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="b1a07-180">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b1a07-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1a07-181">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b1a07-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1a07-182">System-Only</span></span>            | <span data-ttu-id="b1a07-183">Falso</span><span class="sxs-lookup"><span data-stu-id="b1a07-183">False</span></span>                                                        |
| <span data-ttu-id="b1a07-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b1a07-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b1a07-185">Falso</span><span class="sxs-lookup"><span data-stu-id="b1a07-185">False</span></span>                                                        |
| <span data-ttu-id="b1a07-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="b1a07-186">Is Indexed</span></span>             | <span data-ttu-id="b1a07-187">True</span><span class="sxs-lookup"><span data-stu-id="b1a07-187">True</span></span>                                                         |
| <span data-ttu-id="b1a07-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b1a07-188">In Global Catalog</span></span>      | <span data-ttu-id="b1a07-189">True</span><span class="sxs-lookup"><span data-stu-id="b1a07-189">True</span></span>                                                         |
| <span data-ttu-id="b1a07-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b1a07-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1a07-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b1a07-191">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b1a07-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1a07-192">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b1a07-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1a07-193">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b1a07-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1a07-194">Search-Flags</span></span>           | <span data-ttu-id="b1a07-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b1a07-195">0x00000001</span></span>                                                   |
| <span data-ttu-id="b1a07-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1a07-196">System-Flags</span></span>           | <span data-ttu-id="b1a07-197">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b1a07-197">0x00000012</span></span>                                                   |
| <span data-ttu-id="b1a07-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b1a07-198">Classes used in</span></span>        | [<span data-ttu-id="b1a07-199">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="b1a07-199">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b1a07-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1a07-200">Windows Server 2008</span></span>



| <span data-ttu-id="b1a07-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1a07-201">Entry</span></span> | <span data-ttu-id="b1a07-202">Valor</span><span class="sxs-lookup"><span data-stu-id="b1a07-202">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b1a07-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="b1a07-203">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b1a07-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1a07-204">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b1a07-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1a07-205">System-Only</span></span>            | <span data-ttu-id="b1a07-206">Falso</span><span class="sxs-lookup"><span data-stu-id="b1a07-206">False</span></span>                                                        |
| <span data-ttu-id="b1a07-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b1a07-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b1a07-208">Falso</span><span class="sxs-lookup"><span data-stu-id="b1a07-208">False</span></span>                                                        |
| <span data-ttu-id="b1a07-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="b1a07-209">Is Indexed</span></span>             | <span data-ttu-id="b1a07-210">True</span><span class="sxs-lookup"><span data-stu-id="b1a07-210">True</span></span>                                                         |
| <span data-ttu-id="b1a07-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b1a07-211">In Global Catalog</span></span>      | <span data-ttu-id="b1a07-212">True</span><span class="sxs-lookup"><span data-stu-id="b1a07-212">True</span></span>                                                         |
| <span data-ttu-id="b1a07-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b1a07-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1a07-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b1a07-214">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b1a07-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1a07-215">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b1a07-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1a07-216">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b1a07-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1a07-217">Search-Flags</span></span>           | <span data-ttu-id="b1a07-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b1a07-218">0x00000001</span></span>                                                   |
| <span data-ttu-id="b1a07-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1a07-219">System-Flags</span></span>           | <span data-ttu-id="b1a07-220">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b1a07-220">0x00000012</span></span>                                                   |
| <span data-ttu-id="b1a07-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b1a07-221">Classes used in</span></span>        | [<span data-ttu-id="b1a07-222">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="b1a07-222">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b1a07-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b1a07-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b1a07-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1a07-224">Entry</span></span> | <span data-ttu-id="b1a07-225">Valor</span><span class="sxs-lookup"><span data-stu-id="b1a07-225">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b1a07-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="b1a07-226">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b1a07-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1a07-227">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b1a07-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1a07-228">System-Only</span></span>            | <span data-ttu-id="b1a07-229">Falso</span><span class="sxs-lookup"><span data-stu-id="b1a07-229">False</span></span>                                                        |
| <span data-ttu-id="b1a07-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b1a07-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b1a07-231">Falso</span><span class="sxs-lookup"><span data-stu-id="b1a07-231">False</span></span>                                                        |
| <span data-ttu-id="b1a07-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="b1a07-232">Is Indexed</span></span>             | <span data-ttu-id="b1a07-233">True</span><span class="sxs-lookup"><span data-stu-id="b1a07-233">True</span></span>                                                         |
| <span data-ttu-id="b1a07-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b1a07-234">In Global Catalog</span></span>      | <span data-ttu-id="b1a07-235">True</span><span class="sxs-lookup"><span data-stu-id="b1a07-235">True</span></span>                                                         |
| <span data-ttu-id="b1a07-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b1a07-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1a07-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b1a07-237">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b1a07-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1a07-238">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b1a07-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1a07-239">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b1a07-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1a07-240">Search-Flags</span></span>           | <span data-ttu-id="b1a07-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b1a07-241">0x00000001</span></span>                                                   |
| <span data-ttu-id="b1a07-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1a07-242">System-Flags</span></span>           | <span data-ttu-id="b1a07-243">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b1a07-243">0x00000012</span></span>                                                   |
| <span data-ttu-id="b1a07-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b1a07-244">Classes used in</span></span>        | [<span data-ttu-id="b1a07-245">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="b1a07-245">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b1a07-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1a07-246">Windows Server 2012</span></span>



| <span data-ttu-id="b1a07-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="b1a07-247">Entry</span></span> | <span data-ttu-id="b1a07-248">Valor</span><span class="sxs-lookup"><span data-stu-id="b1a07-248">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b1a07-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="b1a07-249">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b1a07-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1a07-250">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b1a07-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1a07-251">System-Only</span></span>            | <span data-ttu-id="b1a07-252">Falso</span><span class="sxs-lookup"><span data-stu-id="b1a07-252">False</span></span>                                                        |
| <span data-ttu-id="b1a07-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b1a07-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b1a07-254">Falso</span><span class="sxs-lookup"><span data-stu-id="b1a07-254">False</span></span>                                                        |
| <span data-ttu-id="b1a07-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="b1a07-255">Is Indexed</span></span>             | <span data-ttu-id="b1a07-256">True</span><span class="sxs-lookup"><span data-stu-id="b1a07-256">True</span></span>                                                         |
| <span data-ttu-id="b1a07-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b1a07-257">In Global Catalog</span></span>      | <span data-ttu-id="b1a07-258">True</span><span class="sxs-lookup"><span data-stu-id="b1a07-258">True</span></span>                                                         |
| <span data-ttu-id="b1a07-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b1a07-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1a07-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b1a07-260">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b1a07-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1a07-261">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b1a07-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1a07-262">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b1a07-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1a07-263">Search-Flags</span></span>           | <span data-ttu-id="b1a07-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b1a07-264">0x00000001</span></span>                                                   |
| <span data-ttu-id="b1a07-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1a07-265">System-Flags</span></span>           | <span data-ttu-id="b1a07-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b1a07-266">0x00000012</span></span>                                                   |
| <span data-ttu-id="b1a07-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b1a07-267">Classes used in</span></span>        | [<span data-ttu-id="b1a07-268">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="b1a07-268">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





