---
title: Trust-Parent atributo
description: O pai na hierarquia de confiança KERBEROS.
ms.assetid: 738cf509-42a2-40b6-a525-6df34c02d0f0
ms.tgt_platform: multiple
keywords:
- Esquema de Trust-Parent do atributo AD
- Esquema de AD do atributo trustParent
topic_type:
- apiref
api_name:
- Trust-Parent
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d8be971c7597b14daf7a694e41c9d67714e5f0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645493"
---
# <a name="trust-parent-attribute"></a><span data-ttu-id="1beab-105">Trust-Parent atributo</span><span class="sxs-lookup"><span data-stu-id="1beab-105">Trust-Parent attribute</span></span>

<span data-ttu-id="1beab-106">O pai na hierarquia de confiança KERBEROS.</span><span class="sxs-lookup"><span data-stu-id="1beab-106">The parent in KERBEROS trust hierarchy.</span></span>



| <span data-ttu-id="1beab-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="1beab-107">Entry</span></span> | <span data-ttu-id="1beab-108">Valor</span><span class="sxs-lookup"><span data-stu-id="1beab-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="1beab-109">CN</span><span class="sxs-lookup"><span data-stu-id="1beab-109">CN</span></span>                | <span data-ttu-id="1beab-110">Trust-Parent</span><span class="sxs-lookup"><span data-stu-id="1beab-110">Trust-Parent</span></span>                            |
| <span data-ttu-id="1beab-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1beab-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1beab-112">trustParent</span><span class="sxs-lookup"><span data-stu-id="1beab-112">trustParent</span></span>                             |
| <span data-ttu-id="1beab-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="1beab-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="1beab-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="1beab-114">Update Privilege</span></span>  | <span data-ttu-id="1beab-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="1beab-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="1beab-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="1beab-116">Update Frequency</span></span>  | <span data-ttu-id="1beab-117">Quando um domínio filho é criado.</span><span class="sxs-lookup"><span data-stu-id="1beab-117">When a child domain is created.</span></span>         |
| <span data-ttu-id="1beab-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1beab-118">Attribute-Id</span></span>      | <span data-ttu-id="1beab-119">1.2.840.113556.1.4.471</span><span class="sxs-lookup"><span data-stu-id="1beab-119">1.2.840.113556.1.4.471</span></span>                  |
| <span data-ttu-id="1beab-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1beab-120">System-Id-Guid</span></span>    | <span data-ttu-id="1beab-121">b000ea7a-a086-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="1beab-121">b000ea7a-a086-11d0-afdd-00c04fd930c9</span></span>    |
| <span data-ttu-id="1beab-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="1beab-122">Syntax</span></span>            | [<span data-ttu-id="1beab-123">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="1beab-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="1beab-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="1beab-124">Implementations</span></span>

