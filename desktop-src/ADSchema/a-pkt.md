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
# <a name="pkt-attribute"></a><span data-ttu-id="1acb0-106">Atributo PKT</span><span class="sxs-lookup"><span data-stu-id="1acb0-106">PKT attribute</span></span>

<span data-ttu-id="1acb0-107">Tabela de conhecimento da partição DFS.</span><span class="sxs-lookup"><span data-stu-id="1acb0-107">DFS Partition Knowledge Table.</span></span> <span data-ttu-id="1acb0-108">Descreve a estrutura de uma hierarquia de Sistema de Arquivos Distribuído.</span><span class="sxs-lookup"><span data-stu-id="1acb0-108">Describes the structure of a Distributed File System hierarchy.</span></span>



| <span data-ttu-id="1acb0-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="1acb0-109">Entry</span></span> | <span data-ttu-id="1acb0-110">Valor</span><span class="sxs-lookup"><span data-stu-id="1acb0-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="1acb0-111">CN</span><span class="sxs-lookup"><span data-stu-id="1acb0-111">CN</span></span>                | <span data-ttu-id="1acb0-112">PCT</span><span class="sxs-lookup"><span data-stu-id="1acb0-112">PKT</span></span>                                                   |
| <span data-ttu-id="1acb0-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1acb0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1acb0-114">PCT</span><span class="sxs-lookup"><span data-stu-id="1acb0-114">pKT</span></span>                                                   |
| <span data-ttu-id="1acb0-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="1acb0-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="1acb0-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="1acb0-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="1acb0-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="1acb0-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="1acb0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1acb0-118">Attribute-Id</span></span>      | <span data-ttu-id="1acb0-119">1.2.840.113556.1.4.206</span><span class="sxs-lookup"><span data-stu-id="1acb0-119">1.2.840.113556.1.4.206</span></span>                                |
| <span data-ttu-id="1acb0-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1acb0-120">System-Id-Guid</span></span>    | <span data-ttu-id="1acb0-121">8447f9f1-1027-11d0-a05f-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="1acb0-121">8447f9f1-1027-11d0-a05f-00aa006c33ed</span></span>                  |
| <span data-ttu-id="1acb0-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="1acb0-122">Syntax</span></span>            | [<span data-ttu-id="1acb0-123">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="1acb0-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="1acb0-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="1acb0-124">Implementations</span></span>

