---
title: Atributo usuário-compartilhado-pasta
description: Especifica um caminho UNC para a pasta de documentos compartilhados do usuário. O caminho deve ser um caminho UNC de rede do diretório de compartilhamento do servidor de formulário \\ \\ \\ \\ . Esse valor pode ser uma cadeia de caracteres nula.
ms.assetid: 23b4177a-0a05-4111-affe-d81bc115580d
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo de pasta compartilhada do usuário
- Esquema de AD do atributo userSharedFolder
topic_type:
- apiref
api_name:
- User-Shared-Folder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a20e9772302e79837fccd301943554191cf3b862
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919546"
---
# <a name="user-shared-folder-attribute"></a><span data-ttu-id="2695c-107">Atributo usuário-compartilhado-pasta</span><span class="sxs-lookup"><span data-stu-id="2695c-107">User-Shared-Folder attribute</span></span>

<span data-ttu-id="2695c-108">Especifica um caminho UNC para a pasta de documentos compartilhados do usuário.</span><span class="sxs-lookup"><span data-stu-id="2695c-108">Specifies a UNC path to the user's shared documents folder.</span></span> <span data-ttu-id="2695c-109">O caminho deve ser um caminho UNC de rede do **\\\\** diretório de compartilhamento do _servidor_ de formulário *_\\_*  *_\\_* .</span><span class="sxs-lookup"><span data-stu-id="2695c-109">The path must be a network UNC path of the form **\\\\**_Server_*_\\_*_Share_*_\\_*_Directory_.</span></span> <span data-ttu-id="2695c-110">Esse valor pode ser uma cadeia de caracteres nula.</span><span class="sxs-lookup"><span data-stu-id="2695c-110">This value can be a null string.</span></span>



| <span data-ttu-id="2695c-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="2695c-111">Entry</span></span> | <span data-ttu-id="2695c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="2695c-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2695c-113">CN</span><span class="sxs-lookup"><span data-stu-id="2695c-113">CN</span></span>                | <span data-ttu-id="2695c-114">Pasta compartilhada pelo usuário</span><span class="sxs-lookup"><span data-stu-id="2695c-114">User-Shared-Folder</span></span>                                                                |
| <span data-ttu-id="2695c-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2695c-115">Ldap-Display-Name</span></span> | <span data-ttu-id="2695c-116">userSharedFolder</span><span class="sxs-lookup"><span data-stu-id="2695c-116">userSharedFolder</span></span>                                                                  |
| <span data-ttu-id="2695c-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="2695c-117">Size</span></span>              | \-                                                                                |
| <span data-ttu-id="2695c-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="2695c-118">Update Privilege</span></span>  | <span data-ttu-id="2695c-119">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="2695c-119">Domain administrator or account owner.</span></span>                                            |
| <span data-ttu-id="2695c-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="2695c-120">Update Frequency</span></span>  | <span data-ttu-id="2695c-121">Quando o registro do usuário é criado e sempre que a pasta compartilhada precisa ser alterada.</span><span class="sxs-lookup"><span data-stu-id="2695c-121">When the user's record is created and whenever the shared folder needs to change.</span></span> |
| <span data-ttu-id="2695c-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2695c-122">Attribute-Id</span></span>      | <span data-ttu-id="2695c-123">1.2.840.113556.1.4.751</span><span class="sxs-lookup"><span data-stu-id="2695c-123">1.2.840.113556.1.4.751</span></span>                                                            |
| <span data-ttu-id="2695c-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2695c-124">System-Id-Guid</span></span>    | <span data-ttu-id="2695c-125">9a9a021f-4a5b-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="2695c-125">9a9a021f-4a5b-11d1-a9c3-0000f80367c1</span></span>                                              |
| <span data-ttu-id="2695c-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="2695c-126">Syntax</span></span>            | [<span data-ttu-id="2695c-127">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="2695c-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="2695c-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="2695c-128">Implementations</span></span>

