---
title: Atributo admin-MultiSelect-Property-Pages
description: Esse é um atributo COM vários valores cujos são um número que representa a ordem na qual as páginas são adicionadas e um GUID de um objeto COM que implementa páginas de propriedades de seleção múltipla para o snap-in usuários e computadores do AD.
ms.assetid: b2b4aafe-ac2d-44b3-80eb-910ba9852bb0
ms.tgt_platform: multiple
keywords:
- Administrador-MultiSelect-Property-Pages atributo AD Schema
- Esquema de AD do atributo adminMultiselectPropertyPages
topic_type:
- apiref
api_name:
- Admin-Multiselect-Property-Pages
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e653568d4f8f6653e4c7dc939c91a7d3cd8b83c6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105769075"
---
# <a name="admin-multiselect-property-pages-attribute"></a><span data-ttu-id="186ff-105">Atributo admin-MultiSelect-Property-Pages</span><span class="sxs-lookup"><span data-stu-id="186ff-105">Admin-Multiselect-Property-Pages attribute</span></span>

<span data-ttu-id="186ff-106">Esse é um atributo COM vários valores cujos são um número que representa a ordem na qual as páginas são adicionadas e um GUID de um objeto COM que implementa páginas de propriedades de seleção múltipla para o snap-in usuários e computadores do AD.</span><span class="sxs-lookup"><span data-stu-id="186ff-106">This is a multivalued attribute whose values are a number that represents the order in which the pages are added and a GUID of a COM object that implements multi-select property pages for the AD Users and Computers snap-in.</span></span>



| <span data-ttu-id="186ff-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="186ff-107">Entry</span></span> | <span data-ttu-id="186ff-108">Valor</span><span class="sxs-lookup"><span data-stu-id="186ff-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="186ff-109">CN</span><span class="sxs-lookup"><span data-stu-id="186ff-109">CN</span></span>                | <span data-ttu-id="186ff-110">Admin – MultiSelect-Property-Pages</span><span class="sxs-lookup"><span data-stu-id="186ff-110">Admin-Multiselect-Property-Pages</span></span>                                                                                                            |
| <span data-ttu-id="186ff-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="186ff-111">Ldap-Display-Name</span></span> | <span data-ttu-id="186ff-112">adminMultiselectPropertyPages</span><span class="sxs-lookup"><span data-stu-id="186ff-112">adminMultiselectPropertyPages</span></span>                                                                                                               |
| <span data-ttu-id="186ff-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="186ff-113">Size</span></span>              | <span data-ttu-id="186ff-114">40 bytes</span><span class="sxs-lookup"><span data-stu-id="186ff-114">40 bytes</span></span>                                                                                                                                    |
| <span data-ttu-id="186ff-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="186ff-115">Update Privilege</span></span>  | <span data-ttu-id="186ff-116">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="186ff-116">Domain administrator</span></span>                                                                                                                        |
| <span data-ttu-id="186ff-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="186ff-117">Update Frequency</span></span>  | <span data-ttu-id="186ff-118">Isso só será atualizado se um serviço, como o Exchange ou Terminal Server estiver instalado, que implemente suas próprias páginas de propriedades de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="186ff-118">This will only be updated if a service like Exchange or Terminal Server is installed that implements their own multi-select property pages.</span></span> |
| <span data-ttu-id="186ff-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="186ff-119">Attribute-Id</span></span>      | <span data-ttu-id="186ff-120">1.2.840.113556.1.4.1690</span><span class="sxs-lookup"><span data-stu-id="186ff-120">1.2.840.113556.1.4.1690</span></span>                                                                                                                     |
| <span data-ttu-id="186ff-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="186ff-121">System-Id-Guid</span></span>    | <span data-ttu-id="186ff-122">18f9b67d-5ac6-4b3b-97db-d0a406afb7ba</span><span class="sxs-lookup"><span data-stu-id="186ff-122">18f9b67d-5ac6-4b3b-97db-d0a406afb7ba</span></span>                                                                                                        |
| <span data-ttu-id="186ff-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="186ff-123">Syntax</span></span>            | [<span data-ttu-id="186ff-124">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="186ff-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                                 |



## <a name="implementations"></a><span data-ttu-id="186ff-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="186ff-125">Implementations</span></span>

