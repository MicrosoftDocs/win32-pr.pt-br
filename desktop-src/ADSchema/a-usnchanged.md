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
# <a name="usn-changed-attribute"></a><span data-ttu-id="1d7e8-106">USN-Changed atributo</span><span class="sxs-lookup"><span data-stu-id="1d7e8-106">USN-Changed attribute</span></span>

<span data-ttu-id="1d7e8-107">O USN (número de sequência de atualização) atribuído pelo diretório local para a alteração mais recente, incluindo a criação.</span><span class="sxs-lookup"><span data-stu-id="1d7e8-107">The update sequence number (USN) assigned by the local directory for the latest change, including creation.</span></span> <span data-ttu-id="1d7e8-108">Consulte também, [**criado pelo USN**](a-usncreated.md).</span><span class="sxs-lookup"><span data-stu-id="1d7e8-108">See also , [**USN-Created**](a-usncreated.md).</span></span>



| <span data-ttu-id="1d7e8-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d7e8-109">Entry</span></span> | <span data-ttu-id="1d7e8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="1d7e8-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1d7e8-111">CN</span><span class="sxs-lookup"><span data-stu-id="1d7e8-111">CN</span></span>                | <span data-ttu-id="1d7e8-112">USN-Changed</span><span class="sxs-lookup"><span data-stu-id="1d7e8-112">USN-Changed</span></span>                          |
| <span data-ttu-id="1d7e8-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1d7e8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1d7e8-114">uSNChanged</span><span class="sxs-lookup"><span data-stu-id="1d7e8-114">uSNChanged</span></span>                           |
| <span data-ttu-id="1d7e8-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="1d7e8-115">Size</span></span>              | <span data-ttu-id="1d7e8-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="1d7e8-116">8 bytes</span></span>                              |
| <span data-ttu-id="1d7e8-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="1d7e8-117">Update Privilege</span></span>  | <span data-ttu-id="1d7e8-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="1d7e8-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="1d7e8-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="1d7e8-119">Update Frequency</span></span>  | <span data-ttu-id="1d7e8-120">Quando o objeto é alterado.</span><span class="sxs-lookup"><span data-stu-id="1d7e8-120">When the object is changed.</span></span>          |
| <span data-ttu-id="1d7e8-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1d7e8-121">Attribute-Id</span></span>      | <span data-ttu-id="1d7e8-122">1.2.840.113556.1.2.120</span><span class="sxs-lookup"><span data-stu-id="1d7e8-122">1.2.840.113556.1.2.120</span></span>               |
| <span data-ttu-id="1d7e8-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1d7e8-123">System-Id-Guid</span></span>    | <span data-ttu-id="1d7e8-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1d7e8-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="1d7e8-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d7e8-125">Syntax</span></span>            | [<span data-ttu-id="1d7e8-126">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="1d7e8-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="1d7e8-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="1d7e8-127">Implementations</span></span>

