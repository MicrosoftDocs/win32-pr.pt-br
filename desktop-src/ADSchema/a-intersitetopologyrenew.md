---
title: Atributo entre sites-de renovação de topologia
description: Essa classe indica com que frequência o gerador de topologia entre sites atualiza a mensagem Keep-Alive que é enviada aos controladores de domínio contidos no mesmo site.
ms.assetid: 523d8161-0678-482f-8d66-55a112995fe5
ms.tgt_platform: multiple
keywords:
- Atributo do AD de atributos entre sites-Topology-rerenew
- Esquema de AD do atributo interSiteTopologyRenew
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Renew
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821bd294f777fd29738ff102955cd170a42205e2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105769112"
---
# <a name="inter-site-topology-renew-attribute"></a><span data-ttu-id="abd29-105">Atributo entre sites-de renovação de topologia</span><span class="sxs-lookup"><span data-stu-id="abd29-105">Inter-Site-Topology-Renew attribute</span></span>

<span data-ttu-id="abd29-106">Essa classe indica com que frequência o gerador de topologia entre sites atualiza a mensagem Keep-Alive que é enviada aos controladores de domínio contidos no mesmo site.</span><span class="sxs-lookup"><span data-stu-id="abd29-106">This class indicates how often the intersite topology generator updates the keep-alive message that is sent to domain controllers contained in the same site.</span></span>



