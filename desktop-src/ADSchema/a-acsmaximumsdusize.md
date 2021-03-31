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
# <a name="acs-maximum-sdu-size-attribute"></a><span data-ttu-id="b0883-105">ACS-atributo Maximum-SDU-size</span><span class="sxs-lookup"><span data-stu-id="b0883-105">ACS-Maximum-SDU-Size attribute</span></span>

<span data-ttu-id="b0883-106">O atributo **ACS-Maximum-SDU-size** é somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="b0883-106">The **ACS-Maximum-SDU-Size** attribute is for internal use only.</span></span> <span data-ttu-id="b0883-107">Com base em RFC2210.</span><span class="sxs-lookup"><span data-stu-id="b0883-107">Based on RFC2210.</span></span>



| <span data-ttu-id="b0883-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="b0883-108">Entry</span></span> | <span data-ttu-id="b0883-109">Valor</span><span class="sxs-lookup"><span data-stu-id="b0883-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b0883-110">CN</span><span class="sxs-lookup"><span data-stu-id="b0883-110">CN</span></span>                | <span data-ttu-id="b0883-111">ACS-Maximum-SDU-tamanho</span><span class="sxs-lookup"><span data-stu-id="b0883-111">ACS-Maximum-SDU-Size</span></span>                 |
| <span data-ttu-id="b0883-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b0883-112">Ldap-Display-Name</span></span> | <span data-ttu-id="b0883-113">aCSMaximumSDUSize</span><span class="sxs-lookup"><span data-stu-id="b0883-113">aCSMaximumSDUSize</span></span>                    |
| <span data-ttu-id="b0883-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b0883-114">Size</span></span>              | <span data-ttu-id="b0883-115">8 bytes</span><span class="sxs-lookup"><span data-stu-id="b0883-115">8 bytes</span></span>                              |
| <span data-ttu-id="b0883-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="b0883-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="b0883-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="b0883-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b0883-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b0883-118">Attribute-Id</span></span>      | <span data-ttu-id="b0883-119">1.2.840.113556.1.4.1314</span><span class="sxs-lookup"><span data-stu-id="b0883-119">1.2.840.113556.1.4.1314</span></span>              |
| <span data-ttu-id="b0883-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b0883-120">System-Id-Guid</span></span>    | <span data-ttu-id="b0883-121">87a2d8f9-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="b0883-121">87a2d8f9-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="b0883-122">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0883-122">Syntax</span></span>            | [<span data-ttu-id="b0883-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="b0883-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="b0883-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="b0883-124">Implementations</span></span>

