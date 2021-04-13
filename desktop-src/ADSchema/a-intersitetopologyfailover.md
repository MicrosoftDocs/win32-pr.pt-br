---
title: Atributo entre sites-topologia-failover
description: Indica quanto tempo deve ser transcorrido desde a última atividade para o gerador de topologia entre sites ser considerada inativa.
ms.assetid: d351dbec-d5a3-46e1-87a9-0856d19e07c6
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo entre sites-Topology-failover
- Esquema de AD do atributo interSiteTopologyFailover
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Failover
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4e9cad98bade7fd69178a8fce795d0b92f35b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456241"
---
# <a name="inter-site-topology-failover-attribute"></a><span data-ttu-id="cc8c1-105">Atributo entre sites-topologia-failover</span><span class="sxs-lookup"><span data-stu-id="cc8c1-105">Inter-Site-Topology-Failover attribute</span></span>

<span data-ttu-id="cc8c1-106">Indica quanto tempo deve ser transcorrido desde a última atividade para o gerador de topologia entre sites ser considerada inativa.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-106">Indicates how much time must transpire since the last keep-alive for the inter-site topology generator to be considered dead.</span></span>



| <span data-ttu-id="cc8c1-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="cc8c1-107">Entry</span></span> | <span data-ttu-id="cc8c1-108">Valor</span><span class="sxs-lookup"><span data-stu-id="cc8c1-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="cc8c1-109">CN</span><span class="sxs-lookup"><span data-stu-id="cc8c1-109">CN</span></span>                | <span data-ttu-id="cc8c1-110">Failover entre sites-topologia</span><span class="sxs-lookup"><span data-stu-id="cc8c1-110">Inter-Site-Topology-Failover</span></span>         |
| <span data-ttu-id="cc8c1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cc8c1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cc8c1-112">interSiteTopologyFailover</span><span class="sxs-lookup"><span data-stu-id="cc8c1-112">interSiteTopologyFailover</span></span>            |
| <span data-ttu-id="cc8c1-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="cc8c1-113">Size</span></span>              | <span data-ttu-id="cc8c1-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="cc8c1-114">4 bytes</span></span>                              |
| <span data-ttu-id="cc8c1-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="cc8c1-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="cc8c1-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="cc8c1-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="cc8c1-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cc8c1-117">Attribute-Id</span></span>      | <span data-ttu-id="cc8c1-118">1.2.840.113556.1.4.1248</span><span class="sxs-lookup"><span data-stu-id="cc8c1-118">1.2.840.113556.1.4.1248</span></span>              |
| <span data-ttu-id="cc8c1-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cc8c1-119">System-Id-Guid</span></span>    | <span data-ttu-id="cc8c1-120">b7c69e60-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="cc8c1-120">b7c69e60-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="cc8c1-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc8c1-121">Syntax</span></span>            | [<span data-ttu-id="cc8c1-122">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="cc8c1-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="cc8c1-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="cc8c1-123">Implementations</span></span>

-   [<span data-ttu-id="cc8c1-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cc8c1-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cc8c1-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cc8c1-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cc8c1-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cc8c1-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cc8c1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cc8c1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cc8c1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cc8c1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cc8c1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cc8c1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cc8c1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cc8c1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cc8c1-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cc8c1-131">Windows 2000 Server</span></span>



| <span data-ttu-id="cc8c1-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="cc8c1-132">Entry</span></span> | <span data-ttu-id="cc8c1-133">Valor</span><span class="sxs-lookup"><span data-stu-id="cc8c1-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="cc8c1-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="cc8c1-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="cc8c1-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc8c1-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="cc8c1-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc8c1-136">System-Only</span></span>            | <span data-ttu-id="cc8c1-137">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-137">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cc8c1-138">Is-Single-Valued</span></span>       | <span data-ttu-id="cc8c1-139">True</span><span class="sxs-lookup"><span data-stu-id="cc8c1-139">True</span></span>                                                        |
| <span data-ttu-id="cc8c1-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="cc8c1-140">Is Indexed</span></span>             | <span data-ttu-id="cc8c1-141">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-141">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cc8c1-142">In Global Catalog</span></span>      | <span data-ttu-id="cc8c1-143">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-143">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cc8c1-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc8c1-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cc8c1-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="cc8c1-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc8c1-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="cc8c1-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc8c1-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="cc8c1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc8c1-148">Search-Flags</span></span>           | <span data-ttu-id="cc8c1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc8c1-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="cc8c1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc8c1-150">System-Flags</span></span>           | <span data-ttu-id="cc8c1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc8c1-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="cc8c1-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cc8c1-152">Classes used in</span></span>        | [<span data-ttu-id="cc8c1-153">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="cc8c1-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cc8c1-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cc8c1-154">Windows Server 2003</span></span>



| <span data-ttu-id="cc8c1-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="cc8c1-155">Entry</span></span> | <span data-ttu-id="cc8c1-156">Valor</span><span class="sxs-lookup"><span data-stu-id="cc8c1-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="cc8c1-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="cc8c1-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="cc8c1-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc8c1-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="cc8c1-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc8c1-159">System-Only</span></span>            | <span data-ttu-id="cc8c1-160">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-160">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cc8c1-161">Is-Single-Valued</span></span>       | <span data-ttu-id="cc8c1-162">True</span><span class="sxs-lookup"><span data-stu-id="cc8c1-162">True</span></span>                                                        |
| <span data-ttu-id="cc8c1-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="cc8c1-163">Is Indexed</span></span>             | <span data-ttu-id="cc8c1-164">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-164">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cc8c1-165">In Global Catalog</span></span>      | <span data-ttu-id="cc8c1-166">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-166">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cc8c1-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc8c1-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cc8c1-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="cc8c1-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc8c1-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="cc8c1-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc8c1-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="cc8c1-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc8c1-171">Search-Flags</span></span>           | <span data-ttu-id="cc8c1-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc8c1-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="cc8c1-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc8c1-173">System-Flags</span></span>           | <span data-ttu-id="cc8c1-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc8c1-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="cc8c1-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cc8c1-175">Classes used in</span></span>        | [<span data-ttu-id="cc8c1-176">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="cc8c1-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cc8c1-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="cc8c1-177">ADAM</span></span>



| <span data-ttu-id="cc8c1-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="cc8c1-178">Entry</span></span> | <span data-ttu-id="cc8c1-179">Valor</span><span class="sxs-lookup"><span data-stu-id="cc8c1-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="cc8c1-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="cc8c1-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="cc8c1-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc8c1-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="cc8c1-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc8c1-182">System-Only</span></span>            | <span data-ttu-id="cc8c1-183">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-183">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cc8c1-184">Is-Single-Valued</span></span>       | <span data-ttu-id="cc8c1-185">True</span><span class="sxs-lookup"><span data-stu-id="cc8c1-185">True</span></span>                                                        |
| <span data-ttu-id="cc8c1-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="cc8c1-186">Is Indexed</span></span>             | <span data-ttu-id="cc8c1-187">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-187">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cc8c1-188">In Global Catalog</span></span>      | <span data-ttu-id="cc8c1-189">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-189">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cc8c1-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc8c1-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cc8c1-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="cc8c1-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc8c1-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="cc8c1-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc8c1-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="cc8c1-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc8c1-194">Search-Flags</span></span>           | <span data-ttu-id="cc8c1-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc8c1-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="cc8c1-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc8c1-196">System-Flags</span></span>           | <span data-ttu-id="cc8c1-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc8c1-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="cc8c1-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cc8c1-198">Classes used in</span></span>        | [<span data-ttu-id="cc8c1-199">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="cc8c1-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cc8c1-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cc8c1-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cc8c1-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="cc8c1-201">Entry</span></span> | <span data-ttu-id="cc8c1-202">Valor</span><span class="sxs-lookup"><span data-stu-id="cc8c1-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="cc8c1-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="cc8c1-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="cc8c1-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc8c1-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="cc8c1-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc8c1-205">System-Only</span></span>            | <span data-ttu-id="cc8c1-206">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-206">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cc8c1-207">Is-Single-Valued</span></span>       | <span data-ttu-id="cc8c1-208">True</span><span class="sxs-lookup"><span data-stu-id="cc8c1-208">True</span></span>                                                        |
| <span data-ttu-id="cc8c1-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="cc8c1-209">Is Indexed</span></span>             | <span data-ttu-id="cc8c1-210">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-210">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cc8c1-211">In Global Catalog</span></span>      | <span data-ttu-id="cc8c1-212">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-212">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cc8c1-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc8c1-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cc8c1-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="cc8c1-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc8c1-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="cc8c1-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc8c1-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="cc8c1-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc8c1-217">Search-Flags</span></span>           | <span data-ttu-id="cc8c1-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc8c1-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="cc8c1-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc8c1-219">System-Flags</span></span>           | <span data-ttu-id="cc8c1-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc8c1-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="cc8c1-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cc8c1-221">Classes used in</span></span>        | [<span data-ttu-id="cc8c1-222">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="cc8c1-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cc8c1-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc8c1-223">Windows Server 2008</span></span>



| <span data-ttu-id="cc8c1-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="cc8c1-224">Entry</span></span> | <span data-ttu-id="cc8c1-225">Valor</span><span class="sxs-lookup"><span data-stu-id="cc8c1-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="cc8c1-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="cc8c1-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="cc8c1-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc8c1-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="cc8c1-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc8c1-228">System-Only</span></span>            | <span data-ttu-id="cc8c1-229">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-229">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cc8c1-230">Is-Single-Valued</span></span>       | <span data-ttu-id="cc8c1-231">True</span><span class="sxs-lookup"><span data-stu-id="cc8c1-231">True</span></span>                                                        |
| <span data-ttu-id="cc8c1-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="cc8c1-232">Is Indexed</span></span>             | <span data-ttu-id="cc8c1-233">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-233">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cc8c1-234">In Global Catalog</span></span>      | <span data-ttu-id="cc8c1-235">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-235">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cc8c1-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc8c1-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cc8c1-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="cc8c1-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc8c1-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="cc8c1-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc8c1-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="cc8c1-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc8c1-240">Search-Flags</span></span>           | <span data-ttu-id="cc8c1-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc8c1-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="cc8c1-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc8c1-242">System-Flags</span></span>           | <span data-ttu-id="cc8c1-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc8c1-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="cc8c1-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cc8c1-244">Classes used in</span></span>        | [<span data-ttu-id="cc8c1-245">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="cc8c1-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cc8c1-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cc8c1-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cc8c1-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="cc8c1-247">Entry</span></span> | <span data-ttu-id="cc8c1-248">Valor</span><span class="sxs-lookup"><span data-stu-id="cc8c1-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="cc8c1-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="cc8c1-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="cc8c1-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc8c1-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="cc8c1-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc8c1-251">System-Only</span></span>            | <span data-ttu-id="cc8c1-252">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-252">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cc8c1-253">Is-Single-Valued</span></span>       | <span data-ttu-id="cc8c1-254">True</span><span class="sxs-lookup"><span data-stu-id="cc8c1-254">True</span></span>                                                        |
| <span data-ttu-id="cc8c1-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="cc8c1-255">Is Indexed</span></span>             | <span data-ttu-id="cc8c1-256">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-256">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cc8c1-257">In Global Catalog</span></span>      | <span data-ttu-id="cc8c1-258">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-258">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cc8c1-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc8c1-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cc8c1-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="cc8c1-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc8c1-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="cc8c1-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc8c1-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="cc8c1-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc8c1-263">Search-Flags</span></span>           | <span data-ttu-id="cc8c1-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc8c1-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="cc8c1-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc8c1-265">System-Flags</span></span>           | <span data-ttu-id="cc8c1-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc8c1-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="cc8c1-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cc8c1-267">Classes used in</span></span>        | [<span data-ttu-id="cc8c1-268">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="cc8c1-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cc8c1-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cc8c1-269">Windows Server 2012</span></span>



| <span data-ttu-id="cc8c1-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="cc8c1-270">Entry</span></span> | <span data-ttu-id="cc8c1-271">Valor</span><span class="sxs-lookup"><span data-stu-id="cc8c1-271">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="cc8c1-272">ID do link</span><span class="sxs-lookup"><span data-stu-id="cc8c1-272">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="cc8c1-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc8c1-273">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="cc8c1-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc8c1-274">System-Only</span></span>            | <span data-ttu-id="cc8c1-275">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-275">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-276">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cc8c1-276">Is-Single-Valued</span></span>       | <span data-ttu-id="cc8c1-277">True</span><span class="sxs-lookup"><span data-stu-id="cc8c1-277">True</span></span>                                                        |
| <span data-ttu-id="cc8c1-278">É indexado</span><span class="sxs-lookup"><span data-stu-id="cc8c1-278">Is Indexed</span></span>             | <span data-ttu-id="cc8c1-279">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-279">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-280">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cc8c1-280">In Global Catalog</span></span>      | <span data-ttu-id="cc8c1-281">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-281">False</span></span>                                                       |
| <span data-ttu-id="cc8c1-282">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cc8c1-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc8c1-283">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cc8c1-283">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="cc8c1-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc8c1-284">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="cc8c1-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc8c1-285">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="cc8c1-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc8c1-286">Search-Flags</span></span>           | <span data-ttu-id="cc8c1-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc8c1-287">0x00000000</span></span>                                                  |
| <span data-ttu-id="cc8c1-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc8c1-288">System-Flags</span></span>           | <span data-ttu-id="cc8c1-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc8c1-289">0x00000010</span></span>                                                  |
| <span data-ttu-id="cc8c1-290">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cc8c1-290">Classes used in</span></span>        | [<span data-ttu-id="cc8c1-291">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="cc8c1-291">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





