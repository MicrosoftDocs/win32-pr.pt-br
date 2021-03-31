---
title: Authentication-Options atributo
description: As opções de autenticação usadas no ADSI para ligar a objetos de serviços de diretório.
ms.assetid: a6dc4591-d825-456a-8f77-78cb3c91af9f
ms.tgt_platform: multiple
keywords:
- Esquema de Authentication-Options do atributo AD
- Esquema de AD do atributo authenticationoptions
topic_type:
- apiref
api_name:
- Authentication-Options
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cfa9c422dfe196ab002c02c361759461f43965d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086760"
---
# <a name="authentication-options-attribute"></a><span data-ttu-id="63305-105">Authentication-Options atributo</span><span class="sxs-lookup"><span data-stu-id="63305-105">Authentication-Options attribute</span></span>

<span data-ttu-id="63305-106">As opções de autenticação usadas no ADSI para ligar a objetos de serviços de diretório.</span><span class="sxs-lookup"><span data-stu-id="63305-106">The authentication options used in ADSI to bind to directory services objects.</span></span>



| <span data-ttu-id="63305-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="63305-107">Entry</span></span> | <span data-ttu-id="63305-108">Valor</span><span class="sxs-lookup"><span data-stu-id="63305-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63305-109">CN</span><span class="sxs-lookup"><span data-stu-id="63305-109">CN</span></span>                | <span data-ttu-id="63305-110">Authentication-Options</span><span class="sxs-lookup"><span data-stu-id="63305-110">Authentication-Options</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="63305-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="63305-111">Ldap-Display-Name</span></span> | <span data-ttu-id="63305-112">autenticaçãooptions</span><span class="sxs-lookup"><span data-stu-id="63305-112">authenticationOptions</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="63305-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="63305-113">Size</span></span>              | <span data-ttu-id="63305-114">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="63305-114">4 bytes.</span></span> <span data-ttu-id="63305-115">Valores definidos em IADS. h: ADS \_ \_ autenticação segura 0x1, os ads \_ usam \_ criptografia 0x2, os ads \_ usam \_ SSL 0x2, \_ servidor AD ReadOnly \_ 0X4, anúncios \_ solicitam \_ credenciais 0x8, anúncios \_ sem \_ autenticação 0x10, ADS \_ Fast \_ BIND 0x20, ADS \_ usam \_ assinatura 0x40, os anúncios \_ usam \_ lacre 0x80</span><span class="sxs-lookup"><span data-stu-id="63305-115">Values defined in IADS.h: ADS\_SECURE\_AUTHENTICATION 0x1, ADS\_USE\_ENCRYPTION 0x2, ADS\_USE\_SSL 0x2, ADS\_READONLY\_SERVER 0x4, ADS\_PROMPT\_CREDENTIALS 0x8, ADS\_NO\_AUTHENTICATION 0x10, ADS\_FAST\_BIND 0x20, ADS\_USE\_SIGNING 0x40, ADS\_USE\_SEALING 0x80</span></span> |
| <span data-ttu-id="63305-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="63305-116">Update Privilege</span></span>  | \-                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="63305-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="63305-117">Update Frequency</span></span>  | \-                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="63305-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="63305-118">Attribute-Id</span></span>      | <span data-ttu-id="63305-119">1.2.840.113556.1.4.11</span><span class="sxs-lookup"><span data-stu-id="63305-119">1.2.840.113556.1.4.11</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="63305-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="63305-120">System-Id-Guid</span></span>    | <span data-ttu-id="63305-121">bf967928-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="63305-121">bf967928-0de6-11d0-a285-00aa003049e2</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="63305-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="63305-122">Syntax</span></span>            | [<span data-ttu-id="63305-123">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="63305-123">**Enumeration**</span></span>](s-enumeration.md)                                                                                                                                                                                                                                         |



## <a name="implementations"></a><span data-ttu-id="63305-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="63305-124">Implementations</span></span>