-   [<span data-ttu-id="1beab-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1beab-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1beab-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1beab-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1beab-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1beab-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1beab-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1beab-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1beab-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1beab-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1beab-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1beab-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1beab-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1beab-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1beab-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1beab-132">Windows 2000 Server</span></span>



| <span data-ttu-id="1beab-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="1beab-133">Entry</span></span> | <span data-ttu-id="1beab-134">Valor</span><span class="sxs-lookup"><span data-stu-id="1beab-134">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="1beab-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="1beab-135">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="1beab-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1beab-136">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="1beab-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="1beab-137">System-Only</span></span>            | <span data-ttu-id="1beab-138">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-138">False</span></span>                                      |
| <span data-ttu-id="1beab-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1beab-139">Is-Single-Valued</span></span>       | <span data-ttu-id="1beab-140">True</span><span class="sxs-lookup"><span data-stu-id="1beab-140">True</span></span>                                       |
| <span data-ttu-id="1beab-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="1beab-141">Is Indexed</span></span>             | <span data-ttu-id="1beab-142">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-142">False</span></span>                                      |
| <span data-ttu-id="1beab-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1beab-143">In Global Catalog</span></span>      | <span data-ttu-id="1beab-144">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-144">False</span></span>                                      |
| <span data-ttu-id="1beab-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1beab-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="1beab-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1beab-146">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="1beab-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1beab-147">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="1beab-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1beab-148">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="1beab-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1beab-149">Search-Flags</span></span>           | <span data-ttu-id="1beab-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1beab-150">0x00000000</span></span>                                 |
| <span data-ttu-id="1beab-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1beab-151">System-Flags</span></span>           | <span data-ttu-id="1beab-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1beab-152">0x00000010</span></span>                                 |
| <span data-ttu-id="1beab-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1beab-153">Classes used in</span></span>        | [<span data-ttu-id="1beab-154">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="1beab-154">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1beab-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1beab-155">Windows Server 2003</span></span>



| <span data-ttu-id="1beab-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="1beab-156">Entry</span></span> | <span data-ttu-id="1beab-157">Valor</span><span class="sxs-lookup"><span data-stu-id="1beab-157">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="1beab-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="1beab-158">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="1beab-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1beab-159">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="1beab-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="1beab-160">System-Only</span></span>            | <span data-ttu-id="1beab-161">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-161">False</span></span>                                      |
| <span data-ttu-id="1beab-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1beab-162">Is-Single-Valued</span></span>       | <span data-ttu-id="1beab-163">True</span><span class="sxs-lookup"><span data-stu-id="1beab-163">True</span></span>                                       |
| <span data-ttu-id="1beab-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="1beab-164">Is Indexed</span></span>             | <span data-ttu-id="1beab-165">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-165">False</span></span>                                      |
| <span data-ttu-id="1beab-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1beab-166">In Global Catalog</span></span>      | <span data-ttu-id="1beab-167">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-167">False</span></span>                                      |
| <span data-ttu-id="1beab-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1beab-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="1beab-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1beab-169">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="1beab-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1beab-170">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="1beab-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1beab-171">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="1beab-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1beab-172">Search-Flags</span></span>           | <span data-ttu-id="1beab-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1beab-173">0x00000000</span></span>                                 |
| <span data-ttu-id="1beab-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1beab-174">System-Flags</span></span>           | <span data-ttu-id="1beab-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1beab-175">0x00000010</span></span>                                 |
| <span data-ttu-id="1beab-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1beab-176">Classes used in</span></span>        | [<span data-ttu-id="1beab-177">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="1beab-177">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1beab-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="1beab-178">ADAM</span></span>



| <span data-ttu-id="1beab-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="1beab-179">Entry</span></span> | <span data-ttu-id="1beab-180">Valor</span><span class="sxs-lookup"><span data-stu-id="1beab-180">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="1beab-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="1beab-181">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="1beab-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1beab-182">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="1beab-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="1beab-183">System-Only</span></span>            | <span data-ttu-id="1beab-184">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-184">False</span></span>                                      |
| <span data-ttu-id="1beab-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1beab-185">Is-Single-Valued</span></span>       | <span data-ttu-id="1beab-186">True</span><span class="sxs-lookup"><span data-stu-id="1beab-186">True</span></span>                                       |
| <span data-ttu-id="1beab-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="1beab-187">Is Indexed</span></span>             | <span data-ttu-id="1beab-188">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-188">False</span></span>                                      |
| <span data-ttu-id="1beab-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1beab-189">In Global Catalog</span></span>      | <span data-ttu-id="1beab-190">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-190">False</span></span>                                      |
| <span data-ttu-id="1beab-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1beab-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="1beab-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1beab-192">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="1beab-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1beab-193">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="1beab-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1beab-194">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="1beab-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1beab-195">Search-Flags</span></span>           | <span data-ttu-id="1beab-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1beab-196">0x00000000</span></span>                                 |
| <span data-ttu-id="1beab-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1beab-197">System-Flags</span></span>           | <span data-ttu-id="1beab-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1beab-198">0x00000010</span></span>                                 |
| <span data-ttu-id="1beab-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1beab-199">Classes used in</span></span>        | [<span data-ttu-id="1beab-200">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="1beab-200">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1beab-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1beab-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1beab-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="1beab-202">Entry</span></span> | <span data-ttu-id="1beab-203">Valor</span><span class="sxs-lookup"><span data-stu-id="1beab-203">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="1beab-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="1beab-204">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="1beab-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1beab-205">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="1beab-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="1beab-206">System-Only</span></span>            | <span data-ttu-id="1beab-207">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-207">False</span></span>                                      |
| <span data-ttu-id="1beab-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1beab-208">Is-Single-Valued</span></span>       | <span data-ttu-id="1beab-209">True</span><span class="sxs-lookup"><span data-stu-id="1beab-209">True</span></span>                                       |
| <span data-ttu-id="1beab-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="1beab-210">Is Indexed</span></span>             | <span data-ttu-id="1beab-211">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-211">False</span></span>                                      |
| <span data-ttu-id="1beab-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1beab-212">In Global Catalog</span></span>      | <span data-ttu-id="1beab-213">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-213">False</span></span>                                      |
| <span data-ttu-id="1beab-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1beab-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="1beab-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1beab-215">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="1beab-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1beab-216">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="1beab-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1beab-217">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="1beab-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1beab-218">Search-Flags</span></span>           | <span data-ttu-id="1beab-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1beab-219">0x00000000</span></span>                                 |
| <span data-ttu-id="1beab-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1beab-220">System-Flags</span></span>           | <span data-ttu-id="1beab-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1beab-221">0x00000010</span></span>                                 |
| <span data-ttu-id="1beab-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1beab-222">Classes used in</span></span>        | [<span data-ttu-id="1beab-223">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="1beab-223">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1beab-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1beab-224">Windows Server 2008</span></span>



| <span data-ttu-id="1beab-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="1beab-225">Entry</span></span> | <span data-ttu-id="1beab-226">Valor</span><span class="sxs-lookup"><span data-stu-id="1beab-226">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="1beab-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="1beab-227">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="1beab-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1beab-228">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="1beab-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="1beab-229">System-Only</span></span>            | <span data-ttu-id="1beab-230">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-230">False</span></span>                                      |
| <span data-ttu-id="1beab-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1beab-231">Is-Single-Valued</span></span>       | <span data-ttu-id="1beab-232">True</span><span class="sxs-lookup"><span data-stu-id="1beab-232">True</span></span>                                       |
| <span data-ttu-id="1beab-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="1beab-233">Is Indexed</span></span>             | <span data-ttu-id="1beab-234">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-234">False</span></span>                                      |
| <span data-ttu-id="1beab-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1beab-235">In Global Catalog</span></span>      | <span data-ttu-id="1beab-236">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-236">False</span></span>                                      |
| <span data-ttu-id="1beab-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1beab-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="1beab-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1beab-238">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="1beab-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1beab-239">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="1beab-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1beab-240">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="1beab-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1beab-241">Search-Flags</span></span>           | <span data-ttu-id="1beab-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1beab-242">0x00000000</span></span>                                 |
| <span data-ttu-id="1beab-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1beab-243">System-Flags</span></span>           | <span data-ttu-id="1beab-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1beab-244">0x00000010</span></span>                                 |
| <span data-ttu-id="1beab-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1beab-245">Classes used in</span></span>        | [<span data-ttu-id="1beab-246">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="1beab-246">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1beab-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1beab-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1beab-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="1beab-248">Entry</span></span> | <span data-ttu-id="1beab-249">Valor</span><span class="sxs-lookup"><span data-stu-id="1beab-249">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="1beab-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="1beab-250">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="1beab-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1beab-251">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="1beab-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="1beab-252">System-Only</span></span>            | <span data-ttu-id="1beab-253">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-253">False</span></span>                                      |
| <span data-ttu-id="1beab-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1beab-254">Is-Single-Valued</span></span>       | <span data-ttu-id="1beab-255">True</span><span class="sxs-lookup"><span data-stu-id="1beab-255">True</span></span>                                       |
| <span data-ttu-id="1beab-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="1beab-256">Is Indexed</span></span>             | <span data-ttu-id="1beab-257">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-257">False</span></span>                                      |
| <span data-ttu-id="1beab-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1beab-258">In Global Catalog</span></span>      | <span data-ttu-id="1beab-259">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-259">False</span></span>                                      |
| <span data-ttu-id="1beab-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1beab-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="1beab-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1beab-261">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="1beab-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1beab-262">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="1beab-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1beab-263">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="1beab-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1beab-264">Search-Flags</span></span>           | <span data-ttu-id="1beab-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1beab-265">0x00000000</span></span>                                 |
| <span data-ttu-id="1beab-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1beab-266">System-Flags</span></span>           | <span data-ttu-id="1beab-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1beab-267">0x00000010</span></span>                                 |
| <span data-ttu-id="1beab-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1beab-268">Classes used in</span></span>        | [<span data-ttu-id="1beab-269">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="1beab-269">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1beab-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1beab-270">Windows Server 2012</span></span>



| <span data-ttu-id="1beab-271">Entrada</span><span class="sxs-lookup"><span data-stu-id="1beab-271">Entry</span></span> | <span data-ttu-id="1beab-272">Valor</span><span class="sxs-lookup"><span data-stu-id="1beab-272">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="1beab-273">ID do link</span><span class="sxs-lookup"><span data-stu-id="1beab-273">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="1beab-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1beab-274">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="1beab-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="1beab-275">System-Only</span></span>            | <span data-ttu-id="1beab-276">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-276">False</span></span>                                      |
| <span data-ttu-id="1beab-277">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1beab-277">Is-Single-Valued</span></span>       | <span data-ttu-id="1beab-278">True</span><span class="sxs-lookup"><span data-stu-id="1beab-278">True</span></span>                                       |
| <span data-ttu-id="1beab-279">É indexado</span><span class="sxs-lookup"><span data-stu-id="1beab-279">Is Indexed</span></span>             | <span data-ttu-id="1beab-280">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-280">False</span></span>                                      |
| <span data-ttu-id="1beab-281">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1beab-281">In Global Catalog</span></span>      | <span data-ttu-id="1beab-282">Falso</span><span class="sxs-lookup"><span data-stu-id="1beab-282">False</span></span>                                      |
| <span data-ttu-id="1beab-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1beab-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="1beab-284">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1beab-284">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="1beab-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1beab-285">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="1beab-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1beab-286">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="1beab-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1beab-287">Search-Flags</span></span>           | <span data-ttu-id="1beab-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1beab-288">0x00000000</span></span>                                 |
| <span data-ttu-id="1beab-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1beab-289">System-Flags</span></span>           | <span data-ttu-id="1beab-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1beab-290">0x00000010</span></span>                                 |
| <span data-ttu-id="1beab-291">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1beab-291">Classes used in</span></span>        | [<span data-ttu-id="1beab-292">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="1beab-292">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





