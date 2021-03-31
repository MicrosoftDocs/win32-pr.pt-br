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
# <a name="object-classes-attribute"></a><span data-ttu-id="1ebab-106">Object-Classes atributo</span><span class="sxs-lookup"><span data-stu-id="1ebab-106">Object-Classes attribute</span></span>

<span data-ttu-id="1ebab-107">Uma propriedade de valores múltiplos que contém cadeias de caracteres que representam cada classe no esquema.</span><span class="sxs-lookup"><span data-stu-id="1ebab-107">A multiple-valued property that contains strings that represent each class in the schema.</span></span> <span data-ttu-id="1ebab-108">Cada valor contém governsID, lDAPDisplayName, mustContain, mayContain e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="1ebab-108">Each value contains the governsID, lDAPDisplayName, mustContain, mayContain, and so on.</span></span>



| <span data-ttu-id="1ebab-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ebab-109">Entry</span></span> | <span data-ttu-id="1ebab-110">Valor</span><span class="sxs-lookup"><span data-stu-id="1ebab-110">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="1ebab-111">CN</span><span class="sxs-lookup"><span data-stu-id="1ebab-111">CN</span></span>                | <span data-ttu-id="1ebab-112">Object-Classes</span><span class="sxs-lookup"><span data-stu-id="1ebab-112">Object-Classes</span></span>                                   |
| <span data-ttu-id="1ebab-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1ebab-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1ebab-114">objectclasss</span><span class="sxs-lookup"><span data-stu-id="1ebab-114">objectClasses</span></span>                                    |
| <span data-ttu-id="1ebab-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="1ebab-115">Size</span></span>              | <span data-ttu-id="1ebab-116">Cerca de 20 bytes em média por nome de classe.</span><span class="sxs-lookup"><span data-stu-id="1ebab-116">About 20 bytes on average per class name.</span></span>        |
| <span data-ttu-id="1ebab-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="1ebab-117">Update Privilege</span></span>  | <span data-ttu-id="1ebab-118">O designer do objeto definiria esse valor.</span><span class="sxs-lookup"><span data-stu-id="1ebab-118">The designer of the object would set this value.</span></span> |
| <span data-ttu-id="1ebab-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="1ebab-119">Update Frequency</span></span>  | <span data-ttu-id="1ebab-120">Sempre que o design da classe é alterado.</span><span class="sxs-lookup"><span data-stu-id="1ebab-120">Whenever the design of the class changes.</span></span>        |
| <span data-ttu-id="1ebab-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1ebab-121">Attribute-Id</span></span>      | <span data-ttu-id="1ebab-122">2.5.21.6</span><span class="sxs-lookup"><span data-stu-id="1ebab-122">2.5.21.6</span></span>                                         |
| <span data-ttu-id="1ebab-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1ebab-123">System-Id-Guid</span></span>    | <span data-ttu-id="1ebab-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="1ebab-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span></span>             |
| <span data-ttu-id="1ebab-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ebab-125">Syntax</span></span>            | [<span data-ttu-id="1ebab-126">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1ebab-126">**String(Unicode)**</span></span>](s-string-unicode.md)      |



## <a name="implementations"></a><span data-ttu-id="1ebab-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="1ebab-127">Implementations</span></span>

-   [<span data-ttu-id="1ebab-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1ebab-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1ebab-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1ebab-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1ebab-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1ebab-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1ebab-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1ebab-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1ebab-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1ebab-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1ebab-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1ebab-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1ebab-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1ebab-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1ebab-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1ebab-135">Windows 2000 Server</span></span>



| <span data-ttu-id="1ebab-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ebab-136">Entry</span></span> | <span data-ttu-id="1ebab-137">Valor</span><span class="sxs-lookup"><span data-stu-id="1ebab-137">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="1ebab-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="1ebab-138">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="1ebab-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ebab-139">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="1ebab-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ebab-140">System-Only</span></span>            | <span data-ttu-id="1ebab-141">True</span><span class="sxs-lookup"><span data-stu-id="1ebab-141">True</span></span>                                        |
| <span data-ttu-id="1ebab-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1ebab-142">Is-Single-Valued</span></span>       | <span data-ttu-id="1ebab-143">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-143">False</span></span>                                       |
| <span data-ttu-id="1ebab-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="1ebab-144">Is Indexed</span></span>             | <span data-ttu-id="1ebab-145">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-145">False</span></span>                                       |
| <span data-ttu-id="1ebab-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ebab-146">In Global Catalog</span></span>      | <span data-ttu-id="1ebab-147">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-147">False</span></span>                                       |
| <span data-ttu-id="1ebab-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1ebab-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ebab-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1ebab-149">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="1ebab-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ebab-150">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="1ebab-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ebab-151">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="1ebab-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ebab-152">Search-Flags</span></span>           | <span data-ttu-id="1ebab-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ebab-153">0x00000000</span></span>                                  |
| <span data-ttu-id="1ebab-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ebab-154">System-Flags</span></span>           | <span data-ttu-id="1ebab-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1ebab-155">0x08000014</span></span>                                  |
| <span data-ttu-id="1ebab-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1ebab-156">Classes used in</span></span>        | [<span data-ttu-id="1ebab-157">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="1ebab-157">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1ebab-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1ebab-158">Windows Server 2003</span></span>



| <span data-ttu-id="1ebab-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ebab-159">Entry</span></span> | <span data-ttu-id="1ebab-160">Valor</span><span class="sxs-lookup"><span data-stu-id="1ebab-160">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="1ebab-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="1ebab-161">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="1ebab-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ebab-162">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="1ebab-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ebab-163">System-Only</span></span>            | <span data-ttu-id="1ebab-164">True</span><span class="sxs-lookup"><span data-stu-id="1ebab-164">True</span></span>                                        |
| <span data-ttu-id="1ebab-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1ebab-165">Is-Single-Valued</span></span>       | <span data-ttu-id="1ebab-166">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-166">False</span></span>                                       |
| <span data-ttu-id="1ebab-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="1ebab-167">Is Indexed</span></span>             | <span data-ttu-id="1ebab-168">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-168">False</span></span>                                       |
| <span data-ttu-id="1ebab-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ebab-169">In Global Catalog</span></span>      | <span data-ttu-id="1ebab-170">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-170">False</span></span>                                       |
| <span data-ttu-id="1ebab-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1ebab-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ebab-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1ebab-172">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="1ebab-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ebab-173">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="1ebab-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ebab-174">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="1ebab-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ebab-175">Search-Flags</span></span>           | <span data-ttu-id="1ebab-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ebab-176">0x00000000</span></span>                                  |
| <span data-ttu-id="1ebab-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ebab-177">System-Flags</span></span>           | <span data-ttu-id="1ebab-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1ebab-178">0x08000014</span></span>                                  |
| <span data-ttu-id="1ebab-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1ebab-179">Classes used in</span></span>        | [<span data-ttu-id="1ebab-180">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="1ebab-180">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1ebab-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="1ebab-181">ADAM</span></span>



| <span data-ttu-id="1ebab-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ebab-182">Entry</span></span> | <span data-ttu-id="1ebab-183">Valor</span><span class="sxs-lookup"><span data-stu-id="1ebab-183">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="1ebab-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="1ebab-184">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="1ebab-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ebab-185">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="1ebab-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ebab-186">System-Only</span></span>            | <span data-ttu-id="1ebab-187">True</span><span class="sxs-lookup"><span data-stu-id="1ebab-187">True</span></span>                                        |
| <span data-ttu-id="1ebab-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1ebab-188">Is-Single-Valued</span></span>       | <span data-ttu-id="1ebab-189">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-189">False</span></span>                                       |
| <span data-ttu-id="1ebab-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="1ebab-190">Is Indexed</span></span>             | <span data-ttu-id="1ebab-191">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-191">False</span></span>                                       |
| <span data-ttu-id="1ebab-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ebab-192">In Global Catalog</span></span>      | <span data-ttu-id="1ebab-193">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-193">False</span></span>                                       |
| <span data-ttu-id="1ebab-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1ebab-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ebab-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1ebab-195">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="1ebab-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ebab-196">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="1ebab-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ebab-197">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="1ebab-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ebab-198">Search-Flags</span></span>           | <span data-ttu-id="1ebab-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ebab-199">0x00000000</span></span>                                  |
| <span data-ttu-id="1ebab-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ebab-200">System-Flags</span></span>           | <span data-ttu-id="1ebab-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1ebab-201">0x08000014</span></span>                                  |
| <span data-ttu-id="1ebab-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1ebab-202">Classes used in</span></span>        | [<span data-ttu-id="1ebab-203">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="1ebab-203">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1ebab-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1ebab-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1ebab-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ebab-205">Entry</span></span> | <span data-ttu-id="1ebab-206">Valor</span><span class="sxs-lookup"><span data-stu-id="1ebab-206">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="1ebab-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="1ebab-207">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="1ebab-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ebab-208">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="1ebab-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ebab-209">System-Only</span></span>            | <span data-ttu-id="1ebab-210">True</span><span class="sxs-lookup"><span data-stu-id="1ebab-210">True</span></span>                                        |
| <span data-ttu-id="1ebab-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1ebab-211">Is-Single-Valued</span></span>       | <span data-ttu-id="1ebab-212">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-212">False</span></span>                                       |
| <span data-ttu-id="1ebab-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="1ebab-213">Is Indexed</span></span>             | <span data-ttu-id="1ebab-214">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-214">False</span></span>                                       |
| <span data-ttu-id="1ebab-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ebab-215">In Global Catalog</span></span>      | <span data-ttu-id="1ebab-216">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-216">False</span></span>                                       |
| <span data-ttu-id="1ebab-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1ebab-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ebab-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1ebab-218">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="1ebab-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ebab-219">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="1ebab-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ebab-220">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="1ebab-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ebab-221">Search-Flags</span></span>           | <span data-ttu-id="1ebab-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ebab-222">0x00000000</span></span>                                  |
| <span data-ttu-id="1ebab-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ebab-223">System-Flags</span></span>           | <span data-ttu-id="1ebab-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1ebab-224">0x08000014</span></span>                                  |
| <span data-ttu-id="1ebab-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1ebab-225">Classes used in</span></span>        | [<span data-ttu-id="1ebab-226">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="1ebab-226">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1ebab-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ebab-227">Windows Server 2008</span></span>



| <span data-ttu-id="1ebab-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ebab-228">Entry</span></span> | <span data-ttu-id="1ebab-229">Valor</span><span class="sxs-lookup"><span data-stu-id="1ebab-229">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="1ebab-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="1ebab-230">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="1ebab-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ebab-231">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="1ebab-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ebab-232">System-Only</span></span>            | <span data-ttu-id="1ebab-233">True</span><span class="sxs-lookup"><span data-stu-id="1ebab-233">True</span></span>                                        |
| <span data-ttu-id="1ebab-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1ebab-234">Is-Single-Valued</span></span>       | <span data-ttu-id="1ebab-235">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-235">False</span></span>                                       |
| <span data-ttu-id="1ebab-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="1ebab-236">Is Indexed</span></span>             | <span data-ttu-id="1ebab-237">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-237">False</span></span>                                       |
| <span data-ttu-id="1ebab-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ebab-238">In Global Catalog</span></span>      | <span data-ttu-id="1ebab-239">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-239">False</span></span>                                       |
| <span data-ttu-id="1ebab-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1ebab-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ebab-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1ebab-241">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="1ebab-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ebab-242">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="1ebab-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ebab-243">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="1ebab-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ebab-244">Search-Flags</span></span>           | <span data-ttu-id="1ebab-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ebab-245">0x00000000</span></span>                                  |
| <span data-ttu-id="1ebab-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ebab-246">System-Flags</span></span>           | <span data-ttu-id="1ebab-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1ebab-247">0x08000014</span></span>                                  |
| <span data-ttu-id="1ebab-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1ebab-248">Classes used in</span></span>        | [<span data-ttu-id="1ebab-249">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="1ebab-249">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1ebab-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1ebab-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1ebab-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ebab-251">Entry</span></span> | <span data-ttu-id="1ebab-252">Valor</span><span class="sxs-lookup"><span data-stu-id="1ebab-252">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="1ebab-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="1ebab-253">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="1ebab-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ebab-254">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="1ebab-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ebab-255">System-Only</span></span>            | <span data-ttu-id="1ebab-256">True</span><span class="sxs-lookup"><span data-stu-id="1ebab-256">True</span></span>                                        |
| <span data-ttu-id="1ebab-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1ebab-257">Is-Single-Valued</span></span>       | <span data-ttu-id="1ebab-258">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-258">False</span></span>                                       |
| <span data-ttu-id="1ebab-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="1ebab-259">Is Indexed</span></span>             | <span data-ttu-id="1ebab-260">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-260">False</span></span>                                       |
| <span data-ttu-id="1ebab-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ebab-261">In Global Catalog</span></span>      | <span data-ttu-id="1ebab-262">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-262">False</span></span>                                       |
| <span data-ttu-id="1ebab-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1ebab-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ebab-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1ebab-264">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="1ebab-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ebab-265">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="1ebab-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ebab-266">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="1ebab-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ebab-267">Search-Flags</span></span>           | <span data-ttu-id="1ebab-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ebab-268">0x00000000</span></span>                                  |
| <span data-ttu-id="1ebab-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ebab-269">System-Flags</span></span>           | <span data-ttu-id="1ebab-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1ebab-270">0x08000014</span></span>                                  |
| <span data-ttu-id="1ebab-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1ebab-271">Classes used in</span></span>        | [<span data-ttu-id="1ebab-272">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="1ebab-272">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1ebab-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1ebab-273">Windows Server 2012</span></span>



| <span data-ttu-id="1ebab-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ebab-274">Entry</span></span> | <span data-ttu-id="1ebab-275">Valor</span><span class="sxs-lookup"><span data-stu-id="1ebab-275">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="1ebab-276">ID do link</span><span class="sxs-lookup"><span data-stu-id="1ebab-276">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="1ebab-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ebab-277">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="1ebab-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ebab-278">System-Only</span></span>            | <span data-ttu-id="1ebab-279">True</span><span class="sxs-lookup"><span data-stu-id="1ebab-279">True</span></span>                                        |
| <span data-ttu-id="1ebab-280">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1ebab-280">Is-Single-Valued</span></span>       | <span data-ttu-id="1ebab-281">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-281">False</span></span>                                       |
| <span data-ttu-id="1ebab-282">É indexado</span><span class="sxs-lookup"><span data-stu-id="1ebab-282">Is Indexed</span></span>             | <span data-ttu-id="1ebab-283">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-283">False</span></span>                                       |
| <span data-ttu-id="1ebab-284">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1ebab-284">In Global Catalog</span></span>      | <span data-ttu-id="1ebab-285">Falso</span><span class="sxs-lookup"><span data-stu-id="1ebab-285">False</span></span>                                       |
| <span data-ttu-id="1ebab-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1ebab-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ebab-287">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1ebab-287">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="1ebab-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ebab-288">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="1ebab-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ebab-289">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="1ebab-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ebab-290">Search-Flags</span></span>           | <span data-ttu-id="1ebab-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ebab-291">0x00000000</span></span>                                  |
| <span data-ttu-id="1ebab-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ebab-292">System-Flags</span></span>           | <span data-ttu-id="1ebab-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="1ebab-293">0x08000014</span></span>                                  |
| <span data-ttu-id="1ebab-294">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1ebab-294">Classes used in</span></span>        | [<span data-ttu-id="1ebab-295">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="1ebab-295">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





