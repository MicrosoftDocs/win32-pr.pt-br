---
title: ACS-atributo de latência mínima
description: O atributo ACS-Minimum-latência é somente para uso interno.
ms.assetid: ec2cca55-9e31-49da-98aa-aa2f6664ea90
ms.tgt_platform: multiple
keywords:
- ACS-esquema de AD de atributo de latência mínima
- Esquema de AD do atributo aCSMinimumLatency
topic_type:
- apiref
api_name:
- ACS-Minimum-Latency
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab7e9e6d5a9ccf626cdf8849ffe0e29504b4a0b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104009810"
---
# <a name="acs-minimum-latency-attribute"></a><span data-ttu-id="5bcce-105">ACS-atributo de latência mínima</span><span class="sxs-lookup"><span data-stu-id="5bcce-105">ACS-Minimum-Latency attribute</span></span>

<span data-ttu-id="5bcce-106">O atributo **ACS-Minimum-latência** é somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="5bcce-106">The **ACS-Minimum-Latency** attribute is for internal use only.</span></span> <span data-ttu-id="5bcce-107">Com base em RFC2210.</span><span class="sxs-lookup"><span data-stu-id="5bcce-107">Based on RFC2210.</span></span>



| <span data-ttu-id="5bcce-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="5bcce-108">Entry</span></span> | <span data-ttu-id="5bcce-109">Valor</span><span class="sxs-lookup"><span data-stu-id="5bcce-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5bcce-110">CN</span><span class="sxs-lookup"><span data-stu-id="5bcce-110">CN</span></span>                | <span data-ttu-id="5bcce-111">ACS – latência mínima</span><span class="sxs-lookup"><span data-stu-id="5bcce-111">ACS-Minimum-Latency</span></span>                  |
| <span data-ttu-id="5bcce-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5bcce-112">Ldap-Display-Name</span></span> | <span data-ttu-id="5bcce-113">aCSMinimumLatency</span><span class="sxs-lookup"><span data-stu-id="5bcce-113">aCSMinimumLatency</span></span>                    |
| <span data-ttu-id="5bcce-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="5bcce-114">Size</span></span>              | <span data-ttu-id="5bcce-115">8 bytes</span><span class="sxs-lookup"><span data-stu-id="5bcce-115">8 bytes</span></span>                              |
| <span data-ttu-id="5bcce-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="5bcce-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="5bcce-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="5bcce-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="5bcce-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5bcce-118">Attribute-Id</span></span>      | <span data-ttu-id="5bcce-119">1.2.840.113556.1.4.1316</span><span class="sxs-lookup"><span data-stu-id="5bcce-119">1.2.840.113556.1.4.1316</span></span>              |
| <span data-ttu-id="5bcce-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5bcce-120">System-Id-Guid</span></span>    | <span data-ttu-id="5bcce-121">9517fefb-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="5bcce-121">9517fefb-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="5bcce-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bcce-122">Syntax</span></span>            | [<span data-ttu-id="5bcce-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="5bcce-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="5bcce-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="5bcce-124">Implementations</span></span>

-   [<span data-ttu-id="5bcce-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5bcce-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5bcce-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5bcce-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5bcce-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5bcce-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5bcce-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5bcce-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5bcce-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5bcce-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5bcce-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5bcce-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5bcce-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5bcce-131">Windows 2000 Server</span></span>



| <span data-ttu-id="5bcce-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="5bcce-132">Entry</span></span> | <span data-ttu-id="5bcce-133">Valor</span><span class="sxs-lookup"><span data-stu-id="5bcce-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5bcce-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="5bcce-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5bcce-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5bcce-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5bcce-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="5bcce-136">System-Only</span></span>            | <span data-ttu-id="5bcce-137">Falso</span><span class="sxs-lookup"><span data-stu-id="5bcce-137">False</span></span>                                        |
| <span data-ttu-id="5bcce-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5bcce-138">Is-Single-Valued</span></span>       | <span data-ttu-id="5bcce-139">True</span><span class="sxs-lookup"><span data-stu-id="5bcce-139">True</span></span>                                         |
| <span data-ttu-id="5bcce-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="5bcce-140">Is Indexed</span></span>             | <span data-ttu-id="5bcce-141">Falso</span><span class="sxs-lookup"><span data-stu-id="5bcce-141">False</span></span>                                        |
| <span data-ttu-id="5bcce-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5bcce-142">In Global Catalog</span></span>      | <span data-ttu-id="5bcce-143">Falso</span><span class="sxs-lookup"><span data-stu-id="5bcce-143">False</span></span>                                        |
| <span data-ttu-id="5bcce-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5bcce-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="5bcce-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5bcce-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5bcce-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5bcce-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5bcce-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5bcce-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5bcce-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5bcce-148">Search-Flags</span></span>           | <span data-ttu-id="5bcce-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5bcce-149">0x00000000</span></span>                                   |
| <span data-ttu-id="5bcce-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5bcce-150">System-Flags</span></span>           | <span data-ttu-id="5bcce-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5bcce-151">0x00000010</span></span>                                   |
| <span data-ttu-id="5bcce-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5bcce-152">Classes used in</span></span>        | [<span data-ttu-id="5bcce-153">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="5bcce-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5bcce-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5bcce-154">Windows Server 2003</span></span>



| <span data-ttu-id="5bcce-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="5bcce-155">Entry</span></span> | <span data-ttu-id="5bcce-156">Valor</span><span class="sxs-lookup"><span data-stu-id="5bcce-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5bcce-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="5bcce-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5bcce-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5bcce-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5bcce-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5bcce-159">System-Only</span></span>            | <span data-ttu-id="5bcce-160">Falso</span><span class="sxs-lookup"><span data-stu-id="5bcce-160">False</span></span>                                        |
| <span data-ttu-id="5bcce-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5bcce-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5bcce-162">True</span><span class="sxs-lookup"><span data-stu-id="5bcce-162">True</span></span>                                         |
| <span data-ttu-id="5bcce-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="5bcce-163">Is Indexed</span></span>             | <span data-ttu-id="5bcce-164">Falso</span><span class="sxs-lookup"><span data-stu-id="5bcce-164">False</span></span>                                        |
| <span data-ttu-id="5bcce-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5bcce-165">In Global Catalog</span></span>      | <span data-ttu-id="5bcce-166">Falso</span><span class="sxs-lookup"><span data-stu-id="5bcce-166">False</span></span>                                        |
| <span data-ttu-id="5bcce-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5bcce-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5bcce-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5bcce-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5bcce-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5bcce-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5bcce-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5bcce-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5bcce-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5bcce-171">Search-Flags</span></span>           | <span data-ttu-id="5bcce-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5bcce-172">0x00000000</span></span>                                   |
| <span data-ttu-id="5bcce-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5bcce-173">System-Flags</span></span>           | <span data-ttu-id="5bcce-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5bcce-174">0x00000010</span></span>                                   |
| <span data-ttu-id="5bcce-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5bcce-175">Classes used in</span></span>        | [<span data-ttu-id="5bcce-176">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="5bcce-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5bcce-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5bcce-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5bcce-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="5bcce-178">Entry</span></span> | <span data-ttu-id="5bcce-179">Valor</span><span class="sxs-lookup"><span data-stu-id="5bcce-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5bcce-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="5bcce-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5bcce-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5bcce-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5bcce-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="5bcce-182">System-Only</span></span>            | <span data-ttu-id="5bcce-183">Falso</span><span class="sxs-lookup"><span data-stu-id="5bcce-183">False</span></span>                                        |
| <span data-ttu-id="5bcce-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5bcce-184">Is-Single-Valued</span></span>       | <span data-ttu-id="5bcce-185">True</span><span class="sxs-lookup"><span data-stu-id="5bcce-185">True</span></span>                                         |
| <span data-ttu-id="5bcce-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="5bcce-186">Is Indexed</span></span>             | <span data-ttu-id="5bcce-187">Falso</span><span class="sxs-lookup"><span data-stu-id="5bcce-187">False</span></span>                                        |
| <span data-ttu-id="5bcce-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5bcce-188">In Global Catalog</span></span>      | <span data-ttu-id="5bcce-189">Falso</span><span class="sxs-lookup"><span data-stu-id="5bcce-189">False</span></span>                                        |
| <span data-ttu-id="5bcce-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5bcce-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="5bcce-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5bcce-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5bcce-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5bcce-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5bcce-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5bcce-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5bcce-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5bcce-194">Search-Flags</span></span>           | <span data-ttu-id="5bcce-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5bcce-195">0x00000000</span></span>                                   |
| <span data-ttu-id="5bcce-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5bcce-196">System-Flags</span></span>           | <span data-ttu-id="5bcce-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5bcce-197">0x00000010</span></span>                                   |
| <span data-ttu-id="5bcce-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5bcce-198">Classes used in</span></span>        | [<span data-ttu-id="5bcce-199">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="5bcce-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5bcce-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5bcce-200">Windows Server 2008</span></span>



| <span data-ttu-id="5bcce-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="5bcce-201">Entry</span></span> | <span data-ttu-id="5bcce-202">Valor</span><span class="sxs-lookup"><span data-stu-id="5bcce-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5bcce-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="5bcce-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5bcce-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5bcce-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5bcce-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="5bcce-205">System-Only</span></span>            | <span data-ttu-id="5bcce-206">Falso</span><span class="sxs-lookup"><span data-stu-id="5bcce-206">False</span></span>                                        |
| <span data-ttu-id="5bcce-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5bcce-207">Is-Single-Valued</span></span>       | <span data-ttu-id="5bcce-208">True</span><span class="sxs-lookup"><span data-stu-id="5bcce-208">True</span></span>                                         |
| <span data-ttu-id="5bcce-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="5bcce-209">Is Indexed</span></span>             | <span data-ttu-id="5bcce-210">Falso</span><span class="sxs-lookup"><span data-stu-id="5bcce-210">False</span></span>                                        |
| <span data-ttu-id="5bcce-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5bcce-211">In Global Catalog</span></span>      | <span data-ttu-id="5bcce-212">Falso</span><span class="sxs-lookup"><span data-stu-id="5bcce-212">False</span></span>                                        |
| <span data-ttu-id="5bcce-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5bcce-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="5bcce-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5bcce-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5bcce-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5bcce-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5bcce-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5bcce-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5bcce-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5bcce-217">Search-Flags</span></span>           | <span data-ttu-id="5bcce-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5bcce-218">0x00000000</span></span>                                   |
| <span data-ttu-id="5bcce-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5bcce-219">System-Flags</span></span>           | <span data-ttu-id="5bcce-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5bcce-220">0x00000010</span></span>                                   |
| <span data-ttu-id="5bcce-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5bcce-221">Classes used in</span></span>        | [<span data-ttu-id="5bcce-222">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="5bcce-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5bcce-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5bcce-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5bcce-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="5bcce-224">Entry</span></span> | <span data-ttu-id="5bcce-225">Valor</span><span class="sxs-lookup"><span data-stu-id="5bcce-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5bcce-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="5bcce-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5bcce-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5bcce-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5bcce-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="5bcce-228">System-Only</span></span>            | <span data-ttu-id="5bcce-229">Falso</span><span class="sxs-lookup"><span data-stu-id="5bcce-229">False</span></span>                                        |
| <span data-ttu-id="5bcce-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5bcce-230">Is-Single-Valued</span></span>       | <span data-ttu-id="5bcce-231">True</span><span class="sxs-lookup"><span data-stu-id="5bcce-231">True</span></span>                                         |
| <span data-ttu-id="5bcce-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="5bcce-232">Is Indexed</span></span>             | <span data-ttu-id="5bcce-233">Falso</span><span class="sxs-lookup"><span data-stu-id="5bcce-233">False</span></span>                                        |
| <span data-ttu-id="5bcce-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5bcce-234">In Global Catalog</span></span>      | <span data-ttu-id="5bcce-235">Falso</span><span class="sxs-lookup"><span data-stu-id="5bcce-235">False</span></span>                                        |
| <span data-ttu-id="5bcce-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5bcce-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="5bcce-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5bcce-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5bcce-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5bcce-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5bcce-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5bcce-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5bcce-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5bcce-240">Search-Flags</span></span>           | <span data-ttu-id="5bcce-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5bcce-241">0x00000000</span></span>                                   |
| <span data-ttu-id="5bcce-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5bcce-242">System-Flags</span></span>           | <span data-ttu-id="5bcce-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5bcce-243">0x00000010</span></span>                                   |
| <span data-ttu-id="5bcce-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5bcce-244">Classes used in</span></span>        | [<span data-ttu-id="5bcce-245">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="5bcce-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5bcce-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5bcce-246">Windows Server 2012</span></span>



| <span data-ttu-id="5bcce-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="5bcce-247">Entry</span></span> | <span data-ttu-id="5bcce-248">Valor</span><span class="sxs-lookup"><span data-stu-id="5bcce-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5bcce-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="5bcce-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5bcce-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5bcce-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5bcce-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="5bcce-251">System-Only</span></span>            | <span data-ttu-id="5bcce-252">Falso</span><span class="sxs-lookup"><span data-stu-id="5bcce-252">False</span></span>                                        |
| <span data-ttu-id="5bcce-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5bcce-253">Is-Single-Valued</span></span>       | <span data-ttu-id="5bcce-254">True</span><span class="sxs-lookup"><span data-stu-id="5bcce-254">True</span></span>                                         |
| <span data-ttu-id="5bcce-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="5bcce-255">Is Indexed</span></span>             | <span data-ttu-id="5bcce-256">Falso</span><span class="sxs-lookup"><span data-stu-id="5bcce-256">False</span></span>                                        |
| <span data-ttu-id="5bcce-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5bcce-257">In Global Catalog</span></span>      | <span data-ttu-id="5bcce-258">Falso</span><span class="sxs-lookup"><span data-stu-id="5bcce-258">False</span></span>                                        |
| <span data-ttu-id="5bcce-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5bcce-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="5bcce-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5bcce-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5bcce-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5bcce-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5bcce-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5bcce-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5bcce-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5bcce-263">Search-Flags</span></span>           | <span data-ttu-id="5bcce-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5bcce-264">0x00000000</span></span>                                   |
| <span data-ttu-id="5bcce-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5bcce-265">System-Flags</span></span>           | <span data-ttu-id="5bcce-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5bcce-266">0x00000010</span></span>                                   |
| <span data-ttu-id="5bcce-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5bcce-267">Classes used in</span></span>        | [<span data-ttu-id="5bcce-268">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="5bcce-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





