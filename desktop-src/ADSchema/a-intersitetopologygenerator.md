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
# <a name="inter-site-topology-generator-attribute"></a><span data-ttu-id="8552c-105">Atributo Inter-Site-Topology-Generator</span><span class="sxs-lookup"><span data-stu-id="8552c-105">Inter-Site-Topology-Generator attribute</span></span>

<span data-ttu-id="8552c-106">Esse atributo será usado para dar suporte ao failover para o computador designado como aquele que é executado Knowledge Consistency Checker geração de topologia entre sites em um determinado site.</span><span class="sxs-lookup"><span data-stu-id="8552c-106">This attribute will be used to support failover for the computer designated as the one that runs Knowledge Consistency Checker inter-site topology generation in a given site.</span></span>



| <span data-ttu-id="8552c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="8552c-107">Entry</span></span> | <span data-ttu-id="8552c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="8552c-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="8552c-109">CN</span><span class="sxs-lookup"><span data-stu-id="8552c-109">CN</span></span>                | <span data-ttu-id="8552c-110">Gerador de topologia entre sites</span><span class="sxs-lookup"><span data-stu-id="8552c-110">Inter-Site-Topology-Generator</span></span>           |
| <span data-ttu-id="8552c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8552c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8552c-112">interSiteTopologyGenerator</span><span class="sxs-lookup"><span data-stu-id="8552c-112">interSiteTopologyGenerator</span></span>              |
| <span data-ttu-id="8552c-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="8552c-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="8552c-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="8552c-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="8552c-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="8552c-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="8552c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8552c-116">Attribute-Id</span></span>      | <span data-ttu-id="8552c-117">1.2.840.113556.1.4.1246</span><span class="sxs-lookup"><span data-stu-id="8552c-117">1.2.840.113556.1.4.1246</span></span>                 |
| <span data-ttu-id="8552c-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8552c-118">System-Id-Guid</span></span>    | <span data-ttu-id="8552c-119">b7c69e5e-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="8552c-119">b7c69e5e-2cc7-11d2-854e-00a0c983f608</span></span>    |
| <span data-ttu-id="8552c-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="8552c-120">Syntax</span></span>            | [<span data-ttu-id="8552c-121">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="8552c-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="8552c-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="8552c-122">Implementations</span></span>

