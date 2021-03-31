---
title: Object-Category atributo
description: Um nome de classe de objeto usado para agrupar objetos desse ou classes derivadas.
ms.assetid: 06fd0314-08b0-49eb-867c-463f7e0afee4
ms.tgt_platform: multiple
keywords:
- Esquema de Object-Category do atributo AD
- Esquema de AD do atributo objectCategory
topic_type:
- apiref
api_name:
- Object-Category
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b828e4d466b1013ab3854232859a69707553775f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086877"
---
# <a name="object-category-attribute"></a><span data-ttu-id="6faed-105">Object-Category atributo</span><span class="sxs-lookup"><span data-stu-id="6faed-105">Object-Category attribute</span></span>

<span data-ttu-id="6faed-106">Um nome de classe de objeto usado para agrupar objetos desse ou classes derivadas.</span><span class="sxs-lookup"><span data-stu-id="6faed-106">An object class name used to group objects of this or derived classes.</span></span>



| <span data-ttu-id="6faed-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="6faed-107">Entry</span></span> | <span data-ttu-id="6faed-108">Valor</span><span class="sxs-lookup"><span data-stu-id="6faed-108">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="6faed-109">CN</span><span class="sxs-lookup"><span data-stu-id="6faed-109">CN</span></span>                | <span data-ttu-id="6faed-110">Object-Category</span><span class="sxs-lookup"><span data-stu-id="6faed-110">Object-Category</span></span>                                  |
| <span data-ttu-id="6faed-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6faed-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6faed-112">objectCategory</span><span class="sxs-lookup"><span data-stu-id="6faed-112">objectCategory</span></span>                                   |
| <span data-ttu-id="6faed-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="6faed-113">Size</span></span>              | <span data-ttu-id="6faed-114">Cerca de 20 bytes em média.</span><span class="sxs-lookup"><span data-stu-id="6faed-114">About 20 bytes on average.</span></span>                       |
| <span data-ttu-id="6faed-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="6faed-115">Update Privilege</span></span>  | <span data-ttu-id="6faed-116">O designer do objeto definiria esse valor.</span><span class="sxs-lookup"><span data-stu-id="6faed-116">The designer of the object would set this value.</span></span> |
| <span data-ttu-id="6faed-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="6faed-117">Update Frequency</span></span>  | <span data-ttu-id="6faed-118">Esse valor nunca deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="6faed-118">This value should never change.</span></span>                  |
| <span data-ttu-id="6faed-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6faed-119">Attribute-Id</span></span>      | <span data-ttu-id="6faed-120">1.2.840.113556.1.4.782</span><span class="sxs-lookup"><span data-stu-id="6faed-120">1.2.840.113556.1.4.782</span></span>                           |
| <span data-ttu-id="6faed-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6faed-121">System-Id-Guid</span></span>    | <span data-ttu-id="6faed-122">26d97369-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="6faed-122">26d97369-6070-11d1-a9c6-0000f80367c1</span></span>             |
| <span data-ttu-id="6faed-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="6faed-123">Syntax</span></span>            | [<span data-ttu-id="6faed-124">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="6faed-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)          |



## <a name="implementations"></a><span data-ttu-id="6faed-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="6faed-125">Implementations</span></span>

