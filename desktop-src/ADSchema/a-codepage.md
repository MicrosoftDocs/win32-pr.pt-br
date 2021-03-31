---
title: Code-Page atributo
description: Especifica a página de código para o idioma de escolha do usuário. Esse valor não é usado pelo Windows 2000.
ms.assetid: f98e6fbe-0c9a-4ee0-8158-3eaaca359675
ms.tgt_platform: multiple
keywords:
- Esquema de Code-Page do atributo AD
- Esquema de anúncio de atributo codePage
topic_type:
- apiref
api_name:
- Code-Page
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c3e9858ba387b98d5556c6010490c024be836b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645375"
---
# <a name="code-page-attribute"></a><span data-ttu-id="efad2-106">Code-Page atributo</span><span class="sxs-lookup"><span data-stu-id="efad2-106">Code-Page attribute</span></span>

<span data-ttu-id="efad2-107">Especifica a página de código para o idioma de escolha do usuário.</span><span class="sxs-lookup"><span data-stu-id="efad2-107">Specifies the code page for the user's language of choice.</span></span> <span data-ttu-id="efad2-108">Esse valor não é usado pelo Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="efad2-108">This value is not used by Windows 2000.</span></span>



| <span data-ttu-id="efad2-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="efad2-109">Entry</span></span> | <span data-ttu-id="efad2-110">Valor</span><span class="sxs-lookup"><span data-stu-id="efad2-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="efad2-111">CN</span><span class="sxs-lookup"><span data-stu-id="efad2-111">CN</span></span>                | <span data-ttu-id="efad2-112">Code-Page</span><span class="sxs-lookup"><span data-stu-id="efad2-112">Code-Page</span></span>                                             |
| <span data-ttu-id="efad2-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="efad2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="efad2-114">Código</span><span class="sxs-lookup"><span data-stu-id="efad2-114">codePage</span></span>                                              |
| <span data-ttu-id="efad2-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="efad2-115">Size</span></span>              | <span data-ttu-id="efad2-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="efad2-116">4 bytes</span></span>                                               |
| <span data-ttu-id="efad2-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="efad2-117">Update Privilege</span></span>  | <span data-ttu-id="efad2-118">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="efad2-118">Domain administrator</span></span>                                  |
| <span data-ttu-id="efad2-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="efad2-119">Update Frequency</span></span>  | <span data-ttu-id="efad2-120">Quando o usuário desejar alterar o idioma padrão.</span><span class="sxs-lookup"><span data-stu-id="efad2-120">When the user desires to change the default language.</span></span> |
| <span data-ttu-id="efad2-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="efad2-121">Attribute-Id</span></span>      | <span data-ttu-id="efad2-122">1.2.840.113556.1.4.16</span><span class="sxs-lookup"><span data-stu-id="efad2-122">1.2.840.113556.1.4.16</span></span>                                 |
| <span data-ttu-id="efad2-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="efad2-123">System-Id-Guid</span></span>    | <span data-ttu-id="efad2-124">bf967938-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="efad2-124">bf967938-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="efad2-125">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efad2-125">Syntax</span></span>            | [<span data-ttu-id="efad2-126">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="efad2-126">**Enumeration**</span></span>](s-enumeration.md)                  |



## <a name="implementations"></a><span data-ttu-id="efad2-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="efad2-127">Implementations</span></span>

