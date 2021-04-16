---
title: atributo ms-IIS-FTP-root
description: Esse atributo determina o compartilhamento do servidor de arquivos. Ele é usado em conjunto com MS-IIS-FTP-dir para determinar o diretório base do usuário de FTP.
ms.assetid: b86dcafb-0b0d-4225-924c-690f739092a8
ms.tgt_platform: multiple
keywords:
- Esquema do AD do MS-IIS-FTP-root
- Esquema de AD do atributo msIIS-FTPRoot
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e7c55980b8b08865889f7567fa6bdb4dcf7bde1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456276"
---
# <a name="ms-iis-ftp-root-attribute"></a><span data-ttu-id="f0534-106">atributo ms-IIS-FTP-root</span><span class="sxs-lookup"><span data-stu-id="f0534-106">ms-IIS-FTP-Root attribute</span></span>

<span data-ttu-id="f0534-107">Esse atributo determina o compartilhamento do servidor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f0534-107">This attribute determines the file server share.</span></span> <span data-ttu-id="f0534-108">Ele é usado em conjunto com MS-IIS-FTP-dir para determinar o diretório base do usuário de FTP.</span><span class="sxs-lookup"><span data-stu-id="f0534-108">It is used in conjunction with ms-IIS-FTP-Dir to determine the FTP user home directory.</span></span>



