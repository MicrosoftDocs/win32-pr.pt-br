---
title: ms-DS-AZ-LDAP-atributo de consulta
description: Uma cadeia de caracteres que define a consulta LDAP (comprimento máximo 4096) que determina a associação de um objeto de usuário ao grupo.
ms.assetid: e24d4c50-2153-49a6-8aef-4872ccaab13e
ms.tgt_platform: multiple
keywords:
- ms-DS-AZ-LDAP-Query atributo AD Schema
- atributo msDS-AzLDAPQuery do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Az-LDAP-Query
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1f6c21d5ed28a9d2419b16c6ce7986f3250488
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086943"
---
# <a name="ms-ds-az-ldap-query-attribute"></a><span data-ttu-id="90bf0-105">ms-DS-AZ-LDAP-atributo de consulta</span><span class="sxs-lookup"><span data-stu-id="90bf0-105">ms-DS-Az-LDAP-Query attribute</span></span>

<span data-ttu-id="90bf0-106">Uma cadeia de caracteres que define a consulta LDAP (comprimento máximo 4096) que determina a associação de um objeto de usuário ao grupo.</span><span class="sxs-lookup"><span data-stu-id="90bf0-106">A string that defines the LDAP query (max length 4096) which determines the membership of a user object to the group.</span></span>



| <span data-ttu-id="90bf0-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="90bf0-107">Entry</span></span> | <span data-ttu-id="90bf0-108">Valor</span><span class="sxs-lookup"><span data-stu-id="90bf0-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="90bf0-109">CN</span><span class="sxs-lookup"><span data-stu-id="90bf0-109">CN</span></span>                | <span data-ttu-id="90bf0-110">ms-DS-AZ-LDAP-Query</span><span class="sxs-lookup"><span data-stu-id="90bf0-110">ms-DS-Az-LDAP-Query</span></span>                         |
| <span data-ttu-id="90bf0-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="90bf0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="90bf0-112">msDS-AzLDAPQuery</span><span class="sxs-lookup"><span data-stu-id="90bf0-112">msDS-AzLDAPQuery</span></span>                            |
| <span data-ttu-id="90bf0-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="90bf0-113">Size</span></span>              | <span data-ttu-id="90bf0-114">4096 caracteres</span><span class="sxs-lookup"><span data-stu-id="90bf0-114">4096 characters</span></span>                             |
| <span data-ttu-id="90bf0-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="90bf0-115">Update Privilege</span></span>  | <span data-ttu-id="90bf0-116">Administrador do AzRoles</span><span class="sxs-lookup"><span data-stu-id="90bf0-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="90bf0-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="90bf0-117">Update Frequency</span></span>  | <span data-ttu-id="90bf0-118">Durante a inicialização ou a alteração da política.</span><span class="sxs-lookup"><span data-stu-id="90bf0-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="90bf0-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="90bf0-119">Attribute-Id</span></span>      | <span data-ttu-id="90bf0-120">1.2.840.113556.1.4.1792</span><span class="sxs-lookup"><span data-stu-id="90bf0-120">1.2.840.113556.1.4.1792</span></span>                     |
| <span data-ttu-id="90bf0-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="90bf0-121">System-Id-Guid</span></span>    | <span data-ttu-id="90bf0-122">5e53368b-fc94-45c8-9d7d-daf31ee7112d</span><span class="sxs-lookup"><span data-stu-id="90bf0-122">5e53368b-fc94-45c8-9d7d-daf31ee7112d</span></span>        |
| <span data-ttu-id="90bf0-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="90bf0-123">Syntax</span></span>            | [<span data-ttu-id="90bf0-124">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="90bf0-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="90bf0-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="90bf0-125">Implementations</span></span>

