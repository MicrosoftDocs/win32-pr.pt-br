---
title: Atributo Inter-Site-Topology-Generator
description: Esse atributo será usado para dar suporte ao failover para o computador designado como aquele que é executado Knowledge Consistency Checker geração de topologia entre sites em um determinado site.
ms.assetid: 077f4331-ead9-4f17-942e-d55cf253d03b
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo Inter-Site-Topology-Generator
- Esquema de AD do atributo interSiteTopologyGenerator
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Generator
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df7b354d05e882373715e4c49498c9daff41652
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086671"
---
# <a name="inter-site-topology-generator-attribute"></a><span data-ttu-id="db345-105">Atributo Inter-Site-Topology-Generator</span><span class="sxs-lookup"><span data-stu-id="db345-105">Inter-Site-Topology-Generator attribute</span></span>

<span data-ttu-id="db345-106">Esse atributo será usado para dar suporte ao failover para o computador designado como aquele que é executado Knowledge Consistency Checker geração de topologia entre sites em um determinado site.</span><span class="sxs-lookup"><span data-stu-id="db345-106">This attribute will be used to support failover for the computer designated as the one that runs Knowledge Consistency Checker inter-site topology generation in a given site.</span></span>



| <span data-ttu-id="db345-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="db345-107">Entry</span></span> | <span data-ttu-id="db345-108">Valor</span><span class="sxs-lookup"><span data-stu-id="db345-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="db345-109">CN</span><span class="sxs-lookup"><span data-stu-id="db345-109">CN</span></span>                | <span data-ttu-id="db345-110">Gerador de topologia entre sites</span><span class="sxs-lookup"><span data-stu-id="db345-110">Inter-Site-Topology-Generator</span></span>           |
| <span data-ttu-id="db345-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="db345-111">Ldap-Display-Name</span></span> | <span data-ttu-id="db345-112">interSiteTopologyGenerator</span><span class="sxs-lookup"><span data-stu-id="db345-112">interSiteTopologyGenerator</span></span>              |
| <span data-ttu-id="db345-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="db345-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="db345-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="db345-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="db345-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="db345-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="db345-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="db345-116">Attribute-Id</span></span>      | <span data-ttu-id="db345-117">1.2.840.113556.1.4.1246</span><span class="sxs-lookup"><span data-stu-id="db345-117">1.2.840.113556.1.4.1246</span></span>                 |
| <span data-ttu-id="db345-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="db345-118">System-Id-Guid</span></span>    | <span data-ttu-id="db345-119">b7c69e5e-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="db345-119">b7c69e5e-2cc7-11d2-854e-00a0c983f608</span></span>    |
| <span data-ttu-id="db345-120">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db345-120">Syntax</span></span>            | [<span data-ttu-id="db345-121">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="db345-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="db345-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="db345-122">Implementations</span></span>

