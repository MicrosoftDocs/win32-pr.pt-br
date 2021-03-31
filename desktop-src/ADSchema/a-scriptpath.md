---
title: Script-Path atributo
description: Esse atributo especifica o caminho para o script de logon do usuário. A cadeia de caracteres pode ser nula.
ms.assetid: 356f2ba0-ceca-4805-a536-286c6a8b54fc
ms.tgt_platform: multiple
keywords:
- Esquema de Script-Path do atributo AD
- atributo scriptPath do esquema do AD
topic_type:
- apiref
api_name:
- Script-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0909c35c41ae65f75481910d1377aa2761e99487
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086993"
---
# <a name="script-path-attribute"></a><span data-ttu-id="16633-106">Script-Path atributo</span><span class="sxs-lookup"><span data-stu-id="16633-106">Script-Path attribute</span></span>

<span data-ttu-id="16633-107">Esse atributo especifica o caminho para o script de logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="16633-107">This attribute specifies the path for the user's logon script.</span></span> <span data-ttu-id="16633-108">A cadeia de caracteres pode ser nula.</span><span class="sxs-lookup"><span data-stu-id="16633-108">The string can be null.</span></span>



| <span data-ttu-id="16633-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="16633-109">Entry</span></span> | <span data-ttu-id="16633-110">Valor</span><span class="sxs-lookup"><span data-stu-id="16633-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="16633-111">CN</span><span class="sxs-lookup"><span data-stu-id="16633-111">CN</span></span>                | <span data-ttu-id="16633-112">Script-Path</span><span class="sxs-lookup"><span data-stu-id="16633-112">Script-Path</span></span>                                                            |
| <span data-ttu-id="16633-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="16633-113">Ldap-Display-Name</span></span> | <span data-ttu-id="16633-114">scriptPath</span><span class="sxs-lookup"><span data-stu-id="16633-114">scriptPath</span></span>                                                             |
| <span data-ttu-id="16633-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="16633-115">Size</span></span>              | \-                                                                     |
| <span data-ttu-id="16633-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="16633-116">Update Privilege</span></span>  | <span data-ttu-id="16633-117">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="16633-117">Domain administrator or account owner.</span></span>                                 |
| <span data-ttu-id="16633-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="16633-118">Update Frequency</span></span>  | <span data-ttu-id="16633-119">Quando o registro de usuário é criado e sempre que o caminho precisa ser alterado.</span><span class="sxs-lookup"><span data-stu-id="16633-119">When the user record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="16633-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="16633-120">Attribute-Id</span></span>      | <span data-ttu-id="16633-121">1.2.840.113556.1.4.62</span><span class="sxs-lookup"><span data-stu-id="16633-121">1.2.840.113556.1.4.62</span></span>                                                  |
| <span data-ttu-id="16633-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="16633-122">System-Id-Guid</span></span>    | <span data-ttu-id="16633-123">bf9679a8-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="16633-123">bf9679a8-0de6-11d0-a285-00aa003049e2</span></span>                                   |
| <span data-ttu-id="16633-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="16633-124">Syntax</span></span>            | [<span data-ttu-id="16633-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="16633-125">**String(Unicode)**</span></span>](s-string-unicode.md)                            |



## <a name="implementations"></a><span data-ttu-id="16633-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="16633-126">Implementations</span></span>

