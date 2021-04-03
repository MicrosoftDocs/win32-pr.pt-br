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
# <a name="primary-group-id-attribute"></a><span data-ttu-id="8fc46-106">Atributo Primary-Group-ID</span><span class="sxs-lookup"><span data-stu-id="8fc46-106">Primary-Group-ID attribute</span></span>

<span data-ttu-id="8fc46-107">Contém o identificador relativo (RID) do grupo primário do usuário.</span><span class="sxs-lookup"><span data-stu-id="8fc46-107">Contains the relative identifier (RID) for the primary group of the user.</span></span> <span data-ttu-id="8fc46-108">Por padrão, esse é o RID do grupo usuários do domínio.</span><span class="sxs-lookup"><span data-stu-id="8fc46-108">By default, this is the RID for the Domain Users group.</span></span>



| <span data-ttu-id="8fc46-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fc46-109">Entry</span></span> | <span data-ttu-id="8fc46-110">Valor</span><span class="sxs-lookup"><span data-stu-id="8fc46-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8fc46-111">CN</span><span class="sxs-lookup"><span data-stu-id="8fc46-111">CN</span></span>                | <span data-ttu-id="8fc46-112">ID do grupo primário</span><span class="sxs-lookup"><span data-stu-id="8fc46-112">Primary-Group-ID</span></span>                     |
| <span data-ttu-id="8fc46-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8fc46-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8fc46-114">primaryGroupID</span><span class="sxs-lookup"><span data-stu-id="8fc46-114">primaryGroupID</span></span>                       |
| <span data-ttu-id="8fc46-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="8fc46-115">Size</span></span>              | <span data-ttu-id="8fc46-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="8fc46-116">4 bytes</span></span>                              |
| <span data-ttu-id="8fc46-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="8fc46-117">Update Privilege</span></span>  | <span data-ttu-id="8fc46-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="8fc46-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="8fc46-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="8fc46-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8fc46-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8fc46-120">Attribute-Id</span></span>      | <span data-ttu-id="8fc46-121">1.2.840.113556.1.4.98</span><span class="sxs-lookup"><span data-stu-id="8fc46-121">1.2.840.113556.1.4.98</span></span>                |
| <span data-ttu-id="8fc46-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8fc46-122">System-Id-Guid</span></span>    | <span data-ttu-id="8fc46-123">bf967a00-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8fc46-123">bf967a00-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="8fc46-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fc46-124">Syntax</span></span>            | [<span data-ttu-id="8fc46-125">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="8fc46-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="8fc46-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="8fc46-126">Implementations</span></span>