-   [<span data-ttu-id="1acb0-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1acb0-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1acb0-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1acb0-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1acb0-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1acb0-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1acb0-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1acb0-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1acb0-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1acb0-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1acb0-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1acb0-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1acb0-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1acb0-131">Windows 2000 Server</span></span>



| <span data-ttu-id="1acb0-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="1acb0-132">Entry</span></span> | <span data-ttu-id="1acb0-133">Valor</span><span class="sxs-lookup"><span data-stu-id="1acb0-133">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="1acb0-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="1acb0-134">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="1acb0-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1acb0-135">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="1acb0-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="1acb0-136">System-Only</span></span>            | <span data-ttu-id="1acb0-137">Falso</span><span class="sxs-lookup"><span data-stu-id="1acb0-137">False</span></span>                                |
| <span data-ttu-id="1acb0-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1acb0-138">Is-Single-Valued</span></span>       | <span data-ttu-id="1acb0-139">True</span><span class="sxs-lookup"><span data-stu-id="1acb0-139">True</span></span>                                 |
| <span data-ttu-id="1acb0-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="1acb0-140">Is Indexed</span></span>             | <span data-ttu-id="1acb0-141">Falso</span><span class="sxs-lookup"><span data-stu-id="1acb0-141">False</span></span>                                |
| <span data-ttu-id="1acb0-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1acb0-142">In Global Catalog</span></span>      | <span data-ttu-id="1acb0-143">Falso</span><span class="sxs-lookup"><span data-stu-id="1acb0-143">False</span></span>                                |
| <span data-ttu-id="1acb0-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1acb0-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="1acb0-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1acb0-145">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="1acb0-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1acb0-146">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="1acb0-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1acb0-147">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="1acb0-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1acb0-148">Search-Flags</span></span>           | <span data-ttu-id="1acb0-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1acb0-149">0x00000000</span></span>                           |
| <span data-ttu-id="1acb0-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1acb0-150">System-Flags</span></span>           | <span data-ttu-id="1acb0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1acb0-151">0x00000010</span></span>                           |
| <span data-ttu-id="1acb0-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1acb0-152">Classes used in</span></span>        | [<span data-ttu-id="1acb0-153">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="1acb0-153">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1acb0-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1acb0-154">Windows Server 2003</span></span>



| <span data-ttu-id="1acb0-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="1acb0-155">Entry</span></span> | <span data-ttu-id="1acb0-156">Valor</span><span class="sxs-lookup"><span data-stu-id="1acb0-156">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="1acb0-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="1acb0-157">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="1acb0-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1acb0-158">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="1acb0-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="1acb0-159">System-Only</span></span>            | <span data-ttu-id="1acb0-160">Falso</span><span class="sxs-lookup"><span data-stu-id="1acb0-160">False</span></span>                                |
| <span data-ttu-id="1acb0-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1acb0-161">Is-Single-Valued</span></span>       | <span data-ttu-id="1acb0-162">True</span><span class="sxs-lookup"><span data-stu-id="1acb0-162">True</span></span>                                 |
| <span data-ttu-id="1acb0-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="1acb0-163">Is Indexed</span></span>             | <span data-ttu-id="1acb0-164">Falso</span><span class="sxs-lookup"><span data-stu-id="1acb0-164">False</span></span>                                |
| <span data-ttu-id="1acb0-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1acb0-165">In Global Catalog</span></span>      | <span data-ttu-id="1acb0-166">Falso</span><span class="sxs-lookup"><span data-stu-id="1acb0-166">False</span></span>                                |
| <span data-ttu-id="1acb0-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1acb0-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="1acb0-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1acb0-168">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="1acb0-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1acb0-169">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="1acb0-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1acb0-170">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="1acb0-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1acb0-171">Search-Flags</span></span>           | <span data-ttu-id="1acb0-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1acb0-172">0x00000000</span></span>                           |
| <span data-ttu-id="1acb0-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1acb0-173">System-Flags</span></span>           | <span data-ttu-id="1acb0-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1acb0-174">0x00000010</span></span>                           |
| <span data-ttu-id="1acb0-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1acb0-175">Classes used in</span></span>        | [<span data-ttu-id="1acb0-176">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="1acb0-176">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1acb0-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1acb0-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1acb0-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="1acb0-178">Entry</span></span> | <span data-ttu-id="1acb0-179">Valor</span><span class="sxs-lookup"><span data-stu-id="1acb0-179">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="1acb0-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="1acb0-180">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="1acb0-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1acb0-181">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="1acb0-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="1acb0-182">System-Only</span></span>            | <span data-ttu-id="1acb0-183">Falso</span><span class="sxs-lookup"><span data-stu-id="1acb0-183">False</span></span>                                |
| <span data-ttu-id="1acb0-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1acb0-184">Is-Single-Valued</span></span>       | <span data-ttu-id="1acb0-185">True</span><span class="sxs-lookup"><span data-stu-id="1acb0-185">True</span></span>                                 |
| <span data-ttu-id="1acb0-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="1acb0-186">Is Indexed</span></span>             | <span data-ttu-id="1acb0-187">Falso</span><span class="sxs-lookup"><span data-stu-id="1acb0-187">False</span></span>                                |
| <span data-ttu-id="1acb0-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1acb0-188">In Global Catalog</span></span>      | <span data-ttu-id="1acb0-189">Falso</span><span class="sxs-lookup"><span data-stu-id="1acb0-189">False</span></span>                                |
| <span data-ttu-id="1acb0-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1acb0-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="1acb0-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1acb0-191">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="1acb0-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1acb0-192">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="1acb0-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1acb0-193">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="1acb0-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1acb0-194">Search-Flags</span></span>           | <span data-ttu-id="1acb0-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1acb0-195">0x00000000</span></span>                           |
| <span data-ttu-id="1acb0-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1acb0-196">System-Flags</span></span>           | <span data-ttu-id="1acb0-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1acb0-197">0x00000010</span></span>                           |
| <span data-ttu-id="1acb0-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1acb0-198">Classes used in</span></span>        | [<span data-ttu-id="1acb0-199">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="1acb0-199">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1acb0-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1acb0-200">Windows Server 2008</span></span>



| <span data-ttu-id="1acb0-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="1acb0-201">Entry</span></span> | <span data-ttu-id="1acb0-202">Valor</span><span class="sxs-lookup"><span data-stu-id="1acb0-202">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="1acb0-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="1acb0-203">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="1acb0-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1acb0-204">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="1acb0-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="1acb0-205">System-Only</span></span>            | <span data-ttu-id="1acb0-206">Falso</span><span class="sxs-lookup"><span data-stu-id="1acb0-206">False</span></span>                                |
| <span data-ttu-id="1acb0-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1acb0-207">Is-Single-Valued</span></span>       | <span data-ttu-id="1acb0-208">True</span><span class="sxs-lookup"><span data-stu-id="1acb0-208">True</span></span>                                 |
| <span data-ttu-id="1acb0-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="1acb0-209">Is Indexed</span></span>             | <span data-ttu-id="1acb0-210">Falso</span><span class="sxs-lookup"><span data-stu-id="1acb0-210">False</span></span>                                |
| <span data-ttu-id="1acb0-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1acb0-211">In Global Catalog</span></span>      | <span data-ttu-id="1acb0-212">Falso</span><span class="sxs-lookup"><span data-stu-id="1acb0-212">False</span></span>                                |
| <span data-ttu-id="1acb0-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1acb0-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="1acb0-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1acb0-214">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="1acb0-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1acb0-215">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="1acb0-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1acb0-216">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="1acb0-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1acb0-217">Search-Flags</span></span>           | <span data-ttu-id="1acb0-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1acb0-218">0x00000000</span></span>                           |
| <span data-ttu-id="1acb0-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1acb0-219">System-Flags</span></span>           | <span data-ttu-id="1acb0-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1acb0-220">0x00000010</span></span>                           |
| <span data-ttu-id="1acb0-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1acb0-221">Classes used in</span></span>        | [<span data-ttu-id="1acb0-222">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="1acb0-222">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1acb0-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1acb0-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1acb0-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="1acb0-224">Entry</span></span> | <span data-ttu-id="1acb0-225">Valor</span><span class="sxs-lookup"><span data-stu-id="1acb0-225">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="1acb0-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="1acb0-226">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="1acb0-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1acb0-227">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="1acb0-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="1acb0-228">System-Only</span></span>            | <span data-ttu-id="1acb0-229">Falso</span><span class="sxs-lookup"><span data-stu-id="1acb0-229">False</span></span>                                |
| <span data-ttu-id="1acb0-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1acb0-230">Is-Single-Valued</span></span>       | <span data-ttu-id="1acb0-231">True</span><span class="sxs-lookup"><span data-stu-id="1acb0-231">True</span></span>                                 |
| <span data-ttu-id="1acb0-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="1acb0-232">Is Indexed</span></span>             | <span data-ttu-id="1acb0-233">Falso</span><span class="sxs-lookup"><span data-stu-id="1acb0-233">False</span></span>                                |
| <span data-ttu-id="1acb0-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1acb0-234">In Global Catalog</span></span>      | <span data-ttu-id="1acb0-235">Falso</span><span class="sxs-lookup"><span data-stu-id="1acb0-235">False</span></span>                                |
| <span data-ttu-id="1acb0-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1acb0-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="1acb0-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1acb0-237">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="1acb0-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1acb0-238">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="1acb0-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1acb0-239">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="1acb0-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1acb0-240">Search-Flags</span></span>           | <span data-ttu-id="1acb0-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1acb0-241">0x00000000</span></span>                           |
| <span data-ttu-id="1acb0-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1acb0-242">System-Flags</span></span>           | <span data-ttu-id="1acb0-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1acb0-243">0x00000010</span></span>                           |
| <span data-ttu-id="1acb0-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1acb0-244">Classes used in</span></span>        | [<span data-ttu-id="1acb0-245">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="1acb0-245">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1acb0-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1acb0-246">Windows Server 2012</span></span>



| <span data-ttu-id="1acb0-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="1acb0-247">Entry</span></span> | <span data-ttu-id="1acb0-248">Valor</span><span class="sxs-lookup"><span data-stu-id="1acb0-248">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="1acb0-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="1acb0-249">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="1acb0-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1acb0-250">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="1acb0-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="1acb0-251">System-Only</span></span>            | <span data-ttu-id="1acb0-252">Falso</span><span class="sxs-lookup"><span data-stu-id="1acb0-252">False</span></span>                                |
| <span data-ttu-id="1acb0-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1acb0-253">Is-Single-Valued</span></span>       | <span data-ttu-id="1acb0-254">True</span><span class="sxs-lookup"><span data-stu-id="1acb0-254">True</span></span>                                 |
| <span data-ttu-id="1acb0-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="1acb0-255">Is Indexed</span></span>             | <span data-ttu-id="1acb0-256">Falso</span><span class="sxs-lookup"><span data-stu-id="1acb0-256">False</span></span>                                |
| <span data-ttu-id="1acb0-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1acb0-257">In Global Catalog</span></span>      | <span data-ttu-id="1acb0-258">Falso</span><span class="sxs-lookup"><span data-stu-id="1acb0-258">False</span></span>                                |
| <span data-ttu-id="1acb0-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1acb0-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="1acb0-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1acb0-260">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="1acb0-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1acb0-261">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="1acb0-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1acb0-262">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="1acb0-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1acb0-263">Search-Flags</span></span>           | <span data-ttu-id="1acb0-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1acb0-264">0x00000000</span></span>                           |
| <span data-ttu-id="1acb0-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1acb0-265">System-Flags</span></span>           | <span data-ttu-id="1acb0-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1acb0-266">0x00000010</span></span>                           |
| <span data-ttu-id="1acb0-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1acb0-267">Classes used in</span></span>        | [<span data-ttu-id="1acb0-268">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="1acb0-268">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



 

 