-   [<span data-ttu-id="8552c-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8552c-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8552c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8552c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8552c-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8552c-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8552c-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8552c-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8552c-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8552c-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8552c-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8552c-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8552c-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8552c-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8552c-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8552c-130">Windows 2000 Server</span></span>



| <span data-ttu-id="8552c-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="8552c-131">Entry</span></span> | <span data-ttu-id="8552c-132">Valor</span><span class="sxs-lookup"><span data-stu-id="8552c-132">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="8552c-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="8552c-133">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="8552c-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8552c-134">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="8552c-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="8552c-135">System-Only</span></span>            | <span data-ttu-id="8552c-136">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-136">False</span></span>                                                       |
| <span data-ttu-id="8552c-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8552c-137">Is-Single-Valued</span></span>       | <span data-ttu-id="8552c-138">True</span><span class="sxs-lookup"><span data-stu-id="8552c-138">True</span></span>                                                        |
| <span data-ttu-id="8552c-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="8552c-139">Is Indexed</span></span>             | <span data-ttu-id="8552c-140">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-140">False</span></span>                                                       |
| <span data-ttu-id="8552c-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8552c-141">In Global Catalog</span></span>      | <span data-ttu-id="8552c-142">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-142">False</span></span>                                                       |
| <span data-ttu-id="8552c-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8552c-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="8552c-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8552c-144">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="8552c-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8552c-145">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="8552c-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8552c-146">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="8552c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8552c-147">Search-Flags</span></span>           | <span data-ttu-id="8552c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8552c-148">0x00000000</span></span>                                                  |
| <span data-ttu-id="8552c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8552c-149">System-Flags</span></span>           | <span data-ttu-id="8552c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8552c-150">0x00000010</span></span>                                                  |
| <span data-ttu-id="8552c-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8552c-151">Classes used in</span></span>        | [<span data-ttu-id="8552c-152">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="8552c-152">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8552c-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8552c-153">Windows Server 2003</span></span>



| <span data-ttu-id="8552c-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="8552c-154">Entry</span></span> | <span data-ttu-id="8552c-155">Valor</span><span class="sxs-lookup"><span data-stu-id="8552c-155">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="8552c-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="8552c-156">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="8552c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8552c-157">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="8552c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="8552c-158">System-Only</span></span>            | <span data-ttu-id="8552c-159">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-159">False</span></span>                                                       |
| <span data-ttu-id="8552c-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8552c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="8552c-161">True</span><span class="sxs-lookup"><span data-stu-id="8552c-161">True</span></span>                                                        |
| <span data-ttu-id="8552c-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="8552c-162">Is Indexed</span></span>             | <span data-ttu-id="8552c-163">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-163">False</span></span>                                                       |
| <span data-ttu-id="8552c-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8552c-164">In Global Catalog</span></span>      | <span data-ttu-id="8552c-165">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-165">False</span></span>                                                       |
| <span data-ttu-id="8552c-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8552c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="8552c-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8552c-167">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="8552c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8552c-168">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="8552c-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8552c-169">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="8552c-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8552c-170">Search-Flags</span></span>           | <span data-ttu-id="8552c-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8552c-171">0x00000000</span></span>                                                  |
| <span data-ttu-id="8552c-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8552c-172">System-Flags</span></span>           | <span data-ttu-id="8552c-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8552c-173">0x00000010</span></span>                                                  |
| <span data-ttu-id="8552c-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8552c-174">Classes used in</span></span>        | [<span data-ttu-id="8552c-175">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="8552c-175">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8552c-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="8552c-176">ADAM</span></span>



| <span data-ttu-id="8552c-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="8552c-177">Entry</span></span> | <span data-ttu-id="8552c-178">Valor</span><span class="sxs-lookup"><span data-stu-id="8552c-178">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="8552c-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="8552c-179">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="8552c-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8552c-180">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="8552c-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="8552c-181">System-Only</span></span>            | <span data-ttu-id="8552c-182">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-182">False</span></span>                                                       |
| <span data-ttu-id="8552c-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8552c-183">Is-Single-Valued</span></span>       | <span data-ttu-id="8552c-184">True</span><span class="sxs-lookup"><span data-stu-id="8552c-184">True</span></span>                                                        |
| <span data-ttu-id="8552c-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="8552c-185">Is Indexed</span></span>             | <span data-ttu-id="8552c-186">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-186">False</span></span>                                                       |
| <span data-ttu-id="8552c-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8552c-187">In Global Catalog</span></span>      | <span data-ttu-id="8552c-188">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-188">False</span></span>                                                       |
| <span data-ttu-id="8552c-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8552c-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="8552c-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8552c-190">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="8552c-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8552c-191">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="8552c-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8552c-192">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="8552c-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8552c-193">Search-Flags</span></span>           | <span data-ttu-id="8552c-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8552c-194">0x00000000</span></span>                                                  |
| <span data-ttu-id="8552c-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8552c-195">System-Flags</span></span>           | <span data-ttu-id="8552c-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8552c-196">0x00000010</span></span>                                                  |
| <span data-ttu-id="8552c-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8552c-197">Classes used in</span></span>        | [<span data-ttu-id="8552c-198">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="8552c-198">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8552c-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8552c-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8552c-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="8552c-200">Entry</span></span> | <span data-ttu-id="8552c-201">Valor</span><span class="sxs-lookup"><span data-stu-id="8552c-201">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="8552c-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="8552c-202">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="8552c-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8552c-203">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="8552c-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="8552c-204">System-Only</span></span>            | <span data-ttu-id="8552c-205">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-205">False</span></span>                                                       |
| <span data-ttu-id="8552c-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8552c-206">Is-Single-Valued</span></span>       | <span data-ttu-id="8552c-207">True</span><span class="sxs-lookup"><span data-stu-id="8552c-207">True</span></span>                                                        |
| <span data-ttu-id="8552c-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="8552c-208">Is Indexed</span></span>             | <span data-ttu-id="8552c-209">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-209">False</span></span>                                                       |
| <span data-ttu-id="8552c-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8552c-210">In Global Catalog</span></span>      | <span data-ttu-id="8552c-211">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-211">False</span></span>                                                       |
| <span data-ttu-id="8552c-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8552c-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="8552c-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8552c-213">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="8552c-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8552c-214">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="8552c-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8552c-215">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="8552c-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8552c-216">Search-Flags</span></span>           | <span data-ttu-id="8552c-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8552c-217">0x00000000</span></span>                                                  |
| <span data-ttu-id="8552c-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8552c-218">System-Flags</span></span>           | <span data-ttu-id="8552c-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8552c-219">0x00000010</span></span>                                                  |
| <span data-ttu-id="8552c-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8552c-220">Classes used in</span></span>        | [<span data-ttu-id="8552c-221">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="8552c-221">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8552c-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8552c-222">Windows Server 2008</span></span>



| <span data-ttu-id="8552c-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="8552c-223">Entry</span></span> | <span data-ttu-id="8552c-224">Valor</span><span class="sxs-lookup"><span data-stu-id="8552c-224">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="8552c-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="8552c-225">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="8552c-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8552c-226">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="8552c-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="8552c-227">System-Only</span></span>            | <span data-ttu-id="8552c-228">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-228">False</span></span>                                                       |
| <span data-ttu-id="8552c-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8552c-229">Is-Single-Valued</span></span>       | <span data-ttu-id="8552c-230">True</span><span class="sxs-lookup"><span data-stu-id="8552c-230">True</span></span>                                                        |
| <span data-ttu-id="8552c-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="8552c-231">Is Indexed</span></span>             | <span data-ttu-id="8552c-232">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-232">False</span></span>                                                       |
| <span data-ttu-id="8552c-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8552c-233">In Global Catalog</span></span>      | <span data-ttu-id="8552c-234">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-234">False</span></span>                                                       |
| <span data-ttu-id="8552c-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8552c-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="8552c-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8552c-236">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="8552c-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8552c-237">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="8552c-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8552c-238">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="8552c-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8552c-239">Search-Flags</span></span>           | <span data-ttu-id="8552c-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8552c-240">0x00000000</span></span>                                                  |
| <span data-ttu-id="8552c-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8552c-241">System-Flags</span></span>           | <span data-ttu-id="8552c-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8552c-242">0x00000010</span></span>                                                  |
| <span data-ttu-id="8552c-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8552c-243">Classes used in</span></span>        | [<span data-ttu-id="8552c-244">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="8552c-244">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8552c-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8552c-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8552c-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="8552c-246">Entry</span></span> | <span data-ttu-id="8552c-247">Valor</span><span class="sxs-lookup"><span data-stu-id="8552c-247">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="8552c-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="8552c-248">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="8552c-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8552c-249">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="8552c-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="8552c-250">System-Only</span></span>            | <span data-ttu-id="8552c-251">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-251">False</span></span>                                                       |
| <span data-ttu-id="8552c-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8552c-252">Is-Single-Valued</span></span>       | <span data-ttu-id="8552c-253">True</span><span class="sxs-lookup"><span data-stu-id="8552c-253">True</span></span>                                                        |
| <span data-ttu-id="8552c-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="8552c-254">Is Indexed</span></span>             | <span data-ttu-id="8552c-255">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-255">False</span></span>                                                       |
| <span data-ttu-id="8552c-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8552c-256">In Global Catalog</span></span>      | <span data-ttu-id="8552c-257">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-257">False</span></span>                                                       |
| <span data-ttu-id="8552c-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8552c-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="8552c-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8552c-259">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="8552c-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8552c-260">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="8552c-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8552c-261">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="8552c-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8552c-262">Search-Flags</span></span>           | <span data-ttu-id="8552c-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8552c-263">0x00000000</span></span>                                                  |
| <span data-ttu-id="8552c-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8552c-264">System-Flags</span></span>           | <span data-ttu-id="8552c-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8552c-265">0x00000010</span></span>                                                  |
| <span data-ttu-id="8552c-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8552c-266">Classes used in</span></span>        | [<span data-ttu-id="8552c-267">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="8552c-267">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8552c-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8552c-268">Windows Server 2012</span></span>



| <span data-ttu-id="8552c-269">Entrada</span><span class="sxs-lookup"><span data-stu-id="8552c-269">Entry</span></span> | <span data-ttu-id="8552c-270">Valor</span><span class="sxs-lookup"><span data-stu-id="8552c-270">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="8552c-271">ID do link</span><span class="sxs-lookup"><span data-stu-id="8552c-271">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="8552c-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8552c-272">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="8552c-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="8552c-273">System-Only</span></span>            | <span data-ttu-id="8552c-274">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-274">False</span></span>                                                       |
| <span data-ttu-id="8552c-275">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8552c-275">Is-Single-Valued</span></span>       | <span data-ttu-id="8552c-276">True</span><span class="sxs-lookup"><span data-stu-id="8552c-276">True</span></span>                                                        |
| <span data-ttu-id="8552c-277">É indexado</span><span class="sxs-lookup"><span data-stu-id="8552c-277">Is Indexed</span></span>             | <span data-ttu-id="8552c-278">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-278">False</span></span>                                                       |
| <span data-ttu-id="8552c-279">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8552c-279">In Global Catalog</span></span>      | <span data-ttu-id="8552c-280">Falso</span><span class="sxs-lookup"><span data-stu-id="8552c-280">False</span></span>                                                       |
| <span data-ttu-id="8552c-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8552c-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="8552c-282">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8552c-282">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="8552c-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8552c-283">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="8552c-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8552c-284">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="8552c-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8552c-285">Search-Flags</span></span>           | <span data-ttu-id="8552c-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8552c-286">0x00000000</span></span>                                                  |
| <span data-ttu-id="8552c-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8552c-287">System-Flags</span></span>           | <span data-ttu-id="8552c-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8552c-288">0x00000010</span></span>                                                  |
| <span data-ttu-id="8552c-289">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8552c-289">Classes used in</span></span>        | [<span data-ttu-id="8552c-290">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="8552c-290">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





