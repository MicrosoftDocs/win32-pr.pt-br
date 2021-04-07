---
title: Atributo tem-Master-NCs
description: O nome distinto para os contextos de nomenclatura do controlador de domínio. Link de encaminhamento do atributo Mastered-By.
ms.assetid: 77a7e693-513f-4f76-8c4f-d2ef3240323b
ms.tgt_platform: multiple
keywords:
- Tem Esquema de AD do atributo-Master-NCs
- Esquema de AD do atributo hasMasterNCs
topic_type:
- apiref
api_name:
- Has-Master-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34756c491c5228c58da1b95d4fd7b838c691f38
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919531"
---
# <a name="has-master-ncs-attribute"></a><span data-ttu-id="3ffe9-106">Atributo tem-Master-NCs</span><span class="sxs-lookup"><span data-stu-id="3ffe9-106">Has-Master-NCs attribute</span></span>

<span data-ttu-id="3ffe9-107">O nome distinto para os contextos de nomenclatura do controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="3ffe9-107">The distinguished name for the naming contexts for the DC.</span></span> <span data-ttu-id="3ffe9-108">Link de encaminhamento do atributo Mastered-By.</span><span class="sxs-lookup"><span data-stu-id="3ffe9-108">Forward link for the Mastered-By attribute.</span></span>



| <span data-ttu-id="3ffe9-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ffe9-109">Entry</span></span> | <span data-ttu-id="3ffe9-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3ffe9-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="3ffe9-111">CN</span><span class="sxs-lookup"><span data-stu-id="3ffe9-111">CN</span></span>                | <span data-ttu-id="3ffe9-112">Tem-mestre-NCs</span><span class="sxs-lookup"><span data-stu-id="3ffe9-112">Has-Master-NCs</span></span>                          |
| <span data-ttu-id="3ffe9-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3ffe9-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3ffe9-114">hasMasterNCs</span><span class="sxs-lookup"><span data-stu-id="3ffe9-114">hasMasterNCs</span></span>                            |
| <span data-ttu-id="3ffe9-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="3ffe9-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="3ffe9-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="3ffe9-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="3ffe9-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="3ffe9-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="3ffe9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3ffe9-118">Attribute-Id</span></span>      | <span data-ttu-id="3ffe9-119">1.2.840.113556.1.2.14</span><span class="sxs-lookup"><span data-stu-id="3ffe9-119">1.2.840.113556.1.2.14</span></span>                   |
| <span data-ttu-id="3ffe9-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3ffe9-120">System-Id-Guid</span></span>    | <span data-ttu-id="3ffe9-121">bf967982-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3ffe9-121">bf967982-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="3ffe9-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ffe9-122">Syntax</span></span>            | [<span data-ttu-id="3ffe9-123">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="3ffe9-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="3ffe9-124">Implementations</span></span>

