---
title: Atributo de categoria de classe de objeto
description: Esse atributo contém o tipo de classe, como abstract, auxiliar ou Structured.
ms.assetid: 0698392d-991e-4a3c-b734-54d025a38d50
ms.tgt_platform: multiple
keywords:
- Esquema de atributo de categoria de classe de objeto do AD
- Esquema de AD do atributo objectClassCategory
topic_type:
- apiref
api_name:
- Object-Class-Category
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397bb50e0af0c9dcddcc535d0bcddb1c8d525cfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919437"
---
# <a name="object-class-category-attribute"></a><span data-ttu-id="dbb61-105">Atributo de categoria de classe de objeto</span><span class="sxs-lookup"><span data-stu-id="dbb61-105">Object-Class-Category attribute</span></span>

<span data-ttu-id="dbb61-106">Esse atributo contém o tipo de classe, como abstract, auxiliar ou Structured.</span><span class="sxs-lookup"><span data-stu-id="dbb61-106">This attribute contains the class type, such as abstract, auxiliary, or structured.</span></span>



| <span data-ttu-id="dbb61-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="dbb61-107">Entry</span></span> | <span data-ttu-id="dbb61-108">Valor</span><span class="sxs-lookup"><span data-stu-id="dbb61-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="dbb61-109">CN</span><span class="sxs-lookup"><span data-stu-id="dbb61-109">CN</span></span>                | <span data-ttu-id="dbb61-110">Categoria de classe de objeto</span><span class="sxs-lookup"><span data-stu-id="dbb61-110">Object-Class-Category</span></span>                                                           |
| <span data-ttu-id="dbb61-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="dbb61-111">Ldap-Display-Name</span></span> | <span data-ttu-id="dbb61-112">objectClassCategory</span><span class="sxs-lookup"><span data-stu-id="dbb61-112">objectClassCategory</span></span>                                                             |
| <span data-ttu-id="dbb61-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="dbb61-113">Size</span></span>              | <span data-ttu-id="dbb61-114">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="dbb61-114">4 bytes.</span></span> <span data-ttu-id="dbb61-115">Estrutural 1, abstrata 2, auxiliar 3.</span><span class="sxs-lookup"><span data-stu-id="dbb61-115">Structural 1, abstract 2, auxiliary 3.</span></span> <span data-ttu-id="dbb61-116">A classe 88, 0 não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="dbb61-116">Class 88, 0 should not be used.</span></span> |
| <span data-ttu-id="dbb61-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="dbb61-117">Update Privilege</span></span>  | <span data-ttu-id="dbb61-118">O designer do objeto definiria esse valor.</span><span class="sxs-lookup"><span data-stu-id="dbb61-118">The designer of the object would set this value.</span></span>                                |
| <span data-ttu-id="dbb61-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="dbb61-119">Update Frequency</span></span>  | <span data-ttu-id="dbb61-120">Esse valor nunca deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="dbb61-120">This value should never change.</span></span>                                                 |
| <span data-ttu-id="dbb61-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dbb61-121">Attribute-Id</span></span>      | <span data-ttu-id="dbb61-122">1.2.840.113556.1.2.370</span><span class="sxs-lookup"><span data-stu-id="dbb61-122">1.2.840.113556.1.2.370</span></span>                                                          |
| <span data-ttu-id="dbb61-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dbb61-123">System-Id-Guid</span></span>    | <span data-ttu-id="dbb61-124">bf9679e6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="dbb61-124">bf9679e6-0de6-11d0-a285-00aa003049e2</span></span>                                            |
| <span data-ttu-id="dbb61-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbb61-125">Syntax</span></span>            | [<span data-ttu-id="dbb61-126">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="dbb61-126">**Enumeration**</span></span>](s-enumeration.md)                                            |



## <a name="implementations"></a><span data-ttu-id="dbb61-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="dbb61-127">Implementations</span></span>

