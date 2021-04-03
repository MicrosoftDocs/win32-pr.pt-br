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
# <a name="code-page-attribute"></a><span data-ttu-id="410b5-106">Code-Page atributo</span><span class="sxs-lookup"><span data-stu-id="410b5-106">Code-Page attribute</span></span>

<span data-ttu-id="410b5-107">Especifica a página de código para o idioma de escolha do usuário.</span><span class="sxs-lookup"><span data-stu-id="410b5-107">Specifies the code page for the user's language of choice.</span></span> <span data-ttu-id="410b5-108">Esse valor não é usado pelo Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="410b5-108">This value is not used by Windows 2000.</span></span>



| <span data-ttu-id="410b5-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="410b5-109">Entry</span></span> | <span data-ttu-id="410b5-110">Valor</span><span class="sxs-lookup"><span data-stu-id="410b5-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="410b5-111">CN</span><span class="sxs-lookup"><span data-stu-id="410b5-111">CN</span></span>                | <span data-ttu-id="410b5-112">Code-Page</span><span class="sxs-lookup"><span data-stu-id="410b5-112">Code-Page</span></span>                                             |
| <span data-ttu-id="410b5-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="410b5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="410b5-114">Código</span><span class="sxs-lookup"><span data-stu-id="410b5-114">codePage</span></span>                                              |
| <span data-ttu-id="410b5-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="410b5-115">Size</span></span>              | <span data-ttu-id="410b5-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="410b5-116">4 bytes</span></span>                                               |
| <span data-ttu-id="410b5-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="410b5-117">Update Privilege</span></span>  | <span data-ttu-id="410b5-118">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="410b5-118">Domain administrator</span></span>                                  |
| <span data-ttu-id="410b5-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="410b5-119">Update Frequency</span></span>  | <span data-ttu-id="410b5-120">Quando o usuário desejar alterar o idioma padrão.</span><span class="sxs-lookup"><span data-stu-id="410b5-120">When the user desires to change the default language.</span></span> |
| <span data-ttu-id="410b5-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="410b5-121">Attribute-Id</span></span>      | <span data-ttu-id="410b5-122">1.2.840.113556.1.4.16</span><span class="sxs-lookup"><span data-stu-id="410b5-122">1.2.840.113556.1.4.16</span></span>                                 |
| <span data-ttu-id="410b5-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="410b5-123">System-Id-Guid</span></span>    | <span data-ttu-id="410b5-124">bf967938-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="410b5-124">bf967938-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="410b5-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="410b5-125">Syntax</span></span>            | [<span data-ttu-id="410b5-126">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="410b5-126">**Enumeration**</span></span>](s-enumeration.md)                  |



## <a name="implementations"></a><span data-ttu-id="410b5-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="410b5-127">Implementations</span></span>

