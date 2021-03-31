---
title: Atributo Shell-Property-Pages
description: O número do pedido e o GUID das páginas de propriedades para gerenciar Active Directory objetos. Essas páginas de propriedades podem ser acessadas no Shell do Windows. Para obter mais informações, consulte o documento, estendendo a interface do usuário para objetos de diretório.
ms.assetid: e0edd91b-bdb6-47aa-9be2-8a23a89adb26
ms.tgt_platform: multiple
keywords:
- Esquema de atributos de propriedade Shell-Property-Pages
- Esquema de AD do atributo shellPropertyPages
topic_type:
- apiref
api_name:
- Shell-Property-Pages
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: befad2334a754843fa0ae412565db8c82260f7cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086837"
---
# <a name="shell-property-pages-attribute"></a><span data-ttu-id="370a6-107">Atributo Shell-Property-Pages</span><span class="sxs-lookup"><span data-stu-id="370a6-107">Shell-Property-Pages attribute</span></span>

<span data-ttu-id="370a6-108">O número do pedido e o GUID das páginas de propriedades para gerenciar Active Directory objetos.</span><span class="sxs-lookup"><span data-stu-id="370a6-108">The order number and GUID of property pages for managing Active Directory objects.</span></span> <span data-ttu-id="370a6-109">Essas páginas de propriedades podem ser acessadas no Shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="370a6-109">These property pages can be accessed from the Windows shell.</span></span> <span data-ttu-id="370a6-110">Para obter mais informações, consulte o documento, estendendo a interface do usuário para objetos de diretório.</span><span class="sxs-lookup"><span data-stu-id="370a6-110">For more information see the document, Extending the User Interface for Directory Objects.</span></span>



| <span data-ttu-id="370a6-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="370a6-111">Entry</span></span> | <span data-ttu-id="370a6-112">Valor</span><span class="sxs-lookup"><span data-stu-id="370a6-112">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="370a6-113">CN</span><span class="sxs-lookup"><span data-stu-id="370a6-113">CN</span></span>                | <span data-ttu-id="370a6-114">Páginas de propriedades do Shell</span><span class="sxs-lookup"><span data-stu-id="370a6-114">Shell-Property-Pages</span></span>                           |
| <span data-ttu-id="370a6-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="370a6-115">Ldap-Display-Name</span></span> | <span data-ttu-id="370a6-116">shellPropertyPages</span><span class="sxs-lookup"><span data-stu-id="370a6-116">shellPropertyPages</span></span>                             |
| <span data-ttu-id="370a6-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="370a6-117">Size</span></span>              | \-                                             |
| <span data-ttu-id="370a6-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="370a6-118">Update Privilege</span></span>  | <span data-ttu-id="370a6-119">Administrador de domínio ou desenvolvedor de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="370a6-119">Domain administrator or application developer.</span></span> |
| <span data-ttu-id="370a6-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="370a6-120">Update Frequency</span></span>  | <span data-ttu-id="370a6-121">Sempre que uma página de propriedades é adicionada ou removida.</span><span class="sxs-lookup"><span data-stu-id="370a6-121">Whenever a property page is added or removed.</span></span>  |
| <span data-ttu-id="370a6-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="370a6-122">Attribute-Id</span></span>      | <span data-ttu-id="370a6-123">1.2.840.113556.1.4.563</span><span class="sxs-lookup"><span data-stu-id="370a6-123">1.2.840.113556.1.4.563</span></span>                         |
| <span data-ttu-id="370a6-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="370a6-124">System-Id-Guid</span></span>    | <span data-ttu-id="370a6-125">52458039-ca6a-11D0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="370a6-125">52458039-ca6a-11d0-afff-0000f80367c1</span></span>           |
| <span data-ttu-id="370a6-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="370a6-126">Syntax</span></span>            | [<span data-ttu-id="370a6-127">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="370a6-127">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="370a6-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="370a6-128">Implementations</span></span>

