---
title: Profile-Path atributo
description: Especifica um caminho para o perfil do usuário. Esse valor pode ser uma cadeia de caracteres nula, um caminho absoluto local ou um caminho UNC.
ms.assetid: 03891152-52c6-4799-ae79-3be284204391
ms.tgt_platform: multiple
keywords:
- Esquema de Profile-Path do atributo AD
- Esquema de AD do atributo ProfilePath
topic_type:
- apiref
api_name:
- Profile-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d1c255843cf578301ce330b79f3ca983030952
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919573"
---
# <a name="profile-path-attribute"></a><span data-ttu-id="75a06-106">Profile-Path atributo</span><span class="sxs-lookup"><span data-stu-id="75a06-106">Profile-Path attribute</span></span>

<span data-ttu-id="75a06-107">Especifica um caminho para o perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="75a06-107">Specifies a path to the user's profile.</span></span> <span data-ttu-id="75a06-108">Esse valor pode ser uma cadeia de caracteres nula, um caminho absoluto local ou um caminho UNC.</span><span class="sxs-lookup"><span data-stu-id="75a06-108">This value can be a null string, a local absolute path, or a UNC path.</span></span>



| <span data-ttu-id="75a06-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="75a06-109">Entry</span></span> | <span data-ttu-id="75a06-110">Valor</span><span class="sxs-lookup"><span data-stu-id="75a06-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="75a06-111">CN</span><span class="sxs-lookup"><span data-stu-id="75a06-111">CN</span></span>                | <span data-ttu-id="75a06-112">Profile-Path</span><span class="sxs-lookup"><span data-stu-id="75a06-112">Profile-Path</span></span>                                                             |
| <span data-ttu-id="75a06-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="75a06-113">Ldap-Display-Name</span></span> | <span data-ttu-id="75a06-114">profilepath</span><span class="sxs-lookup"><span data-stu-id="75a06-114">profilePath</span></span>                                                              |
| <span data-ttu-id="75a06-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="75a06-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="75a06-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="75a06-116">Update Privilege</span></span>  | <span data-ttu-id="75a06-117">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="75a06-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="75a06-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="75a06-118">Update Frequency</span></span>  | <span data-ttu-id="75a06-119">Quando o registro do usuário é criado e sempre que o caminho precisa ser alterado.</span><span class="sxs-lookup"><span data-stu-id="75a06-119">When the user's record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="75a06-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="75a06-120">Attribute-Id</span></span>      | <span data-ttu-id="75a06-121">1.2.840.113556.1.4.139</span><span class="sxs-lookup"><span data-stu-id="75a06-121">1.2.840.113556.1.4.139</span></span>                                                   |
| <span data-ttu-id="75a06-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="75a06-122">System-Id-Guid</span></span>    | <span data-ttu-id="75a06-123">bf967a05-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="75a06-123">bf967a05-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="75a06-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="75a06-124">Syntax</span></span>            | [<span data-ttu-id="75a06-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="75a06-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="75a06-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="75a06-126">Implementations</span></span>

-   [<span data-ttu-id="75a06-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="75a06-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="75a06-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="75a06-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="75a06-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="75a06-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="75a06-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="75a06-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="75a06-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="75a06-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="75a06-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="75a06-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="75a06-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="75a06-133">Windows 2000 Server</span></span>



| <span data-ttu-id="75a06-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="75a06-134">Entry</span></span> | <span data-ttu-id="75a06-135">Valor</span><span class="sxs-lookup"><span data-stu-id="75a06-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="75a06-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="75a06-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="75a06-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75a06-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="75a06-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="75a06-138">System-Only</span></span>            | <span data-ttu-id="75a06-139">Falso</span><span class="sxs-lookup"><span data-stu-id="75a06-139">False</span></span>                             |
| <span data-ttu-id="75a06-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="75a06-140">Is-Single-Valued</span></span>       | <span data-ttu-id="75a06-141">True</span><span class="sxs-lookup"><span data-stu-id="75a06-141">True</span></span>                              |
| <span data-ttu-id="75a06-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="75a06-142">Is Indexed</span></span>             | <span data-ttu-id="75a06-143">Falso</span><span class="sxs-lookup"><span data-stu-id="75a06-143">False</span></span>                             |
| <span data-ttu-id="75a06-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="75a06-144">In Global Catalog</span></span>      | <span data-ttu-id="75a06-145">Falso</span><span class="sxs-lookup"><span data-stu-id="75a06-145">False</span></span>                             |
| <span data-ttu-id="75a06-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="75a06-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="75a06-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="75a06-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="75a06-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75a06-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="75a06-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75a06-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="75a06-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75a06-150">Search-Flags</span></span>           | <span data-ttu-id="75a06-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a06-151">0x00000010</span></span>                        |
| <span data-ttu-id="75a06-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75a06-152">System-Flags</span></span>           | <span data-ttu-id="75a06-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a06-153">0x00000010</span></span>                        |
| <span data-ttu-id="75a06-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="75a06-154">Classes used in</span></span>        | [<span data-ttu-id="75a06-155">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="75a06-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="75a06-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="75a06-156">Windows Server 2003</span></span>



| <span data-ttu-id="75a06-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="75a06-157">Entry</span></span> | <span data-ttu-id="75a06-158">Valor</span><span class="sxs-lookup"><span data-stu-id="75a06-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="75a06-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="75a06-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="75a06-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75a06-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="75a06-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="75a06-161">System-Only</span></span>            | <span data-ttu-id="75a06-162">Falso</span><span class="sxs-lookup"><span data-stu-id="75a06-162">False</span></span>                             |
| <span data-ttu-id="75a06-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="75a06-163">Is-Single-Valued</span></span>       | <span data-ttu-id="75a06-164">True</span><span class="sxs-lookup"><span data-stu-id="75a06-164">True</span></span>                              |
| <span data-ttu-id="75a06-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="75a06-165">Is Indexed</span></span>             | <span data-ttu-id="75a06-166">Falso</span><span class="sxs-lookup"><span data-stu-id="75a06-166">False</span></span>                             |
| <span data-ttu-id="75a06-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="75a06-167">In Global Catalog</span></span>      | <span data-ttu-id="75a06-168">Falso</span><span class="sxs-lookup"><span data-stu-id="75a06-168">False</span></span>                             |
| <span data-ttu-id="75a06-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="75a06-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="75a06-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="75a06-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="75a06-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75a06-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="75a06-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75a06-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="75a06-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75a06-173">Search-Flags</span></span>           | <span data-ttu-id="75a06-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a06-174">0x00000010</span></span>                        |
| <span data-ttu-id="75a06-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75a06-175">System-Flags</span></span>           | <span data-ttu-id="75a06-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a06-176">0x00000010</span></span>                        |
| <span data-ttu-id="75a06-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="75a06-177">Classes used in</span></span>        | [<span data-ttu-id="75a06-178">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="75a06-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="75a06-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="75a06-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="75a06-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="75a06-180">Entry</span></span> | <span data-ttu-id="75a06-181">Valor</span><span class="sxs-lookup"><span data-stu-id="75a06-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="75a06-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="75a06-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="75a06-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75a06-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="75a06-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="75a06-184">System-Only</span></span>            | <span data-ttu-id="75a06-185">Falso</span><span class="sxs-lookup"><span data-stu-id="75a06-185">False</span></span>                             |
| <span data-ttu-id="75a06-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="75a06-186">Is-Single-Valued</span></span>       | <span data-ttu-id="75a06-187">True</span><span class="sxs-lookup"><span data-stu-id="75a06-187">True</span></span>                              |
| <span data-ttu-id="75a06-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="75a06-188">Is Indexed</span></span>             | <span data-ttu-id="75a06-189">Falso</span><span class="sxs-lookup"><span data-stu-id="75a06-189">False</span></span>                             |
| <span data-ttu-id="75a06-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="75a06-190">In Global Catalog</span></span>      | <span data-ttu-id="75a06-191">Falso</span><span class="sxs-lookup"><span data-stu-id="75a06-191">False</span></span>                             |
| <span data-ttu-id="75a06-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="75a06-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="75a06-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="75a06-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="75a06-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75a06-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="75a06-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75a06-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="75a06-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75a06-196">Search-Flags</span></span>           | <span data-ttu-id="75a06-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a06-197">0x00000010</span></span>                        |
| <span data-ttu-id="75a06-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75a06-198">System-Flags</span></span>           | <span data-ttu-id="75a06-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a06-199">0x00000010</span></span>                        |
| <span data-ttu-id="75a06-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="75a06-200">Classes used in</span></span>        | [<span data-ttu-id="75a06-201">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="75a06-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="75a06-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75a06-202">Windows Server 2008</span></span>



| <span data-ttu-id="75a06-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="75a06-203">Entry</span></span> | <span data-ttu-id="75a06-204">Valor</span><span class="sxs-lookup"><span data-stu-id="75a06-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="75a06-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="75a06-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="75a06-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75a06-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="75a06-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="75a06-207">System-Only</span></span>            | <span data-ttu-id="75a06-208">Falso</span><span class="sxs-lookup"><span data-stu-id="75a06-208">False</span></span>                             |
| <span data-ttu-id="75a06-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="75a06-209">Is-Single-Valued</span></span>       | <span data-ttu-id="75a06-210">True</span><span class="sxs-lookup"><span data-stu-id="75a06-210">True</span></span>                              |
| <span data-ttu-id="75a06-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="75a06-211">Is Indexed</span></span>             | <span data-ttu-id="75a06-212">Falso</span><span class="sxs-lookup"><span data-stu-id="75a06-212">False</span></span>                             |
| <span data-ttu-id="75a06-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="75a06-213">In Global Catalog</span></span>      | <span data-ttu-id="75a06-214">Falso</span><span class="sxs-lookup"><span data-stu-id="75a06-214">False</span></span>                             |
| <span data-ttu-id="75a06-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="75a06-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="75a06-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="75a06-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="75a06-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75a06-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="75a06-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75a06-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="75a06-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75a06-219">Search-Flags</span></span>           | <span data-ttu-id="75a06-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a06-220">0x00000010</span></span>                        |
| <span data-ttu-id="75a06-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75a06-221">System-Flags</span></span>           | <span data-ttu-id="75a06-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a06-222">0x00000010</span></span>                        |
| <span data-ttu-id="75a06-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="75a06-223">Classes used in</span></span>        | [<span data-ttu-id="75a06-224">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="75a06-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="75a06-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="75a06-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="75a06-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="75a06-226">Entry</span></span> | <span data-ttu-id="75a06-227">Valor</span><span class="sxs-lookup"><span data-stu-id="75a06-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="75a06-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="75a06-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="75a06-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75a06-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="75a06-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="75a06-230">System-Only</span></span>            | <span data-ttu-id="75a06-231">Falso</span><span class="sxs-lookup"><span data-stu-id="75a06-231">False</span></span>                             |
| <span data-ttu-id="75a06-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="75a06-232">Is-Single-Valued</span></span>       | <span data-ttu-id="75a06-233">True</span><span class="sxs-lookup"><span data-stu-id="75a06-233">True</span></span>                              |
| <span data-ttu-id="75a06-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="75a06-234">Is Indexed</span></span>             | <span data-ttu-id="75a06-235">Falso</span><span class="sxs-lookup"><span data-stu-id="75a06-235">False</span></span>                             |
| <span data-ttu-id="75a06-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="75a06-236">In Global Catalog</span></span>      | <span data-ttu-id="75a06-237">Falso</span><span class="sxs-lookup"><span data-stu-id="75a06-237">False</span></span>                             |
| <span data-ttu-id="75a06-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="75a06-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="75a06-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="75a06-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="75a06-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75a06-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="75a06-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75a06-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="75a06-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75a06-242">Search-Flags</span></span>           | <span data-ttu-id="75a06-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a06-243">0x00000010</span></span>                        |
| <span data-ttu-id="75a06-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75a06-244">System-Flags</span></span>           | <span data-ttu-id="75a06-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a06-245">0x00000010</span></span>                        |
| <span data-ttu-id="75a06-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="75a06-246">Classes used in</span></span>        | [<span data-ttu-id="75a06-247">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="75a06-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="75a06-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="75a06-248">Windows Server 2012</span></span>



| <span data-ttu-id="75a06-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="75a06-249">Entry</span></span> | <span data-ttu-id="75a06-250">Valor</span><span class="sxs-lookup"><span data-stu-id="75a06-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="75a06-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="75a06-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="75a06-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75a06-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="75a06-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="75a06-253">System-Only</span></span>            | <span data-ttu-id="75a06-254">Falso</span><span class="sxs-lookup"><span data-stu-id="75a06-254">False</span></span>                             |
| <span data-ttu-id="75a06-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="75a06-255">Is-Single-Valued</span></span>       | <span data-ttu-id="75a06-256">True</span><span class="sxs-lookup"><span data-stu-id="75a06-256">True</span></span>                              |
| <span data-ttu-id="75a06-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="75a06-257">Is Indexed</span></span>             | <span data-ttu-id="75a06-258">Falso</span><span class="sxs-lookup"><span data-stu-id="75a06-258">False</span></span>                             |
| <span data-ttu-id="75a06-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="75a06-259">In Global Catalog</span></span>      | <span data-ttu-id="75a06-260">Falso</span><span class="sxs-lookup"><span data-stu-id="75a06-260">False</span></span>                             |
| <span data-ttu-id="75a06-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="75a06-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="75a06-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="75a06-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="75a06-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75a06-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="75a06-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75a06-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="75a06-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75a06-265">Search-Flags</span></span>           | <span data-ttu-id="75a06-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a06-266">0x00000010</span></span>                        |
| <span data-ttu-id="75a06-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75a06-267">System-Flags</span></span>           | <span data-ttu-id="75a06-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a06-268">0x00000010</span></span>                        |
| <span data-ttu-id="75a06-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="75a06-269">Classes used in</span></span>        | [<span data-ttu-id="75a06-270">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="75a06-270">**User**</span></span>](c-user.md)<br/> |



 

 





