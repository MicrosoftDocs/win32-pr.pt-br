---
title: Atributo de membro
description: A lista de usuários que pertencem ao grupo.
ms.assetid: 0f5e249e-1fa1-4191-90e6-94c0b657b7fc
ms.tgt_platform: multiple
keywords:
- Atributo de membro esquema do AD
- atributo de membro esquema do AD
topic_type:
- apiref
api_name:
- Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c237c7cb7b41ae73bcbdff5a13f6cb34f546449b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105771756"
---
# <a name="member-attribute"></a><span data-ttu-id="a5526-105">Atributo de membro</span><span class="sxs-lookup"><span data-stu-id="a5526-105">Member attribute</span></span>

<span data-ttu-id="a5526-106">A lista de usuários que pertencem ao grupo.</span><span class="sxs-lookup"><span data-stu-id="a5526-106">The list of users that belong to the group.</span></span>



| <span data-ttu-id="a5526-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5526-107">Entry</span></span> | <span data-ttu-id="a5526-108">Valor</span><span class="sxs-lookup"><span data-stu-id="a5526-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="a5526-109">CN</span><span class="sxs-lookup"><span data-stu-id="a5526-109">CN</span></span>                | <span data-ttu-id="a5526-110">Membro</span><span class="sxs-lookup"><span data-stu-id="a5526-110">Member</span></span>                                                |
| <span data-ttu-id="a5526-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a5526-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a5526-112">member</span><span class="sxs-lookup"><span data-stu-id="a5526-112">member</span></span>                                                |
| <span data-ttu-id="a5526-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a5526-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="a5526-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a5526-114">Update Privilege</span></span>  | <span data-ttu-id="a5526-115">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="a5526-115">Domain administrator</span></span>                                  |
| <span data-ttu-id="a5526-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a5526-116">Update Frequency</span></span>  | <span data-ttu-id="a5526-117">Cada vez que um usuário é adicionado ou removido de um grupo.</span><span class="sxs-lookup"><span data-stu-id="a5526-117">Each time a user is added to or removed from a group.</span></span> |
| <span data-ttu-id="a5526-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a5526-118">Attribute-Id</span></span>      | <span data-ttu-id="a5526-119">2.5.4.31</span><span class="sxs-lookup"><span data-stu-id="a5526-119">2.5.4.31</span></span>                                              |
| <span data-ttu-id="a5526-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a5526-120">System-Id-Guid</span></span>    | <span data-ttu-id="a5526-121">bf9679c0-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a5526-121">bf9679c0-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="a5526-122">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5526-122">Syntax</span></span>            | [<span data-ttu-id="a5526-123">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="a5526-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)               |



## <a name="implementations"></a><span data-ttu-id="a5526-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="a5526-124">Implementations</span></span>

-   [<span data-ttu-id="a5526-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a5526-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a5526-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a5526-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a5526-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a5526-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a5526-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a5526-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a5526-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a5526-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a5526-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a5526-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a5526-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a5526-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a5526-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a5526-132">Windows 2000 Server</span></span>



| <span data-ttu-id="a5526-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5526-133">Entry</span></span> | <span data-ttu-id="a5526-134">Valor</span><span class="sxs-lookup"><span data-stu-id="a5526-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5526-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="a5526-135">Link-Id</span></span>                | <span data-ttu-id="a5526-136">2</span><span class="sxs-lookup"><span data-stu-id="a5526-136">2</span></span>                                                                                       |
| <span data-ttu-id="a5526-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5526-137">MAPI-Id</span></span>                | <span data-ttu-id="a5526-138">0x8009</span><span class="sxs-lookup"><span data-stu-id="a5526-138">0x8009</span></span>                                                                                  |
| <span data-ttu-id="a5526-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5526-139">System-Only</span></span>            | <span data-ttu-id="a5526-140">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-140">False</span></span>                                                                                   |
| <span data-ttu-id="a5526-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a5526-141">Is-Single-Valued</span></span>       | <span data-ttu-id="a5526-142">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-142">False</span></span>                                                                                   |
| <span data-ttu-id="a5526-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="a5526-143">Is Indexed</span></span>             | <span data-ttu-id="a5526-144">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-144">False</span></span>                                                                                   |
| <span data-ttu-id="a5526-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a5526-145">In Global Catalog</span></span>      | <span data-ttu-id="a5526-146">True</span><span class="sxs-lookup"><span data-stu-id="a5526-146">True</span></span>                                                                                    |
| <span data-ttu-id="a5526-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a5526-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5526-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a5526-148">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="a5526-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5526-149">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="a5526-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5526-150">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="a5526-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5526-151">Search-Flags</span></span>           | <span data-ttu-id="a5526-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5526-152">0x00000000</span></span>                                                                              |
| <span data-ttu-id="a5526-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5526-153">System-Flags</span></span>           | <span data-ttu-id="a5526-154">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a5526-154">0x00000012</span></span>                                                                              |
| <span data-ttu-id="a5526-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a5526-155">Classes used in</span></span>        | [<span data-ttu-id="a5526-156">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="a5526-156">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="a5526-157">**Grupos de nomes**</span><span class="sxs-lookup"><span data-stu-id="a5526-157">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a5526-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a5526-158">Windows Server 2003</span></span>



| <span data-ttu-id="a5526-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5526-159">Entry</span></span> | <span data-ttu-id="a5526-160">Valor</span><span class="sxs-lookup"><span data-stu-id="a5526-160">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5526-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="a5526-161">Link-Id</span></span>                | <span data-ttu-id="a5526-162">2</span><span class="sxs-lookup"><span data-stu-id="a5526-162">2</span></span>                                                                                                                                     |
| <span data-ttu-id="a5526-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5526-163">MAPI-Id</span></span>                | <span data-ttu-id="a5526-164">0x8009</span><span class="sxs-lookup"><span data-stu-id="a5526-164">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="a5526-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5526-165">System-Only</span></span>            | <span data-ttu-id="a5526-166">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-166">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a5526-167">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a5526-167">Is-Single-Valued</span></span>       | <span data-ttu-id="a5526-168">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-168">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a5526-169">É indexado</span><span class="sxs-lookup"><span data-stu-id="a5526-169">Is Indexed</span></span>             | <span data-ttu-id="a5526-170">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-170">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a5526-171">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a5526-171">In Global Catalog</span></span>      | <span data-ttu-id="a5526-172">True</span><span class="sxs-lookup"><span data-stu-id="a5526-172">True</span></span>                                                                                                                                  |
| <span data-ttu-id="a5526-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a5526-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5526-174">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a5526-174">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="a5526-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5526-175">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="a5526-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5526-176">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="a5526-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5526-177">Search-Flags</span></span>           | <span data-ttu-id="a5526-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5526-178">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="a5526-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5526-179">System-Flags</span></span>           | <span data-ttu-id="a5526-180">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a5526-180">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="a5526-181">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a5526-181">Classes used in</span></span>        | [<span data-ttu-id="a5526-182">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="a5526-182">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="a5526-183">**Grupos de nomes**</span><span class="sxs-lookup"><span data-stu-id="a5526-183">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="a5526-184">**Grupo MSMQ**</span><span class="sxs-lookup"><span data-stu-id="a5526-184">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a5526-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="a5526-185">ADAM</span></span>



| <span data-ttu-id="a5526-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5526-186">Entry</span></span> | <span data-ttu-id="a5526-187">Valor</span><span class="sxs-lookup"><span data-stu-id="a5526-187">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="a5526-188">ID do link</span><span class="sxs-lookup"><span data-stu-id="a5526-188">Link-Id</span></span>                | <span data-ttu-id="a5526-189">2</span><span class="sxs-lookup"><span data-stu-id="a5526-189">2</span></span>                                   |
| <span data-ttu-id="a5526-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5526-190">MAPI-Id</span></span>                | <span data-ttu-id="a5526-191">0x8009</span><span class="sxs-lookup"><span data-stu-id="a5526-191">0x8009</span></span>                              |
| <span data-ttu-id="a5526-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5526-192">System-Only</span></span>            | <span data-ttu-id="a5526-193">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-193">False</span></span>                               |
| <span data-ttu-id="a5526-194">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a5526-194">Is-Single-Valued</span></span>       | <span data-ttu-id="a5526-195">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-195">False</span></span>                               |
| <span data-ttu-id="a5526-196">É indexado</span><span class="sxs-lookup"><span data-stu-id="a5526-196">Is Indexed</span></span>             | <span data-ttu-id="a5526-197">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-197">False</span></span>                               |
| <span data-ttu-id="a5526-198">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a5526-198">In Global Catalog</span></span>      | <span data-ttu-id="a5526-199">True</span><span class="sxs-lookup"><span data-stu-id="a5526-199">True</span></span>                                |
| <span data-ttu-id="a5526-200">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a5526-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5526-201">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a5526-201">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="a5526-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5526-202">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="a5526-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5526-203">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="a5526-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5526-204">Search-Flags</span></span>           | <span data-ttu-id="a5526-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5526-205">0x00000000</span></span>                          |
| <span data-ttu-id="a5526-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5526-206">System-Flags</span></span>           | <span data-ttu-id="a5526-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a5526-207">0x00000012</span></span>                          |
| <span data-ttu-id="a5526-208">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a5526-208">Classes used in</span></span>        | [<span data-ttu-id="a5526-209">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="a5526-209">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a5526-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a5526-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a5526-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5526-211">Entry</span></span> | <span data-ttu-id="a5526-212">Valor</span><span class="sxs-lookup"><span data-stu-id="a5526-212">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5526-213">ID do link</span><span class="sxs-lookup"><span data-stu-id="a5526-213">Link-Id</span></span>                | <span data-ttu-id="a5526-214">2</span><span class="sxs-lookup"><span data-stu-id="a5526-214">2</span></span>                                                                                                                                     |
| <span data-ttu-id="a5526-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5526-215">MAPI-Id</span></span>                | <span data-ttu-id="a5526-216">0x8009</span><span class="sxs-lookup"><span data-stu-id="a5526-216">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="a5526-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5526-217">System-Only</span></span>            | <span data-ttu-id="a5526-218">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-218">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a5526-219">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a5526-219">Is-Single-Valued</span></span>       | <span data-ttu-id="a5526-220">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-220">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a5526-221">É indexado</span><span class="sxs-lookup"><span data-stu-id="a5526-221">Is Indexed</span></span>             | <span data-ttu-id="a5526-222">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-222">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a5526-223">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a5526-223">In Global Catalog</span></span>      | <span data-ttu-id="a5526-224">True</span><span class="sxs-lookup"><span data-stu-id="a5526-224">True</span></span>                                                                                                                                  |
| <span data-ttu-id="a5526-225">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a5526-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5526-226">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a5526-226">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="a5526-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5526-227">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="a5526-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5526-228">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="a5526-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5526-229">Search-Flags</span></span>           | <span data-ttu-id="a5526-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5526-230">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="a5526-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5526-231">System-Flags</span></span>           | <span data-ttu-id="a5526-232">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a5526-232">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="a5526-233">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a5526-233">Classes used in</span></span>        | [<span data-ttu-id="a5526-234">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="a5526-234">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="a5526-235">**Grupos de nomes**</span><span class="sxs-lookup"><span data-stu-id="a5526-235">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="a5526-236">**Grupo MSMQ**</span><span class="sxs-lookup"><span data-stu-id="a5526-236">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a5526-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5526-237">Windows Server 2008</span></span>



| <span data-ttu-id="a5526-238">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5526-238">Entry</span></span> | <span data-ttu-id="a5526-239">Valor</span><span class="sxs-lookup"><span data-stu-id="a5526-239">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5526-240">ID do link</span><span class="sxs-lookup"><span data-stu-id="a5526-240">Link-Id</span></span>                | <span data-ttu-id="a5526-241">2</span><span class="sxs-lookup"><span data-stu-id="a5526-241">2</span></span>                                                                                                                                     |
| <span data-ttu-id="a5526-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5526-242">MAPI-Id</span></span>                | <span data-ttu-id="a5526-243">0x8009</span><span class="sxs-lookup"><span data-stu-id="a5526-243">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="a5526-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5526-244">System-Only</span></span>            | <span data-ttu-id="a5526-245">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-245">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a5526-246">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a5526-246">Is-Single-Valued</span></span>       | <span data-ttu-id="a5526-247">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-247">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a5526-248">É indexado</span><span class="sxs-lookup"><span data-stu-id="a5526-248">Is Indexed</span></span>             | <span data-ttu-id="a5526-249">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-249">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a5526-250">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a5526-250">In Global Catalog</span></span>      | <span data-ttu-id="a5526-251">True</span><span class="sxs-lookup"><span data-stu-id="a5526-251">True</span></span>                                                                                                                                  |
| <span data-ttu-id="a5526-252">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a5526-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5526-253">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a5526-253">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="a5526-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5526-254">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="a5526-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5526-255">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="a5526-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5526-256">Search-Flags</span></span>           | <span data-ttu-id="a5526-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5526-257">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="a5526-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5526-258">System-Flags</span></span>           | <span data-ttu-id="a5526-259">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a5526-259">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="a5526-260">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a5526-260">Classes used in</span></span>        | [<span data-ttu-id="a5526-261">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="a5526-261">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="a5526-262">**Grupos de nomes**</span><span class="sxs-lookup"><span data-stu-id="a5526-262">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="a5526-263">**Grupo MSMQ**</span><span class="sxs-lookup"><span data-stu-id="a5526-263">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a5526-264">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a5526-264">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a5526-265">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5526-265">Entry</span></span> | <span data-ttu-id="a5526-266">Valor</span><span class="sxs-lookup"><span data-stu-id="a5526-266">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5526-267">ID do link</span><span class="sxs-lookup"><span data-stu-id="a5526-267">Link-Id</span></span>                | <span data-ttu-id="a5526-268">2</span><span class="sxs-lookup"><span data-stu-id="a5526-268">2</span></span>                                                                                                                                     |
| <span data-ttu-id="a5526-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5526-269">MAPI-Id</span></span>                | <span data-ttu-id="a5526-270">0x8009</span><span class="sxs-lookup"><span data-stu-id="a5526-270">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="a5526-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5526-271">System-Only</span></span>            | <span data-ttu-id="a5526-272">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-272">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a5526-273">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a5526-273">Is-Single-Valued</span></span>       | <span data-ttu-id="a5526-274">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-274">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a5526-275">É indexado</span><span class="sxs-lookup"><span data-stu-id="a5526-275">Is Indexed</span></span>             | <span data-ttu-id="a5526-276">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-276">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a5526-277">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a5526-277">In Global Catalog</span></span>      | <span data-ttu-id="a5526-278">True</span><span class="sxs-lookup"><span data-stu-id="a5526-278">True</span></span>                                                                                                                                  |
| <span data-ttu-id="a5526-279">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a5526-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5526-280">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a5526-280">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="a5526-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5526-281">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="a5526-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5526-282">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="a5526-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5526-283">Search-Flags</span></span>           | <span data-ttu-id="a5526-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5526-284">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="a5526-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5526-285">System-Flags</span></span>           | <span data-ttu-id="a5526-286">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a5526-286">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="a5526-287">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a5526-287">Classes used in</span></span>        | [<span data-ttu-id="a5526-288">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="a5526-288">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="a5526-289">**Grupos de nomes**</span><span class="sxs-lookup"><span data-stu-id="a5526-289">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="a5526-290">**Grupo MSMQ**</span><span class="sxs-lookup"><span data-stu-id="a5526-290">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a5526-291">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a5526-291">Windows Server 2012</span></span>



| <span data-ttu-id="a5526-292">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5526-292">Entry</span></span> | <span data-ttu-id="a5526-293">Valor</span><span class="sxs-lookup"><span data-stu-id="a5526-293">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5526-294">ID do link</span><span class="sxs-lookup"><span data-stu-id="a5526-294">Link-Id</span></span>                | <span data-ttu-id="a5526-295">2</span><span class="sxs-lookup"><span data-stu-id="a5526-295">2</span></span>                                                                                                                                     |
| <span data-ttu-id="a5526-296">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5526-296">MAPI-Id</span></span>                | <span data-ttu-id="a5526-297">0x8009</span><span class="sxs-lookup"><span data-stu-id="a5526-297">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="a5526-298">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5526-298">System-Only</span></span>            | <span data-ttu-id="a5526-299">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-299">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a5526-300">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a5526-300">Is-Single-Valued</span></span>       | <span data-ttu-id="a5526-301">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-301">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a5526-302">É indexado</span><span class="sxs-lookup"><span data-stu-id="a5526-302">Is Indexed</span></span>             | <span data-ttu-id="a5526-303">Falso</span><span class="sxs-lookup"><span data-stu-id="a5526-303">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a5526-304">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a5526-304">In Global Catalog</span></span>      | <span data-ttu-id="a5526-305">True</span><span class="sxs-lookup"><span data-stu-id="a5526-305">True</span></span>                                                                                                                                  |
| <span data-ttu-id="a5526-306">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a5526-306">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5526-307">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a5526-307">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="a5526-308">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5526-308">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="a5526-309">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5526-309">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="a5526-310">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5526-310">Search-Flags</span></span>           | <span data-ttu-id="a5526-311">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5526-311">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="a5526-312">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5526-312">System-Flags</span></span>           | <span data-ttu-id="a5526-313">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a5526-313">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="a5526-314">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a5526-314">Classes used in</span></span>        | [<span data-ttu-id="a5526-315">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="a5526-315">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="a5526-316">**Grupos de nomes**</span><span class="sxs-lookup"><span data-stu-id="a5526-316">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="a5526-317">**Grupo MSMQ**</span><span class="sxs-lookup"><span data-stu-id="a5526-317">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



 

 





