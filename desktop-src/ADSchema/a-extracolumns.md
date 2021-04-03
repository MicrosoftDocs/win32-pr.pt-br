---
title: Extra-Columns atributo
description: Este é um atributo com vários valores, cujo valor consiste em uma tupla de 5 (nome do atributo), (título da coluna), (visibilidade padrão (0, 1)), (largura da coluna (\ 8211; 1 para largura automática)), 0 (reservado para uso futuro deve ser zero).
ms.assetid: aafe4657-0295-4af2-a7d0-8c7561516e17
ms.tgt_platform: multiple
keywords:
- Esquema de Extra-Columns do atributo AD
- Esquema de AD do atributo extraColumns
topic_type:
- apiref
api_name:
- Extra-Columns
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0bc74532296c5e0f23da9635bb26df299ae60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645369"
---
# <a name="extra-columns-attribute"></a><span data-ttu-id="67b87-105">Extra-Columns atributo</span><span class="sxs-lookup"><span data-stu-id="67b87-105">Extra-Columns attribute</span></span>

<span data-ttu-id="67b87-106">Este é um atributo com vários valores, cujo valor consiste em uma tupla de 5: (nome do atributo), (título da coluna), (visibilidade padrão (0, 1)), (largura da coluna (1 para largura automática)), 0 (reservado para uso futuro deve ser zero).</span><span class="sxs-lookup"><span data-stu-id="67b87-106">This is a multivalued attribute whose values consist of a 5 tuple: (attribute name), (column title), (default visibility (0,1)), (column width ( 1 for auto width)), 0 (reserved for future use must be zero).</span></span> <span data-ttu-id="67b87-107">Esse valor é usado pelo console usuários e computadores do AD.</span><span class="sxs-lookup"><span data-stu-id="67b87-107">This value is used by the AD Users and Computers console.</span></span>



| <span data-ttu-id="67b87-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="67b87-108">Entry</span></span> | <span data-ttu-id="67b87-109">Valor</span><span class="sxs-lookup"><span data-stu-id="67b87-109">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67b87-110">CN</span><span class="sxs-lookup"><span data-stu-id="67b87-110">CN</span></span>                | <span data-ttu-id="67b87-111">Extra-Columns</span><span class="sxs-lookup"><span data-stu-id="67b87-111">Extra-Columns</span></span>                                                                                                                                                        |
| <span data-ttu-id="67b87-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="67b87-112">Ldap-Display-Name</span></span> | <span data-ttu-id="67b87-113">extraColumns</span><span class="sxs-lookup"><span data-stu-id="67b87-113">extraColumns</span></span>                                                                                                                                                         |
| <span data-ttu-id="67b87-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="67b87-114">Size</span></span>              | <span data-ttu-id="67b87-115">Cada valor seria o tamanho da cadeia de caracteres da tupla de 5.</span><span class="sxs-lookup"><span data-stu-id="67b87-115">Each value would be the size of the string of the 5 tuple above.</span></span> <span data-ttu-id="67b87-116">Por padrão, haverá 22 valores no objeto de exibição padrão no contêiner DisplaySpecifier.</span><span class="sxs-lookup"><span data-stu-id="67b87-116">By default there will be 22 values on the default-Display object in the DisplaySpecifier container.</span></span> |
| <span data-ttu-id="67b87-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="67b87-117">Update Privilege</span></span>  | <span data-ttu-id="67b87-118">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="67b87-118">Domain administrator</span></span>                                                                                                                                                 |
| <span data-ttu-id="67b87-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="67b87-119">Update Frequency</span></span>  | <span data-ttu-id="67b87-120">Isso só será atualizado se um serviço como o Exchange estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="67b87-120">This will only be updated if a service like Exchange is installed.</span></span>                                                                                                   |
| <span data-ttu-id="67b87-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="67b87-121">Attribute-Id</span></span>      | <span data-ttu-id="67b87-122">1.2.840.113556.1.4.1687</span><span class="sxs-lookup"><span data-stu-id="67b87-122">1.2.840.113556.1.4.1687</span></span>                                                                                                                                              |
| <span data-ttu-id="67b87-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="67b87-123">System-Id-Guid</span></span>    | <span data-ttu-id="67b87-124">d24e2846-1dd9-4bcf-99d7-a6227cc86da7</span><span class="sxs-lookup"><span data-stu-id="67b87-124">d24e2846-1dd9-4bcf-99d7-a6227cc86da7</span></span>                                                                                                                                 |
| <span data-ttu-id="67b87-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="67b87-125">Syntax</span></span>            | [<span data-ttu-id="67b87-126">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="67b87-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                                                          |



