---
title: Usuário-compartilhado-pasta-outro atributo
description: Especifica um caminho UNC para a pasta de documentos compartilhados adicional do usuário. O caminho deve ser um caminho UNC de rede do diretório de compartilhamento do servidor de formulário \\ \\ \\ \\ . Esse valor pode ser uma cadeia de caracteres nula.
ms.assetid: 7d546cda-b2c1-46a6-a3cf-a7c78ddb1422
ms.tgt_platform: multiple
keywords:
- Usuário-compartilhado-pasta-outro esquema do AD do atributo
- Esquema de AD do atributo userSharedFolderOther
topic_type:
- apiref
api_name:
- User-Shared-Folder-Other
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6087a28df474ff06c1d8bf54d694176df8591b5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645403"
---
# <a name="user-shared-folder-other-attribute"></a><span data-ttu-id="29a12-107">Usuário-compartilhado-pasta-outro atributo</span><span class="sxs-lookup"><span data-stu-id="29a12-107">User-Shared-Folder-Other attribute</span></span>

<span data-ttu-id="29a12-108">Especifica um caminho UNC para a pasta de documentos compartilhados adicional do usuário.</span><span class="sxs-lookup"><span data-stu-id="29a12-108">Specifies a UNC path to the user's additional shared documents folder.</span></span> <span data-ttu-id="29a12-109">O caminho deve ser um caminho UNC de rede do **\\\\** diretório de compartilhamento do _servidor_ de formulário *_\\_*  *_\\_* .</span><span class="sxs-lookup"><span data-stu-id="29a12-109">The path must be a network UNC path of the form **\\\\**_Server_*_\\_*_Share_*_\\_*_Directory_.</span></span> <span data-ttu-id="29a12-110">Esse valor pode ser uma cadeia de caracteres nula.</span><span class="sxs-lookup"><span data-stu-id="29a12-110">This value can be a null string.</span></span>



| <span data-ttu-id="29a12-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="29a12-111">Entry</span></span> | <span data-ttu-id="29a12-112">Valor</span><span class="sxs-lookup"><span data-stu-id="29a12-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="29a12-113">CN</span><span class="sxs-lookup"><span data-stu-id="29a12-113">CN</span></span>                | <span data-ttu-id="29a12-114">Usuário-compartilhado-pasta-outro</span><span class="sxs-lookup"><span data-stu-id="29a12-114">User-Shared-Folder-Other</span></span>                                                          |
| <span data-ttu-id="29a12-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="29a12-115">Ldap-Display-Name</span></span> | <span data-ttu-id="29a12-116">userSharedFolderOther</span><span class="sxs-lookup"><span data-stu-id="29a12-116">userSharedFolderOther</span></span>                                                             |
| <span data-ttu-id="29a12-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="29a12-117">Size</span></span>              | \-                                                                                |
| <span data-ttu-id="29a12-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="29a12-118">Update Privilege</span></span>  | <span data-ttu-id="29a12-119">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="29a12-119">Domain administrator or account owner.</span></span>                                            |
| <span data-ttu-id="29a12-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="29a12-120">Update Frequency</span></span>  | <span data-ttu-id="29a12-121">Quando o registro do usuário é criado e sempre que a pasta compartilhada precisa ser alterada.</span><span class="sxs-lookup"><span data-stu-id="29a12-121">When the user's record is created and whenever the shared folder needs to change.</span></span> |
| <span data-ttu-id="29a12-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="29a12-122">Attribute-Id</span></span>      | <span data-ttu-id="29a12-123">1.2.840.113556.1.4.752</span><span class="sxs-lookup"><span data-stu-id="29a12-123">1.2.840.113556.1.4.752</span></span>                                                            |
| <span data-ttu-id="29a12-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="29a12-124">System-Id-Guid</span></span>    | <span data-ttu-id="29a12-125">9a9a0220-4a5b-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="29a12-125">9a9a0220-4a5b-11d1-a9c3-0000f80367c1</span></span>                                              |
| <span data-ttu-id="29a12-126">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29a12-126">Syntax</span></span>            | [<span data-ttu-id="29a12-127">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="29a12-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="29a12-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="29a12-128">Implementations</span></span>

