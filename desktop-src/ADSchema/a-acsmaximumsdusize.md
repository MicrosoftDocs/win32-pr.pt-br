---
title: ACS-atributo Maximum-SDU-size
description: O atributo ACS-Maximum-SDU-Size é somente para uso interno.
ms.assetid: 60dc8b92-888f-4eaf-8c7a-70d1ee12b490
ms.tgt_platform: multiple
keywords:
- ACS-esquema de AD de atributo de tamanho máximo SDU
- Esquema de AD do atributo aCSMaximumSDUSize
topic_type:
- apiref
api_name:
- ACS-Maximum-SDU-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c9fa6260b3e0370f8a3d6e0ddfdab206d41db02
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645380"
---
# <a name="acs-maximum-sdu-size-attribute"></a><span data-ttu-id="5eb75-105">ACS-atributo Maximum-SDU-size</span><span class="sxs-lookup"><span data-stu-id="5eb75-105">ACS-Maximum-SDU-Size attribute</span></span>

<span data-ttu-id="5eb75-106">O atributo **ACS-Maximum-SDU-size** é somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="5eb75-106">The **ACS-Maximum-SDU-Size** attribute is for internal use only.</span></span> <span data-ttu-id="5eb75-107">Com base em RFC2210.</span><span class="sxs-lookup"><span data-stu-id="5eb75-107">Based on RFC2210.</span></span>



