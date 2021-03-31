---
title: RID-usado-atributo de pool
description: Os pools RID que foram usados por um controlador de domínio.
ms.assetid: ca779461-5b8f-4ab2-b9cf-5f829889f10d
ms.tgt_platform: multiple
keywords:
- RID-usado-esquema de AD do atributo de pool
- Esquema de AD do atributo rIDUsedPool
topic_type:
- apiref
api_name:
- RID-Used-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84547d99b162da9da6e634a7c35eb9700e84e2a6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086853"
---
# <a name="rid-used-pool-attribute"></a><span data-ttu-id="bad9e-105">RID-usado-atributo de pool</span><span class="sxs-lookup"><span data-stu-id="bad9e-105">RID-Used-Pool attribute</span></span>

<span data-ttu-id="bad9e-106">Os pools RID que foram usados por um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="bad9e-106">The RID Pools that have been used by a DC.</span></span>



| <span data-ttu-id="bad9e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="bad9e-107">Entry</span></span> | <span data-ttu-id="bad9e-108">Valor</span><span class="sxs-lookup"><span data-stu-id="bad9e-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="bad9e-109">CN</span><span class="sxs-lookup"><span data-stu-id="bad9e-109">CN</span></span>                | <span data-ttu-id="bad9e-110">RID-usado-pool</span><span class="sxs-lookup"><span data-stu-id="bad9e-110">RID-Used-Pool</span></span>                        |
| <span data-ttu-id="bad9e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bad9e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bad9e-112">rIDUsedPool</span><span class="sxs-lookup"><span data-stu-id="bad9e-112">rIDUsedPool</span></span>                          |
| <span data-ttu-id="bad9e-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="bad9e-113">Size</span></span>              | <span data-ttu-id="bad9e-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="bad9e-114">8 bytes</span></span>                              |
| <span data-ttu-id="bad9e-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="bad9e-115">Update Privilege</span></span>  | <span data-ttu-id="bad9e-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="bad9e-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="bad9e-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="bad9e-117">Update Frequency</span></span>  | <span data-ttu-id="bad9e-118">Sempre que um pool RID é esvaziado.</span><span class="sxs-lookup"><span data-stu-id="bad9e-118">Whenever a RID pool is emptied.</span></span>      |
| <span data-ttu-id="bad9e-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bad9e-119">Attribute-Id</span></span>      | <span data-ttu-id="bad9e-120">1.2.840.113556.1.4.373</span><span class="sxs-lookup"><span data-stu-id="bad9e-120">1.2.840.113556.1.4.373</span></span>               |
| <span data-ttu-id="bad9e-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bad9e-121">System-Id-Guid</span></span>    | <span data-ttu-id="bad9e-122">6617188b-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="bad9e-122">6617188b-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="bad9e-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="bad9e-123">Syntax</span></span>            | [<span data-ttu-id="bad9e-124">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="bad9e-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="bad9e-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="bad9e-125">Implementations</span></span>

