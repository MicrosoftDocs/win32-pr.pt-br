---
title: Padrão-atributo de descritor de segurança
description: O descritor de segurança a ser atribuído ao objeto quando ele é criado pela primeira vez.
ms.assetid: 22575883-2ef3-492b-9868-1eb350c4f547
ms.tgt_platform: multiple
keywords:
- Padrão-Security-Descriptor atributo AD Schema
- Esquema de AD do atributo defaultSecurityDescriptor
topic_type:
- apiref
api_name:
- Default-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cd0b4a8dbe0c633a15b6a5167cb1171a14d1769
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456127"
---
# <a name="default-security-descriptor-attribute"></a><span data-ttu-id="450be-105">Padrão-atributo de descritor de segurança</span><span class="sxs-lookup"><span data-stu-id="450be-105">Default-Security-Descriptor attribute</span></span>

<span data-ttu-id="450be-106">O descritor de segurança a ser atribuído ao objeto quando ele é criado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="450be-106">The security descriptor to be assigned to the object when it is first created.</span></span>



| <span data-ttu-id="450be-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="450be-107">Entry</span></span> | <span data-ttu-id="450be-108">Valor</span><span class="sxs-lookup"><span data-stu-id="450be-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="450be-109">CN</span><span class="sxs-lookup"><span data-stu-id="450be-109">CN</span></span>                | <span data-ttu-id="450be-110">Padrão-descritor de segurança</span><span class="sxs-lookup"><span data-stu-id="450be-110">Default-Security-Descriptor</span></span>                 |
| <span data-ttu-id="450be-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="450be-111">Ldap-Display-Name</span></span> | <span data-ttu-id="450be-112">defaultSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="450be-112">defaultSecurityDescriptor</span></span>                   |
| <span data-ttu-id="450be-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="450be-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="450be-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="450be-114">Update Privilege</span></span>  | <span data-ttu-id="450be-115">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="450be-115">Schema administrator</span></span>                        |
| <span data-ttu-id="450be-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="450be-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="450be-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="450be-117">Attribute-Id</span></span>      | <span data-ttu-id="450be-118">1.2.840.113556.1.4.224</span><span class="sxs-lookup"><span data-stu-id="450be-118">1.2.840.113556.1.4.224</span></span>                      |
| <span data-ttu-id="450be-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="450be-119">System-Id-Guid</span></span>    | <span data-ttu-id="450be-120">807a6d30-1669-11d0-a064-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="450be-120">807a6d30-1669-11d0-a064-00aa006c33ed</span></span>        |
| <span data-ttu-id="450be-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="450be-121">Syntax</span></span>            | [<span data-ttu-id="450be-122">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="450be-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="450be-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="450be-123">Implementations</span></span>

