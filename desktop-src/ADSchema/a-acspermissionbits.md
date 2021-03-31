---
title: ACS-atributo de permissão-bits
description: Permite a origem do fluxo de multicast para um determinado usuário.
ms.assetid: c7e7866d-b906-4a64-bd51-4e9cc7b8fb86
ms.tgt_platform: multiple
keywords:
- ACS-Permission-bits-esquema de atributo do AD
- Esquema de AD do atributo aCSPermissionBits
topic_type:
- apiref
api_name:
- ACS-Permission-Bits
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a27370178dd46fd50df44b1226686db5a70a846
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086770"
---
# <a name="acs-permission-bits-attribute"></a><span data-ttu-id="e6ed3-105">ACS-atributo de permissão-bits</span><span class="sxs-lookup"><span data-stu-id="e6ed3-105">ACS-Permission-Bits attribute</span></span>

<span data-ttu-id="e6ed3-106">Permite a origem do fluxo de multicast para um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="e6ed3-106">Allows multicast flow origination for a given user.</span></span>



| <span data-ttu-id="e6ed3-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6ed3-107">Entry</span></span> | <span data-ttu-id="e6ed3-108">Valor</span><span class="sxs-lookup"><span data-stu-id="e6ed3-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e6ed3-109">CN</span><span class="sxs-lookup"><span data-stu-id="e6ed3-109">CN</span></span>                | <span data-ttu-id="e6ed3-110">ACS-permissão-bits</span><span class="sxs-lookup"><span data-stu-id="e6ed3-110">ACS-Permission-Bits</span></span>                  |
| <span data-ttu-id="e6ed3-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e6ed3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e6ed3-112">aCSPermissionBits</span><span class="sxs-lookup"><span data-stu-id="e6ed3-112">aCSPermissionBits</span></span>                    |
| <span data-ttu-id="e6ed3-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="e6ed3-113">Size</span></span>              | <span data-ttu-id="e6ed3-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="e6ed3-114">8 bytes</span></span>                              |
| <span data-ttu-id="e6ed3-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="e6ed3-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e6ed3-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="e6ed3-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e6ed3-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e6ed3-117">Attribute-Id</span></span>      | <span data-ttu-id="e6ed3-118">1.2.840.113556.1.4.765</span><span class="sxs-lookup"><span data-stu-id="e6ed3-118">1.2.840.113556.1.4.765</span></span>               |
| <span data-ttu-id="e6ed3-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e6ed3-119">System-Id-Guid</span></span>    | <span data-ttu-id="e6ed3-120">7f561282-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e6ed3-120">7f561282-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="e6ed3-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6ed3-121">Syntax</span></span>            | [<span data-ttu-id="e6ed3-122">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="e6ed3-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="e6ed3-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="e6ed3-123">Implementations</span></span>

