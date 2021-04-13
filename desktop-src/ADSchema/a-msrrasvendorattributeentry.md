---
title: atributo ms-RRAS-Vendor-Attribute-entry
description: Uma cadeia de caracteres que permite que os fornecedores adicionem atributos de roteador ao DS para uso em consultas, no formato AttributeName vendornameelement AttributeType.
ms.assetid: 07bc4d9b-eba9-456b-be21-cd7bb8a5b0b6
ms.tgt_platform: multiple
keywords:
- Esquema do AD do MS-RRAS-Vendor-Attribute-entry
- Esquema de AD do atributo msRRASVendorAttributeEntry
topic_type:
- apiref
api_name:
- ms-RRAS-Vendor-Attribute-Entry
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28ee353122107db5b1247860e9799db861b4d6bf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456200"
---
# <a name="ms-rras-vendor-attribute-entry-attribute"></a><span data-ttu-id="a08e1-105">atributo ms-RRAS-Vendor-Attribute-entry</span><span class="sxs-lookup"><span data-stu-id="a08e1-105">ms-RRAS-Vendor-Attribute-Entry attribute</span></span>

<span data-ttu-id="a08e1-106">Uma cadeia de caracteres que permite aos fornecedores adicionar atributos de roteador ao DS para uso em consultas, no formato AttributeName: VendorID: AttributeType.</span><span class="sxs-lookup"><span data-stu-id="a08e1-106">A string that enables vendors to add router attributes to the DS for use in queries, in the form AttributeName:vendorID:AttributeType.</span></span>



| <span data-ttu-id="a08e1-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a08e1-107">Entry</span></span> | <span data-ttu-id="a08e1-108">Valor</span><span class="sxs-lookup"><span data-stu-id="a08e1-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a08e1-109">CN</span><span class="sxs-lookup"><span data-stu-id="a08e1-109">CN</span></span>                | <span data-ttu-id="a08e1-110">Entrada de atributo ms-RRAS-Vendor</span><span class="sxs-lookup"><span data-stu-id="a08e1-110">ms-RRAS-Vendor-Attribute-Entry</span></span>              |
| <span data-ttu-id="a08e1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a08e1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a08e1-112">msRRASVendorAttributeEntry</span><span class="sxs-lookup"><span data-stu-id="a08e1-112">msRRASVendorAttributeEntry</span></span>                  |
| <span data-ttu-id="a08e1-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a08e1-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="a08e1-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a08e1-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="a08e1-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a08e1-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="a08e1-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a08e1-116">Attribute-Id</span></span>      | <span data-ttu-id="a08e1-117">1.2.840.113556.1.4.883</span><span class="sxs-lookup"><span data-stu-id="a08e1-117">1.2.840.113556.1.4.883</span></span>                      |
| <span data-ttu-id="a08e1-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a08e1-118">System-Id-Guid</span></span>    | <span data-ttu-id="a08e1-119">f39b98ac-938d-11d1-aebd-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a08e1-119">f39b98ac-938d-11d1-aebd-0000f80367c1</span></span>        |
| <span data-ttu-id="a08e1-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="a08e1-120">Syntax</span></span>            | [<span data-ttu-id="a08e1-121">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a08e1-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a08e1-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="a08e1-122">Implementations</span></span>

