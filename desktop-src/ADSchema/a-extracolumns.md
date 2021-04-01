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
# <a name="extra-columns-attribute"></a><span data-ttu-id="f87b1-105">Extra-Columns atributo</span><span class="sxs-lookup"><span data-stu-id="f87b1-105">Extra-Columns attribute</span></span>

<span data-ttu-id="f87b1-106">Este é um atributo com vários valores, cujo valor consiste em uma tupla de 5: (nome do atributo), (título da coluna), (visibilidade padrão (0, 1)), (largura da coluna (1 para largura automática)), 0 (reservado para uso futuro deve ser zero).</span><span class="sxs-lookup"><span data-stu-id="f87b1-106">This is a multivalued attribute whose values consist of a 5 tuple: (attribute name), (column title), (default visibility (0,1)), (column width ( 1 for auto width)), 0 (reserved for future use must be zero).</span></span> <span data-ttu-id="f87b1-107">Esse valor é usado pelo console usuários e computadores do AD.</span><span class="sxs-lookup"><span data-stu-id="f87b1-107">This value is used by the AD Users and Computers console.</span></span>



| <span data-ttu-id="f87b1-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="f87b1-108">Entry</span></span> | <span data-ttu-id="f87b1-109">Valor</span><span class="sxs-lookup"><span data-stu-id="f87b1-109">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f87b1-110">CN</span><span class="sxs-lookup"><span data-stu-id="f87b1-110">CN</span></span>                | <span data-ttu-id="f87b1-111">Extra-Columns</span><span class="sxs-lookup"><span data-stu-id="f87b1-111">Extra-Columns</span></span>                                                                                                                                                        |
| <span data-ttu-id="f87b1-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f87b1-112">Ldap-Display-Name</span></span> | <span data-ttu-id="f87b1-113">extraColumns</span><span class="sxs-lookup"><span data-stu-id="f87b1-113">extraColumns</span></span>                                                                                                                                                         |
| <span data-ttu-id="f87b1-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f87b1-114">Size</span></span>              | <span data-ttu-id="f87b1-115">Cada valor seria o tamanho da cadeia de caracteres da tupla de 5.</span><span class="sxs-lookup"><span data-stu-id="f87b1-115">Each value would be the size of the string of the 5 tuple above.</span></span> <span data-ttu-id="f87b1-116">Por padrão, haverá 22 valores no objeto de exibição padrão no contêiner DisplaySpecifier.</span><span class="sxs-lookup"><span data-stu-id="f87b1-116">By default there will be 22 values on the default-Display object in the DisplaySpecifier container.</span></span> |
| <span data-ttu-id="f87b1-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f87b1-117">Update Privilege</span></span>  | <span data-ttu-id="f87b1-118">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="f87b1-118">Domain administrator</span></span>                                                                                                                                                 |
| <span data-ttu-id="f87b1-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f87b1-119">Update Frequency</span></span>  | <span data-ttu-id="f87b1-120">Isso só será atualizado se um serviço como o Exchange estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="f87b1-120">This will only be updated if a service like Exchange is installed.</span></span>                                                                                                   |
| <span data-ttu-id="f87b1-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f87b1-121">Attribute-Id</span></span>      | <span data-ttu-id="f87b1-122">1.2.840.113556.1.4.1687</span><span class="sxs-lookup"><span data-stu-id="f87b1-122">1.2.840.113556.1.4.1687</span></span>                                                                                                                                              |
| <span data-ttu-id="f87b1-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f87b1-123">System-Id-Guid</span></span>    | <span data-ttu-id="f87b1-124">d24e2846-1dd9-4bcf-99d7-a6227cc86da7</span><span class="sxs-lookup"><span data-stu-id="f87b1-124">d24e2846-1dd9-4bcf-99d7-a6227cc86da7</span></span>                                                                                                                                 |
| <span data-ttu-id="f87b1-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="f87b1-125">Syntax</span></span>            | [<span data-ttu-id="f87b1-126">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f87b1-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                                                          |



## <a name="implementations"></a><span data-ttu-id="f87b1-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="f87b1-127">Implementations</span></span>

