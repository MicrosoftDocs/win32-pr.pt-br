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
# <a name="create-time-stamp-attribute"></a><span data-ttu-id="ead9b-106">Criar-atributo de carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="ead9b-106">Create-Time-Stamp attribute</span></span>

<span data-ttu-id="ead9b-107">A data em que este objeto foi criado.</span><span class="sxs-lookup"><span data-stu-id="ead9b-107">The date when this object was created.</span></span> <span data-ttu-id="ead9b-108">Esse valor é replicado.</span><span class="sxs-lookup"><span data-stu-id="ead9b-108">This value is replicated.</span></span>



| <span data-ttu-id="ead9b-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="ead9b-109">Entry</span></span> | <span data-ttu-id="ead9b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="ead9b-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="ead9b-111">CN</span><span class="sxs-lookup"><span data-stu-id="ead9b-111">CN</span></span>                | <span data-ttu-id="ead9b-112">Criação-carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="ead9b-112">Create-Time-Stamp</span></span>                                             |
| <span data-ttu-id="ead9b-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ead9b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ead9b-114">createtimestamp</span><span class="sxs-lookup"><span data-stu-id="ead9b-114">createTimeStamp</span></span>                                               |
| <span data-ttu-id="ead9b-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ead9b-115">Size</span></span>              | <span data-ttu-id="ead9b-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="ead9b-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="ead9b-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="ead9b-117">Update Privilege</span></span>  | <span data-ttu-id="ead9b-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="ead9b-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="ead9b-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="ead9b-119">Update Frequency</span></span>  | <span data-ttu-id="ead9b-120">Quando o objeto é criado.</span><span class="sxs-lookup"><span data-stu-id="ead9b-120">When the object is created.</span></span>                                   |
| <span data-ttu-id="ead9b-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ead9b-121">Attribute-Id</span></span>      | <span data-ttu-id="ead9b-122">2.5.18.1</span><span class="sxs-lookup"><span data-stu-id="ead9b-122">2.5.18.1</span></span>                                                      |
| <span data-ttu-id="ead9b-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ead9b-123">System-Id-Guid</span></span>    | <span data-ttu-id="ead9b-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="ead9b-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span></span>                          |
| <span data-ttu-id="ead9b-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="ead9b-125">Syntax</span></span>            | [<span data-ttu-id="ead9b-126">**Cadeia de caracteres (em tempo geral)**</span><span class="sxs-lookup"><span data-stu-id="ead9b-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="ead9b-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="ead9b-127">Implementations</span></span>

