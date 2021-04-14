---
title: Atributo de ID de link
description: Um inteiro que indica que o atributo é um atributo vinculado. Um inteiro par é um link para frente e um inteiro ímpar é um link para trás.
ms.assetid: 73851839-f70c-40c6-976c-0bf727083791
ms.tgt_platform: multiple
keywords:
- Esquema do atributo ID do link do AD
- atributo LinkID do esquema do AD
topic_type:
- apiref
api_name:
- Link-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a64ad1d26ce5510ac5643419ade46d0565df6487
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104500012"
---
# <a name="link-id-attribute"></a><span data-ttu-id="daef8-106">Atributo de ID de link</span><span class="sxs-lookup"><span data-stu-id="daef8-106">Link-ID attribute</span></span>

<span data-ttu-id="daef8-107">Um inteiro que indica que o atributo é um atributo vinculado.</span><span class="sxs-lookup"><span data-stu-id="daef8-107">An integer that indicates that the attribute is a linked attribute.</span></span> <span data-ttu-id="daef8-108">Um inteiro par é um link para frente e um inteiro ímpar é um link para trás.</span><span class="sxs-lookup"><span data-stu-id="daef8-108">An even integer is a forward link and an odd integer is a backward link.</span></span>



| <span data-ttu-id="daef8-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="daef8-109">Entry</span></span> | <span data-ttu-id="daef8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="daef8-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="daef8-111">CN</span><span class="sxs-lookup"><span data-stu-id="daef8-111">CN</span></span>                | <span data-ttu-id="daef8-112">ID do link</span><span class="sxs-lookup"><span data-stu-id="daef8-112">Link-ID</span></span>                              |
| <span data-ttu-id="daef8-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="daef8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="daef8-114">linkID</span><span class="sxs-lookup"><span data-stu-id="daef8-114">linkID</span></span>                               |
| <span data-ttu-id="daef8-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="daef8-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="daef8-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="daef8-116">Update Privilege</span></span>  | <span data-ttu-id="daef8-117">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="daef8-117">Schema administrator</span></span>                 |
| <span data-ttu-id="daef8-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="daef8-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="daef8-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="daef8-119">Attribute-Id</span></span>      | <span data-ttu-id="daef8-120">1.2.840.113556.1.2.50</span><span class="sxs-lookup"><span data-stu-id="daef8-120">1.2.840.113556.1.2.50</span></span>                |
| <span data-ttu-id="daef8-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="daef8-121">System-Id-Guid</span></span>    | <span data-ttu-id="daef8-122">bf96799b-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="daef8-122">bf96799b-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="daef8-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="daef8-123">Syntax</span></span>            | [<span data-ttu-id="daef8-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="daef8-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="daef8-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="daef8-125">Implementations</span></span>

-   [<span data-ttu-id="daef8-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="daef8-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="daef8-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="daef8-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="daef8-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="daef8-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="daef8-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="daef8-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="daef8-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="daef8-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="daef8-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="daef8-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="daef8-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="daef8-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="daef8-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="daef8-133">Windows 2000 Server</span></span>



| <span data-ttu-id="daef8-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="daef8-134">Entry</span></span> | <span data-ttu-id="daef8-135">Valor</span><span class="sxs-lookup"><span data-stu-id="daef8-135">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="daef8-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="daef8-136">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="daef8-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="daef8-137">MAPI-Id</span></span>                | <span data-ttu-id="daef8-138">0x80C5</span><span class="sxs-lookup"><span data-stu-id="daef8-138">0x80C5</span></span>                                                   |
| <span data-ttu-id="daef8-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="daef8-139">System-Only</span></span>            | <span data-ttu-id="daef8-140">True</span><span class="sxs-lookup"><span data-stu-id="daef8-140">True</span></span>                                                     |
| <span data-ttu-id="daef8-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="daef8-141">Is-Single-Valued</span></span>       | <span data-ttu-id="daef8-142">True</span><span class="sxs-lookup"><span data-stu-id="daef8-142">True</span></span>                                                     |
| <span data-ttu-id="daef8-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="daef8-143">Is Indexed</span></span>             | <span data-ttu-id="daef8-144">Falso</span><span class="sxs-lookup"><span data-stu-id="daef8-144">False</span></span>                                                    |
| <span data-ttu-id="daef8-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="daef8-145">In Global Catalog</span></span>      | <span data-ttu-id="daef8-146">Falso</span><span class="sxs-lookup"><span data-stu-id="daef8-146">False</span></span>                                                    |
| <span data-ttu-id="daef8-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="daef8-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="daef8-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="daef8-148">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="daef8-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="daef8-149">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="daef8-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="daef8-150">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="daef8-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="daef8-151">Search-Flags</span></span>           | <span data-ttu-id="daef8-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="daef8-152">0x00000000</span></span>                                               |
| <span data-ttu-id="daef8-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="daef8-153">System-Flags</span></span>           | <span data-ttu-id="daef8-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="daef8-154">0x00000010</span></span>                                               |
| <span data-ttu-id="daef8-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="daef8-155">Classes used in</span></span>        | [<span data-ttu-id="daef8-156">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="daef8-156">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="daef8-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="daef8-157">Windows Server 2003</span></span>



| <span data-ttu-id="daef8-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="daef8-158">Entry</span></span> | <span data-ttu-id="daef8-159">Valor</span><span class="sxs-lookup"><span data-stu-id="daef8-159">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="daef8-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="daef8-160">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="daef8-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="daef8-161">MAPI-Id</span></span>                | <span data-ttu-id="daef8-162">0x80C5</span><span class="sxs-lookup"><span data-stu-id="daef8-162">0x80C5</span></span>                                                   |
| <span data-ttu-id="daef8-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="daef8-163">System-Only</span></span>            | <span data-ttu-id="daef8-164">True</span><span class="sxs-lookup"><span data-stu-id="daef8-164">True</span></span>                                                     |
| <span data-ttu-id="daef8-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="daef8-165">Is-Single-Valued</span></span>       | <span data-ttu-id="daef8-166">True</span><span class="sxs-lookup"><span data-stu-id="daef8-166">True</span></span>                                                     |
| <span data-ttu-id="daef8-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="daef8-167">Is Indexed</span></span>             | <span data-ttu-id="daef8-168">Falso</span><span class="sxs-lookup"><span data-stu-id="daef8-168">False</span></span>                                                    |
| <span data-ttu-id="daef8-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="daef8-169">In Global Catalog</span></span>      | <span data-ttu-id="daef8-170">Falso</span><span class="sxs-lookup"><span data-stu-id="daef8-170">False</span></span>                                                    |
| <span data-ttu-id="daef8-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="daef8-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="daef8-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="daef8-172">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="daef8-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="daef8-173">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="daef8-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="daef8-174">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="daef8-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="daef8-175">Search-Flags</span></span>           | <span data-ttu-id="daef8-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="daef8-176">0x00000000</span></span>                                               |
| <span data-ttu-id="daef8-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="daef8-177">System-Flags</span></span>           | <span data-ttu-id="daef8-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="daef8-178">0x00000010</span></span>                                               |
| <span data-ttu-id="daef8-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="daef8-179">Classes used in</span></span>        | [<span data-ttu-id="daef8-180">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="daef8-180">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="daef8-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="daef8-181">ADAM</span></span>



| <span data-ttu-id="daef8-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="daef8-182">Entry</span></span> | <span data-ttu-id="daef8-183">Valor</span><span class="sxs-lookup"><span data-stu-id="daef8-183">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="daef8-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="daef8-184">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="daef8-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="daef8-185">MAPI-Id</span></span>                | <span data-ttu-id="daef8-186">0x80C5</span><span class="sxs-lookup"><span data-stu-id="daef8-186">0x80C5</span></span>                                                   |
| <span data-ttu-id="daef8-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="daef8-187">System-Only</span></span>            | <span data-ttu-id="daef8-188">True</span><span class="sxs-lookup"><span data-stu-id="daef8-188">True</span></span>                                                     |
| <span data-ttu-id="daef8-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="daef8-189">Is-Single-Valued</span></span>       | <span data-ttu-id="daef8-190">True</span><span class="sxs-lookup"><span data-stu-id="daef8-190">True</span></span>                                                     |
| <span data-ttu-id="daef8-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="daef8-191">Is Indexed</span></span>             | <span data-ttu-id="daef8-192">Falso</span><span class="sxs-lookup"><span data-stu-id="daef8-192">False</span></span>                                                    |
| <span data-ttu-id="daef8-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="daef8-193">In Global Catalog</span></span>      | <span data-ttu-id="daef8-194">Falso</span><span class="sxs-lookup"><span data-stu-id="daef8-194">False</span></span>                                                    |
| <span data-ttu-id="daef8-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="daef8-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="daef8-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="daef8-196">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="daef8-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="daef8-197">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="daef8-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="daef8-198">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="daef8-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="daef8-199">Search-Flags</span></span>           | <span data-ttu-id="daef8-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="daef8-200">0x00000000</span></span>                                               |
| <span data-ttu-id="daef8-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="daef8-201">System-Flags</span></span>           | <span data-ttu-id="daef8-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="daef8-202">0x00000010</span></span>                                               |
| <span data-ttu-id="daef8-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="daef8-203">Classes used in</span></span>        | [<span data-ttu-id="daef8-204">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="daef8-204">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="daef8-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="daef8-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="daef8-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="daef8-206">Entry</span></span> | <span data-ttu-id="daef8-207">Valor</span><span class="sxs-lookup"><span data-stu-id="daef8-207">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="daef8-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="daef8-208">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="daef8-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="daef8-209">MAPI-Id</span></span>                | <span data-ttu-id="daef8-210">0x80C5</span><span class="sxs-lookup"><span data-stu-id="daef8-210">0x80C5</span></span>                                                   |
| <span data-ttu-id="daef8-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="daef8-211">System-Only</span></span>            | <span data-ttu-id="daef8-212">True</span><span class="sxs-lookup"><span data-stu-id="daef8-212">True</span></span>                                                     |
| <span data-ttu-id="daef8-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="daef8-213">Is-Single-Valued</span></span>       | <span data-ttu-id="daef8-214">True</span><span class="sxs-lookup"><span data-stu-id="daef8-214">True</span></span>                                                     |
| <span data-ttu-id="daef8-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="daef8-215">Is Indexed</span></span>             | <span data-ttu-id="daef8-216">Falso</span><span class="sxs-lookup"><span data-stu-id="daef8-216">False</span></span>                                                    |
| <span data-ttu-id="daef8-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="daef8-217">In Global Catalog</span></span>      | <span data-ttu-id="daef8-218">Falso</span><span class="sxs-lookup"><span data-stu-id="daef8-218">False</span></span>                                                    |
| <span data-ttu-id="daef8-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="daef8-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="daef8-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="daef8-220">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="daef8-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="daef8-221">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="daef8-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="daef8-222">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="daef8-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="daef8-223">Search-Flags</span></span>           | <span data-ttu-id="daef8-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="daef8-224">0x00000000</span></span>                                               |
| <span data-ttu-id="daef8-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="daef8-225">System-Flags</span></span>           | <span data-ttu-id="daef8-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="daef8-226">0x00000010</span></span>                                               |
| <span data-ttu-id="daef8-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="daef8-227">Classes used in</span></span>        | [<span data-ttu-id="daef8-228">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="daef8-228">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="daef8-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="daef8-229">Windows Server 2008</span></span>



| <span data-ttu-id="daef8-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="daef8-230">Entry</span></span> | <span data-ttu-id="daef8-231">Valor</span><span class="sxs-lookup"><span data-stu-id="daef8-231">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="daef8-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="daef8-232">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="daef8-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="daef8-233">MAPI-Id</span></span>                | <span data-ttu-id="daef8-234">0x80C5</span><span class="sxs-lookup"><span data-stu-id="daef8-234">0x80C5</span></span>                                                   |
| <span data-ttu-id="daef8-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="daef8-235">System-Only</span></span>            | <span data-ttu-id="daef8-236">True</span><span class="sxs-lookup"><span data-stu-id="daef8-236">True</span></span>                                                     |
| <span data-ttu-id="daef8-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="daef8-237">Is-Single-Valued</span></span>       | <span data-ttu-id="daef8-238">True</span><span class="sxs-lookup"><span data-stu-id="daef8-238">True</span></span>                                                     |
| <span data-ttu-id="daef8-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="daef8-239">Is Indexed</span></span>             | <span data-ttu-id="daef8-240">Falso</span><span class="sxs-lookup"><span data-stu-id="daef8-240">False</span></span>                                                    |
| <span data-ttu-id="daef8-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="daef8-241">In Global Catalog</span></span>      | <span data-ttu-id="daef8-242">Falso</span><span class="sxs-lookup"><span data-stu-id="daef8-242">False</span></span>                                                    |
| <span data-ttu-id="daef8-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="daef8-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="daef8-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="daef8-244">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="daef8-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="daef8-245">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="daef8-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="daef8-246">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="daef8-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="daef8-247">Search-Flags</span></span>           | <span data-ttu-id="daef8-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="daef8-248">0x00000000</span></span>                                               |
| <span data-ttu-id="daef8-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="daef8-249">System-Flags</span></span>           | <span data-ttu-id="daef8-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="daef8-250">0x00000010</span></span>                                               |
| <span data-ttu-id="daef8-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="daef8-251">Classes used in</span></span>        | [<span data-ttu-id="daef8-252">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="daef8-252">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="daef8-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="daef8-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="daef8-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="daef8-254">Entry</span></span> | <span data-ttu-id="daef8-255">Valor</span><span class="sxs-lookup"><span data-stu-id="daef8-255">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="daef8-256">ID do link</span><span class="sxs-lookup"><span data-stu-id="daef8-256">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="daef8-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="daef8-257">MAPI-Id</span></span>                | <span data-ttu-id="daef8-258">0x80C5</span><span class="sxs-lookup"><span data-stu-id="daef8-258">0x80C5</span></span>                                                   |
| <span data-ttu-id="daef8-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="daef8-259">System-Only</span></span>            | <span data-ttu-id="daef8-260">True</span><span class="sxs-lookup"><span data-stu-id="daef8-260">True</span></span>                                                     |
| <span data-ttu-id="daef8-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="daef8-261">Is-Single-Valued</span></span>       | <span data-ttu-id="daef8-262">True</span><span class="sxs-lookup"><span data-stu-id="daef8-262">True</span></span>                                                     |
| <span data-ttu-id="daef8-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="daef8-263">Is Indexed</span></span>             | <span data-ttu-id="daef8-264">Falso</span><span class="sxs-lookup"><span data-stu-id="daef8-264">False</span></span>                                                    |
| <span data-ttu-id="daef8-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="daef8-265">In Global Catalog</span></span>      | <span data-ttu-id="daef8-266">Falso</span><span class="sxs-lookup"><span data-stu-id="daef8-266">False</span></span>                                                    |
| <span data-ttu-id="daef8-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="daef8-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="daef8-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="daef8-268">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="daef8-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="daef8-269">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="daef8-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="daef8-270">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="daef8-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="daef8-271">Search-Flags</span></span>           | <span data-ttu-id="daef8-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="daef8-272">0x00000000</span></span>                                               |
| <span data-ttu-id="daef8-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="daef8-273">System-Flags</span></span>           | <span data-ttu-id="daef8-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="daef8-274">0x00000010</span></span>                                               |
| <span data-ttu-id="daef8-275">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="daef8-275">Classes used in</span></span>        | [<span data-ttu-id="daef8-276">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="daef8-276">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="daef8-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="daef8-277">Windows Server 2012</span></span>



| <span data-ttu-id="daef8-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="daef8-278">Entry</span></span> | <span data-ttu-id="daef8-279">Valor</span><span class="sxs-lookup"><span data-stu-id="daef8-279">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="daef8-280">ID do link</span><span class="sxs-lookup"><span data-stu-id="daef8-280">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="daef8-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="daef8-281">MAPI-Id</span></span>                | <span data-ttu-id="daef8-282">0x80C5</span><span class="sxs-lookup"><span data-stu-id="daef8-282">0x80C5</span></span>                                                   |
| <span data-ttu-id="daef8-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="daef8-283">System-Only</span></span>            | <span data-ttu-id="daef8-284">True</span><span class="sxs-lookup"><span data-stu-id="daef8-284">True</span></span>                                                     |
| <span data-ttu-id="daef8-285">É de valor único</span><span class="sxs-lookup"><span data-stu-id="daef8-285">Is-Single-Valued</span></span>       | <span data-ttu-id="daef8-286">True</span><span class="sxs-lookup"><span data-stu-id="daef8-286">True</span></span>                                                     |
| <span data-ttu-id="daef8-287">É indexado</span><span class="sxs-lookup"><span data-stu-id="daef8-287">Is Indexed</span></span>             | <span data-ttu-id="daef8-288">Falso</span><span class="sxs-lookup"><span data-stu-id="daef8-288">False</span></span>                                                    |
| <span data-ttu-id="daef8-289">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="daef8-289">In Global Catalog</span></span>      | <span data-ttu-id="daef8-290">Falso</span><span class="sxs-lookup"><span data-stu-id="daef8-290">False</span></span>                                                    |
| <span data-ttu-id="daef8-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="daef8-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="daef8-292">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="daef8-292">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="daef8-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="daef8-293">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="daef8-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="daef8-294">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="daef8-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="daef8-295">Search-Flags</span></span>           | <span data-ttu-id="daef8-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="daef8-296">0x00000000</span></span>                                               |
| <span data-ttu-id="daef8-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="daef8-297">System-Flags</span></span>           | <span data-ttu-id="daef8-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="daef8-298">0x00000010</span></span>                                               |
| <span data-ttu-id="daef8-299">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="daef8-299">Classes used in</span></span>        | [<span data-ttu-id="daef8-300">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="daef8-300">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