-   [<span data-ttu-id="e6ed3-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e6ed3-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e6ed3-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e6ed3-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e6ed3-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e6ed3-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e6ed3-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e6ed3-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e6ed3-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e6ed3-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e6ed3-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e6ed3-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e6ed3-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e6ed3-130">Windows 2000 Server</span></span>



| <span data-ttu-id="e6ed3-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6ed3-131">Entry</span></span> | <span data-ttu-id="e6ed3-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e6ed3-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e6ed3-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="e6ed3-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ed3-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6ed3-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ed3-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6ed3-135">System-Only</span></span>            | <span data-ttu-id="e6ed3-136">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ed3-136">False</span></span>                                        |
| <span data-ttu-id="e6ed3-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e6ed3-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e6ed3-138">True</span><span class="sxs-lookup"><span data-stu-id="e6ed3-138">True</span></span>                                         |
| <span data-ttu-id="e6ed3-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="e6ed3-139">Is Indexed</span></span>             | <span data-ttu-id="e6ed3-140">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ed3-140">False</span></span>                                        |
| <span data-ttu-id="e6ed3-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e6ed3-141">In Global Catalog</span></span>      | <span data-ttu-id="e6ed3-142">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ed3-142">False</span></span>                                        |
| <span data-ttu-id="e6ed3-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e6ed3-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6ed3-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e6ed3-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e6ed3-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6ed3-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e6ed3-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6ed3-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e6ed3-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ed3-147">Search-Flags</span></span>           | <span data-ttu-id="e6ed3-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6ed3-148">0x00000000</span></span>                                   |
| <span data-ttu-id="e6ed3-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ed3-149">System-Flags</span></span>           | <span data-ttu-id="e6ed3-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6ed3-150">0x00000010</span></span>                                   |
| <span data-ttu-id="e6ed3-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e6ed3-151">Classes used in</span></span>        | [<span data-ttu-id="e6ed3-152">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="e6ed3-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e6ed3-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e6ed3-153">Windows Server 2003</span></span>



| <span data-ttu-id="e6ed3-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6ed3-154">Entry</span></span> | <span data-ttu-id="e6ed3-155">Valor</span><span class="sxs-lookup"><span data-stu-id="e6ed3-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e6ed3-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="e6ed3-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ed3-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6ed3-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ed3-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6ed3-158">System-Only</span></span>            | <span data-ttu-id="e6ed3-159">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ed3-159">False</span></span>                                        |
| <span data-ttu-id="e6ed3-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e6ed3-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e6ed3-161">True</span><span class="sxs-lookup"><span data-stu-id="e6ed3-161">True</span></span>                                         |
| <span data-ttu-id="e6ed3-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="e6ed3-162">Is Indexed</span></span>             | <span data-ttu-id="e6ed3-163">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ed3-163">False</span></span>                                        |
| <span data-ttu-id="e6ed3-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e6ed3-164">In Global Catalog</span></span>      | <span data-ttu-id="e6ed3-165">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ed3-165">False</span></span>                                        |
| <span data-ttu-id="e6ed3-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e6ed3-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6ed3-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e6ed3-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e6ed3-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6ed3-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e6ed3-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6ed3-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e6ed3-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ed3-170">Search-Flags</span></span>           | <span data-ttu-id="e6ed3-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6ed3-171">0x00000000</span></span>                                   |
| <span data-ttu-id="e6ed3-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ed3-172">System-Flags</span></span>           | <span data-ttu-id="e6ed3-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6ed3-173">0x00000010</span></span>                                   |
| <span data-ttu-id="e6ed3-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e6ed3-174">Classes used in</span></span>        | [<span data-ttu-id="e6ed3-175">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="e6ed3-175">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e6ed3-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e6ed3-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e6ed3-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6ed3-177">Entry</span></span> | <span data-ttu-id="e6ed3-178">Valor</span><span class="sxs-lookup"><span data-stu-id="e6ed3-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e6ed3-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="e6ed3-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ed3-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6ed3-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ed3-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6ed3-181">System-Only</span></span>            | <span data-ttu-id="e6ed3-182">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ed3-182">False</span></span>                                        |
| <span data-ttu-id="e6ed3-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e6ed3-183">Is-Single-Valued</span></span>       | <span data-ttu-id="e6ed3-184">True</span><span class="sxs-lookup"><span data-stu-id="e6ed3-184">True</span></span>                                         |
| <span data-ttu-id="e6ed3-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="e6ed3-185">Is Indexed</span></span>             | <span data-ttu-id="e6ed3-186">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ed3-186">False</span></span>                                        |
| <span data-ttu-id="e6ed3-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e6ed3-187">In Global Catalog</span></span>      | <span data-ttu-id="e6ed3-188">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ed3-188">False</span></span>                                        |
| <span data-ttu-id="e6ed3-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e6ed3-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6ed3-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e6ed3-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e6ed3-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6ed3-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e6ed3-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6ed3-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e6ed3-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ed3-193">Search-Flags</span></span>           | <span data-ttu-id="e6ed3-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6ed3-194">0x00000000</span></span>                                   |
| <span data-ttu-id="e6ed3-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ed3-195">System-Flags</span></span>           | <span data-ttu-id="e6ed3-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6ed3-196">0x00000010</span></span>                                   |
| <span data-ttu-id="e6ed3-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e6ed3-197">Classes used in</span></span>        | [<span data-ttu-id="e6ed3-198">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="e6ed3-198">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e6ed3-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6ed3-199">Windows Server 2008</span></span>



| <span data-ttu-id="e6ed3-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6ed3-200">Entry</span></span> | <span data-ttu-id="e6ed3-201">Valor</span><span class="sxs-lookup"><span data-stu-id="e6ed3-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e6ed3-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="e6ed3-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ed3-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6ed3-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ed3-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6ed3-204">System-Only</span></span>            | <span data-ttu-id="e6ed3-205">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ed3-205">False</span></span>                                        |
| <span data-ttu-id="e6ed3-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e6ed3-206">Is-Single-Valued</span></span>       | <span data-ttu-id="e6ed3-207">True</span><span class="sxs-lookup"><span data-stu-id="e6ed3-207">True</span></span>                                         |
| <span data-ttu-id="e6ed3-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="e6ed3-208">Is Indexed</span></span>             | <span data-ttu-id="e6ed3-209">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ed3-209">False</span></span>                                        |
| <span data-ttu-id="e6ed3-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e6ed3-210">In Global Catalog</span></span>      | <span data-ttu-id="e6ed3-211">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ed3-211">False</span></span>                                        |
| <span data-ttu-id="e6ed3-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e6ed3-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6ed3-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e6ed3-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e6ed3-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6ed3-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e6ed3-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6ed3-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e6ed3-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ed3-216">Search-Flags</span></span>           | <span data-ttu-id="e6ed3-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6ed3-217">0x00000000</span></span>                                   |
| <span data-ttu-id="e6ed3-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ed3-218">System-Flags</span></span>           | <span data-ttu-id="e6ed3-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6ed3-219">0x00000010</span></span>                                   |
| <span data-ttu-id="e6ed3-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e6ed3-220">Classes used in</span></span>        | [<span data-ttu-id="e6ed3-221">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="e6ed3-221">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e6ed3-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e6ed3-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e6ed3-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6ed3-223">Entry</span></span> | <span data-ttu-id="e6ed3-224">Valor</span><span class="sxs-lookup"><span data-stu-id="e6ed3-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e6ed3-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="e6ed3-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ed3-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6ed3-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ed3-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6ed3-227">System-Only</span></span>            | <span data-ttu-id="e6ed3-228">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ed3-228">False</span></span>                                        |
| <span data-ttu-id="e6ed3-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e6ed3-229">Is-Single-Valued</span></span>       | <span data-ttu-id="e6ed3-230">True</span><span class="sxs-lookup"><span data-stu-id="e6ed3-230">True</span></span>                                         |
| <span data-ttu-id="e6ed3-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="e6ed3-231">Is Indexed</span></span>             | <span data-ttu-id="e6ed3-232">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ed3-232">False</span></span>                                        |
| <span data-ttu-id="e6ed3-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e6ed3-233">In Global Catalog</span></span>      | <span data-ttu-id="e6ed3-234">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ed3-234">False</span></span>                                        |
| <span data-ttu-id="e6ed3-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e6ed3-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6ed3-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e6ed3-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e6ed3-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6ed3-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e6ed3-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6ed3-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e6ed3-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ed3-239">Search-Flags</span></span>           | <span data-ttu-id="e6ed3-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6ed3-240">0x00000000</span></span>                                   |
| <span data-ttu-id="e6ed3-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ed3-241">System-Flags</span></span>           | <span data-ttu-id="e6ed3-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6ed3-242">0x00000010</span></span>                                   |
| <span data-ttu-id="e6ed3-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e6ed3-243">Classes used in</span></span>        | [<span data-ttu-id="e6ed3-244">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="e6ed3-244">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e6ed3-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e6ed3-245">Windows Server 2012</span></span>



| <span data-ttu-id="e6ed3-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="e6ed3-246">Entry</span></span> | <span data-ttu-id="e6ed3-247">Valor</span><span class="sxs-lookup"><span data-stu-id="e6ed3-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e6ed3-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="e6ed3-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ed3-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6ed3-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e6ed3-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6ed3-250">System-Only</span></span>            | <span data-ttu-id="e6ed3-251">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ed3-251">False</span></span>                                        |
| <span data-ttu-id="e6ed3-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e6ed3-252">Is-Single-Valued</span></span>       | <span data-ttu-id="e6ed3-253">True</span><span class="sxs-lookup"><span data-stu-id="e6ed3-253">True</span></span>                                         |
| <span data-ttu-id="e6ed3-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="e6ed3-254">Is Indexed</span></span>             | <span data-ttu-id="e6ed3-255">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ed3-255">False</span></span>                                        |
| <span data-ttu-id="e6ed3-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e6ed3-256">In Global Catalog</span></span>      | <span data-ttu-id="e6ed3-257">Falso</span><span class="sxs-lookup"><span data-stu-id="e6ed3-257">False</span></span>                                        |
| <span data-ttu-id="e6ed3-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e6ed3-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6ed3-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e6ed3-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e6ed3-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6ed3-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e6ed3-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6ed3-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e6ed3-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ed3-262">Search-Flags</span></span>           | <span data-ttu-id="e6ed3-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6ed3-263">0x00000000</span></span>                                   |
| <span data-ttu-id="e6ed3-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6ed3-264">System-Flags</span></span>           | <span data-ttu-id="e6ed3-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6ed3-265">0x00000010</span></span>                                   |
| <span data-ttu-id="e6ed3-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e6ed3-266">Classes used in</span></span>        | [<span data-ttu-id="e6ed3-267">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="e6ed3-267">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





