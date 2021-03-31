---
title: Admin-Count atributo
description: Indica que um determinado objeto teve suas ACLs alteradas para um valor mais seguro pelo sistema porque ele era um membro de um dos grupos administrativos (de forma direta ou transitiva).
ms.assetid: b2384ada-a792-42fa-be64-291d23e00887
ms.tgt_platform: multiple
keywords:
- Esquema de Admin-Count do atributo AD
- Esquema de AD do atributo adminCount
topic_type:
- apiref
api_name:
- Admin-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95b953aebaa39bb3fc3e4c9cf96632f32a37850
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645601"
---
# <a name="admin-count-attribute"></a><span data-ttu-id="c4237-105">Admin-Count atributo</span><span class="sxs-lookup"><span data-stu-id="c4237-105">Admin-Count attribute</span></span>

<span data-ttu-id="c4237-106">Indica que um determinado objeto teve suas ACLs alteradas para um valor mais seguro pelo sistema porque ele era um membro de um dos grupos administrativos (de forma direta ou transitiva).</span><span class="sxs-lookup"><span data-stu-id="c4237-106">Indicates that a given object has had its ACLs changed to a more secure value by the system because it was a member of one of the administrative groups (directly or transitively).</span></span>



| <span data-ttu-id="c4237-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4237-107">Entry</span></span> | <span data-ttu-id="c4237-108">Valor</span><span class="sxs-lookup"><span data-stu-id="c4237-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="c4237-109">CN</span><span class="sxs-lookup"><span data-stu-id="c4237-109">CN</span></span>                | <span data-ttu-id="c4237-110">Admin-Count</span><span class="sxs-lookup"><span data-stu-id="c4237-110">Admin-Count</span></span>                                         |
| <span data-ttu-id="c4237-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c4237-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c4237-112">adminCount</span><span class="sxs-lookup"><span data-stu-id="c4237-112">adminCount</span></span>                                          |
| <span data-ttu-id="c4237-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c4237-113">Size</span></span>              | <span data-ttu-id="c4237-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="c4237-114">4 bytes</span></span>                                             |
| <span data-ttu-id="c4237-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="c4237-115">Update Privilege</span></span>  | <span data-ttu-id="c4237-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="c4237-116">This value is set by the system.</span></span>                    |
| <span data-ttu-id="c4237-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="c4237-117">Update Frequency</span></span>  | <span data-ttu-id="c4237-118">Quando um objeto é adicionado a um grupo administrativo.</span><span class="sxs-lookup"><span data-stu-id="c4237-118">When an object is added to an administrative group.</span></span> |
| <span data-ttu-id="c4237-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c4237-119">Attribute-Id</span></span>      | <span data-ttu-id="c4237-120">1.2.840.113556.1.4.150</span><span class="sxs-lookup"><span data-stu-id="c4237-120">1.2.840.113556.1.4.150</span></span>                              |
| <span data-ttu-id="c4237-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c4237-121">System-Id-Guid</span></span>    | <span data-ttu-id="c4237-122">bf967918-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c4237-122">bf967918-0de6-11d0-a285-00aa003049e2</span></span>                |
| <span data-ttu-id="c4237-123">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4237-123">Syntax</span></span>            | [<span data-ttu-id="c4237-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="c4237-124">**Enumeration**</span></span>](s-enumeration.md)                |



## <a name="implementations"></a><span data-ttu-id="c4237-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="c4237-125">Implementations</span></span>

