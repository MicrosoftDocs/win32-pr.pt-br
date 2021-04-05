---
title: Ajuda-atributo de nome de arquivo
description: Esse atributo foi usado para o Exchange 4,0. Ele continha o nome que deve ser usado para o arquivo quando o provedor baixasse os dados de ajuda para um computador cliente. Ele não é usado para nenhuma outra versão do Exchange.
ms.assetid: 3383b953-8a5c-4dfd-9d06-c35d29d6ea2d
ms.tgt_platform: multiple
keywords:
- Help-arquivo-nome do atributo AD Schema
- atributo de anúncio de atributos do helpFilename
topic_type:
- apiref
api_name:
- Help-File-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e049e34fe43cb17314f8483a2a77bd680a4e7fa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825243"
---
# <a name="help-file-name-attribute"></a><span data-ttu-id="671b1-107">Ajuda-atributo de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="671b1-107">Help-File-Name attribute</span></span>

<span data-ttu-id="671b1-108">Esse atributo foi usado para o Exchange 4,0.</span><span class="sxs-lookup"><span data-stu-id="671b1-108">This attribute was used for Exchange 4.0.</span></span> <span data-ttu-id="671b1-109">Ele continha o nome que deve ser usado para o arquivo quando o provedor baixasse os dados de ajuda para um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="671b1-109">It contained the name that should be used for the file when the provider downloaded help data to a client computer.</span></span> <span data-ttu-id="671b1-110">Ele não é usado para nenhuma outra versão do Exchange.</span><span class="sxs-lookup"><span data-stu-id="671b1-110">It is not used for any other versions of Exchange.</span></span>



