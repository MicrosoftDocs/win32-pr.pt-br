---
title: É um atributo de valor único
description: Se for TRUE, esse atributo só poderá armazenar um valor.
ms.assetid: 53dd8dfe-2123-4a61-a346-12abe340ea11
ms.tgt_platform: multiple
keywords:
- É um esquema de AD de atributo de valor único
- Esquema de AD do atributo isSingleValued
topic_type:
- apiref
api_name:
- Is-Single-Valued
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a1fafd047afa47b874fb0385a690e2c0d13161
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103824992"
---
# <a name="is-single-valued-attribute"></a><span data-ttu-id="7bc8f-105">É um atributo de valor único</span><span class="sxs-lookup"><span data-stu-id="7bc8f-105">Is-Single-Valued attribute</span></span>

<span data-ttu-id="7bc8f-106">Se **for true**, esse atributo só poderá armazenar um valor.</span><span class="sxs-lookup"><span data-stu-id="7bc8f-106">If **TRUE**, this attribute can only store one value.</span></span>



| <span data-ttu-id="7bc8f-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bc8f-107">Entry</span></span> | <span data-ttu-id="7bc8f-108">Valor</span><span class="sxs-lookup"><span data-stu-id="7bc8f-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7bc8f-109">CN</span><span class="sxs-lookup"><span data-stu-id="7bc8f-109">CN</span></span>                | <span data-ttu-id="7bc8f-110">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7bc8f-110">Is-Single-Valued</span></span>                     |
| <span data-ttu-id="7bc8f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7bc8f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7bc8f-112">isSingleValued</span><span class="sxs-lookup"><span data-stu-id="7bc8f-112">isSingleValued</span></span>                       |
| <span data-ttu-id="7bc8f-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="7bc8f-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="7bc8f-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="7bc8f-114">Update Privilege</span></span>  | <span data-ttu-id="7bc8f-115">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="7bc8f-115">Schema administrator</span></span>                 |
| <span data-ttu-id="7bc8f-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="7bc8f-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7bc8f-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7bc8f-117">Attribute-Id</span></span>      | <span data-ttu-id="7bc8f-118">1.2.840.113556.1.2.33</span><span class="sxs-lookup"><span data-stu-id="7bc8f-118">1.2.840.113556.1.2.33</span></span>                |
| <span data-ttu-id="7bc8f-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7bc8f-119">System-Id-Guid</span></span>    | <span data-ttu-id="7bc8f-120">bf967992-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7bc8f-120">bf967992-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="7bc8f-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bc8f-121">Syntax</span></span>            | [<span data-ttu-id="7bc8f-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7bc8f-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="7bc8f-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="7bc8f-123">Implementations</span></span>

