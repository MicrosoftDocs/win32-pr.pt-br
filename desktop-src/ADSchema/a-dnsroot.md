---
title: Dns-Root atributo
description: O nome de domínio DNS superior atribuído a uma partição de domínio/diretório.
ms.assetid: 0b33daad-b5c5-4126-86fa-abd3e0006c5f
ms.tgt_platform: multiple
keywords:
- Esquema de Dns-Root do atributo AD
- Esquema de AD do atributo dnsRoot
topic_type:
- apiref
api_name:
- Dns-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2c2fd2c39e8f0015d7641eccd27279b3478ec4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755736"
---
# <a name="dns-root-attribute"></a><span data-ttu-id="3773f-105">Dns-Root atributo</span><span class="sxs-lookup"><span data-stu-id="3773f-105">Dns-Root attribute</span></span>

<span data-ttu-id="3773f-106">O nome de domínio DNS superior atribuído a uma partição de domínio/diretório.</span><span class="sxs-lookup"><span data-stu-id="3773f-106">The uppermost DNS domain name assigned to a domain/directory partition.</span></span> <span data-ttu-id="3773f-107">Isso é definido em um objeto crossRef e é usado, entre outras coisas, para a geração de referência.</span><span class="sxs-lookup"><span data-stu-id="3773f-107">This is set on a crossRef object and is used, among other things, for referral generation.</span></span> <span data-ttu-id="3773f-108">Ao pesquisar uma árvore de domínio inteira, a pesquisa deve ser iniciada no objeto Dns-Root.</span><span class="sxs-lookup"><span data-stu-id="3773f-108">When searching through an entire domain tree, the search must be initiated at the Dns-Root object.</span></span> <span data-ttu-id="3773f-109">Esse atributo pode ter valores múltiplos e, nesse caso, várias referências são geradas.</span><span class="sxs-lookup"><span data-stu-id="3773f-109">This attribute can be multi-valued, in which case multiple referrals are generated.</span></span>