-   [<span data-ttu-id="3ffe9-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3ffe9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3ffe9-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3ffe9-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3ffe9-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3ffe9-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3ffe9-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3ffe9-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3ffe9-132">Windows 2000 Server</span></span>



| <span data-ttu-id="3ffe9-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ffe9-133">Entry</span></span> | <span data-ttu-id="3ffe9-134">Valor</span><span class="sxs-lookup"><span data-stu-id="3ffe9-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3ffe9-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ffe9-135">Link-Id</span></span>                | <span data-ttu-id="3ffe9-136">76</span><span class="sxs-lookup"><span data-stu-id="3ffe9-136">76</span></span>                                       |
| <span data-ttu-id="3ffe9-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ffe9-137">MAPI-Id</span></span>                | <span data-ttu-id="3ffe9-138">0x80B6</span><span class="sxs-lookup"><span data-stu-id="3ffe9-138">0x80B6</span></span>                                   |
| <span data-ttu-id="3ffe9-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ffe9-139">System-Only</span></span>            | <span data-ttu-id="3ffe9-140">True</span><span class="sxs-lookup"><span data-stu-id="3ffe9-140">True</span></span>                                     |
| <span data-ttu-id="3ffe9-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ffe9-141">Is-Single-Valued</span></span>       | <span data-ttu-id="3ffe9-142">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-142">False</span></span>                                    |
| <span data-ttu-id="3ffe9-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ffe9-143">Is Indexed</span></span>             | <span data-ttu-id="3ffe9-144">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-144">False</span></span>                                    |
| <span data-ttu-id="3ffe9-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ffe9-145">In Global Catalog</span></span>      | <span data-ttu-id="3ffe9-146">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-146">False</span></span>                                    |
| <span data-ttu-id="3ffe9-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ffe9-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ffe9-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ffe9-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3ffe9-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ffe9-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3ffe9-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ffe9-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3ffe9-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ffe9-151">Search-Flags</span></span>           | <span data-ttu-id="3ffe9-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ffe9-152">0x00000000</span></span>                               |
| <span data-ttu-id="3ffe9-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ffe9-153">System-Flags</span></span>           | <span data-ttu-id="3ffe9-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ffe9-154">0x00000010</span></span>                               |
| <span data-ttu-id="3ffe9-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ffe9-155">Classes used in</span></span>        | [<span data-ttu-id="3ffe9-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3ffe9-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3ffe9-157">Windows Server 2003</span></span>



| <span data-ttu-id="3ffe9-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ffe9-158">Entry</span></span> | <span data-ttu-id="3ffe9-159">Valor</span><span class="sxs-lookup"><span data-stu-id="3ffe9-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3ffe9-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ffe9-160">Link-Id</span></span>                | <span data-ttu-id="3ffe9-161">76</span><span class="sxs-lookup"><span data-stu-id="3ffe9-161">76</span></span>                                       |
| <span data-ttu-id="3ffe9-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ffe9-162">MAPI-Id</span></span>                | <span data-ttu-id="3ffe9-163">0x80B6</span><span class="sxs-lookup"><span data-stu-id="3ffe9-163">0x80B6</span></span>                                   |
| <span data-ttu-id="3ffe9-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ffe9-164">System-Only</span></span>            | <span data-ttu-id="3ffe9-165">True</span><span class="sxs-lookup"><span data-stu-id="3ffe9-165">True</span></span>                                     |
| <span data-ttu-id="3ffe9-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ffe9-166">Is-Single-Valued</span></span>       | <span data-ttu-id="3ffe9-167">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-167">False</span></span>                                    |
| <span data-ttu-id="3ffe9-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ffe9-168">Is Indexed</span></span>             | <span data-ttu-id="3ffe9-169">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-169">False</span></span>                                    |
| <span data-ttu-id="3ffe9-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ffe9-170">In Global Catalog</span></span>      | <span data-ttu-id="3ffe9-171">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-171">False</span></span>                                    |
| <span data-ttu-id="3ffe9-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ffe9-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ffe9-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ffe9-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3ffe9-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ffe9-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3ffe9-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ffe9-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3ffe9-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ffe9-176">Search-Flags</span></span>           | <span data-ttu-id="3ffe9-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ffe9-177">0x00000000</span></span>                               |
| <span data-ttu-id="3ffe9-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ffe9-178">System-Flags</span></span>           | <span data-ttu-id="3ffe9-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ffe9-179">0x00000010</span></span>                               |
| <span data-ttu-id="3ffe9-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ffe9-180">Classes used in</span></span>        | [<span data-ttu-id="3ffe9-181">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-181">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="3ffe9-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="3ffe9-182">ADAM</span></span>



| <span data-ttu-id="3ffe9-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ffe9-183">Entry</span></span> | <span data-ttu-id="3ffe9-184">Valor</span><span class="sxs-lookup"><span data-stu-id="3ffe9-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3ffe9-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ffe9-185">Link-Id</span></span>                | <span data-ttu-id="3ffe9-186">76</span><span class="sxs-lookup"><span data-stu-id="3ffe9-186">76</span></span>                                       |
| <span data-ttu-id="3ffe9-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ffe9-187">MAPI-Id</span></span>                | <span data-ttu-id="3ffe9-188">0x80B6</span><span class="sxs-lookup"><span data-stu-id="3ffe9-188">0x80B6</span></span>                                   |
| <span data-ttu-id="3ffe9-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ffe9-189">System-Only</span></span>            | <span data-ttu-id="3ffe9-190">True</span><span class="sxs-lookup"><span data-stu-id="3ffe9-190">True</span></span>                                     |
| <span data-ttu-id="3ffe9-191">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ffe9-191">Is-Single-Valued</span></span>       | <span data-ttu-id="3ffe9-192">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-192">False</span></span>                                    |
| <span data-ttu-id="3ffe9-193">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ffe9-193">Is Indexed</span></span>             | <span data-ttu-id="3ffe9-194">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-194">False</span></span>                                    |
| <span data-ttu-id="3ffe9-195">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ffe9-195">In Global Catalog</span></span>      | <span data-ttu-id="3ffe9-196">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-196">False</span></span>                                    |
| <span data-ttu-id="3ffe9-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ffe9-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ffe9-198">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ffe9-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3ffe9-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ffe9-199">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3ffe9-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ffe9-200">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3ffe9-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ffe9-201">Search-Flags</span></span>           | <span data-ttu-id="3ffe9-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ffe9-202">0x00000000</span></span>                               |
| <span data-ttu-id="3ffe9-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ffe9-203">System-Flags</span></span>           | <span data-ttu-id="3ffe9-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ffe9-204">0x00000010</span></span>                               |
| <span data-ttu-id="3ffe9-205">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ffe9-205">Classes used in</span></span>        | [<span data-ttu-id="3ffe9-206">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-206">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3ffe9-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3ffe9-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3ffe9-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ffe9-208">Entry</span></span> | <span data-ttu-id="3ffe9-209">Valor</span><span class="sxs-lookup"><span data-stu-id="3ffe9-209">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3ffe9-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ffe9-210">Link-Id</span></span>                | <span data-ttu-id="3ffe9-211">76</span><span class="sxs-lookup"><span data-stu-id="3ffe9-211">76</span></span>                                       |
| <span data-ttu-id="3ffe9-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ffe9-212">MAPI-Id</span></span>                | <span data-ttu-id="3ffe9-213">0x80B6</span><span class="sxs-lookup"><span data-stu-id="3ffe9-213">0x80B6</span></span>                                   |
| <span data-ttu-id="3ffe9-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ffe9-214">System-Only</span></span>            | <span data-ttu-id="3ffe9-215">True</span><span class="sxs-lookup"><span data-stu-id="3ffe9-215">True</span></span>                                     |
| <span data-ttu-id="3ffe9-216">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ffe9-216">Is-Single-Valued</span></span>       | <span data-ttu-id="3ffe9-217">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-217">False</span></span>                                    |
| <span data-ttu-id="3ffe9-218">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ffe9-218">Is Indexed</span></span>             | <span data-ttu-id="3ffe9-219">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-219">False</span></span>                                    |
| <span data-ttu-id="3ffe9-220">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ffe9-220">In Global Catalog</span></span>      | <span data-ttu-id="3ffe9-221">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-221">False</span></span>                                    |
| <span data-ttu-id="3ffe9-222">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ffe9-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ffe9-223">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ffe9-223">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3ffe9-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ffe9-224">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3ffe9-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ffe9-225">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3ffe9-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ffe9-226">Search-Flags</span></span>           | <span data-ttu-id="3ffe9-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ffe9-227">0x00000000</span></span>                               |
| <span data-ttu-id="3ffe9-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ffe9-228">System-Flags</span></span>           | <span data-ttu-id="3ffe9-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ffe9-229">0x00000010</span></span>                               |
| <span data-ttu-id="3ffe9-230">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ffe9-230">Classes used in</span></span>        | [<span data-ttu-id="3ffe9-231">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-231">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3ffe9-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ffe9-232">Windows Server 2008</span></span>



| <span data-ttu-id="3ffe9-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ffe9-233">Entry</span></span> | <span data-ttu-id="3ffe9-234">Valor</span><span class="sxs-lookup"><span data-stu-id="3ffe9-234">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3ffe9-235">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ffe9-235">Link-Id</span></span>                | <span data-ttu-id="3ffe9-236">76</span><span class="sxs-lookup"><span data-stu-id="3ffe9-236">76</span></span>                                       |
| <span data-ttu-id="3ffe9-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ffe9-237">MAPI-Id</span></span>                | <span data-ttu-id="3ffe9-238">0x80B6</span><span class="sxs-lookup"><span data-stu-id="3ffe9-238">0x80B6</span></span>                                   |
| <span data-ttu-id="3ffe9-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ffe9-239">System-Only</span></span>            | <span data-ttu-id="3ffe9-240">True</span><span class="sxs-lookup"><span data-stu-id="3ffe9-240">True</span></span>                                     |
| <span data-ttu-id="3ffe9-241">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ffe9-241">Is-Single-Valued</span></span>       | <span data-ttu-id="3ffe9-242">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-242">False</span></span>                                    |
| <span data-ttu-id="3ffe9-243">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ffe9-243">Is Indexed</span></span>             | <span data-ttu-id="3ffe9-244">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-244">False</span></span>                                    |
| <span data-ttu-id="3ffe9-245">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ffe9-245">In Global Catalog</span></span>      | <span data-ttu-id="3ffe9-246">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-246">False</span></span>                                    |
| <span data-ttu-id="3ffe9-247">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ffe9-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ffe9-248">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ffe9-248">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3ffe9-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ffe9-249">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3ffe9-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ffe9-250">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3ffe9-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ffe9-251">Search-Flags</span></span>           | <span data-ttu-id="3ffe9-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ffe9-252">0x00000000</span></span>                               |
| <span data-ttu-id="3ffe9-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ffe9-253">System-Flags</span></span>           | <span data-ttu-id="3ffe9-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ffe9-254">0x00000010</span></span>                               |
| <span data-ttu-id="3ffe9-255">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ffe9-255">Classes used in</span></span>        | [<span data-ttu-id="3ffe9-256">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-256">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3ffe9-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3ffe9-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3ffe9-258">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ffe9-258">Entry</span></span> | <span data-ttu-id="3ffe9-259">Valor</span><span class="sxs-lookup"><span data-stu-id="3ffe9-259">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3ffe9-260">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ffe9-260">Link-Id</span></span>                | <span data-ttu-id="3ffe9-261">76</span><span class="sxs-lookup"><span data-stu-id="3ffe9-261">76</span></span>                                       |
| <span data-ttu-id="3ffe9-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ffe9-262">MAPI-Id</span></span>                | <span data-ttu-id="3ffe9-263">0x80B6</span><span class="sxs-lookup"><span data-stu-id="3ffe9-263">0x80B6</span></span>                                   |
| <span data-ttu-id="3ffe9-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ffe9-264">System-Only</span></span>            | <span data-ttu-id="3ffe9-265">True</span><span class="sxs-lookup"><span data-stu-id="3ffe9-265">True</span></span>                                     |
| <span data-ttu-id="3ffe9-266">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ffe9-266">Is-Single-Valued</span></span>       | <span data-ttu-id="3ffe9-267">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-267">False</span></span>                                    |
| <span data-ttu-id="3ffe9-268">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ffe9-268">Is Indexed</span></span>             | <span data-ttu-id="3ffe9-269">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-269">False</span></span>                                    |
| <span data-ttu-id="3ffe9-270">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ffe9-270">In Global Catalog</span></span>      | <span data-ttu-id="3ffe9-271">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-271">False</span></span>                                    |
| <span data-ttu-id="3ffe9-272">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ffe9-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ffe9-273">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ffe9-273">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3ffe9-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ffe9-274">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3ffe9-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ffe9-275">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3ffe9-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ffe9-276">Search-Flags</span></span>           | <span data-ttu-id="3ffe9-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ffe9-277">0x00000000</span></span>                               |
| <span data-ttu-id="3ffe9-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ffe9-278">System-Flags</span></span>           | <span data-ttu-id="3ffe9-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ffe9-279">0x00000010</span></span>                               |
| <span data-ttu-id="3ffe9-280">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ffe9-280">Classes used in</span></span>        | [<span data-ttu-id="3ffe9-281">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-281">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3ffe9-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3ffe9-282">Windows Server 2012</span></span>



| <span data-ttu-id="3ffe9-283">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ffe9-283">Entry</span></span> | <span data-ttu-id="3ffe9-284">Valor</span><span class="sxs-lookup"><span data-stu-id="3ffe9-284">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3ffe9-285">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ffe9-285">Link-Id</span></span>                | <span data-ttu-id="3ffe9-286">76</span><span class="sxs-lookup"><span data-stu-id="3ffe9-286">76</span></span>                                       |
| <span data-ttu-id="3ffe9-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ffe9-287">MAPI-Id</span></span>                | <span data-ttu-id="3ffe9-288">0x80B6</span><span class="sxs-lookup"><span data-stu-id="3ffe9-288">0x80B6</span></span>                                   |
| <span data-ttu-id="3ffe9-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ffe9-289">System-Only</span></span>            | <span data-ttu-id="3ffe9-290">True</span><span class="sxs-lookup"><span data-stu-id="3ffe9-290">True</span></span>                                     |
| <span data-ttu-id="3ffe9-291">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ffe9-291">Is-Single-Valued</span></span>       | <span data-ttu-id="3ffe9-292">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-292">False</span></span>                                    |
| <span data-ttu-id="3ffe9-293">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ffe9-293">Is Indexed</span></span>             | <span data-ttu-id="3ffe9-294">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-294">False</span></span>                                    |
| <span data-ttu-id="3ffe9-295">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ffe9-295">In Global Catalog</span></span>      | <span data-ttu-id="3ffe9-296">Falso</span><span class="sxs-lookup"><span data-stu-id="3ffe9-296">False</span></span>                                    |
| <span data-ttu-id="3ffe9-297">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ffe9-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ffe9-298">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ffe9-298">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3ffe9-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ffe9-299">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3ffe9-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ffe9-300">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3ffe9-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ffe9-301">Search-Flags</span></span>           | <span data-ttu-id="3ffe9-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ffe9-302">0x00000000</span></span>                               |
| <span data-ttu-id="3ffe9-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ffe9-303">System-Flags</span></span>           | <span data-ttu-id="3ffe9-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ffe9-304">0x00000010</span></span>                               |
| <span data-ttu-id="3ffe9-305">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ffe9-305">Classes used in</span></span>        | [<span data-ttu-id="3ffe9-306">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3ffe9-306">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





