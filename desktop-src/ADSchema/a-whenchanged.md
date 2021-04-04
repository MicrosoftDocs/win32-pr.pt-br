---
title: When-Changed atributo
description: A data em que esse objeto foi alterado pela última vez. Esse valor não é replicado e existe no catálogo global.
ms.assetid: 32dc9458-5692-4bce-abc1-7bea3ea680a9
ms.tgt_platform: multiple
keywords:
- Esquema de When-Changed do atributo AD
- Esquema de AD do atributo WHENCHANGED
topic_type:
- apiref
api_name:
- When-Changed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c3608a33aa5d5ac52b226cd7a3d94ff0b95520
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103824891"
---
# <a name="when-changed-attribute"></a><span data-ttu-id="9f0b4-106">When-Changed atributo</span><span class="sxs-lookup"><span data-stu-id="9f0b4-106">When-Changed attribute</span></span>

<span data-ttu-id="9f0b4-107">A data em que esse objeto foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-107">The date when this object was last changed.</span></span> <span data-ttu-id="9f0b4-108">Esse valor não é replicado e existe no catálogo global.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-108">This value is not replicated and exists in the global catalog.</span></span>



| <span data-ttu-id="9f0b4-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="9f0b4-109">Entry</span></span> | <span data-ttu-id="9f0b4-110">Valor</span><span class="sxs-lookup"><span data-stu-id="9f0b4-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="9f0b4-111">CN</span><span class="sxs-lookup"><span data-stu-id="9f0b4-111">CN</span></span>                | <span data-ttu-id="9f0b4-112">When-Changed</span><span class="sxs-lookup"><span data-stu-id="9f0b4-112">When-Changed</span></span>                                                  |
| <span data-ttu-id="9f0b4-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9f0b4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9f0b4-114">whenChanged</span><span class="sxs-lookup"><span data-stu-id="9f0b4-114">whenChanged</span></span>                                                   |
| <span data-ttu-id="9f0b4-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="9f0b4-115">Size</span></span>              | <span data-ttu-id="9f0b4-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="9f0b4-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="9f0b4-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="9f0b4-117">Update Privilege</span></span>  | <span data-ttu-id="9f0b4-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="9f0b4-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="9f0b4-119">Update Frequency</span></span>  | <span data-ttu-id="9f0b4-120">Cada vez que o objeto é alterado.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-120">Each time the object is changed.</span></span>                              |
| <span data-ttu-id="9f0b4-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9f0b4-121">Attribute-Id</span></span>      | <span data-ttu-id="9f0b4-122">1.2.840.113556.1.2.3</span><span class="sxs-lookup"><span data-stu-id="9f0b4-122">1.2.840.113556.1.2.3</span></span>                                          |
| <span data-ttu-id="9f0b4-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9f0b4-123">System-Id-Guid</span></span>    | <span data-ttu-id="9f0b4-124">bf967a77-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="9f0b4-124">bf967a77-0de6-11d0-a285-00aa003049e2</span></span>                          |
| <span data-ttu-id="9f0b4-125">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f0b4-125">Syntax</span></span>            | [<span data-ttu-id="9f0b4-126">**Cadeia de caracteres (em tempo geral)**</span><span class="sxs-lookup"><span data-stu-id="9f0b4-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="9f0b4-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="9f0b4-127">Implementations</span></span>

