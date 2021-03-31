---
title: Object-Class atributo
description: A lista de classes da qual essa classe é derivada.
ms.assetid: def98723-2d8a-49ea-84f8-afe6ff9cdfd9
ms.tgt_platform: multiple
keywords:
- Esquema de Object-Class do atributo AD
- atributo objectClass do esquema do AD
topic_type:
- apiref
api_name:
- Object-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851d48bcbcc40640af3ee555c343feaab05edf6b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087015"
---
# <a name="object-class-attribute"></a><span data-ttu-id="65001-105">Object-Class atributo</span><span class="sxs-lookup"><span data-stu-id="65001-105">Object-Class attribute</span></span>

<span data-ttu-id="65001-106">A lista de classes da qual essa classe é derivada.</span><span class="sxs-lookup"><span data-stu-id="65001-106">The list of classes from which this class is derived.</span></span>



| <span data-ttu-id="65001-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="65001-107">Entry</span></span> | <span data-ttu-id="65001-108">Valor</span><span class="sxs-lookup"><span data-stu-id="65001-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="65001-109">CN</span><span class="sxs-lookup"><span data-stu-id="65001-109">CN</span></span>                | <span data-ttu-id="65001-110">Object-Class</span><span class="sxs-lookup"><span data-stu-id="65001-110">Object-Class</span></span>                                                    |
| <span data-ttu-id="65001-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="65001-111">Ldap-Display-Name</span></span> | <span data-ttu-id="65001-112">objectClass</span><span class="sxs-lookup"><span data-stu-id="65001-112">objectClass</span></span>                                                     |
| <span data-ttu-id="65001-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="65001-113">Size</span></span>              | <span data-ttu-id="65001-114">Cerca de 20 bytes em média.</span><span class="sxs-lookup"><span data-stu-id="65001-114">About 20 bytes on average.</span></span>                                      |
| <span data-ttu-id="65001-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="65001-115">Update Privilege</span></span>  | <span data-ttu-id="65001-116">O designer do objeto definiria esse valor.</span><span class="sxs-lookup"><span data-stu-id="65001-116">The designer of the object would set this value.</span></span>                |
| <span data-ttu-id="65001-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="65001-117">Update Frequency</span></span>  | <span data-ttu-id="65001-118">Esse valor nunca deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="65001-118">This value should never change.</span></span>                                 |
| <span data-ttu-id="65001-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="65001-119">Attribute-Id</span></span>      | <span data-ttu-id="65001-120">2.5.4.0</span><span class="sxs-lookup"><span data-stu-id="65001-120">2.5.4.0</span></span>                                                         |
| <span data-ttu-id="65001-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="65001-121">System-Id-Guid</span></span>    | <span data-ttu-id="65001-122">bf9679e5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="65001-122">bf9679e5-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="65001-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="65001-123">Syntax</span></span>            | [<span data-ttu-id="65001-124">**Cadeia de caracteres (identificador de objeto)**</span><span class="sxs-lookup"><span data-stu-id="65001-124">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="65001-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="65001-125">Implementations</span></span>

-   [<span data-ttu-id="65001-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="65001-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="65001-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="65001-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="65001-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="65001-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="65001-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="65001-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="65001-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="65001-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="65001-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="65001-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="65001-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="65001-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="65001-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="65001-133">Windows 2000 Server</span></span>



| <span data-ttu-id="65001-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="65001-134">Entry</span></span> | <span data-ttu-id="65001-135">Valor</span><span class="sxs-lookup"><span data-stu-id="65001-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65001-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="65001-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65001-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65001-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="65001-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="65001-138">System-Only</span></span>            | <span data-ttu-id="65001-139">True</span><span class="sxs-lookup"><span data-stu-id="65001-139">True</span></span>                            |
| <span data-ttu-id="65001-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="65001-140">Is-Single-Valued</span></span>       | <span data-ttu-id="65001-141">Falso</span><span class="sxs-lookup"><span data-stu-id="65001-141">False</span></span>                           |
| <span data-ttu-id="65001-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="65001-142">Is Indexed</span></span>             | <span data-ttu-id="65001-143">Falso</span><span class="sxs-lookup"><span data-stu-id="65001-143">False</span></span>                           |
| <span data-ttu-id="65001-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="65001-144">In Global Catalog</span></span>      | <span data-ttu-id="65001-145">True</span><span class="sxs-lookup"><span data-stu-id="65001-145">True</span></span>                            |
| <span data-ttu-id="65001-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="65001-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="65001-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="65001-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65001-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65001-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65001-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65001-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65001-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65001-150">Search-Flags</span></span>           | <span data-ttu-id="65001-151">0x00000008</span><span class="sxs-lookup"><span data-stu-id="65001-151">0x00000008</span></span>                      |
| <span data-ttu-id="65001-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65001-152">System-Flags</span></span>           | <span data-ttu-id="65001-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="65001-153">0x00000012</span></span>                      |
| <span data-ttu-id="65001-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="65001-154">Classes used in</span></span>        | [<span data-ttu-id="65001-155">**Início**</span><span class="sxs-lookup"><span data-stu-id="65001-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="65001-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="65001-156">Windows Server 2003</span></span>



| <span data-ttu-id="65001-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="65001-157">Entry</span></span> | <span data-ttu-id="65001-158">Valor</span><span class="sxs-lookup"><span data-stu-id="65001-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65001-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="65001-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65001-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65001-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="65001-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="65001-161">System-Only</span></span>            | <span data-ttu-id="65001-162">True</span><span class="sxs-lookup"><span data-stu-id="65001-162">True</span></span>                            |
| <span data-ttu-id="65001-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="65001-163">Is-Single-Valued</span></span>       | <span data-ttu-id="65001-164">Falso</span><span class="sxs-lookup"><span data-stu-id="65001-164">False</span></span>                           |
| <span data-ttu-id="65001-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="65001-165">Is Indexed</span></span>             | <span data-ttu-id="65001-166">Falso</span><span class="sxs-lookup"><span data-stu-id="65001-166">False</span></span>                           |
| <span data-ttu-id="65001-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="65001-167">In Global Catalog</span></span>      | <span data-ttu-id="65001-168">True</span><span class="sxs-lookup"><span data-stu-id="65001-168">True</span></span>                            |
| <span data-ttu-id="65001-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="65001-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="65001-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="65001-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65001-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65001-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65001-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65001-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65001-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65001-173">Search-Flags</span></span>           | <span data-ttu-id="65001-174">0x00000008</span><span class="sxs-lookup"><span data-stu-id="65001-174">0x00000008</span></span>                      |
| <span data-ttu-id="65001-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65001-175">System-Flags</span></span>           | <span data-ttu-id="65001-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="65001-176">0x00000012</span></span>                      |
| <span data-ttu-id="65001-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="65001-177">Classes used in</span></span>        | [<span data-ttu-id="65001-178">**Início**</span><span class="sxs-lookup"><span data-stu-id="65001-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="65001-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="65001-179">ADAM</span></span>



| <span data-ttu-id="65001-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="65001-180">Entry</span></span> | <span data-ttu-id="65001-181">Valor</span><span class="sxs-lookup"><span data-stu-id="65001-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65001-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="65001-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65001-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65001-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="65001-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="65001-184">System-Only</span></span>            | <span data-ttu-id="65001-185">True</span><span class="sxs-lookup"><span data-stu-id="65001-185">True</span></span>                            |
| <span data-ttu-id="65001-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="65001-186">Is-Single-Valued</span></span>       | <span data-ttu-id="65001-187">Falso</span><span class="sxs-lookup"><span data-stu-id="65001-187">False</span></span>                           |
| <span data-ttu-id="65001-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="65001-188">Is Indexed</span></span>             | <span data-ttu-id="65001-189">Falso</span><span class="sxs-lookup"><span data-stu-id="65001-189">False</span></span>                           |
| <span data-ttu-id="65001-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="65001-190">In Global Catalog</span></span>      | <span data-ttu-id="65001-191">True</span><span class="sxs-lookup"><span data-stu-id="65001-191">True</span></span>                            |
| <span data-ttu-id="65001-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="65001-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="65001-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="65001-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65001-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65001-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65001-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65001-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65001-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65001-196">Search-Flags</span></span>           | <span data-ttu-id="65001-197">0x00000008</span><span class="sxs-lookup"><span data-stu-id="65001-197">0x00000008</span></span>                      |
| <span data-ttu-id="65001-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65001-198">System-Flags</span></span>           | <span data-ttu-id="65001-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="65001-199">0x00000012</span></span>                      |
| <span data-ttu-id="65001-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="65001-200">Classes used in</span></span>        | [<span data-ttu-id="65001-201">**Início**</span><span class="sxs-lookup"><span data-stu-id="65001-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="65001-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="65001-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="65001-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="65001-203">Entry</span></span> | <span data-ttu-id="65001-204">Valor</span><span class="sxs-lookup"><span data-stu-id="65001-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65001-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="65001-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65001-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65001-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="65001-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="65001-207">System-Only</span></span>            | <span data-ttu-id="65001-208">True</span><span class="sxs-lookup"><span data-stu-id="65001-208">True</span></span>                            |
| <span data-ttu-id="65001-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="65001-209">Is-Single-Valued</span></span>       | <span data-ttu-id="65001-210">Falso</span><span class="sxs-lookup"><span data-stu-id="65001-210">False</span></span>                           |
| <span data-ttu-id="65001-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="65001-211">Is Indexed</span></span>             | <span data-ttu-id="65001-212">Falso</span><span class="sxs-lookup"><span data-stu-id="65001-212">False</span></span>                           |
| <span data-ttu-id="65001-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="65001-213">In Global Catalog</span></span>      | <span data-ttu-id="65001-214">True</span><span class="sxs-lookup"><span data-stu-id="65001-214">True</span></span>                            |
| <span data-ttu-id="65001-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="65001-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="65001-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="65001-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65001-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65001-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65001-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65001-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65001-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65001-219">Search-Flags</span></span>           | <span data-ttu-id="65001-220">0x00000008</span><span class="sxs-lookup"><span data-stu-id="65001-220">0x00000008</span></span>                      |
| <span data-ttu-id="65001-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65001-221">System-Flags</span></span>           | <span data-ttu-id="65001-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="65001-222">0x00000012</span></span>                      |
| <span data-ttu-id="65001-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="65001-223">Classes used in</span></span>        | [<span data-ttu-id="65001-224">**Início**</span><span class="sxs-lookup"><span data-stu-id="65001-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="65001-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65001-225">Windows Server 2008</span></span>



| <span data-ttu-id="65001-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="65001-226">Entry</span></span> | <span data-ttu-id="65001-227">Valor</span><span class="sxs-lookup"><span data-stu-id="65001-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65001-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="65001-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65001-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65001-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="65001-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="65001-230">System-Only</span></span>            | <span data-ttu-id="65001-231">True</span><span class="sxs-lookup"><span data-stu-id="65001-231">True</span></span>                            |
| <span data-ttu-id="65001-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="65001-232">Is-Single-Valued</span></span>       | <span data-ttu-id="65001-233">Falso</span><span class="sxs-lookup"><span data-stu-id="65001-233">False</span></span>                           |
| <span data-ttu-id="65001-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="65001-234">Is Indexed</span></span>             | <span data-ttu-id="65001-235">True</span><span class="sxs-lookup"><span data-stu-id="65001-235">True</span></span>                            |
| <span data-ttu-id="65001-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="65001-236">In Global Catalog</span></span>      | <span data-ttu-id="65001-237">True</span><span class="sxs-lookup"><span data-stu-id="65001-237">True</span></span>                            |
| <span data-ttu-id="65001-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="65001-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="65001-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="65001-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65001-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65001-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65001-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65001-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65001-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65001-242">Search-Flags</span></span>           | <span data-ttu-id="65001-243">0x00000009</span><span class="sxs-lookup"><span data-stu-id="65001-243">0x00000009</span></span>                      |
| <span data-ttu-id="65001-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65001-244">System-Flags</span></span>           | <span data-ttu-id="65001-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="65001-245">0x00000012</span></span>                      |
| <span data-ttu-id="65001-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="65001-246">Classes used in</span></span>        | [<span data-ttu-id="65001-247">**Início**</span><span class="sxs-lookup"><span data-stu-id="65001-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="65001-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="65001-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="65001-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="65001-249">Entry</span></span> | <span data-ttu-id="65001-250">Valor</span><span class="sxs-lookup"><span data-stu-id="65001-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65001-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="65001-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65001-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65001-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="65001-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="65001-253">System-Only</span></span>            | <span data-ttu-id="65001-254">True</span><span class="sxs-lookup"><span data-stu-id="65001-254">True</span></span>                            |
| <span data-ttu-id="65001-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="65001-255">Is-Single-Valued</span></span>       | <span data-ttu-id="65001-256">Falso</span><span class="sxs-lookup"><span data-stu-id="65001-256">False</span></span>                           |
| <span data-ttu-id="65001-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="65001-257">Is Indexed</span></span>             | <span data-ttu-id="65001-258">True</span><span class="sxs-lookup"><span data-stu-id="65001-258">True</span></span>                            |
| <span data-ttu-id="65001-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="65001-259">In Global Catalog</span></span>      | <span data-ttu-id="65001-260">True</span><span class="sxs-lookup"><span data-stu-id="65001-260">True</span></span>                            |
| <span data-ttu-id="65001-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="65001-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="65001-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="65001-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65001-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65001-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65001-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65001-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65001-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65001-265">Search-Flags</span></span>           | <span data-ttu-id="65001-266">0x00000009</span><span class="sxs-lookup"><span data-stu-id="65001-266">0x00000009</span></span>                      |
| <span data-ttu-id="65001-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65001-267">System-Flags</span></span>           | <span data-ttu-id="65001-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="65001-268">0x00000012</span></span>                      |
| <span data-ttu-id="65001-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="65001-269">Classes used in</span></span>        | [<span data-ttu-id="65001-270">**Início**</span><span class="sxs-lookup"><span data-stu-id="65001-270">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="65001-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="65001-271">Windows Server 2012</span></span>



| <span data-ttu-id="65001-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="65001-272">Entry</span></span> | <span data-ttu-id="65001-273">Valor</span><span class="sxs-lookup"><span data-stu-id="65001-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65001-274">ID do link</span><span class="sxs-lookup"><span data-stu-id="65001-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65001-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65001-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="65001-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="65001-276">System-Only</span></span>            | <span data-ttu-id="65001-277">True</span><span class="sxs-lookup"><span data-stu-id="65001-277">True</span></span>                            |
| <span data-ttu-id="65001-278">É de valor único</span><span class="sxs-lookup"><span data-stu-id="65001-278">Is-Single-Valued</span></span>       | <span data-ttu-id="65001-279">Falso</span><span class="sxs-lookup"><span data-stu-id="65001-279">False</span></span>                           |
| <span data-ttu-id="65001-280">É indexado</span><span class="sxs-lookup"><span data-stu-id="65001-280">Is Indexed</span></span>             | <span data-ttu-id="65001-281">True</span><span class="sxs-lookup"><span data-stu-id="65001-281">True</span></span>                            |
| <span data-ttu-id="65001-282">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="65001-282">In Global Catalog</span></span>      | <span data-ttu-id="65001-283">True</span><span class="sxs-lookup"><span data-stu-id="65001-283">True</span></span>                            |
| <span data-ttu-id="65001-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="65001-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="65001-285">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="65001-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65001-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65001-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65001-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65001-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65001-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65001-288">Search-Flags</span></span>           | <span data-ttu-id="65001-289">0x00000009</span><span class="sxs-lookup"><span data-stu-id="65001-289">0x00000009</span></span>                      |
| <span data-ttu-id="65001-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65001-290">System-Flags</span></span>           | <span data-ttu-id="65001-291">0x00000012</span><span class="sxs-lookup"><span data-stu-id="65001-291">0x00000012</span></span>                      |
| <span data-ttu-id="65001-292">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="65001-292">Classes used in</span></span>        | [<span data-ttu-id="65001-293">**Início**</span><span class="sxs-lookup"><span data-stu-id="65001-293">**Top**</span></span>](c-top.md)<br/> |



 

 





