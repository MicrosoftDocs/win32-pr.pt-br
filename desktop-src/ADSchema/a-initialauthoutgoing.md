---
title: Autenticação inicial – atributo de saída
description: Contém informações sobre uma autenticação de saída inicial enviada pelo servidor de autenticação para esse domínio para o cliente que solicitou a autenticação.
ms.assetid: cc5ceb14-0424-4caa-bcd9-1e48988af67a
ms.tgt_platform: multiple
keywords:
- Esquema do AD de atributo inicial-auth-
- Esquema de AD do atributo initialAuthOutgoing
topic_type:
- apiref
api_name:
- Initial-Auth-Outgoing
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84faaa443c9589e04f4998dc41d72fe870b5f2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086677"
---
# <a name="initial-auth-outgoing-attribute"></a><span data-ttu-id="4f3ce-105">Autenticação inicial – atributo de saída</span><span class="sxs-lookup"><span data-stu-id="4f3ce-105">Initial-Auth-Outgoing attribute</span></span>

<span data-ttu-id="4f3ce-106">Contém informações sobre uma autenticação de saída inicial enviada pelo servidor de autenticação para esse domínio para o cliente que solicitou a autenticação.</span><span class="sxs-lookup"><span data-stu-id="4f3ce-106">Contains information about an initial outgoing authentication sent by the authentication server for this domain to the client that requested authentication.</span></span> <span data-ttu-id="4f3ce-107">O servidor que usa esse atributo recebe a autorização do servidor de autenticação e a envia para o cliente.</span><span class="sxs-lookup"><span data-stu-id="4f3ce-107">The server that uses this attribute receives the authorization from the authentication server and sends it to the client.</span></span>



