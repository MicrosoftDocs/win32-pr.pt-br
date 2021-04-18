---
title: USN-Created atributo
description: O número de sequência de atualização (USN) atribuído na criação do objeto. Consulte também, USN-alterado.
ms.assetid: c38456b8-fc8f-4ea0-8f3d-e2bb3b44ff50
ms.tgt_platform: multiple
keywords:
- Esquema de USN-Created do atributo AD
- Esquema de AD do atributo uSNCreated
topic_type:
- apiref
api_name:
- USN-Created
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b950ddfe261de5d46980e51b236da0f775fcb01b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105756080"
---
# <a name="usn-created-attribute"></a><span data-ttu-id="8fae0-106">USN-Created atributo</span><span class="sxs-lookup"><span data-stu-id="8fae0-106">USN-Created attribute</span></span>

<span data-ttu-id="8fae0-107">O número de sequência de atualização (USN) atribuído na criação do objeto.</span><span class="sxs-lookup"><span data-stu-id="8fae0-107">The update sequence number (USN) assigned at object creation.</span></span> <span data-ttu-id="8fae0-108">Consulte também, [**USN-alterado**](a-usnchanged.md).</span><span class="sxs-lookup"><span data-stu-id="8fae0-108">See also, [**USN-Changed**](a-usnchanged.md).</span></span>



| <span data-ttu-id="8fae0-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fae0-109">Entry</span></span> | <span data-ttu-id="8fae0-110">Valor</span><span class="sxs-lookup"><span data-stu-id="8fae0-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8fae0-111">CN</span><span class="sxs-lookup"><span data-stu-id="8fae0-111">CN</span></span>                | <span data-ttu-id="8fae0-112">USN-Created</span><span class="sxs-lookup"><span data-stu-id="8fae0-112">USN-Created</span></span>                          |
| <span data-ttu-id="8fae0-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8fae0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8fae0-114">uSNCreated</span><span class="sxs-lookup"><span data-stu-id="8fae0-114">uSNCreated</span></span>                           |
| <span data-ttu-id="8fae0-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="8fae0-115">Size</span></span>              | <span data-ttu-id="8fae0-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="8fae0-116">8 bytes</span></span>                              |
| <span data-ttu-id="8fae0-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="8fae0-117">Update Privilege</span></span>  | <span data-ttu-id="8fae0-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="8fae0-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="8fae0-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="8fae0-119">Update Frequency</span></span>  | <span data-ttu-id="8fae0-120">Quando o objeto é criado.</span><span class="sxs-lookup"><span data-stu-id="8fae0-120">When the object is created.</span></span>          |
| <span data-ttu-id="8fae0-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8fae0-121">Attribute-Id</span></span>      | <span data-ttu-id="8fae0-122">1.2.840.113556.1.2.19</span><span class="sxs-lookup"><span data-stu-id="8fae0-122">1.2.840.113556.1.2.19</span></span>                |
| <span data-ttu-id="8fae0-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8fae0-123">System-Id-Guid</span></span>    | <span data-ttu-id="8fae0-124">bf967a70-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8fae0-124">bf967a70-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="8fae0-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fae0-125">Syntax</span></span>            | [<span data-ttu-id="8fae0-126">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="8fae0-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="8fae0-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="8fae0-127">Implementations</span></span>