-   [<span data-ttu-id="dbb61-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dbb61-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dbb61-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dbb61-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dbb61-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="dbb61-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="dbb61-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dbb61-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dbb61-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dbb61-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dbb61-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dbb61-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dbb61-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dbb61-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dbb61-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dbb61-135">Windows 2000 Server</span></span>



| <span data-ttu-id="dbb61-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="dbb61-136">Entry</span></span> | <span data-ttu-id="dbb61-137">Valor</span><span class="sxs-lookup"><span data-stu-id="dbb61-137">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dbb61-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="dbb61-138">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dbb61-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbb61-139">MAPI-Id</span></span>                | <span data-ttu-id="dbb61-140">0x80F6</span><span class="sxs-lookup"><span data-stu-id="dbb61-140">0x80F6</span></span>                                           |
| <span data-ttu-id="dbb61-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbb61-141">System-Only</span></span>            | <span data-ttu-id="dbb61-142">True</span><span class="sxs-lookup"><span data-stu-id="dbb61-142">True</span></span>                                             |
| <span data-ttu-id="dbb61-143">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dbb61-143">Is-Single-Valued</span></span>       | <span data-ttu-id="dbb61-144">True</span><span class="sxs-lookup"><span data-stu-id="dbb61-144">True</span></span>                                             |
| <span data-ttu-id="dbb61-145">É indexado</span><span class="sxs-lookup"><span data-stu-id="dbb61-145">Is Indexed</span></span>             | <span data-ttu-id="dbb61-146">Falso</span><span class="sxs-lookup"><span data-stu-id="dbb61-146">False</span></span>                                            |
| <span data-ttu-id="dbb61-147">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dbb61-147">In Global Catalog</span></span>      | <span data-ttu-id="dbb61-148">Falso</span><span class="sxs-lookup"><span data-stu-id="dbb61-148">False</span></span>                                            |
| <span data-ttu-id="dbb61-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dbb61-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbb61-150">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dbb61-150">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dbb61-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbb61-151">Range-Lower</span></span>            | <span data-ttu-id="dbb61-152">0</span><span class="sxs-lookup"><span data-stu-id="dbb61-152">0</span></span>                                                |
| <span data-ttu-id="dbb61-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbb61-153">Range-Upper</span></span>            | <span data-ttu-id="dbb61-154">3</span><span class="sxs-lookup"><span data-stu-id="dbb61-154">3</span></span>                                                |
| <span data-ttu-id="dbb61-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbb61-155">Search-Flags</span></span>           | <span data-ttu-id="dbb61-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbb61-156">0x00000000</span></span>                                       |
| <span data-ttu-id="dbb61-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbb61-157">System-Flags</span></span>           | <span data-ttu-id="dbb61-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dbb61-158">0x00000010</span></span>                                       |
| <span data-ttu-id="dbb61-159">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dbb61-159">Classes used in</span></span>        | [<span data-ttu-id="dbb61-160">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="dbb61-160">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dbb61-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dbb61-161">Windows Server 2003</span></span>



| <span data-ttu-id="dbb61-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="dbb61-162">Entry</span></span> | <span data-ttu-id="dbb61-163">Valor</span><span class="sxs-lookup"><span data-stu-id="dbb61-163">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dbb61-164">ID do link</span><span class="sxs-lookup"><span data-stu-id="dbb61-164">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dbb61-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbb61-165">MAPI-Id</span></span>                | <span data-ttu-id="dbb61-166">0x80F6</span><span class="sxs-lookup"><span data-stu-id="dbb61-166">0x80F6</span></span>                                           |
| <span data-ttu-id="dbb61-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbb61-167">System-Only</span></span>            | <span data-ttu-id="dbb61-168">True</span><span class="sxs-lookup"><span data-stu-id="dbb61-168">True</span></span>                                             |
| <span data-ttu-id="dbb61-169">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dbb61-169">Is-Single-Valued</span></span>       | <span data-ttu-id="dbb61-170">True</span><span class="sxs-lookup"><span data-stu-id="dbb61-170">True</span></span>                                             |
| <span data-ttu-id="dbb61-171">É indexado</span><span class="sxs-lookup"><span data-stu-id="dbb61-171">Is Indexed</span></span>             | <span data-ttu-id="dbb61-172">Falso</span><span class="sxs-lookup"><span data-stu-id="dbb61-172">False</span></span>                                            |
| <span data-ttu-id="dbb61-173">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dbb61-173">In Global Catalog</span></span>      | <span data-ttu-id="dbb61-174">Falso</span><span class="sxs-lookup"><span data-stu-id="dbb61-174">False</span></span>                                            |
| <span data-ttu-id="dbb61-175">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dbb61-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbb61-176">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dbb61-176">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dbb61-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbb61-177">Range-Lower</span></span>            | <span data-ttu-id="dbb61-178">0</span><span class="sxs-lookup"><span data-stu-id="dbb61-178">0</span></span>                                                |
| <span data-ttu-id="dbb61-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbb61-179">Range-Upper</span></span>            | <span data-ttu-id="dbb61-180">3</span><span class="sxs-lookup"><span data-stu-id="dbb61-180">3</span></span>                                                |
| <span data-ttu-id="dbb61-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbb61-181">Search-Flags</span></span>           | <span data-ttu-id="dbb61-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbb61-182">0x00000000</span></span>                                       |
| <span data-ttu-id="dbb61-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbb61-183">System-Flags</span></span>           | <span data-ttu-id="dbb61-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dbb61-184">0x00000010</span></span>                                       |
| <span data-ttu-id="dbb61-185">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dbb61-185">Classes used in</span></span>        | [<span data-ttu-id="dbb61-186">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="dbb61-186">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="dbb61-187">ADAM</span><span class="sxs-lookup"><span data-stu-id="dbb61-187">ADAM</span></span>



| <span data-ttu-id="dbb61-188">Entrada</span><span class="sxs-lookup"><span data-stu-id="dbb61-188">Entry</span></span> | <span data-ttu-id="dbb61-189">Valor</span><span class="sxs-lookup"><span data-stu-id="dbb61-189">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dbb61-190">ID do link</span><span class="sxs-lookup"><span data-stu-id="dbb61-190">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dbb61-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbb61-191">MAPI-Id</span></span>                | <span data-ttu-id="dbb61-192">0x80F6</span><span class="sxs-lookup"><span data-stu-id="dbb61-192">0x80F6</span></span>                                           |
| <span data-ttu-id="dbb61-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbb61-193">System-Only</span></span>            | <span data-ttu-id="dbb61-194">True</span><span class="sxs-lookup"><span data-stu-id="dbb61-194">True</span></span>                                             |
| <span data-ttu-id="dbb61-195">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dbb61-195">Is-Single-Valued</span></span>       | <span data-ttu-id="dbb61-196">True</span><span class="sxs-lookup"><span data-stu-id="dbb61-196">True</span></span>                                             |
| <span data-ttu-id="dbb61-197">É indexado</span><span class="sxs-lookup"><span data-stu-id="dbb61-197">Is Indexed</span></span>             | <span data-ttu-id="dbb61-198">Falso</span><span class="sxs-lookup"><span data-stu-id="dbb61-198">False</span></span>                                            |
| <span data-ttu-id="dbb61-199">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dbb61-199">In Global Catalog</span></span>      | <span data-ttu-id="dbb61-200">Falso</span><span class="sxs-lookup"><span data-stu-id="dbb61-200">False</span></span>                                            |
| <span data-ttu-id="dbb61-201">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dbb61-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbb61-202">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dbb61-202">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dbb61-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbb61-203">Range-Lower</span></span>            | <span data-ttu-id="dbb61-204">0</span><span class="sxs-lookup"><span data-stu-id="dbb61-204">0</span></span>                                                |
| <span data-ttu-id="dbb61-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbb61-205">Range-Upper</span></span>            | <span data-ttu-id="dbb61-206">3</span><span class="sxs-lookup"><span data-stu-id="dbb61-206">3</span></span>                                                |
| <span data-ttu-id="dbb61-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbb61-207">Search-Flags</span></span>           | <span data-ttu-id="dbb61-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbb61-208">0x00000000</span></span>                                       |
| <span data-ttu-id="dbb61-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbb61-209">System-Flags</span></span>           | <span data-ttu-id="dbb61-210">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dbb61-210">0x00000010</span></span>                                       |
| <span data-ttu-id="dbb61-211">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dbb61-211">Classes used in</span></span>        | [<span data-ttu-id="dbb61-212">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="dbb61-212">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dbb61-213">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dbb61-213">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dbb61-214">Entrada</span><span class="sxs-lookup"><span data-stu-id="dbb61-214">Entry</span></span> | <span data-ttu-id="dbb61-215">Valor</span><span class="sxs-lookup"><span data-stu-id="dbb61-215">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dbb61-216">ID do link</span><span class="sxs-lookup"><span data-stu-id="dbb61-216">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dbb61-217">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbb61-217">MAPI-Id</span></span>                | <span data-ttu-id="dbb61-218">0x80F6</span><span class="sxs-lookup"><span data-stu-id="dbb61-218">0x80F6</span></span>                                           |
| <span data-ttu-id="dbb61-219">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbb61-219">System-Only</span></span>            | <span data-ttu-id="dbb61-220">True</span><span class="sxs-lookup"><span data-stu-id="dbb61-220">True</span></span>                                             |
| <span data-ttu-id="dbb61-221">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dbb61-221">Is-Single-Valued</span></span>       | <span data-ttu-id="dbb61-222">True</span><span class="sxs-lookup"><span data-stu-id="dbb61-222">True</span></span>                                             |
| <span data-ttu-id="dbb61-223">É indexado</span><span class="sxs-lookup"><span data-stu-id="dbb61-223">Is Indexed</span></span>             | <span data-ttu-id="dbb61-224">Falso</span><span class="sxs-lookup"><span data-stu-id="dbb61-224">False</span></span>                                            |
| <span data-ttu-id="dbb61-225">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dbb61-225">In Global Catalog</span></span>      | <span data-ttu-id="dbb61-226">Falso</span><span class="sxs-lookup"><span data-stu-id="dbb61-226">False</span></span>                                            |
| <span data-ttu-id="dbb61-227">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dbb61-227">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbb61-228">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dbb61-228">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dbb61-229">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbb61-229">Range-Lower</span></span>            | <span data-ttu-id="dbb61-230">0</span><span class="sxs-lookup"><span data-stu-id="dbb61-230">0</span></span>                                                |
| <span data-ttu-id="dbb61-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbb61-231">Range-Upper</span></span>            | <span data-ttu-id="dbb61-232">3</span><span class="sxs-lookup"><span data-stu-id="dbb61-232">3</span></span>                                                |
| <span data-ttu-id="dbb61-233">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbb61-233">Search-Flags</span></span>           | <span data-ttu-id="dbb61-234">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbb61-234">0x00000000</span></span>                                       |
| <span data-ttu-id="dbb61-235">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbb61-235">System-Flags</span></span>           | <span data-ttu-id="dbb61-236">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dbb61-236">0x00000010</span></span>                                       |
| <span data-ttu-id="dbb61-237">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dbb61-237">Classes used in</span></span>        | [<span data-ttu-id="dbb61-238">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="dbb61-238">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dbb61-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbb61-239">Windows Server 2008</span></span>



| <span data-ttu-id="dbb61-240">Entrada</span><span class="sxs-lookup"><span data-stu-id="dbb61-240">Entry</span></span> | <span data-ttu-id="dbb61-241">Valor</span><span class="sxs-lookup"><span data-stu-id="dbb61-241">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dbb61-242">ID do link</span><span class="sxs-lookup"><span data-stu-id="dbb61-242">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dbb61-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbb61-243">MAPI-Id</span></span>                | <span data-ttu-id="dbb61-244">0x80F6</span><span class="sxs-lookup"><span data-stu-id="dbb61-244">0x80F6</span></span>                                           |
| <span data-ttu-id="dbb61-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbb61-245">System-Only</span></span>            | <span data-ttu-id="dbb61-246">True</span><span class="sxs-lookup"><span data-stu-id="dbb61-246">True</span></span>                                             |
| <span data-ttu-id="dbb61-247">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dbb61-247">Is-Single-Valued</span></span>       | <span data-ttu-id="dbb61-248">True</span><span class="sxs-lookup"><span data-stu-id="dbb61-248">True</span></span>                                             |
| <span data-ttu-id="dbb61-249">É indexado</span><span class="sxs-lookup"><span data-stu-id="dbb61-249">Is Indexed</span></span>             | <span data-ttu-id="dbb61-250">Falso</span><span class="sxs-lookup"><span data-stu-id="dbb61-250">False</span></span>                                            |
| <span data-ttu-id="dbb61-251">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dbb61-251">In Global Catalog</span></span>      | <span data-ttu-id="dbb61-252">Falso</span><span class="sxs-lookup"><span data-stu-id="dbb61-252">False</span></span>                                            |
| <span data-ttu-id="dbb61-253">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dbb61-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbb61-254">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dbb61-254">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dbb61-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbb61-255">Range-Lower</span></span>            | <span data-ttu-id="dbb61-256">0</span><span class="sxs-lookup"><span data-stu-id="dbb61-256">0</span></span>                                                |
| <span data-ttu-id="dbb61-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbb61-257">Range-Upper</span></span>            | <span data-ttu-id="dbb61-258">3</span><span class="sxs-lookup"><span data-stu-id="dbb61-258">3</span></span>                                                |
| <span data-ttu-id="dbb61-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbb61-259">Search-Flags</span></span>           | <span data-ttu-id="dbb61-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbb61-260">0x00000000</span></span>                                       |
| <span data-ttu-id="dbb61-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbb61-261">System-Flags</span></span>           | <span data-ttu-id="dbb61-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dbb61-262">0x00000010</span></span>                                       |
| <span data-ttu-id="dbb61-263">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dbb61-263">Classes used in</span></span>        | [<span data-ttu-id="dbb61-264">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="dbb61-264">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dbb61-265">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dbb61-265">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dbb61-266">Entrada</span><span class="sxs-lookup"><span data-stu-id="dbb61-266">Entry</span></span> | <span data-ttu-id="dbb61-267">Valor</span><span class="sxs-lookup"><span data-stu-id="dbb61-267">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dbb61-268">ID do link</span><span class="sxs-lookup"><span data-stu-id="dbb61-268">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dbb61-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbb61-269">MAPI-Id</span></span>                | <span data-ttu-id="dbb61-270">0x80F6</span><span class="sxs-lookup"><span data-stu-id="dbb61-270">0x80F6</span></span>                                           |
| <span data-ttu-id="dbb61-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbb61-271">System-Only</span></span>            | <span data-ttu-id="dbb61-272">True</span><span class="sxs-lookup"><span data-stu-id="dbb61-272">True</span></span>                                             |
| <span data-ttu-id="dbb61-273">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dbb61-273">Is-Single-Valued</span></span>       | <span data-ttu-id="dbb61-274">True</span><span class="sxs-lookup"><span data-stu-id="dbb61-274">True</span></span>                                             |
| <span data-ttu-id="dbb61-275">É indexado</span><span class="sxs-lookup"><span data-stu-id="dbb61-275">Is Indexed</span></span>             | <span data-ttu-id="dbb61-276">Falso</span><span class="sxs-lookup"><span data-stu-id="dbb61-276">False</span></span>                                            |
| <span data-ttu-id="dbb61-277">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dbb61-277">In Global Catalog</span></span>      | <span data-ttu-id="dbb61-278">Falso</span><span class="sxs-lookup"><span data-stu-id="dbb61-278">False</span></span>                                            |
| <span data-ttu-id="dbb61-279">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dbb61-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbb61-280">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dbb61-280">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dbb61-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbb61-281">Range-Lower</span></span>            | <span data-ttu-id="dbb61-282">0</span><span class="sxs-lookup"><span data-stu-id="dbb61-282">0</span></span>                                                |
| <span data-ttu-id="dbb61-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbb61-283">Range-Upper</span></span>            | <span data-ttu-id="dbb61-284">3</span><span class="sxs-lookup"><span data-stu-id="dbb61-284">3</span></span>                                                |
| <span data-ttu-id="dbb61-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbb61-285">Search-Flags</span></span>           | <span data-ttu-id="dbb61-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbb61-286">0x00000000</span></span>                                       |
| <span data-ttu-id="dbb61-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbb61-287">System-Flags</span></span>           | <span data-ttu-id="dbb61-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dbb61-288">0x00000010</span></span>                                       |
| <span data-ttu-id="dbb61-289">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dbb61-289">Classes used in</span></span>        | [<span data-ttu-id="dbb61-290">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="dbb61-290">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dbb61-291">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dbb61-291">Windows Server 2012</span></span>



| <span data-ttu-id="dbb61-292">Entrada</span><span class="sxs-lookup"><span data-stu-id="dbb61-292">Entry</span></span> | <span data-ttu-id="dbb61-293">Valor</span><span class="sxs-lookup"><span data-stu-id="dbb61-293">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dbb61-294">ID do link</span><span class="sxs-lookup"><span data-stu-id="dbb61-294">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dbb61-295">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbb61-295">MAPI-Id</span></span>                | <span data-ttu-id="dbb61-296">0x80F6</span><span class="sxs-lookup"><span data-stu-id="dbb61-296">0x80F6</span></span>                                           |
| <span data-ttu-id="dbb61-297">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbb61-297">System-Only</span></span>            | <span data-ttu-id="dbb61-298">True</span><span class="sxs-lookup"><span data-stu-id="dbb61-298">True</span></span>                                             |
| <span data-ttu-id="dbb61-299">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dbb61-299">Is-Single-Valued</span></span>       | <span data-ttu-id="dbb61-300">True</span><span class="sxs-lookup"><span data-stu-id="dbb61-300">True</span></span>                                             |
| <span data-ttu-id="dbb61-301">É indexado</span><span class="sxs-lookup"><span data-stu-id="dbb61-301">Is Indexed</span></span>             | <span data-ttu-id="dbb61-302">Falso</span><span class="sxs-lookup"><span data-stu-id="dbb61-302">False</span></span>                                            |
| <span data-ttu-id="dbb61-303">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dbb61-303">In Global Catalog</span></span>      | <span data-ttu-id="dbb61-304">Falso</span><span class="sxs-lookup"><span data-stu-id="dbb61-304">False</span></span>                                            |
| <span data-ttu-id="dbb61-305">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dbb61-305">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbb61-306">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dbb61-306">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dbb61-307">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbb61-307">Range-Lower</span></span>            | <span data-ttu-id="dbb61-308">0</span><span class="sxs-lookup"><span data-stu-id="dbb61-308">0</span></span>                                                |
| <span data-ttu-id="dbb61-309">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbb61-309">Range-Upper</span></span>            | <span data-ttu-id="dbb61-310">3</span><span class="sxs-lookup"><span data-stu-id="dbb61-310">3</span></span>                                                |
| <span data-ttu-id="dbb61-311">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbb61-311">Search-Flags</span></span>           | <span data-ttu-id="dbb61-312">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbb61-312">0x00000000</span></span>                                       |
| <span data-ttu-id="dbb61-313">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbb61-313">System-Flags</span></span>           | <span data-ttu-id="dbb61-314">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dbb61-314">0x00000010</span></span>                                       |
| <span data-ttu-id="dbb61-315">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dbb61-315">Classes used in</span></span>        | [<span data-ttu-id="dbb61-316">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="dbb61-316">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





