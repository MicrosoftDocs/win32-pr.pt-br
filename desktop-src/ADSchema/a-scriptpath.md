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
# <a name="script-path-attribute"></a><span data-ttu-id="d22ee-106">Script-Path atributo</span><span class="sxs-lookup"><span data-stu-id="d22ee-106">Script-Path attribute</span></span>

<span data-ttu-id="d22ee-107">Esse atributo especifica o caminho para o script de logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="d22ee-107">This attribute specifies the path for the user's logon script.</span></span> <span data-ttu-id="d22ee-108">A cadeia de caracteres pode ser nula.</span><span class="sxs-lookup"><span data-stu-id="d22ee-108">The string can be null.</span></span>



| <span data-ttu-id="d22ee-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="d22ee-109">Entry</span></span> | <span data-ttu-id="d22ee-110">Valor</span><span class="sxs-lookup"><span data-stu-id="d22ee-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="d22ee-111">CN</span><span class="sxs-lookup"><span data-stu-id="d22ee-111">CN</span></span>                | <span data-ttu-id="d22ee-112">Script-Path</span><span class="sxs-lookup"><span data-stu-id="d22ee-112">Script-Path</span></span>                                                            |
| <span data-ttu-id="d22ee-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d22ee-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d22ee-114">scriptPath</span><span class="sxs-lookup"><span data-stu-id="d22ee-114">scriptPath</span></span>                                                             |
| <span data-ttu-id="d22ee-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="d22ee-115">Size</span></span>              | \-                                                                     |
| <span data-ttu-id="d22ee-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="d22ee-116">Update Privilege</span></span>  | <span data-ttu-id="d22ee-117">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="d22ee-117">Domain administrator or account owner.</span></span>                                 |
| <span data-ttu-id="d22ee-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="d22ee-118">Update Frequency</span></span>  | <span data-ttu-id="d22ee-119">Quando o registro de usuário é criado e sempre que o caminho precisa ser alterado.</span><span class="sxs-lookup"><span data-stu-id="d22ee-119">When the user record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="d22ee-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d22ee-120">Attribute-Id</span></span>      | <span data-ttu-id="d22ee-121">1.2.840.113556.1.4.62</span><span class="sxs-lookup"><span data-stu-id="d22ee-121">1.2.840.113556.1.4.62</span></span>                                                  |
| <span data-ttu-id="d22ee-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d22ee-122">System-Id-Guid</span></span>    | <span data-ttu-id="d22ee-123">bf9679a8-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="d22ee-123">bf9679a8-0de6-11d0-a285-00aa003049e2</span></span>                                   |
| <span data-ttu-id="d22ee-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="d22ee-124">Syntax</span></span>            | [<span data-ttu-id="d22ee-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d22ee-125">**String(Unicode)**</span></span>](s-string-unicode.md)                            |



## <a name="implementations"></a><span data-ttu-id="d22ee-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="d22ee-126">Implementations</span></span>

