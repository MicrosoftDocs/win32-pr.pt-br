---
title: atributo ms-DS-quota-Trustee
description: O SID da entidade de segurança para a qual a cota está sendo atribuída.
ms.assetid: 4da8f731-0a8f-4d8a-a4e7-81ed881a30b5
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DS-quota-Trustee
- atributo msDS-QuotaTrustee do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Quota-Trustee
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7733e74c2f5d381aa6f52ea58bb03c377fab7cbe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105754835"
---
# <a name="ms-ds-quota-trustee-attribute"></a><span data-ttu-id="d60dc-105">atributo ms-DS-quota-Trustee</span><span class="sxs-lookup"><span data-stu-id="d60dc-105">ms-DS-Quota-Trustee attribute</span></span>

<span data-ttu-id="d60dc-106">O SID da entidade de segurança para a qual a cota está sendo atribuída.</span><span class="sxs-lookup"><span data-stu-id="d60dc-106">The SID of the security principal for which the quota is being assigned.</span></span>



| <span data-ttu-id="d60dc-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d60dc-107">Entry</span></span> | <span data-ttu-id="d60dc-108">Valor</span><span class="sxs-lookup"><span data-stu-id="d60dc-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d60dc-109">CN</span><span class="sxs-lookup"><span data-stu-id="d60dc-109">CN</span></span>                | <span data-ttu-id="d60dc-110">ms-DS-quota-Trustee</span><span class="sxs-lookup"><span data-stu-id="d60dc-110">ms-DS-Quota-Trustee</span></span>                  |
| <span data-ttu-id="d60dc-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d60dc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d60dc-112">msDS-QuotaTrustee</span><span class="sxs-lookup"><span data-stu-id="d60dc-112">msDS-QuotaTrustee</span></span>                    |
| <span data-ttu-id="d60dc-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="d60dc-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="d60dc-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="d60dc-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="d60dc-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="d60dc-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="d60dc-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d60dc-116">Attribute-Id</span></span>      | <span data-ttu-id="d60dc-117">1.2.840.113556.1.4.1844</span><span class="sxs-lookup"><span data-stu-id="d60dc-117">1.2.840.113556.1.4.1844</span></span>              |
| <span data-ttu-id="d60dc-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d60dc-118">System-Id-Guid</span></span>    | <span data-ttu-id="d60dc-119">16378906-4ea5-49be-a8d1-bfd41dff4f65</span><span class="sxs-lookup"><span data-stu-id="d60dc-119">16378906-4ea5-49be-a8d1-bfd41dff4f65</span></span> |
| <span data-ttu-id="d60dc-120">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d60dc-120">Syntax</span></span>            | [<span data-ttu-id="d60dc-121">**Cadeia de caracteres (SID)**</span><span class="sxs-lookup"><span data-stu-id="d60dc-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="d60dc-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="d60dc-122">Implementations</span></span>