-   [<span data-ttu-id="8fae0-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8fae0-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8fae0-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8fae0-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8fae0-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8fae0-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8fae0-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8fae0-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8fae0-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8fae0-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8fae0-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8fae0-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8fae0-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8fae0-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8fae0-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8fae0-135">Windows 2000 Server</span></span>



| <span data-ttu-id="8fae0-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fae0-136">Entry</span></span> | <span data-ttu-id="8fae0-137">Valor</span><span class="sxs-lookup"><span data-stu-id="8fae0-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8fae0-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fae0-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8fae0-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fae0-139">MAPI-Id</span></span>                | <span data-ttu-id="8fae0-140">0x8154</span><span class="sxs-lookup"><span data-stu-id="8fae0-140">0x8154</span></span>                          |
| <span data-ttu-id="8fae0-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fae0-141">System-Only</span></span>            | <span data-ttu-id="8fae0-142">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-142">True</span></span>                            |
| <span data-ttu-id="8fae0-143">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fae0-143">Is-Single-Valued</span></span>       | <span data-ttu-id="8fae0-144">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-144">True</span></span>                            |
| <span data-ttu-id="8fae0-145">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fae0-145">Is Indexed</span></span>             | <span data-ttu-id="8fae0-146">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-146">True</span></span>                            |
| <span data-ttu-id="8fae0-147">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fae0-147">In Global Catalog</span></span>      | <span data-ttu-id="8fae0-148">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-148">True</span></span>                            |
| <span data-ttu-id="8fae0-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fae0-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fae0-150">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fae0-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8fae0-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fae0-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8fae0-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fae0-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8fae0-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fae0-153">Search-Flags</span></span>           | <span data-ttu-id="8fae0-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="8fae0-154">0x00000009</span></span>                      |
| <span data-ttu-id="8fae0-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fae0-155">System-Flags</span></span>           | <span data-ttu-id="8fae0-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="8fae0-156">0x00000013</span></span>                      |
| <span data-ttu-id="8fae0-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fae0-157">Classes used in</span></span>        | [<span data-ttu-id="8fae0-158">**Início**</span><span class="sxs-lookup"><span data-stu-id="8fae0-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8fae0-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8fae0-159">Windows Server 2003</span></span>



| <span data-ttu-id="8fae0-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fae0-160">Entry</span></span> | <span data-ttu-id="8fae0-161">Valor</span><span class="sxs-lookup"><span data-stu-id="8fae0-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8fae0-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fae0-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8fae0-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fae0-163">MAPI-Id</span></span>                | <span data-ttu-id="8fae0-164">0x8154</span><span class="sxs-lookup"><span data-stu-id="8fae0-164">0x8154</span></span>                          |
| <span data-ttu-id="8fae0-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fae0-165">System-Only</span></span>            | <span data-ttu-id="8fae0-166">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-166">True</span></span>                            |
| <span data-ttu-id="8fae0-167">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fae0-167">Is-Single-Valued</span></span>       | <span data-ttu-id="8fae0-168">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-168">True</span></span>                            |
| <span data-ttu-id="8fae0-169">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fae0-169">Is Indexed</span></span>             | <span data-ttu-id="8fae0-170">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-170">True</span></span>                            |
| <span data-ttu-id="8fae0-171">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fae0-171">In Global Catalog</span></span>      | <span data-ttu-id="8fae0-172">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-172">True</span></span>                            |
| <span data-ttu-id="8fae0-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fae0-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fae0-174">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fae0-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8fae0-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fae0-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8fae0-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fae0-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8fae0-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fae0-177">Search-Flags</span></span>           | <span data-ttu-id="8fae0-178">0x00000009</span><span class="sxs-lookup"><span data-stu-id="8fae0-178">0x00000009</span></span>                      |
| <span data-ttu-id="8fae0-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fae0-179">System-Flags</span></span>           | <span data-ttu-id="8fae0-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="8fae0-180">0x00000013</span></span>                      |
| <span data-ttu-id="8fae0-181">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fae0-181">Classes used in</span></span>        | [<span data-ttu-id="8fae0-182">**Início**</span><span class="sxs-lookup"><span data-stu-id="8fae0-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8fae0-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="8fae0-183">ADAM</span></span>



| <span data-ttu-id="8fae0-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fae0-184">Entry</span></span> | <span data-ttu-id="8fae0-185">Valor</span><span class="sxs-lookup"><span data-stu-id="8fae0-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8fae0-186">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fae0-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8fae0-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fae0-187">MAPI-Id</span></span>                | <span data-ttu-id="8fae0-188">0x8154</span><span class="sxs-lookup"><span data-stu-id="8fae0-188">0x8154</span></span>                          |
| <span data-ttu-id="8fae0-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fae0-189">System-Only</span></span>            | <span data-ttu-id="8fae0-190">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-190">True</span></span>                            |
| <span data-ttu-id="8fae0-191">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fae0-191">Is-Single-Valued</span></span>       | <span data-ttu-id="8fae0-192">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-192">True</span></span>                            |
| <span data-ttu-id="8fae0-193">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fae0-193">Is Indexed</span></span>             | <span data-ttu-id="8fae0-194">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-194">True</span></span>                            |
| <span data-ttu-id="8fae0-195">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fae0-195">In Global Catalog</span></span>      | <span data-ttu-id="8fae0-196">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-196">True</span></span>                            |
| <span data-ttu-id="8fae0-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fae0-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fae0-198">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fae0-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8fae0-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fae0-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8fae0-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fae0-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8fae0-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fae0-201">Search-Flags</span></span>           | <span data-ttu-id="8fae0-202">0x00000009</span><span class="sxs-lookup"><span data-stu-id="8fae0-202">0x00000009</span></span>                      |
| <span data-ttu-id="8fae0-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fae0-203">System-Flags</span></span>           | <span data-ttu-id="8fae0-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="8fae0-204">0x00000013</span></span>                      |
| <span data-ttu-id="8fae0-205">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fae0-205">Classes used in</span></span>        | [<span data-ttu-id="8fae0-206">**Início**</span><span class="sxs-lookup"><span data-stu-id="8fae0-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8fae0-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8fae0-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8fae0-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fae0-208">Entry</span></span> | <span data-ttu-id="8fae0-209">Valor</span><span class="sxs-lookup"><span data-stu-id="8fae0-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8fae0-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fae0-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8fae0-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fae0-211">MAPI-Id</span></span>                | <span data-ttu-id="8fae0-212">0x8154</span><span class="sxs-lookup"><span data-stu-id="8fae0-212">0x8154</span></span>                          |
| <span data-ttu-id="8fae0-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fae0-213">System-Only</span></span>            | <span data-ttu-id="8fae0-214">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-214">True</span></span>                            |
| <span data-ttu-id="8fae0-215">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fae0-215">Is-Single-Valued</span></span>       | <span data-ttu-id="8fae0-216">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-216">True</span></span>                            |
| <span data-ttu-id="8fae0-217">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fae0-217">Is Indexed</span></span>             | <span data-ttu-id="8fae0-218">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-218">True</span></span>                            |
| <span data-ttu-id="8fae0-219">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fae0-219">In Global Catalog</span></span>      | <span data-ttu-id="8fae0-220">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-220">True</span></span>                            |
| <span data-ttu-id="8fae0-221">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fae0-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fae0-222">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fae0-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8fae0-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fae0-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8fae0-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fae0-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8fae0-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fae0-225">Search-Flags</span></span>           | <span data-ttu-id="8fae0-226">0x00000009</span><span class="sxs-lookup"><span data-stu-id="8fae0-226">0x00000009</span></span>                      |
| <span data-ttu-id="8fae0-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fae0-227">System-Flags</span></span>           | <span data-ttu-id="8fae0-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="8fae0-228">0x00000013</span></span>                      |
| <span data-ttu-id="8fae0-229">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fae0-229">Classes used in</span></span>        | [<span data-ttu-id="8fae0-230">**Início**</span><span class="sxs-lookup"><span data-stu-id="8fae0-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8fae0-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fae0-231">Windows Server 2008</span></span>



| <span data-ttu-id="8fae0-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fae0-232">Entry</span></span> | <span data-ttu-id="8fae0-233">Valor</span><span class="sxs-lookup"><span data-stu-id="8fae0-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8fae0-234">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fae0-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8fae0-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fae0-235">MAPI-Id</span></span>                | <span data-ttu-id="8fae0-236">0x8154</span><span class="sxs-lookup"><span data-stu-id="8fae0-236">0x8154</span></span>                          |
| <span data-ttu-id="8fae0-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fae0-237">System-Only</span></span>            | <span data-ttu-id="8fae0-238">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-238">True</span></span>                            |
| <span data-ttu-id="8fae0-239">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fae0-239">Is-Single-Valued</span></span>       | <span data-ttu-id="8fae0-240">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-240">True</span></span>                            |
| <span data-ttu-id="8fae0-241">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fae0-241">Is Indexed</span></span>             | <span data-ttu-id="8fae0-242">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-242">True</span></span>                            |
| <span data-ttu-id="8fae0-243">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fae0-243">In Global Catalog</span></span>      | <span data-ttu-id="8fae0-244">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-244">True</span></span>                            |
| <span data-ttu-id="8fae0-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fae0-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fae0-246">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fae0-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8fae0-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fae0-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8fae0-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fae0-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8fae0-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fae0-249">Search-Flags</span></span>           | <span data-ttu-id="8fae0-250">0x00000009</span><span class="sxs-lookup"><span data-stu-id="8fae0-250">0x00000009</span></span>                      |
| <span data-ttu-id="8fae0-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fae0-251">System-Flags</span></span>           | <span data-ttu-id="8fae0-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="8fae0-252">0x00000013</span></span>                      |
| <span data-ttu-id="8fae0-253">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fae0-253">Classes used in</span></span>        | [<span data-ttu-id="8fae0-254">**Início**</span><span class="sxs-lookup"><span data-stu-id="8fae0-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8fae0-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8fae0-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8fae0-256">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fae0-256">Entry</span></span> | <span data-ttu-id="8fae0-257">Valor</span><span class="sxs-lookup"><span data-stu-id="8fae0-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8fae0-258">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fae0-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8fae0-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fae0-259">MAPI-Id</span></span>                | <span data-ttu-id="8fae0-260">0x8154</span><span class="sxs-lookup"><span data-stu-id="8fae0-260">0x8154</span></span>                          |
| <span data-ttu-id="8fae0-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fae0-261">System-Only</span></span>            | <span data-ttu-id="8fae0-262">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-262">True</span></span>                            |
| <span data-ttu-id="8fae0-263">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fae0-263">Is-Single-Valued</span></span>       | <span data-ttu-id="8fae0-264">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-264">True</span></span>                            |
| <span data-ttu-id="8fae0-265">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fae0-265">Is Indexed</span></span>             | <span data-ttu-id="8fae0-266">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-266">True</span></span>                            |
| <span data-ttu-id="8fae0-267">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fae0-267">In Global Catalog</span></span>      | <span data-ttu-id="8fae0-268">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-268">True</span></span>                            |
| <span data-ttu-id="8fae0-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fae0-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fae0-270">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fae0-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8fae0-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fae0-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8fae0-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fae0-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8fae0-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fae0-273">Search-Flags</span></span>           | <span data-ttu-id="8fae0-274">0x00000009</span><span class="sxs-lookup"><span data-stu-id="8fae0-274">0x00000009</span></span>                      |
| <span data-ttu-id="8fae0-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fae0-275">System-Flags</span></span>           | <span data-ttu-id="8fae0-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="8fae0-276">0x00000013</span></span>                      |
| <span data-ttu-id="8fae0-277">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fae0-277">Classes used in</span></span>        | [<span data-ttu-id="8fae0-278">**Início**</span><span class="sxs-lookup"><span data-stu-id="8fae0-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8fae0-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8fae0-279">Windows Server 2012</span></span>



| <span data-ttu-id="8fae0-280">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fae0-280">Entry</span></span> | <span data-ttu-id="8fae0-281">Valor</span><span class="sxs-lookup"><span data-stu-id="8fae0-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8fae0-282">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fae0-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8fae0-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fae0-283">MAPI-Id</span></span>                | <span data-ttu-id="8fae0-284">0x8154</span><span class="sxs-lookup"><span data-stu-id="8fae0-284">0x8154</span></span>                          |
| <span data-ttu-id="8fae0-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fae0-285">System-Only</span></span>            | <span data-ttu-id="8fae0-286">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-286">True</span></span>                            |
| <span data-ttu-id="8fae0-287">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fae0-287">Is-Single-Valued</span></span>       | <span data-ttu-id="8fae0-288">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-288">True</span></span>                            |
| <span data-ttu-id="8fae0-289">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fae0-289">Is Indexed</span></span>             | <span data-ttu-id="8fae0-290">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-290">True</span></span>                            |
| <span data-ttu-id="8fae0-291">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fae0-291">In Global Catalog</span></span>      | <span data-ttu-id="8fae0-292">True</span><span class="sxs-lookup"><span data-stu-id="8fae0-292">True</span></span>                            |
| <span data-ttu-id="8fae0-293">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fae0-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fae0-294">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fae0-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8fae0-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fae0-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8fae0-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fae0-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8fae0-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fae0-297">Search-Flags</span></span>           | <span data-ttu-id="8fae0-298">0x00000009</span><span class="sxs-lookup"><span data-stu-id="8fae0-298">0x00000009</span></span>                      |
| <span data-ttu-id="8fae0-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fae0-299">System-Flags</span></span>           | <span data-ttu-id="8fae0-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="8fae0-300">0x00000013</span></span>                      |
| <span data-ttu-id="8fae0-301">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fae0-301">Classes used in</span></span>        | [<span data-ttu-id="8fae0-302">**Início**</span><span class="sxs-lookup"><span data-stu-id="8fae0-302">**Top**</span></span>](c-top.md)<br/> |



 

 





