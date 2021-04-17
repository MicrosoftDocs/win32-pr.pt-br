---
title: NT-Mixed-atributo de domínio
description: Indica que o domínio está no modo nativo ou misto. Esse atributo é encontrado no objeto domainDNS (cabeçalho) do domínio.
ms.assetid: 49872cbc-844f-4d60-89b6-0150b9116740
ms.tgt_platform: multiple
keywords:
- Esquema do AD de atributos de domínio do NT-Mixed-
- Esquema de AD do atributo nTMixedDomain
topic_type:
- apiref
api_name:
- NT-Mixed-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d73291f392141b80ca8916b86fffa0055226c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105749145"
---
# <a name="nt-mixed-domain-attribute"></a><span data-ttu-id="c3547-106">NT-Mixed-atributo de domínio</span><span class="sxs-lookup"><span data-stu-id="c3547-106">NT-Mixed-Domain attribute</span></span>

<span data-ttu-id="c3547-107">Indica que o domínio está no modo nativo ou misto.</span><span class="sxs-lookup"><span data-stu-id="c3547-107">Indicates that the domain is in native mode or mixed mode.</span></span> <span data-ttu-id="c3547-108">Esse atributo é encontrado no objeto domainDNS (cabeçalho) do domínio.</span><span class="sxs-lookup"><span data-stu-id="c3547-108">This attribute is found in the domainDNS (head) object for the domain.</span></span>



| <span data-ttu-id="c3547-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="c3547-109">Entry</span></span> | <span data-ttu-id="c3547-110">Valor</span><span class="sxs-lookup"><span data-stu-id="c3547-110">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="c3547-111">CN</span><span class="sxs-lookup"><span data-stu-id="c3547-111">CN</span></span>                | <span data-ttu-id="c3547-112">NT-Mixed-Domain</span><span class="sxs-lookup"><span data-stu-id="c3547-112">NT-Mixed-Domain</span></span>                       |
| <span data-ttu-id="c3547-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c3547-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c3547-114">nTMixedDomain</span><span class="sxs-lookup"><span data-stu-id="c3547-114">nTMixedDomain</span></span>                         |
| <span data-ttu-id="c3547-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c3547-115">Size</span></span>              | <span data-ttu-id="c3547-116">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="c3547-116">4 bytes.</span></span> <span data-ttu-id="c3547-117">Modo misto 1, modo nativo 0.</span><span class="sxs-lookup"><span data-stu-id="c3547-117">Mixed mode 1, native mode 0.</span></span> |
| <span data-ttu-id="c3547-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="c3547-118">Update Privilege</span></span>  | \-                                    |
| <span data-ttu-id="c3547-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="c3547-119">Update Frequency</span></span>  | \-                                    |
| <span data-ttu-id="c3547-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c3547-120">Attribute-Id</span></span>      | <span data-ttu-id="c3547-121">1.2.840.113556.1.4.357</span><span class="sxs-lookup"><span data-stu-id="c3547-121">1.2.840.113556.1.4.357</span></span>                |
| <span data-ttu-id="c3547-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c3547-122">System-Id-Guid</span></span>    | <span data-ttu-id="c3547-123">3e97891f-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="c3547-123">3e97891f-8c01-11d0-afda-00c04fd930c9</span></span>  |
| <span data-ttu-id="c3547-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3547-124">Syntax</span></span>            | [<span data-ttu-id="c3547-125">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="c3547-125">**Enumeration**</span></span>](s-enumeration.md)  |



## <a name="implementations"></a><span data-ttu-id="c3547-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="c3547-126">Implementations</span></span>

