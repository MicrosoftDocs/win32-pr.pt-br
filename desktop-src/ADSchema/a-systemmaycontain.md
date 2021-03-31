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
# <a name="system-may-contain-attribute"></a><span data-ttu-id="afdd3-106">Atributo System-Mai-contain</span><span class="sxs-lookup"><span data-stu-id="afdd3-106">System-May-Contain attribute</span></span>

<span data-ttu-id="afdd3-107">A lista de atributos opcionais para uma classe.</span><span class="sxs-lookup"><span data-stu-id="afdd3-107">The list of optional attributes for a class.</span></span> <span data-ttu-id="afdd3-108">A lista de atributos só pode ser modificada pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="afdd3-108">The list of attributes can only be modified by the system.</span></span>



| <span data-ttu-id="afdd3-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="afdd3-109">Entry</span></span> | <span data-ttu-id="afdd3-110">Valor</span><span class="sxs-lookup"><span data-stu-id="afdd3-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="afdd3-111">CN</span><span class="sxs-lookup"><span data-stu-id="afdd3-111">CN</span></span>                | <span data-ttu-id="afdd3-112">Sistema-pode-conter</span><span class="sxs-lookup"><span data-stu-id="afdd3-112">System-May-Contain</span></span>                                                           |
| <span data-ttu-id="afdd3-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="afdd3-113">Ldap-Display-Name</span></span> | <span data-ttu-id="afdd3-114">systemMayContain</span><span class="sxs-lookup"><span data-stu-id="afdd3-114">systemMayContain</span></span>                                                             |
| <span data-ttu-id="afdd3-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="afdd3-115">Size</span></span>              | \-                                                                           |
| <span data-ttu-id="afdd3-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="afdd3-116">Update Privilege</span></span>  | <span data-ttu-id="afdd3-117">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="afdd3-117">Schema administrator</span></span>                                                         |
| <span data-ttu-id="afdd3-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="afdd3-118">Update Frequency</span></span>  | <span data-ttu-id="afdd3-119">Quando a classe é criada ou um novo atributo opcional é adicionado à classe.</span><span class="sxs-lookup"><span data-stu-id="afdd3-119">When the class is created or a new optional attribute is added to the class.</span></span> |
| <span data-ttu-id="afdd3-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="afdd3-120">Attribute-Id</span></span>      | <span data-ttu-id="afdd3-121">1.2.840.113556.1.4.196</span><span class="sxs-lookup"><span data-stu-id="afdd3-121">1.2.840.113556.1.4.196</span></span>                                                       |
| <span data-ttu-id="afdd3-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="afdd3-122">System-Id-Guid</span></span>    | <span data-ttu-id="afdd3-123">bf967a44-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="afdd3-123">bf967a44-0de6-11d0-a285-00aa003049e2</span></span>                                         |
| <span data-ttu-id="afdd3-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="afdd3-124">Syntax</span></span>            | [<span data-ttu-id="afdd3-125">**Cadeia de caracteres (identificador de objeto)**</span><span class="sxs-lookup"><span data-stu-id="afdd3-125">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)              |



## <a name="implementations"></a><span data-ttu-id="afdd3-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="afdd3-126">Implementations</span></span>

