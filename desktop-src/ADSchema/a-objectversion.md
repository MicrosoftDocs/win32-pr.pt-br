---
title: Object-Version atributo
description: Isso pode ser usado para armazenar um número de versão para o objeto.
ms.assetid: 1aa8520b-c640-4ea2-9230-f28154bf69b0
ms.tgt_platform: multiple
keywords:
- Esquema de Object-Version do atributo AD
- Esquema de AD do atributo objectVersion
topic_type:
- apiref
api_name:
- Object-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f038f6286db575f4141c2e306086bb9a8faac71
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105750362"
---
# <a name="object-version-attribute"></a><span data-ttu-id="19f6d-105">Object-Version atributo</span><span class="sxs-lookup"><span data-stu-id="19f6d-105">Object-Version attribute</span></span>

<span data-ttu-id="19f6d-106">Isso pode ser usado para armazenar um número de versão para o objeto.</span><span class="sxs-lookup"><span data-stu-id="19f6d-106">This can be used to store a version number for the object.</span></span>



| <span data-ttu-id="19f6d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="19f6d-107">Entry</span></span> | <span data-ttu-id="19f6d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="19f6d-108">Value</span></span> |
|-------------------|----------------------------------------------------------------|
| <span data-ttu-id="19f6d-109">CN</span><span class="sxs-lookup"><span data-stu-id="19f6d-109">CN</span></span>                | <span data-ttu-id="19f6d-110">Object-Version</span><span class="sxs-lookup"><span data-stu-id="19f6d-110">Object-Version</span></span>                                                 |
| <span data-ttu-id="19f6d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="19f6d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="19f6d-112">objectVersion</span><span class="sxs-lookup"><span data-stu-id="19f6d-112">objectVersion</span></span>                                                  |
| <span data-ttu-id="19f6d-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="19f6d-113">Size</span></span>              | <span data-ttu-id="19f6d-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="19f6d-114">4 bytes</span></span>                                                        |
| <span data-ttu-id="19f6d-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="19f6d-115">Update Privilege</span></span>  | <span data-ttu-id="19f6d-116">O designer do objeto definiria esse valor.</span><span class="sxs-lookup"><span data-stu-id="19f6d-116">The designer of the object would set this value.</span></span>               |
| <span data-ttu-id="19f6d-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="19f6d-117">Update Frequency</span></span>  | <span data-ttu-id="19f6d-118">Esse valor deve ser incrementado toda vez que o objeto for alterado.</span><span class="sxs-lookup"><span data-stu-id="19f6d-118">This value should be incremented each time the object changes.</span></span> |
| <span data-ttu-id="19f6d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="19f6d-119">Attribute-Id</span></span>      | <span data-ttu-id="19f6d-120">1.2.840.113556.1.2.76</span><span class="sxs-lookup"><span data-stu-id="19f6d-120">1.2.840.113556.1.2.76</span></span>                                          |
| <span data-ttu-id="19f6d-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="19f6d-121">System-Id-Guid</span></span>    | <span data-ttu-id="19f6d-122">16775848-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="19f6d-122">16775848-47f3-11d1-a9c3-0000f80367c1</span></span>                           |
| <span data-ttu-id="19f6d-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="19f6d-123">Syntax</span></span>            | [<span data-ttu-id="19f6d-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="19f6d-124">**Enumeration**</span></span>](s-enumeration.md)                           |



## <a name="implementations"></a><span data-ttu-id="19f6d-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="19f6d-125">Implementations</span></span>

