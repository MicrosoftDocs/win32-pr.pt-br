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
# <a name="home-directory-attribute"></a><span data-ttu-id="841f0-105">Home-Directory atributo</span><span class="sxs-lookup"><span data-stu-id="841f0-105">Home-Directory attribute</span></span>

<span data-ttu-id="841f0-106">O diretório base da conta.</span><span class="sxs-lookup"><span data-stu-id="841f0-106">The home directory for the account.</span></span> <span data-ttu-id="841f0-107">Se [**homeDrive**](a-homedrive.md) for definido e especificar uma letra de unidade, **HomeDirectory** deverá ser um caminho UNC.</span><span class="sxs-lookup"><span data-stu-id="841f0-107">If [**homeDrive**](a-homedrive.md) is set and specifies a drive letter, **homeDirectory** must be a UNC path.</span></span> <span data-ttu-id="841f0-108">Caso contrário, **HomeDirectory** é um caminho local totalmente qualificado, incluindo a letra da unidade (por exemplo, \*DriveLetter ***: \\** pasta _do diretório_* _\\_ \* ).</span><span class="sxs-lookup"><span data-stu-id="841f0-108">Otherwise, **homeDirectory** is a fully qualified local path including the drive letter (for example, *DriveLetter\***:\\**_Directory_*_\\_\*_Folder_).</span></span> <span data-ttu-id="841f0-109">Esse valor pode ser uma cadeia de caracteres nula.</span><span class="sxs-lookup"><span data-stu-id="841f0-109">This value can be a null string.</span></span>



| <span data-ttu-id="841f0-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="841f0-110">Entry</span></span> | <span data-ttu-id="841f0-111">Valor</span><span class="sxs-lookup"><span data-stu-id="841f0-111">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="841f0-112">CN</span><span class="sxs-lookup"><span data-stu-id="841f0-112">CN</span></span>                | <span data-ttu-id="841f0-113">Home-Directory</span><span class="sxs-lookup"><span data-stu-id="841f0-113">Home-Directory</span></span>                                                                     |
| <span data-ttu-id="841f0-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="841f0-114">Ldap-Display-Name</span></span> | <span data-ttu-id="841f0-115">homeDirectory</span><span class="sxs-lookup"><span data-stu-id="841f0-115">homeDirectory</span></span>                                                                      |
| <span data-ttu-id="841f0-116">Tamanho</span><span class="sxs-lookup"><span data-stu-id="841f0-116">Size</span></span>              | \-                                                                                 |
| <span data-ttu-id="841f0-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="841f0-117">Update Privilege</span></span>  | <span data-ttu-id="841f0-118">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="841f0-118">Domain administrator</span></span>                                                               |
| <span data-ttu-id="841f0-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="841f0-119">Update Frequency</span></span>  | <span data-ttu-id="841f0-120">Quando o registro do usuário é criado e sempre que o diretório base precisa ser alterado.</span><span class="sxs-lookup"><span data-stu-id="841f0-120">When the user's record is created and whenever the home directory needs to change.</span></span> |
| <span data-ttu-id="841f0-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="841f0-121">Attribute-Id</span></span>      | <span data-ttu-id="841f0-122">1.2.840.113556.1.4.44</span><span class="sxs-lookup"><span data-stu-id="841f0-122">1.2.840.113556.1.4.44</span></span>                                                              |
| <span data-ttu-id="841f0-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="841f0-123">System-Id-Guid</span></span>    | <span data-ttu-id="841f0-124">bf967985-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="841f0-124">bf967985-0de6-11d0-a285-00aa003049e2</span></span>                                               |
| <span data-ttu-id="841f0-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="841f0-125">Syntax</span></span>            | [<span data-ttu-id="841f0-126">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="841f0-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                        |



## <a name="implementations"></a><span data-ttu-id="841f0-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="841f0-127">Implementations</span></span>

