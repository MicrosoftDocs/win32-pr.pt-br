---
title: Atributo PKT
description: Tabela de conhecimento da partição DFS. Descreve a estrutura de uma hierarquia de Sistema de Arquivos Distribuído.
ms.assetid: a7b2e9ee-04c0-40e8-8670-8261575a45ab
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo PKT
- Esquema de AD do atributo pKT
topic_type:
- apiref
api_name:
- PKT
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1647e2730b254121763b6598a8ec365b376dd52d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086665"
---
# <a name="pkt-attribute"></a><span data-ttu-id="8f113-106">Atributo PKT</span><span class="sxs-lookup"><span data-stu-id="8f113-106">PKT attribute</span></span>

<span data-ttu-id="8f113-107">Tabela de conhecimento da partição DFS.</span><span class="sxs-lookup"><span data-stu-id="8f113-107">DFS Partition Knowledge Table.</span></span> <span data-ttu-id="8f113-108">Descreve a estrutura de uma hierarquia de Sistema de Arquivos Distribuído.</span><span class="sxs-lookup"><span data-stu-id="8f113-108">Describes the structure of a Distributed File System hierarchy.</span></span>



| <span data-ttu-id="8f113-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="8f113-109">Entry</span></span> | <span data-ttu-id="8f113-110">Valor</span><span class="sxs-lookup"><span data-stu-id="8f113-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="8f113-111">CN</span><span class="sxs-lookup"><span data-stu-id="8f113-111">CN</span></span>                | <span data-ttu-id="8f113-112">PCT</span><span class="sxs-lookup"><span data-stu-id="8f113-112">PKT</span></span>                                                   |
| <span data-ttu-id="8f113-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8f113-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8f113-114">PCT</span><span class="sxs-lookup"><span data-stu-id="8f113-114">pKT</span></span>                                                   |
| <span data-ttu-id="8f113-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="8f113-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="8f113-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="8f113-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="8f113-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="8f113-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="8f113-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8f113-118">Attribute-Id</span></span>      | <span data-ttu-id="8f113-119">1.2.840.113556.1.4.206</span><span class="sxs-lookup"><span data-stu-id="8f113-119">1.2.840.113556.1.4.206</span></span>                                |
| <span data-ttu-id="8f113-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8f113-120">System-Id-Guid</span></span>    | <span data-ttu-id="8f113-121">8447f9f1-1027-11d0-a05f-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="8f113-121">8447f9f1-1027-11d0-a05f-00aa006c33ed</span></span>                  |
| <span data-ttu-id="8f113-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f113-122">Syntax</span></span>            | [<span data-ttu-id="8f113-123">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="8f113-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="8f113-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="8f113-124">Implementations</span></span>

-   [<span data-ttu-id="8f113-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8f113-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8f113-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8f113-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8f113-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8f113-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8f113-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8f113-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8f113-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8f113-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8f113-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8f113-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8f113-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8f113-131">Windows 2000 Server</span></span>



| <span data-ttu-id="8f113-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="8f113-132">Entry</span></span> | <span data-ttu-id="8f113-133">Valor</span><span class="sxs-lookup"><span data-stu-id="8f113-133">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="8f113-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="8f113-134">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="8f113-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f113-135">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="8f113-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f113-136">System-Only</span></span>            | <span data-ttu-id="8f113-137">Falso</span><span class="sxs-lookup"><span data-stu-id="8f113-137">False</span></span>                                |
| <span data-ttu-id="8f113-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8f113-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8f113-139">True</span><span class="sxs-lookup"><span data-stu-id="8f113-139">True</span></span>                                 |
| <span data-ttu-id="8f113-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="8f113-140">Is Indexed</span></span>             | <span data-ttu-id="8f113-141">Falso</span><span class="sxs-lookup"><span data-stu-id="8f113-141">False</span></span>                                |
| <span data-ttu-id="8f113-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8f113-142">In Global Catalog</span></span>      | <span data-ttu-id="8f113-143">Falso</span><span class="sxs-lookup"><span data-stu-id="8f113-143">False</span></span>                                |
| <span data-ttu-id="8f113-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8f113-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f113-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8f113-145">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="8f113-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f113-146">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="8f113-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f113-147">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="8f113-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f113-148">Search-Flags</span></span>           | <span data-ttu-id="8f113-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f113-149">0x00000000</span></span>                           |
| <span data-ttu-id="8f113-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f113-150">System-Flags</span></span>           | <span data-ttu-id="8f113-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f113-151">0x00000010</span></span>                           |
| <span data-ttu-id="8f113-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8f113-152">Classes used in</span></span>        | [<span data-ttu-id="8f113-153">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="8f113-153">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8f113-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f113-154">Windows Server 2003</span></span>



| <span data-ttu-id="8f113-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="8f113-155">Entry</span></span> | <span data-ttu-id="8f113-156">Valor</span><span class="sxs-lookup"><span data-stu-id="8f113-156">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="8f113-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="8f113-157">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="8f113-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f113-158">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="8f113-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f113-159">System-Only</span></span>            | <span data-ttu-id="8f113-160">Falso</span><span class="sxs-lookup"><span data-stu-id="8f113-160">False</span></span>                                |
| <span data-ttu-id="8f113-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8f113-161">Is-Single-Valued</span></span>       | <span data-ttu-id="8f113-162">True</span><span class="sxs-lookup"><span data-stu-id="8f113-162">True</span></span>                                 |
| <span data-ttu-id="8f113-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="8f113-163">Is Indexed</span></span>             | <span data-ttu-id="8f113-164">Falso</span><span class="sxs-lookup"><span data-stu-id="8f113-164">False</span></span>                                |
| <span data-ttu-id="8f113-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8f113-165">In Global Catalog</span></span>      | <span data-ttu-id="8f113-166">Falso</span><span class="sxs-lookup"><span data-stu-id="8f113-166">False</span></span>                                |
| <span data-ttu-id="8f113-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8f113-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f113-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8f113-168">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="8f113-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f113-169">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="8f113-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f113-170">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="8f113-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f113-171">Search-Flags</span></span>           | <span data-ttu-id="8f113-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f113-172">0x00000000</span></span>                           |
| <span data-ttu-id="8f113-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f113-173">System-Flags</span></span>           | <span data-ttu-id="8f113-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f113-174">0x00000010</span></span>                           |
| <span data-ttu-id="8f113-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8f113-175">Classes used in</span></span>        | [<span data-ttu-id="8f113-176">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="8f113-176">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8f113-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8f113-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8f113-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="8f113-178">Entry</span></span> | <span data-ttu-id="8f113-179">Valor</span><span class="sxs-lookup"><span data-stu-id="8f113-179">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="8f113-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="8f113-180">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="8f113-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f113-181">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="8f113-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f113-182">System-Only</span></span>            | <span data-ttu-id="8f113-183">Falso</span><span class="sxs-lookup"><span data-stu-id="8f113-183">False</span></span>                                |
| <span data-ttu-id="8f113-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8f113-184">Is-Single-Valued</span></span>       | <span data-ttu-id="8f113-185">True</span><span class="sxs-lookup"><span data-stu-id="8f113-185">True</span></span>                                 |
| <span data-ttu-id="8f113-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="8f113-186">Is Indexed</span></span>             | <span data-ttu-id="8f113-187">Falso</span><span class="sxs-lookup"><span data-stu-id="8f113-187">False</span></span>                                |
| <span data-ttu-id="8f113-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8f113-188">In Global Catalog</span></span>      | <span data-ttu-id="8f113-189">Falso</span><span class="sxs-lookup"><span data-stu-id="8f113-189">False</span></span>                                |
| <span data-ttu-id="8f113-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8f113-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f113-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8f113-191">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="8f113-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f113-192">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="8f113-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f113-193">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="8f113-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f113-194">Search-Flags</span></span>           | <span data-ttu-id="8f113-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f113-195">0x00000000</span></span>                           |
| <span data-ttu-id="8f113-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f113-196">System-Flags</span></span>           | <span data-ttu-id="8f113-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f113-197">0x00000010</span></span>                           |
| <span data-ttu-id="8f113-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8f113-198">Classes used in</span></span>        | [<span data-ttu-id="8f113-199">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="8f113-199">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8f113-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f113-200">Windows Server 2008</span></span>



| <span data-ttu-id="8f113-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="8f113-201">Entry</span></span> | <span data-ttu-id="8f113-202">Valor</span><span class="sxs-lookup"><span data-stu-id="8f113-202">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="8f113-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="8f113-203">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="8f113-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f113-204">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="8f113-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f113-205">System-Only</span></span>            | <span data-ttu-id="8f113-206">Falso</span><span class="sxs-lookup"><span data-stu-id="8f113-206">False</span></span>                                |
| <span data-ttu-id="8f113-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8f113-207">Is-Single-Valued</span></span>       | <span data-ttu-id="8f113-208">True</span><span class="sxs-lookup"><span data-stu-id="8f113-208">True</span></span>                                 |
| <span data-ttu-id="8f113-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="8f113-209">Is Indexed</span></span>             | <span data-ttu-id="8f113-210">Falso</span><span class="sxs-lookup"><span data-stu-id="8f113-210">False</span></span>                                |
| <span data-ttu-id="8f113-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8f113-211">In Global Catalog</span></span>      | <span data-ttu-id="8f113-212">Falso</span><span class="sxs-lookup"><span data-stu-id="8f113-212">False</span></span>                                |
| <span data-ttu-id="8f113-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8f113-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f113-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8f113-214">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="8f113-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f113-215">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="8f113-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f113-216">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="8f113-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f113-217">Search-Flags</span></span>           | <span data-ttu-id="8f113-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f113-218">0x00000000</span></span>                           |
| <span data-ttu-id="8f113-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f113-219">System-Flags</span></span>           | <span data-ttu-id="8f113-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f113-220">0x00000010</span></span>                           |
| <span data-ttu-id="8f113-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8f113-221">Classes used in</span></span>        | [<span data-ttu-id="8f113-222">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="8f113-222">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8f113-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8f113-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8f113-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="8f113-224">Entry</span></span> | <span data-ttu-id="8f113-225">Valor</span><span class="sxs-lookup"><span data-stu-id="8f113-225">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="8f113-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="8f113-226">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="8f113-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f113-227">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="8f113-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f113-228">System-Only</span></span>            | <span data-ttu-id="8f113-229">Falso</span><span class="sxs-lookup"><span data-stu-id="8f113-229">False</span></span>                                |
| <span data-ttu-id="8f113-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8f113-230">Is-Single-Valued</span></span>       | <span data-ttu-id="8f113-231">True</span><span class="sxs-lookup"><span data-stu-id="8f113-231">True</span></span>                                 |
| <span data-ttu-id="8f113-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="8f113-232">Is Indexed</span></span>             | <span data-ttu-id="8f113-233">Falso</span><span class="sxs-lookup"><span data-stu-id="8f113-233">False</span></span>                                |
| <span data-ttu-id="8f113-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8f113-234">In Global Catalog</span></span>      | <span data-ttu-id="8f113-235">Falso</span><span class="sxs-lookup"><span data-stu-id="8f113-235">False</span></span>                                |
| <span data-ttu-id="8f113-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8f113-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f113-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8f113-237">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="8f113-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f113-238">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="8f113-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f113-239">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="8f113-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f113-240">Search-Flags</span></span>           | <span data-ttu-id="8f113-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f113-241">0x00000000</span></span>                           |
| <span data-ttu-id="8f113-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f113-242">System-Flags</span></span>           | <span data-ttu-id="8f113-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f113-243">0x00000010</span></span>                           |
| <span data-ttu-id="8f113-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8f113-244">Classes used in</span></span>        | [<span data-ttu-id="8f113-245">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="8f113-245">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8f113-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8f113-246">Windows Server 2012</span></span>



| <span data-ttu-id="8f113-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="8f113-247">Entry</span></span> | <span data-ttu-id="8f113-248">Valor</span><span class="sxs-lookup"><span data-stu-id="8f113-248">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="8f113-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="8f113-249">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="8f113-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f113-250">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="8f113-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f113-251">System-Only</span></span>            | <span data-ttu-id="8f113-252">Falso</span><span class="sxs-lookup"><span data-stu-id="8f113-252">False</span></span>                                |
| <span data-ttu-id="8f113-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8f113-253">Is-Single-Valued</span></span>       | <span data-ttu-id="8f113-254">True</span><span class="sxs-lookup"><span data-stu-id="8f113-254">True</span></span>                                 |
| <span data-ttu-id="8f113-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="8f113-255">Is Indexed</span></span>             | <span data-ttu-id="8f113-256">Falso</span><span class="sxs-lookup"><span data-stu-id="8f113-256">False</span></span>                                |
| <span data-ttu-id="8f113-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8f113-257">In Global Catalog</span></span>      | <span data-ttu-id="8f113-258">Falso</span><span class="sxs-lookup"><span data-stu-id="8f113-258">False</span></span>                                |
| <span data-ttu-id="8f113-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8f113-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f113-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8f113-260">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="8f113-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f113-261">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="8f113-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f113-262">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="8f113-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f113-263">Search-Flags</span></span>           | <span data-ttu-id="8f113-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f113-264">0x00000000</span></span>                           |
| <span data-ttu-id="8f113-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f113-265">System-Flags</span></span>           | <span data-ttu-id="8f113-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f113-266">0x00000010</span></span>                           |
| <span data-ttu-id="8f113-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8f113-267">Classes used in</span></span>        | [<span data-ttu-id="8f113-268">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="8f113-268">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



 

 





