---
title: atributo ms-DS-Top-quota-Usage
description: A lista de principais usuários de cota atualmente no banco de dados de diretório, ordenada por diminuir o uso de cota.
ms.assetid: c52db8c8-233c-495f-b3fe-edbe1d723677
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DS-Top-quota-Usage
- atributo msDS-TopQuotaUsage do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Top-Quota-Usage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db787c0360eff64c726ec680c9fd2a18da1e8d1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755445"
---
# <a name="ms-ds-top-quota-usage-attribute"></a><span data-ttu-id="451b2-105">atributo ms-DS-Top-quota-Usage</span><span class="sxs-lookup"><span data-stu-id="451b2-105">ms-DS-Top-Quota-Usage attribute</span></span>

<span data-ttu-id="451b2-106">A lista de principais usuários de cota atualmente no banco de dados de diretório, ordenada por diminuir o uso de cota.</span><span class="sxs-lookup"><span data-stu-id="451b2-106">The list of top quota users currently in the directory database, ordered by decreasing quota usage.</span></span>



| <span data-ttu-id="451b2-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="451b2-107">Entry</span></span> | <span data-ttu-id="451b2-108">Valor</span><span class="sxs-lookup"><span data-stu-id="451b2-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="451b2-109">CN</span><span class="sxs-lookup"><span data-stu-id="451b2-109">CN</span></span>                | <span data-ttu-id="451b2-110">ms-DS-Top-quota-Usage</span><span class="sxs-lookup"><span data-stu-id="451b2-110">ms-DS-Top-Quota-Usage</span></span>                       |
| <span data-ttu-id="451b2-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="451b2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="451b2-112">msDS-TopQuotaUsage</span><span class="sxs-lookup"><span data-stu-id="451b2-112">msDS-TopQuotaUsage</span></span>                          |
| <span data-ttu-id="451b2-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="451b2-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="451b2-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="451b2-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="451b2-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="451b2-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="451b2-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="451b2-116">Attribute-Id</span></span>      | <span data-ttu-id="451b2-117">1.2.840.113556.1.4.1850</span><span class="sxs-lookup"><span data-stu-id="451b2-117">1.2.840.113556.1.4.1850</span></span>                     |
| <span data-ttu-id="451b2-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="451b2-118">System-Id-Guid</span></span>    | <span data-ttu-id="451b2-119">7b7cce4f-f1f5-4bb6-b7eb-23504af19e75</span><span class="sxs-lookup"><span data-stu-id="451b2-119">7b7cce4f-f1f5-4bb6-b7eb-23504af19e75</span></span>        |
| <span data-ttu-id="451b2-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="451b2-120">Syntax</span></span>            | [<span data-ttu-id="451b2-121">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="451b2-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="451b2-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="451b2-122">Implementations</span></span>