-   [<span data-ttu-id="370a6-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="370a6-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="370a6-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="370a6-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="370a6-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="370a6-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="370a6-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="370a6-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="370a6-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="370a6-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="370a6-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="370a6-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="370a6-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="370a6-135">Windows 2000 Server</span></span>



| <span data-ttu-id="370a6-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="370a6-136">Entry</span></span> | <span data-ttu-id="370a6-137">Valor</span><span class="sxs-lookup"><span data-stu-id="370a6-137">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="370a6-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="370a6-138">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="370a6-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="370a6-139">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="370a6-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="370a6-140">System-Only</span></span>            | <span data-ttu-id="370a6-141">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-141">False</span></span>                                                      |
| <span data-ttu-id="370a6-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="370a6-142">Is-Single-Valued</span></span>       | <span data-ttu-id="370a6-143">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-143">False</span></span>                                                      |
| <span data-ttu-id="370a6-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="370a6-144">Is Indexed</span></span>             | <span data-ttu-id="370a6-145">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-145">False</span></span>                                                      |
| <span data-ttu-id="370a6-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="370a6-146">In Global Catalog</span></span>      | <span data-ttu-id="370a6-147">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-147">False</span></span>                                                      |
| <span data-ttu-id="370a6-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="370a6-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="370a6-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="370a6-149">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="370a6-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="370a6-150">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="370a6-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="370a6-151">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="370a6-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="370a6-152">Search-Flags</span></span>           | <span data-ttu-id="370a6-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="370a6-153">0x00000000</span></span>                                                 |
| <span data-ttu-id="370a6-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="370a6-154">System-Flags</span></span>           | <span data-ttu-id="370a6-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="370a6-155">0x00000010</span></span>                                                 |
| <span data-ttu-id="370a6-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="370a6-156">Classes used in</span></span>        | [<span data-ttu-id="370a6-157">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="370a6-157">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="370a6-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="370a6-158">Windows Server 2003</span></span>



| <span data-ttu-id="370a6-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="370a6-159">Entry</span></span> | <span data-ttu-id="370a6-160">Valor</span><span class="sxs-lookup"><span data-stu-id="370a6-160">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="370a6-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="370a6-161">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="370a6-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="370a6-162">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="370a6-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="370a6-163">System-Only</span></span>            | <span data-ttu-id="370a6-164">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-164">False</span></span>                                                      |
| <span data-ttu-id="370a6-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="370a6-165">Is-Single-Valued</span></span>       | <span data-ttu-id="370a6-166">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-166">False</span></span>                                                      |
| <span data-ttu-id="370a6-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="370a6-167">Is Indexed</span></span>             | <span data-ttu-id="370a6-168">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-168">False</span></span>                                                      |
| <span data-ttu-id="370a6-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="370a6-169">In Global Catalog</span></span>      | <span data-ttu-id="370a6-170">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-170">False</span></span>                                                      |
| <span data-ttu-id="370a6-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="370a6-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="370a6-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="370a6-172">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="370a6-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="370a6-173">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="370a6-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="370a6-174">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="370a6-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="370a6-175">Search-Flags</span></span>           | <span data-ttu-id="370a6-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="370a6-176">0x00000000</span></span>                                                 |
| <span data-ttu-id="370a6-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="370a6-177">System-Flags</span></span>           | <span data-ttu-id="370a6-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="370a6-178">0x00000010</span></span>                                                 |
| <span data-ttu-id="370a6-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="370a6-179">Classes used in</span></span>        | [<span data-ttu-id="370a6-180">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="370a6-180">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="370a6-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="370a6-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="370a6-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="370a6-182">Entry</span></span> | <span data-ttu-id="370a6-183">Valor</span><span class="sxs-lookup"><span data-stu-id="370a6-183">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="370a6-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="370a6-184">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="370a6-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="370a6-185">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="370a6-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="370a6-186">System-Only</span></span>            | <span data-ttu-id="370a6-187">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-187">False</span></span>                                                      |
| <span data-ttu-id="370a6-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="370a6-188">Is-Single-Valued</span></span>       | <span data-ttu-id="370a6-189">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-189">False</span></span>                                                      |
| <span data-ttu-id="370a6-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="370a6-190">Is Indexed</span></span>             | <span data-ttu-id="370a6-191">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-191">False</span></span>                                                      |
| <span data-ttu-id="370a6-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="370a6-192">In Global Catalog</span></span>      | <span data-ttu-id="370a6-193">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-193">False</span></span>                                                      |
| <span data-ttu-id="370a6-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="370a6-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="370a6-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="370a6-195">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="370a6-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="370a6-196">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="370a6-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="370a6-197">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="370a6-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="370a6-198">Search-Flags</span></span>           | <span data-ttu-id="370a6-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="370a6-199">0x00000000</span></span>                                                 |
| <span data-ttu-id="370a6-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="370a6-200">System-Flags</span></span>           | <span data-ttu-id="370a6-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="370a6-201">0x00000010</span></span>                                                 |
| <span data-ttu-id="370a6-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="370a6-202">Classes used in</span></span>        | [<span data-ttu-id="370a6-203">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="370a6-203">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="370a6-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="370a6-204">Windows Server 2008</span></span>



| <span data-ttu-id="370a6-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="370a6-205">Entry</span></span> | <span data-ttu-id="370a6-206">Valor</span><span class="sxs-lookup"><span data-stu-id="370a6-206">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="370a6-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="370a6-207">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="370a6-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="370a6-208">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="370a6-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="370a6-209">System-Only</span></span>            | <span data-ttu-id="370a6-210">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-210">False</span></span>                                                      |
| <span data-ttu-id="370a6-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="370a6-211">Is-Single-Valued</span></span>       | <span data-ttu-id="370a6-212">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-212">False</span></span>                                                      |
| <span data-ttu-id="370a6-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="370a6-213">Is Indexed</span></span>             | <span data-ttu-id="370a6-214">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-214">False</span></span>                                                      |
| <span data-ttu-id="370a6-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="370a6-215">In Global Catalog</span></span>      | <span data-ttu-id="370a6-216">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-216">False</span></span>                                                      |
| <span data-ttu-id="370a6-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="370a6-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="370a6-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="370a6-218">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="370a6-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="370a6-219">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="370a6-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="370a6-220">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="370a6-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="370a6-221">Search-Flags</span></span>           | <span data-ttu-id="370a6-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="370a6-222">0x00000000</span></span>                                                 |
| <span data-ttu-id="370a6-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="370a6-223">System-Flags</span></span>           | <span data-ttu-id="370a6-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="370a6-224">0x00000010</span></span>                                                 |
| <span data-ttu-id="370a6-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="370a6-225">Classes used in</span></span>        | [<span data-ttu-id="370a6-226">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="370a6-226">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="370a6-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="370a6-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="370a6-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="370a6-228">Entry</span></span> | <span data-ttu-id="370a6-229">Valor</span><span class="sxs-lookup"><span data-stu-id="370a6-229">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="370a6-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="370a6-230">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="370a6-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="370a6-231">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="370a6-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="370a6-232">System-Only</span></span>            | <span data-ttu-id="370a6-233">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-233">False</span></span>                                                      |
| <span data-ttu-id="370a6-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="370a6-234">Is-Single-Valued</span></span>       | <span data-ttu-id="370a6-235">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-235">False</span></span>                                                      |
| <span data-ttu-id="370a6-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="370a6-236">Is Indexed</span></span>             | <span data-ttu-id="370a6-237">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-237">False</span></span>                                                      |
| <span data-ttu-id="370a6-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="370a6-238">In Global Catalog</span></span>      | <span data-ttu-id="370a6-239">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-239">False</span></span>                                                      |
| <span data-ttu-id="370a6-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="370a6-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="370a6-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="370a6-241">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="370a6-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="370a6-242">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="370a6-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="370a6-243">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="370a6-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="370a6-244">Search-Flags</span></span>           | <span data-ttu-id="370a6-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="370a6-245">0x00000000</span></span>                                                 |
| <span data-ttu-id="370a6-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="370a6-246">System-Flags</span></span>           | <span data-ttu-id="370a6-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="370a6-247">0x00000010</span></span>                                                 |
| <span data-ttu-id="370a6-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="370a6-248">Classes used in</span></span>        | [<span data-ttu-id="370a6-249">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="370a6-249">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="370a6-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="370a6-250">Windows Server 2012</span></span>



| <span data-ttu-id="370a6-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="370a6-251">Entry</span></span> | <span data-ttu-id="370a6-252">Valor</span><span class="sxs-lookup"><span data-stu-id="370a6-252">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="370a6-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="370a6-253">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="370a6-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="370a6-254">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="370a6-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="370a6-255">System-Only</span></span>            | <span data-ttu-id="370a6-256">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-256">False</span></span>                                                      |
| <span data-ttu-id="370a6-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="370a6-257">Is-Single-Valued</span></span>       | <span data-ttu-id="370a6-258">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-258">False</span></span>                                                      |
| <span data-ttu-id="370a6-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="370a6-259">Is Indexed</span></span>             | <span data-ttu-id="370a6-260">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-260">False</span></span>                                                      |
| <span data-ttu-id="370a6-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="370a6-261">In Global Catalog</span></span>      | <span data-ttu-id="370a6-262">Falso</span><span class="sxs-lookup"><span data-stu-id="370a6-262">False</span></span>                                                      |
| <span data-ttu-id="370a6-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="370a6-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="370a6-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="370a6-264">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="370a6-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="370a6-265">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="370a6-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="370a6-266">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="370a6-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="370a6-267">Search-Flags</span></span>           | <span data-ttu-id="370a6-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="370a6-268">0x00000000</span></span>                                                 |
| <span data-ttu-id="370a6-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="370a6-269">System-Flags</span></span>           | <span data-ttu-id="370a6-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="370a6-270">0x00000010</span></span>                                                 |
| <span data-ttu-id="370a6-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="370a6-271">Classes used in</span></span>        | [<span data-ttu-id="370a6-272">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="370a6-272">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





