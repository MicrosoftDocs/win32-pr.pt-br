---
title: Atributo Vol-Table-IDX-GUID
description: O identificador de índice para uma entrada de tabela de faixa de link-volume.
ms.assetid: f6df4ff1-87aa-480e-90f5-0a47822cd461
ms.tgt_platform: multiple
keywords:
- Vol-Table-IDX-GUID atributo AD Schema
- Esquema de AD do atributo volTableIdxGUID
topic_type:
- apiref
api_name:
- Vol-Table-Idx-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a760d99b6883ea070e2f06daf11227056ea74a08
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104500022"
---
# <a name="vol-table-idx-guid-attribute"></a><span data-ttu-id="d61fe-105">Atributo Vol-Table-IDX-GUID</span><span class="sxs-lookup"><span data-stu-id="d61fe-105">Vol-Table-Idx-GUID attribute</span></span>

<span data-ttu-id="d61fe-106">O identificador de índice para uma entrada de tabela de faixa de link-volume.</span><span class="sxs-lookup"><span data-stu-id="d61fe-106">The index identifier for a Link-Track-Volume table entry.</span></span>



| <span data-ttu-id="d61fe-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d61fe-107">Entry</span></span> | <span data-ttu-id="d61fe-108">Valor</span><span class="sxs-lookup"><span data-stu-id="d61fe-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="d61fe-109">CN</span><span class="sxs-lookup"><span data-stu-id="d61fe-109">CN</span></span>                | <span data-ttu-id="d61fe-110">Vol-Table-IDX-GUID</span><span class="sxs-lookup"><span data-stu-id="d61fe-110">Vol-Table-Idx-GUID</span></span>                                    |
| <span data-ttu-id="d61fe-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d61fe-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d61fe-112">volTableIdxGUID</span><span class="sxs-lookup"><span data-stu-id="d61fe-112">volTableIdxGUID</span></span>                                       |
| <span data-ttu-id="d61fe-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="d61fe-113">Size</span></span>              | <span data-ttu-id="d61fe-114">16 bytes</span><span class="sxs-lookup"><span data-stu-id="d61fe-114">16 bytes</span></span>                                              |
| <span data-ttu-id="d61fe-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="d61fe-115">Update Privilege</span></span>  | <span data-ttu-id="d61fe-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="d61fe-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="d61fe-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="d61fe-117">Update Frequency</span></span>  | <span data-ttu-id="d61fe-118">Sempre que um novo link para um arquivo for criado.</span><span class="sxs-lookup"><span data-stu-id="d61fe-118">Whenever a new link to a file is created.</span></span>             |
| <span data-ttu-id="d61fe-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d61fe-119">Attribute-Id</span></span>      | <span data-ttu-id="d61fe-120">1.2.840.113556.1.4.334</span><span class="sxs-lookup"><span data-stu-id="d61fe-120">1.2.840.113556.1.4.334</span></span>                                |
| <span data-ttu-id="d61fe-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d61fe-121">System-Id-Guid</span></span>    | <span data-ttu-id="d61fe-122">1f0075fb-7e40-11d0-afd6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="d61fe-122">1f0075fb-7e40-11d0-afd6-00c04fd930c9</span></span>                  |
| <span data-ttu-id="d61fe-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="d61fe-123">Syntax</span></span>            | [<span data-ttu-id="d61fe-124">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="d61fe-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="d61fe-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="d61fe-125">Implementations</span></span>

