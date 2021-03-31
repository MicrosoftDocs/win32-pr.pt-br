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
# <a name="inter-site-topology-generator-attribute"></a><span data-ttu-id="7678d-105">Atributo Inter-Site-Topology-Generator</span><span class="sxs-lookup"><span data-stu-id="7678d-105">Inter-Site-Topology-Generator attribute</span></span>

<span data-ttu-id="7678d-106">Esse atributo será usado para dar suporte ao failover para o computador designado como aquele que é executado Knowledge Consistency Checker geração de topologia entre sites em um determinado site.</span><span class="sxs-lookup"><span data-stu-id="7678d-106">This attribute will be used to support failover for the computer designated as the one that runs Knowledge Consistency Checker inter-site topology generation in a given site.</span></span>



| <span data-ttu-id="7678d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="7678d-107">Entry</span></span> | <span data-ttu-id="7678d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="7678d-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="7678d-109">CN</span><span class="sxs-lookup"><span data-stu-id="7678d-109">CN</span></span>                | <span data-ttu-id="7678d-110">Gerador de topologia entre sites</span><span class="sxs-lookup"><span data-stu-id="7678d-110">Inter-Site-Topology-Generator</span></span>           |
| <span data-ttu-id="7678d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7678d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7678d-112">interSiteTopologyGenerator</span><span class="sxs-lookup"><span data-stu-id="7678d-112">interSiteTopologyGenerator</span></span>              |
| <span data-ttu-id="7678d-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="7678d-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="7678d-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="7678d-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="7678d-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="7678d-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="7678d-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7678d-116">Attribute-Id</span></span>      | <span data-ttu-id="7678d-117">1.2.840.113556.1.4.1246</span><span class="sxs-lookup"><span data-stu-id="7678d-117">1.2.840.113556.1.4.1246</span></span>                 |
| <span data-ttu-id="7678d-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7678d-118">System-Id-Guid</span></span>    | <span data-ttu-id="7678d-119">b7c69e5e-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="7678d-119">b7c69e5e-2cc7-11d2-854e-00a0c983f608</span></span>    |
| <span data-ttu-id="7678d-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="7678d-120">Syntax</span></span>            | [<span data-ttu-id="7678d-121">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="7678d-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="7678d-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="7678d-122">Implementations</span></span>

