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
# <a name="object-class-attribute"></a><span data-ttu-id="4ea0b-105">Object-Class atributo</span><span class="sxs-lookup"><span data-stu-id="4ea0b-105">Object-Class attribute</span></span>

<span data-ttu-id="4ea0b-106">A lista de classes da qual essa classe é derivada.</span><span class="sxs-lookup"><span data-stu-id="4ea0b-106">The list of classes from which this class is derived.</span></span>



| <span data-ttu-id="4ea0b-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ea0b-107">Entry</span></span> | <span data-ttu-id="4ea0b-108">Valor</span><span class="sxs-lookup"><span data-stu-id="4ea0b-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4ea0b-109">CN</span><span class="sxs-lookup"><span data-stu-id="4ea0b-109">CN</span></span>                | <span data-ttu-id="4ea0b-110">Object-Class</span><span class="sxs-lookup"><span data-stu-id="4ea0b-110">Object-Class</span></span>                                                    |
| <span data-ttu-id="4ea0b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4ea0b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4ea0b-112">objectClass</span><span class="sxs-lookup"><span data-stu-id="4ea0b-112">objectClass</span></span>                                                     |
| <span data-ttu-id="4ea0b-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="4ea0b-113">Size</span></span>              | <span data-ttu-id="4ea0b-114">Cerca de 20 bytes em média.</span><span class="sxs-lookup"><span data-stu-id="4ea0b-114">About 20 bytes on average.</span></span>                                      |
| <span data-ttu-id="4ea0b-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="4ea0b-115">Update Privilege</span></span>  | <span data-ttu-id="4ea0b-116">O designer do objeto definiria esse valor.</span><span class="sxs-lookup"><span data-stu-id="4ea0b-116">The designer of the object would set this value.</span></span>                |
| <span data-ttu-id="4ea0b-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="4ea0b-117">Update Frequency</span></span>  | <span data-ttu-id="4ea0b-118">Esse valor nunca deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="4ea0b-118">This value should never change.</span></span>                                 |
| <span data-ttu-id="4ea0b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4ea0b-119">Attribute-Id</span></span>      | <span data-ttu-id="4ea0b-120">2.5.4.0</span><span class="sxs-lookup"><span data-stu-id="4ea0b-120">2.5.4.0</span></span>                                                         |
| <span data-ttu-id="4ea0b-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4ea0b-121">System-Id-Guid</span></span>    | <span data-ttu-id="4ea0b-122">bf9679e5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="4ea0b-122">bf9679e5-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="4ea0b-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ea0b-123">Syntax</span></span>            | [<span data-ttu-id="4ea0b-124">**Cadeia de caracteres (identificador de objeto)**</span><span class="sxs-lookup"><span data-stu-id="4ea0b-124">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="4ea0b-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="4ea0b-125">Implementations</span></span>

-   [<span data-ttu-id="4ea0b-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4ea0b-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4ea0b-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4ea0b-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4ea0b-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="4ea0b-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4ea0b-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4ea0b-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4ea0b-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4ea0b-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4ea0b-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4ea0b-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4ea0b-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4ea0b-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4ea0b-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4ea0b-133">Windows 2000 Server</span></span>



| <span data-ttu-id="4ea0b-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ea0b-134">Entry</span></span> | <span data-ttu-id="4ea0b-135">Valor</span><span class="sxs-lookup"><span data-stu-id="4ea0b-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4ea0b-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="4ea0b-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4ea0b-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ea0b-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="4ea0b-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ea0b-138">System-Only</span></span>            | <span data-ttu-id="4ea0b-139">True</span><span class="sxs-lookup"><span data-stu-id="4ea0b-139">True</span></span>                            |
| <span data-ttu-id="4ea0b-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4ea0b-140">Is-Single-Valued</span></span>       | <span data-ttu-id="4ea0b-141">Falso</span><span class="sxs-lookup"><span data-stu-id="4ea0b-141">False</span></span>                           |
| <span data-ttu-id="4ea0b-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="4ea0b-142">Is Indexed</span></span>             | <span data-ttu-id="4ea0b-143">Falso</span><span class="sxs-lookup"><span data-stu-id="4ea0b-143">False</span></span>                           |
| <span data-ttu-id="4ea0b-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4ea0b-144">In Global Catalog</span></span>      | <span data-ttu-id="4ea0b-145">True</span><span class="sxs-lookup"><span data-stu-id="4ea0b-145">True</span></span>                            |
| <span data-ttu-id="4ea0b-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4ea0b-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ea0b-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4ea0b-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4ea0b-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ea0b-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4ea0b-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ea0b-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4ea0b-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ea0b-150">Search-Flags</span></span>           | <span data-ttu-id="4ea0b-151">0x00000008</span><span class="sxs-lookup"><span data-stu-id="4ea0b-151">0x00000008</span></span>                      |
| <span data-ttu-id="4ea0b-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ea0b-152">System-Flags</span></span>           | <span data-ttu-id="4ea0b-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="4ea0b-153">0x00000012</span></span>                      |
| <span data-ttu-id="4ea0b-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4ea0b-154">Classes used in</span></span>        | [<span data-ttu-id="4ea0b-155">**Início**</span><span class="sxs-lookup"><span data-stu-id="4ea0b-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4ea0b-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4ea0b-156">Windows Server 2003</span></span>



| <span data-ttu-id="4ea0b-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ea0b-157">Entry</span></span> | <span data-ttu-id="4ea0b-158">Valor</span><span class="sxs-lookup"><span data-stu-id="4ea0b-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4ea0b-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="4ea0b-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4ea0b-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ea0b-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="4ea0b-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ea0b-161">System-Only</span></span>            | <span data-ttu-id="4ea0b-162">True</span><span class="sxs-lookup"><span data-stu-id="4ea0b-162">True</span></span>                            |
| <span data-ttu-id="4ea0b-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4ea0b-163">Is-Single-Valued</span></span>       | <span data-ttu-id="4ea0b-164">Falso</span><span class="sxs-lookup"><span data-stu-id="4ea0b-164">False</span></span>                           |
| <span data-ttu-id="4ea0b-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="4ea0b-165">Is Indexed</span></span>             | <span data-ttu-id="4ea0b-166">Falso</span><span class="sxs-lookup"><span data-stu-id="4ea0b-166">False</span></span>                           |
| <span data-ttu-id="4ea0b-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4ea0b-167">In Global Catalog</span></span>      | <span data-ttu-id="4ea0b-168">True</span><span class="sxs-lookup"><span data-stu-id="4ea0b-168">True</span></span>                            |
| <span data-ttu-id="4ea0b-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4ea0b-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ea0b-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4ea0b-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4ea0b-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ea0b-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4ea0b-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ea0b-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4ea0b-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ea0b-173">Search-Flags</span></span>           | <span data-ttu-id="4ea0b-174">0x00000008</span><span class="sxs-lookup"><span data-stu-id="4ea0b-174">0x00000008</span></span>                      |
| <span data-ttu-id="4ea0b-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ea0b-175">System-Flags</span></span>           | <span data-ttu-id="4ea0b-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="4ea0b-176">0x00000012</span></span>                      |
| <span data-ttu-id="4ea0b-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4ea0b-177">Classes used in</span></span>        | [<span data-ttu-id="4ea0b-178">**Início**</span><span class="sxs-lookup"><span data-stu-id="4ea0b-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4ea0b-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="4ea0b-179">ADAM</span></span>



| <span data-ttu-id="4ea0b-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ea0b-180">Entry</span></span> | <span data-ttu-id="4ea0b-181">Valor</span><span class="sxs-lookup"><span data-stu-id="4ea0b-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4ea0b-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="4ea0b-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4ea0b-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ea0b-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="4ea0b-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ea0b-184">System-Only</span></span>            | <span data-ttu-id="4ea0b-185">True</span><span class="sxs-lookup"><span data-stu-id="4ea0b-185">True</span></span>                            |
| <span data-ttu-id="4ea0b-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4ea0b-186">Is-Single-Valued</span></span>       | <span data-ttu-id="4ea0b-187">Falso</span><span class="sxs-lookup"><span data-stu-id="4ea0b-187">False</span></span>                           |
| <span data-ttu-id="4ea0b-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="4ea0b-188">Is Indexed</span></span>             | <span data-ttu-id="4ea0b-189">Falso</span><span class="sxs-lookup"><span data-stu-id="4ea0b-189">False</span></span>                           |
| <span data-ttu-id="4ea0b-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4ea0b-190">In Global Catalog</span></span>      | <span data-ttu-id="4ea0b-191">True</span><span class="sxs-lookup"><span data-stu-id="4ea0b-191">True</span></span>                            |
| <span data-ttu-id="4ea0b-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4ea0b-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ea0b-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4ea0b-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4ea0b-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ea0b-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4ea0b-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ea0b-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4ea0b-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ea0b-196">Search-Flags</span></span>           | <span data-ttu-id="4ea0b-197">0x00000008</span><span class="sxs-lookup"><span data-stu-id="4ea0b-197">0x00000008</span></span>                      |
| <span data-ttu-id="4ea0b-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ea0b-198">System-Flags</span></span>           | <span data-ttu-id="4ea0b-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="4ea0b-199">0x00000012</span></span>                      |
| <span data-ttu-id="4ea0b-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4ea0b-200">Classes used in</span></span>        | [<span data-ttu-id="4ea0b-201">**Início**</span><span class="sxs-lookup"><span data-stu-id="4ea0b-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4ea0b-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4ea0b-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4ea0b-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ea0b-203">Entry</span></span> | <span data-ttu-id="4ea0b-204">Valor</span><span class="sxs-lookup"><span data-stu-id="4ea0b-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4ea0b-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="4ea0b-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4ea0b-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ea0b-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="4ea0b-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ea0b-207">System-Only</span></span>            | <span data-ttu-id="4ea0b-208">True</span><span class="sxs-lookup"><span data-stu-id="4ea0b-208">True</span></span>                            |
| <span data-ttu-id="4ea0b-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4ea0b-209">Is-Single-Valued</span></span>       | <span data-ttu-id="4ea0b-210">Falso</span><span class="sxs-lookup"><span data-stu-id="4ea0b-210">False</span></span>                           |
| <span data-ttu-id="4ea0b-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="4ea0b-211">Is Indexed</span></span>             | <span data-ttu-id="4ea0b-212">Falso</span><span class="sxs-lookup"><span data-stu-id="4ea0b-212">False</span></span>                           |
| <span data-ttu-id="4ea0b-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4ea0b-213">In Global Catalog</span></span>      | <span data-ttu-id="4ea0b-214">True</span><span class="sxs-lookup"><span data-stu-id="4ea0b-214">True</span></span>                            |
| <span data-ttu-id="4ea0b-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4ea0b-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ea0b-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4ea0b-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4ea0b-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ea0b-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4ea0b-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ea0b-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4ea0b-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ea0b-219">Search-Flags</span></span>           | <span data-ttu-id="4ea0b-220">0x00000008</span><span class="sxs-lookup"><span data-stu-id="4ea0b-220">0x00000008</span></span>                      |
| <span data-ttu-id="4ea0b-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ea0b-221">System-Flags</span></span>           | <span data-ttu-id="4ea0b-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="4ea0b-222">0x00000012</span></span>                      |
| <span data-ttu-id="4ea0b-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4ea0b-223">Classes used in</span></span>        | [<span data-ttu-id="4ea0b-224">**Início**</span><span class="sxs-lookup"><span data-stu-id="4ea0b-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4ea0b-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ea0b-225">Windows Server 2008</span></span>



| <span data-ttu-id="4ea0b-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ea0b-226">Entry</span></span> | <span data-ttu-id="4ea0b-227">Valor</span><span class="sxs-lookup"><span data-stu-id="4ea0b-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4ea0b-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="4ea0b-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4ea0b-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ea0b-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="4ea0b-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ea0b-230">System-Only</span></span>            | <span data-ttu-id="4ea0b-231">True</span><span class="sxs-lookup"><span data-stu-id="4ea0b-231">True</span></span>                            |
| <span data-ttu-id="4ea0b-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4ea0b-232">Is-Single-Valued</span></span>       | <span data-ttu-id="4ea0b-233">Falso</span><span class="sxs-lookup"><span data-stu-id="4ea0b-233">False</span></span>                           |
| <span data-ttu-id="4ea0b-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="4ea0b-234">Is Indexed</span></span>             | <span data-ttu-id="4ea0b-235">True</span><span class="sxs-lookup"><span data-stu-id="4ea0b-235">True</span></span>                            |
| <span data-ttu-id="4ea0b-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4ea0b-236">In Global Catalog</span></span>      | <span data-ttu-id="4ea0b-237">True</span><span class="sxs-lookup"><span data-stu-id="4ea0b-237">True</span></span>                            |
| <span data-ttu-id="4ea0b-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4ea0b-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ea0b-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4ea0b-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4ea0b-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ea0b-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4ea0b-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ea0b-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4ea0b-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ea0b-242">Search-Flags</span></span>           | <span data-ttu-id="4ea0b-243">0x00000009</span><span class="sxs-lookup"><span data-stu-id="4ea0b-243">0x00000009</span></span>                      |
| <span data-ttu-id="4ea0b-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ea0b-244">System-Flags</span></span>           | <span data-ttu-id="4ea0b-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="4ea0b-245">0x00000012</span></span>                      |
| <span data-ttu-id="4ea0b-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4ea0b-246">Classes used in</span></span>        | [<span data-ttu-id="4ea0b-247">**Início**</span><span class="sxs-lookup"><span data-stu-id="4ea0b-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4ea0b-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4ea0b-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4ea0b-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ea0b-249">Entry</span></span> | <span data-ttu-id="4ea0b-250">Valor</span><span class="sxs-lookup"><span data-stu-id="4ea0b-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4ea0b-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="4ea0b-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4ea0b-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ea0b-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="4ea0b-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ea0b-253">System-Only</span></span>            | <span data-ttu-id="4ea0b-254">True</span><span class="sxs-lookup"><span data-stu-id="4ea0b-254">True</span></span>                            |
| <span data-ttu-id="4ea0b-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4ea0b-255">Is-Single-Valued</span></span>       | <span data-ttu-id="4ea0b-256">Falso</span><span class="sxs-lookup"><span data-stu-id="4ea0b-256">False</span></span>                           |
| <span data-ttu-id="4ea0b-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="4ea0b-257">Is Indexed</span></span>             | <span data-ttu-id="4ea0b-258">True</span><span class="sxs-lookup"><span data-stu-id="4ea0b-258">True</span></span>                            |
| <span data-ttu-id="4ea0b-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4ea0b-259">In Global Catalog</span></span>      | <span data-ttu-id="4ea0b-260">True</span><span class="sxs-lookup"><span data-stu-id="4ea0b-260">True</span></span>                            |
| <span data-ttu-id="4ea0b-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4ea0b-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ea0b-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4ea0b-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4ea0b-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ea0b-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4ea0b-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ea0b-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4ea0b-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ea0b-265">Search-Flags</span></span>           | <span data-ttu-id="4ea0b-266">0x00000009</span><span class="sxs-lookup"><span data-stu-id="4ea0b-266">0x00000009</span></span>                      |
| <span data-ttu-id="4ea0b-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ea0b-267">System-Flags</span></span>           | <span data-ttu-id="4ea0b-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="4ea0b-268">0x00000012</span></span>                      |
| <span data-ttu-id="4ea0b-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4ea0b-269">Classes used in</span></span>        | [<span data-ttu-id="4ea0b-270">**Início**</span><span class="sxs-lookup"><span data-stu-id="4ea0b-270">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4ea0b-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ea0b-271">Windows Server 2012</span></span>



| <span data-ttu-id="4ea0b-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ea0b-272">Entry</span></span> | <span data-ttu-id="4ea0b-273">Valor</span><span class="sxs-lookup"><span data-stu-id="4ea0b-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4ea0b-274">ID do link</span><span class="sxs-lookup"><span data-stu-id="4ea0b-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4ea0b-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ea0b-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="4ea0b-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ea0b-276">System-Only</span></span>            | <span data-ttu-id="4ea0b-277">True</span><span class="sxs-lookup"><span data-stu-id="4ea0b-277">True</span></span>                            |
| <span data-ttu-id="4ea0b-278">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4ea0b-278">Is-Single-Valued</span></span>       | <span data-ttu-id="4ea0b-279">Falso</span><span class="sxs-lookup"><span data-stu-id="4ea0b-279">False</span></span>                           |
| <span data-ttu-id="4ea0b-280">É indexado</span><span class="sxs-lookup"><span data-stu-id="4ea0b-280">Is Indexed</span></span>             | <span data-ttu-id="4ea0b-281">True</span><span class="sxs-lookup"><span data-stu-id="4ea0b-281">True</span></span>                            |
| <span data-ttu-id="4ea0b-282">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4ea0b-282">In Global Catalog</span></span>      | <span data-ttu-id="4ea0b-283">True</span><span class="sxs-lookup"><span data-stu-id="4ea0b-283">True</span></span>                            |
| <span data-ttu-id="4ea0b-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4ea0b-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ea0b-285">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4ea0b-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4ea0b-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ea0b-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4ea0b-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ea0b-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4ea0b-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ea0b-288">Search-Flags</span></span>           | <span data-ttu-id="4ea0b-289">0x00000009</span><span class="sxs-lookup"><span data-stu-id="4ea0b-289">0x00000009</span></span>                      |
| <span data-ttu-id="4ea0b-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ea0b-290">System-Flags</span></span>           | <span data-ttu-id="4ea0b-291">0x00000012</span><span class="sxs-lookup"><span data-stu-id="4ea0b-291">0x00000012</span></span>                      |
| <span data-ttu-id="4ea0b-292">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4ea0b-292">Classes used in</span></span>        | [<span data-ttu-id="4ea0b-293">**Início**</span><span class="sxs-lookup"><span data-stu-id="4ea0b-293">**Top**</span></span>](c-top.md)<br/> |



 

 





