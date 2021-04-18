---
title: Atributo System-deve-conter
description: A lista de atributos obrigatórios para uma classe. Esses atributos devem ser especificados quando uma instância da classe é criada. A lista de atributos só pode ser modificada pelo sistema.
ms.assetid: 5131bd16-1a8d-4d4a-98e4-6140438c6517
ms.tgt_platform: multiple
keywords:
- Sistema-deve conter o atributo AD Schema
- Esquema de AD do atributo systemMustContain
topic_type:
- apiref
api_name:
- System-Must-Contain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f8d36419ca7e6cd24422645579fb7f9ecc69457
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104500028"
---
# <a name="system-must-contain-attribute"></a><span data-ttu-id="6161a-107">Atributo System-deve-conter</span><span class="sxs-lookup"><span data-stu-id="6161a-107">System-Must-Contain attribute</span></span>

<span data-ttu-id="6161a-108">A lista de atributos obrigatórios para uma classe.</span><span class="sxs-lookup"><span data-stu-id="6161a-108">The list of mandatory attributes for a class.</span></span> <span data-ttu-id="6161a-109">Esses atributos devem ser especificados quando uma instância da classe é criada.</span><span class="sxs-lookup"><span data-stu-id="6161a-109">These attributes must be specified when an instance of the class is created.</span></span> <span data-ttu-id="6161a-110">A lista de atributos só pode ser modificada pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="6161a-110">The list of attributes can only be modified by the system.</span></span>



| <span data-ttu-id="6161a-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="6161a-111">Entry</span></span> | <span data-ttu-id="6161a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="6161a-112">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="6161a-113">CN</span><span class="sxs-lookup"><span data-stu-id="6161a-113">CN</span></span>                | <span data-ttu-id="6161a-114">Sistema-deve conter</span><span class="sxs-lookup"><span data-stu-id="6161a-114">System-Must-Contain</span></span>                                                           |
| <span data-ttu-id="6161a-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6161a-115">Ldap-Display-Name</span></span> | <span data-ttu-id="6161a-116">systemMustContain</span><span class="sxs-lookup"><span data-stu-id="6161a-116">systemMustContain</span></span>                                                             |
| <span data-ttu-id="6161a-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="6161a-117">Size</span></span>              | \-                                                                            |
| <span data-ttu-id="6161a-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="6161a-118">Update Privilege</span></span>  | <span data-ttu-id="6161a-119">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="6161a-119">Schema administrator</span></span>                                                          |
| <span data-ttu-id="6161a-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="6161a-120">Update Frequency</span></span>  | <span data-ttu-id="6161a-121">Quando a classe é criada ou um novo atributo obrigatório é adicionado à classe.</span><span class="sxs-lookup"><span data-stu-id="6161a-121">When the class is created or a new mandatory attribute is added to the class.</span></span> |
| <span data-ttu-id="6161a-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6161a-122">Attribute-Id</span></span>      | <span data-ttu-id="6161a-123">1.2.840.113556.1.4.197</span><span class="sxs-lookup"><span data-stu-id="6161a-123">1.2.840.113556.1.4.197</span></span>                                                        |
| <span data-ttu-id="6161a-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6161a-124">System-Id-Guid</span></span>    | <span data-ttu-id="6161a-125">bf967a45-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6161a-125">bf967a45-0de6-11d0-a285-00aa003049e2</span></span>                                          |
| <span data-ttu-id="6161a-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="6161a-126">Syntax</span></span>            | [<span data-ttu-id="6161a-127">**Cadeia de caracteres (identificador de objeto)**</span><span class="sxs-lookup"><span data-stu-id="6161a-127">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)               |



## <a name="implementations"></a><span data-ttu-id="6161a-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="6161a-128">Implementations</span></span>