## <a name="implementations"></a><span data-ttu-id="67b87-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="67b87-127">Implementations</span></span>

-   [<span data-ttu-id="67b87-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="67b87-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="67b87-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="67b87-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="67b87-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="67b87-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="67b87-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="67b87-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="67b87-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="67b87-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="67b87-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="67b87-133">Windows Server 2003</span></span>



| <span data-ttu-id="67b87-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="67b87-134">Entry</span></span> | <span data-ttu-id="67b87-135">Valor</span><span class="sxs-lookup"><span data-stu-id="67b87-135">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="67b87-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="67b87-136">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="67b87-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67b87-137">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="67b87-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="67b87-138">System-Only</span></span>            | <span data-ttu-id="67b87-139">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-139">False</span></span>                                                      |
| <span data-ttu-id="67b87-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="67b87-140">Is-Single-Valued</span></span>       | <span data-ttu-id="67b87-141">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-141">False</span></span>                                                      |
| <span data-ttu-id="67b87-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="67b87-142">Is Indexed</span></span>             | <span data-ttu-id="67b87-143">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-143">False</span></span>                                                      |
| <span data-ttu-id="67b87-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="67b87-144">In Global Catalog</span></span>      | <span data-ttu-id="67b87-145">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-145">False</span></span>                                                      |
| <span data-ttu-id="67b87-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="67b87-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="67b87-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="67b87-147">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="67b87-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67b87-148">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="67b87-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67b87-149">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="67b87-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67b87-150">Search-Flags</span></span>           | <span data-ttu-id="67b87-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67b87-151">0x00000000</span></span>                                                 |
| <span data-ttu-id="67b87-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67b87-152">System-Flags</span></span>           | <span data-ttu-id="67b87-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67b87-153">0x00000010</span></span>                                                 |
| <span data-ttu-id="67b87-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="67b87-154">Classes used in</span></span>        | [<span data-ttu-id="67b87-155">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="67b87-155">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="67b87-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="67b87-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="67b87-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="67b87-157">Entry</span></span> | <span data-ttu-id="67b87-158">Valor</span><span class="sxs-lookup"><span data-stu-id="67b87-158">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="67b87-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="67b87-159">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="67b87-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67b87-160">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="67b87-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="67b87-161">System-Only</span></span>            | <span data-ttu-id="67b87-162">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-162">False</span></span>                                                      |
| <span data-ttu-id="67b87-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="67b87-163">Is-Single-Valued</span></span>       | <span data-ttu-id="67b87-164">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-164">False</span></span>                                                      |
| <span data-ttu-id="67b87-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="67b87-165">Is Indexed</span></span>             | <span data-ttu-id="67b87-166">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-166">False</span></span>                                                      |
| <span data-ttu-id="67b87-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="67b87-167">In Global Catalog</span></span>      | <span data-ttu-id="67b87-168">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-168">False</span></span>                                                      |
| <span data-ttu-id="67b87-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="67b87-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="67b87-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="67b87-170">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="67b87-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67b87-171">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="67b87-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67b87-172">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="67b87-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67b87-173">Search-Flags</span></span>           | <span data-ttu-id="67b87-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67b87-174">0x00000000</span></span>                                                 |
| <span data-ttu-id="67b87-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67b87-175">System-Flags</span></span>           | <span data-ttu-id="67b87-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67b87-176">0x00000010</span></span>                                                 |
| <span data-ttu-id="67b87-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="67b87-177">Classes used in</span></span>        | [<span data-ttu-id="67b87-178">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="67b87-178">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="67b87-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67b87-179">Windows Server 2008</span></span>



| <span data-ttu-id="67b87-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="67b87-180">Entry</span></span> | <span data-ttu-id="67b87-181">Valor</span><span class="sxs-lookup"><span data-stu-id="67b87-181">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="67b87-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="67b87-182">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="67b87-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67b87-183">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="67b87-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="67b87-184">System-Only</span></span>            | <span data-ttu-id="67b87-185">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-185">False</span></span>                                                      |
| <span data-ttu-id="67b87-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="67b87-186">Is-Single-Valued</span></span>       | <span data-ttu-id="67b87-187">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-187">False</span></span>                                                      |
| <span data-ttu-id="67b87-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="67b87-188">Is Indexed</span></span>             | <span data-ttu-id="67b87-189">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-189">False</span></span>                                                      |
| <span data-ttu-id="67b87-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="67b87-190">In Global Catalog</span></span>      | <span data-ttu-id="67b87-191">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-191">False</span></span>                                                      |
| <span data-ttu-id="67b87-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="67b87-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="67b87-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="67b87-193">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="67b87-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67b87-194">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="67b87-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67b87-195">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="67b87-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67b87-196">Search-Flags</span></span>           | <span data-ttu-id="67b87-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67b87-197">0x00000000</span></span>                                                 |
| <span data-ttu-id="67b87-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67b87-198">System-Flags</span></span>           | <span data-ttu-id="67b87-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67b87-199">0x00000010</span></span>                                                 |
| <span data-ttu-id="67b87-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="67b87-200">Classes used in</span></span>        | [<span data-ttu-id="67b87-201">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="67b87-201">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="67b87-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="67b87-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="67b87-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="67b87-203">Entry</span></span> | <span data-ttu-id="67b87-204">Valor</span><span class="sxs-lookup"><span data-stu-id="67b87-204">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="67b87-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="67b87-205">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="67b87-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67b87-206">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="67b87-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="67b87-207">System-Only</span></span>            | <span data-ttu-id="67b87-208">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-208">False</span></span>                                                      |
| <span data-ttu-id="67b87-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="67b87-209">Is-Single-Valued</span></span>       | <span data-ttu-id="67b87-210">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-210">False</span></span>                                                      |
| <span data-ttu-id="67b87-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="67b87-211">Is Indexed</span></span>             | <span data-ttu-id="67b87-212">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-212">False</span></span>                                                      |
| <span data-ttu-id="67b87-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="67b87-213">In Global Catalog</span></span>      | <span data-ttu-id="67b87-214">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-214">False</span></span>                                                      |
| <span data-ttu-id="67b87-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="67b87-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="67b87-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="67b87-216">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="67b87-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67b87-217">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="67b87-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67b87-218">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="67b87-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67b87-219">Search-Flags</span></span>           | <span data-ttu-id="67b87-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67b87-220">0x00000000</span></span>                                                 |
| <span data-ttu-id="67b87-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67b87-221">System-Flags</span></span>           | <span data-ttu-id="67b87-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67b87-222">0x00000010</span></span>                                                 |
| <span data-ttu-id="67b87-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="67b87-223">Classes used in</span></span>        | [<span data-ttu-id="67b87-224">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="67b87-224">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="67b87-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="67b87-225">Windows Server 2012</span></span>



| <span data-ttu-id="67b87-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="67b87-226">Entry</span></span> | <span data-ttu-id="67b87-227">Valor</span><span class="sxs-lookup"><span data-stu-id="67b87-227">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="67b87-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="67b87-228">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="67b87-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="67b87-229">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="67b87-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="67b87-230">System-Only</span></span>            | <span data-ttu-id="67b87-231">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-231">False</span></span>                                                      |
| <span data-ttu-id="67b87-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="67b87-232">Is-Single-Valued</span></span>       | <span data-ttu-id="67b87-233">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-233">False</span></span>                                                      |
| <span data-ttu-id="67b87-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="67b87-234">Is Indexed</span></span>             | <span data-ttu-id="67b87-235">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-235">False</span></span>                                                      |
| <span data-ttu-id="67b87-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="67b87-236">In Global Catalog</span></span>      | <span data-ttu-id="67b87-237">Falso</span><span class="sxs-lookup"><span data-stu-id="67b87-237">False</span></span>                                                      |
| <span data-ttu-id="67b87-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="67b87-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="67b87-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="67b87-239">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="67b87-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="67b87-240">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="67b87-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="67b87-241">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="67b87-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="67b87-242">Search-Flags</span></span>           | <span data-ttu-id="67b87-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="67b87-243">0x00000000</span></span>                                                 |
| <span data-ttu-id="67b87-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="67b87-244">System-Flags</span></span>           | <span data-ttu-id="67b87-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="67b87-245">0x00000010</span></span>                                                 |
| <span data-ttu-id="67b87-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="67b87-246">Classes used in</span></span>        | [<span data-ttu-id="67b87-247">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="67b87-247">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





