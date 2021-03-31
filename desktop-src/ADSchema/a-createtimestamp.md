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
# <a name="create-time-stamp-attribute"></a><span data-ttu-id="91efd-106">Criar-atributo de carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="91efd-106">Create-Time-Stamp attribute</span></span>

<span data-ttu-id="91efd-107">A data em que este objeto foi criado.</span><span class="sxs-lookup"><span data-stu-id="91efd-107">The date when this object was created.</span></span> <span data-ttu-id="91efd-108">Esse valor é replicado.</span><span class="sxs-lookup"><span data-stu-id="91efd-108">This value is replicated.</span></span>



| <span data-ttu-id="91efd-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="91efd-109">Entry</span></span> | <span data-ttu-id="91efd-110">Valor</span><span class="sxs-lookup"><span data-stu-id="91efd-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="91efd-111">CN</span><span class="sxs-lookup"><span data-stu-id="91efd-111">CN</span></span>                | <span data-ttu-id="91efd-112">Criação-carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="91efd-112">Create-Time-Stamp</span></span>                                             |
| <span data-ttu-id="91efd-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="91efd-113">Ldap-Display-Name</span></span> | <span data-ttu-id="91efd-114">createtimestamp</span><span class="sxs-lookup"><span data-stu-id="91efd-114">createTimeStamp</span></span>                                               |
| <span data-ttu-id="91efd-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="91efd-115">Size</span></span>              | <span data-ttu-id="91efd-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="91efd-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="91efd-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="91efd-117">Update Privilege</span></span>  | <span data-ttu-id="91efd-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="91efd-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="91efd-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="91efd-119">Update Frequency</span></span>  | <span data-ttu-id="91efd-120">Quando o objeto é criado.</span><span class="sxs-lookup"><span data-stu-id="91efd-120">When the object is created.</span></span>                                   |
| <span data-ttu-id="91efd-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="91efd-121">Attribute-Id</span></span>      | <span data-ttu-id="91efd-122">2.5.18.1</span><span class="sxs-lookup"><span data-stu-id="91efd-122">2.5.18.1</span></span>                                                      |
| <span data-ttu-id="91efd-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="91efd-123">System-Id-Guid</span></span>    | <span data-ttu-id="91efd-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="91efd-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span></span>                          |
| <span data-ttu-id="91efd-125">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91efd-125">Syntax</span></span>            | [<span data-ttu-id="91efd-126">**Cadeia de caracteres (em tempo geral)**</span><span class="sxs-lookup"><span data-stu-id="91efd-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="91efd-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="91efd-127">Implementations</span></span>

