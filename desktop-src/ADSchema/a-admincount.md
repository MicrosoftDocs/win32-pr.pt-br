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
# <a name="admin-count-attribute"></a><span data-ttu-id="3e844-105">Admin-Count atributo</span><span class="sxs-lookup"><span data-stu-id="3e844-105">Admin-Count attribute</span></span>

<span data-ttu-id="3e844-106">Indica que um determinado objeto teve suas ACLs alteradas para um valor mais seguro pelo sistema porque ele era um membro de um dos grupos administrativos (de forma direta ou transitiva).</span><span class="sxs-lookup"><span data-stu-id="3e844-106">Indicates that a given object has had its ACLs changed to a more secure value by the system because it was a member of one of the administrative groups (directly or transitively).</span></span>



| <span data-ttu-id="3e844-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="3e844-107">Entry</span></span> | <span data-ttu-id="3e844-108">Valor</span><span class="sxs-lookup"><span data-stu-id="3e844-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="3e844-109">CN</span><span class="sxs-lookup"><span data-stu-id="3e844-109">CN</span></span>                | <span data-ttu-id="3e844-110">Admin-Count</span><span class="sxs-lookup"><span data-stu-id="3e844-110">Admin-Count</span></span>                                         |
| <span data-ttu-id="3e844-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3e844-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3e844-112">adminCount</span><span class="sxs-lookup"><span data-stu-id="3e844-112">adminCount</span></span>                                          |
| <span data-ttu-id="3e844-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="3e844-113">Size</span></span>              | <span data-ttu-id="3e844-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="3e844-114">4 bytes</span></span>                                             |
| <span data-ttu-id="3e844-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="3e844-115">Update Privilege</span></span>  | <span data-ttu-id="3e844-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="3e844-116">This value is set by the system.</span></span>                    |
| <span data-ttu-id="3e844-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="3e844-117">Update Frequency</span></span>  | <span data-ttu-id="3e844-118">Quando um objeto é adicionado a um grupo administrativo.</span><span class="sxs-lookup"><span data-stu-id="3e844-118">When an object is added to an administrative group.</span></span> |
| <span data-ttu-id="3e844-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3e844-119">Attribute-Id</span></span>      | <span data-ttu-id="3e844-120">1.2.840.113556.1.4.150</span><span class="sxs-lookup"><span data-stu-id="3e844-120">1.2.840.113556.1.4.150</span></span>                              |
| <span data-ttu-id="3e844-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3e844-121">System-Id-Guid</span></span>    | <span data-ttu-id="3e844-122">bf967918-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3e844-122">bf967918-0de6-11d0-a285-00aa003049e2</span></span>                |
| <span data-ttu-id="3e844-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e844-123">Syntax</span></span>            | [<span data-ttu-id="3e844-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="3e844-124">**Enumeration**</span></span>](s-enumeration.md)                |



## <a name="implementations"></a><span data-ttu-id="3e844-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="3e844-125">Implementations</span></span>

-   [<span data-ttu-id="3e844-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3e844-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3e844-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3e844-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3e844-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3e844-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3e844-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3e844-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3e844-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3e844-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3e844-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3e844-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3e844-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3e844-132">Windows 2000 Server</span></span>



| <span data-ttu-id="3e844-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="3e844-133">Entry</span></span> | <span data-ttu-id="3e844-134">Valor</span><span class="sxs-lookup"><span data-stu-id="3e844-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="3e844-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="3e844-135">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="3e844-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e844-136">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="3e844-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e844-137">System-Only</span></span>            | <span data-ttu-id="3e844-138">Falso</span><span class="sxs-lookup"><span data-stu-id="3e844-138">False</span></span>                                                                 |
| <span data-ttu-id="3e844-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3e844-139">Is-Single-Valued</span></span>       | <span data-ttu-id="3e844-140">True</span><span class="sxs-lookup"><span data-stu-id="3e844-140">True</span></span>                                                                  |
| <span data-ttu-id="3e844-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="3e844-141">Is Indexed</span></span>             | <span data-ttu-id="3e844-142">Falso</span><span class="sxs-lookup"><span data-stu-id="3e844-142">False</span></span>                                                                 |
| <span data-ttu-id="3e844-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3e844-143">In Global Catalog</span></span>      | <span data-ttu-id="3e844-144">Falso</span><span class="sxs-lookup"><span data-stu-id="3e844-144">False</span></span>                                                                 |
| <span data-ttu-id="3e844-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e844-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e844-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3e844-146">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="3e844-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e844-147">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="3e844-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e844-148">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="3e844-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e844-149">Search-Flags</span></span>           | <span data-ttu-id="3e844-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e844-150">0x00000000</span></span>                                                            |
| <span data-ttu-id="3e844-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e844-151">System-Flags</span></span>           | <span data-ttu-id="3e844-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e844-152">0x00000010</span></span>                                                            |
| <span data-ttu-id="3e844-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3e844-153">Classes used in</span></span>        | [<span data-ttu-id="3e844-154">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="3e844-154">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="3e844-155">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="3e844-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3e844-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3e844-156">Windows Server 2003</span></span>



| <span data-ttu-id="3e844-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="3e844-157">Entry</span></span> | <span data-ttu-id="3e844-158">Valor</span><span class="sxs-lookup"><span data-stu-id="3e844-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="3e844-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="3e844-159">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="3e844-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e844-160">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="3e844-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e844-161">System-Only</span></span>            | <span data-ttu-id="3e844-162">Falso</span><span class="sxs-lookup"><span data-stu-id="3e844-162">False</span></span>                                                                 |
| <span data-ttu-id="3e844-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3e844-163">Is-Single-Valued</span></span>       | <span data-ttu-id="3e844-164">True</span><span class="sxs-lookup"><span data-stu-id="3e844-164">True</span></span>                                                                  |
| <span data-ttu-id="3e844-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="3e844-165">Is Indexed</span></span>             | <span data-ttu-id="3e844-166">Falso</span><span class="sxs-lookup"><span data-stu-id="3e844-166">False</span></span>                                                                 |
| <span data-ttu-id="3e844-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3e844-167">In Global Catalog</span></span>      | <span data-ttu-id="3e844-168">Falso</span><span class="sxs-lookup"><span data-stu-id="3e844-168">False</span></span>                                                                 |
| <span data-ttu-id="3e844-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e844-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e844-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3e844-170">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="3e844-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e844-171">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="3e844-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e844-172">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="3e844-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e844-173">Search-Flags</span></span>           | <span data-ttu-id="3e844-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e844-174">0x00000000</span></span>                                                            |
| <span data-ttu-id="3e844-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e844-175">System-Flags</span></span>           | <span data-ttu-id="3e844-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e844-176">0x00000010</span></span>                                                            |
| <span data-ttu-id="3e844-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3e844-177">Classes used in</span></span>        | [<span data-ttu-id="3e844-178">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="3e844-178">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="3e844-179">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="3e844-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3e844-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3e844-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3e844-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="3e844-181">Entry</span></span> | <span data-ttu-id="3e844-182">Valor</span><span class="sxs-lookup"><span data-stu-id="3e844-182">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="3e844-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="3e844-183">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="3e844-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e844-184">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="3e844-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e844-185">System-Only</span></span>            | <span data-ttu-id="3e844-186">Falso</span><span class="sxs-lookup"><span data-stu-id="3e844-186">False</span></span>                                                                 |
| <span data-ttu-id="3e844-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3e844-187">Is-Single-Valued</span></span>       | <span data-ttu-id="3e844-188">True</span><span class="sxs-lookup"><span data-stu-id="3e844-188">True</span></span>                                                                  |
| <span data-ttu-id="3e844-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="3e844-189">Is Indexed</span></span>             | <span data-ttu-id="3e844-190">Falso</span><span class="sxs-lookup"><span data-stu-id="3e844-190">False</span></span>                                                                 |
| <span data-ttu-id="3e844-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3e844-191">In Global Catalog</span></span>      | <span data-ttu-id="3e844-192">Falso</span><span class="sxs-lookup"><span data-stu-id="3e844-192">False</span></span>                                                                 |
| <span data-ttu-id="3e844-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e844-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e844-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3e844-194">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="3e844-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e844-195">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="3e844-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e844-196">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="3e844-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e844-197">Search-Flags</span></span>           | <span data-ttu-id="3e844-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e844-198">0x00000000</span></span>                                                            |
| <span data-ttu-id="3e844-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e844-199">System-Flags</span></span>           | <span data-ttu-id="3e844-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e844-200">0x00000010</span></span>                                                            |
| <span data-ttu-id="3e844-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3e844-201">Classes used in</span></span>        | [<span data-ttu-id="3e844-202">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="3e844-202">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="3e844-203">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="3e844-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3e844-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e844-204">Windows Server 2008</span></span>



| <span data-ttu-id="3e844-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="3e844-205">Entry</span></span> | <span data-ttu-id="3e844-206">Valor</span><span class="sxs-lookup"><span data-stu-id="3e844-206">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="3e844-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="3e844-207">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="3e844-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e844-208">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="3e844-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e844-209">System-Only</span></span>            | <span data-ttu-id="3e844-210">Falso</span><span class="sxs-lookup"><span data-stu-id="3e844-210">False</span></span>                                                                 |
| <span data-ttu-id="3e844-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3e844-211">Is-Single-Valued</span></span>       | <span data-ttu-id="3e844-212">True</span><span class="sxs-lookup"><span data-stu-id="3e844-212">True</span></span>                                                                  |
| <span data-ttu-id="3e844-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="3e844-213">Is Indexed</span></span>             | <span data-ttu-id="3e844-214">Falso</span><span class="sxs-lookup"><span data-stu-id="3e844-214">False</span></span>                                                                 |
| <span data-ttu-id="3e844-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3e844-215">In Global Catalog</span></span>      | <span data-ttu-id="3e844-216">Falso</span><span class="sxs-lookup"><span data-stu-id="3e844-216">False</span></span>                                                                 |
| <span data-ttu-id="3e844-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e844-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e844-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3e844-218">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="3e844-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e844-219">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="3e844-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e844-220">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="3e844-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e844-221">Search-Flags</span></span>           | <span data-ttu-id="3e844-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e844-222">0x00000000</span></span>                                                            |
| <span data-ttu-id="3e844-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e844-223">System-Flags</span></span>           | <span data-ttu-id="3e844-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e844-224">0x00000010</span></span>                                                            |
| <span data-ttu-id="3e844-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3e844-225">Classes used in</span></span>        | [<span data-ttu-id="3e844-226">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="3e844-226">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="3e844-227">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="3e844-227">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3e844-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3e844-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3e844-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="3e844-229">Entry</span></span> | <span data-ttu-id="3e844-230">Valor</span><span class="sxs-lookup"><span data-stu-id="3e844-230">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="3e844-231">ID do link</span><span class="sxs-lookup"><span data-stu-id="3e844-231">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="3e844-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e844-232">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="3e844-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e844-233">System-Only</span></span>            | <span data-ttu-id="3e844-234">Falso</span><span class="sxs-lookup"><span data-stu-id="3e844-234">False</span></span>                                                                 |
| <span data-ttu-id="3e844-235">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3e844-235">Is-Single-Valued</span></span>       | <span data-ttu-id="3e844-236">True</span><span class="sxs-lookup"><span data-stu-id="3e844-236">True</span></span>                                                                  |
| <span data-ttu-id="3e844-237">É indexado</span><span class="sxs-lookup"><span data-stu-id="3e844-237">Is Indexed</span></span>             | <span data-ttu-id="3e844-238">Falso</span><span class="sxs-lookup"><span data-stu-id="3e844-238">False</span></span>                                                                 |
| <span data-ttu-id="3e844-239">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3e844-239">In Global Catalog</span></span>      | <span data-ttu-id="3e844-240">Falso</span><span class="sxs-lookup"><span data-stu-id="3e844-240">False</span></span>                                                                 |
| <span data-ttu-id="3e844-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e844-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e844-242">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3e844-242">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="3e844-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e844-243">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="3e844-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e844-244">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="3e844-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e844-245">Search-Flags</span></span>           | <span data-ttu-id="3e844-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e844-246">0x00000000</span></span>                                                            |
| <span data-ttu-id="3e844-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e844-247">System-Flags</span></span>           | <span data-ttu-id="3e844-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e844-248">0x00000010</span></span>                                                            |
| <span data-ttu-id="3e844-249">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3e844-249">Classes used in</span></span>        | [<span data-ttu-id="3e844-250">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="3e844-250">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="3e844-251">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="3e844-251">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3e844-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e844-252">Windows Server 2012</span></span>



| <span data-ttu-id="3e844-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="3e844-253">Entry</span></span> | <span data-ttu-id="3e844-254">Valor</span><span class="sxs-lookup"><span data-stu-id="3e844-254">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="3e844-255">ID do link</span><span class="sxs-lookup"><span data-stu-id="3e844-255">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="3e844-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e844-256">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="3e844-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e844-257">System-Only</span></span>            | <span data-ttu-id="3e844-258">Falso</span><span class="sxs-lookup"><span data-stu-id="3e844-258">False</span></span>                                                                 |
| <span data-ttu-id="3e844-259">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3e844-259">Is-Single-Valued</span></span>       | <span data-ttu-id="3e844-260">True</span><span class="sxs-lookup"><span data-stu-id="3e844-260">True</span></span>                                                                  |
| <span data-ttu-id="3e844-261">É indexado</span><span class="sxs-lookup"><span data-stu-id="3e844-261">Is Indexed</span></span>             | <span data-ttu-id="3e844-262">Falso</span><span class="sxs-lookup"><span data-stu-id="3e844-262">False</span></span>                                                                 |
| <span data-ttu-id="3e844-263">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3e844-263">In Global Catalog</span></span>      | <span data-ttu-id="3e844-264">Falso</span><span class="sxs-lookup"><span data-stu-id="3e844-264">False</span></span>                                                                 |
| <span data-ttu-id="3e844-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e844-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e844-266">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3e844-266">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="3e844-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e844-267">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="3e844-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e844-268">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="3e844-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e844-269">Search-Flags</span></span>           | <span data-ttu-id="3e844-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e844-270">0x00000000</span></span>                                                            |
| <span data-ttu-id="3e844-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e844-271">System-Flags</span></span>           | <span data-ttu-id="3e844-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e844-272">0x00000010</span></span>                                                            |
| <span data-ttu-id="3e844-273">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3e844-273">Classes used in</span></span>        | [<span data-ttu-id="3e844-274">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="3e844-274">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="3e844-275">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="3e844-275">**User**</span></span>](c-user.md)<br/> |



 

 





