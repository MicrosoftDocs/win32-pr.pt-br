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
# <a name="acs-permission-bits-attribute"></a><span data-ttu-id="28d1c-105">ACS-atributo de permissão-bits</span><span class="sxs-lookup"><span data-stu-id="28d1c-105">ACS-Permission-Bits attribute</span></span>

<span data-ttu-id="28d1c-106">Permite a origem do fluxo de multicast para um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="28d1c-106">Allows multicast flow origination for a given user.</span></span>



| <span data-ttu-id="28d1c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="28d1c-107">Entry</span></span> | <span data-ttu-id="28d1c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="28d1c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="28d1c-109">CN</span><span class="sxs-lookup"><span data-stu-id="28d1c-109">CN</span></span>                | <span data-ttu-id="28d1c-110">ACS-permissão-bits</span><span class="sxs-lookup"><span data-stu-id="28d1c-110">ACS-Permission-Bits</span></span>                  |
| <span data-ttu-id="28d1c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="28d1c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="28d1c-112">aCSPermissionBits</span><span class="sxs-lookup"><span data-stu-id="28d1c-112">aCSPermissionBits</span></span>                    |
| <span data-ttu-id="28d1c-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="28d1c-113">Size</span></span>              | <span data-ttu-id="28d1c-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="28d1c-114">8 bytes</span></span>                              |
| <span data-ttu-id="28d1c-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="28d1c-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="28d1c-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="28d1c-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="28d1c-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="28d1c-117">Attribute-Id</span></span>      | <span data-ttu-id="28d1c-118">1.2.840.113556.1.4.765</span><span class="sxs-lookup"><span data-stu-id="28d1c-118">1.2.840.113556.1.4.765</span></span>               |
| <span data-ttu-id="28d1c-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="28d1c-119">System-Id-Guid</span></span>    | <span data-ttu-id="28d1c-120">7f561282-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="28d1c-120">7f561282-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="28d1c-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="28d1c-121">Syntax</span></span>            | [<span data-ttu-id="28d1c-122">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="28d1c-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="28d1c-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="28d1c-123">Implementations</span></span>

-   [<span data-ttu-id="28d1c-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="28d1c-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="28d1c-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="28d1c-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="28d1c-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="28d1c-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="28d1c-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="28d1c-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="28d1c-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="28d1c-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="28d1c-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="28d1c-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="28d1c-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28d1c-130">Windows 2000 Server</span></span>



| <span data-ttu-id="28d1c-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="28d1c-131">Entry</span></span> | <span data-ttu-id="28d1c-132">Valor</span><span class="sxs-lookup"><span data-stu-id="28d1c-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="28d1c-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="28d1c-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="28d1c-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28d1c-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="28d1c-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="28d1c-135">System-Only</span></span>            | <span data-ttu-id="28d1c-136">Falso</span><span class="sxs-lookup"><span data-stu-id="28d1c-136">False</span></span>                                        |
| <span data-ttu-id="28d1c-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="28d1c-137">Is-Single-Valued</span></span>       | <span data-ttu-id="28d1c-138">True</span><span class="sxs-lookup"><span data-stu-id="28d1c-138">True</span></span>                                         |
| <span data-ttu-id="28d1c-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="28d1c-139">Is Indexed</span></span>             | <span data-ttu-id="28d1c-140">Falso</span><span class="sxs-lookup"><span data-stu-id="28d1c-140">False</span></span>                                        |
| <span data-ttu-id="28d1c-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="28d1c-141">In Global Catalog</span></span>      | <span data-ttu-id="28d1c-142">Falso</span><span class="sxs-lookup"><span data-stu-id="28d1c-142">False</span></span>                                        |
| <span data-ttu-id="28d1c-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="28d1c-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="28d1c-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="28d1c-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="28d1c-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28d1c-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="28d1c-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28d1c-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="28d1c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28d1c-147">Search-Flags</span></span>           | <span data-ttu-id="28d1c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28d1c-148">0x00000000</span></span>                                   |
| <span data-ttu-id="28d1c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28d1c-149">System-Flags</span></span>           | <span data-ttu-id="28d1c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28d1c-150">0x00000010</span></span>                                   |
| <span data-ttu-id="28d1c-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="28d1c-151">Classes used in</span></span>        | [<span data-ttu-id="28d1c-152">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="28d1c-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="28d1c-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="28d1c-153">Windows Server 2003</span></span>



| <span data-ttu-id="28d1c-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="28d1c-154">Entry</span></span> | <span data-ttu-id="28d1c-155">Valor</span><span class="sxs-lookup"><span data-stu-id="28d1c-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="28d1c-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="28d1c-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="28d1c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28d1c-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="28d1c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="28d1c-158">System-Only</span></span>            | <span data-ttu-id="28d1c-159">Falso</span><span class="sxs-lookup"><span data-stu-id="28d1c-159">False</span></span>                                        |
| <span data-ttu-id="28d1c-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="28d1c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="28d1c-161">True</span><span class="sxs-lookup"><span data-stu-id="28d1c-161">True</span></span>                                         |
| <span data-ttu-id="28d1c-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="28d1c-162">Is Indexed</span></span>             | <span data-ttu-id="28d1c-163">Falso</span><span class="sxs-lookup"><span data-stu-id="28d1c-163">False</span></span>                                        |
| <span data-ttu-id="28d1c-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="28d1c-164">In Global Catalog</span></span>      | <span data-ttu-id="28d1c-165">Falso</span><span class="sxs-lookup"><span data-stu-id="28d1c-165">False</span></span>                                        |
| <span data-ttu-id="28d1c-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="28d1c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="28d1c-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="28d1c-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="28d1c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28d1c-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="28d1c-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28d1c-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="28d1c-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28d1c-170">Search-Flags</span></span>           | <span data-ttu-id="28d1c-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28d1c-171">0x00000000</span></span>                                   |
| <span data-ttu-id="28d1c-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28d1c-172">System-Flags</span></span>           | <span data-ttu-id="28d1c-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28d1c-173">0x00000010</span></span>                                   |
| <span data-ttu-id="28d1c-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="28d1c-174">Classes used in</span></span>        | [<span data-ttu-id="28d1c-175">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="28d1c-175">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="28d1c-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="28d1c-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="28d1c-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="28d1c-177">Entry</span></span> | <span data-ttu-id="28d1c-178">Valor</span><span class="sxs-lookup"><span data-stu-id="28d1c-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="28d1c-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="28d1c-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="28d1c-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28d1c-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="28d1c-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="28d1c-181">System-Only</span></span>            | <span data-ttu-id="28d1c-182">Falso</span><span class="sxs-lookup"><span data-stu-id="28d1c-182">False</span></span>                                        |
| <span data-ttu-id="28d1c-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="28d1c-183">Is-Single-Valued</span></span>       | <span data-ttu-id="28d1c-184">True</span><span class="sxs-lookup"><span data-stu-id="28d1c-184">True</span></span>                                         |
| <span data-ttu-id="28d1c-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="28d1c-185">Is Indexed</span></span>             | <span data-ttu-id="28d1c-186">Falso</span><span class="sxs-lookup"><span data-stu-id="28d1c-186">False</span></span>                                        |
| <span data-ttu-id="28d1c-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="28d1c-187">In Global Catalog</span></span>      | <span data-ttu-id="28d1c-188">Falso</span><span class="sxs-lookup"><span data-stu-id="28d1c-188">False</span></span>                                        |
| <span data-ttu-id="28d1c-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="28d1c-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="28d1c-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="28d1c-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="28d1c-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28d1c-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="28d1c-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28d1c-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="28d1c-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28d1c-193">Search-Flags</span></span>           | <span data-ttu-id="28d1c-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28d1c-194">0x00000000</span></span>                                   |
| <span data-ttu-id="28d1c-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28d1c-195">System-Flags</span></span>           | <span data-ttu-id="28d1c-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28d1c-196">0x00000010</span></span>                                   |
| <span data-ttu-id="28d1c-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="28d1c-197">Classes used in</span></span>        | [<span data-ttu-id="28d1c-198">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="28d1c-198">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="28d1c-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28d1c-199">Windows Server 2008</span></span>



| <span data-ttu-id="28d1c-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="28d1c-200">Entry</span></span> | <span data-ttu-id="28d1c-201">Valor</span><span class="sxs-lookup"><span data-stu-id="28d1c-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="28d1c-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="28d1c-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="28d1c-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28d1c-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="28d1c-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="28d1c-204">System-Only</span></span>            | <span data-ttu-id="28d1c-205">Falso</span><span class="sxs-lookup"><span data-stu-id="28d1c-205">False</span></span>                                        |
| <span data-ttu-id="28d1c-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="28d1c-206">Is-Single-Valued</span></span>       | <span data-ttu-id="28d1c-207">True</span><span class="sxs-lookup"><span data-stu-id="28d1c-207">True</span></span>                                         |
| <span data-ttu-id="28d1c-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="28d1c-208">Is Indexed</span></span>             | <span data-ttu-id="28d1c-209">Falso</span><span class="sxs-lookup"><span data-stu-id="28d1c-209">False</span></span>                                        |
| <span data-ttu-id="28d1c-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="28d1c-210">In Global Catalog</span></span>      | <span data-ttu-id="28d1c-211">Falso</span><span class="sxs-lookup"><span data-stu-id="28d1c-211">False</span></span>                                        |
| <span data-ttu-id="28d1c-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="28d1c-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="28d1c-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="28d1c-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="28d1c-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28d1c-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="28d1c-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28d1c-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="28d1c-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28d1c-216">Search-Flags</span></span>           | <span data-ttu-id="28d1c-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28d1c-217">0x00000000</span></span>                                   |
| <span data-ttu-id="28d1c-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28d1c-218">System-Flags</span></span>           | <span data-ttu-id="28d1c-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28d1c-219">0x00000010</span></span>                                   |
| <span data-ttu-id="28d1c-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="28d1c-220">Classes used in</span></span>        | [<span data-ttu-id="28d1c-221">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="28d1c-221">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="28d1c-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="28d1c-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="28d1c-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="28d1c-223">Entry</span></span> | <span data-ttu-id="28d1c-224">Valor</span><span class="sxs-lookup"><span data-stu-id="28d1c-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="28d1c-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="28d1c-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="28d1c-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28d1c-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="28d1c-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="28d1c-227">System-Only</span></span>            | <span data-ttu-id="28d1c-228">Falso</span><span class="sxs-lookup"><span data-stu-id="28d1c-228">False</span></span>                                        |
| <span data-ttu-id="28d1c-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="28d1c-229">Is-Single-Valued</span></span>       | <span data-ttu-id="28d1c-230">True</span><span class="sxs-lookup"><span data-stu-id="28d1c-230">True</span></span>                                         |
| <span data-ttu-id="28d1c-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="28d1c-231">Is Indexed</span></span>             | <span data-ttu-id="28d1c-232">Falso</span><span class="sxs-lookup"><span data-stu-id="28d1c-232">False</span></span>                                        |
| <span data-ttu-id="28d1c-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="28d1c-233">In Global Catalog</span></span>      | <span data-ttu-id="28d1c-234">Falso</span><span class="sxs-lookup"><span data-stu-id="28d1c-234">False</span></span>                                        |
| <span data-ttu-id="28d1c-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="28d1c-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="28d1c-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="28d1c-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="28d1c-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28d1c-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="28d1c-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28d1c-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="28d1c-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28d1c-239">Search-Flags</span></span>           | <span data-ttu-id="28d1c-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28d1c-240">0x00000000</span></span>                                   |
| <span data-ttu-id="28d1c-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28d1c-241">System-Flags</span></span>           | <span data-ttu-id="28d1c-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28d1c-242">0x00000010</span></span>                                   |
| <span data-ttu-id="28d1c-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="28d1c-243">Classes used in</span></span>        | [<span data-ttu-id="28d1c-244">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="28d1c-244">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="28d1c-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="28d1c-245">Windows Server 2012</span></span>



| <span data-ttu-id="28d1c-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="28d1c-246">Entry</span></span> | <span data-ttu-id="28d1c-247">Valor</span><span class="sxs-lookup"><span data-stu-id="28d1c-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="28d1c-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="28d1c-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="28d1c-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28d1c-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="28d1c-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="28d1c-250">System-Only</span></span>            | <span data-ttu-id="28d1c-251">Falso</span><span class="sxs-lookup"><span data-stu-id="28d1c-251">False</span></span>                                        |
| <span data-ttu-id="28d1c-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="28d1c-252">Is-Single-Valued</span></span>       | <span data-ttu-id="28d1c-253">True</span><span class="sxs-lookup"><span data-stu-id="28d1c-253">True</span></span>                                         |
| <span data-ttu-id="28d1c-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="28d1c-254">Is Indexed</span></span>             | <span data-ttu-id="28d1c-255">Falso</span><span class="sxs-lookup"><span data-stu-id="28d1c-255">False</span></span>                                        |
| <span data-ttu-id="28d1c-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="28d1c-256">In Global Catalog</span></span>      | <span data-ttu-id="28d1c-257">Falso</span><span class="sxs-lookup"><span data-stu-id="28d1c-257">False</span></span>                                        |
| <span data-ttu-id="28d1c-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="28d1c-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="28d1c-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="28d1c-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="28d1c-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28d1c-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="28d1c-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28d1c-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="28d1c-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28d1c-262">Search-Flags</span></span>           | <span data-ttu-id="28d1c-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28d1c-263">0x00000000</span></span>                                   |
| <span data-ttu-id="28d1c-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28d1c-264">System-Flags</span></span>           | <span data-ttu-id="28d1c-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28d1c-265">0x00000010</span></span>                                   |
| <span data-ttu-id="28d1c-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="28d1c-266">Classes used in</span></span>        | [<span data-ttu-id="28d1c-267">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="28d1c-267">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