-   [<span data-ttu-id="d61fe-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d61fe-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d61fe-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d61fe-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d61fe-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d61fe-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d61fe-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d61fe-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d61fe-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d61fe-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d61fe-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d61fe-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d61fe-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d61fe-132">Windows 2000 Server</span></span>



| <span data-ttu-id="d61fe-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="d61fe-133">Entry</span></span> | <span data-ttu-id="d61fe-134">Valor</span><span class="sxs-lookup"><span data-stu-id="d61fe-134">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="d61fe-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="d61fe-135">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="d61fe-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d61fe-136">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="d61fe-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="d61fe-137">System-Only</span></span>            | <span data-ttu-id="d61fe-138">Falso</span><span class="sxs-lookup"><span data-stu-id="d61fe-138">False</span></span>                                                          |
| <span data-ttu-id="d61fe-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d61fe-139">Is-Single-Valued</span></span>       | <span data-ttu-id="d61fe-140">True</span><span class="sxs-lookup"><span data-stu-id="d61fe-140">True</span></span>                                                           |
| <span data-ttu-id="d61fe-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="d61fe-141">Is Indexed</span></span>             | <span data-ttu-id="d61fe-142">True</span><span class="sxs-lookup"><span data-stu-id="d61fe-142">True</span></span>                                                           |
| <span data-ttu-id="d61fe-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d61fe-143">In Global Catalog</span></span>      | <span data-ttu-id="d61fe-144">Falso</span><span class="sxs-lookup"><span data-stu-id="d61fe-144">False</span></span>                                                          |
| <span data-ttu-id="d61fe-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d61fe-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="d61fe-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d61fe-146">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="d61fe-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d61fe-147">Range-Lower</span></span>            | <span data-ttu-id="d61fe-148">0</span><span class="sxs-lookup"><span data-stu-id="d61fe-148">0</span></span>                                                              |
| <span data-ttu-id="d61fe-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d61fe-149">Range-Upper</span></span>            | <span data-ttu-id="d61fe-150">16</span><span class="sxs-lookup"><span data-stu-id="d61fe-150">16</span></span>                                                             |
| <span data-ttu-id="d61fe-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d61fe-151">Search-Flags</span></span>           | <span data-ttu-id="d61fe-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d61fe-152">0x00000001</span></span>                                                     |
| <span data-ttu-id="d61fe-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d61fe-153">System-Flags</span></span>           | <span data-ttu-id="d61fe-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d61fe-154">0x00000010</span></span>                                                     |
| <span data-ttu-id="d61fe-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d61fe-155">Classes used in</span></span>        | [<span data-ttu-id="d61fe-156">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="d61fe-156">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d61fe-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d61fe-157">Windows Server 2003</span></span>



| <span data-ttu-id="d61fe-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="d61fe-158">Entry</span></span> | <span data-ttu-id="d61fe-159">Valor</span><span class="sxs-lookup"><span data-stu-id="d61fe-159">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="d61fe-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="d61fe-160">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="d61fe-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d61fe-161">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="d61fe-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="d61fe-162">System-Only</span></span>            | <span data-ttu-id="d61fe-163">Falso</span><span class="sxs-lookup"><span data-stu-id="d61fe-163">False</span></span>                                                          |
| <span data-ttu-id="d61fe-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d61fe-164">Is-Single-Valued</span></span>       | <span data-ttu-id="d61fe-165">True</span><span class="sxs-lookup"><span data-stu-id="d61fe-165">True</span></span>                                                           |
| <span data-ttu-id="d61fe-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="d61fe-166">Is Indexed</span></span>             | <span data-ttu-id="d61fe-167">True</span><span class="sxs-lookup"><span data-stu-id="d61fe-167">True</span></span>                                                           |
| <span data-ttu-id="d61fe-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d61fe-168">In Global Catalog</span></span>      | <span data-ttu-id="d61fe-169">Falso</span><span class="sxs-lookup"><span data-stu-id="d61fe-169">False</span></span>                                                          |
| <span data-ttu-id="d61fe-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d61fe-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="d61fe-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d61fe-171">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="d61fe-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d61fe-172">Range-Lower</span></span>            | <span data-ttu-id="d61fe-173">0</span><span class="sxs-lookup"><span data-stu-id="d61fe-173">0</span></span>                                                              |
| <span data-ttu-id="d61fe-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d61fe-174">Range-Upper</span></span>            | <span data-ttu-id="d61fe-175">16</span><span class="sxs-lookup"><span data-stu-id="d61fe-175">16</span></span>                                                             |
| <span data-ttu-id="d61fe-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d61fe-176">Search-Flags</span></span>           | <span data-ttu-id="d61fe-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d61fe-177">0x00000001</span></span>                                                     |
| <span data-ttu-id="d61fe-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d61fe-178">System-Flags</span></span>           | <span data-ttu-id="d61fe-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d61fe-179">0x00000010</span></span>                                                     |
| <span data-ttu-id="d61fe-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d61fe-180">Classes used in</span></span>        | [<span data-ttu-id="d61fe-181">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="d61fe-181">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d61fe-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d61fe-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d61fe-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="d61fe-183">Entry</span></span> | <span data-ttu-id="d61fe-184">Valor</span><span class="sxs-lookup"><span data-stu-id="d61fe-184">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="d61fe-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="d61fe-185">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="d61fe-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d61fe-186">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="d61fe-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="d61fe-187">System-Only</span></span>            | <span data-ttu-id="d61fe-188">Falso</span><span class="sxs-lookup"><span data-stu-id="d61fe-188">False</span></span>                                                          |
| <span data-ttu-id="d61fe-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d61fe-189">Is-Single-Valued</span></span>       | <span data-ttu-id="d61fe-190">True</span><span class="sxs-lookup"><span data-stu-id="d61fe-190">True</span></span>                                                           |
| <span data-ttu-id="d61fe-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="d61fe-191">Is Indexed</span></span>             | <span data-ttu-id="d61fe-192">True</span><span class="sxs-lookup"><span data-stu-id="d61fe-192">True</span></span>                                                           |
| <span data-ttu-id="d61fe-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d61fe-193">In Global Catalog</span></span>      | <span data-ttu-id="d61fe-194">Falso</span><span class="sxs-lookup"><span data-stu-id="d61fe-194">False</span></span>                                                          |
| <span data-ttu-id="d61fe-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d61fe-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="d61fe-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d61fe-196">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="d61fe-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d61fe-197">Range-Lower</span></span>            | <span data-ttu-id="d61fe-198">0</span><span class="sxs-lookup"><span data-stu-id="d61fe-198">0</span></span>                                                              |
| <span data-ttu-id="d61fe-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d61fe-199">Range-Upper</span></span>            | <span data-ttu-id="d61fe-200">16</span><span class="sxs-lookup"><span data-stu-id="d61fe-200">16</span></span>                                                             |
| <span data-ttu-id="d61fe-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d61fe-201">Search-Flags</span></span>           | <span data-ttu-id="d61fe-202">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d61fe-202">0x00000001</span></span>                                                     |
| <span data-ttu-id="d61fe-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d61fe-203">System-Flags</span></span>           | <span data-ttu-id="d61fe-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d61fe-204">0x00000010</span></span>                                                     |
| <span data-ttu-id="d61fe-205">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d61fe-205">Classes used in</span></span>        | [<span data-ttu-id="d61fe-206">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="d61fe-206">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d61fe-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d61fe-207">Windows Server 2008</span></span>



| <span data-ttu-id="d61fe-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="d61fe-208">Entry</span></span> | <span data-ttu-id="d61fe-209">Valor</span><span class="sxs-lookup"><span data-stu-id="d61fe-209">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="d61fe-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="d61fe-210">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="d61fe-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d61fe-211">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="d61fe-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="d61fe-212">System-Only</span></span>            | <span data-ttu-id="d61fe-213">Falso</span><span class="sxs-lookup"><span data-stu-id="d61fe-213">False</span></span>                                                          |
| <span data-ttu-id="d61fe-214">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d61fe-214">Is-Single-Valued</span></span>       | <span data-ttu-id="d61fe-215">True</span><span class="sxs-lookup"><span data-stu-id="d61fe-215">True</span></span>                                                           |
| <span data-ttu-id="d61fe-216">É indexado</span><span class="sxs-lookup"><span data-stu-id="d61fe-216">Is Indexed</span></span>             | <span data-ttu-id="d61fe-217">True</span><span class="sxs-lookup"><span data-stu-id="d61fe-217">True</span></span>                                                           |
| <span data-ttu-id="d61fe-218">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d61fe-218">In Global Catalog</span></span>      | <span data-ttu-id="d61fe-219">Falso</span><span class="sxs-lookup"><span data-stu-id="d61fe-219">False</span></span>                                                          |
| <span data-ttu-id="d61fe-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d61fe-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="d61fe-221">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d61fe-221">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="d61fe-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d61fe-222">Range-Lower</span></span>            | <span data-ttu-id="d61fe-223">0</span><span class="sxs-lookup"><span data-stu-id="d61fe-223">0</span></span>                                                              |
| <span data-ttu-id="d61fe-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d61fe-224">Range-Upper</span></span>            | <span data-ttu-id="d61fe-225">16</span><span class="sxs-lookup"><span data-stu-id="d61fe-225">16</span></span>                                                             |
| <span data-ttu-id="d61fe-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d61fe-226">Search-Flags</span></span>           | <span data-ttu-id="d61fe-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d61fe-227">0x00000001</span></span>                                                     |
| <span data-ttu-id="d61fe-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d61fe-228">System-Flags</span></span>           | <span data-ttu-id="d61fe-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d61fe-229">0x00000010</span></span>                                                     |
| <span data-ttu-id="d61fe-230">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d61fe-230">Classes used in</span></span>        | [<span data-ttu-id="d61fe-231">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="d61fe-231">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d61fe-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d61fe-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d61fe-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="d61fe-233">Entry</span></span> | <span data-ttu-id="d61fe-234">Valor</span><span class="sxs-lookup"><span data-stu-id="d61fe-234">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="d61fe-235">ID do link</span><span class="sxs-lookup"><span data-stu-id="d61fe-235">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="d61fe-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d61fe-236">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="d61fe-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="d61fe-237">System-Only</span></span>            | <span data-ttu-id="d61fe-238">Falso</span><span class="sxs-lookup"><span data-stu-id="d61fe-238">False</span></span>                                                          |
| <span data-ttu-id="d61fe-239">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d61fe-239">Is-Single-Valued</span></span>       | <span data-ttu-id="d61fe-240">True</span><span class="sxs-lookup"><span data-stu-id="d61fe-240">True</span></span>                                                           |
| <span data-ttu-id="d61fe-241">É indexado</span><span class="sxs-lookup"><span data-stu-id="d61fe-241">Is Indexed</span></span>             | <span data-ttu-id="d61fe-242">True</span><span class="sxs-lookup"><span data-stu-id="d61fe-242">True</span></span>                                                           |
| <span data-ttu-id="d61fe-243">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d61fe-243">In Global Catalog</span></span>      | <span data-ttu-id="d61fe-244">Falso</span><span class="sxs-lookup"><span data-stu-id="d61fe-244">False</span></span>                                                          |
| <span data-ttu-id="d61fe-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d61fe-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="d61fe-246">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d61fe-246">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="d61fe-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d61fe-247">Range-Lower</span></span>            | <span data-ttu-id="d61fe-248">0</span><span class="sxs-lookup"><span data-stu-id="d61fe-248">0</span></span>                                                              |
| <span data-ttu-id="d61fe-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d61fe-249">Range-Upper</span></span>            | <span data-ttu-id="d61fe-250">16</span><span class="sxs-lookup"><span data-stu-id="d61fe-250">16</span></span>                                                             |
| <span data-ttu-id="d61fe-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d61fe-251">Search-Flags</span></span>           | <span data-ttu-id="d61fe-252">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d61fe-252">0x00000001</span></span>                                                     |
| <span data-ttu-id="d61fe-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d61fe-253">System-Flags</span></span>           | <span data-ttu-id="d61fe-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d61fe-254">0x00000010</span></span>                                                     |
| <span data-ttu-id="d61fe-255">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d61fe-255">Classes used in</span></span>        | [<span data-ttu-id="d61fe-256">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="d61fe-256">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d61fe-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d61fe-257">Windows Server 2012</span></span>



| <span data-ttu-id="d61fe-258">Entrada</span><span class="sxs-lookup"><span data-stu-id="d61fe-258">Entry</span></span> | <span data-ttu-id="d61fe-259">Valor</span><span class="sxs-lookup"><span data-stu-id="d61fe-259">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="d61fe-260">ID do link</span><span class="sxs-lookup"><span data-stu-id="d61fe-260">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="d61fe-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d61fe-261">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="d61fe-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="d61fe-262">System-Only</span></span>            | <span data-ttu-id="d61fe-263">Falso</span><span class="sxs-lookup"><span data-stu-id="d61fe-263">False</span></span>                                                          |
| <span data-ttu-id="d61fe-264">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d61fe-264">Is-Single-Valued</span></span>       | <span data-ttu-id="d61fe-265">True</span><span class="sxs-lookup"><span data-stu-id="d61fe-265">True</span></span>                                                           |
| <span data-ttu-id="d61fe-266">É indexado</span><span class="sxs-lookup"><span data-stu-id="d61fe-266">Is Indexed</span></span>             | <span data-ttu-id="d61fe-267">True</span><span class="sxs-lookup"><span data-stu-id="d61fe-267">True</span></span>                                                           |
| <span data-ttu-id="d61fe-268">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d61fe-268">In Global Catalog</span></span>      | <span data-ttu-id="d61fe-269">Falso</span><span class="sxs-lookup"><span data-stu-id="d61fe-269">False</span></span>                                                          |
| <span data-ttu-id="d61fe-270">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d61fe-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="d61fe-271">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d61fe-271">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="d61fe-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d61fe-272">Range-Lower</span></span>            | <span data-ttu-id="d61fe-273">0</span><span class="sxs-lookup"><span data-stu-id="d61fe-273">0</span></span>                                                              |
| <span data-ttu-id="d61fe-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d61fe-274">Range-Upper</span></span>            | <span data-ttu-id="d61fe-275">16</span><span class="sxs-lookup"><span data-stu-id="d61fe-275">16</span></span>                                                             |
| <span data-ttu-id="d61fe-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d61fe-276">Search-Flags</span></span>           | <span data-ttu-id="d61fe-277">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d61fe-277">0x00000001</span></span>                                                     |
| <span data-ttu-id="d61fe-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d61fe-278">System-Flags</span></span>           | <span data-ttu-id="d61fe-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d61fe-279">0x00000010</span></span>                                                     |
| <span data-ttu-id="d61fe-280">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d61fe-280">Classes used in</span></span>        | [<span data-ttu-id="d61fe-281">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="d61fe-281">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





