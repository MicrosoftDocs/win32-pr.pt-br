---
title: atributo ms-DS-Additional-DNS-Host-Name
description: O atributo é usado para armazenar o nome de host DNS adicional de um objeto de computador. Esse atributo é usado no momento em que um DC é renomeado.
ms.assetid: ea06f756-d9b6-409d-a008-0e3a1874ad94
ms.tgt_platform: multiple
keywords:
- ms-DS-Additional-DNS-Host-Name atributo AD Schema
- atributo msDS-AdditionalDnsHostName do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Additional-Dns-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dea3212a19bf743e608f356170adf7a03c06d0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919504"
---
# <a name="ms-ds-additional-dns-host-name-attribute"></a><span data-ttu-id="c940f-106">atributo ms-DS-Additional-DNS-Host-Name</span><span class="sxs-lookup"><span data-stu-id="c940f-106">ms-DS-Additional-Dns-Host-Name attribute</span></span>

<span data-ttu-id="c940f-107">O atributo é usado para armazenar o nome de host DNS adicional de um objeto de computador.</span><span class="sxs-lookup"><span data-stu-id="c940f-107">The attribute is used to store the additional DNS host name of a computer object.</span></span> <span data-ttu-id="c940f-108">Esse atributo é usado no momento em que um computador é renomeado ou os nomes são gerenciados com "netdom computername".</span><span class="sxs-lookup"><span data-stu-id="c940f-108">This attribute is used at the time a computer is renamed, or names are managed with "netdom computername".</span></span>



| <span data-ttu-id="c940f-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="c940f-109">Entry</span></span> | <span data-ttu-id="c940f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="c940f-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="c940f-111">CN</span><span class="sxs-lookup"><span data-stu-id="c940f-111">CN</span></span>                | <span data-ttu-id="c940f-112">ms-DS-adicional-DNS-Host-Name</span><span class="sxs-lookup"><span data-stu-id="c940f-112">ms-DS-Additional-Dns-Host-Name</span></span>                                              |
| <span data-ttu-id="c940f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c940f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c940f-114">msDS-AdditionalDnsHostName</span><span class="sxs-lookup"><span data-stu-id="c940f-114">msDS-AdditionalDnsHostName</span></span>                                                  |
| <span data-ttu-id="c940f-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c940f-115">Size</span></span>              | <span data-ttu-id="c940f-116">Cada valor pode ser de 2048 caracteres.</span><span class="sxs-lookup"><span data-stu-id="c940f-116">Each value can be 2048 characters.</span></span> <span data-ttu-id="c940f-117">O número de valor é o limite de banco de dados de aproximadamente 1200 valores.</span><span class="sxs-lookup"><span data-stu-id="c940f-117">The number of value is the database limit of about 1200 values.</span></span> |
| <span data-ttu-id="c940f-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="c940f-118">Update Privilege</span></span>  | <span data-ttu-id="c940f-119">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="c940f-119">This value is set by the system.</span></span>                                            |
| <span data-ttu-id="c940f-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="c940f-120">Update Frequency</span></span>  | <span data-ttu-id="c940f-121">Quando um computador é renomeado.</span><span class="sxs-lookup"><span data-stu-id="c940f-121">When a computer is renamed.</span></span>                                                 |
| <span data-ttu-id="c940f-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c940f-122">Attribute-Id</span></span>      | <span data-ttu-id="c940f-123">1.2.840.113556.1.4.1717</span><span class="sxs-lookup"><span data-stu-id="c940f-123">1.2.840.113556.1.4.1717</span></span>                                                     |
| <span data-ttu-id="c940f-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c940f-124">System-Id-Guid</span></span>    | <span data-ttu-id="c940f-125">80863791-dbe9-4eb8-837E-7f0ab55d9ac7</span><span class="sxs-lookup"><span data-stu-id="c940f-125">80863791-dbe9-4eb8-837e-7f0ab55d9ac7</span></span>                                        |
| <span data-ttu-id="c940f-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="c940f-126">Syntax</span></span>            | [<span data-ttu-id="c940f-127">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c940f-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                 |