-   [<span data-ttu-id="c4237-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c4237-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c4237-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c4237-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c4237-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c4237-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c4237-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c4237-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c4237-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c4237-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c4237-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c4237-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c4237-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c4237-132">Windows 2000 Server</span></span>



| <span data-ttu-id="c4237-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4237-133">Entry</span></span> | <span data-ttu-id="c4237-134">Valor</span><span class="sxs-lookup"><span data-stu-id="c4237-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c4237-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="c4237-135">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c4237-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4237-136">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c4237-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4237-137">System-Only</span></span>            | <span data-ttu-id="c4237-138">Falso</span><span class="sxs-lookup"><span data-stu-id="c4237-138">False</span></span>                                                                 |
| <span data-ttu-id="c4237-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c4237-139">Is-Single-Valued</span></span>       | <span data-ttu-id="c4237-140">True</span><span class="sxs-lookup"><span data-stu-id="c4237-140">True</span></span>                                                                  |
| <span data-ttu-id="c4237-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="c4237-141">Is Indexed</span></span>             | <span data-ttu-id="c4237-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c4237-142">False</span></span>                                                                 |
| <span data-ttu-id="c4237-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c4237-143">In Global Catalog</span></span>      | <span data-ttu-id="c4237-144">Falso</span><span class="sxs-lookup"><span data-stu-id="c4237-144">False</span></span>                                                                 |
| <span data-ttu-id="c4237-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4237-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4237-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c4237-146">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="c4237-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4237-147">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="c4237-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4237-148">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="c4237-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4237-149">Search-Flags</span></span>           | <span data-ttu-id="c4237-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4237-150">0x00000000</span></span>                                                            |
| <span data-ttu-id="c4237-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4237-151">System-Flags</span></span>           | <span data-ttu-id="c4237-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4237-152">0x00000010</span></span>                                                            |
| <span data-ttu-id="c4237-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c4237-153">Classes used in</span></span>        | [<span data-ttu-id="c4237-154">**Group**</span><span class="sxs-lookup"><span data-stu-id="c4237-154">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="c4237-155">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="c4237-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c4237-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c4237-156">Windows Server 2003</span></span>



| <span data-ttu-id="c4237-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4237-157">Entry</span></span> | <span data-ttu-id="c4237-158">Valor</span><span class="sxs-lookup"><span data-stu-id="c4237-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c4237-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="c4237-159">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c4237-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4237-160">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c4237-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4237-161">System-Only</span></span>            | <span data-ttu-id="c4237-162">Falso</span><span class="sxs-lookup"><span data-stu-id="c4237-162">False</span></span>                                                                 |
| <span data-ttu-id="c4237-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c4237-163">Is-Single-Valued</span></span>       | <span data-ttu-id="c4237-164">True</span><span class="sxs-lookup"><span data-stu-id="c4237-164">True</span></span>                                                                  |
| <span data-ttu-id="c4237-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="c4237-165">Is Indexed</span></span>             | <span data-ttu-id="c4237-166">Falso</span><span class="sxs-lookup"><span data-stu-id="c4237-166">False</span></span>                                                                 |
| <span data-ttu-id="c4237-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c4237-167">In Global Catalog</span></span>      | <span data-ttu-id="c4237-168">Falso</span><span class="sxs-lookup"><span data-stu-id="c4237-168">False</span></span>                                                                 |
| <span data-ttu-id="c4237-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4237-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4237-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c4237-170">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="c4237-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4237-171">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="c4237-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4237-172">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="c4237-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4237-173">Search-Flags</span></span>           | <span data-ttu-id="c4237-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4237-174">0x00000000</span></span>                                                            |
| <span data-ttu-id="c4237-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4237-175">System-Flags</span></span>           | <span data-ttu-id="c4237-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4237-176">0x00000010</span></span>                                                            |
| <span data-ttu-id="c4237-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c4237-177">Classes used in</span></span>        | [<span data-ttu-id="c4237-178">**Group**</span><span class="sxs-lookup"><span data-stu-id="c4237-178">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="c4237-179">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="c4237-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c4237-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c4237-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c4237-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4237-181">Entry</span></span> | <span data-ttu-id="c4237-182">Valor</span><span class="sxs-lookup"><span data-stu-id="c4237-182">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c4237-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="c4237-183">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c4237-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4237-184">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c4237-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4237-185">System-Only</span></span>            | <span data-ttu-id="c4237-186">Falso</span><span class="sxs-lookup"><span data-stu-id="c4237-186">False</span></span>                                                                 |
| <span data-ttu-id="c4237-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c4237-187">Is-Single-Valued</span></span>       | <span data-ttu-id="c4237-188">True</span><span class="sxs-lookup"><span data-stu-id="c4237-188">True</span></span>                                                                  |
| <span data-ttu-id="c4237-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="c4237-189">Is Indexed</span></span>             | <span data-ttu-id="c4237-190">Falso</span><span class="sxs-lookup"><span data-stu-id="c4237-190">False</span></span>                                                                 |
| <span data-ttu-id="c4237-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c4237-191">In Global Catalog</span></span>      | <span data-ttu-id="c4237-192">Falso</span><span class="sxs-lookup"><span data-stu-id="c4237-192">False</span></span>                                                                 |
| <span data-ttu-id="c4237-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4237-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4237-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c4237-194">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="c4237-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4237-195">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="c4237-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4237-196">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="c4237-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4237-197">Search-Flags</span></span>           | <span data-ttu-id="c4237-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4237-198">0x00000000</span></span>                                                            |
| <span data-ttu-id="c4237-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4237-199">System-Flags</span></span>           | <span data-ttu-id="c4237-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4237-200">0x00000010</span></span>                                                            |
| <span data-ttu-id="c4237-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c4237-201">Classes used in</span></span>        | [<span data-ttu-id="c4237-202">**Group**</span><span class="sxs-lookup"><span data-stu-id="c4237-202">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="c4237-203">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="c4237-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c4237-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4237-204">Windows Server 2008</span></span>



| <span data-ttu-id="c4237-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4237-205">Entry</span></span> | <span data-ttu-id="c4237-206">Valor</span><span class="sxs-lookup"><span data-stu-id="c4237-206">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c4237-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="c4237-207">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c4237-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4237-208">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c4237-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4237-209">System-Only</span></span>            | <span data-ttu-id="c4237-210">Falso</span><span class="sxs-lookup"><span data-stu-id="c4237-210">False</span></span>                                                                 |
| <span data-ttu-id="c4237-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c4237-211">Is-Single-Valued</span></span>       | <span data-ttu-id="c4237-212">True</span><span class="sxs-lookup"><span data-stu-id="c4237-212">True</span></span>                                                                  |
| <span data-ttu-id="c4237-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="c4237-213">Is Indexed</span></span>             | <span data-ttu-id="c4237-214">Falso</span><span class="sxs-lookup"><span data-stu-id="c4237-214">False</span></span>                                                                 |
| <span data-ttu-id="c4237-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c4237-215">In Global Catalog</span></span>      | <span data-ttu-id="c4237-216">Falso</span><span class="sxs-lookup"><span data-stu-id="c4237-216">False</span></span>                                                                 |
| <span data-ttu-id="c4237-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4237-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4237-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c4237-218">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="c4237-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4237-219">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="c4237-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4237-220">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="c4237-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4237-221">Search-Flags</span></span>           | <span data-ttu-id="c4237-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4237-222">0x00000000</span></span>                                                            |
| <span data-ttu-id="c4237-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4237-223">System-Flags</span></span>           | <span data-ttu-id="c4237-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4237-224">0x00000010</span></span>                                                            |
| <span data-ttu-id="c4237-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c4237-225">Classes used in</span></span>        | [<span data-ttu-id="c4237-226">**Group**</span><span class="sxs-lookup"><span data-stu-id="c4237-226">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="c4237-227">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="c4237-227">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c4237-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c4237-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c4237-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4237-229">Entry</span></span> | <span data-ttu-id="c4237-230">Valor</span><span class="sxs-lookup"><span data-stu-id="c4237-230">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c4237-231">ID do link</span><span class="sxs-lookup"><span data-stu-id="c4237-231">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c4237-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4237-232">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c4237-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4237-233">System-Only</span></span>            | <span data-ttu-id="c4237-234">Falso</span><span class="sxs-lookup"><span data-stu-id="c4237-234">False</span></span>                                                                 |
| <span data-ttu-id="c4237-235">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c4237-235">Is-Single-Valued</span></span>       | <span data-ttu-id="c4237-236">True</span><span class="sxs-lookup"><span data-stu-id="c4237-236">True</span></span>                                                                  |
| <span data-ttu-id="c4237-237">É indexado</span><span class="sxs-lookup"><span data-stu-id="c4237-237">Is Indexed</span></span>             | <span data-ttu-id="c4237-238">Falso</span><span class="sxs-lookup"><span data-stu-id="c4237-238">False</span></span>                                                                 |
| <span data-ttu-id="c4237-239">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c4237-239">In Global Catalog</span></span>      | <span data-ttu-id="c4237-240">Falso</span><span class="sxs-lookup"><span data-stu-id="c4237-240">False</span></span>                                                                 |
| <span data-ttu-id="c4237-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4237-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4237-242">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c4237-242">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="c4237-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4237-243">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="c4237-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4237-244">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="c4237-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4237-245">Search-Flags</span></span>           | <span data-ttu-id="c4237-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4237-246">0x00000000</span></span>                                                            |
| <span data-ttu-id="c4237-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4237-247">System-Flags</span></span>           | <span data-ttu-id="c4237-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4237-248">0x00000010</span></span>                                                            |
| <span data-ttu-id="c4237-249">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c4237-249">Classes used in</span></span>        | [<span data-ttu-id="c4237-250">**Group**</span><span class="sxs-lookup"><span data-stu-id="c4237-250">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="c4237-251">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="c4237-251">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c4237-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c4237-252">Windows Server 2012</span></span>



| <span data-ttu-id="c4237-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4237-253">Entry</span></span> | <span data-ttu-id="c4237-254">Valor</span><span class="sxs-lookup"><span data-stu-id="c4237-254">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c4237-255">ID do link</span><span class="sxs-lookup"><span data-stu-id="c4237-255">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c4237-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4237-256">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c4237-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4237-257">System-Only</span></span>            | <span data-ttu-id="c4237-258">Falso</span><span class="sxs-lookup"><span data-stu-id="c4237-258">False</span></span>                                                                 |
| <span data-ttu-id="c4237-259">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c4237-259">Is-Single-Valued</span></span>       | <span data-ttu-id="c4237-260">True</span><span class="sxs-lookup"><span data-stu-id="c4237-260">True</span></span>                                                                  |
| <span data-ttu-id="c4237-261">É indexado</span><span class="sxs-lookup"><span data-stu-id="c4237-261">Is Indexed</span></span>             | <span data-ttu-id="c4237-262">Falso</span><span class="sxs-lookup"><span data-stu-id="c4237-262">False</span></span>                                                                 |
| <span data-ttu-id="c4237-263">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c4237-263">In Global Catalog</span></span>      | <span data-ttu-id="c4237-264">Falso</span><span class="sxs-lookup"><span data-stu-id="c4237-264">False</span></span>                                                                 |
| <span data-ttu-id="c4237-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c4237-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4237-266">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c4237-266">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="c4237-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4237-267">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="c4237-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4237-268">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="c4237-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4237-269">Search-Flags</span></span>           | <span data-ttu-id="c4237-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4237-270">0x00000000</span></span>                                                            |
| <span data-ttu-id="c4237-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4237-271">System-Flags</span></span>           | <span data-ttu-id="c4237-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4237-272">0x00000010</span></span>                                                            |
| <span data-ttu-id="c4237-273">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c4237-273">Classes used in</span></span>        | [<span data-ttu-id="c4237-274">**Group**</span><span class="sxs-lookup"><span data-stu-id="c4237-274">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="c4237-275">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="c4237-275">**User**</span></span>](c-user.md)<br/> |



 

 