-   [<span data-ttu-id="16633-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="16633-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="16633-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="16633-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="16633-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="16633-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="16633-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="16633-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="16633-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="16633-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="16633-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="16633-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="16633-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="16633-133">Windows 2000 Server</span></span>



| <span data-ttu-id="16633-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="16633-134">Entry</span></span> | <span data-ttu-id="16633-135">Valor</span><span class="sxs-lookup"><span data-stu-id="16633-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="16633-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="16633-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="16633-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16633-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="16633-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="16633-138">System-Only</span></span>            | <span data-ttu-id="16633-139">Falso</span><span class="sxs-lookup"><span data-stu-id="16633-139">False</span></span>                             |
| <span data-ttu-id="16633-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="16633-140">Is-Single-Valued</span></span>       | <span data-ttu-id="16633-141">True</span><span class="sxs-lookup"><span data-stu-id="16633-141">True</span></span>                              |
| <span data-ttu-id="16633-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="16633-142">Is Indexed</span></span>             | <span data-ttu-id="16633-143">Falso</span><span class="sxs-lookup"><span data-stu-id="16633-143">False</span></span>                             |
| <span data-ttu-id="16633-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="16633-144">In Global Catalog</span></span>      | <span data-ttu-id="16633-145">Falso</span><span class="sxs-lookup"><span data-stu-id="16633-145">False</span></span>                             |
| <span data-ttu-id="16633-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="16633-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="16633-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="16633-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="16633-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16633-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="16633-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16633-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="16633-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16633-150">Search-Flags</span></span>           | <span data-ttu-id="16633-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16633-151">0x00000010</span></span>                        |
| <span data-ttu-id="16633-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16633-152">System-Flags</span></span>           | <span data-ttu-id="16633-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16633-153">0x00000010</span></span>                        |
| <span data-ttu-id="16633-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="16633-154">Classes used in</span></span>        | [<span data-ttu-id="16633-155">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="16633-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="16633-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="16633-156">Windows Server 2003</span></span>



| <span data-ttu-id="16633-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="16633-157">Entry</span></span> | <span data-ttu-id="16633-158">Valor</span><span class="sxs-lookup"><span data-stu-id="16633-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="16633-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="16633-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="16633-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16633-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="16633-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="16633-161">System-Only</span></span>            | <span data-ttu-id="16633-162">Falso</span><span class="sxs-lookup"><span data-stu-id="16633-162">False</span></span>                             |
| <span data-ttu-id="16633-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="16633-163">Is-Single-Valued</span></span>       | <span data-ttu-id="16633-164">True</span><span class="sxs-lookup"><span data-stu-id="16633-164">True</span></span>                              |
| <span data-ttu-id="16633-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="16633-165">Is Indexed</span></span>             | <span data-ttu-id="16633-166">Falso</span><span class="sxs-lookup"><span data-stu-id="16633-166">False</span></span>                             |
| <span data-ttu-id="16633-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="16633-167">In Global Catalog</span></span>      | <span data-ttu-id="16633-168">Falso</span><span class="sxs-lookup"><span data-stu-id="16633-168">False</span></span>                             |
| <span data-ttu-id="16633-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="16633-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="16633-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="16633-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="16633-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16633-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="16633-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16633-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="16633-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16633-173">Search-Flags</span></span>           | <span data-ttu-id="16633-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16633-174">0x00000010</span></span>                        |
| <span data-ttu-id="16633-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16633-175">System-Flags</span></span>           | <span data-ttu-id="16633-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16633-176">0x00000010</span></span>                        |
| <span data-ttu-id="16633-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="16633-177">Classes used in</span></span>        | [<span data-ttu-id="16633-178">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="16633-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="16633-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="16633-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="16633-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="16633-180">Entry</span></span> | <span data-ttu-id="16633-181">Valor</span><span class="sxs-lookup"><span data-stu-id="16633-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="16633-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="16633-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="16633-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16633-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="16633-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="16633-184">System-Only</span></span>            | <span data-ttu-id="16633-185">Falso</span><span class="sxs-lookup"><span data-stu-id="16633-185">False</span></span>                             |
| <span data-ttu-id="16633-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="16633-186">Is-Single-Valued</span></span>       | <span data-ttu-id="16633-187">True</span><span class="sxs-lookup"><span data-stu-id="16633-187">True</span></span>                              |
| <span data-ttu-id="16633-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="16633-188">Is Indexed</span></span>             | <span data-ttu-id="16633-189">Falso</span><span class="sxs-lookup"><span data-stu-id="16633-189">False</span></span>                             |
| <span data-ttu-id="16633-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="16633-190">In Global Catalog</span></span>      | <span data-ttu-id="16633-191">Falso</span><span class="sxs-lookup"><span data-stu-id="16633-191">False</span></span>                             |
| <span data-ttu-id="16633-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="16633-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="16633-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="16633-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="16633-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16633-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="16633-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16633-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="16633-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16633-196">Search-Flags</span></span>           | <span data-ttu-id="16633-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16633-197">0x00000010</span></span>                        |
| <span data-ttu-id="16633-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16633-198">System-Flags</span></span>           | <span data-ttu-id="16633-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16633-199">0x00000010</span></span>                        |
| <span data-ttu-id="16633-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="16633-200">Classes used in</span></span>        | [<span data-ttu-id="16633-201">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="16633-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="16633-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16633-202">Windows Server 2008</span></span>



| <span data-ttu-id="16633-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="16633-203">Entry</span></span> | <span data-ttu-id="16633-204">Valor</span><span class="sxs-lookup"><span data-stu-id="16633-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="16633-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="16633-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="16633-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16633-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="16633-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="16633-207">System-Only</span></span>            | <span data-ttu-id="16633-208">Falso</span><span class="sxs-lookup"><span data-stu-id="16633-208">False</span></span>                             |
| <span data-ttu-id="16633-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="16633-209">Is-Single-Valued</span></span>       | <span data-ttu-id="16633-210">True</span><span class="sxs-lookup"><span data-stu-id="16633-210">True</span></span>                              |
| <span data-ttu-id="16633-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="16633-211">Is Indexed</span></span>             | <span data-ttu-id="16633-212">Falso</span><span class="sxs-lookup"><span data-stu-id="16633-212">False</span></span>                             |
| <span data-ttu-id="16633-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="16633-213">In Global Catalog</span></span>      | <span data-ttu-id="16633-214">Falso</span><span class="sxs-lookup"><span data-stu-id="16633-214">False</span></span>                             |
| <span data-ttu-id="16633-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="16633-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="16633-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="16633-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="16633-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16633-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="16633-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16633-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="16633-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16633-219">Search-Flags</span></span>           | <span data-ttu-id="16633-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16633-220">0x00000010</span></span>                        |
| <span data-ttu-id="16633-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16633-221">System-Flags</span></span>           | <span data-ttu-id="16633-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16633-222">0x00000010</span></span>                        |
| <span data-ttu-id="16633-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="16633-223">Classes used in</span></span>        | [<span data-ttu-id="16633-224">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="16633-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="16633-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="16633-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="16633-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="16633-226">Entry</span></span> | <span data-ttu-id="16633-227">Valor</span><span class="sxs-lookup"><span data-stu-id="16633-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="16633-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="16633-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="16633-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16633-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="16633-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="16633-230">System-Only</span></span>            | <span data-ttu-id="16633-231">Falso</span><span class="sxs-lookup"><span data-stu-id="16633-231">False</span></span>                             |
| <span data-ttu-id="16633-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="16633-232">Is-Single-Valued</span></span>       | <span data-ttu-id="16633-233">True</span><span class="sxs-lookup"><span data-stu-id="16633-233">True</span></span>                              |
| <span data-ttu-id="16633-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="16633-234">Is Indexed</span></span>             | <span data-ttu-id="16633-235">Falso</span><span class="sxs-lookup"><span data-stu-id="16633-235">False</span></span>                             |
| <span data-ttu-id="16633-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="16633-236">In Global Catalog</span></span>      | <span data-ttu-id="16633-237">Falso</span><span class="sxs-lookup"><span data-stu-id="16633-237">False</span></span>                             |
| <span data-ttu-id="16633-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="16633-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="16633-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="16633-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="16633-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16633-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="16633-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16633-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="16633-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16633-242">Search-Flags</span></span>           | <span data-ttu-id="16633-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16633-243">0x00000010</span></span>                        |
| <span data-ttu-id="16633-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16633-244">System-Flags</span></span>           | <span data-ttu-id="16633-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16633-245">0x00000010</span></span>                        |
| <span data-ttu-id="16633-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="16633-246">Classes used in</span></span>        | [<span data-ttu-id="16633-247">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="16633-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="16633-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16633-248">Windows Server 2012</span></span>



| <span data-ttu-id="16633-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="16633-249">Entry</span></span> | <span data-ttu-id="16633-250">Valor</span><span class="sxs-lookup"><span data-stu-id="16633-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="16633-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="16633-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="16633-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16633-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="16633-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="16633-253">System-Only</span></span>            | <span data-ttu-id="16633-254">Falso</span><span class="sxs-lookup"><span data-stu-id="16633-254">False</span></span>                             |
| <span data-ttu-id="16633-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="16633-255">Is-Single-Valued</span></span>       | <span data-ttu-id="16633-256">True</span><span class="sxs-lookup"><span data-stu-id="16633-256">True</span></span>                              |
| <span data-ttu-id="16633-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="16633-257">Is Indexed</span></span>             | <span data-ttu-id="16633-258">Falso</span><span class="sxs-lookup"><span data-stu-id="16633-258">False</span></span>                             |
| <span data-ttu-id="16633-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="16633-259">In Global Catalog</span></span>      | <span data-ttu-id="16633-260">Falso</span><span class="sxs-lookup"><span data-stu-id="16633-260">False</span></span>                             |
| <span data-ttu-id="16633-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="16633-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="16633-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="16633-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="16633-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16633-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="16633-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16633-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="16633-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16633-265">Search-Flags</span></span>           | <span data-ttu-id="16633-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16633-266">0x00000010</span></span>                        |
| <span data-ttu-id="16633-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16633-267">System-Flags</span></span>           | <span data-ttu-id="16633-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16633-268">0x00000010</span></span>                        |
| <span data-ttu-id="16633-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="16633-269">Classes used in</span></span>        | [<span data-ttu-id="16633-270">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="16633-270">**User**</span></span>](c-user.md)<br/> |



 

 





