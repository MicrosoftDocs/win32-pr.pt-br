---
title: Home-Directory atributo
description: O diretório base da conta.
ms.assetid: 7fd431f2-f2e0-476f-82ed-04f776c234eb
ms.tgt_platform: multiple
keywords:
- Esquema de Home-Directory do atributo AD
- Esquema de AD do atributo homeDirectory
topic_type:
- apiref
api_name:
- Home-Directory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 070285336284e6d07b6333d28eff5c85c4dc6c5a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645487"
---
# <a name="home-directory-attribute"></a><span data-ttu-id="046fc-105">Home-Directory atributo</span><span class="sxs-lookup"><span data-stu-id="046fc-105">Home-Directory attribute</span></span>

<span data-ttu-id="046fc-106">O diretório base da conta.</span><span class="sxs-lookup"><span data-stu-id="046fc-106">The home directory for the account.</span></span> <span data-ttu-id="046fc-107">Se [**homeDrive**](a-homedrive.md) for definido e especificar uma letra de unidade, **HomeDirectory** deverá ser um caminho UNC.</span><span class="sxs-lookup"><span data-stu-id="046fc-107">If [**homeDrive**](a-homedrive.md) is set and specifies a drive letter, **homeDirectory** must be a UNC path.</span></span> <span data-ttu-id="046fc-108">Caso contrário, **HomeDirectory** é um caminho local totalmente qualificado, incluindo a letra da unidade (por exemplo, \*DriveLetter ***: \\** pasta _do diretório_* _\\_ \* ).</span><span class="sxs-lookup"><span data-stu-id="046fc-108">Otherwise, **homeDirectory** is a fully qualified local path including the drive letter (for example, *DriveLetter\***:\\**_Directory_*_\\_\*_Folder_).</span></span> <span data-ttu-id="046fc-109">Esse valor pode ser uma cadeia de caracteres nula.</span><span class="sxs-lookup"><span data-stu-id="046fc-109">This value can be a null string.</span></span>