| <span data-ttu-id="4f3ce-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f3ce-108">Entry</span></span> | <span data-ttu-id="4f3ce-109">Valor</span><span class="sxs-lookup"><span data-stu-id="4f3ce-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="4f3ce-110">CN</span><span class="sxs-lookup"><span data-stu-id="4f3ce-110">CN</span></span>                | <span data-ttu-id="4f3ce-111">Inicial-autenticação-saída</span><span class="sxs-lookup"><span data-stu-id="4f3ce-111">Initial-Auth-Outgoing</span></span>                       |
| <span data-ttu-id="4f3ce-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4f3ce-112">Ldap-Display-Name</span></span> | <span data-ttu-id="4f3ce-113">initialAuthOutgoing</span><span class="sxs-lookup"><span data-stu-id="4f3ce-113">initialAuthOutgoing</span></span>                         |
| <span data-ttu-id="4f3ce-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="4f3ce-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="4f3ce-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="4f3ce-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="4f3ce-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="4f3ce-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="4f3ce-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4f3ce-117">Attribute-Id</span></span>      | <span data-ttu-id="4f3ce-118">1.2.840.113556.1.4.540</span><span class="sxs-lookup"><span data-stu-id="4f3ce-118">1.2.840.113556.1.4.540</span></span>                      |
| <span data-ttu-id="4f3ce-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4f3ce-119">System-Id-Guid</span></span>    | <span data-ttu-id="4f3ce-120">52458024-ca6a-11D0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="4f3ce-120">52458024-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="4f3ce-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f3ce-121">Syntax</span></span>            | [<span data-ttu-id="4f3ce-122">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4f3ce-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="4f3ce-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="4f3ce-123">Implementations</span></span>

-   [<span data-ttu-id="4f3ce-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4f3ce-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4f3ce-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4f3ce-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4f3ce-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4f3ce-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4f3ce-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4f3ce-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4f3ce-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4f3ce-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4f3ce-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4f3ce-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4f3ce-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4f3ce-130">Windows 2000 Server</span></span>



| <span data-ttu-id="4f3ce-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f3ce-131">Entry</span></span> | <span data-ttu-id="4f3ce-132">Valor</span><span class="sxs-lookup"><span data-stu-id="4f3ce-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4f3ce-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="4f3ce-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4f3ce-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f3ce-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4f3ce-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f3ce-135">System-Only</span></span>            | <span data-ttu-id="4f3ce-136">Falso</span><span class="sxs-lookup"><span data-stu-id="4f3ce-136">False</span></span>                                                |
| <span data-ttu-id="4f3ce-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4f3ce-137">Is-Single-Valued</span></span>       | <span data-ttu-id="4f3ce-138">True</span><span class="sxs-lookup"><span data-stu-id="4f3ce-138">True</span></span>                                                 |
| <span data-ttu-id="4f3ce-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="4f3ce-139">Is Indexed</span></span>             | <span data-ttu-id="4f3ce-140">Falso</span><span class="sxs-lookup"><span data-stu-id="4f3ce-140">False</span></span>                                                |
| <span data-ttu-id="4f3ce-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4f3ce-141">In Global Catalog</span></span>      | <span data-ttu-id="4f3ce-142">Falso</span><span class="sxs-lookup"><span data-stu-id="4f3ce-142">False</span></span>                                                |
| <span data-ttu-id="4f3ce-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f3ce-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f3ce-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4f3ce-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4f3ce-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f3ce-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="4f3ce-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f3ce-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="4f3ce-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f3ce-147">Search-Flags</span></span>           | <span data-ttu-id="4f3ce-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f3ce-148">0x00000000</span></span>                                           |
| <span data-ttu-id="4f3ce-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f3ce-149">System-Flags</span></span>           | <span data-ttu-id="4f3ce-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f3ce-150">0x00000010</span></span>                                           |
| <span data-ttu-id="4f3ce-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4f3ce-151">Classes used in</span></span>        | [<span data-ttu-id="4f3ce-152">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="4f3ce-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4f3ce-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4f3ce-153">Windows Server 2003</span></span>



| <span data-ttu-id="4f3ce-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f3ce-154">Entry</span></span> | <span data-ttu-id="4f3ce-155">Valor</span><span class="sxs-lookup"><span data-stu-id="4f3ce-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4f3ce-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="4f3ce-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4f3ce-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f3ce-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4f3ce-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f3ce-158">System-Only</span></span>            | <span data-ttu-id="4f3ce-159">Falso</span><span class="sxs-lookup"><span data-stu-id="4f3ce-159">False</span></span>                                                |
| <span data-ttu-id="4f3ce-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4f3ce-160">Is-Single-Valued</span></span>       | <span data-ttu-id="4f3ce-161">True</span><span class="sxs-lookup"><span data-stu-id="4f3ce-161">True</span></span>                                                 |
| <span data-ttu-id="4f3ce-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="4f3ce-162">Is Indexed</span></span>             | <span data-ttu-id="4f3ce-163">Falso</span><span class="sxs-lookup"><span data-stu-id="4f3ce-163">False</span></span>                                                |
| <span data-ttu-id="4f3ce-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4f3ce-164">In Global Catalog</span></span>      | <span data-ttu-id="4f3ce-165">Falso</span><span class="sxs-lookup"><span data-stu-id="4f3ce-165">False</span></span>                                                |
| <span data-ttu-id="4f3ce-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f3ce-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f3ce-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4f3ce-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4f3ce-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f3ce-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="4f3ce-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f3ce-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="4f3ce-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f3ce-170">Search-Flags</span></span>           | <span data-ttu-id="4f3ce-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f3ce-171">0x00000000</span></span>                                           |
| <span data-ttu-id="4f3ce-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f3ce-172">System-Flags</span></span>           | <span data-ttu-id="4f3ce-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f3ce-173">0x00000010</span></span>                                           |
| <span data-ttu-id="4f3ce-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4f3ce-174">Classes used in</span></span>        | [<span data-ttu-id="4f3ce-175">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="4f3ce-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4f3ce-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4f3ce-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4f3ce-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f3ce-177">Entry</span></span> | <span data-ttu-id="4f3ce-178">Valor</span><span class="sxs-lookup"><span data-stu-id="4f3ce-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4f3ce-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="4f3ce-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4f3ce-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f3ce-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4f3ce-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f3ce-181">System-Only</span></span>            | <span data-ttu-id="4f3ce-182">Falso</span><span class="sxs-lookup"><span data-stu-id="4f3ce-182">False</span></span>                                                |
| <span data-ttu-id="4f3ce-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4f3ce-183">Is-Single-Valued</span></span>       | <span data-ttu-id="4f3ce-184">True</span><span class="sxs-lookup"><span data-stu-id="4f3ce-184">True</span></span>                                                 |
| <span data-ttu-id="4f3ce-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="4f3ce-185">Is Indexed</span></span>             | <span data-ttu-id="4f3ce-186">Falso</span><span class="sxs-lookup"><span data-stu-id="4f3ce-186">False</span></span>                                                |
| <span data-ttu-id="4f3ce-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4f3ce-187">In Global Catalog</span></span>      | <span data-ttu-id="4f3ce-188">Falso</span><span class="sxs-lookup"><span data-stu-id="4f3ce-188">False</span></span>                                                |
| <span data-ttu-id="4f3ce-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f3ce-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f3ce-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4f3ce-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4f3ce-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f3ce-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="4f3ce-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f3ce-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="4f3ce-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f3ce-193">Search-Flags</span></span>           | <span data-ttu-id="4f3ce-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f3ce-194">0x00000000</span></span>                                           |
| <span data-ttu-id="4f3ce-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f3ce-195">System-Flags</span></span>           | <span data-ttu-id="4f3ce-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f3ce-196">0x00000010</span></span>                                           |
| <span data-ttu-id="4f3ce-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4f3ce-197">Classes used in</span></span>        | [<span data-ttu-id="4f3ce-198">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="4f3ce-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4f3ce-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f3ce-199">Windows Server 2008</span></span>



| <span data-ttu-id="4f3ce-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f3ce-200">Entry</span></span> | <span data-ttu-id="4f3ce-201">Valor</span><span class="sxs-lookup"><span data-stu-id="4f3ce-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4f3ce-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="4f3ce-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4f3ce-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f3ce-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4f3ce-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f3ce-204">System-Only</span></span>            | <span data-ttu-id="4f3ce-205">Falso</span><span class="sxs-lookup"><span data-stu-id="4f3ce-205">False</span></span>                                                |
| <span data-ttu-id="4f3ce-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4f3ce-206">Is-Single-Valued</span></span>       | <span data-ttu-id="4f3ce-207">True</span><span class="sxs-lookup"><span data-stu-id="4f3ce-207">True</span></span>                                                 |
| <span data-ttu-id="4f3ce-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="4f3ce-208">Is Indexed</span></span>             | <span data-ttu-id="4f3ce-209">Falso</span><span class="sxs-lookup"><span data-stu-id="4f3ce-209">False</span></span>                                                |
| <span data-ttu-id="4f3ce-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4f3ce-210">In Global Catalog</span></span>      | <span data-ttu-id="4f3ce-211">Falso</span><span class="sxs-lookup"><span data-stu-id="4f3ce-211">False</span></span>                                                |
| <span data-ttu-id="4f3ce-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f3ce-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f3ce-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4f3ce-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4f3ce-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f3ce-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="4f3ce-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f3ce-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="4f3ce-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f3ce-216">Search-Flags</span></span>           | <span data-ttu-id="4f3ce-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f3ce-217">0x00000000</span></span>                                           |
| <span data-ttu-id="4f3ce-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f3ce-218">System-Flags</span></span>           | <span data-ttu-id="4f3ce-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f3ce-219">0x00000010</span></span>                                           |
| <span data-ttu-id="4f3ce-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4f3ce-220">Classes used in</span></span>        | [<span data-ttu-id="4f3ce-221">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="4f3ce-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4f3ce-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4f3ce-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4f3ce-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f3ce-223">Entry</span></span> | <span data-ttu-id="4f3ce-224">Valor</span><span class="sxs-lookup"><span data-stu-id="4f3ce-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4f3ce-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="4f3ce-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4f3ce-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f3ce-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4f3ce-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f3ce-227">System-Only</span></span>            | <span data-ttu-id="4f3ce-228">Falso</span><span class="sxs-lookup"><span data-stu-id="4f3ce-228">False</span></span>                                                |
| <span data-ttu-id="4f3ce-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4f3ce-229">Is-Single-Valued</span></span>       | <span data-ttu-id="4f3ce-230">True</span><span class="sxs-lookup"><span data-stu-id="4f3ce-230">True</span></span>                                                 |
| <span data-ttu-id="4f3ce-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="4f3ce-231">Is Indexed</span></span>             | <span data-ttu-id="4f3ce-232">Falso</span><span class="sxs-lookup"><span data-stu-id="4f3ce-232">False</span></span>                                                |
| <span data-ttu-id="4f3ce-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4f3ce-233">In Global Catalog</span></span>      | <span data-ttu-id="4f3ce-234">Falso</span><span class="sxs-lookup"><span data-stu-id="4f3ce-234">False</span></span>                                                |
| <span data-ttu-id="4f3ce-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f3ce-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f3ce-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4f3ce-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4f3ce-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f3ce-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="4f3ce-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f3ce-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="4f3ce-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f3ce-239">Search-Flags</span></span>           | <span data-ttu-id="4f3ce-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f3ce-240">0x00000000</span></span>                                           |
| <span data-ttu-id="4f3ce-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f3ce-241">System-Flags</span></span>           | <span data-ttu-id="4f3ce-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f3ce-242">0x00000010</span></span>                                           |
| <span data-ttu-id="4f3ce-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4f3ce-243">Classes used in</span></span>        | [<span data-ttu-id="4f3ce-244">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="4f3ce-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4f3ce-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4f3ce-245">Windows Server 2012</span></span>



| <span data-ttu-id="4f3ce-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f3ce-246">Entry</span></span> | <span data-ttu-id="4f3ce-247">Valor</span><span class="sxs-lookup"><span data-stu-id="4f3ce-247">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4f3ce-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="4f3ce-248">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4f3ce-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f3ce-249">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4f3ce-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f3ce-250">System-Only</span></span>            | <span data-ttu-id="4f3ce-251">Falso</span><span class="sxs-lookup"><span data-stu-id="4f3ce-251">False</span></span>                                                |
| <span data-ttu-id="4f3ce-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4f3ce-252">Is-Single-Valued</span></span>       | <span data-ttu-id="4f3ce-253">True</span><span class="sxs-lookup"><span data-stu-id="4f3ce-253">True</span></span>                                                 |
| <span data-ttu-id="4f3ce-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="4f3ce-254">Is Indexed</span></span>             | <span data-ttu-id="4f3ce-255">Falso</span><span class="sxs-lookup"><span data-stu-id="4f3ce-255">False</span></span>                                                |
| <span data-ttu-id="4f3ce-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4f3ce-256">In Global Catalog</span></span>      | <span data-ttu-id="4f3ce-257">Falso</span><span class="sxs-lookup"><span data-stu-id="4f3ce-257">False</span></span>                                                |
| <span data-ttu-id="4f3ce-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f3ce-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f3ce-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4f3ce-259">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4f3ce-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f3ce-260">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="4f3ce-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f3ce-261">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="4f3ce-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f3ce-262">Search-Flags</span></span>           | <span data-ttu-id="4f3ce-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f3ce-263">0x00000000</span></span>                                           |
| <span data-ttu-id="4f3ce-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f3ce-264">System-Flags</span></span>           | <span data-ttu-id="4f3ce-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f3ce-265">0x00000010</span></span>                                           |
| <span data-ttu-id="4f3ce-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4f3ce-266">Classes used in</span></span>        | [<span data-ttu-id="4f3ce-267">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="4f3ce-267">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