-   [<span data-ttu-id="450be-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="450be-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="450be-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="450be-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="450be-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="450be-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="450be-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="450be-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="450be-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="450be-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="450be-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="450be-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="450be-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="450be-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="450be-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="450be-131">Windows 2000 Server</span></span>



| <span data-ttu-id="450be-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="450be-132">Entry</span></span> | <span data-ttu-id="450be-133">Valor</span><span class="sxs-lookup"><span data-stu-id="450be-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="450be-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="450be-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="450be-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="450be-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="450be-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="450be-136">System-Only</span></span>            | <span data-ttu-id="450be-137">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-137">False</span></span>                                            |
| <span data-ttu-id="450be-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="450be-138">Is-Single-Valued</span></span>       | <span data-ttu-id="450be-139">True</span><span class="sxs-lookup"><span data-stu-id="450be-139">True</span></span>                                             |
| <span data-ttu-id="450be-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="450be-140">Is Indexed</span></span>             | <span data-ttu-id="450be-141">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-141">False</span></span>                                            |
| <span data-ttu-id="450be-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="450be-142">In Global Catalog</span></span>      | <span data-ttu-id="450be-143">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-143">False</span></span>                                            |
| <span data-ttu-id="450be-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="450be-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="450be-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="450be-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="450be-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="450be-146">Range-Lower</span></span>            | <span data-ttu-id="450be-147">0</span><span class="sxs-lookup"><span data-stu-id="450be-147">0</span></span>                                                |
| <span data-ttu-id="450be-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="450be-148">Range-Upper</span></span>            | <span data-ttu-id="450be-149">32767</span><span class="sxs-lookup"><span data-stu-id="450be-149">32767</span></span>                                            |
| <span data-ttu-id="450be-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="450be-150">Search-Flags</span></span>           | <span data-ttu-id="450be-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="450be-151">0x00000000</span></span>                                       |
| <span data-ttu-id="450be-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="450be-152">System-Flags</span></span>           | <span data-ttu-id="450be-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="450be-153">0x00000010</span></span>                                       |
| <span data-ttu-id="450be-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="450be-154">Classes used in</span></span>        | [<span data-ttu-id="450be-155">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="450be-155">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="450be-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="450be-156">Windows Server 2003</span></span>



| <span data-ttu-id="450be-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="450be-157">Entry</span></span> | <span data-ttu-id="450be-158">Valor</span><span class="sxs-lookup"><span data-stu-id="450be-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="450be-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="450be-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="450be-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="450be-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="450be-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="450be-161">System-Only</span></span>            | <span data-ttu-id="450be-162">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-162">False</span></span>                                            |
| <span data-ttu-id="450be-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="450be-163">Is-Single-Valued</span></span>       | <span data-ttu-id="450be-164">True</span><span class="sxs-lookup"><span data-stu-id="450be-164">True</span></span>                                             |
| <span data-ttu-id="450be-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="450be-165">Is Indexed</span></span>             | <span data-ttu-id="450be-166">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-166">False</span></span>                                            |
| <span data-ttu-id="450be-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="450be-167">In Global Catalog</span></span>      | <span data-ttu-id="450be-168">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-168">False</span></span>                                            |
| <span data-ttu-id="450be-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="450be-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="450be-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="450be-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="450be-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="450be-171">Range-Lower</span></span>            | <span data-ttu-id="450be-172">0</span><span class="sxs-lookup"><span data-stu-id="450be-172">0</span></span>                                                |
| <span data-ttu-id="450be-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="450be-173">Range-Upper</span></span>            | <span data-ttu-id="450be-174">32767</span><span class="sxs-lookup"><span data-stu-id="450be-174">32767</span></span>                                            |
| <span data-ttu-id="450be-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="450be-175">Search-Flags</span></span>           | <span data-ttu-id="450be-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="450be-176">0x00000000</span></span>                                       |
| <span data-ttu-id="450be-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="450be-177">System-Flags</span></span>           | <span data-ttu-id="450be-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="450be-178">0x00000010</span></span>                                       |
| <span data-ttu-id="450be-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="450be-179">Classes used in</span></span>        | [<span data-ttu-id="450be-180">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="450be-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="450be-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="450be-181">ADAM</span></span>



| <span data-ttu-id="450be-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="450be-182">Entry</span></span> | <span data-ttu-id="450be-183">Valor</span><span class="sxs-lookup"><span data-stu-id="450be-183">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="450be-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="450be-184">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="450be-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="450be-185">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="450be-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="450be-186">System-Only</span></span>            | <span data-ttu-id="450be-187">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-187">False</span></span>                                            |
| <span data-ttu-id="450be-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="450be-188">Is-Single-Valued</span></span>       | <span data-ttu-id="450be-189">True</span><span class="sxs-lookup"><span data-stu-id="450be-189">True</span></span>                                             |
| <span data-ttu-id="450be-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="450be-190">Is Indexed</span></span>             | <span data-ttu-id="450be-191">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-191">False</span></span>                                            |
| <span data-ttu-id="450be-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="450be-192">In Global Catalog</span></span>      | <span data-ttu-id="450be-193">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-193">False</span></span>                                            |
| <span data-ttu-id="450be-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="450be-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="450be-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="450be-195">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="450be-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="450be-196">Range-Lower</span></span>            | <span data-ttu-id="450be-197">0</span><span class="sxs-lookup"><span data-stu-id="450be-197">0</span></span>                                                |
| <span data-ttu-id="450be-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="450be-198">Range-Upper</span></span>            | <span data-ttu-id="450be-199">32767</span><span class="sxs-lookup"><span data-stu-id="450be-199">32767</span></span>                                            |
| <span data-ttu-id="450be-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="450be-200">Search-Flags</span></span>           | <span data-ttu-id="450be-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="450be-201">0x00000000</span></span>                                       |
| <span data-ttu-id="450be-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="450be-202">System-Flags</span></span>           | <span data-ttu-id="450be-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="450be-203">0x00000010</span></span>                                       |
| <span data-ttu-id="450be-204">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="450be-204">Classes used in</span></span>        | [<span data-ttu-id="450be-205">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="450be-205">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="450be-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="450be-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="450be-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="450be-207">Entry</span></span> | <span data-ttu-id="450be-208">Valor</span><span class="sxs-lookup"><span data-stu-id="450be-208">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="450be-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="450be-209">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="450be-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="450be-210">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="450be-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="450be-211">System-Only</span></span>            | <span data-ttu-id="450be-212">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-212">False</span></span>                                            |
| <span data-ttu-id="450be-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="450be-213">Is-Single-Valued</span></span>       | <span data-ttu-id="450be-214">True</span><span class="sxs-lookup"><span data-stu-id="450be-214">True</span></span>                                             |
| <span data-ttu-id="450be-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="450be-215">Is Indexed</span></span>             | <span data-ttu-id="450be-216">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-216">False</span></span>                                            |
| <span data-ttu-id="450be-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="450be-217">In Global Catalog</span></span>      | <span data-ttu-id="450be-218">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-218">False</span></span>                                            |
| <span data-ttu-id="450be-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="450be-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="450be-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="450be-220">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="450be-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="450be-221">Range-Lower</span></span>            | <span data-ttu-id="450be-222">0</span><span class="sxs-lookup"><span data-stu-id="450be-222">0</span></span>                                                |
| <span data-ttu-id="450be-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="450be-223">Range-Upper</span></span>            | <span data-ttu-id="450be-224">32767</span><span class="sxs-lookup"><span data-stu-id="450be-224">32767</span></span>                                            |
| <span data-ttu-id="450be-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="450be-225">Search-Flags</span></span>           | <span data-ttu-id="450be-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="450be-226">0x00000000</span></span>                                       |
| <span data-ttu-id="450be-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="450be-227">System-Flags</span></span>           | <span data-ttu-id="450be-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="450be-228">0x00000010</span></span>                                       |
| <span data-ttu-id="450be-229">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="450be-229">Classes used in</span></span>        | [<span data-ttu-id="450be-230">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="450be-230">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="450be-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="450be-231">Windows Server 2008</span></span>



| <span data-ttu-id="450be-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="450be-232">Entry</span></span> | <span data-ttu-id="450be-233">Valor</span><span class="sxs-lookup"><span data-stu-id="450be-233">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="450be-234">ID do link</span><span class="sxs-lookup"><span data-stu-id="450be-234">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="450be-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="450be-235">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="450be-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="450be-236">System-Only</span></span>            | <span data-ttu-id="450be-237">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-237">False</span></span>                                            |
| <span data-ttu-id="450be-238">É de valor único</span><span class="sxs-lookup"><span data-stu-id="450be-238">Is-Single-Valued</span></span>       | <span data-ttu-id="450be-239">True</span><span class="sxs-lookup"><span data-stu-id="450be-239">True</span></span>                                             |
| <span data-ttu-id="450be-240">É indexado</span><span class="sxs-lookup"><span data-stu-id="450be-240">Is Indexed</span></span>             | <span data-ttu-id="450be-241">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-241">False</span></span>                                            |
| <span data-ttu-id="450be-242">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="450be-242">In Global Catalog</span></span>      | <span data-ttu-id="450be-243">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-243">False</span></span>                                            |
| <span data-ttu-id="450be-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="450be-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="450be-245">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="450be-245">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="450be-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="450be-246">Range-Lower</span></span>            | <span data-ttu-id="450be-247">0</span><span class="sxs-lookup"><span data-stu-id="450be-247">0</span></span>                                                |
| <span data-ttu-id="450be-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="450be-248">Range-Upper</span></span>            | <span data-ttu-id="450be-249">32767</span><span class="sxs-lookup"><span data-stu-id="450be-249">32767</span></span>                                            |
| <span data-ttu-id="450be-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="450be-250">Search-Flags</span></span>           | <span data-ttu-id="450be-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="450be-251">0x00000000</span></span>                                       |
| <span data-ttu-id="450be-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="450be-252">System-Flags</span></span>           | <span data-ttu-id="450be-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="450be-253">0x00000010</span></span>                                       |
| <span data-ttu-id="450be-254">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="450be-254">Classes used in</span></span>        | [<span data-ttu-id="450be-255">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="450be-255">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="450be-256">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="450be-256">Windows Server 2008 R2</span></span>



| <span data-ttu-id="450be-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="450be-257">Entry</span></span> | <span data-ttu-id="450be-258">Valor</span><span class="sxs-lookup"><span data-stu-id="450be-258">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="450be-259">ID do link</span><span class="sxs-lookup"><span data-stu-id="450be-259">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="450be-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="450be-260">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="450be-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="450be-261">System-Only</span></span>            | <span data-ttu-id="450be-262">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-262">False</span></span>                                            |
| <span data-ttu-id="450be-263">É de valor único</span><span class="sxs-lookup"><span data-stu-id="450be-263">Is-Single-Valued</span></span>       | <span data-ttu-id="450be-264">True</span><span class="sxs-lookup"><span data-stu-id="450be-264">True</span></span>                                             |
| <span data-ttu-id="450be-265">É indexado</span><span class="sxs-lookup"><span data-stu-id="450be-265">Is Indexed</span></span>             | <span data-ttu-id="450be-266">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-266">False</span></span>                                            |
| <span data-ttu-id="450be-267">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="450be-267">In Global Catalog</span></span>      | <span data-ttu-id="450be-268">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-268">False</span></span>                                            |
| <span data-ttu-id="450be-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="450be-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="450be-270">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="450be-270">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="450be-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="450be-271">Range-Lower</span></span>            | <span data-ttu-id="450be-272">0</span><span class="sxs-lookup"><span data-stu-id="450be-272">0</span></span>                                                |
| <span data-ttu-id="450be-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="450be-273">Range-Upper</span></span>            | <span data-ttu-id="450be-274">32767</span><span class="sxs-lookup"><span data-stu-id="450be-274">32767</span></span>                                            |
| <span data-ttu-id="450be-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="450be-275">Search-Flags</span></span>           | <span data-ttu-id="450be-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="450be-276">0x00000000</span></span>                                       |
| <span data-ttu-id="450be-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="450be-277">System-Flags</span></span>           | <span data-ttu-id="450be-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="450be-278">0x00000010</span></span>                                       |
| <span data-ttu-id="450be-279">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="450be-279">Classes used in</span></span>        | [<span data-ttu-id="450be-280">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="450be-280">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="450be-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="450be-281">Windows Server 2012</span></span>



| <span data-ttu-id="450be-282">Entrada</span><span class="sxs-lookup"><span data-stu-id="450be-282">Entry</span></span> | <span data-ttu-id="450be-283">Valor</span><span class="sxs-lookup"><span data-stu-id="450be-283">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="450be-284">ID do link</span><span class="sxs-lookup"><span data-stu-id="450be-284">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="450be-285">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="450be-285">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="450be-286">System-Only</span><span class="sxs-lookup"><span data-stu-id="450be-286">System-Only</span></span>            | <span data-ttu-id="450be-287">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-287">False</span></span>                                            |
| <span data-ttu-id="450be-288">É de valor único</span><span class="sxs-lookup"><span data-stu-id="450be-288">Is-Single-Valued</span></span>       | <span data-ttu-id="450be-289">True</span><span class="sxs-lookup"><span data-stu-id="450be-289">True</span></span>                                             |
| <span data-ttu-id="450be-290">É indexado</span><span class="sxs-lookup"><span data-stu-id="450be-290">Is Indexed</span></span>             | <span data-ttu-id="450be-291">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-291">False</span></span>                                            |
| <span data-ttu-id="450be-292">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="450be-292">In Global Catalog</span></span>      | <span data-ttu-id="450be-293">Falso</span><span class="sxs-lookup"><span data-stu-id="450be-293">False</span></span>                                            |
| <span data-ttu-id="450be-294">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="450be-294">NT-Security-Descriptor</span></span> | <span data-ttu-id="450be-295">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="450be-295">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="450be-296">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="450be-296">Range-Lower</span></span>            | <span data-ttu-id="450be-297">0</span><span class="sxs-lookup"><span data-stu-id="450be-297">0</span></span>                                                |
| <span data-ttu-id="450be-298">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="450be-298">Range-Upper</span></span>            | <span data-ttu-id="450be-299">32767</span><span class="sxs-lookup"><span data-stu-id="450be-299">32767</span></span>                                            |
| <span data-ttu-id="450be-300">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="450be-300">Search-Flags</span></span>           | <span data-ttu-id="450be-301">0x00000000</span><span class="sxs-lookup"><span data-stu-id="450be-301">0x00000000</span></span>                                       |
| <span data-ttu-id="450be-302">System-Flags</span><span class="sxs-lookup"><span data-stu-id="450be-302">System-Flags</span></span>           | <span data-ttu-id="450be-303">0x00000010</span><span class="sxs-lookup"><span data-stu-id="450be-303">0x00000010</span></span>                                       |
| <span data-ttu-id="450be-304">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="450be-304">Classes used in</span></span>        | [<span data-ttu-id="450be-305">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="450be-305">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





