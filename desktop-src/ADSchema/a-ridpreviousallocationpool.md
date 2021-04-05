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
# <a name="rid-previous-allocation-pool-attribute"></a><span data-ttu-id="42f67-105">Atributo RID-Previous-Allocation-pool</span><span class="sxs-lookup"><span data-stu-id="42f67-105">RID-Previous-Allocation-Pool attribute</span></span>

<span data-ttu-id="42f67-106">O atributo **RID-Previous-Alloc-pool** contém o pool de RIDs (identificadores relativos) do qual um controlador de domínio se aloca.</span><span class="sxs-lookup"><span data-stu-id="42f67-106">The **RID-Previous-Allocation-Pool** attribute contains the pool of relative identifiers (RIDs) that a domain controller allocates from.</span></span> <span data-ttu-id="42f67-107">Esse atributo é um valor de oito bytes que contém um par de inteiros de quatro bytes que representam os valores de início e término do pool de RIDs.</span><span class="sxs-lookup"><span data-stu-id="42f67-107">This attribute is an eight-byte value that contains a pair of four-byte integers that represent the start and end values of the RID pool.</span></span> <span data-ttu-id="42f67-108">O valor inicial está nos quatro bytes inferiores e o valor final está nos quatro bytes superiores.</span><span class="sxs-lookup"><span data-stu-id="42f67-108">The start value is in the lower four bytes and the end value is in the upper four bytes.</span></span>



