---
title: Atributo de não-segurança-membro
description: Membros de não segurança de um grupo. Usado para listas de distribuição do Exchange.
ms.assetid: 0db135e4-dcba-4afb-a174-3c7b2b40688e
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de não segurança-membro
- Esquema de AD do atributo nonSecurityMember
topic_type:
- apiref
api_name:
- Non-Security-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a04919d9d538ff4da97d73e79d14e9a2706032b8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919582"
---
# <a name="non-security-member-attribute"></a><span data-ttu-id="27fbb-106">Atributo de não-segurança-membro</span><span class="sxs-lookup"><span data-stu-id="27fbb-106">Non-Security-Member attribute</span></span>

<span data-ttu-id="27fbb-107">Membros de não segurança de um grupo.</span><span class="sxs-lookup"><span data-stu-id="27fbb-107">Nonsecurity members of a group.</span></span> <span data-ttu-id="27fbb-108">Usado para listas de distribuição do Exchange.</span><span class="sxs-lookup"><span data-stu-id="27fbb-108">Used for Exchange distribution lists.</span></span>



| <span data-ttu-id="27fbb-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="27fbb-109">Entry</span></span> | <span data-ttu-id="27fbb-110">Valor</span><span class="sxs-lookup"><span data-stu-id="27fbb-110">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="27fbb-111">CN</span><span class="sxs-lookup"><span data-stu-id="27fbb-111">CN</span></span>                | <span data-ttu-id="27fbb-112">Não-segurança-membro</span><span class="sxs-lookup"><span data-stu-id="27fbb-112">Non-Security-Member</span></span>                              |
| <span data-ttu-id="27fbb-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="27fbb-113">Ldap-Display-Name</span></span> | <span data-ttu-id="27fbb-114">nonSecurityMember</span><span class="sxs-lookup"><span data-stu-id="27fbb-114">nonSecurityMember</span></span>                                |
| <span data-ttu-id="27fbb-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="27fbb-115">Size</span></span>              | \-                                               |
| <span data-ttu-id="27fbb-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="27fbb-116">Update Privilege</span></span>  | <span data-ttu-id="27fbb-117">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="27fbb-117">Domain administrator</span></span>                             |
| <span data-ttu-id="27fbb-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="27fbb-118">Update Frequency</span></span>  | <span data-ttu-id="27fbb-119">Sempre que um usuário é adicionado ou removido da DL.</span><span class="sxs-lookup"><span data-stu-id="27fbb-119">Whenever a user is added or removed from the DL.</span></span> |
| <span data-ttu-id="27fbb-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="27fbb-120">Attribute-Id</span></span>      | <span data-ttu-id="27fbb-121">1.2.840.113556.1.4.530</span><span class="sxs-lookup"><span data-stu-id="27fbb-121">1.2.840.113556.1.4.530</span></span>                           |
| <span data-ttu-id="27fbb-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="27fbb-122">System-Id-Guid</span></span>    | <span data-ttu-id="27fbb-123">52458018-ca6a-11D0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="27fbb-123">52458018-ca6a-11d0-afff-0000f80367c1</span></span>             |
| <span data-ttu-id="27fbb-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="27fbb-124">Syntax</span></span>            | [<span data-ttu-id="27fbb-125">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="27fbb-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)          |



## <a name="implementations"></a><span data-ttu-id="27fbb-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="27fbb-126">Implementations</span></span>

