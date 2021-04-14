---
title: Atributo ANR
description: Atributo de resolução de nome ambíguo a ser usado ao escolher entre objetos.
ms.assetid: 9057dc7e-f669-4821-86b0-703ff7e5b120
ms.tgt_platform: multiple
keywords:
- Esquema de atributos de atributo ANR
- Esquema de atributos de atributo aNR
topic_type:
- apiref
api_name:
- ANR
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28efc6d6871eb737f9c1953fbdb5ad5798f7fd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456315"
---
# <a name="anr-attribute"></a><span data-ttu-id="31c22-105">Atributo ANR</span><span class="sxs-lookup"><span data-stu-id="31c22-105">ANR attribute</span></span>

<span data-ttu-id="31c22-106">Atributo de resolução de nome ambíguo a ser usado ao escolher entre objetos.</span><span class="sxs-lookup"><span data-stu-id="31c22-106">Ambiguous name resolution attribute to be used when choosing between objects.</span></span>



| <span data-ttu-id="31c22-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="31c22-107">Entry</span></span> | <span data-ttu-id="31c22-108">Valor</span><span class="sxs-lookup"><span data-stu-id="31c22-108">Value</span></span> |
|-------------------|-------------------------------------------------------------------|
| <span data-ttu-id="31c22-109">CN</span><span class="sxs-lookup"><span data-stu-id="31c22-109">CN</span></span>                | <span data-ttu-id="31c22-110">ANR</span><span class="sxs-lookup"><span data-stu-id="31c22-110">ANR</span></span>                                                               |
| <span data-ttu-id="31c22-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="31c22-111">Ldap-Display-Name</span></span> | <span data-ttu-id="31c22-112">aNR</span><span class="sxs-lookup"><span data-stu-id="31c22-112">aNR</span></span>                                                               |
| <span data-ttu-id="31c22-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="31c22-113">Size</span></span>              | \-                                                                |
| <span data-ttu-id="31c22-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="31c22-114">Update Privilege</span></span>  | <span data-ttu-id="31c22-115">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="31c22-115">Schema administrator</span></span>                                              |
| <span data-ttu-id="31c22-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="31c22-116">Update Frequency</span></span>  | <span data-ttu-id="31c22-117">Quando um atributo precisa ser adicionado ou removido da lista ANR.</span><span class="sxs-lookup"><span data-stu-id="31c22-117">When an attribute needs to be added or removed from the ANR list.</span></span> |
| <span data-ttu-id="31c22-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="31c22-118">Attribute-Id</span></span>      | <span data-ttu-id="31c22-119">1.2.840.113556.1.4.1208</span><span class="sxs-lookup"><span data-stu-id="31c22-119">1.2.840.113556.1.4.1208</span></span>                                           |
| <span data-ttu-id="31c22-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="31c22-120">System-Id-Guid</span></span>    | <span data-ttu-id="31c22-121">45b01500-c419-11d1-bbc9-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="31c22-121">45b01500-c419-11d1-bbc9-0080c76670c0</span></span>                              |
| <span data-ttu-id="31c22-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="31c22-122">Syntax</span></span>            | [<span data-ttu-id="31c22-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="31c22-123">**String(Unicode)**</span></span>](s-string-unicode.md)                       |



## <a name="implementations"></a><span data-ttu-id="31c22-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="31c22-124">Implementations</span></span>

