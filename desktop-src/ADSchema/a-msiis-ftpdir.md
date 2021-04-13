---
title: atributo ms-IIS-FTP-dir
description: Esse atributo determina o diretório base do usuário relativo ao compartilhamento do servidor de arquivos. Ele é usado em conjunto com MS-IIS-FTP-root para determinar o diretório base do usuário de FTP.
ms.assetid: 99b22b79-1d42-440d-b92b-33bac3e811cb
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo ms-IIS-FTP-dir
- Esquema de AD do atributo msIIS-FTPDir
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Dir
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3067476e7dc275dbe14471d6c3c98fa5445a9dfe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104499982"
---
# <a name="ms-iis-ftp-dir-attribute"></a><span data-ttu-id="9c841-106">atributo ms-IIS-FTP-dir</span><span class="sxs-lookup"><span data-stu-id="9c841-106">ms-IIS-FTP-Dir attribute</span></span>

<span data-ttu-id="9c841-107">Esse atributo determina o diretório base do usuário relativo ao compartilhamento do servidor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9c841-107">This attribute determines the user home directory relative to the file server share.</span></span> <span data-ttu-id="9c841-108">Ele é usado em conjunto com MS-IIS-FTP-root para determinar o diretório base do usuário de FTP.</span><span class="sxs-lookup"><span data-stu-id="9c841-108">It is used in conjunction with ms-IIS-FTP-Root to determine the FTP user home directory.</span></span>



