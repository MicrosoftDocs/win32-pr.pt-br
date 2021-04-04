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
# <a name="rid-used-pool-attribute"></a><span data-ttu-id="61ba5-105">RID-usado-atributo de pool</span><span class="sxs-lookup"><span data-stu-id="61ba5-105">RID-Used-Pool attribute</span></span>

<span data-ttu-id="61ba5-106">Os pools RID que foram usados por um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="61ba5-106">The RID Pools that have been used by a DC.</span></span>



| <span data-ttu-id="61ba5-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="61ba5-107">Entry</span></span> | <span data-ttu-id="61ba5-108">Valor</span><span class="sxs-lookup"><span data-stu-id="61ba5-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="61ba5-109">CN</span><span class="sxs-lookup"><span data-stu-id="61ba5-109">CN</span></span>                | <span data-ttu-id="61ba5-110">RID-usado-pool</span><span class="sxs-lookup"><span data-stu-id="61ba5-110">RID-Used-Pool</span></span>                        |
| <span data-ttu-id="61ba5-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="61ba5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="61ba5-112">rIDUsedPool</span><span class="sxs-lookup"><span data-stu-id="61ba5-112">rIDUsedPool</span></span>                          |
| <span data-ttu-id="61ba5-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="61ba5-113">Size</span></span>              | <span data-ttu-id="61ba5-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="61ba5-114">8 bytes</span></span>                              |
| <span data-ttu-id="61ba5-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="61ba5-115">Update Privilege</span></span>  | <span data-ttu-id="61ba5-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="61ba5-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="61ba5-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="61ba5-117">Update Frequency</span></span>  | <span data-ttu-id="61ba5-118">Sempre que um pool RID é esvaziado.</span><span class="sxs-lookup"><span data-stu-id="61ba5-118">Whenever a RID pool is emptied.</span></span>      |
| <span data-ttu-id="61ba5-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="61ba5-119">Attribute-Id</span></span>      | <span data-ttu-id="61ba5-120">1.2.840.113556.1.4.373</span><span class="sxs-lookup"><span data-stu-id="61ba5-120">1.2.840.113556.1.4.373</span></span>               |
| <span data-ttu-id="61ba5-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="61ba5-121">System-Id-Guid</span></span>    | <span data-ttu-id="61ba5-122">6617188b-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="61ba5-122">6617188b-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="61ba5-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="61ba5-123">Syntax</span></span>            | [<span data-ttu-id="61ba5-124">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="61ba5-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="61ba5-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="61ba5-125">Implementations</span></span>

-   [<span data-ttu-id="61ba5-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="61ba5-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="61ba5-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="61ba5-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="61ba5-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="61ba5-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="61ba5-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="61ba5-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="61ba5-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="61ba5-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="61ba5-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="61ba5-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="61ba5-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="61ba5-132">Windows 2000 Server</span></span>



| <span data-ttu-id="61ba5-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="61ba5-133">Entry</span></span> | <span data-ttu-id="61ba5-134">Valor</span><span class="sxs-lookup"><span data-stu-id="61ba5-134">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="61ba5-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="61ba5-135">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="61ba5-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ba5-136">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="61ba5-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ba5-137">System-Only</span></span>            | <span data-ttu-id="61ba5-138">True</span><span class="sxs-lookup"><span data-stu-id="61ba5-138">True</span></span>                                   |
| <span data-ttu-id="61ba5-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="61ba5-139">Is-Single-Valued</span></span>       | <span data-ttu-id="61ba5-140">True</span><span class="sxs-lookup"><span data-stu-id="61ba5-140">True</span></span>                                   |
| <span data-ttu-id="61ba5-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="61ba5-141">Is Indexed</span></span>             | <span data-ttu-id="61ba5-142">Falso</span><span class="sxs-lookup"><span data-stu-id="61ba5-142">False</span></span>                                  |
| <span data-ttu-id="61ba5-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="61ba5-143">In Global Catalog</span></span>      | <span data-ttu-id="61ba5-144">Falso</span><span class="sxs-lookup"><span data-stu-id="61ba5-144">False</span></span>                                  |
| <span data-ttu-id="61ba5-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="61ba5-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ba5-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="61ba5-146">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="61ba5-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ba5-147">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="61ba5-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ba5-148">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="61ba5-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba5-149">Search-Flags</span></span>           | <span data-ttu-id="61ba5-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ba5-150">0x00000000</span></span>                             |
| <span data-ttu-id="61ba5-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba5-151">System-Flags</span></span>           | <span data-ttu-id="61ba5-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61ba5-152">0x00000010</span></span>                             |
| <span data-ttu-id="61ba5-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="61ba5-153">Classes used in</span></span>        | [<span data-ttu-id="61ba5-154">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="61ba5-154">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="61ba5-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="61ba5-155">Windows Server 2003</span></span>



| <span data-ttu-id="61ba5-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="61ba5-156">Entry</span></span> | <span data-ttu-id="61ba5-157">Valor</span><span class="sxs-lookup"><span data-stu-id="61ba5-157">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="61ba5-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="61ba5-158">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="61ba5-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ba5-159">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="61ba5-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ba5-160">System-Only</span></span>            | <span data-ttu-id="61ba5-161">True</span><span class="sxs-lookup"><span data-stu-id="61ba5-161">True</span></span>                                   |
| <span data-ttu-id="61ba5-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="61ba5-162">Is-Single-Valued</span></span>       | <span data-ttu-id="61ba5-163">True</span><span class="sxs-lookup"><span data-stu-id="61ba5-163">True</span></span>                                   |
| <span data-ttu-id="61ba5-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="61ba5-164">Is Indexed</span></span>             | <span data-ttu-id="61ba5-165">Falso</span><span class="sxs-lookup"><span data-stu-id="61ba5-165">False</span></span>                                  |
| <span data-ttu-id="61ba5-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="61ba5-166">In Global Catalog</span></span>      | <span data-ttu-id="61ba5-167">Falso</span><span class="sxs-lookup"><span data-stu-id="61ba5-167">False</span></span>                                  |
| <span data-ttu-id="61ba5-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="61ba5-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ba5-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="61ba5-169">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="61ba5-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ba5-170">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="61ba5-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ba5-171">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="61ba5-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba5-172">Search-Flags</span></span>           | <span data-ttu-id="61ba5-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ba5-173">0x00000000</span></span>                             |
| <span data-ttu-id="61ba5-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba5-174">System-Flags</span></span>           | <span data-ttu-id="61ba5-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61ba5-175">0x00000010</span></span>                             |
| <span data-ttu-id="61ba5-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="61ba5-176">Classes used in</span></span>        | [<span data-ttu-id="61ba5-177">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="61ba5-177">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="61ba5-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="61ba5-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="61ba5-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="61ba5-179">Entry</span></span> | <span data-ttu-id="61ba5-180">Valor</span><span class="sxs-lookup"><span data-stu-id="61ba5-180">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="61ba5-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="61ba5-181">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="61ba5-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ba5-182">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="61ba5-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ba5-183">System-Only</span></span>            | <span data-ttu-id="61ba5-184">True</span><span class="sxs-lookup"><span data-stu-id="61ba5-184">True</span></span>                                   |
| <span data-ttu-id="61ba5-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="61ba5-185">Is-Single-Valued</span></span>       | <span data-ttu-id="61ba5-186">True</span><span class="sxs-lookup"><span data-stu-id="61ba5-186">True</span></span>                                   |
| <span data-ttu-id="61ba5-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="61ba5-187">Is Indexed</span></span>             | <span data-ttu-id="61ba5-188">Falso</span><span class="sxs-lookup"><span data-stu-id="61ba5-188">False</span></span>                                  |
| <span data-ttu-id="61ba5-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="61ba5-189">In Global Catalog</span></span>      | <span data-ttu-id="61ba5-190">Falso</span><span class="sxs-lookup"><span data-stu-id="61ba5-190">False</span></span>                                  |
| <span data-ttu-id="61ba5-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="61ba5-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ba5-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="61ba5-192">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="61ba5-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ba5-193">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="61ba5-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ba5-194">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="61ba5-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba5-195">Search-Flags</span></span>           | <span data-ttu-id="61ba5-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ba5-196">0x00000000</span></span>                             |
| <span data-ttu-id="61ba5-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba5-197">System-Flags</span></span>           | <span data-ttu-id="61ba5-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61ba5-198">0x00000010</span></span>                             |
| <span data-ttu-id="61ba5-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="61ba5-199">Classes used in</span></span>        | [<span data-ttu-id="61ba5-200">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="61ba5-200">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="61ba5-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61ba5-201">Windows Server 2008</span></span>



| <span data-ttu-id="61ba5-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="61ba5-202">Entry</span></span> | <span data-ttu-id="61ba5-203">Valor</span><span class="sxs-lookup"><span data-stu-id="61ba5-203">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="61ba5-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="61ba5-204">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="61ba5-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ba5-205">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="61ba5-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ba5-206">System-Only</span></span>            | <span data-ttu-id="61ba5-207">True</span><span class="sxs-lookup"><span data-stu-id="61ba5-207">True</span></span>                                   |
| <span data-ttu-id="61ba5-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="61ba5-208">Is-Single-Valued</span></span>       | <span data-ttu-id="61ba5-209">True</span><span class="sxs-lookup"><span data-stu-id="61ba5-209">True</span></span>                                   |
| <span data-ttu-id="61ba5-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="61ba5-210">Is Indexed</span></span>             | <span data-ttu-id="61ba5-211">Falso</span><span class="sxs-lookup"><span data-stu-id="61ba5-211">False</span></span>                                  |
| <span data-ttu-id="61ba5-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="61ba5-212">In Global Catalog</span></span>      | <span data-ttu-id="61ba5-213">Falso</span><span class="sxs-lookup"><span data-stu-id="61ba5-213">False</span></span>                                  |
| <span data-ttu-id="61ba5-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="61ba5-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ba5-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="61ba5-215">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="61ba5-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ba5-216">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="61ba5-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ba5-217">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="61ba5-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba5-218">Search-Flags</span></span>           | <span data-ttu-id="61ba5-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ba5-219">0x00000000</span></span>                             |
| <span data-ttu-id="61ba5-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba5-220">System-Flags</span></span>           | <span data-ttu-id="61ba5-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61ba5-221">0x00000010</span></span>                             |
| <span data-ttu-id="61ba5-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="61ba5-222">Classes used in</span></span>        | [<span data-ttu-id="61ba5-223">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="61ba5-223">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="61ba5-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="61ba5-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="61ba5-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="61ba5-225">Entry</span></span> | <span data-ttu-id="61ba5-226">Valor</span><span class="sxs-lookup"><span data-stu-id="61ba5-226">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="61ba5-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="61ba5-227">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="61ba5-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ba5-228">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="61ba5-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ba5-229">System-Only</span></span>            | <span data-ttu-id="61ba5-230">True</span><span class="sxs-lookup"><span data-stu-id="61ba5-230">True</span></span>                                   |
| <span data-ttu-id="61ba5-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="61ba5-231">Is-Single-Valued</span></span>       | <span data-ttu-id="61ba5-232">True</span><span class="sxs-lookup"><span data-stu-id="61ba5-232">True</span></span>                                   |
| <span data-ttu-id="61ba5-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="61ba5-233">Is Indexed</span></span>             | <span data-ttu-id="61ba5-234">Falso</span><span class="sxs-lookup"><span data-stu-id="61ba5-234">False</span></span>                                  |
| <span data-ttu-id="61ba5-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="61ba5-235">In Global Catalog</span></span>      | <span data-ttu-id="61ba5-236">Falso</span><span class="sxs-lookup"><span data-stu-id="61ba5-236">False</span></span>                                  |
| <span data-ttu-id="61ba5-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="61ba5-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ba5-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="61ba5-238">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="61ba5-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ba5-239">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="61ba5-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ba5-240">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="61ba5-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba5-241">Search-Flags</span></span>           | <span data-ttu-id="61ba5-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ba5-242">0x00000000</span></span>                             |
| <span data-ttu-id="61ba5-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba5-243">System-Flags</span></span>           | <span data-ttu-id="61ba5-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61ba5-244">0x00000010</span></span>                             |
| <span data-ttu-id="61ba5-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="61ba5-245">Classes used in</span></span>        | [<span data-ttu-id="61ba5-246">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="61ba5-246">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="61ba5-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61ba5-247">Windows Server 2012</span></span>



| <span data-ttu-id="61ba5-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="61ba5-248">Entry</span></span> | <span data-ttu-id="61ba5-249">Valor</span><span class="sxs-lookup"><span data-stu-id="61ba5-249">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="61ba5-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="61ba5-250">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="61ba5-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ba5-251">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="61ba5-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ba5-252">System-Only</span></span>            | <span data-ttu-id="61ba5-253">True</span><span class="sxs-lookup"><span data-stu-id="61ba5-253">True</span></span>                                   |
| <span data-ttu-id="61ba5-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="61ba5-254">Is-Single-Valued</span></span>       | <span data-ttu-id="61ba5-255">True</span><span class="sxs-lookup"><span data-stu-id="61ba5-255">True</span></span>                                   |
| <span data-ttu-id="61ba5-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="61ba5-256">Is Indexed</span></span>             | <span data-ttu-id="61ba5-257">Falso</span><span class="sxs-lookup"><span data-stu-id="61ba5-257">False</span></span>                                  |
| <span data-ttu-id="61ba5-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="61ba5-258">In Global Catalog</span></span>      | <span data-ttu-id="61ba5-259">Falso</span><span class="sxs-lookup"><span data-stu-id="61ba5-259">False</span></span>                                  |
| <span data-ttu-id="61ba5-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="61ba5-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ba5-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="61ba5-261">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="61ba5-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ba5-262">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="61ba5-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ba5-263">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="61ba5-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba5-264">Search-Flags</span></span>           | <span data-ttu-id="61ba5-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ba5-265">0x00000000</span></span>                             |
| <span data-ttu-id="61ba5-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ba5-266">System-Flags</span></span>           | <span data-ttu-id="61ba5-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61ba5-267">0x00000010</span></span>                             |
| <span data-ttu-id="61ba5-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="61ba5-268">Classes used in</span></span>        | [<span data-ttu-id="61ba5-269">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="61ba5-269">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





