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
# <a name="must-contain-attribute"></a><span data-ttu-id="9a3e4-106">Must-Contain atributo</span><span class="sxs-lookup"><span data-stu-id="9a3e4-106">Must-Contain attribute</span></span>

<span data-ttu-id="9a3e4-107">A lista de atributos obrigatórios para uma classe.</span><span class="sxs-lookup"><span data-stu-id="9a3e4-107">The list of mandatory attributes for a class.</span></span> <span data-ttu-id="9a3e4-108">Esses atributos devem ser especificados quando uma instância da classe é criada.</span><span class="sxs-lookup"><span data-stu-id="9a3e4-108">These attributes must be specified when an instance of the class is created.</span></span>



| <span data-ttu-id="9a3e4-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a3e4-109">Entry</span></span> | <span data-ttu-id="9a3e4-110">Valor</span><span class="sxs-lookup"><span data-stu-id="9a3e4-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9a3e4-111">CN</span><span class="sxs-lookup"><span data-stu-id="9a3e4-111">CN</span></span>                | <span data-ttu-id="9a3e4-112">Must-Contain</span><span class="sxs-lookup"><span data-stu-id="9a3e4-112">Must-Contain</span></span>                                                    |
| <span data-ttu-id="9a3e4-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9a3e4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9a3e4-114">mustContain</span><span class="sxs-lookup"><span data-stu-id="9a3e4-114">mustContain</span></span>                                                     |
| <span data-ttu-id="9a3e4-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="9a3e4-115">Size</span></span>              | \-                                                              |
| <span data-ttu-id="9a3e4-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="9a3e4-116">Update Privilege</span></span>  | <span data-ttu-id="9a3e4-117">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="9a3e4-117">Schema administrator</span></span>                                            |
| <span data-ttu-id="9a3e4-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="9a3e4-118">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="9a3e4-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9a3e4-119">Attribute-Id</span></span>      | <span data-ttu-id="9a3e4-120">1.2.840.113556.1.2.24</span><span class="sxs-lookup"><span data-stu-id="9a3e4-120">1.2.840.113556.1.2.24</span></span>                                           |
| <span data-ttu-id="9a3e4-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9a3e4-121">System-Id-Guid</span></span>    | <span data-ttu-id="9a3e4-122">bf9679d3-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="9a3e4-122">bf9679d3-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="9a3e4-123">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a3e4-123">Syntax</span></span>            | [<span data-ttu-id="9a3e4-124">**Cadeia de caracteres (identificador de objeto)**</span><span class="sxs-lookup"><span data-stu-id="9a3e4-124">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="9a3e4-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="9a3e4-125">Implementations</span></span>

