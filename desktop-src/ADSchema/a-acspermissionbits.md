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
# <a name="acs-permission-bits-attribute"></a><span data-ttu-id="18950-105">ACS-atributo de permissão-bits</span><span class="sxs-lookup"><span data-stu-id="18950-105">ACS-Permission-Bits attribute</span></span>

<span data-ttu-id="18950-106">Permite a origem do fluxo de multicast para um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="18950-106">Allows multicast flow origination for a given user.</span></span>



| <span data-ttu-id="18950-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="18950-107">Entry</span></span> | <span data-ttu-id="18950-108">Valor</span><span class="sxs-lookup"><span data-stu-id="18950-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="18950-109">CN</span><span class="sxs-lookup"><span data-stu-id="18950-109">CN</span></span>                | <span data-ttu-id="18950-110">ACS-permissão-bits</span><span class="sxs-lookup"><span data-stu-id="18950-110">ACS-Permission-Bits</span></span>                  |
| <span data-ttu-id="18950-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="18950-111">Ldap-Display-Name</span></span> | <span data-ttu-id="18950-112">aCSPermissionBits</span><span class="sxs-lookup"><span data-stu-id="18950-112">aCSPermissionBits</span></span>                    |
| <span data-ttu-id="18950-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="18950-113">Size</span></span>              | <span data-ttu-id="18950-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="18950-114">8 bytes</span></span>                              |
| <span data-ttu-id="18950-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="18950-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="18950-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="18950-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="18950-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="18950-117">Attribute-Id</span></span>      | <span data-ttu-id="18950-118">1.2.840.113556.1.4.765</span><span class="sxs-lookup"><span data-stu-id="18950-118">1.2.840.113556.1.4.765</span></span>               |
| <span data-ttu-id="18950-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="18950-119">System-Id-Guid</span></span>    | <span data-ttu-id="18950-120">7f561282-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="18950-120">7f561282-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="18950-121">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18950-121">Syntax</span></span>            | [<span data-ttu-id="18950-122">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="18950-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="18950-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="18950-123">Implementations</span></span>

-   [<span data-ttu-id="18950-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="18950-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="18950-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="18950-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="18950-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="18950-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="18950-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="18950-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="18950-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="18950-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="18950-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="18950-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="18950-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="18950-130">Windows 2000 Server</span></span>



| <span data-ttu-id="18950-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="18950-131">Entry</span></span> | <span data-ttu-id="18950-132">Valor</span><span class="sxs-lookup"><span data-stu-id="18950-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="18950-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="18950-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="18950-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18950-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="18950-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="18950-135">System-Only</span></span>            | <span data-ttu-id="18950-136">Falso</span><span class="sxs-lookup"><span data-stu-id="18950-136">False</span></span>                                        |
| <span data-ttu-id="18950-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="18950-137">Is-Single-Valued</span></span>       | <span data-ttu-id="18950-138">True</span><span class="sxs-lookup"><span data-stu-id="18950-138">True</span></span>                                         |
| <span data-ttu-id="18950-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="18950-139">Is Indexed</span></span>             | <span data-ttu-id="18950-140">Falso</span><span class="sxs-lookup"><span data-stu-id="18950-140">False</span></span>                                        |
| <span data-ttu-id="18950-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="18950-141">In Global Catalog</span></span>      | <span data-ttu-id="18950-142">Falso</span><span class="sxs-lookup"><span data-stu-id="18950-142">False</span></span>                                        |
| <span data-ttu-id="18950-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="18950-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="18950-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="18950-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="18950-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18950-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="18950-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18950-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="18950-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18950-147">Search-Flags</span></span>           | <span data-ttu-id="18950-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18950-148">0x00000000</span></span>                                   |
| <span data-ttu-id="18950-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18950-149">System-Flags</span></span>           | <span data-ttu-id="18950-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18950-150">0x00000010</span></span>                                   |
| <span data-ttu-id="18950-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="18950-151">Classes used in</span></span>        | [<span data-ttu-id="18950-152">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="18950-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="18950-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="18950-153">Windows Server 2003</span></span>



| <span data-ttu-id="18950-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="18950-154">Entry</span></span> | <span data-ttu-id="18950-155">Valor</span><span class="sxs-lookup"><span data-stu-id="18950-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="18950-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="18950-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="18950-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18950-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="18950-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="18950-158">System-Only</span></span>            | <span data-ttu-id="18950-159">Falso</span><span class="sxs-lookup"><span data-stu-id="18950-159">False</span></span>                                        |
| <span data-ttu-id="18950-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="18950-160">Is-Single-Valued</span></span>       | <span data-ttu-id="18950-161">True</span><span class="sxs-lookup"><span data-stu-id="18950-161">True</span></span>                                         |
| <span data-ttu-id="18950-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="18950-162">Is Indexed</span></span>             | <span data-ttu-id="18950-163">Falso</span><span class="sxs-lookup"><span data-stu-id="18950-163">False</span></span>                                        |
| <span data-ttu-id="18950-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="18950-164">In Global Catalog</span></span>      | <span data-ttu-id="18950-165">Falso</span><span class="sxs-lookup"><span data-stu-id="18950-165">False</span></span>                                        |
| <span data-ttu-id="18950-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="18950-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="18950-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="18950-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="18950-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18950-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="18950-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18950-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="18950-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18950-170">Search-Flags</span></span>           | <span data-ttu-id="18950-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18950-171">0x00000000</span></span>                                   |
| <span data-ttu-id="18950-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18950-172">System-Flags</span></span>           | <span data-ttu-id="18950-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18950-173">0x00000010</span></span>                                   |
| <span data-ttu-id="18950-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="18950-174">Classes used in</span></span>        | [<span data-ttu-id="18950-175">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="18950-175">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="18950-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="18950-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="18950-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="18950-177">Entry</span></span> | <span data-ttu-id="18950-178">Valor</span><span class="sxs-lookup"><span data-stu-id="18950-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="18950-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="18950-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="18950-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18950-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="18950-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="18950-181">System-Only</span></span>            | <span data-ttu-id="18950-182">Falso</span><span class="sxs-lookup"><span data-stu-id="18950-182">False</span></span>                                        |
| <span data-ttu-id="18950-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="18950-183">Is-Single-Valued</span></span>       | <span data-ttu-id="18950-184">True</span><span class="sxs-lookup"><span data-stu-id="18950-184">True</span></span>                                         |
| <span data-ttu-id="18950-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="18950-185">Is Indexed</span></span>             | <span data-ttu-id="18950-186">Falso</span><span class="sxs-lookup"><span data-stu-id="18950-186">False</span></span>                                        |
| <span data-ttu-id="18950-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="18950-187">In Global Catalog</span></span>      | <span data-ttu-id="18950-188">Falso</span><span class="sxs-lookup"><span data-stu-id="18950-188">False</span></span>                                        |
| <span data-ttu-id="18950-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="18950-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="18950-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="18950-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="18950-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18950-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="18950-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18950-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="18950-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18950-193">Search-Flags</span></span>           | <span data-ttu-id="18950-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18950-194">0x00000000</span></span>                                   |
| <span data-ttu-id="18950-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18950-195">System-Flags</span></span>           | <span data-ttu-id="18950-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18950-196">0x00000010</span></span>                                   |
| <span data-ttu-id="18950-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="18950-197">Classes used in</span></span>        | [<span data-ttu-id="18950-198">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="18950-198">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="18950-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18950-199">Windows Server 2008</span></span>



| <span data-ttu-id="18950-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="18950-200">Entry</span></span> | <span data-ttu-id="18950-201">Valor</span><span class="sxs-lookup"><span data-stu-id="18950-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="18950-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="18950-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="18950-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18950-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="18950-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="18950-204">System-Only</span></span>            | <span data-ttu-id="18950-205">Falso</span><span class="sxs-lookup"><span data-stu-id="18950-205">False</span></span>                                        |
| <span data-ttu-id="18950-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="18950-206">Is-Single-Valued</span></span>       | <span data-ttu-id="18950-207">True</span><span class="sxs-lookup"><span data-stu-id="18950-207">True</span></span>                                         |
| <span data-ttu-id="18950-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="18950-208">Is Indexed</span></span>             | <span data-ttu-id="18950-209">Falso</span><span class="sxs-lookup"><span data-stu-id="18950-209">False</span></span>                                        |
| <span data-ttu-id="18950-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="18950-210">In Global Catalog</span></span>      | <span data-ttu-id="18950-211">Falso</span><span class="sxs-lookup"><span data-stu-id="18950-211">False</span></span>                                        |
| <span data-ttu-id="18950-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="18950-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="18950-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="18950-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="18950-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18950-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="18950-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18950-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="18950-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18950-216">Search-Flags</span></span>           | <span data-ttu-id="18950-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18950-217">0x00000000</span></span>                                   |
| <span data-ttu-id="18950-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18950-218">System-Flags</span></span>           | <span data-ttu-id="18950-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18950-219">0x00000010</span></span>                                   |
| <span data-ttu-id="18950-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="18950-220">Classes used in</span></span>        | [<span data-ttu-id="18950-221">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="18950-221">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="18950-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="18950-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="18950-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="18950-223">Entry</span></span> | <span data-ttu-id="18950-224">Valor</span><span class="sxs-lookup"><span data-stu-id="18950-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="18950-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="18950-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="18950-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18950-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="18950-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="18950-227">System-Only</span></span>            | <span data-ttu-id="18950-228">Falso</span><span class="sxs-lookup"><span data-stu-id="18950-228">False</span></span>                                        |
| <span data-ttu-id="18950-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="18950-229">Is-Single-Valued</span></span>       | <span data-ttu-id="18950-230">True</span><span class="sxs-lookup"><span data-stu-id="18950-230">True</span></span>                                         |
| <span data-ttu-id="18950-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="18950-231">Is Indexed</span></span>             | <span data-ttu-id="18950-232">Falso</span><span class="sxs-lookup"><span data-stu-id="18950-232">False</span></span>                                        |
| <span data-ttu-id="18950-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="18950-233">In Global Catalog</span></span>      | <span data-ttu-id="18950-234">Falso</span><span class="sxs-lookup"><span data-stu-id="18950-234">False</span></span>                                        |
| <span data-ttu-id="18950-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="18950-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="18950-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="18950-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="18950-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18950-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="18950-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18950-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="18950-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18950-239">Search-Flags</span></span>           | <span data-ttu-id="18950-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18950-240">0x00000000</span></span>                                   |
| <span data-ttu-id="18950-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18950-241">System-Flags</span></span>           | <span data-ttu-id="18950-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18950-242">0x00000010</span></span>                                   |
| <span data-ttu-id="18950-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="18950-243">Classes used in</span></span>        | [<span data-ttu-id="18950-244">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="18950-244">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="18950-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="18950-245">Windows Server 2012</span></span>



| <span data-ttu-id="18950-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="18950-246">Entry</span></span> | <span data-ttu-id="18950-247">Valor</span><span class="sxs-lookup"><span data-stu-id="18950-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="18950-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="18950-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="18950-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18950-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="18950-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="18950-250">System-Only</span></span>            | <span data-ttu-id="18950-251">Falso</span><span class="sxs-lookup"><span data-stu-id="18950-251">False</span></span>                                        |
| <span data-ttu-id="18950-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="18950-252">Is-Single-Valued</span></span>       | <span data-ttu-id="18950-253">True</span><span class="sxs-lookup"><span data-stu-id="18950-253">True</span></span>                                         |
| <span data-ttu-id="18950-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="18950-254">Is Indexed</span></span>             | <span data-ttu-id="18950-255">Falso</span><span class="sxs-lookup"><span data-stu-id="18950-255">False</span></span>                                        |
| <span data-ttu-id="18950-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="18950-256">In Global Catalog</span></span>      | <span data-ttu-id="18950-257">Falso</span><span class="sxs-lookup"><span data-stu-id="18950-257">False</span></span>                                        |
| <span data-ttu-id="18950-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="18950-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="18950-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="18950-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="18950-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18950-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="18950-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18950-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="18950-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18950-262">Search-Flags</span></span>           | <span data-ttu-id="18950-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18950-263">0x00000000</span></span>                                   |
| <span data-ttu-id="18950-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18950-264">System-Flags</span></span>           | <span data-ttu-id="18950-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18950-265">0x00000010</span></span>                                   |
| <span data-ttu-id="18950-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="18950-266">Classes used in</span></span>        | [<span data-ttu-id="18950-267">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="18950-267">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





