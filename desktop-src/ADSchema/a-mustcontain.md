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
# <a name="must-contain-attribute"></a><span data-ttu-id="3ed26-106">Must-Contain atributo</span><span class="sxs-lookup"><span data-stu-id="3ed26-106">Must-Contain attribute</span></span>

<span data-ttu-id="3ed26-107">A lista de atributos obrigatórios para uma classe.</span><span class="sxs-lookup"><span data-stu-id="3ed26-107">The list of mandatory attributes for a class.</span></span> <span data-ttu-id="3ed26-108">Esses atributos devem ser especificados quando uma instância da classe é criada.</span><span class="sxs-lookup"><span data-stu-id="3ed26-108">These attributes must be specified when an instance of the class is created.</span></span>



| <span data-ttu-id="3ed26-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ed26-109">Entry</span></span> | <span data-ttu-id="3ed26-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3ed26-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="3ed26-111">CN</span><span class="sxs-lookup"><span data-stu-id="3ed26-111">CN</span></span>                | <span data-ttu-id="3ed26-112">Must-Contain</span><span class="sxs-lookup"><span data-stu-id="3ed26-112">Must-Contain</span></span>                                                    |
| <span data-ttu-id="3ed26-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3ed26-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3ed26-114">mustContain</span><span class="sxs-lookup"><span data-stu-id="3ed26-114">mustContain</span></span>                                                     |
| <span data-ttu-id="3ed26-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="3ed26-115">Size</span></span>              | \-                                                              |
| <span data-ttu-id="3ed26-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="3ed26-116">Update Privilege</span></span>  | <span data-ttu-id="3ed26-117">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="3ed26-117">Schema administrator</span></span>                                            |
| <span data-ttu-id="3ed26-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="3ed26-118">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="3ed26-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3ed26-119">Attribute-Id</span></span>      | <span data-ttu-id="3ed26-120">1.2.840.113556.1.2.24</span><span class="sxs-lookup"><span data-stu-id="3ed26-120">1.2.840.113556.1.2.24</span></span>                                           |
| <span data-ttu-id="3ed26-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3ed26-121">System-Id-Guid</span></span>    | <span data-ttu-id="3ed26-122">bf9679d3-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3ed26-122">bf9679d3-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="3ed26-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ed26-123">Syntax</span></span>            | [<span data-ttu-id="3ed26-124">**Cadeia de caracteres (identificador de objeto)**</span><span class="sxs-lookup"><span data-stu-id="3ed26-124">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="3ed26-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="3ed26-125">Implementations</span></span>