| <span data-ttu-id="f0534-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0534-109">Entry</span></span> | <span data-ttu-id="f0534-110">Valor</span><span class="sxs-lookup"><span data-stu-id="f0534-110">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0534-111">CN</span><span class="sxs-lookup"><span data-stu-id="f0534-111">CN</span></span>                | <span data-ttu-id="f0534-112">MS-IIS-FTP-root</span><span class="sxs-lookup"><span data-stu-id="f0534-112">ms-IIS-FTP-Root</span></span>                                                                                                                 |
| <span data-ttu-id="f0534-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f0534-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f0534-114">msIIS-FTPRoot</span><span class="sxs-lookup"><span data-stu-id="f0534-114">msIIS-FTPRoot</span></span>                                                                                                                   |
| <span data-ttu-id="f0534-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f0534-115">Size</span></span>              | <span data-ttu-id="f0534-116">30-50 caracteres (15-25 caracteres Unicode para cada propriedade)</span><span class="sxs-lookup"><span data-stu-id="f0534-116">30-50 characters (15-25 Unicode characters for each property)</span></span>                                                                   |
| <span data-ttu-id="f0534-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f0534-117">Update Privilege</span></span>  | <span data-ttu-id="f0534-118">Administrador de domínio & sistema local</span><span class="sxs-lookup"><span data-stu-id="f0534-118">Domain administrator & local system</span></span>                                                                                             |
| <span data-ttu-id="f0534-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f0534-119">Update Frequency</span></span>  | <span data-ttu-id="f0534-120">Essa propriedade é definida quando o administrador cria o site e define o isolamento de FTP.</span><span class="sxs-lookup"><span data-stu-id="f0534-120">This property is set when the administrator creates the website and sets FTP isolation.</span></span> <span data-ttu-id="f0534-121">Ele raramente será alterado depois disso.</span><span class="sxs-lookup"><span data-stu-id="f0534-121">It's rarely going to change after that.</span></span> |
| <span data-ttu-id="f0534-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f0534-122">Attribute-Id</span></span>      | <span data-ttu-id="f0534-123">1.2.840.113556.1.4.1785</span><span class="sxs-lookup"><span data-stu-id="f0534-123">1.2.840.113556.1.4.1785</span></span>                                                                                                         |
| <span data-ttu-id="f0534-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f0534-124">System-Id-Guid</span></span>    | <span data-ttu-id="f0534-125">2a7827a4-1483-49a5-9d84-52e3812156b4</span><span class="sxs-lookup"><span data-stu-id="f0534-125">2a7827a4-1483-49a5-9d84-52e3812156b4</span></span>                                                                                            |
| <span data-ttu-id="f0534-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0534-126">Syntax</span></span>            | [<span data-ttu-id="f0534-127">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f0534-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                     |



## <a name="implementations"></a><span data-ttu-id="f0534-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="f0534-128">Implementations</span></span>

-   [<span data-ttu-id="f0534-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f0534-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f0534-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f0534-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f0534-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f0534-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f0534-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f0534-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f0534-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f0534-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f0534-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f0534-134">Windows Server 2003</span></span>



| <span data-ttu-id="f0534-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0534-135">Entry</span></span> | <span data-ttu-id="f0534-136">Valor</span><span class="sxs-lookup"><span data-stu-id="f0534-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f0534-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="f0534-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f0534-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0534-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f0534-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0534-139">System-Only</span></span>            | <span data-ttu-id="f0534-140">Falso</span><span class="sxs-lookup"><span data-stu-id="f0534-140">False</span></span>                             |
| <span data-ttu-id="f0534-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f0534-141">Is-Single-Valued</span></span>       | <span data-ttu-id="f0534-142">True</span><span class="sxs-lookup"><span data-stu-id="f0534-142">True</span></span>                              |
| <span data-ttu-id="f0534-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="f0534-143">Is Indexed</span></span>             | <span data-ttu-id="f0534-144">Falso</span><span class="sxs-lookup"><span data-stu-id="f0534-144">False</span></span>                             |
| <span data-ttu-id="f0534-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f0534-145">In Global Catalog</span></span>      | <span data-ttu-id="f0534-146">Falso</span><span class="sxs-lookup"><span data-stu-id="f0534-146">False</span></span>                             |
| <span data-ttu-id="f0534-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f0534-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0534-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f0534-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f0534-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0534-149">Range-Lower</span></span>            | <span data-ttu-id="f0534-150">1</span><span class="sxs-lookup"><span data-stu-id="f0534-150">1</span></span>                                 |
| <span data-ttu-id="f0534-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0534-151">Range-Upper</span></span>            | <span data-ttu-id="f0534-152">256</span><span class="sxs-lookup"><span data-stu-id="f0534-152">256</span></span>                               |
| <span data-ttu-id="f0534-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0534-153">Search-Flags</span></span>           | <span data-ttu-id="f0534-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0534-154">0x00000000</span></span>                        |
| <span data-ttu-id="f0534-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0534-155">System-Flags</span></span>           | <span data-ttu-id="f0534-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0534-156">0x00000010</span></span>                        |
| <span data-ttu-id="f0534-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f0534-157">Classes used in</span></span>        | [<span data-ttu-id="f0534-158">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f0534-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f0534-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f0534-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f0534-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0534-160">Entry</span></span> | <span data-ttu-id="f0534-161">Valor</span><span class="sxs-lookup"><span data-stu-id="f0534-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f0534-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="f0534-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f0534-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0534-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f0534-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0534-164">System-Only</span></span>            | <span data-ttu-id="f0534-165">Falso</span><span class="sxs-lookup"><span data-stu-id="f0534-165">False</span></span>                             |
| <span data-ttu-id="f0534-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f0534-166">Is-Single-Valued</span></span>       | <span data-ttu-id="f0534-167">True</span><span class="sxs-lookup"><span data-stu-id="f0534-167">True</span></span>                              |
| <span data-ttu-id="f0534-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="f0534-168">Is Indexed</span></span>             | <span data-ttu-id="f0534-169">Falso</span><span class="sxs-lookup"><span data-stu-id="f0534-169">False</span></span>                             |
| <span data-ttu-id="f0534-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f0534-170">In Global Catalog</span></span>      | <span data-ttu-id="f0534-171">Falso</span><span class="sxs-lookup"><span data-stu-id="f0534-171">False</span></span>                             |
| <span data-ttu-id="f0534-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f0534-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0534-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f0534-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f0534-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0534-174">Range-Lower</span></span>            | <span data-ttu-id="f0534-175">1</span><span class="sxs-lookup"><span data-stu-id="f0534-175">1</span></span>                                 |
| <span data-ttu-id="f0534-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0534-176">Range-Upper</span></span>            | <span data-ttu-id="f0534-177">256</span><span class="sxs-lookup"><span data-stu-id="f0534-177">256</span></span>                               |
| <span data-ttu-id="f0534-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0534-178">Search-Flags</span></span>           | <span data-ttu-id="f0534-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0534-179">0x00000000</span></span>                        |
| <span data-ttu-id="f0534-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0534-180">System-Flags</span></span>           | <span data-ttu-id="f0534-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0534-181">0x00000010</span></span>                        |
| <span data-ttu-id="f0534-182">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f0534-182">Classes used in</span></span>        | [<span data-ttu-id="f0534-183">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f0534-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f0534-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0534-184">Windows Server 2008</span></span>



| <span data-ttu-id="f0534-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0534-185">Entry</span></span> | <span data-ttu-id="f0534-186">Valor</span><span class="sxs-lookup"><span data-stu-id="f0534-186">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f0534-187">ID do link</span><span class="sxs-lookup"><span data-stu-id="f0534-187">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f0534-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0534-188">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f0534-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0534-189">System-Only</span></span>            | <span data-ttu-id="f0534-190">Falso</span><span class="sxs-lookup"><span data-stu-id="f0534-190">False</span></span>                             |
| <span data-ttu-id="f0534-191">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f0534-191">Is-Single-Valued</span></span>       | <span data-ttu-id="f0534-192">True</span><span class="sxs-lookup"><span data-stu-id="f0534-192">True</span></span>                              |
| <span data-ttu-id="f0534-193">É indexado</span><span class="sxs-lookup"><span data-stu-id="f0534-193">Is Indexed</span></span>             | <span data-ttu-id="f0534-194">Falso</span><span class="sxs-lookup"><span data-stu-id="f0534-194">False</span></span>                             |
| <span data-ttu-id="f0534-195">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f0534-195">In Global Catalog</span></span>      | <span data-ttu-id="f0534-196">Falso</span><span class="sxs-lookup"><span data-stu-id="f0534-196">False</span></span>                             |
| <span data-ttu-id="f0534-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f0534-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0534-198">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f0534-198">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f0534-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0534-199">Range-Lower</span></span>            | <span data-ttu-id="f0534-200">1</span><span class="sxs-lookup"><span data-stu-id="f0534-200">1</span></span>                                 |
| <span data-ttu-id="f0534-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0534-201">Range-Upper</span></span>            | <span data-ttu-id="f0534-202">256</span><span class="sxs-lookup"><span data-stu-id="f0534-202">256</span></span>                               |
| <span data-ttu-id="f0534-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0534-203">Search-Flags</span></span>           | <span data-ttu-id="f0534-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0534-204">0x00000000</span></span>                        |
| <span data-ttu-id="f0534-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0534-205">System-Flags</span></span>           | <span data-ttu-id="f0534-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0534-206">0x00000010</span></span>                        |
| <span data-ttu-id="f0534-207">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f0534-207">Classes used in</span></span>        | [<span data-ttu-id="f0534-208">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f0534-208">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f0534-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f0534-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f0534-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0534-210">Entry</span></span> | <span data-ttu-id="f0534-211">Valor</span><span class="sxs-lookup"><span data-stu-id="f0534-211">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f0534-212">ID do link</span><span class="sxs-lookup"><span data-stu-id="f0534-212">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f0534-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0534-213">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f0534-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0534-214">System-Only</span></span>            | <span data-ttu-id="f0534-215">Falso</span><span class="sxs-lookup"><span data-stu-id="f0534-215">False</span></span>                             |
| <span data-ttu-id="f0534-216">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f0534-216">Is-Single-Valued</span></span>       | <span data-ttu-id="f0534-217">True</span><span class="sxs-lookup"><span data-stu-id="f0534-217">True</span></span>                              |
| <span data-ttu-id="f0534-218">É indexado</span><span class="sxs-lookup"><span data-stu-id="f0534-218">Is Indexed</span></span>             | <span data-ttu-id="f0534-219">Falso</span><span class="sxs-lookup"><span data-stu-id="f0534-219">False</span></span>                             |
| <span data-ttu-id="f0534-220">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f0534-220">In Global Catalog</span></span>      | <span data-ttu-id="f0534-221">Falso</span><span class="sxs-lookup"><span data-stu-id="f0534-221">False</span></span>                             |
| <span data-ttu-id="f0534-222">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f0534-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0534-223">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f0534-223">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f0534-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0534-224">Range-Lower</span></span>            | <span data-ttu-id="f0534-225">1</span><span class="sxs-lookup"><span data-stu-id="f0534-225">1</span></span>                                 |
| <span data-ttu-id="f0534-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0534-226">Range-Upper</span></span>            | <span data-ttu-id="f0534-227">256</span><span class="sxs-lookup"><span data-stu-id="f0534-227">256</span></span>                               |
| <span data-ttu-id="f0534-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0534-228">Search-Flags</span></span>           | <span data-ttu-id="f0534-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0534-229">0x00000000</span></span>                        |
| <span data-ttu-id="f0534-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0534-230">System-Flags</span></span>           | <span data-ttu-id="f0534-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0534-231">0x00000010</span></span>                        |
| <span data-ttu-id="f0534-232">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f0534-232">Classes used in</span></span>        | [<span data-ttu-id="f0534-233">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f0534-233">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f0534-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f0534-234">Windows Server 2012</span></span>



| <span data-ttu-id="f0534-235">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0534-235">Entry</span></span> | <span data-ttu-id="f0534-236">Valor</span><span class="sxs-lookup"><span data-stu-id="f0534-236">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f0534-237">ID do link</span><span class="sxs-lookup"><span data-stu-id="f0534-237">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f0534-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0534-238">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f0534-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0534-239">System-Only</span></span>            | <span data-ttu-id="f0534-240">Falso</span><span class="sxs-lookup"><span data-stu-id="f0534-240">False</span></span>                             |
| <span data-ttu-id="f0534-241">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f0534-241">Is-Single-Valued</span></span>       | <span data-ttu-id="f0534-242">True</span><span class="sxs-lookup"><span data-stu-id="f0534-242">True</span></span>                              |
| <span data-ttu-id="f0534-243">É indexado</span><span class="sxs-lookup"><span data-stu-id="f0534-243">Is Indexed</span></span>             | <span data-ttu-id="f0534-244">Falso</span><span class="sxs-lookup"><span data-stu-id="f0534-244">False</span></span>                             |
| <span data-ttu-id="f0534-245">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f0534-245">In Global Catalog</span></span>      | <span data-ttu-id="f0534-246">Falso</span><span class="sxs-lookup"><span data-stu-id="f0534-246">False</span></span>                             |
| <span data-ttu-id="f0534-247">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f0534-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0534-248">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f0534-248">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f0534-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0534-249">Range-Lower</span></span>            | <span data-ttu-id="f0534-250">1</span><span class="sxs-lookup"><span data-stu-id="f0534-250">1</span></span>                                 |
| <span data-ttu-id="f0534-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0534-251">Range-Upper</span></span>            | <span data-ttu-id="f0534-252">256</span><span class="sxs-lookup"><span data-stu-id="f0534-252">256</span></span>                               |
| <span data-ttu-id="f0534-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0534-253">Search-Flags</span></span>           | <span data-ttu-id="f0534-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0534-254">0x00000000</span></span>                        |
| <span data-ttu-id="f0534-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0534-255">System-Flags</span></span>           | <span data-ttu-id="f0534-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0534-256">0x00000010</span></span>                        |
| <span data-ttu-id="f0534-257">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f0534-257">Classes used in</span></span>        | [<span data-ttu-id="f0534-258">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f0534-258">**User**</span></span>](c-user.md)<br/> |



 

 