-   [<span data-ttu-id="b0883-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b0883-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b0883-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b0883-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b0883-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b0883-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b0883-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b0883-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b0883-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b0883-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b0883-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b0883-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b0883-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b0883-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b0883-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="b0883-132">Entry</span></span> | <span data-ttu-id="b0883-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b0883-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b0883-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="b0883-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0883-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0883-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0883-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0883-136">System-Only</span></span>            | <span data-ttu-id="b0883-137">Falso</span><span class="sxs-lookup"><span data-stu-id="b0883-137">False</span></span>                                        |
| <span data-ttu-id="b0883-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b0883-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b0883-139">True</span><span class="sxs-lookup"><span data-stu-id="b0883-139">True</span></span>                                         |
| <span data-ttu-id="b0883-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="b0883-140">Is Indexed</span></span>             | <span data-ttu-id="b0883-141">Falso</span><span class="sxs-lookup"><span data-stu-id="b0883-141">False</span></span>                                        |
| <span data-ttu-id="b0883-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b0883-142">In Global Catalog</span></span>      | <span data-ttu-id="b0883-143">Falso</span><span class="sxs-lookup"><span data-stu-id="b0883-143">False</span></span>                                        |
| <span data-ttu-id="b0883-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b0883-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0883-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b0883-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b0883-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0883-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b0883-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0883-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b0883-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0883-148">Search-Flags</span></span>           | <span data-ttu-id="b0883-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0883-149">0x00000000</span></span>                                   |
| <span data-ttu-id="b0883-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0883-150">System-Flags</span></span>           | <span data-ttu-id="b0883-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0883-151">0x00000010</span></span>                                   |
| <span data-ttu-id="b0883-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b0883-152">Classes used in</span></span>        | [<span data-ttu-id="b0883-153">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="b0883-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b0883-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b0883-154">Windows Server 2003</span></span>



| <span data-ttu-id="b0883-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="b0883-155">Entry</span></span> | <span data-ttu-id="b0883-156">Valor</span><span class="sxs-lookup"><span data-stu-id="b0883-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b0883-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="b0883-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0883-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0883-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0883-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0883-159">System-Only</span></span>            | <span data-ttu-id="b0883-160">Falso</span><span class="sxs-lookup"><span data-stu-id="b0883-160">False</span></span>                                        |
| <span data-ttu-id="b0883-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b0883-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b0883-162">True</span><span class="sxs-lookup"><span data-stu-id="b0883-162">True</span></span>                                         |
| <span data-ttu-id="b0883-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="b0883-163">Is Indexed</span></span>             | <span data-ttu-id="b0883-164">Falso</span><span class="sxs-lookup"><span data-stu-id="b0883-164">False</span></span>                                        |
| <span data-ttu-id="b0883-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b0883-165">In Global Catalog</span></span>      | <span data-ttu-id="b0883-166">Falso</span><span class="sxs-lookup"><span data-stu-id="b0883-166">False</span></span>                                        |
| <span data-ttu-id="b0883-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b0883-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0883-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b0883-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b0883-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0883-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b0883-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0883-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b0883-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0883-171">Search-Flags</span></span>           | <span data-ttu-id="b0883-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0883-172">0x00000000</span></span>                                   |
| <span data-ttu-id="b0883-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0883-173">System-Flags</span></span>           | <span data-ttu-id="b0883-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0883-174">0x00000010</span></span>                                   |
| <span data-ttu-id="b0883-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b0883-175">Classes used in</span></span>        | [<span data-ttu-id="b0883-176">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="b0883-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b0883-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b0883-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b0883-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="b0883-178">Entry</span></span> | <span data-ttu-id="b0883-179">Valor</span><span class="sxs-lookup"><span data-stu-id="b0883-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b0883-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="b0883-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0883-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0883-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0883-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0883-182">System-Only</span></span>            | <span data-ttu-id="b0883-183">Falso</span><span class="sxs-lookup"><span data-stu-id="b0883-183">False</span></span>                                        |
| <span data-ttu-id="b0883-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b0883-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b0883-185">True</span><span class="sxs-lookup"><span data-stu-id="b0883-185">True</span></span>                                         |
| <span data-ttu-id="b0883-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="b0883-186">Is Indexed</span></span>             | <span data-ttu-id="b0883-187">Falso</span><span class="sxs-lookup"><span data-stu-id="b0883-187">False</span></span>                                        |
| <span data-ttu-id="b0883-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b0883-188">In Global Catalog</span></span>      | <span data-ttu-id="b0883-189">Falso</span><span class="sxs-lookup"><span data-stu-id="b0883-189">False</span></span>                                        |
| <span data-ttu-id="b0883-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b0883-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0883-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b0883-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b0883-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0883-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b0883-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0883-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b0883-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0883-194">Search-Flags</span></span>           | <span data-ttu-id="b0883-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0883-195">0x00000000</span></span>                                   |
| <span data-ttu-id="b0883-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0883-196">System-Flags</span></span>           | <span data-ttu-id="b0883-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0883-197">0x00000010</span></span>                                   |
| <span data-ttu-id="b0883-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b0883-198">Classes used in</span></span>        | [<span data-ttu-id="b0883-199">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="b0883-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b0883-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0883-200">Windows Server 2008</span></span>



| <span data-ttu-id="b0883-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="b0883-201">Entry</span></span> | <span data-ttu-id="b0883-202">Valor</span><span class="sxs-lookup"><span data-stu-id="b0883-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b0883-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="b0883-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0883-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0883-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0883-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0883-205">System-Only</span></span>            | <span data-ttu-id="b0883-206">Falso</span><span class="sxs-lookup"><span data-stu-id="b0883-206">False</span></span>                                        |
| <span data-ttu-id="b0883-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b0883-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b0883-208">True</span><span class="sxs-lookup"><span data-stu-id="b0883-208">True</span></span>                                         |
| <span data-ttu-id="b0883-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="b0883-209">Is Indexed</span></span>             | <span data-ttu-id="b0883-210">Falso</span><span class="sxs-lookup"><span data-stu-id="b0883-210">False</span></span>                                        |
| <span data-ttu-id="b0883-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b0883-211">In Global Catalog</span></span>      | <span data-ttu-id="b0883-212">Falso</span><span class="sxs-lookup"><span data-stu-id="b0883-212">False</span></span>                                        |
| <span data-ttu-id="b0883-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b0883-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0883-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b0883-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b0883-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0883-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b0883-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0883-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b0883-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0883-217">Search-Flags</span></span>           | <span data-ttu-id="b0883-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0883-218">0x00000000</span></span>                                   |
| <span data-ttu-id="b0883-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0883-219">System-Flags</span></span>           | <span data-ttu-id="b0883-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0883-220">0x00000010</span></span>                                   |
| <span data-ttu-id="b0883-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b0883-221">Classes used in</span></span>        | [<span data-ttu-id="b0883-222">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="b0883-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b0883-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b0883-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b0883-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="b0883-224">Entry</span></span> | <span data-ttu-id="b0883-225">Valor</span><span class="sxs-lookup"><span data-stu-id="b0883-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b0883-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="b0883-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0883-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0883-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0883-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0883-228">System-Only</span></span>            | <span data-ttu-id="b0883-229">Falso</span><span class="sxs-lookup"><span data-stu-id="b0883-229">False</span></span>                                        |
| <span data-ttu-id="b0883-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b0883-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b0883-231">True</span><span class="sxs-lookup"><span data-stu-id="b0883-231">True</span></span>                                         |
| <span data-ttu-id="b0883-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="b0883-232">Is Indexed</span></span>             | <span data-ttu-id="b0883-233">Falso</span><span class="sxs-lookup"><span data-stu-id="b0883-233">False</span></span>                                        |
| <span data-ttu-id="b0883-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b0883-234">In Global Catalog</span></span>      | <span data-ttu-id="b0883-235">Falso</span><span class="sxs-lookup"><span data-stu-id="b0883-235">False</span></span>                                        |
| <span data-ttu-id="b0883-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b0883-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0883-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b0883-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b0883-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0883-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b0883-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0883-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b0883-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0883-240">Search-Flags</span></span>           | <span data-ttu-id="b0883-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0883-241">0x00000000</span></span>                                   |
| <span data-ttu-id="b0883-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0883-242">System-Flags</span></span>           | <span data-ttu-id="b0883-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0883-243">0x00000010</span></span>                                   |
| <span data-ttu-id="b0883-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b0883-244">Classes used in</span></span>        | [<span data-ttu-id="b0883-245">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="b0883-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b0883-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b0883-246">Windows Server 2012</span></span>



| <span data-ttu-id="b0883-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="b0883-247">Entry</span></span> | <span data-ttu-id="b0883-248">Valor</span><span class="sxs-lookup"><span data-stu-id="b0883-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b0883-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="b0883-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0883-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0883-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0883-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0883-251">System-Only</span></span>            | <span data-ttu-id="b0883-252">Falso</span><span class="sxs-lookup"><span data-stu-id="b0883-252">False</span></span>                                        |
| <span data-ttu-id="b0883-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b0883-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b0883-254">True</span><span class="sxs-lookup"><span data-stu-id="b0883-254">True</span></span>                                         |
| <span data-ttu-id="b0883-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="b0883-255">Is Indexed</span></span>             | <span data-ttu-id="b0883-256">Falso</span><span class="sxs-lookup"><span data-stu-id="b0883-256">False</span></span>                                        |
| <span data-ttu-id="b0883-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b0883-257">In Global Catalog</span></span>      | <span data-ttu-id="b0883-258">Falso</span><span class="sxs-lookup"><span data-stu-id="b0883-258">False</span></span>                                        |
| <span data-ttu-id="b0883-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b0883-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0883-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b0883-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b0883-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0883-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b0883-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0883-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b0883-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0883-263">Search-Flags</span></span>           | <span data-ttu-id="b0883-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0883-264">0x00000000</span></span>                                   |
| <span data-ttu-id="b0883-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0883-265">System-Flags</span></span>           | <span data-ttu-id="b0883-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0883-266">0x00000010</span></span>                                   |
| <span data-ttu-id="b0883-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b0883-267">Classes used in</span></span>        | [<span data-ttu-id="b0883-268">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="b0883-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





