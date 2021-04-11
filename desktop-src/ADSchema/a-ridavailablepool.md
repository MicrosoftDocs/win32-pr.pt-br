---
title: RID-disponível-atributo de pool
description: O espaço do qual os pools RID são alocados.
ms.assetid: abb6218f-def2-4a38-964f-3f0ee6c6f917
ms.tgt_platform: multiple
keywords:
- RID-disponível-esquema de AD do atributo de pool
- Esquema de AD do atributo rIDAvailablePool
topic_type:
- apiref
api_name:
- RID-Available-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59faf801b7f6f70e92c55a1d2a27857ed6ecb0c9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104163660"
---
# <a name="rid-available-pool-attribute"></a><span data-ttu-id="80918-105">RID-disponível-atributo de pool</span><span class="sxs-lookup"><span data-stu-id="80918-105">RID-Available-Pool attribute</span></span>

<span data-ttu-id="80918-106">O espaço do qual os pools RID são alocados.</span><span class="sxs-lookup"><span data-stu-id="80918-106">The space from which RID Pools are allocated.</span></span>



| <span data-ttu-id="80918-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="80918-107">Entry</span></span> | <span data-ttu-id="80918-108">Valor</span><span class="sxs-lookup"><span data-stu-id="80918-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="80918-109">CN</span><span class="sxs-lookup"><span data-stu-id="80918-109">CN</span></span>                | <span data-ttu-id="80918-110">RID-disponível-pool</span><span class="sxs-lookup"><span data-stu-id="80918-110">RID-Available-Pool</span></span>                   |
| <span data-ttu-id="80918-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="80918-111">Ldap-Display-Name</span></span> | <span data-ttu-id="80918-112">rIDAvailablePool</span><span class="sxs-lookup"><span data-stu-id="80918-112">rIDAvailablePool</span></span>                     |
| <span data-ttu-id="80918-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="80918-113">Size</span></span>              | <span data-ttu-id="80918-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="80918-114">8 bytes</span></span>                              |
| <span data-ttu-id="80918-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="80918-115">Update Privilege</span></span>  | <span data-ttu-id="80918-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="80918-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="80918-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="80918-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="80918-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="80918-118">Attribute-Id</span></span>      | <span data-ttu-id="80918-119">1.2.840.113556.1.4.370</span><span class="sxs-lookup"><span data-stu-id="80918-119">1.2.840.113556.1.4.370</span></span>               |
| <span data-ttu-id="80918-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="80918-120">System-Id-Guid</span></span>    | <span data-ttu-id="80918-121">66171888-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="80918-121">66171888-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="80918-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="80918-122">Syntax</span></span>            | [<span data-ttu-id="80918-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="80918-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="80918-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="80918-124">Implementations</span></span>

-   [<span data-ttu-id="80918-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="80918-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="80918-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="80918-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="80918-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="80918-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="80918-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="80918-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="80918-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="80918-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="80918-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="80918-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="80918-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="80918-131">Windows 2000 Server</span></span>



| <span data-ttu-id="80918-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="80918-132">Entry</span></span> | <span data-ttu-id="80918-133">Valor</span><span class="sxs-lookup"><span data-stu-id="80918-133">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="80918-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="80918-134">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="80918-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80918-135">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="80918-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="80918-136">System-Only</span></span>            | <span data-ttu-id="80918-137">Falso</span><span class="sxs-lookup"><span data-stu-id="80918-137">False</span></span>                                          |
| <span data-ttu-id="80918-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="80918-138">Is-Single-Valued</span></span>       | <span data-ttu-id="80918-139">True</span><span class="sxs-lookup"><span data-stu-id="80918-139">True</span></span>                                           |
| <span data-ttu-id="80918-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="80918-140">Is Indexed</span></span>             | <span data-ttu-id="80918-141">Falso</span><span class="sxs-lookup"><span data-stu-id="80918-141">False</span></span>                                          |
| <span data-ttu-id="80918-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="80918-142">In Global Catalog</span></span>      | <span data-ttu-id="80918-143">Falso</span><span class="sxs-lookup"><span data-stu-id="80918-143">False</span></span>                                          |
| <span data-ttu-id="80918-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="80918-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="80918-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="80918-145">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="80918-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80918-146">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="80918-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80918-147">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="80918-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80918-148">Search-Flags</span></span>           | <span data-ttu-id="80918-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80918-149">0x00000000</span></span>                                     |
| <span data-ttu-id="80918-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80918-150">System-Flags</span></span>           | <span data-ttu-id="80918-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80918-151">0x00000010</span></span>                                     |
| <span data-ttu-id="80918-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="80918-152">Classes used in</span></span>        | [<span data-ttu-id="80918-153">**Gerenciador de RID**</span><span class="sxs-lookup"><span data-stu-id="80918-153">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="80918-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="80918-154">Windows Server 2003</span></span>



| <span data-ttu-id="80918-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="80918-155">Entry</span></span> | <span data-ttu-id="80918-156">Valor</span><span class="sxs-lookup"><span data-stu-id="80918-156">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="80918-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="80918-157">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="80918-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80918-158">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="80918-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="80918-159">System-Only</span></span>            | <span data-ttu-id="80918-160">Falso</span><span class="sxs-lookup"><span data-stu-id="80918-160">False</span></span>                                          |
| <span data-ttu-id="80918-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="80918-161">Is-Single-Valued</span></span>       | <span data-ttu-id="80918-162">True</span><span class="sxs-lookup"><span data-stu-id="80918-162">True</span></span>                                           |
| <span data-ttu-id="80918-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="80918-163">Is Indexed</span></span>             | <span data-ttu-id="80918-164">Falso</span><span class="sxs-lookup"><span data-stu-id="80918-164">False</span></span>                                          |
| <span data-ttu-id="80918-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="80918-165">In Global Catalog</span></span>      | <span data-ttu-id="80918-166">Falso</span><span class="sxs-lookup"><span data-stu-id="80918-166">False</span></span>                                          |
| <span data-ttu-id="80918-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="80918-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="80918-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="80918-168">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="80918-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80918-169">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="80918-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80918-170">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="80918-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80918-171">Search-Flags</span></span>           | <span data-ttu-id="80918-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80918-172">0x00000000</span></span>                                     |
| <span data-ttu-id="80918-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80918-173">System-Flags</span></span>           | <span data-ttu-id="80918-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80918-174">0x00000010</span></span>                                     |
| <span data-ttu-id="80918-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="80918-175">Classes used in</span></span>        | [<span data-ttu-id="80918-176">**Gerenciador de RID**</span><span class="sxs-lookup"><span data-stu-id="80918-176">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="80918-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="80918-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="80918-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="80918-178">Entry</span></span> | <span data-ttu-id="80918-179">Valor</span><span class="sxs-lookup"><span data-stu-id="80918-179">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="80918-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="80918-180">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="80918-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80918-181">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="80918-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="80918-182">System-Only</span></span>            | <span data-ttu-id="80918-183">Falso</span><span class="sxs-lookup"><span data-stu-id="80918-183">False</span></span>                                          |
| <span data-ttu-id="80918-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="80918-184">Is-Single-Valued</span></span>       | <span data-ttu-id="80918-185">True</span><span class="sxs-lookup"><span data-stu-id="80918-185">True</span></span>                                           |
| <span data-ttu-id="80918-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="80918-186">Is Indexed</span></span>             | <span data-ttu-id="80918-187">Falso</span><span class="sxs-lookup"><span data-stu-id="80918-187">False</span></span>                                          |
| <span data-ttu-id="80918-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="80918-188">In Global Catalog</span></span>      | <span data-ttu-id="80918-189">Falso</span><span class="sxs-lookup"><span data-stu-id="80918-189">False</span></span>                                          |
| <span data-ttu-id="80918-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="80918-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="80918-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="80918-191">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="80918-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80918-192">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="80918-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80918-193">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="80918-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80918-194">Search-Flags</span></span>           | <span data-ttu-id="80918-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80918-195">0x00000000</span></span>                                     |
| <span data-ttu-id="80918-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80918-196">System-Flags</span></span>           | <span data-ttu-id="80918-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80918-197">0x00000010</span></span>                                     |
| <span data-ttu-id="80918-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="80918-198">Classes used in</span></span>        | [<span data-ttu-id="80918-199">**Gerenciador de RID**</span><span class="sxs-lookup"><span data-stu-id="80918-199">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="80918-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80918-200">Windows Server 2008</span></span>



| <span data-ttu-id="80918-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="80918-201">Entry</span></span> | <span data-ttu-id="80918-202">Valor</span><span class="sxs-lookup"><span data-stu-id="80918-202">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="80918-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="80918-203">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="80918-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80918-204">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="80918-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="80918-205">System-Only</span></span>            | <span data-ttu-id="80918-206">Falso</span><span class="sxs-lookup"><span data-stu-id="80918-206">False</span></span>                                          |
| <span data-ttu-id="80918-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="80918-207">Is-Single-Valued</span></span>       | <span data-ttu-id="80918-208">True</span><span class="sxs-lookup"><span data-stu-id="80918-208">True</span></span>                                           |
| <span data-ttu-id="80918-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="80918-209">Is Indexed</span></span>             | <span data-ttu-id="80918-210">Falso</span><span class="sxs-lookup"><span data-stu-id="80918-210">False</span></span>                                          |
| <span data-ttu-id="80918-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="80918-211">In Global Catalog</span></span>      | <span data-ttu-id="80918-212">Falso</span><span class="sxs-lookup"><span data-stu-id="80918-212">False</span></span>                                          |
| <span data-ttu-id="80918-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="80918-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="80918-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="80918-214">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="80918-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80918-215">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="80918-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80918-216">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="80918-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80918-217">Search-Flags</span></span>           | <span data-ttu-id="80918-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80918-218">0x00000000</span></span>                                     |
| <span data-ttu-id="80918-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80918-219">System-Flags</span></span>           | <span data-ttu-id="80918-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80918-220">0x00000010</span></span>                                     |
| <span data-ttu-id="80918-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="80918-221">Classes used in</span></span>        | [<span data-ttu-id="80918-222">**Gerenciador de RID**</span><span class="sxs-lookup"><span data-stu-id="80918-222">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="80918-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="80918-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="80918-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="80918-224">Entry</span></span> | <span data-ttu-id="80918-225">Valor</span><span class="sxs-lookup"><span data-stu-id="80918-225">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="80918-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="80918-226">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="80918-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80918-227">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="80918-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="80918-228">System-Only</span></span>            | <span data-ttu-id="80918-229">Falso</span><span class="sxs-lookup"><span data-stu-id="80918-229">False</span></span>                                          |
| <span data-ttu-id="80918-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="80918-230">Is-Single-Valued</span></span>       | <span data-ttu-id="80918-231">True</span><span class="sxs-lookup"><span data-stu-id="80918-231">True</span></span>                                           |
| <span data-ttu-id="80918-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="80918-232">Is Indexed</span></span>             | <span data-ttu-id="80918-233">Falso</span><span class="sxs-lookup"><span data-stu-id="80918-233">False</span></span>                                          |
| <span data-ttu-id="80918-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="80918-234">In Global Catalog</span></span>      | <span data-ttu-id="80918-235">Falso</span><span class="sxs-lookup"><span data-stu-id="80918-235">False</span></span>                                          |
| <span data-ttu-id="80918-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="80918-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="80918-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="80918-237">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="80918-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80918-238">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="80918-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80918-239">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="80918-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80918-240">Search-Flags</span></span>           | <span data-ttu-id="80918-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80918-241">0x00000000</span></span>                                     |
| <span data-ttu-id="80918-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80918-242">System-Flags</span></span>           | <span data-ttu-id="80918-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80918-243">0x00000010</span></span>                                     |
| <span data-ttu-id="80918-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="80918-244">Classes used in</span></span>        | [<span data-ttu-id="80918-245">**Gerenciador de RID**</span><span class="sxs-lookup"><span data-stu-id="80918-245">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="80918-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="80918-246">Windows Server 2012</span></span>



| <span data-ttu-id="80918-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="80918-247">Entry</span></span> | <span data-ttu-id="80918-248">Valor</span><span class="sxs-lookup"><span data-stu-id="80918-248">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="80918-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="80918-249">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="80918-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80918-250">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="80918-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="80918-251">System-Only</span></span>            | <span data-ttu-id="80918-252">Falso</span><span class="sxs-lookup"><span data-stu-id="80918-252">False</span></span>                                          |
| <span data-ttu-id="80918-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="80918-253">Is-Single-Valued</span></span>       | <span data-ttu-id="80918-254">True</span><span class="sxs-lookup"><span data-stu-id="80918-254">True</span></span>                                           |
| <span data-ttu-id="80918-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="80918-255">Is Indexed</span></span>             | <span data-ttu-id="80918-256">Falso</span><span class="sxs-lookup"><span data-stu-id="80918-256">False</span></span>                                          |
| <span data-ttu-id="80918-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="80918-257">In Global Catalog</span></span>      | <span data-ttu-id="80918-258">Falso</span><span class="sxs-lookup"><span data-stu-id="80918-258">False</span></span>                                          |
| <span data-ttu-id="80918-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="80918-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="80918-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="80918-260">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="80918-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80918-261">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="80918-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80918-262">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="80918-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80918-263">Search-Flags</span></span>           | <span data-ttu-id="80918-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80918-264">0x00000000</span></span>                                     |
| <span data-ttu-id="80918-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80918-265">System-Flags</span></span>           | <span data-ttu-id="80918-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80918-266">0x00000010</span></span>                                     |
| <span data-ttu-id="80918-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="80918-267">Classes used in</span></span>        | [<span data-ttu-id="80918-268">**Gerenciador de RID**</span><span class="sxs-lookup"><span data-stu-id="80918-268">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



 

 