-   [<span data-ttu-id="186ff-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="186ff-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="186ff-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="186ff-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="186ff-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="186ff-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="186ff-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="186ff-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="186ff-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="186ff-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="186ff-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="186ff-131">Windows Server 2003</span></span>



| <span data-ttu-id="186ff-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="186ff-132">Entry</span></span> | <span data-ttu-id="186ff-133">Valor</span><span class="sxs-lookup"><span data-stu-id="186ff-133">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="186ff-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="186ff-134">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="186ff-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="186ff-135">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="186ff-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="186ff-136">System-Only</span></span>            | <span data-ttu-id="186ff-137">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-137">False</span></span>                                                      |
| <span data-ttu-id="186ff-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="186ff-138">Is-Single-Valued</span></span>       | <span data-ttu-id="186ff-139">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-139">False</span></span>                                                      |
| <span data-ttu-id="186ff-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="186ff-140">Is Indexed</span></span>             | <span data-ttu-id="186ff-141">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-141">False</span></span>                                                      |
| <span data-ttu-id="186ff-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="186ff-142">In Global Catalog</span></span>      | <span data-ttu-id="186ff-143">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-143">False</span></span>                                                      |
| <span data-ttu-id="186ff-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="186ff-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="186ff-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="186ff-145">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="186ff-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="186ff-146">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="186ff-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="186ff-147">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="186ff-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="186ff-148">Search-Flags</span></span>           | <span data-ttu-id="186ff-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="186ff-149">0x00000000</span></span>                                                 |
| <span data-ttu-id="186ff-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="186ff-150">System-Flags</span></span>           | <span data-ttu-id="186ff-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="186ff-151">0x00000010</span></span>                                                 |
| <span data-ttu-id="186ff-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="186ff-152">Classes used in</span></span>        | [<span data-ttu-id="186ff-153">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="186ff-153">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="186ff-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="186ff-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="186ff-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="186ff-155">Entry</span></span> | <span data-ttu-id="186ff-156">Valor</span><span class="sxs-lookup"><span data-stu-id="186ff-156">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="186ff-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="186ff-157">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="186ff-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="186ff-158">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="186ff-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="186ff-159">System-Only</span></span>            | <span data-ttu-id="186ff-160">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-160">False</span></span>                                                      |
| <span data-ttu-id="186ff-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="186ff-161">Is-Single-Valued</span></span>       | <span data-ttu-id="186ff-162">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-162">False</span></span>                                                      |
| <span data-ttu-id="186ff-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="186ff-163">Is Indexed</span></span>             | <span data-ttu-id="186ff-164">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-164">False</span></span>                                                      |
| <span data-ttu-id="186ff-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="186ff-165">In Global Catalog</span></span>      | <span data-ttu-id="186ff-166">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-166">False</span></span>                                                      |
| <span data-ttu-id="186ff-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="186ff-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="186ff-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="186ff-168">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="186ff-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="186ff-169">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="186ff-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="186ff-170">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="186ff-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="186ff-171">Search-Flags</span></span>           | <span data-ttu-id="186ff-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="186ff-172">0x00000000</span></span>                                                 |
| <span data-ttu-id="186ff-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="186ff-173">System-Flags</span></span>           | <span data-ttu-id="186ff-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="186ff-174">0x00000010</span></span>                                                 |
| <span data-ttu-id="186ff-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="186ff-175">Classes used in</span></span>        | [<span data-ttu-id="186ff-176">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="186ff-176">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="186ff-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="186ff-177">Windows Server 2008</span></span>



| <span data-ttu-id="186ff-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="186ff-178">Entry</span></span> | <span data-ttu-id="186ff-179">Valor</span><span class="sxs-lookup"><span data-stu-id="186ff-179">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="186ff-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="186ff-180">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="186ff-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="186ff-181">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="186ff-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="186ff-182">System-Only</span></span>            | <span data-ttu-id="186ff-183">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-183">False</span></span>                                                      |
| <span data-ttu-id="186ff-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="186ff-184">Is-Single-Valued</span></span>       | <span data-ttu-id="186ff-185">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-185">False</span></span>                                                      |
| <span data-ttu-id="186ff-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="186ff-186">Is Indexed</span></span>             | <span data-ttu-id="186ff-187">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-187">False</span></span>                                                      |
| <span data-ttu-id="186ff-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="186ff-188">In Global Catalog</span></span>      | <span data-ttu-id="186ff-189">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-189">False</span></span>                                                      |
| <span data-ttu-id="186ff-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="186ff-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="186ff-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="186ff-191">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="186ff-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="186ff-192">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="186ff-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="186ff-193">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="186ff-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="186ff-194">Search-Flags</span></span>           | <span data-ttu-id="186ff-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="186ff-195">0x00000000</span></span>                                                 |
| <span data-ttu-id="186ff-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="186ff-196">System-Flags</span></span>           | <span data-ttu-id="186ff-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="186ff-197">0x00000010</span></span>                                                 |
| <span data-ttu-id="186ff-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="186ff-198">Classes used in</span></span>        | [<span data-ttu-id="186ff-199">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="186ff-199">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="186ff-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="186ff-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="186ff-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="186ff-201">Entry</span></span> | <span data-ttu-id="186ff-202">Valor</span><span class="sxs-lookup"><span data-stu-id="186ff-202">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="186ff-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="186ff-203">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="186ff-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="186ff-204">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="186ff-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="186ff-205">System-Only</span></span>            | <span data-ttu-id="186ff-206">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-206">False</span></span>                                                      |
| <span data-ttu-id="186ff-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="186ff-207">Is-Single-Valued</span></span>       | <span data-ttu-id="186ff-208">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-208">False</span></span>                                                      |
| <span data-ttu-id="186ff-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="186ff-209">Is Indexed</span></span>             | <span data-ttu-id="186ff-210">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-210">False</span></span>                                                      |
| <span data-ttu-id="186ff-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="186ff-211">In Global Catalog</span></span>      | <span data-ttu-id="186ff-212">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-212">False</span></span>                                                      |
| <span data-ttu-id="186ff-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="186ff-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="186ff-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="186ff-214">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="186ff-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="186ff-215">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="186ff-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="186ff-216">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="186ff-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="186ff-217">Search-Flags</span></span>           | <span data-ttu-id="186ff-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="186ff-218">0x00000000</span></span>                                                 |
| <span data-ttu-id="186ff-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="186ff-219">System-Flags</span></span>           | <span data-ttu-id="186ff-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="186ff-220">0x00000010</span></span>                                                 |
| <span data-ttu-id="186ff-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="186ff-221">Classes used in</span></span>        | [<span data-ttu-id="186ff-222">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="186ff-222">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="186ff-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="186ff-223">Windows Server 2012</span></span>



| <span data-ttu-id="186ff-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="186ff-224">Entry</span></span> | <span data-ttu-id="186ff-225">Valor</span><span class="sxs-lookup"><span data-stu-id="186ff-225">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="186ff-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="186ff-226">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="186ff-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="186ff-227">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="186ff-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="186ff-228">System-Only</span></span>            | <span data-ttu-id="186ff-229">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-229">False</span></span>                                                      |
| <span data-ttu-id="186ff-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="186ff-230">Is-Single-Valued</span></span>       | <span data-ttu-id="186ff-231">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-231">False</span></span>                                                      |
| <span data-ttu-id="186ff-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="186ff-232">Is Indexed</span></span>             | <span data-ttu-id="186ff-233">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-233">False</span></span>                                                      |
| <span data-ttu-id="186ff-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="186ff-234">In Global Catalog</span></span>      | <span data-ttu-id="186ff-235">Falso</span><span class="sxs-lookup"><span data-stu-id="186ff-235">False</span></span>                                                      |
| <span data-ttu-id="186ff-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="186ff-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="186ff-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="186ff-237">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="186ff-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="186ff-238">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="186ff-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="186ff-239">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="186ff-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="186ff-240">Search-Flags</span></span>           | <span data-ttu-id="186ff-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="186ff-241">0x00000000</span></span>                                                 |
| <span data-ttu-id="186ff-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="186ff-242">System-Flags</span></span>           | <span data-ttu-id="186ff-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="186ff-243">0x00000010</span></span>                                                 |
| <span data-ttu-id="186ff-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="186ff-244">Classes used in</span></span>        | [<span data-ttu-id="186ff-245">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="186ff-245">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





