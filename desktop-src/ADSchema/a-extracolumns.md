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
# <a name="extra-columns-attribute"></a><span data-ttu-id="a56a9-105">Extra-Columns atributo</span><span class="sxs-lookup"><span data-stu-id="a56a9-105">Extra-Columns attribute</span></span>

<span data-ttu-id="a56a9-106">Este é um atributo com vários valores, cujo valor consiste em uma tupla de 5: (nome do atributo), (título da coluna), (visibilidade padrão (0, 1)), (largura da coluna (1 para largura automática)), 0 (reservado para uso futuro deve ser zero).</span><span class="sxs-lookup"><span data-stu-id="a56a9-106">This is a multivalued attribute whose values consist of a 5 tuple: (attribute name), (column title), (default visibility (0,1)), (column width ( 1 for auto width)), 0 (reserved for future use must be zero).</span></span> <span data-ttu-id="a56a9-107">Esse valor é usado pelo console usuários e computadores do AD.</span><span class="sxs-lookup"><span data-stu-id="a56a9-107">This value is used by the AD Users and Computers console.</span></span>



| <span data-ttu-id="a56a9-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="a56a9-108">Entry</span></span> | <span data-ttu-id="a56a9-109">Valor</span><span class="sxs-lookup"><span data-stu-id="a56a9-109">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a56a9-110">CN</span><span class="sxs-lookup"><span data-stu-id="a56a9-110">CN</span></span>                | <span data-ttu-id="a56a9-111">Extra-Columns</span><span class="sxs-lookup"><span data-stu-id="a56a9-111">Extra-Columns</span></span>                                                                                                                                                        |
| <span data-ttu-id="a56a9-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a56a9-112">Ldap-Display-Name</span></span> | <span data-ttu-id="a56a9-113">extraColumns</span><span class="sxs-lookup"><span data-stu-id="a56a9-113">extraColumns</span></span>                                                                                                                                                         |
| <span data-ttu-id="a56a9-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a56a9-114">Size</span></span>              | <span data-ttu-id="a56a9-115">Cada valor seria o tamanho da cadeia de caracteres da tupla de 5.</span><span class="sxs-lookup"><span data-stu-id="a56a9-115">Each value would be the size of the string of the 5 tuple above.</span></span> <span data-ttu-id="a56a9-116">Por padrão, haverá 22 valores no objeto de exibição padrão no contêiner DisplaySpecifier.</span><span class="sxs-lookup"><span data-stu-id="a56a9-116">By default there will be 22 values on the default-Display object in the DisplaySpecifier container.</span></span> |
| <span data-ttu-id="a56a9-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a56a9-117">Update Privilege</span></span>  | <span data-ttu-id="a56a9-118">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="a56a9-118">Domain administrator</span></span>                                                                                                                                                 |
| <span data-ttu-id="a56a9-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a56a9-119">Update Frequency</span></span>  | <span data-ttu-id="a56a9-120">Isso só será atualizado se um serviço como o Exchange estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="a56a9-120">This will only be updated if a service like Exchange is installed.</span></span>                                                                                                   |
| <span data-ttu-id="a56a9-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a56a9-121">Attribute-Id</span></span>      | <span data-ttu-id="a56a9-122">1.2.840.113556.1.4.1687</span><span class="sxs-lookup"><span data-stu-id="a56a9-122">1.2.840.113556.1.4.1687</span></span>                                                                                                                                              |
| <span data-ttu-id="a56a9-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a56a9-123">System-Id-Guid</span></span>    | <span data-ttu-id="a56a9-124">d24e2846-1dd9-4bcf-99d7-a6227cc86da7</span><span class="sxs-lookup"><span data-stu-id="a56a9-124">d24e2846-1dd9-4bcf-99d7-a6227cc86da7</span></span>                                                                                                                                 |
| <span data-ttu-id="a56a9-125">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a56a9-125">Syntax</span></span>            | [<span data-ttu-id="a56a9-126">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a56a9-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                                                          |



## <a name="implementations"></a><span data-ttu-id="a56a9-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="a56a9-127">Implementations</span></span>