-   [<span data-ttu-id="afdd3-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="afdd3-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="afdd3-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="afdd3-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="afdd3-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="afdd3-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="afdd3-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="afdd3-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="afdd3-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="afdd3-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="afdd3-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="afdd3-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="afdd3-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="afdd3-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="afdd3-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="afdd3-134">Windows 2000 Server</span></span>



| <span data-ttu-id="afdd3-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="afdd3-135">Entry</span></span> | <span data-ttu-id="afdd3-136">Valor</span><span class="sxs-lookup"><span data-stu-id="afdd3-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="afdd3-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="afdd3-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="afdd3-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afdd3-138">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="afdd3-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="afdd3-139">System-Only</span></span>            | <span data-ttu-id="afdd3-140">True</span><span class="sxs-lookup"><span data-stu-id="afdd3-140">True</span></span>                                             |
| <span data-ttu-id="afdd3-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="afdd3-141">Is-Single-Valued</span></span>       | <span data-ttu-id="afdd3-142">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-142">False</span></span>                                            |
| <span data-ttu-id="afdd3-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="afdd3-143">Is Indexed</span></span>             | <span data-ttu-id="afdd3-144">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-144">False</span></span>                                            |
| <span data-ttu-id="afdd3-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="afdd3-145">In Global Catalog</span></span>      | <span data-ttu-id="afdd3-146">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-146">False</span></span>                                            |
| <span data-ttu-id="afdd3-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="afdd3-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="afdd3-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="afdd3-148">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="afdd3-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afdd3-149">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="afdd3-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afdd3-150">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="afdd3-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afdd3-151">Search-Flags</span></span>           | <span data-ttu-id="afdd3-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afdd3-152">0x00000000</span></span>                                       |
| <span data-ttu-id="afdd3-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afdd3-153">System-Flags</span></span>           | <span data-ttu-id="afdd3-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afdd3-154">0x00000010</span></span>                                       |
| <span data-ttu-id="afdd3-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="afdd3-155">Classes used in</span></span>        | [<span data-ttu-id="afdd3-156">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="afdd3-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="afdd3-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="afdd3-157">Windows Server 2003</span></span>



| <span data-ttu-id="afdd3-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="afdd3-158">Entry</span></span> | <span data-ttu-id="afdd3-159">Valor</span><span class="sxs-lookup"><span data-stu-id="afdd3-159">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="afdd3-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="afdd3-160">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="afdd3-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afdd3-161">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="afdd3-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="afdd3-162">System-Only</span></span>            | <span data-ttu-id="afdd3-163">True</span><span class="sxs-lookup"><span data-stu-id="afdd3-163">True</span></span>                                             |
| <span data-ttu-id="afdd3-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="afdd3-164">Is-Single-Valued</span></span>       | <span data-ttu-id="afdd3-165">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-165">False</span></span>                                            |
| <span data-ttu-id="afdd3-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="afdd3-166">Is Indexed</span></span>             | <span data-ttu-id="afdd3-167">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-167">False</span></span>                                            |
| <span data-ttu-id="afdd3-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="afdd3-168">In Global Catalog</span></span>      | <span data-ttu-id="afdd3-169">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-169">False</span></span>                                            |
| <span data-ttu-id="afdd3-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="afdd3-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="afdd3-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="afdd3-171">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="afdd3-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afdd3-172">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="afdd3-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afdd3-173">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="afdd3-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afdd3-174">Search-Flags</span></span>           | <span data-ttu-id="afdd3-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afdd3-175">0x00000000</span></span>                                       |
| <span data-ttu-id="afdd3-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afdd3-176">System-Flags</span></span>           | <span data-ttu-id="afdd3-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afdd3-177">0x00000010</span></span>                                       |
| <span data-ttu-id="afdd3-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="afdd3-178">Classes used in</span></span>        | [<span data-ttu-id="afdd3-179">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="afdd3-179">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="afdd3-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="afdd3-180">ADAM</span></span>



| <span data-ttu-id="afdd3-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="afdd3-181">Entry</span></span> | <span data-ttu-id="afdd3-182">Valor</span><span class="sxs-lookup"><span data-stu-id="afdd3-182">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="afdd3-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="afdd3-183">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="afdd3-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afdd3-184">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="afdd3-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="afdd3-185">System-Only</span></span>            | <span data-ttu-id="afdd3-186">True</span><span class="sxs-lookup"><span data-stu-id="afdd3-186">True</span></span>                                             |
| <span data-ttu-id="afdd3-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="afdd3-187">Is-Single-Valued</span></span>       | <span data-ttu-id="afdd3-188">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-188">False</span></span>                                            |
| <span data-ttu-id="afdd3-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="afdd3-189">Is Indexed</span></span>             | <span data-ttu-id="afdd3-190">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-190">False</span></span>                                            |
| <span data-ttu-id="afdd3-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="afdd3-191">In Global Catalog</span></span>      | <span data-ttu-id="afdd3-192">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-192">False</span></span>                                            |
| <span data-ttu-id="afdd3-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="afdd3-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="afdd3-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="afdd3-194">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="afdd3-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afdd3-195">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="afdd3-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afdd3-196">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="afdd3-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afdd3-197">Search-Flags</span></span>           | <span data-ttu-id="afdd3-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afdd3-198">0x00000000</span></span>                                       |
| <span data-ttu-id="afdd3-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afdd3-199">System-Flags</span></span>           | <span data-ttu-id="afdd3-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afdd3-200">0x00000010</span></span>                                       |
| <span data-ttu-id="afdd3-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="afdd3-201">Classes used in</span></span>        | [<span data-ttu-id="afdd3-202">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="afdd3-202">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="afdd3-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="afdd3-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="afdd3-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="afdd3-204">Entry</span></span> | <span data-ttu-id="afdd3-205">Valor</span><span class="sxs-lookup"><span data-stu-id="afdd3-205">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="afdd3-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="afdd3-206">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="afdd3-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afdd3-207">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="afdd3-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="afdd3-208">System-Only</span></span>            | <span data-ttu-id="afdd3-209">True</span><span class="sxs-lookup"><span data-stu-id="afdd3-209">True</span></span>                                             |
| <span data-ttu-id="afdd3-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="afdd3-210">Is-Single-Valued</span></span>       | <span data-ttu-id="afdd3-211">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-211">False</span></span>                                            |
| <span data-ttu-id="afdd3-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="afdd3-212">Is Indexed</span></span>             | <span data-ttu-id="afdd3-213">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-213">False</span></span>                                            |
| <span data-ttu-id="afdd3-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="afdd3-214">In Global Catalog</span></span>      | <span data-ttu-id="afdd3-215">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-215">False</span></span>                                            |
| <span data-ttu-id="afdd3-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="afdd3-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="afdd3-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="afdd3-217">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="afdd3-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afdd3-218">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="afdd3-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afdd3-219">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="afdd3-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afdd3-220">Search-Flags</span></span>           | <span data-ttu-id="afdd3-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afdd3-221">0x00000000</span></span>                                       |
| <span data-ttu-id="afdd3-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afdd3-222">System-Flags</span></span>           | <span data-ttu-id="afdd3-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afdd3-223">0x00000010</span></span>                                       |
| <span data-ttu-id="afdd3-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="afdd3-224">Classes used in</span></span>        | [<span data-ttu-id="afdd3-225">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="afdd3-225">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="afdd3-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afdd3-226">Windows Server 2008</span></span>



| <span data-ttu-id="afdd3-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="afdd3-227">Entry</span></span> | <span data-ttu-id="afdd3-228">Valor</span><span class="sxs-lookup"><span data-stu-id="afdd3-228">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="afdd3-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="afdd3-229">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="afdd3-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afdd3-230">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="afdd3-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="afdd3-231">System-Only</span></span>            | <span data-ttu-id="afdd3-232">True</span><span class="sxs-lookup"><span data-stu-id="afdd3-232">True</span></span>                                             |
| <span data-ttu-id="afdd3-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="afdd3-233">Is-Single-Valued</span></span>       | <span data-ttu-id="afdd3-234">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-234">False</span></span>                                            |
| <span data-ttu-id="afdd3-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="afdd3-235">Is Indexed</span></span>             | <span data-ttu-id="afdd3-236">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-236">False</span></span>                                            |
| <span data-ttu-id="afdd3-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="afdd3-237">In Global Catalog</span></span>      | <span data-ttu-id="afdd3-238">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-238">False</span></span>                                            |
| <span data-ttu-id="afdd3-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="afdd3-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="afdd3-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="afdd3-240">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="afdd3-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afdd3-241">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="afdd3-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afdd3-242">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="afdd3-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afdd3-243">Search-Flags</span></span>           | <span data-ttu-id="afdd3-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afdd3-244">0x00000000</span></span>                                       |
| <span data-ttu-id="afdd3-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afdd3-245">System-Flags</span></span>           | <span data-ttu-id="afdd3-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afdd3-246">0x00000010</span></span>                                       |
| <span data-ttu-id="afdd3-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="afdd3-247">Classes used in</span></span>        | [<span data-ttu-id="afdd3-248">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="afdd3-248">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="afdd3-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="afdd3-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="afdd3-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="afdd3-250">Entry</span></span> | <span data-ttu-id="afdd3-251">Valor</span><span class="sxs-lookup"><span data-stu-id="afdd3-251">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="afdd3-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="afdd3-252">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="afdd3-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afdd3-253">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="afdd3-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="afdd3-254">System-Only</span></span>            | <span data-ttu-id="afdd3-255">True</span><span class="sxs-lookup"><span data-stu-id="afdd3-255">True</span></span>                                             |
| <span data-ttu-id="afdd3-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="afdd3-256">Is-Single-Valued</span></span>       | <span data-ttu-id="afdd3-257">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-257">False</span></span>                                            |
| <span data-ttu-id="afdd3-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="afdd3-258">Is Indexed</span></span>             | <span data-ttu-id="afdd3-259">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-259">False</span></span>                                            |
| <span data-ttu-id="afdd3-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="afdd3-260">In Global Catalog</span></span>      | <span data-ttu-id="afdd3-261">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-261">False</span></span>                                            |
| <span data-ttu-id="afdd3-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="afdd3-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="afdd3-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="afdd3-263">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="afdd3-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afdd3-264">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="afdd3-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afdd3-265">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="afdd3-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afdd3-266">Search-Flags</span></span>           | <span data-ttu-id="afdd3-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afdd3-267">0x00000000</span></span>                                       |
| <span data-ttu-id="afdd3-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afdd3-268">System-Flags</span></span>           | <span data-ttu-id="afdd3-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afdd3-269">0x00000010</span></span>                                       |
| <span data-ttu-id="afdd3-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="afdd3-270">Classes used in</span></span>        | [<span data-ttu-id="afdd3-271">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="afdd3-271">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="afdd3-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="afdd3-272">Windows Server 2012</span></span>



| <span data-ttu-id="afdd3-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="afdd3-273">Entry</span></span> | <span data-ttu-id="afdd3-274">Valor</span><span class="sxs-lookup"><span data-stu-id="afdd3-274">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="afdd3-275">ID do link</span><span class="sxs-lookup"><span data-stu-id="afdd3-275">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="afdd3-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afdd3-276">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="afdd3-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="afdd3-277">System-Only</span></span>            | <span data-ttu-id="afdd3-278">True</span><span class="sxs-lookup"><span data-stu-id="afdd3-278">True</span></span>                                             |
| <span data-ttu-id="afdd3-279">É de valor único</span><span class="sxs-lookup"><span data-stu-id="afdd3-279">Is-Single-Valued</span></span>       | <span data-ttu-id="afdd3-280">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-280">False</span></span>                                            |
| <span data-ttu-id="afdd3-281">É indexado</span><span class="sxs-lookup"><span data-stu-id="afdd3-281">Is Indexed</span></span>             | <span data-ttu-id="afdd3-282">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-282">False</span></span>                                            |
| <span data-ttu-id="afdd3-283">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="afdd3-283">In Global Catalog</span></span>      | <span data-ttu-id="afdd3-284">Falso</span><span class="sxs-lookup"><span data-stu-id="afdd3-284">False</span></span>                                            |
| <span data-ttu-id="afdd3-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="afdd3-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="afdd3-286">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="afdd3-286">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="afdd3-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afdd3-287">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="afdd3-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afdd3-288">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="afdd3-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afdd3-289">Search-Flags</span></span>           | <span data-ttu-id="afdd3-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afdd3-290">0x00000000</span></span>                                       |
| <span data-ttu-id="afdd3-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afdd3-291">System-Flags</span></span>           | <span data-ttu-id="afdd3-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afdd3-292">0x00000010</span></span>                                       |
| <span data-ttu-id="afdd3-293">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="afdd3-293">Classes used in</span></span>        | [<span data-ttu-id="afdd3-294">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="afdd3-294">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





