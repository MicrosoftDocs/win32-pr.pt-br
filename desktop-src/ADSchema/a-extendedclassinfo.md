---
title: Atributo de informações de classe estendida
description: Uma propriedade com valores múltiplos que contém cadeias de caracteres que representam informações adicionais para cada classe. Cada valor contém o governsID, lDAPDisplayName e schemaIDGUID da classe.
ms.assetid: f0f07950-28f8-4fe7-b030-1ab7632569e1
ms.tgt_platform: multiple
keywords:
- Atributo de anúncio de classe de informações estendidas
- Esquema de AD do atributo extendedClassInfo
topic_type:
- apiref
api_name:
- Extended-Class-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1b3320f547a3dbb41a151a33765cf9729e82c6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104369962"
---
# <a name="extended-class-info-attribute"></a><span data-ttu-id="5ee72-106">Atributo de informações de classe estendida</span><span class="sxs-lookup"><span data-stu-id="5ee72-106">Extended-Class-Info attribute</span></span>

<span data-ttu-id="5ee72-107">Uma propriedade com valores múltiplos que contém cadeias de caracteres que representam informações adicionais para cada classe.</span><span class="sxs-lookup"><span data-stu-id="5ee72-107">A multi-valued property that contains strings that represent additional information for each class.</span></span> <span data-ttu-id="5ee72-108">Cada valor contém o governsID, lDAPDisplayName e schemaIDGUID da classe.</span><span class="sxs-lookup"><span data-stu-id="5ee72-108">Each value contains the governsID, lDAPDisplayName, and schemaIDGUID of the class.</span></span>



