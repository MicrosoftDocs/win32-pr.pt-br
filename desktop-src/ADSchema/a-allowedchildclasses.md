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
# <a name="allowed-child-classes-attribute"></a><span data-ttu-id="cfad1-105">Atributo allowed-Child-classes</span><span class="sxs-lookup"><span data-stu-id="cfad1-105">Allowed-Child-Classes attribute</span></span>

<span data-ttu-id="cfad1-106">Classes que podem ser contidas por uma classe.</span><span class="sxs-lookup"><span data-stu-id="cfad1-106">Classes that can be contained by a class.</span></span>



| <span data-ttu-id="cfad1-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="cfad1-107">Entry</span></span> | <span data-ttu-id="cfad1-108">Valor</span><span class="sxs-lookup"><span data-stu-id="cfad1-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="cfad1-109">CN</span><span class="sxs-lookup"><span data-stu-id="cfad1-109">CN</span></span>                | <span data-ttu-id="cfad1-110">Classes filho permitidas</span><span class="sxs-lookup"><span data-stu-id="cfad1-110">Allowed-Child-Classes</span></span>                                           |
| <span data-ttu-id="cfad1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cfad1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cfad1-112">allowedChildClasses</span><span class="sxs-lookup"><span data-stu-id="cfad1-112">allowedChildClasses</span></span>                                             |
| <span data-ttu-id="cfad1-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="cfad1-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="cfad1-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="cfad1-114">Update Privilege</span></span>  | \-                                                              |
| <span data-ttu-id="cfad1-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="cfad1-115">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="cfad1-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cfad1-116">Attribute-Id</span></span>      | <span data-ttu-id="cfad1-117">1.2.840.113556.1.4.911</span><span class="sxs-lookup"><span data-stu-id="cfad1-117">1.2.840.113556.1.4.911</span></span>                                          |
| <span data-ttu-id="cfad1-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cfad1-118">System-Id-Guid</span></span>    | <span data-ttu-id="cfad1-119">9a7ad942-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="cfad1-119">9a7ad942-ca53-11d1-bbd0-0080c76670c0</span></span>                            |
| <span data-ttu-id="cfad1-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfad1-120">Syntax</span></span>            | [<span data-ttu-id="cfad1-121">**Cadeia de caracteres (identificador de objeto)**</span><span class="sxs-lookup"><span data-stu-id="cfad1-121">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="cfad1-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="cfad1-122">Implementations</span></span>

-   [<span data-ttu-id="cfad1-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cfad1-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cfad1-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cfad1-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cfad1-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cfad1-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cfad1-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cfad1-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cfad1-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cfad1-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cfad1-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cfad1-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cfad1-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cfad1-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cfad1-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cfad1-130">Windows 2000 Server</span></span>



| <span data-ttu-id="cfad1-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="cfad1-131">Entry</span></span> | <span data-ttu-id="cfad1-132">Valor</span><span class="sxs-lookup"><span data-stu-id="cfad1-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cfad1-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="cfad1-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cfad1-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfad1-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cfad1-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfad1-135">System-Only</span></span>            | <span data-ttu-id="cfad1-136">True</span><span class="sxs-lookup"><span data-stu-id="cfad1-136">True</span></span>                            |
| <span data-ttu-id="cfad1-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cfad1-137">Is-Single-Valued</span></span>       | <span data-ttu-id="cfad1-138">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-138">False</span></span>                           |
| <span data-ttu-id="cfad1-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="cfad1-139">Is Indexed</span></span>             | <span data-ttu-id="cfad1-140">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-140">False</span></span>                           |
| <span data-ttu-id="cfad1-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cfad1-141">In Global Catalog</span></span>      | <span data-ttu-id="cfad1-142">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-142">False</span></span>                           |
| <span data-ttu-id="cfad1-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cfad1-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfad1-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cfad1-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cfad1-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfad1-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cfad1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfad1-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cfad1-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfad1-147">Search-Flags</span></span>           | <span data-ttu-id="cfad1-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfad1-148">0x00000000</span></span>                      |
| <span data-ttu-id="cfad1-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfad1-149">System-Flags</span></span>           | <span data-ttu-id="cfad1-150">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cfad1-150">0x08000014</span></span>                      |
| <span data-ttu-id="cfad1-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cfad1-151">Classes used in</span></span>        | [<span data-ttu-id="cfad1-152">**Início**</span><span class="sxs-lookup"><span data-stu-id="cfad1-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cfad1-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cfad1-153">Windows Server 2003</span></span>



| <span data-ttu-id="cfad1-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="cfad1-154">Entry</span></span> | <span data-ttu-id="cfad1-155">Valor</span><span class="sxs-lookup"><span data-stu-id="cfad1-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cfad1-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="cfad1-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cfad1-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfad1-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cfad1-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfad1-158">System-Only</span></span>            | <span data-ttu-id="cfad1-159">True</span><span class="sxs-lookup"><span data-stu-id="cfad1-159">True</span></span>                            |
| <span data-ttu-id="cfad1-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cfad1-160">Is-Single-Valued</span></span>       | <span data-ttu-id="cfad1-161">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-161">False</span></span>                           |
| <span data-ttu-id="cfad1-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="cfad1-162">Is Indexed</span></span>             | <span data-ttu-id="cfad1-163">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-163">False</span></span>                           |
| <span data-ttu-id="cfad1-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cfad1-164">In Global Catalog</span></span>      | <span data-ttu-id="cfad1-165">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-165">False</span></span>                           |
| <span data-ttu-id="cfad1-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cfad1-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfad1-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cfad1-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cfad1-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfad1-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cfad1-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfad1-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cfad1-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfad1-170">Search-Flags</span></span>           | <span data-ttu-id="cfad1-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfad1-171">0x00000000</span></span>                      |
| <span data-ttu-id="cfad1-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfad1-172">System-Flags</span></span>           | <span data-ttu-id="cfad1-173">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cfad1-173">0x08000014</span></span>                      |
| <span data-ttu-id="cfad1-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cfad1-174">Classes used in</span></span>        | [<span data-ttu-id="cfad1-175">**Início**</span><span class="sxs-lookup"><span data-stu-id="cfad1-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cfad1-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="cfad1-176">ADAM</span></span>



| <span data-ttu-id="cfad1-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="cfad1-177">Entry</span></span> | <span data-ttu-id="cfad1-178">Valor</span><span class="sxs-lookup"><span data-stu-id="cfad1-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cfad1-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="cfad1-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cfad1-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfad1-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cfad1-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfad1-181">System-Only</span></span>            | <span data-ttu-id="cfad1-182">True</span><span class="sxs-lookup"><span data-stu-id="cfad1-182">True</span></span>                            |
| <span data-ttu-id="cfad1-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cfad1-183">Is-Single-Valued</span></span>       | <span data-ttu-id="cfad1-184">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-184">False</span></span>                           |
| <span data-ttu-id="cfad1-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="cfad1-185">Is Indexed</span></span>             | <span data-ttu-id="cfad1-186">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-186">False</span></span>                           |
| <span data-ttu-id="cfad1-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cfad1-187">In Global Catalog</span></span>      | <span data-ttu-id="cfad1-188">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-188">False</span></span>                           |
| <span data-ttu-id="cfad1-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cfad1-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfad1-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cfad1-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cfad1-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfad1-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cfad1-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfad1-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cfad1-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfad1-193">Search-Flags</span></span>           | <span data-ttu-id="cfad1-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfad1-194">0x00000000</span></span>                      |
| <span data-ttu-id="cfad1-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfad1-195">System-Flags</span></span>           | <span data-ttu-id="cfad1-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cfad1-196">0x08000014</span></span>                      |
| <span data-ttu-id="cfad1-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cfad1-197">Classes used in</span></span>        | [<span data-ttu-id="cfad1-198">**Início**</span><span class="sxs-lookup"><span data-stu-id="cfad1-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cfad1-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cfad1-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cfad1-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="cfad1-200">Entry</span></span> | <span data-ttu-id="cfad1-201">Valor</span><span class="sxs-lookup"><span data-stu-id="cfad1-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cfad1-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="cfad1-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cfad1-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfad1-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cfad1-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfad1-204">System-Only</span></span>            | <span data-ttu-id="cfad1-205">True</span><span class="sxs-lookup"><span data-stu-id="cfad1-205">True</span></span>                            |
| <span data-ttu-id="cfad1-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cfad1-206">Is-Single-Valued</span></span>       | <span data-ttu-id="cfad1-207">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-207">False</span></span>                           |
| <span data-ttu-id="cfad1-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="cfad1-208">Is Indexed</span></span>             | <span data-ttu-id="cfad1-209">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-209">False</span></span>                           |
| <span data-ttu-id="cfad1-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cfad1-210">In Global Catalog</span></span>      | <span data-ttu-id="cfad1-211">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-211">False</span></span>                           |
| <span data-ttu-id="cfad1-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cfad1-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfad1-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cfad1-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cfad1-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfad1-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cfad1-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfad1-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cfad1-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfad1-216">Search-Flags</span></span>           | <span data-ttu-id="cfad1-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfad1-217">0x00000000</span></span>                      |
| <span data-ttu-id="cfad1-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfad1-218">System-Flags</span></span>           | <span data-ttu-id="cfad1-219">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cfad1-219">0x08000014</span></span>                      |
| <span data-ttu-id="cfad1-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cfad1-220">Classes used in</span></span>        | [<span data-ttu-id="cfad1-221">**Início**</span><span class="sxs-lookup"><span data-stu-id="cfad1-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cfad1-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfad1-222">Windows Server 2008</span></span>



| <span data-ttu-id="cfad1-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="cfad1-223">Entry</span></span> | <span data-ttu-id="cfad1-224">Valor</span><span class="sxs-lookup"><span data-stu-id="cfad1-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cfad1-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="cfad1-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cfad1-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfad1-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cfad1-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfad1-227">System-Only</span></span>            | <span data-ttu-id="cfad1-228">True</span><span class="sxs-lookup"><span data-stu-id="cfad1-228">True</span></span>                            |
| <span data-ttu-id="cfad1-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cfad1-229">Is-Single-Valued</span></span>       | <span data-ttu-id="cfad1-230">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-230">False</span></span>                           |
| <span data-ttu-id="cfad1-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="cfad1-231">Is Indexed</span></span>             | <span data-ttu-id="cfad1-232">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-232">False</span></span>                           |
| <span data-ttu-id="cfad1-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cfad1-233">In Global Catalog</span></span>      | <span data-ttu-id="cfad1-234">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-234">False</span></span>                           |
| <span data-ttu-id="cfad1-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cfad1-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfad1-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cfad1-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cfad1-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfad1-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cfad1-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfad1-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cfad1-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfad1-239">Search-Flags</span></span>           | <span data-ttu-id="cfad1-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfad1-240">0x00000000</span></span>                      |
| <span data-ttu-id="cfad1-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfad1-241">System-Flags</span></span>           | <span data-ttu-id="cfad1-242">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cfad1-242">0x08000014</span></span>                      |
| <span data-ttu-id="cfad1-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cfad1-243">Classes used in</span></span>        | [<span data-ttu-id="cfad1-244">**Início**</span><span class="sxs-lookup"><span data-stu-id="cfad1-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cfad1-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cfad1-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cfad1-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="cfad1-246">Entry</span></span> | <span data-ttu-id="cfad1-247">Valor</span><span class="sxs-lookup"><span data-stu-id="cfad1-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cfad1-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="cfad1-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cfad1-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfad1-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cfad1-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfad1-250">System-Only</span></span>            | <span data-ttu-id="cfad1-251">True</span><span class="sxs-lookup"><span data-stu-id="cfad1-251">True</span></span>                            |
| <span data-ttu-id="cfad1-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cfad1-252">Is-Single-Valued</span></span>       | <span data-ttu-id="cfad1-253">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-253">False</span></span>                           |
| <span data-ttu-id="cfad1-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="cfad1-254">Is Indexed</span></span>             | <span data-ttu-id="cfad1-255">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-255">False</span></span>                           |
| <span data-ttu-id="cfad1-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cfad1-256">In Global Catalog</span></span>      | <span data-ttu-id="cfad1-257">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-257">False</span></span>                           |
| <span data-ttu-id="cfad1-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cfad1-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfad1-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cfad1-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cfad1-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfad1-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cfad1-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfad1-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cfad1-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfad1-262">Search-Flags</span></span>           | <span data-ttu-id="cfad1-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfad1-263">0x00000000</span></span>                      |
| <span data-ttu-id="cfad1-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfad1-264">System-Flags</span></span>           | <span data-ttu-id="cfad1-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cfad1-265">0x08000014</span></span>                      |
| <span data-ttu-id="cfad1-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cfad1-266">Classes used in</span></span>        | [<span data-ttu-id="cfad1-267">**Início**</span><span class="sxs-lookup"><span data-stu-id="cfad1-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cfad1-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cfad1-268">Windows Server 2012</span></span>



| <span data-ttu-id="cfad1-269">Entrada</span><span class="sxs-lookup"><span data-stu-id="cfad1-269">Entry</span></span> | <span data-ttu-id="cfad1-270">Valor</span><span class="sxs-lookup"><span data-stu-id="cfad1-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cfad1-271">ID do link</span><span class="sxs-lookup"><span data-stu-id="cfad1-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cfad1-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfad1-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cfad1-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfad1-273">System-Only</span></span>            | <span data-ttu-id="cfad1-274">True</span><span class="sxs-lookup"><span data-stu-id="cfad1-274">True</span></span>                            |
| <span data-ttu-id="cfad1-275">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cfad1-275">Is-Single-Valued</span></span>       | <span data-ttu-id="cfad1-276">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-276">False</span></span>                           |
| <span data-ttu-id="cfad1-277">É indexado</span><span class="sxs-lookup"><span data-stu-id="cfad1-277">Is Indexed</span></span>             | <span data-ttu-id="cfad1-278">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-278">False</span></span>                           |
| <span data-ttu-id="cfad1-279">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cfad1-279">In Global Catalog</span></span>      | <span data-ttu-id="cfad1-280">Falso</span><span class="sxs-lookup"><span data-stu-id="cfad1-280">False</span></span>                           |
| <span data-ttu-id="cfad1-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cfad1-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfad1-282">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cfad1-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cfad1-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfad1-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cfad1-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfad1-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cfad1-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfad1-285">Search-Flags</span></span>           | <span data-ttu-id="cfad1-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfad1-286">0x00000000</span></span>                      |
| <span data-ttu-id="cfad1-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfad1-287">System-Flags</span></span>           | <span data-ttu-id="cfad1-288">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cfad1-288">0x08000014</span></span>                      |
| <span data-ttu-id="cfad1-289">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cfad1-289">Classes used in</span></span>        | [<span data-ttu-id="cfad1-290">**Início**</span><span class="sxs-lookup"><span data-stu-id="cfad1-290">**Top**</span></span>](c-top.md)<br/> |



 

 