-   [<span data-ttu-id="63305-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="63305-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="63305-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="63305-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="63305-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="63305-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="63305-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="63305-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="63305-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="63305-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="63305-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="63305-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="63305-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="63305-131">Windows 2000 Server</span></span>



| <span data-ttu-id="63305-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="63305-132">Entry</span></span> | <span data-ttu-id="63305-133">Valor</span><span class="sxs-lookup"><span data-stu-id="63305-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="63305-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="63305-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="63305-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63305-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="63305-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="63305-136">System-Only</span></span>            | <span data-ttu-id="63305-137">Falso</span><span class="sxs-lookup"><span data-stu-id="63305-137">False</span></span>                                              |
| <span data-ttu-id="63305-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="63305-138">Is-Single-Valued</span></span>       | <span data-ttu-id="63305-139">True</span><span class="sxs-lookup"><span data-stu-id="63305-139">True</span></span>                                               |
| <span data-ttu-id="63305-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="63305-140">Is Indexed</span></span>             | <span data-ttu-id="63305-141">Falso</span><span class="sxs-lookup"><span data-stu-id="63305-141">False</span></span>                                              |
| <span data-ttu-id="63305-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="63305-142">In Global Catalog</span></span>      | <span data-ttu-id="63305-143">Falso</span><span class="sxs-lookup"><span data-stu-id="63305-143">False</span></span>                                              |
| <span data-ttu-id="63305-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="63305-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="63305-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="63305-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="63305-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63305-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="63305-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63305-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="63305-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63305-148">Search-Flags</span></span>           | <span data-ttu-id="63305-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63305-149">0x00000000</span></span>                                         |
| <span data-ttu-id="63305-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63305-150">System-Flags</span></span>           | <span data-ttu-id="63305-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63305-151">0x00000010</span></span>                                         |
| <span data-ttu-id="63305-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="63305-152">Classes used in</span></span>        | [<span data-ttu-id="63305-153">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="63305-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="63305-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="63305-154">Windows Server 2003</span></span>



| <span data-ttu-id="63305-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="63305-155">Entry</span></span> | <span data-ttu-id="63305-156">Valor</span><span class="sxs-lookup"><span data-stu-id="63305-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="63305-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="63305-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="63305-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63305-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="63305-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="63305-159">System-Only</span></span>            | <span data-ttu-id="63305-160">Falso</span><span class="sxs-lookup"><span data-stu-id="63305-160">False</span></span>                                              |
| <span data-ttu-id="63305-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="63305-161">Is-Single-Valued</span></span>       | <span data-ttu-id="63305-162">True</span><span class="sxs-lookup"><span data-stu-id="63305-162">True</span></span>                                               |
| <span data-ttu-id="63305-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="63305-163">Is Indexed</span></span>             | <span data-ttu-id="63305-164">Falso</span><span class="sxs-lookup"><span data-stu-id="63305-164">False</span></span>                                              |
| <span data-ttu-id="63305-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="63305-165">In Global Catalog</span></span>      | <span data-ttu-id="63305-166">Falso</span><span class="sxs-lookup"><span data-stu-id="63305-166">False</span></span>                                              |
| <span data-ttu-id="63305-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="63305-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="63305-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="63305-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="63305-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63305-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="63305-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63305-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="63305-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63305-171">Search-Flags</span></span>           | <span data-ttu-id="63305-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63305-172">0x00000000</span></span>                                         |
| <span data-ttu-id="63305-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63305-173">System-Flags</span></span>           | <span data-ttu-id="63305-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63305-174">0x00000010</span></span>                                         |
| <span data-ttu-id="63305-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="63305-175">Classes used in</span></span>        | [<span data-ttu-id="63305-176">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="63305-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="63305-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="63305-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="63305-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="63305-178">Entry</span></span> | <span data-ttu-id="63305-179">Valor</span><span class="sxs-lookup"><span data-stu-id="63305-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="63305-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="63305-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="63305-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63305-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="63305-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="63305-182">System-Only</span></span>            | <span data-ttu-id="63305-183">Falso</span><span class="sxs-lookup"><span data-stu-id="63305-183">False</span></span>                                              |
| <span data-ttu-id="63305-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="63305-184">Is-Single-Valued</span></span>       | <span data-ttu-id="63305-185">True</span><span class="sxs-lookup"><span data-stu-id="63305-185">True</span></span>                                               |
| <span data-ttu-id="63305-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="63305-186">Is Indexed</span></span>             | <span data-ttu-id="63305-187">Falso</span><span class="sxs-lookup"><span data-stu-id="63305-187">False</span></span>                                              |
| <span data-ttu-id="63305-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="63305-188">In Global Catalog</span></span>      | <span data-ttu-id="63305-189">Falso</span><span class="sxs-lookup"><span data-stu-id="63305-189">False</span></span>                                              |
| <span data-ttu-id="63305-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="63305-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="63305-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="63305-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="63305-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63305-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="63305-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63305-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="63305-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63305-194">Search-Flags</span></span>           | <span data-ttu-id="63305-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63305-195">0x00000000</span></span>                                         |
| <span data-ttu-id="63305-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63305-196">System-Flags</span></span>           | <span data-ttu-id="63305-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63305-197">0x00000010</span></span>                                         |
| <span data-ttu-id="63305-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="63305-198">Classes used in</span></span>        | [<span data-ttu-id="63305-199">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="63305-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="63305-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63305-200">Windows Server 2008</span></span>



| <span data-ttu-id="63305-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="63305-201">Entry</span></span> | <span data-ttu-id="63305-202">Valor</span><span class="sxs-lookup"><span data-stu-id="63305-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="63305-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="63305-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="63305-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63305-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="63305-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="63305-205">System-Only</span></span>            | <span data-ttu-id="63305-206">Falso</span><span class="sxs-lookup"><span data-stu-id="63305-206">False</span></span>                                              |
| <span data-ttu-id="63305-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="63305-207">Is-Single-Valued</span></span>       | <span data-ttu-id="63305-208">True</span><span class="sxs-lookup"><span data-stu-id="63305-208">True</span></span>                                               |
| <span data-ttu-id="63305-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="63305-209">Is Indexed</span></span>             | <span data-ttu-id="63305-210">Falso</span><span class="sxs-lookup"><span data-stu-id="63305-210">False</span></span>                                              |
| <span data-ttu-id="63305-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="63305-211">In Global Catalog</span></span>      | <span data-ttu-id="63305-212">Falso</span><span class="sxs-lookup"><span data-stu-id="63305-212">False</span></span>                                              |
| <span data-ttu-id="63305-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="63305-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="63305-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="63305-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="63305-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63305-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="63305-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63305-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="63305-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63305-217">Search-Flags</span></span>           | <span data-ttu-id="63305-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63305-218">0x00000000</span></span>                                         |
| <span data-ttu-id="63305-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63305-219">System-Flags</span></span>           | <span data-ttu-id="63305-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63305-220">0x00000010</span></span>                                         |
| <span data-ttu-id="63305-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="63305-221">Classes used in</span></span>        | [<span data-ttu-id="63305-222">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="63305-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="63305-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="63305-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="63305-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="63305-224">Entry</span></span> | <span data-ttu-id="63305-225">Valor</span><span class="sxs-lookup"><span data-stu-id="63305-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="63305-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="63305-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="63305-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63305-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="63305-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="63305-228">System-Only</span></span>            | <span data-ttu-id="63305-229">Falso</span><span class="sxs-lookup"><span data-stu-id="63305-229">False</span></span>                                              |
| <span data-ttu-id="63305-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="63305-230">Is-Single-Valued</span></span>       | <span data-ttu-id="63305-231">True</span><span class="sxs-lookup"><span data-stu-id="63305-231">True</span></span>                                               |
| <span data-ttu-id="63305-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="63305-232">Is Indexed</span></span>             | <span data-ttu-id="63305-233">Falso</span><span class="sxs-lookup"><span data-stu-id="63305-233">False</span></span>                                              |
| <span data-ttu-id="63305-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="63305-234">In Global Catalog</span></span>      | <span data-ttu-id="63305-235">Falso</span><span class="sxs-lookup"><span data-stu-id="63305-235">False</span></span>                                              |
| <span data-ttu-id="63305-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="63305-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="63305-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="63305-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="63305-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63305-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="63305-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63305-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="63305-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63305-240">Search-Flags</span></span>           | <span data-ttu-id="63305-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63305-241">0x00000000</span></span>                                         |
| <span data-ttu-id="63305-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63305-242">System-Flags</span></span>           | <span data-ttu-id="63305-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63305-243">0x00000010</span></span>                                         |
| <span data-ttu-id="63305-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="63305-244">Classes used in</span></span>        | [<span data-ttu-id="63305-245">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="63305-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="63305-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="63305-246">Windows Server 2012</span></span>



| <span data-ttu-id="63305-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="63305-247">Entry</span></span> | <span data-ttu-id="63305-248">Valor</span><span class="sxs-lookup"><span data-stu-id="63305-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="63305-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="63305-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="63305-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63305-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="63305-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="63305-251">System-Only</span></span>            | <span data-ttu-id="63305-252">Falso</span><span class="sxs-lookup"><span data-stu-id="63305-252">False</span></span>                                              |
| <span data-ttu-id="63305-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="63305-253">Is-Single-Valued</span></span>       | <span data-ttu-id="63305-254">True</span><span class="sxs-lookup"><span data-stu-id="63305-254">True</span></span>                                               |
| <span data-ttu-id="63305-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="63305-255">Is Indexed</span></span>             | <span data-ttu-id="63305-256">Falso</span><span class="sxs-lookup"><span data-stu-id="63305-256">False</span></span>                                              |
| <span data-ttu-id="63305-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="63305-257">In Global Catalog</span></span>      | <span data-ttu-id="63305-258">Falso</span><span class="sxs-lookup"><span data-stu-id="63305-258">False</span></span>                                              |
| <span data-ttu-id="63305-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="63305-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="63305-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="63305-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="63305-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63305-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="63305-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63305-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="63305-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63305-263">Search-Flags</span></span>           | <span data-ttu-id="63305-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63305-264">0x00000000</span></span>                                         |
| <span data-ttu-id="63305-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63305-265">System-Flags</span></span>           | <span data-ttu-id="63305-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63305-266">0x00000010</span></span>                                         |
| <span data-ttu-id="63305-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="63305-267">Classes used in</span></span>        | [<span data-ttu-id="63305-268">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="63305-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