| <span data-ttu-id="9c841-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="9c841-109">Entry</span></span> | <span data-ttu-id="9c841-110">Valor</span><span class="sxs-lookup"><span data-stu-id="9c841-110">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c841-111">CN</span><span class="sxs-lookup"><span data-stu-id="9c841-111">CN</span></span>                | <span data-ttu-id="9c841-112">MS-IIS-FTP-dir</span><span class="sxs-lookup"><span data-stu-id="9c841-112">ms-IIS-FTP-Dir</span></span>                                                                                                                  |
| <span data-ttu-id="9c841-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9c841-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9c841-114">msIIS-FTPDir</span><span class="sxs-lookup"><span data-stu-id="9c841-114">msIIS-FTPDir</span></span>                                                                                                                    |
| <span data-ttu-id="9c841-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="9c841-115">Size</span></span>              | <span data-ttu-id="9c841-116">30-50 caracteres (15-25 caracteres Unicode para cada propriedade)</span><span class="sxs-lookup"><span data-stu-id="9c841-116">30-50 characters (15-25 Unicode characters for each property)</span></span>                                                                   |
| <span data-ttu-id="9c841-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="9c841-117">Update Privilege</span></span>  | <span data-ttu-id="9c841-118">Administrador de domínio & sistema local</span><span class="sxs-lookup"><span data-stu-id="9c841-118">Domain administrator & local system</span></span>                                                                                             |
| <span data-ttu-id="9c841-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="9c841-119">Update Frequency</span></span>  | <span data-ttu-id="9c841-120">Essa propriedade é definida quando o administrador cria o site e define o isolamento de FTP.</span><span class="sxs-lookup"><span data-stu-id="9c841-120">This property is set when the administrator creates the website and sets FTP isolation.</span></span> <span data-ttu-id="9c841-121">Ele raramente será alterado depois disso.</span><span class="sxs-lookup"><span data-stu-id="9c841-121">It's rarely going to change after that.</span></span> |
| <span data-ttu-id="9c841-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9c841-122">Attribute-Id</span></span>      | <span data-ttu-id="9c841-123">1.2.840.113556.1.4.1786</span><span class="sxs-lookup"><span data-stu-id="9c841-123">1.2.840.113556.1.4.1786</span></span>                                                                                                         |
| <span data-ttu-id="9c841-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9c841-124">System-Id-Guid</span></span>    | <span data-ttu-id="9c841-125">8a5c99e9-2230-46eb-b8e8-e59d712eb9ee</span><span class="sxs-lookup"><span data-stu-id="9c841-125">8a5c99e9-2230-46eb-b8e8-e59d712eb9ee</span></span>                                                                                            |
| <span data-ttu-id="9c841-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c841-126">Syntax</span></span>            | [<span data-ttu-id="9c841-127">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9c841-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                     |



## <a name="implementations"></a><span data-ttu-id="9c841-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="9c841-128">Implementations</span></span>

-   [<span data-ttu-id="9c841-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9c841-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9c841-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9c841-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9c841-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9c841-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9c841-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9c841-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9c841-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9c841-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9c841-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9c841-134">Windows Server 2003</span></span>



| <span data-ttu-id="9c841-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="9c841-135">Entry</span></span> | <span data-ttu-id="9c841-136">Valor</span><span class="sxs-lookup"><span data-stu-id="9c841-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9c841-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="9c841-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9c841-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c841-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9c841-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c841-139">System-Only</span></span>            | <span data-ttu-id="9c841-140">Falso</span><span class="sxs-lookup"><span data-stu-id="9c841-140">False</span></span>                             |
| <span data-ttu-id="9c841-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9c841-141">Is-Single-Valued</span></span>       | <span data-ttu-id="9c841-142">True</span><span class="sxs-lookup"><span data-stu-id="9c841-142">True</span></span>                              |
| <span data-ttu-id="9c841-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="9c841-143">Is Indexed</span></span>             | <span data-ttu-id="9c841-144">Falso</span><span class="sxs-lookup"><span data-stu-id="9c841-144">False</span></span>                             |
| <span data-ttu-id="9c841-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9c841-145">In Global Catalog</span></span>      | <span data-ttu-id="9c841-146">Falso</span><span class="sxs-lookup"><span data-stu-id="9c841-146">False</span></span>                             |
| <span data-ttu-id="9c841-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9c841-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c841-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9c841-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9c841-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c841-149">Range-Lower</span></span>            | <span data-ttu-id="9c841-150">1</span><span class="sxs-lookup"><span data-stu-id="9c841-150">1</span></span>                                 |
| <span data-ttu-id="9c841-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c841-151">Range-Upper</span></span>            | <span data-ttu-id="9c841-152">256</span><span class="sxs-lookup"><span data-stu-id="9c841-152">256</span></span>                               |
| <span data-ttu-id="9c841-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c841-153">Search-Flags</span></span>           | <span data-ttu-id="9c841-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c841-154">0x00000000</span></span>                        |
| <span data-ttu-id="9c841-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c841-155">System-Flags</span></span>           | <span data-ttu-id="9c841-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c841-156">0x00000010</span></span>                        |
| <span data-ttu-id="9c841-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9c841-157">Classes used in</span></span>        | [<span data-ttu-id="9c841-158">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="9c841-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9c841-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9c841-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9c841-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="9c841-160">Entry</span></span> | <span data-ttu-id="9c841-161">Valor</span><span class="sxs-lookup"><span data-stu-id="9c841-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9c841-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="9c841-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9c841-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c841-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9c841-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c841-164">System-Only</span></span>            | <span data-ttu-id="9c841-165">Falso</span><span class="sxs-lookup"><span data-stu-id="9c841-165">False</span></span>                             |
| <span data-ttu-id="9c841-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9c841-166">Is-Single-Valued</span></span>       | <span data-ttu-id="9c841-167">True</span><span class="sxs-lookup"><span data-stu-id="9c841-167">True</span></span>                              |
| <span data-ttu-id="9c841-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="9c841-168">Is Indexed</span></span>             | <span data-ttu-id="9c841-169">Falso</span><span class="sxs-lookup"><span data-stu-id="9c841-169">False</span></span>                             |
| <span data-ttu-id="9c841-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9c841-170">In Global Catalog</span></span>      | <span data-ttu-id="9c841-171">Falso</span><span class="sxs-lookup"><span data-stu-id="9c841-171">False</span></span>                             |
| <span data-ttu-id="9c841-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9c841-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c841-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9c841-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9c841-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c841-174">Range-Lower</span></span>            | <span data-ttu-id="9c841-175">1</span><span class="sxs-lookup"><span data-stu-id="9c841-175">1</span></span>                                 |
| <span data-ttu-id="9c841-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c841-176">Range-Upper</span></span>            | <span data-ttu-id="9c841-177">256</span><span class="sxs-lookup"><span data-stu-id="9c841-177">256</span></span>                               |
| <span data-ttu-id="9c841-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c841-178">Search-Flags</span></span>           | <span data-ttu-id="9c841-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c841-179">0x00000000</span></span>                        |
| <span data-ttu-id="9c841-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c841-180">System-Flags</span></span>           | <span data-ttu-id="9c841-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c841-181">0x00000010</span></span>                        |
| <span data-ttu-id="9c841-182">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9c841-182">Classes used in</span></span>        | [<span data-ttu-id="9c841-183">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="9c841-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9c841-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c841-184">Windows Server 2008</span></span>



| <span data-ttu-id="9c841-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="9c841-185">Entry</span></span> | <span data-ttu-id="9c841-186">Valor</span><span class="sxs-lookup"><span data-stu-id="9c841-186">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9c841-187">ID do link</span><span class="sxs-lookup"><span data-stu-id="9c841-187">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9c841-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c841-188">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9c841-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c841-189">System-Only</span></span>            | <span data-ttu-id="9c841-190">Falso</span><span class="sxs-lookup"><span data-stu-id="9c841-190">False</span></span>                             |
| <span data-ttu-id="9c841-191">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9c841-191">Is-Single-Valued</span></span>       | <span data-ttu-id="9c841-192">True</span><span class="sxs-lookup"><span data-stu-id="9c841-192">True</span></span>                              |
| <span data-ttu-id="9c841-193">É indexado</span><span class="sxs-lookup"><span data-stu-id="9c841-193">Is Indexed</span></span>             | <span data-ttu-id="9c841-194">Falso</span><span class="sxs-lookup"><span data-stu-id="9c841-194">False</span></span>                             |
| <span data-ttu-id="9c841-195">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9c841-195">In Global Catalog</span></span>      | <span data-ttu-id="9c841-196">Falso</span><span class="sxs-lookup"><span data-stu-id="9c841-196">False</span></span>                             |
| <span data-ttu-id="9c841-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9c841-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c841-198">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9c841-198">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9c841-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c841-199">Range-Lower</span></span>            | <span data-ttu-id="9c841-200">1</span><span class="sxs-lookup"><span data-stu-id="9c841-200">1</span></span>                                 |
| <span data-ttu-id="9c841-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c841-201">Range-Upper</span></span>            | <span data-ttu-id="9c841-202">256</span><span class="sxs-lookup"><span data-stu-id="9c841-202">256</span></span>                               |
| <span data-ttu-id="9c841-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c841-203">Search-Flags</span></span>           | <span data-ttu-id="9c841-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c841-204">0x00000000</span></span>                        |
| <span data-ttu-id="9c841-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c841-205">System-Flags</span></span>           | <span data-ttu-id="9c841-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c841-206">0x00000010</span></span>                        |
| <span data-ttu-id="9c841-207">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9c841-207">Classes used in</span></span>        | [<span data-ttu-id="9c841-208">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="9c841-208">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9c841-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9c841-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9c841-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="9c841-210">Entry</span></span> | <span data-ttu-id="9c841-211">Valor</span><span class="sxs-lookup"><span data-stu-id="9c841-211">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9c841-212">ID do link</span><span class="sxs-lookup"><span data-stu-id="9c841-212">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9c841-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c841-213">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9c841-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c841-214">System-Only</span></span>            | <span data-ttu-id="9c841-215">Falso</span><span class="sxs-lookup"><span data-stu-id="9c841-215">False</span></span>                             |
| <span data-ttu-id="9c841-216">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9c841-216">Is-Single-Valued</span></span>       | <span data-ttu-id="9c841-217">True</span><span class="sxs-lookup"><span data-stu-id="9c841-217">True</span></span>                              |
| <span data-ttu-id="9c841-218">É indexado</span><span class="sxs-lookup"><span data-stu-id="9c841-218">Is Indexed</span></span>             | <span data-ttu-id="9c841-219">Falso</span><span class="sxs-lookup"><span data-stu-id="9c841-219">False</span></span>                             |
| <span data-ttu-id="9c841-220">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9c841-220">In Global Catalog</span></span>      | <span data-ttu-id="9c841-221">Falso</span><span class="sxs-lookup"><span data-stu-id="9c841-221">False</span></span>                             |
| <span data-ttu-id="9c841-222">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9c841-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c841-223">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9c841-223">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9c841-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c841-224">Range-Lower</span></span>            | <span data-ttu-id="9c841-225">1</span><span class="sxs-lookup"><span data-stu-id="9c841-225">1</span></span>                                 |
| <span data-ttu-id="9c841-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c841-226">Range-Upper</span></span>            | <span data-ttu-id="9c841-227">256</span><span class="sxs-lookup"><span data-stu-id="9c841-227">256</span></span>                               |
| <span data-ttu-id="9c841-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c841-228">Search-Flags</span></span>           | <span data-ttu-id="9c841-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c841-229">0x00000000</span></span>                        |
| <span data-ttu-id="9c841-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c841-230">System-Flags</span></span>           | <span data-ttu-id="9c841-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c841-231">0x00000010</span></span>                        |
| <span data-ttu-id="9c841-232">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9c841-232">Classes used in</span></span>        | [<span data-ttu-id="9c841-233">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="9c841-233">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9c841-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c841-234">Windows Server 2012</span></span>



| <span data-ttu-id="9c841-235">Entrada</span><span class="sxs-lookup"><span data-stu-id="9c841-235">Entry</span></span> | <span data-ttu-id="9c841-236">Valor</span><span class="sxs-lookup"><span data-stu-id="9c841-236">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9c841-237">ID do link</span><span class="sxs-lookup"><span data-stu-id="9c841-237">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9c841-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c841-238">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9c841-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c841-239">System-Only</span></span>            | <span data-ttu-id="9c841-240">Falso</span><span class="sxs-lookup"><span data-stu-id="9c841-240">False</span></span>                             |
| <span data-ttu-id="9c841-241">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9c841-241">Is-Single-Valued</span></span>       | <span data-ttu-id="9c841-242">True</span><span class="sxs-lookup"><span data-stu-id="9c841-242">True</span></span>                              |
| <span data-ttu-id="9c841-243">É indexado</span><span class="sxs-lookup"><span data-stu-id="9c841-243">Is Indexed</span></span>             | <span data-ttu-id="9c841-244">Falso</span><span class="sxs-lookup"><span data-stu-id="9c841-244">False</span></span>                             |
| <span data-ttu-id="9c841-245">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9c841-245">In Global Catalog</span></span>      | <span data-ttu-id="9c841-246">Falso</span><span class="sxs-lookup"><span data-stu-id="9c841-246">False</span></span>                             |
| <span data-ttu-id="9c841-247">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9c841-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c841-248">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9c841-248">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9c841-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c841-249">Range-Lower</span></span>            | <span data-ttu-id="9c841-250">1</span><span class="sxs-lookup"><span data-stu-id="9c841-250">1</span></span>                                 |
| <span data-ttu-id="9c841-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c841-251">Range-Upper</span></span>            | <span data-ttu-id="9c841-252">256</span><span class="sxs-lookup"><span data-stu-id="9c841-252">256</span></span>                               |
| <span data-ttu-id="9c841-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c841-253">Search-Flags</span></span>           | <span data-ttu-id="9c841-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c841-254">0x00000000</span></span>                        |
| <span data-ttu-id="9c841-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c841-255">System-Flags</span></span>           | <span data-ttu-id="9c841-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c841-256">0x00000010</span></span>                        |
| <span data-ttu-id="9c841-257">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9c841-257">Classes used in</span></span>        | [<span data-ttu-id="9c841-258">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="9c841-258">**User**</span></span>](c-user.md)<br/> |



 

 





