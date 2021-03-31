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
# <a name="rid-used-pool-attribute"></a><span data-ttu-id="06f7d-105">RID-usado-atributo de pool</span><span class="sxs-lookup"><span data-stu-id="06f7d-105">RID-Used-Pool attribute</span></span>

<span data-ttu-id="06f7d-106">Os pools RID que foram usados por um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="06f7d-106">The RID Pools that have been used by a DC.</span></span>



| <span data-ttu-id="06f7d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="06f7d-107">Entry</span></span> | <span data-ttu-id="06f7d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="06f7d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="06f7d-109">CN</span><span class="sxs-lookup"><span data-stu-id="06f7d-109">CN</span></span>                | <span data-ttu-id="06f7d-110">RID-usado-pool</span><span class="sxs-lookup"><span data-stu-id="06f7d-110">RID-Used-Pool</span></span>                        |
| <span data-ttu-id="06f7d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="06f7d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="06f7d-112">rIDUsedPool</span><span class="sxs-lookup"><span data-stu-id="06f7d-112">rIDUsedPool</span></span>                          |
| <span data-ttu-id="06f7d-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="06f7d-113">Size</span></span>              | <span data-ttu-id="06f7d-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="06f7d-114">8 bytes</span></span>                              |
| <span data-ttu-id="06f7d-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="06f7d-115">Update Privilege</span></span>  | <span data-ttu-id="06f7d-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="06f7d-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="06f7d-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="06f7d-117">Update Frequency</span></span>  | <span data-ttu-id="06f7d-118">Sempre que um pool RID é esvaziado.</span><span class="sxs-lookup"><span data-stu-id="06f7d-118">Whenever a RID pool is emptied.</span></span>      |
| <span data-ttu-id="06f7d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="06f7d-119">Attribute-Id</span></span>      | <span data-ttu-id="06f7d-120">1.2.840.113556.1.4.373</span><span class="sxs-lookup"><span data-stu-id="06f7d-120">1.2.840.113556.1.4.373</span></span>               |
| <span data-ttu-id="06f7d-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="06f7d-121">System-Id-Guid</span></span>    | <span data-ttu-id="06f7d-122">6617188b-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="06f7d-122">6617188b-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="06f7d-123">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06f7d-123">Syntax</span></span>            | [<span data-ttu-id="06f7d-124">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="06f7d-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="06f7d-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="06f7d-125">Implementations</span></span>

-   [<span data-ttu-id="06f7d-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="06f7d-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="06f7d-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="06f7d-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="06f7d-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="06f7d-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="06f7d-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="06f7d-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="06f7d-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="06f7d-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="06f7d-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="06f7d-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="06f7d-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="06f7d-132">Windows 2000 Server</span></span>



| <span data-ttu-id="06f7d-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="06f7d-133">Entry</span></span> | <span data-ttu-id="06f7d-134">Valor</span><span class="sxs-lookup"><span data-stu-id="06f7d-134">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="06f7d-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="06f7d-135">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="06f7d-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06f7d-136">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="06f7d-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="06f7d-137">System-Only</span></span>            | <span data-ttu-id="06f7d-138">True</span><span class="sxs-lookup"><span data-stu-id="06f7d-138">True</span></span>                                   |
| <span data-ttu-id="06f7d-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="06f7d-139">Is-Single-Valued</span></span>       | <span data-ttu-id="06f7d-140">True</span><span class="sxs-lookup"><span data-stu-id="06f7d-140">True</span></span>                                   |
| <span data-ttu-id="06f7d-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="06f7d-141">Is Indexed</span></span>             | <span data-ttu-id="06f7d-142">Falso</span><span class="sxs-lookup"><span data-stu-id="06f7d-142">False</span></span>                                  |
| <span data-ttu-id="06f7d-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="06f7d-143">In Global Catalog</span></span>      | <span data-ttu-id="06f7d-144">Falso</span><span class="sxs-lookup"><span data-stu-id="06f7d-144">False</span></span>                                  |
| <span data-ttu-id="06f7d-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06f7d-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="06f7d-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="06f7d-146">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="06f7d-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06f7d-147">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="06f7d-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06f7d-148">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="06f7d-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06f7d-149">Search-Flags</span></span>           | <span data-ttu-id="06f7d-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06f7d-150">0x00000000</span></span>                             |
| <span data-ttu-id="06f7d-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06f7d-151">System-Flags</span></span>           | <span data-ttu-id="06f7d-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06f7d-152">0x00000010</span></span>                             |
| <span data-ttu-id="06f7d-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="06f7d-153">Classes used in</span></span>        | [<span data-ttu-id="06f7d-154">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="06f7d-154">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="06f7d-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="06f7d-155">Windows Server 2003</span></span>



| <span data-ttu-id="06f7d-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="06f7d-156">Entry</span></span> | <span data-ttu-id="06f7d-157">Valor</span><span class="sxs-lookup"><span data-stu-id="06f7d-157">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="06f7d-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="06f7d-158">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="06f7d-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06f7d-159">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="06f7d-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="06f7d-160">System-Only</span></span>            | <span data-ttu-id="06f7d-161">True</span><span class="sxs-lookup"><span data-stu-id="06f7d-161">True</span></span>                                   |
| <span data-ttu-id="06f7d-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="06f7d-162">Is-Single-Valued</span></span>       | <span data-ttu-id="06f7d-163">True</span><span class="sxs-lookup"><span data-stu-id="06f7d-163">True</span></span>                                   |
| <span data-ttu-id="06f7d-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="06f7d-164">Is Indexed</span></span>             | <span data-ttu-id="06f7d-165">Falso</span><span class="sxs-lookup"><span data-stu-id="06f7d-165">False</span></span>                                  |
| <span data-ttu-id="06f7d-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="06f7d-166">In Global Catalog</span></span>      | <span data-ttu-id="06f7d-167">Falso</span><span class="sxs-lookup"><span data-stu-id="06f7d-167">False</span></span>                                  |
| <span data-ttu-id="06f7d-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06f7d-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="06f7d-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="06f7d-169">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="06f7d-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06f7d-170">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="06f7d-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06f7d-171">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="06f7d-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06f7d-172">Search-Flags</span></span>           | <span data-ttu-id="06f7d-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06f7d-173">0x00000000</span></span>                             |
| <span data-ttu-id="06f7d-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06f7d-174">System-Flags</span></span>           | <span data-ttu-id="06f7d-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06f7d-175">0x00000010</span></span>                             |
| <span data-ttu-id="06f7d-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="06f7d-176">Classes used in</span></span>        | [<span data-ttu-id="06f7d-177">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="06f7d-177">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="06f7d-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="06f7d-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="06f7d-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="06f7d-179">Entry</span></span> | <span data-ttu-id="06f7d-180">Valor</span><span class="sxs-lookup"><span data-stu-id="06f7d-180">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="06f7d-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="06f7d-181">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="06f7d-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06f7d-182">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="06f7d-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="06f7d-183">System-Only</span></span>            | <span data-ttu-id="06f7d-184">True</span><span class="sxs-lookup"><span data-stu-id="06f7d-184">True</span></span>                                   |
| <span data-ttu-id="06f7d-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="06f7d-185">Is-Single-Valued</span></span>       | <span data-ttu-id="06f7d-186">True</span><span class="sxs-lookup"><span data-stu-id="06f7d-186">True</span></span>                                   |
| <span data-ttu-id="06f7d-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="06f7d-187">Is Indexed</span></span>             | <span data-ttu-id="06f7d-188">Falso</span><span class="sxs-lookup"><span data-stu-id="06f7d-188">False</span></span>                                  |
| <span data-ttu-id="06f7d-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="06f7d-189">In Global Catalog</span></span>      | <span data-ttu-id="06f7d-190">Falso</span><span class="sxs-lookup"><span data-stu-id="06f7d-190">False</span></span>                                  |
| <span data-ttu-id="06f7d-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06f7d-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="06f7d-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="06f7d-192">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="06f7d-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06f7d-193">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="06f7d-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06f7d-194">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="06f7d-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06f7d-195">Search-Flags</span></span>           | <span data-ttu-id="06f7d-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06f7d-196">0x00000000</span></span>                             |
| <span data-ttu-id="06f7d-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06f7d-197">System-Flags</span></span>           | <span data-ttu-id="06f7d-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06f7d-198">0x00000010</span></span>                             |
| <span data-ttu-id="06f7d-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="06f7d-199">Classes used in</span></span>        | [<span data-ttu-id="06f7d-200">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="06f7d-200">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="06f7d-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06f7d-201">Windows Server 2008</span></span>



| <span data-ttu-id="06f7d-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="06f7d-202">Entry</span></span> | <span data-ttu-id="06f7d-203">Valor</span><span class="sxs-lookup"><span data-stu-id="06f7d-203">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="06f7d-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="06f7d-204">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="06f7d-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06f7d-205">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="06f7d-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="06f7d-206">System-Only</span></span>            | <span data-ttu-id="06f7d-207">True</span><span class="sxs-lookup"><span data-stu-id="06f7d-207">True</span></span>                                   |
| <span data-ttu-id="06f7d-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="06f7d-208">Is-Single-Valued</span></span>       | <span data-ttu-id="06f7d-209">True</span><span class="sxs-lookup"><span data-stu-id="06f7d-209">True</span></span>                                   |
| <span data-ttu-id="06f7d-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="06f7d-210">Is Indexed</span></span>             | <span data-ttu-id="06f7d-211">Falso</span><span class="sxs-lookup"><span data-stu-id="06f7d-211">False</span></span>                                  |
| <span data-ttu-id="06f7d-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="06f7d-212">In Global Catalog</span></span>      | <span data-ttu-id="06f7d-213">Falso</span><span class="sxs-lookup"><span data-stu-id="06f7d-213">False</span></span>                                  |
| <span data-ttu-id="06f7d-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06f7d-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="06f7d-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="06f7d-215">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="06f7d-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06f7d-216">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="06f7d-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06f7d-217">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="06f7d-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06f7d-218">Search-Flags</span></span>           | <span data-ttu-id="06f7d-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06f7d-219">0x00000000</span></span>                             |
| <span data-ttu-id="06f7d-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06f7d-220">System-Flags</span></span>           | <span data-ttu-id="06f7d-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06f7d-221">0x00000010</span></span>                             |
| <span data-ttu-id="06f7d-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="06f7d-222">Classes used in</span></span>        | [<span data-ttu-id="06f7d-223">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="06f7d-223">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="06f7d-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="06f7d-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="06f7d-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="06f7d-225">Entry</span></span> | <span data-ttu-id="06f7d-226">Valor</span><span class="sxs-lookup"><span data-stu-id="06f7d-226">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="06f7d-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="06f7d-227">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="06f7d-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06f7d-228">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="06f7d-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="06f7d-229">System-Only</span></span>            | <span data-ttu-id="06f7d-230">True</span><span class="sxs-lookup"><span data-stu-id="06f7d-230">True</span></span>                                   |
| <span data-ttu-id="06f7d-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="06f7d-231">Is-Single-Valued</span></span>       | <span data-ttu-id="06f7d-232">True</span><span class="sxs-lookup"><span data-stu-id="06f7d-232">True</span></span>                                   |
| <span data-ttu-id="06f7d-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="06f7d-233">Is Indexed</span></span>             | <span data-ttu-id="06f7d-234">Falso</span><span class="sxs-lookup"><span data-stu-id="06f7d-234">False</span></span>                                  |
| <span data-ttu-id="06f7d-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="06f7d-235">In Global Catalog</span></span>      | <span data-ttu-id="06f7d-236">Falso</span><span class="sxs-lookup"><span data-stu-id="06f7d-236">False</span></span>                                  |
| <span data-ttu-id="06f7d-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06f7d-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="06f7d-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="06f7d-238">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="06f7d-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06f7d-239">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="06f7d-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06f7d-240">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="06f7d-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06f7d-241">Search-Flags</span></span>           | <span data-ttu-id="06f7d-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06f7d-242">0x00000000</span></span>                             |
| <span data-ttu-id="06f7d-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06f7d-243">System-Flags</span></span>           | <span data-ttu-id="06f7d-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06f7d-244">0x00000010</span></span>                             |
| <span data-ttu-id="06f7d-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="06f7d-245">Classes used in</span></span>        | [<span data-ttu-id="06f7d-246">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="06f7d-246">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="06f7d-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="06f7d-247">Windows Server 2012</span></span>



| <span data-ttu-id="06f7d-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="06f7d-248">Entry</span></span> | <span data-ttu-id="06f7d-249">Valor</span><span class="sxs-lookup"><span data-stu-id="06f7d-249">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="06f7d-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="06f7d-250">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="06f7d-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06f7d-251">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="06f7d-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="06f7d-252">System-Only</span></span>            | <span data-ttu-id="06f7d-253">True</span><span class="sxs-lookup"><span data-stu-id="06f7d-253">True</span></span>                                   |
| <span data-ttu-id="06f7d-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="06f7d-254">Is-Single-Valued</span></span>       | <span data-ttu-id="06f7d-255">True</span><span class="sxs-lookup"><span data-stu-id="06f7d-255">True</span></span>                                   |
| <span data-ttu-id="06f7d-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="06f7d-256">Is Indexed</span></span>             | <span data-ttu-id="06f7d-257">Falso</span><span class="sxs-lookup"><span data-stu-id="06f7d-257">False</span></span>                                  |
| <span data-ttu-id="06f7d-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="06f7d-258">In Global Catalog</span></span>      | <span data-ttu-id="06f7d-259">Falso</span><span class="sxs-lookup"><span data-stu-id="06f7d-259">False</span></span>                                  |
| <span data-ttu-id="06f7d-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06f7d-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="06f7d-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="06f7d-261">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="06f7d-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06f7d-262">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="06f7d-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06f7d-263">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="06f7d-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06f7d-264">Search-Flags</span></span>           | <span data-ttu-id="06f7d-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06f7d-265">0x00000000</span></span>                             |
| <span data-ttu-id="06f7d-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06f7d-266">System-Flags</span></span>           | <span data-ttu-id="06f7d-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="06f7d-267">0x00000010</span></span>                             |
| <span data-ttu-id="06f7d-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="06f7d-268">Classes used in</span></span>        | [<span data-ttu-id="06f7d-269">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="06f7d-269">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





