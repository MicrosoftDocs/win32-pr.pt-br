---
title: Atributo System-Mai-contain
description: A lista de atributos opcionais para uma classe. A lista de atributos só pode ser modificada pelo sistema.
ms.assetid: b2fbeb64-d147-4c1a-a609-4f16327609ce
ms.tgt_platform: multiple
keywords:
- System-maio-conter o atributo AD Schema
- Esquema de AD do atributo systemMayContain
topic_type:
- apiref
api_name:
- System-May-Contain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03730e9904cbaa6ee5954662556fba261c51cd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086830"
---
# <a name="system-may-contain-attribute"></a><span data-ttu-id="51760-106">Atributo System-Mai-contain</span><span class="sxs-lookup"><span data-stu-id="51760-106">System-May-Contain attribute</span></span>

<span data-ttu-id="51760-107">A lista de atributos opcionais para uma classe.</span><span class="sxs-lookup"><span data-stu-id="51760-107">The list of optional attributes for a class.</span></span> <span data-ttu-id="51760-108">A lista de atributos só pode ser modificada pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="51760-108">The list of attributes can only be modified by the system.</span></span>



| <span data-ttu-id="51760-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="51760-109">Entry</span></span> | <span data-ttu-id="51760-110">Valor</span><span class="sxs-lookup"><span data-stu-id="51760-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="51760-111">CN</span><span class="sxs-lookup"><span data-stu-id="51760-111">CN</span></span>                | <span data-ttu-id="51760-112">Sistema-pode-conter</span><span class="sxs-lookup"><span data-stu-id="51760-112">System-May-Contain</span></span>                                                           |
| <span data-ttu-id="51760-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="51760-113">Ldap-Display-Name</span></span> | <span data-ttu-id="51760-114">systemMayContain</span><span class="sxs-lookup"><span data-stu-id="51760-114">systemMayContain</span></span>                                                             |
| <span data-ttu-id="51760-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="51760-115">Size</span></span>              | \-                                                                           |
| <span data-ttu-id="51760-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="51760-116">Update Privilege</span></span>  | <span data-ttu-id="51760-117">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="51760-117">Schema administrator</span></span>                                                         |
| <span data-ttu-id="51760-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="51760-118">Update Frequency</span></span>  | <span data-ttu-id="51760-119">Quando a classe é criada ou um novo atributo opcional é adicionado à classe.</span><span class="sxs-lookup"><span data-stu-id="51760-119">When the class is created or a new optional attribute is added to the class.</span></span> |
| <span data-ttu-id="51760-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="51760-120">Attribute-Id</span></span>      | <span data-ttu-id="51760-121">1.2.840.113556.1.4.196</span><span class="sxs-lookup"><span data-stu-id="51760-121">1.2.840.113556.1.4.196</span></span>                                                       |
| <span data-ttu-id="51760-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="51760-122">System-Id-Guid</span></span>    | <span data-ttu-id="51760-123">bf967a44-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="51760-123">bf967a44-0de6-11d0-a285-00aa003049e2</span></span>                                         |
| <span data-ttu-id="51760-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="51760-124">Syntax</span></span>            | [<span data-ttu-id="51760-125">**Cadeia de caracteres (identificador de objeto)**</span><span class="sxs-lookup"><span data-stu-id="51760-125">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)              |



## <a name="implementations"></a><span data-ttu-id="51760-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="51760-126">Implementations</span></span>