-   [<span data-ttu-id="8fc46-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8fc46-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8fc46-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8fc46-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8fc46-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8fc46-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8fc46-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8fc46-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8fc46-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8fc46-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8fc46-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8fc46-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8fc46-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8fc46-133">Windows 2000 Server</span></span>



| <span data-ttu-id="8fc46-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fc46-134">Entry</span></span> | <span data-ttu-id="8fc46-135">Valor</span><span class="sxs-lookup"><span data-stu-id="8fc46-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8fc46-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fc46-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8fc46-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fc46-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8fc46-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fc46-138">System-Only</span></span>            | <span data-ttu-id="8fc46-139">Falso</span><span class="sxs-lookup"><span data-stu-id="8fc46-139">False</span></span>                             |
| <span data-ttu-id="8fc46-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fc46-140">Is-Single-Valued</span></span>       | <span data-ttu-id="8fc46-141">True</span><span class="sxs-lookup"><span data-stu-id="8fc46-141">True</span></span>                              |
| <span data-ttu-id="8fc46-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fc46-142">Is Indexed</span></span>             | <span data-ttu-id="8fc46-143">True</span><span class="sxs-lookup"><span data-stu-id="8fc46-143">True</span></span>                              |
| <span data-ttu-id="8fc46-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fc46-144">In Global Catalog</span></span>      | <span data-ttu-id="8fc46-145">True</span><span class="sxs-lookup"><span data-stu-id="8fc46-145">True</span></span>                              |
| <span data-ttu-id="8fc46-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fc46-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fc46-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fc46-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8fc46-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fc46-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8fc46-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fc46-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8fc46-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fc46-150">Search-Flags</span></span>           | <span data-ttu-id="8fc46-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="8fc46-151">0x00000011</span></span>                        |
| <span data-ttu-id="8fc46-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fc46-152">System-Flags</span></span>           | <span data-ttu-id="8fc46-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8fc46-153">0x00000012</span></span>                        |
| <span data-ttu-id="8fc46-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fc46-154">Classes used in</span></span>        | [<span data-ttu-id="8fc46-155">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="8fc46-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8fc46-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8fc46-156">Windows Server 2003</span></span>



| <span data-ttu-id="8fc46-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fc46-157">Entry</span></span> | <span data-ttu-id="8fc46-158">Valor</span><span class="sxs-lookup"><span data-stu-id="8fc46-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8fc46-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fc46-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8fc46-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fc46-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8fc46-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fc46-161">System-Only</span></span>            | <span data-ttu-id="8fc46-162">Falso</span><span class="sxs-lookup"><span data-stu-id="8fc46-162">False</span></span>                             |
| <span data-ttu-id="8fc46-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fc46-163">Is-Single-Valued</span></span>       | <span data-ttu-id="8fc46-164">True</span><span class="sxs-lookup"><span data-stu-id="8fc46-164">True</span></span>                              |
| <span data-ttu-id="8fc46-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fc46-165">Is Indexed</span></span>             | <span data-ttu-id="8fc46-166">True</span><span class="sxs-lookup"><span data-stu-id="8fc46-166">True</span></span>                              |
| <span data-ttu-id="8fc46-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fc46-167">In Global Catalog</span></span>      | <span data-ttu-id="8fc46-168">True</span><span class="sxs-lookup"><span data-stu-id="8fc46-168">True</span></span>                              |
| <span data-ttu-id="8fc46-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fc46-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fc46-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fc46-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8fc46-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fc46-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8fc46-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fc46-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8fc46-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fc46-173">Search-Flags</span></span>           | <span data-ttu-id="8fc46-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="8fc46-174">0x00000011</span></span>                        |
| <span data-ttu-id="8fc46-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fc46-175">System-Flags</span></span>           | <span data-ttu-id="8fc46-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8fc46-176">0x00000012</span></span>                        |
| <span data-ttu-id="8fc46-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fc46-177">Classes used in</span></span>        | [<span data-ttu-id="8fc46-178">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="8fc46-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8fc46-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8fc46-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8fc46-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fc46-180">Entry</span></span> | <span data-ttu-id="8fc46-181">Valor</span><span class="sxs-lookup"><span data-stu-id="8fc46-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8fc46-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fc46-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8fc46-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fc46-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8fc46-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fc46-184">System-Only</span></span>            | <span data-ttu-id="8fc46-185">Falso</span><span class="sxs-lookup"><span data-stu-id="8fc46-185">False</span></span>                             |
| <span data-ttu-id="8fc46-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fc46-186">Is-Single-Valued</span></span>       | <span data-ttu-id="8fc46-187">True</span><span class="sxs-lookup"><span data-stu-id="8fc46-187">True</span></span>                              |
| <span data-ttu-id="8fc46-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fc46-188">Is Indexed</span></span>             | <span data-ttu-id="8fc46-189">True</span><span class="sxs-lookup"><span data-stu-id="8fc46-189">True</span></span>                              |
| <span data-ttu-id="8fc46-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fc46-190">In Global Catalog</span></span>      | <span data-ttu-id="8fc46-191">True</span><span class="sxs-lookup"><span data-stu-id="8fc46-191">True</span></span>                              |
| <span data-ttu-id="8fc46-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fc46-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fc46-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fc46-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8fc46-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fc46-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8fc46-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fc46-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8fc46-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fc46-196">Search-Flags</span></span>           | <span data-ttu-id="8fc46-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="8fc46-197">0x00000011</span></span>                        |
| <span data-ttu-id="8fc46-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fc46-198">System-Flags</span></span>           | <span data-ttu-id="8fc46-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8fc46-199">0x00000012</span></span>                        |
| <span data-ttu-id="8fc46-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fc46-200">Classes used in</span></span>        | [<span data-ttu-id="8fc46-201">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="8fc46-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8fc46-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fc46-202">Windows Server 2008</span></span>



| <span data-ttu-id="8fc46-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fc46-203">Entry</span></span> | <span data-ttu-id="8fc46-204">Valor</span><span class="sxs-lookup"><span data-stu-id="8fc46-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8fc46-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fc46-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8fc46-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fc46-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8fc46-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fc46-207">System-Only</span></span>            | <span data-ttu-id="8fc46-208">Falso</span><span class="sxs-lookup"><span data-stu-id="8fc46-208">False</span></span>                             |
| <span data-ttu-id="8fc46-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fc46-209">Is-Single-Valued</span></span>       | <span data-ttu-id="8fc46-210">True</span><span class="sxs-lookup"><span data-stu-id="8fc46-210">True</span></span>                              |
| <span data-ttu-id="8fc46-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fc46-211">Is Indexed</span></span>             | <span data-ttu-id="8fc46-212">True</span><span class="sxs-lookup"><span data-stu-id="8fc46-212">True</span></span>                              |
| <span data-ttu-id="8fc46-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fc46-213">In Global Catalog</span></span>      | <span data-ttu-id="8fc46-214">True</span><span class="sxs-lookup"><span data-stu-id="8fc46-214">True</span></span>                              |
| <span data-ttu-id="8fc46-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fc46-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fc46-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fc46-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8fc46-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fc46-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8fc46-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fc46-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8fc46-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fc46-219">Search-Flags</span></span>           | <span data-ttu-id="8fc46-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="8fc46-220">0x00000011</span></span>                        |
| <span data-ttu-id="8fc46-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fc46-221">System-Flags</span></span>           | <span data-ttu-id="8fc46-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8fc46-222">0x00000012</span></span>                        |
| <span data-ttu-id="8fc46-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fc46-223">Classes used in</span></span>        | [<span data-ttu-id="8fc46-224">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="8fc46-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8fc46-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8fc46-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8fc46-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fc46-226">Entry</span></span> | <span data-ttu-id="8fc46-227">Valor</span><span class="sxs-lookup"><span data-stu-id="8fc46-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8fc46-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fc46-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8fc46-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fc46-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8fc46-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fc46-230">System-Only</span></span>            | <span data-ttu-id="8fc46-231">Falso</span><span class="sxs-lookup"><span data-stu-id="8fc46-231">False</span></span>                             |
| <span data-ttu-id="8fc46-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fc46-232">Is-Single-Valued</span></span>       | <span data-ttu-id="8fc46-233">True</span><span class="sxs-lookup"><span data-stu-id="8fc46-233">True</span></span>                              |
| <span data-ttu-id="8fc46-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fc46-234">Is Indexed</span></span>             | <span data-ttu-id="8fc46-235">True</span><span class="sxs-lookup"><span data-stu-id="8fc46-235">True</span></span>                              |
| <span data-ttu-id="8fc46-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fc46-236">In Global Catalog</span></span>      | <span data-ttu-id="8fc46-237">True</span><span class="sxs-lookup"><span data-stu-id="8fc46-237">True</span></span>                              |
| <span data-ttu-id="8fc46-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fc46-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fc46-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fc46-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8fc46-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fc46-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8fc46-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fc46-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8fc46-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fc46-242">Search-Flags</span></span>           | <span data-ttu-id="8fc46-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="8fc46-243">0x00000011</span></span>                        |
| <span data-ttu-id="8fc46-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fc46-244">System-Flags</span></span>           | <span data-ttu-id="8fc46-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8fc46-245">0x00000012</span></span>                        |
| <span data-ttu-id="8fc46-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fc46-246">Classes used in</span></span>        | [<span data-ttu-id="8fc46-247">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="8fc46-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8fc46-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8fc46-248">Windows Server 2012</span></span>



| <span data-ttu-id="8fc46-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fc46-249">Entry</span></span> | <span data-ttu-id="8fc46-250">Valor</span><span class="sxs-lookup"><span data-stu-id="8fc46-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8fc46-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fc46-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8fc46-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fc46-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8fc46-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fc46-253">System-Only</span></span>            | <span data-ttu-id="8fc46-254">Falso</span><span class="sxs-lookup"><span data-stu-id="8fc46-254">False</span></span>                             |
| <span data-ttu-id="8fc46-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fc46-255">Is-Single-Valued</span></span>       | <span data-ttu-id="8fc46-256">True</span><span class="sxs-lookup"><span data-stu-id="8fc46-256">True</span></span>                              |
| <span data-ttu-id="8fc46-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fc46-257">Is Indexed</span></span>             | <span data-ttu-id="8fc46-258">True</span><span class="sxs-lookup"><span data-stu-id="8fc46-258">True</span></span>                              |
| <span data-ttu-id="8fc46-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fc46-259">In Global Catalog</span></span>      | <span data-ttu-id="8fc46-260">True</span><span class="sxs-lookup"><span data-stu-id="8fc46-260">True</span></span>                              |
| <span data-ttu-id="8fc46-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fc46-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fc46-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fc46-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8fc46-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fc46-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8fc46-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fc46-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8fc46-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fc46-265">Search-Flags</span></span>           | <span data-ttu-id="8fc46-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="8fc46-266">0x00000011</span></span>                        |
| <span data-ttu-id="8fc46-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fc46-267">System-Flags</span></span>           | <span data-ttu-id="8fc46-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8fc46-268">0x00000012</span></span>                        |
| <span data-ttu-id="8fc46-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fc46-269">Classes used in</span></span>        | [<span data-ttu-id="8fc46-270">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="8fc46-270">**User**</span></span>](c-user.md)<br/> |



 

 