-   [<span data-ttu-id="27fbb-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="27fbb-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="27fbb-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="27fbb-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="27fbb-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="27fbb-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="27fbb-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="27fbb-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="27fbb-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="27fbb-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="27fbb-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="27fbb-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="27fbb-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="27fbb-133">Windows 2000 Server</span></span>



| <span data-ttu-id="27fbb-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="27fbb-134">Entry</span></span> | <span data-ttu-id="27fbb-135">Valor</span><span class="sxs-lookup"><span data-stu-id="27fbb-135">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="27fbb-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="27fbb-136">Link-Id</span></span>                | <span data-ttu-id="27fbb-137">50</span><span class="sxs-lookup"><span data-stu-id="27fbb-137">50</span></span>                                  |
| <span data-ttu-id="27fbb-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27fbb-138">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="27fbb-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="27fbb-139">System-Only</span></span>            | <span data-ttu-id="27fbb-140">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-140">False</span></span>                               |
| <span data-ttu-id="27fbb-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="27fbb-141">Is-Single-Valued</span></span>       | <span data-ttu-id="27fbb-142">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-142">False</span></span>                               |
| <span data-ttu-id="27fbb-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="27fbb-143">Is Indexed</span></span>             | <span data-ttu-id="27fbb-144">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-144">False</span></span>                               |
| <span data-ttu-id="27fbb-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="27fbb-145">In Global Catalog</span></span>      | <span data-ttu-id="27fbb-146">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-146">False</span></span>                               |
| <span data-ttu-id="27fbb-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27fbb-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="27fbb-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="27fbb-148">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="27fbb-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27fbb-149">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="27fbb-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27fbb-150">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="27fbb-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27fbb-151">Search-Flags</span></span>           | <span data-ttu-id="27fbb-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27fbb-152">0x00000000</span></span>                          |
| <span data-ttu-id="27fbb-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27fbb-153">System-Flags</span></span>           | <span data-ttu-id="27fbb-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27fbb-154">0x00000010</span></span>                          |
| <span data-ttu-id="27fbb-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="27fbb-155">Classes used in</span></span>        | [<span data-ttu-id="27fbb-156">**Group**</span><span class="sxs-lookup"><span data-stu-id="27fbb-156">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="27fbb-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27fbb-157">Windows Server 2003</span></span>



| <span data-ttu-id="27fbb-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="27fbb-158">Entry</span></span> | <span data-ttu-id="27fbb-159">Valor</span><span class="sxs-lookup"><span data-stu-id="27fbb-159">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="27fbb-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="27fbb-160">Link-Id</span></span>                | <span data-ttu-id="27fbb-161">50</span><span class="sxs-lookup"><span data-stu-id="27fbb-161">50</span></span>                                  |
| <span data-ttu-id="27fbb-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27fbb-162">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="27fbb-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="27fbb-163">System-Only</span></span>            | <span data-ttu-id="27fbb-164">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-164">False</span></span>                               |
| <span data-ttu-id="27fbb-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="27fbb-165">Is-Single-Valued</span></span>       | <span data-ttu-id="27fbb-166">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-166">False</span></span>                               |
| <span data-ttu-id="27fbb-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="27fbb-167">Is Indexed</span></span>             | <span data-ttu-id="27fbb-168">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-168">False</span></span>                               |
| <span data-ttu-id="27fbb-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="27fbb-169">In Global Catalog</span></span>      | <span data-ttu-id="27fbb-170">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-170">False</span></span>                               |
| <span data-ttu-id="27fbb-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27fbb-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="27fbb-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="27fbb-172">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="27fbb-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27fbb-173">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="27fbb-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27fbb-174">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="27fbb-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27fbb-175">Search-Flags</span></span>           | <span data-ttu-id="27fbb-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27fbb-176">0x00000000</span></span>                          |
| <span data-ttu-id="27fbb-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27fbb-177">System-Flags</span></span>           | <span data-ttu-id="27fbb-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27fbb-178">0x00000010</span></span>                          |
| <span data-ttu-id="27fbb-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="27fbb-179">Classes used in</span></span>        | [<span data-ttu-id="27fbb-180">**Group**</span><span class="sxs-lookup"><span data-stu-id="27fbb-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="27fbb-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="27fbb-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="27fbb-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="27fbb-182">Entry</span></span> | <span data-ttu-id="27fbb-183">Valor</span><span class="sxs-lookup"><span data-stu-id="27fbb-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="27fbb-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="27fbb-184">Link-Id</span></span>                | <span data-ttu-id="27fbb-185">50</span><span class="sxs-lookup"><span data-stu-id="27fbb-185">50</span></span>                                  |
| <span data-ttu-id="27fbb-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27fbb-186">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="27fbb-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="27fbb-187">System-Only</span></span>            | <span data-ttu-id="27fbb-188">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-188">False</span></span>                               |
| <span data-ttu-id="27fbb-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="27fbb-189">Is-Single-Valued</span></span>       | <span data-ttu-id="27fbb-190">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-190">False</span></span>                               |
| <span data-ttu-id="27fbb-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="27fbb-191">Is Indexed</span></span>             | <span data-ttu-id="27fbb-192">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-192">False</span></span>                               |
| <span data-ttu-id="27fbb-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="27fbb-193">In Global Catalog</span></span>      | <span data-ttu-id="27fbb-194">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-194">False</span></span>                               |
| <span data-ttu-id="27fbb-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27fbb-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="27fbb-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="27fbb-196">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="27fbb-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27fbb-197">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="27fbb-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27fbb-198">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="27fbb-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27fbb-199">Search-Flags</span></span>           | <span data-ttu-id="27fbb-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27fbb-200">0x00000000</span></span>                          |
| <span data-ttu-id="27fbb-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27fbb-201">System-Flags</span></span>           | <span data-ttu-id="27fbb-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27fbb-202">0x00000010</span></span>                          |
| <span data-ttu-id="27fbb-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="27fbb-203">Classes used in</span></span>        | [<span data-ttu-id="27fbb-204">**Group**</span><span class="sxs-lookup"><span data-stu-id="27fbb-204">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="27fbb-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27fbb-205">Windows Server 2008</span></span>



| <span data-ttu-id="27fbb-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="27fbb-206">Entry</span></span> | <span data-ttu-id="27fbb-207">Valor</span><span class="sxs-lookup"><span data-stu-id="27fbb-207">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="27fbb-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="27fbb-208">Link-Id</span></span>                | <span data-ttu-id="27fbb-209">50</span><span class="sxs-lookup"><span data-stu-id="27fbb-209">50</span></span>                                  |
| <span data-ttu-id="27fbb-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27fbb-210">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="27fbb-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="27fbb-211">System-Only</span></span>            | <span data-ttu-id="27fbb-212">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-212">False</span></span>                               |
| <span data-ttu-id="27fbb-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="27fbb-213">Is-Single-Valued</span></span>       | <span data-ttu-id="27fbb-214">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-214">False</span></span>                               |
| <span data-ttu-id="27fbb-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="27fbb-215">Is Indexed</span></span>             | <span data-ttu-id="27fbb-216">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-216">False</span></span>                               |
| <span data-ttu-id="27fbb-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="27fbb-217">In Global Catalog</span></span>      | <span data-ttu-id="27fbb-218">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-218">False</span></span>                               |
| <span data-ttu-id="27fbb-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27fbb-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="27fbb-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="27fbb-220">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="27fbb-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27fbb-221">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="27fbb-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27fbb-222">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="27fbb-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27fbb-223">Search-Flags</span></span>           | <span data-ttu-id="27fbb-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27fbb-224">0x00000000</span></span>                          |
| <span data-ttu-id="27fbb-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27fbb-225">System-Flags</span></span>           | <span data-ttu-id="27fbb-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27fbb-226">0x00000010</span></span>                          |
| <span data-ttu-id="27fbb-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="27fbb-227">Classes used in</span></span>        | [<span data-ttu-id="27fbb-228">**Group**</span><span class="sxs-lookup"><span data-stu-id="27fbb-228">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="27fbb-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="27fbb-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="27fbb-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="27fbb-230">Entry</span></span> | <span data-ttu-id="27fbb-231">Valor</span><span class="sxs-lookup"><span data-stu-id="27fbb-231">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="27fbb-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="27fbb-232">Link-Id</span></span>                | <span data-ttu-id="27fbb-233">50</span><span class="sxs-lookup"><span data-stu-id="27fbb-233">50</span></span>                                  |
| <span data-ttu-id="27fbb-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27fbb-234">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="27fbb-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="27fbb-235">System-Only</span></span>            | <span data-ttu-id="27fbb-236">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-236">False</span></span>                               |
| <span data-ttu-id="27fbb-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="27fbb-237">Is-Single-Valued</span></span>       | <span data-ttu-id="27fbb-238">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-238">False</span></span>                               |
| <span data-ttu-id="27fbb-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="27fbb-239">Is Indexed</span></span>             | <span data-ttu-id="27fbb-240">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-240">False</span></span>                               |
| <span data-ttu-id="27fbb-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="27fbb-241">In Global Catalog</span></span>      | <span data-ttu-id="27fbb-242">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-242">False</span></span>                               |
| <span data-ttu-id="27fbb-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27fbb-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="27fbb-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="27fbb-244">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="27fbb-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27fbb-245">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="27fbb-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27fbb-246">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="27fbb-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27fbb-247">Search-Flags</span></span>           | <span data-ttu-id="27fbb-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27fbb-248">0x00000000</span></span>                          |
| <span data-ttu-id="27fbb-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27fbb-249">System-Flags</span></span>           | <span data-ttu-id="27fbb-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27fbb-250">0x00000010</span></span>                          |
| <span data-ttu-id="27fbb-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="27fbb-251">Classes used in</span></span>        | [<span data-ttu-id="27fbb-252">**Group**</span><span class="sxs-lookup"><span data-stu-id="27fbb-252">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="27fbb-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27fbb-253">Windows Server 2012</span></span>



| <span data-ttu-id="27fbb-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="27fbb-254">Entry</span></span> | <span data-ttu-id="27fbb-255">Valor</span><span class="sxs-lookup"><span data-stu-id="27fbb-255">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="27fbb-256">ID do link</span><span class="sxs-lookup"><span data-stu-id="27fbb-256">Link-Id</span></span>                | <span data-ttu-id="27fbb-257">50</span><span class="sxs-lookup"><span data-stu-id="27fbb-257">50</span></span>                                  |
| <span data-ttu-id="27fbb-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27fbb-258">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="27fbb-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="27fbb-259">System-Only</span></span>            | <span data-ttu-id="27fbb-260">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-260">False</span></span>                               |
| <span data-ttu-id="27fbb-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="27fbb-261">Is-Single-Valued</span></span>       | <span data-ttu-id="27fbb-262">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-262">False</span></span>                               |
| <span data-ttu-id="27fbb-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="27fbb-263">Is Indexed</span></span>             | <span data-ttu-id="27fbb-264">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-264">False</span></span>                               |
| <span data-ttu-id="27fbb-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="27fbb-265">In Global Catalog</span></span>      | <span data-ttu-id="27fbb-266">Falso</span><span class="sxs-lookup"><span data-stu-id="27fbb-266">False</span></span>                               |
| <span data-ttu-id="27fbb-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27fbb-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="27fbb-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="27fbb-268">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="27fbb-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27fbb-269">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="27fbb-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27fbb-270">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="27fbb-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27fbb-271">Search-Flags</span></span>           | <span data-ttu-id="27fbb-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27fbb-272">0x00000000</span></span>                          |
| <span data-ttu-id="27fbb-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27fbb-273">System-Flags</span></span>           | <span data-ttu-id="27fbb-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27fbb-274">0x00000010</span></span>                          |
| <span data-ttu-id="27fbb-275">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="27fbb-275">Classes used in</span></span>        | [<span data-ttu-id="27fbb-276">**Group**</span><span class="sxs-lookup"><span data-stu-id="27fbb-276">**Group**</span></span>](c-group.md)<br/> |



 

 