-   [<span data-ttu-id="6faed-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6faed-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6faed-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6faed-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6faed-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6faed-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6faed-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6faed-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6faed-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6faed-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6faed-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6faed-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6faed-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6faed-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6faed-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6faed-133">Windows 2000 Server</span></span>



| <span data-ttu-id="6faed-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="6faed-134">Entry</span></span> | <span data-ttu-id="6faed-135">Valor</span><span class="sxs-lookup"><span data-stu-id="6faed-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6faed-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="6faed-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6faed-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6faed-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6faed-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="6faed-138">System-Only</span></span>            | <span data-ttu-id="6faed-139">Falso</span><span class="sxs-lookup"><span data-stu-id="6faed-139">False</span></span>                           |
| <span data-ttu-id="6faed-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6faed-140">Is-Single-Valued</span></span>       | <span data-ttu-id="6faed-141">True</span><span class="sxs-lookup"><span data-stu-id="6faed-141">True</span></span>                            |
| <span data-ttu-id="6faed-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="6faed-142">Is Indexed</span></span>             | <span data-ttu-id="6faed-143">True</span><span class="sxs-lookup"><span data-stu-id="6faed-143">True</span></span>                            |
| <span data-ttu-id="6faed-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6faed-144">In Global Catalog</span></span>      | <span data-ttu-id="6faed-145">True</span><span class="sxs-lookup"><span data-stu-id="6faed-145">True</span></span>                            |
| <span data-ttu-id="6faed-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6faed-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="6faed-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6faed-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6faed-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6faed-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6faed-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6faed-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6faed-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6faed-150">Search-Flags</span></span>           | <span data-ttu-id="6faed-151">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6faed-151">0x00000001</span></span>                      |
| <span data-ttu-id="6faed-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6faed-152">System-Flags</span></span>           | <span data-ttu-id="6faed-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="6faed-153">0x00000012</span></span>                      |
| <span data-ttu-id="6faed-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6faed-154">Classes used in</span></span>        | [<span data-ttu-id="6faed-155">**Início**</span><span class="sxs-lookup"><span data-stu-id="6faed-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6faed-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6faed-156">Windows Server 2003</span></span>



| <span data-ttu-id="6faed-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="6faed-157">Entry</span></span> | <span data-ttu-id="6faed-158">Valor</span><span class="sxs-lookup"><span data-stu-id="6faed-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6faed-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="6faed-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6faed-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6faed-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6faed-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="6faed-161">System-Only</span></span>            | <span data-ttu-id="6faed-162">Falso</span><span class="sxs-lookup"><span data-stu-id="6faed-162">False</span></span>                           |
| <span data-ttu-id="6faed-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6faed-163">Is-Single-Valued</span></span>       | <span data-ttu-id="6faed-164">True</span><span class="sxs-lookup"><span data-stu-id="6faed-164">True</span></span>                            |
| <span data-ttu-id="6faed-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="6faed-165">Is Indexed</span></span>             | <span data-ttu-id="6faed-166">True</span><span class="sxs-lookup"><span data-stu-id="6faed-166">True</span></span>                            |
| <span data-ttu-id="6faed-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6faed-167">In Global Catalog</span></span>      | <span data-ttu-id="6faed-168">True</span><span class="sxs-lookup"><span data-stu-id="6faed-168">True</span></span>                            |
| <span data-ttu-id="6faed-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6faed-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="6faed-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6faed-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6faed-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6faed-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6faed-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6faed-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6faed-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6faed-173">Search-Flags</span></span>           | <span data-ttu-id="6faed-174">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6faed-174">0x00000001</span></span>                      |
| <span data-ttu-id="6faed-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6faed-175">System-Flags</span></span>           | <span data-ttu-id="6faed-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="6faed-176">0x00000012</span></span>                      |
| <span data-ttu-id="6faed-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6faed-177">Classes used in</span></span>        | [<span data-ttu-id="6faed-178">**Início**</span><span class="sxs-lookup"><span data-stu-id="6faed-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6faed-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="6faed-179">ADAM</span></span>



| <span data-ttu-id="6faed-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="6faed-180">Entry</span></span> | <span data-ttu-id="6faed-181">Valor</span><span class="sxs-lookup"><span data-stu-id="6faed-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6faed-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="6faed-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6faed-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6faed-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6faed-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="6faed-184">System-Only</span></span>            | <span data-ttu-id="6faed-185">Falso</span><span class="sxs-lookup"><span data-stu-id="6faed-185">False</span></span>                           |
| <span data-ttu-id="6faed-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6faed-186">Is-Single-Valued</span></span>       | <span data-ttu-id="6faed-187">True</span><span class="sxs-lookup"><span data-stu-id="6faed-187">True</span></span>                            |
| <span data-ttu-id="6faed-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="6faed-188">Is Indexed</span></span>             | <span data-ttu-id="6faed-189">True</span><span class="sxs-lookup"><span data-stu-id="6faed-189">True</span></span>                            |
| <span data-ttu-id="6faed-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6faed-190">In Global Catalog</span></span>      | <span data-ttu-id="6faed-191">True</span><span class="sxs-lookup"><span data-stu-id="6faed-191">True</span></span>                            |
| <span data-ttu-id="6faed-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6faed-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="6faed-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6faed-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6faed-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6faed-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6faed-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6faed-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6faed-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6faed-196">Search-Flags</span></span>           | <span data-ttu-id="6faed-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6faed-197">0x00000001</span></span>                      |
| <span data-ttu-id="6faed-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6faed-198">System-Flags</span></span>           | <span data-ttu-id="6faed-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="6faed-199">0x00000012</span></span>                      |
| <span data-ttu-id="6faed-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6faed-200">Classes used in</span></span>        | [<span data-ttu-id="6faed-201">**Início**</span><span class="sxs-lookup"><span data-stu-id="6faed-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6faed-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6faed-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6faed-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="6faed-203">Entry</span></span> | <span data-ttu-id="6faed-204">Valor</span><span class="sxs-lookup"><span data-stu-id="6faed-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6faed-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="6faed-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6faed-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6faed-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6faed-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="6faed-207">System-Only</span></span>            | <span data-ttu-id="6faed-208">Falso</span><span class="sxs-lookup"><span data-stu-id="6faed-208">False</span></span>                           |
| <span data-ttu-id="6faed-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6faed-209">Is-Single-Valued</span></span>       | <span data-ttu-id="6faed-210">True</span><span class="sxs-lookup"><span data-stu-id="6faed-210">True</span></span>                            |
| <span data-ttu-id="6faed-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="6faed-211">Is Indexed</span></span>             | <span data-ttu-id="6faed-212">True</span><span class="sxs-lookup"><span data-stu-id="6faed-212">True</span></span>                            |
| <span data-ttu-id="6faed-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6faed-213">In Global Catalog</span></span>      | <span data-ttu-id="6faed-214">True</span><span class="sxs-lookup"><span data-stu-id="6faed-214">True</span></span>                            |
| <span data-ttu-id="6faed-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6faed-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="6faed-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6faed-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6faed-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6faed-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6faed-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6faed-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6faed-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6faed-219">Search-Flags</span></span>           | <span data-ttu-id="6faed-220">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6faed-220">0x00000001</span></span>                      |
| <span data-ttu-id="6faed-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6faed-221">System-Flags</span></span>           | <span data-ttu-id="6faed-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="6faed-222">0x00000012</span></span>                      |
| <span data-ttu-id="6faed-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6faed-223">Classes used in</span></span>        | [<span data-ttu-id="6faed-224">**Início**</span><span class="sxs-lookup"><span data-stu-id="6faed-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6faed-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6faed-225">Windows Server 2008</span></span>



| <span data-ttu-id="6faed-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="6faed-226">Entry</span></span> | <span data-ttu-id="6faed-227">Valor</span><span class="sxs-lookup"><span data-stu-id="6faed-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6faed-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="6faed-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6faed-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6faed-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6faed-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="6faed-230">System-Only</span></span>            | <span data-ttu-id="6faed-231">Falso</span><span class="sxs-lookup"><span data-stu-id="6faed-231">False</span></span>                           |
| <span data-ttu-id="6faed-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6faed-232">Is-Single-Valued</span></span>       | <span data-ttu-id="6faed-233">True</span><span class="sxs-lookup"><span data-stu-id="6faed-233">True</span></span>                            |
| <span data-ttu-id="6faed-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="6faed-234">Is Indexed</span></span>             | <span data-ttu-id="6faed-235">True</span><span class="sxs-lookup"><span data-stu-id="6faed-235">True</span></span>                            |
| <span data-ttu-id="6faed-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6faed-236">In Global Catalog</span></span>      | <span data-ttu-id="6faed-237">True</span><span class="sxs-lookup"><span data-stu-id="6faed-237">True</span></span>                            |
| <span data-ttu-id="6faed-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6faed-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="6faed-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6faed-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6faed-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6faed-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6faed-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6faed-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6faed-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6faed-242">Search-Flags</span></span>           | <span data-ttu-id="6faed-243">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6faed-243">0x00000001</span></span>                      |
| <span data-ttu-id="6faed-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6faed-244">System-Flags</span></span>           | <span data-ttu-id="6faed-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="6faed-245">0x00000012</span></span>                      |
| <span data-ttu-id="6faed-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6faed-246">Classes used in</span></span>        | [<span data-ttu-id="6faed-247">**Início**</span><span class="sxs-lookup"><span data-stu-id="6faed-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6faed-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6faed-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6faed-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="6faed-249">Entry</span></span> | <span data-ttu-id="6faed-250">Valor</span><span class="sxs-lookup"><span data-stu-id="6faed-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6faed-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="6faed-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6faed-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6faed-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6faed-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="6faed-253">System-Only</span></span>            | <span data-ttu-id="6faed-254">Falso</span><span class="sxs-lookup"><span data-stu-id="6faed-254">False</span></span>                           |
| <span data-ttu-id="6faed-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6faed-255">Is-Single-Valued</span></span>       | <span data-ttu-id="6faed-256">True</span><span class="sxs-lookup"><span data-stu-id="6faed-256">True</span></span>                            |
| <span data-ttu-id="6faed-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="6faed-257">Is Indexed</span></span>             | <span data-ttu-id="6faed-258">True</span><span class="sxs-lookup"><span data-stu-id="6faed-258">True</span></span>                            |
| <span data-ttu-id="6faed-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6faed-259">In Global Catalog</span></span>      | <span data-ttu-id="6faed-260">True</span><span class="sxs-lookup"><span data-stu-id="6faed-260">True</span></span>                            |
| <span data-ttu-id="6faed-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6faed-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="6faed-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6faed-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6faed-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6faed-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6faed-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6faed-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6faed-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6faed-265">Search-Flags</span></span>           | <span data-ttu-id="6faed-266">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6faed-266">0x00000001</span></span>                      |
| <span data-ttu-id="6faed-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6faed-267">System-Flags</span></span>           | <span data-ttu-id="6faed-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="6faed-268">0x00000012</span></span>                      |
| <span data-ttu-id="6faed-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6faed-269">Classes used in</span></span>        | [<span data-ttu-id="6faed-270">**Início**</span><span class="sxs-lookup"><span data-stu-id="6faed-270">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6faed-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6faed-271">Windows Server 2012</span></span>



| <span data-ttu-id="6faed-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="6faed-272">Entry</span></span> | <span data-ttu-id="6faed-273">Valor</span><span class="sxs-lookup"><span data-stu-id="6faed-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6faed-274">ID do link</span><span class="sxs-lookup"><span data-stu-id="6faed-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6faed-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6faed-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6faed-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="6faed-276">System-Only</span></span>            | <span data-ttu-id="6faed-277">Falso</span><span class="sxs-lookup"><span data-stu-id="6faed-277">False</span></span>                           |
| <span data-ttu-id="6faed-278">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6faed-278">Is-Single-Valued</span></span>       | <span data-ttu-id="6faed-279">True</span><span class="sxs-lookup"><span data-stu-id="6faed-279">True</span></span>                            |
| <span data-ttu-id="6faed-280">É indexado</span><span class="sxs-lookup"><span data-stu-id="6faed-280">Is Indexed</span></span>             | <span data-ttu-id="6faed-281">True</span><span class="sxs-lookup"><span data-stu-id="6faed-281">True</span></span>                            |
| <span data-ttu-id="6faed-282">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6faed-282">In Global Catalog</span></span>      | <span data-ttu-id="6faed-283">True</span><span class="sxs-lookup"><span data-stu-id="6faed-283">True</span></span>                            |
| <span data-ttu-id="6faed-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6faed-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="6faed-285">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6faed-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6faed-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6faed-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6faed-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6faed-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6faed-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6faed-288">Search-Flags</span></span>           | <span data-ttu-id="6faed-289">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6faed-289">0x00000001</span></span>                      |
| <span data-ttu-id="6faed-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6faed-290">System-Flags</span></span>           | <span data-ttu-id="6faed-291">0x00000012</span><span class="sxs-lookup"><span data-stu-id="6faed-291">0x00000012</span></span>                      |
| <span data-ttu-id="6faed-292">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6faed-292">Classes used in</span></span>        | [<span data-ttu-id="6faed-293">**Início**</span><span class="sxs-lookup"><span data-stu-id="6faed-293">**Top**</span></span>](c-top.md)<br/> |



 

 