-   [<span data-ttu-id="bad9e-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bad9e-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bad9e-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bad9e-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bad9e-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bad9e-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bad9e-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bad9e-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bad9e-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bad9e-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bad9e-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bad9e-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bad9e-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bad9e-132">Windows 2000 Server</span></span>



| <span data-ttu-id="bad9e-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="bad9e-133">Entry</span></span> | <span data-ttu-id="bad9e-134">Valor</span><span class="sxs-lookup"><span data-stu-id="bad9e-134">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="bad9e-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="bad9e-135">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="bad9e-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bad9e-136">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="bad9e-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="bad9e-137">System-Only</span></span>            | <span data-ttu-id="bad9e-138">True</span><span class="sxs-lookup"><span data-stu-id="bad9e-138">True</span></span>                                   |
| <span data-ttu-id="bad9e-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bad9e-139">Is-Single-Valued</span></span>       | <span data-ttu-id="bad9e-140">True</span><span class="sxs-lookup"><span data-stu-id="bad9e-140">True</span></span>                                   |
| <span data-ttu-id="bad9e-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="bad9e-141">Is Indexed</span></span>             | <span data-ttu-id="bad9e-142">Falso</span><span class="sxs-lookup"><span data-stu-id="bad9e-142">False</span></span>                                  |
| <span data-ttu-id="bad9e-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bad9e-143">In Global Catalog</span></span>      | <span data-ttu-id="bad9e-144">Falso</span><span class="sxs-lookup"><span data-stu-id="bad9e-144">False</span></span>                                  |
| <span data-ttu-id="bad9e-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bad9e-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="bad9e-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bad9e-146">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="bad9e-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bad9e-147">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="bad9e-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bad9e-148">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="bad9e-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bad9e-149">Search-Flags</span></span>           | <span data-ttu-id="bad9e-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bad9e-150">0x00000000</span></span>                             |
| <span data-ttu-id="bad9e-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bad9e-151">System-Flags</span></span>           | <span data-ttu-id="bad9e-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bad9e-152">0x00000010</span></span>                             |
| <span data-ttu-id="bad9e-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bad9e-153">Classes used in</span></span>        | [<span data-ttu-id="bad9e-154">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="bad9e-154">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bad9e-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bad9e-155">Windows Server 2003</span></span>



| <span data-ttu-id="bad9e-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="bad9e-156">Entry</span></span> | <span data-ttu-id="bad9e-157">Valor</span><span class="sxs-lookup"><span data-stu-id="bad9e-157">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="bad9e-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="bad9e-158">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="bad9e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bad9e-159">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="bad9e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="bad9e-160">System-Only</span></span>            | <span data-ttu-id="bad9e-161">True</span><span class="sxs-lookup"><span data-stu-id="bad9e-161">True</span></span>                                   |
| <span data-ttu-id="bad9e-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bad9e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="bad9e-163">True</span><span class="sxs-lookup"><span data-stu-id="bad9e-163">True</span></span>                                   |
| <span data-ttu-id="bad9e-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="bad9e-164">Is Indexed</span></span>             | <span data-ttu-id="bad9e-165">Falso</span><span class="sxs-lookup"><span data-stu-id="bad9e-165">False</span></span>                                  |
| <span data-ttu-id="bad9e-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bad9e-166">In Global Catalog</span></span>      | <span data-ttu-id="bad9e-167">Falso</span><span class="sxs-lookup"><span data-stu-id="bad9e-167">False</span></span>                                  |
| <span data-ttu-id="bad9e-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bad9e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="bad9e-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bad9e-169">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="bad9e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bad9e-170">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="bad9e-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bad9e-171">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="bad9e-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bad9e-172">Search-Flags</span></span>           | <span data-ttu-id="bad9e-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bad9e-173">0x00000000</span></span>                             |
| <span data-ttu-id="bad9e-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bad9e-174">System-Flags</span></span>           | <span data-ttu-id="bad9e-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bad9e-175">0x00000010</span></span>                             |
| <span data-ttu-id="bad9e-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bad9e-176">Classes used in</span></span>        | [<span data-ttu-id="bad9e-177">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="bad9e-177">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bad9e-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bad9e-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bad9e-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="bad9e-179">Entry</span></span> | <span data-ttu-id="bad9e-180">Valor</span><span class="sxs-lookup"><span data-stu-id="bad9e-180">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="bad9e-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="bad9e-181">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="bad9e-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bad9e-182">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="bad9e-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="bad9e-183">System-Only</span></span>            | <span data-ttu-id="bad9e-184">True</span><span class="sxs-lookup"><span data-stu-id="bad9e-184">True</span></span>                                   |
| <span data-ttu-id="bad9e-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bad9e-185">Is-Single-Valued</span></span>       | <span data-ttu-id="bad9e-186">True</span><span class="sxs-lookup"><span data-stu-id="bad9e-186">True</span></span>                                   |
| <span data-ttu-id="bad9e-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="bad9e-187">Is Indexed</span></span>             | <span data-ttu-id="bad9e-188">Falso</span><span class="sxs-lookup"><span data-stu-id="bad9e-188">False</span></span>                                  |
| <span data-ttu-id="bad9e-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bad9e-189">In Global Catalog</span></span>      | <span data-ttu-id="bad9e-190">Falso</span><span class="sxs-lookup"><span data-stu-id="bad9e-190">False</span></span>                                  |
| <span data-ttu-id="bad9e-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bad9e-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="bad9e-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bad9e-192">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="bad9e-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bad9e-193">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="bad9e-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bad9e-194">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="bad9e-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bad9e-195">Search-Flags</span></span>           | <span data-ttu-id="bad9e-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bad9e-196">0x00000000</span></span>                             |
| <span data-ttu-id="bad9e-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bad9e-197">System-Flags</span></span>           | <span data-ttu-id="bad9e-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bad9e-198">0x00000010</span></span>                             |
| <span data-ttu-id="bad9e-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bad9e-199">Classes used in</span></span>        | [<span data-ttu-id="bad9e-200">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="bad9e-200">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bad9e-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bad9e-201">Windows Server 2008</span></span>



| <span data-ttu-id="bad9e-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="bad9e-202">Entry</span></span> | <span data-ttu-id="bad9e-203">Valor</span><span class="sxs-lookup"><span data-stu-id="bad9e-203">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="bad9e-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="bad9e-204">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="bad9e-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bad9e-205">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="bad9e-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="bad9e-206">System-Only</span></span>            | <span data-ttu-id="bad9e-207">True</span><span class="sxs-lookup"><span data-stu-id="bad9e-207">True</span></span>                                   |
| <span data-ttu-id="bad9e-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bad9e-208">Is-Single-Valued</span></span>       | <span data-ttu-id="bad9e-209">True</span><span class="sxs-lookup"><span data-stu-id="bad9e-209">True</span></span>                                   |
| <span data-ttu-id="bad9e-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="bad9e-210">Is Indexed</span></span>             | <span data-ttu-id="bad9e-211">Falso</span><span class="sxs-lookup"><span data-stu-id="bad9e-211">False</span></span>                                  |
| <span data-ttu-id="bad9e-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bad9e-212">In Global Catalog</span></span>      | <span data-ttu-id="bad9e-213">Falso</span><span class="sxs-lookup"><span data-stu-id="bad9e-213">False</span></span>                                  |
| <span data-ttu-id="bad9e-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bad9e-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="bad9e-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bad9e-215">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="bad9e-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bad9e-216">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="bad9e-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bad9e-217">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="bad9e-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bad9e-218">Search-Flags</span></span>           | <span data-ttu-id="bad9e-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bad9e-219">0x00000000</span></span>                             |
| <span data-ttu-id="bad9e-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bad9e-220">System-Flags</span></span>           | <span data-ttu-id="bad9e-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bad9e-221">0x00000010</span></span>                             |
| <span data-ttu-id="bad9e-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bad9e-222">Classes used in</span></span>        | [<span data-ttu-id="bad9e-223">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="bad9e-223">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bad9e-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bad9e-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bad9e-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="bad9e-225">Entry</span></span> | <span data-ttu-id="bad9e-226">Valor</span><span class="sxs-lookup"><span data-stu-id="bad9e-226">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="bad9e-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="bad9e-227">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="bad9e-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bad9e-228">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="bad9e-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="bad9e-229">System-Only</span></span>            | <span data-ttu-id="bad9e-230">True</span><span class="sxs-lookup"><span data-stu-id="bad9e-230">True</span></span>                                   |
| <span data-ttu-id="bad9e-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bad9e-231">Is-Single-Valued</span></span>       | <span data-ttu-id="bad9e-232">True</span><span class="sxs-lookup"><span data-stu-id="bad9e-232">True</span></span>                                   |
| <span data-ttu-id="bad9e-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="bad9e-233">Is Indexed</span></span>             | <span data-ttu-id="bad9e-234">Falso</span><span class="sxs-lookup"><span data-stu-id="bad9e-234">False</span></span>                                  |
| <span data-ttu-id="bad9e-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bad9e-235">In Global Catalog</span></span>      | <span data-ttu-id="bad9e-236">Falso</span><span class="sxs-lookup"><span data-stu-id="bad9e-236">False</span></span>                                  |
| <span data-ttu-id="bad9e-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bad9e-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="bad9e-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bad9e-238">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="bad9e-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bad9e-239">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="bad9e-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bad9e-240">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="bad9e-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bad9e-241">Search-Flags</span></span>           | <span data-ttu-id="bad9e-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bad9e-242">0x00000000</span></span>                             |
| <span data-ttu-id="bad9e-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bad9e-243">System-Flags</span></span>           | <span data-ttu-id="bad9e-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bad9e-244">0x00000010</span></span>                             |
| <span data-ttu-id="bad9e-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bad9e-245">Classes used in</span></span>        | [<span data-ttu-id="bad9e-246">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="bad9e-246">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bad9e-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bad9e-247">Windows Server 2012</span></span>



| <span data-ttu-id="bad9e-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="bad9e-248">Entry</span></span> | <span data-ttu-id="bad9e-249">Valor</span><span class="sxs-lookup"><span data-stu-id="bad9e-249">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="bad9e-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="bad9e-250">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="bad9e-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bad9e-251">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="bad9e-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="bad9e-252">System-Only</span></span>            | <span data-ttu-id="bad9e-253">True</span><span class="sxs-lookup"><span data-stu-id="bad9e-253">True</span></span>                                   |
| <span data-ttu-id="bad9e-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bad9e-254">Is-Single-Valued</span></span>       | <span data-ttu-id="bad9e-255">True</span><span class="sxs-lookup"><span data-stu-id="bad9e-255">True</span></span>                                   |
| <span data-ttu-id="bad9e-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="bad9e-256">Is Indexed</span></span>             | <span data-ttu-id="bad9e-257">Falso</span><span class="sxs-lookup"><span data-stu-id="bad9e-257">False</span></span>                                  |
| <span data-ttu-id="bad9e-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bad9e-258">In Global Catalog</span></span>      | <span data-ttu-id="bad9e-259">Falso</span><span class="sxs-lookup"><span data-stu-id="bad9e-259">False</span></span>                                  |
| <span data-ttu-id="bad9e-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bad9e-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="bad9e-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bad9e-261">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="bad9e-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bad9e-262">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="bad9e-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bad9e-263">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="bad9e-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bad9e-264">Search-Flags</span></span>           | <span data-ttu-id="bad9e-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bad9e-265">0x00000000</span></span>                             |
| <span data-ttu-id="bad9e-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bad9e-266">System-Flags</span></span>           | <span data-ttu-id="bad9e-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bad9e-267">0x00000010</span></span>                             |
| <span data-ttu-id="bad9e-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bad9e-268">Classes used in</span></span>        | [<span data-ttu-id="bad9e-269">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="bad9e-269">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