-   [<span data-ttu-id="51760-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="51760-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="51760-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="51760-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="51760-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="51760-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="51760-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="51760-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="51760-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="51760-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="51760-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="51760-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="51760-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="51760-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="51760-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="51760-134">Windows 2000 Server</span></span>



| <span data-ttu-id="51760-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="51760-135">Entry</span></span> | <span data-ttu-id="51760-136">Valor</span><span class="sxs-lookup"><span data-stu-id="51760-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="51760-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="51760-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="51760-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51760-138">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="51760-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="51760-139">System-Only</span></span>            | <span data-ttu-id="51760-140">True</span><span class="sxs-lookup"><span data-stu-id="51760-140">True</span></span>                                             |
| <span data-ttu-id="51760-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="51760-141">Is-Single-Valued</span></span>       | <span data-ttu-id="51760-142">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-142">False</span></span>                                            |
| <span data-ttu-id="51760-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="51760-143">Is Indexed</span></span>             | <span data-ttu-id="51760-144">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-144">False</span></span>                                            |
| <span data-ttu-id="51760-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="51760-145">In Global Catalog</span></span>      | <span data-ttu-id="51760-146">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-146">False</span></span>                                            |
| <span data-ttu-id="51760-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="51760-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="51760-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="51760-148">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="51760-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51760-149">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="51760-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51760-150">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="51760-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51760-151">Search-Flags</span></span>           | <span data-ttu-id="51760-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51760-152">0x00000000</span></span>                                       |
| <span data-ttu-id="51760-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51760-153">System-Flags</span></span>           | <span data-ttu-id="51760-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51760-154">0x00000010</span></span>                                       |
| <span data-ttu-id="51760-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="51760-155">Classes used in</span></span>        | [<span data-ttu-id="51760-156">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="51760-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="51760-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="51760-157">Windows Server 2003</span></span>



| <span data-ttu-id="51760-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="51760-158">Entry</span></span> | <span data-ttu-id="51760-159">Valor</span><span class="sxs-lookup"><span data-stu-id="51760-159">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="51760-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="51760-160">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="51760-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51760-161">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="51760-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="51760-162">System-Only</span></span>            | <span data-ttu-id="51760-163">True</span><span class="sxs-lookup"><span data-stu-id="51760-163">True</span></span>                                             |
| <span data-ttu-id="51760-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="51760-164">Is-Single-Valued</span></span>       | <span data-ttu-id="51760-165">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-165">False</span></span>                                            |
| <span data-ttu-id="51760-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="51760-166">Is Indexed</span></span>             | <span data-ttu-id="51760-167">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-167">False</span></span>                                            |
| <span data-ttu-id="51760-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="51760-168">In Global Catalog</span></span>      | <span data-ttu-id="51760-169">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-169">False</span></span>                                            |
| <span data-ttu-id="51760-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="51760-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="51760-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="51760-171">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="51760-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51760-172">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="51760-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51760-173">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="51760-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51760-174">Search-Flags</span></span>           | <span data-ttu-id="51760-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51760-175">0x00000000</span></span>                                       |
| <span data-ttu-id="51760-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51760-176">System-Flags</span></span>           | <span data-ttu-id="51760-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51760-177">0x00000010</span></span>                                       |
| <span data-ttu-id="51760-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="51760-178">Classes used in</span></span>        | [<span data-ttu-id="51760-179">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="51760-179">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="51760-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="51760-180">ADAM</span></span>



| <span data-ttu-id="51760-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="51760-181">Entry</span></span> | <span data-ttu-id="51760-182">Valor</span><span class="sxs-lookup"><span data-stu-id="51760-182">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="51760-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="51760-183">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="51760-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51760-184">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="51760-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="51760-185">System-Only</span></span>            | <span data-ttu-id="51760-186">True</span><span class="sxs-lookup"><span data-stu-id="51760-186">True</span></span>                                             |
| <span data-ttu-id="51760-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="51760-187">Is-Single-Valued</span></span>       | <span data-ttu-id="51760-188">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-188">False</span></span>                                            |
| <span data-ttu-id="51760-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="51760-189">Is Indexed</span></span>             | <span data-ttu-id="51760-190">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-190">False</span></span>                                            |
| <span data-ttu-id="51760-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="51760-191">In Global Catalog</span></span>      | <span data-ttu-id="51760-192">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-192">False</span></span>                                            |
| <span data-ttu-id="51760-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="51760-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="51760-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="51760-194">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="51760-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51760-195">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="51760-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51760-196">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="51760-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51760-197">Search-Flags</span></span>           | <span data-ttu-id="51760-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51760-198">0x00000000</span></span>                                       |
| <span data-ttu-id="51760-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51760-199">System-Flags</span></span>           | <span data-ttu-id="51760-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51760-200">0x00000010</span></span>                                       |
| <span data-ttu-id="51760-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="51760-201">Classes used in</span></span>        | [<span data-ttu-id="51760-202">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="51760-202">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="51760-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="51760-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="51760-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="51760-204">Entry</span></span> | <span data-ttu-id="51760-205">Valor</span><span class="sxs-lookup"><span data-stu-id="51760-205">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="51760-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="51760-206">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="51760-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51760-207">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="51760-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="51760-208">System-Only</span></span>            | <span data-ttu-id="51760-209">True</span><span class="sxs-lookup"><span data-stu-id="51760-209">True</span></span>                                             |
| <span data-ttu-id="51760-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="51760-210">Is-Single-Valued</span></span>       | <span data-ttu-id="51760-211">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-211">False</span></span>                                            |
| <span data-ttu-id="51760-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="51760-212">Is Indexed</span></span>             | <span data-ttu-id="51760-213">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-213">False</span></span>                                            |
| <span data-ttu-id="51760-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="51760-214">In Global Catalog</span></span>      | <span data-ttu-id="51760-215">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-215">False</span></span>                                            |
| <span data-ttu-id="51760-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="51760-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="51760-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="51760-217">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="51760-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51760-218">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="51760-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51760-219">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="51760-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51760-220">Search-Flags</span></span>           | <span data-ttu-id="51760-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51760-221">0x00000000</span></span>                                       |
| <span data-ttu-id="51760-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51760-222">System-Flags</span></span>           | <span data-ttu-id="51760-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51760-223">0x00000010</span></span>                                       |
| <span data-ttu-id="51760-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="51760-224">Classes used in</span></span>        | [<span data-ttu-id="51760-225">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="51760-225">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="51760-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51760-226">Windows Server 2008</span></span>



| <span data-ttu-id="51760-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="51760-227">Entry</span></span> | <span data-ttu-id="51760-228">Valor</span><span class="sxs-lookup"><span data-stu-id="51760-228">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="51760-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="51760-229">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="51760-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51760-230">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="51760-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="51760-231">System-Only</span></span>            | <span data-ttu-id="51760-232">True</span><span class="sxs-lookup"><span data-stu-id="51760-232">True</span></span>                                             |
| <span data-ttu-id="51760-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="51760-233">Is-Single-Valued</span></span>       | <span data-ttu-id="51760-234">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-234">False</span></span>                                            |
| <span data-ttu-id="51760-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="51760-235">Is Indexed</span></span>             | <span data-ttu-id="51760-236">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-236">False</span></span>                                            |
| <span data-ttu-id="51760-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="51760-237">In Global Catalog</span></span>      | <span data-ttu-id="51760-238">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-238">False</span></span>                                            |
| <span data-ttu-id="51760-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="51760-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="51760-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="51760-240">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="51760-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51760-241">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="51760-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51760-242">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="51760-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51760-243">Search-Flags</span></span>           | <span data-ttu-id="51760-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51760-244">0x00000000</span></span>                                       |
| <span data-ttu-id="51760-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51760-245">System-Flags</span></span>           | <span data-ttu-id="51760-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51760-246">0x00000010</span></span>                                       |
| <span data-ttu-id="51760-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="51760-247">Classes used in</span></span>        | [<span data-ttu-id="51760-248">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="51760-248">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="51760-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="51760-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="51760-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="51760-250">Entry</span></span> | <span data-ttu-id="51760-251">Valor</span><span class="sxs-lookup"><span data-stu-id="51760-251">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="51760-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="51760-252">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="51760-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51760-253">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="51760-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="51760-254">System-Only</span></span>            | <span data-ttu-id="51760-255">True</span><span class="sxs-lookup"><span data-stu-id="51760-255">True</span></span>                                             |
| <span data-ttu-id="51760-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="51760-256">Is-Single-Valued</span></span>       | <span data-ttu-id="51760-257">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-257">False</span></span>                                            |
| <span data-ttu-id="51760-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="51760-258">Is Indexed</span></span>             | <span data-ttu-id="51760-259">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-259">False</span></span>                                            |
| <span data-ttu-id="51760-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="51760-260">In Global Catalog</span></span>      | <span data-ttu-id="51760-261">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-261">False</span></span>                                            |
| <span data-ttu-id="51760-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="51760-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="51760-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="51760-263">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="51760-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51760-264">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="51760-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51760-265">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="51760-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51760-266">Search-Flags</span></span>           | <span data-ttu-id="51760-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51760-267">0x00000000</span></span>                                       |
| <span data-ttu-id="51760-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51760-268">System-Flags</span></span>           | <span data-ttu-id="51760-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51760-269">0x00000010</span></span>                                       |
| <span data-ttu-id="51760-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="51760-270">Classes used in</span></span>        | [<span data-ttu-id="51760-271">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="51760-271">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="51760-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="51760-272">Windows Server 2012</span></span>



| <span data-ttu-id="51760-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="51760-273">Entry</span></span> | <span data-ttu-id="51760-274">Valor</span><span class="sxs-lookup"><span data-stu-id="51760-274">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="51760-275">ID do link</span><span class="sxs-lookup"><span data-stu-id="51760-275">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="51760-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51760-276">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="51760-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="51760-277">System-Only</span></span>            | <span data-ttu-id="51760-278">True</span><span class="sxs-lookup"><span data-stu-id="51760-278">True</span></span>                                             |
| <span data-ttu-id="51760-279">É de valor único</span><span class="sxs-lookup"><span data-stu-id="51760-279">Is-Single-Valued</span></span>       | <span data-ttu-id="51760-280">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-280">False</span></span>                                            |
| <span data-ttu-id="51760-281">É indexado</span><span class="sxs-lookup"><span data-stu-id="51760-281">Is Indexed</span></span>             | <span data-ttu-id="51760-282">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-282">False</span></span>                                            |
| <span data-ttu-id="51760-283">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="51760-283">In Global Catalog</span></span>      | <span data-ttu-id="51760-284">Falso</span><span class="sxs-lookup"><span data-stu-id="51760-284">False</span></span>                                            |
| <span data-ttu-id="51760-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="51760-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="51760-286">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="51760-286">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="51760-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51760-287">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="51760-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51760-288">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="51760-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51760-289">Search-Flags</span></span>           | <span data-ttu-id="51760-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51760-290">0x00000000</span></span>                                       |
| <span data-ttu-id="51760-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51760-291">System-Flags</span></span>           | <span data-ttu-id="51760-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51760-292">0x00000010</span></span>                                       |
| <span data-ttu-id="51760-293">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="51760-293">Classes used in</span></span>        | [<span data-ttu-id="51760-294">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="51760-294">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