-   [<span data-ttu-id="841f0-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="841f0-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="841f0-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="841f0-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="841f0-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="841f0-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="841f0-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="841f0-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="841f0-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="841f0-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="841f0-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="841f0-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="841f0-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="841f0-134">Windows 2000 Server</span></span>



| <span data-ttu-id="841f0-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="841f0-135">Entry</span></span> | <span data-ttu-id="841f0-136">Valor</span><span class="sxs-lookup"><span data-stu-id="841f0-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="841f0-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="841f0-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="841f0-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="841f0-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="841f0-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="841f0-139">System-Only</span></span>            | <span data-ttu-id="841f0-140">Falso</span><span class="sxs-lookup"><span data-stu-id="841f0-140">False</span></span>                             |
| <span data-ttu-id="841f0-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="841f0-141">Is-Single-Valued</span></span>       | <span data-ttu-id="841f0-142">True</span><span class="sxs-lookup"><span data-stu-id="841f0-142">True</span></span>                              |
| <span data-ttu-id="841f0-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="841f0-143">Is Indexed</span></span>             | <span data-ttu-id="841f0-144">Falso</span><span class="sxs-lookup"><span data-stu-id="841f0-144">False</span></span>                             |
| <span data-ttu-id="841f0-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="841f0-145">In Global Catalog</span></span>      | <span data-ttu-id="841f0-146">Falso</span><span class="sxs-lookup"><span data-stu-id="841f0-146">False</span></span>                             |
| <span data-ttu-id="841f0-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="841f0-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="841f0-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="841f0-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="841f0-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="841f0-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="841f0-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="841f0-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="841f0-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="841f0-151">Search-Flags</span></span>           | <span data-ttu-id="841f0-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="841f0-152">0x00000010</span></span>                        |
| <span data-ttu-id="841f0-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="841f0-153">System-Flags</span></span>           | <span data-ttu-id="841f0-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="841f0-154">0x00000010</span></span>                        |
| <span data-ttu-id="841f0-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="841f0-155">Classes used in</span></span>        | [<span data-ttu-id="841f0-156">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="841f0-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="841f0-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="841f0-157">Windows Server 2003</span></span>



| <span data-ttu-id="841f0-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="841f0-158">Entry</span></span> | <span data-ttu-id="841f0-159">Valor</span><span class="sxs-lookup"><span data-stu-id="841f0-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="841f0-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="841f0-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="841f0-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="841f0-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="841f0-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="841f0-162">System-Only</span></span>            | <span data-ttu-id="841f0-163">Falso</span><span class="sxs-lookup"><span data-stu-id="841f0-163">False</span></span>                             |
| <span data-ttu-id="841f0-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="841f0-164">Is-Single-Valued</span></span>       | <span data-ttu-id="841f0-165">True</span><span class="sxs-lookup"><span data-stu-id="841f0-165">True</span></span>                              |
| <span data-ttu-id="841f0-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="841f0-166">Is Indexed</span></span>             | <span data-ttu-id="841f0-167">Falso</span><span class="sxs-lookup"><span data-stu-id="841f0-167">False</span></span>                             |
| <span data-ttu-id="841f0-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="841f0-168">In Global Catalog</span></span>      | <span data-ttu-id="841f0-169">Falso</span><span class="sxs-lookup"><span data-stu-id="841f0-169">False</span></span>                             |
| <span data-ttu-id="841f0-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="841f0-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="841f0-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="841f0-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="841f0-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="841f0-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="841f0-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="841f0-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="841f0-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="841f0-174">Search-Flags</span></span>           | <span data-ttu-id="841f0-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="841f0-175">0x00000010</span></span>                        |
| <span data-ttu-id="841f0-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="841f0-176">System-Flags</span></span>           | <span data-ttu-id="841f0-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="841f0-177">0x00000010</span></span>                        |
| <span data-ttu-id="841f0-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="841f0-178">Classes used in</span></span>        | [<span data-ttu-id="841f0-179">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="841f0-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="841f0-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="841f0-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="841f0-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="841f0-181">Entry</span></span> | <span data-ttu-id="841f0-182">Valor</span><span class="sxs-lookup"><span data-stu-id="841f0-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="841f0-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="841f0-183">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="841f0-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="841f0-184">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="841f0-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="841f0-185">System-Only</span></span>            | <span data-ttu-id="841f0-186">Falso</span><span class="sxs-lookup"><span data-stu-id="841f0-186">False</span></span>                                                                               |
| <span data-ttu-id="841f0-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="841f0-187">Is-Single-Valued</span></span>       | <span data-ttu-id="841f0-188">True</span><span class="sxs-lookup"><span data-stu-id="841f0-188">True</span></span>                                                                                |
| <span data-ttu-id="841f0-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="841f0-189">Is Indexed</span></span>             | <span data-ttu-id="841f0-190">Falso</span><span class="sxs-lookup"><span data-stu-id="841f0-190">False</span></span>                                                                               |
| <span data-ttu-id="841f0-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="841f0-191">In Global Catalog</span></span>      | <span data-ttu-id="841f0-192">Falso</span><span class="sxs-lookup"><span data-stu-id="841f0-192">False</span></span>                                                                               |
| <span data-ttu-id="841f0-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="841f0-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="841f0-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="841f0-194">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="841f0-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="841f0-195">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="841f0-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="841f0-196">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="841f0-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="841f0-197">Search-Flags</span></span>           | <span data-ttu-id="841f0-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="841f0-198">0x00000010</span></span>                                                                          |
| <span data-ttu-id="841f0-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="841f0-199">System-Flags</span></span>           | <span data-ttu-id="841f0-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="841f0-200">0x00000010</span></span>                                                                          |
| <span data-ttu-id="841f0-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="841f0-201">Classes used in</span></span>        | [<span data-ttu-id="841f0-202">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="841f0-202">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="841f0-203">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="841f0-203">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="841f0-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="841f0-204">Windows Server 2008</span></span>



| <span data-ttu-id="841f0-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="841f0-205">Entry</span></span> | <span data-ttu-id="841f0-206">Valor</span><span class="sxs-lookup"><span data-stu-id="841f0-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="841f0-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="841f0-207">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="841f0-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="841f0-208">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="841f0-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="841f0-209">System-Only</span></span>            | <span data-ttu-id="841f0-210">Falso</span><span class="sxs-lookup"><span data-stu-id="841f0-210">False</span></span>                                                                               |
| <span data-ttu-id="841f0-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="841f0-211">Is-Single-Valued</span></span>       | <span data-ttu-id="841f0-212">True</span><span class="sxs-lookup"><span data-stu-id="841f0-212">True</span></span>                                                                                |
| <span data-ttu-id="841f0-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="841f0-213">Is Indexed</span></span>             | <span data-ttu-id="841f0-214">Falso</span><span class="sxs-lookup"><span data-stu-id="841f0-214">False</span></span>                                                                               |
| <span data-ttu-id="841f0-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="841f0-215">In Global Catalog</span></span>      | <span data-ttu-id="841f0-216">Falso</span><span class="sxs-lookup"><span data-stu-id="841f0-216">False</span></span>                                                                               |
| <span data-ttu-id="841f0-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="841f0-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="841f0-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="841f0-218">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="841f0-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="841f0-219">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="841f0-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="841f0-220">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="841f0-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="841f0-221">Search-Flags</span></span>           | <span data-ttu-id="841f0-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="841f0-222">0x00000010</span></span>                                                                          |
| <span data-ttu-id="841f0-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="841f0-223">System-Flags</span></span>           | <span data-ttu-id="841f0-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="841f0-224">0x00000010</span></span>                                                                          |
| <span data-ttu-id="841f0-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="841f0-225">Classes used in</span></span>        | [<span data-ttu-id="841f0-226">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="841f0-226">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="841f0-227">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="841f0-227">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="841f0-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="841f0-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="841f0-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="841f0-229">Entry</span></span> | <span data-ttu-id="841f0-230">Valor</span><span class="sxs-lookup"><span data-stu-id="841f0-230">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="841f0-231">ID do link</span><span class="sxs-lookup"><span data-stu-id="841f0-231">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="841f0-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="841f0-232">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="841f0-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="841f0-233">System-Only</span></span>            | <span data-ttu-id="841f0-234">Falso</span><span class="sxs-lookup"><span data-stu-id="841f0-234">False</span></span>                                                                               |
| <span data-ttu-id="841f0-235">É de valor único</span><span class="sxs-lookup"><span data-stu-id="841f0-235">Is-Single-Valued</span></span>       | <span data-ttu-id="841f0-236">True</span><span class="sxs-lookup"><span data-stu-id="841f0-236">True</span></span>                                                                                |
| <span data-ttu-id="841f0-237">É indexado</span><span class="sxs-lookup"><span data-stu-id="841f0-237">Is Indexed</span></span>             | <span data-ttu-id="841f0-238">Falso</span><span class="sxs-lookup"><span data-stu-id="841f0-238">False</span></span>                                                                               |
| <span data-ttu-id="841f0-239">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="841f0-239">In Global Catalog</span></span>      | <span data-ttu-id="841f0-240">Falso</span><span class="sxs-lookup"><span data-stu-id="841f0-240">False</span></span>                                                                               |
| <span data-ttu-id="841f0-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="841f0-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="841f0-242">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="841f0-242">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="841f0-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="841f0-243">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="841f0-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="841f0-244">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="841f0-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="841f0-245">Search-Flags</span></span>           | <span data-ttu-id="841f0-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="841f0-246">0x00000010</span></span>                                                                          |
| <span data-ttu-id="841f0-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="841f0-247">System-Flags</span></span>           | <span data-ttu-id="841f0-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="841f0-248">0x00000010</span></span>                                                                          |
| <span data-ttu-id="841f0-249">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="841f0-249">Classes used in</span></span>        | [<span data-ttu-id="841f0-250">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="841f0-250">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="841f0-251">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="841f0-251">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="841f0-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="841f0-252">Windows Server 2012</span></span>



| <span data-ttu-id="841f0-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="841f0-253">Entry</span></span> | <span data-ttu-id="841f0-254">Valor</span><span class="sxs-lookup"><span data-stu-id="841f0-254">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="841f0-255">ID do link</span><span class="sxs-lookup"><span data-stu-id="841f0-255">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="841f0-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="841f0-256">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="841f0-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="841f0-257">System-Only</span></span>            | <span data-ttu-id="841f0-258">Falso</span><span class="sxs-lookup"><span data-stu-id="841f0-258">False</span></span>                                                                               |
| <span data-ttu-id="841f0-259">É de valor único</span><span class="sxs-lookup"><span data-stu-id="841f0-259">Is-Single-Valued</span></span>       | <span data-ttu-id="841f0-260">True</span><span class="sxs-lookup"><span data-stu-id="841f0-260">True</span></span>                                                                                |
| <span data-ttu-id="841f0-261">É indexado</span><span class="sxs-lookup"><span data-stu-id="841f0-261">Is Indexed</span></span>             | <span data-ttu-id="841f0-262">Falso</span><span class="sxs-lookup"><span data-stu-id="841f0-262">False</span></span>                                                                               |
| <span data-ttu-id="841f0-263">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="841f0-263">In Global Catalog</span></span>      | <span data-ttu-id="841f0-264">Falso</span><span class="sxs-lookup"><span data-stu-id="841f0-264">False</span></span>                                                                               |
| <span data-ttu-id="841f0-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="841f0-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="841f0-266">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="841f0-266">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="841f0-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="841f0-267">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="841f0-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="841f0-268">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="841f0-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="841f0-269">Search-Flags</span></span>           | <span data-ttu-id="841f0-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="841f0-270">0x00000010</span></span>                                                                          |
| <span data-ttu-id="841f0-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="841f0-271">System-Flags</span></span>           | <span data-ttu-id="841f0-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="841f0-272">0x00000010</span></span>                                                                          |
| <span data-ttu-id="841f0-273">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="841f0-273">Classes used in</span></span>        | [<span data-ttu-id="841f0-274">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="841f0-274">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="841f0-275">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="841f0-275">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="841f0-276">Confira também</span><span class="sxs-lookup"><span data-stu-id="841f0-276">See also</span></span>

<dl> <dt>

[<span data-ttu-id="841f0-277">**homeDrive**</span><span class="sxs-lookup"><span data-stu-id="841f0-277">**homeDrive**</span></span>](a-homedrive.md)
</dt> </dl>

 

 





