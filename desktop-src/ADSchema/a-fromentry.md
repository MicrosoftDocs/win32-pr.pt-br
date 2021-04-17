---
title: From-Entry atributo
description: Esse é um atributo construído que será verdadeiro se o objeto for gravável e FALSE se for somente leitura, por exemplo, uma instância de réplica de GC.
ms.assetid: b43e979d-15f9-4425-8a58-c9ed71bab1e4
ms.tgt_platform: multiple
keywords:
- Esquema de From-Entry do atributo AD
- Esquema de AD do atributo fromEntry
topic_type:
- apiref
api_name:
- From-Entry
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c5f5e45e2897b917ad442f1b1b5d77246fa079c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105749117"
---
# <a name="from-entry-attribute"></a><span data-ttu-id="453e3-105">From-Entry atributo</span><span class="sxs-lookup"><span data-stu-id="453e3-105">From-Entry attribute</span></span>

<span data-ttu-id="453e3-106">Esse é um atributo construído que será **verdadeiro** se o objeto for gravável e **false** se for somente leitura, por exemplo, uma instância de réplica de GC.</span><span class="sxs-lookup"><span data-stu-id="453e3-106">This is a constructed attribute that is **TRUE** if the object is writable and **FALSE** if it is read-only, for example, a GC replica instance.</span></span>



| <span data-ttu-id="453e3-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="453e3-107">Entry</span></span> | <span data-ttu-id="453e3-108">Valor</span><span class="sxs-lookup"><span data-stu-id="453e3-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="453e3-109">CN</span><span class="sxs-lookup"><span data-stu-id="453e3-109">CN</span></span>                | <span data-ttu-id="453e3-110">From-Entry</span><span class="sxs-lookup"><span data-stu-id="453e3-110">From-Entry</span></span>                           |
| <span data-ttu-id="453e3-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="453e3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="453e3-112">fromEntry</span><span class="sxs-lookup"><span data-stu-id="453e3-112">fromEntry</span></span>                            |
| <span data-ttu-id="453e3-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="453e3-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="453e3-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="453e3-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="453e3-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="453e3-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="453e3-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="453e3-116">Attribute-Id</span></span>      | <span data-ttu-id="453e3-117">1.2.840.113556.1.4.910</span><span class="sxs-lookup"><span data-stu-id="453e3-117">1.2.840.113556.1.4.910</span></span>               |
| <span data-ttu-id="453e3-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="453e3-118">System-Id-Guid</span></span>    | <span data-ttu-id="453e3-119">9a7ad949-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="453e3-119">9a7ad949-ca53-11d1-bbd0-0080c76670c0</span></span> |
| <span data-ttu-id="453e3-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="453e3-120">Syntax</span></span>            | [<span data-ttu-id="453e3-121">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="453e3-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="453e3-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="453e3-122">Implementations</span></span>