-   [<span data-ttu-id="d22ee-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d22ee-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d22ee-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d22ee-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d22ee-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d22ee-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d22ee-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d22ee-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d22ee-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d22ee-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d22ee-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d22ee-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d22ee-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d22ee-133">Windows 2000 Server</span></span>



| <span data-ttu-id="d22ee-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="d22ee-134">Entry</span></span> | <span data-ttu-id="d22ee-135">Valor</span><span class="sxs-lookup"><span data-stu-id="d22ee-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d22ee-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="d22ee-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d22ee-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d22ee-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d22ee-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="d22ee-138">System-Only</span></span>            | <span data-ttu-id="d22ee-139">Falso</span><span class="sxs-lookup"><span data-stu-id="d22ee-139">False</span></span>                             |
| <span data-ttu-id="d22ee-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d22ee-140">Is-Single-Valued</span></span>       | <span data-ttu-id="d22ee-141">True</span><span class="sxs-lookup"><span data-stu-id="d22ee-141">True</span></span>                              |
| <span data-ttu-id="d22ee-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="d22ee-142">Is Indexed</span></span>             | <span data-ttu-id="d22ee-143">Falso</span><span class="sxs-lookup"><span data-stu-id="d22ee-143">False</span></span>                             |
| <span data-ttu-id="d22ee-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d22ee-144">In Global Catalog</span></span>      | <span data-ttu-id="d22ee-145">Falso</span><span class="sxs-lookup"><span data-stu-id="d22ee-145">False</span></span>                             |
| <span data-ttu-id="d22ee-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d22ee-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="d22ee-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d22ee-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d22ee-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d22ee-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d22ee-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d22ee-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d22ee-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d22ee-150">Search-Flags</span></span>           | <span data-ttu-id="d22ee-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d22ee-151">0x00000010</span></span>                        |
| <span data-ttu-id="d22ee-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d22ee-152">System-Flags</span></span>           | <span data-ttu-id="d22ee-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d22ee-153">0x00000010</span></span>                        |
| <span data-ttu-id="d22ee-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d22ee-154">Classes used in</span></span>        | [<span data-ttu-id="d22ee-155">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="d22ee-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d22ee-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d22ee-156">Windows Server 2003</span></span>



| <span data-ttu-id="d22ee-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="d22ee-157">Entry</span></span> | <span data-ttu-id="d22ee-158">Valor</span><span class="sxs-lookup"><span data-stu-id="d22ee-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d22ee-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="d22ee-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d22ee-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d22ee-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d22ee-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="d22ee-161">System-Only</span></span>            | <span data-ttu-id="d22ee-162">Falso</span><span class="sxs-lookup"><span data-stu-id="d22ee-162">False</span></span>                             |
| <span data-ttu-id="d22ee-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d22ee-163">Is-Single-Valued</span></span>       | <span data-ttu-id="d22ee-164">True</span><span class="sxs-lookup"><span data-stu-id="d22ee-164">True</span></span>                              |
| <span data-ttu-id="d22ee-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="d22ee-165">Is Indexed</span></span>             | <span data-ttu-id="d22ee-166">Falso</span><span class="sxs-lookup"><span data-stu-id="d22ee-166">False</span></span>                             |
| <span data-ttu-id="d22ee-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d22ee-167">In Global Catalog</span></span>      | <span data-ttu-id="d22ee-168">Falso</span><span class="sxs-lookup"><span data-stu-id="d22ee-168">False</span></span>                             |
| <span data-ttu-id="d22ee-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d22ee-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="d22ee-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d22ee-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d22ee-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d22ee-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d22ee-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d22ee-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d22ee-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d22ee-173">Search-Flags</span></span>           | <span data-ttu-id="d22ee-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d22ee-174">0x00000010</span></span>                        |
| <span data-ttu-id="d22ee-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d22ee-175">System-Flags</span></span>           | <span data-ttu-id="d22ee-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d22ee-176">0x00000010</span></span>                        |
| <span data-ttu-id="d22ee-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d22ee-177">Classes used in</span></span>        | [<span data-ttu-id="d22ee-178">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="d22ee-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d22ee-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d22ee-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d22ee-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="d22ee-180">Entry</span></span> | <span data-ttu-id="d22ee-181">Valor</span><span class="sxs-lookup"><span data-stu-id="d22ee-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d22ee-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="d22ee-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d22ee-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d22ee-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d22ee-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="d22ee-184">System-Only</span></span>            | <span data-ttu-id="d22ee-185">Falso</span><span class="sxs-lookup"><span data-stu-id="d22ee-185">False</span></span>                             |
| <span data-ttu-id="d22ee-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d22ee-186">Is-Single-Valued</span></span>       | <span data-ttu-id="d22ee-187">True</span><span class="sxs-lookup"><span data-stu-id="d22ee-187">True</span></span>                              |
| <span data-ttu-id="d22ee-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="d22ee-188">Is Indexed</span></span>             | <span data-ttu-id="d22ee-189">Falso</span><span class="sxs-lookup"><span data-stu-id="d22ee-189">False</span></span>                             |
| <span data-ttu-id="d22ee-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d22ee-190">In Global Catalog</span></span>      | <span data-ttu-id="d22ee-191">Falso</span><span class="sxs-lookup"><span data-stu-id="d22ee-191">False</span></span>                             |
| <span data-ttu-id="d22ee-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d22ee-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="d22ee-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d22ee-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d22ee-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d22ee-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d22ee-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d22ee-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d22ee-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d22ee-196">Search-Flags</span></span>           | <span data-ttu-id="d22ee-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d22ee-197">0x00000010</span></span>                        |
| <span data-ttu-id="d22ee-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d22ee-198">System-Flags</span></span>           | <span data-ttu-id="d22ee-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d22ee-199">0x00000010</span></span>                        |
| <span data-ttu-id="d22ee-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d22ee-200">Classes used in</span></span>        | [<span data-ttu-id="d22ee-201">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="d22ee-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d22ee-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d22ee-202">Windows Server 2008</span></span>



| <span data-ttu-id="d22ee-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="d22ee-203">Entry</span></span> | <span data-ttu-id="d22ee-204">Valor</span><span class="sxs-lookup"><span data-stu-id="d22ee-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d22ee-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="d22ee-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d22ee-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d22ee-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d22ee-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="d22ee-207">System-Only</span></span>            | <span data-ttu-id="d22ee-208">Falso</span><span class="sxs-lookup"><span data-stu-id="d22ee-208">False</span></span>                             |
| <span data-ttu-id="d22ee-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d22ee-209">Is-Single-Valued</span></span>       | <span data-ttu-id="d22ee-210">True</span><span class="sxs-lookup"><span data-stu-id="d22ee-210">True</span></span>                              |
| <span data-ttu-id="d22ee-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="d22ee-211">Is Indexed</span></span>             | <span data-ttu-id="d22ee-212">Falso</span><span class="sxs-lookup"><span data-stu-id="d22ee-212">False</span></span>                             |
| <span data-ttu-id="d22ee-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d22ee-213">In Global Catalog</span></span>      | <span data-ttu-id="d22ee-214">Falso</span><span class="sxs-lookup"><span data-stu-id="d22ee-214">False</span></span>                             |
| <span data-ttu-id="d22ee-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d22ee-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="d22ee-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d22ee-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d22ee-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d22ee-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d22ee-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d22ee-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d22ee-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d22ee-219">Search-Flags</span></span>           | <span data-ttu-id="d22ee-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d22ee-220">0x00000010</span></span>                        |
| <span data-ttu-id="d22ee-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d22ee-221">System-Flags</span></span>           | <span data-ttu-id="d22ee-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d22ee-222">0x00000010</span></span>                        |
| <span data-ttu-id="d22ee-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d22ee-223">Classes used in</span></span>        | [<span data-ttu-id="d22ee-224">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="d22ee-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d22ee-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d22ee-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d22ee-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="d22ee-226">Entry</span></span> | <span data-ttu-id="d22ee-227">Valor</span><span class="sxs-lookup"><span data-stu-id="d22ee-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d22ee-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="d22ee-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d22ee-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d22ee-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d22ee-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="d22ee-230">System-Only</span></span>            | <span data-ttu-id="d22ee-231">Falso</span><span class="sxs-lookup"><span data-stu-id="d22ee-231">False</span></span>                             |
| <span data-ttu-id="d22ee-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d22ee-232">Is-Single-Valued</span></span>       | <span data-ttu-id="d22ee-233">True</span><span class="sxs-lookup"><span data-stu-id="d22ee-233">True</span></span>                              |
| <span data-ttu-id="d22ee-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="d22ee-234">Is Indexed</span></span>             | <span data-ttu-id="d22ee-235">Falso</span><span class="sxs-lookup"><span data-stu-id="d22ee-235">False</span></span>                             |
| <span data-ttu-id="d22ee-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d22ee-236">In Global Catalog</span></span>      | <span data-ttu-id="d22ee-237">Falso</span><span class="sxs-lookup"><span data-stu-id="d22ee-237">False</span></span>                             |
| <span data-ttu-id="d22ee-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d22ee-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="d22ee-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d22ee-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d22ee-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d22ee-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d22ee-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d22ee-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d22ee-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d22ee-242">Search-Flags</span></span>           | <span data-ttu-id="d22ee-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d22ee-243">0x00000010</span></span>                        |
| <span data-ttu-id="d22ee-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d22ee-244">System-Flags</span></span>           | <span data-ttu-id="d22ee-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d22ee-245">0x00000010</span></span>                        |
| <span data-ttu-id="d22ee-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d22ee-246">Classes used in</span></span>        | [<span data-ttu-id="d22ee-247">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="d22ee-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d22ee-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d22ee-248">Windows Server 2012</span></span>



| <span data-ttu-id="d22ee-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="d22ee-249">Entry</span></span> | <span data-ttu-id="d22ee-250">Valor</span><span class="sxs-lookup"><span data-stu-id="d22ee-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d22ee-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="d22ee-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d22ee-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d22ee-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d22ee-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="d22ee-253">System-Only</span></span>            | <span data-ttu-id="d22ee-254">Falso</span><span class="sxs-lookup"><span data-stu-id="d22ee-254">False</span></span>                             |
| <span data-ttu-id="d22ee-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d22ee-255">Is-Single-Valued</span></span>       | <span data-ttu-id="d22ee-256">True</span><span class="sxs-lookup"><span data-stu-id="d22ee-256">True</span></span>                              |
| <span data-ttu-id="d22ee-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="d22ee-257">Is Indexed</span></span>             | <span data-ttu-id="d22ee-258">Falso</span><span class="sxs-lookup"><span data-stu-id="d22ee-258">False</span></span>                             |
| <span data-ttu-id="d22ee-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d22ee-259">In Global Catalog</span></span>      | <span data-ttu-id="d22ee-260">Falso</span><span class="sxs-lookup"><span data-stu-id="d22ee-260">False</span></span>                             |
| <span data-ttu-id="d22ee-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d22ee-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="d22ee-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d22ee-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d22ee-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d22ee-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d22ee-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d22ee-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d22ee-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d22ee-265">Search-Flags</span></span>           | <span data-ttu-id="d22ee-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d22ee-266">0x00000010</span></span>                        |
| <span data-ttu-id="d22ee-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d22ee-267">System-Flags</span></span>           | <span data-ttu-id="d22ee-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d22ee-268">0x00000010</span></span>                        |
| <span data-ttu-id="d22ee-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d22ee-269">Classes used in</span></span>        | [<span data-ttu-id="d22ee-270">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="d22ee-270">**User**</span></span>](c-user.md)<br/> |



 

 





