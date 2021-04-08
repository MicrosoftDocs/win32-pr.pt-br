---
title: ACS-Max-token-bucket-atributo por fluxo
description: O atributo ACS-Max-token-bucket-por-Flow é somente para uso interno.
ms.assetid: 2c269bda-7b0d-4ef4-8c67-9f5e7c52e3ae
ms.tgt_platform: multiple
keywords:
- ACS-Max-token-bucket por esquema de AD do atributo de fluxo
- Esquema de AD do atributo aCSMaxTokenBucketPerFlow
topic_type:
- apiref
api_name:
- ACS-Max-Token-Bucket-Per-Flow
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb323af82b270c20478e8af4aafc3ee4142125ee
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087171"
---
# <a name="acs-max-token-bucket-per-flow-attribute"></a><span data-ttu-id="4d3fd-105">ACS-Max-token-bucket-atributo por fluxo</span><span class="sxs-lookup"><span data-stu-id="4d3fd-105">ACS-Max-Token-Bucket-Per-Flow attribute</span></span>

<span data-ttu-id="4d3fd-106">O atributo **ACS-Max-token-bucket-por-Flow** é somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="4d3fd-106">The **ACS-Max-Token-Bucket-Per-Flow** attribute is for internal use only.</span></span> <span data-ttu-id="4d3fd-107">Com base em RFC2210.</span><span class="sxs-lookup"><span data-stu-id="4d3fd-107">Based on RFC2210.</span></span>