-   [<span data-ttu-id="451b2-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="451b2-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="451b2-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="451b2-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="451b2-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="451b2-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="451b2-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="451b2-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="451b2-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="451b2-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="451b2-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="451b2-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="451b2-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="451b2-129">Windows Server 2003</span></span>



| <span data-ttu-id="451b2-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="451b2-130">Entry</span></span> | <span data-ttu-id="451b2-131">Valor</span><span class="sxs-lookup"><span data-stu-id="451b2-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="451b2-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="451b2-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="451b2-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="451b2-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="451b2-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="451b2-134">System-Only</span></span>            | <span data-ttu-id="451b2-135">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-135">False</span></span>                                                             |
| <span data-ttu-id="451b2-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="451b2-136">Is-Single-Valued</span></span>       | <span data-ttu-id="451b2-137">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-137">False</span></span>                                                             |
| <span data-ttu-id="451b2-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="451b2-138">Is Indexed</span></span>             | <span data-ttu-id="451b2-139">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-139">False</span></span>                                                             |
| <span data-ttu-id="451b2-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="451b2-140">In Global Catalog</span></span>      | <span data-ttu-id="451b2-141">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-141">False</span></span>                                                             |
| <span data-ttu-id="451b2-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="451b2-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="451b2-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="451b2-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="451b2-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="451b2-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="451b2-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="451b2-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="451b2-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="451b2-146">Search-Flags</span></span>           | <span data-ttu-id="451b2-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="451b2-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="451b2-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="451b2-148">System-Flags</span></span>           | <span data-ttu-id="451b2-149">0x00000014</span><span class="sxs-lookup"><span data-stu-id="451b2-149">0x00000014</span></span>                                                        |
| <span data-ttu-id="451b2-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="451b2-150">Classes used in</span></span>        | [<span data-ttu-id="451b2-151">**ms-DS-quota-container**</span><span class="sxs-lookup"><span data-stu-id="451b2-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="451b2-152">ADAM</span><span class="sxs-lookup"><span data-stu-id="451b2-152">ADAM</span></span>



| <span data-ttu-id="451b2-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="451b2-153">Entry</span></span> | <span data-ttu-id="451b2-154">Valor</span><span class="sxs-lookup"><span data-stu-id="451b2-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="451b2-155">ID do link</span><span class="sxs-lookup"><span data-stu-id="451b2-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="451b2-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="451b2-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="451b2-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="451b2-157">System-Only</span></span>            | <span data-ttu-id="451b2-158">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-158">False</span></span>                                                             |
| <span data-ttu-id="451b2-159">É de valor único</span><span class="sxs-lookup"><span data-stu-id="451b2-159">Is-Single-Valued</span></span>       | <span data-ttu-id="451b2-160">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-160">False</span></span>                                                             |
| <span data-ttu-id="451b2-161">É indexado</span><span class="sxs-lookup"><span data-stu-id="451b2-161">Is Indexed</span></span>             | <span data-ttu-id="451b2-162">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-162">False</span></span>                                                             |
| <span data-ttu-id="451b2-163">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="451b2-163">In Global Catalog</span></span>      | <span data-ttu-id="451b2-164">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-164">False</span></span>                                                             |
| <span data-ttu-id="451b2-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="451b2-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="451b2-166">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="451b2-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="451b2-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="451b2-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="451b2-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="451b2-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="451b2-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="451b2-169">Search-Flags</span></span>           | <span data-ttu-id="451b2-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="451b2-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="451b2-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="451b2-171">System-Flags</span></span>           | <span data-ttu-id="451b2-172">0x00000014</span><span class="sxs-lookup"><span data-stu-id="451b2-172">0x00000014</span></span>                                                        |
| <span data-ttu-id="451b2-173">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="451b2-173">Classes used in</span></span>        | [<span data-ttu-id="451b2-174">**ms-DS-quota-container**</span><span class="sxs-lookup"><span data-stu-id="451b2-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="451b2-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="451b2-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="451b2-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="451b2-176">Entry</span></span> | <span data-ttu-id="451b2-177">Valor</span><span class="sxs-lookup"><span data-stu-id="451b2-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="451b2-178">ID do link</span><span class="sxs-lookup"><span data-stu-id="451b2-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="451b2-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="451b2-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="451b2-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="451b2-180">System-Only</span></span>            | <span data-ttu-id="451b2-181">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-181">False</span></span>                                                             |
| <span data-ttu-id="451b2-182">É de valor único</span><span class="sxs-lookup"><span data-stu-id="451b2-182">Is-Single-Valued</span></span>       | <span data-ttu-id="451b2-183">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-183">False</span></span>                                                             |
| <span data-ttu-id="451b2-184">É indexado</span><span class="sxs-lookup"><span data-stu-id="451b2-184">Is Indexed</span></span>             | <span data-ttu-id="451b2-185">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-185">False</span></span>                                                             |
| <span data-ttu-id="451b2-186">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="451b2-186">In Global Catalog</span></span>      | <span data-ttu-id="451b2-187">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-187">False</span></span>                                                             |
| <span data-ttu-id="451b2-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="451b2-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="451b2-189">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="451b2-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="451b2-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="451b2-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="451b2-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="451b2-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="451b2-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="451b2-192">Search-Flags</span></span>           | <span data-ttu-id="451b2-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="451b2-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="451b2-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="451b2-194">System-Flags</span></span>           | <span data-ttu-id="451b2-195">0x00000014</span><span class="sxs-lookup"><span data-stu-id="451b2-195">0x00000014</span></span>                                                        |
| <span data-ttu-id="451b2-196">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="451b2-196">Classes used in</span></span>        | [<span data-ttu-id="451b2-197">**ms-DS-quota-container**</span><span class="sxs-lookup"><span data-stu-id="451b2-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="451b2-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="451b2-198">Windows Server 2008</span></span>



| <span data-ttu-id="451b2-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="451b2-199">Entry</span></span> | <span data-ttu-id="451b2-200">Valor</span><span class="sxs-lookup"><span data-stu-id="451b2-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="451b2-201">ID do link</span><span class="sxs-lookup"><span data-stu-id="451b2-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="451b2-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="451b2-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="451b2-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="451b2-203">System-Only</span></span>            | <span data-ttu-id="451b2-204">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-204">False</span></span>                                                             |
| <span data-ttu-id="451b2-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="451b2-205">Is-Single-Valued</span></span>       | <span data-ttu-id="451b2-206">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-206">False</span></span>                                                             |
| <span data-ttu-id="451b2-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="451b2-207">Is Indexed</span></span>             | <span data-ttu-id="451b2-208">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-208">False</span></span>                                                             |
| <span data-ttu-id="451b2-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="451b2-209">In Global Catalog</span></span>      | <span data-ttu-id="451b2-210">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-210">False</span></span>                                                             |
| <span data-ttu-id="451b2-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="451b2-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="451b2-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="451b2-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="451b2-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="451b2-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="451b2-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="451b2-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="451b2-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="451b2-215">Search-Flags</span></span>           | <span data-ttu-id="451b2-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="451b2-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="451b2-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="451b2-217">System-Flags</span></span>           | <span data-ttu-id="451b2-218">0x00000014</span><span class="sxs-lookup"><span data-stu-id="451b2-218">0x00000014</span></span>                                                        |
| <span data-ttu-id="451b2-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="451b2-219">Classes used in</span></span>        | [<span data-ttu-id="451b2-220">**ms-DS-quota-container**</span><span class="sxs-lookup"><span data-stu-id="451b2-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="451b2-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="451b2-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="451b2-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="451b2-222">Entry</span></span> | <span data-ttu-id="451b2-223">Valor</span><span class="sxs-lookup"><span data-stu-id="451b2-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="451b2-224">ID do link</span><span class="sxs-lookup"><span data-stu-id="451b2-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="451b2-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="451b2-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="451b2-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="451b2-226">System-Only</span></span>            | <span data-ttu-id="451b2-227">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-227">False</span></span>                                                             |
| <span data-ttu-id="451b2-228">É de valor único</span><span class="sxs-lookup"><span data-stu-id="451b2-228">Is-Single-Valued</span></span>       | <span data-ttu-id="451b2-229">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-229">False</span></span>                                                             |
| <span data-ttu-id="451b2-230">É indexado</span><span class="sxs-lookup"><span data-stu-id="451b2-230">Is Indexed</span></span>             | <span data-ttu-id="451b2-231">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-231">False</span></span>                                                             |
| <span data-ttu-id="451b2-232">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="451b2-232">In Global Catalog</span></span>      | <span data-ttu-id="451b2-233">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-233">False</span></span>                                                             |
| <span data-ttu-id="451b2-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="451b2-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="451b2-235">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="451b2-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="451b2-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="451b2-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="451b2-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="451b2-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="451b2-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="451b2-238">Search-Flags</span></span>           | <span data-ttu-id="451b2-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="451b2-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="451b2-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="451b2-240">System-Flags</span></span>           | <span data-ttu-id="451b2-241">0x00000014</span><span class="sxs-lookup"><span data-stu-id="451b2-241">0x00000014</span></span>                                                        |
| <span data-ttu-id="451b2-242">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="451b2-242">Classes used in</span></span>        | [<span data-ttu-id="451b2-243">**ms-DS-quota-container**</span><span class="sxs-lookup"><span data-stu-id="451b2-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="451b2-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="451b2-244">Windows Server 2012</span></span>



| <span data-ttu-id="451b2-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="451b2-245">Entry</span></span> | <span data-ttu-id="451b2-246">Valor</span><span class="sxs-lookup"><span data-stu-id="451b2-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="451b2-247">ID do link</span><span class="sxs-lookup"><span data-stu-id="451b2-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="451b2-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="451b2-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="451b2-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="451b2-249">System-Only</span></span>            | <span data-ttu-id="451b2-250">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-250">False</span></span>                                                             |
| <span data-ttu-id="451b2-251">É de valor único</span><span class="sxs-lookup"><span data-stu-id="451b2-251">Is-Single-Valued</span></span>       | <span data-ttu-id="451b2-252">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-252">False</span></span>                                                             |
| <span data-ttu-id="451b2-253">É indexado</span><span class="sxs-lookup"><span data-stu-id="451b2-253">Is Indexed</span></span>             | <span data-ttu-id="451b2-254">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-254">False</span></span>                                                             |
| <span data-ttu-id="451b2-255">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="451b2-255">In Global Catalog</span></span>      | <span data-ttu-id="451b2-256">Falso</span><span class="sxs-lookup"><span data-stu-id="451b2-256">False</span></span>                                                             |
| <span data-ttu-id="451b2-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="451b2-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="451b2-258">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="451b2-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="451b2-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="451b2-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="451b2-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="451b2-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="451b2-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="451b2-261">Search-Flags</span></span>           | <span data-ttu-id="451b2-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="451b2-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="451b2-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="451b2-263">System-Flags</span></span>           | <span data-ttu-id="451b2-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="451b2-264">0x00000014</span></span>                                                        |
| <span data-ttu-id="451b2-265">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="451b2-265">Classes used in</span></span>        | [<span data-ttu-id="451b2-266">**ms-DS-quota-container**</span><span class="sxs-lookup"><span data-stu-id="451b2-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