-   [<span data-ttu-id="31c22-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="31c22-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="31c22-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="31c22-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="31c22-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="31c22-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="31c22-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="31c22-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="31c22-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="31c22-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="31c22-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="31c22-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="31c22-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="31c22-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="31c22-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="31c22-132">Windows 2000 Server</span></span>



| <span data-ttu-id="31c22-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="31c22-133">Entry</span></span> | <span data-ttu-id="31c22-134">Valor</span><span class="sxs-lookup"><span data-stu-id="31c22-134">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="31c22-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="31c22-135">Link-Id</span></span>                | \-           |
| <span data-ttu-id="31c22-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31c22-136">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="31c22-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="31c22-137">System-Only</span></span>            | <span data-ttu-id="31c22-138">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-138">False</span></span>        |
| <span data-ttu-id="31c22-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="31c22-139">Is-Single-Valued</span></span>       | <span data-ttu-id="31c22-140">True</span><span class="sxs-lookup"><span data-stu-id="31c22-140">True</span></span>         |
| <span data-ttu-id="31c22-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="31c22-141">Is Indexed</span></span>             | <span data-ttu-id="31c22-142">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-142">False</span></span>        |
| <span data-ttu-id="31c22-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="31c22-143">In Global Catalog</span></span>      | <span data-ttu-id="31c22-144">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-144">False</span></span>        |
| <span data-ttu-id="31c22-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="31c22-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="31c22-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="31c22-146">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="31c22-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31c22-147">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="31c22-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31c22-148">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="31c22-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31c22-149">Search-Flags</span></span>           | <span data-ttu-id="31c22-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31c22-150">0x00000000</span></span>   |
| <span data-ttu-id="31c22-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31c22-151">System-Flags</span></span>           | <span data-ttu-id="31c22-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="31c22-152">0x08000014</span></span>   |
| <span data-ttu-id="31c22-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="31c22-153">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="31c22-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="31c22-154">Windows Server 2003</span></span>



| <span data-ttu-id="31c22-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="31c22-155">Entry</span></span> | <span data-ttu-id="31c22-156">Valor</span><span class="sxs-lookup"><span data-stu-id="31c22-156">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="31c22-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="31c22-157">Link-Id</span></span>                | \-           |
| <span data-ttu-id="31c22-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31c22-158">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="31c22-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="31c22-159">System-Only</span></span>            | <span data-ttu-id="31c22-160">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-160">False</span></span>        |
| <span data-ttu-id="31c22-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="31c22-161">Is-Single-Valued</span></span>       | <span data-ttu-id="31c22-162">True</span><span class="sxs-lookup"><span data-stu-id="31c22-162">True</span></span>         |
| <span data-ttu-id="31c22-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="31c22-163">Is Indexed</span></span>             | <span data-ttu-id="31c22-164">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-164">False</span></span>        |
| <span data-ttu-id="31c22-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="31c22-165">In Global Catalog</span></span>      | <span data-ttu-id="31c22-166">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-166">False</span></span>        |
| <span data-ttu-id="31c22-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="31c22-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="31c22-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="31c22-168">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="31c22-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31c22-169">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="31c22-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31c22-170">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="31c22-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31c22-171">Search-Flags</span></span>           | <span data-ttu-id="31c22-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31c22-172">0x00000000</span></span>   |
| <span data-ttu-id="31c22-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31c22-173">System-Flags</span></span>           | <span data-ttu-id="31c22-174">0x08000014</span><span class="sxs-lookup"><span data-stu-id="31c22-174">0x08000014</span></span>   |
| <span data-ttu-id="31c22-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="31c22-175">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="31c22-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="31c22-176">ADAM</span></span>



| <span data-ttu-id="31c22-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="31c22-177">Entry</span></span> | <span data-ttu-id="31c22-178">Valor</span><span class="sxs-lookup"><span data-stu-id="31c22-178">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="31c22-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="31c22-179">Link-Id</span></span>                | \-           |
| <span data-ttu-id="31c22-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31c22-180">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="31c22-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="31c22-181">System-Only</span></span>            | <span data-ttu-id="31c22-182">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-182">False</span></span>        |
| <span data-ttu-id="31c22-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="31c22-183">Is-Single-Valued</span></span>       | <span data-ttu-id="31c22-184">True</span><span class="sxs-lookup"><span data-stu-id="31c22-184">True</span></span>         |
| <span data-ttu-id="31c22-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="31c22-185">Is Indexed</span></span>             | <span data-ttu-id="31c22-186">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-186">False</span></span>        |
| <span data-ttu-id="31c22-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="31c22-187">In Global Catalog</span></span>      | <span data-ttu-id="31c22-188">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-188">False</span></span>        |
| <span data-ttu-id="31c22-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="31c22-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="31c22-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="31c22-190">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="31c22-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31c22-191">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="31c22-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31c22-192">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="31c22-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31c22-193">Search-Flags</span></span>           | <span data-ttu-id="31c22-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31c22-194">0x00000000</span></span>   |
| <span data-ttu-id="31c22-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31c22-195">System-Flags</span></span>           | <span data-ttu-id="31c22-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="31c22-196">0x08000014</span></span>   |
| <span data-ttu-id="31c22-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="31c22-197">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="31c22-198">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="31c22-198">Windows Server 2003 R2</span></span>



| <span data-ttu-id="31c22-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="31c22-199">Entry</span></span> | <span data-ttu-id="31c22-200">Valor</span><span class="sxs-lookup"><span data-stu-id="31c22-200">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="31c22-201">ID do link</span><span class="sxs-lookup"><span data-stu-id="31c22-201">Link-Id</span></span>                | \-           |
| <span data-ttu-id="31c22-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31c22-202">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="31c22-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="31c22-203">System-Only</span></span>            | <span data-ttu-id="31c22-204">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-204">False</span></span>        |
| <span data-ttu-id="31c22-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="31c22-205">Is-Single-Valued</span></span>       | <span data-ttu-id="31c22-206">True</span><span class="sxs-lookup"><span data-stu-id="31c22-206">True</span></span>         |
| <span data-ttu-id="31c22-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="31c22-207">Is Indexed</span></span>             | <span data-ttu-id="31c22-208">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-208">False</span></span>        |
| <span data-ttu-id="31c22-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="31c22-209">In Global Catalog</span></span>      | <span data-ttu-id="31c22-210">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-210">False</span></span>        |
| <span data-ttu-id="31c22-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="31c22-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="31c22-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="31c22-212">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="31c22-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31c22-213">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="31c22-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31c22-214">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="31c22-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31c22-215">Search-Flags</span></span>           | <span data-ttu-id="31c22-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31c22-216">0x00000000</span></span>   |
| <span data-ttu-id="31c22-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31c22-217">System-Flags</span></span>           | <span data-ttu-id="31c22-218">0x08000014</span><span class="sxs-lookup"><span data-stu-id="31c22-218">0x08000014</span></span>   |
| <span data-ttu-id="31c22-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="31c22-219">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="31c22-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31c22-220">Windows Server 2008</span></span>



| <span data-ttu-id="31c22-221">Entrada</span><span class="sxs-lookup"><span data-stu-id="31c22-221">Entry</span></span> | <span data-ttu-id="31c22-222">Valor</span><span class="sxs-lookup"><span data-stu-id="31c22-222">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="31c22-223">ID do link</span><span class="sxs-lookup"><span data-stu-id="31c22-223">Link-Id</span></span>                | \-           |
| <span data-ttu-id="31c22-224">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31c22-224">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="31c22-225">System-Only</span><span class="sxs-lookup"><span data-stu-id="31c22-225">System-Only</span></span>            | <span data-ttu-id="31c22-226">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-226">False</span></span>        |
| <span data-ttu-id="31c22-227">É de valor único</span><span class="sxs-lookup"><span data-stu-id="31c22-227">Is-Single-Valued</span></span>       | <span data-ttu-id="31c22-228">True</span><span class="sxs-lookup"><span data-stu-id="31c22-228">True</span></span>         |
| <span data-ttu-id="31c22-229">É indexado</span><span class="sxs-lookup"><span data-stu-id="31c22-229">Is Indexed</span></span>             | <span data-ttu-id="31c22-230">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-230">False</span></span>        |
| <span data-ttu-id="31c22-231">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="31c22-231">In Global Catalog</span></span>      | <span data-ttu-id="31c22-232">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-232">False</span></span>        |
| <span data-ttu-id="31c22-233">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="31c22-233">NT-Security-Descriptor</span></span> | <span data-ttu-id="31c22-234">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="31c22-234">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="31c22-235">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31c22-235">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="31c22-236">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31c22-236">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="31c22-237">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31c22-237">Search-Flags</span></span>           | <span data-ttu-id="31c22-238">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31c22-238">0x00000000</span></span>   |
| <span data-ttu-id="31c22-239">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31c22-239">System-Flags</span></span>           | <span data-ttu-id="31c22-240">0x08000014</span><span class="sxs-lookup"><span data-stu-id="31c22-240">0x08000014</span></span>   |
| <span data-ttu-id="31c22-241">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="31c22-241">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="31c22-242">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="31c22-242">Windows Server 2008 R2</span></span>



| <span data-ttu-id="31c22-243">Entrada</span><span class="sxs-lookup"><span data-stu-id="31c22-243">Entry</span></span> | <span data-ttu-id="31c22-244">Valor</span><span class="sxs-lookup"><span data-stu-id="31c22-244">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="31c22-245">ID do link</span><span class="sxs-lookup"><span data-stu-id="31c22-245">Link-Id</span></span>                | \-           |
| <span data-ttu-id="31c22-246">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31c22-246">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="31c22-247">System-Only</span><span class="sxs-lookup"><span data-stu-id="31c22-247">System-Only</span></span>            | <span data-ttu-id="31c22-248">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-248">False</span></span>        |
| <span data-ttu-id="31c22-249">É de valor único</span><span class="sxs-lookup"><span data-stu-id="31c22-249">Is-Single-Valued</span></span>       | <span data-ttu-id="31c22-250">True</span><span class="sxs-lookup"><span data-stu-id="31c22-250">True</span></span>         |
| <span data-ttu-id="31c22-251">É indexado</span><span class="sxs-lookup"><span data-stu-id="31c22-251">Is Indexed</span></span>             | <span data-ttu-id="31c22-252">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-252">False</span></span>        |
| <span data-ttu-id="31c22-253">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="31c22-253">In Global Catalog</span></span>      | <span data-ttu-id="31c22-254">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-254">False</span></span>        |
| <span data-ttu-id="31c22-255">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="31c22-255">NT-Security-Descriptor</span></span> | <span data-ttu-id="31c22-256">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="31c22-256">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="31c22-257">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31c22-257">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="31c22-258">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31c22-258">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="31c22-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31c22-259">Search-Flags</span></span>           | <span data-ttu-id="31c22-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31c22-260">0x00000000</span></span>   |
| <span data-ttu-id="31c22-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31c22-261">System-Flags</span></span>           | <span data-ttu-id="31c22-262">0x08000014</span><span class="sxs-lookup"><span data-stu-id="31c22-262">0x08000014</span></span>   |
| <span data-ttu-id="31c22-263">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="31c22-263">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="31c22-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="31c22-264">Windows Server 2012</span></span>



| <span data-ttu-id="31c22-265">Entrada</span><span class="sxs-lookup"><span data-stu-id="31c22-265">Entry</span></span> | <span data-ttu-id="31c22-266">Valor</span><span class="sxs-lookup"><span data-stu-id="31c22-266">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="31c22-267">ID do link</span><span class="sxs-lookup"><span data-stu-id="31c22-267">Link-Id</span></span>                | \-           |
| <span data-ttu-id="31c22-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31c22-268">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="31c22-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="31c22-269">System-Only</span></span>            | <span data-ttu-id="31c22-270">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-270">False</span></span>        |
| <span data-ttu-id="31c22-271">É de valor único</span><span class="sxs-lookup"><span data-stu-id="31c22-271">Is-Single-Valued</span></span>       | <span data-ttu-id="31c22-272">True</span><span class="sxs-lookup"><span data-stu-id="31c22-272">True</span></span>         |
| <span data-ttu-id="31c22-273">É indexado</span><span class="sxs-lookup"><span data-stu-id="31c22-273">Is Indexed</span></span>             | <span data-ttu-id="31c22-274">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-274">False</span></span>        |
| <span data-ttu-id="31c22-275">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="31c22-275">In Global Catalog</span></span>      | <span data-ttu-id="31c22-276">Falso</span><span class="sxs-lookup"><span data-stu-id="31c22-276">False</span></span>        |
| <span data-ttu-id="31c22-277">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="31c22-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="31c22-278">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="31c22-278">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="31c22-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31c22-279">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="31c22-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31c22-280">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="31c22-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31c22-281">Search-Flags</span></span>           | <span data-ttu-id="31c22-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31c22-282">0x00000000</span></span>   |
| <span data-ttu-id="31c22-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31c22-283">System-Flags</span></span>           | <span data-ttu-id="31c22-284">0x08000014</span><span class="sxs-lookup"><span data-stu-id="31c22-284">0x08000014</span></span>   |
| <span data-ttu-id="31c22-285">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="31c22-285">Classes used in</span></span>        | \-           |



 

 