-   [<span data-ttu-id="29a12-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="29a12-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="29a12-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="29a12-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="29a12-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="29a12-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="29a12-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="29a12-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="29a12-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="29a12-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="29a12-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="29a12-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="29a12-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="29a12-135">Windows 2000 Server</span></span>



| <span data-ttu-id="29a12-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="29a12-136">Entry</span></span> | <span data-ttu-id="29a12-137">Valor</span><span class="sxs-lookup"><span data-stu-id="29a12-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="29a12-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="29a12-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="29a12-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29a12-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="29a12-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="29a12-140">System-Only</span></span>            | <span data-ttu-id="29a12-141">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-141">False</span></span>                             |
| <span data-ttu-id="29a12-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="29a12-142">Is-Single-Valued</span></span>       | <span data-ttu-id="29a12-143">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-143">False</span></span>                             |
| <span data-ttu-id="29a12-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="29a12-144">Is Indexed</span></span>             | <span data-ttu-id="29a12-145">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-145">False</span></span>                             |
| <span data-ttu-id="29a12-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="29a12-146">In Global Catalog</span></span>      | <span data-ttu-id="29a12-147">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-147">False</span></span>                             |
| <span data-ttu-id="29a12-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="29a12-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="29a12-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="29a12-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="29a12-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29a12-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="29a12-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29a12-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="29a12-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29a12-152">Search-Flags</span></span>           | <span data-ttu-id="29a12-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29a12-153">0x00000000</span></span>                        |
| <span data-ttu-id="29a12-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29a12-154">System-Flags</span></span>           | <span data-ttu-id="29a12-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29a12-155">0x00000010</span></span>                        |
| <span data-ttu-id="29a12-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="29a12-156">Classes used in</span></span>        | [<span data-ttu-id="29a12-157">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="29a12-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="29a12-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="29a12-158">Windows Server 2003</span></span>



| <span data-ttu-id="29a12-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="29a12-159">Entry</span></span> | <span data-ttu-id="29a12-160">Valor</span><span class="sxs-lookup"><span data-stu-id="29a12-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="29a12-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="29a12-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="29a12-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29a12-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="29a12-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="29a12-163">System-Only</span></span>            | <span data-ttu-id="29a12-164">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-164">False</span></span>                             |
| <span data-ttu-id="29a12-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="29a12-165">Is-Single-Valued</span></span>       | <span data-ttu-id="29a12-166">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-166">False</span></span>                             |
| <span data-ttu-id="29a12-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="29a12-167">Is Indexed</span></span>             | <span data-ttu-id="29a12-168">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-168">False</span></span>                             |
| <span data-ttu-id="29a12-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="29a12-169">In Global Catalog</span></span>      | <span data-ttu-id="29a12-170">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-170">False</span></span>                             |
| <span data-ttu-id="29a12-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="29a12-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="29a12-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="29a12-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="29a12-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29a12-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="29a12-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29a12-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="29a12-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29a12-175">Search-Flags</span></span>           | <span data-ttu-id="29a12-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29a12-176">0x00000000</span></span>                        |
| <span data-ttu-id="29a12-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29a12-177">System-Flags</span></span>           | <span data-ttu-id="29a12-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29a12-178">0x00000010</span></span>                        |
| <span data-ttu-id="29a12-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="29a12-179">Classes used in</span></span>        | [<span data-ttu-id="29a12-180">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="29a12-180">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="29a12-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="29a12-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="29a12-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="29a12-182">Entry</span></span> | <span data-ttu-id="29a12-183">Valor</span><span class="sxs-lookup"><span data-stu-id="29a12-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="29a12-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="29a12-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="29a12-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29a12-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="29a12-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="29a12-186">System-Only</span></span>            | <span data-ttu-id="29a12-187">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-187">False</span></span>                             |
| <span data-ttu-id="29a12-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="29a12-188">Is-Single-Valued</span></span>       | <span data-ttu-id="29a12-189">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-189">False</span></span>                             |
| <span data-ttu-id="29a12-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="29a12-190">Is Indexed</span></span>             | <span data-ttu-id="29a12-191">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-191">False</span></span>                             |
| <span data-ttu-id="29a12-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="29a12-192">In Global Catalog</span></span>      | <span data-ttu-id="29a12-193">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-193">False</span></span>                             |
| <span data-ttu-id="29a12-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="29a12-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="29a12-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="29a12-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="29a12-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29a12-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="29a12-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29a12-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="29a12-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29a12-198">Search-Flags</span></span>           | <span data-ttu-id="29a12-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29a12-199">0x00000000</span></span>                        |
| <span data-ttu-id="29a12-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29a12-200">System-Flags</span></span>           | <span data-ttu-id="29a12-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29a12-201">0x00000010</span></span>                        |
| <span data-ttu-id="29a12-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="29a12-202">Classes used in</span></span>        | [<span data-ttu-id="29a12-203">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="29a12-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="29a12-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29a12-204">Windows Server 2008</span></span>



| <span data-ttu-id="29a12-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="29a12-205">Entry</span></span> | <span data-ttu-id="29a12-206">Valor</span><span class="sxs-lookup"><span data-stu-id="29a12-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="29a12-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="29a12-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="29a12-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29a12-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="29a12-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="29a12-209">System-Only</span></span>            | <span data-ttu-id="29a12-210">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-210">False</span></span>                             |
| <span data-ttu-id="29a12-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="29a12-211">Is-Single-Valued</span></span>       | <span data-ttu-id="29a12-212">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-212">False</span></span>                             |
| <span data-ttu-id="29a12-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="29a12-213">Is Indexed</span></span>             | <span data-ttu-id="29a12-214">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-214">False</span></span>                             |
| <span data-ttu-id="29a12-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="29a12-215">In Global Catalog</span></span>      | <span data-ttu-id="29a12-216">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-216">False</span></span>                             |
| <span data-ttu-id="29a12-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="29a12-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="29a12-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="29a12-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="29a12-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29a12-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="29a12-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29a12-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="29a12-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29a12-221">Search-Flags</span></span>           | <span data-ttu-id="29a12-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29a12-222">0x00000000</span></span>                        |
| <span data-ttu-id="29a12-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29a12-223">System-Flags</span></span>           | <span data-ttu-id="29a12-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29a12-224">0x00000010</span></span>                        |
| <span data-ttu-id="29a12-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="29a12-225">Classes used in</span></span>        | [<span data-ttu-id="29a12-226">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="29a12-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="29a12-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="29a12-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="29a12-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="29a12-228">Entry</span></span> | <span data-ttu-id="29a12-229">Valor</span><span class="sxs-lookup"><span data-stu-id="29a12-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="29a12-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="29a12-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="29a12-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29a12-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="29a12-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="29a12-232">System-Only</span></span>            | <span data-ttu-id="29a12-233">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-233">False</span></span>                             |
| <span data-ttu-id="29a12-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="29a12-234">Is-Single-Valued</span></span>       | <span data-ttu-id="29a12-235">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-235">False</span></span>                             |
| <span data-ttu-id="29a12-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="29a12-236">Is Indexed</span></span>             | <span data-ttu-id="29a12-237">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-237">False</span></span>                             |
| <span data-ttu-id="29a12-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="29a12-238">In Global Catalog</span></span>      | <span data-ttu-id="29a12-239">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-239">False</span></span>                             |
| <span data-ttu-id="29a12-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="29a12-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="29a12-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="29a12-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="29a12-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29a12-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="29a12-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29a12-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="29a12-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29a12-244">Search-Flags</span></span>           | <span data-ttu-id="29a12-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29a12-245">0x00000000</span></span>                        |
| <span data-ttu-id="29a12-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29a12-246">System-Flags</span></span>           | <span data-ttu-id="29a12-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29a12-247">0x00000010</span></span>                        |
| <span data-ttu-id="29a12-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="29a12-248">Classes used in</span></span>        | [<span data-ttu-id="29a12-249">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="29a12-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="29a12-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29a12-250">Windows Server 2012</span></span>



| <span data-ttu-id="29a12-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="29a12-251">Entry</span></span> | <span data-ttu-id="29a12-252">Valor</span><span class="sxs-lookup"><span data-stu-id="29a12-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="29a12-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="29a12-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="29a12-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29a12-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="29a12-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="29a12-255">System-Only</span></span>            | <span data-ttu-id="29a12-256">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-256">False</span></span>                             |
| <span data-ttu-id="29a12-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="29a12-257">Is-Single-Valued</span></span>       | <span data-ttu-id="29a12-258">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-258">False</span></span>                             |
| <span data-ttu-id="29a12-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="29a12-259">Is Indexed</span></span>             | <span data-ttu-id="29a12-260">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-260">False</span></span>                             |
| <span data-ttu-id="29a12-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="29a12-261">In Global Catalog</span></span>      | <span data-ttu-id="29a12-262">Falso</span><span class="sxs-lookup"><span data-stu-id="29a12-262">False</span></span>                             |
| <span data-ttu-id="29a12-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="29a12-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="29a12-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="29a12-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="29a12-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29a12-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="29a12-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29a12-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="29a12-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29a12-267">Search-Flags</span></span>           | <span data-ttu-id="29a12-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29a12-268">0x00000000</span></span>                        |
| <span data-ttu-id="29a12-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29a12-269">System-Flags</span></span>           | <span data-ttu-id="29a12-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29a12-270">0x00000010</span></span>                        |
| <span data-ttu-id="29a12-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="29a12-271">Classes used in</span></span>        | [<span data-ttu-id="29a12-272">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="29a12-272">**User**</span></span>](c-user.md)<br/> |



 

 