## <a name="implementations"></a><span data-ttu-id="c940f-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="c940f-128">Implementations</span></span>

-   [<span data-ttu-id="c940f-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c940f-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c940f-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c940f-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c940f-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c940f-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c940f-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c940f-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c940f-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c940f-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c940f-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c940f-134">Windows Server 2003</span></span>



| <span data-ttu-id="c940f-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="c940f-135">Entry</span></span> | <span data-ttu-id="c940f-136">Valor</span><span class="sxs-lookup"><span data-stu-id="c940f-136">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="c940f-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="c940f-137">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="c940f-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c940f-138">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="c940f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="c940f-139">System-Only</span></span>            | <span data-ttu-id="c940f-140">True</span><span class="sxs-lookup"><span data-stu-id="c940f-140">True</span></span>                                      |
| <span data-ttu-id="c940f-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c940f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="c940f-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c940f-142">False</span></span>                                     |
| <span data-ttu-id="c940f-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="c940f-143">Is Indexed</span></span>             | <span data-ttu-id="c940f-144">Falso</span><span class="sxs-lookup"><span data-stu-id="c940f-144">False</span></span>                                     |
| <span data-ttu-id="c940f-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c940f-145">In Global Catalog</span></span>      | <span data-ttu-id="c940f-146">Falso</span><span class="sxs-lookup"><span data-stu-id="c940f-146">False</span></span>                                     |
| <span data-ttu-id="c940f-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c940f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="c940f-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c940f-148">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="c940f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c940f-149">Range-Lower</span></span>            | <span data-ttu-id="c940f-150">0</span><span class="sxs-lookup"><span data-stu-id="c940f-150">0</span></span>                                         |
| <span data-ttu-id="c940f-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c940f-151">Range-Upper</span></span>            | <span data-ttu-id="c940f-152">2.048</span><span class="sxs-lookup"><span data-stu-id="c940f-152">2048</span></span>                                      |
| <span data-ttu-id="c940f-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c940f-153">Search-Flags</span></span>           | <span data-ttu-id="c940f-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c940f-154">0x00000000</span></span>                                |
| <span data-ttu-id="c940f-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c940f-155">System-Flags</span></span>           | <span data-ttu-id="c940f-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c940f-156">0x00000010</span></span>                                |
| <span data-ttu-id="c940f-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c940f-157">Classes used in</span></span>        | [<span data-ttu-id="c940f-158">**Computador**</span><span class="sxs-lookup"><span data-stu-id="c940f-158">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c940f-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c940f-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c940f-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="c940f-160">Entry</span></span> | <span data-ttu-id="c940f-161">Valor</span><span class="sxs-lookup"><span data-stu-id="c940f-161">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="c940f-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="c940f-162">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="c940f-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c940f-163">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="c940f-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="c940f-164">System-Only</span></span>            | <span data-ttu-id="c940f-165">True</span><span class="sxs-lookup"><span data-stu-id="c940f-165">True</span></span>                                      |
| <span data-ttu-id="c940f-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c940f-166">Is-Single-Valued</span></span>       | <span data-ttu-id="c940f-167">Falso</span><span class="sxs-lookup"><span data-stu-id="c940f-167">False</span></span>                                     |
| <span data-ttu-id="c940f-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="c940f-168">Is Indexed</span></span>             | <span data-ttu-id="c940f-169">Falso</span><span class="sxs-lookup"><span data-stu-id="c940f-169">False</span></span>                                     |
| <span data-ttu-id="c940f-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c940f-170">In Global Catalog</span></span>      | <span data-ttu-id="c940f-171">Falso</span><span class="sxs-lookup"><span data-stu-id="c940f-171">False</span></span>                                     |
| <span data-ttu-id="c940f-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c940f-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="c940f-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c940f-173">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="c940f-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c940f-174">Range-Lower</span></span>            | <span data-ttu-id="c940f-175">0</span><span class="sxs-lookup"><span data-stu-id="c940f-175">0</span></span>                                         |
| <span data-ttu-id="c940f-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c940f-176">Range-Upper</span></span>            | <span data-ttu-id="c940f-177">2.048</span><span class="sxs-lookup"><span data-stu-id="c940f-177">2048</span></span>                                      |
| <span data-ttu-id="c940f-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c940f-178">Search-Flags</span></span>           | <span data-ttu-id="c940f-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c940f-179">0x00000000</span></span>                                |
| <span data-ttu-id="c940f-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c940f-180">System-Flags</span></span>           | <span data-ttu-id="c940f-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c940f-181">0x00000010</span></span>                                |
| <span data-ttu-id="c940f-182">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c940f-182">Classes used in</span></span>        | [<span data-ttu-id="c940f-183">**Computador**</span><span class="sxs-lookup"><span data-stu-id="c940f-183">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c940f-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c940f-184">Windows Server 2008</span></span>



| <span data-ttu-id="c940f-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="c940f-185">Entry</span></span> | <span data-ttu-id="c940f-186">Valor</span><span class="sxs-lookup"><span data-stu-id="c940f-186">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="c940f-187">ID do link</span><span class="sxs-lookup"><span data-stu-id="c940f-187">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="c940f-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c940f-188">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="c940f-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="c940f-189">System-Only</span></span>            | <span data-ttu-id="c940f-190">True</span><span class="sxs-lookup"><span data-stu-id="c940f-190">True</span></span>                                      |
| <span data-ttu-id="c940f-191">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c940f-191">Is-Single-Valued</span></span>       | <span data-ttu-id="c940f-192">Falso</span><span class="sxs-lookup"><span data-stu-id="c940f-192">False</span></span>                                     |
| <span data-ttu-id="c940f-193">É indexado</span><span class="sxs-lookup"><span data-stu-id="c940f-193">Is Indexed</span></span>             | <span data-ttu-id="c940f-194">Falso</span><span class="sxs-lookup"><span data-stu-id="c940f-194">False</span></span>                                     |
| <span data-ttu-id="c940f-195">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c940f-195">In Global Catalog</span></span>      | <span data-ttu-id="c940f-196">Falso</span><span class="sxs-lookup"><span data-stu-id="c940f-196">False</span></span>                                     |
| <span data-ttu-id="c940f-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c940f-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="c940f-198">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c940f-198">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="c940f-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c940f-199">Range-Lower</span></span>            | <span data-ttu-id="c940f-200">0</span><span class="sxs-lookup"><span data-stu-id="c940f-200">0</span></span>                                         |
| <span data-ttu-id="c940f-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c940f-201">Range-Upper</span></span>            | <span data-ttu-id="c940f-202">2.048</span><span class="sxs-lookup"><span data-stu-id="c940f-202">2048</span></span>                                      |
| <span data-ttu-id="c940f-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c940f-203">Search-Flags</span></span>           | <span data-ttu-id="c940f-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c940f-204">0x00000000</span></span>                                |
| <span data-ttu-id="c940f-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c940f-205">System-Flags</span></span>           | <span data-ttu-id="c940f-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c940f-206">0x00000010</span></span>                                |
| <span data-ttu-id="c940f-207">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c940f-207">Classes used in</span></span>        | [<span data-ttu-id="c940f-208">**Computador**</span><span class="sxs-lookup"><span data-stu-id="c940f-208">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c940f-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c940f-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c940f-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="c940f-210">Entry</span></span> | <span data-ttu-id="c940f-211">Valor</span><span class="sxs-lookup"><span data-stu-id="c940f-211">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="c940f-212">ID do link</span><span class="sxs-lookup"><span data-stu-id="c940f-212">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="c940f-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c940f-213">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="c940f-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="c940f-214">System-Only</span></span>            | <span data-ttu-id="c940f-215">True</span><span class="sxs-lookup"><span data-stu-id="c940f-215">True</span></span>                                      |
| <span data-ttu-id="c940f-216">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c940f-216">Is-Single-Valued</span></span>       | <span data-ttu-id="c940f-217">Falso</span><span class="sxs-lookup"><span data-stu-id="c940f-217">False</span></span>                                     |
| <span data-ttu-id="c940f-218">É indexado</span><span class="sxs-lookup"><span data-stu-id="c940f-218">Is Indexed</span></span>             | <span data-ttu-id="c940f-219">Falso</span><span class="sxs-lookup"><span data-stu-id="c940f-219">False</span></span>                                     |
| <span data-ttu-id="c940f-220">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c940f-220">In Global Catalog</span></span>      | <span data-ttu-id="c940f-221">Falso</span><span class="sxs-lookup"><span data-stu-id="c940f-221">False</span></span>                                     |
| <span data-ttu-id="c940f-222">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c940f-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="c940f-223">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c940f-223">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="c940f-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c940f-224">Range-Lower</span></span>            | <span data-ttu-id="c940f-225">0</span><span class="sxs-lookup"><span data-stu-id="c940f-225">0</span></span>                                         |
| <span data-ttu-id="c940f-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c940f-226">Range-Upper</span></span>            | <span data-ttu-id="c940f-227">2.048</span><span class="sxs-lookup"><span data-stu-id="c940f-227">2048</span></span>                                      |
| <span data-ttu-id="c940f-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c940f-228">Search-Flags</span></span>           | <span data-ttu-id="c940f-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c940f-229">0x00000000</span></span>                                |
| <span data-ttu-id="c940f-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c940f-230">System-Flags</span></span>           | <span data-ttu-id="c940f-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c940f-231">0x00000010</span></span>                                |
| <span data-ttu-id="c940f-232">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c940f-232">Classes used in</span></span>        | [<span data-ttu-id="c940f-233">**Computador**</span><span class="sxs-lookup"><span data-stu-id="c940f-233">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c940f-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c940f-234">Windows Server 2012</span></span>



| <span data-ttu-id="c940f-235">Entrada</span><span class="sxs-lookup"><span data-stu-id="c940f-235">Entry</span></span> | <span data-ttu-id="c940f-236">Valor</span><span class="sxs-lookup"><span data-stu-id="c940f-236">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="c940f-237">ID do link</span><span class="sxs-lookup"><span data-stu-id="c940f-237">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="c940f-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c940f-238">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="c940f-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="c940f-239">System-Only</span></span>            | <span data-ttu-id="c940f-240">True</span><span class="sxs-lookup"><span data-stu-id="c940f-240">True</span></span>                                      |
| <span data-ttu-id="c940f-241">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c940f-241">Is-Single-Valued</span></span>       | <span data-ttu-id="c940f-242">Falso</span><span class="sxs-lookup"><span data-stu-id="c940f-242">False</span></span>                                     |
| <span data-ttu-id="c940f-243">É indexado</span><span class="sxs-lookup"><span data-stu-id="c940f-243">Is Indexed</span></span>             | <span data-ttu-id="c940f-244">Falso</span><span class="sxs-lookup"><span data-stu-id="c940f-244">False</span></span>                                     |
| <span data-ttu-id="c940f-245">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c940f-245">In Global Catalog</span></span>      | <span data-ttu-id="c940f-246">Falso</span><span class="sxs-lookup"><span data-stu-id="c940f-246">False</span></span>                                     |
| <span data-ttu-id="c940f-247">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c940f-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="c940f-248">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c940f-248">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="c940f-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c940f-249">Range-Lower</span></span>            | <span data-ttu-id="c940f-250">0</span><span class="sxs-lookup"><span data-stu-id="c940f-250">0</span></span>                                         |
| <span data-ttu-id="c940f-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c940f-251">Range-Upper</span></span>            | <span data-ttu-id="c940f-252">2.048</span><span class="sxs-lookup"><span data-stu-id="c940f-252">2048</span></span>                                      |
| <span data-ttu-id="c940f-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c940f-253">Search-Flags</span></span>           | <span data-ttu-id="c940f-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c940f-254">0x00000000</span></span>                                |
| <span data-ttu-id="c940f-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c940f-255">System-Flags</span></span>           | <span data-ttu-id="c940f-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c940f-256">0x00000010</span></span>                                |
| <span data-ttu-id="c940f-257">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c940f-257">Classes used in</span></span>        | [<span data-ttu-id="c940f-258">**Computador**</span><span class="sxs-lookup"><span data-stu-id="c940f-258">**Computer**</span></span>](c-computer.md)<br/> |



 

 





