---
title: Trust-Direction atributo
description: A direção de uma relação de confiança.
ms.assetid: 29ee19c6-a6c5-40e6-ad70-bfa0a16e3a84
ms.tgt_platform: multiple
keywords:
- Esquema de Trust-Direction do atributo AD
- Esquema de AD do atributo trustDirection
topic_type:
- apiref
api_name:
- Trust-Direction
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54feb80079ea4ac8f1b68fee7d223275313b64b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456169"
---
# <a name="trust-direction-attribute"></a><span data-ttu-id="b8ede-105">Trust-Direction atributo</span><span class="sxs-lookup"><span data-stu-id="b8ede-105">Trust-Direction attribute</span></span>

<span data-ttu-id="b8ede-106">A direção de uma relação de confiança.</span><span class="sxs-lookup"><span data-stu-id="b8ede-106">The direction of a trust.</span></span>



| <span data-ttu-id="b8ede-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8ede-107">Entry</span></span> | <span data-ttu-id="b8ede-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b8ede-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b8ede-109">CN</span><span class="sxs-lookup"><span data-stu-id="b8ede-109">CN</span></span>                | <span data-ttu-id="b8ede-110">Trust-Direction</span><span class="sxs-lookup"><span data-stu-id="b8ede-110">Trust-Direction</span></span>                      |
| <span data-ttu-id="b8ede-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b8ede-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b8ede-112">trustDirection</span><span class="sxs-lookup"><span data-stu-id="b8ede-112">trustDirection</span></span>                       |
| <span data-ttu-id="b8ede-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b8ede-113">Size</span></span>              | <span data-ttu-id="b8ede-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="b8ede-114">4 bytes</span></span>                              |
| <span data-ttu-id="b8ede-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="b8ede-115">Update Privilege</span></span>  | <span data-ttu-id="b8ede-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="b8ede-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="b8ede-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="b8ede-117">Update Frequency</span></span>  | <span data-ttu-id="b8ede-118">Quando uma nova relação de confiança é criada.</span><span class="sxs-lookup"><span data-stu-id="b8ede-118">When a new trust is created.</span></span>         |
| <span data-ttu-id="b8ede-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b8ede-119">Attribute-Id</span></span>      | <span data-ttu-id="b8ede-120">1.2.840.113556.1.4.132</span><span class="sxs-lookup"><span data-stu-id="b8ede-120">1.2.840.113556.1.4.132</span></span>               |
| <span data-ttu-id="b8ede-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b8ede-121">System-Id-Guid</span></span>    | <span data-ttu-id="b8ede-122">bf967a5c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b8ede-122">bf967a5c-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="b8ede-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8ede-123">Syntax</span></span>            | [<span data-ttu-id="b8ede-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="b8ede-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="b8ede-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="b8ede-125">Implementations</span></span>

