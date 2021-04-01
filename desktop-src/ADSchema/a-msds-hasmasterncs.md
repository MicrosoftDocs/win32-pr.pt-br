---
title: atributo ms-DS-tem-Master-NCs
description: Contém os contextos de nomenclatura mantidos por um controlador de domínio. Esse atributo é substituído por-Master-NCs.
ms.assetid: 5325db42-afd7-472c-8797-447e752a3907
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DS-tem-Master-NCs
- atributo msDS-hasMasterNCs do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Has-Master-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24507460eaa7653cfc2c98d3772942de9936162c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825367"
---
# <a name="ms-ds-has-master-ncs-attribute"></a><span data-ttu-id="96391-106">atributo ms-DS-tem-Master-NCs</span><span class="sxs-lookup"><span data-stu-id="96391-106">ms-DS-Has-Master-NCs attribute</span></span>

<span data-ttu-id="96391-107">Contém os contextos de nomenclatura mantidos por um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="96391-107">Contains the naming contexts held by a domain controller.</span></span> <span data-ttu-id="96391-108">Esse atributo é substituído por-Master-NCs.</span><span class="sxs-lookup"><span data-stu-id="96391-108">This attribute deprecates has-Master-NCs.</span></span>



| <span data-ttu-id="96391-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="96391-109">Entry</span></span> | <span data-ttu-id="96391-110">Valor</span><span class="sxs-lookup"><span data-stu-id="96391-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="96391-111">CN</span><span class="sxs-lookup"><span data-stu-id="96391-111">CN</span></span>                | <span data-ttu-id="96391-112">ms-DS-tem-mestre-NCs</span><span class="sxs-lookup"><span data-stu-id="96391-112">ms-DS-Has-Master-NCs</span></span>                    |
| <span data-ttu-id="96391-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="96391-113">Ldap-Display-Name</span></span> | <span data-ttu-id="96391-114">msDS-hasMasterNCs</span><span class="sxs-lookup"><span data-stu-id="96391-114">msDS-hasMasterNCs</span></span>                       |
| <span data-ttu-id="96391-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="96391-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="96391-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="96391-116">Update Privilege</span></span>  | <span data-ttu-id="96391-117">Esse valor é definido pelo sistema</span><span class="sxs-lookup"><span data-stu-id="96391-117">This value is set by the system</span></span>         |
| <span data-ttu-id="96391-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="96391-118">Update Frequency</span></span>  | <span data-ttu-id="96391-119">Cada vez que um novo NC é criado.</span><span class="sxs-lookup"><span data-stu-id="96391-119">Each time a new NC is created.</span></span>          |
| <span data-ttu-id="96391-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="96391-120">Attribute-Id</span></span>      | <span data-ttu-id="96391-121">1.2.840.113556.1.4.1836</span><span class="sxs-lookup"><span data-stu-id="96391-121">1.2.840.113556.1.4.1836</span></span>                 |
| <span data-ttu-id="96391-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="96391-122">System-Id-Guid</span></span>    | <span data-ttu-id="96391-123">ae2de0e2-59d7-4d47-8d47-ed4dfe4357ad</span><span class="sxs-lookup"><span data-stu-id="96391-123">ae2de0e2-59d7-4d47-8d47-ed4dfe4357ad</span></span>    |
| <span data-ttu-id="96391-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="96391-124">Syntax</span></span>            | [<span data-ttu-id="96391-125">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="96391-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="96391-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="96391-126">Implementations</span></span>

