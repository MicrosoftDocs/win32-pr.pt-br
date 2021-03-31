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
# <a name="script-path-attribute"></a><span data-ttu-id="b40ff-106">Script-Path atributo</span><span class="sxs-lookup"><span data-stu-id="b40ff-106">Script-Path attribute</span></span>

<span data-ttu-id="b40ff-107">Esse atributo especifica o caminho para o script de logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="b40ff-107">This attribute specifies the path for the user's logon script.</span></span> <span data-ttu-id="b40ff-108">A cadeia de caracteres pode ser nula.</span><span class="sxs-lookup"><span data-stu-id="b40ff-108">The string can be null.</span></span>



| <span data-ttu-id="b40ff-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="b40ff-109">Entry</span></span> | <span data-ttu-id="b40ff-110">Valor</span><span class="sxs-lookup"><span data-stu-id="b40ff-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="b40ff-111">CN</span><span class="sxs-lookup"><span data-stu-id="b40ff-111">CN</span></span>                | <span data-ttu-id="b40ff-112">Script-Path</span><span class="sxs-lookup"><span data-stu-id="b40ff-112">Script-Path</span></span>                                                            |
| <span data-ttu-id="b40ff-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b40ff-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b40ff-114">scriptPath</span><span class="sxs-lookup"><span data-stu-id="b40ff-114">scriptPath</span></span>                                                             |
| <span data-ttu-id="b40ff-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b40ff-115">Size</span></span>              | \-                                                                     |
| <span data-ttu-id="b40ff-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="b40ff-116">Update Privilege</span></span>  | <span data-ttu-id="b40ff-117">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="b40ff-117">Domain administrator or account owner.</span></span>                                 |
| <span data-ttu-id="b40ff-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="b40ff-118">Update Frequency</span></span>  | <span data-ttu-id="b40ff-119">Quando o registro de usuário é criado e sempre que o caminho precisa ser alterado.</span><span class="sxs-lookup"><span data-stu-id="b40ff-119">When the user record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="b40ff-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b40ff-120">Attribute-Id</span></span>      | <span data-ttu-id="b40ff-121">1.2.840.113556.1.4.62</span><span class="sxs-lookup"><span data-stu-id="b40ff-121">1.2.840.113556.1.4.62</span></span>                                                  |
| <span data-ttu-id="b40ff-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b40ff-122">System-Id-Guid</span></span>    | <span data-ttu-id="b40ff-123">bf9679a8-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b40ff-123">bf9679a8-0de6-11d0-a285-00aa003049e2</span></span>                                   |
| <span data-ttu-id="b40ff-124">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b40ff-124">Syntax</span></span>            | [<span data-ttu-id="b40ff-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b40ff-125">**String(Unicode)**</span></span>](s-string-unicode.md)                            |



## <a name="implementations"></a><span data-ttu-id="b40ff-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="b40ff-126">Implementations</span></span>

