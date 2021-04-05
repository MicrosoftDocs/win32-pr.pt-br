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
# <a name="ms-ds-has-master-ncs-attribute"></a><span data-ttu-id="3d605-106">atributo ms-DS-tem-Master-NCs</span><span class="sxs-lookup"><span data-stu-id="3d605-106">ms-DS-Has-Master-NCs attribute</span></span>

<span data-ttu-id="3d605-107">Contém os contextos de nomenclatura mantidos por um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="3d605-107">Contains the naming contexts held by a domain controller.</span></span> <span data-ttu-id="3d605-108">Esse atributo é substituído por-Master-NCs.</span><span class="sxs-lookup"><span data-stu-id="3d605-108">This attribute deprecates has-Master-NCs.</span></span>



| <span data-ttu-id="3d605-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="3d605-109">Entry</span></span> | <span data-ttu-id="3d605-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3d605-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="3d605-111">CN</span><span class="sxs-lookup"><span data-stu-id="3d605-111">CN</span></span>                | <span data-ttu-id="3d605-112">ms-DS-tem-mestre-NCs</span><span class="sxs-lookup"><span data-stu-id="3d605-112">ms-DS-Has-Master-NCs</span></span>                    |
| <span data-ttu-id="3d605-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3d605-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3d605-114">msDS-hasMasterNCs</span><span class="sxs-lookup"><span data-stu-id="3d605-114">msDS-hasMasterNCs</span></span>                       |
| <span data-ttu-id="3d605-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="3d605-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="3d605-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="3d605-116">Update Privilege</span></span>  | <span data-ttu-id="3d605-117">Esse valor é definido pelo sistema</span><span class="sxs-lookup"><span data-stu-id="3d605-117">This value is set by the system</span></span>         |
| <span data-ttu-id="3d605-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="3d605-118">Update Frequency</span></span>  | <span data-ttu-id="3d605-119">Cada vez que um novo NC é criado.</span><span class="sxs-lookup"><span data-stu-id="3d605-119">Each time a new NC is created.</span></span>          |
| <span data-ttu-id="3d605-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3d605-120">Attribute-Id</span></span>      | <span data-ttu-id="3d605-121">1.2.840.113556.1.4.1836</span><span class="sxs-lookup"><span data-stu-id="3d605-121">1.2.840.113556.1.4.1836</span></span>                 |
| <span data-ttu-id="3d605-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3d605-122">System-Id-Guid</span></span>    | <span data-ttu-id="3d605-123">ae2de0e2-59d7-4d47-8d47-ed4dfe4357ad</span><span class="sxs-lookup"><span data-stu-id="3d605-123">ae2de0e2-59d7-4d47-8d47-ed4dfe4357ad</span></span>    |
| <span data-ttu-id="3d605-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d605-124">Syntax</span></span>            | [<span data-ttu-id="3d605-125">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="3d605-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="3d605-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="3d605-126">Implementations</span></span>

-   [<span data-ttu-id="3d605-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3d605-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3d605-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="3d605-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3d605-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3d605-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3d605-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3d605-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3d605-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3d605-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3d605-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3d605-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="3d605-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3d605-133">Windows Server 2003</span></span>



| <span data-ttu-id="3d605-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="3d605-134">Entry</span></span> | <span data-ttu-id="3d605-135">Valor</span><span class="sxs-lookup"><span data-stu-id="3d605-135">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3d605-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="3d605-136">Link-Id</span></span>                | <span data-ttu-id="3d605-137">2036</span><span class="sxs-lookup"><span data-stu-id="3d605-137">2036</span></span>                                     |
| <span data-ttu-id="3d605-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d605-138">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="3d605-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d605-139">System-Only</span></span>            | <span data-ttu-id="3d605-140">True</span><span class="sxs-lookup"><span data-stu-id="3d605-140">True</span></span>                                     |
| <span data-ttu-id="3d605-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3d605-141">Is-Single-Valued</span></span>       | <span data-ttu-id="3d605-142">Falso</span><span class="sxs-lookup"><span data-stu-id="3d605-142">False</span></span>                                    |
| <span data-ttu-id="3d605-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="3d605-143">Is Indexed</span></span>             | <span data-ttu-id="3d605-144">Falso</span><span class="sxs-lookup"><span data-stu-id="3d605-144">False</span></span>                                    |
| <span data-ttu-id="3d605-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3d605-145">In Global Catalog</span></span>      | <span data-ttu-id="3d605-146">Falso</span><span class="sxs-lookup"><span data-stu-id="3d605-146">False</span></span>                                    |
| <span data-ttu-id="3d605-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3d605-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d605-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3d605-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3d605-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d605-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3d605-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d605-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3d605-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d605-151">Search-Flags</span></span>           | <span data-ttu-id="3d605-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d605-152">0x00000000</span></span>                               |
| <span data-ttu-id="3d605-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d605-153">System-Flags</span></span>           | <span data-ttu-id="3d605-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d605-154">0x00000010</span></span>                               |
| <span data-ttu-id="3d605-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3d605-155">Classes used in</span></span>        | [<span data-ttu-id="3d605-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3d605-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="3d605-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="3d605-157">ADAM</span></span>



| <span data-ttu-id="3d605-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="3d605-158">Entry</span></span> | <span data-ttu-id="3d605-159">Valor</span><span class="sxs-lookup"><span data-stu-id="3d605-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3d605-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="3d605-160">Link-Id</span></span>                | <span data-ttu-id="3d605-161">2036</span><span class="sxs-lookup"><span data-stu-id="3d605-161">2036</span></span>                                     |
| <span data-ttu-id="3d605-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d605-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="3d605-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d605-163">System-Only</span></span>            | <span data-ttu-id="3d605-164">True</span><span class="sxs-lookup"><span data-stu-id="3d605-164">True</span></span>                                     |
| <span data-ttu-id="3d605-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3d605-165">Is-Single-Valued</span></span>       | <span data-ttu-id="3d605-166">Falso</span><span class="sxs-lookup"><span data-stu-id="3d605-166">False</span></span>                                    |
| <span data-ttu-id="3d605-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="3d605-167">Is Indexed</span></span>             | <span data-ttu-id="3d605-168">Falso</span><span class="sxs-lookup"><span data-stu-id="3d605-168">False</span></span>                                    |
| <span data-ttu-id="3d605-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3d605-169">In Global Catalog</span></span>      | <span data-ttu-id="3d605-170">Falso</span><span class="sxs-lookup"><span data-stu-id="3d605-170">False</span></span>                                    |
| <span data-ttu-id="3d605-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3d605-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d605-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3d605-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3d605-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d605-173">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3d605-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d605-174">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3d605-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d605-175">Search-Flags</span></span>           | <span data-ttu-id="3d605-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d605-176">0x00000000</span></span>                               |
| <span data-ttu-id="3d605-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d605-177">System-Flags</span></span>           | <span data-ttu-id="3d605-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d605-178">0x00000010</span></span>                               |
| <span data-ttu-id="3d605-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3d605-179">Classes used in</span></span>        | [<span data-ttu-id="3d605-180">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3d605-180">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3d605-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3d605-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3d605-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="3d605-182">Entry</span></span> | <span data-ttu-id="3d605-183">Valor</span><span class="sxs-lookup"><span data-stu-id="3d605-183">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3d605-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="3d605-184">Link-Id</span></span>                | <span data-ttu-id="3d605-185">2036</span><span class="sxs-lookup"><span data-stu-id="3d605-185">2036</span></span>                                     |
| <span data-ttu-id="3d605-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d605-186">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="3d605-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d605-187">System-Only</span></span>            | <span data-ttu-id="3d605-188">True</span><span class="sxs-lookup"><span data-stu-id="3d605-188">True</span></span>                                     |
| <span data-ttu-id="3d605-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3d605-189">Is-Single-Valued</span></span>       | <span data-ttu-id="3d605-190">Falso</span><span class="sxs-lookup"><span data-stu-id="3d605-190">False</span></span>                                    |
| <span data-ttu-id="3d605-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="3d605-191">Is Indexed</span></span>             | <span data-ttu-id="3d605-192">Falso</span><span class="sxs-lookup"><span data-stu-id="3d605-192">False</span></span>                                    |
| <span data-ttu-id="3d605-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3d605-193">In Global Catalog</span></span>      | <span data-ttu-id="3d605-194">Falso</span><span class="sxs-lookup"><span data-stu-id="3d605-194">False</span></span>                                    |
| <span data-ttu-id="3d605-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3d605-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d605-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3d605-196">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3d605-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d605-197">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3d605-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d605-198">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3d605-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d605-199">Search-Flags</span></span>           | <span data-ttu-id="3d605-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d605-200">0x00000000</span></span>                               |
| <span data-ttu-id="3d605-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d605-201">System-Flags</span></span>           | <span data-ttu-id="3d605-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d605-202">0x00000010</span></span>                               |
| <span data-ttu-id="3d605-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3d605-203">Classes used in</span></span>        | [<span data-ttu-id="3d605-204">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3d605-204">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3d605-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d605-205">Windows Server 2008</span></span>



| <span data-ttu-id="3d605-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="3d605-206">Entry</span></span> | <span data-ttu-id="3d605-207">Valor</span><span class="sxs-lookup"><span data-stu-id="3d605-207">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3d605-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="3d605-208">Link-Id</span></span>                | <span data-ttu-id="3d605-209">2036</span><span class="sxs-lookup"><span data-stu-id="3d605-209">2036</span></span>                                     |
| <span data-ttu-id="3d605-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d605-210">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="3d605-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d605-211">System-Only</span></span>            | <span data-ttu-id="3d605-212">True</span><span class="sxs-lookup"><span data-stu-id="3d605-212">True</span></span>                                     |
| <span data-ttu-id="3d605-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3d605-213">Is-Single-Valued</span></span>       | <span data-ttu-id="3d605-214">Falso</span><span class="sxs-lookup"><span data-stu-id="3d605-214">False</span></span>                                    |
| <span data-ttu-id="3d605-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="3d605-215">Is Indexed</span></span>             | <span data-ttu-id="3d605-216">Falso</span><span class="sxs-lookup"><span data-stu-id="3d605-216">False</span></span>                                    |
| <span data-ttu-id="3d605-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3d605-217">In Global Catalog</span></span>      | <span data-ttu-id="3d605-218">Falso</span><span class="sxs-lookup"><span data-stu-id="3d605-218">False</span></span>                                    |
| <span data-ttu-id="3d605-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3d605-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d605-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3d605-220">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3d605-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d605-221">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3d605-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d605-222">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3d605-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d605-223">Search-Flags</span></span>           | <span data-ttu-id="3d605-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d605-224">0x00000000</span></span>                               |
| <span data-ttu-id="3d605-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d605-225">System-Flags</span></span>           | <span data-ttu-id="3d605-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d605-226">0x00000010</span></span>                               |
| <span data-ttu-id="3d605-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3d605-227">Classes used in</span></span>        | [<span data-ttu-id="3d605-228">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3d605-228">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3d605-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3d605-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3d605-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="3d605-230">Entry</span></span> | <span data-ttu-id="3d605-231">Valor</span><span class="sxs-lookup"><span data-stu-id="3d605-231">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3d605-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="3d605-232">Link-Id</span></span>                | <span data-ttu-id="3d605-233">2036</span><span class="sxs-lookup"><span data-stu-id="3d605-233">2036</span></span>                                     |
| <span data-ttu-id="3d605-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d605-234">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="3d605-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d605-235">System-Only</span></span>            | <span data-ttu-id="3d605-236">True</span><span class="sxs-lookup"><span data-stu-id="3d605-236">True</span></span>                                     |
| <span data-ttu-id="3d605-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3d605-237">Is-Single-Valued</span></span>       | <span data-ttu-id="3d605-238">Falso</span><span class="sxs-lookup"><span data-stu-id="3d605-238">False</span></span>                                    |
| <span data-ttu-id="3d605-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="3d605-239">Is Indexed</span></span>             | <span data-ttu-id="3d605-240">Falso</span><span class="sxs-lookup"><span data-stu-id="3d605-240">False</span></span>                                    |
| <span data-ttu-id="3d605-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3d605-241">In Global Catalog</span></span>      | <span data-ttu-id="3d605-242">Falso</span><span class="sxs-lookup"><span data-stu-id="3d605-242">False</span></span>                                    |
| <span data-ttu-id="3d605-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3d605-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d605-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3d605-244">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3d605-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d605-245">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3d605-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d605-246">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3d605-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d605-247">Search-Flags</span></span>           | <span data-ttu-id="3d605-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d605-248">0x00000000</span></span>                               |
| <span data-ttu-id="3d605-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d605-249">System-Flags</span></span>           | <span data-ttu-id="3d605-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d605-250">0x00000010</span></span>                               |
| <span data-ttu-id="3d605-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3d605-251">Classes used in</span></span>        | [<span data-ttu-id="3d605-252">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3d605-252">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3d605-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3d605-253">Windows Server 2012</span></span>



| <span data-ttu-id="3d605-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="3d605-254">Entry</span></span> | <span data-ttu-id="3d605-255">Valor</span><span class="sxs-lookup"><span data-stu-id="3d605-255">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3d605-256">ID do link</span><span class="sxs-lookup"><span data-stu-id="3d605-256">Link-Id</span></span>                | <span data-ttu-id="3d605-257">2036</span><span class="sxs-lookup"><span data-stu-id="3d605-257">2036</span></span>                                     |
| <span data-ttu-id="3d605-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d605-258">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="3d605-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d605-259">System-Only</span></span>            | <span data-ttu-id="3d605-260">True</span><span class="sxs-lookup"><span data-stu-id="3d605-260">True</span></span>                                     |
| <span data-ttu-id="3d605-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3d605-261">Is-Single-Valued</span></span>       | <span data-ttu-id="3d605-262">Falso</span><span class="sxs-lookup"><span data-stu-id="3d605-262">False</span></span>                                    |
| <span data-ttu-id="3d605-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="3d605-263">Is Indexed</span></span>             | <span data-ttu-id="3d605-264">Falso</span><span class="sxs-lookup"><span data-stu-id="3d605-264">False</span></span>                                    |
| <span data-ttu-id="3d605-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3d605-265">In Global Catalog</span></span>      | <span data-ttu-id="3d605-266">Falso</span><span class="sxs-lookup"><span data-stu-id="3d605-266">False</span></span>                                    |
| <span data-ttu-id="3d605-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3d605-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d605-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3d605-268">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3d605-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d605-269">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3d605-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d605-270">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3d605-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d605-271">Search-Flags</span></span>           | <span data-ttu-id="3d605-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d605-272">0x00000000</span></span>                               |
| <span data-ttu-id="3d605-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d605-273">System-Flags</span></span>           | <span data-ttu-id="3d605-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d605-274">0x00000010</span></span>                               |
| <span data-ttu-id="3d605-275">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3d605-275">Classes used in</span></span>        | [<span data-ttu-id="3d605-276">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3d605-276">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





