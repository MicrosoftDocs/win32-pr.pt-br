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
# <a name="profile-path-attribute"></a><span data-ttu-id="f59e3-106">Profile-Path atributo</span><span class="sxs-lookup"><span data-stu-id="f59e3-106">Profile-Path attribute</span></span>

<span data-ttu-id="f59e3-107">Especifica um caminho para o perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="f59e3-107">Specifies a path to the user's profile.</span></span> <span data-ttu-id="f59e3-108">Esse valor pode ser uma cadeia de caracteres nula, um caminho absoluto local ou um caminho UNC.</span><span class="sxs-lookup"><span data-stu-id="f59e3-108">This value can be a null string, a local absolute path, or a UNC path.</span></span>



| <span data-ttu-id="f59e3-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="f59e3-109">Entry</span></span> | <span data-ttu-id="f59e3-110">Valor</span><span class="sxs-lookup"><span data-stu-id="f59e3-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="f59e3-111">CN</span><span class="sxs-lookup"><span data-stu-id="f59e3-111">CN</span></span>                | <span data-ttu-id="f59e3-112">Profile-Path</span><span class="sxs-lookup"><span data-stu-id="f59e3-112">Profile-Path</span></span>                                                             |
| <span data-ttu-id="f59e3-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f59e3-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f59e3-114">profilepath</span><span class="sxs-lookup"><span data-stu-id="f59e3-114">profilePath</span></span>                                                              |
| <span data-ttu-id="f59e3-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f59e3-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="f59e3-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f59e3-116">Update Privilege</span></span>  | <span data-ttu-id="f59e3-117">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="f59e3-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="f59e3-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f59e3-118">Update Frequency</span></span>  | <span data-ttu-id="f59e3-119">Quando o registro do usuário é criado e sempre que o caminho precisa ser alterado.</span><span class="sxs-lookup"><span data-stu-id="f59e3-119">When the user's record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="f59e3-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f59e3-120">Attribute-Id</span></span>      | <span data-ttu-id="f59e3-121">1.2.840.113556.1.4.139</span><span class="sxs-lookup"><span data-stu-id="f59e3-121">1.2.840.113556.1.4.139</span></span>                                                   |
| <span data-ttu-id="f59e3-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f59e3-122">System-Id-Guid</span></span>    | <span data-ttu-id="f59e3-123">bf967a05-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f59e3-123">bf967a05-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="f59e3-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="f59e3-124">Syntax</span></span>            | [<span data-ttu-id="f59e3-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f59e3-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="f59e3-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="f59e3-126">Implementations</span></span>

-   [<span data-ttu-id="f59e3-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f59e3-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f59e3-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f59e3-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f59e3-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f59e3-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f59e3-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f59e3-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f59e3-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f59e3-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f59e3-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f59e3-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f59e3-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f59e3-133">Windows 2000 Server</span></span>



| <span data-ttu-id="f59e3-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="f59e3-134">Entry</span></span> | <span data-ttu-id="f59e3-135">Valor</span><span class="sxs-lookup"><span data-stu-id="f59e3-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f59e3-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="f59e3-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f59e3-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f59e3-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f59e3-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="f59e3-138">System-Only</span></span>            | <span data-ttu-id="f59e3-139">Falso</span><span class="sxs-lookup"><span data-stu-id="f59e3-139">False</span></span>                             |
| <span data-ttu-id="f59e3-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f59e3-140">Is-Single-Valued</span></span>       | <span data-ttu-id="f59e3-141">True</span><span class="sxs-lookup"><span data-stu-id="f59e3-141">True</span></span>                              |
| <span data-ttu-id="f59e3-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="f59e3-142">Is Indexed</span></span>             | <span data-ttu-id="f59e3-143">Falso</span><span class="sxs-lookup"><span data-stu-id="f59e3-143">False</span></span>                             |
| <span data-ttu-id="f59e3-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f59e3-144">In Global Catalog</span></span>      | <span data-ttu-id="f59e3-145">Falso</span><span class="sxs-lookup"><span data-stu-id="f59e3-145">False</span></span>                             |
| <span data-ttu-id="f59e3-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f59e3-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="f59e3-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f59e3-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f59e3-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f59e3-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f59e3-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f59e3-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f59e3-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f59e3-150">Search-Flags</span></span>           | <span data-ttu-id="f59e3-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f59e3-151">0x00000010</span></span>                        |
| <span data-ttu-id="f59e3-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f59e3-152">System-Flags</span></span>           | <span data-ttu-id="f59e3-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f59e3-153">0x00000010</span></span>                        |
| <span data-ttu-id="f59e3-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f59e3-154">Classes used in</span></span>        | [<span data-ttu-id="f59e3-155">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f59e3-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f59e3-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f59e3-156">Windows Server 2003</span></span>



| <span data-ttu-id="f59e3-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="f59e3-157">Entry</span></span> | <span data-ttu-id="f59e3-158">Valor</span><span class="sxs-lookup"><span data-stu-id="f59e3-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f59e3-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="f59e3-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f59e3-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f59e3-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f59e3-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="f59e3-161">System-Only</span></span>            | <span data-ttu-id="f59e3-162">Falso</span><span class="sxs-lookup"><span data-stu-id="f59e3-162">False</span></span>                             |
| <span data-ttu-id="f59e3-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f59e3-163">Is-Single-Valued</span></span>       | <span data-ttu-id="f59e3-164">True</span><span class="sxs-lookup"><span data-stu-id="f59e3-164">True</span></span>                              |
| <span data-ttu-id="f59e3-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="f59e3-165">Is Indexed</span></span>             | <span data-ttu-id="f59e3-166">Falso</span><span class="sxs-lookup"><span data-stu-id="f59e3-166">False</span></span>                             |
| <span data-ttu-id="f59e3-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f59e3-167">In Global Catalog</span></span>      | <span data-ttu-id="f59e3-168">Falso</span><span class="sxs-lookup"><span data-stu-id="f59e3-168">False</span></span>                             |
| <span data-ttu-id="f59e3-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f59e3-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="f59e3-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f59e3-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f59e3-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f59e3-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f59e3-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f59e3-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f59e3-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f59e3-173">Search-Flags</span></span>           | <span data-ttu-id="f59e3-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f59e3-174">0x00000010</span></span>                        |
| <span data-ttu-id="f59e3-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f59e3-175">System-Flags</span></span>           | <span data-ttu-id="f59e3-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f59e3-176">0x00000010</span></span>                        |
| <span data-ttu-id="f59e3-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f59e3-177">Classes used in</span></span>        | [<span data-ttu-id="f59e3-178">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f59e3-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f59e3-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f59e3-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f59e3-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="f59e3-180">Entry</span></span> | <span data-ttu-id="f59e3-181">Valor</span><span class="sxs-lookup"><span data-stu-id="f59e3-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f59e3-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="f59e3-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f59e3-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f59e3-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f59e3-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="f59e3-184">System-Only</span></span>            | <span data-ttu-id="f59e3-185">Falso</span><span class="sxs-lookup"><span data-stu-id="f59e3-185">False</span></span>                             |
| <span data-ttu-id="f59e3-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f59e3-186">Is-Single-Valued</span></span>       | <span data-ttu-id="f59e3-187">True</span><span class="sxs-lookup"><span data-stu-id="f59e3-187">True</span></span>                              |
| <span data-ttu-id="f59e3-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="f59e3-188">Is Indexed</span></span>             | <span data-ttu-id="f59e3-189">Falso</span><span class="sxs-lookup"><span data-stu-id="f59e3-189">False</span></span>                             |
| <span data-ttu-id="f59e3-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f59e3-190">In Global Catalog</span></span>      | <span data-ttu-id="f59e3-191">Falso</span><span class="sxs-lookup"><span data-stu-id="f59e3-191">False</span></span>                             |
| <span data-ttu-id="f59e3-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f59e3-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="f59e3-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f59e3-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f59e3-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f59e3-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f59e3-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f59e3-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f59e3-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f59e3-196">Search-Flags</span></span>           | <span data-ttu-id="f59e3-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f59e3-197">0x00000010</span></span>                        |
| <span data-ttu-id="f59e3-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f59e3-198">System-Flags</span></span>           | <span data-ttu-id="f59e3-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f59e3-199">0x00000010</span></span>                        |
| <span data-ttu-id="f59e3-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f59e3-200">Classes used in</span></span>        | [<span data-ttu-id="f59e3-201">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f59e3-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f59e3-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f59e3-202">Windows Server 2008</span></span>



| <span data-ttu-id="f59e3-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="f59e3-203">Entry</span></span> | <span data-ttu-id="f59e3-204">Valor</span><span class="sxs-lookup"><span data-stu-id="f59e3-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f59e3-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="f59e3-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f59e3-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f59e3-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f59e3-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="f59e3-207">System-Only</span></span>            | <span data-ttu-id="f59e3-208">Falso</span><span class="sxs-lookup"><span data-stu-id="f59e3-208">False</span></span>                             |
| <span data-ttu-id="f59e3-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f59e3-209">Is-Single-Valued</span></span>       | <span data-ttu-id="f59e3-210">True</span><span class="sxs-lookup"><span data-stu-id="f59e3-210">True</span></span>                              |
| <span data-ttu-id="f59e3-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="f59e3-211">Is Indexed</span></span>             | <span data-ttu-id="f59e3-212">Falso</span><span class="sxs-lookup"><span data-stu-id="f59e3-212">False</span></span>                             |
| <span data-ttu-id="f59e3-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f59e3-213">In Global Catalog</span></span>      | <span data-ttu-id="f59e3-214">Falso</span><span class="sxs-lookup"><span data-stu-id="f59e3-214">False</span></span>                             |
| <span data-ttu-id="f59e3-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f59e3-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="f59e3-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f59e3-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f59e3-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f59e3-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f59e3-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f59e3-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f59e3-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f59e3-219">Search-Flags</span></span>           | <span data-ttu-id="f59e3-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f59e3-220">0x00000010</span></span>                        |
| <span data-ttu-id="f59e3-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f59e3-221">System-Flags</span></span>           | <span data-ttu-id="f59e3-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f59e3-222">0x00000010</span></span>                        |
| <span data-ttu-id="f59e3-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f59e3-223">Classes used in</span></span>        | [<span data-ttu-id="f59e3-224">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f59e3-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f59e3-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f59e3-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f59e3-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="f59e3-226">Entry</span></span> | <span data-ttu-id="f59e3-227">Valor</span><span class="sxs-lookup"><span data-stu-id="f59e3-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f59e3-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="f59e3-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f59e3-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f59e3-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f59e3-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="f59e3-230">System-Only</span></span>            | <span data-ttu-id="f59e3-231">Falso</span><span class="sxs-lookup"><span data-stu-id="f59e3-231">False</span></span>                             |
| <span data-ttu-id="f59e3-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f59e3-232">Is-Single-Valued</span></span>       | <span data-ttu-id="f59e3-233">True</span><span class="sxs-lookup"><span data-stu-id="f59e3-233">True</span></span>                              |
| <span data-ttu-id="f59e3-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="f59e3-234">Is Indexed</span></span>             | <span data-ttu-id="f59e3-235">Falso</span><span class="sxs-lookup"><span data-stu-id="f59e3-235">False</span></span>                             |
| <span data-ttu-id="f59e3-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f59e3-236">In Global Catalog</span></span>      | <span data-ttu-id="f59e3-237">Falso</span><span class="sxs-lookup"><span data-stu-id="f59e3-237">False</span></span>                             |
| <span data-ttu-id="f59e3-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f59e3-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="f59e3-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f59e3-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f59e3-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f59e3-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f59e3-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f59e3-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f59e3-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f59e3-242">Search-Flags</span></span>           | <span data-ttu-id="f59e3-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f59e3-243">0x00000010</span></span>                        |
| <span data-ttu-id="f59e3-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f59e3-244">System-Flags</span></span>           | <span data-ttu-id="f59e3-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f59e3-245">0x00000010</span></span>                        |
| <span data-ttu-id="f59e3-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f59e3-246">Classes used in</span></span>        | [<span data-ttu-id="f59e3-247">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f59e3-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f59e3-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f59e3-248">Windows Server 2012</span></span>



| <span data-ttu-id="f59e3-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="f59e3-249">Entry</span></span> | <span data-ttu-id="f59e3-250">Valor</span><span class="sxs-lookup"><span data-stu-id="f59e3-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f59e3-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="f59e3-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f59e3-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f59e3-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f59e3-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="f59e3-253">System-Only</span></span>            | <span data-ttu-id="f59e3-254">Falso</span><span class="sxs-lookup"><span data-stu-id="f59e3-254">False</span></span>                             |
| <span data-ttu-id="f59e3-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f59e3-255">Is-Single-Valued</span></span>       | <span data-ttu-id="f59e3-256">True</span><span class="sxs-lookup"><span data-stu-id="f59e3-256">True</span></span>                              |
| <span data-ttu-id="f59e3-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="f59e3-257">Is Indexed</span></span>             | <span data-ttu-id="f59e3-258">Falso</span><span class="sxs-lookup"><span data-stu-id="f59e3-258">False</span></span>                             |
| <span data-ttu-id="f59e3-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f59e3-259">In Global Catalog</span></span>      | <span data-ttu-id="f59e3-260">Falso</span><span class="sxs-lookup"><span data-stu-id="f59e3-260">False</span></span>                             |
| <span data-ttu-id="f59e3-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f59e3-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="f59e3-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f59e3-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f59e3-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f59e3-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f59e3-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f59e3-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f59e3-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f59e3-265">Search-Flags</span></span>           | <span data-ttu-id="f59e3-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f59e3-266">0x00000010</span></span>                        |
| <span data-ttu-id="f59e3-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f59e3-267">System-Flags</span></span>           | <span data-ttu-id="f59e3-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f59e3-268">0x00000010</span></span>                        |
| <span data-ttu-id="f59e3-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f59e3-269">Classes used in</span></span>        | [<span data-ttu-id="f59e3-270">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f59e3-270">**User**</span></span>](c-user.md)<br/> |



 

 





