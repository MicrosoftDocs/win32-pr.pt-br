---
title: Criar-atributo de carimbo de data/hora
description: A data em que este objeto foi criado. Esse valor é replicado.
ms.assetid: 7b957a44-7185-49fa-a219-7c7f4b3e9fce
ms.tgt_platform: multiple
keywords:
- Criar-atributo de carimbo de data/hora esquema do AD
- atributo de AD de atributos createtimestamp
topic_type:
- apiref
api_name:
- Create-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66714aeb035667bc858b7a2e888f6334e7d09c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645591"
---
# <a name="create-time-stamp-attribute"></a><span data-ttu-id="65539-106">Criar-atributo de carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="65539-106">Create-Time-Stamp attribute</span></span>

<span data-ttu-id="65539-107">A data em que este objeto foi criado.</span><span class="sxs-lookup"><span data-stu-id="65539-107">The date when this object was created.</span></span> <span data-ttu-id="65539-108">Esse valor é replicado.</span><span class="sxs-lookup"><span data-stu-id="65539-108">This value is replicated.</span></span>



| <span data-ttu-id="65539-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="65539-109">Entry</span></span> | <span data-ttu-id="65539-110">Valor</span><span class="sxs-lookup"><span data-stu-id="65539-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="65539-111">CN</span><span class="sxs-lookup"><span data-stu-id="65539-111">CN</span></span>                | <span data-ttu-id="65539-112">Criação-carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="65539-112">Create-Time-Stamp</span></span>                                             |
| <span data-ttu-id="65539-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="65539-113">Ldap-Display-Name</span></span> | <span data-ttu-id="65539-114">createtimestamp</span><span class="sxs-lookup"><span data-stu-id="65539-114">createTimeStamp</span></span>                                               |
| <span data-ttu-id="65539-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="65539-115">Size</span></span>              | <span data-ttu-id="65539-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="65539-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="65539-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="65539-117">Update Privilege</span></span>  | <span data-ttu-id="65539-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="65539-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="65539-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="65539-119">Update Frequency</span></span>  | <span data-ttu-id="65539-120">Quando o objeto é criado.</span><span class="sxs-lookup"><span data-stu-id="65539-120">When the object is created.</span></span>                                   |
| <span data-ttu-id="65539-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="65539-121">Attribute-Id</span></span>      | <span data-ttu-id="65539-122">2.5.18.1</span><span class="sxs-lookup"><span data-stu-id="65539-122">2.5.18.1</span></span>                                                      |
| <span data-ttu-id="65539-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="65539-123">System-Id-Guid</span></span>    | <span data-ttu-id="65539-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="65539-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span></span>                          |
| <span data-ttu-id="65539-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="65539-125">Syntax</span></span>            | [<span data-ttu-id="65539-126">**Cadeia de caracteres (em tempo geral)**</span><span class="sxs-lookup"><span data-stu-id="65539-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="65539-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="65539-127">Implementations</span></span>

