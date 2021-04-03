---
title: ms-DS-allowed-atributo DNS-Suffixs
description: A lista de sufixos permitidos para o atributo dNSHostName em objetos de computador.
ms.assetid: acd57af8-a021-4704-8a56-304126cd3d4b
ms.tgt_platform: multiple
keywords:
- ms-DS-allowed-DNS-sufixos atributo AD Schema
- atributo msDS-AllowedDNSSuffixes do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Allowed-DNS-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46c3e4848f96c68041bfdc5f3f1cc9533b52d3e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645461"
---
# <a name="ms-ds-allowed-dns-suffixes-attribute"></a><span data-ttu-id="bb4aa-105">ms-DS-allowed-atributo DNS-Suffixs</span><span class="sxs-lookup"><span data-stu-id="bb4aa-105">ms-DS-Allowed-DNS-Suffixes attribute</span></span>

<span data-ttu-id="bb4aa-106">A lista de sufixos permitidos para o atributo dNSHostName em objetos de computador.</span><span class="sxs-lookup"><span data-stu-id="bb4aa-106">The list of allowed suffixes for the dNSHostName attribute in computer objects.</span></span>



| <span data-ttu-id="bb4aa-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb4aa-107">Entry</span></span> | <span data-ttu-id="bb4aa-108">Valor</span><span class="sxs-lookup"><span data-stu-id="bb4aa-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="bb4aa-109">CN</span><span class="sxs-lookup"><span data-stu-id="bb4aa-109">CN</span></span>                | <span data-ttu-id="bb4aa-110">ms-DS-allowed-sufixos-DNS</span><span class="sxs-lookup"><span data-stu-id="bb4aa-110">ms-DS-Allowed-DNS-Suffixes</span></span>                  |
| <span data-ttu-id="bb4aa-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bb4aa-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bb4aa-112">msDS-AllowedDNSSuffixes</span><span class="sxs-lookup"><span data-stu-id="bb4aa-112">msDS-AllowedDNSSuffixes</span></span>                     |
| <span data-ttu-id="bb4aa-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="bb4aa-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="bb4aa-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="bb4aa-114">Update Privilege</span></span>  | <span data-ttu-id="bb4aa-115">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="bb4aa-115">Domain administrator</span></span>                        |
| <span data-ttu-id="bb4aa-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="bb4aa-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="bb4aa-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bb4aa-117">Attribute-Id</span></span>      | <span data-ttu-id="bb4aa-118">1.2.840.113556.1.4.1710</span><span class="sxs-lookup"><span data-stu-id="bb4aa-118">1.2.840.113556.1.4.1710</span></span>                     |
| <span data-ttu-id="bb4aa-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bb4aa-119">System-Id-Guid</span></span>    | <span data-ttu-id="bb4aa-120">8469441b-9ac4-4e45-8205-bd219dbf672d</span><span class="sxs-lookup"><span data-stu-id="bb4aa-120">8469441b-9ac4-4e45-8205-bd219dbf672d</span></span>        |
| <span data-ttu-id="bb4aa-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb4aa-121">Syntax</span></span>            | [<span data-ttu-id="bb4aa-122">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bb4aa-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="bb4aa-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="bb4aa-123">Implementations</span></span>

-   [<span data-ttu-id="bb4aa-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bb4aa-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bb4aa-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bb4aa-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bb4aa-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bb4aa-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bb4aa-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bb4aa-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bb4aa-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bb4aa-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bb4aa-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bb4aa-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="bb4aa-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bb4aa-130">Windows Server 2003</span></span>



| <span data-ttu-id="bb4aa-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb4aa-131">Entry</span></span> | <span data-ttu-id="bb4aa-132">Valor</span><span class="sxs-lookup"><span data-stu-id="bb4aa-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="bb4aa-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="bb4aa-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="bb4aa-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb4aa-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="bb4aa-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb4aa-135">System-Only</span></span>            | <span data-ttu-id="bb4aa-136">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-136">False</span></span>                                        |
| <span data-ttu-id="bb4aa-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bb4aa-137">Is-Single-Valued</span></span>       | <span data-ttu-id="bb4aa-138">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-138">False</span></span>                                        |
| <span data-ttu-id="bb4aa-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="bb4aa-139">Is Indexed</span></span>             | <span data-ttu-id="bb4aa-140">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-140">False</span></span>                                        |
| <span data-ttu-id="bb4aa-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bb4aa-141">In Global Catalog</span></span>      | <span data-ttu-id="bb4aa-142">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-142">False</span></span>                                        |
| <span data-ttu-id="bb4aa-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bb4aa-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb4aa-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bb4aa-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="bb4aa-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb4aa-145">Range-Lower</span></span>            | <span data-ttu-id="bb4aa-146">0</span><span class="sxs-lookup"><span data-stu-id="bb4aa-146">0</span></span>                                            |
| <span data-ttu-id="bb4aa-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb4aa-147">Range-Upper</span></span>            | <span data-ttu-id="bb4aa-148">2.048</span><span class="sxs-lookup"><span data-stu-id="bb4aa-148">2048</span></span>                                         |
| <span data-ttu-id="bb4aa-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb4aa-149">Search-Flags</span></span>           | <span data-ttu-id="bb4aa-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb4aa-150">0x00000000</span></span>                                   |
| <span data-ttu-id="bb4aa-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb4aa-151">System-Flags</span></span>           | <span data-ttu-id="bb4aa-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb4aa-152">0x00000010</span></span>                                   |
| <span data-ttu-id="bb4aa-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bb4aa-153">Classes used in</span></span>        | [<span data-ttu-id="bb4aa-154">**Domínio-DNS**</span><span class="sxs-lookup"><span data-stu-id="bb4aa-154">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bb4aa-155">ADAM</span><span class="sxs-lookup"><span data-stu-id="bb4aa-155">ADAM</span></span>



| <span data-ttu-id="bb4aa-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb4aa-156">Entry</span></span> | <span data-ttu-id="bb4aa-157">Valor</span><span class="sxs-lookup"><span data-stu-id="bb4aa-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="bb4aa-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="bb4aa-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="bb4aa-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb4aa-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="bb4aa-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb4aa-160">System-Only</span></span>            | <span data-ttu-id="bb4aa-161">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-161">False</span></span>                                        |
| <span data-ttu-id="bb4aa-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bb4aa-162">Is-Single-Valued</span></span>       | <span data-ttu-id="bb4aa-163">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-163">False</span></span>                                        |
| <span data-ttu-id="bb4aa-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="bb4aa-164">Is Indexed</span></span>             | <span data-ttu-id="bb4aa-165">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-165">False</span></span>                                        |
| <span data-ttu-id="bb4aa-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bb4aa-166">In Global Catalog</span></span>      | <span data-ttu-id="bb4aa-167">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-167">False</span></span>                                        |
| <span data-ttu-id="bb4aa-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bb4aa-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb4aa-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bb4aa-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="bb4aa-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb4aa-170">Range-Lower</span></span>            | <span data-ttu-id="bb4aa-171">0</span><span class="sxs-lookup"><span data-stu-id="bb4aa-171">0</span></span>                                            |
| <span data-ttu-id="bb4aa-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb4aa-172">Range-Upper</span></span>            | <span data-ttu-id="bb4aa-173">2.048</span><span class="sxs-lookup"><span data-stu-id="bb4aa-173">2048</span></span>                                         |
| <span data-ttu-id="bb4aa-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb4aa-174">Search-Flags</span></span>           | <span data-ttu-id="bb4aa-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb4aa-175">0x00000000</span></span>                                   |
| <span data-ttu-id="bb4aa-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb4aa-176">System-Flags</span></span>           | <span data-ttu-id="bb4aa-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb4aa-177">0x00000010</span></span>                                   |
| <span data-ttu-id="bb4aa-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bb4aa-178">Classes used in</span></span>        | [<span data-ttu-id="bb4aa-179">**Domínio-DNS**</span><span class="sxs-lookup"><span data-stu-id="bb4aa-179">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bb4aa-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bb4aa-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bb4aa-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb4aa-181">Entry</span></span> | <span data-ttu-id="bb4aa-182">Valor</span><span class="sxs-lookup"><span data-stu-id="bb4aa-182">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="bb4aa-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="bb4aa-183">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="bb4aa-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb4aa-184">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="bb4aa-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb4aa-185">System-Only</span></span>            | <span data-ttu-id="bb4aa-186">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-186">False</span></span>                                        |
| <span data-ttu-id="bb4aa-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bb4aa-187">Is-Single-Valued</span></span>       | <span data-ttu-id="bb4aa-188">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-188">False</span></span>                                        |
| <span data-ttu-id="bb4aa-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="bb4aa-189">Is Indexed</span></span>             | <span data-ttu-id="bb4aa-190">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-190">False</span></span>                                        |
| <span data-ttu-id="bb4aa-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bb4aa-191">In Global Catalog</span></span>      | <span data-ttu-id="bb4aa-192">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-192">False</span></span>                                        |
| <span data-ttu-id="bb4aa-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bb4aa-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb4aa-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bb4aa-194">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="bb4aa-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb4aa-195">Range-Lower</span></span>            | <span data-ttu-id="bb4aa-196">0</span><span class="sxs-lookup"><span data-stu-id="bb4aa-196">0</span></span>                                            |
| <span data-ttu-id="bb4aa-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb4aa-197">Range-Upper</span></span>            | <span data-ttu-id="bb4aa-198">2.048</span><span class="sxs-lookup"><span data-stu-id="bb4aa-198">2048</span></span>                                         |
| <span data-ttu-id="bb4aa-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb4aa-199">Search-Flags</span></span>           | <span data-ttu-id="bb4aa-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb4aa-200">0x00000000</span></span>                                   |
| <span data-ttu-id="bb4aa-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb4aa-201">System-Flags</span></span>           | <span data-ttu-id="bb4aa-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb4aa-202">0x00000010</span></span>                                   |
| <span data-ttu-id="bb4aa-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bb4aa-203">Classes used in</span></span>        | [<span data-ttu-id="bb4aa-204">**Domínio-DNS**</span><span class="sxs-lookup"><span data-stu-id="bb4aa-204">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bb4aa-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb4aa-205">Windows Server 2008</span></span>



| <span data-ttu-id="bb4aa-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb4aa-206">Entry</span></span> | <span data-ttu-id="bb4aa-207">Valor</span><span class="sxs-lookup"><span data-stu-id="bb4aa-207">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="bb4aa-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="bb4aa-208">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="bb4aa-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb4aa-209">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="bb4aa-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb4aa-210">System-Only</span></span>            | <span data-ttu-id="bb4aa-211">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-211">False</span></span>                                        |
| <span data-ttu-id="bb4aa-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bb4aa-212">Is-Single-Valued</span></span>       | <span data-ttu-id="bb4aa-213">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-213">False</span></span>                                        |
| <span data-ttu-id="bb4aa-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="bb4aa-214">Is Indexed</span></span>             | <span data-ttu-id="bb4aa-215">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-215">False</span></span>                                        |
| <span data-ttu-id="bb4aa-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bb4aa-216">In Global Catalog</span></span>      | <span data-ttu-id="bb4aa-217">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-217">False</span></span>                                        |
| <span data-ttu-id="bb4aa-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bb4aa-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb4aa-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bb4aa-219">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="bb4aa-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb4aa-220">Range-Lower</span></span>            | <span data-ttu-id="bb4aa-221">0</span><span class="sxs-lookup"><span data-stu-id="bb4aa-221">0</span></span>                                            |
| <span data-ttu-id="bb4aa-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb4aa-222">Range-Upper</span></span>            | <span data-ttu-id="bb4aa-223">2.048</span><span class="sxs-lookup"><span data-stu-id="bb4aa-223">2048</span></span>                                         |
| <span data-ttu-id="bb4aa-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb4aa-224">Search-Flags</span></span>           | <span data-ttu-id="bb4aa-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb4aa-225">0x00000000</span></span>                                   |
| <span data-ttu-id="bb4aa-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb4aa-226">System-Flags</span></span>           | <span data-ttu-id="bb4aa-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb4aa-227">0x00000010</span></span>                                   |
| <span data-ttu-id="bb4aa-228">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bb4aa-228">Classes used in</span></span>        | [<span data-ttu-id="bb4aa-229">**Domínio-DNS**</span><span class="sxs-lookup"><span data-stu-id="bb4aa-229">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bb4aa-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bb4aa-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bb4aa-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb4aa-231">Entry</span></span> | <span data-ttu-id="bb4aa-232">Valor</span><span class="sxs-lookup"><span data-stu-id="bb4aa-232">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="bb4aa-233">ID do link</span><span class="sxs-lookup"><span data-stu-id="bb4aa-233">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="bb4aa-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb4aa-234">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="bb4aa-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb4aa-235">System-Only</span></span>            | <span data-ttu-id="bb4aa-236">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-236">False</span></span>                                        |
| <span data-ttu-id="bb4aa-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bb4aa-237">Is-Single-Valued</span></span>       | <span data-ttu-id="bb4aa-238">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-238">False</span></span>                                        |
| <span data-ttu-id="bb4aa-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="bb4aa-239">Is Indexed</span></span>             | <span data-ttu-id="bb4aa-240">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-240">False</span></span>                                        |
| <span data-ttu-id="bb4aa-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bb4aa-241">In Global Catalog</span></span>      | <span data-ttu-id="bb4aa-242">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-242">False</span></span>                                        |
| <span data-ttu-id="bb4aa-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bb4aa-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb4aa-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bb4aa-244">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="bb4aa-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb4aa-245">Range-Lower</span></span>            | <span data-ttu-id="bb4aa-246">0</span><span class="sxs-lookup"><span data-stu-id="bb4aa-246">0</span></span>                                            |
| <span data-ttu-id="bb4aa-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb4aa-247">Range-Upper</span></span>            | <span data-ttu-id="bb4aa-248">2.048</span><span class="sxs-lookup"><span data-stu-id="bb4aa-248">2048</span></span>                                         |
| <span data-ttu-id="bb4aa-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb4aa-249">Search-Flags</span></span>           | <span data-ttu-id="bb4aa-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb4aa-250">0x00000000</span></span>                                   |
| <span data-ttu-id="bb4aa-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb4aa-251">System-Flags</span></span>           | <span data-ttu-id="bb4aa-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb4aa-252">0x00000010</span></span>                                   |
| <span data-ttu-id="bb4aa-253">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bb4aa-253">Classes used in</span></span>        | [<span data-ttu-id="bb4aa-254">**Domínio-DNS**</span><span class="sxs-lookup"><span data-stu-id="bb4aa-254">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bb4aa-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bb4aa-255">Windows Server 2012</span></span>



| <span data-ttu-id="bb4aa-256">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb4aa-256">Entry</span></span> | <span data-ttu-id="bb4aa-257">Valor</span><span class="sxs-lookup"><span data-stu-id="bb4aa-257">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="bb4aa-258">ID do link</span><span class="sxs-lookup"><span data-stu-id="bb4aa-258">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="bb4aa-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb4aa-259">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="bb4aa-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb4aa-260">System-Only</span></span>            | <span data-ttu-id="bb4aa-261">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-261">False</span></span>                                        |
| <span data-ttu-id="bb4aa-262">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bb4aa-262">Is-Single-Valued</span></span>       | <span data-ttu-id="bb4aa-263">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-263">False</span></span>                                        |
| <span data-ttu-id="bb4aa-264">É indexado</span><span class="sxs-lookup"><span data-stu-id="bb4aa-264">Is Indexed</span></span>             | <span data-ttu-id="bb4aa-265">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-265">False</span></span>                                        |
| <span data-ttu-id="bb4aa-266">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bb4aa-266">In Global Catalog</span></span>      | <span data-ttu-id="bb4aa-267">Falso</span><span class="sxs-lookup"><span data-stu-id="bb4aa-267">False</span></span>                                        |
| <span data-ttu-id="bb4aa-268">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bb4aa-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb4aa-269">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bb4aa-269">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="bb4aa-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb4aa-270">Range-Lower</span></span>            | <span data-ttu-id="bb4aa-271">0</span><span class="sxs-lookup"><span data-stu-id="bb4aa-271">0</span></span>                                            |
| <span data-ttu-id="bb4aa-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb4aa-272">Range-Upper</span></span>            | <span data-ttu-id="bb4aa-273">2.048</span><span class="sxs-lookup"><span data-stu-id="bb4aa-273">2048</span></span>                                         |
| <span data-ttu-id="bb4aa-274">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb4aa-274">Search-Flags</span></span>           | <span data-ttu-id="bb4aa-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb4aa-275">0x00000000</span></span>                                   |
| <span data-ttu-id="bb4aa-276">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb4aa-276">System-Flags</span></span>           | <span data-ttu-id="bb4aa-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb4aa-277">0x00000010</span></span>                                   |
| <span data-ttu-id="bb4aa-278">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bb4aa-278">Classes used in</span></span>        | [<span data-ttu-id="bb4aa-279">**Domínio-DNS**</span><span class="sxs-lookup"><span data-stu-id="bb4aa-279">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



 

 





