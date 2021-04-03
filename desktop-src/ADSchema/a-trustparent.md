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
# <a name="trust-parent-attribute"></a><span data-ttu-id="f9eeb-105">Trust-Parent atributo</span><span class="sxs-lookup"><span data-stu-id="f9eeb-105">Trust-Parent attribute</span></span>

<span data-ttu-id="f9eeb-106">O pai na hierarquia de confiança KERBEROS.</span><span class="sxs-lookup"><span data-stu-id="f9eeb-106">The parent in KERBEROS trust hierarchy.</span></span>



| <span data-ttu-id="f9eeb-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9eeb-107">Entry</span></span> | <span data-ttu-id="f9eeb-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f9eeb-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="f9eeb-109">CN</span><span class="sxs-lookup"><span data-stu-id="f9eeb-109">CN</span></span>                | <span data-ttu-id="f9eeb-110">Trust-Parent</span><span class="sxs-lookup"><span data-stu-id="f9eeb-110">Trust-Parent</span></span>                            |
| <span data-ttu-id="f9eeb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f9eeb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f9eeb-112">trustParent</span><span class="sxs-lookup"><span data-stu-id="f9eeb-112">trustParent</span></span>                             |
| <span data-ttu-id="f9eeb-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f9eeb-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="f9eeb-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f9eeb-114">Update Privilege</span></span>  | <span data-ttu-id="f9eeb-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="f9eeb-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="f9eeb-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f9eeb-116">Update Frequency</span></span>  | <span data-ttu-id="f9eeb-117">Quando um domínio filho é criado.</span><span class="sxs-lookup"><span data-stu-id="f9eeb-117">When a child domain is created.</span></span>         |
| <span data-ttu-id="f9eeb-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f9eeb-118">Attribute-Id</span></span>      | <span data-ttu-id="f9eeb-119">1.2.840.113556.1.4.471</span><span class="sxs-lookup"><span data-stu-id="f9eeb-119">1.2.840.113556.1.4.471</span></span>                  |
| <span data-ttu-id="f9eeb-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f9eeb-120">System-Id-Guid</span></span>    | <span data-ttu-id="f9eeb-121">b000ea7a-a086-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="f9eeb-121">b000ea7a-a086-11d0-afdd-00c04fd930c9</span></span>    |
| <span data-ttu-id="f9eeb-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9eeb-122">Syntax</span></span>            | [<span data-ttu-id="f9eeb-123">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="f9eeb-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="f9eeb-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="f9eeb-124">Implementations</span></span>

-   [<span data-ttu-id="f9eeb-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f9eeb-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f9eeb-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f9eeb-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f9eeb-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f9eeb-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f9eeb-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f9eeb-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f9eeb-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f9eeb-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f9eeb-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f9eeb-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f9eeb-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f9eeb-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f9eeb-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f9eeb-132">Windows 2000 Server</span></span>



| <span data-ttu-id="f9eeb-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9eeb-133">Entry</span></span> | <span data-ttu-id="f9eeb-134">Valor</span><span class="sxs-lookup"><span data-stu-id="f9eeb-134">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="f9eeb-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="f9eeb-135">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="f9eeb-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9eeb-136">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="f9eeb-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9eeb-137">System-Only</span></span>            | <span data-ttu-id="f9eeb-138">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-138">False</span></span>                                      |
| <span data-ttu-id="f9eeb-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f9eeb-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f9eeb-140">True</span><span class="sxs-lookup"><span data-stu-id="f9eeb-140">True</span></span>                                       |
| <span data-ttu-id="f9eeb-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="f9eeb-141">Is Indexed</span></span>             | <span data-ttu-id="f9eeb-142">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-142">False</span></span>                                      |
| <span data-ttu-id="f9eeb-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f9eeb-143">In Global Catalog</span></span>      | <span data-ttu-id="f9eeb-144">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-144">False</span></span>                                      |
| <span data-ttu-id="f9eeb-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f9eeb-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9eeb-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f9eeb-146">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="f9eeb-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9eeb-147">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="f9eeb-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9eeb-148">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="f9eeb-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9eeb-149">Search-Flags</span></span>           | <span data-ttu-id="f9eeb-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9eeb-150">0x00000000</span></span>                                 |
| <span data-ttu-id="f9eeb-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9eeb-151">System-Flags</span></span>           | <span data-ttu-id="f9eeb-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9eeb-152">0x00000010</span></span>                                 |
| <span data-ttu-id="f9eeb-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f9eeb-153">Classes used in</span></span>        | [<span data-ttu-id="f9eeb-154">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="f9eeb-154">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f9eeb-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f9eeb-155">Windows Server 2003</span></span>



| <span data-ttu-id="f9eeb-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9eeb-156">Entry</span></span> | <span data-ttu-id="f9eeb-157">Valor</span><span class="sxs-lookup"><span data-stu-id="f9eeb-157">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="f9eeb-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="f9eeb-158">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="f9eeb-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9eeb-159">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="f9eeb-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9eeb-160">System-Only</span></span>            | <span data-ttu-id="f9eeb-161">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-161">False</span></span>                                      |
| <span data-ttu-id="f9eeb-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f9eeb-162">Is-Single-Valued</span></span>       | <span data-ttu-id="f9eeb-163">True</span><span class="sxs-lookup"><span data-stu-id="f9eeb-163">True</span></span>                                       |
| <span data-ttu-id="f9eeb-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="f9eeb-164">Is Indexed</span></span>             | <span data-ttu-id="f9eeb-165">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-165">False</span></span>                                      |
| <span data-ttu-id="f9eeb-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f9eeb-166">In Global Catalog</span></span>      | <span data-ttu-id="f9eeb-167">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-167">False</span></span>                                      |
| <span data-ttu-id="f9eeb-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f9eeb-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9eeb-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f9eeb-169">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="f9eeb-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9eeb-170">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="f9eeb-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9eeb-171">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="f9eeb-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9eeb-172">Search-Flags</span></span>           | <span data-ttu-id="f9eeb-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9eeb-173">0x00000000</span></span>                                 |
| <span data-ttu-id="f9eeb-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9eeb-174">System-Flags</span></span>           | <span data-ttu-id="f9eeb-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9eeb-175">0x00000010</span></span>                                 |
| <span data-ttu-id="f9eeb-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f9eeb-176">Classes used in</span></span>        | [<span data-ttu-id="f9eeb-177">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="f9eeb-177">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f9eeb-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="f9eeb-178">ADAM</span></span>



| <span data-ttu-id="f9eeb-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9eeb-179">Entry</span></span> | <span data-ttu-id="f9eeb-180">Valor</span><span class="sxs-lookup"><span data-stu-id="f9eeb-180">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="f9eeb-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="f9eeb-181">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="f9eeb-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9eeb-182">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="f9eeb-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9eeb-183">System-Only</span></span>            | <span data-ttu-id="f9eeb-184">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-184">False</span></span>                                      |
| <span data-ttu-id="f9eeb-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f9eeb-185">Is-Single-Valued</span></span>       | <span data-ttu-id="f9eeb-186">True</span><span class="sxs-lookup"><span data-stu-id="f9eeb-186">True</span></span>                                       |
| <span data-ttu-id="f9eeb-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="f9eeb-187">Is Indexed</span></span>             | <span data-ttu-id="f9eeb-188">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-188">False</span></span>                                      |
| <span data-ttu-id="f9eeb-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f9eeb-189">In Global Catalog</span></span>      | <span data-ttu-id="f9eeb-190">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-190">False</span></span>                                      |
| <span data-ttu-id="f9eeb-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f9eeb-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9eeb-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f9eeb-192">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="f9eeb-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9eeb-193">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="f9eeb-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9eeb-194">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="f9eeb-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9eeb-195">Search-Flags</span></span>           | <span data-ttu-id="f9eeb-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9eeb-196">0x00000000</span></span>                                 |
| <span data-ttu-id="f9eeb-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9eeb-197">System-Flags</span></span>           | <span data-ttu-id="f9eeb-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9eeb-198">0x00000010</span></span>                                 |
| <span data-ttu-id="f9eeb-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f9eeb-199">Classes used in</span></span>        | [<span data-ttu-id="f9eeb-200">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="f9eeb-200">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f9eeb-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f9eeb-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f9eeb-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9eeb-202">Entry</span></span> | <span data-ttu-id="f9eeb-203">Valor</span><span class="sxs-lookup"><span data-stu-id="f9eeb-203">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="f9eeb-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="f9eeb-204">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="f9eeb-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9eeb-205">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="f9eeb-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9eeb-206">System-Only</span></span>            | <span data-ttu-id="f9eeb-207">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-207">False</span></span>                                      |
| <span data-ttu-id="f9eeb-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f9eeb-208">Is-Single-Valued</span></span>       | <span data-ttu-id="f9eeb-209">True</span><span class="sxs-lookup"><span data-stu-id="f9eeb-209">True</span></span>                                       |
| <span data-ttu-id="f9eeb-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="f9eeb-210">Is Indexed</span></span>             | <span data-ttu-id="f9eeb-211">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-211">False</span></span>                                      |
| <span data-ttu-id="f9eeb-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f9eeb-212">In Global Catalog</span></span>      | <span data-ttu-id="f9eeb-213">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-213">False</span></span>                                      |
| <span data-ttu-id="f9eeb-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f9eeb-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9eeb-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f9eeb-215">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="f9eeb-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9eeb-216">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="f9eeb-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9eeb-217">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="f9eeb-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9eeb-218">Search-Flags</span></span>           | <span data-ttu-id="f9eeb-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9eeb-219">0x00000000</span></span>                                 |
| <span data-ttu-id="f9eeb-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9eeb-220">System-Flags</span></span>           | <span data-ttu-id="f9eeb-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9eeb-221">0x00000010</span></span>                                 |
| <span data-ttu-id="f9eeb-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f9eeb-222">Classes used in</span></span>        | [<span data-ttu-id="f9eeb-223">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="f9eeb-223">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f9eeb-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9eeb-224">Windows Server 2008</span></span>



| <span data-ttu-id="f9eeb-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9eeb-225">Entry</span></span> | <span data-ttu-id="f9eeb-226">Valor</span><span class="sxs-lookup"><span data-stu-id="f9eeb-226">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="f9eeb-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="f9eeb-227">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="f9eeb-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9eeb-228">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="f9eeb-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9eeb-229">System-Only</span></span>            | <span data-ttu-id="f9eeb-230">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-230">False</span></span>                                      |
| <span data-ttu-id="f9eeb-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f9eeb-231">Is-Single-Valued</span></span>       | <span data-ttu-id="f9eeb-232">True</span><span class="sxs-lookup"><span data-stu-id="f9eeb-232">True</span></span>                                       |
| <span data-ttu-id="f9eeb-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="f9eeb-233">Is Indexed</span></span>             | <span data-ttu-id="f9eeb-234">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-234">False</span></span>                                      |
| <span data-ttu-id="f9eeb-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f9eeb-235">In Global Catalog</span></span>      | <span data-ttu-id="f9eeb-236">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-236">False</span></span>                                      |
| <span data-ttu-id="f9eeb-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f9eeb-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9eeb-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f9eeb-238">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="f9eeb-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9eeb-239">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="f9eeb-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9eeb-240">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="f9eeb-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9eeb-241">Search-Flags</span></span>           | <span data-ttu-id="f9eeb-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9eeb-242">0x00000000</span></span>                                 |
| <span data-ttu-id="f9eeb-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9eeb-243">System-Flags</span></span>           | <span data-ttu-id="f9eeb-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9eeb-244">0x00000010</span></span>                                 |
| <span data-ttu-id="f9eeb-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f9eeb-245">Classes used in</span></span>        | [<span data-ttu-id="f9eeb-246">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="f9eeb-246">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f9eeb-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f9eeb-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f9eeb-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9eeb-248">Entry</span></span> | <span data-ttu-id="f9eeb-249">Valor</span><span class="sxs-lookup"><span data-stu-id="f9eeb-249">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="f9eeb-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="f9eeb-250">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="f9eeb-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9eeb-251">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="f9eeb-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9eeb-252">System-Only</span></span>            | <span data-ttu-id="f9eeb-253">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-253">False</span></span>                                      |
| <span data-ttu-id="f9eeb-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f9eeb-254">Is-Single-Valued</span></span>       | <span data-ttu-id="f9eeb-255">True</span><span class="sxs-lookup"><span data-stu-id="f9eeb-255">True</span></span>                                       |
| <span data-ttu-id="f9eeb-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="f9eeb-256">Is Indexed</span></span>             | <span data-ttu-id="f9eeb-257">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-257">False</span></span>                                      |
| <span data-ttu-id="f9eeb-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f9eeb-258">In Global Catalog</span></span>      | <span data-ttu-id="f9eeb-259">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-259">False</span></span>                                      |
| <span data-ttu-id="f9eeb-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f9eeb-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9eeb-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f9eeb-261">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="f9eeb-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9eeb-262">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="f9eeb-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9eeb-263">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="f9eeb-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9eeb-264">Search-Flags</span></span>           | <span data-ttu-id="f9eeb-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9eeb-265">0x00000000</span></span>                                 |
| <span data-ttu-id="f9eeb-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9eeb-266">System-Flags</span></span>           | <span data-ttu-id="f9eeb-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9eeb-267">0x00000010</span></span>                                 |
| <span data-ttu-id="f9eeb-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f9eeb-268">Classes used in</span></span>        | [<span data-ttu-id="f9eeb-269">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="f9eeb-269">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f9eeb-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f9eeb-270">Windows Server 2012</span></span>



| <span data-ttu-id="f9eeb-271">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9eeb-271">Entry</span></span> | <span data-ttu-id="f9eeb-272">Valor</span><span class="sxs-lookup"><span data-stu-id="f9eeb-272">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="f9eeb-273">ID do link</span><span class="sxs-lookup"><span data-stu-id="f9eeb-273">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="f9eeb-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9eeb-274">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="f9eeb-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9eeb-275">System-Only</span></span>            | <span data-ttu-id="f9eeb-276">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-276">False</span></span>                                      |
| <span data-ttu-id="f9eeb-277">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f9eeb-277">Is-Single-Valued</span></span>       | <span data-ttu-id="f9eeb-278">True</span><span class="sxs-lookup"><span data-stu-id="f9eeb-278">True</span></span>                                       |
| <span data-ttu-id="f9eeb-279">É indexado</span><span class="sxs-lookup"><span data-stu-id="f9eeb-279">Is Indexed</span></span>             | <span data-ttu-id="f9eeb-280">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-280">False</span></span>                                      |
| <span data-ttu-id="f9eeb-281">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f9eeb-281">In Global Catalog</span></span>      | <span data-ttu-id="f9eeb-282">Falso</span><span class="sxs-lookup"><span data-stu-id="f9eeb-282">False</span></span>                                      |
| <span data-ttu-id="f9eeb-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f9eeb-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9eeb-284">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f9eeb-284">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="f9eeb-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9eeb-285">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="f9eeb-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9eeb-286">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="f9eeb-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9eeb-287">Search-Flags</span></span>           | <span data-ttu-id="f9eeb-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9eeb-288">0x00000000</span></span>                                 |
| <span data-ttu-id="f9eeb-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9eeb-289">System-Flags</span></span>           | <span data-ttu-id="f9eeb-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9eeb-290">0x00000010</span></span>                                 |
| <span data-ttu-id="f9eeb-291">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f9eeb-291">Classes used in</span></span>        | [<span data-ttu-id="f9eeb-292">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="f9eeb-292">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