| <span data-ttu-id="abd29-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="abd29-107">Entry</span></span> | <span data-ttu-id="abd29-108">Valor</span><span class="sxs-lookup"><span data-stu-id="abd29-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="abd29-109">CN</span><span class="sxs-lookup"><span data-stu-id="abd29-109">CN</span></span>                | <span data-ttu-id="abd29-110">Topologia entre sites-renovar</span><span class="sxs-lookup"><span data-stu-id="abd29-110">Inter-Site-Topology-Renew</span></span>            |
| <span data-ttu-id="abd29-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="abd29-111">Ldap-Display-Name</span></span> | <span data-ttu-id="abd29-112">interSiteTopologyRenew</span><span class="sxs-lookup"><span data-stu-id="abd29-112">interSiteTopologyRenew</span></span>               |
| <span data-ttu-id="abd29-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="abd29-113">Size</span></span>              | <span data-ttu-id="abd29-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="abd29-114">4 bytes</span></span>                              |
| <span data-ttu-id="abd29-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="abd29-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="abd29-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="abd29-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="abd29-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="abd29-117">Attribute-Id</span></span>      | <span data-ttu-id="abd29-118">1.2.840.113556.1.4.1247</span><span class="sxs-lookup"><span data-stu-id="abd29-118">1.2.840.113556.1.4.1247</span></span>              |
| <span data-ttu-id="abd29-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="abd29-119">System-Id-Guid</span></span>    | <span data-ttu-id="abd29-120">b7c69e5f-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="abd29-120">b7c69e5f-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="abd29-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="abd29-121">Syntax</span></span>            | [<span data-ttu-id="abd29-122">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="abd29-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="abd29-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="abd29-123">Implementations</span></span>

-   [<span data-ttu-id="abd29-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="abd29-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="abd29-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="abd29-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="abd29-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="abd29-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="abd29-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="abd29-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="abd29-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="abd29-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="abd29-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="abd29-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="abd29-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="abd29-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="abd29-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="abd29-131">Windows 2000 Server</span></span>



| <span data-ttu-id="abd29-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="abd29-132">Entry</span></span> | <span data-ttu-id="abd29-133">Valor</span><span class="sxs-lookup"><span data-stu-id="abd29-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="abd29-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="abd29-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="abd29-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="abd29-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="abd29-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="abd29-136">System-Only</span></span>            | <span data-ttu-id="abd29-137">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-137">False</span></span>                                                       |
| <span data-ttu-id="abd29-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="abd29-138">Is-Single-Valued</span></span>       | <span data-ttu-id="abd29-139">True</span><span class="sxs-lookup"><span data-stu-id="abd29-139">True</span></span>                                                        |
| <span data-ttu-id="abd29-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="abd29-140">Is Indexed</span></span>             | <span data-ttu-id="abd29-141">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-141">False</span></span>                                                       |
| <span data-ttu-id="abd29-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="abd29-142">In Global Catalog</span></span>      | <span data-ttu-id="abd29-143">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-143">False</span></span>                                                       |
| <span data-ttu-id="abd29-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="abd29-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="abd29-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="abd29-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="abd29-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="abd29-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="abd29-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="abd29-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="abd29-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="abd29-148">Search-Flags</span></span>           | <span data-ttu-id="abd29-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="abd29-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="abd29-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="abd29-150">System-Flags</span></span>           | <span data-ttu-id="abd29-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="abd29-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="abd29-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="abd29-152">Classes used in</span></span>        | [<span data-ttu-id="abd29-153">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="abd29-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="abd29-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="abd29-154">Windows Server 2003</span></span>



| <span data-ttu-id="abd29-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="abd29-155">Entry</span></span> | <span data-ttu-id="abd29-156">Valor</span><span class="sxs-lookup"><span data-stu-id="abd29-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="abd29-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="abd29-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="abd29-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="abd29-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="abd29-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="abd29-159">System-Only</span></span>            | <span data-ttu-id="abd29-160">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-160">False</span></span>                                                       |
| <span data-ttu-id="abd29-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="abd29-161">Is-Single-Valued</span></span>       | <span data-ttu-id="abd29-162">True</span><span class="sxs-lookup"><span data-stu-id="abd29-162">True</span></span>                                                        |
| <span data-ttu-id="abd29-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="abd29-163">Is Indexed</span></span>             | <span data-ttu-id="abd29-164">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-164">False</span></span>                                                       |
| <span data-ttu-id="abd29-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="abd29-165">In Global Catalog</span></span>      | <span data-ttu-id="abd29-166">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-166">False</span></span>                                                       |
| <span data-ttu-id="abd29-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="abd29-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="abd29-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="abd29-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="abd29-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="abd29-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="abd29-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="abd29-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="abd29-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="abd29-171">Search-Flags</span></span>           | <span data-ttu-id="abd29-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="abd29-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="abd29-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="abd29-173">System-Flags</span></span>           | <span data-ttu-id="abd29-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="abd29-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="abd29-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="abd29-175">Classes used in</span></span>        | [<span data-ttu-id="abd29-176">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="abd29-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="abd29-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="abd29-177">ADAM</span></span>



| <span data-ttu-id="abd29-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="abd29-178">Entry</span></span> | <span data-ttu-id="abd29-179">Valor</span><span class="sxs-lookup"><span data-stu-id="abd29-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="abd29-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="abd29-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="abd29-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="abd29-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="abd29-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="abd29-182">System-Only</span></span>            | <span data-ttu-id="abd29-183">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-183">False</span></span>                                                       |
| <span data-ttu-id="abd29-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="abd29-184">Is-Single-Valued</span></span>       | <span data-ttu-id="abd29-185">True</span><span class="sxs-lookup"><span data-stu-id="abd29-185">True</span></span>                                                        |
| <span data-ttu-id="abd29-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="abd29-186">Is Indexed</span></span>             | <span data-ttu-id="abd29-187">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-187">False</span></span>                                                       |
| <span data-ttu-id="abd29-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="abd29-188">In Global Catalog</span></span>      | <span data-ttu-id="abd29-189">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-189">False</span></span>                                                       |
| <span data-ttu-id="abd29-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="abd29-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="abd29-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="abd29-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="abd29-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="abd29-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="abd29-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="abd29-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="abd29-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="abd29-194">Search-Flags</span></span>           | <span data-ttu-id="abd29-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="abd29-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="abd29-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="abd29-196">System-Flags</span></span>           | <span data-ttu-id="abd29-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="abd29-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="abd29-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="abd29-198">Classes used in</span></span>        | [<span data-ttu-id="abd29-199">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="abd29-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="abd29-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="abd29-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="abd29-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="abd29-201">Entry</span></span> | <span data-ttu-id="abd29-202">Valor</span><span class="sxs-lookup"><span data-stu-id="abd29-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="abd29-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="abd29-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="abd29-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="abd29-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="abd29-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="abd29-205">System-Only</span></span>            | <span data-ttu-id="abd29-206">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-206">False</span></span>                                                       |
| <span data-ttu-id="abd29-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="abd29-207">Is-Single-Valued</span></span>       | <span data-ttu-id="abd29-208">True</span><span class="sxs-lookup"><span data-stu-id="abd29-208">True</span></span>                                                        |
| <span data-ttu-id="abd29-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="abd29-209">Is Indexed</span></span>             | <span data-ttu-id="abd29-210">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-210">False</span></span>                                                       |
| <span data-ttu-id="abd29-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="abd29-211">In Global Catalog</span></span>      | <span data-ttu-id="abd29-212">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-212">False</span></span>                                                       |
| <span data-ttu-id="abd29-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="abd29-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="abd29-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="abd29-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="abd29-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="abd29-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="abd29-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="abd29-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="abd29-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="abd29-217">Search-Flags</span></span>           | <span data-ttu-id="abd29-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="abd29-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="abd29-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="abd29-219">System-Flags</span></span>           | <span data-ttu-id="abd29-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="abd29-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="abd29-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="abd29-221">Classes used in</span></span>        | [<span data-ttu-id="abd29-222">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="abd29-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="abd29-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="abd29-223">Windows Server 2008</span></span>



| <span data-ttu-id="abd29-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="abd29-224">Entry</span></span> | <span data-ttu-id="abd29-225">Valor</span><span class="sxs-lookup"><span data-stu-id="abd29-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="abd29-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="abd29-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="abd29-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="abd29-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="abd29-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="abd29-228">System-Only</span></span>            | <span data-ttu-id="abd29-229">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-229">False</span></span>                                                       |
| <span data-ttu-id="abd29-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="abd29-230">Is-Single-Valued</span></span>       | <span data-ttu-id="abd29-231">True</span><span class="sxs-lookup"><span data-stu-id="abd29-231">True</span></span>                                                        |
| <span data-ttu-id="abd29-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="abd29-232">Is Indexed</span></span>             | <span data-ttu-id="abd29-233">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-233">False</span></span>                                                       |
| <span data-ttu-id="abd29-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="abd29-234">In Global Catalog</span></span>      | <span data-ttu-id="abd29-235">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-235">False</span></span>                                                       |
| <span data-ttu-id="abd29-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="abd29-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="abd29-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="abd29-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="abd29-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="abd29-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="abd29-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="abd29-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="abd29-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="abd29-240">Search-Flags</span></span>           | <span data-ttu-id="abd29-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="abd29-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="abd29-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="abd29-242">System-Flags</span></span>           | <span data-ttu-id="abd29-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="abd29-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="abd29-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="abd29-244">Classes used in</span></span>        | [<span data-ttu-id="abd29-245">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="abd29-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="abd29-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="abd29-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="abd29-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="abd29-247">Entry</span></span> | <span data-ttu-id="abd29-248">Valor</span><span class="sxs-lookup"><span data-stu-id="abd29-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="abd29-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="abd29-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="abd29-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="abd29-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="abd29-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="abd29-251">System-Only</span></span>            | <span data-ttu-id="abd29-252">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-252">False</span></span>                                                       |
| <span data-ttu-id="abd29-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="abd29-253">Is-Single-Valued</span></span>       | <span data-ttu-id="abd29-254">True</span><span class="sxs-lookup"><span data-stu-id="abd29-254">True</span></span>                                                        |
| <span data-ttu-id="abd29-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="abd29-255">Is Indexed</span></span>             | <span data-ttu-id="abd29-256">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-256">False</span></span>                                                       |
| <span data-ttu-id="abd29-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="abd29-257">In Global Catalog</span></span>      | <span data-ttu-id="abd29-258">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-258">False</span></span>                                                       |
| <span data-ttu-id="abd29-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="abd29-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="abd29-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="abd29-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="abd29-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="abd29-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="abd29-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="abd29-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="abd29-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="abd29-263">Search-Flags</span></span>           | <span data-ttu-id="abd29-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="abd29-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="abd29-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="abd29-265">System-Flags</span></span>           | <span data-ttu-id="abd29-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="abd29-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="abd29-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="abd29-267">Classes used in</span></span>        | [<span data-ttu-id="abd29-268">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="abd29-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="abd29-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="abd29-269">Windows Server 2012</span></span>



| <span data-ttu-id="abd29-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="abd29-270">Entry</span></span> | <span data-ttu-id="abd29-271">Valor</span><span class="sxs-lookup"><span data-stu-id="abd29-271">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="abd29-272">ID do link</span><span class="sxs-lookup"><span data-stu-id="abd29-272">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="abd29-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="abd29-273">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="abd29-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="abd29-274">System-Only</span></span>            | <span data-ttu-id="abd29-275">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-275">False</span></span>                                                       |
| <span data-ttu-id="abd29-276">É de valor único</span><span class="sxs-lookup"><span data-stu-id="abd29-276">Is-Single-Valued</span></span>       | <span data-ttu-id="abd29-277">True</span><span class="sxs-lookup"><span data-stu-id="abd29-277">True</span></span>                                                        |
| <span data-ttu-id="abd29-278">É indexado</span><span class="sxs-lookup"><span data-stu-id="abd29-278">Is Indexed</span></span>             | <span data-ttu-id="abd29-279">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-279">False</span></span>                                                       |
| <span data-ttu-id="abd29-280">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="abd29-280">In Global Catalog</span></span>      | <span data-ttu-id="abd29-281">Falso</span><span class="sxs-lookup"><span data-stu-id="abd29-281">False</span></span>                                                       |
| <span data-ttu-id="abd29-282">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="abd29-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="abd29-283">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="abd29-283">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="abd29-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="abd29-284">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="abd29-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="abd29-285">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="abd29-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="abd29-286">Search-Flags</span></span>           | <span data-ttu-id="abd29-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="abd29-287">0x00000000</span></span>                                                  |
| <span data-ttu-id="abd29-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="abd29-288">System-Flags</span></span>           | <span data-ttu-id="abd29-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="abd29-289">0x00000010</span></span>                                                  |
| <span data-ttu-id="abd29-290">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="abd29-290">Classes used in</span></span>        | [<span data-ttu-id="abd29-291">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="abd29-291">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