-   [<span data-ttu-id="453e3-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="453e3-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="453e3-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="453e3-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="453e3-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="453e3-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="453e3-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="453e3-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="453e3-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="453e3-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="453e3-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="453e3-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="453e3-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="453e3-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="453e3-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="453e3-130">Windows 2000 Server</span></span>



| <span data-ttu-id="453e3-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="453e3-131">Entry</span></span> | <span data-ttu-id="453e3-132">Valor</span><span class="sxs-lookup"><span data-stu-id="453e3-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="453e3-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="453e3-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="453e3-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="453e3-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="453e3-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="453e3-135">System-Only</span></span>            | <span data-ttu-id="453e3-136">True</span><span class="sxs-lookup"><span data-stu-id="453e3-136">True</span></span>                            |
| <span data-ttu-id="453e3-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="453e3-137">Is-Single-Valued</span></span>       | <span data-ttu-id="453e3-138">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-138">False</span></span>                           |
| <span data-ttu-id="453e3-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="453e3-139">Is Indexed</span></span>             | <span data-ttu-id="453e3-140">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-140">False</span></span>                           |
| <span data-ttu-id="453e3-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="453e3-141">In Global Catalog</span></span>      | <span data-ttu-id="453e3-142">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-142">False</span></span>                           |
| <span data-ttu-id="453e3-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="453e3-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="453e3-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="453e3-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="453e3-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="453e3-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="453e3-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="453e3-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="453e3-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="453e3-147">Search-Flags</span></span>           | <span data-ttu-id="453e3-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="453e3-148">0x00000000</span></span>                      |
| <span data-ttu-id="453e3-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="453e3-149">System-Flags</span></span>           | <span data-ttu-id="453e3-150">0x08000014</span><span class="sxs-lookup"><span data-stu-id="453e3-150">0x08000014</span></span>                      |
| <span data-ttu-id="453e3-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="453e3-151">Classes used in</span></span>        | [<span data-ttu-id="453e3-152">**Início**</span><span class="sxs-lookup"><span data-stu-id="453e3-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="453e3-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="453e3-153">Windows Server 2003</span></span>



| <span data-ttu-id="453e3-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="453e3-154">Entry</span></span> | <span data-ttu-id="453e3-155">Valor</span><span class="sxs-lookup"><span data-stu-id="453e3-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="453e3-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="453e3-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="453e3-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="453e3-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="453e3-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="453e3-158">System-Only</span></span>            | <span data-ttu-id="453e3-159">True</span><span class="sxs-lookup"><span data-stu-id="453e3-159">True</span></span>                            |
| <span data-ttu-id="453e3-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="453e3-160">Is-Single-Valued</span></span>       | <span data-ttu-id="453e3-161">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-161">False</span></span>                           |
| <span data-ttu-id="453e3-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="453e3-162">Is Indexed</span></span>             | <span data-ttu-id="453e3-163">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-163">False</span></span>                           |
| <span data-ttu-id="453e3-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="453e3-164">In Global Catalog</span></span>      | <span data-ttu-id="453e3-165">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-165">False</span></span>                           |
| <span data-ttu-id="453e3-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="453e3-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="453e3-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="453e3-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="453e3-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="453e3-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="453e3-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="453e3-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="453e3-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="453e3-170">Search-Flags</span></span>           | <span data-ttu-id="453e3-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="453e3-171">0x00000000</span></span>                      |
| <span data-ttu-id="453e3-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="453e3-172">System-Flags</span></span>           | <span data-ttu-id="453e3-173">0x08000014</span><span class="sxs-lookup"><span data-stu-id="453e3-173">0x08000014</span></span>                      |
| <span data-ttu-id="453e3-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="453e3-174">Classes used in</span></span>        | [<span data-ttu-id="453e3-175">**Início**</span><span class="sxs-lookup"><span data-stu-id="453e3-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="453e3-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="453e3-176">ADAM</span></span>



| <span data-ttu-id="453e3-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="453e3-177">Entry</span></span> | <span data-ttu-id="453e3-178">Valor</span><span class="sxs-lookup"><span data-stu-id="453e3-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="453e3-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="453e3-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="453e3-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="453e3-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="453e3-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="453e3-181">System-Only</span></span>            | <span data-ttu-id="453e3-182">True</span><span class="sxs-lookup"><span data-stu-id="453e3-182">True</span></span>                            |
| <span data-ttu-id="453e3-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="453e3-183">Is-Single-Valued</span></span>       | <span data-ttu-id="453e3-184">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-184">False</span></span>                           |
| <span data-ttu-id="453e3-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="453e3-185">Is Indexed</span></span>             | <span data-ttu-id="453e3-186">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-186">False</span></span>                           |
| <span data-ttu-id="453e3-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="453e3-187">In Global Catalog</span></span>      | <span data-ttu-id="453e3-188">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-188">False</span></span>                           |
| <span data-ttu-id="453e3-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="453e3-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="453e3-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="453e3-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="453e3-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="453e3-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="453e3-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="453e3-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="453e3-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="453e3-193">Search-Flags</span></span>           | <span data-ttu-id="453e3-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="453e3-194">0x00000000</span></span>                      |
| <span data-ttu-id="453e3-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="453e3-195">System-Flags</span></span>           | <span data-ttu-id="453e3-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="453e3-196">0x08000014</span></span>                      |
| <span data-ttu-id="453e3-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="453e3-197">Classes used in</span></span>        | [<span data-ttu-id="453e3-198">**Início**</span><span class="sxs-lookup"><span data-stu-id="453e3-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="453e3-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="453e3-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="453e3-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="453e3-200">Entry</span></span> | <span data-ttu-id="453e3-201">Valor</span><span class="sxs-lookup"><span data-stu-id="453e3-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="453e3-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="453e3-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="453e3-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="453e3-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="453e3-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="453e3-204">System-Only</span></span>            | <span data-ttu-id="453e3-205">True</span><span class="sxs-lookup"><span data-stu-id="453e3-205">True</span></span>                            |
| <span data-ttu-id="453e3-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="453e3-206">Is-Single-Valued</span></span>       | <span data-ttu-id="453e3-207">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-207">False</span></span>                           |
| <span data-ttu-id="453e3-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="453e3-208">Is Indexed</span></span>             | <span data-ttu-id="453e3-209">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-209">False</span></span>                           |
| <span data-ttu-id="453e3-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="453e3-210">In Global Catalog</span></span>      | <span data-ttu-id="453e3-211">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-211">False</span></span>                           |
| <span data-ttu-id="453e3-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="453e3-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="453e3-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="453e3-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="453e3-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="453e3-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="453e3-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="453e3-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="453e3-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="453e3-216">Search-Flags</span></span>           | <span data-ttu-id="453e3-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="453e3-217">0x00000000</span></span>                      |
| <span data-ttu-id="453e3-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="453e3-218">System-Flags</span></span>           | <span data-ttu-id="453e3-219">0x08000014</span><span class="sxs-lookup"><span data-stu-id="453e3-219">0x08000014</span></span>                      |
| <span data-ttu-id="453e3-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="453e3-220">Classes used in</span></span>        | [<span data-ttu-id="453e3-221">**Início**</span><span class="sxs-lookup"><span data-stu-id="453e3-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="453e3-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="453e3-222">Windows Server 2008</span></span>



| <span data-ttu-id="453e3-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="453e3-223">Entry</span></span> | <span data-ttu-id="453e3-224">Valor</span><span class="sxs-lookup"><span data-stu-id="453e3-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="453e3-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="453e3-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="453e3-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="453e3-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="453e3-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="453e3-227">System-Only</span></span>            | <span data-ttu-id="453e3-228">True</span><span class="sxs-lookup"><span data-stu-id="453e3-228">True</span></span>                            |
| <span data-ttu-id="453e3-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="453e3-229">Is-Single-Valued</span></span>       | <span data-ttu-id="453e3-230">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-230">False</span></span>                           |
| <span data-ttu-id="453e3-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="453e3-231">Is Indexed</span></span>             | <span data-ttu-id="453e3-232">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-232">False</span></span>                           |
| <span data-ttu-id="453e3-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="453e3-233">In Global Catalog</span></span>      | <span data-ttu-id="453e3-234">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-234">False</span></span>                           |
| <span data-ttu-id="453e3-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="453e3-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="453e3-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="453e3-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="453e3-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="453e3-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="453e3-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="453e3-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="453e3-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="453e3-239">Search-Flags</span></span>           | <span data-ttu-id="453e3-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="453e3-240">0x00000000</span></span>                      |
| <span data-ttu-id="453e3-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="453e3-241">System-Flags</span></span>           | <span data-ttu-id="453e3-242">0x08000014</span><span class="sxs-lookup"><span data-stu-id="453e3-242">0x08000014</span></span>                      |
| <span data-ttu-id="453e3-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="453e3-243">Classes used in</span></span>        | [<span data-ttu-id="453e3-244">**Início**</span><span class="sxs-lookup"><span data-stu-id="453e3-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="453e3-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="453e3-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="453e3-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="453e3-246">Entry</span></span> | <span data-ttu-id="453e3-247">Valor</span><span class="sxs-lookup"><span data-stu-id="453e3-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="453e3-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="453e3-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="453e3-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="453e3-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="453e3-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="453e3-250">System-Only</span></span>            | <span data-ttu-id="453e3-251">True</span><span class="sxs-lookup"><span data-stu-id="453e3-251">True</span></span>                            |
| <span data-ttu-id="453e3-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="453e3-252">Is-Single-Valued</span></span>       | <span data-ttu-id="453e3-253">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-253">False</span></span>                           |
| <span data-ttu-id="453e3-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="453e3-254">Is Indexed</span></span>             | <span data-ttu-id="453e3-255">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-255">False</span></span>                           |
| <span data-ttu-id="453e3-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="453e3-256">In Global Catalog</span></span>      | <span data-ttu-id="453e3-257">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-257">False</span></span>                           |
| <span data-ttu-id="453e3-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="453e3-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="453e3-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="453e3-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="453e3-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="453e3-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="453e3-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="453e3-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="453e3-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="453e3-262">Search-Flags</span></span>           | <span data-ttu-id="453e3-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="453e3-263">0x00000000</span></span>                      |
| <span data-ttu-id="453e3-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="453e3-264">System-Flags</span></span>           | <span data-ttu-id="453e3-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="453e3-265">0x08000014</span></span>                      |
| <span data-ttu-id="453e3-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="453e3-266">Classes used in</span></span>        | [<span data-ttu-id="453e3-267">**Início**</span><span class="sxs-lookup"><span data-stu-id="453e3-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="453e3-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="453e3-268">Windows Server 2012</span></span>



| <span data-ttu-id="453e3-269">Entrada</span><span class="sxs-lookup"><span data-stu-id="453e3-269">Entry</span></span> | <span data-ttu-id="453e3-270">Valor</span><span class="sxs-lookup"><span data-stu-id="453e3-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="453e3-271">ID do link</span><span class="sxs-lookup"><span data-stu-id="453e3-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="453e3-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="453e3-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="453e3-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="453e3-273">System-Only</span></span>            | <span data-ttu-id="453e3-274">True</span><span class="sxs-lookup"><span data-stu-id="453e3-274">True</span></span>                            |
| <span data-ttu-id="453e3-275">É de valor único</span><span class="sxs-lookup"><span data-stu-id="453e3-275">Is-Single-Valued</span></span>       | <span data-ttu-id="453e3-276">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-276">False</span></span>                           |
| <span data-ttu-id="453e3-277">É indexado</span><span class="sxs-lookup"><span data-stu-id="453e3-277">Is Indexed</span></span>             | <span data-ttu-id="453e3-278">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-278">False</span></span>                           |
| <span data-ttu-id="453e3-279">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="453e3-279">In Global Catalog</span></span>      | <span data-ttu-id="453e3-280">Falso</span><span class="sxs-lookup"><span data-stu-id="453e3-280">False</span></span>                           |
| <span data-ttu-id="453e3-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="453e3-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="453e3-282">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="453e3-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="453e3-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="453e3-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="453e3-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="453e3-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="453e3-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="453e3-285">Search-Flags</span></span>           | <span data-ttu-id="453e3-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="453e3-286">0x00000000</span></span>                      |
| <span data-ttu-id="453e3-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="453e3-287">System-Flags</span></span>           | <span data-ttu-id="453e3-288">0x08000014</span><span class="sxs-lookup"><span data-stu-id="453e3-288">0x08000014</span></span>                      |
| <span data-ttu-id="453e3-289">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="453e3-289">Classes used in</span></span>        | [<span data-ttu-id="453e3-290">**Início**</span><span class="sxs-lookup"><span data-stu-id="453e3-290">**Top**</span></span>](c-top.md)<br/> |



 

 





