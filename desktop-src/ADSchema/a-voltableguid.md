---
title: Atributo Vol-Table-GUID
description: O identificador exclusivo para uma entrada de tabela de faixa de link-volume.
ms.assetid: 3a63406a-e751-4234-a601-8f5a57f0a3b7
ms.tgt_platform: multiple
keywords:
- Atributo Vol-Table-GUID do AD Schema
- Esquema de AD do atributo volTableGUID
topic_type:
- apiref
api_name:
- Vol-Table-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a23bcd088304b4a683ce3ff0f203d3c82fecf8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456162"
---
# <a name="vol-table-guid-attribute"></a><span data-ttu-id="26817-105">Atributo Vol-Table-GUID</span><span class="sxs-lookup"><span data-stu-id="26817-105">Vol-Table-GUID attribute</span></span>

<span data-ttu-id="26817-106">O identificador exclusivo para uma entrada de tabela de faixa de link-volume.</span><span class="sxs-lookup"><span data-stu-id="26817-106">The unique identifier for a Link-Track-Volume table entry.</span></span>



| <span data-ttu-id="26817-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="26817-107">Entry</span></span> | <span data-ttu-id="26817-108">Valor</span><span class="sxs-lookup"><span data-stu-id="26817-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="26817-109">CN</span><span class="sxs-lookup"><span data-stu-id="26817-109">CN</span></span>                | <span data-ttu-id="26817-110">Vol-Table-GUID</span><span class="sxs-lookup"><span data-stu-id="26817-110">Vol-Table-GUID</span></span>                                        |
| <span data-ttu-id="26817-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="26817-111">Ldap-Display-Name</span></span> | <span data-ttu-id="26817-112">volTableGUID</span><span class="sxs-lookup"><span data-stu-id="26817-112">volTableGUID</span></span>                                          |
| <span data-ttu-id="26817-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="26817-113">Size</span></span>              | <span data-ttu-id="26817-114">16 bytes</span><span class="sxs-lookup"><span data-stu-id="26817-114">16 bytes</span></span>                                              |
| <span data-ttu-id="26817-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="26817-115">Update Privilege</span></span>  | <span data-ttu-id="26817-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="26817-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="26817-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="26817-117">Update Frequency</span></span>  | <span data-ttu-id="26817-118">Sempre que um novo link para um arquivo for criado.</span><span class="sxs-lookup"><span data-stu-id="26817-118">Whenever a new link to a file is created.</span></span>             |
| <span data-ttu-id="26817-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="26817-119">Attribute-Id</span></span>      | <span data-ttu-id="26817-120">1.2.840.113556.1.4.336</span><span class="sxs-lookup"><span data-stu-id="26817-120">1.2.840.113556.1.4.336</span></span>                                |
| <span data-ttu-id="26817-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="26817-121">System-Id-Guid</span></span>    | <span data-ttu-id="26817-122">1f0075fd-7e40-11d0-afd6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="26817-122">1f0075fd-7e40-11d0-afd6-00c04fd930c9</span></span>                  |
| <span data-ttu-id="26817-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="26817-123">Syntax</span></span>            | [<span data-ttu-id="26817-124">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="26817-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="26817-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="26817-125">Implementations</span></span>

