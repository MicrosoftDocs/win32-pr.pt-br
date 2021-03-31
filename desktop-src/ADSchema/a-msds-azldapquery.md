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
# <a name="ms-ds-az-ldap-query-attribute"></a><span data-ttu-id="2e676-105">ms-DS-AZ-LDAP-atributo de consulta</span><span class="sxs-lookup"><span data-stu-id="2e676-105">ms-DS-Az-LDAP-Query attribute</span></span>

<span data-ttu-id="2e676-106">Uma cadeia de caracteres que define a consulta LDAP (comprimento máximo 4096) que determina a associação de um objeto de usuário ao grupo.</span><span class="sxs-lookup"><span data-stu-id="2e676-106">A string that defines the LDAP query (max length 4096) which determines the membership of a user object to the group.</span></span>



| <span data-ttu-id="2e676-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e676-107">Entry</span></span> | <span data-ttu-id="2e676-108">Valor</span><span class="sxs-lookup"><span data-stu-id="2e676-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="2e676-109">CN</span><span class="sxs-lookup"><span data-stu-id="2e676-109">CN</span></span>                | <span data-ttu-id="2e676-110">ms-DS-AZ-LDAP-Query</span><span class="sxs-lookup"><span data-stu-id="2e676-110">ms-DS-Az-LDAP-Query</span></span>                         |
| <span data-ttu-id="2e676-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2e676-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2e676-112">msDS-AzLDAPQuery</span><span class="sxs-lookup"><span data-stu-id="2e676-112">msDS-AzLDAPQuery</span></span>                            |
| <span data-ttu-id="2e676-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="2e676-113">Size</span></span>              | <span data-ttu-id="2e676-114">4096 caracteres</span><span class="sxs-lookup"><span data-stu-id="2e676-114">4096 characters</span></span>                             |
| <span data-ttu-id="2e676-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="2e676-115">Update Privilege</span></span>  | <span data-ttu-id="2e676-116">Administrador do AzRoles</span><span class="sxs-lookup"><span data-stu-id="2e676-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="2e676-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="2e676-117">Update Frequency</span></span>  | <span data-ttu-id="2e676-118">Durante a inicialização ou a alteração da política.</span><span class="sxs-lookup"><span data-stu-id="2e676-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="2e676-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2e676-119">Attribute-Id</span></span>      | <span data-ttu-id="2e676-120">1.2.840.113556.1.4.1792</span><span class="sxs-lookup"><span data-stu-id="2e676-120">1.2.840.113556.1.4.1792</span></span>                     |
| <span data-ttu-id="2e676-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2e676-121">System-Id-Guid</span></span>    | <span data-ttu-id="2e676-122">5e53368b-fc94-45c8-9d7d-daf31ee7112d</span><span class="sxs-lookup"><span data-stu-id="2e676-122">5e53368b-fc94-45c8-9d7d-daf31ee7112d</span></span>        |
| <span data-ttu-id="2e676-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e676-123">Syntax</span></span>            | [<span data-ttu-id="2e676-124">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="2e676-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="2e676-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="2e676-125">Implementations</span></span>

-   [<span data-ttu-id="2e676-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2e676-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2e676-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2e676-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2e676-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2e676-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2e676-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2e676-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2e676-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2e676-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="2e676-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2e676-131">Windows Server 2003</span></span>



| <span data-ttu-id="2e676-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e676-132">Entry</span></span> | <span data-ttu-id="2e676-133">Valor</span><span class="sxs-lookup"><span data-stu-id="2e676-133">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="2e676-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="2e676-134">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="2e676-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e676-135">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="2e676-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e676-136">System-Only</span></span>            | <span data-ttu-id="2e676-137">Falso</span><span class="sxs-lookup"><span data-stu-id="2e676-137">False</span></span>                               |
| <span data-ttu-id="2e676-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2e676-138">Is-Single-Valued</span></span>       | <span data-ttu-id="2e676-139">True</span><span class="sxs-lookup"><span data-stu-id="2e676-139">True</span></span>                                |
| <span data-ttu-id="2e676-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="2e676-140">Is Indexed</span></span>             | <span data-ttu-id="2e676-141">Falso</span><span class="sxs-lookup"><span data-stu-id="2e676-141">False</span></span>                               |
| <span data-ttu-id="2e676-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2e676-142">In Global Catalog</span></span>      | <span data-ttu-id="2e676-143">Falso</span><span class="sxs-lookup"><span data-stu-id="2e676-143">False</span></span>                               |
| <span data-ttu-id="2e676-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2e676-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e676-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2e676-145">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="2e676-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e676-146">Range-Lower</span></span>            | <span data-ttu-id="2e676-147">0</span><span class="sxs-lookup"><span data-stu-id="2e676-147">0</span></span>                                   |
| <span data-ttu-id="2e676-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e676-148">Range-Upper</span></span>            | <span data-ttu-id="2e676-149">4096</span><span class="sxs-lookup"><span data-stu-id="2e676-149">4096</span></span>                                |
| <span data-ttu-id="2e676-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e676-150">Search-Flags</span></span>           | <span data-ttu-id="2e676-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e676-151">0x00000000</span></span>                          |
| <span data-ttu-id="2e676-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e676-152">System-Flags</span></span>           | <span data-ttu-id="2e676-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e676-153">0x00000010</span></span>                          |
| <span data-ttu-id="2e676-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2e676-154">Classes used in</span></span>        | [<span data-ttu-id="2e676-155">**Group**</span><span class="sxs-lookup"><span data-stu-id="2e676-155">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2e676-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2e676-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2e676-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e676-157">Entry</span></span> | <span data-ttu-id="2e676-158">Valor</span><span class="sxs-lookup"><span data-stu-id="2e676-158">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="2e676-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="2e676-159">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="2e676-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e676-160">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="2e676-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e676-161">System-Only</span></span>            | <span data-ttu-id="2e676-162">Falso</span><span class="sxs-lookup"><span data-stu-id="2e676-162">False</span></span>                               |
| <span data-ttu-id="2e676-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2e676-163">Is-Single-Valued</span></span>       | <span data-ttu-id="2e676-164">True</span><span class="sxs-lookup"><span data-stu-id="2e676-164">True</span></span>                                |
| <span data-ttu-id="2e676-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="2e676-165">Is Indexed</span></span>             | <span data-ttu-id="2e676-166">Falso</span><span class="sxs-lookup"><span data-stu-id="2e676-166">False</span></span>                               |
| <span data-ttu-id="2e676-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2e676-167">In Global Catalog</span></span>      | <span data-ttu-id="2e676-168">Falso</span><span class="sxs-lookup"><span data-stu-id="2e676-168">False</span></span>                               |
| <span data-ttu-id="2e676-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2e676-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e676-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2e676-170">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="2e676-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e676-171">Range-Lower</span></span>            | <span data-ttu-id="2e676-172">0</span><span class="sxs-lookup"><span data-stu-id="2e676-172">0</span></span>                                   |
| <span data-ttu-id="2e676-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e676-173">Range-Upper</span></span>            | <span data-ttu-id="2e676-174">4096</span><span class="sxs-lookup"><span data-stu-id="2e676-174">4096</span></span>                                |
| <span data-ttu-id="2e676-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e676-175">Search-Flags</span></span>           | <span data-ttu-id="2e676-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e676-176">0x00000000</span></span>                          |
| <span data-ttu-id="2e676-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e676-177">System-Flags</span></span>           | <span data-ttu-id="2e676-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e676-178">0x00000010</span></span>                          |
| <span data-ttu-id="2e676-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2e676-179">Classes used in</span></span>        | [<span data-ttu-id="2e676-180">**Group**</span><span class="sxs-lookup"><span data-stu-id="2e676-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2e676-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e676-181">Windows Server 2008</span></span>



| <span data-ttu-id="2e676-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e676-182">Entry</span></span> | <span data-ttu-id="2e676-183">Valor</span><span class="sxs-lookup"><span data-stu-id="2e676-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="2e676-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="2e676-184">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="2e676-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e676-185">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="2e676-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e676-186">System-Only</span></span>            | <span data-ttu-id="2e676-187">Falso</span><span class="sxs-lookup"><span data-stu-id="2e676-187">False</span></span>                               |
| <span data-ttu-id="2e676-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2e676-188">Is-Single-Valued</span></span>       | <span data-ttu-id="2e676-189">True</span><span class="sxs-lookup"><span data-stu-id="2e676-189">True</span></span>                                |
| <span data-ttu-id="2e676-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="2e676-190">Is Indexed</span></span>             | <span data-ttu-id="2e676-191">Falso</span><span class="sxs-lookup"><span data-stu-id="2e676-191">False</span></span>                               |
| <span data-ttu-id="2e676-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2e676-192">In Global Catalog</span></span>      | <span data-ttu-id="2e676-193">Falso</span><span class="sxs-lookup"><span data-stu-id="2e676-193">False</span></span>                               |
| <span data-ttu-id="2e676-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2e676-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e676-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2e676-195">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="2e676-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e676-196">Range-Lower</span></span>            | <span data-ttu-id="2e676-197">0</span><span class="sxs-lookup"><span data-stu-id="2e676-197">0</span></span>                                   |
| <span data-ttu-id="2e676-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e676-198">Range-Upper</span></span>            | <span data-ttu-id="2e676-199">4096</span><span class="sxs-lookup"><span data-stu-id="2e676-199">4096</span></span>                                |
| <span data-ttu-id="2e676-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e676-200">Search-Flags</span></span>           | <span data-ttu-id="2e676-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e676-201">0x00000000</span></span>                          |
| <span data-ttu-id="2e676-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e676-202">System-Flags</span></span>           | <span data-ttu-id="2e676-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e676-203">0x00000010</span></span>                          |
| <span data-ttu-id="2e676-204">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2e676-204">Classes used in</span></span>        | [<span data-ttu-id="2e676-205">**Group**</span><span class="sxs-lookup"><span data-stu-id="2e676-205">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2e676-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2e676-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2e676-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e676-207">Entry</span></span> | <span data-ttu-id="2e676-208">Valor</span><span class="sxs-lookup"><span data-stu-id="2e676-208">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="2e676-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="2e676-209">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="2e676-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e676-210">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="2e676-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e676-211">System-Only</span></span>            | <span data-ttu-id="2e676-212">Falso</span><span class="sxs-lookup"><span data-stu-id="2e676-212">False</span></span>                               |
| <span data-ttu-id="2e676-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2e676-213">Is-Single-Valued</span></span>       | <span data-ttu-id="2e676-214">True</span><span class="sxs-lookup"><span data-stu-id="2e676-214">True</span></span>                                |
| <span data-ttu-id="2e676-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="2e676-215">Is Indexed</span></span>             | <span data-ttu-id="2e676-216">Falso</span><span class="sxs-lookup"><span data-stu-id="2e676-216">False</span></span>                               |
| <span data-ttu-id="2e676-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2e676-217">In Global Catalog</span></span>      | <span data-ttu-id="2e676-218">Falso</span><span class="sxs-lookup"><span data-stu-id="2e676-218">False</span></span>                               |
| <span data-ttu-id="2e676-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2e676-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e676-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2e676-220">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="2e676-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e676-221">Range-Lower</span></span>            | <span data-ttu-id="2e676-222">0</span><span class="sxs-lookup"><span data-stu-id="2e676-222">0</span></span>                                   |
| <span data-ttu-id="2e676-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e676-223">Range-Upper</span></span>            | <span data-ttu-id="2e676-224">4096</span><span class="sxs-lookup"><span data-stu-id="2e676-224">4096</span></span>                                |
| <span data-ttu-id="2e676-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e676-225">Search-Flags</span></span>           | <span data-ttu-id="2e676-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e676-226">0x00000000</span></span>                          |
| <span data-ttu-id="2e676-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e676-227">System-Flags</span></span>           | <span data-ttu-id="2e676-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e676-228">0x00000010</span></span>                          |
| <span data-ttu-id="2e676-229">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2e676-229">Classes used in</span></span>        | [<span data-ttu-id="2e676-230">**Group**</span><span class="sxs-lookup"><span data-stu-id="2e676-230">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2e676-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e676-231">Windows Server 2012</span></span>



| <span data-ttu-id="2e676-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e676-232">Entry</span></span> | <span data-ttu-id="2e676-233">Valor</span><span class="sxs-lookup"><span data-stu-id="2e676-233">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="2e676-234">ID do link</span><span class="sxs-lookup"><span data-stu-id="2e676-234">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="2e676-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e676-235">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="2e676-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e676-236">System-Only</span></span>            | <span data-ttu-id="2e676-237">Falso</span><span class="sxs-lookup"><span data-stu-id="2e676-237">False</span></span>                               |
| <span data-ttu-id="2e676-238">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2e676-238">Is-Single-Valued</span></span>       | <span data-ttu-id="2e676-239">True</span><span class="sxs-lookup"><span data-stu-id="2e676-239">True</span></span>                                |
| <span data-ttu-id="2e676-240">É indexado</span><span class="sxs-lookup"><span data-stu-id="2e676-240">Is Indexed</span></span>             | <span data-ttu-id="2e676-241">Falso</span><span class="sxs-lookup"><span data-stu-id="2e676-241">False</span></span>                               |
| <span data-ttu-id="2e676-242">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2e676-242">In Global Catalog</span></span>      | <span data-ttu-id="2e676-243">Falso</span><span class="sxs-lookup"><span data-stu-id="2e676-243">False</span></span>                               |
| <span data-ttu-id="2e676-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2e676-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e676-245">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2e676-245">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="2e676-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e676-246">Range-Lower</span></span>            | <span data-ttu-id="2e676-247">0</span><span class="sxs-lookup"><span data-stu-id="2e676-247">0</span></span>                                   |
| <span data-ttu-id="2e676-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e676-248">Range-Upper</span></span>            | <span data-ttu-id="2e676-249">4096</span><span class="sxs-lookup"><span data-stu-id="2e676-249">4096</span></span>                                |
| <span data-ttu-id="2e676-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e676-250">Search-Flags</span></span>           | <span data-ttu-id="2e676-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e676-251">0x00000000</span></span>                          |
| <span data-ttu-id="2e676-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e676-252">System-Flags</span></span>           | <span data-ttu-id="2e676-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e676-253">0x00000010</span></span>                          |
| <span data-ttu-id="2e676-254">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2e676-254">Classes used in</span></span>        | [<span data-ttu-id="2e676-255">**Group**</span><span class="sxs-lookup"><span data-stu-id="2e676-255">**Group**</span></span>](c-group.md)<br/> |



 

 





