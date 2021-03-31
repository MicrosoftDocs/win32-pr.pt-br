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
# <a name="usn-changed-attribute"></a><span data-ttu-id="b8069-106">USN-Changed atributo</span><span class="sxs-lookup"><span data-stu-id="b8069-106">USN-Changed attribute</span></span>

<span data-ttu-id="b8069-107">O USN (número de sequência de atualização) atribuído pelo diretório local para a alteração mais recente, incluindo a criação.</span><span class="sxs-lookup"><span data-stu-id="b8069-107">The update sequence number (USN) assigned by the local directory for the latest change, including creation.</span></span> <span data-ttu-id="b8069-108">Consulte também, [**criado pelo USN**](a-usncreated.md).</span><span class="sxs-lookup"><span data-stu-id="b8069-108">See also , [**USN-Created**](a-usncreated.md).</span></span>



| <span data-ttu-id="b8069-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8069-109">Entry</span></span> | <span data-ttu-id="b8069-110">Valor</span><span class="sxs-lookup"><span data-stu-id="b8069-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b8069-111">CN</span><span class="sxs-lookup"><span data-stu-id="b8069-111">CN</span></span>                | <span data-ttu-id="b8069-112">USN-Changed</span><span class="sxs-lookup"><span data-stu-id="b8069-112">USN-Changed</span></span>                          |
| <span data-ttu-id="b8069-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b8069-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b8069-114">uSNChanged</span><span class="sxs-lookup"><span data-stu-id="b8069-114">uSNChanged</span></span>                           |
| <span data-ttu-id="b8069-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b8069-115">Size</span></span>              | <span data-ttu-id="b8069-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="b8069-116">8 bytes</span></span>                              |
| <span data-ttu-id="b8069-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="b8069-117">Update Privilege</span></span>  | <span data-ttu-id="b8069-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="b8069-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="b8069-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="b8069-119">Update Frequency</span></span>  | <span data-ttu-id="b8069-120">Quando o objeto é alterado.</span><span class="sxs-lookup"><span data-stu-id="b8069-120">When the object is changed.</span></span>          |
| <span data-ttu-id="b8069-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b8069-121">Attribute-Id</span></span>      | <span data-ttu-id="b8069-122">1.2.840.113556.1.2.120</span><span class="sxs-lookup"><span data-stu-id="b8069-122">1.2.840.113556.1.2.120</span></span>               |
| <span data-ttu-id="b8069-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b8069-123">System-Id-Guid</span></span>    | <span data-ttu-id="b8069-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b8069-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="b8069-125">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8069-125">Syntax</span></span>            | [<span data-ttu-id="b8069-126">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="b8069-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="b8069-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="b8069-127">Implementations</span></span>

-   [<span data-ttu-id="b8069-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b8069-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b8069-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b8069-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b8069-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b8069-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b8069-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b8069-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b8069-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b8069-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b8069-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b8069-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b8069-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b8069-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b8069-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b8069-135">Windows 2000 Server</span></span>



| <span data-ttu-id="b8069-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8069-136">Entry</span></span> | <span data-ttu-id="b8069-137">Valor</span><span class="sxs-lookup"><span data-stu-id="b8069-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8069-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8069-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8069-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8069-139">MAPI-Id</span></span>                | <span data-ttu-id="b8069-140">0x8029</span><span class="sxs-lookup"><span data-stu-id="b8069-140">0x8029</span></span>                          |
| <span data-ttu-id="b8069-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8069-141">System-Only</span></span>            | <span data-ttu-id="b8069-142">True</span><span class="sxs-lookup"><span data-stu-id="b8069-142">True</span></span>                            |
| <span data-ttu-id="b8069-143">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8069-143">Is-Single-Valued</span></span>       | <span data-ttu-id="b8069-144">True</span><span class="sxs-lookup"><span data-stu-id="b8069-144">True</span></span>                            |
| <span data-ttu-id="b8069-145">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8069-145">Is Indexed</span></span>             | <span data-ttu-id="b8069-146">True</span><span class="sxs-lookup"><span data-stu-id="b8069-146">True</span></span>                            |
| <span data-ttu-id="b8069-147">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8069-147">In Global Catalog</span></span>      | <span data-ttu-id="b8069-148">True</span><span class="sxs-lookup"><span data-stu-id="b8069-148">True</span></span>                            |
| <span data-ttu-id="b8069-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8069-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8069-150">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8069-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8069-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8069-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8069-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8069-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8069-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8069-153">Search-Flags</span></span>           | <span data-ttu-id="b8069-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b8069-154">0x00000009</span></span>                      |
| <span data-ttu-id="b8069-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8069-155">System-Flags</span></span>           | <span data-ttu-id="b8069-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8069-156">0x00000013</span></span>                      |
| <span data-ttu-id="b8069-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8069-157">Classes used in</span></span>        | [<span data-ttu-id="b8069-158">**Início**</span><span class="sxs-lookup"><span data-stu-id="b8069-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b8069-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b8069-159">Windows Server 2003</span></span>



| <span data-ttu-id="b8069-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8069-160">Entry</span></span> | <span data-ttu-id="b8069-161">Valor</span><span class="sxs-lookup"><span data-stu-id="b8069-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8069-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8069-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8069-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8069-163">MAPI-Id</span></span>                | <span data-ttu-id="b8069-164">0x8029</span><span class="sxs-lookup"><span data-stu-id="b8069-164">0x8029</span></span>                          |
| <span data-ttu-id="b8069-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8069-165">System-Only</span></span>            | <span data-ttu-id="b8069-166">True</span><span class="sxs-lookup"><span data-stu-id="b8069-166">True</span></span>                            |
| <span data-ttu-id="b8069-167">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8069-167">Is-Single-Valued</span></span>       | <span data-ttu-id="b8069-168">True</span><span class="sxs-lookup"><span data-stu-id="b8069-168">True</span></span>                            |
| <span data-ttu-id="b8069-169">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8069-169">Is Indexed</span></span>             | <span data-ttu-id="b8069-170">True</span><span class="sxs-lookup"><span data-stu-id="b8069-170">True</span></span>                            |
| <span data-ttu-id="b8069-171">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8069-171">In Global Catalog</span></span>      | <span data-ttu-id="b8069-172">True</span><span class="sxs-lookup"><span data-stu-id="b8069-172">True</span></span>                            |
| <span data-ttu-id="b8069-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8069-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8069-174">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8069-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8069-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8069-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8069-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8069-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8069-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8069-177">Search-Flags</span></span>           | <span data-ttu-id="b8069-178">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b8069-178">0x00000009</span></span>                      |
| <span data-ttu-id="b8069-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8069-179">System-Flags</span></span>           | <span data-ttu-id="b8069-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8069-180">0x00000013</span></span>                      |
| <span data-ttu-id="b8069-181">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8069-181">Classes used in</span></span>        | [<span data-ttu-id="b8069-182">**Início**</span><span class="sxs-lookup"><span data-stu-id="b8069-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b8069-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="b8069-183">ADAM</span></span>



| <span data-ttu-id="b8069-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8069-184">Entry</span></span> | <span data-ttu-id="b8069-185">Valor</span><span class="sxs-lookup"><span data-stu-id="b8069-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8069-186">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8069-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8069-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8069-187">MAPI-Id</span></span>                | <span data-ttu-id="b8069-188">0x8029</span><span class="sxs-lookup"><span data-stu-id="b8069-188">0x8029</span></span>                          |
| <span data-ttu-id="b8069-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8069-189">System-Only</span></span>            | <span data-ttu-id="b8069-190">True</span><span class="sxs-lookup"><span data-stu-id="b8069-190">True</span></span>                            |
| <span data-ttu-id="b8069-191">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8069-191">Is-Single-Valued</span></span>       | <span data-ttu-id="b8069-192">True</span><span class="sxs-lookup"><span data-stu-id="b8069-192">True</span></span>                            |
| <span data-ttu-id="b8069-193">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8069-193">Is Indexed</span></span>             | <span data-ttu-id="b8069-194">True</span><span class="sxs-lookup"><span data-stu-id="b8069-194">True</span></span>                            |
| <span data-ttu-id="b8069-195">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8069-195">In Global Catalog</span></span>      | <span data-ttu-id="b8069-196">True</span><span class="sxs-lookup"><span data-stu-id="b8069-196">True</span></span>                            |
| <span data-ttu-id="b8069-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8069-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8069-198">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8069-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8069-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8069-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8069-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8069-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8069-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8069-201">Search-Flags</span></span>           | <span data-ttu-id="b8069-202">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b8069-202">0x00000009</span></span>                      |
| <span data-ttu-id="b8069-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8069-203">System-Flags</span></span>           | <span data-ttu-id="b8069-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8069-204">0x00000013</span></span>                      |
| <span data-ttu-id="b8069-205">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8069-205">Classes used in</span></span>        | [<span data-ttu-id="b8069-206">**Início**</span><span class="sxs-lookup"><span data-stu-id="b8069-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b8069-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b8069-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b8069-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8069-208">Entry</span></span> | <span data-ttu-id="b8069-209">Valor</span><span class="sxs-lookup"><span data-stu-id="b8069-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8069-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8069-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8069-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8069-211">MAPI-Id</span></span>                | <span data-ttu-id="b8069-212">0x8029</span><span class="sxs-lookup"><span data-stu-id="b8069-212">0x8029</span></span>                          |
| <span data-ttu-id="b8069-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8069-213">System-Only</span></span>            | <span data-ttu-id="b8069-214">True</span><span class="sxs-lookup"><span data-stu-id="b8069-214">True</span></span>                            |
| <span data-ttu-id="b8069-215">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8069-215">Is-Single-Valued</span></span>       | <span data-ttu-id="b8069-216">True</span><span class="sxs-lookup"><span data-stu-id="b8069-216">True</span></span>                            |
| <span data-ttu-id="b8069-217">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8069-217">Is Indexed</span></span>             | <span data-ttu-id="b8069-218">True</span><span class="sxs-lookup"><span data-stu-id="b8069-218">True</span></span>                            |
| <span data-ttu-id="b8069-219">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8069-219">In Global Catalog</span></span>      | <span data-ttu-id="b8069-220">True</span><span class="sxs-lookup"><span data-stu-id="b8069-220">True</span></span>                            |
| <span data-ttu-id="b8069-221">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8069-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8069-222">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8069-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8069-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8069-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8069-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8069-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8069-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8069-225">Search-Flags</span></span>           | <span data-ttu-id="b8069-226">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b8069-226">0x00000009</span></span>                      |
| <span data-ttu-id="b8069-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8069-227">System-Flags</span></span>           | <span data-ttu-id="b8069-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8069-228">0x00000013</span></span>                      |
| <span data-ttu-id="b8069-229">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8069-229">Classes used in</span></span>        | [<span data-ttu-id="b8069-230">**Início**</span><span class="sxs-lookup"><span data-stu-id="b8069-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b8069-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8069-231">Windows Server 2008</span></span>



| <span data-ttu-id="b8069-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8069-232">Entry</span></span> | <span data-ttu-id="b8069-233">Valor</span><span class="sxs-lookup"><span data-stu-id="b8069-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8069-234">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8069-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8069-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8069-235">MAPI-Id</span></span>                | <span data-ttu-id="b8069-236">0x8029</span><span class="sxs-lookup"><span data-stu-id="b8069-236">0x8029</span></span>                          |
| <span data-ttu-id="b8069-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8069-237">System-Only</span></span>            | <span data-ttu-id="b8069-238">True</span><span class="sxs-lookup"><span data-stu-id="b8069-238">True</span></span>                            |
| <span data-ttu-id="b8069-239">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8069-239">Is-Single-Valued</span></span>       | <span data-ttu-id="b8069-240">True</span><span class="sxs-lookup"><span data-stu-id="b8069-240">True</span></span>                            |
| <span data-ttu-id="b8069-241">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8069-241">Is Indexed</span></span>             | <span data-ttu-id="b8069-242">True</span><span class="sxs-lookup"><span data-stu-id="b8069-242">True</span></span>                            |
| <span data-ttu-id="b8069-243">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8069-243">In Global Catalog</span></span>      | <span data-ttu-id="b8069-244">True</span><span class="sxs-lookup"><span data-stu-id="b8069-244">True</span></span>                            |
| <span data-ttu-id="b8069-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8069-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8069-246">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8069-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8069-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8069-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8069-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8069-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8069-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8069-249">Search-Flags</span></span>           | <span data-ttu-id="b8069-250">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b8069-250">0x00000009</span></span>                      |
| <span data-ttu-id="b8069-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8069-251">System-Flags</span></span>           | <span data-ttu-id="b8069-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8069-252">0x00000013</span></span>                      |
| <span data-ttu-id="b8069-253">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8069-253">Classes used in</span></span>        | [<span data-ttu-id="b8069-254">**Início**</span><span class="sxs-lookup"><span data-stu-id="b8069-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b8069-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8069-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b8069-256">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8069-256">Entry</span></span> | <span data-ttu-id="b8069-257">Valor</span><span class="sxs-lookup"><span data-stu-id="b8069-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8069-258">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8069-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8069-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8069-259">MAPI-Id</span></span>                | <span data-ttu-id="b8069-260">0x8029</span><span class="sxs-lookup"><span data-stu-id="b8069-260">0x8029</span></span>                          |
| <span data-ttu-id="b8069-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8069-261">System-Only</span></span>            | <span data-ttu-id="b8069-262">True</span><span class="sxs-lookup"><span data-stu-id="b8069-262">True</span></span>                            |
| <span data-ttu-id="b8069-263">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8069-263">Is-Single-Valued</span></span>       | <span data-ttu-id="b8069-264">True</span><span class="sxs-lookup"><span data-stu-id="b8069-264">True</span></span>                            |
| <span data-ttu-id="b8069-265">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8069-265">Is Indexed</span></span>             | <span data-ttu-id="b8069-266">True</span><span class="sxs-lookup"><span data-stu-id="b8069-266">True</span></span>                            |
| <span data-ttu-id="b8069-267">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8069-267">In Global Catalog</span></span>      | <span data-ttu-id="b8069-268">True</span><span class="sxs-lookup"><span data-stu-id="b8069-268">True</span></span>                            |
| <span data-ttu-id="b8069-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8069-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8069-270">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8069-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8069-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8069-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8069-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8069-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8069-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8069-273">Search-Flags</span></span>           | <span data-ttu-id="b8069-274">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b8069-274">0x00000009</span></span>                      |
| <span data-ttu-id="b8069-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8069-275">System-Flags</span></span>           | <span data-ttu-id="b8069-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8069-276">0x00000013</span></span>                      |
| <span data-ttu-id="b8069-277">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8069-277">Classes used in</span></span>        | [<span data-ttu-id="b8069-278">**Início**</span><span class="sxs-lookup"><span data-stu-id="b8069-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b8069-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b8069-279">Windows Server 2012</span></span>



| <span data-ttu-id="b8069-280">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8069-280">Entry</span></span> | <span data-ttu-id="b8069-281">Valor</span><span class="sxs-lookup"><span data-stu-id="b8069-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8069-282">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8069-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8069-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8069-283">MAPI-Id</span></span>                | <span data-ttu-id="b8069-284">0x8029</span><span class="sxs-lookup"><span data-stu-id="b8069-284">0x8029</span></span>                          |
| <span data-ttu-id="b8069-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8069-285">System-Only</span></span>            | <span data-ttu-id="b8069-286">True</span><span class="sxs-lookup"><span data-stu-id="b8069-286">True</span></span>                            |
| <span data-ttu-id="b8069-287">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8069-287">Is-Single-Valued</span></span>       | <span data-ttu-id="b8069-288">True</span><span class="sxs-lookup"><span data-stu-id="b8069-288">True</span></span>                            |
| <span data-ttu-id="b8069-289">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8069-289">Is Indexed</span></span>             | <span data-ttu-id="b8069-290">True</span><span class="sxs-lookup"><span data-stu-id="b8069-290">True</span></span>                            |
| <span data-ttu-id="b8069-291">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8069-291">In Global Catalog</span></span>      | <span data-ttu-id="b8069-292">True</span><span class="sxs-lookup"><span data-stu-id="b8069-292">True</span></span>                            |
| <span data-ttu-id="b8069-293">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8069-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8069-294">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8069-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8069-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8069-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8069-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8069-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8069-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8069-297">Search-Flags</span></span>           | <span data-ttu-id="b8069-298">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b8069-298">0x00000009</span></span>                      |
| <span data-ttu-id="b8069-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8069-299">System-Flags</span></span>           | <span data-ttu-id="b8069-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8069-300">0x00000013</span></span>                      |
| <span data-ttu-id="b8069-301">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8069-301">Classes used in</span></span>        | [<span data-ttu-id="b8069-302">**Início**</span><span class="sxs-lookup"><span data-stu-id="b8069-302">**Top**</span></span>](c-top.md)<br/> |



 

 





