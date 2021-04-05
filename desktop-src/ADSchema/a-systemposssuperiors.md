---
title: System-poss-superior atributo
description: A lista de classes que podem conter esta classe. Essa lista só pode ser modificada pelo sistema.
ms.assetid: 8b98249a-fe9a-4a42-abb8-a8b042250a76
ms.tgt_platform: multiple
keywords:
- System-poss-superior atributo AD Schema
- Esquema de AD do atributo systemPossSuperiors
topic_type:
- apiref
api_name:
- System-Poss-Superiors
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b2116dfb8d2ad21d8a52854b1eb98ef156eb46a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825266"
---
# <a name="system-poss-superiors-attribute"></a><span data-ttu-id="1e882-106">System-poss-superior atributo</span><span class="sxs-lookup"><span data-stu-id="1e882-106">System-Poss-Superiors attribute</span></span>

<span data-ttu-id="1e882-107">A lista de classes que podem conter esta classe.</span><span class="sxs-lookup"><span data-stu-id="1e882-107">The list of classes that can contain this class.</span></span> <span data-ttu-id="1e882-108">Essa lista só pode ser modificada pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="1e882-108">This list can only be modified by the system.</span></span>



| <span data-ttu-id="1e882-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e882-109">Entry</span></span> | <span data-ttu-id="1e882-110">Valor</span><span class="sxs-lookup"><span data-stu-id="1e882-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="1e882-111">CN</span><span class="sxs-lookup"><span data-stu-id="1e882-111">CN</span></span>                | <span data-ttu-id="1e882-112">Sistema-poss-superiors</span><span class="sxs-lookup"><span data-stu-id="1e882-112">System-Poss-Superiors</span></span>                                                       |
| <span data-ttu-id="1e882-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1e882-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1e882-114">systemPossSuperiors</span><span class="sxs-lookup"><span data-stu-id="1e882-114">systemPossSuperiors</span></span>                                                         |
| <span data-ttu-id="1e882-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="1e882-115">Size</span></span>              | \-                                                                          |
| <span data-ttu-id="1e882-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="1e882-116">Update Privilege</span></span>  | <span data-ttu-id="1e882-117">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="1e882-117">Schema administrator</span></span>                                                        |
| <span data-ttu-id="1e882-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="1e882-118">Update Frequency</span></span>  | <span data-ttu-id="1e882-119">Quando a classe é criada ou um novo superior possível é adicionado à classe.</span><span class="sxs-lookup"><span data-stu-id="1e882-119">When the class is created or a new possible superior is added to the class.</span></span> |
| <span data-ttu-id="1e882-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1e882-120">Attribute-Id</span></span>      | <span data-ttu-id="1e882-121">1.2.840.113556.1.4.195</span><span class="sxs-lookup"><span data-stu-id="1e882-121">1.2.840.113556.1.4.195</span></span>                                                      |
| <span data-ttu-id="1e882-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1e882-122">System-Id-Guid</span></span>    | <span data-ttu-id="1e882-123">bf967a47-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1e882-123">bf967a47-0de6-11d0-a285-00aa003049e2</span></span>                                        |
| <span data-ttu-id="1e882-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e882-124">Syntax</span></span>            | [<span data-ttu-id="1e882-125">**Cadeia de caracteres (identificador de objeto)**</span><span class="sxs-lookup"><span data-stu-id="1e882-125">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)             |



## <a name="implementations"></a><span data-ttu-id="1e882-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="1e882-126">Implementations</span></span>