| <span data-ttu-id="5eb75-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="5eb75-108">Entry</span></span> | <span data-ttu-id="5eb75-109">Valor</span><span class="sxs-lookup"><span data-stu-id="5eb75-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5eb75-110">CN</span><span class="sxs-lookup"><span data-stu-id="5eb75-110">CN</span></span>                | <span data-ttu-id="5eb75-111">ACS-Maximum-SDU-tamanho</span><span class="sxs-lookup"><span data-stu-id="5eb75-111">ACS-Maximum-SDU-Size</span></span>                 |
| <span data-ttu-id="5eb75-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5eb75-112">Ldap-Display-Name</span></span> | <span data-ttu-id="5eb75-113">aCSMaximumSDUSize</span><span class="sxs-lookup"><span data-stu-id="5eb75-113">aCSMaximumSDUSize</span></span>                    |
| <span data-ttu-id="5eb75-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="5eb75-114">Size</span></span>              | <span data-ttu-id="5eb75-115">8 bytes</span><span class="sxs-lookup"><span data-stu-id="5eb75-115">8 bytes</span></span>                              |
| <span data-ttu-id="5eb75-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="5eb75-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="5eb75-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="5eb75-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="5eb75-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5eb75-118">Attribute-Id</span></span>      | <span data-ttu-id="5eb75-119">1.2.840.113556.1.4.1314</span><span class="sxs-lookup"><span data-stu-id="5eb75-119">1.2.840.113556.1.4.1314</span></span>              |
| <span data-ttu-id="5eb75-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5eb75-120">System-Id-Guid</span></span>    | <span data-ttu-id="5eb75-121">87a2d8f9-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="5eb75-121">87a2d8f9-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="5eb75-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5eb75-122">Syntax</span></span>            | [<span data-ttu-id="5eb75-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="5eb75-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="5eb75-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="5eb75-124">Implementations</span></span>

-   [<span data-ttu-id="5eb75-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5eb75-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5eb75-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5eb75-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5eb75-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5eb75-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5eb75-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5eb75-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5eb75-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5eb75-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5eb75-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5eb75-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5eb75-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5eb75-131">Windows 2000 Server</span></span>



| <span data-ttu-id="5eb75-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="5eb75-132">Entry</span></span> | <span data-ttu-id="5eb75-133">Valor</span><span class="sxs-lookup"><span data-stu-id="5eb75-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5eb75-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="5eb75-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5eb75-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5eb75-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5eb75-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="5eb75-136">System-Only</span></span>            | <span data-ttu-id="5eb75-137">Falso</span><span class="sxs-lookup"><span data-stu-id="5eb75-137">False</span></span>                                        |
| <span data-ttu-id="5eb75-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5eb75-138">Is-Single-Valued</span></span>       | <span data-ttu-id="5eb75-139">True</span><span class="sxs-lookup"><span data-stu-id="5eb75-139">True</span></span>                                         |
| <span data-ttu-id="5eb75-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="5eb75-140">Is Indexed</span></span>             | <span data-ttu-id="5eb75-141">Falso</span><span class="sxs-lookup"><span data-stu-id="5eb75-141">False</span></span>                                        |
| <span data-ttu-id="5eb75-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5eb75-142">In Global Catalog</span></span>      | <span data-ttu-id="5eb75-143">Falso</span><span class="sxs-lookup"><span data-stu-id="5eb75-143">False</span></span>                                        |
| <span data-ttu-id="5eb75-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5eb75-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="5eb75-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5eb75-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5eb75-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5eb75-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5eb75-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5eb75-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5eb75-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5eb75-148">Search-Flags</span></span>           | <span data-ttu-id="5eb75-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5eb75-149">0x00000000</span></span>                                   |
| <span data-ttu-id="5eb75-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5eb75-150">System-Flags</span></span>           | <span data-ttu-id="5eb75-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5eb75-151">0x00000010</span></span>                                   |
| <span data-ttu-id="5eb75-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5eb75-152">Classes used in</span></span>        | [<span data-ttu-id="5eb75-153">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="5eb75-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5eb75-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5eb75-154">Windows Server 2003</span></span>



| <span data-ttu-id="5eb75-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="5eb75-155">Entry</span></span> | <span data-ttu-id="5eb75-156">Valor</span><span class="sxs-lookup"><span data-stu-id="5eb75-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5eb75-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="5eb75-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5eb75-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5eb75-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5eb75-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5eb75-159">System-Only</span></span>            | <span data-ttu-id="5eb75-160">Falso</span><span class="sxs-lookup"><span data-stu-id="5eb75-160">False</span></span>                                        |
| <span data-ttu-id="5eb75-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5eb75-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5eb75-162">True</span><span class="sxs-lookup"><span data-stu-id="5eb75-162">True</span></span>                                         |
| <span data-ttu-id="5eb75-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="5eb75-163">Is Indexed</span></span>             | <span data-ttu-id="5eb75-164">Falso</span><span class="sxs-lookup"><span data-stu-id="5eb75-164">False</span></span>                                        |
| <span data-ttu-id="5eb75-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5eb75-165">In Global Catalog</span></span>      | <span data-ttu-id="5eb75-166">Falso</span><span class="sxs-lookup"><span data-stu-id="5eb75-166">False</span></span>                                        |
| <span data-ttu-id="5eb75-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5eb75-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5eb75-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5eb75-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5eb75-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5eb75-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5eb75-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5eb75-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5eb75-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5eb75-171">Search-Flags</span></span>           | <span data-ttu-id="5eb75-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5eb75-172">0x00000000</span></span>                                   |
| <span data-ttu-id="5eb75-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5eb75-173">System-Flags</span></span>           | <span data-ttu-id="5eb75-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5eb75-174">0x00000010</span></span>                                   |
| <span data-ttu-id="5eb75-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5eb75-175">Classes used in</span></span>        | [<span data-ttu-id="5eb75-176">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="5eb75-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5eb75-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5eb75-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5eb75-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="5eb75-178">Entry</span></span> | <span data-ttu-id="5eb75-179">Valor</span><span class="sxs-lookup"><span data-stu-id="5eb75-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5eb75-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="5eb75-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5eb75-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5eb75-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5eb75-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="5eb75-182">System-Only</span></span>            | <span data-ttu-id="5eb75-183">Falso</span><span class="sxs-lookup"><span data-stu-id="5eb75-183">False</span></span>                                        |
| <span data-ttu-id="5eb75-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5eb75-184">Is-Single-Valued</span></span>       | <span data-ttu-id="5eb75-185">True</span><span class="sxs-lookup"><span data-stu-id="5eb75-185">True</span></span>                                         |
| <span data-ttu-id="5eb75-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="5eb75-186">Is Indexed</span></span>             | <span data-ttu-id="5eb75-187">Falso</span><span class="sxs-lookup"><span data-stu-id="5eb75-187">False</span></span>                                        |
| <span data-ttu-id="5eb75-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5eb75-188">In Global Catalog</span></span>      | <span data-ttu-id="5eb75-189">Falso</span><span class="sxs-lookup"><span data-stu-id="5eb75-189">False</span></span>                                        |
| <span data-ttu-id="5eb75-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5eb75-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="5eb75-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5eb75-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5eb75-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5eb75-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5eb75-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5eb75-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5eb75-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5eb75-194">Search-Flags</span></span>           | <span data-ttu-id="5eb75-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5eb75-195">0x00000000</span></span>                                   |
| <span data-ttu-id="5eb75-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5eb75-196">System-Flags</span></span>           | <span data-ttu-id="5eb75-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5eb75-197">0x00000010</span></span>                                   |
| <span data-ttu-id="5eb75-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5eb75-198">Classes used in</span></span>        | [<span data-ttu-id="5eb75-199">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="5eb75-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5eb75-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5eb75-200">Windows Server 2008</span></span>



| <span data-ttu-id="5eb75-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="5eb75-201">Entry</span></span> | <span data-ttu-id="5eb75-202">Valor</span><span class="sxs-lookup"><span data-stu-id="5eb75-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5eb75-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="5eb75-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5eb75-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5eb75-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5eb75-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="5eb75-205">System-Only</span></span>            | <span data-ttu-id="5eb75-206">Falso</span><span class="sxs-lookup"><span data-stu-id="5eb75-206">False</span></span>                                        |
| <span data-ttu-id="5eb75-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5eb75-207">Is-Single-Valued</span></span>       | <span data-ttu-id="5eb75-208">True</span><span class="sxs-lookup"><span data-stu-id="5eb75-208">True</span></span>                                         |
| <span data-ttu-id="5eb75-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="5eb75-209">Is Indexed</span></span>             | <span data-ttu-id="5eb75-210">Falso</span><span class="sxs-lookup"><span data-stu-id="5eb75-210">False</span></span>                                        |
| <span data-ttu-id="5eb75-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5eb75-211">In Global Catalog</span></span>      | <span data-ttu-id="5eb75-212">Falso</span><span class="sxs-lookup"><span data-stu-id="5eb75-212">False</span></span>                                        |
| <span data-ttu-id="5eb75-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5eb75-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="5eb75-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5eb75-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5eb75-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5eb75-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5eb75-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5eb75-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5eb75-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5eb75-217">Search-Flags</span></span>           | <span data-ttu-id="5eb75-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5eb75-218">0x00000000</span></span>                                   |
| <span data-ttu-id="5eb75-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5eb75-219">System-Flags</span></span>           | <span data-ttu-id="5eb75-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5eb75-220">0x00000010</span></span>                                   |
| <span data-ttu-id="5eb75-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5eb75-221">Classes used in</span></span>        | [<span data-ttu-id="5eb75-222">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="5eb75-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5eb75-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5eb75-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5eb75-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="5eb75-224">Entry</span></span> | <span data-ttu-id="5eb75-225">Valor</span><span class="sxs-lookup"><span data-stu-id="5eb75-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5eb75-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="5eb75-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5eb75-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5eb75-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5eb75-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="5eb75-228">System-Only</span></span>            | <span data-ttu-id="5eb75-229">Falso</span><span class="sxs-lookup"><span data-stu-id="5eb75-229">False</span></span>                                        |
| <span data-ttu-id="5eb75-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5eb75-230">Is-Single-Valued</span></span>       | <span data-ttu-id="5eb75-231">True</span><span class="sxs-lookup"><span data-stu-id="5eb75-231">True</span></span>                                         |
| <span data-ttu-id="5eb75-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="5eb75-232">Is Indexed</span></span>             | <span data-ttu-id="5eb75-233">Falso</span><span class="sxs-lookup"><span data-stu-id="5eb75-233">False</span></span>                                        |
| <span data-ttu-id="5eb75-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5eb75-234">In Global Catalog</span></span>      | <span data-ttu-id="5eb75-235">Falso</span><span class="sxs-lookup"><span data-stu-id="5eb75-235">False</span></span>                                        |
| <span data-ttu-id="5eb75-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5eb75-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="5eb75-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5eb75-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5eb75-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5eb75-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5eb75-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5eb75-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5eb75-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5eb75-240">Search-Flags</span></span>           | <span data-ttu-id="5eb75-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5eb75-241">0x00000000</span></span>                                   |
| <span data-ttu-id="5eb75-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5eb75-242">System-Flags</span></span>           | <span data-ttu-id="5eb75-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5eb75-243">0x00000010</span></span>                                   |
| <span data-ttu-id="5eb75-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5eb75-244">Classes used in</span></span>        | [<span data-ttu-id="5eb75-245">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="5eb75-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5eb75-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5eb75-246">Windows Server 2012</span></span>



| <span data-ttu-id="5eb75-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="5eb75-247">Entry</span></span> | <span data-ttu-id="5eb75-248">Valor</span><span class="sxs-lookup"><span data-stu-id="5eb75-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5eb75-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="5eb75-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5eb75-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5eb75-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5eb75-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="5eb75-251">System-Only</span></span>            | <span data-ttu-id="5eb75-252">Falso</span><span class="sxs-lookup"><span data-stu-id="5eb75-252">False</span></span>                                        |
| <span data-ttu-id="5eb75-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5eb75-253">Is-Single-Valued</span></span>       | <span data-ttu-id="5eb75-254">True</span><span class="sxs-lookup"><span data-stu-id="5eb75-254">True</span></span>                                         |
| <span data-ttu-id="5eb75-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="5eb75-255">Is Indexed</span></span>             | <span data-ttu-id="5eb75-256">Falso</span><span class="sxs-lookup"><span data-stu-id="5eb75-256">False</span></span>                                        |
| <span data-ttu-id="5eb75-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5eb75-257">In Global Catalog</span></span>      | <span data-ttu-id="5eb75-258">Falso</span><span class="sxs-lookup"><span data-stu-id="5eb75-258">False</span></span>                                        |
| <span data-ttu-id="5eb75-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5eb75-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="5eb75-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5eb75-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5eb75-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5eb75-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5eb75-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5eb75-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5eb75-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5eb75-263">Search-Flags</span></span>           | <span data-ttu-id="5eb75-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5eb75-264">0x00000000</span></span>                                   |
| <span data-ttu-id="5eb75-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5eb75-265">System-Flags</span></span>           | <span data-ttu-id="5eb75-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5eb75-266">0x00000010</span></span>                                   |
| <span data-ttu-id="5eb75-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5eb75-267">Classes used in</span></span>        | [<span data-ttu-id="5eb75-268">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="5eb75-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