-   [<span data-ttu-id="65539-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="65539-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="65539-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="65539-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="65539-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="65539-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="65539-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="65539-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="65539-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="65539-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="65539-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="65539-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="65539-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="65539-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="65539-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="65539-135">Windows 2000 Server</span></span>



| <span data-ttu-id="65539-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="65539-136">Entry</span></span> | <span data-ttu-id="65539-137">Valor</span><span class="sxs-lookup"><span data-stu-id="65539-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65539-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="65539-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65539-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65539-139">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="65539-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="65539-140">System-Only</span></span>            | <span data-ttu-id="65539-141">True</span><span class="sxs-lookup"><span data-stu-id="65539-141">True</span></span>                            |
| <span data-ttu-id="65539-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="65539-142">Is-Single-Valued</span></span>       | <span data-ttu-id="65539-143">True</span><span class="sxs-lookup"><span data-stu-id="65539-143">True</span></span>                            |
| <span data-ttu-id="65539-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="65539-144">Is Indexed</span></span>             | <span data-ttu-id="65539-145">Falso</span><span class="sxs-lookup"><span data-stu-id="65539-145">False</span></span>                           |
| <span data-ttu-id="65539-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="65539-146">In Global Catalog</span></span>      | <span data-ttu-id="65539-147">Falso</span><span class="sxs-lookup"><span data-stu-id="65539-147">False</span></span>                           |
| <span data-ttu-id="65539-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="65539-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="65539-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="65539-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65539-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65539-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65539-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65539-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65539-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65539-152">Search-Flags</span></span>           | <span data-ttu-id="65539-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65539-153">0x00000000</span></span>                      |
| <span data-ttu-id="65539-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65539-154">System-Flags</span></span>           | <span data-ttu-id="65539-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="65539-155">0x08000014</span></span>                      |
| <span data-ttu-id="65539-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="65539-156">Classes used in</span></span>        | [<span data-ttu-id="65539-157">**Início**</span><span class="sxs-lookup"><span data-stu-id="65539-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="65539-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="65539-158">Windows Server 2003</span></span>



| <span data-ttu-id="65539-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="65539-159">Entry</span></span> | <span data-ttu-id="65539-160">Valor</span><span class="sxs-lookup"><span data-stu-id="65539-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65539-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="65539-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65539-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65539-162">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="65539-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="65539-163">System-Only</span></span>            | <span data-ttu-id="65539-164">True</span><span class="sxs-lookup"><span data-stu-id="65539-164">True</span></span>                            |
| <span data-ttu-id="65539-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="65539-165">Is-Single-Valued</span></span>       | <span data-ttu-id="65539-166">True</span><span class="sxs-lookup"><span data-stu-id="65539-166">True</span></span>                            |
| <span data-ttu-id="65539-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="65539-167">Is Indexed</span></span>             | <span data-ttu-id="65539-168">Falso</span><span class="sxs-lookup"><span data-stu-id="65539-168">False</span></span>                           |
| <span data-ttu-id="65539-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="65539-169">In Global Catalog</span></span>      | <span data-ttu-id="65539-170">Falso</span><span class="sxs-lookup"><span data-stu-id="65539-170">False</span></span>                           |
| <span data-ttu-id="65539-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="65539-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="65539-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="65539-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65539-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65539-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65539-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65539-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65539-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65539-175">Search-Flags</span></span>           | <span data-ttu-id="65539-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65539-176">0x00000000</span></span>                      |
| <span data-ttu-id="65539-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65539-177">System-Flags</span></span>           | <span data-ttu-id="65539-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="65539-178">0x08000014</span></span>                      |
| <span data-ttu-id="65539-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="65539-179">Classes used in</span></span>        | [<span data-ttu-id="65539-180">**Início**</span><span class="sxs-lookup"><span data-stu-id="65539-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="65539-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="65539-181">ADAM</span></span>



| <span data-ttu-id="65539-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="65539-182">Entry</span></span> | <span data-ttu-id="65539-183">Valor</span><span class="sxs-lookup"><span data-stu-id="65539-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65539-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="65539-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65539-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65539-185">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="65539-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="65539-186">System-Only</span></span>            | <span data-ttu-id="65539-187">True</span><span class="sxs-lookup"><span data-stu-id="65539-187">True</span></span>                            |
| <span data-ttu-id="65539-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="65539-188">Is-Single-Valued</span></span>       | <span data-ttu-id="65539-189">True</span><span class="sxs-lookup"><span data-stu-id="65539-189">True</span></span>                            |
| <span data-ttu-id="65539-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="65539-190">Is Indexed</span></span>             | <span data-ttu-id="65539-191">Falso</span><span class="sxs-lookup"><span data-stu-id="65539-191">False</span></span>                           |
| <span data-ttu-id="65539-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="65539-192">In Global Catalog</span></span>      | <span data-ttu-id="65539-193">Falso</span><span class="sxs-lookup"><span data-stu-id="65539-193">False</span></span>                           |
| <span data-ttu-id="65539-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="65539-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="65539-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="65539-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65539-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65539-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65539-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65539-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65539-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65539-198">Search-Flags</span></span>           | <span data-ttu-id="65539-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65539-199">0x00000000</span></span>                      |
| <span data-ttu-id="65539-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65539-200">System-Flags</span></span>           | <span data-ttu-id="65539-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="65539-201">0x08000014</span></span>                      |
| <span data-ttu-id="65539-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="65539-202">Classes used in</span></span>        | [<span data-ttu-id="65539-203">**Início**</span><span class="sxs-lookup"><span data-stu-id="65539-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="65539-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="65539-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="65539-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="65539-205">Entry</span></span> | <span data-ttu-id="65539-206">Valor</span><span class="sxs-lookup"><span data-stu-id="65539-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65539-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="65539-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65539-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65539-208">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="65539-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="65539-209">System-Only</span></span>            | <span data-ttu-id="65539-210">True</span><span class="sxs-lookup"><span data-stu-id="65539-210">True</span></span>                            |
| <span data-ttu-id="65539-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="65539-211">Is-Single-Valued</span></span>       | <span data-ttu-id="65539-212">True</span><span class="sxs-lookup"><span data-stu-id="65539-212">True</span></span>                            |
| <span data-ttu-id="65539-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="65539-213">Is Indexed</span></span>             | <span data-ttu-id="65539-214">Falso</span><span class="sxs-lookup"><span data-stu-id="65539-214">False</span></span>                           |
| <span data-ttu-id="65539-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="65539-215">In Global Catalog</span></span>      | <span data-ttu-id="65539-216">Falso</span><span class="sxs-lookup"><span data-stu-id="65539-216">False</span></span>                           |
| <span data-ttu-id="65539-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="65539-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="65539-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="65539-218">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65539-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65539-219">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65539-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65539-220">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65539-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65539-221">Search-Flags</span></span>           | <span data-ttu-id="65539-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65539-222">0x00000000</span></span>                      |
| <span data-ttu-id="65539-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65539-223">System-Flags</span></span>           | <span data-ttu-id="65539-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="65539-224">0x08000014</span></span>                      |
| <span data-ttu-id="65539-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="65539-225">Classes used in</span></span>        | [<span data-ttu-id="65539-226">**Início**</span><span class="sxs-lookup"><span data-stu-id="65539-226">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="65539-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65539-227">Windows Server 2008</span></span>



| <span data-ttu-id="65539-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="65539-228">Entry</span></span> | <span data-ttu-id="65539-229">Valor</span><span class="sxs-lookup"><span data-stu-id="65539-229">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65539-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="65539-230">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65539-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65539-231">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="65539-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="65539-232">System-Only</span></span>            | <span data-ttu-id="65539-233">True</span><span class="sxs-lookup"><span data-stu-id="65539-233">True</span></span>                            |
| <span data-ttu-id="65539-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="65539-234">Is-Single-Valued</span></span>       | <span data-ttu-id="65539-235">True</span><span class="sxs-lookup"><span data-stu-id="65539-235">True</span></span>                            |
| <span data-ttu-id="65539-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="65539-236">Is Indexed</span></span>             | <span data-ttu-id="65539-237">Falso</span><span class="sxs-lookup"><span data-stu-id="65539-237">False</span></span>                           |
| <span data-ttu-id="65539-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="65539-238">In Global Catalog</span></span>      | <span data-ttu-id="65539-239">Falso</span><span class="sxs-lookup"><span data-stu-id="65539-239">False</span></span>                           |
| <span data-ttu-id="65539-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="65539-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="65539-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="65539-241">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65539-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65539-242">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65539-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65539-243">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65539-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65539-244">Search-Flags</span></span>           | <span data-ttu-id="65539-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65539-245">0x00000000</span></span>                      |
| <span data-ttu-id="65539-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65539-246">System-Flags</span></span>           | <span data-ttu-id="65539-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="65539-247">0x08000014</span></span>                      |
| <span data-ttu-id="65539-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="65539-248">Classes used in</span></span>        | [<span data-ttu-id="65539-249">**Início**</span><span class="sxs-lookup"><span data-stu-id="65539-249">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="65539-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="65539-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="65539-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="65539-251">Entry</span></span> | <span data-ttu-id="65539-252">Valor</span><span class="sxs-lookup"><span data-stu-id="65539-252">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65539-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="65539-253">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65539-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65539-254">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="65539-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="65539-255">System-Only</span></span>            | <span data-ttu-id="65539-256">True</span><span class="sxs-lookup"><span data-stu-id="65539-256">True</span></span>                            |
| <span data-ttu-id="65539-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="65539-257">Is-Single-Valued</span></span>       | <span data-ttu-id="65539-258">True</span><span class="sxs-lookup"><span data-stu-id="65539-258">True</span></span>                            |
| <span data-ttu-id="65539-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="65539-259">Is Indexed</span></span>             | <span data-ttu-id="65539-260">Falso</span><span class="sxs-lookup"><span data-stu-id="65539-260">False</span></span>                           |
| <span data-ttu-id="65539-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="65539-261">In Global Catalog</span></span>      | <span data-ttu-id="65539-262">Falso</span><span class="sxs-lookup"><span data-stu-id="65539-262">False</span></span>                           |
| <span data-ttu-id="65539-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="65539-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="65539-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="65539-264">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65539-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65539-265">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65539-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65539-266">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65539-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65539-267">Search-Flags</span></span>           | <span data-ttu-id="65539-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65539-268">0x00000000</span></span>                      |
| <span data-ttu-id="65539-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65539-269">System-Flags</span></span>           | <span data-ttu-id="65539-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="65539-270">0x08000014</span></span>                      |
| <span data-ttu-id="65539-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="65539-271">Classes used in</span></span>        | [<span data-ttu-id="65539-272">**Início**</span><span class="sxs-lookup"><span data-stu-id="65539-272">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="65539-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="65539-273">Windows Server 2012</span></span>



| <span data-ttu-id="65539-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="65539-274">Entry</span></span> | <span data-ttu-id="65539-275">Valor</span><span class="sxs-lookup"><span data-stu-id="65539-275">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65539-276">ID do link</span><span class="sxs-lookup"><span data-stu-id="65539-276">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65539-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65539-277">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="65539-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="65539-278">System-Only</span></span>            | <span data-ttu-id="65539-279">True</span><span class="sxs-lookup"><span data-stu-id="65539-279">True</span></span>                            |
| <span data-ttu-id="65539-280">É de valor único</span><span class="sxs-lookup"><span data-stu-id="65539-280">Is-Single-Valued</span></span>       | <span data-ttu-id="65539-281">True</span><span class="sxs-lookup"><span data-stu-id="65539-281">True</span></span>                            |
| <span data-ttu-id="65539-282">É indexado</span><span class="sxs-lookup"><span data-stu-id="65539-282">Is Indexed</span></span>             | <span data-ttu-id="65539-283">Falso</span><span class="sxs-lookup"><span data-stu-id="65539-283">False</span></span>                           |
| <span data-ttu-id="65539-284">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="65539-284">In Global Catalog</span></span>      | <span data-ttu-id="65539-285">Falso</span><span class="sxs-lookup"><span data-stu-id="65539-285">False</span></span>                           |
| <span data-ttu-id="65539-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="65539-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="65539-287">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="65539-287">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65539-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65539-288">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65539-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65539-289">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65539-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65539-290">Search-Flags</span></span>           | <span data-ttu-id="65539-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65539-291">0x00000000</span></span>                      |
| <span data-ttu-id="65539-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65539-292">System-Flags</span></span>           | <span data-ttu-id="65539-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="65539-293">0x08000014</span></span>                      |
| <span data-ttu-id="65539-294">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="65539-294">Classes used in</span></span>        | [<span data-ttu-id="65539-295">**Início**</span><span class="sxs-lookup"><span data-stu-id="65539-295">**Top**</span></span>](c-top.md)<br/> |



 

 