| <span data-ttu-id="671b1-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="671b1-111">Entry</span></span> | <span data-ttu-id="671b1-112">Valor</span><span class="sxs-lookup"><span data-stu-id="671b1-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="671b1-113">CN</span><span class="sxs-lookup"><span data-stu-id="671b1-113">CN</span></span>                | <span data-ttu-id="671b1-114">Ajuda-nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="671b1-114">Help-File-Name</span></span>                              |
| <span data-ttu-id="671b1-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="671b1-115">Ldap-Display-Name</span></span> | <span data-ttu-id="671b1-116">Arquivodeajudaname</span><span class="sxs-lookup"><span data-stu-id="671b1-116">helpFileName</span></span>                                |
| <span data-ttu-id="671b1-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="671b1-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="671b1-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="671b1-118">Update Privilege</span></span>  | <span data-ttu-id="671b1-119">Isso é usado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="671b1-119">This is used by the system.</span></span>                 |
| <span data-ttu-id="671b1-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="671b1-120">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="671b1-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="671b1-121">Attribute-Id</span></span>      | <span data-ttu-id="671b1-122">1.2.840.113556.1.2.327</span><span class="sxs-lookup"><span data-stu-id="671b1-122">1.2.840.113556.1.2.327</span></span>                      |
| <span data-ttu-id="671b1-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="671b1-123">System-Id-Guid</span></span>    | <span data-ttu-id="671b1-124">5fd424a9-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="671b1-124">5fd424a9-1262-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="671b1-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="671b1-125">Syntax</span></span>            | [<span data-ttu-id="671b1-126">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="671b1-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="671b1-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="671b1-127">Implementations</span></span>

-   [<span data-ttu-id="671b1-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="671b1-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="671b1-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="671b1-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="671b1-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="671b1-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="671b1-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="671b1-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="671b1-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="671b1-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="671b1-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="671b1-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="671b1-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="671b1-134">Windows 2000 Server</span></span>



| <span data-ttu-id="671b1-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="671b1-135">Entry</span></span> | <span data-ttu-id="671b1-136">Valor</span><span class="sxs-lookup"><span data-stu-id="671b1-136">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="671b1-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="671b1-137">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="671b1-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="671b1-138">MAPI-Id</span></span>                | <span data-ttu-id="671b1-139">0x803B</span><span class="sxs-lookup"><span data-stu-id="671b1-139">0x803B</span></span>                                                   |
| <span data-ttu-id="671b1-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="671b1-140">System-Only</span></span>            | <span data-ttu-id="671b1-141">Falso</span><span class="sxs-lookup"><span data-stu-id="671b1-141">False</span></span>                                                    |
| <span data-ttu-id="671b1-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="671b1-142">Is-Single-Valued</span></span>       | <span data-ttu-id="671b1-143">True</span><span class="sxs-lookup"><span data-stu-id="671b1-143">True</span></span>                                                     |
| <span data-ttu-id="671b1-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="671b1-144">Is Indexed</span></span>             | <span data-ttu-id="671b1-145">Falso</span><span class="sxs-lookup"><span data-stu-id="671b1-145">False</span></span>                                                    |
| <span data-ttu-id="671b1-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="671b1-146">In Global Catalog</span></span>      | <span data-ttu-id="671b1-147">Falso</span><span class="sxs-lookup"><span data-stu-id="671b1-147">False</span></span>                                                    |
| <span data-ttu-id="671b1-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="671b1-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="671b1-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="671b1-149">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="671b1-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="671b1-150">Range-Lower</span></span>            | <span data-ttu-id="671b1-151">1</span><span class="sxs-lookup"><span data-stu-id="671b1-151">1</span></span>                                                        |
| <span data-ttu-id="671b1-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="671b1-152">Range-Upper</span></span>            | <span data-ttu-id="671b1-153">13</span><span class="sxs-lookup"><span data-stu-id="671b1-153">13</span></span>                                                       |
| <span data-ttu-id="671b1-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="671b1-154">Search-Flags</span></span>           | <span data-ttu-id="671b1-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="671b1-155">0x00000000</span></span>                                               |
| <span data-ttu-id="671b1-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="671b1-156">System-Flags</span></span>           | <span data-ttu-id="671b1-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="671b1-157">0x00000010</span></span>                                               |
| <span data-ttu-id="671b1-158">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="671b1-158">Classes used in</span></span>        | [<span data-ttu-id="671b1-159">**Display-template**</span><span class="sxs-lookup"><span data-stu-id="671b1-159">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="671b1-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="671b1-160">Windows Server 2003</span></span>



| <span data-ttu-id="671b1-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="671b1-161">Entry</span></span> | <span data-ttu-id="671b1-162">Valor</span><span class="sxs-lookup"><span data-stu-id="671b1-162">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="671b1-163">ID do link</span><span class="sxs-lookup"><span data-stu-id="671b1-163">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="671b1-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="671b1-164">MAPI-Id</span></span>                | <span data-ttu-id="671b1-165">0x803B</span><span class="sxs-lookup"><span data-stu-id="671b1-165">0x803B</span></span>                                                   |
| <span data-ttu-id="671b1-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="671b1-166">System-Only</span></span>            | <span data-ttu-id="671b1-167">Falso</span><span class="sxs-lookup"><span data-stu-id="671b1-167">False</span></span>                                                    |
| <span data-ttu-id="671b1-168">É de valor único</span><span class="sxs-lookup"><span data-stu-id="671b1-168">Is-Single-Valued</span></span>       | <span data-ttu-id="671b1-169">True</span><span class="sxs-lookup"><span data-stu-id="671b1-169">True</span></span>                                                     |
| <span data-ttu-id="671b1-170">É indexado</span><span class="sxs-lookup"><span data-stu-id="671b1-170">Is Indexed</span></span>             | <span data-ttu-id="671b1-171">Falso</span><span class="sxs-lookup"><span data-stu-id="671b1-171">False</span></span>                                                    |
| <span data-ttu-id="671b1-172">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="671b1-172">In Global Catalog</span></span>      | <span data-ttu-id="671b1-173">Falso</span><span class="sxs-lookup"><span data-stu-id="671b1-173">False</span></span>                                                    |
| <span data-ttu-id="671b1-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="671b1-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="671b1-175">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="671b1-175">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="671b1-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="671b1-176">Range-Lower</span></span>            | <span data-ttu-id="671b1-177">1</span><span class="sxs-lookup"><span data-stu-id="671b1-177">1</span></span>                                                        |
| <span data-ttu-id="671b1-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="671b1-178">Range-Upper</span></span>            | <span data-ttu-id="671b1-179">13</span><span class="sxs-lookup"><span data-stu-id="671b1-179">13</span></span>                                                       |
| <span data-ttu-id="671b1-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="671b1-180">Search-Flags</span></span>           | <span data-ttu-id="671b1-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="671b1-181">0x00000000</span></span>                                               |
| <span data-ttu-id="671b1-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="671b1-182">System-Flags</span></span>           | <span data-ttu-id="671b1-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="671b1-183">0x00000010</span></span>                                               |
| <span data-ttu-id="671b1-184">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="671b1-184">Classes used in</span></span>        | [<span data-ttu-id="671b1-185">**Display-template**</span><span class="sxs-lookup"><span data-stu-id="671b1-185">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="671b1-186">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="671b1-186">Windows Server 2003 R2</span></span>



| <span data-ttu-id="671b1-187">Entrada</span><span class="sxs-lookup"><span data-stu-id="671b1-187">Entry</span></span> | <span data-ttu-id="671b1-188">Valor</span><span class="sxs-lookup"><span data-stu-id="671b1-188">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="671b1-189">ID do link</span><span class="sxs-lookup"><span data-stu-id="671b1-189">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="671b1-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="671b1-190">MAPI-Id</span></span>                | <span data-ttu-id="671b1-191">0x803B</span><span class="sxs-lookup"><span data-stu-id="671b1-191">0x803B</span></span>                                                   |
| <span data-ttu-id="671b1-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="671b1-192">System-Only</span></span>            | <span data-ttu-id="671b1-193">Falso</span><span class="sxs-lookup"><span data-stu-id="671b1-193">False</span></span>                                                    |
| <span data-ttu-id="671b1-194">É de valor único</span><span class="sxs-lookup"><span data-stu-id="671b1-194">Is-Single-Valued</span></span>       | <span data-ttu-id="671b1-195">True</span><span class="sxs-lookup"><span data-stu-id="671b1-195">True</span></span>                                                     |
| <span data-ttu-id="671b1-196">É indexado</span><span class="sxs-lookup"><span data-stu-id="671b1-196">Is Indexed</span></span>             | <span data-ttu-id="671b1-197">Falso</span><span class="sxs-lookup"><span data-stu-id="671b1-197">False</span></span>                                                    |
| <span data-ttu-id="671b1-198">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="671b1-198">In Global Catalog</span></span>      | <span data-ttu-id="671b1-199">Falso</span><span class="sxs-lookup"><span data-stu-id="671b1-199">False</span></span>                                                    |
| <span data-ttu-id="671b1-200">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="671b1-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="671b1-201">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="671b1-201">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="671b1-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="671b1-202">Range-Lower</span></span>            | <span data-ttu-id="671b1-203">1</span><span class="sxs-lookup"><span data-stu-id="671b1-203">1</span></span>                                                        |
| <span data-ttu-id="671b1-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="671b1-204">Range-Upper</span></span>            | <span data-ttu-id="671b1-205">13</span><span class="sxs-lookup"><span data-stu-id="671b1-205">13</span></span>                                                       |
| <span data-ttu-id="671b1-206">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="671b1-206">Search-Flags</span></span>           | <span data-ttu-id="671b1-207">0x00000000</span><span class="sxs-lookup"><span data-stu-id="671b1-207">0x00000000</span></span>                                               |
| <span data-ttu-id="671b1-208">System-Flags</span><span class="sxs-lookup"><span data-stu-id="671b1-208">System-Flags</span></span>           | <span data-ttu-id="671b1-209">0x00000010</span><span class="sxs-lookup"><span data-stu-id="671b1-209">0x00000010</span></span>                                               |
| <span data-ttu-id="671b1-210">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="671b1-210">Classes used in</span></span>        | [<span data-ttu-id="671b1-211">**Display-template**</span><span class="sxs-lookup"><span data-stu-id="671b1-211">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="671b1-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="671b1-212">Windows Server 2008</span></span>



| <span data-ttu-id="671b1-213">Entrada</span><span class="sxs-lookup"><span data-stu-id="671b1-213">Entry</span></span> | <span data-ttu-id="671b1-214">Valor</span><span class="sxs-lookup"><span data-stu-id="671b1-214">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="671b1-215">ID do link</span><span class="sxs-lookup"><span data-stu-id="671b1-215">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="671b1-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="671b1-216">MAPI-Id</span></span>                | <span data-ttu-id="671b1-217">0x803B</span><span class="sxs-lookup"><span data-stu-id="671b1-217">0x803B</span></span>                                                   |
| <span data-ttu-id="671b1-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="671b1-218">System-Only</span></span>            | <span data-ttu-id="671b1-219">Falso</span><span class="sxs-lookup"><span data-stu-id="671b1-219">False</span></span>                                                    |
| <span data-ttu-id="671b1-220">É de valor único</span><span class="sxs-lookup"><span data-stu-id="671b1-220">Is-Single-Valued</span></span>       | <span data-ttu-id="671b1-221">True</span><span class="sxs-lookup"><span data-stu-id="671b1-221">True</span></span>                                                     |
| <span data-ttu-id="671b1-222">É indexado</span><span class="sxs-lookup"><span data-stu-id="671b1-222">Is Indexed</span></span>             | <span data-ttu-id="671b1-223">Falso</span><span class="sxs-lookup"><span data-stu-id="671b1-223">False</span></span>                                                    |
| <span data-ttu-id="671b1-224">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="671b1-224">In Global Catalog</span></span>      | <span data-ttu-id="671b1-225">Falso</span><span class="sxs-lookup"><span data-stu-id="671b1-225">False</span></span>                                                    |
| <span data-ttu-id="671b1-226">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="671b1-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="671b1-227">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="671b1-227">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="671b1-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="671b1-228">Range-Lower</span></span>            | <span data-ttu-id="671b1-229">1</span><span class="sxs-lookup"><span data-stu-id="671b1-229">1</span></span>                                                        |
| <span data-ttu-id="671b1-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="671b1-230">Range-Upper</span></span>            | <span data-ttu-id="671b1-231">13</span><span class="sxs-lookup"><span data-stu-id="671b1-231">13</span></span>                                                       |
| <span data-ttu-id="671b1-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="671b1-232">Search-Flags</span></span>           | <span data-ttu-id="671b1-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="671b1-233">0x00000000</span></span>                                               |
| <span data-ttu-id="671b1-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="671b1-234">System-Flags</span></span>           | <span data-ttu-id="671b1-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="671b1-235">0x00000010</span></span>                                               |
| <span data-ttu-id="671b1-236">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="671b1-236">Classes used in</span></span>        | [<span data-ttu-id="671b1-237">**Display-template**</span><span class="sxs-lookup"><span data-stu-id="671b1-237">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="671b1-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="671b1-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="671b1-239">Entrada</span><span class="sxs-lookup"><span data-stu-id="671b1-239">Entry</span></span> | <span data-ttu-id="671b1-240">Valor</span><span class="sxs-lookup"><span data-stu-id="671b1-240">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="671b1-241">ID do link</span><span class="sxs-lookup"><span data-stu-id="671b1-241">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="671b1-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="671b1-242">MAPI-Id</span></span>                | <span data-ttu-id="671b1-243">0x803B</span><span class="sxs-lookup"><span data-stu-id="671b1-243">0x803B</span></span>                                                   |
| <span data-ttu-id="671b1-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="671b1-244">System-Only</span></span>            | <span data-ttu-id="671b1-245">Falso</span><span class="sxs-lookup"><span data-stu-id="671b1-245">False</span></span>                                                    |
| <span data-ttu-id="671b1-246">É de valor único</span><span class="sxs-lookup"><span data-stu-id="671b1-246">Is-Single-Valued</span></span>       | <span data-ttu-id="671b1-247">True</span><span class="sxs-lookup"><span data-stu-id="671b1-247">True</span></span>                                                     |
| <span data-ttu-id="671b1-248">É indexado</span><span class="sxs-lookup"><span data-stu-id="671b1-248">Is Indexed</span></span>             | <span data-ttu-id="671b1-249">Falso</span><span class="sxs-lookup"><span data-stu-id="671b1-249">False</span></span>                                                    |
| <span data-ttu-id="671b1-250">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="671b1-250">In Global Catalog</span></span>      | <span data-ttu-id="671b1-251">Falso</span><span class="sxs-lookup"><span data-stu-id="671b1-251">False</span></span>                                                    |
| <span data-ttu-id="671b1-252">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="671b1-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="671b1-253">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="671b1-253">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="671b1-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="671b1-254">Range-Lower</span></span>            | <span data-ttu-id="671b1-255">1</span><span class="sxs-lookup"><span data-stu-id="671b1-255">1</span></span>                                                        |
| <span data-ttu-id="671b1-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="671b1-256">Range-Upper</span></span>            | <span data-ttu-id="671b1-257">13</span><span class="sxs-lookup"><span data-stu-id="671b1-257">13</span></span>                                                       |
| <span data-ttu-id="671b1-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="671b1-258">Search-Flags</span></span>           | <span data-ttu-id="671b1-259">0x00000000</span><span class="sxs-lookup"><span data-stu-id="671b1-259">0x00000000</span></span>                                               |
| <span data-ttu-id="671b1-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="671b1-260">System-Flags</span></span>           | <span data-ttu-id="671b1-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="671b1-261">0x00000010</span></span>                                               |
| <span data-ttu-id="671b1-262">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="671b1-262">Classes used in</span></span>        | [<span data-ttu-id="671b1-263">**Display-template**</span><span class="sxs-lookup"><span data-stu-id="671b1-263">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="671b1-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="671b1-264">Windows Server 2012</span></span>



| <span data-ttu-id="671b1-265">Entrada</span><span class="sxs-lookup"><span data-stu-id="671b1-265">Entry</span></span> | <span data-ttu-id="671b1-266">Valor</span><span class="sxs-lookup"><span data-stu-id="671b1-266">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="671b1-267">ID do link</span><span class="sxs-lookup"><span data-stu-id="671b1-267">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="671b1-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="671b1-268">MAPI-Id</span></span>                | <span data-ttu-id="671b1-269">0x803B</span><span class="sxs-lookup"><span data-stu-id="671b1-269">0x803B</span></span>                                                   |
| <span data-ttu-id="671b1-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="671b1-270">System-Only</span></span>            | <span data-ttu-id="671b1-271">Falso</span><span class="sxs-lookup"><span data-stu-id="671b1-271">False</span></span>                                                    |
| <span data-ttu-id="671b1-272">É de valor único</span><span class="sxs-lookup"><span data-stu-id="671b1-272">Is-Single-Valued</span></span>       | <span data-ttu-id="671b1-273">True</span><span class="sxs-lookup"><span data-stu-id="671b1-273">True</span></span>                                                     |
| <span data-ttu-id="671b1-274">É indexado</span><span class="sxs-lookup"><span data-stu-id="671b1-274">Is Indexed</span></span>             | <span data-ttu-id="671b1-275">Falso</span><span class="sxs-lookup"><span data-stu-id="671b1-275">False</span></span>                                                    |
| <span data-ttu-id="671b1-276">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="671b1-276">In Global Catalog</span></span>      | <span data-ttu-id="671b1-277">Falso</span><span class="sxs-lookup"><span data-stu-id="671b1-277">False</span></span>                                                    |
| <span data-ttu-id="671b1-278">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="671b1-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="671b1-279">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="671b1-279">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="671b1-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="671b1-280">Range-Lower</span></span>            | <span data-ttu-id="671b1-281">1</span><span class="sxs-lookup"><span data-stu-id="671b1-281">1</span></span>                                                        |
| <span data-ttu-id="671b1-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="671b1-282">Range-Upper</span></span>            | <span data-ttu-id="671b1-283">13</span><span class="sxs-lookup"><span data-stu-id="671b1-283">13</span></span>                                                       |
| <span data-ttu-id="671b1-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="671b1-284">Search-Flags</span></span>           | <span data-ttu-id="671b1-285">0x00000000</span><span class="sxs-lookup"><span data-stu-id="671b1-285">0x00000000</span></span>                                               |
| <span data-ttu-id="671b1-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="671b1-286">System-Flags</span></span>           | <span data-ttu-id="671b1-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="671b1-287">0x00000010</span></span>                                               |
| <span data-ttu-id="671b1-288">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="671b1-288">Classes used in</span></span>        | [<span data-ttu-id="671b1-289">**Display-template**</span><span class="sxs-lookup"><span data-stu-id="671b1-289">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



 

 





