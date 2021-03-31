---
title: Atributo allowed-Child-classes
description: Classes que podem ser contidas por uma classe.
ms.assetid: 3bfeefe3-b728-40a2-8b0a-3064a9ca42d0
ms.tgt_platform: multiple
keywords:
- Atributo AD de atributos de classes filho permitidas
- Esquema de AD do atributo allowedChildClasses
topic_type:
- apiref
api_name:
- Allowed-Child-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45c295036ad8b1c132e2dbf97d2e0d9ab38f9598
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645600"
---
# <a name="allowed-child-classes-attribute"></a><span data-ttu-id="872d4-105">Atributo allowed-Child-classes</span><span class="sxs-lookup"><span data-stu-id="872d4-105">Allowed-Child-Classes attribute</span></span>

<span data-ttu-id="872d4-106">Classes que podem ser contidas por uma classe.</span><span class="sxs-lookup"><span data-stu-id="872d4-106">Classes that can be contained by a class.</span></span>



| <span data-ttu-id="872d4-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="872d4-107">Entry</span></span> | <span data-ttu-id="872d4-108">Valor</span><span class="sxs-lookup"><span data-stu-id="872d4-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="872d4-109">CN</span><span class="sxs-lookup"><span data-stu-id="872d4-109">CN</span></span>                | <span data-ttu-id="872d4-110">Classes filho permitidas</span><span class="sxs-lookup"><span data-stu-id="872d4-110">Allowed-Child-Classes</span></span>                                           |
| <span data-ttu-id="872d4-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="872d4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="872d4-112">allowedChildClasses</span><span class="sxs-lookup"><span data-stu-id="872d4-112">allowedChildClasses</span></span>                                             |
| <span data-ttu-id="872d4-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="872d4-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="872d4-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="872d4-114">Update Privilege</span></span>  | \-                                                              |
| <span data-ttu-id="872d4-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="872d4-115">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="872d4-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="872d4-116">Attribute-Id</span></span>      | <span data-ttu-id="872d4-117">1.2.840.113556.1.4.911</span><span class="sxs-lookup"><span data-stu-id="872d4-117">1.2.840.113556.1.4.911</span></span>                                          |
| <span data-ttu-id="872d4-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="872d4-118">System-Id-Guid</span></span>    | <span data-ttu-id="872d4-119">9a7ad942-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="872d4-119">9a7ad942-ca53-11d1-bbd0-0080c76670c0</span></span>                            |
| <span data-ttu-id="872d4-120">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="872d4-120">Syntax</span></span>            | [<span data-ttu-id="872d4-121">**Cadeia de caracteres (identificador de objeto)**</span><span class="sxs-lookup"><span data-stu-id="872d4-121">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="872d4-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="872d4-122">Implementations</span></span>

-   [<span data-ttu-id="872d4-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="872d4-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="872d4-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="872d4-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="872d4-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="872d4-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="872d4-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="872d4-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="872d4-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="872d4-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="872d4-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="872d4-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="872d4-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="872d4-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="872d4-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="872d4-130">Windows 2000 Server</span></span>



| <span data-ttu-id="872d4-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="872d4-131">Entry</span></span> | <span data-ttu-id="872d4-132">Valor</span><span class="sxs-lookup"><span data-stu-id="872d4-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="872d4-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="872d4-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="872d4-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="872d4-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="872d4-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="872d4-135">System-Only</span></span>            | <span data-ttu-id="872d4-136">True</span><span class="sxs-lookup"><span data-stu-id="872d4-136">True</span></span>                            |
| <span data-ttu-id="872d4-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="872d4-137">Is-Single-Valued</span></span>       | <span data-ttu-id="872d4-138">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-138">False</span></span>                           |
| <span data-ttu-id="872d4-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="872d4-139">Is Indexed</span></span>             | <span data-ttu-id="872d4-140">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-140">False</span></span>                           |
| <span data-ttu-id="872d4-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="872d4-141">In Global Catalog</span></span>      | <span data-ttu-id="872d4-142">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-142">False</span></span>                           |
| <span data-ttu-id="872d4-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="872d4-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="872d4-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="872d4-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="872d4-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="872d4-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="872d4-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="872d4-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="872d4-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="872d4-147">Search-Flags</span></span>           | <span data-ttu-id="872d4-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="872d4-148">0x00000000</span></span>                      |
| <span data-ttu-id="872d4-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="872d4-149">System-Flags</span></span>           | <span data-ttu-id="872d4-150">0x08000014</span><span class="sxs-lookup"><span data-stu-id="872d4-150">0x08000014</span></span>                      |
| <span data-ttu-id="872d4-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="872d4-151">Classes used in</span></span>        | [<span data-ttu-id="872d4-152">**Início**</span><span class="sxs-lookup"><span data-stu-id="872d4-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="872d4-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="872d4-153">Windows Server 2003</span></span>



| <span data-ttu-id="872d4-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="872d4-154">Entry</span></span> | <span data-ttu-id="872d4-155">Valor</span><span class="sxs-lookup"><span data-stu-id="872d4-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="872d4-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="872d4-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="872d4-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="872d4-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="872d4-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="872d4-158">System-Only</span></span>            | <span data-ttu-id="872d4-159">True</span><span class="sxs-lookup"><span data-stu-id="872d4-159">True</span></span>                            |
| <span data-ttu-id="872d4-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="872d4-160">Is-Single-Valued</span></span>       | <span data-ttu-id="872d4-161">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-161">False</span></span>                           |
| <span data-ttu-id="872d4-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="872d4-162">Is Indexed</span></span>             | <span data-ttu-id="872d4-163">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-163">False</span></span>                           |
| <span data-ttu-id="872d4-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="872d4-164">In Global Catalog</span></span>      | <span data-ttu-id="872d4-165">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-165">False</span></span>                           |
| <span data-ttu-id="872d4-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="872d4-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="872d4-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="872d4-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="872d4-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="872d4-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="872d4-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="872d4-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="872d4-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="872d4-170">Search-Flags</span></span>           | <span data-ttu-id="872d4-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="872d4-171">0x00000000</span></span>                      |
| <span data-ttu-id="872d4-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="872d4-172">System-Flags</span></span>           | <span data-ttu-id="872d4-173">0x08000014</span><span class="sxs-lookup"><span data-stu-id="872d4-173">0x08000014</span></span>                      |
| <span data-ttu-id="872d4-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="872d4-174">Classes used in</span></span>        | [<span data-ttu-id="872d4-175">**Início**</span><span class="sxs-lookup"><span data-stu-id="872d4-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="872d4-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="872d4-176">ADAM</span></span>



| <span data-ttu-id="872d4-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="872d4-177">Entry</span></span> | <span data-ttu-id="872d4-178">Valor</span><span class="sxs-lookup"><span data-stu-id="872d4-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="872d4-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="872d4-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="872d4-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="872d4-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="872d4-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="872d4-181">System-Only</span></span>            | <span data-ttu-id="872d4-182">True</span><span class="sxs-lookup"><span data-stu-id="872d4-182">True</span></span>                            |
| <span data-ttu-id="872d4-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="872d4-183">Is-Single-Valued</span></span>       | <span data-ttu-id="872d4-184">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-184">False</span></span>                           |
| <span data-ttu-id="872d4-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="872d4-185">Is Indexed</span></span>             | <span data-ttu-id="872d4-186">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-186">False</span></span>                           |
| <span data-ttu-id="872d4-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="872d4-187">In Global Catalog</span></span>      | <span data-ttu-id="872d4-188">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-188">False</span></span>                           |
| <span data-ttu-id="872d4-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="872d4-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="872d4-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="872d4-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="872d4-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="872d4-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="872d4-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="872d4-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="872d4-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="872d4-193">Search-Flags</span></span>           | <span data-ttu-id="872d4-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="872d4-194">0x00000000</span></span>                      |
| <span data-ttu-id="872d4-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="872d4-195">System-Flags</span></span>           | <span data-ttu-id="872d4-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="872d4-196">0x08000014</span></span>                      |
| <span data-ttu-id="872d4-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="872d4-197">Classes used in</span></span>        | [<span data-ttu-id="872d4-198">**Início**</span><span class="sxs-lookup"><span data-stu-id="872d4-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="872d4-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="872d4-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="872d4-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="872d4-200">Entry</span></span> | <span data-ttu-id="872d4-201">Valor</span><span class="sxs-lookup"><span data-stu-id="872d4-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="872d4-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="872d4-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="872d4-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="872d4-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="872d4-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="872d4-204">System-Only</span></span>            | <span data-ttu-id="872d4-205">True</span><span class="sxs-lookup"><span data-stu-id="872d4-205">True</span></span>                            |
| <span data-ttu-id="872d4-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="872d4-206">Is-Single-Valued</span></span>       | <span data-ttu-id="872d4-207">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-207">False</span></span>                           |
| <span data-ttu-id="872d4-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="872d4-208">Is Indexed</span></span>             | <span data-ttu-id="872d4-209">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-209">False</span></span>                           |
| <span data-ttu-id="872d4-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="872d4-210">In Global Catalog</span></span>      | <span data-ttu-id="872d4-211">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-211">False</span></span>                           |
| <span data-ttu-id="872d4-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="872d4-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="872d4-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="872d4-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="872d4-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="872d4-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="872d4-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="872d4-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="872d4-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="872d4-216">Search-Flags</span></span>           | <span data-ttu-id="872d4-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="872d4-217">0x00000000</span></span>                      |
| <span data-ttu-id="872d4-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="872d4-218">System-Flags</span></span>           | <span data-ttu-id="872d4-219">0x08000014</span><span class="sxs-lookup"><span data-stu-id="872d4-219">0x08000014</span></span>                      |
| <span data-ttu-id="872d4-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="872d4-220">Classes used in</span></span>        | [<span data-ttu-id="872d4-221">**Início**</span><span class="sxs-lookup"><span data-stu-id="872d4-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="872d4-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="872d4-222">Windows Server 2008</span></span>



| <span data-ttu-id="872d4-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="872d4-223">Entry</span></span> | <span data-ttu-id="872d4-224">Valor</span><span class="sxs-lookup"><span data-stu-id="872d4-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="872d4-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="872d4-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="872d4-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="872d4-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="872d4-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="872d4-227">System-Only</span></span>            | <span data-ttu-id="872d4-228">True</span><span class="sxs-lookup"><span data-stu-id="872d4-228">True</span></span>                            |
| <span data-ttu-id="872d4-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="872d4-229">Is-Single-Valued</span></span>       | <span data-ttu-id="872d4-230">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-230">False</span></span>                           |
| <span data-ttu-id="872d4-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="872d4-231">Is Indexed</span></span>             | <span data-ttu-id="872d4-232">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-232">False</span></span>                           |
| <span data-ttu-id="872d4-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="872d4-233">In Global Catalog</span></span>      | <span data-ttu-id="872d4-234">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-234">False</span></span>                           |
| <span data-ttu-id="872d4-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="872d4-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="872d4-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="872d4-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="872d4-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="872d4-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="872d4-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="872d4-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="872d4-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="872d4-239">Search-Flags</span></span>           | <span data-ttu-id="872d4-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="872d4-240">0x00000000</span></span>                      |
| <span data-ttu-id="872d4-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="872d4-241">System-Flags</span></span>           | <span data-ttu-id="872d4-242">0x08000014</span><span class="sxs-lookup"><span data-stu-id="872d4-242">0x08000014</span></span>                      |
| <span data-ttu-id="872d4-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="872d4-243">Classes used in</span></span>        | [<span data-ttu-id="872d4-244">**Início**</span><span class="sxs-lookup"><span data-stu-id="872d4-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="872d4-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="872d4-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="872d4-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="872d4-246">Entry</span></span> | <span data-ttu-id="872d4-247">Valor</span><span class="sxs-lookup"><span data-stu-id="872d4-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="872d4-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="872d4-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="872d4-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="872d4-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="872d4-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="872d4-250">System-Only</span></span>            | <span data-ttu-id="872d4-251">True</span><span class="sxs-lookup"><span data-stu-id="872d4-251">True</span></span>                            |
| <span data-ttu-id="872d4-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="872d4-252">Is-Single-Valued</span></span>       | <span data-ttu-id="872d4-253">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-253">False</span></span>                           |
| <span data-ttu-id="872d4-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="872d4-254">Is Indexed</span></span>             | <span data-ttu-id="872d4-255">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-255">False</span></span>                           |
| <span data-ttu-id="872d4-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="872d4-256">In Global Catalog</span></span>      | <span data-ttu-id="872d4-257">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-257">False</span></span>                           |
| <span data-ttu-id="872d4-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="872d4-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="872d4-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="872d4-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="872d4-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="872d4-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="872d4-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="872d4-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="872d4-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="872d4-262">Search-Flags</span></span>           | <span data-ttu-id="872d4-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="872d4-263">0x00000000</span></span>                      |
| <span data-ttu-id="872d4-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="872d4-264">System-Flags</span></span>           | <span data-ttu-id="872d4-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="872d4-265">0x08000014</span></span>                      |
| <span data-ttu-id="872d4-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="872d4-266">Classes used in</span></span>        | [<span data-ttu-id="872d4-267">**Início**</span><span class="sxs-lookup"><span data-stu-id="872d4-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="872d4-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="872d4-268">Windows Server 2012</span></span>



| <span data-ttu-id="872d4-269">Entrada</span><span class="sxs-lookup"><span data-stu-id="872d4-269">Entry</span></span> | <span data-ttu-id="872d4-270">Valor</span><span class="sxs-lookup"><span data-stu-id="872d4-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="872d4-271">ID do link</span><span class="sxs-lookup"><span data-stu-id="872d4-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="872d4-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="872d4-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="872d4-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="872d4-273">System-Only</span></span>            | <span data-ttu-id="872d4-274">True</span><span class="sxs-lookup"><span data-stu-id="872d4-274">True</span></span>                            |
| <span data-ttu-id="872d4-275">É de valor único</span><span class="sxs-lookup"><span data-stu-id="872d4-275">Is-Single-Valued</span></span>       | <span data-ttu-id="872d4-276">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-276">False</span></span>                           |
| <span data-ttu-id="872d4-277">É indexado</span><span class="sxs-lookup"><span data-stu-id="872d4-277">Is Indexed</span></span>             | <span data-ttu-id="872d4-278">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-278">False</span></span>                           |
| <span data-ttu-id="872d4-279">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="872d4-279">In Global Catalog</span></span>      | <span data-ttu-id="872d4-280">Falso</span><span class="sxs-lookup"><span data-stu-id="872d4-280">False</span></span>                           |
| <span data-ttu-id="872d4-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="872d4-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="872d4-282">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="872d4-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="872d4-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="872d4-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="872d4-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="872d4-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="872d4-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="872d4-285">Search-Flags</span></span>           | <span data-ttu-id="872d4-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="872d4-286">0x00000000</span></span>                      |
| <span data-ttu-id="872d4-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="872d4-287">System-Flags</span></span>           | <span data-ttu-id="872d4-288">0x08000014</span><span class="sxs-lookup"><span data-stu-id="872d4-288">0x08000014</span></span>                      |
| <span data-ttu-id="872d4-289">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="872d4-289">Classes used in</span></span>        | [<span data-ttu-id="872d4-290">**Início**</span><span class="sxs-lookup"><span data-stu-id="872d4-290">**Top**</span></span>](c-top.md)<br/> |



 

 





