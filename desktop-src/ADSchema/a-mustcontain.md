---
title: Must-Contain atributo
description: A lista de atributos obrigatórios para uma classe. Esses atributos devem ser especificados quando uma instância da classe é criada.
ms.assetid: ad112640-0e99-453a-8eff-f964419d8631
ms.tgt_platform: multiple
keywords:
- Esquema de Must-Contain do atributo AD
- Esquema de AD do atributo mustContain
topic_type:
- apiref
api_name:
- Must-Contain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d791468691f438d01161f0d6252f7b995fc0f51e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645422"
---
# <a name="must-contain-attribute"></a><span data-ttu-id="85f80-106">Must-Contain atributo</span><span class="sxs-lookup"><span data-stu-id="85f80-106">Must-Contain attribute</span></span>

<span data-ttu-id="85f80-107">A lista de atributos obrigatórios para uma classe.</span><span class="sxs-lookup"><span data-stu-id="85f80-107">The list of mandatory attributes for a class.</span></span> <span data-ttu-id="85f80-108">Esses atributos devem ser especificados quando uma instância da classe é criada.</span><span class="sxs-lookup"><span data-stu-id="85f80-108">These attributes must be specified when an instance of the class is created.</span></span>



| <span data-ttu-id="85f80-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="85f80-109">Entry</span></span> | <span data-ttu-id="85f80-110">Valor</span><span class="sxs-lookup"><span data-stu-id="85f80-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="85f80-111">CN</span><span class="sxs-lookup"><span data-stu-id="85f80-111">CN</span></span>                | <span data-ttu-id="85f80-112">Must-Contain</span><span class="sxs-lookup"><span data-stu-id="85f80-112">Must-Contain</span></span>                                                    |
| <span data-ttu-id="85f80-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="85f80-113">Ldap-Display-Name</span></span> | <span data-ttu-id="85f80-114">mustContain</span><span class="sxs-lookup"><span data-stu-id="85f80-114">mustContain</span></span>                                                     |
| <span data-ttu-id="85f80-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="85f80-115">Size</span></span>              | \-                                                              |
| <span data-ttu-id="85f80-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="85f80-116">Update Privilege</span></span>  | <span data-ttu-id="85f80-117">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="85f80-117">Schema administrator</span></span>                                            |
| <span data-ttu-id="85f80-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="85f80-118">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="85f80-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="85f80-119">Attribute-Id</span></span>      | <span data-ttu-id="85f80-120">1.2.840.113556.1.2.24</span><span class="sxs-lookup"><span data-stu-id="85f80-120">1.2.840.113556.1.2.24</span></span>                                           |
| <span data-ttu-id="85f80-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="85f80-121">System-Id-Guid</span></span>    | <span data-ttu-id="85f80-122">bf9679d3-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="85f80-122">bf9679d3-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="85f80-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="85f80-123">Syntax</span></span>            | [<span data-ttu-id="85f80-124">**Cadeia de caracteres (identificador de objeto)**</span><span class="sxs-lookup"><span data-stu-id="85f80-124">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="85f80-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="85f80-125">Implementations</span></span>

-   [<span data-ttu-id="85f80-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="85f80-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="85f80-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="85f80-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="85f80-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="85f80-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="85f80-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="85f80-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="85f80-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="85f80-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="85f80-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="85f80-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="85f80-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="85f80-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="85f80-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="85f80-133">Windows 2000 Server</span></span>



| <span data-ttu-id="85f80-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="85f80-134">Entry</span></span> | <span data-ttu-id="85f80-135">Valor</span><span class="sxs-lookup"><span data-stu-id="85f80-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="85f80-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="85f80-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="85f80-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85f80-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="85f80-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="85f80-138">System-Only</span></span>            | <span data-ttu-id="85f80-139">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-139">False</span></span>                                            |
| <span data-ttu-id="85f80-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="85f80-140">Is-Single-Valued</span></span>       | <span data-ttu-id="85f80-141">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-141">False</span></span>                                            |
| <span data-ttu-id="85f80-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="85f80-142">Is Indexed</span></span>             | <span data-ttu-id="85f80-143">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-143">False</span></span>                                            |
| <span data-ttu-id="85f80-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="85f80-144">In Global Catalog</span></span>      | <span data-ttu-id="85f80-145">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-145">False</span></span>                                            |
| <span data-ttu-id="85f80-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85f80-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="85f80-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="85f80-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="85f80-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85f80-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="85f80-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85f80-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="85f80-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85f80-150">Search-Flags</span></span>           | <span data-ttu-id="85f80-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85f80-151">0x00000000</span></span>                                       |
| <span data-ttu-id="85f80-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85f80-152">System-Flags</span></span>           | <span data-ttu-id="85f80-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85f80-153">0x00000010</span></span>                                       |
| <span data-ttu-id="85f80-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="85f80-154">Classes used in</span></span>        | [<span data-ttu-id="85f80-155">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="85f80-155">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="85f80-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="85f80-156">Windows Server 2003</span></span>



| <span data-ttu-id="85f80-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="85f80-157">Entry</span></span> | <span data-ttu-id="85f80-158">Valor</span><span class="sxs-lookup"><span data-stu-id="85f80-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="85f80-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="85f80-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="85f80-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85f80-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="85f80-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="85f80-161">System-Only</span></span>            | <span data-ttu-id="85f80-162">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-162">False</span></span>                                            |
| <span data-ttu-id="85f80-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="85f80-163">Is-Single-Valued</span></span>       | <span data-ttu-id="85f80-164">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-164">False</span></span>                                            |
| <span data-ttu-id="85f80-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="85f80-165">Is Indexed</span></span>             | <span data-ttu-id="85f80-166">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-166">False</span></span>                                            |
| <span data-ttu-id="85f80-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="85f80-167">In Global Catalog</span></span>      | <span data-ttu-id="85f80-168">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-168">False</span></span>                                            |
| <span data-ttu-id="85f80-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85f80-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="85f80-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="85f80-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="85f80-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85f80-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="85f80-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85f80-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="85f80-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85f80-173">Search-Flags</span></span>           | <span data-ttu-id="85f80-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85f80-174">0x00000000</span></span>                                       |
| <span data-ttu-id="85f80-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85f80-175">System-Flags</span></span>           | <span data-ttu-id="85f80-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85f80-176">0x00000010</span></span>                                       |
| <span data-ttu-id="85f80-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="85f80-177">Classes used in</span></span>        | [<span data-ttu-id="85f80-178">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="85f80-178">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="85f80-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="85f80-179">ADAM</span></span>



| <span data-ttu-id="85f80-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="85f80-180">Entry</span></span> | <span data-ttu-id="85f80-181">Valor</span><span class="sxs-lookup"><span data-stu-id="85f80-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="85f80-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="85f80-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="85f80-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85f80-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="85f80-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="85f80-184">System-Only</span></span>            | <span data-ttu-id="85f80-185">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-185">False</span></span>                                            |
| <span data-ttu-id="85f80-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="85f80-186">Is-Single-Valued</span></span>       | <span data-ttu-id="85f80-187">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-187">False</span></span>                                            |
| <span data-ttu-id="85f80-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="85f80-188">Is Indexed</span></span>             | <span data-ttu-id="85f80-189">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-189">False</span></span>                                            |
| <span data-ttu-id="85f80-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="85f80-190">In Global Catalog</span></span>      | <span data-ttu-id="85f80-191">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-191">False</span></span>                                            |
| <span data-ttu-id="85f80-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85f80-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="85f80-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="85f80-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="85f80-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85f80-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="85f80-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85f80-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="85f80-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85f80-196">Search-Flags</span></span>           | <span data-ttu-id="85f80-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85f80-197">0x00000000</span></span>                                       |
| <span data-ttu-id="85f80-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85f80-198">System-Flags</span></span>           | <span data-ttu-id="85f80-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85f80-199">0x00000010</span></span>                                       |
| <span data-ttu-id="85f80-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="85f80-200">Classes used in</span></span>        | [<span data-ttu-id="85f80-201">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="85f80-201">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="85f80-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="85f80-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="85f80-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="85f80-203">Entry</span></span> | <span data-ttu-id="85f80-204">Valor</span><span class="sxs-lookup"><span data-stu-id="85f80-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="85f80-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="85f80-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="85f80-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85f80-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="85f80-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="85f80-207">System-Only</span></span>            | <span data-ttu-id="85f80-208">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-208">False</span></span>                                            |
| <span data-ttu-id="85f80-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="85f80-209">Is-Single-Valued</span></span>       | <span data-ttu-id="85f80-210">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-210">False</span></span>                                            |
| <span data-ttu-id="85f80-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="85f80-211">Is Indexed</span></span>             | <span data-ttu-id="85f80-212">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-212">False</span></span>                                            |
| <span data-ttu-id="85f80-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="85f80-213">In Global Catalog</span></span>      | <span data-ttu-id="85f80-214">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-214">False</span></span>                                            |
| <span data-ttu-id="85f80-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85f80-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="85f80-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="85f80-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="85f80-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85f80-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="85f80-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85f80-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="85f80-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85f80-219">Search-Flags</span></span>           | <span data-ttu-id="85f80-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85f80-220">0x00000000</span></span>                                       |
| <span data-ttu-id="85f80-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85f80-221">System-Flags</span></span>           | <span data-ttu-id="85f80-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85f80-222">0x00000010</span></span>                                       |
| <span data-ttu-id="85f80-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="85f80-223">Classes used in</span></span>        | [<span data-ttu-id="85f80-224">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="85f80-224">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="85f80-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85f80-225">Windows Server 2008</span></span>



| <span data-ttu-id="85f80-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="85f80-226">Entry</span></span> | <span data-ttu-id="85f80-227">Valor</span><span class="sxs-lookup"><span data-stu-id="85f80-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="85f80-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="85f80-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="85f80-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85f80-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="85f80-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="85f80-230">System-Only</span></span>            | <span data-ttu-id="85f80-231">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-231">False</span></span>                                            |
| <span data-ttu-id="85f80-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="85f80-232">Is-Single-Valued</span></span>       | <span data-ttu-id="85f80-233">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-233">False</span></span>                                            |
| <span data-ttu-id="85f80-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="85f80-234">Is Indexed</span></span>             | <span data-ttu-id="85f80-235">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-235">False</span></span>                                            |
| <span data-ttu-id="85f80-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="85f80-236">In Global Catalog</span></span>      | <span data-ttu-id="85f80-237">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-237">False</span></span>                                            |
| <span data-ttu-id="85f80-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85f80-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="85f80-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="85f80-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="85f80-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85f80-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="85f80-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85f80-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="85f80-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85f80-242">Search-Flags</span></span>           | <span data-ttu-id="85f80-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85f80-243">0x00000000</span></span>                                       |
| <span data-ttu-id="85f80-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85f80-244">System-Flags</span></span>           | <span data-ttu-id="85f80-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85f80-245">0x00000010</span></span>                                       |
| <span data-ttu-id="85f80-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="85f80-246">Classes used in</span></span>        | [<span data-ttu-id="85f80-247">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="85f80-247">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="85f80-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="85f80-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="85f80-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="85f80-249">Entry</span></span> | <span data-ttu-id="85f80-250">Valor</span><span class="sxs-lookup"><span data-stu-id="85f80-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="85f80-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="85f80-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="85f80-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85f80-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="85f80-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="85f80-253">System-Only</span></span>            | <span data-ttu-id="85f80-254">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-254">False</span></span>                                            |
| <span data-ttu-id="85f80-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="85f80-255">Is-Single-Valued</span></span>       | <span data-ttu-id="85f80-256">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-256">False</span></span>                                            |
| <span data-ttu-id="85f80-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="85f80-257">Is Indexed</span></span>             | <span data-ttu-id="85f80-258">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-258">False</span></span>                                            |
| <span data-ttu-id="85f80-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="85f80-259">In Global Catalog</span></span>      | <span data-ttu-id="85f80-260">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-260">False</span></span>                                            |
| <span data-ttu-id="85f80-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85f80-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="85f80-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="85f80-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="85f80-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85f80-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="85f80-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85f80-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="85f80-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85f80-265">Search-Flags</span></span>           | <span data-ttu-id="85f80-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85f80-266">0x00000000</span></span>                                       |
| <span data-ttu-id="85f80-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85f80-267">System-Flags</span></span>           | <span data-ttu-id="85f80-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85f80-268">0x00000010</span></span>                                       |
| <span data-ttu-id="85f80-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="85f80-269">Classes used in</span></span>        | [<span data-ttu-id="85f80-270">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="85f80-270">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="85f80-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="85f80-271">Windows Server 2012</span></span>



| <span data-ttu-id="85f80-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="85f80-272">Entry</span></span> | <span data-ttu-id="85f80-273">Valor</span><span class="sxs-lookup"><span data-stu-id="85f80-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="85f80-274">ID do link</span><span class="sxs-lookup"><span data-stu-id="85f80-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="85f80-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85f80-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="85f80-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="85f80-276">System-Only</span></span>            | <span data-ttu-id="85f80-277">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-277">False</span></span>                                            |
| <span data-ttu-id="85f80-278">É de valor único</span><span class="sxs-lookup"><span data-stu-id="85f80-278">Is-Single-Valued</span></span>       | <span data-ttu-id="85f80-279">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-279">False</span></span>                                            |
| <span data-ttu-id="85f80-280">É indexado</span><span class="sxs-lookup"><span data-stu-id="85f80-280">Is Indexed</span></span>             | <span data-ttu-id="85f80-281">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-281">False</span></span>                                            |
| <span data-ttu-id="85f80-282">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="85f80-282">In Global Catalog</span></span>      | <span data-ttu-id="85f80-283">Falso</span><span class="sxs-lookup"><span data-stu-id="85f80-283">False</span></span>                                            |
| <span data-ttu-id="85f80-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85f80-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="85f80-285">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="85f80-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="85f80-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85f80-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="85f80-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85f80-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="85f80-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85f80-288">Search-Flags</span></span>           | <span data-ttu-id="85f80-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85f80-289">0x00000000</span></span>                                       |
| <span data-ttu-id="85f80-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85f80-290">System-Flags</span></span>           | <span data-ttu-id="85f80-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85f80-291">0x00000010</span></span>                                       |
| <span data-ttu-id="85f80-292">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="85f80-292">Classes used in</span></span>        | [<span data-ttu-id="85f80-293">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="85f80-293">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