| <span data-ttu-id="42f67-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="42f67-109">Entry</span></span> | <span data-ttu-id="42f67-110">Valor</span><span class="sxs-lookup"><span data-stu-id="42f67-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="42f67-111">CN</span><span class="sxs-lookup"><span data-stu-id="42f67-111">CN</span></span>                | <span data-ttu-id="42f67-112">RID-anterior-pool de alocação</span><span class="sxs-lookup"><span data-stu-id="42f67-112">RID-Previous-Allocation-Pool</span></span>         |
| <span data-ttu-id="42f67-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="42f67-113">Ldap-Display-Name</span></span> | <span data-ttu-id="42f67-114">rIDPreviousAllocationPool</span><span class="sxs-lookup"><span data-stu-id="42f67-114">rIDPreviousAllocationPool</span></span>            |
| <span data-ttu-id="42f67-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="42f67-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="42f67-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="42f67-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="42f67-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="42f67-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="42f67-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="42f67-118">Attribute-Id</span></span>      | <span data-ttu-id="42f67-119">1.2.840.113556.1.4.372</span><span class="sxs-lookup"><span data-stu-id="42f67-119">1.2.840.113556.1.4.372</span></span>               |
| <span data-ttu-id="42f67-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="42f67-120">System-Id-Guid</span></span>    | <span data-ttu-id="42f67-121">6617188a-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="42f67-121">6617188a-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="42f67-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="42f67-122">Syntax</span></span>            | [<span data-ttu-id="42f67-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="42f67-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="42f67-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="42f67-124">Implementations</span></span>

-   [<span data-ttu-id="42f67-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="42f67-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="42f67-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="42f67-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="42f67-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="42f67-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="42f67-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="42f67-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="42f67-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="42f67-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="42f67-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="42f67-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="42f67-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="42f67-131">Windows 2000 Server</span></span>



| <span data-ttu-id="42f67-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="42f67-132">Entry</span></span> | <span data-ttu-id="42f67-133">Valor</span><span class="sxs-lookup"><span data-stu-id="42f67-133">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="42f67-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="42f67-134">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="42f67-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42f67-135">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="42f67-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="42f67-136">System-Only</span></span>            | <span data-ttu-id="42f67-137">True</span><span class="sxs-lookup"><span data-stu-id="42f67-137">True</span></span>                                   |
| <span data-ttu-id="42f67-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="42f67-138">Is-Single-Valued</span></span>       | <span data-ttu-id="42f67-139">True</span><span class="sxs-lookup"><span data-stu-id="42f67-139">True</span></span>                                   |
| <span data-ttu-id="42f67-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="42f67-140">Is Indexed</span></span>             | <span data-ttu-id="42f67-141">Falso</span><span class="sxs-lookup"><span data-stu-id="42f67-141">False</span></span>                                  |
| <span data-ttu-id="42f67-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="42f67-142">In Global Catalog</span></span>      | <span data-ttu-id="42f67-143">Falso</span><span class="sxs-lookup"><span data-stu-id="42f67-143">False</span></span>                                  |
| <span data-ttu-id="42f67-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="42f67-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="42f67-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="42f67-145">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="42f67-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42f67-146">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="42f67-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42f67-147">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="42f67-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42f67-148">Search-Flags</span></span>           | <span data-ttu-id="42f67-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42f67-149">0x00000000</span></span>                             |
| <span data-ttu-id="42f67-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42f67-150">System-Flags</span></span>           | <span data-ttu-id="42f67-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="42f67-151">0x00000011</span></span>                             |
| <span data-ttu-id="42f67-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="42f67-152">Classes used in</span></span>        | [<span data-ttu-id="42f67-153">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="42f67-153">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="42f67-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="42f67-154">Windows Server 2003</span></span>



| <span data-ttu-id="42f67-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="42f67-155">Entry</span></span> | <span data-ttu-id="42f67-156">Valor</span><span class="sxs-lookup"><span data-stu-id="42f67-156">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="42f67-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="42f67-157">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="42f67-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42f67-158">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="42f67-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="42f67-159">System-Only</span></span>            | <span data-ttu-id="42f67-160">True</span><span class="sxs-lookup"><span data-stu-id="42f67-160">True</span></span>                                   |
| <span data-ttu-id="42f67-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="42f67-161">Is-Single-Valued</span></span>       | <span data-ttu-id="42f67-162">True</span><span class="sxs-lookup"><span data-stu-id="42f67-162">True</span></span>                                   |
| <span data-ttu-id="42f67-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="42f67-163">Is Indexed</span></span>             | <span data-ttu-id="42f67-164">Falso</span><span class="sxs-lookup"><span data-stu-id="42f67-164">False</span></span>                                  |
| <span data-ttu-id="42f67-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="42f67-165">In Global Catalog</span></span>      | <span data-ttu-id="42f67-166">Falso</span><span class="sxs-lookup"><span data-stu-id="42f67-166">False</span></span>                                  |
| <span data-ttu-id="42f67-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="42f67-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="42f67-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="42f67-168">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="42f67-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42f67-169">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="42f67-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42f67-170">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="42f67-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42f67-171">Search-Flags</span></span>           | <span data-ttu-id="42f67-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42f67-172">0x00000000</span></span>                             |
| <span data-ttu-id="42f67-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42f67-173">System-Flags</span></span>           | <span data-ttu-id="42f67-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="42f67-174">0x00000011</span></span>                             |
| <span data-ttu-id="42f67-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="42f67-175">Classes used in</span></span>        | [<span data-ttu-id="42f67-176">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="42f67-176">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="42f67-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="42f67-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="42f67-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="42f67-178">Entry</span></span> | <span data-ttu-id="42f67-179">Valor</span><span class="sxs-lookup"><span data-stu-id="42f67-179">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="42f67-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="42f67-180">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="42f67-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42f67-181">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="42f67-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="42f67-182">System-Only</span></span>            | <span data-ttu-id="42f67-183">True</span><span class="sxs-lookup"><span data-stu-id="42f67-183">True</span></span>                                   |
| <span data-ttu-id="42f67-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="42f67-184">Is-Single-Valued</span></span>       | <span data-ttu-id="42f67-185">True</span><span class="sxs-lookup"><span data-stu-id="42f67-185">True</span></span>                                   |
| <span data-ttu-id="42f67-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="42f67-186">Is Indexed</span></span>             | <span data-ttu-id="42f67-187">Falso</span><span class="sxs-lookup"><span data-stu-id="42f67-187">False</span></span>                                  |
| <span data-ttu-id="42f67-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="42f67-188">In Global Catalog</span></span>      | <span data-ttu-id="42f67-189">Falso</span><span class="sxs-lookup"><span data-stu-id="42f67-189">False</span></span>                                  |
| <span data-ttu-id="42f67-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="42f67-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="42f67-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="42f67-191">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="42f67-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42f67-192">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="42f67-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42f67-193">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="42f67-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42f67-194">Search-Flags</span></span>           | <span data-ttu-id="42f67-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42f67-195">0x00000000</span></span>                             |
| <span data-ttu-id="42f67-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42f67-196">System-Flags</span></span>           | <span data-ttu-id="42f67-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="42f67-197">0x00000011</span></span>                             |
| <span data-ttu-id="42f67-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="42f67-198">Classes used in</span></span>        | [<span data-ttu-id="42f67-199">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="42f67-199">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="42f67-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42f67-200">Windows Server 2008</span></span>



| <span data-ttu-id="42f67-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="42f67-201">Entry</span></span> | <span data-ttu-id="42f67-202">Valor</span><span class="sxs-lookup"><span data-stu-id="42f67-202">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="42f67-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="42f67-203">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="42f67-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42f67-204">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="42f67-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="42f67-205">System-Only</span></span>            | <span data-ttu-id="42f67-206">True</span><span class="sxs-lookup"><span data-stu-id="42f67-206">True</span></span>                                   |
| <span data-ttu-id="42f67-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="42f67-207">Is-Single-Valued</span></span>       | <span data-ttu-id="42f67-208">True</span><span class="sxs-lookup"><span data-stu-id="42f67-208">True</span></span>                                   |
| <span data-ttu-id="42f67-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="42f67-209">Is Indexed</span></span>             | <span data-ttu-id="42f67-210">Falso</span><span class="sxs-lookup"><span data-stu-id="42f67-210">False</span></span>                                  |
| <span data-ttu-id="42f67-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="42f67-211">In Global Catalog</span></span>      | <span data-ttu-id="42f67-212">Falso</span><span class="sxs-lookup"><span data-stu-id="42f67-212">False</span></span>                                  |
| <span data-ttu-id="42f67-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="42f67-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="42f67-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="42f67-214">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="42f67-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42f67-215">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="42f67-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42f67-216">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="42f67-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42f67-217">Search-Flags</span></span>           | <span data-ttu-id="42f67-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42f67-218">0x00000000</span></span>                             |
| <span data-ttu-id="42f67-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42f67-219">System-Flags</span></span>           | <span data-ttu-id="42f67-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="42f67-220">0x00000011</span></span>                             |
| <span data-ttu-id="42f67-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="42f67-221">Classes used in</span></span>        | [<span data-ttu-id="42f67-222">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="42f67-222">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="42f67-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="42f67-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="42f67-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="42f67-224">Entry</span></span> | <span data-ttu-id="42f67-225">Valor</span><span class="sxs-lookup"><span data-stu-id="42f67-225">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="42f67-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="42f67-226">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="42f67-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42f67-227">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="42f67-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="42f67-228">System-Only</span></span>            | <span data-ttu-id="42f67-229">True</span><span class="sxs-lookup"><span data-stu-id="42f67-229">True</span></span>                                   |
| <span data-ttu-id="42f67-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="42f67-230">Is-Single-Valued</span></span>       | <span data-ttu-id="42f67-231">True</span><span class="sxs-lookup"><span data-stu-id="42f67-231">True</span></span>                                   |
| <span data-ttu-id="42f67-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="42f67-232">Is Indexed</span></span>             | <span data-ttu-id="42f67-233">Falso</span><span class="sxs-lookup"><span data-stu-id="42f67-233">False</span></span>                                  |
| <span data-ttu-id="42f67-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="42f67-234">In Global Catalog</span></span>      | <span data-ttu-id="42f67-235">Falso</span><span class="sxs-lookup"><span data-stu-id="42f67-235">False</span></span>                                  |
| <span data-ttu-id="42f67-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="42f67-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="42f67-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="42f67-237">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="42f67-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42f67-238">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="42f67-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42f67-239">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="42f67-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42f67-240">Search-Flags</span></span>           | <span data-ttu-id="42f67-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42f67-241">0x00000000</span></span>                             |
| <span data-ttu-id="42f67-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42f67-242">System-Flags</span></span>           | <span data-ttu-id="42f67-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="42f67-243">0x00000011</span></span>                             |
| <span data-ttu-id="42f67-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="42f67-244">Classes used in</span></span>        | [<span data-ttu-id="42f67-245">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="42f67-245">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="42f67-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="42f67-246">Windows Server 2012</span></span>



| <span data-ttu-id="42f67-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="42f67-247">Entry</span></span> | <span data-ttu-id="42f67-248">Valor</span><span class="sxs-lookup"><span data-stu-id="42f67-248">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="42f67-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="42f67-249">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="42f67-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42f67-250">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="42f67-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="42f67-251">System-Only</span></span>            | <span data-ttu-id="42f67-252">True</span><span class="sxs-lookup"><span data-stu-id="42f67-252">True</span></span>                                   |
| <span data-ttu-id="42f67-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="42f67-253">Is-Single-Valued</span></span>       | <span data-ttu-id="42f67-254">True</span><span class="sxs-lookup"><span data-stu-id="42f67-254">True</span></span>                                   |
| <span data-ttu-id="42f67-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="42f67-255">Is Indexed</span></span>             | <span data-ttu-id="42f67-256">Falso</span><span class="sxs-lookup"><span data-stu-id="42f67-256">False</span></span>                                  |
| <span data-ttu-id="42f67-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="42f67-257">In Global Catalog</span></span>      | <span data-ttu-id="42f67-258">Falso</span><span class="sxs-lookup"><span data-stu-id="42f67-258">False</span></span>                                  |
| <span data-ttu-id="42f67-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="42f67-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="42f67-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="42f67-260">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="42f67-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42f67-261">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="42f67-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42f67-262">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="42f67-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42f67-263">Search-Flags</span></span>           | <span data-ttu-id="42f67-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42f67-264">0x00000000</span></span>                             |
| <span data-ttu-id="42f67-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42f67-265">System-Flags</span></span>           | <span data-ttu-id="42f67-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="42f67-266">0x00000011</span></span>                             |
| <span data-ttu-id="42f67-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="42f67-267">Classes used in</span></span>        | [<span data-ttu-id="42f67-268">**RID-definido**</span><span class="sxs-lookup"><span data-stu-id="42f67-268">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