-   [<span data-ttu-id="19f6d-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="19f6d-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="19f6d-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="19f6d-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="19f6d-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="19f6d-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="19f6d-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="19f6d-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="19f6d-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="19f6d-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="19f6d-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="19f6d-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="19f6d-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="19f6d-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="19f6d-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="19f6d-133">Windows 2000 Server</span></span>



| <span data-ttu-id="19f6d-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="19f6d-134">Entry</span></span> | <span data-ttu-id="19f6d-135">Valor</span><span class="sxs-lookup"><span data-stu-id="19f6d-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="19f6d-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="19f6d-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="19f6d-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f6d-137">MAPI-Id</span></span>                | <span data-ttu-id="19f6d-138">0x80F7</span><span class="sxs-lookup"><span data-stu-id="19f6d-138">0x80F7</span></span>                          |
| <span data-ttu-id="19f6d-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f6d-139">System-Only</span></span>            | <span data-ttu-id="19f6d-140">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-140">False</span></span>                           |
| <span data-ttu-id="19f6d-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="19f6d-141">Is-Single-Valued</span></span>       | <span data-ttu-id="19f6d-142">True</span><span class="sxs-lookup"><span data-stu-id="19f6d-142">True</span></span>                            |
| <span data-ttu-id="19f6d-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="19f6d-143">Is Indexed</span></span>             | <span data-ttu-id="19f6d-144">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-144">False</span></span>                           |
| <span data-ttu-id="19f6d-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="19f6d-145">In Global Catalog</span></span>      | <span data-ttu-id="19f6d-146">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-146">False</span></span>                           |
| <span data-ttu-id="19f6d-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19f6d-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f6d-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="19f6d-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="19f6d-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f6d-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="19f6d-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f6d-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="19f6d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f6d-151">Search-Flags</span></span>           | <span data-ttu-id="19f6d-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19f6d-152">0x00000000</span></span>                      |
| <span data-ttu-id="19f6d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f6d-153">System-Flags</span></span>           | <span data-ttu-id="19f6d-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f6d-154">0x00000010</span></span>                      |
| <span data-ttu-id="19f6d-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="19f6d-155">Classes used in</span></span>        | [<span data-ttu-id="19f6d-156">**Início**</span><span class="sxs-lookup"><span data-stu-id="19f6d-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="19f6d-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="19f6d-157">Windows Server 2003</span></span>



| <span data-ttu-id="19f6d-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="19f6d-158">Entry</span></span> | <span data-ttu-id="19f6d-159">Valor</span><span class="sxs-lookup"><span data-stu-id="19f6d-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="19f6d-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="19f6d-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="19f6d-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f6d-161">MAPI-Id</span></span>                | <span data-ttu-id="19f6d-162">0x80F7</span><span class="sxs-lookup"><span data-stu-id="19f6d-162">0x80F7</span></span>                          |
| <span data-ttu-id="19f6d-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f6d-163">System-Only</span></span>            | <span data-ttu-id="19f6d-164">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-164">False</span></span>                           |
| <span data-ttu-id="19f6d-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="19f6d-165">Is-Single-Valued</span></span>       | <span data-ttu-id="19f6d-166">True</span><span class="sxs-lookup"><span data-stu-id="19f6d-166">True</span></span>                            |
| <span data-ttu-id="19f6d-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="19f6d-167">Is Indexed</span></span>             | <span data-ttu-id="19f6d-168">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-168">False</span></span>                           |
| <span data-ttu-id="19f6d-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="19f6d-169">In Global Catalog</span></span>      | <span data-ttu-id="19f6d-170">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-170">False</span></span>                           |
| <span data-ttu-id="19f6d-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19f6d-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f6d-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="19f6d-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="19f6d-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f6d-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="19f6d-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f6d-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="19f6d-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f6d-175">Search-Flags</span></span>           | <span data-ttu-id="19f6d-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19f6d-176">0x00000000</span></span>                      |
| <span data-ttu-id="19f6d-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f6d-177">System-Flags</span></span>           | <span data-ttu-id="19f6d-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f6d-178">0x00000010</span></span>                      |
| <span data-ttu-id="19f6d-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="19f6d-179">Classes used in</span></span>        | [<span data-ttu-id="19f6d-180">**Início**</span><span class="sxs-lookup"><span data-stu-id="19f6d-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="19f6d-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="19f6d-181">ADAM</span></span>



| <span data-ttu-id="19f6d-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="19f6d-182">Entry</span></span> | <span data-ttu-id="19f6d-183">Valor</span><span class="sxs-lookup"><span data-stu-id="19f6d-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="19f6d-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="19f6d-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="19f6d-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f6d-185">MAPI-Id</span></span>                | <span data-ttu-id="19f6d-186">0x80F7</span><span class="sxs-lookup"><span data-stu-id="19f6d-186">0x80F7</span></span>                          |
| <span data-ttu-id="19f6d-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f6d-187">System-Only</span></span>            | <span data-ttu-id="19f6d-188">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-188">False</span></span>                           |
| <span data-ttu-id="19f6d-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="19f6d-189">Is-Single-Valued</span></span>       | <span data-ttu-id="19f6d-190">True</span><span class="sxs-lookup"><span data-stu-id="19f6d-190">True</span></span>                            |
| <span data-ttu-id="19f6d-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="19f6d-191">Is Indexed</span></span>             | <span data-ttu-id="19f6d-192">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-192">False</span></span>                           |
| <span data-ttu-id="19f6d-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="19f6d-193">In Global Catalog</span></span>      | <span data-ttu-id="19f6d-194">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-194">False</span></span>                           |
| <span data-ttu-id="19f6d-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19f6d-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f6d-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="19f6d-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="19f6d-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f6d-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="19f6d-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f6d-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="19f6d-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f6d-199">Search-Flags</span></span>           | <span data-ttu-id="19f6d-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19f6d-200">0x00000000</span></span>                      |
| <span data-ttu-id="19f6d-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f6d-201">System-Flags</span></span>           | <span data-ttu-id="19f6d-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f6d-202">0x00000010</span></span>                      |
| <span data-ttu-id="19f6d-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="19f6d-203">Classes used in</span></span>        | [<span data-ttu-id="19f6d-204">**Início**</span><span class="sxs-lookup"><span data-stu-id="19f6d-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="19f6d-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="19f6d-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="19f6d-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="19f6d-206">Entry</span></span> | <span data-ttu-id="19f6d-207">Valor</span><span class="sxs-lookup"><span data-stu-id="19f6d-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="19f6d-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="19f6d-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="19f6d-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f6d-209">MAPI-Id</span></span>                | <span data-ttu-id="19f6d-210">0x80F7</span><span class="sxs-lookup"><span data-stu-id="19f6d-210">0x80F7</span></span>                          |
| <span data-ttu-id="19f6d-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f6d-211">System-Only</span></span>            | <span data-ttu-id="19f6d-212">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-212">False</span></span>                           |
| <span data-ttu-id="19f6d-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="19f6d-213">Is-Single-Valued</span></span>       | <span data-ttu-id="19f6d-214">True</span><span class="sxs-lookup"><span data-stu-id="19f6d-214">True</span></span>                            |
| <span data-ttu-id="19f6d-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="19f6d-215">Is Indexed</span></span>             | <span data-ttu-id="19f6d-216">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-216">False</span></span>                           |
| <span data-ttu-id="19f6d-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="19f6d-217">In Global Catalog</span></span>      | <span data-ttu-id="19f6d-218">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-218">False</span></span>                           |
| <span data-ttu-id="19f6d-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19f6d-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f6d-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="19f6d-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="19f6d-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f6d-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="19f6d-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f6d-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="19f6d-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f6d-223">Search-Flags</span></span>           | <span data-ttu-id="19f6d-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19f6d-224">0x00000000</span></span>                      |
| <span data-ttu-id="19f6d-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f6d-225">System-Flags</span></span>           | <span data-ttu-id="19f6d-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f6d-226">0x00000010</span></span>                      |
| <span data-ttu-id="19f6d-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="19f6d-227">Classes used in</span></span>        | [<span data-ttu-id="19f6d-228">**Início**</span><span class="sxs-lookup"><span data-stu-id="19f6d-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="19f6d-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19f6d-229">Windows Server 2008</span></span>



| <span data-ttu-id="19f6d-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="19f6d-230">Entry</span></span> | <span data-ttu-id="19f6d-231">Valor</span><span class="sxs-lookup"><span data-stu-id="19f6d-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="19f6d-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="19f6d-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="19f6d-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f6d-233">MAPI-Id</span></span>                | <span data-ttu-id="19f6d-234">0x80F7</span><span class="sxs-lookup"><span data-stu-id="19f6d-234">0x80F7</span></span>                          |
| <span data-ttu-id="19f6d-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f6d-235">System-Only</span></span>            | <span data-ttu-id="19f6d-236">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-236">False</span></span>                           |
| <span data-ttu-id="19f6d-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="19f6d-237">Is-Single-Valued</span></span>       | <span data-ttu-id="19f6d-238">True</span><span class="sxs-lookup"><span data-stu-id="19f6d-238">True</span></span>                            |
| <span data-ttu-id="19f6d-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="19f6d-239">Is Indexed</span></span>             | <span data-ttu-id="19f6d-240">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-240">False</span></span>                           |
| <span data-ttu-id="19f6d-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="19f6d-241">In Global Catalog</span></span>      | <span data-ttu-id="19f6d-242">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-242">False</span></span>                           |
| <span data-ttu-id="19f6d-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19f6d-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f6d-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="19f6d-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="19f6d-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f6d-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="19f6d-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f6d-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="19f6d-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f6d-247">Search-Flags</span></span>           | <span data-ttu-id="19f6d-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19f6d-248">0x00000000</span></span>                      |
| <span data-ttu-id="19f6d-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f6d-249">System-Flags</span></span>           | <span data-ttu-id="19f6d-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f6d-250">0x00000010</span></span>                      |
| <span data-ttu-id="19f6d-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="19f6d-251">Classes used in</span></span>        | [<span data-ttu-id="19f6d-252">**Início**</span><span class="sxs-lookup"><span data-stu-id="19f6d-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="19f6d-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="19f6d-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="19f6d-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="19f6d-254">Entry</span></span> | <span data-ttu-id="19f6d-255">Valor</span><span class="sxs-lookup"><span data-stu-id="19f6d-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="19f6d-256">ID do link</span><span class="sxs-lookup"><span data-stu-id="19f6d-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="19f6d-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f6d-257">MAPI-Id</span></span>                | <span data-ttu-id="19f6d-258">0x80F7</span><span class="sxs-lookup"><span data-stu-id="19f6d-258">0x80F7</span></span>                          |
| <span data-ttu-id="19f6d-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f6d-259">System-Only</span></span>            | <span data-ttu-id="19f6d-260">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-260">False</span></span>                           |
| <span data-ttu-id="19f6d-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="19f6d-261">Is-Single-Valued</span></span>       | <span data-ttu-id="19f6d-262">True</span><span class="sxs-lookup"><span data-stu-id="19f6d-262">True</span></span>                            |
| <span data-ttu-id="19f6d-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="19f6d-263">Is Indexed</span></span>             | <span data-ttu-id="19f6d-264">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-264">False</span></span>                           |
| <span data-ttu-id="19f6d-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="19f6d-265">In Global Catalog</span></span>      | <span data-ttu-id="19f6d-266">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-266">False</span></span>                           |
| <span data-ttu-id="19f6d-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19f6d-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f6d-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="19f6d-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="19f6d-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f6d-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="19f6d-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f6d-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="19f6d-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f6d-271">Search-Flags</span></span>           | <span data-ttu-id="19f6d-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19f6d-272">0x00000000</span></span>                      |
| <span data-ttu-id="19f6d-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f6d-273">System-Flags</span></span>           | <span data-ttu-id="19f6d-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f6d-274">0x00000010</span></span>                      |
| <span data-ttu-id="19f6d-275">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="19f6d-275">Classes used in</span></span>        | [<span data-ttu-id="19f6d-276">**Início**</span><span class="sxs-lookup"><span data-stu-id="19f6d-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="19f6d-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="19f6d-277">Windows Server 2012</span></span>



| <span data-ttu-id="19f6d-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="19f6d-278">Entry</span></span> | <span data-ttu-id="19f6d-279">Valor</span><span class="sxs-lookup"><span data-stu-id="19f6d-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="19f6d-280">ID do link</span><span class="sxs-lookup"><span data-stu-id="19f6d-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="19f6d-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f6d-281">MAPI-Id</span></span>                | <span data-ttu-id="19f6d-282">0x80F7</span><span class="sxs-lookup"><span data-stu-id="19f6d-282">0x80F7</span></span>                          |
| <span data-ttu-id="19f6d-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f6d-283">System-Only</span></span>            | <span data-ttu-id="19f6d-284">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-284">False</span></span>                           |
| <span data-ttu-id="19f6d-285">É de valor único</span><span class="sxs-lookup"><span data-stu-id="19f6d-285">Is-Single-Valued</span></span>       | <span data-ttu-id="19f6d-286">True</span><span class="sxs-lookup"><span data-stu-id="19f6d-286">True</span></span>                            |
| <span data-ttu-id="19f6d-287">É indexado</span><span class="sxs-lookup"><span data-stu-id="19f6d-287">Is Indexed</span></span>             | <span data-ttu-id="19f6d-288">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-288">False</span></span>                           |
| <span data-ttu-id="19f6d-289">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="19f6d-289">In Global Catalog</span></span>      | <span data-ttu-id="19f6d-290">Falso</span><span class="sxs-lookup"><span data-stu-id="19f6d-290">False</span></span>                           |
| <span data-ttu-id="19f6d-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19f6d-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f6d-292">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="19f6d-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="19f6d-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f6d-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="19f6d-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f6d-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="19f6d-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f6d-295">Search-Flags</span></span>           | <span data-ttu-id="19f6d-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19f6d-296">0x00000000</span></span>                      |
| <span data-ttu-id="19f6d-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f6d-297">System-Flags</span></span>           | <span data-ttu-id="19f6d-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f6d-298">0x00000010</span></span>                      |
| <span data-ttu-id="19f6d-299">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="19f6d-299">Classes used in</span></span>        | [<span data-ttu-id="19f6d-300">**Início**</span><span class="sxs-lookup"><span data-stu-id="19f6d-300">**Top**</span></span>](c-top.md)<br/> |



 

 





