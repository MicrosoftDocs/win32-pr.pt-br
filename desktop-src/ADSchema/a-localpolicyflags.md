---
title: Atributo local-sinalizadores de política
description: Sinalizadores que determinam onde um computador obtém sua política. Referência de política local.
ms.assetid: 1f2fa723-507a-4e27-a325-8bd6f6cb6bd6
ms.tgt_platform: multiple
keywords:
- Atributo local-de-política-sinalizadores-esquema do AD
- Esquema de AD do atributo localPolicyFlags
topic_type:
- apiref
api_name:
- Local-Policy-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc077fe793a523b41974280ada7e54b82335d733
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105811227"
---
# <a name="local-policy-flags-attribute"></a><span data-ttu-id="df268-106">Atributo local-sinalizadores de política</span><span class="sxs-lookup"><span data-stu-id="df268-106">Local-Policy-Flags attribute</span></span>

<span data-ttu-id="df268-107">Sinalizadores que determinam onde um computador obtém sua política.</span><span class="sxs-lookup"><span data-stu-id="df268-107">Flags that determine where a computer gets its policy.</span></span> <span data-ttu-id="df268-108">Referência de política local.</span><span class="sxs-lookup"><span data-stu-id="df268-108">Local-Policy-Reference.</span></span>



| <span data-ttu-id="df268-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="df268-109">Entry</span></span> | <span data-ttu-id="df268-110">Valor</span><span class="sxs-lookup"><span data-stu-id="df268-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="df268-111">CN</span><span class="sxs-lookup"><span data-stu-id="df268-111">CN</span></span>                | <span data-ttu-id="df268-112">Sinalizadores de política local</span><span class="sxs-lookup"><span data-stu-id="df268-112">Local-Policy-Flags</span></span>                   |
| <span data-ttu-id="df268-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="df268-113">Ldap-Display-Name</span></span> | <span data-ttu-id="df268-114">localPolicyFlags</span><span class="sxs-lookup"><span data-stu-id="df268-114">localPolicyFlags</span></span>                     |
| <span data-ttu-id="df268-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="df268-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="df268-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="df268-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="df268-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="df268-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="df268-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="df268-118">Attribute-Id</span></span>      | <span data-ttu-id="df268-119">1.2.840.113556.1.4.56</span><span class="sxs-lookup"><span data-stu-id="df268-119">1.2.840.113556.1.4.56</span></span>                |
| <span data-ttu-id="df268-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="df268-120">System-Id-Guid</span></span>    | <span data-ttu-id="df268-121">bf96799e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="df268-121">bf96799e-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="df268-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="df268-122">Syntax</span></span>            | [<span data-ttu-id="df268-123">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="df268-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="df268-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="df268-124">Implementations</span></span>

-   [<span data-ttu-id="df268-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="df268-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="df268-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="df268-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="df268-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="df268-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="df268-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="df268-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="df268-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="df268-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="df268-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="df268-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="df268-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="df268-131">Windows 2000 Server</span></span>



| <span data-ttu-id="df268-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="df268-132">Entry</span></span> | <span data-ttu-id="df268-133">Valor</span><span class="sxs-lookup"><span data-stu-id="df268-133">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="df268-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="df268-134">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="df268-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df268-135">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="df268-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="df268-136">System-Only</span></span>            | <span data-ttu-id="df268-137">Falso</span><span class="sxs-lookup"><span data-stu-id="df268-137">False</span></span>                                     |
| <span data-ttu-id="df268-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="df268-138">Is-Single-Valued</span></span>       | <span data-ttu-id="df268-139">True</span><span class="sxs-lookup"><span data-stu-id="df268-139">True</span></span>                                      |
| <span data-ttu-id="df268-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="df268-140">Is Indexed</span></span>             | <span data-ttu-id="df268-141">Falso</span><span class="sxs-lookup"><span data-stu-id="df268-141">False</span></span>                                     |
| <span data-ttu-id="df268-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="df268-142">In Global Catalog</span></span>      | <span data-ttu-id="df268-143">Falso</span><span class="sxs-lookup"><span data-stu-id="df268-143">False</span></span>                                     |
| <span data-ttu-id="df268-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df268-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="df268-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="df268-145">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="df268-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df268-146">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="df268-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df268-147">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="df268-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df268-148">Search-Flags</span></span>           | <span data-ttu-id="df268-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df268-149">0x00000000</span></span>                                |
| <span data-ttu-id="df268-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df268-150">System-Flags</span></span>           | <span data-ttu-id="df268-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df268-151">0x00000010</span></span>                                |
| <span data-ttu-id="df268-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="df268-152">Classes used in</span></span>        | [<span data-ttu-id="df268-153">**Computador**</span><span class="sxs-lookup"><span data-stu-id="df268-153">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="df268-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="df268-154">Windows Server 2003</span></span>



| <span data-ttu-id="df268-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="df268-155">Entry</span></span> | <span data-ttu-id="df268-156">Valor</span><span class="sxs-lookup"><span data-stu-id="df268-156">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="df268-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="df268-157">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="df268-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df268-158">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="df268-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="df268-159">System-Only</span></span>            | <span data-ttu-id="df268-160">Falso</span><span class="sxs-lookup"><span data-stu-id="df268-160">False</span></span>                                     |
| <span data-ttu-id="df268-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="df268-161">Is-Single-Valued</span></span>       | <span data-ttu-id="df268-162">True</span><span class="sxs-lookup"><span data-stu-id="df268-162">True</span></span>                                      |
| <span data-ttu-id="df268-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="df268-163">Is Indexed</span></span>             | <span data-ttu-id="df268-164">Falso</span><span class="sxs-lookup"><span data-stu-id="df268-164">False</span></span>                                     |
| <span data-ttu-id="df268-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="df268-165">In Global Catalog</span></span>      | <span data-ttu-id="df268-166">Falso</span><span class="sxs-lookup"><span data-stu-id="df268-166">False</span></span>                                     |
| <span data-ttu-id="df268-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df268-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="df268-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="df268-168">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="df268-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df268-169">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="df268-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df268-170">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="df268-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df268-171">Search-Flags</span></span>           | <span data-ttu-id="df268-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df268-172">0x00000000</span></span>                                |
| <span data-ttu-id="df268-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df268-173">System-Flags</span></span>           | <span data-ttu-id="df268-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df268-174">0x00000010</span></span>                                |
| <span data-ttu-id="df268-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="df268-175">Classes used in</span></span>        | [<span data-ttu-id="df268-176">**Computador**</span><span class="sxs-lookup"><span data-stu-id="df268-176">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="df268-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="df268-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="df268-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="df268-178">Entry</span></span> | <span data-ttu-id="df268-179">Valor</span><span class="sxs-lookup"><span data-stu-id="df268-179">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="df268-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="df268-180">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="df268-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df268-181">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="df268-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="df268-182">System-Only</span></span>            | <span data-ttu-id="df268-183">Falso</span><span class="sxs-lookup"><span data-stu-id="df268-183">False</span></span>                                     |
| <span data-ttu-id="df268-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="df268-184">Is-Single-Valued</span></span>       | <span data-ttu-id="df268-185">True</span><span class="sxs-lookup"><span data-stu-id="df268-185">True</span></span>                                      |
| <span data-ttu-id="df268-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="df268-186">Is Indexed</span></span>             | <span data-ttu-id="df268-187">Falso</span><span class="sxs-lookup"><span data-stu-id="df268-187">False</span></span>                                     |
| <span data-ttu-id="df268-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="df268-188">In Global Catalog</span></span>      | <span data-ttu-id="df268-189">Falso</span><span class="sxs-lookup"><span data-stu-id="df268-189">False</span></span>                                     |
| <span data-ttu-id="df268-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df268-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="df268-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="df268-191">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="df268-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df268-192">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="df268-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df268-193">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="df268-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df268-194">Search-Flags</span></span>           | <span data-ttu-id="df268-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df268-195">0x00000000</span></span>                                |
| <span data-ttu-id="df268-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df268-196">System-Flags</span></span>           | <span data-ttu-id="df268-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df268-197">0x00000010</span></span>                                |
| <span data-ttu-id="df268-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="df268-198">Classes used in</span></span>        | [<span data-ttu-id="df268-199">**Computador**</span><span class="sxs-lookup"><span data-stu-id="df268-199">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="df268-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df268-200">Windows Server 2008</span></span>



| <span data-ttu-id="df268-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="df268-201">Entry</span></span> | <span data-ttu-id="df268-202">Valor</span><span class="sxs-lookup"><span data-stu-id="df268-202">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="df268-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="df268-203">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="df268-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df268-204">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="df268-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="df268-205">System-Only</span></span>            | <span data-ttu-id="df268-206">Falso</span><span class="sxs-lookup"><span data-stu-id="df268-206">False</span></span>                                     |
| <span data-ttu-id="df268-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="df268-207">Is-Single-Valued</span></span>       | <span data-ttu-id="df268-208">True</span><span class="sxs-lookup"><span data-stu-id="df268-208">True</span></span>                                      |
| <span data-ttu-id="df268-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="df268-209">Is Indexed</span></span>             | <span data-ttu-id="df268-210">Falso</span><span class="sxs-lookup"><span data-stu-id="df268-210">False</span></span>                                     |
| <span data-ttu-id="df268-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="df268-211">In Global Catalog</span></span>      | <span data-ttu-id="df268-212">Falso</span><span class="sxs-lookup"><span data-stu-id="df268-212">False</span></span>                                     |
| <span data-ttu-id="df268-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df268-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="df268-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="df268-214">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="df268-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df268-215">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="df268-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df268-216">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="df268-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df268-217">Search-Flags</span></span>           | <span data-ttu-id="df268-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df268-218">0x00000000</span></span>                                |
| <span data-ttu-id="df268-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df268-219">System-Flags</span></span>           | <span data-ttu-id="df268-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df268-220">0x00000010</span></span>                                |
| <span data-ttu-id="df268-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="df268-221">Classes used in</span></span>        | [<span data-ttu-id="df268-222">**Computador**</span><span class="sxs-lookup"><span data-stu-id="df268-222">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="df268-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="df268-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="df268-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="df268-224">Entry</span></span> | <span data-ttu-id="df268-225">Valor</span><span class="sxs-lookup"><span data-stu-id="df268-225">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="df268-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="df268-226">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="df268-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df268-227">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="df268-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="df268-228">System-Only</span></span>            | <span data-ttu-id="df268-229">Falso</span><span class="sxs-lookup"><span data-stu-id="df268-229">False</span></span>                                     |
| <span data-ttu-id="df268-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="df268-230">Is-Single-Valued</span></span>       | <span data-ttu-id="df268-231">True</span><span class="sxs-lookup"><span data-stu-id="df268-231">True</span></span>                                      |
| <span data-ttu-id="df268-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="df268-232">Is Indexed</span></span>             | <span data-ttu-id="df268-233">Falso</span><span class="sxs-lookup"><span data-stu-id="df268-233">False</span></span>                                     |
| <span data-ttu-id="df268-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="df268-234">In Global Catalog</span></span>      | <span data-ttu-id="df268-235">Falso</span><span class="sxs-lookup"><span data-stu-id="df268-235">False</span></span>                                     |
| <span data-ttu-id="df268-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df268-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="df268-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="df268-237">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="df268-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df268-238">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="df268-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df268-239">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="df268-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df268-240">Search-Flags</span></span>           | <span data-ttu-id="df268-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df268-241">0x00000000</span></span>                                |
| <span data-ttu-id="df268-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df268-242">System-Flags</span></span>           | <span data-ttu-id="df268-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df268-243">0x00000010</span></span>                                |
| <span data-ttu-id="df268-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="df268-244">Classes used in</span></span>        | [<span data-ttu-id="df268-245">**Computador**</span><span class="sxs-lookup"><span data-stu-id="df268-245">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="df268-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="df268-246">Windows Server 2012</span></span>



| <span data-ttu-id="df268-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="df268-247">Entry</span></span> | <span data-ttu-id="df268-248">Valor</span><span class="sxs-lookup"><span data-stu-id="df268-248">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="df268-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="df268-249">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="df268-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df268-250">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="df268-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="df268-251">System-Only</span></span>            | <span data-ttu-id="df268-252">Falso</span><span class="sxs-lookup"><span data-stu-id="df268-252">False</span></span>                                     |
| <span data-ttu-id="df268-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="df268-253">Is-Single-Valued</span></span>       | <span data-ttu-id="df268-254">True</span><span class="sxs-lookup"><span data-stu-id="df268-254">True</span></span>                                      |
| <span data-ttu-id="df268-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="df268-255">Is Indexed</span></span>             | <span data-ttu-id="df268-256">Falso</span><span class="sxs-lookup"><span data-stu-id="df268-256">False</span></span>                                     |
| <span data-ttu-id="df268-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="df268-257">In Global Catalog</span></span>      | <span data-ttu-id="df268-258">Falso</span><span class="sxs-lookup"><span data-stu-id="df268-258">False</span></span>                                     |
| <span data-ttu-id="df268-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df268-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="df268-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="df268-260">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="df268-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df268-261">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="df268-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df268-262">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="df268-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df268-263">Search-Flags</span></span>           | <span data-ttu-id="df268-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df268-264">0x00000000</span></span>                                |
| <span data-ttu-id="df268-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df268-265">System-Flags</span></span>           | <span data-ttu-id="df268-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df268-266">0x00000010</span></span>                                |
| <span data-ttu-id="df268-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="df268-267">Classes used in</span></span>        | [<span data-ttu-id="df268-268">**Computador**</span><span class="sxs-lookup"><span data-stu-id="df268-268">**Computer**</span></span>](c-computer.md)<br/> |



 

 