-   [<span data-ttu-id="ead9b-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ead9b-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ead9b-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ead9b-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ead9b-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ead9b-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ead9b-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ead9b-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ead9b-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ead9b-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ead9b-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ead9b-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ead9b-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ead9b-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ead9b-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ead9b-135">Windows 2000 Server</span></span>



| <span data-ttu-id="ead9b-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="ead9b-136">Entry</span></span> | <span data-ttu-id="ead9b-137">Valor</span><span class="sxs-lookup"><span data-stu-id="ead9b-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ead9b-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="ead9b-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ead9b-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead9b-139">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ead9b-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead9b-140">System-Only</span></span>            | <span data-ttu-id="ead9b-141">True</span><span class="sxs-lookup"><span data-stu-id="ead9b-141">True</span></span>                            |
| <span data-ttu-id="ead9b-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ead9b-142">Is-Single-Valued</span></span>       | <span data-ttu-id="ead9b-143">True</span><span class="sxs-lookup"><span data-stu-id="ead9b-143">True</span></span>                            |
| <span data-ttu-id="ead9b-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="ead9b-144">Is Indexed</span></span>             | <span data-ttu-id="ead9b-145">Falso</span><span class="sxs-lookup"><span data-stu-id="ead9b-145">False</span></span>                           |
| <span data-ttu-id="ead9b-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ead9b-146">In Global Catalog</span></span>      | <span data-ttu-id="ead9b-147">Falso</span><span class="sxs-lookup"><span data-stu-id="ead9b-147">False</span></span>                           |
| <span data-ttu-id="ead9b-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ead9b-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead9b-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ead9b-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ead9b-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead9b-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ead9b-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead9b-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ead9b-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead9b-152">Search-Flags</span></span>           | <span data-ttu-id="ead9b-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead9b-153">0x00000000</span></span>                      |
| <span data-ttu-id="ead9b-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead9b-154">System-Flags</span></span>           | <span data-ttu-id="ead9b-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ead9b-155">0x08000014</span></span>                      |
| <span data-ttu-id="ead9b-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ead9b-156">Classes used in</span></span>        | [<span data-ttu-id="ead9b-157">**Início**</span><span class="sxs-lookup"><span data-stu-id="ead9b-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ead9b-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ead9b-158">Windows Server 2003</span></span>



| <span data-ttu-id="ead9b-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="ead9b-159">Entry</span></span> | <span data-ttu-id="ead9b-160">Valor</span><span class="sxs-lookup"><span data-stu-id="ead9b-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ead9b-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="ead9b-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ead9b-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead9b-162">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ead9b-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead9b-163">System-Only</span></span>            | <span data-ttu-id="ead9b-164">True</span><span class="sxs-lookup"><span data-stu-id="ead9b-164">True</span></span>                            |
| <span data-ttu-id="ead9b-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ead9b-165">Is-Single-Valued</span></span>       | <span data-ttu-id="ead9b-166">True</span><span class="sxs-lookup"><span data-stu-id="ead9b-166">True</span></span>                            |
| <span data-ttu-id="ead9b-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="ead9b-167">Is Indexed</span></span>             | <span data-ttu-id="ead9b-168">Falso</span><span class="sxs-lookup"><span data-stu-id="ead9b-168">False</span></span>                           |
| <span data-ttu-id="ead9b-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ead9b-169">In Global Catalog</span></span>      | <span data-ttu-id="ead9b-170">Falso</span><span class="sxs-lookup"><span data-stu-id="ead9b-170">False</span></span>                           |
| <span data-ttu-id="ead9b-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ead9b-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead9b-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ead9b-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ead9b-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead9b-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ead9b-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead9b-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ead9b-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead9b-175">Search-Flags</span></span>           | <span data-ttu-id="ead9b-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead9b-176">0x00000000</span></span>                      |
| <span data-ttu-id="ead9b-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead9b-177">System-Flags</span></span>           | <span data-ttu-id="ead9b-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ead9b-178">0x08000014</span></span>                      |
| <span data-ttu-id="ead9b-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ead9b-179">Classes used in</span></span>        | [<span data-ttu-id="ead9b-180">**Início**</span><span class="sxs-lookup"><span data-stu-id="ead9b-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ead9b-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="ead9b-181">ADAM</span></span>



| <span data-ttu-id="ead9b-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="ead9b-182">Entry</span></span> | <span data-ttu-id="ead9b-183">Valor</span><span class="sxs-lookup"><span data-stu-id="ead9b-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ead9b-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="ead9b-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ead9b-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead9b-185">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ead9b-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead9b-186">System-Only</span></span>            | <span data-ttu-id="ead9b-187">True</span><span class="sxs-lookup"><span data-stu-id="ead9b-187">True</span></span>                            |
| <span data-ttu-id="ead9b-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ead9b-188">Is-Single-Valued</span></span>       | <span data-ttu-id="ead9b-189">True</span><span class="sxs-lookup"><span data-stu-id="ead9b-189">True</span></span>                            |
| <span data-ttu-id="ead9b-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="ead9b-190">Is Indexed</span></span>             | <span data-ttu-id="ead9b-191">Falso</span><span class="sxs-lookup"><span data-stu-id="ead9b-191">False</span></span>                           |
| <span data-ttu-id="ead9b-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ead9b-192">In Global Catalog</span></span>      | <span data-ttu-id="ead9b-193">Falso</span><span class="sxs-lookup"><span data-stu-id="ead9b-193">False</span></span>                           |
| <span data-ttu-id="ead9b-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ead9b-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead9b-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ead9b-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ead9b-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead9b-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ead9b-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead9b-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ead9b-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead9b-198">Search-Flags</span></span>           | <span data-ttu-id="ead9b-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead9b-199">0x00000000</span></span>                      |
| <span data-ttu-id="ead9b-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead9b-200">System-Flags</span></span>           | <span data-ttu-id="ead9b-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ead9b-201">0x08000014</span></span>                      |
| <span data-ttu-id="ead9b-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ead9b-202">Classes used in</span></span>        | [<span data-ttu-id="ead9b-203">**Início**</span><span class="sxs-lookup"><span data-stu-id="ead9b-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ead9b-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ead9b-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ead9b-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="ead9b-205">Entry</span></span> | <span data-ttu-id="ead9b-206">Valor</span><span class="sxs-lookup"><span data-stu-id="ead9b-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ead9b-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="ead9b-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ead9b-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead9b-208">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ead9b-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead9b-209">System-Only</span></span>            | <span data-ttu-id="ead9b-210">True</span><span class="sxs-lookup"><span data-stu-id="ead9b-210">True</span></span>                            |
| <span data-ttu-id="ead9b-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ead9b-211">Is-Single-Valued</span></span>       | <span data-ttu-id="ead9b-212">True</span><span class="sxs-lookup"><span data-stu-id="ead9b-212">True</span></span>                            |
| <span data-ttu-id="ead9b-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="ead9b-213">Is Indexed</span></span>             | <span data-ttu-id="ead9b-214">Falso</span><span class="sxs-lookup"><span data-stu-id="ead9b-214">False</span></span>                           |
| <span data-ttu-id="ead9b-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ead9b-215">In Global Catalog</span></span>      | <span data-ttu-id="ead9b-216">Falso</span><span class="sxs-lookup"><span data-stu-id="ead9b-216">False</span></span>                           |
| <span data-ttu-id="ead9b-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ead9b-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead9b-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ead9b-218">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ead9b-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead9b-219">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ead9b-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead9b-220">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ead9b-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead9b-221">Search-Flags</span></span>           | <span data-ttu-id="ead9b-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead9b-222">0x00000000</span></span>                      |
| <span data-ttu-id="ead9b-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead9b-223">System-Flags</span></span>           | <span data-ttu-id="ead9b-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ead9b-224">0x08000014</span></span>                      |
| <span data-ttu-id="ead9b-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ead9b-225">Classes used in</span></span>        | [<span data-ttu-id="ead9b-226">**Início**</span><span class="sxs-lookup"><span data-stu-id="ead9b-226">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ead9b-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ead9b-227">Windows Server 2008</span></span>



| <span data-ttu-id="ead9b-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="ead9b-228">Entry</span></span> | <span data-ttu-id="ead9b-229">Valor</span><span class="sxs-lookup"><span data-stu-id="ead9b-229">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ead9b-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="ead9b-230">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ead9b-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead9b-231">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ead9b-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead9b-232">System-Only</span></span>            | <span data-ttu-id="ead9b-233">True</span><span class="sxs-lookup"><span data-stu-id="ead9b-233">True</span></span>                            |
| <span data-ttu-id="ead9b-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ead9b-234">Is-Single-Valued</span></span>       | <span data-ttu-id="ead9b-235">True</span><span class="sxs-lookup"><span data-stu-id="ead9b-235">True</span></span>                            |
| <span data-ttu-id="ead9b-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="ead9b-236">Is Indexed</span></span>             | <span data-ttu-id="ead9b-237">Falso</span><span class="sxs-lookup"><span data-stu-id="ead9b-237">False</span></span>                           |
| <span data-ttu-id="ead9b-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ead9b-238">In Global Catalog</span></span>      | <span data-ttu-id="ead9b-239">Falso</span><span class="sxs-lookup"><span data-stu-id="ead9b-239">False</span></span>                           |
| <span data-ttu-id="ead9b-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ead9b-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead9b-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ead9b-241">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ead9b-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead9b-242">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ead9b-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead9b-243">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ead9b-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead9b-244">Search-Flags</span></span>           | <span data-ttu-id="ead9b-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead9b-245">0x00000000</span></span>                      |
| <span data-ttu-id="ead9b-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead9b-246">System-Flags</span></span>           | <span data-ttu-id="ead9b-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ead9b-247">0x08000014</span></span>                      |
| <span data-ttu-id="ead9b-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ead9b-248">Classes used in</span></span>        | [<span data-ttu-id="ead9b-249">**Início**</span><span class="sxs-lookup"><span data-stu-id="ead9b-249">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ead9b-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ead9b-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ead9b-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="ead9b-251">Entry</span></span> | <span data-ttu-id="ead9b-252">Valor</span><span class="sxs-lookup"><span data-stu-id="ead9b-252">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ead9b-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="ead9b-253">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ead9b-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead9b-254">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ead9b-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead9b-255">System-Only</span></span>            | <span data-ttu-id="ead9b-256">True</span><span class="sxs-lookup"><span data-stu-id="ead9b-256">True</span></span>                            |
| <span data-ttu-id="ead9b-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ead9b-257">Is-Single-Valued</span></span>       | <span data-ttu-id="ead9b-258">True</span><span class="sxs-lookup"><span data-stu-id="ead9b-258">True</span></span>                            |
| <span data-ttu-id="ead9b-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="ead9b-259">Is Indexed</span></span>             | <span data-ttu-id="ead9b-260">Falso</span><span class="sxs-lookup"><span data-stu-id="ead9b-260">False</span></span>                           |
| <span data-ttu-id="ead9b-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ead9b-261">In Global Catalog</span></span>      | <span data-ttu-id="ead9b-262">Falso</span><span class="sxs-lookup"><span data-stu-id="ead9b-262">False</span></span>                           |
| <span data-ttu-id="ead9b-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ead9b-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead9b-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ead9b-264">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ead9b-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead9b-265">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ead9b-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead9b-266">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ead9b-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead9b-267">Search-Flags</span></span>           | <span data-ttu-id="ead9b-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead9b-268">0x00000000</span></span>                      |
| <span data-ttu-id="ead9b-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead9b-269">System-Flags</span></span>           | <span data-ttu-id="ead9b-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ead9b-270">0x08000014</span></span>                      |
| <span data-ttu-id="ead9b-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ead9b-271">Classes used in</span></span>        | [<span data-ttu-id="ead9b-272">**Início**</span><span class="sxs-lookup"><span data-stu-id="ead9b-272">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ead9b-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ead9b-273">Windows Server 2012</span></span>



| <span data-ttu-id="ead9b-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="ead9b-274">Entry</span></span> | <span data-ttu-id="ead9b-275">Valor</span><span class="sxs-lookup"><span data-stu-id="ead9b-275">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ead9b-276">ID do link</span><span class="sxs-lookup"><span data-stu-id="ead9b-276">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ead9b-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead9b-277">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ead9b-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead9b-278">System-Only</span></span>            | <span data-ttu-id="ead9b-279">True</span><span class="sxs-lookup"><span data-stu-id="ead9b-279">True</span></span>                            |
| <span data-ttu-id="ead9b-280">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ead9b-280">Is-Single-Valued</span></span>       | <span data-ttu-id="ead9b-281">True</span><span class="sxs-lookup"><span data-stu-id="ead9b-281">True</span></span>                            |
| <span data-ttu-id="ead9b-282">É indexado</span><span class="sxs-lookup"><span data-stu-id="ead9b-282">Is Indexed</span></span>             | <span data-ttu-id="ead9b-283">Falso</span><span class="sxs-lookup"><span data-stu-id="ead9b-283">False</span></span>                           |
| <span data-ttu-id="ead9b-284">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ead9b-284">In Global Catalog</span></span>      | <span data-ttu-id="ead9b-285">Falso</span><span class="sxs-lookup"><span data-stu-id="ead9b-285">False</span></span>                           |
| <span data-ttu-id="ead9b-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ead9b-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead9b-287">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ead9b-287">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ead9b-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead9b-288">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ead9b-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead9b-289">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ead9b-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead9b-290">Search-Flags</span></span>           | <span data-ttu-id="ead9b-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ead9b-291">0x00000000</span></span>                      |
| <span data-ttu-id="ead9b-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead9b-292">System-Flags</span></span>           | <span data-ttu-id="ead9b-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="ead9b-293">0x08000014</span></span>                      |
| <span data-ttu-id="ead9b-294">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ead9b-294">Classes used in</span></span>        | [<span data-ttu-id="ead9b-295">**Início**</span><span class="sxs-lookup"><span data-stu-id="ead9b-295">**Top**</span></span>](c-top.md)<br/> |



 

 





