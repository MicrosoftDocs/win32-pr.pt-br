---
title: ACS-atributo de variação de atraso mínimo
description: O atributo ACS-Minimum-Delay-Variance é somente para uso interno.
ms.assetid: eb82ac12-d570-4edc-bbfa-2de63d8f5088
ms.tgt_platform: multiple
keywords:
- ACS-esquema do AD do atributo de variação mínimo-atraso
- Esquema de AD do atributo aCSMinimumDelayVariation
topic_type:
- apiref
api_name:
- ACS-Minimum-Delay-Variation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d4f360e87bd2d9c36da1651800e5765a0a6f924
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104500108"
---
# <a name="acs-minimum-delay-variation-attribute"></a><span data-ttu-id="b9102-105">ACS-atributo de variação de atraso mínimo</span><span class="sxs-lookup"><span data-stu-id="b9102-105">ACS-Minimum-Delay-Variation attribute</span></span>

<span data-ttu-id="b9102-106">O atributo **ACS-Minimum-Delay-Variance** é somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="b9102-106">The **ACS-Minimum-Delay-Variation** attribute is for internal use only.</span></span> <span data-ttu-id="b9102-107">Com base em RFC2210.</span><span class="sxs-lookup"><span data-stu-id="b9102-107">Based on RFC2210.</span></span>



