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
# <a name="initial-auth-outgoing-attribute"></a><span data-ttu-id="c768c-105">Autenticação inicial – atributo de saída</span><span class="sxs-lookup"><span data-stu-id="c768c-105">Initial-Auth-Outgoing attribute</span></span>

<span data-ttu-id="c768c-106">Contém informações sobre uma autenticação de saída inicial enviada pelo servidor de autenticação para esse domínio para o cliente que solicitou a autenticação.</span><span class="sxs-lookup"><span data-stu-id="c768c-106">Contains information about an initial outgoing authentication sent by the authentication server for this domain to the client that requested authentication.</span></span> <span data-ttu-id="c768c-107">O servidor que usa esse atributo recebe a autorização do servidor de autenticação e a envia para o cliente.</span><span class="sxs-lookup"><span data-stu-id="c768c-107">The server that uses this attribute receives the authorization from the authentication server and sends it to the client.</span></span>



| <span data-ttu-id="c768c-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="c768c-108">Entry</span></span> | <span data-ttu-id="c768c-109">Valor</span><span class="sxs-lookup"><span data-stu-id="c768c-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c768c-110">CN</span><span class="sxs-lookup"><span data-stu-id="c768c-110">CN</span></span>                | <span data-ttu-id="c768c-111">Inicial-autenticação-saída</span><span class="sxs-lookup"><span data-stu-id="c768c-111">Initial-Auth-Outgoing</span></span>                       |
| <span data-ttu-id="c768c-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c768c-112">Ldap-Display-Name</span></span> | <span data-ttu-id="c768c-113">initialAuthOutgoing</span><span class="sxs-lookup"><span data-stu-id="c768c-113">initialAuthOutgoing</span></span>                         |
| <span data-ttu-id="c768c-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c768c-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="c768c-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="c768c-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="c768c-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="c768c-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="c768c-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c768c-117">Attribute-Id</span></span>      | <span data-ttu-id="c768c-118">1.2.840.113556.1.4.540</span><span class="sxs-lookup"><span data-stu-id="c768c-118">1.2.840.113556.1.4.540</span></span>                      |
| <span data-ttu-id="c768c-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c768c-119">System-Id-Guid</span></span>    | <span data-ttu-id="c768c-120">52458024-ca6a-11D0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c768c-120">52458024-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="c768c-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="c768c-121">Syntax</span></span>            | [<span data-ttu-id="c768c-122">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c768c-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c768c-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="c768c-123">Implementations</span></span>

-   [<span data-ttu-id="c768c-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c768c-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c768c-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c768c-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c768c-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c768c-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c768c-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c768c-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c768c-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c768c-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c768c-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c768c-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c768c-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c768c-130">Windows 2000 Server</span></span>



| <span data-ttu-id="c768c-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="c768c-131">Entry</span></span> | <span data-ttu-id="c768c-132">Valor</span><span class="sxs-lookup"><span data-stu-id="c768c-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c768c-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="c768c-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c768c-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c768c-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c768c-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c768c-135">System-Only</span></span>            | <span data-ttu-id="c768c-136">Falso</span><span class="sxs-lookup"><span data-stu-id="c768c-136">False</span></span>                                                |
| <span data-ttu-id="c768c-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c768c-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c768c-138">True</span><span class="sxs-lookup"><span data-stu-id="c768c-138">True</span></span>                                                 |
| <span data-ttu-id="c768c-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="c768c-139">Is Indexed</span></span>             | <span data-ttu-id="c768c-140">Falso</span><span class="sxs-lookup"><span data-stu-id="c768c-140">False</span></span>                                                |
| <span data-ttu-id="c768c-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c768c-141">In Global Catalog</span></span>      | <span data-ttu-id="c768c-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c768c-142">False</span></span>                                                |
| <span data-ttu-id="c768c-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c768c-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c768c-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c768c-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c768c-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c768c-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="c768c-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c768c-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="c768c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c768c-147">Search-Flags</span></span>           | <span data-ttu-id="c768c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c768c-148">0x00000000</span></span>                                           |
| <span data-ttu-id="c768c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c768c-149">System-Flags</span></span>           | <span data-ttu-id="c768c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c768c-150">0x00000010</span></span>                                           |
| <span data-ttu-id="c768c-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c768c-151">Classes used in</span></span>        | [<span data-ttu-id="c768c-152">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="c768c-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c768c-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c768c-153">Windows Server 2003</span></span>



| <span data-ttu-id="c768c-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="c768c-154">Entry</span></span> | <span data-ttu-id="c768c-155">Valor</span><span class="sxs-lookup"><span data-stu-id="c768c-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c768c-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="c768c-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c768c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c768c-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c768c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c768c-158">System-Only</span></span>            | <span data-ttu-id="c768c-159">Falso</span><span class="sxs-lookup"><span data-stu-id="c768c-159">False</span></span>                                                |
| <span data-ttu-id="c768c-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c768c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c768c-161">True</span><span class="sxs-lookup"><span data-stu-id="c768c-161">True</span></span>                                                 |
| <span data-ttu-id="c768c-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="c768c-162">Is Indexed</span></span>             | <span data-ttu-id="c768c-163">Falso</span><span class="sxs-lookup"><span data-stu-id="c768c-163">False</span></span>                                                |
| <span data-ttu-id="c768c-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c768c-164">In Global Catalog</span></span>      | <span data-ttu-id="c768c-165">Falso</span><span class="sxs-lookup"><span data-stu-id="c768c-165">False</span></span>                                                |
| <span data-ttu-id="c768c-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c768c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c768c-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c768c-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c768c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c768c-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="c768c-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c768c-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="c768c-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c768c-170">Search-Flags</span></span>           | <span data-ttu-id="c768c-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c768c-171">0x00000000</span></span>                                           |
| <span data-ttu-id="c768c-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c768c-172">System-Flags</span></span>           | <span data-ttu-id="c768c-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c768c-173">0x00000010</span></span>                                           |
| <span data-ttu-id="c768c-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c768c-174">Classes used in</span></span>        | [<span data-ttu-id="c768c-175">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="c768c-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c768c-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c768c-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c768c-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="c768c-177">Entry</span></span> | <span data-ttu-id="c768c-178">Valor</span><span class="sxs-lookup"><span data-stu-id="c768c-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c768c-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="c768c-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c768c-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c768c-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c768c-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="c768c-181">System-Only</span></span>            | <span data-ttu-id="c768c-182">Falso</span><span class="sxs-lookup"><span data-stu-id="c768c-182">False</span></span>                                                |
| <span data-ttu-id="c768c-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c768c-183">Is-Single-Valued</span></span>       | <span data-ttu-id="c768c-184">True</span><span class="sxs-lookup"><span data-stu-id="c768c-184">True</span></span>                                                 |
| <span data-ttu-id="c768c-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="c768c-185">Is Indexed</span></span>             | <span data-ttu-id="c768c-186">Falso</span><span class="sxs-lookup"><span data-stu-id="c768c-186">False</span></span>                                                |
| <span data-ttu-id="c768c-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c768c-187">In Global Catalog</span></span>      | <span data-ttu-id="c768c-188">Falso</span><span class="sxs-lookup"><span data-stu-id="c768c-188">False</span></span>                                                |
| <span data-ttu-id="c768c-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c768c-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="c768c-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c768c-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c768c-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c768c-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="c768c-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c768c-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="c768c-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c768c-193">Search-Flags</span></span>           | <span data-ttu-id="c768c-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c768c-194">0x00000000</span></span>                                           |
| <span data-ttu-id="c768c-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c768c-195">System-Flags</span></span>           | <span data-ttu-id="c768c-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c768c-196">0x00000010</span></span>                                           |
| <span data-ttu-id="c768c-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c768c-197">Classes used in</span></span>        | [<span data-ttu-id="c768c-198">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="c768c-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c768c-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c768c-199">Windows Server 2008</span></span>



| <span data-ttu-id="c768c-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="c768c-200">Entry</span></span> | <span data-ttu-id="c768c-201">Valor</span><span class="sxs-lookup"><span data-stu-id="c768c-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c768c-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="c768c-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c768c-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c768c-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c768c-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="c768c-204">System-Only</span></span>            | <span data-ttu-id="c768c-205">Falso</span><span class="sxs-lookup"><span data-stu-id="c768c-205">False</span></span>                                                |
| <span data-ttu-id="c768c-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c768c-206">Is-Single-Valued</span></span>       | <span data-ttu-id="c768c-207">True</span><span class="sxs-lookup"><span data-stu-id="c768c-207">True</span></span>                                                 |
| <span data-ttu-id="c768c-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="c768c-208">Is Indexed</span></span>             | <span data-ttu-id="c768c-209">Falso</span><span class="sxs-lookup"><span data-stu-id="c768c-209">False</span></span>                                                |
| <span data-ttu-id="c768c-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c768c-210">In Global Catalog</span></span>      | <span data-ttu-id="c768c-211">Falso</span><span class="sxs-lookup"><span data-stu-id="c768c-211">False</span></span>                                                |
| <span data-ttu-id="c768c-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c768c-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="c768c-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c768c-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c768c-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c768c-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="c768c-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c768c-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="c768c-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c768c-216">Search-Flags</span></span>           | <span data-ttu-id="c768c-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c768c-217">0x00000000</span></span>                                           |
| <span data-ttu-id="c768c-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c768c-218">System-Flags</span></span>           | <span data-ttu-id="c768c-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c768c-219">0x00000010</span></span>                                           |
| <span data-ttu-id="c768c-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c768c-220">Classes used in</span></span>        | [<span data-ttu-id="c768c-221">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="c768c-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c768c-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c768c-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c768c-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="c768c-223">Entry</span></span> | <span data-ttu-id="c768c-224">Valor</span><span class="sxs-lookup"><span data-stu-id="c768c-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c768c-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="c768c-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c768c-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c768c-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c768c-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="c768c-227">System-Only</span></span>            | <span data-ttu-id="c768c-228">Falso</span><span class="sxs-lookup"><span data-stu-id="c768c-228">False</span></span>                                                |
| <span data-ttu-id="c768c-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c768c-229">Is-Single-Valued</span></span>       | <span data-ttu-id="c768c-230">True</span><span class="sxs-lookup"><span data-stu-id="c768c-230">True</span></span>                                                 |
| <span data-ttu-id="c768c-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="c768c-231">Is Indexed</span></span>             | <span data-ttu-id="c768c-232">Falso</span><span class="sxs-lookup"><span data-stu-id="c768c-232">False</span></span>                                                |
| <span data-ttu-id="c768c-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c768c-233">In Global Catalog</span></span>      | <span data-ttu-id="c768c-234">Falso</span><span class="sxs-lookup"><span data-stu-id="c768c-234">False</span></span>                                                |
| <span data-ttu-id="c768c-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c768c-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="c768c-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c768c-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c768c-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c768c-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="c768c-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c768c-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="c768c-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c768c-239">Search-Flags</span></span>           | <span data-ttu-id="c768c-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c768c-240">0x00000000</span></span>                                           |
| <span data-ttu-id="c768c-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c768c-241">System-Flags</span></span>           | <span data-ttu-id="c768c-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c768c-242">0x00000010</span></span>                                           |
| <span data-ttu-id="c768c-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c768c-243">Classes used in</span></span>        | [<span data-ttu-id="c768c-244">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="c768c-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c768c-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c768c-245">Windows Server 2012</span></span>



| <span data-ttu-id="c768c-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="c768c-246">Entry</span></span> | <span data-ttu-id="c768c-247">Valor</span><span class="sxs-lookup"><span data-stu-id="c768c-247">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c768c-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="c768c-248">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c768c-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c768c-249">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c768c-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="c768c-250">System-Only</span></span>            | <span data-ttu-id="c768c-251">Falso</span><span class="sxs-lookup"><span data-stu-id="c768c-251">False</span></span>                                                |
| <span data-ttu-id="c768c-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c768c-252">Is-Single-Valued</span></span>       | <span data-ttu-id="c768c-253">True</span><span class="sxs-lookup"><span data-stu-id="c768c-253">True</span></span>                                                 |
| <span data-ttu-id="c768c-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="c768c-254">Is Indexed</span></span>             | <span data-ttu-id="c768c-255">Falso</span><span class="sxs-lookup"><span data-stu-id="c768c-255">False</span></span>                                                |
| <span data-ttu-id="c768c-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c768c-256">In Global Catalog</span></span>      | <span data-ttu-id="c768c-257">Falso</span><span class="sxs-lookup"><span data-stu-id="c768c-257">False</span></span>                                                |
| <span data-ttu-id="c768c-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c768c-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="c768c-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c768c-259">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c768c-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c768c-260">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="c768c-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c768c-261">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="c768c-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c768c-262">Search-Flags</span></span>           | <span data-ttu-id="c768c-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c768c-263">0x00000000</span></span>                                           |
| <span data-ttu-id="c768c-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c768c-264">System-Flags</span></span>           | <span data-ttu-id="c768c-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c768c-265">0x00000010</span></span>                                           |
| <span data-ttu-id="c768c-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c768c-266">Classes used in</span></span>        | [<span data-ttu-id="c768c-267">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="c768c-267">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