-   [<span data-ttu-id="96391-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="96391-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="96391-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="96391-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="96391-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="96391-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="96391-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="96391-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="96391-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="96391-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="96391-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="96391-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="96391-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="96391-133">Windows Server 2003</span></span>



| <span data-ttu-id="96391-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="96391-134">Entry</span></span> | <span data-ttu-id="96391-135">Valor</span><span class="sxs-lookup"><span data-stu-id="96391-135">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="96391-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="96391-136">Link-Id</span></span>                | <span data-ttu-id="96391-137">2036</span><span class="sxs-lookup"><span data-stu-id="96391-137">2036</span></span>                                     |
| <span data-ttu-id="96391-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96391-138">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="96391-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="96391-139">System-Only</span></span>            | <span data-ttu-id="96391-140">True</span><span class="sxs-lookup"><span data-stu-id="96391-140">True</span></span>                                     |
| <span data-ttu-id="96391-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="96391-141">Is-Single-Valued</span></span>       | <span data-ttu-id="96391-142">Falso</span><span class="sxs-lookup"><span data-stu-id="96391-142">False</span></span>                                    |
| <span data-ttu-id="96391-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="96391-143">Is Indexed</span></span>             | <span data-ttu-id="96391-144">Falso</span><span class="sxs-lookup"><span data-stu-id="96391-144">False</span></span>                                    |
| <span data-ttu-id="96391-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="96391-145">In Global Catalog</span></span>      | <span data-ttu-id="96391-146">Falso</span><span class="sxs-lookup"><span data-stu-id="96391-146">False</span></span>                                    |
| <span data-ttu-id="96391-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96391-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="96391-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="96391-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="96391-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96391-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="96391-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96391-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="96391-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96391-151">Search-Flags</span></span>           | <span data-ttu-id="96391-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96391-152">0x00000000</span></span>                               |
| <span data-ttu-id="96391-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96391-153">System-Flags</span></span>           | <span data-ttu-id="96391-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96391-154">0x00000010</span></span>                               |
| <span data-ttu-id="96391-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="96391-155">Classes used in</span></span>        | [<span data-ttu-id="96391-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="96391-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="96391-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="96391-157">ADAM</span></span>



| <span data-ttu-id="96391-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="96391-158">Entry</span></span> | <span data-ttu-id="96391-159">Valor</span><span class="sxs-lookup"><span data-stu-id="96391-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="96391-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="96391-160">Link-Id</span></span>                | <span data-ttu-id="96391-161">2036</span><span class="sxs-lookup"><span data-stu-id="96391-161">2036</span></span>                                     |
| <span data-ttu-id="96391-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96391-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="96391-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="96391-163">System-Only</span></span>            | <span data-ttu-id="96391-164">True</span><span class="sxs-lookup"><span data-stu-id="96391-164">True</span></span>                                     |
| <span data-ttu-id="96391-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="96391-165">Is-Single-Valued</span></span>       | <span data-ttu-id="96391-166">Falso</span><span class="sxs-lookup"><span data-stu-id="96391-166">False</span></span>                                    |
| <span data-ttu-id="96391-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="96391-167">Is Indexed</span></span>             | <span data-ttu-id="96391-168">Falso</span><span class="sxs-lookup"><span data-stu-id="96391-168">False</span></span>                                    |
| <span data-ttu-id="96391-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="96391-169">In Global Catalog</span></span>      | <span data-ttu-id="96391-170">Falso</span><span class="sxs-lookup"><span data-stu-id="96391-170">False</span></span>                                    |
| <span data-ttu-id="96391-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96391-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="96391-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="96391-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="96391-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96391-173">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="96391-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96391-174">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="96391-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96391-175">Search-Flags</span></span>           | <span data-ttu-id="96391-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96391-176">0x00000000</span></span>                               |
| <span data-ttu-id="96391-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96391-177">System-Flags</span></span>           | <span data-ttu-id="96391-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96391-178">0x00000010</span></span>                               |
| <span data-ttu-id="96391-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="96391-179">Classes used in</span></span>        | [<span data-ttu-id="96391-180">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="96391-180">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="96391-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="96391-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="96391-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="96391-182">Entry</span></span> | <span data-ttu-id="96391-183">Valor</span><span class="sxs-lookup"><span data-stu-id="96391-183">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="96391-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="96391-184">Link-Id</span></span>                | <span data-ttu-id="96391-185">2036</span><span class="sxs-lookup"><span data-stu-id="96391-185">2036</span></span>                                     |
| <span data-ttu-id="96391-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96391-186">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="96391-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="96391-187">System-Only</span></span>            | <span data-ttu-id="96391-188">True</span><span class="sxs-lookup"><span data-stu-id="96391-188">True</span></span>                                     |
| <span data-ttu-id="96391-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="96391-189">Is-Single-Valued</span></span>       | <span data-ttu-id="96391-190">Falso</span><span class="sxs-lookup"><span data-stu-id="96391-190">False</span></span>                                    |
| <span data-ttu-id="96391-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="96391-191">Is Indexed</span></span>             | <span data-ttu-id="96391-192">Falso</span><span class="sxs-lookup"><span data-stu-id="96391-192">False</span></span>                                    |
| <span data-ttu-id="96391-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="96391-193">In Global Catalog</span></span>      | <span data-ttu-id="96391-194">Falso</span><span class="sxs-lookup"><span data-stu-id="96391-194">False</span></span>                                    |
| <span data-ttu-id="96391-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96391-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="96391-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="96391-196">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="96391-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96391-197">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="96391-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96391-198">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="96391-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96391-199">Search-Flags</span></span>           | <span data-ttu-id="96391-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96391-200">0x00000000</span></span>                               |
| <span data-ttu-id="96391-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96391-201">System-Flags</span></span>           | <span data-ttu-id="96391-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96391-202">0x00000010</span></span>                               |
| <span data-ttu-id="96391-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="96391-203">Classes used in</span></span>        | [<span data-ttu-id="96391-204">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="96391-204">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="96391-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96391-205">Windows Server 2008</span></span>



| <span data-ttu-id="96391-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="96391-206">Entry</span></span> | <span data-ttu-id="96391-207">Valor</span><span class="sxs-lookup"><span data-stu-id="96391-207">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="96391-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="96391-208">Link-Id</span></span>                | <span data-ttu-id="96391-209">2036</span><span class="sxs-lookup"><span data-stu-id="96391-209">2036</span></span>                                     |
| <span data-ttu-id="96391-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96391-210">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="96391-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="96391-211">System-Only</span></span>            | <span data-ttu-id="96391-212">True</span><span class="sxs-lookup"><span data-stu-id="96391-212">True</span></span>                                     |
| <span data-ttu-id="96391-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="96391-213">Is-Single-Valued</span></span>       | <span data-ttu-id="96391-214">Falso</span><span class="sxs-lookup"><span data-stu-id="96391-214">False</span></span>                                    |
| <span data-ttu-id="96391-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="96391-215">Is Indexed</span></span>             | <span data-ttu-id="96391-216">Falso</span><span class="sxs-lookup"><span data-stu-id="96391-216">False</span></span>                                    |
| <span data-ttu-id="96391-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="96391-217">In Global Catalog</span></span>      | <span data-ttu-id="96391-218">Falso</span><span class="sxs-lookup"><span data-stu-id="96391-218">False</span></span>                                    |
| <span data-ttu-id="96391-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96391-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="96391-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="96391-220">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="96391-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96391-221">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="96391-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96391-222">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="96391-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96391-223">Search-Flags</span></span>           | <span data-ttu-id="96391-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96391-224">0x00000000</span></span>                               |
| <span data-ttu-id="96391-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96391-225">System-Flags</span></span>           | <span data-ttu-id="96391-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96391-226">0x00000010</span></span>                               |
| <span data-ttu-id="96391-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="96391-227">Classes used in</span></span>        | [<span data-ttu-id="96391-228">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="96391-228">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="96391-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="96391-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="96391-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="96391-230">Entry</span></span> | <span data-ttu-id="96391-231">Valor</span><span class="sxs-lookup"><span data-stu-id="96391-231">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="96391-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="96391-232">Link-Id</span></span>                | <span data-ttu-id="96391-233">2036</span><span class="sxs-lookup"><span data-stu-id="96391-233">2036</span></span>                                     |
| <span data-ttu-id="96391-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96391-234">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="96391-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="96391-235">System-Only</span></span>            | <span data-ttu-id="96391-236">True</span><span class="sxs-lookup"><span data-stu-id="96391-236">True</span></span>                                     |
| <span data-ttu-id="96391-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="96391-237">Is-Single-Valued</span></span>       | <span data-ttu-id="96391-238">Falso</span><span class="sxs-lookup"><span data-stu-id="96391-238">False</span></span>                                    |
| <span data-ttu-id="96391-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="96391-239">Is Indexed</span></span>             | <span data-ttu-id="96391-240">Falso</span><span class="sxs-lookup"><span data-stu-id="96391-240">False</span></span>                                    |
| <span data-ttu-id="96391-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="96391-241">In Global Catalog</span></span>      | <span data-ttu-id="96391-242">Falso</span><span class="sxs-lookup"><span data-stu-id="96391-242">False</span></span>                                    |
| <span data-ttu-id="96391-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96391-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="96391-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="96391-244">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="96391-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96391-245">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="96391-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96391-246">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="96391-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96391-247">Search-Flags</span></span>           | <span data-ttu-id="96391-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96391-248">0x00000000</span></span>                               |
| <span data-ttu-id="96391-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96391-249">System-Flags</span></span>           | <span data-ttu-id="96391-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96391-250">0x00000010</span></span>                               |
| <span data-ttu-id="96391-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="96391-251">Classes used in</span></span>        | [<span data-ttu-id="96391-252">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="96391-252">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="96391-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="96391-253">Windows Server 2012</span></span>



| <span data-ttu-id="96391-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="96391-254">Entry</span></span> | <span data-ttu-id="96391-255">Valor</span><span class="sxs-lookup"><span data-stu-id="96391-255">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="96391-256">ID do link</span><span class="sxs-lookup"><span data-stu-id="96391-256">Link-Id</span></span>                | <span data-ttu-id="96391-257">2036</span><span class="sxs-lookup"><span data-stu-id="96391-257">2036</span></span>                                     |
| <span data-ttu-id="96391-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96391-258">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="96391-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="96391-259">System-Only</span></span>            | <span data-ttu-id="96391-260">True</span><span class="sxs-lookup"><span data-stu-id="96391-260">True</span></span>                                     |
| <span data-ttu-id="96391-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="96391-261">Is-Single-Valued</span></span>       | <span data-ttu-id="96391-262">Falso</span><span class="sxs-lookup"><span data-stu-id="96391-262">False</span></span>                                    |
| <span data-ttu-id="96391-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="96391-263">Is Indexed</span></span>             | <span data-ttu-id="96391-264">Falso</span><span class="sxs-lookup"><span data-stu-id="96391-264">False</span></span>                                    |
| <span data-ttu-id="96391-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="96391-265">In Global Catalog</span></span>      | <span data-ttu-id="96391-266">Falso</span><span class="sxs-lookup"><span data-stu-id="96391-266">False</span></span>                                    |
| <span data-ttu-id="96391-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="96391-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="96391-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="96391-268">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="96391-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96391-269">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="96391-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96391-270">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="96391-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96391-271">Search-Flags</span></span>           | <span data-ttu-id="96391-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96391-272">0x00000000</span></span>                               |
| <span data-ttu-id="96391-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96391-273">System-Flags</span></span>           | <span data-ttu-id="96391-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="96391-274">0x00000010</span></span>                               |
| <span data-ttu-id="96391-275">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="96391-275">Classes used in</span></span>        | [<span data-ttu-id="96391-276">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="96391-276">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