-   [<span data-ttu-id="db345-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="db345-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="db345-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="db345-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="db345-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="db345-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="db345-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="db345-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="db345-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="db345-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="db345-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="db345-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="db345-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="db345-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="db345-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="db345-130">Windows 2000 Server</span></span>



| <span data-ttu-id="db345-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="db345-131">Entry</span></span> | <span data-ttu-id="db345-132">Valor</span><span class="sxs-lookup"><span data-stu-id="db345-132">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="db345-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="db345-133">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="db345-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db345-134">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="db345-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="db345-135">System-Only</span></span>            | <span data-ttu-id="db345-136">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-136">False</span></span>                                                       |
| <span data-ttu-id="db345-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="db345-137">Is-Single-Valued</span></span>       | <span data-ttu-id="db345-138">True</span><span class="sxs-lookup"><span data-stu-id="db345-138">True</span></span>                                                        |
| <span data-ttu-id="db345-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="db345-139">Is Indexed</span></span>             | <span data-ttu-id="db345-140">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-140">False</span></span>                                                       |
| <span data-ttu-id="db345-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="db345-141">In Global Catalog</span></span>      | <span data-ttu-id="db345-142">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-142">False</span></span>                                                       |
| <span data-ttu-id="db345-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db345-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="db345-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="db345-144">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="db345-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db345-145">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="db345-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db345-146">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="db345-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db345-147">Search-Flags</span></span>           | <span data-ttu-id="db345-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db345-148">0x00000000</span></span>                                                  |
| <span data-ttu-id="db345-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db345-149">System-Flags</span></span>           | <span data-ttu-id="db345-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db345-150">0x00000010</span></span>                                                  |
| <span data-ttu-id="db345-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="db345-151">Classes used in</span></span>        | [<span data-ttu-id="db345-152">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="db345-152">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="db345-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="db345-153">Windows Server 2003</span></span>



| <span data-ttu-id="db345-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="db345-154">Entry</span></span> | <span data-ttu-id="db345-155">Valor</span><span class="sxs-lookup"><span data-stu-id="db345-155">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="db345-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="db345-156">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="db345-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db345-157">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="db345-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="db345-158">System-Only</span></span>            | <span data-ttu-id="db345-159">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-159">False</span></span>                                                       |
| <span data-ttu-id="db345-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="db345-160">Is-Single-Valued</span></span>       | <span data-ttu-id="db345-161">True</span><span class="sxs-lookup"><span data-stu-id="db345-161">True</span></span>                                                        |
| <span data-ttu-id="db345-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="db345-162">Is Indexed</span></span>             | <span data-ttu-id="db345-163">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-163">False</span></span>                                                       |
| <span data-ttu-id="db345-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="db345-164">In Global Catalog</span></span>      | <span data-ttu-id="db345-165">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-165">False</span></span>                                                       |
| <span data-ttu-id="db345-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db345-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="db345-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="db345-167">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="db345-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db345-168">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="db345-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db345-169">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="db345-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db345-170">Search-Flags</span></span>           | <span data-ttu-id="db345-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db345-171">0x00000000</span></span>                                                  |
| <span data-ttu-id="db345-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db345-172">System-Flags</span></span>           | <span data-ttu-id="db345-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db345-173">0x00000010</span></span>                                                  |
| <span data-ttu-id="db345-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="db345-174">Classes used in</span></span>        | [<span data-ttu-id="db345-175">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="db345-175">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="db345-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="db345-176">ADAM</span></span>



| <span data-ttu-id="db345-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="db345-177">Entry</span></span> | <span data-ttu-id="db345-178">Valor</span><span class="sxs-lookup"><span data-stu-id="db345-178">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="db345-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="db345-179">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="db345-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db345-180">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="db345-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="db345-181">System-Only</span></span>            | <span data-ttu-id="db345-182">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-182">False</span></span>                                                       |
| <span data-ttu-id="db345-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="db345-183">Is-Single-Valued</span></span>       | <span data-ttu-id="db345-184">True</span><span class="sxs-lookup"><span data-stu-id="db345-184">True</span></span>                                                        |
| <span data-ttu-id="db345-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="db345-185">Is Indexed</span></span>             | <span data-ttu-id="db345-186">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-186">False</span></span>                                                       |
| <span data-ttu-id="db345-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="db345-187">In Global Catalog</span></span>      | <span data-ttu-id="db345-188">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-188">False</span></span>                                                       |
| <span data-ttu-id="db345-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db345-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="db345-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="db345-190">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="db345-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db345-191">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="db345-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db345-192">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="db345-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db345-193">Search-Flags</span></span>           | <span data-ttu-id="db345-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db345-194">0x00000000</span></span>                                                  |
| <span data-ttu-id="db345-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db345-195">System-Flags</span></span>           | <span data-ttu-id="db345-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db345-196">0x00000010</span></span>                                                  |
| <span data-ttu-id="db345-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="db345-197">Classes used in</span></span>        | [<span data-ttu-id="db345-198">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="db345-198">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="db345-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="db345-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="db345-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="db345-200">Entry</span></span> | <span data-ttu-id="db345-201">Valor</span><span class="sxs-lookup"><span data-stu-id="db345-201">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="db345-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="db345-202">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="db345-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db345-203">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="db345-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="db345-204">System-Only</span></span>            | <span data-ttu-id="db345-205">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-205">False</span></span>                                                       |
| <span data-ttu-id="db345-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="db345-206">Is-Single-Valued</span></span>       | <span data-ttu-id="db345-207">True</span><span class="sxs-lookup"><span data-stu-id="db345-207">True</span></span>                                                        |
| <span data-ttu-id="db345-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="db345-208">Is Indexed</span></span>             | <span data-ttu-id="db345-209">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-209">False</span></span>                                                       |
| <span data-ttu-id="db345-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="db345-210">In Global Catalog</span></span>      | <span data-ttu-id="db345-211">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-211">False</span></span>                                                       |
| <span data-ttu-id="db345-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db345-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="db345-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="db345-213">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="db345-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db345-214">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="db345-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db345-215">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="db345-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db345-216">Search-Flags</span></span>           | <span data-ttu-id="db345-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db345-217">0x00000000</span></span>                                                  |
| <span data-ttu-id="db345-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db345-218">System-Flags</span></span>           | <span data-ttu-id="db345-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db345-219">0x00000010</span></span>                                                  |
| <span data-ttu-id="db345-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="db345-220">Classes used in</span></span>        | [<span data-ttu-id="db345-221">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="db345-221">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="db345-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db345-222">Windows Server 2008</span></span>



| <span data-ttu-id="db345-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="db345-223">Entry</span></span> | <span data-ttu-id="db345-224">Valor</span><span class="sxs-lookup"><span data-stu-id="db345-224">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="db345-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="db345-225">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="db345-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db345-226">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="db345-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="db345-227">System-Only</span></span>            | <span data-ttu-id="db345-228">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-228">False</span></span>                                                       |
| <span data-ttu-id="db345-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="db345-229">Is-Single-Valued</span></span>       | <span data-ttu-id="db345-230">True</span><span class="sxs-lookup"><span data-stu-id="db345-230">True</span></span>                                                        |
| <span data-ttu-id="db345-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="db345-231">Is Indexed</span></span>             | <span data-ttu-id="db345-232">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-232">False</span></span>                                                       |
| <span data-ttu-id="db345-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="db345-233">In Global Catalog</span></span>      | <span data-ttu-id="db345-234">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-234">False</span></span>                                                       |
| <span data-ttu-id="db345-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db345-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="db345-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="db345-236">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="db345-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db345-237">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="db345-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db345-238">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="db345-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db345-239">Search-Flags</span></span>           | <span data-ttu-id="db345-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db345-240">0x00000000</span></span>                                                  |
| <span data-ttu-id="db345-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db345-241">System-Flags</span></span>           | <span data-ttu-id="db345-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db345-242">0x00000010</span></span>                                                  |
| <span data-ttu-id="db345-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="db345-243">Classes used in</span></span>        | [<span data-ttu-id="db345-244">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="db345-244">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="db345-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="db345-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="db345-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="db345-246">Entry</span></span> | <span data-ttu-id="db345-247">Valor</span><span class="sxs-lookup"><span data-stu-id="db345-247">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="db345-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="db345-248">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="db345-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db345-249">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="db345-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="db345-250">System-Only</span></span>            | <span data-ttu-id="db345-251">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-251">False</span></span>                                                       |
| <span data-ttu-id="db345-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="db345-252">Is-Single-Valued</span></span>       | <span data-ttu-id="db345-253">True</span><span class="sxs-lookup"><span data-stu-id="db345-253">True</span></span>                                                        |
| <span data-ttu-id="db345-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="db345-254">Is Indexed</span></span>             | <span data-ttu-id="db345-255">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-255">False</span></span>                                                       |
| <span data-ttu-id="db345-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="db345-256">In Global Catalog</span></span>      | <span data-ttu-id="db345-257">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-257">False</span></span>                                                       |
| <span data-ttu-id="db345-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db345-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="db345-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="db345-259">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="db345-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db345-260">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="db345-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db345-261">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="db345-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db345-262">Search-Flags</span></span>           | <span data-ttu-id="db345-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db345-263">0x00000000</span></span>                                                  |
| <span data-ttu-id="db345-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db345-264">System-Flags</span></span>           | <span data-ttu-id="db345-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db345-265">0x00000010</span></span>                                                  |
| <span data-ttu-id="db345-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="db345-266">Classes used in</span></span>        | [<span data-ttu-id="db345-267">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="db345-267">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="db345-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="db345-268">Windows Server 2012</span></span>



| <span data-ttu-id="db345-269">Entrada</span><span class="sxs-lookup"><span data-stu-id="db345-269">Entry</span></span> | <span data-ttu-id="db345-270">Valor</span><span class="sxs-lookup"><span data-stu-id="db345-270">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="db345-271">ID do link</span><span class="sxs-lookup"><span data-stu-id="db345-271">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="db345-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db345-272">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="db345-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="db345-273">System-Only</span></span>            | <span data-ttu-id="db345-274">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-274">False</span></span>                                                       |
| <span data-ttu-id="db345-275">É de valor único</span><span class="sxs-lookup"><span data-stu-id="db345-275">Is-Single-Valued</span></span>       | <span data-ttu-id="db345-276">True</span><span class="sxs-lookup"><span data-stu-id="db345-276">True</span></span>                                                        |
| <span data-ttu-id="db345-277">É indexado</span><span class="sxs-lookup"><span data-stu-id="db345-277">Is Indexed</span></span>             | <span data-ttu-id="db345-278">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-278">False</span></span>                                                       |
| <span data-ttu-id="db345-279">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="db345-279">In Global Catalog</span></span>      | <span data-ttu-id="db345-280">Falso</span><span class="sxs-lookup"><span data-stu-id="db345-280">False</span></span>                                                       |
| <span data-ttu-id="db345-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db345-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="db345-282">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="db345-282">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="db345-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db345-283">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="db345-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db345-284">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="db345-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db345-285">Search-Flags</span></span>           | <span data-ttu-id="db345-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db345-286">0x00000000</span></span>                                                  |
| <span data-ttu-id="db345-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db345-287">System-Flags</span></span>           | <span data-ttu-id="db345-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db345-288">0x00000010</span></span>                                                  |
| <span data-ttu-id="db345-289">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="db345-289">Classes used in</span></span>        | [<span data-ttu-id="db345-290">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="db345-290">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