-   [<span data-ttu-id="9f0b4-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9f0b4-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9f0b4-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9f0b4-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9f0b4-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9f0b4-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9f0b4-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9f0b4-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9f0b4-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9f0b4-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9f0b4-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9f0b4-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9f0b4-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9f0b4-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9f0b4-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9f0b4-135">Windows 2000 Server</span></span>



| <span data-ttu-id="9f0b4-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="9f0b4-136">Entry</span></span> | <span data-ttu-id="9f0b4-137">Valor</span><span class="sxs-lookup"><span data-stu-id="9f0b4-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f0b4-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="9f0b4-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f0b4-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f0b4-139">MAPI-Id</span></span>                | <span data-ttu-id="9f0b4-140">0x3008</span><span class="sxs-lookup"><span data-stu-id="9f0b4-140">0x3008</span></span>                          |
| <span data-ttu-id="9f0b4-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f0b4-141">System-Only</span></span>            | <span data-ttu-id="9f0b4-142">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-142">True</span></span>                            |
| <span data-ttu-id="9f0b4-143">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9f0b4-143">Is-Single-Valued</span></span>       | <span data-ttu-id="9f0b4-144">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-144">True</span></span>                            |
| <span data-ttu-id="9f0b4-145">É indexado</span><span class="sxs-lookup"><span data-stu-id="9f0b4-145">Is Indexed</span></span>             | <span data-ttu-id="9f0b4-146">Falso</span><span class="sxs-lookup"><span data-stu-id="9f0b4-146">False</span></span>                           |
| <span data-ttu-id="9f0b4-147">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9f0b4-147">In Global Catalog</span></span>      | <span data-ttu-id="9f0b4-148">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-148">True</span></span>                            |
| <span data-ttu-id="9f0b4-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9f0b4-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f0b4-150">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9f0b4-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f0b4-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f0b4-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9f0b4-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f0b4-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9f0b4-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f0b4-153">Search-Flags</span></span>           | <span data-ttu-id="9f0b4-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f0b4-154">0x00000000</span></span>                      |
| <span data-ttu-id="9f0b4-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f0b4-155">System-Flags</span></span>           | <span data-ttu-id="9f0b4-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="9f0b4-156">0x00000013</span></span>                      |
| <span data-ttu-id="9f0b4-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9f0b4-157">Classes used in</span></span>        | [<span data-ttu-id="9f0b4-158">**Início**</span><span class="sxs-lookup"><span data-stu-id="9f0b4-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9f0b4-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9f0b4-159">Windows Server 2003</span></span>



| <span data-ttu-id="9f0b4-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="9f0b4-160">Entry</span></span> | <span data-ttu-id="9f0b4-161">Valor</span><span class="sxs-lookup"><span data-stu-id="9f0b4-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f0b4-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="9f0b4-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f0b4-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f0b4-163">MAPI-Id</span></span>                | <span data-ttu-id="9f0b4-164">0x3008</span><span class="sxs-lookup"><span data-stu-id="9f0b4-164">0x3008</span></span>                          |
| <span data-ttu-id="9f0b4-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f0b4-165">System-Only</span></span>            | <span data-ttu-id="9f0b4-166">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-166">True</span></span>                            |
| <span data-ttu-id="9f0b4-167">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9f0b4-167">Is-Single-Valued</span></span>       | <span data-ttu-id="9f0b4-168">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-168">True</span></span>                            |
| <span data-ttu-id="9f0b4-169">É indexado</span><span class="sxs-lookup"><span data-stu-id="9f0b4-169">Is Indexed</span></span>             | <span data-ttu-id="9f0b4-170">Falso</span><span class="sxs-lookup"><span data-stu-id="9f0b4-170">False</span></span>                           |
| <span data-ttu-id="9f0b4-171">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9f0b4-171">In Global Catalog</span></span>      | <span data-ttu-id="9f0b4-172">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-172">True</span></span>                            |
| <span data-ttu-id="9f0b4-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9f0b4-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f0b4-174">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9f0b4-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f0b4-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f0b4-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9f0b4-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f0b4-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9f0b4-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f0b4-177">Search-Flags</span></span>           | <span data-ttu-id="9f0b4-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f0b4-178">0x00000000</span></span>                      |
| <span data-ttu-id="9f0b4-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f0b4-179">System-Flags</span></span>           | <span data-ttu-id="9f0b4-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="9f0b4-180">0x00000013</span></span>                      |
| <span data-ttu-id="9f0b4-181">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9f0b4-181">Classes used in</span></span>        | [<span data-ttu-id="9f0b4-182">**Início**</span><span class="sxs-lookup"><span data-stu-id="9f0b4-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9f0b4-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="9f0b4-183">ADAM</span></span>



| <span data-ttu-id="9f0b4-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="9f0b4-184">Entry</span></span> | <span data-ttu-id="9f0b4-185">Valor</span><span class="sxs-lookup"><span data-stu-id="9f0b4-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f0b4-186">ID do link</span><span class="sxs-lookup"><span data-stu-id="9f0b4-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f0b4-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f0b4-187">MAPI-Id</span></span>                | <span data-ttu-id="9f0b4-188">0x3008</span><span class="sxs-lookup"><span data-stu-id="9f0b4-188">0x3008</span></span>                          |
| <span data-ttu-id="9f0b4-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f0b4-189">System-Only</span></span>            | <span data-ttu-id="9f0b4-190">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-190">True</span></span>                            |
| <span data-ttu-id="9f0b4-191">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9f0b4-191">Is-Single-Valued</span></span>       | <span data-ttu-id="9f0b4-192">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-192">True</span></span>                            |
| <span data-ttu-id="9f0b4-193">É indexado</span><span class="sxs-lookup"><span data-stu-id="9f0b4-193">Is Indexed</span></span>             | <span data-ttu-id="9f0b4-194">Falso</span><span class="sxs-lookup"><span data-stu-id="9f0b4-194">False</span></span>                           |
| <span data-ttu-id="9f0b4-195">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9f0b4-195">In Global Catalog</span></span>      | <span data-ttu-id="9f0b4-196">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-196">True</span></span>                            |
| <span data-ttu-id="9f0b4-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9f0b4-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f0b4-198">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9f0b4-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f0b4-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f0b4-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9f0b4-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f0b4-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9f0b4-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f0b4-201">Search-Flags</span></span>           | <span data-ttu-id="9f0b4-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f0b4-202">0x00000000</span></span>                      |
| <span data-ttu-id="9f0b4-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f0b4-203">System-Flags</span></span>           | <span data-ttu-id="9f0b4-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="9f0b4-204">0x00000013</span></span>                      |
| <span data-ttu-id="9f0b4-205">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9f0b4-205">Classes used in</span></span>        | [<span data-ttu-id="9f0b4-206">**Início**</span><span class="sxs-lookup"><span data-stu-id="9f0b4-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9f0b4-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9f0b4-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9f0b4-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="9f0b4-208">Entry</span></span> | <span data-ttu-id="9f0b4-209">Valor</span><span class="sxs-lookup"><span data-stu-id="9f0b4-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f0b4-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="9f0b4-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f0b4-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f0b4-211">MAPI-Id</span></span>                | <span data-ttu-id="9f0b4-212">0x3008</span><span class="sxs-lookup"><span data-stu-id="9f0b4-212">0x3008</span></span>                          |
| <span data-ttu-id="9f0b4-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f0b4-213">System-Only</span></span>            | <span data-ttu-id="9f0b4-214">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-214">True</span></span>                            |
| <span data-ttu-id="9f0b4-215">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9f0b4-215">Is-Single-Valued</span></span>       | <span data-ttu-id="9f0b4-216">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-216">True</span></span>                            |
| <span data-ttu-id="9f0b4-217">É indexado</span><span class="sxs-lookup"><span data-stu-id="9f0b4-217">Is Indexed</span></span>             | <span data-ttu-id="9f0b4-218">Falso</span><span class="sxs-lookup"><span data-stu-id="9f0b4-218">False</span></span>                           |
| <span data-ttu-id="9f0b4-219">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9f0b4-219">In Global Catalog</span></span>      | <span data-ttu-id="9f0b4-220">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-220">True</span></span>                            |
| <span data-ttu-id="9f0b4-221">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9f0b4-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f0b4-222">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9f0b4-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f0b4-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f0b4-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9f0b4-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f0b4-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9f0b4-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f0b4-225">Search-Flags</span></span>           | <span data-ttu-id="9f0b4-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f0b4-226">0x00000000</span></span>                      |
| <span data-ttu-id="9f0b4-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f0b4-227">System-Flags</span></span>           | <span data-ttu-id="9f0b4-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="9f0b4-228">0x00000013</span></span>                      |
| <span data-ttu-id="9f0b4-229">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9f0b4-229">Classes used in</span></span>        | [<span data-ttu-id="9f0b4-230">**Início**</span><span class="sxs-lookup"><span data-stu-id="9f0b4-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9f0b4-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f0b4-231">Windows Server 2008</span></span>



| <span data-ttu-id="9f0b4-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="9f0b4-232">Entry</span></span> | <span data-ttu-id="9f0b4-233">Valor</span><span class="sxs-lookup"><span data-stu-id="9f0b4-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f0b4-234">ID do link</span><span class="sxs-lookup"><span data-stu-id="9f0b4-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f0b4-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f0b4-235">MAPI-Id</span></span>                | <span data-ttu-id="9f0b4-236">0x3008</span><span class="sxs-lookup"><span data-stu-id="9f0b4-236">0x3008</span></span>                          |
| <span data-ttu-id="9f0b4-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f0b4-237">System-Only</span></span>            | <span data-ttu-id="9f0b4-238">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-238">True</span></span>                            |
| <span data-ttu-id="9f0b4-239">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9f0b4-239">Is-Single-Valued</span></span>       | <span data-ttu-id="9f0b4-240">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-240">True</span></span>                            |
| <span data-ttu-id="9f0b4-241">É indexado</span><span class="sxs-lookup"><span data-stu-id="9f0b4-241">Is Indexed</span></span>             | <span data-ttu-id="9f0b4-242">Falso</span><span class="sxs-lookup"><span data-stu-id="9f0b4-242">False</span></span>                           |
| <span data-ttu-id="9f0b4-243">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9f0b4-243">In Global Catalog</span></span>      | <span data-ttu-id="9f0b4-244">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-244">True</span></span>                            |
| <span data-ttu-id="9f0b4-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9f0b4-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f0b4-246">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9f0b4-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f0b4-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f0b4-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9f0b4-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f0b4-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9f0b4-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f0b4-249">Search-Flags</span></span>           | <span data-ttu-id="9f0b4-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f0b4-250">0x00000000</span></span>                      |
| <span data-ttu-id="9f0b4-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f0b4-251">System-Flags</span></span>           | <span data-ttu-id="9f0b4-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="9f0b4-252">0x00000013</span></span>                      |
| <span data-ttu-id="9f0b4-253">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9f0b4-253">Classes used in</span></span>        | [<span data-ttu-id="9f0b4-254">**Início**</span><span class="sxs-lookup"><span data-stu-id="9f0b4-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9f0b4-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9f0b4-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9f0b4-256">Entrada</span><span class="sxs-lookup"><span data-stu-id="9f0b4-256">Entry</span></span> | <span data-ttu-id="9f0b4-257">Valor</span><span class="sxs-lookup"><span data-stu-id="9f0b4-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f0b4-258">ID do link</span><span class="sxs-lookup"><span data-stu-id="9f0b4-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f0b4-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f0b4-259">MAPI-Id</span></span>                | <span data-ttu-id="9f0b4-260">0x3008</span><span class="sxs-lookup"><span data-stu-id="9f0b4-260">0x3008</span></span>                          |
| <span data-ttu-id="9f0b4-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f0b4-261">System-Only</span></span>            | <span data-ttu-id="9f0b4-262">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-262">True</span></span>                            |
| <span data-ttu-id="9f0b4-263">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9f0b4-263">Is-Single-Valued</span></span>       | <span data-ttu-id="9f0b4-264">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-264">True</span></span>                            |
| <span data-ttu-id="9f0b4-265">É indexado</span><span class="sxs-lookup"><span data-stu-id="9f0b4-265">Is Indexed</span></span>             | <span data-ttu-id="9f0b4-266">Falso</span><span class="sxs-lookup"><span data-stu-id="9f0b4-266">False</span></span>                           |
| <span data-ttu-id="9f0b4-267">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9f0b4-267">In Global Catalog</span></span>      | <span data-ttu-id="9f0b4-268">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-268">True</span></span>                            |
| <span data-ttu-id="9f0b4-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9f0b4-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f0b4-270">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9f0b4-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f0b4-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f0b4-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9f0b4-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f0b4-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9f0b4-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f0b4-273">Search-Flags</span></span>           | <span data-ttu-id="9f0b4-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f0b4-274">0x00000000</span></span>                      |
| <span data-ttu-id="9f0b4-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f0b4-275">System-Flags</span></span>           | <span data-ttu-id="9f0b4-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="9f0b4-276">0x00000013</span></span>                      |
| <span data-ttu-id="9f0b4-277">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9f0b4-277">Classes used in</span></span>        | [<span data-ttu-id="9f0b4-278">**Início**</span><span class="sxs-lookup"><span data-stu-id="9f0b4-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9f0b4-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9f0b4-279">Windows Server 2012</span></span>



| <span data-ttu-id="9f0b4-280">Entrada</span><span class="sxs-lookup"><span data-stu-id="9f0b4-280">Entry</span></span> | <span data-ttu-id="9f0b4-281">Valor</span><span class="sxs-lookup"><span data-stu-id="9f0b4-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9f0b4-282">ID do link</span><span class="sxs-lookup"><span data-stu-id="9f0b4-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9f0b4-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f0b4-283">MAPI-Id</span></span>                | <span data-ttu-id="9f0b4-284">0x3008</span><span class="sxs-lookup"><span data-stu-id="9f0b4-284">0x3008</span></span>                          |
| <span data-ttu-id="9f0b4-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f0b4-285">System-Only</span></span>            | <span data-ttu-id="9f0b4-286">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-286">True</span></span>                            |
| <span data-ttu-id="9f0b4-287">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9f0b4-287">Is-Single-Valued</span></span>       | <span data-ttu-id="9f0b4-288">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-288">True</span></span>                            |
| <span data-ttu-id="9f0b4-289">É indexado</span><span class="sxs-lookup"><span data-stu-id="9f0b4-289">Is Indexed</span></span>             | <span data-ttu-id="9f0b4-290">Falso</span><span class="sxs-lookup"><span data-stu-id="9f0b4-290">False</span></span>                           |
| <span data-ttu-id="9f0b4-291">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9f0b4-291">In Global Catalog</span></span>      | <span data-ttu-id="9f0b4-292">True</span><span class="sxs-lookup"><span data-stu-id="9f0b4-292">True</span></span>                            |
| <span data-ttu-id="9f0b4-293">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9f0b4-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f0b4-294">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9f0b4-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9f0b4-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f0b4-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9f0b4-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f0b4-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9f0b4-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f0b4-297">Search-Flags</span></span>           | <span data-ttu-id="9f0b4-298">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f0b4-298">0x00000000</span></span>                      |
| <span data-ttu-id="9f0b4-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f0b4-299">System-Flags</span></span>           | <span data-ttu-id="9f0b4-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="9f0b4-300">0x00000013</span></span>                      |
| <span data-ttu-id="9f0b4-301">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9f0b4-301">Classes used in</span></span>        | [<span data-ttu-id="9f0b4-302">**Início**</span><span class="sxs-lookup"><span data-stu-id="9f0b4-302">**Top**</span></span>](c-top.md)<br/> |



 

 