-   [<span data-ttu-id="6161a-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6161a-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6161a-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6161a-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6161a-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6161a-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6161a-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6161a-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6161a-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6161a-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6161a-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6161a-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6161a-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6161a-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6161a-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6161a-136">Windows 2000 Server</span></span>



| <span data-ttu-id="6161a-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="6161a-137">Entry</span></span> | <span data-ttu-id="6161a-138">Valor</span><span class="sxs-lookup"><span data-stu-id="6161a-138">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6161a-139">ID do link</span><span class="sxs-lookup"><span data-stu-id="6161a-139">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6161a-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6161a-140">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6161a-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="6161a-141">System-Only</span></span>            | <span data-ttu-id="6161a-142">True</span><span class="sxs-lookup"><span data-stu-id="6161a-142">True</span></span>                                             |
| <span data-ttu-id="6161a-143">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6161a-143">Is-Single-Valued</span></span>       | <span data-ttu-id="6161a-144">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-144">False</span></span>                                            |
| <span data-ttu-id="6161a-145">É indexado</span><span class="sxs-lookup"><span data-stu-id="6161a-145">Is Indexed</span></span>             | <span data-ttu-id="6161a-146">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-146">False</span></span>                                            |
| <span data-ttu-id="6161a-147">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6161a-147">In Global Catalog</span></span>      | <span data-ttu-id="6161a-148">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-148">False</span></span>                                            |
| <span data-ttu-id="6161a-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6161a-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="6161a-150">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6161a-150">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6161a-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6161a-151">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6161a-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6161a-152">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6161a-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6161a-153">Search-Flags</span></span>           | <span data-ttu-id="6161a-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6161a-154">0x00000000</span></span>                                       |
| <span data-ttu-id="6161a-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6161a-155">System-Flags</span></span>           | <span data-ttu-id="6161a-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6161a-156">0x00000010</span></span>                                       |
| <span data-ttu-id="6161a-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6161a-157">Classes used in</span></span>        | [<span data-ttu-id="6161a-158">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="6161a-158">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6161a-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6161a-159">Windows Server 2003</span></span>



| <span data-ttu-id="6161a-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="6161a-160">Entry</span></span> | <span data-ttu-id="6161a-161">Valor</span><span class="sxs-lookup"><span data-stu-id="6161a-161">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6161a-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="6161a-162">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6161a-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6161a-163">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6161a-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="6161a-164">System-Only</span></span>            | <span data-ttu-id="6161a-165">True</span><span class="sxs-lookup"><span data-stu-id="6161a-165">True</span></span>                                             |
| <span data-ttu-id="6161a-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6161a-166">Is-Single-Valued</span></span>       | <span data-ttu-id="6161a-167">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-167">False</span></span>                                            |
| <span data-ttu-id="6161a-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="6161a-168">Is Indexed</span></span>             | <span data-ttu-id="6161a-169">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-169">False</span></span>                                            |
| <span data-ttu-id="6161a-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6161a-170">In Global Catalog</span></span>      | <span data-ttu-id="6161a-171">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-171">False</span></span>                                            |
| <span data-ttu-id="6161a-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6161a-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="6161a-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6161a-173">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6161a-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6161a-174">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6161a-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6161a-175">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6161a-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6161a-176">Search-Flags</span></span>           | <span data-ttu-id="6161a-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6161a-177">0x00000000</span></span>                                       |
| <span data-ttu-id="6161a-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6161a-178">System-Flags</span></span>           | <span data-ttu-id="6161a-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6161a-179">0x00000010</span></span>                                       |
| <span data-ttu-id="6161a-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6161a-180">Classes used in</span></span>        | [<span data-ttu-id="6161a-181">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="6161a-181">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6161a-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="6161a-182">ADAM</span></span>



| <span data-ttu-id="6161a-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="6161a-183">Entry</span></span> | <span data-ttu-id="6161a-184">Valor</span><span class="sxs-lookup"><span data-stu-id="6161a-184">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6161a-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="6161a-185">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6161a-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6161a-186">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6161a-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="6161a-187">System-Only</span></span>            | <span data-ttu-id="6161a-188">True</span><span class="sxs-lookup"><span data-stu-id="6161a-188">True</span></span>                                             |
| <span data-ttu-id="6161a-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6161a-189">Is-Single-Valued</span></span>       | <span data-ttu-id="6161a-190">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-190">False</span></span>                                            |
| <span data-ttu-id="6161a-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="6161a-191">Is Indexed</span></span>             | <span data-ttu-id="6161a-192">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-192">False</span></span>                                            |
| <span data-ttu-id="6161a-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6161a-193">In Global Catalog</span></span>      | <span data-ttu-id="6161a-194">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-194">False</span></span>                                            |
| <span data-ttu-id="6161a-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6161a-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="6161a-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6161a-196">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6161a-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6161a-197">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6161a-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6161a-198">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6161a-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6161a-199">Search-Flags</span></span>           | <span data-ttu-id="6161a-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6161a-200">0x00000000</span></span>                                       |
| <span data-ttu-id="6161a-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6161a-201">System-Flags</span></span>           | <span data-ttu-id="6161a-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6161a-202">0x00000010</span></span>                                       |
| <span data-ttu-id="6161a-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6161a-203">Classes used in</span></span>        | [<span data-ttu-id="6161a-204">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="6161a-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6161a-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6161a-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6161a-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="6161a-206">Entry</span></span> | <span data-ttu-id="6161a-207">Valor</span><span class="sxs-lookup"><span data-stu-id="6161a-207">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6161a-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="6161a-208">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6161a-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6161a-209">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6161a-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="6161a-210">System-Only</span></span>            | <span data-ttu-id="6161a-211">True</span><span class="sxs-lookup"><span data-stu-id="6161a-211">True</span></span>                                             |
| <span data-ttu-id="6161a-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6161a-212">Is-Single-Valued</span></span>       | <span data-ttu-id="6161a-213">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-213">False</span></span>                                            |
| <span data-ttu-id="6161a-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="6161a-214">Is Indexed</span></span>             | <span data-ttu-id="6161a-215">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-215">False</span></span>                                            |
| <span data-ttu-id="6161a-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6161a-216">In Global Catalog</span></span>      | <span data-ttu-id="6161a-217">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-217">False</span></span>                                            |
| <span data-ttu-id="6161a-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6161a-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="6161a-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6161a-219">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6161a-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6161a-220">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6161a-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6161a-221">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6161a-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6161a-222">Search-Flags</span></span>           | <span data-ttu-id="6161a-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6161a-223">0x00000000</span></span>                                       |
| <span data-ttu-id="6161a-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6161a-224">System-Flags</span></span>           | <span data-ttu-id="6161a-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6161a-225">0x00000010</span></span>                                       |
| <span data-ttu-id="6161a-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6161a-226">Classes used in</span></span>        | [<span data-ttu-id="6161a-227">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="6161a-227">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6161a-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6161a-228">Windows Server 2008</span></span>



| <span data-ttu-id="6161a-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="6161a-229">Entry</span></span> | <span data-ttu-id="6161a-230">Valor</span><span class="sxs-lookup"><span data-stu-id="6161a-230">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6161a-231">ID do link</span><span class="sxs-lookup"><span data-stu-id="6161a-231">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6161a-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6161a-232">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6161a-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="6161a-233">System-Only</span></span>            | <span data-ttu-id="6161a-234">True</span><span class="sxs-lookup"><span data-stu-id="6161a-234">True</span></span>                                             |
| <span data-ttu-id="6161a-235">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6161a-235">Is-Single-Valued</span></span>       | <span data-ttu-id="6161a-236">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-236">False</span></span>                                            |
| <span data-ttu-id="6161a-237">É indexado</span><span class="sxs-lookup"><span data-stu-id="6161a-237">Is Indexed</span></span>             | <span data-ttu-id="6161a-238">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-238">False</span></span>                                            |
| <span data-ttu-id="6161a-239">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6161a-239">In Global Catalog</span></span>      | <span data-ttu-id="6161a-240">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-240">False</span></span>                                            |
| <span data-ttu-id="6161a-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6161a-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="6161a-242">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6161a-242">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6161a-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6161a-243">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6161a-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6161a-244">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6161a-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6161a-245">Search-Flags</span></span>           | <span data-ttu-id="6161a-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6161a-246">0x00000000</span></span>                                       |
| <span data-ttu-id="6161a-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6161a-247">System-Flags</span></span>           | <span data-ttu-id="6161a-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6161a-248">0x00000010</span></span>                                       |
| <span data-ttu-id="6161a-249">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6161a-249">Classes used in</span></span>        | [<span data-ttu-id="6161a-250">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="6161a-250">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6161a-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6161a-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6161a-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="6161a-252">Entry</span></span> | <span data-ttu-id="6161a-253">Valor</span><span class="sxs-lookup"><span data-stu-id="6161a-253">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6161a-254">ID do link</span><span class="sxs-lookup"><span data-stu-id="6161a-254">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6161a-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6161a-255">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6161a-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="6161a-256">System-Only</span></span>            | <span data-ttu-id="6161a-257">True</span><span class="sxs-lookup"><span data-stu-id="6161a-257">True</span></span>                                             |
| <span data-ttu-id="6161a-258">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6161a-258">Is-Single-Valued</span></span>       | <span data-ttu-id="6161a-259">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-259">False</span></span>                                            |
| <span data-ttu-id="6161a-260">É indexado</span><span class="sxs-lookup"><span data-stu-id="6161a-260">Is Indexed</span></span>             | <span data-ttu-id="6161a-261">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-261">False</span></span>                                            |
| <span data-ttu-id="6161a-262">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6161a-262">In Global Catalog</span></span>      | <span data-ttu-id="6161a-263">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-263">False</span></span>                                            |
| <span data-ttu-id="6161a-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6161a-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="6161a-265">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6161a-265">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6161a-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6161a-266">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6161a-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6161a-267">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6161a-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6161a-268">Search-Flags</span></span>           | <span data-ttu-id="6161a-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6161a-269">0x00000000</span></span>                                       |
| <span data-ttu-id="6161a-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6161a-270">System-Flags</span></span>           | <span data-ttu-id="6161a-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6161a-271">0x00000010</span></span>                                       |
| <span data-ttu-id="6161a-272">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6161a-272">Classes used in</span></span>        | [<span data-ttu-id="6161a-273">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="6161a-273">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6161a-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6161a-274">Windows Server 2012</span></span>



| <span data-ttu-id="6161a-275">Entrada</span><span class="sxs-lookup"><span data-stu-id="6161a-275">Entry</span></span> | <span data-ttu-id="6161a-276">Valor</span><span class="sxs-lookup"><span data-stu-id="6161a-276">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6161a-277">ID do link</span><span class="sxs-lookup"><span data-stu-id="6161a-277">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6161a-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6161a-278">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6161a-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="6161a-279">System-Only</span></span>            | <span data-ttu-id="6161a-280">True</span><span class="sxs-lookup"><span data-stu-id="6161a-280">True</span></span>                                             |
| <span data-ttu-id="6161a-281">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6161a-281">Is-Single-Valued</span></span>       | <span data-ttu-id="6161a-282">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-282">False</span></span>                                            |
| <span data-ttu-id="6161a-283">É indexado</span><span class="sxs-lookup"><span data-stu-id="6161a-283">Is Indexed</span></span>             | <span data-ttu-id="6161a-284">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-284">False</span></span>                                            |
| <span data-ttu-id="6161a-285">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6161a-285">In Global Catalog</span></span>      | <span data-ttu-id="6161a-286">Falso</span><span class="sxs-lookup"><span data-stu-id="6161a-286">False</span></span>                                            |
| <span data-ttu-id="6161a-287">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6161a-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="6161a-288">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6161a-288">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6161a-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6161a-289">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6161a-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6161a-290">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6161a-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6161a-291">Search-Flags</span></span>           | <span data-ttu-id="6161a-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6161a-292">0x00000000</span></span>                                       |
| <span data-ttu-id="6161a-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6161a-293">System-Flags</span></span>           | <span data-ttu-id="6161a-294">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6161a-294">0x00000010</span></span>                                       |
| <span data-ttu-id="6161a-295">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6161a-295">Classes used in</span></span>        | [<span data-ttu-id="6161a-296">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="6161a-296">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