| <span data-ttu-id="3773f-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="3773f-110">Entry</span></span> | <span data-ttu-id="3773f-111">Valor</span><span class="sxs-lookup"><span data-stu-id="3773f-111">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="3773f-112">CN</span><span class="sxs-lookup"><span data-stu-id="3773f-112">CN</span></span>                | <span data-ttu-id="3773f-113">Dns-Root</span><span class="sxs-lookup"><span data-stu-id="3773f-113">Dns-Root</span></span>                                    |
| <span data-ttu-id="3773f-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3773f-114">Ldap-Display-Name</span></span> | <span data-ttu-id="3773f-115">dnsRoot</span><span class="sxs-lookup"><span data-stu-id="3773f-115">dnsRoot</span></span>                                     |
| <span data-ttu-id="3773f-116">Tamanho</span><span class="sxs-lookup"><span data-stu-id="3773f-116">Size</span></span>              | \-                                          |
| <span data-ttu-id="3773f-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="3773f-117">Update Privilege</span></span>  | <span data-ttu-id="3773f-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="3773f-118">This value is set by the system.</span></span>            |
| <span data-ttu-id="3773f-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="3773f-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="3773f-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3773f-120">Attribute-Id</span></span>      | <span data-ttu-id="3773f-121">1.2.840.113556.1.4.28</span><span class="sxs-lookup"><span data-stu-id="3773f-121">1.2.840.113556.1.4.28</span></span>                       |
| <span data-ttu-id="3773f-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3773f-122">System-Id-Guid</span></span>    | <span data-ttu-id="3773f-123">bf967959-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3773f-123">bf967959-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="3773f-124">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3773f-124">Syntax</span></span>            | [<span data-ttu-id="3773f-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3773f-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="3773f-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="3773f-126">Implementations</span></span>

-   [<span data-ttu-id="3773f-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3773f-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3773f-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3773f-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3773f-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="3773f-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3773f-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3773f-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3773f-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3773f-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3773f-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3773f-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3773f-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3773f-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3773f-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3773f-134">Windows 2000 Server</span></span>



| <span data-ttu-id="3773f-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="3773f-135">Entry</span></span> | <span data-ttu-id="3773f-136">Valor</span><span class="sxs-lookup"><span data-stu-id="3773f-136">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3773f-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="3773f-137">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="3773f-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3773f-138">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3773f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="3773f-139">System-Only</span></span>            | <span data-ttu-id="3773f-140">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-140">False</span></span>                                      |
| <span data-ttu-id="3773f-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3773f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="3773f-142">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-142">False</span></span>                                      |
| <span data-ttu-id="3773f-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="3773f-143">Is Indexed</span></span>             | <span data-ttu-id="3773f-144">True</span><span class="sxs-lookup"><span data-stu-id="3773f-144">True</span></span>                                       |
| <span data-ttu-id="3773f-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3773f-145">In Global Catalog</span></span>      | <span data-ttu-id="3773f-146">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-146">False</span></span>                                      |
| <span data-ttu-id="3773f-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3773f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="3773f-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3773f-148">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3773f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3773f-149">Range-Lower</span></span>            | <span data-ttu-id="3773f-150">1</span><span class="sxs-lookup"><span data-stu-id="3773f-150">1</span></span>                                          |
| <span data-ttu-id="3773f-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3773f-151">Range-Upper</span></span>            | <span data-ttu-id="3773f-152">255</span><span class="sxs-lookup"><span data-stu-id="3773f-152">255</span></span>                                        |
| <span data-ttu-id="3773f-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3773f-153">Search-Flags</span></span>           | <span data-ttu-id="3773f-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3773f-154">0x00000001</span></span>                                 |
| <span data-ttu-id="3773f-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3773f-155">System-Flags</span></span>           | <span data-ttu-id="3773f-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3773f-156">0x00000010</span></span>                                 |
| <span data-ttu-id="3773f-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3773f-157">Classes used in</span></span>        | [<span data-ttu-id="3773f-158">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="3773f-158">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3773f-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3773f-159">Windows Server 2003</span></span>



| <span data-ttu-id="3773f-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="3773f-160">Entry</span></span> | <span data-ttu-id="3773f-161">Valor</span><span class="sxs-lookup"><span data-stu-id="3773f-161">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3773f-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="3773f-162">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="3773f-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3773f-163">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3773f-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="3773f-164">System-Only</span></span>            | <span data-ttu-id="3773f-165">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-165">False</span></span>                                      |
| <span data-ttu-id="3773f-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3773f-166">Is-Single-Valued</span></span>       | <span data-ttu-id="3773f-167">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-167">False</span></span>                                      |
| <span data-ttu-id="3773f-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="3773f-168">Is Indexed</span></span>             | <span data-ttu-id="3773f-169">True</span><span class="sxs-lookup"><span data-stu-id="3773f-169">True</span></span>                                       |
| <span data-ttu-id="3773f-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3773f-170">In Global Catalog</span></span>      | <span data-ttu-id="3773f-171">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-171">False</span></span>                                      |
| <span data-ttu-id="3773f-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3773f-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="3773f-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3773f-173">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3773f-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3773f-174">Range-Lower</span></span>            | <span data-ttu-id="3773f-175">1</span><span class="sxs-lookup"><span data-stu-id="3773f-175">1</span></span>                                          |
| <span data-ttu-id="3773f-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3773f-176">Range-Upper</span></span>            | <span data-ttu-id="3773f-177">255</span><span class="sxs-lookup"><span data-stu-id="3773f-177">255</span></span>                                        |
| <span data-ttu-id="3773f-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3773f-178">Search-Flags</span></span>           | <span data-ttu-id="3773f-179">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3773f-179">0x00000001</span></span>                                 |
| <span data-ttu-id="3773f-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3773f-180">System-Flags</span></span>           | <span data-ttu-id="3773f-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3773f-181">0x00000010</span></span>                                 |
| <span data-ttu-id="3773f-182">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3773f-182">Classes used in</span></span>        | [<span data-ttu-id="3773f-183">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="3773f-183">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="3773f-184">ADAM</span><span class="sxs-lookup"><span data-stu-id="3773f-184">ADAM</span></span>



| <span data-ttu-id="3773f-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="3773f-185">Entry</span></span> | <span data-ttu-id="3773f-186">Valor</span><span class="sxs-lookup"><span data-stu-id="3773f-186">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3773f-187">ID do link</span><span class="sxs-lookup"><span data-stu-id="3773f-187">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="3773f-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3773f-188">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3773f-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="3773f-189">System-Only</span></span>            | <span data-ttu-id="3773f-190">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-190">False</span></span>                                      |
| <span data-ttu-id="3773f-191">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3773f-191">Is-Single-Valued</span></span>       | <span data-ttu-id="3773f-192">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-192">False</span></span>                                      |
| <span data-ttu-id="3773f-193">É indexado</span><span class="sxs-lookup"><span data-stu-id="3773f-193">Is Indexed</span></span>             | <span data-ttu-id="3773f-194">True</span><span class="sxs-lookup"><span data-stu-id="3773f-194">True</span></span>                                       |
| <span data-ttu-id="3773f-195">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3773f-195">In Global Catalog</span></span>      | <span data-ttu-id="3773f-196">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-196">False</span></span>                                      |
| <span data-ttu-id="3773f-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3773f-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="3773f-198">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3773f-198">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3773f-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3773f-199">Range-Lower</span></span>            | <span data-ttu-id="3773f-200">1</span><span class="sxs-lookup"><span data-stu-id="3773f-200">1</span></span>                                          |
| <span data-ttu-id="3773f-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3773f-201">Range-Upper</span></span>            | <span data-ttu-id="3773f-202">255</span><span class="sxs-lookup"><span data-stu-id="3773f-202">255</span></span>                                        |
| <span data-ttu-id="3773f-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3773f-203">Search-Flags</span></span>           | <span data-ttu-id="3773f-204">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3773f-204">0x00000001</span></span>                                 |
| <span data-ttu-id="3773f-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3773f-205">System-Flags</span></span>           | <span data-ttu-id="3773f-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3773f-206">0x00000010</span></span>                                 |
| <span data-ttu-id="3773f-207">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3773f-207">Classes used in</span></span>        | [<span data-ttu-id="3773f-208">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="3773f-208">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3773f-209">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3773f-209">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3773f-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="3773f-210">Entry</span></span> | <span data-ttu-id="3773f-211">Valor</span><span class="sxs-lookup"><span data-stu-id="3773f-211">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3773f-212">ID do link</span><span class="sxs-lookup"><span data-stu-id="3773f-212">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="3773f-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3773f-213">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3773f-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="3773f-214">System-Only</span></span>            | <span data-ttu-id="3773f-215">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-215">False</span></span>                                      |
| <span data-ttu-id="3773f-216">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3773f-216">Is-Single-Valued</span></span>       | <span data-ttu-id="3773f-217">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-217">False</span></span>                                      |
| <span data-ttu-id="3773f-218">É indexado</span><span class="sxs-lookup"><span data-stu-id="3773f-218">Is Indexed</span></span>             | <span data-ttu-id="3773f-219">True</span><span class="sxs-lookup"><span data-stu-id="3773f-219">True</span></span>                                       |
| <span data-ttu-id="3773f-220">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3773f-220">In Global Catalog</span></span>      | <span data-ttu-id="3773f-221">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-221">False</span></span>                                      |
| <span data-ttu-id="3773f-222">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3773f-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="3773f-223">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3773f-223">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3773f-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3773f-224">Range-Lower</span></span>            | <span data-ttu-id="3773f-225">1</span><span class="sxs-lookup"><span data-stu-id="3773f-225">1</span></span>                                          |
| <span data-ttu-id="3773f-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3773f-226">Range-Upper</span></span>            | <span data-ttu-id="3773f-227">255</span><span class="sxs-lookup"><span data-stu-id="3773f-227">255</span></span>                                        |
| <span data-ttu-id="3773f-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3773f-228">Search-Flags</span></span>           | <span data-ttu-id="3773f-229">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3773f-229">0x00000001</span></span>                                 |
| <span data-ttu-id="3773f-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3773f-230">System-Flags</span></span>           | <span data-ttu-id="3773f-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3773f-231">0x00000010</span></span>                                 |
| <span data-ttu-id="3773f-232">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3773f-232">Classes used in</span></span>        | [<span data-ttu-id="3773f-233">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="3773f-233">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3773f-234">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3773f-234">Windows Server 2008</span></span>



| <span data-ttu-id="3773f-235">Entrada</span><span class="sxs-lookup"><span data-stu-id="3773f-235">Entry</span></span> | <span data-ttu-id="3773f-236">Valor</span><span class="sxs-lookup"><span data-stu-id="3773f-236">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3773f-237">ID do link</span><span class="sxs-lookup"><span data-stu-id="3773f-237">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="3773f-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3773f-238">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3773f-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="3773f-239">System-Only</span></span>            | <span data-ttu-id="3773f-240">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-240">False</span></span>                                      |
| <span data-ttu-id="3773f-241">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3773f-241">Is-Single-Valued</span></span>       | <span data-ttu-id="3773f-242">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-242">False</span></span>                                      |
| <span data-ttu-id="3773f-243">É indexado</span><span class="sxs-lookup"><span data-stu-id="3773f-243">Is Indexed</span></span>             | <span data-ttu-id="3773f-244">True</span><span class="sxs-lookup"><span data-stu-id="3773f-244">True</span></span>                                       |
| <span data-ttu-id="3773f-245">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3773f-245">In Global Catalog</span></span>      | <span data-ttu-id="3773f-246">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-246">False</span></span>                                      |
| <span data-ttu-id="3773f-247">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3773f-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="3773f-248">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3773f-248">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3773f-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3773f-249">Range-Lower</span></span>            | <span data-ttu-id="3773f-250">1</span><span class="sxs-lookup"><span data-stu-id="3773f-250">1</span></span>                                          |
| <span data-ttu-id="3773f-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3773f-251">Range-Upper</span></span>            | <span data-ttu-id="3773f-252">255</span><span class="sxs-lookup"><span data-stu-id="3773f-252">255</span></span>                                        |
| <span data-ttu-id="3773f-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3773f-253">Search-Flags</span></span>           | <span data-ttu-id="3773f-254">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3773f-254">0x00000001</span></span>                                 |
| <span data-ttu-id="3773f-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3773f-255">System-Flags</span></span>           | <span data-ttu-id="3773f-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3773f-256">0x00000010</span></span>                                 |
| <span data-ttu-id="3773f-257">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3773f-257">Classes used in</span></span>        | [<span data-ttu-id="3773f-258">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="3773f-258">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3773f-259">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3773f-259">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3773f-260">Entrada</span><span class="sxs-lookup"><span data-stu-id="3773f-260">Entry</span></span> | <span data-ttu-id="3773f-261">Valor</span><span class="sxs-lookup"><span data-stu-id="3773f-261">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3773f-262">ID do link</span><span class="sxs-lookup"><span data-stu-id="3773f-262">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="3773f-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3773f-263">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3773f-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="3773f-264">System-Only</span></span>            | <span data-ttu-id="3773f-265">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-265">False</span></span>                                      |
| <span data-ttu-id="3773f-266">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3773f-266">Is-Single-Valued</span></span>       | <span data-ttu-id="3773f-267">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-267">False</span></span>                                      |
| <span data-ttu-id="3773f-268">É indexado</span><span class="sxs-lookup"><span data-stu-id="3773f-268">Is Indexed</span></span>             | <span data-ttu-id="3773f-269">True</span><span class="sxs-lookup"><span data-stu-id="3773f-269">True</span></span>                                       |
| <span data-ttu-id="3773f-270">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3773f-270">In Global Catalog</span></span>      | <span data-ttu-id="3773f-271">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-271">False</span></span>                                      |
| <span data-ttu-id="3773f-272">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3773f-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="3773f-273">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3773f-273">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3773f-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3773f-274">Range-Lower</span></span>            | <span data-ttu-id="3773f-275">1</span><span class="sxs-lookup"><span data-stu-id="3773f-275">1</span></span>                                          |
| <span data-ttu-id="3773f-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3773f-276">Range-Upper</span></span>            | <span data-ttu-id="3773f-277">255</span><span class="sxs-lookup"><span data-stu-id="3773f-277">255</span></span>                                        |
| <span data-ttu-id="3773f-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3773f-278">Search-Flags</span></span>           | <span data-ttu-id="3773f-279">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3773f-279">0x00000001</span></span>                                 |
| <span data-ttu-id="3773f-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3773f-280">System-Flags</span></span>           | <span data-ttu-id="3773f-281">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3773f-281">0x00000010</span></span>                                 |
| <span data-ttu-id="3773f-282">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3773f-282">Classes used in</span></span>        | [<span data-ttu-id="3773f-283">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="3773f-283">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3773f-284">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3773f-284">Windows Server 2012</span></span>



| <span data-ttu-id="3773f-285">Entrada</span><span class="sxs-lookup"><span data-stu-id="3773f-285">Entry</span></span> | <span data-ttu-id="3773f-286">Valor</span><span class="sxs-lookup"><span data-stu-id="3773f-286">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="3773f-287">ID do link</span><span class="sxs-lookup"><span data-stu-id="3773f-287">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="3773f-288">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3773f-288">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="3773f-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="3773f-289">System-Only</span></span>            | <span data-ttu-id="3773f-290">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-290">False</span></span>                                      |
| <span data-ttu-id="3773f-291">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3773f-291">Is-Single-Valued</span></span>       | <span data-ttu-id="3773f-292">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-292">False</span></span>                                      |
| <span data-ttu-id="3773f-293">É indexado</span><span class="sxs-lookup"><span data-stu-id="3773f-293">Is Indexed</span></span>             | <span data-ttu-id="3773f-294">True</span><span class="sxs-lookup"><span data-stu-id="3773f-294">True</span></span>                                       |
| <span data-ttu-id="3773f-295">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3773f-295">In Global Catalog</span></span>      | <span data-ttu-id="3773f-296">Falso</span><span class="sxs-lookup"><span data-stu-id="3773f-296">False</span></span>                                      |
| <span data-ttu-id="3773f-297">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3773f-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="3773f-298">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3773f-298">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="3773f-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3773f-299">Range-Lower</span></span>            | <span data-ttu-id="3773f-300">1</span><span class="sxs-lookup"><span data-stu-id="3773f-300">1</span></span>                                          |
| <span data-ttu-id="3773f-301">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3773f-301">Range-Upper</span></span>            | <span data-ttu-id="3773f-302">255</span><span class="sxs-lookup"><span data-stu-id="3773f-302">255</span></span>                                        |
| <span data-ttu-id="3773f-303">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3773f-303">Search-Flags</span></span>           | <span data-ttu-id="3773f-304">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3773f-304">0x00000001</span></span>                                 |
| <span data-ttu-id="3773f-305">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3773f-305">System-Flags</span></span>           | <span data-ttu-id="3773f-306">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3773f-306">0x00000010</span></span>                                 |
| <span data-ttu-id="3773f-307">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3773f-307">Classes used in</span></span>        | [<span data-ttu-id="3773f-308">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="3773f-308">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