-   [<span data-ttu-id="1d7e8-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1d7e8-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1d7e8-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1d7e8-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1d7e8-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1d7e8-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1d7e8-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1d7e8-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1d7e8-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1d7e8-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1d7e8-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1d7e8-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1d7e8-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1d7e8-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1d7e8-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1d7e8-135">Windows 2000 Server</span></span>



| <span data-ttu-id="1d7e8-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d7e8-136">Entry</span></span> | <span data-ttu-id="1d7e8-137">Valor</span><span class="sxs-lookup"><span data-stu-id="1d7e8-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d7e8-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="1d7e8-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7e8-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d7e8-139">MAPI-Id</span></span>                | <span data-ttu-id="1d7e8-140">0x8029</span><span class="sxs-lookup"><span data-stu-id="1d7e8-140">0x8029</span></span>                          |
| <span data-ttu-id="1d7e8-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d7e8-141">System-Only</span></span>            | <span data-ttu-id="1d7e8-142">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-142">True</span></span>                            |
| <span data-ttu-id="1d7e8-143">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1d7e8-143">Is-Single-Valued</span></span>       | <span data-ttu-id="1d7e8-144">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-144">True</span></span>                            |
| <span data-ttu-id="1d7e8-145">É indexado</span><span class="sxs-lookup"><span data-stu-id="1d7e8-145">Is Indexed</span></span>             | <span data-ttu-id="1d7e8-146">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-146">True</span></span>                            |
| <span data-ttu-id="1d7e8-147">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d7e8-147">In Global Catalog</span></span>      | <span data-ttu-id="1d7e8-148">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-148">True</span></span>                            |
| <span data-ttu-id="1d7e8-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1d7e8-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d7e8-150">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1d7e8-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d7e8-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d7e8-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d7e8-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d7e8-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d7e8-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7e8-153">Search-Flags</span></span>           | <span data-ttu-id="1d7e8-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="1d7e8-154">0x00000009</span></span>                      |
| <span data-ttu-id="1d7e8-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7e8-155">System-Flags</span></span>           | <span data-ttu-id="1d7e8-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1d7e8-156">0x00000013</span></span>                      |
| <span data-ttu-id="1d7e8-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1d7e8-157">Classes used in</span></span>        | [<span data-ttu-id="1d7e8-158">**Início**</span><span class="sxs-lookup"><span data-stu-id="1d7e8-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1d7e8-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1d7e8-159">Windows Server 2003</span></span>



| <span data-ttu-id="1d7e8-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d7e8-160">Entry</span></span> | <span data-ttu-id="1d7e8-161">Valor</span><span class="sxs-lookup"><span data-stu-id="1d7e8-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d7e8-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="1d7e8-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7e8-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d7e8-163">MAPI-Id</span></span>                | <span data-ttu-id="1d7e8-164">0x8029</span><span class="sxs-lookup"><span data-stu-id="1d7e8-164">0x8029</span></span>                          |
| <span data-ttu-id="1d7e8-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d7e8-165">System-Only</span></span>            | <span data-ttu-id="1d7e8-166">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-166">True</span></span>                            |
| <span data-ttu-id="1d7e8-167">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1d7e8-167">Is-Single-Valued</span></span>       | <span data-ttu-id="1d7e8-168">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-168">True</span></span>                            |
| <span data-ttu-id="1d7e8-169">É indexado</span><span class="sxs-lookup"><span data-stu-id="1d7e8-169">Is Indexed</span></span>             | <span data-ttu-id="1d7e8-170">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-170">True</span></span>                            |
| <span data-ttu-id="1d7e8-171">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d7e8-171">In Global Catalog</span></span>      | <span data-ttu-id="1d7e8-172">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-172">True</span></span>                            |
| <span data-ttu-id="1d7e8-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1d7e8-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d7e8-174">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1d7e8-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d7e8-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d7e8-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d7e8-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d7e8-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d7e8-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7e8-177">Search-Flags</span></span>           | <span data-ttu-id="1d7e8-178">0x00000009</span><span class="sxs-lookup"><span data-stu-id="1d7e8-178">0x00000009</span></span>                      |
| <span data-ttu-id="1d7e8-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7e8-179">System-Flags</span></span>           | <span data-ttu-id="1d7e8-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1d7e8-180">0x00000013</span></span>                      |
| <span data-ttu-id="1d7e8-181">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1d7e8-181">Classes used in</span></span>        | [<span data-ttu-id="1d7e8-182">**Início**</span><span class="sxs-lookup"><span data-stu-id="1d7e8-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1d7e8-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="1d7e8-183">ADAM</span></span>



| <span data-ttu-id="1d7e8-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d7e8-184">Entry</span></span> | <span data-ttu-id="1d7e8-185">Valor</span><span class="sxs-lookup"><span data-stu-id="1d7e8-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d7e8-186">ID do link</span><span class="sxs-lookup"><span data-stu-id="1d7e8-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7e8-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d7e8-187">MAPI-Id</span></span>                | <span data-ttu-id="1d7e8-188">0x8029</span><span class="sxs-lookup"><span data-stu-id="1d7e8-188">0x8029</span></span>                          |
| <span data-ttu-id="1d7e8-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d7e8-189">System-Only</span></span>            | <span data-ttu-id="1d7e8-190">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-190">True</span></span>                            |
| <span data-ttu-id="1d7e8-191">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1d7e8-191">Is-Single-Valued</span></span>       | <span data-ttu-id="1d7e8-192">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-192">True</span></span>                            |
| <span data-ttu-id="1d7e8-193">É indexado</span><span class="sxs-lookup"><span data-stu-id="1d7e8-193">Is Indexed</span></span>             | <span data-ttu-id="1d7e8-194">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-194">True</span></span>                            |
| <span data-ttu-id="1d7e8-195">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d7e8-195">In Global Catalog</span></span>      | <span data-ttu-id="1d7e8-196">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-196">True</span></span>                            |
| <span data-ttu-id="1d7e8-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1d7e8-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d7e8-198">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1d7e8-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d7e8-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d7e8-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d7e8-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d7e8-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d7e8-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7e8-201">Search-Flags</span></span>           | <span data-ttu-id="1d7e8-202">0x00000009</span><span class="sxs-lookup"><span data-stu-id="1d7e8-202">0x00000009</span></span>                      |
| <span data-ttu-id="1d7e8-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7e8-203">System-Flags</span></span>           | <span data-ttu-id="1d7e8-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1d7e8-204">0x00000013</span></span>                      |
| <span data-ttu-id="1d7e8-205">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1d7e8-205">Classes used in</span></span>        | [<span data-ttu-id="1d7e8-206">**Início**</span><span class="sxs-lookup"><span data-stu-id="1d7e8-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1d7e8-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1d7e8-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1d7e8-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d7e8-208">Entry</span></span> | <span data-ttu-id="1d7e8-209">Valor</span><span class="sxs-lookup"><span data-stu-id="1d7e8-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d7e8-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="1d7e8-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7e8-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d7e8-211">MAPI-Id</span></span>                | <span data-ttu-id="1d7e8-212">0x8029</span><span class="sxs-lookup"><span data-stu-id="1d7e8-212">0x8029</span></span>                          |
| <span data-ttu-id="1d7e8-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d7e8-213">System-Only</span></span>            | <span data-ttu-id="1d7e8-214">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-214">True</span></span>                            |
| <span data-ttu-id="1d7e8-215">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1d7e8-215">Is-Single-Valued</span></span>       | <span data-ttu-id="1d7e8-216">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-216">True</span></span>                            |
| <span data-ttu-id="1d7e8-217">É indexado</span><span class="sxs-lookup"><span data-stu-id="1d7e8-217">Is Indexed</span></span>             | <span data-ttu-id="1d7e8-218">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-218">True</span></span>                            |
| <span data-ttu-id="1d7e8-219">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d7e8-219">In Global Catalog</span></span>      | <span data-ttu-id="1d7e8-220">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-220">True</span></span>                            |
| <span data-ttu-id="1d7e8-221">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1d7e8-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d7e8-222">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1d7e8-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d7e8-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d7e8-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d7e8-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d7e8-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d7e8-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7e8-225">Search-Flags</span></span>           | <span data-ttu-id="1d7e8-226">0x00000009</span><span class="sxs-lookup"><span data-stu-id="1d7e8-226">0x00000009</span></span>                      |
| <span data-ttu-id="1d7e8-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7e8-227">System-Flags</span></span>           | <span data-ttu-id="1d7e8-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1d7e8-228">0x00000013</span></span>                      |
| <span data-ttu-id="1d7e8-229">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1d7e8-229">Classes used in</span></span>        | [<span data-ttu-id="1d7e8-230">**Início**</span><span class="sxs-lookup"><span data-stu-id="1d7e8-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1d7e8-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d7e8-231">Windows Server 2008</span></span>



| <span data-ttu-id="1d7e8-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d7e8-232">Entry</span></span> | <span data-ttu-id="1d7e8-233">Valor</span><span class="sxs-lookup"><span data-stu-id="1d7e8-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d7e8-234">ID do link</span><span class="sxs-lookup"><span data-stu-id="1d7e8-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7e8-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d7e8-235">MAPI-Id</span></span>                | <span data-ttu-id="1d7e8-236">0x8029</span><span class="sxs-lookup"><span data-stu-id="1d7e8-236">0x8029</span></span>                          |
| <span data-ttu-id="1d7e8-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d7e8-237">System-Only</span></span>            | <span data-ttu-id="1d7e8-238">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-238">True</span></span>                            |
| <span data-ttu-id="1d7e8-239">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1d7e8-239">Is-Single-Valued</span></span>       | <span data-ttu-id="1d7e8-240">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-240">True</span></span>                            |
| <span data-ttu-id="1d7e8-241">É indexado</span><span class="sxs-lookup"><span data-stu-id="1d7e8-241">Is Indexed</span></span>             | <span data-ttu-id="1d7e8-242">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-242">True</span></span>                            |
| <span data-ttu-id="1d7e8-243">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d7e8-243">In Global Catalog</span></span>      | <span data-ttu-id="1d7e8-244">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-244">True</span></span>                            |
| <span data-ttu-id="1d7e8-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1d7e8-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d7e8-246">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1d7e8-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d7e8-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d7e8-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d7e8-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d7e8-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d7e8-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7e8-249">Search-Flags</span></span>           | <span data-ttu-id="1d7e8-250">0x00000009</span><span class="sxs-lookup"><span data-stu-id="1d7e8-250">0x00000009</span></span>                      |
| <span data-ttu-id="1d7e8-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7e8-251">System-Flags</span></span>           | <span data-ttu-id="1d7e8-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1d7e8-252">0x00000013</span></span>                      |
| <span data-ttu-id="1d7e8-253">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1d7e8-253">Classes used in</span></span>        | [<span data-ttu-id="1d7e8-254">**Início**</span><span class="sxs-lookup"><span data-stu-id="1d7e8-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1d7e8-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1d7e8-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1d7e8-256">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d7e8-256">Entry</span></span> | <span data-ttu-id="1d7e8-257">Valor</span><span class="sxs-lookup"><span data-stu-id="1d7e8-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d7e8-258">ID do link</span><span class="sxs-lookup"><span data-stu-id="1d7e8-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7e8-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d7e8-259">MAPI-Id</span></span>                | <span data-ttu-id="1d7e8-260">0x8029</span><span class="sxs-lookup"><span data-stu-id="1d7e8-260">0x8029</span></span>                          |
| <span data-ttu-id="1d7e8-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d7e8-261">System-Only</span></span>            | <span data-ttu-id="1d7e8-262">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-262">True</span></span>                            |
| <span data-ttu-id="1d7e8-263">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1d7e8-263">Is-Single-Valued</span></span>       | <span data-ttu-id="1d7e8-264">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-264">True</span></span>                            |
| <span data-ttu-id="1d7e8-265">É indexado</span><span class="sxs-lookup"><span data-stu-id="1d7e8-265">Is Indexed</span></span>             | <span data-ttu-id="1d7e8-266">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-266">True</span></span>                            |
| <span data-ttu-id="1d7e8-267">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d7e8-267">In Global Catalog</span></span>      | <span data-ttu-id="1d7e8-268">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-268">True</span></span>                            |
| <span data-ttu-id="1d7e8-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1d7e8-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d7e8-270">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1d7e8-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d7e8-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d7e8-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d7e8-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d7e8-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d7e8-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7e8-273">Search-Flags</span></span>           | <span data-ttu-id="1d7e8-274">0x00000009</span><span class="sxs-lookup"><span data-stu-id="1d7e8-274">0x00000009</span></span>                      |
| <span data-ttu-id="1d7e8-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7e8-275">System-Flags</span></span>           | <span data-ttu-id="1d7e8-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1d7e8-276">0x00000013</span></span>                      |
| <span data-ttu-id="1d7e8-277">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1d7e8-277">Classes used in</span></span>        | [<span data-ttu-id="1d7e8-278">**Início**</span><span class="sxs-lookup"><span data-stu-id="1d7e8-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1d7e8-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1d7e8-279">Windows Server 2012</span></span>



| <span data-ttu-id="1d7e8-280">Entrada</span><span class="sxs-lookup"><span data-stu-id="1d7e8-280">Entry</span></span> | <span data-ttu-id="1d7e8-281">Valor</span><span class="sxs-lookup"><span data-stu-id="1d7e8-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d7e8-282">ID do link</span><span class="sxs-lookup"><span data-stu-id="1d7e8-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7e8-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d7e8-283">MAPI-Id</span></span>                | <span data-ttu-id="1d7e8-284">0x8029</span><span class="sxs-lookup"><span data-stu-id="1d7e8-284">0x8029</span></span>                          |
| <span data-ttu-id="1d7e8-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d7e8-285">System-Only</span></span>            | <span data-ttu-id="1d7e8-286">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-286">True</span></span>                            |
| <span data-ttu-id="1d7e8-287">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1d7e8-287">Is-Single-Valued</span></span>       | <span data-ttu-id="1d7e8-288">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-288">True</span></span>                            |
| <span data-ttu-id="1d7e8-289">É indexado</span><span class="sxs-lookup"><span data-stu-id="1d7e8-289">Is Indexed</span></span>             | <span data-ttu-id="1d7e8-290">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-290">True</span></span>                            |
| <span data-ttu-id="1d7e8-291">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1d7e8-291">In Global Catalog</span></span>      | <span data-ttu-id="1d7e8-292">True</span><span class="sxs-lookup"><span data-stu-id="1d7e8-292">True</span></span>                            |
| <span data-ttu-id="1d7e8-293">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1d7e8-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d7e8-294">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1d7e8-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d7e8-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d7e8-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d7e8-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d7e8-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d7e8-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7e8-297">Search-Flags</span></span>           | <span data-ttu-id="1d7e8-298">0x00000009</span><span class="sxs-lookup"><span data-stu-id="1d7e8-298">0x00000009</span></span>                      |
| <span data-ttu-id="1d7e8-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7e8-299">System-Flags</span></span>           | <span data-ttu-id="1d7e8-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1d7e8-300">0x00000013</span></span>                      |
| <span data-ttu-id="1d7e8-301">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1d7e8-301">Classes used in</span></span>        | [<span data-ttu-id="1d7e8-302">**Início**</span><span class="sxs-lookup"><span data-stu-id="1d7e8-302">**Top**</span></span>](c-top.md)<br/> |



 

 





