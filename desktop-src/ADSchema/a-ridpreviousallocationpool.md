---
title: Atributo RID-Previous-Allocation-pool
description: Contém o pool de RIDs (identificadores relativos) do qual um controlador de domínio se aloca.
ms.assetid: d2f60259-388b-4dea-a1f7-9e650b1a66db
ms.tgt_platform: multiple
keywords:
- RID-Previous-Allocation-pool de atributos do AD Schema
- Esquema de AD do atributo rIDPreviousAllocationPool
topic_type:
- apiref
api_name:
- RID-Previous-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15438d55c9540ecca873395cc329058bc0773399
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825091"
---
# <a name="rid-previous-allocation-pool-attribute"></a><span data-ttu-id="33088-105">Atributo RID-Previous-Allocation-pool</span><span class="sxs-lookup"><span data-stu-id="33088-105">RID-Previous-Allocation-Pool attribute</span></span>

<span data-ttu-id="33088-106">O atributo **RID-Previous-Alloc-pool** contém o pool de RIDs (identificadores relativos) do qual um controlador de domínio se aloca.</span><span class="sxs-lookup"><span data-stu-id="33088-106">The **RID-Previous-Allocation-Pool** attribute contains the pool of relative identifiers (RIDs) that a domain controller allocates from.</span></span> <span data-ttu-id="33088-107">Esse atributo é um valor de oito bytes que contém um par de inteiros de quatro bytes que representam os valores de início e término do pool de RIDs.</span><span class="sxs-lookup"><span data-stu-id="33088-107">This attribute is an eight-byte value that contains a pair of four-byte integers that represent the start and end values of the RID pool.</span></span> <span data-ttu-id="33088-108">O valor inicial está nos quatro bytes inferiores e o valor final está nos quatro bytes superiores.</span><span class="sxs-lookup"><span data-stu-id="33088-108">The start value is in the lower four bytes and the end value is in the upper four bytes.</span></span>