-   [<span data-ttu-id="b40ff-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b40ff-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b40ff-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b40ff-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b40ff-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b40ff-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b40ff-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b40ff-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b40ff-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b40ff-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b40ff-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b40ff-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b40ff-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b40ff-133">Windows 2000 Server</span></span>



| <span data-ttu-id="b40ff-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="b40ff-134">Entry</span></span> | <span data-ttu-id="b40ff-135">Valor</span><span class="sxs-lookup"><span data-stu-id="b40ff-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b40ff-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="b40ff-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b40ff-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b40ff-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b40ff-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="b40ff-138">System-Only</span></span>            | <span data-ttu-id="b40ff-139">Falso</span><span class="sxs-lookup"><span data-stu-id="b40ff-139">False</span></span>                             |
| <span data-ttu-id="b40ff-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b40ff-140">Is-Single-Valued</span></span>       | <span data-ttu-id="b40ff-141">True</span><span class="sxs-lookup"><span data-stu-id="b40ff-141">True</span></span>                              |
| <span data-ttu-id="b40ff-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="b40ff-142">Is Indexed</span></span>             | <span data-ttu-id="b40ff-143">Falso</span><span class="sxs-lookup"><span data-stu-id="b40ff-143">False</span></span>                             |
| <span data-ttu-id="b40ff-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b40ff-144">In Global Catalog</span></span>      | <span data-ttu-id="b40ff-145">Falso</span><span class="sxs-lookup"><span data-stu-id="b40ff-145">False</span></span>                             |
| <span data-ttu-id="b40ff-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b40ff-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="b40ff-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b40ff-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b40ff-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b40ff-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b40ff-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b40ff-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b40ff-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b40ff-150">Search-Flags</span></span>           | <span data-ttu-id="b40ff-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b40ff-151">0x00000010</span></span>                        |
| <span data-ttu-id="b40ff-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b40ff-152">System-Flags</span></span>           | <span data-ttu-id="b40ff-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b40ff-153">0x00000010</span></span>                        |
| <span data-ttu-id="b40ff-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b40ff-154">Classes used in</span></span>        | [<span data-ttu-id="b40ff-155">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="b40ff-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b40ff-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b40ff-156">Windows Server 2003</span></span>



| <span data-ttu-id="b40ff-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="b40ff-157">Entry</span></span> | <span data-ttu-id="b40ff-158">Valor</span><span class="sxs-lookup"><span data-stu-id="b40ff-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b40ff-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="b40ff-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b40ff-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b40ff-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b40ff-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="b40ff-161">System-Only</span></span>            | <span data-ttu-id="b40ff-162">Falso</span><span class="sxs-lookup"><span data-stu-id="b40ff-162">False</span></span>                             |
| <span data-ttu-id="b40ff-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b40ff-163">Is-Single-Valued</span></span>       | <span data-ttu-id="b40ff-164">True</span><span class="sxs-lookup"><span data-stu-id="b40ff-164">True</span></span>                              |
| <span data-ttu-id="b40ff-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="b40ff-165">Is Indexed</span></span>             | <span data-ttu-id="b40ff-166">Falso</span><span class="sxs-lookup"><span data-stu-id="b40ff-166">False</span></span>                             |
| <span data-ttu-id="b40ff-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b40ff-167">In Global Catalog</span></span>      | <span data-ttu-id="b40ff-168">Falso</span><span class="sxs-lookup"><span data-stu-id="b40ff-168">False</span></span>                             |
| <span data-ttu-id="b40ff-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b40ff-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="b40ff-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b40ff-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b40ff-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b40ff-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b40ff-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b40ff-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b40ff-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b40ff-173">Search-Flags</span></span>           | <span data-ttu-id="b40ff-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b40ff-174">0x00000010</span></span>                        |
| <span data-ttu-id="b40ff-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b40ff-175">System-Flags</span></span>           | <span data-ttu-id="b40ff-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b40ff-176">0x00000010</span></span>                        |
| <span data-ttu-id="b40ff-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b40ff-177">Classes used in</span></span>        | [<span data-ttu-id="b40ff-178">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="b40ff-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b40ff-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b40ff-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b40ff-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="b40ff-180">Entry</span></span> | <span data-ttu-id="b40ff-181">Valor</span><span class="sxs-lookup"><span data-stu-id="b40ff-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b40ff-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="b40ff-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b40ff-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b40ff-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b40ff-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="b40ff-184">System-Only</span></span>            | <span data-ttu-id="b40ff-185">Falso</span><span class="sxs-lookup"><span data-stu-id="b40ff-185">False</span></span>                             |
| <span data-ttu-id="b40ff-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b40ff-186">Is-Single-Valued</span></span>       | <span data-ttu-id="b40ff-187">True</span><span class="sxs-lookup"><span data-stu-id="b40ff-187">True</span></span>                              |
| <span data-ttu-id="b40ff-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="b40ff-188">Is Indexed</span></span>             | <span data-ttu-id="b40ff-189">Falso</span><span class="sxs-lookup"><span data-stu-id="b40ff-189">False</span></span>                             |
| <span data-ttu-id="b40ff-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b40ff-190">In Global Catalog</span></span>      | <span data-ttu-id="b40ff-191">Falso</span><span class="sxs-lookup"><span data-stu-id="b40ff-191">False</span></span>                             |
| <span data-ttu-id="b40ff-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b40ff-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="b40ff-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b40ff-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b40ff-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b40ff-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b40ff-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b40ff-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b40ff-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b40ff-196">Search-Flags</span></span>           | <span data-ttu-id="b40ff-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b40ff-197">0x00000010</span></span>                        |
| <span data-ttu-id="b40ff-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b40ff-198">System-Flags</span></span>           | <span data-ttu-id="b40ff-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b40ff-199">0x00000010</span></span>                        |
| <span data-ttu-id="b40ff-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b40ff-200">Classes used in</span></span>        | [<span data-ttu-id="b40ff-201">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="b40ff-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b40ff-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b40ff-202">Windows Server 2008</span></span>



| <span data-ttu-id="b40ff-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="b40ff-203">Entry</span></span> | <span data-ttu-id="b40ff-204">Valor</span><span class="sxs-lookup"><span data-stu-id="b40ff-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b40ff-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="b40ff-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b40ff-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b40ff-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b40ff-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="b40ff-207">System-Only</span></span>            | <span data-ttu-id="b40ff-208">Falso</span><span class="sxs-lookup"><span data-stu-id="b40ff-208">False</span></span>                             |
| <span data-ttu-id="b40ff-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b40ff-209">Is-Single-Valued</span></span>       | <span data-ttu-id="b40ff-210">True</span><span class="sxs-lookup"><span data-stu-id="b40ff-210">True</span></span>                              |
| <span data-ttu-id="b40ff-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="b40ff-211">Is Indexed</span></span>             | <span data-ttu-id="b40ff-212">Falso</span><span class="sxs-lookup"><span data-stu-id="b40ff-212">False</span></span>                             |
| <span data-ttu-id="b40ff-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b40ff-213">In Global Catalog</span></span>      | <span data-ttu-id="b40ff-214">Falso</span><span class="sxs-lookup"><span data-stu-id="b40ff-214">False</span></span>                             |
| <span data-ttu-id="b40ff-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b40ff-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="b40ff-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b40ff-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b40ff-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b40ff-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b40ff-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b40ff-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b40ff-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b40ff-219">Search-Flags</span></span>           | <span data-ttu-id="b40ff-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b40ff-220">0x00000010</span></span>                        |
| <span data-ttu-id="b40ff-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b40ff-221">System-Flags</span></span>           | <span data-ttu-id="b40ff-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b40ff-222">0x00000010</span></span>                        |
| <span data-ttu-id="b40ff-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b40ff-223">Classes used in</span></span>        | [<span data-ttu-id="b40ff-224">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="b40ff-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b40ff-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b40ff-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b40ff-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="b40ff-226">Entry</span></span> | <span data-ttu-id="b40ff-227">Valor</span><span class="sxs-lookup"><span data-stu-id="b40ff-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b40ff-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="b40ff-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b40ff-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b40ff-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b40ff-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="b40ff-230">System-Only</span></span>            | <span data-ttu-id="b40ff-231">Falso</span><span class="sxs-lookup"><span data-stu-id="b40ff-231">False</span></span>                             |
| <span data-ttu-id="b40ff-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b40ff-232">Is-Single-Valued</span></span>       | <span data-ttu-id="b40ff-233">True</span><span class="sxs-lookup"><span data-stu-id="b40ff-233">True</span></span>                              |
| <span data-ttu-id="b40ff-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="b40ff-234">Is Indexed</span></span>             | <span data-ttu-id="b40ff-235">Falso</span><span class="sxs-lookup"><span data-stu-id="b40ff-235">False</span></span>                             |
| <span data-ttu-id="b40ff-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b40ff-236">In Global Catalog</span></span>      | <span data-ttu-id="b40ff-237">Falso</span><span class="sxs-lookup"><span data-stu-id="b40ff-237">False</span></span>                             |
| <span data-ttu-id="b40ff-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b40ff-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="b40ff-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b40ff-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b40ff-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b40ff-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b40ff-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b40ff-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b40ff-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b40ff-242">Search-Flags</span></span>           | <span data-ttu-id="b40ff-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b40ff-243">0x00000010</span></span>                        |
| <span data-ttu-id="b40ff-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b40ff-244">System-Flags</span></span>           | <span data-ttu-id="b40ff-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b40ff-245">0x00000010</span></span>                        |
| <span data-ttu-id="b40ff-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b40ff-246">Classes used in</span></span>        | [<span data-ttu-id="b40ff-247">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="b40ff-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b40ff-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b40ff-248">Windows Server 2012</span></span>



| <span data-ttu-id="b40ff-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="b40ff-249">Entry</span></span> | <span data-ttu-id="b40ff-250">Valor</span><span class="sxs-lookup"><span data-stu-id="b40ff-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b40ff-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="b40ff-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b40ff-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b40ff-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b40ff-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="b40ff-253">System-Only</span></span>            | <span data-ttu-id="b40ff-254">Falso</span><span class="sxs-lookup"><span data-stu-id="b40ff-254">False</span></span>                             |
| <span data-ttu-id="b40ff-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b40ff-255">Is-Single-Valued</span></span>       | <span data-ttu-id="b40ff-256">True</span><span class="sxs-lookup"><span data-stu-id="b40ff-256">True</span></span>                              |
| <span data-ttu-id="b40ff-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="b40ff-257">Is Indexed</span></span>             | <span data-ttu-id="b40ff-258">Falso</span><span class="sxs-lookup"><span data-stu-id="b40ff-258">False</span></span>                             |
| <span data-ttu-id="b40ff-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b40ff-259">In Global Catalog</span></span>      | <span data-ttu-id="b40ff-260">Falso</span><span class="sxs-lookup"><span data-stu-id="b40ff-260">False</span></span>                             |
| <span data-ttu-id="b40ff-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b40ff-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="b40ff-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b40ff-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b40ff-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b40ff-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="b40ff-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b40ff-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="b40ff-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b40ff-265">Search-Flags</span></span>           | <span data-ttu-id="b40ff-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b40ff-266">0x00000010</span></span>                        |
| <span data-ttu-id="b40ff-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b40ff-267">System-Flags</span></span>           | <span data-ttu-id="b40ff-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b40ff-268">0x00000010</span></span>                        |
| <span data-ttu-id="b40ff-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b40ff-269">Classes used in</span></span>        | [<span data-ttu-id="b40ff-270">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="b40ff-270">**User**</span></span>](c-user.md)<br/> |



 

 