-   [<span data-ttu-id="26817-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="26817-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="26817-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="26817-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="26817-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="26817-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="26817-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="26817-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="26817-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="26817-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="26817-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="26817-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="26817-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="26817-132">Windows 2000 Server</span></span>



| <span data-ttu-id="26817-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="26817-133">Entry</span></span> | <span data-ttu-id="26817-134">Valor</span><span class="sxs-lookup"><span data-stu-id="26817-134">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="26817-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="26817-135">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="26817-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26817-136">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="26817-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="26817-137">System-Only</span></span>            | <span data-ttu-id="26817-138">Falso</span><span class="sxs-lookup"><span data-stu-id="26817-138">False</span></span>                                                          |
| <span data-ttu-id="26817-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="26817-139">Is-Single-Valued</span></span>       | <span data-ttu-id="26817-140">True</span><span class="sxs-lookup"><span data-stu-id="26817-140">True</span></span>                                                           |
| <span data-ttu-id="26817-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="26817-141">Is Indexed</span></span>             | <span data-ttu-id="26817-142">Falso</span><span class="sxs-lookup"><span data-stu-id="26817-142">False</span></span>                                                          |
| <span data-ttu-id="26817-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="26817-143">In Global Catalog</span></span>      | <span data-ttu-id="26817-144">Falso</span><span class="sxs-lookup"><span data-stu-id="26817-144">False</span></span>                                                          |
| <span data-ttu-id="26817-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="26817-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="26817-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="26817-146">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="26817-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26817-147">Range-Lower</span></span>            | <span data-ttu-id="26817-148">0</span><span class="sxs-lookup"><span data-stu-id="26817-148">0</span></span>                                                              |
| <span data-ttu-id="26817-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26817-149">Range-Upper</span></span>            | <span data-ttu-id="26817-150">16</span><span class="sxs-lookup"><span data-stu-id="26817-150">16</span></span>                                                             |
| <span data-ttu-id="26817-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26817-151">Search-Flags</span></span>           | <span data-ttu-id="26817-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26817-152">0x00000000</span></span>                                                     |
| <span data-ttu-id="26817-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26817-153">System-Flags</span></span>           | <span data-ttu-id="26817-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26817-154">0x00000010</span></span>                                                     |
| <span data-ttu-id="26817-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="26817-155">Classes used in</span></span>        | [<span data-ttu-id="26817-156">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="26817-156">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="26817-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="26817-157">Windows Server 2003</span></span>



| <span data-ttu-id="26817-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="26817-158">Entry</span></span> | <span data-ttu-id="26817-159">Valor</span><span class="sxs-lookup"><span data-stu-id="26817-159">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="26817-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="26817-160">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="26817-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26817-161">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="26817-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="26817-162">System-Only</span></span>            | <span data-ttu-id="26817-163">Falso</span><span class="sxs-lookup"><span data-stu-id="26817-163">False</span></span>                                                          |
| <span data-ttu-id="26817-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="26817-164">Is-Single-Valued</span></span>       | <span data-ttu-id="26817-165">True</span><span class="sxs-lookup"><span data-stu-id="26817-165">True</span></span>                                                           |
| <span data-ttu-id="26817-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="26817-166">Is Indexed</span></span>             | <span data-ttu-id="26817-167">Falso</span><span class="sxs-lookup"><span data-stu-id="26817-167">False</span></span>                                                          |
| <span data-ttu-id="26817-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="26817-168">In Global Catalog</span></span>      | <span data-ttu-id="26817-169">Falso</span><span class="sxs-lookup"><span data-stu-id="26817-169">False</span></span>                                                          |
| <span data-ttu-id="26817-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="26817-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="26817-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="26817-171">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="26817-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26817-172">Range-Lower</span></span>            | <span data-ttu-id="26817-173">0</span><span class="sxs-lookup"><span data-stu-id="26817-173">0</span></span>                                                              |
| <span data-ttu-id="26817-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26817-174">Range-Upper</span></span>            | <span data-ttu-id="26817-175">16</span><span class="sxs-lookup"><span data-stu-id="26817-175">16</span></span>                                                             |
| <span data-ttu-id="26817-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26817-176">Search-Flags</span></span>           | <span data-ttu-id="26817-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26817-177">0x00000000</span></span>                                                     |
| <span data-ttu-id="26817-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26817-178">System-Flags</span></span>           | <span data-ttu-id="26817-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26817-179">0x00000010</span></span>                                                     |
| <span data-ttu-id="26817-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="26817-180">Classes used in</span></span>        | [<span data-ttu-id="26817-181">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="26817-181">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="26817-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="26817-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="26817-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="26817-183">Entry</span></span> | <span data-ttu-id="26817-184">Valor</span><span class="sxs-lookup"><span data-stu-id="26817-184">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="26817-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="26817-185">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="26817-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26817-186">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="26817-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="26817-187">System-Only</span></span>            | <span data-ttu-id="26817-188">Falso</span><span class="sxs-lookup"><span data-stu-id="26817-188">False</span></span>                                                          |
| <span data-ttu-id="26817-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="26817-189">Is-Single-Valued</span></span>       | <span data-ttu-id="26817-190">True</span><span class="sxs-lookup"><span data-stu-id="26817-190">True</span></span>                                                           |
| <span data-ttu-id="26817-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="26817-191">Is Indexed</span></span>             | <span data-ttu-id="26817-192">Falso</span><span class="sxs-lookup"><span data-stu-id="26817-192">False</span></span>                                                          |
| <span data-ttu-id="26817-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="26817-193">In Global Catalog</span></span>      | <span data-ttu-id="26817-194">Falso</span><span class="sxs-lookup"><span data-stu-id="26817-194">False</span></span>                                                          |
| <span data-ttu-id="26817-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="26817-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="26817-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="26817-196">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="26817-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26817-197">Range-Lower</span></span>            | <span data-ttu-id="26817-198">0</span><span class="sxs-lookup"><span data-stu-id="26817-198">0</span></span>                                                              |
| <span data-ttu-id="26817-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26817-199">Range-Upper</span></span>            | <span data-ttu-id="26817-200">16</span><span class="sxs-lookup"><span data-stu-id="26817-200">16</span></span>                                                             |
| <span data-ttu-id="26817-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26817-201">Search-Flags</span></span>           | <span data-ttu-id="26817-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26817-202">0x00000000</span></span>                                                     |
| <span data-ttu-id="26817-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26817-203">System-Flags</span></span>           | <span data-ttu-id="26817-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26817-204">0x00000010</span></span>                                                     |
| <span data-ttu-id="26817-205">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="26817-205">Classes used in</span></span>        | [<span data-ttu-id="26817-206">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="26817-206">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="26817-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26817-207">Windows Server 2008</span></span>



| <span data-ttu-id="26817-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="26817-208">Entry</span></span> | <span data-ttu-id="26817-209">Valor</span><span class="sxs-lookup"><span data-stu-id="26817-209">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="26817-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="26817-210">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="26817-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26817-211">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="26817-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="26817-212">System-Only</span></span>            | <span data-ttu-id="26817-213">Falso</span><span class="sxs-lookup"><span data-stu-id="26817-213">False</span></span>                                                          |
| <span data-ttu-id="26817-214">É de valor único</span><span class="sxs-lookup"><span data-stu-id="26817-214">Is-Single-Valued</span></span>       | <span data-ttu-id="26817-215">True</span><span class="sxs-lookup"><span data-stu-id="26817-215">True</span></span>                                                           |
| <span data-ttu-id="26817-216">É indexado</span><span class="sxs-lookup"><span data-stu-id="26817-216">Is Indexed</span></span>             | <span data-ttu-id="26817-217">Falso</span><span class="sxs-lookup"><span data-stu-id="26817-217">False</span></span>                                                          |
| <span data-ttu-id="26817-218">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="26817-218">In Global Catalog</span></span>      | <span data-ttu-id="26817-219">Falso</span><span class="sxs-lookup"><span data-stu-id="26817-219">False</span></span>                                                          |
| <span data-ttu-id="26817-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="26817-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="26817-221">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="26817-221">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="26817-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26817-222">Range-Lower</span></span>            | <span data-ttu-id="26817-223">0</span><span class="sxs-lookup"><span data-stu-id="26817-223">0</span></span>                                                              |
| <span data-ttu-id="26817-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26817-224">Range-Upper</span></span>            | <span data-ttu-id="26817-225">16</span><span class="sxs-lookup"><span data-stu-id="26817-225">16</span></span>                                                             |
| <span data-ttu-id="26817-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26817-226">Search-Flags</span></span>           | <span data-ttu-id="26817-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26817-227">0x00000000</span></span>                                                     |
| <span data-ttu-id="26817-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26817-228">System-Flags</span></span>           | <span data-ttu-id="26817-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26817-229">0x00000010</span></span>                                                     |
| <span data-ttu-id="26817-230">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="26817-230">Classes used in</span></span>        | [<span data-ttu-id="26817-231">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="26817-231">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="26817-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="26817-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="26817-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="26817-233">Entry</span></span> | <span data-ttu-id="26817-234">Valor</span><span class="sxs-lookup"><span data-stu-id="26817-234">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="26817-235">ID do link</span><span class="sxs-lookup"><span data-stu-id="26817-235">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="26817-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26817-236">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="26817-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="26817-237">System-Only</span></span>            | <span data-ttu-id="26817-238">Falso</span><span class="sxs-lookup"><span data-stu-id="26817-238">False</span></span>                                                          |
| <span data-ttu-id="26817-239">É de valor único</span><span class="sxs-lookup"><span data-stu-id="26817-239">Is-Single-Valued</span></span>       | <span data-ttu-id="26817-240">True</span><span class="sxs-lookup"><span data-stu-id="26817-240">True</span></span>                                                           |
| <span data-ttu-id="26817-241">É indexado</span><span class="sxs-lookup"><span data-stu-id="26817-241">Is Indexed</span></span>             | <span data-ttu-id="26817-242">Falso</span><span class="sxs-lookup"><span data-stu-id="26817-242">False</span></span>                                                          |
| <span data-ttu-id="26817-243">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="26817-243">In Global Catalog</span></span>      | <span data-ttu-id="26817-244">Falso</span><span class="sxs-lookup"><span data-stu-id="26817-244">False</span></span>                                                          |
| <span data-ttu-id="26817-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="26817-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="26817-246">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="26817-246">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="26817-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26817-247">Range-Lower</span></span>            | <span data-ttu-id="26817-248">0</span><span class="sxs-lookup"><span data-stu-id="26817-248">0</span></span>                                                              |
| <span data-ttu-id="26817-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26817-249">Range-Upper</span></span>            | <span data-ttu-id="26817-250">16</span><span class="sxs-lookup"><span data-stu-id="26817-250">16</span></span>                                                             |
| <span data-ttu-id="26817-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26817-251">Search-Flags</span></span>           | <span data-ttu-id="26817-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26817-252">0x00000000</span></span>                                                     |
| <span data-ttu-id="26817-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26817-253">System-Flags</span></span>           | <span data-ttu-id="26817-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26817-254">0x00000010</span></span>                                                     |
| <span data-ttu-id="26817-255">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="26817-255">Classes used in</span></span>        | [<span data-ttu-id="26817-256">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="26817-256">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="26817-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="26817-257">Windows Server 2012</span></span>



| <span data-ttu-id="26817-258">Entrada</span><span class="sxs-lookup"><span data-stu-id="26817-258">Entry</span></span> | <span data-ttu-id="26817-259">Valor</span><span class="sxs-lookup"><span data-stu-id="26817-259">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="26817-260">ID do link</span><span class="sxs-lookup"><span data-stu-id="26817-260">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="26817-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26817-261">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="26817-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="26817-262">System-Only</span></span>            | <span data-ttu-id="26817-263">Falso</span><span class="sxs-lookup"><span data-stu-id="26817-263">False</span></span>                                                          |
| <span data-ttu-id="26817-264">É de valor único</span><span class="sxs-lookup"><span data-stu-id="26817-264">Is-Single-Valued</span></span>       | <span data-ttu-id="26817-265">True</span><span class="sxs-lookup"><span data-stu-id="26817-265">True</span></span>                                                           |
| <span data-ttu-id="26817-266">É indexado</span><span class="sxs-lookup"><span data-stu-id="26817-266">Is Indexed</span></span>             | <span data-ttu-id="26817-267">Falso</span><span class="sxs-lookup"><span data-stu-id="26817-267">False</span></span>                                                          |
| <span data-ttu-id="26817-268">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="26817-268">In Global Catalog</span></span>      | <span data-ttu-id="26817-269">Falso</span><span class="sxs-lookup"><span data-stu-id="26817-269">False</span></span>                                                          |
| <span data-ttu-id="26817-270">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="26817-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="26817-271">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="26817-271">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="26817-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26817-272">Range-Lower</span></span>            | <span data-ttu-id="26817-273">0</span><span class="sxs-lookup"><span data-stu-id="26817-273">0</span></span>                                                              |
| <span data-ttu-id="26817-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26817-274">Range-Upper</span></span>            | <span data-ttu-id="26817-275">16</span><span class="sxs-lookup"><span data-stu-id="26817-275">16</span></span>                                                             |
| <span data-ttu-id="26817-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26817-276">Search-Flags</span></span>           | <span data-ttu-id="26817-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26817-277">0x00000000</span></span>                                                     |
| <span data-ttu-id="26817-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26817-278">System-Flags</span></span>           | <span data-ttu-id="26817-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26817-279">0x00000010</span></span>                                                     |
| <span data-ttu-id="26817-280">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="26817-280">Classes used in</span></span>        | [<span data-ttu-id="26817-281">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="26817-281">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





