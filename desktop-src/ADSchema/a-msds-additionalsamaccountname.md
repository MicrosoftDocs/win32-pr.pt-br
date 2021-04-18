---
title: ms-DS-Additional-Sam-atributo-Account-Name
description: Esse atributo é usado para armazenar os nomes de conta SAM que correspondem aos nomes de host DNS em MS-DS-Additional-DNS-Host-Name.
ms.assetid: eb69e1d4-42b7-42e1-aeae-77188db307ef
ms.tgt_platform: multiple
keywords:
- ms-DS-adicional-Sam-Account-Name atributo AD Schema
- atributo msDS-AdditionalSamAccountName do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Additional-Sam-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a437c30e6ddb0e551498480f7589791bce59feaf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105749108"
---
# <a name="ms-ds-additional-sam-account-name-attribute"></a><span data-ttu-id="b7ad8-105">ms-DS-Additional-Sam-atributo-Account-Name</span><span class="sxs-lookup"><span data-stu-id="b7ad8-105">ms-DS-Additional-Sam-Account-Name attribute</span></span>

<span data-ttu-id="b7ad8-106">Esse atributo é usado para armazenar os nomes de conta SAM que correspondem aos nomes de host DNS em MS-DS-Additional-DNS-Host-Name.</span><span class="sxs-lookup"><span data-stu-id="b7ad8-106">This attribute is used to store the SAM account names that correspond to the DNS host names in ms-DS-Additional-Dns-Host-Name.</span></span>



