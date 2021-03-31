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
# <a name="trust-parent-attribute"></a><span data-ttu-id="2f8ec-105">Trust-Parent atributo</span><span class="sxs-lookup"><span data-stu-id="2f8ec-105">Trust-Parent attribute</span></span>

<span data-ttu-id="2f8ec-106">O pai na hierarquia de confiança KERBEROS.</span><span class="sxs-lookup"><span data-stu-id="2f8ec-106">The parent in KERBEROS trust hierarchy.</span></span>



| <span data-ttu-id="2f8ec-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="2f8ec-107">Entry</span></span> | <span data-ttu-id="2f8ec-108">Valor</span><span class="sxs-lookup"><span data-stu-id="2f8ec-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="2f8ec-109">CN</span><span class="sxs-lookup"><span data-stu-id="2f8ec-109">CN</span></span>                | <span data-ttu-id="2f8ec-110">Trust-Parent</span><span class="sxs-lookup"><span data-stu-id="2f8ec-110">Trust-Parent</span></span>                            |
| <span data-ttu-id="2f8ec-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2f8ec-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2f8ec-112">trustParent</span><span class="sxs-lookup"><span data-stu-id="2f8ec-112">trustParent</span></span>                             |
| <span data-ttu-id="2f8ec-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="2f8ec-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="2f8ec-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="2f8ec-114">Update Privilege</span></span>  | <span data-ttu-id="2f8ec-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="2f8ec-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="2f8ec-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="2f8ec-116">Update Frequency</span></span>  | <span data-ttu-id="2f8ec-117">Quando um domínio filho é criado.</span><span class="sxs-lookup"><span data-stu-id="2f8ec-117">When a child domain is created.</span></span>         |
| <span data-ttu-id="2f8ec-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2f8ec-118">Attribute-Id</span></span>      | <span data-ttu-id="2f8ec-119">1.2.840.113556.1.4.471</span><span class="sxs-lookup"><span data-stu-id="2f8ec-119">1.2.840.113556.1.4.471</span></span>                  |
| <span data-ttu-id="2f8ec-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2f8ec-120">System-Id-Guid</span></span>    | <span data-ttu-id="2f8ec-121">b000ea7a-a086-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="2f8ec-121">b000ea7a-a086-11d0-afdd-00c04fd930c9</span></span>    |
| <span data-ttu-id="2f8ec-122">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f8ec-122">Syntax</span></span>            | [<span data-ttu-id="2f8ec-123">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="2f8ec-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="2f8ec-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="2f8ec-124">Implementations</span></span>

