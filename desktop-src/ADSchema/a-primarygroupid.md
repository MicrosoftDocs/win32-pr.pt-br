---
title: Atributo Primary-Group-ID
description: Contém o identificador relativo (RID) do grupo primário do usuário. Por padrão, esse é o RID do grupo usuários do domínio.
ms.assetid: 80803734-f7dd-4348-a110-ca6b8bccb60b
ms.tgt_platform: multiple
keywords:
- Esquema primário-grupo-ID de atributo do AD
- Esquema de AD do atributo primaryGroupID
topic_type:
- apiref
api_name:
- Primary-Group-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2b6237ff6e49a01da3b960b58103ae10dca7b2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645514"
---
# <a name="primary-group-id-attribute"></a><span data-ttu-id="417a4-106">Atributo Primary-Group-ID</span><span class="sxs-lookup"><span data-stu-id="417a4-106">Primary-Group-ID attribute</span></span>

<span data-ttu-id="417a4-107">Contém o identificador relativo (RID) do grupo primário do usuário.</span><span class="sxs-lookup"><span data-stu-id="417a4-107">Contains the relative identifier (RID) for the primary group of the user.</span></span> <span data-ttu-id="417a4-108">Por padrão, esse é o RID do grupo usuários do domínio.</span><span class="sxs-lookup"><span data-stu-id="417a4-108">By default, this is the RID for the Domain Users group.</span></span>



| <span data-ttu-id="417a4-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="417a4-109">Entry</span></span> | <span data-ttu-id="417a4-110">Valor</span><span class="sxs-lookup"><span data-stu-id="417a4-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="417a4-111">CN</span><span class="sxs-lookup"><span data-stu-id="417a4-111">CN</span></span>                | <span data-ttu-id="417a4-112">ID do grupo primário</span><span class="sxs-lookup"><span data-stu-id="417a4-112">Primary-Group-ID</span></span>                     |
| <span data-ttu-id="417a4-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="417a4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="417a4-114">primaryGroupID</span><span class="sxs-lookup"><span data-stu-id="417a4-114">primaryGroupID</span></span>                       |
| <span data-ttu-id="417a4-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="417a4-115">Size</span></span>              | <span data-ttu-id="417a4-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="417a4-116">4 bytes</span></span>                              |
| <span data-ttu-id="417a4-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="417a4-117">Update Privilege</span></span>  | <span data-ttu-id="417a4-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="417a4-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="417a4-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="417a4-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="417a4-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="417a4-120">Attribute-Id</span></span>      | <span data-ttu-id="417a4-121">1.2.840.113556.1.4.98</span><span class="sxs-lookup"><span data-stu-id="417a4-121">1.2.840.113556.1.4.98</span></span>                |
| <span data-ttu-id="417a4-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="417a4-122">System-Id-Guid</span></span>    | <span data-ttu-id="417a4-123">bf967a00-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="417a4-123">bf967a00-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="417a4-124">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="417a4-124">Syntax</span></span>            | [<span data-ttu-id="417a4-125">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="417a4-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="417a4-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="417a4-126">Implementations</span></span>