| <span data-ttu-id="5ee72-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ee72-109">Entry</span></span> | <span data-ttu-id="5ee72-110">Valor</span><span class="sxs-lookup"><span data-stu-id="5ee72-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="5ee72-111">CN</span><span class="sxs-lookup"><span data-stu-id="5ee72-111">CN</span></span>                | <span data-ttu-id="5ee72-112">Informações de classe estendida</span><span class="sxs-lookup"><span data-stu-id="5ee72-112">Extended-Class-Info</span></span>                         |
| <span data-ttu-id="5ee72-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5ee72-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5ee72-114">extendedClassInfo</span><span class="sxs-lookup"><span data-stu-id="5ee72-114">extendedClassInfo</span></span>                           |
| <span data-ttu-id="5ee72-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="5ee72-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="5ee72-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="5ee72-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="5ee72-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="5ee72-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="5ee72-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5ee72-118">Attribute-Id</span></span>      | <span data-ttu-id="5ee72-119">1.2.840.113556.1.4.908</span><span class="sxs-lookup"><span data-stu-id="5ee72-119">1.2.840.113556.1.4.908</span></span>                      |
| <span data-ttu-id="5ee72-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5ee72-120">System-Id-Guid</span></span>    | <span data-ttu-id="5ee72-121">9a7ad948-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="5ee72-121">9a7ad948-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="5ee72-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ee72-122">Syntax</span></span>            | [<span data-ttu-id="5ee72-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5ee72-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="5ee72-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="5ee72-124">Implementations</span></span>

-   [<span data-ttu-id="5ee72-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5ee72-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5ee72-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5ee72-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5ee72-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="5ee72-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="5ee72-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5ee72-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5ee72-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5ee72-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5ee72-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5ee72-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5ee72-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5ee72-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5ee72-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5ee72-132">Windows 2000 Server</span></span>



| <span data-ttu-id="5ee72-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ee72-133">Entry</span></span> | <span data-ttu-id="5ee72-134">Valor</span><span class="sxs-lookup"><span data-stu-id="5ee72-134">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="5ee72-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="5ee72-135">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="5ee72-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ee72-136">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="5ee72-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ee72-137">System-Only</span></span>            | <span data-ttu-id="5ee72-138">True</span><span class="sxs-lookup"><span data-stu-id="5ee72-138">True</span></span>                                        |
| <span data-ttu-id="5ee72-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5ee72-139">Is-Single-Valued</span></span>       | <span data-ttu-id="5ee72-140">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-140">False</span></span>                                       |
| <span data-ttu-id="5ee72-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="5ee72-141">Is Indexed</span></span>             | <span data-ttu-id="5ee72-142">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-142">False</span></span>                                       |
| <span data-ttu-id="5ee72-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5ee72-143">In Global Catalog</span></span>      | <span data-ttu-id="5ee72-144">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-144">False</span></span>                                       |
| <span data-ttu-id="5ee72-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5ee72-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ee72-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5ee72-146">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="5ee72-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ee72-147">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="5ee72-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ee72-148">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="5ee72-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ee72-149">Search-Flags</span></span>           | <span data-ttu-id="5ee72-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ee72-150">0x00000000</span></span>                                  |
| <span data-ttu-id="5ee72-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ee72-151">System-Flags</span></span>           | <span data-ttu-id="5ee72-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5ee72-152">0x08000014</span></span>                                  |
| <span data-ttu-id="5ee72-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5ee72-153">Classes used in</span></span>        | [<span data-ttu-id="5ee72-154">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="5ee72-154">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5ee72-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5ee72-155">Windows Server 2003</span></span>



| <span data-ttu-id="5ee72-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ee72-156">Entry</span></span> | <span data-ttu-id="5ee72-157">Valor</span><span class="sxs-lookup"><span data-stu-id="5ee72-157">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="5ee72-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="5ee72-158">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="5ee72-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ee72-159">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="5ee72-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ee72-160">System-Only</span></span>            | <span data-ttu-id="5ee72-161">True</span><span class="sxs-lookup"><span data-stu-id="5ee72-161">True</span></span>                                        |
| <span data-ttu-id="5ee72-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5ee72-162">Is-Single-Valued</span></span>       | <span data-ttu-id="5ee72-163">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-163">False</span></span>                                       |
| <span data-ttu-id="5ee72-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="5ee72-164">Is Indexed</span></span>             | <span data-ttu-id="5ee72-165">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-165">False</span></span>                                       |
| <span data-ttu-id="5ee72-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5ee72-166">In Global Catalog</span></span>      | <span data-ttu-id="5ee72-167">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-167">False</span></span>                                       |
| <span data-ttu-id="5ee72-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5ee72-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ee72-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5ee72-169">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="5ee72-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ee72-170">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="5ee72-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ee72-171">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="5ee72-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ee72-172">Search-Flags</span></span>           | <span data-ttu-id="5ee72-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ee72-173">0x00000000</span></span>                                  |
| <span data-ttu-id="5ee72-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ee72-174">System-Flags</span></span>           | <span data-ttu-id="5ee72-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5ee72-175">0x08000014</span></span>                                  |
| <span data-ttu-id="5ee72-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5ee72-176">Classes used in</span></span>        | [<span data-ttu-id="5ee72-177">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="5ee72-177">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="5ee72-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="5ee72-178">ADAM</span></span>



| <span data-ttu-id="5ee72-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ee72-179">Entry</span></span> | <span data-ttu-id="5ee72-180">Valor</span><span class="sxs-lookup"><span data-stu-id="5ee72-180">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="5ee72-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="5ee72-181">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="5ee72-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ee72-182">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="5ee72-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ee72-183">System-Only</span></span>            | <span data-ttu-id="5ee72-184">True</span><span class="sxs-lookup"><span data-stu-id="5ee72-184">True</span></span>                                        |
| <span data-ttu-id="5ee72-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5ee72-185">Is-Single-Valued</span></span>       | <span data-ttu-id="5ee72-186">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-186">False</span></span>                                       |
| <span data-ttu-id="5ee72-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="5ee72-187">Is Indexed</span></span>             | <span data-ttu-id="5ee72-188">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-188">False</span></span>                                       |
| <span data-ttu-id="5ee72-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5ee72-189">In Global Catalog</span></span>      | <span data-ttu-id="5ee72-190">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-190">False</span></span>                                       |
| <span data-ttu-id="5ee72-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5ee72-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ee72-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5ee72-192">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="5ee72-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ee72-193">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="5ee72-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ee72-194">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="5ee72-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ee72-195">Search-Flags</span></span>           | <span data-ttu-id="5ee72-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ee72-196">0x00000000</span></span>                                  |
| <span data-ttu-id="5ee72-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ee72-197">System-Flags</span></span>           | <span data-ttu-id="5ee72-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5ee72-198">0x08000014</span></span>                                  |
| <span data-ttu-id="5ee72-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5ee72-199">Classes used in</span></span>        | [<span data-ttu-id="5ee72-200">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="5ee72-200">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5ee72-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5ee72-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5ee72-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ee72-202">Entry</span></span> | <span data-ttu-id="5ee72-203">Valor</span><span class="sxs-lookup"><span data-stu-id="5ee72-203">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="5ee72-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="5ee72-204">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="5ee72-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ee72-205">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="5ee72-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ee72-206">System-Only</span></span>            | <span data-ttu-id="5ee72-207">True</span><span class="sxs-lookup"><span data-stu-id="5ee72-207">True</span></span>                                        |
| <span data-ttu-id="5ee72-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5ee72-208">Is-Single-Valued</span></span>       | <span data-ttu-id="5ee72-209">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-209">False</span></span>                                       |
| <span data-ttu-id="5ee72-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="5ee72-210">Is Indexed</span></span>             | <span data-ttu-id="5ee72-211">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-211">False</span></span>                                       |
| <span data-ttu-id="5ee72-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5ee72-212">In Global Catalog</span></span>      | <span data-ttu-id="5ee72-213">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-213">False</span></span>                                       |
| <span data-ttu-id="5ee72-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5ee72-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ee72-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5ee72-215">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="5ee72-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ee72-216">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="5ee72-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ee72-217">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="5ee72-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ee72-218">Search-Flags</span></span>           | <span data-ttu-id="5ee72-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ee72-219">0x00000000</span></span>                                  |
| <span data-ttu-id="5ee72-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ee72-220">System-Flags</span></span>           | <span data-ttu-id="5ee72-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5ee72-221">0x08000014</span></span>                                  |
| <span data-ttu-id="5ee72-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5ee72-222">Classes used in</span></span>        | [<span data-ttu-id="5ee72-223">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="5ee72-223">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5ee72-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ee72-224">Windows Server 2008</span></span>



| <span data-ttu-id="5ee72-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ee72-225">Entry</span></span> | <span data-ttu-id="5ee72-226">Valor</span><span class="sxs-lookup"><span data-stu-id="5ee72-226">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="5ee72-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="5ee72-227">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="5ee72-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ee72-228">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="5ee72-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ee72-229">System-Only</span></span>            | <span data-ttu-id="5ee72-230">True</span><span class="sxs-lookup"><span data-stu-id="5ee72-230">True</span></span>                                        |
| <span data-ttu-id="5ee72-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5ee72-231">Is-Single-Valued</span></span>       | <span data-ttu-id="5ee72-232">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-232">False</span></span>                                       |
| <span data-ttu-id="5ee72-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="5ee72-233">Is Indexed</span></span>             | <span data-ttu-id="5ee72-234">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-234">False</span></span>                                       |
| <span data-ttu-id="5ee72-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5ee72-235">In Global Catalog</span></span>      | <span data-ttu-id="5ee72-236">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-236">False</span></span>                                       |
| <span data-ttu-id="5ee72-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5ee72-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ee72-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5ee72-238">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="5ee72-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ee72-239">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="5ee72-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ee72-240">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="5ee72-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ee72-241">Search-Flags</span></span>           | <span data-ttu-id="5ee72-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ee72-242">0x00000000</span></span>                                  |
| <span data-ttu-id="5ee72-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ee72-243">System-Flags</span></span>           | <span data-ttu-id="5ee72-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5ee72-244">0x08000014</span></span>                                  |
| <span data-ttu-id="5ee72-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5ee72-245">Classes used in</span></span>        | [<span data-ttu-id="5ee72-246">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="5ee72-246">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5ee72-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5ee72-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5ee72-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ee72-248">Entry</span></span> | <span data-ttu-id="5ee72-249">Valor</span><span class="sxs-lookup"><span data-stu-id="5ee72-249">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="5ee72-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="5ee72-250">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="5ee72-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ee72-251">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="5ee72-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ee72-252">System-Only</span></span>            | <span data-ttu-id="5ee72-253">True</span><span class="sxs-lookup"><span data-stu-id="5ee72-253">True</span></span>                                        |
| <span data-ttu-id="5ee72-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5ee72-254">Is-Single-Valued</span></span>       | <span data-ttu-id="5ee72-255">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-255">False</span></span>                                       |
| <span data-ttu-id="5ee72-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="5ee72-256">Is Indexed</span></span>             | <span data-ttu-id="5ee72-257">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-257">False</span></span>                                       |
| <span data-ttu-id="5ee72-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5ee72-258">In Global Catalog</span></span>      | <span data-ttu-id="5ee72-259">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-259">False</span></span>                                       |
| <span data-ttu-id="5ee72-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5ee72-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ee72-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5ee72-261">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="5ee72-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ee72-262">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="5ee72-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ee72-263">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="5ee72-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ee72-264">Search-Flags</span></span>           | <span data-ttu-id="5ee72-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ee72-265">0x00000000</span></span>                                  |
| <span data-ttu-id="5ee72-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ee72-266">System-Flags</span></span>           | <span data-ttu-id="5ee72-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5ee72-267">0x08000014</span></span>                                  |
| <span data-ttu-id="5ee72-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5ee72-268">Classes used in</span></span>        | [<span data-ttu-id="5ee72-269">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="5ee72-269">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5ee72-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ee72-270">Windows Server 2012</span></span>



| <span data-ttu-id="5ee72-271">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ee72-271">Entry</span></span> | <span data-ttu-id="5ee72-272">Valor</span><span class="sxs-lookup"><span data-stu-id="5ee72-272">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="5ee72-273">ID do link</span><span class="sxs-lookup"><span data-stu-id="5ee72-273">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="5ee72-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ee72-274">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="5ee72-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ee72-275">System-Only</span></span>            | <span data-ttu-id="5ee72-276">True</span><span class="sxs-lookup"><span data-stu-id="5ee72-276">True</span></span>                                        |
| <span data-ttu-id="5ee72-277">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5ee72-277">Is-Single-Valued</span></span>       | <span data-ttu-id="5ee72-278">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-278">False</span></span>                                       |
| <span data-ttu-id="5ee72-279">É indexado</span><span class="sxs-lookup"><span data-stu-id="5ee72-279">Is Indexed</span></span>             | <span data-ttu-id="5ee72-280">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-280">False</span></span>                                       |
| <span data-ttu-id="5ee72-281">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5ee72-281">In Global Catalog</span></span>      | <span data-ttu-id="5ee72-282">Falso</span><span class="sxs-lookup"><span data-stu-id="5ee72-282">False</span></span>                                       |
| <span data-ttu-id="5ee72-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5ee72-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ee72-284">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5ee72-284">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="5ee72-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ee72-285">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="5ee72-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ee72-286">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="5ee72-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ee72-287">Search-Flags</span></span>           | <span data-ttu-id="5ee72-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ee72-288">0x00000000</span></span>                                  |
| <span data-ttu-id="5ee72-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ee72-289">System-Flags</span></span>           | <span data-ttu-id="5ee72-290">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5ee72-290">0x08000014</span></span>                                  |
| <span data-ttu-id="5ee72-291">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5ee72-291">Classes used in</span></span>        | [<span data-ttu-id="5ee72-292">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="5ee72-292">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