-   [<span data-ttu-id="d60dc-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d60dc-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d60dc-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d60dc-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d60dc-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d60dc-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d60dc-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d60dc-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d60dc-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d60dc-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d60dc-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d60dc-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d60dc-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d60dc-129">Windows Server 2003</span></span>



| <span data-ttu-id="d60dc-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="d60dc-130">Entry</span></span> | <span data-ttu-id="d60dc-131">Valor</span><span class="sxs-lookup"><span data-stu-id="d60dc-131">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d60dc-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="d60dc-132">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d60dc-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d60dc-133">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d60dc-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="d60dc-134">System-Only</span></span>            | <span data-ttu-id="d60dc-135">Falso</span><span class="sxs-lookup"><span data-stu-id="d60dc-135">False</span></span>                                                         |
| <span data-ttu-id="d60dc-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d60dc-136">Is-Single-Valued</span></span>       | <span data-ttu-id="d60dc-137">True</span><span class="sxs-lookup"><span data-stu-id="d60dc-137">True</span></span>                                                          |
| <span data-ttu-id="d60dc-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="d60dc-138">Is Indexed</span></span>             | <span data-ttu-id="d60dc-139">Falso</span><span class="sxs-lookup"><span data-stu-id="d60dc-139">False</span></span>                                                         |
| <span data-ttu-id="d60dc-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d60dc-140">In Global Catalog</span></span>      | <span data-ttu-id="d60dc-141">Falso</span><span class="sxs-lookup"><span data-stu-id="d60dc-141">False</span></span>                                                         |
| <span data-ttu-id="d60dc-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d60dc-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="d60dc-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d60dc-143">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="d60dc-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d60dc-144">Range-Lower</span></span>            | <span data-ttu-id="d60dc-145">0</span><span class="sxs-lookup"><span data-stu-id="d60dc-145">0</span></span>                                                             |
| <span data-ttu-id="d60dc-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d60dc-146">Range-Upper</span></span>            | <span data-ttu-id="d60dc-147">28</span><span class="sxs-lookup"><span data-stu-id="d60dc-147">28</span></span>                                                            |
| <span data-ttu-id="d60dc-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d60dc-148">Search-Flags</span></span>           | <span data-ttu-id="d60dc-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d60dc-149">0x00000000</span></span>                                                    |
| <span data-ttu-id="d60dc-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d60dc-150">System-Flags</span></span>           | <span data-ttu-id="d60dc-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d60dc-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="d60dc-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d60dc-152">Classes used in</span></span>        | [<span data-ttu-id="d60dc-153">**ms-DS-quota-control**</span><span class="sxs-lookup"><span data-stu-id="d60dc-153">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d60dc-154">ADAM</span><span class="sxs-lookup"><span data-stu-id="d60dc-154">ADAM</span></span>



| <span data-ttu-id="d60dc-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="d60dc-155">Entry</span></span> | <span data-ttu-id="d60dc-156">Valor</span><span class="sxs-lookup"><span data-stu-id="d60dc-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d60dc-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="d60dc-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d60dc-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d60dc-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d60dc-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d60dc-159">System-Only</span></span>            | <span data-ttu-id="d60dc-160">Falso</span><span class="sxs-lookup"><span data-stu-id="d60dc-160">False</span></span>                                                         |
| <span data-ttu-id="d60dc-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d60dc-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d60dc-162">True</span><span class="sxs-lookup"><span data-stu-id="d60dc-162">True</span></span>                                                          |
| <span data-ttu-id="d60dc-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="d60dc-163">Is Indexed</span></span>             | <span data-ttu-id="d60dc-164">Falso</span><span class="sxs-lookup"><span data-stu-id="d60dc-164">False</span></span>                                                         |
| <span data-ttu-id="d60dc-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d60dc-165">In Global Catalog</span></span>      | <span data-ttu-id="d60dc-166">Falso</span><span class="sxs-lookup"><span data-stu-id="d60dc-166">False</span></span>                                                         |
| <span data-ttu-id="d60dc-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d60dc-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d60dc-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d60dc-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="d60dc-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d60dc-169">Range-Lower</span></span>            | <span data-ttu-id="d60dc-170">0</span><span class="sxs-lookup"><span data-stu-id="d60dc-170">0</span></span>                                                             |
| <span data-ttu-id="d60dc-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d60dc-171">Range-Upper</span></span>            | <span data-ttu-id="d60dc-172">28</span><span class="sxs-lookup"><span data-stu-id="d60dc-172">28</span></span>                                                            |
| <span data-ttu-id="d60dc-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d60dc-173">Search-Flags</span></span>           | <span data-ttu-id="d60dc-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d60dc-174">0x00000000</span></span>                                                    |
| <span data-ttu-id="d60dc-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d60dc-175">System-Flags</span></span>           | <span data-ttu-id="d60dc-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d60dc-176">0x00000010</span></span>                                                    |
| <span data-ttu-id="d60dc-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d60dc-177">Classes used in</span></span>        | [<span data-ttu-id="d60dc-178">**ms-DS-quota-control**</span><span class="sxs-lookup"><span data-stu-id="d60dc-178">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d60dc-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d60dc-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d60dc-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="d60dc-180">Entry</span></span> | <span data-ttu-id="d60dc-181">Valor</span><span class="sxs-lookup"><span data-stu-id="d60dc-181">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d60dc-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="d60dc-182">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d60dc-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d60dc-183">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d60dc-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="d60dc-184">System-Only</span></span>            | <span data-ttu-id="d60dc-185">Falso</span><span class="sxs-lookup"><span data-stu-id="d60dc-185">False</span></span>                                                         |
| <span data-ttu-id="d60dc-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d60dc-186">Is-Single-Valued</span></span>       | <span data-ttu-id="d60dc-187">True</span><span class="sxs-lookup"><span data-stu-id="d60dc-187">True</span></span>                                                          |
| <span data-ttu-id="d60dc-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="d60dc-188">Is Indexed</span></span>             | <span data-ttu-id="d60dc-189">Falso</span><span class="sxs-lookup"><span data-stu-id="d60dc-189">False</span></span>                                                         |
| <span data-ttu-id="d60dc-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d60dc-190">In Global Catalog</span></span>      | <span data-ttu-id="d60dc-191">Falso</span><span class="sxs-lookup"><span data-stu-id="d60dc-191">False</span></span>                                                         |
| <span data-ttu-id="d60dc-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d60dc-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="d60dc-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d60dc-193">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="d60dc-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d60dc-194">Range-Lower</span></span>            | <span data-ttu-id="d60dc-195">0</span><span class="sxs-lookup"><span data-stu-id="d60dc-195">0</span></span>                                                             |
| <span data-ttu-id="d60dc-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d60dc-196">Range-Upper</span></span>            | <span data-ttu-id="d60dc-197">28</span><span class="sxs-lookup"><span data-stu-id="d60dc-197">28</span></span>                                                            |
| <span data-ttu-id="d60dc-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d60dc-198">Search-Flags</span></span>           | <span data-ttu-id="d60dc-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d60dc-199">0x00000000</span></span>                                                    |
| <span data-ttu-id="d60dc-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d60dc-200">System-Flags</span></span>           | <span data-ttu-id="d60dc-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d60dc-201">0x00000010</span></span>                                                    |
| <span data-ttu-id="d60dc-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d60dc-202">Classes used in</span></span>        | [<span data-ttu-id="d60dc-203">**ms-DS-quota-control**</span><span class="sxs-lookup"><span data-stu-id="d60dc-203">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d60dc-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d60dc-204">Windows Server 2008</span></span>



| <span data-ttu-id="d60dc-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="d60dc-205">Entry</span></span> | <span data-ttu-id="d60dc-206">Valor</span><span class="sxs-lookup"><span data-stu-id="d60dc-206">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d60dc-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="d60dc-207">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d60dc-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d60dc-208">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d60dc-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="d60dc-209">System-Only</span></span>            | <span data-ttu-id="d60dc-210">Falso</span><span class="sxs-lookup"><span data-stu-id="d60dc-210">False</span></span>                                                         |
| <span data-ttu-id="d60dc-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d60dc-211">Is-Single-Valued</span></span>       | <span data-ttu-id="d60dc-212">True</span><span class="sxs-lookup"><span data-stu-id="d60dc-212">True</span></span>                                                          |
| <span data-ttu-id="d60dc-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="d60dc-213">Is Indexed</span></span>             | <span data-ttu-id="d60dc-214">Falso</span><span class="sxs-lookup"><span data-stu-id="d60dc-214">False</span></span>                                                         |
| <span data-ttu-id="d60dc-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d60dc-215">In Global Catalog</span></span>      | <span data-ttu-id="d60dc-216">Falso</span><span class="sxs-lookup"><span data-stu-id="d60dc-216">False</span></span>                                                         |
| <span data-ttu-id="d60dc-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d60dc-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="d60dc-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d60dc-218">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="d60dc-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d60dc-219">Range-Lower</span></span>            | <span data-ttu-id="d60dc-220">0</span><span class="sxs-lookup"><span data-stu-id="d60dc-220">0</span></span>                                                             |
| <span data-ttu-id="d60dc-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d60dc-221">Range-Upper</span></span>            | <span data-ttu-id="d60dc-222">28</span><span class="sxs-lookup"><span data-stu-id="d60dc-222">28</span></span>                                                            |
| <span data-ttu-id="d60dc-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d60dc-223">Search-Flags</span></span>           | <span data-ttu-id="d60dc-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d60dc-224">0x00000000</span></span>                                                    |
| <span data-ttu-id="d60dc-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d60dc-225">System-Flags</span></span>           | <span data-ttu-id="d60dc-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d60dc-226">0x00000010</span></span>                                                    |
| <span data-ttu-id="d60dc-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d60dc-227">Classes used in</span></span>        | [<span data-ttu-id="d60dc-228">**ms-DS-quota-control**</span><span class="sxs-lookup"><span data-stu-id="d60dc-228">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d60dc-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d60dc-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d60dc-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="d60dc-230">Entry</span></span> | <span data-ttu-id="d60dc-231">Valor</span><span class="sxs-lookup"><span data-stu-id="d60dc-231">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d60dc-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="d60dc-232">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d60dc-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d60dc-233">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d60dc-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="d60dc-234">System-Only</span></span>            | <span data-ttu-id="d60dc-235">Falso</span><span class="sxs-lookup"><span data-stu-id="d60dc-235">False</span></span>                                                         |
| <span data-ttu-id="d60dc-236">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d60dc-236">Is-Single-Valued</span></span>       | <span data-ttu-id="d60dc-237">True</span><span class="sxs-lookup"><span data-stu-id="d60dc-237">True</span></span>                                                          |
| <span data-ttu-id="d60dc-238">É indexado</span><span class="sxs-lookup"><span data-stu-id="d60dc-238">Is Indexed</span></span>             | <span data-ttu-id="d60dc-239">Falso</span><span class="sxs-lookup"><span data-stu-id="d60dc-239">False</span></span>                                                         |
| <span data-ttu-id="d60dc-240">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d60dc-240">In Global Catalog</span></span>      | <span data-ttu-id="d60dc-241">Falso</span><span class="sxs-lookup"><span data-stu-id="d60dc-241">False</span></span>                                                         |
| <span data-ttu-id="d60dc-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d60dc-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="d60dc-243">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d60dc-243">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="d60dc-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d60dc-244">Range-Lower</span></span>            | <span data-ttu-id="d60dc-245">0</span><span class="sxs-lookup"><span data-stu-id="d60dc-245">0</span></span>                                                             |
| <span data-ttu-id="d60dc-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d60dc-246">Range-Upper</span></span>            | <span data-ttu-id="d60dc-247">28</span><span class="sxs-lookup"><span data-stu-id="d60dc-247">28</span></span>                                                            |
| <span data-ttu-id="d60dc-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d60dc-248">Search-Flags</span></span>           | <span data-ttu-id="d60dc-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d60dc-249">0x00000000</span></span>                                                    |
| <span data-ttu-id="d60dc-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d60dc-250">System-Flags</span></span>           | <span data-ttu-id="d60dc-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d60dc-251">0x00000010</span></span>                                                    |
| <span data-ttu-id="d60dc-252">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d60dc-252">Classes used in</span></span>        | [<span data-ttu-id="d60dc-253">**ms-DS-quota-control**</span><span class="sxs-lookup"><span data-stu-id="d60dc-253">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d60dc-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d60dc-254">Windows Server 2012</span></span>



| <span data-ttu-id="d60dc-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="d60dc-255">Entry</span></span> | <span data-ttu-id="d60dc-256">Valor</span><span class="sxs-lookup"><span data-stu-id="d60dc-256">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d60dc-257">ID do link</span><span class="sxs-lookup"><span data-stu-id="d60dc-257">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d60dc-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d60dc-258">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="d60dc-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="d60dc-259">System-Only</span></span>            | <span data-ttu-id="d60dc-260">Falso</span><span class="sxs-lookup"><span data-stu-id="d60dc-260">False</span></span>                                                         |
| <span data-ttu-id="d60dc-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d60dc-261">Is-Single-Valued</span></span>       | <span data-ttu-id="d60dc-262">True</span><span class="sxs-lookup"><span data-stu-id="d60dc-262">True</span></span>                                                          |
| <span data-ttu-id="d60dc-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="d60dc-263">Is Indexed</span></span>             | <span data-ttu-id="d60dc-264">Falso</span><span class="sxs-lookup"><span data-stu-id="d60dc-264">False</span></span>                                                         |
| <span data-ttu-id="d60dc-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d60dc-265">In Global Catalog</span></span>      | <span data-ttu-id="d60dc-266">Falso</span><span class="sxs-lookup"><span data-stu-id="d60dc-266">False</span></span>                                                         |
| <span data-ttu-id="d60dc-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d60dc-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="d60dc-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d60dc-268">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="d60dc-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d60dc-269">Range-Lower</span></span>            | <span data-ttu-id="d60dc-270">0</span><span class="sxs-lookup"><span data-stu-id="d60dc-270">0</span></span>                                                             |
| <span data-ttu-id="d60dc-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d60dc-271">Range-Upper</span></span>            | <span data-ttu-id="d60dc-272">28</span><span class="sxs-lookup"><span data-stu-id="d60dc-272">28</span></span>                                                            |
| <span data-ttu-id="d60dc-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d60dc-273">Search-Flags</span></span>           | <span data-ttu-id="d60dc-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d60dc-274">0x00000000</span></span>                                                    |
| <span data-ttu-id="d60dc-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d60dc-275">System-Flags</span></span>           | <span data-ttu-id="d60dc-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d60dc-276">0x00000010</span></span>                                                    |
| <span data-ttu-id="d60dc-277">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d60dc-277">Classes used in</span></span>        | [<span data-ttu-id="d60dc-278">**ms-DS-quota-control**</span><span class="sxs-lookup"><span data-stu-id="d60dc-278">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



 

 