-   [<span data-ttu-id="7bc8f-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7bc8f-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7bc8f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7bc8f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7bc8f-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7bc8f-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7bc8f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7bc8f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7bc8f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7bc8f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7bc8f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7bc8f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7bc8f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7bc8f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7bc8f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7bc8f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="7bc8f-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bc8f-132">Entry</span></span> | <span data-ttu-id="7bc8f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="7bc8f-133">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="7bc8f-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="7bc8f-134">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="7bc8f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bc8f-135">MAPI-Id</span></span>                | <span data-ttu-id="7bc8f-136">0x80C1</span><span class="sxs-lookup"><span data-stu-id="7bc8f-136">0x80C1</span></span>                                                   |
| <span data-ttu-id="7bc8f-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bc8f-137">System-Only</span></span>            | <span data-ttu-id="7bc8f-138">True</span><span class="sxs-lookup"><span data-stu-id="7bc8f-138">True</span></span>                                                     |
| <span data-ttu-id="7bc8f-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7bc8f-139">Is-Single-Valued</span></span>       | <span data-ttu-id="7bc8f-140">True</span><span class="sxs-lookup"><span data-stu-id="7bc8f-140">True</span></span>                                                     |
| <span data-ttu-id="7bc8f-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="7bc8f-141">Is Indexed</span></span>             | <span data-ttu-id="7bc8f-142">Falso</span><span class="sxs-lookup"><span data-stu-id="7bc8f-142">False</span></span>                                                    |
| <span data-ttu-id="7bc8f-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bc8f-143">In Global Catalog</span></span>      | <span data-ttu-id="7bc8f-144">Falso</span><span class="sxs-lookup"><span data-stu-id="7bc8f-144">False</span></span>                                                    |
| <span data-ttu-id="7bc8f-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7bc8f-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bc8f-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7bc8f-146">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="7bc8f-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bc8f-147">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="7bc8f-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bc8f-148">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="7bc8f-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc8f-149">Search-Flags</span></span>           | <span data-ttu-id="7bc8f-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bc8f-150">0x00000000</span></span>                                               |
| <span data-ttu-id="7bc8f-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc8f-151">System-Flags</span></span>           | <span data-ttu-id="7bc8f-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bc8f-152">0x00000010</span></span>                                               |
| <span data-ttu-id="7bc8f-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7bc8f-153">Classes used in</span></span>        | [<span data-ttu-id="7bc8f-154">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="7bc8f-154">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7bc8f-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7bc8f-155">Windows Server 2003</span></span>



| <span data-ttu-id="7bc8f-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bc8f-156">Entry</span></span> | <span data-ttu-id="7bc8f-157">Valor</span><span class="sxs-lookup"><span data-stu-id="7bc8f-157">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="7bc8f-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="7bc8f-158">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="7bc8f-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bc8f-159">MAPI-Id</span></span>                | <span data-ttu-id="7bc8f-160">0x80C1</span><span class="sxs-lookup"><span data-stu-id="7bc8f-160">0x80C1</span></span>                                                   |
| <span data-ttu-id="7bc8f-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bc8f-161">System-Only</span></span>            | <span data-ttu-id="7bc8f-162">True</span><span class="sxs-lookup"><span data-stu-id="7bc8f-162">True</span></span>                                                     |
| <span data-ttu-id="7bc8f-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7bc8f-163">Is-Single-Valued</span></span>       | <span data-ttu-id="7bc8f-164">True</span><span class="sxs-lookup"><span data-stu-id="7bc8f-164">True</span></span>                                                     |
| <span data-ttu-id="7bc8f-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="7bc8f-165">Is Indexed</span></span>             | <span data-ttu-id="7bc8f-166">Falso</span><span class="sxs-lookup"><span data-stu-id="7bc8f-166">False</span></span>                                                    |
| <span data-ttu-id="7bc8f-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bc8f-167">In Global Catalog</span></span>      | <span data-ttu-id="7bc8f-168">Falso</span><span class="sxs-lookup"><span data-stu-id="7bc8f-168">False</span></span>                                                    |
| <span data-ttu-id="7bc8f-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7bc8f-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bc8f-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7bc8f-170">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="7bc8f-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bc8f-171">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="7bc8f-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bc8f-172">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="7bc8f-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc8f-173">Search-Flags</span></span>           | <span data-ttu-id="7bc8f-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bc8f-174">0x00000000</span></span>                                               |
| <span data-ttu-id="7bc8f-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc8f-175">System-Flags</span></span>           | <span data-ttu-id="7bc8f-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bc8f-176">0x00000010</span></span>                                               |
| <span data-ttu-id="7bc8f-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7bc8f-177">Classes used in</span></span>        | [<span data-ttu-id="7bc8f-178">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="7bc8f-178">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7bc8f-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="7bc8f-179">ADAM</span></span>



| <span data-ttu-id="7bc8f-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bc8f-180">Entry</span></span> | <span data-ttu-id="7bc8f-181">Valor</span><span class="sxs-lookup"><span data-stu-id="7bc8f-181">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="7bc8f-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="7bc8f-182">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="7bc8f-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bc8f-183">MAPI-Id</span></span>                | <span data-ttu-id="7bc8f-184">0x80C1</span><span class="sxs-lookup"><span data-stu-id="7bc8f-184">0x80C1</span></span>                                                   |
| <span data-ttu-id="7bc8f-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bc8f-185">System-Only</span></span>            | <span data-ttu-id="7bc8f-186">True</span><span class="sxs-lookup"><span data-stu-id="7bc8f-186">True</span></span>                                                     |
| <span data-ttu-id="7bc8f-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7bc8f-187">Is-Single-Valued</span></span>       | <span data-ttu-id="7bc8f-188">True</span><span class="sxs-lookup"><span data-stu-id="7bc8f-188">True</span></span>                                                     |
| <span data-ttu-id="7bc8f-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="7bc8f-189">Is Indexed</span></span>             | <span data-ttu-id="7bc8f-190">Falso</span><span class="sxs-lookup"><span data-stu-id="7bc8f-190">False</span></span>                                                    |
| <span data-ttu-id="7bc8f-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bc8f-191">In Global Catalog</span></span>      | <span data-ttu-id="7bc8f-192">Falso</span><span class="sxs-lookup"><span data-stu-id="7bc8f-192">False</span></span>                                                    |
| <span data-ttu-id="7bc8f-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7bc8f-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bc8f-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7bc8f-194">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="7bc8f-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bc8f-195">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="7bc8f-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bc8f-196">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="7bc8f-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc8f-197">Search-Flags</span></span>           | <span data-ttu-id="7bc8f-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bc8f-198">0x00000000</span></span>                                               |
| <span data-ttu-id="7bc8f-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc8f-199">System-Flags</span></span>           | <span data-ttu-id="7bc8f-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bc8f-200">0x00000010</span></span>                                               |
| <span data-ttu-id="7bc8f-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7bc8f-201">Classes used in</span></span>        | [<span data-ttu-id="7bc8f-202">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="7bc8f-202">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7bc8f-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7bc8f-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7bc8f-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bc8f-204">Entry</span></span> | <span data-ttu-id="7bc8f-205">Valor</span><span class="sxs-lookup"><span data-stu-id="7bc8f-205">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="7bc8f-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="7bc8f-206">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="7bc8f-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bc8f-207">MAPI-Id</span></span>                | <span data-ttu-id="7bc8f-208">0x80C1</span><span class="sxs-lookup"><span data-stu-id="7bc8f-208">0x80C1</span></span>                                                   |
| <span data-ttu-id="7bc8f-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bc8f-209">System-Only</span></span>            | <span data-ttu-id="7bc8f-210">True</span><span class="sxs-lookup"><span data-stu-id="7bc8f-210">True</span></span>                                                     |
| <span data-ttu-id="7bc8f-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7bc8f-211">Is-Single-Valued</span></span>       | <span data-ttu-id="7bc8f-212">True</span><span class="sxs-lookup"><span data-stu-id="7bc8f-212">True</span></span>                                                     |
| <span data-ttu-id="7bc8f-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="7bc8f-213">Is Indexed</span></span>             | <span data-ttu-id="7bc8f-214">Falso</span><span class="sxs-lookup"><span data-stu-id="7bc8f-214">False</span></span>                                                    |
| <span data-ttu-id="7bc8f-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bc8f-215">In Global Catalog</span></span>      | <span data-ttu-id="7bc8f-216">Falso</span><span class="sxs-lookup"><span data-stu-id="7bc8f-216">False</span></span>                                                    |
| <span data-ttu-id="7bc8f-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7bc8f-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bc8f-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7bc8f-218">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="7bc8f-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bc8f-219">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="7bc8f-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bc8f-220">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="7bc8f-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc8f-221">Search-Flags</span></span>           | <span data-ttu-id="7bc8f-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bc8f-222">0x00000000</span></span>                                               |
| <span data-ttu-id="7bc8f-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc8f-223">System-Flags</span></span>           | <span data-ttu-id="7bc8f-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bc8f-224">0x00000010</span></span>                                               |
| <span data-ttu-id="7bc8f-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7bc8f-225">Classes used in</span></span>        | [<span data-ttu-id="7bc8f-226">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="7bc8f-226">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7bc8f-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7bc8f-227">Windows Server 2008</span></span>



| <span data-ttu-id="7bc8f-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bc8f-228">Entry</span></span> | <span data-ttu-id="7bc8f-229">Valor</span><span class="sxs-lookup"><span data-stu-id="7bc8f-229">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="7bc8f-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="7bc8f-230">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="7bc8f-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bc8f-231">MAPI-Id</span></span>                | <span data-ttu-id="7bc8f-232">0x80C1</span><span class="sxs-lookup"><span data-stu-id="7bc8f-232">0x80C1</span></span>                                                   |
| <span data-ttu-id="7bc8f-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bc8f-233">System-Only</span></span>            | <span data-ttu-id="7bc8f-234">True</span><span class="sxs-lookup"><span data-stu-id="7bc8f-234">True</span></span>                                                     |
| <span data-ttu-id="7bc8f-235">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7bc8f-235">Is-Single-Valued</span></span>       | <span data-ttu-id="7bc8f-236">True</span><span class="sxs-lookup"><span data-stu-id="7bc8f-236">True</span></span>                                                     |
| <span data-ttu-id="7bc8f-237">É indexado</span><span class="sxs-lookup"><span data-stu-id="7bc8f-237">Is Indexed</span></span>             | <span data-ttu-id="7bc8f-238">Falso</span><span class="sxs-lookup"><span data-stu-id="7bc8f-238">False</span></span>                                                    |
| <span data-ttu-id="7bc8f-239">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bc8f-239">In Global Catalog</span></span>      | <span data-ttu-id="7bc8f-240">Falso</span><span class="sxs-lookup"><span data-stu-id="7bc8f-240">False</span></span>                                                    |
| <span data-ttu-id="7bc8f-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7bc8f-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bc8f-242">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7bc8f-242">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="7bc8f-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bc8f-243">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="7bc8f-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bc8f-244">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="7bc8f-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc8f-245">Search-Flags</span></span>           | <span data-ttu-id="7bc8f-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bc8f-246">0x00000000</span></span>                                               |
| <span data-ttu-id="7bc8f-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc8f-247">System-Flags</span></span>           | <span data-ttu-id="7bc8f-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bc8f-248">0x00000010</span></span>                                               |
| <span data-ttu-id="7bc8f-249">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7bc8f-249">Classes used in</span></span>        | [<span data-ttu-id="7bc8f-250">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="7bc8f-250">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7bc8f-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7bc8f-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7bc8f-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bc8f-252">Entry</span></span> | <span data-ttu-id="7bc8f-253">Valor</span><span class="sxs-lookup"><span data-stu-id="7bc8f-253">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="7bc8f-254">ID do link</span><span class="sxs-lookup"><span data-stu-id="7bc8f-254">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="7bc8f-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bc8f-255">MAPI-Id</span></span>                | <span data-ttu-id="7bc8f-256">0x80C1</span><span class="sxs-lookup"><span data-stu-id="7bc8f-256">0x80C1</span></span>                                                   |
| <span data-ttu-id="7bc8f-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bc8f-257">System-Only</span></span>            | <span data-ttu-id="7bc8f-258">True</span><span class="sxs-lookup"><span data-stu-id="7bc8f-258">True</span></span>                                                     |
| <span data-ttu-id="7bc8f-259">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7bc8f-259">Is-Single-Valued</span></span>       | <span data-ttu-id="7bc8f-260">True</span><span class="sxs-lookup"><span data-stu-id="7bc8f-260">True</span></span>                                                     |
| <span data-ttu-id="7bc8f-261">É indexado</span><span class="sxs-lookup"><span data-stu-id="7bc8f-261">Is Indexed</span></span>             | <span data-ttu-id="7bc8f-262">Falso</span><span class="sxs-lookup"><span data-stu-id="7bc8f-262">False</span></span>                                                    |
| <span data-ttu-id="7bc8f-263">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bc8f-263">In Global Catalog</span></span>      | <span data-ttu-id="7bc8f-264">Falso</span><span class="sxs-lookup"><span data-stu-id="7bc8f-264">False</span></span>                                                    |
| <span data-ttu-id="7bc8f-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7bc8f-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bc8f-266">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7bc8f-266">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="7bc8f-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bc8f-267">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="7bc8f-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bc8f-268">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="7bc8f-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc8f-269">Search-Flags</span></span>           | <span data-ttu-id="7bc8f-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bc8f-270">0x00000000</span></span>                                               |
| <span data-ttu-id="7bc8f-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc8f-271">System-Flags</span></span>           | <span data-ttu-id="7bc8f-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bc8f-272">0x00000010</span></span>                                               |
| <span data-ttu-id="7bc8f-273">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7bc8f-273">Classes used in</span></span>        | [<span data-ttu-id="7bc8f-274">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="7bc8f-274">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7bc8f-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7bc8f-275">Windows Server 2012</span></span>



| <span data-ttu-id="7bc8f-276">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bc8f-276">Entry</span></span> | <span data-ttu-id="7bc8f-277">Valor</span><span class="sxs-lookup"><span data-stu-id="7bc8f-277">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="7bc8f-278">ID do link</span><span class="sxs-lookup"><span data-stu-id="7bc8f-278">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="7bc8f-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bc8f-279">MAPI-Id</span></span>                | <span data-ttu-id="7bc8f-280">0x80C1</span><span class="sxs-lookup"><span data-stu-id="7bc8f-280">0x80C1</span></span>                                                   |
| <span data-ttu-id="7bc8f-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bc8f-281">System-Only</span></span>            | <span data-ttu-id="7bc8f-282">True</span><span class="sxs-lookup"><span data-stu-id="7bc8f-282">True</span></span>                                                     |
| <span data-ttu-id="7bc8f-283">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7bc8f-283">Is-Single-Valued</span></span>       | <span data-ttu-id="7bc8f-284">True</span><span class="sxs-lookup"><span data-stu-id="7bc8f-284">True</span></span>                                                     |
| <span data-ttu-id="7bc8f-285">É indexado</span><span class="sxs-lookup"><span data-stu-id="7bc8f-285">Is Indexed</span></span>             | <span data-ttu-id="7bc8f-286">Falso</span><span class="sxs-lookup"><span data-stu-id="7bc8f-286">False</span></span>                                                    |
| <span data-ttu-id="7bc8f-287">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bc8f-287">In Global Catalog</span></span>      | <span data-ttu-id="7bc8f-288">Falso</span><span class="sxs-lookup"><span data-stu-id="7bc8f-288">False</span></span>                                                    |
| <span data-ttu-id="7bc8f-289">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7bc8f-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bc8f-290">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7bc8f-290">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="7bc8f-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bc8f-291">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="7bc8f-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bc8f-292">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="7bc8f-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc8f-293">Search-Flags</span></span>           | <span data-ttu-id="7bc8f-294">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bc8f-294">0x00000000</span></span>                                               |
| <span data-ttu-id="7bc8f-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bc8f-295">System-Flags</span></span>           | <span data-ttu-id="7bc8f-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bc8f-296">0x00000010</span></span>                                               |
| <span data-ttu-id="7bc8f-297">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7bc8f-297">Classes used in</span></span>        | [<span data-ttu-id="7bc8f-298">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="7bc8f-298">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