-   [<span data-ttu-id="1e882-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1e882-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1e882-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1e882-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1e882-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1e882-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1e882-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1e882-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1e882-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1e882-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1e882-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1e882-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1e882-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1e882-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1e882-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1e882-134">Windows 2000 Server</span></span>



| <span data-ttu-id="1e882-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e882-135">Entry</span></span> | <span data-ttu-id="1e882-136">Valor</span><span class="sxs-lookup"><span data-stu-id="1e882-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="1e882-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="1e882-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="1e882-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e882-138">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="1e882-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e882-139">System-Only</span></span>            | <span data-ttu-id="1e882-140">True</span><span class="sxs-lookup"><span data-stu-id="1e882-140">True</span></span>                                             |
| <span data-ttu-id="1e882-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1e882-141">Is-Single-Valued</span></span>       | <span data-ttu-id="1e882-142">Falso</span><span class="sxs-lookup"><span data-stu-id="1e882-142">False</span></span>                                            |
| <span data-ttu-id="1e882-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="1e882-143">Is Indexed</span></span>             | <span data-ttu-id="1e882-144">Falso</span><span class="sxs-lookup"><span data-stu-id="1e882-144">False</span></span>                                            |
| <span data-ttu-id="1e882-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e882-145">In Global Catalog</span></span>      | <span data-ttu-id="1e882-146">True</span><span class="sxs-lookup"><span data-stu-id="1e882-146">True</span></span>                                             |
| <span data-ttu-id="1e882-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1e882-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e882-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1e882-148">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="1e882-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e882-149">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="1e882-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e882-150">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="1e882-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e882-151">Search-Flags</span></span>           | <span data-ttu-id="1e882-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e882-152">0x00000000</span></span>                                       |
| <span data-ttu-id="1e882-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e882-153">System-Flags</span></span>           | <span data-ttu-id="1e882-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e882-154">0x00000010</span></span>                                       |
| <span data-ttu-id="1e882-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1e882-155">Classes used in</span></span>        | [<span data-ttu-id="1e882-156">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="1e882-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1e882-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1e882-157">Windows Server 2003</span></span>



| <span data-ttu-id="1e882-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e882-158">Entry</span></span> | <span data-ttu-id="1e882-159">Valor</span><span class="sxs-lookup"><span data-stu-id="1e882-159">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="1e882-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="1e882-160">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="1e882-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e882-161">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="1e882-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e882-162">System-Only</span></span>            | <span data-ttu-id="1e882-163">True</span><span class="sxs-lookup"><span data-stu-id="1e882-163">True</span></span>                                             |
| <span data-ttu-id="1e882-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1e882-164">Is-Single-Valued</span></span>       | <span data-ttu-id="1e882-165">Falso</span><span class="sxs-lookup"><span data-stu-id="1e882-165">False</span></span>                                            |
| <span data-ttu-id="1e882-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="1e882-166">Is Indexed</span></span>             | <span data-ttu-id="1e882-167">Falso</span><span class="sxs-lookup"><span data-stu-id="1e882-167">False</span></span>                                            |
| <span data-ttu-id="1e882-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e882-168">In Global Catalog</span></span>      | <span data-ttu-id="1e882-169">True</span><span class="sxs-lookup"><span data-stu-id="1e882-169">True</span></span>                                             |
| <span data-ttu-id="1e882-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1e882-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e882-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1e882-171">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="1e882-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e882-172">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="1e882-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e882-173">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="1e882-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e882-174">Search-Flags</span></span>           | <span data-ttu-id="1e882-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e882-175">0x00000000</span></span>                                       |
| <span data-ttu-id="1e882-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e882-176">System-Flags</span></span>           | <span data-ttu-id="1e882-177">0x00000012</span><span class="sxs-lookup"><span data-stu-id="1e882-177">0x00000012</span></span>                                       |
| <span data-ttu-id="1e882-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1e882-178">Classes used in</span></span>        | [<span data-ttu-id="1e882-179">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="1e882-179">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1e882-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="1e882-180">ADAM</span></span>



| <span data-ttu-id="1e882-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e882-181">Entry</span></span> | <span data-ttu-id="1e882-182">Valor</span><span class="sxs-lookup"><span data-stu-id="1e882-182">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="1e882-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="1e882-183">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="1e882-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e882-184">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="1e882-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e882-185">System-Only</span></span>            | <span data-ttu-id="1e882-186">True</span><span class="sxs-lookup"><span data-stu-id="1e882-186">True</span></span>                                             |
| <span data-ttu-id="1e882-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1e882-187">Is-Single-Valued</span></span>       | <span data-ttu-id="1e882-188">Falso</span><span class="sxs-lookup"><span data-stu-id="1e882-188">False</span></span>                                            |
| <span data-ttu-id="1e882-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="1e882-189">Is Indexed</span></span>             | <span data-ttu-id="1e882-190">Falso</span><span class="sxs-lookup"><span data-stu-id="1e882-190">False</span></span>                                            |
| <span data-ttu-id="1e882-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e882-191">In Global Catalog</span></span>      | <span data-ttu-id="1e882-192">True</span><span class="sxs-lookup"><span data-stu-id="1e882-192">True</span></span>                                             |
| <span data-ttu-id="1e882-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1e882-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e882-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1e882-194">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="1e882-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e882-195">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="1e882-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e882-196">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="1e882-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e882-197">Search-Flags</span></span>           | <span data-ttu-id="1e882-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e882-198">0x00000000</span></span>                                       |
| <span data-ttu-id="1e882-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e882-199">System-Flags</span></span>           | <span data-ttu-id="1e882-200">0x00000012</span><span class="sxs-lookup"><span data-stu-id="1e882-200">0x00000012</span></span>                                       |
| <span data-ttu-id="1e882-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1e882-201">Classes used in</span></span>        | [<span data-ttu-id="1e882-202">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="1e882-202">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1e882-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1e882-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1e882-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e882-204">Entry</span></span> | <span data-ttu-id="1e882-205">Valor</span><span class="sxs-lookup"><span data-stu-id="1e882-205">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="1e882-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="1e882-206">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="1e882-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e882-207">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="1e882-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e882-208">System-Only</span></span>            | <span data-ttu-id="1e882-209">True</span><span class="sxs-lookup"><span data-stu-id="1e882-209">True</span></span>                                             |
| <span data-ttu-id="1e882-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1e882-210">Is-Single-Valued</span></span>       | <span data-ttu-id="1e882-211">Falso</span><span class="sxs-lookup"><span data-stu-id="1e882-211">False</span></span>                                            |
| <span data-ttu-id="1e882-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="1e882-212">Is Indexed</span></span>             | <span data-ttu-id="1e882-213">Falso</span><span class="sxs-lookup"><span data-stu-id="1e882-213">False</span></span>                                            |
| <span data-ttu-id="1e882-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e882-214">In Global Catalog</span></span>      | <span data-ttu-id="1e882-215">True</span><span class="sxs-lookup"><span data-stu-id="1e882-215">True</span></span>                                             |
| <span data-ttu-id="1e882-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1e882-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e882-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1e882-217">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="1e882-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e882-218">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="1e882-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e882-219">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="1e882-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e882-220">Search-Flags</span></span>           | <span data-ttu-id="1e882-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e882-221">0x00000000</span></span>                                       |
| <span data-ttu-id="1e882-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e882-222">System-Flags</span></span>           | <span data-ttu-id="1e882-223">0x00000012</span><span class="sxs-lookup"><span data-stu-id="1e882-223">0x00000012</span></span>                                       |
| <span data-ttu-id="1e882-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1e882-224">Classes used in</span></span>        | [<span data-ttu-id="1e882-225">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="1e882-225">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1e882-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e882-226">Windows Server 2008</span></span>



| <span data-ttu-id="1e882-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e882-227">Entry</span></span> | <span data-ttu-id="1e882-228">Valor</span><span class="sxs-lookup"><span data-stu-id="1e882-228">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="1e882-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="1e882-229">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="1e882-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e882-230">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="1e882-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e882-231">System-Only</span></span>            | <span data-ttu-id="1e882-232">True</span><span class="sxs-lookup"><span data-stu-id="1e882-232">True</span></span>                                             |
| <span data-ttu-id="1e882-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1e882-233">Is-Single-Valued</span></span>       | <span data-ttu-id="1e882-234">Falso</span><span class="sxs-lookup"><span data-stu-id="1e882-234">False</span></span>                                            |
| <span data-ttu-id="1e882-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="1e882-235">Is Indexed</span></span>             | <span data-ttu-id="1e882-236">Falso</span><span class="sxs-lookup"><span data-stu-id="1e882-236">False</span></span>                                            |
| <span data-ttu-id="1e882-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e882-237">In Global Catalog</span></span>      | <span data-ttu-id="1e882-238">True</span><span class="sxs-lookup"><span data-stu-id="1e882-238">True</span></span>                                             |
| <span data-ttu-id="1e882-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1e882-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e882-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1e882-240">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="1e882-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e882-241">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="1e882-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e882-242">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="1e882-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e882-243">Search-Flags</span></span>           | <span data-ttu-id="1e882-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e882-244">0x00000000</span></span>                                       |
| <span data-ttu-id="1e882-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e882-245">System-Flags</span></span>           | <span data-ttu-id="1e882-246">0x00000012</span><span class="sxs-lookup"><span data-stu-id="1e882-246">0x00000012</span></span>                                       |
| <span data-ttu-id="1e882-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1e882-247">Classes used in</span></span>        | [<span data-ttu-id="1e882-248">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="1e882-248">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1e882-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1e882-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1e882-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e882-250">Entry</span></span> | <span data-ttu-id="1e882-251">Valor</span><span class="sxs-lookup"><span data-stu-id="1e882-251">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="1e882-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="1e882-252">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="1e882-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e882-253">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="1e882-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e882-254">System-Only</span></span>            | <span data-ttu-id="1e882-255">True</span><span class="sxs-lookup"><span data-stu-id="1e882-255">True</span></span>                                             |
| <span data-ttu-id="1e882-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1e882-256">Is-Single-Valued</span></span>       | <span data-ttu-id="1e882-257">Falso</span><span class="sxs-lookup"><span data-stu-id="1e882-257">False</span></span>                                            |
| <span data-ttu-id="1e882-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="1e882-258">Is Indexed</span></span>             | <span data-ttu-id="1e882-259">Falso</span><span class="sxs-lookup"><span data-stu-id="1e882-259">False</span></span>                                            |
| <span data-ttu-id="1e882-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e882-260">In Global Catalog</span></span>      | <span data-ttu-id="1e882-261">True</span><span class="sxs-lookup"><span data-stu-id="1e882-261">True</span></span>                                             |
| <span data-ttu-id="1e882-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1e882-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e882-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1e882-263">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="1e882-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e882-264">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="1e882-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e882-265">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="1e882-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e882-266">Search-Flags</span></span>           | <span data-ttu-id="1e882-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e882-267">0x00000000</span></span>                                       |
| <span data-ttu-id="1e882-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e882-268">System-Flags</span></span>           | <span data-ttu-id="1e882-269">0x00000012</span><span class="sxs-lookup"><span data-stu-id="1e882-269">0x00000012</span></span>                                       |
| <span data-ttu-id="1e882-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1e882-270">Classes used in</span></span>        | [<span data-ttu-id="1e882-271">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="1e882-271">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1e882-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1e882-272">Windows Server 2012</span></span>



| <span data-ttu-id="1e882-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e882-273">Entry</span></span> | <span data-ttu-id="1e882-274">Valor</span><span class="sxs-lookup"><span data-stu-id="1e882-274">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="1e882-275">ID do link</span><span class="sxs-lookup"><span data-stu-id="1e882-275">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="1e882-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e882-276">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="1e882-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e882-277">System-Only</span></span>            | <span data-ttu-id="1e882-278">True</span><span class="sxs-lookup"><span data-stu-id="1e882-278">True</span></span>                                             |
| <span data-ttu-id="1e882-279">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1e882-279">Is-Single-Valued</span></span>       | <span data-ttu-id="1e882-280">Falso</span><span class="sxs-lookup"><span data-stu-id="1e882-280">False</span></span>                                            |
| <span data-ttu-id="1e882-281">É indexado</span><span class="sxs-lookup"><span data-stu-id="1e882-281">Is Indexed</span></span>             | <span data-ttu-id="1e882-282">Falso</span><span class="sxs-lookup"><span data-stu-id="1e882-282">False</span></span>                                            |
| <span data-ttu-id="1e882-283">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e882-283">In Global Catalog</span></span>      | <span data-ttu-id="1e882-284">True</span><span class="sxs-lookup"><span data-stu-id="1e882-284">True</span></span>                                             |
| <span data-ttu-id="1e882-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1e882-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e882-286">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1e882-286">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="1e882-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e882-287">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="1e882-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e882-288">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="1e882-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e882-289">Search-Flags</span></span>           | <span data-ttu-id="1e882-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e882-290">0x00000000</span></span>                                       |
| <span data-ttu-id="1e882-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e882-291">System-Flags</span></span>           | <span data-ttu-id="1e882-292">0x00000012</span><span class="sxs-lookup"><span data-stu-id="1e882-292">0x00000012</span></span>                                       |
| <span data-ttu-id="1e882-293">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1e882-293">Classes used in</span></span>        | [<span data-ttu-id="1e882-294">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="1e882-294">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





