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
# <a name="shell-property-pages-attribute"></a><span data-ttu-id="17a32-107">Atributo Shell-Property-Pages</span><span class="sxs-lookup"><span data-stu-id="17a32-107">Shell-Property-Pages attribute</span></span>

<span data-ttu-id="17a32-108">O número do pedido e o GUID das páginas de propriedades para gerenciar Active Directory objetos.</span><span class="sxs-lookup"><span data-stu-id="17a32-108">The order number and GUID of property pages for managing Active Directory objects.</span></span> <span data-ttu-id="17a32-109">Essas páginas de propriedades podem ser acessadas no Shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="17a32-109">These property pages can be accessed from the Windows shell.</span></span> <span data-ttu-id="17a32-110">Para obter mais informações, consulte o documento, estendendo a interface do usuário para objetos de diretório.</span><span class="sxs-lookup"><span data-stu-id="17a32-110">For more information see the document, Extending the User Interface for Directory Objects.</span></span>



| <span data-ttu-id="17a32-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="17a32-111">Entry</span></span> | <span data-ttu-id="17a32-112">Valor</span><span class="sxs-lookup"><span data-stu-id="17a32-112">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="17a32-113">CN</span><span class="sxs-lookup"><span data-stu-id="17a32-113">CN</span></span>                | <span data-ttu-id="17a32-114">Páginas de propriedades do Shell</span><span class="sxs-lookup"><span data-stu-id="17a32-114">Shell-Property-Pages</span></span>                           |
| <span data-ttu-id="17a32-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="17a32-115">Ldap-Display-Name</span></span> | <span data-ttu-id="17a32-116">shellPropertyPages</span><span class="sxs-lookup"><span data-stu-id="17a32-116">shellPropertyPages</span></span>                             |
| <span data-ttu-id="17a32-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="17a32-117">Size</span></span>              | \-                                             |
| <span data-ttu-id="17a32-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="17a32-118">Update Privilege</span></span>  | <span data-ttu-id="17a32-119">Administrador de domínio ou desenvolvedor de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="17a32-119">Domain administrator or application developer.</span></span> |
| <span data-ttu-id="17a32-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="17a32-120">Update Frequency</span></span>  | <span data-ttu-id="17a32-121">Sempre que uma página de propriedades é adicionada ou removida.</span><span class="sxs-lookup"><span data-stu-id="17a32-121">Whenever a property page is added or removed.</span></span>  |
| <span data-ttu-id="17a32-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="17a32-122">Attribute-Id</span></span>      | <span data-ttu-id="17a32-123">1.2.840.113556.1.4.563</span><span class="sxs-lookup"><span data-stu-id="17a32-123">1.2.840.113556.1.4.563</span></span>                         |
| <span data-ttu-id="17a32-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="17a32-124">System-Id-Guid</span></span>    | <span data-ttu-id="17a32-125">52458039-ca6a-11D0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="17a32-125">52458039-ca6a-11d0-afff-0000f80367c1</span></span>           |
| <span data-ttu-id="17a32-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="17a32-126">Syntax</span></span>            | [<span data-ttu-id="17a32-127">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="17a32-127">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="17a32-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="17a32-128">Implementations</span></span>