-   [<span data-ttu-id="90bf0-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="90bf0-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="90bf0-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="90bf0-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="90bf0-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="90bf0-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="90bf0-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="90bf0-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="90bf0-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="90bf0-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="90bf0-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="90bf0-131">Windows Server 2003</span></span>



| <span data-ttu-id="90bf0-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="90bf0-132">Entry</span></span> | <span data-ttu-id="90bf0-133">Valor</span><span class="sxs-lookup"><span data-stu-id="90bf0-133">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="90bf0-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="90bf0-134">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="90bf0-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90bf0-135">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="90bf0-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="90bf0-136">System-Only</span></span>            | <span data-ttu-id="90bf0-137">Falso</span><span class="sxs-lookup"><span data-stu-id="90bf0-137">False</span></span>                               |
| <span data-ttu-id="90bf0-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="90bf0-138">Is-Single-Valued</span></span>       | <span data-ttu-id="90bf0-139">True</span><span class="sxs-lookup"><span data-stu-id="90bf0-139">True</span></span>                                |
| <span data-ttu-id="90bf0-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="90bf0-140">Is Indexed</span></span>             | <span data-ttu-id="90bf0-141">Falso</span><span class="sxs-lookup"><span data-stu-id="90bf0-141">False</span></span>                               |
| <span data-ttu-id="90bf0-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="90bf0-142">In Global Catalog</span></span>      | <span data-ttu-id="90bf0-143">Falso</span><span class="sxs-lookup"><span data-stu-id="90bf0-143">False</span></span>                               |
| <span data-ttu-id="90bf0-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="90bf0-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="90bf0-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="90bf0-145">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="90bf0-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90bf0-146">Range-Lower</span></span>            | <span data-ttu-id="90bf0-147">0</span><span class="sxs-lookup"><span data-stu-id="90bf0-147">0</span></span>                                   |
| <span data-ttu-id="90bf0-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90bf0-148">Range-Upper</span></span>            | <span data-ttu-id="90bf0-149">4096</span><span class="sxs-lookup"><span data-stu-id="90bf0-149">4096</span></span>                                |
| <span data-ttu-id="90bf0-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90bf0-150">Search-Flags</span></span>           | <span data-ttu-id="90bf0-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90bf0-151">0x00000000</span></span>                          |
| <span data-ttu-id="90bf0-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90bf0-152">System-Flags</span></span>           | <span data-ttu-id="90bf0-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90bf0-153">0x00000010</span></span>                          |
| <span data-ttu-id="90bf0-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="90bf0-154">Classes used in</span></span>        | [<span data-ttu-id="90bf0-155">**Group**</span><span class="sxs-lookup"><span data-stu-id="90bf0-155">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="90bf0-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="90bf0-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="90bf0-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="90bf0-157">Entry</span></span> | <span data-ttu-id="90bf0-158">Valor</span><span class="sxs-lookup"><span data-stu-id="90bf0-158">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="90bf0-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="90bf0-159">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="90bf0-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90bf0-160">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="90bf0-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="90bf0-161">System-Only</span></span>            | <span data-ttu-id="90bf0-162">Falso</span><span class="sxs-lookup"><span data-stu-id="90bf0-162">False</span></span>                               |
| <span data-ttu-id="90bf0-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="90bf0-163">Is-Single-Valued</span></span>       | <span data-ttu-id="90bf0-164">True</span><span class="sxs-lookup"><span data-stu-id="90bf0-164">True</span></span>                                |
| <span data-ttu-id="90bf0-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="90bf0-165">Is Indexed</span></span>             | <span data-ttu-id="90bf0-166">Falso</span><span class="sxs-lookup"><span data-stu-id="90bf0-166">False</span></span>                               |
| <span data-ttu-id="90bf0-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="90bf0-167">In Global Catalog</span></span>      | <span data-ttu-id="90bf0-168">Falso</span><span class="sxs-lookup"><span data-stu-id="90bf0-168">False</span></span>                               |
| <span data-ttu-id="90bf0-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="90bf0-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="90bf0-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="90bf0-170">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="90bf0-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90bf0-171">Range-Lower</span></span>            | <span data-ttu-id="90bf0-172">0</span><span class="sxs-lookup"><span data-stu-id="90bf0-172">0</span></span>                                   |
| <span data-ttu-id="90bf0-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90bf0-173">Range-Upper</span></span>            | <span data-ttu-id="90bf0-174">4096</span><span class="sxs-lookup"><span data-stu-id="90bf0-174">4096</span></span>                                |
| <span data-ttu-id="90bf0-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90bf0-175">Search-Flags</span></span>           | <span data-ttu-id="90bf0-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90bf0-176">0x00000000</span></span>                          |
| <span data-ttu-id="90bf0-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90bf0-177">System-Flags</span></span>           | <span data-ttu-id="90bf0-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90bf0-178">0x00000010</span></span>                          |
| <span data-ttu-id="90bf0-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="90bf0-179">Classes used in</span></span>        | [<span data-ttu-id="90bf0-180">**Group**</span><span class="sxs-lookup"><span data-stu-id="90bf0-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="90bf0-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90bf0-181">Windows Server 2008</span></span>



| <span data-ttu-id="90bf0-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="90bf0-182">Entry</span></span> | <span data-ttu-id="90bf0-183">Valor</span><span class="sxs-lookup"><span data-stu-id="90bf0-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="90bf0-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="90bf0-184">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="90bf0-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90bf0-185">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="90bf0-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="90bf0-186">System-Only</span></span>            | <span data-ttu-id="90bf0-187">Falso</span><span class="sxs-lookup"><span data-stu-id="90bf0-187">False</span></span>                               |
| <span data-ttu-id="90bf0-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="90bf0-188">Is-Single-Valued</span></span>       | <span data-ttu-id="90bf0-189">True</span><span class="sxs-lookup"><span data-stu-id="90bf0-189">True</span></span>                                |
| <span data-ttu-id="90bf0-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="90bf0-190">Is Indexed</span></span>             | <span data-ttu-id="90bf0-191">Falso</span><span class="sxs-lookup"><span data-stu-id="90bf0-191">False</span></span>                               |
| <span data-ttu-id="90bf0-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="90bf0-192">In Global Catalog</span></span>      | <span data-ttu-id="90bf0-193">Falso</span><span class="sxs-lookup"><span data-stu-id="90bf0-193">False</span></span>                               |
| <span data-ttu-id="90bf0-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="90bf0-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="90bf0-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="90bf0-195">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="90bf0-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90bf0-196">Range-Lower</span></span>            | <span data-ttu-id="90bf0-197">0</span><span class="sxs-lookup"><span data-stu-id="90bf0-197">0</span></span>                                   |
| <span data-ttu-id="90bf0-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90bf0-198">Range-Upper</span></span>            | <span data-ttu-id="90bf0-199">4096</span><span class="sxs-lookup"><span data-stu-id="90bf0-199">4096</span></span>                                |
| <span data-ttu-id="90bf0-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90bf0-200">Search-Flags</span></span>           | <span data-ttu-id="90bf0-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90bf0-201">0x00000000</span></span>                          |
| <span data-ttu-id="90bf0-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90bf0-202">System-Flags</span></span>           | <span data-ttu-id="90bf0-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90bf0-203">0x00000010</span></span>                          |
| <span data-ttu-id="90bf0-204">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="90bf0-204">Classes used in</span></span>        | [<span data-ttu-id="90bf0-205">**Group**</span><span class="sxs-lookup"><span data-stu-id="90bf0-205">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="90bf0-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="90bf0-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="90bf0-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="90bf0-207">Entry</span></span> | <span data-ttu-id="90bf0-208">Valor</span><span class="sxs-lookup"><span data-stu-id="90bf0-208">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="90bf0-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="90bf0-209">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="90bf0-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90bf0-210">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="90bf0-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="90bf0-211">System-Only</span></span>            | <span data-ttu-id="90bf0-212">Falso</span><span class="sxs-lookup"><span data-stu-id="90bf0-212">False</span></span>                               |
| <span data-ttu-id="90bf0-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="90bf0-213">Is-Single-Valued</span></span>       | <span data-ttu-id="90bf0-214">True</span><span class="sxs-lookup"><span data-stu-id="90bf0-214">True</span></span>                                |
| <span data-ttu-id="90bf0-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="90bf0-215">Is Indexed</span></span>             | <span data-ttu-id="90bf0-216">Falso</span><span class="sxs-lookup"><span data-stu-id="90bf0-216">False</span></span>                               |
| <span data-ttu-id="90bf0-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="90bf0-217">In Global Catalog</span></span>      | <span data-ttu-id="90bf0-218">Falso</span><span class="sxs-lookup"><span data-stu-id="90bf0-218">False</span></span>                               |
| <span data-ttu-id="90bf0-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="90bf0-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="90bf0-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="90bf0-220">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="90bf0-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90bf0-221">Range-Lower</span></span>            | <span data-ttu-id="90bf0-222">0</span><span class="sxs-lookup"><span data-stu-id="90bf0-222">0</span></span>                                   |
| <span data-ttu-id="90bf0-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90bf0-223">Range-Upper</span></span>            | <span data-ttu-id="90bf0-224">4096</span><span class="sxs-lookup"><span data-stu-id="90bf0-224">4096</span></span>                                |
| <span data-ttu-id="90bf0-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90bf0-225">Search-Flags</span></span>           | <span data-ttu-id="90bf0-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90bf0-226">0x00000000</span></span>                          |
| <span data-ttu-id="90bf0-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90bf0-227">System-Flags</span></span>           | <span data-ttu-id="90bf0-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90bf0-228">0x00000010</span></span>                          |
| <span data-ttu-id="90bf0-229">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="90bf0-229">Classes used in</span></span>        | [<span data-ttu-id="90bf0-230">**Group**</span><span class="sxs-lookup"><span data-stu-id="90bf0-230">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="90bf0-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="90bf0-231">Windows Server 2012</span></span>



| <span data-ttu-id="90bf0-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="90bf0-232">Entry</span></span> | <span data-ttu-id="90bf0-233">Valor</span><span class="sxs-lookup"><span data-stu-id="90bf0-233">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="90bf0-234">ID do link</span><span class="sxs-lookup"><span data-stu-id="90bf0-234">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="90bf0-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90bf0-235">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="90bf0-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="90bf0-236">System-Only</span></span>            | <span data-ttu-id="90bf0-237">Falso</span><span class="sxs-lookup"><span data-stu-id="90bf0-237">False</span></span>                               |
| <span data-ttu-id="90bf0-238">É de valor único</span><span class="sxs-lookup"><span data-stu-id="90bf0-238">Is-Single-Valued</span></span>       | <span data-ttu-id="90bf0-239">True</span><span class="sxs-lookup"><span data-stu-id="90bf0-239">True</span></span>                                |
| <span data-ttu-id="90bf0-240">É indexado</span><span class="sxs-lookup"><span data-stu-id="90bf0-240">Is Indexed</span></span>             | <span data-ttu-id="90bf0-241">Falso</span><span class="sxs-lookup"><span data-stu-id="90bf0-241">False</span></span>                               |
| <span data-ttu-id="90bf0-242">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="90bf0-242">In Global Catalog</span></span>      | <span data-ttu-id="90bf0-243">Falso</span><span class="sxs-lookup"><span data-stu-id="90bf0-243">False</span></span>                               |
| <span data-ttu-id="90bf0-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="90bf0-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="90bf0-245">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="90bf0-245">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="90bf0-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90bf0-246">Range-Lower</span></span>            | <span data-ttu-id="90bf0-247">0</span><span class="sxs-lookup"><span data-stu-id="90bf0-247">0</span></span>                                   |
| <span data-ttu-id="90bf0-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90bf0-248">Range-Upper</span></span>            | <span data-ttu-id="90bf0-249">4096</span><span class="sxs-lookup"><span data-stu-id="90bf0-249">4096</span></span>                                |
| <span data-ttu-id="90bf0-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90bf0-250">Search-Flags</span></span>           | <span data-ttu-id="90bf0-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90bf0-251">0x00000000</span></span>                          |
| <span data-ttu-id="90bf0-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90bf0-252">System-Flags</span></span>           | <span data-ttu-id="90bf0-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90bf0-253">0x00000010</span></span>                          |
| <span data-ttu-id="90bf0-254">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="90bf0-254">Classes used in</span></span>        | [<span data-ttu-id="90bf0-255">**Group**</span><span class="sxs-lookup"><span data-stu-id="90bf0-255">**Group**</span></span>](c-group.md)<br/> |



 

 