-   [<span data-ttu-id="efad2-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="efad2-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="efad2-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="efad2-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="efad2-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="efad2-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="efad2-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="efad2-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="efad2-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="efad2-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="efad2-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="efad2-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="efad2-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="efad2-134">Windows 2000 Server</span></span>



| <span data-ttu-id="efad2-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="efad2-135">Entry</span></span> | <span data-ttu-id="efad2-136">Valor</span><span class="sxs-lookup"><span data-stu-id="efad2-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="efad2-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="efad2-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="efad2-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efad2-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="efad2-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="efad2-139">System-Only</span></span>            | <span data-ttu-id="efad2-140">Falso</span><span class="sxs-lookup"><span data-stu-id="efad2-140">False</span></span>                             |
| <span data-ttu-id="efad2-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="efad2-141">Is-Single-Valued</span></span>       | <span data-ttu-id="efad2-142">True</span><span class="sxs-lookup"><span data-stu-id="efad2-142">True</span></span>                              |
| <span data-ttu-id="efad2-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="efad2-143">Is Indexed</span></span>             | <span data-ttu-id="efad2-144">Falso</span><span class="sxs-lookup"><span data-stu-id="efad2-144">False</span></span>                             |
| <span data-ttu-id="efad2-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="efad2-145">In Global Catalog</span></span>      | <span data-ttu-id="efad2-146">Falso</span><span class="sxs-lookup"><span data-stu-id="efad2-146">False</span></span>                             |
| <span data-ttu-id="efad2-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="efad2-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="efad2-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="efad2-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="efad2-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efad2-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="efad2-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efad2-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="efad2-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efad2-151">Search-Flags</span></span>           | <span data-ttu-id="efad2-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efad2-152">0x00000010</span></span>                        |
| <span data-ttu-id="efad2-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efad2-153">System-Flags</span></span>           | <span data-ttu-id="efad2-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efad2-154">0x00000010</span></span>                        |
| <span data-ttu-id="efad2-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="efad2-155">Classes used in</span></span>        | [<span data-ttu-id="efad2-156">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="efad2-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="efad2-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="efad2-157">Windows Server 2003</span></span>



| <span data-ttu-id="efad2-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="efad2-158">Entry</span></span> | <span data-ttu-id="efad2-159">Valor</span><span class="sxs-lookup"><span data-stu-id="efad2-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="efad2-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="efad2-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="efad2-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efad2-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="efad2-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="efad2-162">System-Only</span></span>            | <span data-ttu-id="efad2-163">Falso</span><span class="sxs-lookup"><span data-stu-id="efad2-163">False</span></span>                             |
| <span data-ttu-id="efad2-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="efad2-164">Is-Single-Valued</span></span>       | <span data-ttu-id="efad2-165">True</span><span class="sxs-lookup"><span data-stu-id="efad2-165">True</span></span>                              |
| <span data-ttu-id="efad2-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="efad2-166">Is Indexed</span></span>             | <span data-ttu-id="efad2-167">Falso</span><span class="sxs-lookup"><span data-stu-id="efad2-167">False</span></span>                             |
| <span data-ttu-id="efad2-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="efad2-168">In Global Catalog</span></span>      | <span data-ttu-id="efad2-169">Falso</span><span class="sxs-lookup"><span data-stu-id="efad2-169">False</span></span>                             |
| <span data-ttu-id="efad2-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="efad2-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="efad2-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="efad2-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="efad2-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efad2-172">Range-Lower</span></span>            | <span data-ttu-id="efad2-173">0</span><span class="sxs-lookup"><span data-stu-id="efad2-173">0</span></span>                                 |
| <span data-ttu-id="efad2-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efad2-174">Range-Upper</span></span>            | <span data-ttu-id="efad2-175">65535</span><span class="sxs-lookup"><span data-stu-id="efad2-175">65535</span></span>                             |
| <span data-ttu-id="efad2-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efad2-176">Search-Flags</span></span>           | <span data-ttu-id="efad2-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efad2-177">0x00000010</span></span>                        |
| <span data-ttu-id="efad2-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efad2-178">System-Flags</span></span>           | <span data-ttu-id="efad2-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efad2-179">0x00000010</span></span>                        |
| <span data-ttu-id="efad2-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="efad2-180">Classes used in</span></span>        | [<span data-ttu-id="efad2-181">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="efad2-181">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="efad2-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="efad2-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="efad2-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="efad2-183">Entry</span></span> | <span data-ttu-id="efad2-184">Valor</span><span class="sxs-lookup"><span data-stu-id="efad2-184">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="efad2-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="efad2-185">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="efad2-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efad2-186">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="efad2-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="efad2-187">System-Only</span></span>            | <span data-ttu-id="efad2-188">Falso</span><span class="sxs-lookup"><span data-stu-id="efad2-188">False</span></span>                             |
| <span data-ttu-id="efad2-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="efad2-189">Is-Single-Valued</span></span>       | <span data-ttu-id="efad2-190">True</span><span class="sxs-lookup"><span data-stu-id="efad2-190">True</span></span>                              |
| <span data-ttu-id="efad2-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="efad2-191">Is Indexed</span></span>             | <span data-ttu-id="efad2-192">Falso</span><span class="sxs-lookup"><span data-stu-id="efad2-192">False</span></span>                             |
| <span data-ttu-id="efad2-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="efad2-193">In Global Catalog</span></span>      | <span data-ttu-id="efad2-194">Falso</span><span class="sxs-lookup"><span data-stu-id="efad2-194">False</span></span>                             |
| <span data-ttu-id="efad2-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="efad2-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="efad2-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="efad2-196">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="efad2-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efad2-197">Range-Lower</span></span>            | <span data-ttu-id="efad2-198">0</span><span class="sxs-lookup"><span data-stu-id="efad2-198">0</span></span>                                 |
| <span data-ttu-id="efad2-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efad2-199">Range-Upper</span></span>            | <span data-ttu-id="efad2-200">65535</span><span class="sxs-lookup"><span data-stu-id="efad2-200">65535</span></span>                             |
| <span data-ttu-id="efad2-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efad2-201">Search-Flags</span></span>           | <span data-ttu-id="efad2-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efad2-202">0x00000010</span></span>                        |
| <span data-ttu-id="efad2-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efad2-203">System-Flags</span></span>           | <span data-ttu-id="efad2-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efad2-204">0x00000010</span></span>                        |
| <span data-ttu-id="efad2-205">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="efad2-205">Classes used in</span></span>        | [<span data-ttu-id="efad2-206">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="efad2-206">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="efad2-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="efad2-207">Windows Server 2008</span></span>



| <span data-ttu-id="efad2-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="efad2-208">Entry</span></span> | <span data-ttu-id="efad2-209">Valor</span><span class="sxs-lookup"><span data-stu-id="efad2-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="efad2-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="efad2-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="efad2-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efad2-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="efad2-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="efad2-212">System-Only</span></span>            | <span data-ttu-id="efad2-213">Falso</span><span class="sxs-lookup"><span data-stu-id="efad2-213">False</span></span>                             |
| <span data-ttu-id="efad2-214">É de valor único</span><span class="sxs-lookup"><span data-stu-id="efad2-214">Is-Single-Valued</span></span>       | <span data-ttu-id="efad2-215">True</span><span class="sxs-lookup"><span data-stu-id="efad2-215">True</span></span>                              |
| <span data-ttu-id="efad2-216">É indexado</span><span class="sxs-lookup"><span data-stu-id="efad2-216">Is Indexed</span></span>             | <span data-ttu-id="efad2-217">Falso</span><span class="sxs-lookup"><span data-stu-id="efad2-217">False</span></span>                             |
| <span data-ttu-id="efad2-218">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="efad2-218">In Global Catalog</span></span>      | <span data-ttu-id="efad2-219">Falso</span><span class="sxs-lookup"><span data-stu-id="efad2-219">False</span></span>                             |
| <span data-ttu-id="efad2-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="efad2-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="efad2-221">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="efad2-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="efad2-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efad2-222">Range-Lower</span></span>            | <span data-ttu-id="efad2-223">0</span><span class="sxs-lookup"><span data-stu-id="efad2-223">0</span></span>                                 |
| <span data-ttu-id="efad2-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efad2-224">Range-Upper</span></span>            | <span data-ttu-id="efad2-225">65535</span><span class="sxs-lookup"><span data-stu-id="efad2-225">65535</span></span>                             |
| <span data-ttu-id="efad2-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efad2-226">Search-Flags</span></span>           | <span data-ttu-id="efad2-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efad2-227">0x00000010</span></span>                        |
| <span data-ttu-id="efad2-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efad2-228">System-Flags</span></span>           | <span data-ttu-id="efad2-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efad2-229">0x00000010</span></span>                        |
| <span data-ttu-id="efad2-230">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="efad2-230">Classes used in</span></span>        | [<span data-ttu-id="efad2-231">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="efad2-231">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="efad2-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="efad2-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="efad2-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="efad2-233">Entry</span></span> | <span data-ttu-id="efad2-234">Valor</span><span class="sxs-lookup"><span data-stu-id="efad2-234">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="efad2-235">ID do link</span><span class="sxs-lookup"><span data-stu-id="efad2-235">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="efad2-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efad2-236">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="efad2-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="efad2-237">System-Only</span></span>            | <span data-ttu-id="efad2-238">Falso</span><span class="sxs-lookup"><span data-stu-id="efad2-238">False</span></span>                             |
| <span data-ttu-id="efad2-239">É de valor único</span><span class="sxs-lookup"><span data-stu-id="efad2-239">Is-Single-Valued</span></span>       | <span data-ttu-id="efad2-240">True</span><span class="sxs-lookup"><span data-stu-id="efad2-240">True</span></span>                              |
| <span data-ttu-id="efad2-241">É indexado</span><span class="sxs-lookup"><span data-stu-id="efad2-241">Is Indexed</span></span>             | <span data-ttu-id="efad2-242">Falso</span><span class="sxs-lookup"><span data-stu-id="efad2-242">False</span></span>                             |
| <span data-ttu-id="efad2-243">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="efad2-243">In Global Catalog</span></span>      | <span data-ttu-id="efad2-244">Falso</span><span class="sxs-lookup"><span data-stu-id="efad2-244">False</span></span>                             |
| <span data-ttu-id="efad2-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="efad2-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="efad2-246">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="efad2-246">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="efad2-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efad2-247">Range-Lower</span></span>            | <span data-ttu-id="efad2-248">0</span><span class="sxs-lookup"><span data-stu-id="efad2-248">0</span></span>                                 |
| <span data-ttu-id="efad2-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efad2-249">Range-Upper</span></span>            | <span data-ttu-id="efad2-250">65535</span><span class="sxs-lookup"><span data-stu-id="efad2-250">65535</span></span>                             |
| <span data-ttu-id="efad2-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efad2-251">Search-Flags</span></span>           | <span data-ttu-id="efad2-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efad2-252">0x00000010</span></span>                        |
| <span data-ttu-id="efad2-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efad2-253">System-Flags</span></span>           | <span data-ttu-id="efad2-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efad2-254">0x00000010</span></span>                        |
| <span data-ttu-id="efad2-255">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="efad2-255">Classes used in</span></span>        | [<span data-ttu-id="efad2-256">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="efad2-256">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="efad2-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="efad2-257">Windows Server 2012</span></span>



| <span data-ttu-id="efad2-258">Entrada</span><span class="sxs-lookup"><span data-stu-id="efad2-258">Entry</span></span> | <span data-ttu-id="efad2-259">Valor</span><span class="sxs-lookup"><span data-stu-id="efad2-259">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="efad2-260">ID do link</span><span class="sxs-lookup"><span data-stu-id="efad2-260">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="efad2-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efad2-261">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="efad2-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="efad2-262">System-Only</span></span>            | <span data-ttu-id="efad2-263">Falso</span><span class="sxs-lookup"><span data-stu-id="efad2-263">False</span></span>                             |
| <span data-ttu-id="efad2-264">É de valor único</span><span class="sxs-lookup"><span data-stu-id="efad2-264">Is-Single-Valued</span></span>       | <span data-ttu-id="efad2-265">True</span><span class="sxs-lookup"><span data-stu-id="efad2-265">True</span></span>                              |
| <span data-ttu-id="efad2-266">É indexado</span><span class="sxs-lookup"><span data-stu-id="efad2-266">Is Indexed</span></span>             | <span data-ttu-id="efad2-267">Falso</span><span class="sxs-lookup"><span data-stu-id="efad2-267">False</span></span>                             |
| <span data-ttu-id="efad2-268">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="efad2-268">In Global Catalog</span></span>      | <span data-ttu-id="efad2-269">Falso</span><span class="sxs-lookup"><span data-stu-id="efad2-269">False</span></span>                             |
| <span data-ttu-id="efad2-270">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="efad2-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="efad2-271">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="efad2-271">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="efad2-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efad2-272">Range-Lower</span></span>            | <span data-ttu-id="efad2-273">0</span><span class="sxs-lookup"><span data-stu-id="efad2-273">0</span></span>                                 |
| <span data-ttu-id="efad2-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efad2-274">Range-Upper</span></span>            | <span data-ttu-id="efad2-275">65535</span><span class="sxs-lookup"><span data-stu-id="efad2-275">65535</span></span>                             |
| <span data-ttu-id="efad2-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efad2-276">Search-Flags</span></span>           | <span data-ttu-id="efad2-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efad2-277">0x00000010</span></span>                        |
| <span data-ttu-id="efad2-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efad2-278">System-Flags</span></span>           | <span data-ttu-id="efad2-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efad2-279">0x00000010</span></span>                        |
| <span data-ttu-id="efad2-280">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="efad2-280">Classes used in</span></span>        | [<span data-ttu-id="efad2-281">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="efad2-281">**User**</span></span>](c-user.md)<br/> |



 

 





