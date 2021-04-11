---
title: Atributo LDAP-Display-Name
description: O nome usado por clientes LDAP, como o provedor de LDAP ADSI, para ler e gravar o atributo usando o protocolo LDAP.
ms.assetid: 9cb0b2f0-16cf-4fc6-85b2-d21ff71bc477
ms.tgt_platform: multiple
keywords:
- Atributo LDAP-Display-Name do AD Schema
- atributo lDAPDisplayName de esquema do AD
topic_type:
- apiref
api_name:
- LDAP-Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ffa25777ec4b5139a41ba9e56d8d5f0a9a3d92
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104163638"
---
# <a name="ldap-display-name-attribute"></a><span data-ttu-id="ec016-105">Atributo LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ec016-105">LDAP-Display-Name attribute</span></span>

<span data-ttu-id="ec016-106">O nome usado por clientes LDAP, como o provedor de LDAP ADSI, para ler e gravar o atributo usando o protocolo LDAP.</span><span class="sxs-lookup"><span data-stu-id="ec016-106">The name used by LDAP clients, such as the ADSI LDAP provider, to read and write the attribute by using the LDAP protocol.</span></span>



| <span data-ttu-id="ec016-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec016-107">Entry</span></span> | <span data-ttu-id="ec016-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ec016-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ec016-109">CN</span><span class="sxs-lookup"><span data-stu-id="ec016-109">CN</span></span>                | <span data-ttu-id="ec016-110">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ec016-110">LDAP-Display-Name</span></span>                           |
| <span data-ttu-id="ec016-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ec016-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ec016-112">lDAPDisplayName</span><span class="sxs-lookup"><span data-stu-id="ec016-112">lDAPDisplayName</span></span>                             |
| <span data-ttu-id="ec016-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ec016-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="ec016-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="ec016-114">Update Privilege</span></span>  | <span data-ttu-id="ec016-115">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="ec016-115">Schema administrator</span></span>                        |
| <span data-ttu-id="ec016-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="ec016-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="ec016-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ec016-117">Attribute-Id</span></span>      | <span data-ttu-id="ec016-118">1.2.840.113556.1.2.460</span><span class="sxs-lookup"><span data-stu-id="ec016-118">1.2.840.113556.1.2.460</span></span>                      |
| <span data-ttu-id="ec016-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ec016-119">System-Id-Guid</span></span>    | <span data-ttu-id="ec016-120">bf96799a-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ec016-120">bf96799a-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="ec016-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec016-121">Syntax</span></span>            | [<span data-ttu-id="ec016-122">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ec016-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ec016-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="ec016-123">Implementations</span></span>