| <span data-ttu-id="b9102-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="b9102-108">Entry</span></span> | <span data-ttu-id="b9102-109">Valor</span><span class="sxs-lookup"><span data-stu-id="b9102-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b9102-110">CN</span><span class="sxs-lookup"><span data-stu-id="b9102-110">CN</span></span>                | <span data-ttu-id="b9102-111">ACS-mínimo-variação de atraso</span><span class="sxs-lookup"><span data-stu-id="b9102-111">ACS-Minimum-Delay-Variation</span></span>          |
| <span data-ttu-id="b9102-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b9102-112">Ldap-Display-Name</span></span> | <span data-ttu-id="b9102-113">aCSMinimumDelayVariation</span><span class="sxs-lookup"><span data-stu-id="b9102-113">aCSMinimumDelayVariation</span></span>             |
| <span data-ttu-id="b9102-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b9102-114">Size</span></span>              | <span data-ttu-id="b9102-115">8 bytes</span><span class="sxs-lookup"><span data-stu-id="b9102-115">8 bytes</span></span>                              |
| <span data-ttu-id="b9102-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="b9102-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="b9102-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="b9102-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b9102-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b9102-118">Attribute-Id</span></span>      | <span data-ttu-id="b9102-119">1.2.840.113556.1.4.1317</span><span class="sxs-lookup"><span data-stu-id="b9102-119">1.2.840.113556.1.4.1317</span></span>              |
| <span data-ttu-id="b9102-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b9102-120">System-Id-Guid</span></span>    | <span data-ttu-id="b9102-121">9c65329b-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="b9102-121">9c65329b-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="b9102-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9102-122">Syntax</span></span>            | [<span data-ttu-id="b9102-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="b9102-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="b9102-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="b9102-124">Implementations</span></span>

-   [<span data-ttu-id="b9102-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b9102-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b9102-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b9102-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b9102-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b9102-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b9102-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b9102-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b9102-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b9102-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b9102-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b9102-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b9102-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b9102-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b9102-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="b9102-132">Entry</span></span> | <span data-ttu-id="b9102-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b9102-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b9102-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="b9102-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b9102-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9102-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b9102-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9102-136">System-Only</span></span>            | <span data-ttu-id="b9102-137">Falso</span><span class="sxs-lookup"><span data-stu-id="b9102-137">False</span></span>                                        |
| <span data-ttu-id="b9102-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b9102-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b9102-139">True</span><span class="sxs-lookup"><span data-stu-id="b9102-139">True</span></span>                                         |
| <span data-ttu-id="b9102-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="b9102-140">Is Indexed</span></span>             | <span data-ttu-id="b9102-141">Falso</span><span class="sxs-lookup"><span data-stu-id="b9102-141">False</span></span>                                        |
| <span data-ttu-id="b9102-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b9102-142">In Global Catalog</span></span>      | <span data-ttu-id="b9102-143">Falso</span><span class="sxs-lookup"><span data-stu-id="b9102-143">False</span></span>                                        |
| <span data-ttu-id="b9102-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b9102-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9102-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b9102-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b9102-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9102-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b9102-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9102-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b9102-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9102-148">Search-Flags</span></span>           | <span data-ttu-id="b9102-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9102-149">0x00000000</span></span>                                   |
| <span data-ttu-id="b9102-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9102-150">System-Flags</span></span>           | <span data-ttu-id="b9102-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9102-151">0x00000010</span></span>                                   |
| <span data-ttu-id="b9102-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b9102-152">Classes used in</span></span>        | [<span data-ttu-id="b9102-153">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="b9102-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b9102-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b9102-154">Windows Server 2003</span></span>



| <span data-ttu-id="b9102-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="b9102-155">Entry</span></span> | <span data-ttu-id="b9102-156">Valor</span><span class="sxs-lookup"><span data-stu-id="b9102-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b9102-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="b9102-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b9102-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9102-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b9102-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9102-159">System-Only</span></span>            | <span data-ttu-id="b9102-160">Falso</span><span class="sxs-lookup"><span data-stu-id="b9102-160">False</span></span>                                        |
| <span data-ttu-id="b9102-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b9102-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b9102-162">True</span><span class="sxs-lookup"><span data-stu-id="b9102-162">True</span></span>                                         |
| <span data-ttu-id="b9102-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="b9102-163">Is Indexed</span></span>             | <span data-ttu-id="b9102-164">Falso</span><span class="sxs-lookup"><span data-stu-id="b9102-164">False</span></span>                                        |
| <span data-ttu-id="b9102-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b9102-165">In Global Catalog</span></span>      | <span data-ttu-id="b9102-166">Falso</span><span class="sxs-lookup"><span data-stu-id="b9102-166">False</span></span>                                        |
| <span data-ttu-id="b9102-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b9102-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9102-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b9102-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b9102-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9102-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b9102-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9102-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b9102-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9102-171">Search-Flags</span></span>           | <span data-ttu-id="b9102-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9102-172">0x00000000</span></span>                                   |
| <span data-ttu-id="b9102-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9102-173">System-Flags</span></span>           | <span data-ttu-id="b9102-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9102-174">0x00000010</span></span>                                   |
| <span data-ttu-id="b9102-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b9102-175">Classes used in</span></span>        | [<span data-ttu-id="b9102-176">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="b9102-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b9102-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b9102-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b9102-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="b9102-178">Entry</span></span> | <span data-ttu-id="b9102-179">Valor</span><span class="sxs-lookup"><span data-stu-id="b9102-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b9102-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="b9102-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b9102-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9102-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b9102-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9102-182">System-Only</span></span>            | <span data-ttu-id="b9102-183">Falso</span><span class="sxs-lookup"><span data-stu-id="b9102-183">False</span></span>                                        |
| <span data-ttu-id="b9102-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b9102-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b9102-185">True</span><span class="sxs-lookup"><span data-stu-id="b9102-185">True</span></span>                                         |
| <span data-ttu-id="b9102-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="b9102-186">Is Indexed</span></span>             | <span data-ttu-id="b9102-187">Falso</span><span class="sxs-lookup"><span data-stu-id="b9102-187">False</span></span>                                        |
| <span data-ttu-id="b9102-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b9102-188">In Global Catalog</span></span>      | <span data-ttu-id="b9102-189">Falso</span><span class="sxs-lookup"><span data-stu-id="b9102-189">False</span></span>                                        |
| <span data-ttu-id="b9102-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b9102-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9102-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b9102-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b9102-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9102-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b9102-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9102-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b9102-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9102-194">Search-Flags</span></span>           | <span data-ttu-id="b9102-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9102-195">0x00000000</span></span>                                   |
| <span data-ttu-id="b9102-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9102-196">System-Flags</span></span>           | <span data-ttu-id="b9102-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9102-197">0x00000010</span></span>                                   |
| <span data-ttu-id="b9102-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b9102-198">Classes used in</span></span>        | [<span data-ttu-id="b9102-199">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="b9102-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b9102-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9102-200">Windows Server 2008</span></span>



| <span data-ttu-id="b9102-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="b9102-201">Entry</span></span> | <span data-ttu-id="b9102-202">Valor</span><span class="sxs-lookup"><span data-stu-id="b9102-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b9102-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="b9102-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b9102-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9102-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b9102-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9102-205">System-Only</span></span>            | <span data-ttu-id="b9102-206">Falso</span><span class="sxs-lookup"><span data-stu-id="b9102-206">False</span></span>                                        |
| <span data-ttu-id="b9102-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b9102-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b9102-208">True</span><span class="sxs-lookup"><span data-stu-id="b9102-208">True</span></span>                                         |
| <span data-ttu-id="b9102-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="b9102-209">Is Indexed</span></span>             | <span data-ttu-id="b9102-210">Falso</span><span class="sxs-lookup"><span data-stu-id="b9102-210">False</span></span>                                        |
| <span data-ttu-id="b9102-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b9102-211">In Global Catalog</span></span>      | <span data-ttu-id="b9102-212">Falso</span><span class="sxs-lookup"><span data-stu-id="b9102-212">False</span></span>                                        |
| <span data-ttu-id="b9102-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b9102-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9102-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b9102-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b9102-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9102-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b9102-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9102-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b9102-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9102-217">Search-Flags</span></span>           | <span data-ttu-id="b9102-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9102-218">0x00000000</span></span>                                   |
| <span data-ttu-id="b9102-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9102-219">System-Flags</span></span>           | <span data-ttu-id="b9102-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9102-220">0x00000010</span></span>                                   |
| <span data-ttu-id="b9102-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b9102-221">Classes used in</span></span>        | [<span data-ttu-id="b9102-222">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="b9102-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b9102-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b9102-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b9102-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="b9102-224">Entry</span></span> | <span data-ttu-id="b9102-225">Valor</span><span class="sxs-lookup"><span data-stu-id="b9102-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b9102-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="b9102-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b9102-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9102-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b9102-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9102-228">System-Only</span></span>            | <span data-ttu-id="b9102-229">Falso</span><span class="sxs-lookup"><span data-stu-id="b9102-229">False</span></span>                                        |
| <span data-ttu-id="b9102-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b9102-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b9102-231">True</span><span class="sxs-lookup"><span data-stu-id="b9102-231">True</span></span>                                         |
| <span data-ttu-id="b9102-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="b9102-232">Is Indexed</span></span>             | <span data-ttu-id="b9102-233">Falso</span><span class="sxs-lookup"><span data-stu-id="b9102-233">False</span></span>                                        |
| <span data-ttu-id="b9102-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b9102-234">In Global Catalog</span></span>      | <span data-ttu-id="b9102-235">Falso</span><span class="sxs-lookup"><span data-stu-id="b9102-235">False</span></span>                                        |
| <span data-ttu-id="b9102-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b9102-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9102-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b9102-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b9102-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9102-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b9102-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9102-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b9102-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9102-240">Search-Flags</span></span>           | <span data-ttu-id="b9102-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9102-241">0x00000000</span></span>                                   |
| <span data-ttu-id="b9102-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9102-242">System-Flags</span></span>           | <span data-ttu-id="b9102-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9102-243">0x00000010</span></span>                                   |
| <span data-ttu-id="b9102-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b9102-244">Classes used in</span></span>        | [<span data-ttu-id="b9102-245">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="b9102-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b9102-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b9102-246">Windows Server 2012</span></span>



| <span data-ttu-id="b9102-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="b9102-247">Entry</span></span> | <span data-ttu-id="b9102-248">Valor</span><span class="sxs-lookup"><span data-stu-id="b9102-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b9102-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="b9102-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b9102-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9102-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b9102-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9102-251">System-Only</span></span>            | <span data-ttu-id="b9102-252">Falso</span><span class="sxs-lookup"><span data-stu-id="b9102-252">False</span></span>                                        |
| <span data-ttu-id="b9102-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b9102-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b9102-254">True</span><span class="sxs-lookup"><span data-stu-id="b9102-254">True</span></span>                                         |
| <span data-ttu-id="b9102-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="b9102-255">Is Indexed</span></span>             | <span data-ttu-id="b9102-256">Falso</span><span class="sxs-lookup"><span data-stu-id="b9102-256">False</span></span>                                        |
| <span data-ttu-id="b9102-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b9102-257">In Global Catalog</span></span>      | <span data-ttu-id="b9102-258">Falso</span><span class="sxs-lookup"><span data-stu-id="b9102-258">False</span></span>                                        |
| <span data-ttu-id="b9102-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b9102-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9102-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b9102-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b9102-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9102-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b9102-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9102-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b9102-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9102-263">Search-Flags</span></span>           | <span data-ttu-id="b9102-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9102-264">0x00000000</span></span>                                   |
| <span data-ttu-id="b9102-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9102-265">System-Flags</span></span>           | <span data-ttu-id="b9102-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9102-266">0x00000010</span></span>                                   |
| <span data-ttu-id="b9102-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b9102-267">Classes used in</span></span>        | [<span data-ttu-id="b9102-268">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="b9102-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