-   [<span data-ttu-id="c3547-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c3547-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c3547-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c3547-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c3547-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c3547-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c3547-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c3547-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c3547-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c3547-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c3547-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c3547-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c3547-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c3547-133">Windows 2000 Server</span></span>



| <span data-ttu-id="c3547-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="c3547-134">Entry</span></span> | <span data-ttu-id="c3547-135">Valor</span><span class="sxs-lookup"><span data-stu-id="c3547-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c3547-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="c3547-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c3547-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3547-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c3547-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3547-138">System-Only</span></span>            | <span data-ttu-id="c3547-139">Falso</span><span class="sxs-lookup"><span data-stu-id="c3547-139">False</span></span>                                        |
| <span data-ttu-id="c3547-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c3547-140">Is-Single-Valued</span></span>       | <span data-ttu-id="c3547-141">True</span><span class="sxs-lookup"><span data-stu-id="c3547-141">True</span></span>                                         |
| <span data-ttu-id="c3547-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="c3547-142">Is Indexed</span></span>             | <span data-ttu-id="c3547-143">Falso</span><span class="sxs-lookup"><span data-stu-id="c3547-143">False</span></span>                                        |
| <span data-ttu-id="c3547-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c3547-144">In Global Catalog</span></span>      | <span data-ttu-id="c3547-145">Falso</span><span class="sxs-lookup"><span data-stu-id="c3547-145">False</span></span>                                        |
| <span data-ttu-id="c3547-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c3547-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3547-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c3547-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c3547-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3547-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c3547-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3547-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c3547-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3547-150">Search-Flags</span></span>           | <span data-ttu-id="c3547-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3547-151">0x00000000</span></span>                                   |
| <span data-ttu-id="c3547-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3547-152">System-Flags</span></span>           | <span data-ttu-id="c3547-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3547-153">0x00000010</span></span>                                   |
| <span data-ttu-id="c3547-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c3547-154">Classes used in</span></span>        | [<span data-ttu-id="c3547-155">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="c3547-155">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c3547-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c3547-156">Windows Server 2003</span></span>



| <span data-ttu-id="c3547-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="c3547-157">Entry</span></span> | <span data-ttu-id="c3547-158">Valor</span><span class="sxs-lookup"><span data-stu-id="c3547-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3547-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="c3547-159">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="c3547-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3547-160">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="c3547-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3547-161">System-Only</span></span>            | <span data-ttu-id="c3547-162">Falso</span><span class="sxs-lookup"><span data-stu-id="c3547-162">False</span></span>                                                                                   |
| <span data-ttu-id="c3547-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c3547-163">Is-Single-Valued</span></span>       | <span data-ttu-id="c3547-164">True</span><span class="sxs-lookup"><span data-stu-id="c3547-164">True</span></span>                                                                                    |
| <span data-ttu-id="c3547-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="c3547-165">Is Indexed</span></span>             | <span data-ttu-id="c3547-166">Falso</span><span class="sxs-lookup"><span data-stu-id="c3547-166">False</span></span>                                                                                   |
| <span data-ttu-id="c3547-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c3547-167">In Global Catalog</span></span>      | <span data-ttu-id="c3547-168">Falso</span><span class="sxs-lookup"><span data-stu-id="c3547-168">False</span></span>                                                                                   |
| <span data-ttu-id="c3547-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c3547-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3547-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c3547-170">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="c3547-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3547-171">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="c3547-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3547-172">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="c3547-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3547-173">Search-Flags</span></span>           | <span data-ttu-id="c3547-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3547-174">0x00000000</span></span>                                                                              |
| <span data-ttu-id="c3547-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3547-175">System-Flags</span></span>           | <span data-ttu-id="c3547-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3547-176">0x00000010</span></span>                                                                              |
| <span data-ttu-id="c3547-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c3547-177">Classes used in</span></span>        | [<span data-ttu-id="c3547-178">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="c3547-178">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="c3547-179">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="c3547-179">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c3547-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c3547-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c3547-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="c3547-181">Entry</span></span> | <span data-ttu-id="c3547-182">Valor</span><span class="sxs-lookup"><span data-stu-id="c3547-182">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3547-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="c3547-183">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="c3547-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3547-184">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="c3547-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3547-185">System-Only</span></span>            | <span data-ttu-id="c3547-186">Falso</span><span class="sxs-lookup"><span data-stu-id="c3547-186">False</span></span>                                                                                   |
| <span data-ttu-id="c3547-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c3547-187">Is-Single-Valued</span></span>       | <span data-ttu-id="c3547-188">True</span><span class="sxs-lookup"><span data-stu-id="c3547-188">True</span></span>                                                                                    |
| <span data-ttu-id="c3547-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="c3547-189">Is Indexed</span></span>             | <span data-ttu-id="c3547-190">Falso</span><span class="sxs-lookup"><span data-stu-id="c3547-190">False</span></span>                                                                                   |
| <span data-ttu-id="c3547-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c3547-191">In Global Catalog</span></span>      | <span data-ttu-id="c3547-192">Falso</span><span class="sxs-lookup"><span data-stu-id="c3547-192">False</span></span>                                                                                   |
| <span data-ttu-id="c3547-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c3547-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3547-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c3547-194">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="c3547-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3547-195">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="c3547-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3547-196">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="c3547-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3547-197">Search-Flags</span></span>           | <span data-ttu-id="c3547-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3547-198">0x00000000</span></span>                                                                              |
| <span data-ttu-id="c3547-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3547-199">System-Flags</span></span>           | <span data-ttu-id="c3547-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3547-200">0x00000010</span></span>                                                                              |
| <span data-ttu-id="c3547-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c3547-201">Classes used in</span></span>        | [<span data-ttu-id="c3547-202">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="c3547-202">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="c3547-203">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="c3547-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c3547-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3547-204">Windows Server 2008</span></span>



| <span data-ttu-id="c3547-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="c3547-205">Entry</span></span> | <span data-ttu-id="c3547-206">Valor</span><span class="sxs-lookup"><span data-stu-id="c3547-206">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3547-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="c3547-207">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="c3547-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3547-208">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="c3547-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3547-209">System-Only</span></span>            | <span data-ttu-id="c3547-210">Falso</span><span class="sxs-lookup"><span data-stu-id="c3547-210">False</span></span>                                                                                   |
| <span data-ttu-id="c3547-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c3547-211">Is-Single-Valued</span></span>       | <span data-ttu-id="c3547-212">True</span><span class="sxs-lookup"><span data-stu-id="c3547-212">True</span></span>                                                                                    |
| <span data-ttu-id="c3547-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="c3547-213">Is Indexed</span></span>             | <span data-ttu-id="c3547-214">Falso</span><span class="sxs-lookup"><span data-stu-id="c3547-214">False</span></span>                                                                                   |
| <span data-ttu-id="c3547-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c3547-215">In Global Catalog</span></span>      | <span data-ttu-id="c3547-216">Falso</span><span class="sxs-lookup"><span data-stu-id="c3547-216">False</span></span>                                                                                   |
| <span data-ttu-id="c3547-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c3547-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3547-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c3547-218">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="c3547-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3547-219">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="c3547-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3547-220">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="c3547-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3547-221">Search-Flags</span></span>           | <span data-ttu-id="c3547-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3547-222">0x00000000</span></span>                                                                              |
| <span data-ttu-id="c3547-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3547-223">System-Flags</span></span>           | <span data-ttu-id="c3547-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3547-224">0x00000010</span></span>                                                                              |
| <span data-ttu-id="c3547-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c3547-225">Classes used in</span></span>        | [<span data-ttu-id="c3547-226">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="c3547-226">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="c3547-227">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="c3547-227">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c3547-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c3547-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c3547-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="c3547-229">Entry</span></span> | <span data-ttu-id="c3547-230">Valor</span><span class="sxs-lookup"><span data-stu-id="c3547-230">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3547-231">ID do link</span><span class="sxs-lookup"><span data-stu-id="c3547-231">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="c3547-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3547-232">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="c3547-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3547-233">System-Only</span></span>            | <span data-ttu-id="c3547-234">Falso</span><span class="sxs-lookup"><span data-stu-id="c3547-234">False</span></span>                                                                                   |
| <span data-ttu-id="c3547-235">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c3547-235">Is-Single-Valued</span></span>       | <span data-ttu-id="c3547-236">True</span><span class="sxs-lookup"><span data-stu-id="c3547-236">True</span></span>                                                                                    |
| <span data-ttu-id="c3547-237">É indexado</span><span class="sxs-lookup"><span data-stu-id="c3547-237">Is Indexed</span></span>             | <span data-ttu-id="c3547-238">Falso</span><span class="sxs-lookup"><span data-stu-id="c3547-238">False</span></span>                                                                                   |
| <span data-ttu-id="c3547-239">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c3547-239">In Global Catalog</span></span>      | <span data-ttu-id="c3547-240">Falso</span><span class="sxs-lookup"><span data-stu-id="c3547-240">False</span></span>                                                                                   |
| <span data-ttu-id="c3547-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c3547-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3547-242">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c3547-242">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="c3547-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3547-243">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="c3547-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3547-244">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="c3547-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3547-245">Search-Flags</span></span>           | <span data-ttu-id="c3547-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3547-246">0x00000000</span></span>                                                                              |
| <span data-ttu-id="c3547-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3547-247">System-Flags</span></span>           | <span data-ttu-id="c3547-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3547-248">0x00000010</span></span>                                                                              |
| <span data-ttu-id="c3547-249">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c3547-249">Classes used in</span></span>        | [<span data-ttu-id="c3547-250">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="c3547-250">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="c3547-251">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="c3547-251">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c3547-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3547-252">Windows Server 2012</span></span>



| <span data-ttu-id="c3547-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="c3547-253">Entry</span></span> | <span data-ttu-id="c3547-254">Valor</span><span class="sxs-lookup"><span data-stu-id="c3547-254">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3547-255">ID do link</span><span class="sxs-lookup"><span data-stu-id="c3547-255">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="c3547-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3547-256">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="c3547-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3547-257">System-Only</span></span>            | <span data-ttu-id="c3547-258">Falso</span><span class="sxs-lookup"><span data-stu-id="c3547-258">False</span></span>                                                                                   |
| <span data-ttu-id="c3547-259">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c3547-259">Is-Single-Valued</span></span>       | <span data-ttu-id="c3547-260">True</span><span class="sxs-lookup"><span data-stu-id="c3547-260">True</span></span>                                                                                    |
| <span data-ttu-id="c3547-261">É indexado</span><span class="sxs-lookup"><span data-stu-id="c3547-261">Is Indexed</span></span>             | <span data-ttu-id="c3547-262">Falso</span><span class="sxs-lookup"><span data-stu-id="c3547-262">False</span></span>                                                                                   |
| <span data-ttu-id="c3547-263">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c3547-263">In Global Catalog</span></span>      | <span data-ttu-id="c3547-264">Falso</span><span class="sxs-lookup"><span data-stu-id="c3547-264">False</span></span>                                                                                   |
| <span data-ttu-id="c3547-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c3547-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3547-266">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c3547-266">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="c3547-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3547-267">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="c3547-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3547-268">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="c3547-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3547-269">Search-Flags</span></span>           | <span data-ttu-id="c3547-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3547-270">0x00000000</span></span>                                                                              |
| <span data-ttu-id="c3547-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3547-271">System-Flags</span></span>           | <span data-ttu-id="c3547-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3547-272">0x00000010</span></span>                                                                              |
| <span data-ttu-id="c3547-273">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c3547-273">Classes used in</span></span>        | [<span data-ttu-id="c3547-274">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="c3547-274">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="c3547-275">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="c3547-275">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