-   [<span data-ttu-id="ec016-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ec016-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ec016-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ec016-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ec016-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ec016-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ec016-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ec016-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ec016-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ec016-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ec016-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ec016-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ec016-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ec016-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ec016-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ec016-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ec016-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec016-132">Entry</span></span> | <span data-ttu-id="ec016-133">Valor</span><span class="sxs-lookup"><span data-stu-id="ec016-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec016-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="ec016-134">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ec016-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec016-135">MAPI-Id</span></span>                | <span data-ttu-id="ec016-136">0x8171</span><span class="sxs-lookup"><span data-stu-id="ec016-136">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="ec016-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec016-137">System-Only</span></span>            | <span data-ttu-id="ec016-138">Falso</span><span class="sxs-lookup"><span data-stu-id="ec016-138">False</span></span>                                                                                                     |
| <span data-ttu-id="ec016-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ec016-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ec016-140">True</span><span class="sxs-lookup"><span data-stu-id="ec016-140">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="ec016-141">Is Indexed</span></span>             | <span data-ttu-id="ec016-142">True</span><span class="sxs-lookup"><span data-stu-id="ec016-142">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ec016-143">In Global Catalog</span></span>      | <span data-ttu-id="ec016-144">True</span><span class="sxs-lookup"><span data-stu-id="ec016-144">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ec016-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec016-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ec016-146">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ec016-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec016-147">Range-Lower</span></span>            | <span data-ttu-id="ec016-148">1</span><span class="sxs-lookup"><span data-stu-id="ec016-148">1</span></span>                                                                                                         |
| <span data-ttu-id="ec016-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec016-149">Range-Upper</span></span>            | <span data-ttu-id="ec016-150">256</span><span class="sxs-lookup"><span data-stu-id="ec016-150">256</span></span>                                                                                                       |
| <span data-ttu-id="ec016-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec016-151">Search-Flags</span></span>           | <span data-ttu-id="ec016-152">0x00000009</span><span class="sxs-lookup"><span data-stu-id="ec016-152">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="ec016-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec016-153">System-Flags</span></span>           | <span data-ttu-id="ec016-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec016-154">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ec016-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ec016-155">Classes used in</span></span>        | [<span data-ttu-id="ec016-156">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="ec016-156">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="ec016-157">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ec016-157">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ec016-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ec016-158">Windows Server 2003</span></span>



| <span data-ttu-id="ec016-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec016-159">Entry</span></span> | <span data-ttu-id="ec016-160">Valor</span><span class="sxs-lookup"><span data-stu-id="ec016-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec016-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="ec016-161">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ec016-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec016-162">MAPI-Id</span></span>                | <span data-ttu-id="ec016-163">0x8171</span><span class="sxs-lookup"><span data-stu-id="ec016-163">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="ec016-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec016-164">System-Only</span></span>            | <span data-ttu-id="ec016-165">Falso</span><span class="sxs-lookup"><span data-stu-id="ec016-165">False</span></span>                                                                                                     |
| <span data-ttu-id="ec016-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ec016-166">Is-Single-Valued</span></span>       | <span data-ttu-id="ec016-167">True</span><span class="sxs-lookup"><span data-stu-id="ec016-167">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="ec016-168">Is Indexed</span></span>             | <span data-ttu-id="ec016-169">True</span><span class="sxs-lookup"><span data-stu-id="ec016-169">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ec016-170">In Global Catalog</span></span>      | <span data-ttu-id="ec016-171">True</span><span class="sxs-lookup"><span data-stu-id="ec016-171">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ec016-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec016-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ec016-173">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ec016-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec016-174">Range-Lower</span></span>            | <span data-ttu-id="ec016-175">1</span><span class="sxs-lookup"><span data-stu-id="ec016-175">1</span></span>                                                                                                         |
| <span data-ttu-id="ec016-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec016-176">Range-Upper</span></span>            | <span data-ttu-id="ec016-177">256</span><span class="sxs-lookup"><span data-stu-id="ec016-177">256</span></span>                                                                                                       |
| <span data-ttu-id="ec016-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec016-178">Search-Flags</span></span>           | <span data-ttu-id="ec016-179">0x00000009</span><span class="sxs-lookup"><span data-stu-id="ec016-179">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="ec016-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec016-180">System-Flags</span></span>           | <span data-ttu-id="ec016-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec016-181">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ec016-182">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ec016-182">Classes used in</span></span>        | [<span data-ttu-id="ec016-183">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="ec016-183">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="ec016-184">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ec016-184">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ec016-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="ec016-185">ADAM</span></span>



| <span data-ttu-id="ec016-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec016-186">Entry</span></span> | <span data-ttu-id="ec016-187">Valor</span><span class="sxs-lookup"><span data-stu-id="ec016-187">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec016-188">ID do link</span><span class="sxs-lookup"><span data-stu-id="ec016-188">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ec016-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec016-189">MAPI-Id</span></span>                | <span data-ttu-id="ec016-190">0x8171</span><span class="sxs-lookup"><span data-stu-id="ec016-190">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="ec016-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec016-191">System-Only</span></span>            | <span data-ttu-id="ec016-192">Falso</span><span class="sxs-lookup"><span data-stu-id="ec016-192">False</span></span>                                                                                                     |
| <span data-ttu-id="ec016-193">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ec016-193">Is-Single-Valued</span></span>       | <span data-ttu-id="ec016-194">True</span><span class="sxs-lookup"><span data-stu-id="ec016-194">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-195">É indexado</span><span class="sxs-lookup"><span data-stu-id="ec016-195">Is Indexed</span></span>             | <span data-ttu-id="ec016-196">True</span><span class="sxs-lookup"><span data-stu-id="ec016-196">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-197">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ec016-197">In Global Catalog</span></span>      | <span data-ttu-id="ec016-198">True</span><span class="sxs-lookup"><span data-stu-id="ec016-198">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-199">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ec016-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec016-200">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ec016-200">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ec016-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec016-201">Range-Lower</span></span>            | <span data-ttu-id="ec016-202">1</span><span class="sxs-lookup"><span data-stu-id="ec016-202">1</span></span>                                                                                                         |
| <span data-ttu-id="ec016-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec016-203">Range-Upper</span></span>            | <span data-ttu-id="ec016-204">256</span><span class="sxs-lookup"><span data-stu-id="ec016-204">256</span></span>                                                                                                       |
| <span data-ttu-id="ec016-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec016-205">Search-Flags</span></span>           | <span data-ttu-id="ec016-206">0x00000009</span><span class="sxs-lookup"><span data-stu-id="ec016-206">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="ec016-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec016-207">System-Flags</span></span>           | <span data-ttu-id="ec016-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec016-208">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ec016-209">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ec016-209">Classes used in</span></span>        | [<span data-ttu-id="ec016-210">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="ec016-210">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="ec016-211">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ec016-211">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ec016-212">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ec016-212">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ec016-213">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec016-213">Entry</span></span> | <span data-ttu-id="ec016-214">Valor</span><span class="sxs-lookup"><span data-stu-id="ec016-214">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec016-215">ID do link</span><span class="sxs-lookup"><span data-stu-id="ec016-215">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ec016-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec016-216">MAPI-Id</span></span>                | <span data-ttu-id="ec016-217">0x8171</span><span class="sxs-lookup"><span data-stu-id="ec016-217">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="ec016-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec016-218">System-Only</span></span>            | <span data-ttu-id="ec016-219">Falso</span><span class="sxs-lookup"><span data-stu-id="ec016-219">False</span></span>                                                                                                     |
| <span data-ttu-id="ec016-220">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ec016-220">Is-Single-Valued</span></span>       | <span data-ttu-id="ec016-221">True</span><span class="sxs-lookup"><span data-stu-id="ec016-221">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-222">É indexado</span><span class="sxs-lookup"><span data-stu-id="ec016-222">Is Indexed</span></span>             | <span data-ttu-id="ec016-223">True</span><span class="sxs-lookup"><span data-stu-id="ec016-223">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-224">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ec016-224">In Global Catalog</span></span>      | <span data-ttu-id="ec016-225">True</span><span class="sxs-lookup"><span data-stu-id="ec016-225">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-226">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ec016-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec016-227">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ec016-227">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ec016-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec016-228">Range-Lower</span></span>            | <span data-ttu-id="ec016-229">1</span><span class="sxs-lookup"><span data-stu-id="ec016-229">1</span></span>                                                                                                         |
| <span data-ttu-id="ec016-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec016-230">Range-Upper</span></span>            | <span data-ttu-id="ec016-231">256</span><span class="sxs-lookup"><span data-stu-id="ec016-231">256</span></span>                                                                                                       |
| <span data-ttu-id="ec016-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec016-232">Search-Flags</span></span>           | <span data-ttu-id="ec016-233">0x00000009</span><span class="sxs-lookup"><span data-stu-id="ec016-233">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="ec016-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec016-234">System-Flags</span></span>           | <span data-ttu-id="ec016-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec016-235">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ec016-236">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ec016-236">Classes used in</span></span>        | [<span data-ttu-id="ec016-237">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="ec016-237">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="ec016-238">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ec016-238">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ec016-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec016-239">Windows Server 2008</span></span>



| <span data-ttu-id="ec016-240">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec016-240">Entry</span></span> | <span data-ttu-id="ec016-241">Valor</span><span class="sxs-lookup"><span data-stu-id="ec016-241">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec016-242">ID do link</span><span class="sxs-lookup"><span data-stu-id="ec016-242">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ec016-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec016-243">MAPI-Id</span></span>                | <span data-ttu-id="ec016-244">0x8171</span><span class="sxs-lookup"><span data-stu-id="ec016-244">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="ec016-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec016-245">System-Only</span></span>            | <span data-ttu-id="ec016-246">Falso</span><span class="sxs-lookup"><span data-stu-id="ec016-246">False</span></span>                                                                                                     |
| <span data-ttu-id="ec016-247">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ec016-247">Is-Single-Valued</span></span>       | <span data-ttu-id="ec016-248">True</span><span class="sxs-lookup"><span data-stu-id="ec016-248">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-249">É indexado</span><span class="sxs-lookup"><span data-stu-id="ec016-249">Is Indexed</span></span>             | <span data-ttu-id="ec016-250">True</span><span class="sxs-lookup"><span data-stu-id="ec016-250">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-251">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ec016-251">In Global Catalog</span></span>      | <span data-ttu-id="ec016-252">True</span><span class="sxs-lookup"><span data-stu-id="ec016-252">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-253">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ec016-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec016-254">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ec016-254">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ec016-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec016-255">Range-Lower</span></span>            | <span data-ttu-id="ec016-256">1</span><span class="sxs-lookup"><span data-stu-id="ec016-256">1</span></span>                                                                                                         |
| <span data-ttu-id="ec016-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec016-257">Range-Upper</span></span>            | <span data-ttu-id="ec016-258">256</span><span class="sxs-lookup"><span data-stu-id="ec016-258">256</span></span>                                                                                                       |
| <span data-ttu-id="ec016-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec016-259">Search-Flags</span></span>           | <span data-ttu-id="ec016-260">0x00000009</span><span class="sxs-lookup"><span data-stu-id="ec016-260">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="ec016-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec016-261">System-Flags</span></span>           | <span data-ttu-id="ec016-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec016-262">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ec016-263">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ec016-263">Classes used in</span></span>        | [<span data-ttu-id="ec016-264">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="ec016-264">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="ec016-265">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ec016-265">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ec016-266">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ec016-266">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ec016-267">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec016-267">Entry</span></span> | <span data-ttu-id="ec016-268">Valor</span><span class="sxs-lookup"><span data-stu-id="ec016-268">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec016-269">ID do link</span><span class="sxs-lookup"><span data-stu-id="ec016-269">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ec016-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec016-270">MAPI-Id</span></span>                | <span data-ttu-id="ec016-271">0x8171</span><span class="sxs-lookup"><span data-stu-id="ec016-271">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="ec016-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec016-272">System-Only</span></span>            | <span data-ttu-id="ec016-273">Falso</span><span class="sxs-lookup"><span data-stu-id="ec016-273">False</span></span>                                                                                                     |
| <span data-ttu-id="ec016-274">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ec016-274">Is-Single-Valued</span></span>       | <span data-ttu-id="ec016-275">True</span><span class="sxs-lookup"><span data-stu-id="ec016-275">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-276">É indexado</span><span class="sxs-lookup"><span data-stu-id="ec016-276">Is Indexed</span></span>             | <span data-ttu-id="ec016-277">True</span><span class="sxs-lookup"><span data-stu-id="ec016-277">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-278">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ec016-278">In Global Catalog</span></span>      | <span data-ttu-id="ec016-279">True</span><span class="sxs-lookup"><span data-stu-id="ec016-279">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-280">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ec016-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec016-281">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ec016-281">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ec016-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec016-282">Range-Lower</span></span>            | <span data-ttu-id="ec016-283">1</span><span class="sxs-lookup"><span data-stu-id="ec016-283">1</span></span>                                                                                                         |
| <span data-ttu-id="ec016-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec016-284">Range-Upper</span></span>            | <span data-ttu-id="ec016-285">256</span><span class="sxs-lookup"><span data-stu-id="ec016-285">256</span></span>                                                                                                       |
| <span data-ttu-id="ec016-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec016-286">Search-Flags</span></span>           | <span data-ttu-id="ec016-287">0x00000009</span><span class="sxs-lookup"><span data-stu-id="ec016-287">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="ec016-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec016-288">System-Flags</span></span>           | <span data-ttu-id="ec016-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec016-289">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ec016-290">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ec016-290">Classes used in</span></span>        | [<span data-ttu-id="ec016-291">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="ec016-291">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="ec016-292">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ec016-292">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ec016-293">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec016-293">Windows Server 2012</span></span>



| <span data-ttu-id="ec016-294">Entrada</span><span class="sxs-lookup"><span data-stu-id="ec016-294">Entry</span></span> | <span data-ttu-id="ec016-295">Valor</span><span class="sxs-lookup"><span data-stu-id="ec016-295">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec016-296">ID do link</span><span class="sxs-lookup"><span data-stu-id="ec016-296">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ec016-297">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec016-297">MAPI-Id</span></span>                | <span data-ttu-id="ec016-298">0x8171</span><span class="sxs-lookup"><span data-stu-id="ec016-298">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="ec016-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec016-299">System-Only</span></span>            | <span data-ttu-id="ec016-300">Falso</span><span class="sxs-lookup"><span data-stu-id="ec016-300">False</span></span>                                                                                                     |
| <span data-ttu-id="ec016-301">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ec016-301">Is-Single-Valued</span></span>       | <span data-ttu-id="ec016-302">True</span><span class="sxs-lookup"><span data-stu-id="ec016-302">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-303">É indexado</span><span class="sxs-lookup"><span data-stu-id="ec016-303">Is Indexed</span></span>             | <span data-ttu-id="ec016-304">True</span><span class="sxs-lookup"><span data-stu-id="ec016-304">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-305">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ec016-305">In Global Catalog</span></span>      | <span data-ttu-id="ec016-306">True</span><span class="sxs-lookup"><span data-stu-id="ec016-306">True</span></span>                                                                                                      |
| <span data-ttu-id="ec016-307">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ec016-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec016-308">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ec016-308">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ec016-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec016-309">Range-Lower</span></span>            | <span data-ttu-id="ec016-310">1</span><span class="sxs-lookup"><span data-stu-id="ec016-310">1</span></span>                                                                                                         |
| <span data-ttu-id="ec016-311">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec016-311">Range-Upper</span></span>            | <span data-ttu-id="ec016-312">256</span><span class="sxs-lookup"><span data-stu-id="ec016-312">256</span></span>                                                                                                       |
| <span data-ttu-id="ec016-313">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec016-313">Search-Flags</span></span>           | <span data-ttu-id="ec016-314">0x00000009</span><span class="sxs-lookup"><span data-stu-id="ec016-314">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="ec016-315">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec016-315">System-Flags</span></span>           | <span data-ttu-id="ec016-316">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec016-316">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ec016-317">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ec016-317">Classes used in</span></span>        | [<span data-ttu-id="ec016-318">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="ec016-318">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="ec016-319">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ec016-319">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