-   [<span data-ttu-id="417a4-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="417a4-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="417a4-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="417a4-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="417a4-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="417a4-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="417a4-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="417a4-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="417a4-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="417a4-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="417a4-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="417a4-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="417a4-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="417a4-133">Windows 2000 Server</span></span>



| <span data-ttu-id="417a4-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="417a4-134">Entry</span></span> | <span data-ttu-id="417a4-135">Valor</span><span class="sxs-lookup"><span data-stu-id="417a4-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="417a4-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="417a4-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="417a4-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="417a4-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="417a4-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="417a4-138">System-Only</span></span>            | <span data-ttu-id="417a4-139">Falso</span><span class="sxs-lookup"><span data-stu-id="417a4-139">False</span></span>                             |
| <span data-ttu-id="417a4-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="417a4-140">Is-Single-Valued</span></span>       | <span data-ttu-id="417a4-141">True</span><span class="sxs-lookup"><span data-stu-id="417a4-141">True</span></span>                              |
| <span data-ttu-id="417a4-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="417a4-142">Is Indexed</span></span>             | <span data-ttu-id="417a4-143">True</span><span class="sxs-lookup"><span data-stu-id="417a4-143">True</span></span>                              |
| <span data-ttu-id="417a4-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="417a4-144">In Global Catalog</span></span>      | <span data-ttu-id="417a4-145">True</span><span class="sxs-lookup"><span data-stu-id="417a4-145">True</span></span>                              |
| <span data-ttu-id="417a4-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="417a4-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="417a4-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="417a4-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="417a4-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="417a4-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="417a4-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="417a4-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="417a4-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="417a4-150">Search-Flags</span></span>           | <span data-ttu-id="417a4-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="417a4-151">0x00000011</span></span>                        |
| <span data-ttu-id="417a4-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="417a4-152">System-Flags</span></span>           | <span data-ttu-id="417a4-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="417a4-153">0x00000012</span></span>                        |
| <span data-ttu-id="417a4-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="417a4-154">Classes used in</span></span>        | [<span data-ttu-id="417a4-155">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="417a4-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="417a4-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="417a4-156">Windows Server 2003</span></span>



| <span data-ttu-id="417a4-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="417a4-157">Entry</span></span> | <span data-ttu-id="417a4-158">Valor</span><span class="sxs-lookup"><span data-stu-id="417a4-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="417a4-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="417a4-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="417a4-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="417a4-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="417a4-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="417a4-161">System-Only</span></span>            | <span data-ttu-id="417a4-162">Falso</span><span class="sxs-lookup"><span data-stu-id="417a4-162">False</span></span>                             |
| <span data-ttu-id="417a4-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="417a4-163">Is-Single-Valued</span></span>       | <span data-ttu-id="417a4-164">True</span><span class="sxs-lookup"><span data-stu-id="417a4-164">True</span></span>                              |
| <span data-ttu-id="417a4-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="417a4-165">Is Indexed</span></span>             | <span data-ttu-id="417a4-166">True</span><span class="sxs-lookup"><span data-stu-id="417a4-166">True</span></span>                              |
| <span data-ttu-id="417a4-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="417a4-167">In Global Catalog</span></span>      | <span data-ttu-id="417a4-168">True</span><span class="sxs-lookup"><span data-stu-id="417a4-168">True</span></span>                              |
| <span data-ttu-id="417a4-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="417a4-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="417a4-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="417a4-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="417a4-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="417a4-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="417a4-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="417a4-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="417a4-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="417a4-173">Search-Flags</span></span>           | <span data-ttu-id="417a4-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="417a4-174">0x00000011</span></span>                        |
| <span data-ttu-id="417a4-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="417a4-175">System-Flags</span></span>           | <span data-ttu-id="417a4-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="417a4-176">0x00000012</span></span>                        |
| <span data-ttu-id="417a4-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="417a4-177">Classes used in</span></span>        | [<span data-ttu-id="417a4-178">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="417a4-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="417a4-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="417a4-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="417a4-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="417a4-180">Entry</span></span> | <span data-ttu-id="417a4-181">Valor</span><span class="sxs-lookup"><span data-stu-id="417a4-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="417a4-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="417a4-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="417a4-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="417a4-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="417a4-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="417a4-184">System-Only</span></span>            | <span data-ttu-id="417a4-185">Falso</span><span class="sxs-lookup"><span data-stu-id="417a4-185">False</span></span>                             |
| <span data-ttu-id="417a4-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="417a4-186">Is-Single-Valued</span></span>       | <span data-ttu-id="417a4-187">True</span><span class="sxs-lookup"><span data-stu-id="417a4-187">True</span></span>                              |
| <span data-ttu-id="417a4-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="417a4-188">Is Indexed</span></span>             | <span data-ttu-id="417a4-189">True</span><span class="sxs-lookup"><span data-stu-id="417a4-189">True</span></span>                              |
| <span data-ttu-id="417a4-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="417a4-190">In Global Catalog</span></span>      | <span data-ttu-id="417a4-191">True</span><span class="sxs-lookup"><span data-stu-id="417a4-191">True</span></span>                              |
| <span data-ttu-id="417a4-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="417a4-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="417a4-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="417a4-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="417a4-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="417a4-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="417a4-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="417a4-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="417a4-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="417a4-196">Search-Flags</span></span>           | <span data-ttu-id="417a4-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="417a4-197">0x00000011</span></span>                        |
| <span data-ttu-id="417a4-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="417a4-198">System-Flags</span></span>           | <span data-ttu-id="417a4-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="417a4-199">0x00000012</span></span>                        |
| <span data-ttu-id="417a4-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="417a4-200">Classes used in</span></span>        | [<span data-ttu-id="417a4-201">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="417a4-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="417a4-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="417a4-202">Windows Server 2008</span></span>



| <span data-ttu-id="417a4-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="417a4-203">Entry</span></span> | <span data-ttu-id="417a4-204">Valor</span><span class="sxs-lookup"><span data-stu-id="417a4-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="417a4-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="417a4-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="417a4-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="417a4-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="417a4-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="417a4-207">System-Only</span></span>            | <span data-ttu-id="417a4-208">Falso</span><span class="sxs-lookup"><span data-stu-id="417a4-208">False</span></span>                             |
| <span data-ttu-id="417a4-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="417a4-209">Is-Single-Valued</span></span>       | <span data-ttu-id="417a4-210">True</span><span class="sxs-lookup"><span data-stu-id="417a4-210">True</span></span>                              |
| <span data-ttu-id="417a4-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="417a4-211">Is Indexed</span></span>             | <span data-ttu-id="417a4-212">True</span><span class="sxs-lookup"><span data-stu-id="417a4-212">True</span></span>                              |
| <span data-ttu-id="417a4-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="417a4-213">In Global Catalog</span></span>      | <span data-ttu-id="417a4-214">True</span><span class="sxs-lookup"><span data-stu-id="417a4-214">True</span></span>                              |
| <span data-ttu-id="417a4-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="417a4-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="417a4-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="417a4-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="417a4-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="417a4-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="417a4-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="417a4-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="417a4-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="417a4-219">Search-Flags</span></span>           | <span data-ttu-id="417a4-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="417a4-220">0x00000011</span></span>                        |
| <span data-ttu-id="417a4-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="417a4-221">System-Flags</span></span>           | <span data-ttu-id="417a4-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="417a4-222">0x00000012</span></span>                        |
| <span data-ttu-id="417a4-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="417a4-223">Classes used in</span></span>        | [<span data-ttu-id="417a4-224">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="417a4-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="417a4-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="417a4-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="417a4-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="417a4-226">Entry</span></span> | <span data-ttu-id="417a4-227">Valor</span><span class="sxs-lookup"><span data-stu-id="417a4-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="417a4-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="417a4-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="417a4-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="417a4-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="417a4-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="417a4-230">System-Only</span></span>            | <span data-ttu-id="417a4-231">Falso</span><span class="sxs-lookup"><span data-stu-id="417a4-231">False</span></span>                             |
| <span data-ttu-id="417a4-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="417a4-232">Is-Single-Valued</span></span>       | <span data-ttu-id="417a4-233">True</span><span class="sxs-lookup"><span data-stu-id="417a4-233">True</span></span>                              |
| <span data-ttu-id="417a4-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="417a4-234">Is Indexed</span></span>             | <span data-ttu-id="417a4-235">True</span><span class="sxs-lookup"><span data-stu-id="417a4-235">True</span></span>                              |
| <span data-ttu-id="417a4-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="417a4-236">In Global Catalog</span></span>      | <span data-ttu-id="417a4-237">True</span><span class="sxs-lookup"><span data-stu-id="417a4-237">True</span></span>                              |
| <span data-ttu-id="417a4-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="417a4-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="417a4-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="417a4-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="417a4-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="417a4-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="417a4-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="417a4-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="417a4-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="417a4-242">Search-Flags</span></span>           | <span data-ttu-id="417a4-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="417a4-243">0x00000011</span></span>                        |
| <span data-ttu-id="417a4-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="417a4-244">System-Flags</span></span>           | <span data-ttu-id="417a4-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="417a4-245">0x00000012</span></span>                        |
| <span data-ttu-id="417a4-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="417a4-246">Classes used in</span></span>        | [<span data-ttu-id="417a4-247">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="417a4-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="417a4-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="417a4-248">Windows Server 2012</span></span>



| <span data-ttu-id="417a4-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="417a4-249">Entry</span></span> | <span data-ttu-id="417a4-250">Valor</span><span class="sxs-lookup"><span data-stu-id="417a4-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="417a4-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="417a4-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="417a4-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="417a4-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="417a4-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="417a4-253">System-Only</span></span>            | <span data-ttu-id="417a4-254">Falso</span><span class="sxs-lookup"><span data-stu-id="417a4-254">False</span></span>                             |
| <span data-ttu-id="417a4-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="417a4-255">Is-Single-Valued</span></span>       | <span data-ttu-id="417a4-256">True</span><span class="sxs-lookup"><span data-stu-id="417a4-256">True</span></span>                              |
| <span data-ttu-id="417a4-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="417a4-257">Is Indexed</span></span>             | <span data-ttu-id="417a4-258">True</span><span class="sxs-lookup"><span data-stu-id="417a4-258">True</span></span>                              |
| <span data-ttu-id="417a4-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="417a4-259">In Global Catalog</span></span>      | <span data-ttu-id="417a4-260">True</span><span class="sxs-lookup"><span data-stu-id="417a4-260">True</span></span>                              |
| <span data-ttu-id="417a4-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="417a4-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="417a4-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="417a4-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="417a4-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="417a4-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="417a4-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="417a4-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="417a4-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="417a4-265">Search-Flags</span></span>           | <span data-ttu-id="417a4-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="417a4-266">0x00000011</span></span>                        |
| <span data-ttu-id="417a4-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="417a4-267">System-Flags</span></span>           | <span data-ttu-id="417a4-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="417a4-268">0x00000012</span></span>                        |
| <span data-ttu-id="417a4-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="417a4-269">Classes used in</span></span>        | [<span data-ttu-id="417a4-270">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="417a4-270">**User**</span></span>](c-user.md)<br/> |



 

 