-   [<span data-ttu-id="f87b1-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f87b1-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f87b1-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f87b1-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f87b1-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f87b1-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f87b1-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f87b1-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f87b1-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f87b1-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f87b1-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f87b1-133">Windows Server 2003</span></span>



| <span data-ttu-id="f87b1-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="f87b1-134">Entry</span></span> | <span data-ttu-id="f87b1-135">Valor</span><span class="sxs-lookup"><span data-stu-id="f87b1-135">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="f87b1-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="f87b1-136">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f87b1-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f87b1-137">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f87b1-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="f87b1-138">System-Only</span></span>            | <span data-ttu-id="f87b1-139">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-139">False</span></span>                                                      |
| <span data-ttu-id="f87b1-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f87b1-140">Is-Single-Valued</span></span>       | <span data-ttu-id="f87b1-141">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-141">False</span></span>                                                      |
| <span data-ttu-id="f87b1-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="f87b1-142">Is Indexed</span></span>             | <span data-ttu-id="f87b1-143">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-143">False</span></span>                                                      |
| <span data-ttu-id="f87b1-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f87b1-144">In Global Catalog</span></span>      | <span data-ttu-id="f87b1-145">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-145">False</span></span>                                                      |
| <span data-ttu-id="f87b1-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f87b1-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="f87b1-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f87b1-147">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="f87b1-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f87b1-148">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="f87b1-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f87b1-149">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="f87b1-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f87b1-150">Search-Flags</span></span>           | <span data-ttu-id="f87b1-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f87b1-151">0x00000000</span></span>                                                 |
| <span data-ttu-id="f87b1-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f87b1-152">System-Flags</span></span>           | <span data-ttu-id="f87b1-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f87b1-153">0x00000010</span></span>                                                 |
| <span data-ttu-id="f87b1-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f87b1-154">Classes used in</span></span>        | [<span data-ttu-id="f87b1-155">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="f87b1-155">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f87b1-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f87b1-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f87b1-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="f87b1-157">Entry</span></span> | <span data-ttu-id="f87b1-158">Valor</span><span class="sxs-lookup"><span data-stu-id="f87b1-158">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="f87b1-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="f87b1-159">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f87b1-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f87b1-160">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f87b1-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="f87b1-161">System-Only</span></span>            | <span data-ttu-id="f87b1-162">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-162">False</span></span>                                                      |
| <span data-ttu-id="f87b1-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f87b1-163">Is-Single-Valued</span></span>       | <span data-ttu-id="f87b1-164">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-164">False</span></span>                                                      |
| <span data-ttu-id="f87b1-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="f87b1-165">Is Indexed</span></span>             | <span data-ttu-id="f87b1-166">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-166">False</span></span>                                                      |
| <span data-ttu-id="f87b1-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f87b1-167">In Global Catalog</span></span>      | <span data-ttu-id="f87b1-168">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-168">False</span></span>                                                      |
| <span data-ttu-id="f87b1-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f87b1-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="f87b1-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f87b1-170">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="f87b1-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f87b1-171">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="f87b1-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f87b1-172">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="f87b1-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f87b1-173">Search-Flags</span></span>           | <span data-ttu-id="f87b1-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f87b1-174">0x00000000</span></span>                                                 |
| <span data-ttu-id="f87b1-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f87b1-175">System-Flags</span></span>           | <span data-ttu-id="f87b1-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f87b1-176">0x00000010</span></span>                                                 |
| <span data-ttu-id="f87b1-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f87b1-177">Classes used in</span></span>        | [<span data-ttu-id="f87b1-178">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="f87b1-178">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f87b1-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f87b1-179">Windows Server 2008</span></span>



| <span data-ttu-id="f87b1-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="f87b1-180">Entry</span></span> | <span data-ttu-id="f87b1-181">Valor</span><span class="sxs-lookup"><span data-stu-id="f87b1-181">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="f87b1-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="f87b1-182">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f87b1-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f87b1-183">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f87b1-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="f87b1-184">System-Only</span></span>            | <span data-ttu-id="f87b1-185">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-185">False</span></span>                                                      |
| <span data-ttu-id="f87b1-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f87b1-186">Is-Single-Valued</span></span>       | <span data-ttu-id="f87b1-187">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-187">False</span></span>                                                      |
| <span data-ttu-id="f87b1-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="f87b1-188">Is Indexed</span></span>             | <span data-ttu-id="f87b1-189">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-189">False</span></span>                                                      |
| <span data-ttu-id="f87b1-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f87b1-190">In Global Catalog</span></span>      | <span data-ttu-id="f87b1-191">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-191">False</span></span>                                                      |
| <span data-ttu-id="f87b1-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f87b1-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="f87b1-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f87b1-193">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="f87b1-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f87b1-194">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="f87b1-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f87b1-195">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="f87b1-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f87b1-196">Search-Flags</span></span>           | <span data-ttu-id="f87b1-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f87b1-197">0x00000000</span></span>                                                 |
| <span data-ttu-id="f87b1-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f87b1-198">System-Flags</span></span>           | <span data-ttu-id="f87b1-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f87b1-199">0x00000010</span></span>                                                 |
| <span data-ttu-id="f87b1-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f87b1-200">Classes used in</span></span>        | [<span data-ttu-id="f87b1-201">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="f87b1-201">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f87b1-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f87b1-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f87b1-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="f87b1-203">Entry</span></span> | <span data-ttu-id="f87b1-204">Valor</span><span class="sxs-lookup"><span data-stu-id="f87b1-204">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="f87b1-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="f87b1-205">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f87b1-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f87b1-206">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f87b1-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="f87b1-207">System-Only</span></span>            | <span data-ttu-id="f87b1-208">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-208">False</span></span>                                                      |
| <span data-ttu-id="f87b1-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f87b1-209">Is-Single-Valued</span></span>       | <span data-ttu-id="f87b1-210">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-210">False</span></span>                                                      |
| <span data-ttu-id="f87b1-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="f87b1-211">Is Indexed</span></span>             | <span data-ttu-id="f87b1-212">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-212">False</span></span>                                                      |
| <span data-ttu-id="f87b1-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f87b1-213">In Global Catalog</span></span>      | <span data-ttu-id="f87b1-214">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-214">False</span></span>                                                      |
| <span data-ttu-id="f87b1-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f87b1-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="f87b1-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f87b1-216">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="f87b1-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f87b1-217">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="f87b1-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f87b1-218">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="f87b1-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f87b1-219">Search-Flags</span></span>           | <span data-ttu-id="f87b1-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f87b1-220">0x00000000</span></span>                                                 |
| <span data-ttu-id="f87b1-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f87b1-221">System-Flags</span></span>           | <span data-ttu-id="f87b1-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f87b1-222">0x00000010</span></span>                                                 |
| <span data-ttu-id="f87b1-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f87b1-223">Classes used in</span></span>        | [<span data-ttu-id="f87b1-224">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="f87b1-224">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f87b1-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f87b1-225">Windows Server 2012</span></span>



| <span data-ttu-id="f87b1-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="f87b1-226">Entry</span></span> | <span data-ttu-id="f87b1-227">Valor</span><span class="sxs-lookup"><span data-stu-id="f87b1-227">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="f87b1-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="f87b1-228">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f87b1-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f87b1-229">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f87b1-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="f87b1-230">System-Only</span></span>            | <span data-ttu-id="f87b1-231">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-231">False</span></span>                                                      |
| <span data-ttu-id="f87b1-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f87b1-232">Is-Single-Valued</span></span>       | <span data-ttu-id="f87b1-233">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-233">False</span></span>                                                      |
| <span data-ttu-id="f87b1-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="f87b1-234">Is Indexed</span></span>             | <span data-ttu-id="f87b1-235">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-235">False</span></span>                                                      |
| <span data-ttu-id="f87b1-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f87b1-236">In Global Catalog</span></span>      | <span data-ttu-id="f87b1-237">Falso</span><span class="sxs-lookup"><span data-stu-id="f87b1-237">False</span></span>                                                      |
| <span data-ttu-id="f87b1-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f87b1-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="f87b1-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f87b1-239">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="f87b1-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f87b1-240">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="f87b1-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f87b1-241">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="f87b1-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f87b1-242">Search-Flags</span></span>           | <span data-ttu-id="f87b1-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f87b1-243">0x00000000</span></span>                                                 |
| <span data-ttu-id="f87b1-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f87b1-244">System-Flags</span></span>           | <span data-ttu-id="f87b1-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f87b1-245">0x00000010</span></span>                                                 |
| <span data-ttu-id="f87b1-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f87b1-246">Classes used in</span></span>        | [<span data-ttu-id="f87b1-247">**Especificador de exibição**</span><span class="sxs-lookup"><span data-stu-id="f87b1-247">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





