---
title: Trust-Type atributo
description: O tipo de confiança, por exemplo, Windows NT ou MIT.
ms.assetid: ad3640cd-d634-4ec1-8be8-1fb8272e4b23
ms.tgt_platform: multiple
keywords:
- Esquema de Trust-Type do atributo AD
- Esquema de AD do atributo TrustType
topic_type:
- apiref
api_name:
- Trust-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b8a8f59f7df976f968bb4f2915e667a06e95bb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919418"
---
# <a name="trust-type-attribute"></a><span data-ttu-id="0f4eb-105">Trust-Type atributo</span><span class="sxs-lookup"><span data-stu-id="0f4eb-105">Trust-Type attribute</span></span>

<span data-ttu-id="0f4eb-106">O tipo de confiança, por exemplo, Windows NT ou MIT.</span><span class="sxs-lookup"><span data-stu-id="0f4eb-106">The type of trust, for example, Windows NT or MIT.</span></span>



| <span data-ttu-id="0f4eb-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f4eb-107">Entry</span></span> | <span data-ttu-id="0f4eb-108">Valor</span><span class="sxs-lookup"><span data-stu-id="0f4eb-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0f4eb-109">CN</span><span class="sxs-lookup"><span data-stu-id="0f4eb-109">CN</span></span>                | <span data-ttu-id="0f4eb-110">Trust-Type</span><span class="sxs-lookup"><span data-stu-id="0f4eb-110">Trust-Type</span></span>                           |
| <span data-ttu-id="0f4eb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0f4eb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0f4eb-112">TrustType</span><span class="sxs-lookup"><span data-stu-id="0f4eb-112">trustType</span></span>                            |
| <span data-ttu-id="0f4eb-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="0f4eb-113">Size</span></span>              | <span data-ttu-id="0f4eb-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="0f4eb-114">4 bytes</span></span>                              |
| <span data-ttu-id="0f4eb-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="0f4eb-115">Update Privilege</span></span>  | <span data-ttu-id="0f4eb-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="0f4eb-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="0f4eb-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="0f4eb-117">Update Frequency</span></span>  | <span data-ttu-id="0f4eb-118">Quando uma nova relação de confiança é criada.</span><span class="sxs-lookup"><span data-stu-id="0f4eb-118">When a new trust is created.</span></span>         |
| <span data-ttu-id="0f4eb-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0f4eb-119">Attribute-Id</span></span>      | <span data-ttu-id="0f4eb-120">1.2.840.113556.1.4.136</span><span class="sxs-lookup"><span data-stu-id="0f4eb-120">1.2.840.113556.1.4.136</span></span>               |
| <span data-ttu-id="0f4eb-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0f4eb-121">System-Id-Guid</span></span>    | <span data-ttu-id="0f4eb-122">bf967a60-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0f4eb-122">bf967a60-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="0f4eb-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f4eb-123">Syntax</span></span>            | [<span data-ttu-id="0f4eb-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="0f4eb-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="0f4eb-125">Implementations</span></span>