| <span data-ttu-id="046fc-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="046fc-110">Entry</span></span> | <span data-ttu-id="046fc-111">Valor</span><span class="sxs-lookup"><span data-stu-id="046fc-111">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="046fc-112">CN</span><span class="sxs-lookup"><span data-stu-id="046fc-112">CN</span></span>                | <span data-ttu-id="046fc-113">Home-Directory</span><span class="sxs-lookup"><span data-stu-id="046fc-113">Home-Directory</span></span>                                                                     |
| <span data-ttu-id="046fc-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="046fc-114">Ldap-Display-Name</span></span> | <span data-ttu-id="046fc-115">homeDirectory</span><span class="sxs-lookup"><span data-stu-id="046fc-115">homeDirectory</span></span>                                                                      |
| <span data-ttu-id="046fc-116">Tamanho</span><span class="sxs-lookup"><span data-stu-id="046fc-116">Size</span></span>              | \-                                                                                 |
| <span data-ttu-id="046fc-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="046fc-117">Update Privilege</span></span>  | <span data-ttu-id="046fc-118">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="046fc-118">Domain administrator</span></span>                                                               |
| <span data-ttu-id="046fc-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="046fc-119">Update Frequency</span></span>  | <span data-ttu-id="046fc-120">Quando o registro do usuário é criado e sempre que o diretório base precisa ser alterado.</span><span class="sxs-lookup"><span data-stu-id="046fc-120">When the user's record is created and whenever the home directory needs to change.</span></span> |
| <span data-ttu-id="046fc-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="046fc-121">Attribute-Id</span></span>      | <span data-ttu-id="046fc-122">1.2.840.113556.1.4.44</span><span class="sxs-lookup"><span data-stu-id="046fc-122">1.2.840.113556.1.4.44</span></span>                                                              |
| <span data-ttu-id="046fc-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="046fc-123">System-Id-Guid</span></span>    | <span data-ttu-id="046fc-124">bf967985-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="046fc-124">bf967985-0de6-11d0-a285-00aa003049e2</span></span>                                               |
| <span data-ttu-id="046fc-125">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="046fc-125">Syntax</span></span>            | [<span data-ttu-id="046fc-126">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="046fc-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                        |



## <a name="implementations"></a><span data-ttu-id="046fc-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="046fc-127">Implementations</span></span>

-   [<span data-ttu-id="046fc-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="046fc-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="046fc-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="046fc-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="046fc-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="046fc-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="046fc-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="046fc-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="046fc-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="046fc-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="046fc-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="046fc-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="046fc-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="046fc-134">Windows 2000 Server</span></span>



| <span data-ttu-id="046fc-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="046fc-135">Entry</span></span> | <span data-ttu-id="046fc-136">Valor</span><span class="sxs-lookup"><span data-stu-id="046fc-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="046fc-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="046fc-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="046fc-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="046fc-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="046fc-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="046fc-139">System-Only</span></span>            | <span data-ttu-id="046fc-140">Falso</span><span class="sxs-lookup"><span data-stu-id="046fc-140">False</span></span>                             |
| <span data-ttu-id="046fc-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="046fc-141">Is-Single-Valued</span></span>       | <span data-ttu-id="046fc-142">True</span><span class="sxs-lookup"><span data-stu-id="046fc-142">True</span></span>                              |
| <span data-ttu-id="046fc-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="046fc-143">Is Indexed</span></span>             | <span data-ttu-id="046fc-144">Falso</span><span class="sxs-lookup"><span data-stu-id="046fc-144">False</span></span>                             |
| <span data-ttu-id="046fc-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="046fc-145">In Global Catalog</span></span>      | <span data-ttu-id="046fc-146">Falso</span><span class="sxs-lookup"><span data-stu-id="046fc-146">False</span></span>                             |
| <span data-ttu-id="046fc-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="046fc-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="046fc-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="046fc-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="046fc-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="046fc-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="046fc-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="046fc-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="046fc-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="046fc-151">Search-Flags</span></span>           | <span data-ttu-id="046fc-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="046fc-152">0x00000010</span></span>                        |
| <span data-ttu-id="046fc-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="046fc-153">System-Flags</span></span>           | <span data-ttu-id="046fc-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="046fc-154">0x00000010</span></span>                        |
| <span data-ttu-id="046fc-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="046fc-155">Classes used in</span></span>        | [<span data-ttu-id="046fc-156">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="046fc-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="046fc-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="046fc-157">Windows Server 2003</span></span>



| <span data-ttu-id="046fc-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="046fc-158">Entry</span></span> | <span data-ttu-id="046fc-159">Valor</span><span class="sxs-lookup"><span data-stu-id="046fc-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="046fc-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="046fc-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="046fc-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="046fc-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="046fc-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="046fc-162">System-Only</span></span>            | <span data-ttu-id="046fc-163">Falso</span><span class="sxs-lookup"><span data-stu-id="046fc-163">False</span></span>                             |
| <span data-ttu-id="046fc-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="046fc-164">Is-Single-Valued</span></span>       | <span data-ttu-id="046fc-165">True</span><span class="sxs-lookup"><span data-stu-id="046fc-165">True</span></span>                              |
| <span data-ttu-id="046fc-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="046fc-166">Is Indexed</span></span>             | <span data-ttu-id="046fc-167">Falso</span><span class="sxs-lookup"><span data-stu-id="046fc-167">False</span></span>                             |
| <span data-ttu-id="046fc-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="046fc-168">In Global Catalog</span></span>      | <span data-ttu-id="046fc-169">Falso</span><span class="sxs-lookup"><span data-stu-id="046fc-169">False</span></span>                             |
| <span data-ttu-id="046fc-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="046fc-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="046fc-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="046fc-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="046fc-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="046fc-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="046fc-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="046fc-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="046fc-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="046fc-174">Search-Flags</span></span>           | <span data-ttu-id="046fc-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="046fc-175">0x00000010</span></span>                        |
| <span data-ttu-id="046fc-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="046fc-176">System-Flags</span></span>           | <span data-ttu-id="046fc-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="046fc-177">0x00000010</span></span>                        |
| <span data-ttu-id="046fc-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="046fc-178">Classes used in</span></span>        | [<span data-ttu-id="046fc-179">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="046fc-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="046fc-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="046fc-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="046fc-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="046fc-181">Entry</span></span> | <span data-ttu-id="046fc-182">Valor</span><span class="sxs-lookup"><span data-stu-id="046fc-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="046fc-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="046fc-183">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="046fc-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="046fc-184">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="046fc-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="046fc-185">System-Only</span></span>            | <span data-ttu-id="046fc-186">Falso</span><span class="sxs-lookup"><span data-stu-id="046fc-186">False</span></span>                                                                               |
| <span data-ttu-id="046fc-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="046fc-187">Is-Single-Valued</span></span>       | <span data-ttu-id="046fc-188">True</span><span class="sxs-lookup"><span data-stu-id="046fc-188">True</span></span>                                                                                |
| <span data-ttu-id="046fc-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="046fc-189">Is Indexed</span></span>             | <span data-ttu-id="046fc-190">Falso</span><span class="sxs-lookup"><span data-stu-id="046fc-190">False</span></span>                                                                               |
| <span data-ttu-id="046fc-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="046fc-191">In Global Catalog</span></span>      | <span data-ttu-id="046fc-192">Falso</span><span class="sxs-lookup"><span data-stu-id="046fc-192">False</span></span>                                                                               |
| <span data-ttu-id="046fc-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="046fc-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="046fc-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="046fc-194">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="046fc-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="046fc-195">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="046fc-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="046fc-196">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="046fc-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="046fc-197">Search-Flags</span></span>           | <span data-ttu-id="046fc-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="046fc-198">0x00000010</span></span>                                                                          |
| <span data-ttu-id="046fc-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="046fc-199">System-Flags</span></span>           | <span data-ttu-id="046fc-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="046fc-200">0x00000010</span></span>                                                                          |
| <span data-ttu-id="046fc-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="046fc-201">Classes used in</span></span>        | [<span data-ttu-id="046fc-202">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="046fc-202">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="046fc-203">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="046fc-203">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="046fc-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="046fc-204">Windows Server 2008</span></span>



| <span data-ttu-id="046fc-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="046fc-205">Entry</span></span> | <span data-ttu-id="046fc-206">Valor</span><span class="sxs-lookup"><span data-stu-id="046fc-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="046fc-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="046fc-207">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="046fc-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="046fc-208">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="046fc-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="046fc-209">System-Only</span></span>            | <span data-ttu-id="046fc-210">Falso</span><span class="sxs-lookup"><span data-stu-id="046fc-210">False</span></span>                                                                               |
| <span data-ttu-id="046fc-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="046fc-211">Is-Single-Valued</span></span>       | <span data-ttu-id="046fc-212">True</span><span class="sxs-lookup"><span data-stu-id="046fc-212">True</span></span>                                                                                |
| <span data-ttu-id="046fc-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="046fc-213">Is Indexed</span></span>             | <span data-ttu-id="046fc-214">Falso</span><span class="sxs-lookup"><span data-stu-id="046fc-214">False</span></span>                                                                               |
| <span data-ttu-id="046fc-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="046fc-215">In Global Catalog</span></span>      | <span data-ttu-id="046fc-216">Falso</span><span class="sxs-lookup"><span data-stu-id="046fc-216">False</span></span>                                                                               |
| <span data-ttu-id="046fc-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="046fc-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="046fc-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="046fc-218">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="046fc-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="046fc-219">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="046fc-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="046fc-220">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="046fc-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="046fc-221">Search-Flags</span></span>           | <span data-ttu-id="046fc-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="046fc-222">0x00000010</span></span>                                                                          |
| <span data-ttu-id="046fc-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="046fc-223">System-Flags</span></span>           | <span data-ttu-id="046fc-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="046fc-224">0x00000010</span></span>                                                                          |
| <span data-ttu-id="046fc-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="046fc-225">Classes used in</span></span>        | [<span data-ttu-id="046fc-226">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="046fc-226">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="046fc-227">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="046fc-227">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="046fc-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="046fc-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="046fc-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="046fc-229">Entry</span></span> | <span data-ttu-id="046fc-230">Valor</span><span class="sxs-lookup"><span data-stu-id="046fc-230">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="046fc-231">ID do link</span><span class="sxs-lookup"><span data-stu-id="046fc-231">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="046fc-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="046fc-232">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="046fc-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="046fc-233">System-Only</span></span>            | <span data-ttu-id="046fc-234">Falso</span><span class="sxs-lookup"><span data-stu-id="046fc-234">False</span></span>                                                                               |
| <span data-ttu-id="046fc-235">É de valor único</span><span class="sxs-lookup"><span data-stu-id="046fc-235">Is-Single-Valued</span></span>       | <span data-ttu-id="046fc-236">True</span><span class="sxs-lookup"><span data-stu-id="046fc-236">True</span></span>                                                                                |
| <span data-ttu-id="046fc-237">É indexado</span><span class="sxs-lookup"><span data-stu-id="046fc-237">Is Indexed</span></span>             | <span data-ttu-id="046fc-238">Falso</span><span class="sxs-lookup"><span data-stu-id="046fc-238">False</span></span>                                                                               |
| <span data-ttu-id="046fc-239">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="046fc-239">In Global Catalog</span></span>      | <span data-ttu-id="046fc-240">Falso</span><span class="sxs-lookup"><span data-stu-id="046fc-240">False</span></span>                                                                               |
| <span data-ttu-id="046fc-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="046fc-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="046fc-242">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="046fc-242">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="046fc-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="046fc-243">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="046fc-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="046fc-244">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="046fc-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="046fc-245">Search-Flags</span></span>           | <span data-ttu-id="046fc-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="046fc-246">0x00000010</span></span>                                                                          |
| <span data-ttu-id="046fc-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="046fc-247">System-Flags</span></span>           | <span data-ttu-id="046fc-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="046fc-248">0x00000010</span></span>                                                                          |
| <span data-ttu-id="046fc-249">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="046fc-249">Classes used in</span></span>        | [<span data-ttu-id="046fc-250">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="046fc-250">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="046fc-251">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="046fc-251">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="046fc-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="046fc-252">Windows Server 2012</span></span>



| <span data-ttu-id="046fc-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="046fc-253">Entry</span></span> | <span data-ttu-id="046fc-254">Valor</span><span class="sxs-lookup"><span data-stu-id="046fc-254">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="046fc-255">ID do link</span><span class="sxs-lookup"><span data-stu-id="046fc-255">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="046fc-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="046fc-256">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="046fc-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="046fc-257">System-Only</span></span>            | <span data-ttu-id="046fc-258">Falso</span><span class="sxs-lookup"><span data-stu-id="046fc-258">False</span></span>                                                                               |
| <span data-ttu-id="046fc-259">É de valor único</span><span class="sxs-lookup"><span data-stu-id="046fc-259">Is-Single-Valued</span></span>       | <span data-ttu-id="046fc-260">True</span><span class="sxs-lookup"><span data-stu-id="046fc-260">True</span></span>                                                                                |
| <span data-ttu-id="046fc-261">É indexado</span><span class="sxs-lookup"><span data-stu-id="046fc-261">Is Indexed</span></span>             | <span data-ttu-id="046fc-262">Falso</span><span class="sxs-lookup"><span data-stu-id="046fc-262">False</span></span>                                                                               |
| <span data-ttu-id="046fc-263">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="046fc-263">In Global Catalog</span></span>      | <span data-ttu-id="046fc-264">Falso</span><span class="sxs-lookup"><span data-stu-id="046fc-264">False</span></span>                                                                               |
| <span data-ttu-id="046fc-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="046fc-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="046fc-266">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="046fc-266">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="046fc-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="046fc-267">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="046fc-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="046fc-268">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="046fc-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="046fc-269">Search-Flags</span></span>           | <span data-ttu-id="046fc-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="046fc-270">0x00000010</span></span>                                                                          |
| <span data-ttu-id="046fc-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="046fc-271">System-Flags</span></span>           | <span data-ttu-id="046fc-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="046fc-272">0x00000010</span></span>                                                                          |
| <span data-ttu-id="046fc-273">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="046fc-273">Classes used in</span></span>        | [<span data-ttu-id="046fc-274">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="046fc-274">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="046fc-275">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="046fc-275">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="046fc-276">Confira também</span><span class="sxs-lookup"><span data-stu-id="046fc-276">See also</span></span>

<dl> <dt>

[<span data-ttu-id="046fc-277">**homeDrive**</span><span class="sxs-lookup"><span data-stu-id="046fc-277">**homeDrive**</span></span>](a-homedrive.md)
</dt> </dl>

 

 