-   [<span data-ttu-id="410b5-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="410b5-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="410b5-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="410b5-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="410b5-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="410b5-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="410b5-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="410b5-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="410b5-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="410b5-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="410b5-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="410b5-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="410b5-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="410b5-134">Windows 2000 Server</span></span>



| <span data-ttu-id="410b5-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="410b5-135">Entry</span></span> | <span data-ttu-id="410b5-136">Valor</span><span class="sxs-lookup"><span data-stu-id="410b5-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="410b5-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="410b5-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="410b5-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="410b5-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="410b5-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="410b5-139">System-Only</span></span>            | <span data-ttu-id="410b5-140">Falso</span><span class="sxs-lookup"><span data-stu-id="410b5-140">False</span></span>                             |
| <span data-ttu-id="410b5-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="410b5-141">Is-Single-Valued</span></span>       | <span data-ttu-id="410b5-142">True</span><span class="sxs-lookup"><span data-stu-id="410b5-142">True</span></span>                              |
| <span data-ttu-id="410b5-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="410b5-143">Is Indexed</span></span>             | <span data-ttu-id="410b5-144">Falso</span><span class="sxs-lookup"><span data-stu-id="410b5-144">False</span></span>                             |
| <span data-ttu-id="410b5-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="410b5-145">In Global Catalog</span></span>      | <span data-ttu-id="410b5-146">Falso</span><span class="sxs-lookup"><span data-stu-id="410b5-146">False</span></span>                             |
| <span data-ttu-id="410b5-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="410b5-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="410b5-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="410b5-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="410b5-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="410b5-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="410b5-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="410b5-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="410b5-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="410b5-151">Search-Flags</span></span>           | <span data-ttu-id="410b5-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="410b5-152">0x00000010</span></span>                        |
| <span data-ttu-id="410b5-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="410b5-153">System-Flags</span></span>           | <span data-ttu-id="410b5-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="410b5-154">0x00000010</span></span>                        |
| <span data-ttu-id="410b5-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="410b5-155">Classes used in</span></span>        | [<span data-ttu-id="410b5-156">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="410b5-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="410b5-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="410b5-157">Windows Server 2003</span></span>



| <span data-ttu-id="410b5-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="410b5-158">Entry</span></span> | <span data-ttu-id="410b5-159">Valor</span><span class="sxs-lookup"><span data-stu-id="410b5-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="410b5-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="410b5-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="410b5-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="410b5-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="410b5-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="410b5-162">System-Only</span></span>            | <span data-ttu-id="410b5-163">Falso</span><span class="sxs-lookup"><span data-stu-id="410b5-163">False</span></span>                             |
| <span data-ttu-id="410b5-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="410b5-164">Is-Single-Valued</span></span>       | <span data-ttu-id="410b5-165">True</span><span class="sxs-lookup"><span data-stu-id="410b5-165">True</span></span>                              |
| <span data-ttu-id="410b5-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="410b5-166">Is Indexed</span></span>             | <span data-ttu-id="410b5-167">Falso</span><span class="sxs-lookup"><span data-stu-id="410b5-167">False</span></span>                             |
| <span data-ttu-id="410b5-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="410b5-168">In Global Catalog</span></span>      | <span data-ttu-id="410b5-169">Falso</span><span class="sxs-lookup"><span data-stu-id="410b5-169">False</span></span>                             |
| <span data-ttu-id="410b5-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="410b5-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="410b5-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="410b5-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="410b5-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="410b5-172">Range-Lower</span></span>            | <span data-ttu-id="410b5-173">0</span><span class="sxs-lookup"><span data-stu-id="410b5-173">0</span></span>                                 |
| <span data-ttu-id="410b5-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="410b5-174">Range-Upper</span></span>            | <span data-ttu-id="410b5-175">65535</span><span class="sxs-lookup"><span data-stu-id="410b5-175">65535</span></span>                             |
| <span data-ttu-id="410b5-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="410b5-176">Search-Flags</span></span>           | <span data-ttu-id="410b5-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="410b5-177">0x00000010</span></span>                        |
| <span data-ttu-id="410b5-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="410b5-178">System-Flags</span></span>           | <span data-ttu-id="410b5-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="410b5-179">0x00000010</span></span>                        |
| <span data-ttu-id="410b5-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="410b5-180">Classes used in</span></span>        | [<span data-ttu-id="410b5-181">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="410b5-181">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="410b5-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="410b5-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="410b5-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="410b5-183">Entry</span></span> | <span data-ttu-id="410b5-184">Valor</span><span class="sxs-lookup"><span data-stu-id="410b5-184">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="410b5-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="410b5-185">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="410b5-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="410b5-186">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="410b5-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="410b5-187">System-Only</span></span>            | <span data-ttu-id="410b5-188">Falso</span><span class="sxs-lookup"><span data-stu-id="410b5-188">False</span></span>                             |
| <span data-ttu-id="410b5-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="410b5-189">Is-Single-Valued</span></span>       | <span data-ttu-id="410b5-190">True</span><span class="sxs-lookup"><span data-stu-id="410b5-190">True</span></span>                              |
| <span data-ttu-id="410b5-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="410b5-191">Is Indexed</span></span>             | <span data-ttu-id="410b5-192">Falso</span><span class="sxs-lookup"><span data-stu-id="410b5-192">False</span></span>                             |
| <span data-ttu-id="410b5-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="410b5-193">In Global Catalog</span></span>      | <span data-ttu-id="410b5-194">Falso</span><span class="sxs-lookup"><span data-stu-id="410b5-194">False</span></span>                             |
| <span data-ttu-id="410b5-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="410b5-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="410b5-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="410b5-196">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="410b5-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="410b5-197">Range-Lower</span></span>            | <span data-ttu-id="410b5-198">0</span><span class="sxs-lookup"><span data-stu-id="410b5-198">0</span></span>                                 |
| <span data-ttu-id="410b5-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="410b5-199">Range-Upper</span></span>            | <span data-ttu-id="410b5-200">65535</span><span class="sxs-lookup"><span data-stu-id="410b5-200">65535</span></span>                             |
| <span data-ttu-id="410b5-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="410b5-201">Search-Flags</span></span>           | <span data-ttu-id="410b5-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="410b5-202">0x00000010</span></span>                        |
| <span data-ttu-id="410b5-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="410b5-203">System-Flags</span></span>           | <span data-ttu-id="410b5-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="410b5-204">0x00000010</span></span>                        |
| <span data-ttu-id="410b5-205">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="410b5-205">Classes used in</span></span>        | [<span data-ttu-id="410b5-206">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="410b5-206">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="410b5-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="410b5-207">Windows Server 2008</span></span>



| <span data-ttu-id="410b5-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="410b5-208">Entry</span></span> | <span data-ttu-id="410b5-209">Valor</span><span class="sxs-lookup"><span data-stu-id="410b5-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="410b5-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="410b5-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="410b5-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="410b5-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="410b5-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="410b5-212">System-Only</span></span>            | <span data-ttu-id="410b5-213">Falso</span><span class="sxs-lookup"><span data-stu-id="410b5-213">False</span></span>                             |
| <span data-ttu-id="410b5-214">É de valor único</span><span class="sxs-lookup"><span data-stu-id="410b5-214">Is-Single-Valued</span></span>       | <span data-ttu-id="410b5-215">True</span><span class="sxs-lookup"><span data-stu-id="410b5-215">True</span></span>                              |
| <span data-ttu-id="410b5-216">É indexado</span><span class="sxs-lookup"><span data-stu-id="410b5-216">Is Indexed</span></span>             | <span data-ttu-id="410b5-217">Falso</span><span class="sxs-lookup"><span data-stu-id="410b5-217">False</span></span>                             |
| <span data-ttu-id="410b5-218">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="410b5-218">In Global Catalog</span></span>      | <span data-ttu-id="410b5-219">Falso</span><span class="sxs-lookup"><span data-stu-id="410b5-219">False</span></span>                             |
| <span data-ttu-id="410b5-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="410b5-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="410b5-221">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="410b5-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="410b5-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="410b5-222">Range-Lower</span></span>            | <span data-ttu-id="410b5-223">0</span><span class="sxs-lookup"><span data-stu-id="410b5-223">0</span></span>                                 |
| <span data-ttu-id="410b5-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="410b5-224">Range-Upper</span></span>            | <span data-ttu-id="410b5-225">65535</span><span class="sxs-lookup"><span data-stu-id="410b5-225">65535</span></span>                             |
| <span data-ttu-id="410b5-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="410b5-226">Search-Flags</span></span>           | <span data-ttu-id="410b5-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="410b5-227">0x00000010</span></span>                        |
| <span data-ttu-id="410b5-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="410b5-228">System-Flags</span></span>           | <span data-ttu-id="410b5-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="410b5-229">0x00000010</span></span>                        |
| <span data-ttu-id="410b5-230">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="410b5-230">Classes used in</span></span>        | [<span data-ttu-id="410b5-231">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="410b5-231">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="410b5-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="410b5-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="410b5-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="410b5-233">Entry</span></span> | <span data-ttu-id="410b5-234">Valor</span><span class="sxs-lookup"><span data-stu-id="410b5-234">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="410b5-235">ID do link</span><span class="sxs-lookup"><span data-stu-id="410b5-235">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="410b5-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="410b5-236">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="410b5-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="410b5-237">System-Only</span></span>            | <span data-ttu-id="410b5-238">Falso</span><span class="sxs-lookup"><span data-stu-id="410b5-238">False</span></span>                             |
| <span data-ttu-id="410b5-239">É de valor único</span><span class="sxs-lookup"><span data-stu-id="410b5-239">Is-Single-Valued</span></span>       | <span data-ttu-id="410b5-240">True</span><span class="sxs-lookup"><span data-stu-id="410b5-240">True</span></span>                              |
| <span data-ttu-id="410b5-241">É indexado</span><span class="sxs-lookup"><span data-stu-id="410b5-241">Is Indexed</span></span>             | <span data-ttu-id="410b5-242">Falso</span><span class="sxs-lookup"><span data-stu-id="410b5-242">False</span></span>                             |
| <span data-ttu-id="410b5-243">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="410b5-243">In Global Catalog</span></span>      | <span data-ttu-id="410b5-244">Falso</span><span class="sxs-lookup"><span data-stu-id="410b5-244">False</span></span>                             |
| <span data-ttu-id="410b5-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="410b5-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="410b5-246">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="410b5-246">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="410b5-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="410b5-247">Range-Lower</span></span>            | <span data-ttu-id="410b5-248">0</span><span class="sxs-lookup"><span data-stu-id="410b5-248">0</span></span>                                 |
| <span data-ttu-id="410b5-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="410b5-249">Range-Upper</span></span>            | <span data-ttu-id="410b5-250">65535</span><span class="sxs-lookup"><span data-stu-id="410b5-250">65535</span></span>                             |
| <span data-ttu-id="410b5-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="410b5-251">Search-Flags</span></span>           | <span data-ttu-id="410b5-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="410b5-252">0x00000010</span></span>                        |
| <span data-ttu-id="410b5-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="410b5-253">System-Flags</span></span>           | <span data-ttu-id="410b5-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="410b5-254">0x00000010</span></span>                        |
| <span data-ttu-id="410b5-255">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="410b5-255">Classes used in</span></span>        | [<span data-ttu-id="410b5-256">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="410b5-256">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="410b5-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="410b5-257">Windows Server 2012</span></span>



| <span data-ttu-id="410b5-258">Entrada</span><span class="sxs-lookup"><span data-stu-id="410b5-258">Entry</span></span> | <span data-ttu-id="410b5-259">Valor</span><span class="sxs-lookup"><span data-stu-id="410b5-259">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="410b5-260">ID do link</span><span class="sxs-lookup"><span data-stu-id="410b5-260">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="410b5-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="410b5-261">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="410b5-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="410b5-262">System-Only</span></span>            | <span data-ttu-id="410b5-263">Falso</span><span class="sxs-lookup"><span data-stu-id="410b5-263">False</span></span>                             |
| <span data-ttu-id="410b5-264">É de valor único</span><span class="sxs-lookup"><span data-stu-id="410b5-264">Is-Single-Valued</span></span>       | <span data-ttu-id="410b5-265">True</span><span class="sxs-lookup"><span data-stu-id="410b5-265">True</span></span>                              |
| <span data-ttu-id="410b5-266">É indexado</span><span class="sxs-lookup"><span data-stu-id="410b5-266">Is Indexed</span></span>             | <span data-ttu-id="410b5-267">Falso</span><span class="sxs-lookup"><span data-stu-id="410b5-267">False</span></span>                             |
| <span data-ttu-id="410b5-268">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="410b5-268">In Global Catalog</span></span>      | <span data-ttu-id="410b5-269">Falso</span><span class="sxs-lookup"><span data-stu-id="410b5-269">False</span></span>                             |
| <span data-ttu-id="410b5-270">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="410b5-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="410b5-271">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="410b5-271">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="410b5-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="410b5-272">Range-Lower</span></span>            | <span data-ttu-id="410b5-273">0</span><span class="sxs-lookup"><span data-stu-id="410b5-273">0</span></span>                                 |
| <span data-ttu-id="410b5-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="410b5-274">Range-Upper</span></span>            | <span data-ttu-id="410b5-275">65535</span><span class="sxs-lookup"><span data-stu-id="410b5-275">65535</span></span>                             |
| <span data-ttu-id="410b5-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="410b5-276">Search-Flags</span></span>           | <span data-ttu-id="410b5-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="410b5-277">0x00000010</span></span>                        |
| <span data-ttu-id="410b5-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="410b5-278">System-Flags</span></span>           | <span data-ttu-id="410b5-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="410b5-279">0x00000010</span></span>                        |
| <span data-ttu-id="410b5-280">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="410b5-280">Classes used in</span></span>        | [<span data-ttu-id="410b5-281">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="410b5-281">**User**</span></span>](c-user.md)<br/> |



 

 