-   [<span data-ttu-id="9a3e4-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9a3e4-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9a3e4-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9a3e4-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9a3e4-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9a3e4-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9a3e4-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9a3e4-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9a3e4-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9a3e4-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9a3e4-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9a3e4-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9a3e4-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9a3e4-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9a3e4-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9a3e4-133">Windows 2000 Server</span></span>



| <span data-ttu-id="9a3e4-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a3e4-134">Entry</span></span> | <span data-ttu-id="9a3e4-135">Valor</span><span class="sxs-lookup"><span data-stu-id="9a3e4-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9a3e4-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="9a3e4-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a3e4-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a3e4-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a3e4-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a3e4-138">System-Only</span></span>            | <span data-ttu-id="9a3e4-139">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-139">False</span></span>                                            |
| <span data-ttu-id="9a3e4-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9a3e4-140">Is-Single-Valued</span></span>       | <span data-ttu-id="9a3e4-141">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-141">False</span></span>                                            |
| <span data-ttu-id="9a3e4-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="9a3e4-142">Is Indexed</span></span>             | <span data-ttu-id="9a3e4-143">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-143">False</span></span>                                            |
| <span data-ttu-id="9a3e4-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9a3e4-144">In Global Catalog</span></span>      | <span data-ttu-id="9a3e4-145">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-145">False</span></span>                                            |
| <span data-ttu-id="9a3e4-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a3e4-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a3e4-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9a3e4-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9a3e4-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a3e4-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9a3e4-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a3e4-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9a3e4-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a3e4-150">Search-Flags</span></span>           | <span data-ttu-id="9a3e4-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a3e4-151">0x00000000</span></span>                                       |
| <span data-ttu-id="9a3e4-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a3e4-152">System-Flags</span></span>           | <span data-ttu-id="9a3e4-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a3e4-153">0x00000010</span></span>                                       |
| <span data-ttu-id="9a3e4-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9a3e4-154">Classes used in</span></span>        | [<span data-ttu-id="9a3e4-155">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="9a3e4-155">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9a3e4-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9a3e4-156">Windows Server 2003</span></span>



| <span data-ttu-id="9a3e4-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a3e4-157">Entry</span></span> | <span data-ttu-id="9a3e4-158">Valor</span><span class="sxs-lookup"><span data-stu-id="9a3e4-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9a3e4-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="9a3e4-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a3e4-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a3e4-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a3e4-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a3e4-161">System-Only</span></span>            | <span data-ttu-id="9a3e4-162">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-162">False</span></span>                                            |
| <span data-ttu-id="9a3e4-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9a3e4-163">Is-Single-Valued</span></span>       | <span data-ttu-id="9a3e4-164">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-164">False</span></span>                                            |
| <span data-ttu-id="9a3e4-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="9a3e4-165">Is Indexed</span></span>             | <span data-ttu-id="9a3e4-166">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-166">False</span></span>                                            |
| <span data-ttu-id="9a3e4-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9a3e4-167">In Global Catalog</span></span>      | <span data-ttu-id="9a3e4-168">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-168">False</span></span>                                            |
| <span data-ttu-id="9a3e4-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a3e4-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a3e4-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9a3e4-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9a3e4-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a3e4-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9a3e4-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a3e4-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9a3e4-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a3e4-173">Search-Flags</span></span>           | <span data-ttu-id="9a3e4-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a3e4-174">0x00000000</span></span>                                       |
| <span data-ttu-id="9a3e4-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a3e4-175">System-Flags</span></span>           | <span data-ttu-id="9a3e4-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a3e4-176">0x00000010</span></span>                                       |
| <span data-ttu-id="9a3e4-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9a3e4-177">Classes used in</span></span>        | [<span data-ttu-id="9a3e4-178">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="9a3e4-178">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9a3e4-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="9a3e4-179">ADAM</span></span>



| <span data-ttu-id="9a3e4-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a3e4-180">Entry</span></span> | <span data-ttu-id="9a3e4-181">Valor</span><span class="sxs-lookup"><span data-stu-id="9a3e4-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9a3e4-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="9a3e4-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a3e4-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a3e4-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a3e4-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a3e4-184">System-Only</span></span>            | <span data-ttu-id="9a3e4-185">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-185">False</span></span>                                            |
| <span data-ttu-id="9a3e4-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9a3e4-186">Is-Single-Valued</span></span>       | <span data-ttu-id="9a3e4-187">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-187">False</span></span>                                            |
| <span data-ttu-id="9a3e4-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="9a3e4-188">Is Indexed</span></span>             | <span data-ttu-id="9a3e4-189">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-189">False</span></span>                                            |
| <span data-ttu-id="9a3e4-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9a3e4-190">In Global Catalog</span></span>      | <span data-ttu-id="9a3e4-191">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-191">False</span></span>                                            |
| <span data-ttu-id="9a3e4-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a3e4-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a3e4-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9a3e4-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9a3e4-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a3e4-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9a3e4-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a3e4-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9a3e4-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a3e4-196">Search-Flags</span></span>           | <span data-ttu-id="9a3e4-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a3e4-197">0x00000000</span></span>                                       |
| <span data-ttu-id="9a3e4-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a3e4-198">System-Flags</span></span>           | <span data-ttu-id="9a3e4-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a3e4-199">0x00000010</span></span>                                       |
| <span data-ttu-id="9a3e4-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9a3e4-200">Classes used in</span></span>        | [<span data-ttu-id="9a3e4-201">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="9a3e4-201">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9a3e4-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9a3e4-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9a3e4-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a3e4-203">Entry</span></span> | <span data-ttu-id="9a3e4-204">Valor</span><span class="sxs-lookup"><span data-stu-id="9a3e4-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9a3e4-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="9a3e4-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a3e4-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a3e4-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a3e4-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a3e4-207">System-Only</span></span>            | <span data-ttu-id="9a3e4-208">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-208">False</span></span>                                            |
| <span data-ttu-id="9a3e4-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9a3e4-209">Is-Single-Valued</span></span>       | <span data-ttu-id="9a3e4-210">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-210">False</span></span>                                            |
| <span data-ttu-id="9a3e4-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="9a3e4-211">Is Indexed</span></span>             | <span data-ttu-id="9a3e4-212">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-212">False</span></span>                                            |
| <span data-ttu-id="9a3e4-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9a3e4-213">In Global Catalog</span></span>      | <span data-ttu-id="9a3e4-214">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-214">False</span></span>                                            |
| <span data-ttu-id="9a3e4-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a3e4-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a3e4-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9a3e4-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9a3e4-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a3e4-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9a3e4-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a3e4-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9a3e4-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a3e4-219">Search-Flags</span></span>           | <span data-ttu-id="9a3e4-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a3e4-220">0x00000000</span></span>                                       |
| <span data-ttu-id="9a3e4-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a3e4-221">System-Flags</span></span>           | <span data-ttu-id="9a3e4-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a3e4-222">0x00000010</span></span>                                       |
| <span data-ttu-id="9a3e4-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9a3e4-223">Classes used in</span></span>        | [<span data-ttu-id="9a3e4-224">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="9a3e4-224">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9a3e4-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a3e4-225">Windows Server 2008</span></span>



| <span data-ttu-id="9a3e4-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a3e4-226">Entry</span></span> | <span data-ttu-id="9a3e4-227">Valor</span><span class="sxs-lookup"><span data-stu-id="9a3e4-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9a3e4-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="9a3e4-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a3e4-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a3e4-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a3e4-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a3e4-230">System-Only</span></span>            | <span data-ttu-id="9a3e4-231">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-231">False</span></span>                                            |
| <span data-ttu-id="9a3e4-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9a3e4-232">Is-Single-Valued</span></span>       | <span data-ttu-id="9a3e4-233">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-233">False</span></span>                                            |
| <span data-ttu-id="9a3e4-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="9a3e4-234">Is Indexed</span></span>             | <span data-ttu-id="9a3e4-235">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-235">False</span></span>                                            |
| <span data-ttu-id="9a3e4-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9a3e4-236">In Global Catalog</span></span>      | <span data-ttu-id="9a3e4-237">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-237">False</span></span>                                            |
| <span data-ttu-id="9a3e4-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a3e4-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a3e4-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9a3e4-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9a3e4-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a3e4-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9a3e4-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a3e4-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9a3e4-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a3e4-242">Search-Flags</span></span>           | <span data-ttu-id="9a3e4-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a3e4-243">0x00000000</span></span>                                       |
| <span data-ttu-id="9a3e4-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a3e4-244">System-Flags</span></span>           | <span data-ttu-id="9a3e4-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a3e4-245">0x00000010</span></span>                                       |
| <span data-ttu-id="9a3e4-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9a3e4-246">Classes used in</span></span>        | [<span data-ttu-id="9a3e4-247">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="9a3e4-247">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9a3e4-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9a3e4-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9a3e4-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a3e4-249">Entry</span></span> | <span data-ttu-id="9a3e4-250">Valor</span><span class="sxs-lookup"><span data-stu-id="9a3e4-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9a3e4-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="9a3e4-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a3e4-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a3e4-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a3e4-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a3e4-253">System-Only</span></span>            | <span data-ttu-id="9a3e4-254">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-254">False</span></span>                                            |
| <span data-ttu-id="9a3e4-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9a3e4-255">Is-Single-Valued</span></span>       | <span data-ttu-id="9a3e4-256">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-256">False</span></span>                                            |
| <span data-ttu-id="9a3e4-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="9a3e4-257">Is Indexed</span></span>             | <span data-ttu-id="9a3e4-258">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-258">False</span></span>                                            |
| <span data-ttu-id="9a3e4-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9a3e4-259">In Global Catalog</span></span>      | <span data-ttu-id="9a3e4-260">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-260">False</span></span>                                            |
| <span data-ttu-id="9a3e4-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a3e4-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a3e4-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9a3e4-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9a3e4-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a3e4-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9a3e4-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a3e4-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9a3e4-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a3e4-265">Search-Flags</span></span>           | <span data-ttu-id="9a3e4-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a3e4-266">0x00000000</span></span>                                       |
| <span data-ttu-id="9a3e4-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a3e4-267">System-Flags</span></span>           | <span data-ttu-id="9a3e4-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a3e4-268">0x00000010</span></span>                                       |
| <span data-ttu-id="9a3e4-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9a3e4-269">Classes used in</span></span>        | [<span data-ttu-id="9a3e4-270">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="9a3e4-270">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9a3e4-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9a3e4-271">Windows Server 2012</span></span>



| <span data-ttu-id="9a3e4-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a3e4-272">Entry</span></span> | <span data-ttu-id="9a3e4-273">Valor</span><span class="sxs-lookup"><span data-stu-id="9a3e4-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="9a3e4-274">ID do link</span><span class="sxs-lookup"><span data-stu-id="9a3e4-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a3e4-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a3e4-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="9a3e4-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a3e4-276">System-Only</span></span>            | <span data-ttu-id="9a3e4-277">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-277">False</span></span>                                            |
| <span data-ttu-id="9a3e4-278">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9a3e4-278">Is-Single-Valued</span></span>       | <span data-ttu-id="9a3e4-279">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-279">False</span></span>                                            |
| <span data-ttu-id="9a3e4-280">É indexado</span><span class="sxs-lookup"><span data-stu-id="9a3e4-280">Is Indexed</span></span>             | <span data-ttu-id="9a3e4-281">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-281">False</span></span>                                            |
| <span data-ttu-id="9a3e4-282">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9a3e4-282">In Global Catalog</span></span>      | <span data-ttu-id="9a3e4-283">Falso</span><span class="sxs-lookup"><span data-stu-id="9a3e4-283">False</span></span>                                            |
| <span data-ttu-id="9a3e4-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a3e4-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a3e4-285">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9a3e4-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="9a3e4-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a3e4-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="9a3e4-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a3e4-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="9a3e4-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a3e4-288">Search-Flags</span></span>           | <span data-ttu-id="9a3e4-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a3e4-289">0x00000000</span></span>                                       |
| <span data-ttu-id="9a3e4-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a3e4-290">System-Flags</span></span>           | <span data-ttu-id="9a3e4-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a3e4-291">0x00000010</span></span>                                       |
| <span data-ttu-id="9a3e4-292">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9a3e4-292">Classes used in</span></span>        | [<span data-ttu-id="9a3e4-293">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="9a3e4-293">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