| <span data-ttu-id="b7ad8-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="b7ad8-107">Entry</span></span> | <span data-ttu-id="b7ad8-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b7ad8-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b7ad8-109">CN</span><span class="sxs-lookup"><span data-stu-id="b7ad8-109">CN</span></span>                | <span data-ttu-id="b7ad8-110">ms-DS-adicional-Sam-Account-Name</span><span class="sxs-lookup"><span data-stu-id="b7ad8-110">ms-DS-Additional-Sam-Account-Name</span></span>           |
| <span data-ttu-id="b7ad8-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b7ad8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b7ad8-112">msDS-AdditionalSamAccountName</span><span class="sxs-lookup"><span data-stu-id="b7ad8-112">msDS-AdditionalSamAccountName</span></span>               |
| <span data-ttu-id="b7ad8-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b7ad8-113">Size</span></span>              | <span data-ttu-id="b7ad8-114">Menos de 20 bytes.</span><span class="sxs-lookup"><span data-stu-id="b7ad8-114">Less than 20 bytes.</span></span>                         |
| <span data-ttu-id="b7ad8-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="b7ad8-115">Update Privilege</span></span>  | <span data-ttu-id="b7ad8-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="b7ad8-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="b7ad8-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="b7ad8-117">Update Frequency</span></span>  | <span data-ttu-id="b7ad8-118">Quando o DC é renomeado.</span><span class="sxs-lookup"><span data-stu-id="b7ad8-118">When the DC is renamed.</span></span>                     |
| <span data-ttu-id="b7ad8-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b7ad8-119">Attribute-Id</span></span>      | <span data-ttu-id="b7ad8-120">1.2.840.113556.1.4.1718</span><span class="sxs-lookup"><span data-stu-id="b7ad8-120">1.2.840.113556.1.4.1718</span></span>                     |
| <span data-ttu-id="b7ad8-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b7ad8-121">System-Id-Guid</span></span>    | <span data-ttu-id="b7ad8-122">975571df-a4d5-429a-9f59-cdc6581d91e6</span><span class="sxs-lookup"><span data-stu-id="b7ad8-122">975571df-a4d5-429a-9f59-cdc6581d91e6</span></span>        |
| <span data-ttu-id="b7ad8-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7ad8-123">Syntax</span></span>            | [<span data-ttu-id="b7ad8-124">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b7ad8-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b7ad8-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="b7ad8-125">Implementations</span></span>

-   [<span data-ttu-id="b7ad8-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b7ad8-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b7ad8-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b7ad8-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b7ad8-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b7ad8-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b7ad8-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b7ad8-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b7ad8-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b7ad8-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b7ad8-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b7ad8-131">Windows Server 2003</span></span>



| <span data-ttu-id="b7ad8-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="b7ad8-132">Entry</span></span> | <span data-ttu-id="b7ad8-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b7ad8-133">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="b7ad8-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="b7ad8-134">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="b7ad8-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7ad8-135">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="b7ad8-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7ad8-136">System-Only</span></span>            | <span data-ttu-id="b7ad8-137">True</span><span class="sxs-lookup"><span data-stu-id="b7ad8-137">True</span></span>                                      |
| <span data-ttu-id="b7ad8-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b7ad8-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b7ad8-139">Falso</span><span class="sxs-lookup"><span data-stu-id="b7ad8-139">False</span></span>                                     |
| <span data-ttu-id="b7ad8-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="b7ad8-140">Is Indexed</span></span>             | <span data-ttu-id="b7ad8-141">True</span><span class="sxs-lookup"><span data-stu-id="b7ad8-141">True</span></span>                                      |
| <span data-ttu-id="b7ad8-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b7ad8-142">In Global Catalog</span></span>      | <span data-ttu-id="b7ad8-143">Falso</span><span class="sxs-lookup"><span data-stu-id="b7ad8-143">False</span></span>                                     |
| <span data-ttu-id="b7ad8-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7ad8-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7ad8-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b7ad8-145">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="b7ad8-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7ad8-146">Range-Lower</span></span>            | <span data-ttu-id="b7ad8-147">0</span><span class="sxs-lookup"><span data-stu-id="b7ad8-147">0</span></span>                                         |
| <span data-ttu-id="b7ad8-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7ad8-148">Range-Upper</span></span>            | <span data-ttu-id="b7ad8-149">256</span><span class="sxs-lookup"><span data-stu-id="b7ad8-149">256</span></span>                                       |
| <span data-ttu-id="b7ad8-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7ad8-150">Search-Flags</span></span>           | <span data-ttu-id="b7ad8-151">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="b7ad8-151">0x0000000D</span></span>                                |
| <span data-ttu-id="b7ad8-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7ad8-152">System-Flags</span></span>           | <span data-ttu-id="b7ad8-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7ad8-153">0x00000010</span></span>                                |
| <span data-ttu-id="b7ad8-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b7ad8-154">Classes used in</span></span>        | [<span data-ttu-id="b7ad8-155">**Computador**</span><span class="sxs-lookup"><span data-stu-id="b7ad8-155">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b7ad8-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b7ad8-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b7ad8-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="b7ad8-157">Entry</span></span> | <span data-ttu-id="b7ad8-158">Valor</span><span class="sxs-lookup"><span data-stu-id="b7ad8-158">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="b7ad8-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="b7ad8-159">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="b7ad8-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7ad8-160">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="b7ad8-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7ad8-161">System-Only</span></span>            | <span data-ttu-id="b7ad8-162">True</span><span class="sxs-lookup"><span data-stu-id="b7ad8-162">True</span></span>                                      |
| <span data-ttu-id="b7ad8-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b7ad8-163">Is-Single-Valued</span></span>       | <span data-ttu-id="b7ad8-164">Falso</span><span class="sxs-lookup"><span data-stu-id="b7ad8-164">False</span></span>                                     |
| <span data-ttu-id="b7ad8-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="b7ad8-165">Is Indexed</span></span>             | <span data-ttu-id="b7ad8-166">True</span><span class="sxs-lookup"><span data-stu-id="b7ad8-166">True</span></span>                                      |
| <span data-ttu-id="b7ad8-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b7ad8-167">In Global Catalog</span></span>      | <span data-ttu-id="b7ad8-168">Falso</span><span class="sxs-lookup"><span data-stu-id="b7ad8-168">False</span></span>                                     |
| <span data-ttu-id="b7ad8-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7ad8-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7ad8-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b7ad8-170">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="b7ad8-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7ad8-171">Range-Lower</span></span>            | <span data-ttu-id="b7ad8-172">0</span><span class="sxs-lookup"><span data-stu-id="b7ad8-172">0</span></span>                                         |
| <span data-ttu-id="b7ad8-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7ad8-173">Range-Upper</span></span>            | <span data-ttu-id="b7ad8-174">256</span><span class="sxs-lookup"><span data-stu-id="b7ad8-174">256</span></span>                                       |
| <span data-ttu-id="b7ad8-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7ad8-175">Search-Flags</span></span>           | <span data-ttu-id="b7ad8-176">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="b7ad8-176">0x0000000D</span></span>                                |
| <span data-ttu-id="b7ad8-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7ad8-177">System-Flags</span></span>           | <span data-ttu-id="b7ad8-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7ad8-178">0x00000010</span></span>                                |
| <span data-ttu-id="b7ad8-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b7ad8-179">Classes used in</span></span>        | [<span data-ttu-id="b7ad8-180">**Computador**</span><span class="sxs-lookup"><span data-stu-id="b7ad8-180">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b7ad8-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7ad8-181">Windows Server 2008</span></span>



| <span data-ttu-id="b7ad8-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="b7ad8-182">Entry</span></span> | <span data-ttu-id="b7ad8-183">Valor</span><span class="sxs-lookup"><span data-stu-id="b7ad8-183">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="b7ad8-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="b7ad8-184">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="b7ad8-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7ad8-185">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="b7ad8-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7ad8-186">System-Only</span></span>            | <span data-ttu-id="b7ad8-187">True</span><span class="sxs-lookup"><span data-stu-id="b7ad8-187">True</span></span>                                      |
| <span data-ttu-id="b7ad8-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b7ad8-188">Is-Single-Valued</span></span>       | <span data-ttu-id="b7ad8-189">Falso</span><span class="sxs-lookup"><span data-stu-id="b7ad8-189">False</span></span>                                     |
| <span data-ttu-id="b7ad8-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="b7ad8-190">Is Indexed</span></span>             | <span data-ttu-id="b7ad8-191">True</span><span class="sxs-lookup"><span data-stu-id="b7ad8-191">True</span></span>                                      |
| <span data-ttu-id="b7ad8-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b7ad8-192">In Global Catalog</span></span>      | <span data-ttu-id="b7ad8-193">Falso</span><span class="sxs-lookup"><span data-stu-id="b7ad8-193">False</span></span>                                     |
| <span data-ttu-id="b7ad8-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7ad8-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7ad8-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b7ad8-195">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="b7ad8-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7ad8-196">Range-Lower</span></span>            | <span data-ttu-id="b7ad8-197">0</span><span class="sxs-lookup"><span data-stu-id="b7ad8-197">0</span></span>                                         |
| <span data-ttu-id="b7ad8-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7ad8-198">Range-Upper</span></span>            | <span data-ttu-id="b7ad8-199">256</span><span class="sxs-lookup"><span data-stu-id="b7ad8-199">256</span></span>                                       |
| <span data-ttu-id="b7ad8-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7ad8-200">Search-Flags</span></span>           | <span data-ttu-id="b7ad8-201">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="b7ad8-201">0x0000000D</span></span>                                |
| <span data-ttu-id="b7ad8-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7ad8-202">System-Flags</span></span>           | <span data-ttu-id="b7ad8-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7ad8-203">0x00000010</span></span>                                |
| <span data-ttu-id="b7ad8-204">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b7ad8-204">Classes used in</span></span>        | [<span data-ttu-id="b7ad8-205">**Computador**</span><span class="sxs-lookup"><span data-stu-id="b7ad8-205">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b7ad8-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b7ad8-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b7ad8-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="b7ad8-207">Entry</span></span> | <span data-ttu-id="b7ad8-208">Valor</span><span class="sxs-lookup"><span data-stu-id="b7ad8-208">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="b7ad8-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="b7ad8-209">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="b7ad8-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7ad8-210">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="b7ad8-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7ad8-211">System-Only</span></span>            | <span data-ttu-id="b7ad8-212">True</span><span class="sxs-lookup"><span data-stu-id="b7ad8-212">True</span></span>                                      |
| <span data-ttu-id="b7ad8-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b7ad8-213">Is-Single-Valued</span></span>       | <span data-ttu-id="b7ad8-214">Falso</span><span class="sxs-lookup"><span data-stu-id="b7ad8-214">False</span></span>                                     |
| <span data-ttu-id="b7ad8-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="b7ad8-215">Is Indexed</span></span>             | <span data-ttu-id="b7ad8-216">True</span><span class="sxs-lookup"><span data-stu-id="b7ad8-216">True</span></span>                                      |
| <span data-ttu-id="b7ad8-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b7ad8-217">In Global Catalog</span></span>      | <span data-ttu-id="b7ad8-218">Falso</span><span class="sxs-lookup"><span data-stu-id="b7ad8-218">False</span></span>                                     |
| <span data-ttu-id="b7ad8-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7ad8-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7ad8-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b7ad8-220">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="b7ad8-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7ad8-221">Range-Lower</span></span>            | <span data-ttu-id="b7ad8-222">0</span><span class="sxs-lookup"><span data-stu-id="b7ad8-222">0</span></span>                                         |
| <span data-ttu-id="b7ad8-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7ad8-223">Range-Upper</span></span>            | <span data-ttu-id="b7ad8-224">256</span><span class="sxs-lookup"><span data-stu-id="b7ad8-224">256</span></span>                                       |
| <span data-ttu-id="b7ad8-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7ad8-225">Search-Flags</span></span>           | <span data-ttu-id="b7ad8-226">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="b7ad8-226">0x0000000D</span></span>                                |
| <span data-ttu-id="b7ad8-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7ad8-227">System-Flags</span></span>           | <span data-ttu-id="b7ad8-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7ad8-228">0x00000010</span></span>                                |
| <span data-ttu-id="b7ad8-229">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b7ad8-229">Classes used in</span></span>        | [<span data-ttu-id="b7ad8-230">**Computador**</span><span class="sxs-lookup"><span data-stu-id="b7ad8-230">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b7ad8-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b7ad8-231">Windows Server 2012</span></span>



| <span data-ttu-id="b7ad8-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="b7ad8-232">Entry</span></span> | <span data-ttu-id="b7ad8-233">Valor</span><span class="sxs-lookup"><span data-stu-id="b7ad8-233">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="b7ad8-234">ID do link</span><span class="sxs-lookup"><span data-stu-id="b7ad8-234">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="b7ad8-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7ad8-235">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="b7ad8-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7ad8-236">System-Only</span></span>            | <span data-ttu-id="b7ad8-237">True</span><span class="sxs-lookup"><span data-stu-id="b7ad8-237">True</span></span>                                      |
| <span data-ttu-id="b7ad8-238">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b7ad8-238">Is-Single-Valued</span></span>       | <span data-ttu-id="b7ad8-239">Falso</span><span class="sxs-lookup"><span data-stu-id="b7ad8-239">False</span></span>                                     |
| <span data-ttu-id="b7ad8-240">É indexado</span><span class="sxs-lookup"><span data-stu-id="b7ad8-240">Is Indexed</span></span>             | <span data-ttu-id="b7ad8-241">True</span><span class="sxs-lookup"><span data-stu-id="b7ad8-241">True</span></span>                                      |
| <span data-ttu-id="b7ad8-242">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b7ad8-242">In Global Catalog</span></span>      | <span data-ttu-id="b7ad8-243">Falso</span><span class="sxs-lookup"><span data-stu-id="b7ad8-243">False</span></span>                                     |
| <span data-ttu-id="b7ad8-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7ad8-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7ad8-245">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b7ad8-245">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="b7ad8-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7ad8-246">Range-Lower</span></span>            | <span data-ttu-id="b7ad8-247">0</span><span class="sxs-lookup"><span data-stu-id="b7ad8-247">0</span></span>                                         |
| <span data-ttu-id="b7ad8-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7ad8-248">Range-Upper</span></span>            | <span data-ttu-id="b7ad8-249">256</span><span class="sxs-lookup"><span data-stu-id="b7ad8-249">256</span></span>                                       |
| <span data-ttu-id="b7ad8-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7ad8-250">Search-Flags</span></span>           | <span data-ttu-id="b7ad8-251">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="b7ad8-251">0x0000000D</span></span>                                |
| <span data-ttu-id="b7ad8-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7ad8-252">System-Flags</span></span>           | <span data-ttu-id="b7ad8-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7ad8-253">0x00000010</span></span>                                |
| <span data-ttu-id="b7ad8-254">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b7ad8-254">Classes used in</span></span>        | [<span data-ttu-id="b7ad8-255">**Computador**</span><span class="sxs-lookup"><span data-stu-id="b7ad8-255">**Computer**</span></span>](c-computer.md)<br/> |



 

 