| <span data-ttu-id="4d3fd-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="4d3fd-108">Entry</span></span> | <span data-ttu-id="4d3fd-109">Valor</span><span class="sxs-lookup"><span data-stu-id="4d3fd-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="4d3fd-110">CN</span><span class="sxs-lookup"><span data-stu-id="4d3fd-110">CN</span></span>                | <span data-ttu-id="4d3fd-111">ACS-Max-token-bucket-por-Flow</span><span class="sxs-lookup"><span data-stu-id="4d3fd-111">ACS-Max-Token-Bucket-Per-Flow</span></span>        |
| <span data-ttu-id="4d3fd-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4d3fd-112">Ldap-Display-Name</span></span> | <span data-ttu-id="4d3fd-113">aCSMaxTokenBucketPerFlow</span><span class="sxs-lookup"><span data-stu-id="4d3fd-113">aCSMaxTokenBucketPerFlow</span></span>             |
| <span data-ttu-id="4d3fd-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="4d3fd-114">Size</span></span>              | <span data-ttu-id="4d3fd-115">8 bytes</span><span class="sxs-lookup"><span data-stu-id="4d3fd-115">8 bytes</span></span>                              |
| <span data-ttu-id="4d3fd-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="4d3fd-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="4d3fd-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="4d3fd-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="4d3fd-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4d3fd-118">Attribute-Id</span></span>      | <span data-ttu-id="4d3fd-119">1.2.840.113556.1.4.1313</span><span class="sxs-lookup"><span data-stu-id="4d3fd-119">1.2.840.113556.1.4.1313</span></span>              |
| <span data-ttu-id="4d3fd-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4d3fd-120">System-Id-Guid</span></span>    | <span data-ttu-id="4d3fd-121">81f6e0df-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="4d3fd-121">81f6e0df-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="4d3fd-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d3fd-122">Syntax</span></span>            | [<span data-ttu-id="4d3fd-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="4d3fd-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="4d3fd-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="4d3fd-124">Implementations</span></span>

-   [<span data-ttu-id="4d3fd-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4d3fd-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4d3fd-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4d3fd-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4d3fd-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4d3fd-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4d3fd-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4d3fd-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4d3fd-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4d3fd-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4d3fd-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4d3fd-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4d3fd-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4d3fd-131">Windows 2000 Server</span></span>



| <span data-ttu-id="4d3fd-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="4d3fd-132">Entry</span></span> | <span data-ttu-id="4d3fd-133">Valor</span><span class="sxs-lookup"><span data-stu-id="4d3fd-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4d3fd-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="4d3fd-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4d3fd-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d3fd-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4d3fd-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d3fd-136">System-Only</span></span>            | <span data-ttu-id="4d3fd-137">Falso</span><span class="sxs-lookup"><span data-stu-id="4d3fd-137">False</span></span>                                        |
| <span data-ttu-id="4d3fd-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4d3fd-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4d3fd-139">True</span><span class="sxs-lookup"><span data-stu-id="4d3fd-139">True</span></span>                                         |
| <span data-ttu-id="4d3fd-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="4d3fd-140">Is Indexed</span></span>             | <span data-ttu-id="4d3fd-141">Falso</span><span class="sxs-lookup"><span data-stu-id="4d3fd-141">False</span></span>                                        |
| <span data-ttu-id="4d3fd-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4d3fd-142">In Global Catalog</span></span>      | <span data-ttu-id="4d3fd-143">Falso</span><span class="sxs-lookup"><span data-stu-id="4d3fd-143">False</span></span>                                        |
| <span data-ttu-id="4d3fd-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4d3fd-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d3fd-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4d3fd-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4d3fd-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d3fd-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4d3fd-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d3fd-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4d3fd-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d3fd-148">Search-Flags</span></span>           | <span data-ttu-id="4d3fd-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d3fd-149">0x00000000</span></span>                                   |
| <span data-ttu-id="4d3fd-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d3fd-150">System-Flags</span></span>           | <span data-ttu-id="4d3fd-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d3fd-151">0x00000010</span></span>                                   |
| <span data-ttu-id="4d3fd-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4d3fd-152">Classes used in</span></span>        | [<span data-ttu-id="4d3fd-153">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="4d3fd-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4d3fd-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4d3fd-154">Windows Server 2003</span></span>



| <span data-ttu-id="4d3fd-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="4d3fd-155">Entry</span></span> | <span data-ttu-id="4d3fd-156">Valor</span><span class="sxs-lookup"><span data-stu-id="4d3fd-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4d3fd-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="4d3fd-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4d3fd-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d3fd-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4d3fd-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d3fd-159">System-Only</span></span>            | <span data-ttu-id="4d3fd-160">Falso</span><span class="sxs-lookup"><span data-stu-id="4d3fd-160">False</span></span>                                        |
| <span data-ttu-id="4d3fd-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4d3fd-161">Is-Single-Valued</span></span>       | <span data-ttu-id="4d3fd-162">True</span><span class="sxs-lookup"><span data-stu-id="4d3fd-162">True</span></span>                                         |
| <span data-ttu-id="4d3fd-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="4d3fd-163">Is Indexed</span></span>             | <span data-ttu-id="4d3fd-164">Falso</span><span class="sxs-lookup"><span data-stu-id="4d3fd-164">False</span></span>                                        |
| <span data-ttu-id="4d3fd-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4d3fd-165">In Global Catalog</span></span>      | <span data-ttu-id="4d3fd-166">Falso</span><span class="sxs-lookup"><span data-stu-id="4d3fd-166">False</span></span>                                        |
| <span data-ttu-id="4d3fd-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4d3fd-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d3fd-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4d3fd-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4d3fd-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d3fd-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4d3fd-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d3fd-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4d3fd-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d3fd-171">Search-Flags</span></span>           | <span data-ttu-id="4d3fd-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d3fd-172">0x00000000</span></span>                                   |
| <span data-ttu-id="4d3fd-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d3fd-173">System-Flags</span></span>           | <span data-ttu-id="4d3fd-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d3fd-174">0x00000010</span></span>                                   |
| <span data-ttu-id="4d3fd-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4d3fd-175">Classes used in</span></span>        | [<span data-ttu-id="4d3fd-176">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="4d3fd-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4d3fd-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4d3fd-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4d3fd-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="4d3fd-178">Entry</span></span> | <span data-ttu-id="4d3fd-179">Valor</span><span class="sxs-lookup"><span data-stu-id="4d3fd-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4d3fd-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="4d3fd-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4d3fd-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d3fd-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4d3fd-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d3fd-182">System-Only</span></span>            | <span data-ttu-id="4d3fd-183">Falso</span><span class="sxs-lookup"><span data-stu-id="4d3fd-183">False</span></span>                                        |
| <span data-ttu-id="4d3fd-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4d3fd-184">Is-Single-Valued</span></span>       | <span data-ttu-id="4d3fd-185">True</span><span class="sxs-lookup"><span data-stu-id="4d3fd-185">True</span></span>                                         |
| <span data-ttu-id="4d3fd-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="4d3fd-186">Is Indexed</span></span>             | <span data-ttu-id="4d3fd-187">Falso</span><span class="sxs-lookup"><span data-stu-id="4d3fd-187">False</span></span>                                        |
| <span data-ttu-id="4d3fd-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4d3fd-188">In Global Catalog</span></span>      | <span data-ttu-id="4d3fd-189">Falso</span><span class="sxs-lookup"><span data-stu-id="4d3fd-189">False</span></span>                                        |
| <span data-ttu-id="4d3fd-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4d3fd-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d3fd-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4d3fd-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4d3fd-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d3fd-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4d3fd-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d3fd-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4d3fd-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d3fd-194">Search-Flags</span></span>           | <span data-ttu-id="4d3fd-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d3fd-195">0x00000000</span></span>                                   |
| <span data-ttu-id="4d3fd-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d3fd-196">System-Flags</span></span>           | <span data-ttu-id="4d3fd-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d3fd-197">0x00000010</span></span>                                   |
| <span data-ttu-id="4d3fd-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4d3fd-198">Classes used in</span></span>        | [<span data-ttu-id="4d3fd-199">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="4d3fd-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4d3fd-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d3fd-200">Windows Server 2008</span></span>



| <span data-ttu-id="4d3fd-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="4d3fd-201">Entry</span></span> | <span data-ttu-id="4d3fd-202">Valor</span><span class="sxs-lookup"><span data-stu-id="4d3fd-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4d3fd-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="4d3fd-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4d3fd-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d3fd-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4d3fd-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d3fd-205">System-Only</span></span>            | <span data-ttu-id="4d3fd-206">Falso</span><span class="sxs-lookup"><span data-stu-id="4d3fd-206">False</span></span>                                        |
| <span data-ttu-id="4d3fd-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4d3fd-207">Is-Single-Valued</span></span>       | <span data-ttu-id="4d3fd-208">True</span><span class="sxs-lookup"><span data-stu-id="4d3fd-208">True</span></span>                                         |
| <span data-ttu-id="4d3fd-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="4d3fd-209">Is Indexed</span></span>             | <span data-ttu-id="4d3fd-210">Falso</span><span class="sxs-lookup"><span data-stu-id="4d3fd-210">False</span></span>                                        |
| <span data-ttu-id="4d3fd-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4d3fd-211">In Global Catalog</span></span>      | <span data-ttu-id="4d3fd-212">Falso</span><span class="sxs-lookup"><span data-stu-id="4d3fd-212">False</span></span>                                        |
| <span data-ttu-id="4d3fd-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4d3fd-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d3fd-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4d3fd-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4d3fd-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d3fd-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4d3fd-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d3fd-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4d3fd-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d3fd-217">Search-Flags</span></span>           | <span data-ttu-id="4d3fd-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d3fd-218">0x00000000</span></span>                                   |
| <span data-ttu-id="4d3fd-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d3fd-219">System-Flags</span></span>           | <span data-ttu-id="4d3fd-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d3fd-220">0x00000010</span></span>                                   |
| <span data-ttu-id="4d3fd-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4d3fd-221">Classes used in</span></span>        | [<span data-ttu-id="4d3fd-222">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="4d3fd-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4d3fd-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4d3fd-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4d3fd-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="4d3fd-224">Entry</span></span> | <span data-ttu-id="4d3fd-225">Valor</span><span class="sxs-lookup"><span data-stu-id="4d3fd-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4d3fd-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="4d3fd-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4d3fd-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d3fd-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4d3fd-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d3fd-228">System-Only</span></span>            | <span data-ttu-id="4d3fd-229">Falso</span><span class="sxs-lookup"><span data-stu-id="4d3fd-229">False</span></span>                                        |
| <span data-ttu-id="4d3fd-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4d3fd-230">Is-Single-Valued</span></span>       | <span data-ttu-id="4d3fd-231">True</span><span class="sxs-lookup"><span data-stu-id="4d3fd-231">True</span></span>                                         |
| <span data-ttu-id="4d3fd-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="4d3fd-232">Is Indexed</span></span>             | <span data-ttu-id="4d3fd-233">Falso</span><span class="sxs-lookup"><span data-stu-id="4d3fd-233">False</span></span>                                        |
| <span data-ttu-id="4d3fd-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4d3fd-234">In Global Catalog</span></span>      | <span data-ttu-id="4d3fd-235">Falso</span><span class="sxs-lookup"><span data-stu-id="4d3fd-235">False</span></span>                                        |
| <span data-ttu-id="4d3fd-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4d3fd-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d3fd-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4d3fd-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4d3fd-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d3fd-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4d3fd-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d3fd-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4d3fd-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d3fd-240">Search-Flags</span></span>           | <span data-ttu-id="4d3fd-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d3fd-241">0x00000000</span></span>                                   |
| <span data-ttu-id="4d3fd-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d3fd-242">System-Flags</span></span>           | <span data-ttu-id="4d3fd-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d3fd-243">0x00000010</span></span>                                   |
| <span data-ttu-id="4d3fd-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4d3fd-244">Classes used in</span></span>        | [<span data-ttu-id="4d3fd-245">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="4d3fd-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4d3fd-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4d3fd-246">Windows Server 2012</span></span>



| <span data-ttu-id="4d3fd-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="4d3fd-247">Entry</span></span> | <span data-ttu-id="4d3fd-248">Valor</span><span class="sxs-lookup"><span data-stu-id="4d3fd-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4d3fd-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="4d3fd-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4d3fd-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d3fd-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4d3fd-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d3fd-251">System-Only</span></span>            | <span data-ttu-id="4d3fd-252">Falso</span><span class="sxs-lookup"><span data-stu-id="4d3fd-252">False</span></span>                                        |
| <span data-ttu-id="4d3fd-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4d3fd-253">Is-Single-Valued</span></span>       | <span data-ttu-id="4d3fd-254">True</span><span class="sxs-lookup"><span data-stu-id="4d3fd-254">True</span></span>                                         |
| <span data-ttu-id="4d3fd-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="4d3fd-255">Is Indexed</span></span>             | <span data-ttu-id="4d3fd-256">Falso</span><span class="sxs-lookup"><span data-stu-id="4d3fd-256">False</span></span>                                        |
| <span data-ttu-id="4d3fd-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4d3fd-257">In Global Catalog</span></span>      | <span data-ttu-id="4d3fd-258">Falso</span><span class="sxs-lookup"><span data-stu-id="4d3fd-258">False</span></span>                                        |
| <span data-ttu-id="4d3fd-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4d3fd-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d3fd-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4d3fd-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4d3fd-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d3fd-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4d3fd-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d3fd-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4d3fd-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d3fd-263">Search-Flags</span></span>           | <span data-ttu-id="4d3fd-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d3fd-264">0x00000000</span></span>                                   |
| <span data-ttu-id="4d3fd-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d3fd-265">System-Flags</span></span>           | <span data-ttu-id="4d3fd-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d3fd-266">0x00000010</span></span>                                   |
| <span data-ttu-id="4d3fd-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4d3fd-267">Classes used in</span></span>        | [<span data-ttu-id="4d3fd-268">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="4d3fd-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