-   [<span data-ttu-id="a08e1-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a08e1-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a08e1-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a08e1-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a08e1-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a08e1-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a08e1-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a08e1-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a08e1-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a08e1-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a08e1-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a08e1-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a08e1-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a08e1-129">Windows 2000 Server</span></span>



| <span data-ttu-id="a08e1-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="a08e1-130">Entry</span></span> | <span data-ttu-id="a08e1-131">Valor</span><span class="sxs-lookup"><span data-stu-id="a08e1-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a08e1-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="a08e1-132">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a08e1-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a08e1-133">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a08e1-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="a08e1-134">System-Only</span></span>            | <span data-ttu-id="a08e1-135">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-135">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a08e1-136">Is-Single-Valued</span></span>       | <span data-ttu-id="a08e1-137">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-137">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="a08e1-138">Is Indexed</span></span>             | <span data-ttu-id="a08e1-139">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-139">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a08e1-140">In Global Catalog</span></span>      | <span data-ttu-id="a08e1-141">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-141">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a08e1-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="a08e1-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a08e1-143">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="a08e1-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a08e1-144">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="a08e1-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a08e1-145">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="a08e1-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a08e1-146">Search-Flags</span></span>           | <span data-ttu-id="a08e1-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a08e1-147">0x00000000</span></span>                                                                          |
| <span data-ttu-id="a08e1-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a08e1-148">System-Flags</span></span>           | <span data-ttu-id="a08e1-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a08e1-149">0x00000010</span></span>                                                                          |
| <span data-ttu-id="a08e1-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a08e1-150">Classes used in</span></span>        | [<span data-ttu-id="a08e1-151">**RRAS-administração-dicionário**</span><span class="sxs-lookup"><span data-stu-id="a08e1-151">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a08e1-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a08e1-152">Windows Server 2003</span></span>



| <span data-ttu-id="a08e1-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="a08e1-153">Entry</span></span> | <span data-ttu-id="a08e1-154">Valor</span><span class="sxs-lookup"><span data-stu-id="a08e1-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a08e1-155">ID do link</span><span class="sxs-lookup"><span data-stu-id="a08e1-155">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a08e1-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a08e1-156">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a08e1-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="a08e1-157">System-Only</span></span>            | <span data-ttu-id="a08e1-158">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-158">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-159">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a08e1-159">Is-Single-Valued</span></span>       | <span data-ttu-id="a08e1-160">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-160">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-161">É indexado</span><span class="sxs-lookup"><span data-stu-id="a08e1-161">Is Indexed</span></span>             | <span data-ttu-id="a08e1-162">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-162">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-163">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a08e1-163">In Global Catalog</span></span>      | <span data-ttu-id="a08e1-164">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-164">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a08e1-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="a08e1-166">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a08e1-166">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="a08e1-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a08e1-167">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="a08e1-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a08e1-168">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="a08e1-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a08e1-169">Search-Flags</span></span>           | <span data-ttu-id="a08e1-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a08e1-170">0x00000000</span></span>                                                                          |
| <span data-ttu-id="a08e1-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a08e1-171">System-Flags</span></span>           | <span data-ttu-id="a08e1-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a08e1-172">0x00000010</span></span>                                                                          |
| <span data-ttu-id="a08e1-173">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a08e1-173">Classes used in</span></span>        | [<span data-ttu-id="a08e1-174">**RRAS-administração-dicionário**</span><span class="sxs-lookup"><span data-stu-id="a08e1-174">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a08e1-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a08e1-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a08e1-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="a08e1-176">Entry</span></span> | <span data-ttu-id="a08e1-177">Valor</span><span class="sxs-lookup"><span data-stu-id="a08e1-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a08e1-178">ID do link</span><span class="sxs-lookup"><span data-stu-id="a08e1-178">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a08e1-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a08e1-179">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a08e1-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="a08e1-180">System-Only</span></span>            | <span data-ttu-id="a08e1-181">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-181">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-182">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a08e1-182">Is-Single-Valued</span></span>       | <span data-ttu-id="a08e1-183">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-183">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-184">É indexado</span><span class="sxs-lookup"><span data-stu-id="a08e1-184">Is Indexed</span></span>             | <span data-ttu-id="a08e1-185">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-185">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-186">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a08e1-186">In Global Catalog</span></span>      | <span data-ttu-id="a08e1-187">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-187">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a08e1-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="a08e1-189">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a08e1-189">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="a08e1-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a08e1-190">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="a08e1-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a08e1-191">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="a08e1-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a08e1-192">Search-Flags</span></span>           | <span data-ttu-id="a08e1-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a08e1-193">0x00000000</span></span>                                                                          |
| <span data-ttu-id="a08e1-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a08e1-194">System-Flags</span></span>           | <span data-ttu-id="a08e1-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a08e1-195">0x00000010</span></span>                                                                          |
| <span data-ttu-id="a08e1-196">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a08e1-196">Classes used in</span></span>        | [<span data-ttu-id="a08e1-197">**RRAS-administração-dicionário**</span><span class="sxs-lookup"><span data-stu-id="a08e1-197">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a08e1-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a08e1-198">Windows Server 2008</span></span>



| <span data-ttu-id="a08e1-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="a08e1-199">Entry</span></span> | <span data-ttu-id="a08e1-200">Valor</span><span class="sxs-lookup"><span data-stu-id="a08e1-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a08e1-201">ID do link</span><span class="sxs-lookup"><span data-stu-id="a08e1-201">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a08e1-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a08e1-202">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a08e1-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="a08e1-203">System-Only</span></span>            | <span data-ttu-id="a08e1-204">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-204">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a08e1-205">Is-Single-Valued</span></span>       | <span data-ttu-id="a08e1-206">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-206">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="a08e1-207">Is Indexed</span></span>             | <span data-ttu-id="a08e1-208">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-208">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a08e1-209">In Global Catalog</span></span>      | <span data-ttu-id="a08e1-210">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-210">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a08e1-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="a08e1-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a08e1-212">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="a08e1-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a08e1-213">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="a08e1-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a08e1-214">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="a08e1-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a08e1-215">Search-Flags</span></span>           | <span data-ttu-id="a08e1-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a08e1-216">0x00000000</span></span>                                                                          |
| <span data-ttu-id="a08e1-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a08e1-217">System-Flags</span></span>           | <span data-ttu-id="a08e1-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a08e1-218">0x00000010</span></span>                                                                          |
| <span data-ttu-id="a08e1-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a08e1-219">Classes used in</span></span>        | [<span data-ttu-id="a08e1-220">**RRAS-administração-dicionário**</span><span class="sxs-lookup"><span data-stu-id="a08e1-220">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a08e1-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a08e1-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a08e1-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="a08e1-222">Entry</span></span> | <span data-ttu-id="a08e1-223">Valor</span><span class="sxs-lookup"><span data-stu-id="a08e1-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a08e1-224">ID do link</span><span class="sxs-lookup"><span data-stu-id="a08e1-224">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a08e1-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a08e1-225">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a08e1-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="a08e1-226">System-Only</span></span>            | <span data-ttu-id="a08e1-227">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-227">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-228">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a08e1-228">Is-Single-Valued</span></span>       | <span data-ttu-id="a08e1-229">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-229">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-230">É indexado</span><span class="sxs-lookup"><span data-stu-id="a08e1-230">Is Indexed</span></span>             | <span data-ttu-id="a08e1-231">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-231">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-232">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a08e1-232">In Global Catalog</span></span>      | <span data-ttu-id="a08e1-233">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-233">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a08e1-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="a08e1-235">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a08e1-235">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="a08e1-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a08e1-236">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="a08e1-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a08e1-237">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="a08e1-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a08e1-238">Search-Flags</span></span>           | <span data-ttu-id="a08e1-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a08e1-239">0x00000000</span></span>                                                                          |
| <span data-ttu-id="a08e1-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a08e1-240">System-Flags</span></span>           | <span data-ttu-id="a08e1-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a08e1-241">0x00000010</span></span>                                                                          |
| <span data-ttu-id="a08e1-242">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a08e1-242">Classes used in</span></span>        | [<span data-ttu-id="a08e1-243">**RRAS-administração-dicionário**</span><span class="sxs-lookup"><span data-stu-id="a08e1-243">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a08e1-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a08e1-244">Windows Server 2012</span></span>



| <span data-ttu-id="a08e1-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="a08e1-245">Entry</span></span> | <span data-ttu-id="a08e1-246">Valor</span><span class="sxs-lookup"><span data-stu-id="a08e1-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a08e1-247">ID do link</span><span class="sxs-lookup"><span data-stu-id="a08e1-247">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a08e1-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a08e1-248">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="a08e1-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="a08e1-249">System-Only</span></span>            | <span data-ttu-id="a08e1-250">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-250">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-251">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a08e1-251">Is-Single-Valued</span></span>       | <span data-ttu-id="a08e1-252">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-252">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-253">É indexado</span><span class="sxs-lookup"><span data-stu-id="a08e1-253">Is Indexed</span></span>             | <span data-ttu-id="a08e1-254">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-254">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-255">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a08e1-255">In Global Catalog</span></span>      | <span data-ttu-id="a08e1-256">Falso</span><span class="sxs-lookup"><span data-stu-id="a08e1-256">False</span></span>                                                                               |
| <span data-ttu-id="a08e1-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a08e1-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="a08e1-258">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a08e1-258">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="a08e1-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a08e1-259">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="a08e1-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a08e1-260">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="a08e1-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a08e1-261">Search-Flags</span></span>           | <span data-ttu-id="a08e1-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a08e1-262">0x00000000</span></span>                                                                          |
| <span data-ttu-id="a08e1-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a08e1-263">System-Flags</span></span>           | <span data-ttu-id="a08e1-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a08e1-264">0x00000010</span></span>                                                                          |
| <span data-ttu-id="a08e1-265">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a08e1-265">Classes used in</span></span>        | [<span data-ttu-id="a08e1-266">**RRAS-administração-dicionário**</span><span class="sxs-lookup"><span data-stu-id="a08e1-266">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



 

 