-   [<span data-ttu-id="b8ede-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b8ede-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b8ede-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b8ede-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b8ede-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b8ede-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b8ede-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b8ede-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b8ede-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b8ede-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b8ede-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b8ede-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b8ede-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b8ede-132">Windows 2000 Server</span></span>



| <span data-ttu-id="b8ede-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8ede-133">Entry</span></span> | <span data-ttu-id="b8ede-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b8ede-134">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b8ede-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8ede-135">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b8ede-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8ede-136">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b8ede-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8ede-137">System-Only</span></span>            | <span data-ttu-id="b8ede-138">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ede-138">False</span></span>                                                |
| <span data-ttu-id="b8ede-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8ede-139">Is-Single-Valued</span></span>       | <span data-ttu-id="b8ede-140">True</span><span class="sxs-lookup"><span data-stu-id="b8ede-140">True</span></span>                                                 |
| <span data-ttu-id="b8ede-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8ede-141">Is Indexed</span></span>             | <span data-ttu-id="b8ede-142">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ede-142">False</span></span>                                                |
| <span data-ttu-id="b8ede-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8ede-143">In Global Catalog</span></span>      | <span data-ttu-id="b8ede-144">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ede-144">False</span></span>                                                |
| <span data-ttu-id="b8ede-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8ede-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8ede-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8ede-146">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b8ede-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8ede-147">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b8ede-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8ede-148">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b8ede-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ede-149">Search-Flags</span></span>           | <span data-ttu-id="b8ede-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8ede-150">0x00000000</span></span>                                           |
| <span data-ttu-id="b8ede-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ede-151">System-Flags</span></span>           | <span data-ttu-id="b8ede-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8ede-152">0x00000010</span></span>                                           |
| <span data-ttu-id="b8ede-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8ede-153">Classes used in</span></span>        | [<span data-ttu-id="b8ede-154">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="b8ede-154">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b8ede-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b8ede-155">Windows Server 2003</span></span>



| <span data-ttu-id="b8ede-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8ede-156">Entry</span></span> | <span data-ttu-id="b8ede-157">Valor</span><span class="sxs-lookup"><span data-stu-id="b8ede-157">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b8ede-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8ede-158">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b8ede-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8ede-159">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b8ede-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8ede-160">System-Only</span></span>            | <span data-ttu-id="b8ede-161">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ede-161">False</span></span>                                                |
| <span data-ttu-id="b8ede-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8ede-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b8ede-163">True</span><span class="sxs-lookup"><span data-stu-id="b8ede-163">True</span></span>                                                 |
| <span data-ttu-id="b8ede-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8ede-164">Is Indexed</span></span>             | <span data-ttu-id="b8ede-165">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ede-165">False</span></span>                                                |
| <span data-ttu-id="b8ede-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8ede-166">In Global Catalog</span></span>      | <span data-ttu-id="b8ede-167">True</span><span class="sxs-lookup"><span data-stu-id="b8ede-167">True</span></span>                                                 |
| <span data-ttu-id="b8ede-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8ede-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8ede-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8ede-169">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b8ede-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8ede-170">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b8ede-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8ede-171">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b8ede-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ede-172">Search-Flags</span></span>           | <span data-ttu-id="b8ede-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8ede-173">0x00000000</span></span>                                           |
| <span data-ttu-id="b8ede-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ede-174">System-Flags</span></span>           | <span data-ttu-id="b8ede-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8ede-175">0x00000010</span></span>                                           |
| <span data-ttu-id="b8ede-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8ede-176">Classes used in</span></span>        | [<span data-ttu-id="b8ede-177">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="b8ede-177">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b8ede-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b8ede-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b8ede-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8ede-179">Entry</span></span> | <span data-ttu-id="b8ede-180">Valor</span><span class="sxs-lookup"><span data-stu-id="b8ede-180">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b8ede-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8ede-181">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b8ede-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8ede-182">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b8ede-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8ede-183">System-Only</span></span>            | <span data-ttu-id="b8ede-184">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ede-184">False</span></span>                                                |
| <span data-ttu-id="b8ede-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8ede-185">Is-Single-Valued</span></span>       | <span data-ttu-id="b8ede-186">True</span><span class="sxs-lookup"><span data-stu-id="b8ede-186">True</span></span>                                                 |
| <span data-ttu-id="b8ede-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8ede-187">Is Indexed</span></span>             | <span data-ttu-id="b8ede-188">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ede-188">False</span></span>                                                |
| <span data-ttu-id="b8ede-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8ede-189">In Global Catalog</span></span>      | <span data-ttu-id="b8ede-190">True</span><span class="sxs-lookup"><span data-stu-id="b8ede-190">True</span></span>                                                 |
| <span data-ttu-id="b8ede-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8ede-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8ede-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8ede-192">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b8ede-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8ede-193">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b8ede-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8ede-194">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b8ede-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ede-195">Search-Flags</span></span>           | <span data-ttu-id="b8ede-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8ede-196">0x00000000</span></span>                                           |
| <span data-ttu-id="b8ede-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ede-197">System-Flags</span></span>           | <span data-ttu-id="b8ede-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8ede-198">0x00000010</span></span>                                           |
| <span data-ttu-id="b8ede-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8ede-199">Classes used in</span></span>        | [<span data-ttu-id="b8ede-200">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="b8ede-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b8ede-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8ede-201">Windows Server 2008</span></span>



| <span data-ttu-id="b8ede-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8ede-202">Entry</span></span> | <span data-ttu-id="b8ede-203">Valor</span><span class="sxs-lookup"><span data-stu-id="b8ede-203">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b8ede-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8ede-204">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b8ede-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8ede-205">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b8ede-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8ede-206">System-Only</span></span>            | <span data-ttu-id="b8ede-207">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ede-207">False</span></span>                                                |
| <span data-ttu-id="b8ede-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8ede-208">Is-Single-Valued</span></span>       | <span data-ttu-id="b8ede-209">True</span><span class="sxs-lookup"><span data-stu-id="b8ede-209">True</span></span>                                                 |
| <span data-ttu-id="b8ede-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8ede-210">Is Indexed</span></span>             | <span data-ttu-id="b8ede-211">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ede-211">False</span></span>                                                |
| <span data-ttu-id="b8ede-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8ede-212">In Global Catalog</span></span>      | <span data-ttu-id="b8ede-213">True</span><span class="sxs-lookup"><span data-stu-id="b8ede-213">True</span></span>                                                 |
| <span data-ttu-id="b8ede-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8ede-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8ede-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8ede-215">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b8ede-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8ede-216">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b8ede-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8ede-217">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b8ede-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ede-218">Search-Flags</span></span>           | <span data-ttu-id="b8ede-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8ede-219">0x00000000</span></span>                                           |
| <span data-ttu-id="b8ede-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ede-220">System-Flags</span></span>           | <span data-ttu-id="b8ede-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8ede-221">0x00000010</span></span>                                           |
| <span data-ttu-id="b8ede-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8ede-222">Classes used in</span></span>        | [<span data-ttu-id="b8ede-223">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="b8ede-223">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b8ede-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8ede-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b8ede-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8ede-225">Entry</span></span> | <span data-ttu-id="b8ede-226">Valor</span><span class="sxs-lookup"><span data-stu-id="b8ede-226">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b8ede-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8ede-227">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b8ede-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8ede-228">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b8ede-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8ede-229">System-Only</span></span>            | <span data-ttu-id="b8ede-230">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ede-230">False</span></span>                                                |
| <span data-ttu-id="b8ede-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8ede-231">Is-Single-Valued</span></span>       | <span data-ttu-id="b8ede-232">True</span><span class="sxs-lookup"><span data-stu-id="b8ede-232">True</span></span>                                                 |
| <span data-ttu-id="b8ede-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8ede-233">Is Indexed</span></span>             | <span data-ttu-id="b8ede-234">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ede-234">False</span></span>                                                |
| <span data-ttu-id="b8ede-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8ede-235">In Global Catalog</span></span>      | <span data-ttu-id="b8ede-236">True</span><span class="sxs-lookup"><span data-stu-id="b8ede-236">True</span></span>                                                 |
| <span data-ttu-id="b8ede-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8ede-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8ede-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8ede-238">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b8ede-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8ede-239">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b8ede-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8ede-240">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b8ede-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ede-241">Search-Flags</span></span>           | <span data-ttu-id="b8ede-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8ede-242">0x00000000</span></span>                                           |
| <span data-ttu-id="b8ede-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ede-243">System-Flags</span></span>           | <span data-ttu-id="b8ede-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8ede-244">0x00000010</span></span>                                           |
| <span data-ttu-id="b8ede-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8ede-245">Classes used in</span></span>        | [<span data-ttu-id="b8ede-246">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="b8ede-246">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b8ede-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b8ede-247">Windows Server 2012</span></span>



| <span data-ttu-id="b8ede-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8ede-248">Entry</span></span> | <span data-ttu-id="b8ede-249">Valor</span><span class="sxs-lookup"><span data-stu-id="b8ede-249">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b8ede-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8ede-250">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b8ede-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8ede-251">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b8ede-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8ede-252">System-Only</span></span>            | <span data-ttu-id="b8ede-253">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ede-253">False</span></span>                                                |
| <span data-ttu-id="b8ede-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8ede-254">Is-Single-Valued</span></span>       | <span data-ttu-id="b8ede-255">True</span><span class="sxs-lookup"><span data-stu-id="b8ede-255">True</span></span>                                                 |
| <span data-ttu-id="b8ede-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8ede-256">Is Indexed</span></span>             | <span data-ttu-id="b8ede-257">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ede-257">False</span></span>                                                |
| <span data-ttu-id="b8ede-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8ede-258">In Global Catalog</span></span>      | <span data-ttu-id="b8ede-259">True</span><span class="sxs-lookup"><span data-stu-id="b8ede-259">True</span></span>                                                 |
| <span data-ttu-id="b8ede-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8ede-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8ede-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8ede-261">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b8ede-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8ede-262">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b8ede-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8ede-263">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b8ede-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ede-264">Search-Flags</span></span>           | <span data-ttu-id="b8ede-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8ede-265">0x00000000</span></span>                                           |
| <span data-ttu-id="b8ede-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ede-266">System-Flags</span></span>           | <span data-ttu-id="b8ede-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8ede-267">0x00000010</span></span>                                           |
| <span data-ttu-id="b8ede-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8ede-268">Classes used in</span></span>        | [<span data-ttu-id="b8ede-269">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="b8ede-269">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