-   [<span data-ttu-id="2f8ec-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2f8ec-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2f8ec-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2f8ec-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2f8ec-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2f8ec-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2f8ec-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2f8ec-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2f8ec-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2f8ec-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2f8ec-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2f8ec-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2f8ec-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2f8ec-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2f8ec-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2f8ec-132">Windows 2000 Server</span></span>



| <span data-ttu-id="2f8ec-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="2f8ec-133">Entry</span></span> | <span data-ttu-id="2f8ec-134">Valor</span><span class="sxs-lookup"><span data-stu-id="2f8ec-134">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="2f8ec-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="2f8ec-135">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="2f8ec-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f8ec-136">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="2f8ec-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f8ec-137">System-Only</span></span>            | <span data-ttu-id="2f8ec-138">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-138">False</span></span>                                      |
| <span data-ttu-id="2f8ec-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2f8ec-139">Is-Single-Valued</span></span>       | <span data-ttu-id="2f8ec-140">True</span><span class="sxs-lookup"><span data-stu-id="2f8ec-140">True</span></span>                                       |
| <span data-ttu-id="2f8ec-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="2f8ec-141">Is Indexed</span></span>             | <span data-ttu-id="2f8ec-142">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-142">False</span></span>                                      |
| <span data-ttu-id="2f8ec-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2f8ec-143">In Global Catalog</span></span>      | <span data-ttu-id="2f8ec-144">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-144">False</span></span>                                      |
| <span data-ttu-id="2f8ec-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2f8ec-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f8ec-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2f8ec-146">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="2f8ec-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f8ec-147">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="2f8ec-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f8ec-148">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="2f8ec-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f8ec-149">Search-Flags</span></span>           | <span data-ttu-id="2f8ec-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f8ec-150">0x00000000</span></span>                                 |
| <span data-ttu-id="2f8ec-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f8ec-151">System-Flags</span></span>           | <span data-ttu-id="2f8ec-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f8ec-152">0x00000010</span></span>                                 |
| <span data-ttu-id="2f8ec-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2f8ec-153">Classes used in</span></span>        | [<span data-ttu-id="2f8ec-154">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="2f8ec-154">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2f8ec-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2f8ec-155">Windows Server 2003</span></span>



| <span data-ttu-id="2f8ec-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="2f8ec-156">Entry</span></span> | <span data-ttu-id="2f8ec-157">Valor</span><span class="sxs-lookup"><span data-stu-id="2f8ec-157">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="2f8ec-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="2f8ec-158">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="2f8ec-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f8ec-159">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="2f8ec-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f8ec-160">System-Only</span></span>            | <span data-ttu-id="2f8ec-161">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-161">False</span></span>                                      |
| <span data-ttu-id="2f8ec-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2f8ec-162">Is-Single-Valued</span></span>       | <span data-ttu-id="2f8ec-163">True</span><span class="sxs-lookup"><span data-stu-id="2f8ec-163">True</span></span>                                       |
| <span data-ttu-id="2f8ec-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="2f8ec-164">Is Indexed</span></span>             | <span data-ttu-id="2f8ec-165">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-165">False</span></span>                                      |
| <span data-ttu-id="2f8ec-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2f8ec-166">In Global Catalog</span></span>      | <span data-ttu-id="2f8ec-167">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-167">False</span></span>                                      |
| <span data-ttu-id="2f8ec-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2f8ec-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f8ec-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2f8ec-169">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="2f8ec-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f8ec-170">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="2f8ec-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f8ec-171">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="2f8ec-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f8ec-172">Search-Flags</span></span>           | <span data-ttu-id="2f8ec-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f8ec-173">0x00000000</span></span>                                 |
| <span data-ttu-id="2f8ec-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f8ec-174">System-Flags</span></span>           | <span data-ttu-id="2f8ec-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f8ec-175">0x00000010</span></span>                                 |
| <span data-ttu-id="2f8ec-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2f8ec-176">Classes used in</span></span>        | [<span data-ttu-id="2f8ec-177">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="2f8ec-177">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2f8ec-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="2f8ec-178">ADAM</span></span>



| <span data-ttu-id="2f8ec-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="2f8ec-179">Entry</span></span> | <span data-ttu-id="2f8ec-180">Valor</span><span class="sxs-lookup"><span data-stu-id="2f8ec-180">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="2f8ec-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="2f8ec-181">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="2f8ec-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f8ec-182">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="2f8ec-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f8ec-183">System-Only</span></span>            | <span data-ttu-id="2f8ec-184">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-184">False</span></span>                                      |
| <span data-ttu-id="2f8ec-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2f8ec-185">Is-Single-Valued</span></span>       | <span data-ttu-id="2f8ec-186">True</span><span class="sxs-lookup"><span data-stu-id="2f8ec-186">True</span></span>                                       |
| <span data-ttu-id="2f8ec-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="2f8ec-187">Is Indexed</span></span>             | <span data-ttu-id="2f8ec-188">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-188">False</span></span>                                      |
| <span data-ttu-id="2f8ec-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2f8ec-189">In Global Catalog</span></span>      | <span data-ttu-id="2f8ec-190">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-190">False</span></span>                                      |
| <span data-ttu-id="2f8ec-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2f8ec-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f8ec-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2f8ec-192">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="2f8ec-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f8ec-193">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="2f8ec-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f8ec-194">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="2f8ec-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f8ec-195">Search-Flags</span></span>           | <span data-ttu-id="2f8ec-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f8ec-196">0x00000000</span></span>                                 |
| <span data-ttu-id="2f8ec-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f8ec-197">System-Flags</span></span>           | <span data-ttu-id="2f8ec-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f8ec-198">0x00000010</span></span>                                 |
| <span data-ttu-id="2f8ec-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2f8ec-199">Classes used in</span></span>        | [<span data-ttu-id="2f8ec-200">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="2f8ec-200">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2f8ec-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2f8ec-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2f8ec-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="2f8ec-202">Entry</span></span> | <span data-ttu-id="2f8ec-203">Valor</span><span class="sxs-lookup"><span data-stu-id="2f8ec-203">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="2f8ec-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="2f8ec-204">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="2f8ec-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f8ec-205">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="2f8ec-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f8ec-206">System-Only</span></span>            | <span data-ttu-id="2f8ec-207">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-207">False</span></span>                                      |
| <span data-ttu-id="2f8ec-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2f8ec-208">Is-Single-Valued</span></span>       | <span data-ttu-id="2f8ec-209">True</span><span class="sxs-lookup"><span data-stu-id="2f8ec-209">True</span></span>                                       |
| <span data-ttu-id="2f8ec-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="2f8ec-210">Is Indexed</span></span>             | <span data-ttu-id="2f8ec-211">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-211">False</span></span>                                      |
| <span data-ttu-id="2f8ec-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2f8ec-212">In Global Catalog</span></span>      | <span data-ttu-id="2f8ec-213">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-213">False</span></span>                                      |
| <span data-ttu-id="2f8ec-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2f8ec-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f8ec-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2f8ec-215">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="2f8ec-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f8ec-216">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="2f8ec-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f8ec-217">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="2f8ec-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f8ec-218">Search-Flags</span></span>           | <span data-ttu-id="2f8ec-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f8ec-219">0x00000000</span></span>                                 |
| <span data-ttu-id="2f8ec-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f8ec-220">System-Flags</span></span>           | <span data-ttu-id="2f8ec-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f8ec-221">0x00000010</span></span>                                 |
| <span data-ttu-id="2f8ec-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2f8ec-222">Classes used in</span></span>        | [<span data-ttu-id="2f8ec-223">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="2f8ec-223">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2f8ec-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f8ec-224">Windows Server 2008</span></span>



| <span data-ttu-id="2f8ec-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="2f8ec-225">Entry</span></span> | <span data-ttu-id="2f8ec-226">Valor</span><span class="sxs-lookup"><span data-stu-id="2f8ec-226">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="2f8ec-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="2f8ec-227">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="2f8ec-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f8ec-228">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="2f8ec-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f8ec-229">System-Only</span></span>            | <span data-ttu-id="2f8ec-230">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-230">False</span></span>                                      |
| <span data-ttu-id="2f8ec-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2f8ec-231">Is-Single-Valued</span></span>       | <span data-ttu-id="2f8ec-232">True</span><span class="sxs-lookup"><span data-stu-id="2f8ec-232">True</span></span>                                       |
| <span data-ttu-id="2f8ec-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="2f8ec-233">Is Indexed</span></span>             | <span data-ttu-id="2f8ec-234">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-234">False</span></span>                                      |
| <span data-ttu-id="2f8ec-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2f8ec-235">In Global Catalog</span></span>      | <span data-ttu-id="2f8ec-236">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-236">False</span></span>                                      |
| <span data-ttu-id="2f8ec-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2f8ec-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f8ec-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2f8ec-238">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="2f8ec-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f8ec-239">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="2f8ec-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f8ec-240">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="2f8ec-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f8ec-241">Search-Flags</span></span>           | <span data-ttu-id="2f8ec-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f8ec-242">0x00000000</span></span>                                 |
| <span data-ttu-id="2f8ec-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f8ec-243">System-Flags</span></span>           | <span data-ttu-id="2f8ec-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f8ec-244">0x00000010</span></span>                                 |
| <span data-ttu-id="2f8ec-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2f8ec-245">Classes used in</span></span>        | [<span data-ttu-id="2f8ec-246">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="2f8ec-246">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2f8ec-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2f8ec-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2f8ec-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="2f8ec-248">Entry</span></span> | <span data-ttu-id="2f8ec-249">Valor</span><span class="sxs-lookup"><span data-stu-id="2f8ec-249">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="2f8ec-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="2f8ec-250">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="2f8ec-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f8ec-251">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="2f8ec-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f8ec-252">System-Only</span></span>            | <span data-ttu-id="2f8ec-253">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-253">False</span></span>                                      |
| <span data-ttu-id="2f8ec-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2f8ec-254">Is-Single-Valued</span></span>       | <span data-ttu-id="2f8ec-255">True</span><span class="sxs-lookup"><span data-stu-id="2f8ec-255">True</span></span>                                       |
| <span data-ttu-id="2f8ec-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="2f8ec-256">Is Indexed</span></span>             | <span data-ttu-id="2f8ec-257">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-257">False</span></span>                                      |
| <span data-ttu-id="2f8ec-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2f8ec-258">In Global Catalog</span></span>      | <span data-ttu-id="2f8ec-259">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-259">False</span></span>                                      |
| <span data-ttu-id="2f8ec-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2f8ec-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f8ec-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2f8ec-261">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="2f8ec-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f8ec-262">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="2f8ec-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f8ec-263">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="2f8ec-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f8ec-264">Search-Flags</span></span>           | <span data-ttu-id="2f8ec-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f8ec-265">0x00000000</span></span>                                 |
| <span data-ttu-id="2f8ec-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f8ec-266">System-Flags</span></span>           | <span data-ttu-id="2f8ec-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f8ec-267">0x00000010</span></span>                                 |
| <span data-ttu-id="2f8ec-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2f8ec-268">Classes used in</span></span>        | [<span data-ttu-id="2f8ec-269">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="2f8ec-269">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2f8ec-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2f8ec-270">Windows Server 2012</span></span>



| <span data-ttu-id="2f8ec-271">Entrada</span><span class="sxs-lookup"><span data-stu-id="2f8ec-271">Entry</span></span> | <span data-ttu-id="2f8ec-272">Valor</span><span class="sxs-lookup"><span data-stu-id="2f8ec-272">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="2f8ec-273">ID do link</span><span class="sxs-lookup"><span data-stu-id="2f8ec-273">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="2f8ec-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f8ec-274">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="2f8ec-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f8ec-275">System-Only</span></span>            | <span data-ttu-id="2f8ec-276">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-276">False</span></span>                                      |
| <span data-ttu-id="2f8ec-277">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2f8ec-277">Is-Single-Valued</span></span>       | <span data-ttu-id="2f8ec-278">True</span><span class="sxs-lookup"><span data-stu-id="2f8ec-278">True</span></span>                                       |
| <span data-ttu-id="2f8ec-279">É indexado</span><span class="sxs-lookup"><span data-stu-id="2f8ec-279">Is Indexed</span></span>             | <span data-ttu-id="2f8ec-280">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-280">False</span></span>                                      |
| <span data-ttu-id="2f8ec-281">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2f8ec-281">In Global Catalog</span></span>      | <span data-ttu-id="2f8ec-282">Falso</span><span class="sxs-lookup"><span data-stu-id="2f8ec-282">False</span></span>                                      |
| <span data-ttu-id="2f8ec-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2f8ec-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f8ec-284">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2f8ec-284">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="2f8ec-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f8ec-285">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="2f8ec-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f8ec-286">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="2f8ec-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f8ec-287">Search-Flags</span></span>           | <span data-ttu-id="2f8ec-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f8ec-288">0x00000000</span></span>                                 |
| <span data-ttu-id="2f8ec-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f8ec-289">System-Flags</span></span>           | <span data-ttu-id="2f8ec-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f8ec-290">0x00000010</span></span>                                 |
| <span data-ttu-id="2f8ec-291">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2f8ec-291">Classes used in</span></span>        | [<span data-ttu-id="2f8ec-292">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="2f8ec-292">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