-   [<span data-ttu-id="a56a9-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a56a9-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a56a9-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a56a9-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a56a9-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a56a9-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a56a9-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a56a9-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a56a9-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a56a9-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a56a9-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a56a9-133">Windows Server 2003</span></span>



| <span data-ttu-id="a56a9-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="a56a9-134">Entry</span></span> | <span data-ttu-id="a56a9-135">Valor</span><span class="sxs-lookup"><span data-stu-id="a56a9-135">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="a56a9-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="a56a9-136">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="a56a9-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a56a9-137">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="a56a9-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="a56a9-138">System-Only</span></span>            | <span data-ttu-id="a56a9-139">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-139">False</span></span>                                                      |
| <span data-ttu-id="a56a9-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a56a9-140">Is-Single-Valued</span></span>       | <span data-ttu-id="a56a9-141">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-141">False</span></span>                                                      |
| <span data-ttu-id="a56a9-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="a56a9-142">Is Indexed</span></span>             | <span data-ttu-id="a56a9-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-143">False</span></span>                                                      |
| <span data-ttu-id="a56a9-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a56a9-144">In Global Catalog</span></span>      | <span data-ttu-id="a56a9-145">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-145">False</span></span>                                                      |
| <span data-ttu-id="a56a9-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a56a9-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="a56a9-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a56a9-147">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="a56a9-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a56a9-148">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="a56a9-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a56a9-149">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="a56a9-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a56a9-150">Search-Flags</span></span>           | <span data-ttu-id="a56a9-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a56a9-151">0x00000000</span></span>                                                 |
| <span data-ttu-id="a56a9-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a56a9-152">System-Flags</span></span>           | <span data-ttu-id="a56a9-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a56a9-153">0x00000010</span></span>                                                 |
| <span data-ttu-id="a56a9-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a56a9-154">Classes used in</span></span>        | [<span data-ttu-id="a56a9-155">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="a56a9-155">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a56a9-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a56a9-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a56a9-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="a56a9-157">Entry</span></span> | <span data-ttu-id="a56a9-158">Valor</span><span class="sxs-lookup"><span data-stu-id="a56a9-158">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="a56a9-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="a56a9-159">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="a56a9-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a56a9-160">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="a56a9-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a56a9-161">System-Only</span></span>            | <span data-ttu-id="a56a9-162">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-162">False</span></span>                                                      |
| <span data-ttu-id="a56a9-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a56a9-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a56a9-164">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-164">False</span></span>                                                      |
| <span data-ttu-id="a56a9-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="a56a9-165">Is Indexed</span></span>             | <span data-ttu-id="a56a9-166">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-166">False</span></span>                                                      |
| <span data-ttu-id="a56a9-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a56a9-167">In Global Catalog</span></span>      | <span data-ttu-id="a56a9-168">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-168">False</span></span>                                                      |
| <span data-ttu-id="a56a9-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a56a9-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a56a9-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a56a9-170">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="a56a9-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a56a9-171">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="a56a9-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a56a9-172">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="a56a9-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a56a9-173">Search-Flags</span></span>           | <span data-ttu-id="a56a9-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a56a9-174">0x00000000</span></span>                                                 |
| <span data-ttu-id="a56a9-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a56a9-175">System-Flags</span></span>           | <span data-ttu-id="a56a9-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a56a9-176">0x00000010</span></span>                                                 |
| <span data-ttu-id="a56a9-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a56a9-177">Classes used in</span></span>        | [<span data-ttu-id="a56a9-178">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="a56a9-178">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a56a9-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a56a9-179">Windows Server 2008</span></span>



| <span data-ttu-id="a56a9-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="a56a9-180">Entry</span></span> | <span data-ttu-id="a56a9-181">Valor</span><span class="sxs-lookup"><span data-stu-id="a56a9-181">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="a56a9-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="a56a9-182">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="a56a9-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a56a9-183">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="a56a9-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="a56a9-184">System-Only</span></span>            | <span data-ttu-id="a56a9-185">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-185">False</span></span>                                                      |
| <span data-ttu-id="a56a9-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a56a9-186">Is-Single-Valued</span></span>       | <span data-ttu-id="a56a9-187">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-187">False</span></span>                                                      |
| <span data-ttu-id="a56a9-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="a56a9-188">Is Indexed</span></span>             | <span data-ttu-id="a56a9-189">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-189">False</span></span>                                                      |
| <span data-ttu-id="a56a9-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a56a9-190">In Global Catalog</span></span>      | <span data-ttu-id="a56a9-191">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-191">False</span></span>                                                      |
| <span data-ttu-id="a56a9-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a56a9-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="a56a9-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a56a9-193">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="a56a9-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a56a9-194">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="a56a9-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a56a9-195">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="a56a9-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a56a9-196">Search-Flags</span></span>           | <span data-ttu-id="a56a9-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a56a9-197">0x00000000</span></span>                                                 |
| <span data-ttu-id="a56a9-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a56a9-198">System-Flags</span></span>           | <span data-ttu-id="a56a9-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a56a9-199">0x00000010</span></span>                                                 |
| <span data-ttu-id="a56a9-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a56a9-200">Classes used in</span></span>        | [<span data-ttu-id="a56a9-201">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="a56a9-201">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a56a9-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a56a9-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a56a9-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="a56a9-203">Entry</span></span> | <span data-ttu-id="a56a9-204">Valor</span><span class="sxs-lookup"><span data-stu-id="a56a9-204">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="a56a9-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="a56a9-205">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="a56a9-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a56a9-206">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="a56a9-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="a56a9-207">System-Only</span></span>            | <span data-ttu-id="a56a9-208">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-208">False</span></span>                                                      |
| <span data-ttu-id="a56a9-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a56a9-209">Is-Single-Valued</span></span>       | <span data-ttu-id="a56a9-210">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-210">False</span></span>                                                      |
| <span data-ttu-id="a56a9-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="a56a9-211">Is Indexed</span></span>             | <span data-ttu-id="a56a9-212">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-212">False</span></span>                                                      |
| <span data-ttu-id="a56a9-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a56a9-213">In Global Catalog</span></span>      | <span data-ttu-id="a56a9-214">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-214">False</span></span>                                                      |
| <span data-ttu-id="a56a9-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a56a9-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="a56a9-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a56a9-216">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="a56a9-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a56a9-217">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="a56a9-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a56a9-218">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="a56a9-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a56a9-219">Search-Flags</span></span>           | <span data-ttu-id="a56a9-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a56a9-220">0x00000000</span></span>                                                 |
| <span data-ttu-id="a56a9-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a56a9-221">System-Flags</span></span>           | <span data-ttu-id="a56a9-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a56a9-222">0x00000010</span></span>                                                 |
| <span data-ttu-id="a56a9-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a56a9-223">Classes used in</span></span>        | [<span data-ttu-id="a56a9-224">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="a56a9-224">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a56a9-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a56a9-225">Windows Server 2012</span></span>



| <span data-ttu-id="a56a9-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="a56a9-226">Entry</span></span> | <span data-ttu-id="a56a9-227">Valor</span><span class="sxs-lookup"><span data-stu-id="a56a9-227">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="a56a9-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="a56a9-228">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="a56a9-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a56a9-229">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="a56a9-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="a56a9-230">System-Only</span></span>            | <span data-ttu-id="a56a9-231">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-231">False</span></span>                                                      |
| <span data-ttu-id="a56a9-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a56a9-232">Is-Single-Valued</span></span>       | <span data-ttu-id="a56a9-233">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-233">False</span></span>                                                      |
| <span data-ttu-id="a56a9-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="a56a9-234">Is Indexed</span></span>             | <span data-ttu-id="a56a9-235">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-235">False</span></span>                                                      |
| <span data-ttu-id="a56a9-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a56a9-236">In Global Catalog</span></span>      | <span data-ttu-id="a56a9-237">Falso</span><span class="sxs-lookup"><span data-stu-id="a56a9-237">False</span></span>                                                      |
| <span data-ttu-id="a56a9-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a56a9-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="a56a9-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a56a9-239">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="a56a9-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a56a9-240">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="a56a9-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a56a9-241">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="a56a9-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a56a9-242">Search-Flags</span></span>           | <span data-ttu-id="a56a9-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a56a9-243">0x00000000</span></span>                                                 |
| <span data-ttu-id="a56a9-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a56a9-244">System-Flags</span></span>           | <span data-ttu-id="a56a9-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a56a9-245">0x00000010</span></span>                                                 |
| <span data-ttu-id="a56a9-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a56a9-246">Classes used in</span></span>        | [<span data-ttu-id="a56a9-247">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="a56a9-247">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