-   [<span data-ttu-id="2695c-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2695c-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2695c-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2695c-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2695c-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2695c-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2695c-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2695c-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2695c-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2695c-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2695c-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2695c-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2695c-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2695c-135">Windows 2000 Server</span></span>



| <span data-ttu-id="2695c-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="2695c-136">Entry</span></span> | <span data-ttu-id="2695c-137">Valor</span><span class="sxs-lookup"><span data-stu-id="2695c-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2695c-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="2695c-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2695c-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2695c-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2695c-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="2695c-140">System-Only</span></span>            | <span data-ttu-id="2695c-141">Falso</span><span class="sxs-lookup"><span data-stu-id="2695c-141">False</span></span>                             |
| <span data-ttu-id="2695c-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2695c-142">Is-Single-Valued</span></span>       | <span data-ttu-id="2695c-143">True</span><span class="sxs-lookup"><span data-stu-id="2695c-143">True</span></span>                              |
| <span data-ttu-id="2695c-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="2695c-144">Is Indexed</span></span>             | <span data-ttu-id="2695c-145">Falso</span><span class="sxs-lookup"><span data-stu-id="2695c-145">False</span></span>                             |
| <span data-ttu-id="2695c-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2695c-146">In Global Catalog</span></span>      | <span data-ttu-id="2695c-147">Falso</span><span class="sxs-lookup"><span data-stu-id="2695c-147">False</span></span>                             |
| <span data-ttu-id="2695c-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2695c-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="2695c-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2695c-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2695c-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2695c-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2695c-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2695c-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2695c-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2695c-152">Search-Flags</span></span>           | <span data-ttu-id="2695c-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2695c-153">0x00000000</span></span>                        |
| <span data-ttu-id="2695c-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2695c-154">System-Flags</span></span>           | <span data-ttu-id="2695c-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2695c-155">0x00000010</span></span>                        |
| <span data-ttu-id="2695c-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2695c-156">Classes used in</span></span>        | [<span data-ttu-id="2695c-157">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="2695c-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2695c-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2695c-158">Windows Server 2003</span></span>



| <span data-ttu-id="2695c-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="2695c-159">Entry</span></span> | <span data-ttu-id="2695c-160">Valor</span><span class="sxs-lookup"><span data-stu-id="2695c-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2695c-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="2695c-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2695c-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2695c-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2695c-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="2695c-163">System-Only</span></span>            | <span data-ttu-id="2695c-164">Falso</span><span class="sxs-lookup"><span data-stu-id="2695c-164">False</span></span>                             |
| <span data-ttu-id="2695c-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2695c-165">Is-Single-Valued</span></span>       | <span data-ttu-id="2695c-166">True</span><span class="sxs-lookup"><span data-stu-id="2695c-166">True</span></span>                              |
| <span data-ttu-id="2695c-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="2695c-167">Is Indexed</span></span>             | <span data-ttu-id="2695c-168">Falso</span><span class="sxs-lookup"><span data-stu-id="2695c-168">False</span></span>                             |
| <span data-ttu-id="2695c-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2695c-169">In Global Catalog</span></span>      | <span data-ttu-id="2695c-170">Falso</span><span class="sxs-lookup"><span data-stu-id="2695c-170">False</span></span>                             |
| <span data-ttu-id="2695c-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2695c-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="2695c-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2695c-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2695c-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2695c-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2695c-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2695c-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2695c-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2695c-175">Search-Flags</span></span>           | <span data-ttu-id="2695c-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2695c-176">0x00000000</span></span>                        |
| <span data-ttu-id="2695c-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2695c-177">System-Flags</span></span>           | <span data-ttu-id="2695c-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2695c-178">0x00000010</span></span>                        |
| <span data-ttu-id="2695c-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2695c-179">Classes used in</span></span>        | [<span data-ttu-id="2695c-180">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="2695c-180">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2695c-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2695c-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2695c-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="2695c-182">Entry</span></span> | <span data-ttu-id="2695c-183">Valor</span><span class="sxs-lookup"><span data-stu-id="2695c-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2695c-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="2695c-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2695c-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2695c-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2695c-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="2695c-186">System-Only</span></span>            | <span data-ttu-id="2695c-187">Falso</span><span class="sxs-lookup"><span data-stu-id="2695c-187">False</span></span>                             |
| <span data-ttu-id="2695c-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2695c-188">Is-Single-Valued</span></span>       | <span data-ttu-id="2695c-189">True</span><span class="sxs-lookup"><span data-stu-id="2695c-189">True</span></span>                              |
| <span data-ttu-id="2695c-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="2695c-190">Is Indexed</span></span>             | <span data-ttu-id="2695c-191">Falso</span><span class="sxs-lookup"><span data-stu-id="2695c-191">False</span></span>                             |
| <span data-ttu-id="2695c-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2695c-192">In Global Catalog</span></span>      | <span data-ttu-id="2695c-193">Falso</span><span class="sxs-lookup"><span data-stu-id="2695c-193">False</span></span>                             |
| <span data-ttu-id="2695c-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2695c-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="2695c-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2695c-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2695c-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2695c-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2695c-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2695c-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2695c-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2695c-198">Search-Flags</span></span>           | <span data-ttu-id="2695c-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2695c-199">0x00000000</span></span>                        |
| <span data-ttu-id="2695c-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2695c-200">System-Flags</span></span>           | <span data-ttu-id="2695c-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2695c-201">0x00000010</span></span>                        |
| <span data-ttu-id="2695c-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2695c-202">Classes used in</span></span>        | [<span data-ttu-id="2695c-203">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="2695c-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2695c-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2695c-204">Windows Server 2008</span></span>



| <span data-ttu-id="2695c-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="2695c-205">Entry</span></span> | <span data-ttu-id="2695c-206">Valor</span><span class="sxs-lookup"><span data-stu-id="2695c-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2695c-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="2695c-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2695c-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2695c-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2695c-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="2695c-209">System-Only</span></span>            | <span data-ttu-id="2695c-210">Falso</span><span class="sxs-lookup"><span data-stu-id="2695c-210">False</span></span>                             |
| <span data-ttu-id="2695c-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2695c-211">Is-Single-Valued</span></span>       | <span data-ttu-id="2695c-212">True</span><span class="sxs-lookup"><span data-stu-id="2695c-212">True</span></span>                              |
| <span data-ttu-id="2695c-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="2695c-213">Is Indexed</span></span>             | <span data-ttu-id="2695c-214">Falso</span><span class="sxs-lookup"><span data-stu-id="2695c-214">False</span></span>                             |
| <span data-ttu-id="2695c-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2695c-215">In Global Catalog</span></span>      | <span data-ttu-id="2695c-216">Falso</span><span class="sxs-lookup"><span data-stu-id="2695c-216">False</span></span>                             |
| <span data-ttu-id="2695c-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2695c-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="2695c-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2695c-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2695c-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2695c-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2695c-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2695c-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2695c-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2695c-221">Search-Flags</span></span>           | <span data-ttu-id="2695c-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2695c-222">0x00000000</span></span>                        |
| <span data-ttu-id="2695c-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2695c-223">System-Flags</span></span>           | <span data-ttu-id="2695c-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2695c-224">0x00000010</span></span>                        |
| <span data-ttu-id="2695c-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2695c-225">Classes used in</span></span>        | [<span data-ttu-id="2695c-226">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="2695c-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2695c-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2695c-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2695c-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="2695c-228">Entry</span></span> | <span data-ttu-id="2695c-229">Valor</span><span class="sxs-lookup"><span data-stu-id="2695c-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2695c-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="2695c-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2695c-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2695c-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2695c-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="2695c-232">System-Only</span></span>            | <span data-ttu-id="2695c-233">Falso</span><span class="sxs-lookup"><span data-stu-id="2695c-233">False</span></span>                             |
| <span data-ttu-id="2695c-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2695c-234">Is-Single-Valued</span></span>       | <span data-ttu-id="2695c-235">True</span><span class="sxs-lookup"><span data-stu-id="2695c-235">True</span></span>                              |
| <span data-ttu-id="2695c-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="2695c-236">Is Indexed</span></span>             | <span data-ttu-id="2695c-237">Falso</span><span class="sxs-lookup"><span data-stu-id="2695c-237">False</span></span>                             |
| <span data-ttu-id="2695c-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2695c-238">In Global Catalog</span></span>      | <span data-ttu-id="2695c-239">Falso</span><span class="sxs-lookup"><span data-stu-id="2695c-239">False</span></span>                             |
| <span data-ttu-id="2695c-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2695c-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="2695c-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2695c-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2695c-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2695c-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2695c-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2695c-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2695c-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2695c-244">Search-Flags</span></span>           | <span data-ttu-id="2695c-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2695c-245">0x00000000</span></span>                        |
| <span data-ttu-id="2695c-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2695c-246">System-Flags</span></span>           | <span data-ttu-id="2695c-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2695c-247">0x00000010</span></span>                        |
| <span data-ttu-id="2695c-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2695c-248">Classes used in</span></span>        | [<span data-ttu-id="2695c-249">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="2695c-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2695c-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2695c-250">Windows Server 2012</span></span>



| <span data-ttu-id="2695c-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="2695c-251">Entry</span></span> | <span data-ttu-id="2695c-252">Valor</span><span class="sxs-lookup"><span data-stu-id="2695c-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2695c-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="2695c-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2695c-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2695c-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2695c-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="2695c-255">System-Only</span></span>            | <span data-ttu-id="2695c-256">Falso</span><span class="sxs-lookup"><span data-stu-id="2695c-256">False</span></span>                             |
| <span data-ttu-id="2695c-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2695c-257">Is-Single-Valued</span></span>       | <span data-ttu-id="2695c-258">True</span><span class="sxs-lookup"><span data-stu-id="2695c-258">True</span></span>                              |
| <span data-ttu-id="2695c-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="2695c-259">Is Indexed</span></span>             | <span data-ttu-id="2695c-260">Falso</span><span class="sxs-lookup"><span data-stu-id="2695c-260">False</span></span>                             |
| <span data-ttu-id="2695c-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2695c-261">In Global Catalog</span></span>      | <span data-ttu-id="2695c-262">Falso</span><span class="sxs-lookup"><span data-stu-id="2695c-262">False</span></span>                             |
| <span data-ttu-id="2695c-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2695c-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="2695c-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2695c-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2695c-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2695c-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2695c-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2695c-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2695c-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2695c-267">Search-Flags</span></span>           | <span data-ttu-id="2695c-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2695c-268">0x00000000</span></span>                        |
| <span data-ttu-id="2695c-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2695c-269">System-Flags</span></span>           | <span data-ttu-id="2695c-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2695c-270">0x00000010</span></span>                        |
| <span data-ttu-id="2695c-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2695c-271">Classes used in</span></span>        | [<span data-ttu-id="2695c-272">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="2695c-272">**User**</span></span>](c-user.md)<br/> |



 

 