-   [<span data-ttu-id="7678d-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7678d-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7678d-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7678d-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7678d-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7678d-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7678d-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7678d-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7678d-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7678d-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7678d-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7678d-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7678d-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7678d-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7678d-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7678d-130">Windows 2000 Server</span></span>



| <span data-ttu-id="7678d-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="7678d-131">Entry</span></span> | <span data-ttu-id="7678d-132">Valor</span><span class="sxs-lookup"><span data-stu-id="7678d-132">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7678d-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="7678d-133">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7678d-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7678d-134">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7678d-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7678d-135">System-Only</span></span>            | <span data-ttu-id="7678d-136">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-136">False</span></span>                                                       |
| <span data-ttu-id="7678d-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7678d-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7678d-138">True</span><span class="sxs-lookup"><span data-stu-id="7678d-138">True</span></span>                                                        |
| <span data-ttu-id="7678d-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="7678d-139">Is Indexed</span></span>             | <span data-ttu-id="7678d-140">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-140">False</span></span>                                                       |
| <span data-ttu-id="7678d-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7678d-141">In Global Catalog</span></span>      | <span data-ttu-id="7678d-142">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-142">False</span></span>                                                       |
| <span data-ttu-id="7678d-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7678d-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7678d-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7678d-144">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7678d-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7678d-145">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7678d-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7678d-146">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7678d-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7678d-147">Search-Flags</span></span>           | <span data-ttu-id="7678d-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7678d-148">0x00000000</span></span>                                                  |
| <span data-ttu-id="7678d-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7678d-149">System-Flags</span></span>           | <span data-ttu-id="7678d-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7678d-150">0x00000010</span></span>                                                  |
| <span data-ttu-id="7678d-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7678d-151">Classes used in</span></span>        | [<span data-ttu-id="7678d-152">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="7678d-152">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7678d-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7678d-153">Windows Server 2003</span></span>



| <span data-ttu-id="7678d-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="7678d-154">Entry</span></span> | <span data-ttu-id="7678d-155">Valor</span><span class="sxs-lookup"><span data-stu-id="7678d-155">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7678d-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="7678d-156">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7678d-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7678d-157">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7678d-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="7678d-158">System-Only</span></span>            | <span data-ttu-id="7678d-159">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-159">False</span></span>                                                       |
| <span data-ttu-id="7678d-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7678d-160">Is-Single-Valued</span></span>       | <span data-ttu-id="7678d-161">True</span><span class="sxs-lookup"><span data-stu-id="7678d-161">True</span></span>                                                        |
| <span data-ttu-id="7678d-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="7678d-162">Is Indexed</span></span>             | <span data-ttu-id="7678d-163">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-163">False</span></span>                                                       |
| <span data-ttu-id="7678d-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7678d-164">In Global Catalog</span></span>      | <span data-ttu-id="7678d-165">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-165">False</span></span>                                                       |
| <span data-ttu-id="7678d-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7678d-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="7678d-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7678d-167">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7678d-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7678d-168">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7678d-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7678d-169">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7678d-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7678d-170">Search-Flags</span></span>           | <span data-ttu-id="7678d-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7678d-171">0x00000000</span></span>                                                  |
| <span data-ttu-id="7678d-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7678d-172">System-Flags</span></span>           | <span data-ttu-id="7678d-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7678d-173">0x00000010</span></span>                                                  |
| <span data-ttu-id="7678d-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7678d-174">Classes used in</span></span>        | [<span data-ttu-id="7678d-175">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="7678d-175">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7678d-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="7678d-176">ADAM</span></span>



| <span data-ttu-id="7678d-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="7678d-177">Entry</span></span> | <span data-ttu-id="7678d-178">Valor</span><span class="sxs-lookup"><span data-stu-id="7678d-178">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7678d-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="7678d-179">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7678d-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7678d-180">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7678d-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="7678d-181">System-Only</span></span>            | <span data-ttu-id="7678d-182">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-182">False</span></span>                                                       |
| <span data-ttu-id="7678d-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7678d-183">Is-Single-Valued</span></span>       | <span data-ttu-id="7678d-184">True</span><span class="sxs-lookup"><span data-stu-id="7678d-184">True</span></span>                                                        |
| <span data-ttu-id="7678d-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="7678d-185">Is Indexed</span></span>             | <span data-ttu-id="7678d-186">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-186">False</span></span>                                                       |
| <span data-ttu-id="7678d-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7678d-187">In Global Catalog</span></span>      | <span data-ttu-id="7678d-188">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-188">False</span></span>                                                       |
| <span data-ttu-id="7678d-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7678d-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="7678d-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7678d-190">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7678d-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7678d-191">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7678d-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7678d-192">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7678d-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7678d-193">Search-Flags</span></span>           | <span data-ttu-id="7678d-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7678d-194">0x00000000</span></span>                                                  |
| <span data-ttu-id="7678d-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7678d-195">System-Flags</span></span>           | <span data-ttu-id="7678d-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7678d-196">0x00000010</span></span>                                                  |
| <span data-ttu-id="7678d-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7678d-197">Classes used in</span></span>        | [<span data-ttu-id="7678d-198">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="7678d-198">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7678d-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7678d-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7678d-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="7678d-200">Entry</span></span> | <span data-ttu-id="7678d-201">Valor</span><span class="sxs-lookup"><span data-stu-id="7678d-201">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7678d-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="7678d-202">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7678d-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7678d-203">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7678d-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="7678d-204">System-Only</span></span>            | <span data-ttu-id="7678d-205">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-205">False</span></span>                                                       |
| <span data-ttu-id="7678d-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7678d-206">Is-Single-Valued</span></span>       | <span data-ttu-id="7678d-207">True</span><span class="sxs-lookup"><span data-stu-id="7678d-207">True</span></span>                                                        |
| <span data-ttu-id="7678d-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="7678d-208">Is Indexed</span></span>             | <span data-ttu-id="7678d-209">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-209">False</span></span>                                                       |
| <span data-ttu-id="7678d-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7678d-210">In Global Catalog</span></span>      | <span data-ttu-id="7678d-211">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-211">False</span></span>                                                       |
| <span data-ttu-id="7678d-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7678d-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="7678d-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7678d-213">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7678d-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7678d-214">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7678d-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7678d-215">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7678d-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7678d-216">Search-Flags</span></span>           | <span data-ttu-id="7678d-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7678d-217">0x00000000</span></span>                                                  |
| <span data-ttu-id="7678d-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7678d-218">System-Flags</span></span>           | <span data-ttu-id="7678d-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7678d-219">0x00000010</span></span>                                                  |
| <span data-ttu-id="7678d-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7678d-220">Classes used in</span></span>        | [<span data-ttu-id="7678d-221">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="7678d-221">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7678d-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7678d-222">Windows Server 2008</span></span>



| <span data-ttu-id="7678d-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="7678d-223">Entry</span></span> | <span data-ttu-id="7678d-224">Valor</span><span class="sxs-lookup"><span data-stu-id="7678d-224">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7678d-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="7678d-225">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7678d-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7678d-226">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7678d-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="7678d-227">System-Only</span></span>            | <span data-ttu-id="7678d-228">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-228">False</span></span>                                                       |
| <span data-ttu-id="7678d-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7678d-229">Is-Single-Valued</span></span>       | <span data-ttu-id="7678d-230">True</span><span class="sxs-lookup"><span data-stu-id="7678d-230">True</span></span>                                                        |
| <span data-ttu-id="7678d-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="7678d-231">Is Indexed</span></span>             | <span data-ttu-id="7678d-232">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-232">False</span></span>                                                       |
| <span data-ttu-id="7678d-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7678d-233">In Global Catalog</span></span>      | <span data-ttu-id="7678d-234">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-234">False</span></span>                                                       |
| <span data-ttu-id="7678d-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7678d-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="7678d-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7678d-236">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7678d-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7678d-237">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7678d-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7678d-238">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7678d-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7678d-239">Search-Flags</span></span>           | <span data-ttu-id="7678d-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7678d-240">0x00000000</span></span>                                                  |
| <span data-ttu-id="7678d-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7678d-241">System-Flags</span></span>           | <span data-ttu-id="7678d-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7678d-242">0x00000010</span></span>                                                  |
| <span data-ttu-id="7678d-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7678d-243">Classes used in</span></span>        | [<span data-ttu-id="7678d-244">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="7678d-244">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7678d-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7678d-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7678d-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="7678d-246">Entry</span></span> | <span data-ttu-id="7678d-247">Valor</span><span class="sxs-lookup"><span data-stu-id="7678d-247">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7678d-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="7678d-248">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7678d-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7678d-249">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7678d-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="7678d-250">System-Only</span></span>            | <span data-ttu-id="7678d-251">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-251">False</span></span>                                                       |
| <span data-ttu-id="7678d-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7678d-252">Is-Single-Valued</span></span>       | <span data-ttu-id="7678d-253">True</span><span class="sxs-lookup"><span data-stu-id="7678d-253">True</span></span>                                                        |
| <span data-ttu-id="7678d-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="7678d-254">Is Indexed</span></span>             | <span data-ttu-id="7678d-255">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-255">False</span></span>                                                       |
| <span data-ttu-id="7678d-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7678d-256">In Global Catalog</span></span>      | <span data-ttu-id="7678d-257">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-257">False</span></span>                                                       |
| <span data-ttu-id="7678d-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7678d-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="7678d-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7678d-259">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7678d-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7678d-260">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7678d-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7678d-261">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7678d-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7678d-262">Search-Flags</span></span>           | <span data-ttu-id="7678d-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7678d-263">0x00000000</span></span>                                                  |
| <span data-ttu-id="7678d-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7678d-264">System-Flags</span></span>           | <span data-ttu-id="7678d-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7678d-265">0x00000010</span></span>                                                  |
| <span data-ttu-id="7678d-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7678d-266">Classes used in</span></span>        | [<span data-ttu-id="7678d-267">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="7678d-267">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7678d-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7678d-268">Windows Server 2012</span></span>



| <span data-ttu-id="7678d-269">Entrada</span><span class="sxs-lookup"><span data-stu-id="7678d-269">Entry</span></span> | <span data-ttu-id="7678d-270">Valor</span><span class="sxs-lookup"><span data-stu-id="7678d-270">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7678d-271">ID do link</span><span class="sxs-lookup"><span data-stu-id="7678d-271">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7678d-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7678d-272">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7678d-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="7678d-273">System-Only</span></span>            | <span data-ttu-id="7678d-274">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-274">False</span></span>                                                       |
| <span data-ttu-id="7678d-275">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7678d-275">Is-Single-Valued</span></span>       | <span data-ttu-id="7678d-276">True</span><span class="sxs-lookup"><span data-stu-id="7678d-276">True</span></span>                                                        |
| <span data-ttu-id="7678d-277">É indexado</span><span class="sxs-lookup"><span data-stu-id="7678d-277">Is Indexed</span></span>             | <span data-ttu-id="7678d-278">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-278">False</span></span>                                                       |
| <span data-ttu-id="7678d-279">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7678d-279">In Global Catalog</span></span>      | <span data-ttu-id="7678d-280">Falso</span><span class="sxs-lookup"><span data-stu-id="7678d-280">False</span></span>                                                       |
| <span data-ttu-id="7678d-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7678d-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="7678d-282">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7678d-282">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7678d-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7678d-283">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7678d-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7678d-284">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7678d-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7678d-285">Search-Flags</span></span>           | <span data-ttu-id="7678d-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7678d-286">0x00000000</span></span>                                                  |
| <span data-ttu-id="7678d-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7678d-287">System-Flags</span></span>           | <span data-ttu-id="7678d-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7678d-288">0x00000010</span></span>                                                  |
| <span data-ttu-id="7678d-289">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7678d-289">Classes used in</span></span>        | [<span data-ttu-id="7678d-290">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="7678d-290">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





