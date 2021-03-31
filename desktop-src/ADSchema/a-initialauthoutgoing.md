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
# <a name="initial-auth-outgoing-attribute"></a><span data-ttu-id="10adb-105">Autenticação inicial – atributo de saída</span><span class="sxs-lookup"><span data-stu-id="10adb-105">Initial-Auth-Outgoing attribute</span></span>

<span data-ttu-id="10adb-106">Contém informações sobre uma autenticação de saída inicial enviada pelo servidor de autenticação para esse domínio para o cliente que solicitou a autenticação.</span><span class="sxs-lookup"><span data-stu-id="10adb-106">Contains information about an initial outgoing authentication sent by the authentication server for this domain to the client that requested authentication.</span></span> <span data-ttu-id="10adb-107">O servidor que usa esse atributo recebe a autorização do servidor de autenticação e a envia para o cliente.</span><span class="sxs-lookup"><span data-stu-id="10adb-107">The server that uses this attribute receives the authorization from the authentication server and sends it to the client.</span></span>



| <span data-ttu-id="10adb-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="10adb-108">Entry</span></span> | <span data-ttu-id="10adb-109">Valor</span><span class="sxs-lookup"><span data-stu-id="10adb-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="10adb-110">CN</span><span class="sxs-lookup"><span data-stu-id="10adb-110">CN</span></span>                | <span data-ttu-id="10adb-111">Inicial-autenticação-saída</span><span class="sxs-lookup"><span data-stu-id="10adb-111">Initial-Auth-Outgoing</span></span>                       |
| <span data-ttu-id="10adb-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="10adb-112">Ldap-Display-Name</span></span> | <span data-ttu-id="10adb-113">initialAuthOutgoing</span><span class="sxs-lookup"><span data-stu-id="10adb-113">initialAuthOutgoing</span></span>                         |
| <span data-ttu-id="10adb-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="10adb-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="10adb-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="10adb-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="10adb-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="10adb-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="10adb-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="10adb-117">Attribute-Id</span></span>      | <span data-ttu-id="10adb-118">1.2.840.113556.1.4.540</span><span class="sxs-lookup"><span data-stu-id="10adb-118">1.2.840.113556.1.4.540</span></span>                      |
| <span data-ttu-id="10adb-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="10adb-119">System-Id-Guid</span></span>    | <span data-ttu-id="10adb-120">52458024-ca6a-11D0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="10adb-120">52458024-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="10adb-121">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10adb-121">Syntax</span></span>            | [<span data-ttu-id="10adb-122">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="10adb-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="10adb-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="10adb-123">Implementations</span></span>

-   [<span data-ttu-id="10adb-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="10adb-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="10adb-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="10adb-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="10adb-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="10adb-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="10adb-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="10adb-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="10adb-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="10adb-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="10adb-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="10adb-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="10adb-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="10adb-130">Windows 2000 Server</span></span>



| <span data-ttu-id="10adb-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="10adb-131">Entry</span></span> | <span data-ttu-id="10adb-132">Valor</span><span class="sxs-lookup"><span data-stu-id="10adb-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="10adb-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="10adb-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="10adb-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10adb-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="10adb-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="10adb-135">System-Only</span></span>            | <span data-ttu-id="10adb-136">Falso</span><span class="sxs-lookup"><span data-stu-id="10adb-136">False</span></span>                                                |
| <span data-ttu-id="10adb-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="10adb-137">Is-Single-Valued</span></span>       | <span data-ttu-id="10adb-138">True</span><span class="sxs-lookup"><span data-stu-id="10adb-138">True</span></span>                                                 |
| <span data-ttu-id="10adb-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="10adb-139">Is Indexed</span></span>             | <span data-ttu-id="10adb-140">Falso</span><span class="sxs-lookup"><span data-stu-id="10adb-140">False</span></span>                                                |
| <span data-ttu-id="10adb-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="10adb-141">In Global Catalog</span></span>      | <span data-ttu-id="10adb-142">Falso</span><span class="sxs-lookup"><span data-stu-id="10adb-142">False</span></span>                                                |
| <span data-ttu-id="10adb-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="10adb-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="10adb-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="10adb-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="10adb-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10adb-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="10adb-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10adb-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="10adb-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10adb-147">Search-Flags</span></span>           | <span data-ttu-id="10adb-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10adb-148">0x00000000</span></span>                                           |
| <span data-ttu-id="10adb-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10adb-149">System-Flags</span></span>           | <span data-ttu-id="10adb-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10adb-150">0x00000010</span></span>                                           |
| <span data-ttu-id="10adb-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="10adb-151">Classes used in</span></span>        | [<span data-ttu-id="10adb-152">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="10adb-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="10adb-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="10adb-153">Windows Server 2003</span></span>



| <span data-ttu-id="10adb-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="10adb-154">Entry</span></span> | <span data-ttu-id="10adb-155">Valor</span><span class="sxs-lookup"><span data-stu-id="10adb-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="10adb-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="10adb-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="10adb-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10adb-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="10adb-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="10adb-158">System-Only</span></span>            | <span data-ttu-id="10adb-159">Falso</span><span class="sxs-lookup"><span data-stu-id="10adb-159">False</span></span>                                                |
| <span data-ttu-id="10adb-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="10adb-160">Is-Single-Valued</span></span>       | <span data-ttu-id="10adb-161">True</span><span class="sxs-lookup"><span data-stu-id="10adb-161">True</span></span>                                                 |
| <span data-ttu-id="10adb-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="10adb-162">Is Indexed</span></span>             | <span data-ttu-id="10adb-163">Falso</span><span class="sxs-lookup"><span data-stu-id="10adb-163">False</span></span>                                                |
| <span data-ttu-id="10adb-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="10adb-164">In Global Catalog</span></span>      | <span data-ttu-id="10adb-165">Falso</span><span class="sxs-lookup"><span data-stu-id="10adb-165">False</span></span>                                                |
| <span data-ttu-id="10adb-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="10adb-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="10adb-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="10adb-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="10adb-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10adb-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="10adb-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10adb-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="10adb-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10adb-170">Search-Flags</span></span>           | <span data-ttu-id="10adb-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10adb-171">0x00000000</span></span>                                           |
| <span data-ttu-id="10adb-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10adb-172">System-Flags</span></span>           | <span data-ttu-id="10adb-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10adb-173">0x00000010</span></span>                                           |
| <span data-ttu-id="10adb-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="10adb-174">Classes used in</span></span>        | [<span data-ttu-id="10adb-175">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="10adb-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="10adb-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="10adb-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="10adb-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="10adb-177">Entry</span></span> | <span data-ttu-id="10adb-178">Valor</span><span class="sxs-lookup"><span data-stu-id="10adb-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="10adb-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="10adb-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="10adb-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10adb-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="10adb-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="10adb-181">System-Only</span></span>            | <span data-ttu-id="10adb-182">Falso</span><span class="sxs-lookup"><span data-stu-id="10adb-182">False</span></span>                                                |
| <span data-ttu-id="10adb-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="10adb-183">Is-Single-Valued</span></span>       | <span data-ttu-id="10adb-184">True</span><span class="sxs-lookup"><span data-stu-id="10adb-184">True</span></span>                                                 |
| <span data-ttu-id="10adb-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="10adb-185">Is Indexed</span></span>             | <span data-ttu-id="10adb-186">Falso</span><span class="sxs-lookup"><span data-stu-id="10adb-186">False</span></span>                                                |
| <span data-ttu-id="10adb-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="10adb-187">In Global Catalog</span></span>      | <span data-ttu-id="10adb-188">Falso</span><span class="sxs-lookup"><span data-stu-id="10adb-188">False</span></span>                                                |
| <span data-ttu-id="10adb-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="10adb-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="10adb-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="10adb-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="10adb-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10adb-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="10adb-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10adb-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="10adb-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10adb-193">Search-Flags</span></span>           | <span data-ttu-id="10adb-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10adb-194">0x00000000</span></span>                                           |
| <span data-ttu-id="10adb-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10adb-195">System-Flags</span></span>           | <span data-ttu-id="10adb-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10adb-196">0x00000010</span></span>                                           |
| <span data-ttu-id="10adb-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="10adb-197">Classes used in</span></span>        | [<span data-ttu-id="10adb-198">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="10adb-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="10adb-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10adb-199">Windows Server 2008</span></span>



| <span data-ttu-id="10adb-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="10adb-200">Entry</span></span> | <span data-ttu-id="10adb-201">Valor</span><span class="sxs-lookup"><span data-stu-id="10adb-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="10adb-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="10adb-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="10adb-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10adb-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="10adb-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="10adb-204">System-Only</span></span>            | <span data-ttu-id="10adb-205">Falso</span><span class="sxs-lookup"><span data-stu-id="10adb-205">False</span></span>                                                |
| <span data-ttu-id="10adb-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="10adb-206">Is-Single-Valued</span></span>       | <span data-ttu-id="10adb-207">True</span><span class="sxs-lookup"><span data-stu-id="10adb-207">True</span></span>                                                 |
| <span data-ttu-id="10adb-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="10adb-208">Is Indexed</span></span>             | <span data-ttu-id="10adb-209">Falso</span><span class="sxs-lookup"><span data-stu-id="10adb-209">False</span></span>                                                |
| <span data-ttu-id="10adb-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="10adb-210">In Global Catalog</span></span>      | <span data-ttu-id="10adb-211">Falso</span><span class="sxs-lookup"><span data-stu-id="10adb-211">False</span></span>                                                |
| <span data-ttu-id="10adb-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="10adb-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="10adb-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="10adb-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="10adb-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10adb-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="10adb-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10adb-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="10adb-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10adb-216">Search-Flags</span></span>           | <span data-ttu-id="10adb-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10adb-217">0x00000000</span></span>                                           |
| <span data-ttu-id="10adb-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10adb-218">System-Flags</span></span>           | <span data-ttu-id="10adb-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10adb-219">0x00000010</span></span>                                           |
| <span data-ttu-id="10adb-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="10adb-220">Classes used in</span></span>        | [<span data-ttu-id="10adb-221">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="10adb-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="10adb-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="10adb-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="10adb-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="10adb-223">Entry</span></span> | <span data-ttu-id="10adb-224">Valor</span><span class="sxs-lookup"><span data-stu-id="10adb-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="10adb-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="10adb-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="10adb-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10adb-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="10adb-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="10adb-227">System-Only</span></span>            | <span data-ttu-id="10adb-228">Falso</span><span class="sxs-lookup"><span data-stu-id="10adb-228">False</span></span>                                                |
| <span data-ttu-id="10adb-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="10adb-229">Is-Single-Valued</span></span>       | <span data-ttu-id="10adb-230">True</span><span class="sxs-lookup"><span data-stu-id="10adb-230">True</span></span>                                                 |
| <span data-ttu-id="10adb-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="10adb-231">Is Indexed</span></span>             | <span data-ttu-id="10adb-232">Falso</span><span class="sxs-lookup"><span data-stu-id="10adb-232">False</span></span>                                                |
| <span data-ttu-id="10adb-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="10adb-233">In Global Catalog</span></span>      | <span data-ttu-id="10adb-234">Falso</span><span class="sxs-lookup"><span data-stu-id="10adb-234">False</span></span>                                                |
| <span data-ttu-id="10adb-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="10adb-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="10adb-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="10adb-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="10adb-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10adb-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="10adb-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10adb-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="10adb-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10adb-239">Search-Flags</span></span>           | <span data-ttu-id="10adb-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10adb-240">0x00000000</span></span>                                           |
| <span data-ttu-id="10adb-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10adb-241">System-Flags</span></span>           | <span data-ttu-id="10adb-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10adb-242">0x00000010</span></span>                                           |
| <span data-ttu-id="10adb-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="10adb-243">Classes used in</span></span>        | [<span data-ttu-id="10adb-244">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="10adb-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="10adb-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="10adb-245">Windows Server 2012</span></span>



| <span data-ttu-id="10adb-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="10adb-246">Entry</span></span> | <span data-ttu-id="10adb-247">Valor</span><span class="sxs-lookup"><span data-stu-id="10adb-247">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="10adb-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="10adb-248">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="10adb-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10adb-249">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="10adb-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="10adb-250">System-Only</span></span>            | <span data-ttu-id="10adb-251">Falso</span><span class="sxs-lookup"><span data-stu-id="10adb-251">False</span></span>                                                |
| <span data-ttu-id="10adb-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="10adb-252">Is-Single-Valued</span></span>       | <span data-ttu-id="10adb-253">True</span><span class="sxs-lookup"><span data-stu-id="10adb-253">True</span></span>                                                 |
| <span data-ttu-id="10adb-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="10adb-254">Is Indexed</span></span>             | <span data-ttu-id="10adb-255">Falso</span><span class="sxs-lookup"><span data-stu-id="10adb-255">False</span></span>                                                |
| <span data-ttu-id="10adb-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="10adb-256">In Global Catalog</span></span>      | <span data-ttu-id="10adb-257">Falso</span><span class="sxs-lookup"><span data-stu-id="10adb-257">False</span></span>                                                |
| <span data-ttu-id="10adb-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="10adb-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="10adb-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="10adb-259">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="10adb-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10adb-260">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="10adb-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10adb-261">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="10adb-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10adb-262">Search-Flags</span></span>           | <span data-ttu-id="10adb-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10adb-263">0x00000000</span></span>                                           |
| <span data-ttu-id="10adb-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10adb-264">System-Flags</span></span>           | <span data-ttu-id="10adb-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10adb-265">0x00000010</span></span>                                           |
| <span data-ttu-id="10adb-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="10adb-266">Classes used in</span></span>        | [<span data-ttu-id="10adb-267">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="10adb-267">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