| <span data-ttu-id="33088-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="33088-109">Entry</span></span> | <span data-ttu-id="33088-110">Valor</span><span class="sxs-lookup"><span data-stu-id="33088-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="33088-111">CN</span><span class="sxs-lookup"><span data-stu-id="33088-111">CN</span></span>                | <span data-ttu-id="33088-112">RID-anterior-pool de alocação</span><span class="sxs-lookup"><span data-stu-id="33088-112">RID-Previous-Allocation-Pool</span></span>         |
| <span data-ttu-id="33088-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="33088-113">Ldap-Display-Name</span></span> | <span data-ttu-id="33088-114">rIDPreviousAllocationPool</span><span class="sxs-lookup"><span data-stu-id="33088-114">rIDPreviousAllocationPool</span></span>            |
| <span data-ttu-id="33088-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="33088-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="33088-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="33088-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="33088-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="33088-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="33088-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="33088-118">Attribute-Id</span></span>      | <span data-ttu-id="33088-119">1.2.840.113556.1.4.372</span><span class="sxs-lookup"><span data-stu-id="33088-119">1.2.840.113556.1.4.372</span></span>               |
| <span data-ttu-id="33088-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="33088-120">System-Id-Guid</span></span>    | <span data-ttu-id="33088-121">6617188a-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="33088-121">6617188a-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="33088-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="33088-122">Syntax</span></span>            | [<span data-ttu-id="33088-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="33088-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="33088-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="33088-124">Implementations</span></span>

-   [<span data-ttu-id="33088-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="33088-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="33088-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="33088-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="33088-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="33088-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="33088-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="33088-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="33088-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="33088-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="33088-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="33088-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="33088-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="33088-131">Windows 2000 Server</span></span>



| <span data-ttu-id="33088-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="33088-132">Entry</span></span> | <span data-ttu-id="33088-133">Valor</span><span class="sxs-lookup"><span data-stu-id="33088-133">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="33088-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="33088-134">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="33088-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33088-135">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="33088-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="33088-136">System-Only</span></span>            | <span data-ttu-id="33088-137">True</span><span class="sxs-lookup"><span data-stu-id="33088-137">True</span></span>                                   |
| <span data-ttu-id="33088-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="33088-138">Is-Single-Valued</span></span>       | <span data-ttu-id="33088-139">True</span><span class="sxs-lookup"><span data-stu-id="33088-139">True</span></span>                                   |
| <span data-ttu-id="33088-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="33088-140">Is Indexed</span></span>             | <span data-ttu-id="33088-141">Falso</span><span class="sxs-lookup"><span data-stu-id="33088-141">False</span></span>                                  |
| <span data-ttu-id="33088-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="33088-142">In Global Catalog</span></span>      | <span data-ttu-id="33088-143">Falso</span><span class="sxs-lookup"><span data-stu-id="33088-143">False</span></span>                                  |
| <span data-ttu-id="33088-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="33088-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="33088-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="33088-145">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="33088-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33088-146">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="33088-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33088-147">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="33088-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33088-148">Search-Flags</span></span>           | <span data-ttu-id="33088-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33088-149">0x00000000</span></span>                             |
| <span data-ttu-id="33088-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33088-150">System-Flags</span></span>           | <span data-ttu-id="33088-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="33088-151">0x00000011</span></span>                             |
| <span data-ttu-id="33088-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="33088-152">Classes used in</span></span>        | [<span data-ttu-id="33088-153">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="33088-153">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="33088-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="33088-154">Windows Server 2003</span></span>



| <span data-ttu-id="33088-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="33088-155">Entry</span></span> | <span data-ttu-id="33088-156">Valor</span><span class="sxs-lookup"><span data-stu-id="33088-156">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="33088-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="33088-157">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="33088-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33088-158">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="33088-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="33088-159">System-Only</span></span>            | <span data-ttu-id="33088-160">True</span><span class="sxs-lookup"><span data-stu-id="33088-160">True</span></span>                                   |
| <span data-ttu-id="33088-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="33088-161">Is-Single-Valued</span></span>       | <span data-ttu-id="33088-162">True</span><span class="sxs-lookup"><span data-stu-id="33088-162">True</span></span>                                   |
| <span data-ttu-id="33088-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="33088-163">Is Indexed</span></span>             | <span data-ttu-id="33088-164">Falso</span><span class="sxs-lookup"><span data-stu-id="33088-164">False</span></span>                                  |
| <span data-ttu-id="33088-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="33088-165">In Global Catalog</span></span>      | <span data-ttu-id="33088-166">Falso</span><span class="sxs-lookup"><span data-stu-id="33088-166">False</span></span>                                  |
| <span data-ttu-id="33088-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="33088-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="33088-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="33088-168">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="33088-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33088-169">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="33088-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33088-170">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="33088-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33088-171">Search-Flags</span></span>           | <span data-ttu-id="33088-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33088-172">0x00000000</span></span>                             |
| <span data-ttu-id="33088-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33088-173">System-Flags</span></span>           | <span data-ttu-id="33088-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="33088-174">0x00000011</span></span>                             |
| <span data-ttu-id="33088-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="33088-175">Classes used in</span></span>        | [<span data-ttu-id="33088-176">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="33088-176">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="33088-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="33088-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="33088-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="33088-178">Entry</span></span> | <span data-ttu-id="33088-179">Valor</span><span class="sxs-lookup"><span data-stu-id="33088-179">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="33088-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="33088-180">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="33088-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33088-181">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="33088-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="33088-182">System-Only</span></span>            | <span data-ttu-id="33088-183">True</span><span class="sxs-lookup"><span data-stu-id="33088-183">True</span></span>                                   |
| <span data-ttu-id="33088-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="33088-184">Is-Single-Valued</span></span>       | <span data-ttu-id="33088-185">True</span><span class="sxs-lookup"><span data-stu-id="33088-185">True</span></span>                                   |
| <span data-ttu-id="33088-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="33088-186">Is Indexed</span></span>             | <span data-ttu-id="33088-187">Falso</span><span class="sxs-lookup"><span data-stu-id="33088-187">False</span></span>                                  |
| <span data-ttu-id="33088-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="33088-188">In Global Catalog</span></span>      | <span data-ttu-id="33088-189">Falso</span><span class="sxs-lookup"><span data-stu-id="33088-189">False</span></span>                                  |
| <span data-ttu-id="33088-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="33088-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="33088-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="33088-191">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="33088-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33088-192">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="33088-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33088-193">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="33088-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33088-194">Search-Flags</span></span>           | <span data-ttu-id="33088-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33088-195">0x00000000</span></span>                             |
| <span data-ttu-id="33088-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33088-196">System-Flags</span></span>           | <span data-ttu-id="33088-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="33088-197">0x00000011</span></span>                             |
| <span data-ttu-id="33088-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="33088-198">Classes used in</span></span>        | [<span data-ttu-id="33088-199">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="33088-199">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="33088-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33088-200">Windows Server 2008</span></span>



| <span data-ttu-id="33088-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="33088-201">Entry</span></span> | <span data-ttu-id="33088-202">Valor</span><span class="sxs-lookup"><span data-stu-id="33088-202">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="33088-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="33088-203">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="33088-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33088-204">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="33088-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="33088-205">System-Only</span></span>            | <span data-ttu-id="33088-206">True</span><span class="sxs-lookup"><span data-stu-id="33088-206">True</span></span>                                   |
| <span data-ttu-id="33088-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="33088-207">Is-Single-Valued</span></span>       | <span data-ttu-id="33088-208">True</span><span class="sxs-lookup"><span data-stu-id="33088-208">True</span></span>                                   |
| <span data-ttu-id="33088-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="33088-209">Is Indexed</span></span>             | <span data-ttu-id="33088-210">Falso</span><span class="sxs-lookup"><span data-stu-id="33088-210">False</span></span>                                  |
| <span data-ttu-id="33088-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="33088-211">In Global Catalog</span></span>      | <span data-ttu-id="33088-212">Falso</span><span class="sxs-lookup"><span data-stu-id="33088-212">False</span></span>                                  |
| <span data-ttu-id="33088-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="33088-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="33088-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="33088-214">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="33088-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33088-215">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="33088-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33088-216">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="33088-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33088-217">Search-Flags</span></span>           | <span data-ttu-id="33088-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33088-218">0x00000000</span></span>                             |
| <span data-ttu-id="33088-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33088-219">System-Flags</span></span>           | <span data-ttu-id="33088-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="33088-220">0x00000011</span></span>                             |
| <span data-ttu-id="33088-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="33088-221">Classes used in</span></span>        | [<span data-ttu-id="33088-222">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="33088-222">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="33088-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="33088-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="33088-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="33088-224">Entry</span></span> | <span data-ttu-id="33088-225">Valor</span><span class="sxs-lookup"><span data-stu-id="33088-225">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="33088-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="33088-226">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="33088-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33088-227">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="33088-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="33088-228">System-Only</span></span>            | <span data-ttu-id="33088-229">True</span><span class="sxs-lookup"><span data-stu-id="33088-229">True</span></span>                                   |
| <span data-ttu-id="33088-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="33088-230">Is-Single-Valued</span></span>       | <span data-ttu-id="33088-231">True</span><span class="sxs-lookup"><span data-stu-id="33088-231">True</span></span>                                   |
| <span data-ttu-id="33088-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="33088-232">Is Indexed</span></span>             | <span data-ttu-id="33088-233">Falso</span><span class="sxs-lookup"><span data-stu-id="33088-233">False</span></span>                                  |
| <span data-ttu-id="33088-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="33088-234">In Global Catalog</span></span>      | <span data-ttu-id="33088-235">Falso</span><span class="sxs-lookup"><span data-stu-id="33088-235">False</span></span>                                  |
| <span data-ttu-id="33088-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="33088-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="33088-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="33088-237">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="33088-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33088-238">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="33088-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33088-239">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="33088-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33088-240">Search-Flags</span></span>           | <span data-ttu-id="33088-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33088-241">0x00000000</span></span>                             |
| <span data-ttu-id="33088-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33088-242">System-Flags</span></span>           | <span data-ttu-id="33088-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="33088-243">0x00000011</span></span>                             |
| <span data-ttu-id="33088-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="33088-244">Classes used in</span></span>        | [<span data-ttu-id="33088-245">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="33088-245">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="33088-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="33088-246">Windows Server 2012</span></span>



| <span data-ttu-id="33088-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="33088-247">Entry</span></span> | <span data-ttu-id="33088-248">Valor</span><span class="sxs-lookup"><span data-stu-id="33088-248">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="33088-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="33088-249">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="33088-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33088-250">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="33088-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="33088-251">System-Only</span></span>            | <span data-ttu-id="33088-252">True</span><span class="sxs-lookup"><span data-stu-id="33088-252">True</span></span>                                   |
| <span data-ttu-id="33088-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="33088-253">Is-Single-Valued</span></span>       | <span data-ttu-id="33088-254">True</span><span class="sxs-lookup"><span data-stu-id="33088-254">True</span></span>                                   |
| <span data-ttu-id="33088-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="33088-255">Is Indexed</span></span>             | <span data-ttu-id="33088-256">Falso</span><span class="sxs-lookup"><span data-stu-id="33088-256">False</span></span>                                  |
| <span data-ttu-id="33088-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="33088-257">In Global Catalog</span></span>      | <span data-ttu-id="33088-258">Falso</span><span class="sxs-lookup"><span data-stu-id="33088-258">False</span></span>                                  |
| <span data-ttu-id="33088-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="33088-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="33088-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="33088-260">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="33088-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33088-261">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="33088-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33088-262">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="33088-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33088-263">Search-Flags</span></span>           | <span data-ttu-id="33088-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33088-264">0x00000000</span></span>                             |
| <span data-ttu-id="33088-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33088-265">System-Flags</span></span>           | <span data-ttu-id="33088-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="33088-266">0x00000011</span></span>                             |
| <span data-ttu-id="33088-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="33088-267">Classes used in</span></span>        | [<span data-ttu-id="33088-268">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="33088-268">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