-   [<span data-ttu-id="3ed26-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3ed26-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3ed26-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3ed26-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3ed26-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="3ed26-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3ed26-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3ed26-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3ed26-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3ed26-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3ed26-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3ed26-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3ed26-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3ed26-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3ed26-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3ed26-133">Windows 2000 Server</span></span>



| <span data-ttu-id="3ed26-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ed26-134">Entry</span></span> | <span data-ttu-id="3ed26-135">Valor</span><span class="sxs-lookup"><span data-stu-id="3ed26-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3ed26-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ed26-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3ed26-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ed26-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3ed26-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ed26-138">System-Only</span></span>            | <span data-ttu-id="3ed26-139">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-139">False</span></span>                                            |
| <span data-ttu-id="3ed26-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ed26-140">Is-Single-Valued</span></span>       | <span data-ttu-id="3ed26-141">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-141">False</span></span>                                            |
| <span data-ttu-id="3ed26-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ed26-142">Is Indexed</span></span>             | <span data-ttu-id="3ed26-143">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-143">False</span></span>                                            |
| <span data-ttu-id="3ed26-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ed26-144">In Global Catalog</span></span>      | <span data-ttu-id="3ed26-145">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-145">False</span></span>                                            |
| <span data-ttu-id="3ed26-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ed26-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ed26-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ed26-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3ed26-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ed26-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3ed26-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ed26-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3ed26-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ed26-150">Search-Flags</span></span>           | <span data-ttu-id="3ed26-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ed26-151">0x00000000</span></span>                                       |
| <span data-ttu-id="3ed26-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ed26-152">System-Flags</span></span>           | <span data-ttu-id="3ed26-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ed26-153">0x00000010</span></span>                                       |
| <span data-ttu-id="3ed26-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ed26-154">Classes used in</span></span>        | [<span data-ttu-id="3ed26-155">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="3ed26-155">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3ed26-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3ed26-156">Windows Server 2003</span></span>



| <span data-ttu-id="3ed26-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ed26-157">Entry</span></span> | <span data-ttu-id="3ed26-158">Valor</span><span class="sxs-lookup"><span data-stu-id="3ed26-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3ed26-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ed26-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3ed26-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ed26-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3ed26-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ed26-161">System-Only</span></span>            | <span data-ttu-id="3ed26-162">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-162">False</span></span>                                            |
| <span data-ttu-id="3ed26-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ed26-163">Is-Single-Valued</span></span>       | <span data-ttu-id="3ed26-164">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-164">False</span></span>                                            |
| <span data-ttu-id="3ed26-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ed26-165">Is Indexed</span></span>             | <span data-ttu-id="3ed26-166">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-166">False</span></span>                                            |
| <span data-ttu-id="3ed26-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ed26-167">In Global Catalog</span></span>      | <span data-ttu-id="3ed26-168">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-168">False</span></span>                                            |
| <span data-ttu-id="3ed26-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ed26-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ed26-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ed26-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3ed26-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ed26-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3ed26-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ed26-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3ed26-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ed26-173">Search-Flags</span></span>           | <span data-ttu-id="3ed26-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ed26-174">0x00000000</span></span>                                       |
| <span data-ttu-id="3ed26-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ed26-175">System-Flags</span></span>           | <span data-ttu-id="3ed26-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ed26-176">0x00000010</span></span>                                       |
| <span data-ttu-id="3ed26-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ed26-177">Classes used in</span></span>        | [<span data-ttu-id="3ed26-178">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="3ed26-178">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="3ed26-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="3ed26-179">ADAM</span></span>



| <span data-ttu-id="3ed26-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ed26-180">Entry</span></span> | <span data-ttu-id="3ed26-181">Valor</span><span class="sxs-lookup"><span data-stu-id="3ed26-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3ed26-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ed26-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3ed26-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ed26-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3ed26-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ed26-184">System-Only</span></span>            | <span data-ttu-id="3ed26-185">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-185">False</span></span>                                            |
| <span data-ttu-id="3ed26-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ed26-186">Is-Single-Valued</span></span>       | <span data-ttu-id="3ed26-187">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-187">False</span></span>                                            |
| <span data-ttu-id="3ed26-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ed26-188">Is Indexed</span></span>             | <span data-ttu-id="3ed26-189">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-189">False</span></span>                                            |
| <span data-ttu-id="3ed26-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ed26-190">In Global Catalog</span></span>      | <span data-ttu-id="3ed26-191">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-191">False</span></span>                                            |
| <span data-ttu-id="3ed26-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ed26-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ed26-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ed26-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3ed26-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ed26-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3ed26-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ed26-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3ed26-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ed26-196">Search-Flags</span></span>           | <span data-ttu-id="3ed26-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ed26-197">0x00000000</span></span>                                       |
| <span data-ttu-id="3ed26-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ed26-198">System-Flags</span></span>           | <span data-ttu-id="3ed26-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ed26-199">0x00000010</span></span>                                       |
| <span data-ttu-id="3ed26-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ed26-200">Classes used in</span></span>        | [<span data-ttu-id="3ed26-201">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="3ed26-201">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3ed26-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3ed26-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3ed26-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ed26-203">Entry</span></span> | <span data-ttu-id="3ed26-204">Valor</span><span class="sxs-lookup"><span data-stu-id="3ed26-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3ed26-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ed26-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3ed26-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ed26-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3ed26-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ed26-207">System-Only</span></span>            | <span data-ttu-id="3ed26-208">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-208">False</span></span>                                            |
| <span data-ttu-id="3ed26-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ed26-209">Is-Single-Valued</span></span>       | <span data-ttu-id="3ed26-210">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-210">False</span></span>                                            |
| <span data-ttu-id="3ed26-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ed26-211">Is Indexed</span></span>             | <span data-ttu-id="3ed26-212">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-212">False</span></span>                                            |
| <span data-ttu-id="3ed26-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ed26-213">In Global Catalog</span></span>      | <span data-ttu-id="3ed26-214">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-214">False</span></span>                                            |
| <span data-ttu-id="3ed26-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ed26-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ed26-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ed26-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3ed26-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ed26-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3ed26-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ed26-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3ed26-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ed26-219">Search-Flags</span></span>           | <span data-ttu-id="3ed26-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ed26-220">0x00000000</span></span>                                       |
| <span data-ttu-id="3ed26-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ed26-221">System-Flags</span></span>           | <span data-ttu-id="3ed26-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ed26-222">0x00000010</span></span>                                       |
| <span data-ttu-id="3ed26-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ed26-223">Classes used in</span></span>        | [<span data-ttu-id="3ed26-224">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="3ed26-224">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3ed26-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ed26-225">Windows Server 2008</span></span>



| <span data-ttu-id="3ed26-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ed26-226">Entry</span></span> | <span data-ttu-id="3ed26-227">Valor</span><span class="sxs-lookup"><span data-stu-id="3ed26-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3ed26-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ed26-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3ed26-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ed26-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3ed26-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ed26-230">System-Only</span></span>            | <span data-ttu-id="3ed26-231">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-231">False</span></span>                                            |
| <span data-ttu-id="3ed26-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ed26-232">Is-Single-Valued</span></span>       | <span data-ttu-id="3ed26-233">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-233">False</span></span>                                            |
| <span data-ttu-id="3ed26-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ed26-234">Is Indexed</span></span>             | <span data-ttu-id="3ed26-235">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-235">False</span></span>                                            |
| <span data-ttu-id="3ed26-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ed26-236">In Global Catalog</span></span>      | <span data-ttu-id="3ed26-237">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-237">False</span></span>                                            |
| <span data-ttu-id="3ed26-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ed26-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ed26-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ed26-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3ed26-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ed26-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3ed26-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ed26-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3ed26-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ed26-242">Search-Flags</span></span>           | <span data-ttu-id="3ed26-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ed26-243">0x00000000</span></span>                                       |
| <span data-ttu-id="3ed26-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ed26-244">System-Flags</span></span>           | <span data-ttu-id="3ed26-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ed26-245">0x00000010</span></span>                                       |
| <span data-ttu-id="3ed26-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ed26-246">Classes used in</span></span>        | [<span data-ttu-id="3ed26-247">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="3ed26-247">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3ed26-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3ed26-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3ed26-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ed26-249">Entry</span></span> | <span data-ttu-id="3ed26-250">Valor</span><span class="sxs-lookup"><span data-stu-id="3ed26-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3ed26-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ed26-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3ed26-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ed26-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3ed26-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ed26-253">System-Only</span></span>            | <span data-ttu-id="3ed26-254">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-254">False</span></span>                                            |
| <span data-ttu-id="3ed26-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ed26-255">Is-Single-Valued</span></span>       | <span data-ttu-id="3ed26-256">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-256">False</span></span>                                            |
| <span data-ttu-id="3ed26-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ed26-257">Is Indexed</span></span>             | <span data-ttu-id="3ed26-258">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-258">False</span></span>                                            |
| <span data-ttu-id="3ed26-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ed26-259">In Global Catalog</span></span>      | <span data-ttu-id="3ed26-260">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-260">False</span></span>                                            |
| <span data-ttu-id="3ed26-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ed26-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ed26-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ed26-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3ed26-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ed26-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3ed26-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ed26-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3ed26-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ed26-265">Search-Flags</span></span>           | <span data-ttu-id="3ed26-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ed26-266">0x00000000</span></span>                                       |
| <span data-ttu-id="3ed26-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ed26-267">System-Flags</span></span>           | <span data-ttu-id="3ed26-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ed26-268">0x00000010</span></span>                                       |
| <span data-ttu-id="3ed26-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ed26-269">Classes used in</span></span>        | [<span data-ttu-id="3ed26-270">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="3ed26-270">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3ed26-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3ed26-271">Windows Server 2012</span></span>



| <span data-ttu-id="3ed26-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ed26-272">Entry</span></span> | <span data-ttu-id="3ed26-273">Valor</span><span class="sxs-lookup"><span data-stu-id="3ed26-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3ed26-274">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ed26-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3ed26-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ed26-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3ed26-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ed26-276">System-Only</span></span>            | <span data-ttu-id="3ed26-277">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-277">False</span></span>                                            |
| <span data-ttu-id="3ed26-278">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ed26-278">Is-Single-Valued</span></span>       | <span data-ttu-id="3ed26-279">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-279">False</span></span>                                            |
| <span data-ttu-id="3ed26-280">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ed26-280">Is Indexed</span></span>             | <span data-ttu-id="3ed26-281">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-281">False</span></span>                                            |
| <span data-ttu-id="3ed26-282">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ed26-282">In Global Catalog</span></span>      | <span data-ttu-id="3ed26-283">Falso</span><span class="sxs-lookup"><span data-stu-id="3ed26-283">False</span></span>                                            |
| <span data-ttu-id="3ed26-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ed26-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ed26-285">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ed26-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3ed26-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ed26-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3ed26-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ed26-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3ed26-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ed26-288">Search-Flags</span></span>           | <span data-ttu-id="3ed26-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ed26-289">0x00000000</span></span>                                       |
| <span data-ttu-id="3ed26-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ed26-290">System-Flags</span></span>           | <span data-ttu-id="3ed26-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ed26-291">0x00000010</span></span>                                       |
| <span data-ttu-id="3ed26-292">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ed26-292">Classes used in</span></span>        | [<span data-ttu-id="3ed26-293">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="3ed26-293">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





