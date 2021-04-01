---
title: Object-Classes atributo
description: Uma propriedade de valores múltiplos que contém cadeias de caracteres que representam cada classe no esquema. Cada valor contém governsID, lDAPDisplayName, mustContain, mayContain e assim por diante.
ms.assetid: 7e3eda48-8e64-4a52-8d92-7a0d37e513ef
ms.tgt_platform: multiple
keywords:
- Esquema de Object-Classes do atributo AD
- atributo do AD de atributos objectclasss
topic_type:
- apiref
api_name:
- Object-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b799c725790115152ac70c0214d82a8c242ea600
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825311"
---
# <a name="object-classes-attribute"></a><span data-ttu-id="e0b66-106">Object-Classes atributo</span><span class="sxs-lookup"><span data-stu-id="e0b66-106">Object-Classes attribute</span></span>

<span data-ttu-id="e0b66-107">Uma propriedade de valores múltiplos que contém cadeias de caracteres que representam cada classe no esquema.</span><span class="sxs-lookup"><span data-stu-id="e0b66-107">A multiple-valued property that contains strings that represent each class in the schema.</span></span> <span data-ttu-id="e0b66-108">Cada valor contém governsID, lDAPDisplayName, mustContain, mayContain e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e0b66-108">Each value contains the governsID, lDAPDisplayName, mustContain, mayContain, and so on.</span></span>