-   [<span data-ttu-id="17a32-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="17a32-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="17a32-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="17a32-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="17a32-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="17a32-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="17a32-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="17a32-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="17a32-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="17a32-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="17a32-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="17a32-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="17a32-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="17a32-135">Windows 2000 Server</span></span>



| <span data-ttu-id="17a32-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="17a32-136">Entry</span></span> | <span data-ttu-id="17a32-137">Valor</span><span class="sxs-lookup"><span data-stu-id="17a32-137">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="17a32-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="17a32-138">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="17a32-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17a32-139">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="17a32-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="17a32-140">System-Only</span></span>            | <span data-ttu-id="17a32-141">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-141">False</span></span>                                                      |
| <span data-ttu-id="17a32-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17a32-142">Is-Single-Valued</span></span>       | <span data-ttu-id="17a32-143">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-143">False</span></span>                                                      |
| <span data-ttu-id="17a32-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="17a32-144">Is Indexed</span></span>             | <span data-ttu-id="17a32-145">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-145">False</span></span>                                                      |
| <span data-ttu-id="17a32-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17a32-146">In Global Catalog</span></span>      | <span data-ttu-id="17a32-147">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-147">False</span></span>                                                      |
| <span data-ttu-id="17a32-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17a32-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="17a32-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17a32-149">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="17a32-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17a32-150">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="17a32-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17a32-151">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="17a32-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17a32-152">Search-Flags</span></span>           | <span data-ttu-id="17a32-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17a32-153">0x00000000</span></span>                                                 |
| <span data-ttu-id="17a32-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17a32-154">System-Flags</span></span>           | <span data-ttu-id="17a32-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17a32-155">0x00000010</span></span>                                                 |
| <span data-ttu-id="17a32-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17a32-156">Classes used in</span></span>        | [<span data-ttu-id="17a32-157">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="17a32-157">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="17a32-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="17a32-158">Windows Server 2003</span></span>



| <span data-ttu-id="17a32-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="17a32-159">Entry</span></span> | <span data-ttu-id="17a32-160">Valor</span><span class="sxs-lookup"><span data-stu-id="17a32-160">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="17a32-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="17a32-161">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="17a32-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17a32-162">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="17a32-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="17a32-163">System-Only</span></span>            | <span data-ttu-id="17a32-164">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-164">False</span></span>                                                      |
| <span data-ttu-id="17a32-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17a32-165">Is-Single-Valued</span></span>       | <span data-ttu-id="17a32-166">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-166">False</span></span>                                                      |
| <span data-ttu-id="17a32-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="17a32-167">Is Indexed</span></span>             | <span data-ttu-id="17a32-168">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-168">False</span></span>                                                      |
| <span data-ttu-id="17a32-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17a32-169">In Global Catalog</span></span>      | <span data-ttu-id="17a32-170">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-170">False</span></span>                                                      |
| <span data-ttu-id="17a32-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17a32-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="17a32-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17a32-172">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="17a32-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17a32-173">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="17a32-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17a32-174">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="17a32-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17a32-175">Search-Flags</span></span>           | <span data-ttu-id="17a32-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17a32-176">0x00000000</span></span>                                                 |
| <span data-ttu-id="17a32-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17a32-177">System-Flags</span></span>           | <span data-ttu-id="17a32-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17a32-178">0x00000010</span></span>                                                 |
| <span data-ttu-id="17a32-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17a32-179">Classes used in</span></span>        | [<span data-ttu-id="17a32-180">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="17a32-180">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="17a32-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="17a32-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="17a32-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="17a32-182">Entry</span></span> | <span data-ttu-id="17a32-183">Valor</span><span class="sxs-lookup"><span data-stu-id="17a32-183">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="17a32-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="17a32-184">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="17a32-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17a32-185">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="17a32-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="17a32-186">System-Only</span></span>            | <span data-ttu-id="17a32-187">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-187">False</span></span>                                                      |
| <span data-ttu-id="17a32-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17a32-188">Is-Single-Valued</span></span>       | <span data-ttu-id="17a32-189">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-189">False</span></span>                                                      |
| <span data-ttu-id="17a32-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="17a32-190">Is Indexed</span></span>             | <span data-ttu-id="17a32-191">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-191">False</span></span>                                                      |
| <span data-ttu-id="17a32-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17a32-192">In Global Catalog</span></span>      | <span data-ttu-id="17a32-193">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-193">False</span></span>                                                      |
| <span data-ttu-id="17a32-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17a32-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="17a32-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17a32-195">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="17a32-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17a32-196">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="17a32-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17a32-197">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="17a32-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17a32-198">Search-Flags</span></span>           | <span data-ttu-id="17a32-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17a32-199">0x00000000</span></span>                                                 |
| <span data-ttu-id="17a32-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17a32-200">System-Flags</span></span>           | <span data-ttu-id="17a32-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17a32-201">0x00000010</span></span>                                                 |
| <span data-ttu-id="17a32-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17a32-202">Classes used in</span></span>        | [<span data-ttu-id="17a32-203">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="17a32-203">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="17a32-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17a32-204">Windows Server 2008</span></span>



| <span data-ttu-id="17a32-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="17a32-205">Entry</span></span> | <span data-ttu-id="17a32-206">Valor</span><span class="sxs-lookup"><span data-stu-id="17a32-206">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="17a32-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="17a32-207">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="17a32-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17a32-208">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="17a32-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="17a32-209">System-Only</span></span>            | <span data-ttu-id="17a32-210">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-210">False</span></span>                                                      |
| <span data-ttu-id="17a32-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17a32-211">Is-Single-Valued</span></span>       | <span data-ttu-id="17a32-212">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-212">False</span></span>                                                      |
| <span data-ttu-id="17a32-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="17a32-213">Is Indexed</span></span>             | <span data-ttu-id="17a32-214">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-214">False</span></span>                                                      |
| <span data-ttu-id="17a32-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17a32-215">In Global Catalog</span></span>      | <span data-ttu-id="17a32-216">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-216">False</span></span>                                                      |
| <span data-ttu-id="17a32-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17a32-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="17a32-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17a32-218">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="17a32-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17a32-219">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="17a32-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17a32-220">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="17a32-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17a32-221">Search-Flags</span></span>           | <span data-ttu-id="17a32-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17a32-222">0x00000000</span></span>                                                 |
| <span data-ttu-id="17a32-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17a32-223">System-Flags</span></span>           | <span data-ttu-id="17a32-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17a32-224">0x00000010</span></span>                                                 |
| <span data-ttu-id="17a32-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17a32-225">Classes used in</span></span>        | [<span data-ttu-id="17a32-226">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="17a32-226">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="17a32-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="17a32-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="17a32-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="17a32-228">Entry</span></span> | <span data-ttu-id="17a32-229">Valor</span><span class="sxs-lookup"><span data-stu-id="17a32-229">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="17a32-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="17a32-230">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="17a32-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17a32-231">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="17a32-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="17a32-232">System-Only</span></span>            | <span data-ttu-id="17a32-233">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-233">False</span></span>                                                      |
| <span data-ttu-id="17a32-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17a32-234">Is-Single-Valued</span></span>       | <span data-ttu-id="17a32-235">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-235">False</span></span>                                                      |
| <span data-ttu-id="17a32-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="17a32-236">Is Indexed</span></span>             | <span data-ttu-id="17a32-237">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-237">False</span></span>                                                      |
| <span data-ttu-id="17a32-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17a32-238">In Global Catalog</span></span>      | <span data-ttu-id="17a32-239">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-239">False</span></span>                                                      |
| <span data-ttu-id="17a32-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17a32-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="17a32-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17a32-241">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="17a32-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17a32-242">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="17a32-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17a32-243">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="17a32-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17a32-244">Search-Flags</span></span>           | <span data-ttu-id="17a32-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17a32-245">0x00000000</span></span>                                                 |
| <span data-ttu-id="17a32-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17a32-246">System-Flags</span></span>           | <span data-ttu-id="17a32-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17a32-247">0x00000010</span></span>                                                 |
| <span data-ttu-id="17a32-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17a32-248">Classes used in</span></span>        | [<span data-ttu-id="17a32-249">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="17a32-249">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="17a32-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17a32-250">Windows Server 2012</span></span>



| <span data-ttu-id="17a32-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="17a32-251">Entry</span></span> | <span data-ttu-id="17a32-252">Valor</span><span class="sxs-lookup"><span data-stu-id="17a32-252">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="17a32-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="17a32-253">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="17a32-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17a32-254">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="17a32-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="17a32-255">System-Only</span></span>            | <span data-ttu-id="17a32-256">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-256">False</span></span>                                                      |
| <span data-ttu-id="17a32-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17a32-257">Is-Single-Valued</span></span>       | <span data-ttu-id="17a32-258">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-258">False</span></span>                                                      |
| <span data-ttu-id="17a32-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="17a32-259">Is Indexed</span></span>             | <span data-ttu-id="17a32-260">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-260">False</span></span>                                                      |
| <span data-ttu-id="17a32-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17a32-261">In Global Catalog</span></span>      | <span data-ttu-id="17a32-262">Falso</span><span class="sxs-lookup"><span data-stu-id="17a32-262">False</span></span>                                                      |
| <span data-ttu-id="17a32-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17a32-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="17a32-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17a32-264">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="17a32-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17a32-265">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="17a32-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17a32-266">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="17a32-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17a32-267">Search-Flags</span></span>           | <span data-ttu-id="17a32-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17a32-268">0x00000000</span></span>                                                 |
| <span data-ttu-id="17a32-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17a32-269">System-Flags</span></span>           | <span data-ttu-id="17a32-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17a32-270">0x00000010</span></span>                                                 |
| <span data-ttu-id="17a32-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17a32-271">Classes used in</span></span>        | [<span data-ttu-id="17a32-272">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="17a32-272">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