-   [<span data-ttu-id="0f4eb-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0f4eb-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0f4eb-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0f4eb-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0f4eb-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0f4eb-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0f4eb-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0f4eb-132">Windows 2000 Server</span></span>



| <span data-ttu-id="0f4eb-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f4eb-133">Entry</span></span> | <span data-ttu-id="0f4eb-134">Valor</span><span class="sxs-lookup"><span data-stu-id="0f4eb-134">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0f4eb-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="0f4eb-135">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0f4eb-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f4eb-136">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0f4eb-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f4eb-137">System-Only</span></span>            | <span data-ttu-id="0f4eb-138">Falso</span><span class="sxs-lookup"><span data-stu-id="0f4eb-138">False</span></span>                                                |
| <span data-ttu-id="0f4eb-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0f4eb-139">Is-Single-Valued</span></span>       | <span data-ttu-id="0f4eb-140">True</span><span class="sxs-lookup"><span data-stu-id="0f4eb-140">True</span></span>                                                 |
| <span data-ttu-id="0f4eb-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="0f4eb-141">Is Indexed</span></span>             | <span data-ttu-id="0f4eb-142">Falso</span><span class="sxs-lookup"><span data-stu-id="0f4eb-142">False</span></span>                                                |
| <span data-ttu-id="0f4eb-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0f4eb-143">In Global Catalog</span></span>      | <span data-ttu-id="0f4eb-144">Falso</span><span class="sxs-lookup"><span data-stu-id="0f4eb-144">False</span></span>                                                |
| <span data-ttu-id="0f4eb-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f4eb-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f4eb-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0f4eb-146">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0f4eb-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f4eb-147">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0f4eb-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f4eb-148">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0f4eb-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f4eb-149">Search-Flags</span></span>           | <span data-ttu-id="0f4eb-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f4eb-150">0x00000000</span></span>                                           |
| <span data-ttu-id="0f4eb-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f4eb-151">System-Flags</span></span>           | <span data-ttu-id="0f4eb-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f4eb-152">0x00000010</span></span>                                           |
| <span data-ttu-id="0f4eb-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0f4eb-153">Classes used in</span></span>        | [<span data-ttu-id="0f4eb-154">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-154">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0f4eb-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0f4eb-155">Windows Server 2003</span></span>



| <span data-ttu-id="0f4eb-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f4eb-156">Entry</span></span> | <span data-ttu-id="0f4eb-157">Valor</span><span class="sxs-lookup"><span data-stu-id="0f4eb-157">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0f4eb-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="0f4eb-158">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0f4eb-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f4eb-159">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0f4eb-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f4eb-160">System-Only</span></span>            | <span data-ttu-id="0f4eb-161">Falso</span><span class="sxs-lookup"><span data-stu-id="0f4eb-161">False</span></span>                                                |
| <span data-ttu-id="0f4eb-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0f4eb-162">Is-Single-Valued</span></span>       | <span data-ttu-id="0f4eb-163">True</span><span class="sxs-lookup"><span data-stu-id="0f4eb-163">True</span></span>                                                 |
| <span data-ttu-id="0f4eb-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="0f4eb-164">Is Indexed</span></span>             | <span data-ttu-id="0f4eb-165">Falso</span><span class="sxs-lookup"><span data-stu-id="0f4eb-165">False</span></span>                                                |
| <span data-ttu-id="0f4eb-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0f4eb-166">In Global Catalog</span></span>      | <span data-ttu-id="0f4eb-167">True</span><span class="sxs-lookup"><span data-stu-id="0f4eb-167">True</span></span>                                                 |
| <span data-ttu-id="0f4eb-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f4eb-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f4eb-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0f4eb-169">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0f4eb-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f4eb-170">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0f4eb-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f4eb-171">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0f4eb-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f4eb-172">Search-Flags</span></span>           | <span data-ttu-id="0f4eb-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f4eb-173">0x00000000</span></span>                                           |
| <span data-ttu-id="0f4eb-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f4eb-174">System-Flags</span></span>           | <span data-ttu-id="0f4eb-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f4eb-175">0x00000010</span></span>                                           |
| <span data-ttu-id="0f4eb-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0f4eb-176">Classes used in</span></span>        | [<span data-ttu-id="0f4eb-177">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-177">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0f4eb-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0f4eb-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0f4eb-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f4eb-179">Entry</span></span> | <span data-ttu-id="0f4eb-180">Valor</span><span class="sxs-lookup"><span data-stu-id="0f4eb-180">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0f4eb-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="0f4eb-181">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0f4eb-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f4eb-182">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0f4eb-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f4eb-183">System-Only</span></span>            | <span data-ttu-id="0f4eb-184">Falso</span><span class="sxs-lookup"><span data-stu-id="0f4eb-184">False</span></span>                                                |
| <span data-ttu-id="0f4eb-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0f4eb-185">Is-Single-Valued</span></span>       | <span data-ttu-id="0f4eb-186">True</span><span class="sxs-lookup"><span data-stu-id="0f4eb-186">True</span></span>                                                 |
| <span data-ttu-id="0f4eb-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="0f4eb-187">Is Indexed</span></span>             | <span data-ttu-id="0f4eb-188">Falso</span><span class="sxs-lookup"><span data-stu-id="0f4eb-188">False</span></span>                                                |
| <span data-ttu-id="0f4eb-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0f4eb-189">In Global Catalog</span></span>      | <span data-ttu-id="0f4eb-190">True</span><span class="sxs-lookup"><span data-stu-id="0f4eb-190">True</span></span>                                                 |
| <span data-ttu-id="0f4eb-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f4eb-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f4eb-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0f4eb-192">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0f4eb-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f4eb-193">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0f4eb-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f4eb-194">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0f4eb-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f4eb-195">Search-Flags</span></span>           | <span data-ttu-id="0f4eb-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f4eb-196">0x00000000</span></span>                                           |
| <span data-ttu-id="0f4eb-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f4eb-197">System-Flags</span></span>           | <span data-ttu-id="0f4eb-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f4eb-198">0x00000010</span></span>                                           |
| <span data-ttu-id="0f4eb-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0f4eb-199">Classes used in</span></span>        | [<span data-ttu-id="0f4eb-200">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0f4eb-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f4eb-201">Windows Server 2008</span></span>



| <span data-ttu-id="0f4eb-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f4eb-202">Entry</span></span> | <span data-ttu-id="0f4eb-203">Valor</span><span class="sxs-lookup"><span data-stu-id="0f4eb-203">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0f4eb-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="0f4eb-204">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0f4eb-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f4eb-205">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0f4eb-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f4eb-206">System-Only</span></span>            | <span data-ttu-id="0f4eb-207">Falso</span><span class="sxs-lookup"><span data-stu-id="0f4eb-207">False</span></span>                                                |
| <span data-ttu-id="0f4eb-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0f4eb-208">Is-Single-Valued</span></span>       | <span data-ttu-id="0f4eb-209">True</span><span class="sxs-lookup"><span data-stu-id="0f4eb-209">True</span></span>                                                 |
| <span data-ttu-id="0f4eb-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="0f4eb-210">Is Indexed</span></span>             | <span data-ttu-id="0f4eb-211">Falso</span><span class="sxs-lookup"><span data-stu-id="0f4eb-211">False</span></span>                                                |
| <span data-ttu-id="0f4eb-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0f4eb-212">In Global Catalog</span></span>      | <span data-ttu-id="0f4eb-213">True</span><span class="sxs-lookup"><span data-stu-id="0f4eb-213">True</span></span>                                                 |
| <span data-ttu-id="0f4eb-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f4eb-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f4eb-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0f4eb-215">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0f4eb-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f4eb-216">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0f4eb-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f4eb-217">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0f4eb-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f4eb-218">Search-Flags</span></span>           | <span data-ttu-id="0f4eb-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f4eb-219">0x00000000</span></span>                                           |
| <span data-ttu-id="0f4eb-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f4eb-220">System-Flags</span></span>           | <span data-ttu-id="0f4eb-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f4eb-221">0x00000010</span></span>                                           |
| <span data-ttu-id="0f4eb-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0f4eb-222">Classes used in</span></span>        | [<span data-ttu-id="0f4eb-223">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-223">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0f4eb-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0f4eb-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0f4eb-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f4eb-225">Entry</span></span> | <span data-ttu-id="0f4eb-226">Valor</span><span class="sxs-lookup"><span data-stu-id="0f4eb-226">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0f4eb-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="0f4eb-227">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0f4eb-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f4eb-228">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0f4eb-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f4eb-229">System-Only</span></span>            | <span data-ttu-id="0f4eb-230">Falso</span><span class="sxs-lookup"><span data-stu-id="0f4eb-230">False</span></span>                                                |
| <span data-ttu-id="0f4eb-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0f4eb-231">Is-Single-Valued</span></span>       | <span data-ttu-id="0f4eb-232">True</span><span class="sxs-lookup"><span data-stu-id="0f4eb-232">True</span></span>                                                 |
| <span data-ttu-id="0f4eb-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="0f4eb-233">Is Indexed</span></span>             | <span data-ttu-id="0f4eb-234">Falso</span><span class="sxs-lookup"><span data-stu-id="0f4eb-234">False</span></span>                                                |
| <span data-ttu-id="0f4eb-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0f4eb-235">In Global Catalog</span></span>      | <span data-ttu-id="0f4eb-236">True</span><span class="sxs-lookup"><span data-stu-id="0f4eb-236">True</span></span>                                                 |
| <span data-ttu-id="0f4eb-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f4eb-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f4eb-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0f4eb-238">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0f4eb-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f4eb-239">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0f4eb-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f4eb-240">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0f4eb-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f4eb-241">Search-Flags</span></span>           | <span data-ttu-id="0f4eb-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f4eb-242">0x00000000</span></span>                                           |
| <span data-ttu-id="0f4eb-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f4eb-243">System-Flags</span></span>           | <span data-ttu-id="0f4eb-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f4eb-244">0x00000010</span></span>                                           |
| <span data-ttu-id="0f4eb-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0f4eb-245">Classes used in</span></span>        | [<span data-ttu-id="0f4eb-246">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-246">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0f4eb-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0f4eb-247">Windows Server 2012</span></span>



| <span data-ttu-id="0f4eb-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f4eb-248">Entry</span></span> | <span data-ttu-id="0f4eb-249">Valor</span><span class="sxs-lookup"><span data-stu-id="0f4eb-249">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="0f4eb-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="0f4eb-250">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0f4eb-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f4eb-251">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="0f4eb-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f4eb-252">System-Only</span></span>            | <span data-ttu-id="0f4eb-253">Falso</span><span class="sxs-lookup"><span data-stu-id="0f4eb-253">False</span></span>                                                |
| <span data-ttu-id="0f4eb-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0f4eb-254">Is-Single-Valued</span></span>       | <span data-ttu-id="0f4eb-255">True</span><span class="sxs-lookup"><span data-stu-id="0f4eb-255">True</span></span>                                                 |
| <span data-ttu-id="0f4eb-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="0f4eb-256">Is Indexed</span></span>             | <span data-ttu-id="0f4eb-257">Falso</span><span class="sxs-lookup"><span data-stu-id="0f4eb-257">False</span></span>                                                |
| <span data-ttu-id="0f4eb-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0f4eb-258">In Global Catalog</span></span>      | <span data-ttu-id="0f4eb-259">True</span><span class="sxs-lookup"><span data-stu-id="0f4eb-259">True</span></span>                                                 |
| <span data-ttu-id="0f4eb-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f4eb-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f4eb-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0f4eb-261">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="0f4eb-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f4eb-262">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="0f4eb-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f4eb-263">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="0f4eb-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f4eb-264">Search-Flags</span></span>           | <span data-ttu-id="0f4eb-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f4eb-265">0x00000000</span></span>                                           |
| <span data-ttu-id="0f4eb-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f4eb-266">System-Flags</span></span>           | <span data-ttu-id="0f4eb-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0f4eb-267">0x00000010</span></span>                                           |
| <span data-ttu-id="0f4eb-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0f4eb-268">Classes used in</span></span>        | [<span data-ttu-id="0f4eb-269">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-269">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





