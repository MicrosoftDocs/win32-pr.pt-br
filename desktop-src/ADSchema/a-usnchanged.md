---
title: USN-Changed atributo
description: O USN (número de sequência de atualização) atribuído pelo diretório local para a alteração mais recente, incluindo a criação. Consulte também, criado pelo USN.
ms.assetid: ccd61940-2c0a-4d46-af9f-5f23f577a1ad
ms.tgt_platform: multiple
keywords:
- Esquema de USN-Changed do atributo AD
- Esquema de AD do atributo uSNChanged
topic_type:
- apiref
api_name:
- USN-Changed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c00f30a2ba7ca38f78246cd14b33ea358da6fa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645491"
---
# <a name="usn-changed-attribute"></a><span data-ttu-id="a42eb-106">USN-Changed atributo</span><span class="sxs-lookup"><span data-stu-id="a42eb-106">USN-Changed attribute</span></span>

<span data-ttu-id="a42eb-107">O USN (número de sequência de atualização) atribuído pelo diretório local para a alteração mais recente, incluindo a criação.</span><span class="sxs-lookup"><span data-stu-id="a42eb-107">The update sequence number (USN) assigned by the local directory for the latest change, including creation.</span></span> <span data-ttu-id="a42eb-108">Consulte também, [**criado pelo USN**](a-usncreated.md).</span><span class="sxs-lookup"><span data-stu-id="a42eb-108">See also , [**USN-Created**](a-usncreated.md).</span></span>