-   [<span data-ttu-id="91efd-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="91efd-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="91efd-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="91efd-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="91efd-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="91efd-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="91efd-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="91efd-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="91efd-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="91efd-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="91efd-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="91efd-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="91efd-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="91efd-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="91efd-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="91efd-135">Windows 2000 Server</span></span>



| <span data-ttu-id="91efd-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="91efd-136">Entry</span></span> | <span data-ttu-id="91efd-137">Valor</span><span class="sxs-lookup"><span data-stu-id="91efd-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="91efd-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="91efd-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="91efd-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91efd-139">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="91efd-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="91efd-140">System-Only</span></span>            | <span data-ttu-id="91efd-141">True</span><span class="sxs-lookup"><span data-stu-id="91efd-141">True</span></span>                            |
| <span data-ttu-id="91efd-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="91efd-142">Is-Single-Valued</span></span>       | <span data-ttu-id="91efd-143">True</span><span class="sxs-lookup"><span data-stu-id="91efd-143">True</span></span>                            |
| <span data-ttu-id="91efd-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="91efd-144">Is Indexed</span></span>             | <span data-ttu-id="91efd-145">Falso</span><span class="sxs-lookup"><span data-stu-id="91efd-145">False</span></span>                           |
| <span data-ttu-id="91efd-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="91efd-146">In Global Catalog</span></span>      | <span data-ttu-id="91efd-147">Falso</span><span class="sxs-lookup"><span data-stu-id="91efd-147">False</span></span>                           |
| <span data-ttu-id="91efd-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="91efd-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="91efd-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="91efd-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="91efd-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91efd-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="91efd-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91efd-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="91efd-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91efd-152">Search-Flags</span></span>           | <span data-ttu-id="91efd-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91efd-153">0x00000000</span></span>                      |
| <span data-ttu-id="91efd-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91efd-154">System-Flags</span></span>           | <span data-ttu-id="91efd-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="91efd-155">0x08000014</span></span>                      |
| <span data-ttu-id="91efd-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="91efd-156">Classes used in</span></span>        | [<span data-ttu-id="91efd-157">**Início**</span><span class="sxs-lookup"><span data-stu-id="91efd-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="91efd-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="91efd-158">Windows Server 2003</span></span>



| <span data-ttu-id="91efd-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="91efd-159">Entry</span></span> | <span data-ttu-id="91efd-160">Valor</span><span class="sxs-lookup"><span data-stu-id="91efd-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="91efd-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="91efd-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="91efd-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91efd-162">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="91efd-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="91efd-163">System-Only</span></span>            | <span data-ttu-id="91efd-164">True</span><span class="sxs-lookup"><span data-stu-id="91efd-164">True</span></span>                            |
| <span data-ttu-id="91efd-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="91efd-165">Is-Single-Valued</span></span>       | <span data-ttu-id="91efd-166">True</span><span class="sxs-lookup"><span data-stu-id="91efd-166">True</span></span>                            |
| <span data-ttu-id="91efd-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="91efd-167">Is Indexed</span></span>             | <span data-ttu-id="91efd-168">Falso</span><span class="sxs-lookup"><span data-stu-id="91efd-168">False</span></span>                           |
| <span data-ttu-id="91efd-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="91efd-169">In Global Catalog</span></span>      | <span data-ttu-id="91efd-170">Falso</span><span class="sxs-lookup"><span data-stu-id="91efd-170">False</span></span>                           |
| <span data-ttu-id="91efd-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="91efd-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="91efd-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="91efd-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="91efd-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91efd-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="91efd-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91efd-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="91efd-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91efd-175">Search-Flags</span></span>           | <span data-ttu-id="91efd-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91efd-176">0x00000000</span></span>                      |
| <span data-ttu-id="91efd-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91efd-177">System-Flags</span></span>           | <span data-ttu-id="91efd-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="91efd-178">0x08000014</span></span>                      |
| <span data-ttu-id="91efd-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="91efd-179">Classes used in</span></span>        | [<span data-ttu-id="91efd-180">**Início**</span><span class="sxs-lookup"><span data-stu-id="91efd-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="91efd-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="91efd-181">ADAM</span></span>



| <span data-ttu-id="91efd-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="91efd-182">Entry</span></span> | <span data-ttu-id="91efd-183">Valor</span><span class="sxs-lookup"><span data-stu-id="91efd-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="91efd-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="91efd-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="91efd-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91efd-185">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="91efd-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="91efd-186">System-Only</span></span>            | <span data-ttu-id="91efd-187">True</span><span class="sxs-lookup"><span data-stu-id="91efd-187">True</span></span>                            |
| <span data-ttu-id="91efd-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="91efd-188">Is-Single-Valued</span></span>       | <span data-ttu-id="91efd-189">True</span><span class="sxs-lookup"><span data-stu-id="91efd-189">True</span></span>                            |
| <span data-ttu-id="91efd-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="91efd-190">Is Indexed</span></span>             | <span data-ttu-id="91efd-191">Falso</span><span class="sxs-lookup"><span data-stu-id="91efd-191">False</span></span>                           |
| <span data-ttu-id="91efd-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="91efd-192">In Global Catalog</span></span>      | <span data-ttu-id="91efd-193">Falso</span><span class="sxs-lookup"><span data-stu-id="91efd-193">False</span></span>                           |
| <span data-ttu-id="91efd-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="91efd-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="91efd-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="91efd-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="91efd-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91efd-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="91efd-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91efd-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="91efd-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91efd-198">Search-Flags</span></span>           | <span data-ttu-id="91efd-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91efd-199">0x00000000</span></span>                      |
| <span data-ttu-id="91efd-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91efd-200">System-Flags</span></span>           | <span data-ttu-id="91efd-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="91efd-201">0x08000014</span></span>                      |
| <span data-ttu-id="91efd-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="91efd-202">Classes used in</span></span>        | [<span data-ttu-id="91efd-203">**Início**</span><span class="sxs-lookup"><span data-stu-id="91efd-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="91efd-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="91efd-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="91efd-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="91efd-205">Entry</span></span> | <span data-ttu-id="91efd-206">Valor</span><span class="sxs-lookup"><span data-stu-id="91efd-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="91efd-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="91efd-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="91efd-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91efd-208">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="91efd-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="91efd-209">System-Only</span></span>            | <span data-ttu-id="91efd-210">True</span><span class="sxs-lookup"><span data-stu-id="91efd-210">True</span></span>                            |
| <span data-ttu-id="91efd-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="91efd-211">Is-Single-Valued</span></span>       | <span data-ttu-id="91efd-212">True</span><span class="sxs-lookup"><span data-stu-id="91efd-212">True</span></span>                            |
| <span data-ttu-id="91efd-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="91efd-213">Is Indexed</span></span>             | <span data-ttu-id="91efd-214">Falso</span><span class="sxs-lookup"><span data-stu-id="91efd-214">False</span></span>                           |
| <span data-ttu-id="91efd-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="91efd-215">In Global Catalog</span></span>      | <span data-ttu-id="91efd-216">Falso</span><span class="sxs-lookup"><span data-stu-id="91efd-216">False</span></span>                           |
| <span data-ttu-id="91efd-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="91efd-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="91efd-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="91efd-218">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="91efd-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91efd-219">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="91efd-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91efd-220">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="91efd-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91efd-221">Search-Flags</span></span>           | <span data-ttu-id="91efd-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91efd-222">0x00000000</span></span>                      |
| <span data-ttu-id="91efd-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91efd-223">System-Flags</span></span>           | <span data-ttu-id="91efd-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="91efd-224">0x08000014</span></span>                      |
| <span data-ttu-id="91efd-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="91efd-225">Classes used in</span></span>        | [<span data-ttu-id="91efd-226">**Início**</span><span class="sxs-lookup"><span data-stu-id="91efd-226">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="91efd-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91efd-227">Windows Server 2008</span></span>



| <span data-ttu-id="91efd-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="91efd-228">Entry</span></span> | <span data-ttu-id="91efd-229">Valor</span><span class="sxs-lookup"><span data-stu-id="91efd-229">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="91efd-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="91efd-230">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="91efd-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91efd-231">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="91efd-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="91efd-232">System-Only</span></span>            | <span data-ttu-id="91efd-233">True</span><span class="sxs-lookup"><span data-stu-id="91efd-233">True</span></span>                            |
| <span data-ttu-id="91efd-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="91efd-234">Is-Single-Valued</span></span>       | <span data-ttu-id="91efd-235">True</span><span class="sxs-lookup"><span data-stu-id="91efd-235">True</span></span>                            |
| <span data-ttu-id="91efd-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="91efd-236">Is Indexed</span></span>             | <span data-ttu-id="91efd-237">Falso</span><span class="sxs-lookup"><span data-stu-id="91efd-237">False</span></span>                           |
| <span data-ttu-id="91efd-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="91efd-238">In Global Catalog</span></span>      | <span data-ttu-id="91efd-239">Falso</span><span class="sxs-lookup"><span data-stu-id="91efd-239">False</span></span>                           |
| <span data-ttu-id="91efd-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="91efd-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="91efd-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="91efd-241">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="91efd-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91efd-242">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="91efd-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91efd-243">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="91efd-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91efd-244">Search-Flags</span></span>           | <span data-ttu-id="91efd-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91efd-245">0x00000000</span></span>                      |
| <span data-ttu-id="91efd-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91efd-246">System-Flags</span></span>           | <span data-ttu-id="91efd-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="91efd-247">0x08000014</span></span>                      |
| <span data-ttu-id="91efd-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="91efd-248">Classes used in</span></span>        | [<span data-ttu-id="91efd-249">**Início**</span><span class="sxs-lookup"><span data-stu-id="91efd-249">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="91efd-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="91efd-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="91efd-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="91efd-251">Entry</span></span> | <span data-ttu-id="91efd-252">Valor</span><span class="sxs-lookup"><span data-stu-id="91efd-252">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="91efd-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="91efd-253">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="91efd-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91efd-254">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="91efd-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="91efd-255">System-Only</span></span>            | <span data-ttu-id="91efd-256">True</span><span class="sxs-lookup"><span data-stu-id="91efd-256">True</span></span>                            |
| <span data-ttu-id="91efd-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="91efd-257">Is-Single-Valued</span></span>       | <span data-ttu-id="91efd-258">True</span><span class="sxs-lookup"><span data-stu-id="91efd-258">True</span></span>                            |
| <span data-ttu-id="91efd-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="91efd-259">Is Indexed</span></span>             | <span data-ttu-id="91efd-260">Falso</span><span class="sxs-lookup"><span data-stu-id="91efd-260">False</span></span>                           |
| <span data-ttu-id="91efd-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="91efd-261">In Global Catalog</span></span>      | <span data-ttu-id="91efd-262">Falso</span><span class="sxs-lookup"><span data-stu-id="91efd-262">False</span></span>                           |
| <span data-ttu-id="91efd-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="91efd-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="91efd-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="91efd-264">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="91efd-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91efd-265">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="91efd-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91efd-266">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="91efd-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91efd-267">Search-Flags</span></span>           | <span data-ttu-id="91efd-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91efd-268">0x00000000</span></span>                      |
| <span data-ttu-id="91efd-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91efd-269">System-Flags</span></span>           | <span data-ttu-id="91efd-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="91efd-270">0x08000014</span></span>                      |
| <span data-ttu-id="91efd-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="91efd-271">Classes used in</span></span>        | [<span data-ttu-id="91efd-272">**Início**</span><span class="sxs-lookup"><span data-stu-id="91efd-272">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="91efd-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="91efd-273">Windows Server 2012</span></span>



| <span data-ttu-id="91efd-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="91efd-274">Entry</span></span> | <span data-ttu-id="91efd-275">Valor</span><span class="sxs-lookup"><span data-stu-id="91efd-275">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="91efd-276">ID do link</span><span class="sxs-lookup"><span data-stu-id="91efd-276">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="91efd-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91efd-277">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="91efd-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="91efd-278">System-Only</span></span>            | <span data-ttu-id="91efd-279">True</span><span class="sxs-lookup"><span data-stu-id="91efd-279">True</span></span>                            |
| <span data-ttu-id="91efd-280">É de valor único</span><span class="sxs-lookup"><span data-stu-id="91efd-280">Is-Single-Valued</span></span>       | <span data-ttu-id="91efd-281">True</span><span class="sxs-lookup"><span data-stu-id="91efd-281">True</span></span>                            |
| <span data-ttu-id="91efd-282">É indexado</span><span class="sxs-lookup"><span data-stu-id="91efd-282">Is Indexed</span></span>             | <span data-ttu-id="91efd-283">Falso</span><span class="sxs-lookup"><span data-stu-id="91efd-283">False</span></span>                           |
| <span data-ttu-id="91efd-284">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="91efd-284">In Global Catalog</span></span>      | <span data-ttu-id="91efd-285">Falso</span><span class="sxs-lookup"><span data-stu-id="91efd-285">False</span></span>                           |
| <span data-ttu-id="91efd-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="91efd-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="91efd-287">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="91efd-287">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="91efd-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91efd-288">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="91efd-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91efd-289">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="91efd-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91efd-290">Search-Flags</span></span>           | <span data-ttu-id="91efd-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91efd-291">0x00000000</span></span>                      |
| <span data-ttu-id="91efd-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91efd-292">System-Flags</span></span>           | <span data-ttu-id="91efd-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="91efd-293">0x08000014</span></span>                      |
| <span data-ttu-id="91efd-294">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="91efd-294">Classes used in</span></span>        | [<span data-ttu-id="91efd-295">**Início**</span><span class="sxs-lookup"><span data-stu-id="91efd-295">**Top**</span></span>](c-top.md)<br/> |



 

 