| <span data-ttu-id="e0b66-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="e0b66-109">Entry</span></span> | <span data-ttu-id="e0b66-110">Valor</span><span class="sxs-lookup"><span data-stu-id="e0b66-110">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="e0b66-111">CN</span><span class="sxs-lookup"><span data-stu-id="e0b66-111">CN</span></span>                | <span data-ttu-id="e0b66-112">Object-Classes</span><span class="sxs-lookup"><span data-stu-id="e0b66-112">Object-Classes</span></span>                                   |
| <span data-ttu-id="e0b66-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e0b66-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e0b66-114">objectclasss</span><span class="sxs-lookup"><span data-stu-id="e0b66-114">objectClasses</span></span>                                    |
| <span data-ttu-id="e0b66-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="e0b66-115">Size</span></span>              | <span data-ttu-id="e0b66-116">Cerca de 20 bytes em média por nome de classe.</span><span class="sxs-lookup"><span data-stu-id="e0b66-116">About 20 bytes on average per class name.</span></span>        |
| <span data-ttu-id="e0b66-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="e0b66-117">Update Privilege</span></span>  | <span data-ttu-id="e0b66-118">O designer do objeto definiria esse valor.</span><span class="sxs-lookup"><span data-stu-id="e0b66-118">The designer of the object would set this value.</span></span> |
| <span data-ttu-id="e0b66-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="e0b66-119">Update Frequency</span></span>  | <span data-ttu-id="e0b66-120">Sempre que o design da classe é alterado.</span><span class="sxs-lookup"><span data-stu-id="e0b66-120">Whenever the design of the class changes.</span></span>        |
| <span data-ttu-id="e0b66-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e0b66-121">Attribute-Id</span></span>      | <span data-ttu-id="e0b66-122">2.5.21.6</span><span class="sxs-lookup"><span data-stu-id="e0b66-122">2.5.21.6</span></span>                                         |
| <span data-ttu-id="e0b66-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e0b66-123">System-Id-Guid</span></span>    | <span data-ttu-id="e0b66-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="e0b66-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span></span>             |
| <span data-ttu-id="e0b66-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0b66-125">Syntax</span></span>            | [<span data-ttu-id="e0b66-126">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e0b66-126">**String(Unicode)**</span></span>](s-string-unicode.md)      |



## <a name="implementations"></a><span data-ttu-id="e0b66-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="e0b66-127">Implementations</span></span>

-   [<span data-ttu-id="e0b66-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e0b66-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e0b66-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e0b66-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e0b66-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e0b66-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e0b66-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e0b66-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e0b66-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e0b66-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e0b66-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e0b66-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e0b66-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e0b66-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e0b66-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e0b66-135">Windows 2000 Server</span></span>



| <span data-ttu-id="e0b66-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="e0b66-136">Entry</span></span> | <span data-ttu-id="e0b66-137">Valor</span><span class="sxs-lookup"><span data-stu-id="e0b66-137">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="e0b66-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="e0b66-138">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="e0b66-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0b66-139">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="e0b66-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0b66-140">System-Only</span></span>            | <span data-ttu-id="e0b66-141">True</span><span class="sxs-lookup"><span data-stu-id="e0b66-141">True</span></span>                                        |
| <span data-ttu-id="e0b66-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e0b66-142">Is-Single-Valued</span></span>       | <span data-ttu-id="e0b66-143">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-143">False</span></span>                                       |
| <span data-ttu-id="e0b66-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="e0b66-144">Is Indexed</span></span>             | <span data-ttu-id="e0b66-145">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-145">False</span></span>                                       |
| <span data-ttu-id="e0b66-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e0b66-146">In Global Catalog</span></span>      | <span data-ttu-id="e0b66-147">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-147">False</span></span>                                       |
| <span data-ttu-id="e0b66-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0b66-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0b66-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e0b66-149">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="e0b66-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0b66-150">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="e0b66-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0b66-151">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="e0b66-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0b66-152">Search-Flags</span></span>           | <span data-ttu-id="e0b66-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0b66-153">0x00000000</span></span>                                  |
| <span data-ttu-id="e0b66-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0b66-154">System-Flags</span></span>           | <span data-ttu-id="e0b66-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e0b66-155">0x08000014</span></span>                                  |
| <span data-ttu-id="e0b66-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e0b66-156">Classes used in</span></span>        | [<span data-ttu-id="e0b66-157">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="e0b66-157">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e0b66-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e0b66-158">Windows Server 2003</span></span>



| <span data-ttu-id="e0b66-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="e0b66-159">Entry</span></span> | <span data-ttu-id="e0b66-160">Valor</span><span class="sxs-lookup"><span data-stu-id="e0b66-160">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="e0b66-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="e0b66-161">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="e0b66-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0b66-162">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="e0b66-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0b66-163">System-Only</span></span>            | <span data-ttu-id="e0b66-164">True</span><span class="sxs-lookup"><span data-stu-id="e0b66-164">True</span></span>                                        |
| <span data-ttu-id="e0b66-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e0b66-165">Is-Single-Valued</span></span>       | <span data-ttu-id="e0b66-166">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-166">False</span></span>                                       |
| <span data-ttu-id="e0b66-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="e0b66-167">Is Indexed</span></span>             | <span data-ttu-id="e0b66-168">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-168">False</span></span>                                       |
| <span data-ttu-id="e0b66-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e0b66-169">In Global Catalog</span></span>      | <span data-ttu-id="e0b66-170">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-170">False</span></span>                                       |
| <span data-ttu-id="e0b66-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0b66-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0b66-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e0b66-172">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="e0b66-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0b66-173">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="e0b66-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0b66-174">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="e0b66-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0b66-175">Search-Flags</span></span>           | <span data-ttu-id="e0b66-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0b66-176">0x00000000</span></span>                                  |
| <span data-ttu-id="e0b66-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0b66-177">System-Flags</span></span>           | <span data-ttu-id="e0b66-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e0b66-178">0x08000014</span></span>                                  |
| <span data-ttu-id="e0b66-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e0b66-179">Classes used in</span></span>        | [<span data-ttu-id="e0b66-180">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="e0b66-180">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e0b66-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="e0b66-181">ADAM</span></span>



| <span data-ttu-id="e0b66-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="e0b66-182">Entry</span></span> | <span data-ttu-id="e0b66-183">Valor</span><span class="sxs-lookup"><span data-stu-id="e0b66-183">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="e0b66-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="e0b66-184">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="e0b66-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0b66-185">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="e0b66-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0b66-186">System-Only</span></span>            | <span data-ttu-id="e0b66-187">True</span><span class="sxs-lookup"><span data-stu-id="e0b66-187">True</span></span>                                        |
| <span data-ttu-id="e0b66-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e0b66-188">Is-Single-Valued</span></span>       | <span data-ttu-id="e0b66-189">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-189">False</span></span>                                       |
| <span data-ttu-id="e0b66-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="e0b66-190">Is Indexed</span></span>             | <span data-ttu-id="e0b66-191">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-191">False</span></span>                                       |
| <span data-ttu-id="e0b66-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e0b66-192">In Global Catalog</span></span>      | <span data-ttu-id="e0b66-193">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-193">False</span></span>                                       |
| <span data-ttu-id="e0b66-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0b66-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0b66-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e0b66-195">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="e0b66-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0b66-196">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="e0b66-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0b66-197">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="e0b66-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0b66-198">Search-Flags</span></span>           | <span data-ttu-id="e0b66-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0b66-199">0x00000000</span></span>                                  |
| <span data-ttu-id="e0b66-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0b66-200">System-Flags</span></span>           | <span data-ttu-id="e0b66-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e0b66-201">0x08000014</span></span>                                  |
| <span data-ttu-id="e0b66-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e0b66-202">Classes used in</span></span>        | [<span data-ttu-id="e0b66-203">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="e0b66-203">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e0b66-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e0b66-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e0b66-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="e0b66-205">Entry</span></span> | <span data-ttu-id="e0b66-206">Valor</span><span class="sxs-lookup"><span data-stu-id="e0b66-206">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="e0b66-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="e0b66-207">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="e0b66-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0b66-208">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="e0b66-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0b66-209">System-Only</span></span>            | <span data-ttu-id="e0b66-210">True</span><span class="sxs-lookup"><span data-stu-id="e0b66-210">True</span></span>                                        |
| <span data-ttu-id="e0b66-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e0b66-211">Is-Single-Valued</span></span>       | <span data-ttu-id="e0b66-212">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-212">False</span></span>                                       |
| <span data-ttu-id="e0b66-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="e0b66-213">Is Indexed</span></span>             | <span data-ttu-id="e0b66-214">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-214">False</span></span>                                       |
| <span data-ttu-id="e0b66-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e0b66-215">In Global Catalog</span></span>      | <span data-ttu-id="e0b66-216">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-216">False</span></span>                                       |
| <span data-ttu-id="e0b66-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0b66-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0b66-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e0b66-218">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="e0b66-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0b66-219">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="e0b66-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0b66-220">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="e0b66-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0b66-221">Search-Flags</span></span>           | <span data-ttu-id="e0b66-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0b66-222">0x00000000</span></span>                                  |
| <span data-ttu-id="e0b66-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0b66-223">System-Flags</span></span>           | <span data-ttu-id="e0b66-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e0b66-224">0x08000014</span></span>                                  |
| <span data-ttu-id="e0b66-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e0b66-225">Classes used in</span></span>        | [<span data-ttu-id="e0b66-226">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="e0b66-226">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e0b66-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0b66-227">Windows Server 2008</span></span>



| <span data-ttu-id="e0b66-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="e0b66-228">Entry</span></span> | <span data-ttu-id="e0b66-229">Valor</span><span class="sxs-lookup"><span data-stu-id="e0b66-229">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="e0b66-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="e0b66-230">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="e0b66-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0b66-231">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="e0b66-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0b66-232">System-Only</span></span>            | <span data-ttu-id="e0b66-233">True</span><span class="sxs-lookup"><span data-stu-id="e0b66-233">True</span></span>                                        |
| <span data-ttu-id="e0b66-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e0b66-234">Is-Single-Valued</span></span>       | <span data-ttu-id="e0b66-235">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-235">False</span></span>                                       |
| <span data-ttu-id="e0b66-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="e0b66-236">Is Indexed</span></span>             | <span data-ttu-id="e0b66-237">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-237">False</span></span>                                       |
| <span data-ttu-id="e0b66-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e0b66-238">In Global Catalog</span></span>      | <span data-ttu-id="e0b66-239">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-239">False</span></span>                                       |
| <span data-ttu-id="e0b66-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0b66-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0b66-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e0b66-241">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="e0b66-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0b66-242">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="e0b66-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0b66-243">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="e0b66-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0b66-244">Search-Flags</span></span>           | <span data-ttu-id="e0b66-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0b66-245">0x00000000</span></span>                                  |
| <span data-ttu-id="e0b66-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0b66-246">System-Flags</span></span>           | <span data-ttu-id="e0b66-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e0b66-247">0x08000014</span></span>                                  |
| <span data-ttu-id="e0b66-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e0b66-248">Classes used in</span></span>        | [<span data-ttu-id="e0b66-249">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="e0b66-249">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e0b66-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e0b66-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e0b66-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="e0b66-251">Entry</span></span> | <span data-ttu-id="e0b66-252">Valor</span><span class="sxs-lookup"><span data-stu-id="e0b66-252">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="e0b66-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="e0b66-253">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="e0b66-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0b66-254">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="e0b66-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0b66-255">System-Only</span></span>            | <span data-ttu-id="e0b66-256">True</span><span class="sxs-lookup"><span data-stu-id="e0b66-256">True</span></span>                                        |
| <span data-ttu-id="e0b66-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e0b66-257">Is-Single-Valued</span></span>       | <span data-ttu-id="e0b66-258">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-258">False</span></span>                                       |
| <span data-ttu-id="e0b66-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="e0b66-259">Is Indexed</span></span>             | <span data-ttu-id="e0b66-260">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-260">False</span></span>                                       |
| <span data-ttu-id="e0b66-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e0b66-261">In Global Catalog</span></span>      | <span data-ttu-id="e0b66-262">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-262">False</span></span>                                       |
| <span data-ttu-id="e0b66-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0b66-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0b66-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e0b66-264">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="e0b66-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0b66-265">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="e0b66-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0b66-266">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="e0b66-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0b66-267">Search-Flags</span></span>           | <span data-ttu-id="e0b66-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0b66-268">0x00000000</span></span>                                  |
| <span data-ttu-id="e0b66-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0b66-269">System-Flags</span></span>           | <span data-ttu-id="e0b66-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e0b66-270">0x08000014</span></span>                                  |
| <span data-ttu-id="e0b66-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e0b66-271">Classes used in</span></span>        | [<span data-ttu-id="e0b66-272">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="e0b66-272">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e0b66-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e0b66-273">Windows Server 2012</span></span>



| <span data-ttu-id="e0b66-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="e0b66-274">Entry</span></span> | <span data-ttu-id="e0b66-275">Valor</span><span class="sxs-lookup"><span data-stu-id="e0b66-275">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="e0b66-276">ID do link</span><span class="sxs-lookup"><span data-stu-id="e0b66-276">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="e0b66-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0b66-277">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="e0b66-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0b66-278">System-Only</span></span>            | <span data-ttu-id="e0b66-279">True</span><span class="sxs-lookup"><span data-stu-id="e0b66-279">True</span></span>                                        |
| <span data-ttu-id="e0b66-280">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e0b66-280">Is-Single-Valued</span></span>       | <span data-ttu-id="e0b66-281">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-281">False</span></span>                                       |
| <span data-ttu-id="e0b66-282">É indexado</span><span class="sxs-lookup"><span data-stu-id="e0b66-282">Is Indexed</span></span>             | <span data-ttu-id="e0b66-283">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-283">False</span></span>                                       |
| <span data-ttu-id="e0b66-284">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e0b66-284">In Global Catalog</span></span>      | <span data-ttu-id="e0b66-285">Falso</span><span class="sxs-lookup"><span data-stu-id="e0b66-285">False</span></span>                                       |
| <span data-ttu-id="e0b66-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e0b66-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0b66-287">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e0b66-287">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="e0b66-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0b66-288">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="e0b66-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0b66-289">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="e0b66-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0b66-290">Search-Flags</span></span>           | <span data-ttu-id="e0b66-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0b66-291">0x00000000</span></span>                                  |
| <span data-ttu-id="e0b66-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0b66-292">System-Flags</span></span>           | <span data-ttu-id="e0b66-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e0b66-293">0x08000014</span></span>                                  |
| <span data-ttu-id="e0b66-294">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e0b66-294">Classes used in</span></span>        | [<span data-ttu-id="e0b66-295">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="e0b66-295">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