| <span data-ttu-id="a42eb-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="a42eb-109">Entry</span></span> | <span data-ttu-id="a42eb-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a42eb-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a42eb-111">CN</span><span class="sxs-lookup"><span data-stu-id="a42eb-111">CN</span></span>                | <span data-ttu-id="a42eb-112">USN-Changed</span><span class="sxs-lookup"><span data-stu-id="a42eb-112">USN-Changed</span></span>                          |
| <span data-ttu-id="a42eb-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a42eb-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a42eb-114">uSNChanged</span><span class="sxs-lookup"><span data-stu-id="a42eb-114">uSNChanged</span></span>                           |
| <span data-ttu-id="a42eb-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a42eb-115">Size</span></span>              | <span data-ttu-id="a42eb-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="a42eb-116">8 bytes</span></span>                              |
| <span data-ttu-id="a42eb-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a42eb-117">Update Privilege</span></span>  | <span data-ttu-id="a42eb-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="a42eb-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="a42eb-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a42eb-119">Update Frequency</span></span>  | <span data-ttu-id="a42eb-120">Quando o objeto é alterado.</span><span class="sxs-lookup"><span data-stu-id="a42eb-120">When the object is changed.</span></span>          |
| <span data-ttu-id="a42eb-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a42eb-121">Attribute-Id</span></span>      | <span data-ttu-id="a42eb-122">1.2.840.113556.1.2.120</span><span class="sxs-lookup"><span data-stu-id="a42eb-122">1.2.840.113556.1.2.120</span></span>               |
| <span data-ttu-id="a42eb-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a42eb-123">System-Id-Guid</span></span>    | <span data-ttu-id="a42eb-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a42eb-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="a42eb-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="a42eb-125">Syntax</span></span>            | [<span data-ttu-id="a42eb-126">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="a42eb-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="a42eb-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="a42eb-127">Implementations</span></span>

-   [<span data-ttu-id="a42eb-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a42eb-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a42eb-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a42eb-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a42eb-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a42eb-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a42eb-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a42eb-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a42eb-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a42eb-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a42eb-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a42eb-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a42eb-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a42eb-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a42eb-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a42eb-135">Windows 2000 Server</span></span>



| <span data-ttu-id="a42eb-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="a42eb-136">Entry</span></span> | <span data-ttu-id="a42eb-137">Valor</span><span class="sxs-lookup"><span data-stu-id="a42eb-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a42eb-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="a42eb-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a42eb-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a42eb-139">MAPI-Id</span></span>                | <span data-ttu-id="a42eb-140">0x8029</span><span class="sxs-lookup"><span data-stu-id="a42eb-140">0x8029</span></span>                          |
| <span data-ttu-id="a42eb-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="a42eb-141">System-Only</span></span>            | <span data-ttu-id="a42eb-142">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-142">True</span></span>                            |
| <span data-ttu-id="a42eb-143">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a42eb-143">Is-Single-Valued</span></span>       | <span data-ttu-id="a42eb-144">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-144">True</span></span>                            |
| <span data-ttu-id="a42eb-145">É indexado</span><span class="sxs-lookup"><span data-stu-id="a42eb-145">Is Indexed</span></span>             | <span data-ttu-id="a42eb-146">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-146">True</span></span>                            |
| <span data-ttu-id="a42eb-147">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a42eb-147">In Global Catalog</span></span>      | <span data-ttu-id="a42eb-148">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-148">True</span></span>                            |
| <span data-ttu-id="a42eb-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a42eb-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="a42eb-150">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a42eb-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a42eb-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a42eb-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a42eb-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a42eb-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a42eb-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a42eb-153">Search-Flags</span></span>           | <span data-ttu-id="a42eb-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="a42eb-154">0x00000009</span></span>                      |
| <span data-ttu-id="a42eb-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a42eb-155">System-Flags</span></span>           | <span data-ttu-id="a42eb-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a42eb-156">0x00000013</span></span>                      |
| <span data-ttu-id="a42eb-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a42eb-157">Classes used in</span></span>        | [<span data-ttu-id="a42eb-158">**Início**</span><span class="sxs-lookup"><span data-stu-id="a42eb-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a42eb-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a42eb-159">Windows Server 2003</span></span>



| <span data-ttu-id="a42eb-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="a42eb-160">Entry</span></span> | <span data-ttu-id="a42eb-161">Valor</span><span class="sxs-lookup"><span data-stu-id="a42eb-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a42eb-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="a42eb-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a42eb-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a42eb-163">MAPI-Id</span></span>                | <span data-ttu-id="a42eb-164">0x8029</span><span class="sxs-lookup"><span data-stu-id="a42eb-164">0x8029</span></span>                          |
| <span data-ttu-id="a42eb-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="a42eb-165">System-Only</span></span>            | <span data-ttu-id="a42eb-166">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-166">True</span></span>                            |
| <span data-ttu-id="a42eb-167">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a42eb-167">Is-Single-Valued</span></span>       | <span data-ttu-id="a42eb-168">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-168">True</span></span>                            |
| <span data-ttu-id="a42eb-169">É indexado</span><span class="sxs-lookup"><span data-stu-id="a42eb-169">Is Indexed</span></span>             | <span data-ttu-id="a42eb-170">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-170">True</span></span>                            |
| <span data-ttu-id="a42eb-171">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a42eb-171">In Global Catalog</span></span>      | <span data-ttu-id="a42eb-172">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-172">True</span></span>                            |
| <span data-ttu-id="a42eb-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a42eb-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="a42eb-174">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a42eb-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a42eb-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a42eb-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a42eb-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a42eb-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a42eb-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a42eb-177">Search-Flags</span></span>           | <span data-ttu-id="a42eb-178">0x00000009</span><span class="sxs-lookup"><span data-stu-id="a42eb-178">0x00000009</span></span>                      |
| <span data-ttu-id="a42eb-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a42eb-179">System-Flags</span></span>           | <span data-ttu-id="a42eb-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a42eb-180">0x00000013</span></span>                      |
| <span data-ttu-id="a42eb-181">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a42eb-181">Classes used in</span></span>        | [<span data-ttu-id="a42eb-182">**Início**</span><span class="sxs-lookup"><span data-stu-id="a42eb-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a42eb-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="a42eb-183">ADAM</span></span>



| <span data-ttu-id="a42eb-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="a42eb-184">Entry</span></span> | <span data-ttu-id="a42eb-185">Valor</span><span class="sxs-lookup"><span data-stu-id="a42eb-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a42eb-186">ID do link</span><span class="sxs-lookup"><span data-stu-id="a42eb-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a42eb-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a42eb-187">MAPI-Id</span></span>                | <span data-ttu-id="a42eb-188">0x8029</span><span class="sxs-lookup"><span data-stu-id="a42eb-188">0x8029</span></span>                          |
| <span data-ttu-id="a42eb-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="a42eb-189">System-Only</span></span>            | <span data-ttu-id="a42eb-190">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-190">True</span></span>                            |
| <span data-ttu-id="a42eb-191">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a42eb-191">Is-Single-Valued</span></span>       | <span data-ttu-id="a42eb-192">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-192">True</span></span>                            |
| <span data-ttu-id="a42eb-193">É indexado</span><span class="sxs-lookup"><span data-stu-id="a42eb-193">Is Indexed</span></span>             | <span data-ttu-id="a42eb-194">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-194">True</span></span>                            |
| <span data-ttu-id="a42eb-195">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a42eb-195">In Global Catalog</span></span>      | <span data-ttu-id="a42eb-196">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-196">True</span></span>                            |
| <span data-ttu-id="a42eb-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a42eb-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="a42eb-198">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a42eb-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a42eb-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a42eb-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a42eb-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a42eb-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a42eb-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a42eb-201">Search-Flags</span></span>           | <span data-ttu-id="a42eb-202">0x00000009</span><span class="sxs-lookup"><span data-stu-id="a42eb-202">0x00000009</span></span>                      |
| <span data-ttu-id="a42eb-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a42eb-203">System-Flags</span></span>           | <span data-ttu-id="a42eb-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a42eb-204">0x00000013</span></span>                      |
| <span data-ttu-id="a42eb-205">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a42eb-205">Classes used in</span></span>        | [<span data-ttu-id="a42eb-206">**Início**</span><span class="sxs-lookup"><span data-stu-id="a42eb-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a42eb-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a42eb-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a42eb-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="a42eb-208">Entry</span></span> | <span data-ttu-id="a42eb-209">Valor</span><span class="sxs-lookup"><span data-stu-id="a42eb-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a42eb-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="a42eb-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a42eb-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a42eb-211">MAPI-Id</span></span>                | <span data-ttu-id="a42eb-212">0x8029</span><span class="sxs-lookup"><span data-stu-id="a42eb-212">0x8029</span></span>                          |
| <span data-ttu-id="a42eb-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="a42eb-213">System-Only</span></span>            | <span data-ttu-id="a42eb-214">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-214">True</span></span>                            |
| <span data-ttu-id="a42eb-215">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a42eb-215">Is-Single-Valued</span></span>       | <span data-ttu-id="a42eb-216">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-216">True</span></span>                            |
| <span data-ttu-id="a42eb-217">É indexado</span><span class="sxs-lookup"><span data-stu-id="a42eb-217">Is Indexed</span></span>             | <span data-ttu-id="a42eb-218">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-218">True</span></span>                            |
| <span data-ttu-id="a42eb-219">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a42eb-219">In Global Catalog</span></span>      | <span data-ttu-id="a42eb-220">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-220">True</span></span>                            |
| <span data-ttu-id="a42eb-221">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a42eb-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="a42eb-222">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a42eb-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a42eb-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a42eb-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a42eb-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a42eb-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a42eb-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a42eb-225">Search-Flags</span></span>           | <span data-ttu-id="a42eb-226">0x00000009</span><span class="sxs-lookup"><span data-stu-id="a42eb-226">0x00000009</span></span>                      |
| <span data-ttu-id="a42eb-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a42eb-227">System-Flags</span></span>           | <span data-ttu-id="a42eb-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a42eb-228">0x00000013</span></span>                      |
| <span data-ttu-id="a42eb-229">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a42eb-229">Classes used in</span></span>        | [<span data-ttu-id="a42eb-230">**Início**</span><span class="sxs-lookup"><span data-stu-id="a42eb-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a42eb-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a42eb-231">Windows Server 2008</span></span>



| <span data-ttu-id="a42eb-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="a42eb-232">Entry</span></span> | <span data-ttu-id="a42eb-233">Valor</span><span class="sxs-lookup"><span data-stu-id="a42eb-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a42eb-234">ID do link</span><span class="sxs-lookup"><span data-stu-id="a42eb-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a42eb-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a42eb-235">MAPI-Id</span></span>                | <span data-ttu-id="a42eb-236">0x8029</span><span class="sxs-lookup"><span data-stu-id="a42eb-236">0x8029</span></span>                          |
| <span data-ttu-id="a42eb-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="a42eb-237">System-Only</span></span>            | <span data-ttu-id="a42eb-238">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-238">True</span></span>                            |
| <span data-ttu-id="a42eb-239">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a42eb-239">Is-Single-Valued</span></span>       | <span data-ttu-id="a42eb-240">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-240">True</span></span>                            |
| <span data-ttu-id="a42eb-241">É indexado</span><span class="sxs-lookup"><span data-stu-id="a42eb-241">Is Indexed</span></span>             | <span data-ttu-id="a42eb-242">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-242">True</span></span>                            |
| <span data-ttu-id="a42eb-243">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a42eb-243">In Global Catalog</span></span>      | <span data-ttu-id="a42eb-244">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-244">True</span></span>                            |
| <span data-ttu-id="a42eb-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a42eb-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="a42eb-246">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a42eb-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a42eb-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a42eb-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a42eb-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a42eb-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a42eb-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a42eb-249">Search-Flags</span></span>           | <span data-ttu-id="a42eb-250">0x00000009</span><span class="sxs-lookup"><span data-stu-id="a42eb-250">0x00000009</span></span>                      |
| <span data-ttu-id="a42eb-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a42eb-251">System-Flags</span></span>           | <span data-ttu-id="a42eb-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a42eb-252">0x00000013</span></span>                      |
| <span data-ttu-id="a42eb-253">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a42eb-253">Classes used in</span></span>        | [<span data-ttu-id="a42eb-254">**Início**</span><span class="sxs-lookup"><span data-stu-id="a42eb-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a42eb-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a42eb-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a42eb-256">Entrada</span><span class="sxs-lookup"><span data-stu-id="a42eb-256">Entry</span></span> | <span data-ttu-id="a42eb-257">Valor</span><span class="sxs-lookup"><span data-stu-id="a42eb-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a42eb-258">ID do link</span><span class="sxs-lookup"><span data-stu-id="a42eb-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a42eb-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a42eb-259">MAPI-Id</span></span>                | <span data-ttu-id="a42eb-260">0x8029</span><span class="sxs-lookup"><span data-stu-id="a42eb-260">0x8029</span></span>                          |
| <span data-ttu-id="a42eb-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="a42eb-261">System-Only</span></span>            | <span data-ttu-id="a42eb-262">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-262">True</span></span>                            |
| <span data-ttu-id="a42eb-263">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a42eb-263">Is-Single-Valued</span></span>       | <span data-ttu-id="a42eb-264">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-264">True</span></span>                            |
| <span data-ttu-id="a42eb-265">É indexado</span><span class="sxs-lookup"><span data-stu-id="a42eb-265">Is Indexed</span></span>             | <span data-ttu-id="a42eb-266">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-266">True</span></span>                            |
| <span data-ttu-id="a42eb-267">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a42eb-267">In Global Catalog</span></span>      | <span data-ttu-id="a42eb-268">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-268">True</span></span>                            |
| <span data-ttu-id="a42eb-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a42eb-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="a42eb-270">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a42eb-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a42eb-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a42eb-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a42eb-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a42eb-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a42eb-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a42eb-273">Search-Flags</span></span>           | <span data-ttu-id="a42eb-274">0x00000009</span><span class="sxs-lookup"><span data-stu-id="a42eb-274">0x00000009</span></span>                      |
| <span data-ttu-id="a42eb-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a42eb-275">System-Flags</span></span>           | <span data-ttu-id="a42eb-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a42eb-276">0x00000013</span></span>                      |
| <span data-ttu-id="a42eb-277">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a42eb-277">Classes used in</span></span>        | [<span data-ttu-id="a42eb-278">**Início**</span><span class="sxs-lookup"><span data-stu-id="a42eb-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a42eb-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a42eb-279">Windows Server 2012</span></span>



| <span data-ttu-id="a42eb-280">Entrada</span><span class="sxs-lookup"><span data-stu-id="a42eb-280">Entry</span></span> | <span data-ttu-id="a42eb-281">Valor</span><span class="sxs-lookup"><span data-stu-id="a42eb-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a42eb-282">ID do link</span><span class="sxs-lookup"><span data-stu-id="a42eb-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a42eb-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a42eb-283">MAPI-Id</span></span>                | <span data-ttu-id="a42eb-284">0x8029</span><span class="sxs-lookup"><span data-stu-id="a42eb-284">0x8029</span></span>                          |
| <span data-ttu-id="a42eb-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="a42eb-285">System-Only</span></span>            | <span data-ttu-id="a42eb-286">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-286">True</span></span>                            |
| <span data-ttu-id="a42eb-287">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a42eb-287">Is-Single-Valued</span></span>       | <span data-ttu-id="a42eb-288">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-288">True</span></span>                            |
| <span data-ttu-id="a42eb-289">É indexado</span><span class="sxs-lookup"><span data-stu-id="a42eb-289">Is Indexed</span></span>             | <span data-ttu-id="a42eb-290">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-290">True</span></span>                            |
| <span data-ttu-id="a42eb-291">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a42eb-291">In Global Catalog</span></span>      | <span data-ttu-id="a42eb-292">True</span><span class="sxs-lookup"><span data-stu-id="a42eb-292">True</span></span>                            |
| <span data-ttu-id="a42eb-293">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a42eb-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="a42eb-294">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a42eb-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a42eb-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a42eb-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a42eb-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a42eb-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a42eb-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a42eb-297">Search-Flags</span></span>           | <span data-ttu-id="a42eb-298">0x00000009</span><span class="sxs-lookup"><span data-stu-id="a42eb-298">0x00000009</span></span>                      |
| <span data-ttu-id="a42eb-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a42eb-299">System-Flags</span></span>           | <span data-ttu-id="a42eb-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="a42eb-300">0x00000013</span></span>                      |
| <span data-ttu-id="a42eb-301">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a42eb-301">Classes used in</span></span>        | [<span data-ttu-id="a42eb-302">**Início**</span><span class="sxs-lookup"><span data-stu-id="a42eb-302">**Top**</span></span>](c-top.md)<br/> |



 

 





