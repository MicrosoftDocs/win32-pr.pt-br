---
title: Schema-Version atributo
description: O número de versão do esquema.
ms.assetid: b937d704-cd76-41fc-84df-5ea614b1785d
ms.tgt_platform: multiple
keywords:
- Esquema de Schema-Version do atributo AD
- Esquema de AD do atributo schemaVersion
topic_type:
- apiref
api_name:
- Schema-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d00ca6ad8626933b39a82b2288f89454225ed47f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456254"
---
# <a name="schema-version-attribute"></a><span data-ttu-id="64a91-105">Schema-Version atributo</span><span class="sxs-lookup"><span data-stu-id="64a91-105">Schema-Version attribute</span></span>

<span data-ttu-id="64a91-106">O número de versão do esquema.</span><span class="sxs-lookup"><span data-stu-id="64a91-106">The version number for the schema.</span></span>



| <span data-ttu-id="64a91-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="64a91-107">Entry</span></span> | <span data-ttu-id="64a91-108">Valor</span><span class="sxs-lookup"><span data-stu-id="64a91-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="64a91-109">CN</span><span class="sxs-lookup"><span data-stu-id="64a91-109">CN</span></span>                | <span data-ttu-id="64a91-110">Schema-Version</span><span class="sxs-lookup"><span data-stu-id="64a91-110">Schema-Version</span></span>                       |
| <span data-ttu-id="64a91-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="64a91-111">Ldap-Display-Name</span></span> | <span data-ttu-id="64a91-112">schemaVersion</span><span class="sxs-lookup"><span data-stu-id="64a91-112">schemaVersion</span></span>                        |
| <span data-ttu-id="64a91-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="64a91-113">Size</span></span>              | <span data-ttu-id="64a91-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="64a91-114">4 bytes</span></span>                              |
| <span data-ttu-id="64a91-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="64a91-115">Update Privilege</span></span>  | <span data-ttu-id="64a91-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="64a91-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="64a91-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="64a91-117">Update Frequency</span></span>  | <span data-ttu-id="64a91-118">Cada vez que o esquema é liberado.</span><span class="sxs-lookup"><span data-stu-id="64a91-118">Each time the schema is released.</span></span>    |
| <span data-ttu-id="64a91-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="64a91-119">Attribute-Id</span></span>      | <span data-ttu-id="64a91-120">1.2.840.113556.1.2.471</span><span class="sxs-lookup"><span data-stu-id="64a91-120">1.2.840.113556.1.2.471</span></span>               |
| <span data-ttu-id="64a91-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="64a91-121">System-Id-Guid</span></span>    | <span data-ttu-id="64a91-122">bf967a2c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="64a91-122">bf967a2c-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="64a91-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="64a91-123">Syntax</span></span>            | [<span data-ttu-id="64a91-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="64a91-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="64a91-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="64a91-125">Implementations</span></span>

-   [<span data-ttu-id="64a91-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="64a91-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="64a91-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="64a91-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="64a91-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="64a91-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="64a91-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="64a91-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="64a91-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="64a91-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="64a91-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="64a91-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="64a91-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="64a91-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="64a91-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="64a91-133">Windows 2000 Server</span></span>



| <span data-ttu-id="64a91-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="64a91-134">Entry</span></span> | <span data-ttu-id="64a91-135">Valor</span><span class="sxs-lookup"><span data-stu-id="64a91-135">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="64a91-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="64a91-136">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="64a91-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64a91-137">MAPI-Id</span></span>                | <span data-ttu-id="64a91-138">0x817C</span><span class="sxs-lookup"><span data-stu-id="64a91-138">0x817C</span></span>                                      |
| <span data-ttu-id="64a91-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="64a91-139">System-Only</span></span>            | <span data-ttu-id="64a91-140">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-140">False</span></span>                                       |
| <span data-ttu-id="64a91-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64a91-141">Is-Single-Valued</span></span>       | <span data-ttu-id="64a91-142">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-142">False</span></span>                                       |
| <span data-ttu-id="64a91-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="64a91-143">Is Indexed</span></span>             | <span data-ttu-id="64a91-144">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-144">False</span></span>                                       |
| <span data-ttu-id="64a91-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64a91-145">In Global Catalog</span></span>      | <span data-ttu-id="64a91-146">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-146">False</span></span>                                       |
| <span data-ttu-id="64a91-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64a91-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="64a91-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64a91-148">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="64a91-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64a91-149">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="64a91-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64a91-150">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="64a91-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64a91-151">Search-Flags</span></span>           | <span data-ttu-id="64a91-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64a91-152">0x00000000</span></span>                                  |
| <span data-ttu-id="64a91-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64a91-153">System-Flags</span></span>           | <span data-ttu-id="64a91-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64a91-154">0x00000010</span></span>                                  |
| <span data-ttu-id="64a91-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64a91-155">Classes used in</span></span>        | [<span data-ttu-id="64a91-156">**Contêiner**</span><span class="sxs-lookup"><span data-stu-id="64a91-156">**Container**</span></span>](c-container.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="64a91-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="64a91-157">Windows Server 2003</span></span>



| <span data-ttu-id="64a91-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="64a91-158">Entry</span></span> | <span data-ttu-id="64a91-159">Valor</span><span class="sxs-lookup"><span data-stu-id="64a91-159">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="64a91-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="64a91-160">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="64a91-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64a91-161">MAPI-Id</span></span>                | <span data-ttu-id="64a91-162">0x817C</span><span class="sxs-lookup"><span data-stu-id="64a91-162">0x817C</span></span>                                      |
| <span data-ttu-id="64a91-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="64a91-163">System-Only</span></span>            | <span data-ttu-id="64a91-164">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-164">False</span></span>                                       |
| <span data-ttu-id="64a91-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64a91-165">Is-Single-Valued</span></span>       | <span data-ttu-id="64a91-166">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-166">False</span></span>                                       |
| <span data-ttu-id="64a91-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="64a91-167">Is Indexed</span></span>             | <span data-ttu-id="64a91-168">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-168">False</span></span>                                       |
| <span data-ttu-id="64a91-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64a91-169">In Global Catalog</span></span>      | <span data-ttu-id="64a91-170">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-170">False</span></span>                                       |
| <span data-ttu-id="64a91-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64a91-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="64a91-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64a91-172">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="64a91-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64a91-173">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="64a91-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64a91-174">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="64a91-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64a91-175">Search-Flags</span></span>           | <span data-ttu-id="64a91-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64a91-176">0x00000000</span></span>                                  |
| <span data-ttu-id="64a91-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64a91-177">System-Flags</span></span>           | <span data-ttu-id="64a91-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64a91-178">0x00000010</span></span>                                  |
| <span data-ttu-id="64a91-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64a91-179">Classes used in</span></span>        | [<span data-ttu-id="64a91-180">**Contêiner**</span><span class="sxs-lookup"><span data-stu-id="64a91-180">**Container**</span></span>](c-container.md)<br/> |



## <a name="adam"></a><span data-ttu-id="64a91-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="64a91-181">ADAM</span></span>



| <span data-ttu-id="64a91-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="64a91-182">Entry</span></span> | <span data-ttu-id="64a91-183">Valor</span><span class="sxs-lookup"><span data-stu-id="64a91-183">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="64a91-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="64a91-184">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="64a91-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64a91-185">MAPI-Id</span></span>                | <span data-ttu-id="64a91-186">0x817C</span><span class="sxs-lookup"><span data-stu-id="64a91-186">0x817C</span></span>                                      |
| <span data-ttu-id="64a91-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="64a91-187">System-Only</span></span>            | <span data-ttu-id="64a91-188">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-188">False</span></span>                                       |
| <span data-ttu-id="64a91-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64a91-189">Is-Single-Valued</span></span>       | <span data-ttu-id="64a91-190">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-190">False</span></span>                                       |
| <span data-ttu-id="64a91-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="64a91-191">Is Indexed</span></span>             | <span data-ttu-id="64a91-192">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-192">False</span></span>                                       |
| <span data-ttu-id="64a91-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64a91-193">In Global Catalog</span></span>      | <span data-ttu-id="64a91-194">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-194">False</span></span>                                       |
| <span data-ttu-id="64a91-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64a91-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="64a91-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64a91-196">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="64a91-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64a91-197">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="64a91-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64a91-198">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="64a91-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64a91-199">Search-Flags</span></span>           | <span data-ttu-id="64a91-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64a91-200">0x00000000</span></span>                                  |
| <span data-ttu-id="64a91-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64a91-201">System-Flags</span></span>           | <span data-ttu-id="64a91-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64a91-202">0x00000010</span></span>                                  |
| <span data-ttu-id="64a91-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64a91-203">Classes used in</span></span>        | [<span data-ttu-id="64a91-204">**Contêiner**</span><span class="sxs-lookup"><span data-stu-id="64a91-204">**Container**</span></span>](c-container.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="64a91-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="64a91-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="64a91-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="64a91-206">Entry</span></span> | <span data-ttu-id="64a91-207">Valor</span><span class="sxs-lookup"><span data-stu-id="64a91-207">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="64a91-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="64a91-208">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="64a91-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64a91-209">MAPI-Id</span></span>                | <span data-ttu-id="64a91-210">0x817C</span><span class="sxs-lookup"><span data-stu-id="64a91-210">0x817C</span></span>                                      |
| <span data-ttu-id="64a91-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="64a91-211">System-Only</span></span>            | <span data-ttu-id="64a91-212">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-212">False</span></span>                                       |
| <span data-ttu-id="64a91-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64a91-213">Is-Single-Valued</span></span>       | <span data-ttu-id="64a91-214">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-214">False</span></span>                                       |
| <span data-ttu-id="64a91-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="64a91-215">Is Indexed</span></span>             | <span data-ttu-id="64a91-216">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-216">False</span></span>                                       |
| <span data-ttu-id="64a91-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64a91-217">In Global Catalog</span></span>      | <span data-ttu-id="64a91-218">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-218">False</span></span>                                       |
| <span data-ttu-id="64a91-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64a91-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="64a91-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64a91-220">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="64a91-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64a91-221">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="64a91-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64a91-222">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="64a91-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64a91-223">Search-Flags</span></span>           | <span data-ttu-id="64a91-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64a91-224">0x00000000</span></span>                                  |
| <span data-ttu-id="64a91-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64a91-225">System-Flags</span></span>           | <span data-ttu-id="64a91-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64a91-226">0x00000010</span></span>                                  |
| <span data-ttu-id="64a91-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64a91-227">Classes used in</span></span>        | [<span data-ttu-id="64a91-228">**Contêiner**</span><span class="sxs-lookup"><span data-stu-id="64a91-228">**Container**</span></span>](c-container.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="64a91-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64a91-229">Windows Server 2008</span></span>



| <span data-ttu-id="64a91-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="64a91-230">Entry</span></span> | <span data-ttu-id="64a91-231">Valor</span><span class="sxs-lookup"><span data-stu-id="64a91-231">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="64a91-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="64a91-232">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="64a91-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64a91-233">MAPI-Id</span></span>                | <span data-ttu-id="64a91-234">0x817C</span><span class="sxs-lookup"><span data-stu-id="64a91-234">0x817C</span></span>                                      |
| <span data-ttu-id="64a91-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="64a91-235">System-Only</span></span>            | <span data-ttu-id="64a91-236">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-236">False</span></span>                                       |
| <span data-ttu-id="64a91-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64a91-237">Is-Single-Valued</span></span>       | <span data-ttu-id="64a91-238">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-238">False</span></span>                                       |
| <span data-ttu-id="64a91-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="64a91-239">Is Indexed</span></span>             | <span data-ttu-id="64a91-240">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-240">False</span></span>                                       |
| <span data-ttu-id="64a91-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64a91-241">In Global Catalog</span></span>      | <span data-ttu-id="64a91-242">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-242">False</span></span>                                       |
| <span data-ttu-id="64a91-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64a91-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="64a91-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64a91-244">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="64a91-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64a91-245">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="64a91-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64a91-246">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="64a91-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64a91-247">Search-Flags</span></span>           | <span data-ttu-id="64a91-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64a91-248">0x00000000</span></span>                                  |
| <span data-ttu-id="64a91-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64a91-249">System-Flags</span></span>           | <span data-ttu-id="64a91-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64a91-250">0x00000010</span></span>                                  |
| <span data-ttu-id="64a91-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64a91-251">Classes used in</span></span>        | [<span data-ttu-id="64a91-252">**Contêiner**</span><span class="sxs-lookup"><span data-stu-id="64a91-252">**Container**</span></span>](c-container.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="64a91-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="64a91-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="64a91-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="64a91-254">Entry</span></span> | <span data-ttu-id="64a91-255">Valor</span><span class="sxs-lookup"><span data-stu-id="64a91-255">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="64a91-256">ID do link</span><span class="sxs-lookup"><span data-stu-id="64a91-256">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="64a91-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64a91-257">MAPI-Id</span></span>                | <span data-ttu-id="64a91-258">0x817C</span><span class="sxs-lookup"><span data-stu-id="64a91-258">0x817C</span></span>                                      |
| <span data-ttu-id="64a91-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="64a91-259">System-Only</span></span>            | <span data-ttu-id="64a91-260">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-260">False</span></span>                                       |
| <span data-ttu-id="64a91-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64a91-261">Is-Single-Valued</span></span>       | <span data-ttu-id="64a91-262">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-262">False</span></span>                                       |
| <span data-ttu-id="64a91-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="64a91-263">Is Indexed</span></span>             | <span data-ttu-id="64a91-264">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-264">False</span></span>                                       |
| <span data-ttu-id="64a91-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64a91-265">In Global Catalog</span></span>      | <span data-ttu-id="64a91-266">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-266">False</span></span>                                       |
| <span data-ttu-id="64a91-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64a91-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="64a91-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64a91-268">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="64a91-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64a91-269">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="64a91-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64a91-270">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="64a91-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64a91-271">Search-Flags</span></span>           | <span data-ttu-id="64a91-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64a91-272">0x00000000</span></span>                                  |
| <span data-ttu-id="64a91-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64a91-273">System-Flags</span></span>           | <span data-ttu-id="64a91-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64a91-274">0x00000010</span></span>                                  |
| <span data-ttu-id="64a91-275">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64a91-275">Classes used in</span></span>        | [<span data-ttu-id="64a91-276">**Contêiner**</span><span class="sxs-lookup"><span data-stu-id="64a91-276">**Container**</span></span>](c-container.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="64a91-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="64a91-277">Windows Server 2012</span></span>



| <span data-ttu-id="64a91-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="64a91-278">Entry</span></span> | <span data-ttu-id="64a91-279">Valor</span><span class="sxs-lookup"><span data-stu-id="64a91-279">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="64a91-280">ID do link</span><span class="sxs-lookup"><span data-stu-id="64a91-280">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="64a91-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64a91-281">MAPI-Id</span></span>                | <span data-ttu-id="64a91-282">0x817C</span><span class="sxs-lookup"><span data-stu-id="64a91-282">0x817C</span></span>                                      |
| <span data-ttu-id="64a91-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="64a91-283">System-Only</span></span>            | <span data-ttu-id="64a91-284">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-284">False</span></span>                                       |
| <span data-ttu-id="64a91-285">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64a91-285">Is-Single-Valued</span></span>       | <span data-ttu-id="64a91-286">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-286">False</span></span>                                       |
| <span data-ttu-id="64a91-287">É indexado</span><span class="sxs-lookup"><span data-stu-id="64a91-287">Is Indexed</span></span>             | <span data-ttu-id="64a91-288">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-288">False</span></span>                                       |
| <span data-ttu-id="64a91-289">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64a91-289">In Global Catalog</span></span>      | <span data-ttu-id="64a91-290">Falso</span><span class="sxs-lookup"><span data-stu-id="64a91-290">False</span></span>                                       |
| <span data-ttu-id="64a91-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64a91-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="64a91-292">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64a91-292">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="64a91-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64a91-293">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="64a91-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64a91-294">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="64a91-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64a91-295">Search-Flags</span></span>           | <span data-ttu-id="64a91-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64a91-296">0x00000000</span></span>                                  |
| <span data-ttu-id="64a91-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64a91-297">System-Flags</span></span>           | <span data-ttu-id="64a91-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64a91-298">0x00000010</span></span>                                  |
| <span data-ttu-id="64a91-299">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64a91-299">Classes used in</span></span>        | [<span data-ttu-id="64a91-300">**Contêiner**</span><span class="sxs-lookup"><span data-stu-id="64a91-300">**Container**</span></span>](c-container.md)<br/> |



 

 





