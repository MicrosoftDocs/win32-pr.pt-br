---
title: ACS-atributo de tamanho mínimo-policiado
description: O atributo ACS-tamanho mínimo-policiado é somente para uso interno.
ms.assetid: 27b4273a-a625-430b-baa0-a6037e2aac1e
ms.tgt_platform: multiple
keywords:
- ACS-esquema do AD do atributo de tamanho mínimo-policiado
- Esquema de AD do atributo aCSMinimumPolicedSize
topic_type:
- apiref
api_name:
- ACS-Minimum-Policed-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3de4bb2b33a45ab7d10bad72ba286d1695b980a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105754849"
---
# <a name="acs-minimum-policed-size-attribute"></a><span data-ttu-id="8007c-105">ACS-atributo de tamanho mínimo-policiado</span><span class="sxs-lookup"><span data-stu-id="8007c-105">ACS-Minimum-Policed-Size attribute</span></span>

<span data-ttu-id="8007c-106">O atributo **ACS-tamanho mínimo-policiado** é somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="8007c-106">The **ACS-Minimum-Policed-Size** attribute is for internal use only.</span></span> <span data-ttu-id="8007c-107">Com base em RFC2210.</span><span class="sxs-lookup"><span data-stu-id="8007c-107">Based on RFC2210.</span></span>



| <span data-ttu-id="8007c-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="8007c-108">Entry</span></span> | <span data-ttu-id="8007c-109">Valor</span><span class="sxs-lookup"><span data-stu-id="8007c-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8007c-110">CN</span><span class="sxs-lookup"><span data-stu-id="8007c-110">CN</span></span>                | <span data-ttu-id="8007c-111">ACS-tamanho mínimo-policiado</span><span class="sxs-lookup"><span data-stu-id="8007c-111">ACS-Minimum-Policed-Size</span></span>             |
| <span data-ttu-id="8007c-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8007c-112">Ldap-Display-Name</span></span> | <span data-ttu-id="8007c-113">aCSMinimumPolicedSize</span><span class="sxs-lookup"><span data-stu-id="8007c-113">aCSMinimumPolicedSize</span></span>                |
| <span data-ttu-id="8007c-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="8007c-114">Size</span></span>              | <span data-ttu-id="8007c-115">8 bytes</span><span class="sxs-lookup"><span data-stu-id="8007c-115">8 bytes</span></span>                              |
| <span data-ttu-id="8007c-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="8007c-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="8007c-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="8007c-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8007c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8007c-118">Attribute-Id</span></span>      | <span data-ttu-id="8007c-119">1.2.840.113556.1.4.1315</span><span class="sxs-lookup"><span data-stu-id="8007c-119">1.2.840.113556.1.4.1315</span></span>              |
| <span data-ttu-id="8007c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8007c-120">System-Id-Guid</span></span>    | <span data-ttu-id="8007c-121">8d0e7195-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="8007c-121">8d0e7195-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="8007c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="8007c-122">Syntax</span></span>            | [<span data-ttu-id="8007c-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="8007c-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="8007c-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="8007c-124">Implementations</span></span>

-   [<span data-ttu-id="8007c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8007c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8007c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8007c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8007c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8007c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8007c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8007c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8007c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8007c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8007c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8007c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8007c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8007c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="8007c-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="8007c-132">Entry</span></span> | <span data-ttu-id="8007c-133">Valor</span><span class="sxs-lookup"><span data-stu-id="8007c-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8007c-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="8007c-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8007c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8007c-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8007c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8007c-136">System-Only</span></span>            | <span data-ttu-id="8007c-137">Falso</span><span class="sxs-lookup"><span data-stu-id="8007c-137">False</span></span>                                        |
| <span data-ttu-id="8007c-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8007c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8007c-139">True</span><span class="sxs-lookup"><span data-stu-id="8007c-139">True</span></span>                                         |
| <span data-ttu-id="8007c-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="8007c-140">Is Indexed</span></span>             | <span data-ttu-id="8007c-141">Falso</span><span class="sxs-lookup"><span data-stu-id="8007c-141">False</span></span>                                        |
| <span data-ttu-id="8007c-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8007c-142">In Global Catalog</span></span>      | <span data-ttu-id="8007c-143">Falso</span><span class="sxs-lookup"><span data-stu-id="8007c-143">False</span></span>                                        |
| <span data-ttu-id="8007c-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8007c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8007c-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8007c-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8007c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8007c-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8007c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8007c-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8007c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8007c-148">Search-Flags</span></span>           | <span data-ttu-id="8007c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8007c-149">0x00000000</span></span>                                   |
| <span data-ttu-id="8007c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8007c-150">System-Flags</span></span>           | <span data-ttu-id="8007c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8007c-151">0x00000010</span></span>                                   |
| <span data-ttu-id="8007c-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8007c-152">Classes used in</span></span>        | [<span data-ttu-id="8007c-153">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="8007c-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8007c-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8007c-154">Windows Server 2003</span></span>



| <span data-ttu-id="8007c-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="8007c-155">Entry</span></span> | <span data-ttu-id="8007c-156">Valor</span><span class="sxs-lookup"><span data-stu-id="8007c-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8007c-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="8007c-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8007c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8007c-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8007c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="8007c-159">System-Only</span></span>            | <span data-ttu-id="8007c-160">Falso</span><span class="sxs-lookup"><span data-stu-id="8007c-160">False</span></span>                                        |
| <span data-ttu-id="8007c-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8007c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="8007c-162">True</span><span class="sxs-lookup"><span data-stu-id="8007c-162">True</span></span>                                         |
| <span data-ttu-id="8007c-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="8007c-163">Is Indexed</span></span>             | <span data-ttu-id="8007c-164">Falso</span><span class="sxs-lookup"><span data-stu-id="8007c-164">False</span></span>                                        |
| <span data-ttu-id="8007c-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8007c-165">In Global Catalog</span></span>      | <span data-ttu-id="8007c-166">Falso</span><span class="sxs-lookup"><span data-stu-id="8007c-166">False</span></span>                                        |
| <span data-ttu-id="8007c-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8007c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="8007c-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8007c-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8007c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8007c-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8007c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8007c-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8007c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8007c-171">Search-Flags</span></span>           | <span data-ttu-id="8007c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8007c-172">0x00000000</span></span>                                   |
| <span data-ttu-id="8007c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8007c-173">System-Flags</span></span>           | <span data-ttu-id="8007c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8007c-174">0x00000010</span></span>                                   |
| <span data-ttu-id="8007c-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8007c-175">Classes used in</span></span>        | [<span data-ttu-id="8007c-176">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="8007c-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8007c-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8007c-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8007c-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="8007c-178">Entry</span></span> | <span data-ttu-id="8007c-179">Valor</span><span class="sxs-lookup"><span data-stu-id="8007c-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8007c-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="8007c-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8007c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8007c-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8007c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="8007c-182">System-Only</span></span>            | <span data-ttu-id="8007c-183">Falso</span><span class="sxs-lookup"><span data-stu-id="8007c-183">False</span></span>                                        |
| <span data-ttu-id="8007c-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8007c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="8007c-185">True</span><span class="sxs-lookup"><span data-stu-id="8007c-185">True</span></span>                                         |
| <span data-ttu-id="8007c-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="8007c-186">Is Indexed</span></span>             | <span data-ttu-id="8007c-187">Falso</span><span class="sxs-lookup"><span data-stu-id="8007c-187">False</span></span>                                        |
| <span data-ttu-id="8007c-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8007c-188">In Global Catalog</span></span>      | <span data-ttu-id="8007c-189">Falso</span><span class="sxs-lookup"><span data-stu-id="8007c-189">False</span></span>                                        |
| <span data-ttu-id="8007c-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8007c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="8007c-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8007c-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8007c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8007c-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8007c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8007c-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8007c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8007c-194">Search-Flags</span></span>           | <span data-ttu-id="8007c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8007c-195">0x00000000</span></span>                                   |
| <span data-ttu-id="8007c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8007c-196">System-Flags</span></span>           | <span data-ttu-id="8007c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8007c-197">0x00000010</span></span>                                   |
| <span data-ttu-id="8007c-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8007c-198">Classes used in</span></span>        | [<span data-ttu-id="8007c-199">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="8007c-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8007c-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8007c-200">Windows Server 2008</span></span>



| <span data-ttu-id="8007c-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="8007c-201">Entry</span></span> | <span data-ttu-id="8007c-202">Valor</span><span class="sxs-lookup"><span data-stu-id="8007c-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8007c-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="8007c-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8007c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8007c-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8007c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="8007c-205">System-Only</span></span>            | <span data-ttu-id="8007c-206">Falso</span><span class="sxs-lookup"><span data-stu-id="8007c-206">False</span></span>                                        |
| <span data-ttu-id="8007c-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8007c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="8007c-208">True</span><span class="sxs-lookup"><span data-stu-id="8007c-208">True</span></span>                                         |
| <span data-ttu-id="8007c-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="8007c-209">Is Indexed</span></span>             | <span data-ttu-id="8007c-210">Falso</span><span class="sxs-lookup"><span data-stu-id="8007c-210">False</span></span>                                        |
| <span data-ttu-id="8007c-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8007c-211">In Global Catalog</span></span>      | <span data-ttu-id="8007c-212">Falso</span><span class="sxs-lookup"><span data-stu-id="8007c-212">False</span></span>                                        |
| <span data-ttu-id="8007c-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8007c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="8007c-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8007c-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8007c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8007c-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8007c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8007c-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8007c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8007c-217">Search-Flags</span></span>           | <span data-ttu-id="8007c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8007c-218">0x00000000</span></span>                                   |
| <span data-ttu-id="8007c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8007c-219">System-Flags</span></span>           | <span data-ttu-id="8007c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8007c-220">0x00000010</span></span>                                   |
| <span data-ttu-id="8007c-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8007c-221">Classes used in</span></span>        | [<span data-ttu-id="8007c-222">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="8007c-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8007c-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8007c-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8007c-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="8007c-224">Entry</span></span> | <span data-ttu-id="8007c-225">Valor</span><span class="sxs-lookup"><span data-stu-id="8007c-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8007c-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="8007c-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8007c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8007c-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8007c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="8007c-228">System-Only</span></span>            | <span data-ttu-id="8007c-229">Falso</span><span class="sxs-lookup"><span data-stu-id="8007c-229">False</span></span>                                        |
| <span data-ttu-id="8007c-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8007c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="8007c-231">True</span><span class="sxs-lookup"><span data-stu-id="8007c-231">True</span></span>                                         |
| <span data-ttu-id="8007c-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="8007c-232">Is Indexed</span></span>             | <span data-ttu-id="8007c-233">Falso</span><span class="sxs-lookup"><span data-stu-id="8007c-233">False</span></span>                                        |
| <span data-ttu-id="8007c-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8007c-234">In Global Catalog</span></span>      | <span data-ttu-id="8007c-235">Falso</span><span class="sxs-lookup"><span data-stu-id="8007c-235">False</span></span>                                        |
| <span data-ttu-id="8007c-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8007c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="8007c-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8007c-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8007c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8007c-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8007c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8007c-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8007c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8007c-240">Search-Flags</span></span>           | <span data-ttu-id="8007c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8007c-241">0x00000000</span></span>                                   |
| <span data-ttu-id="8007c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8007c-242">System-Flags</span></span>           | <span data-ttu-id="8007c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8007c-243">0x00000010</span></span>                                   |
| <span data-ttu-id="8007c-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8007c-244">Classes used in</span></span>        | [<span data-ttu-id="8007c-245">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="8007c-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8007c-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8007c-246">Windows Server 2012</span></span>



| <span data-ttu-id="8007c-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="8007c-247">Entry</span></span> | <span data-ttu-id="8007c-248">Valor</span><span class="sxs-lookup"><span data-stu-id="8007c-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8007c-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="8007c-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8007c-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8007c-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8007c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="8007c-251">System-Only</span></span>            | <span data-ttu-id="8007c-252">Falso</span><span class="sxs-lookup"><span data-stu-id="8007c-252">False</span></span>                                        |
| <span data-ttu-id="8007c-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8007c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="8007c-254">True</span><span class="sxs-lookup"><span data-stu-id="8007c-254">True</span></span>                                         |
| <span data-ttu-id="8007c-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="8007c-255">Is Indexed</span></span>             | <span data-ttu-id="8007c-256">Falso</span><span class="sxs-lookup"><span data-stu-id="8007c-256">False</span></span>                                        |
| <span data-ttu-id="8007c-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8007c-257">In Global Catalog</span></span>      | <span data-ttu-id="8007c-258">Falso</span><span class="sxs-lookup"><span data-stu-id="8007c-258">False</span></span>                                        |
| <span data-ttu-id="8007c-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8007c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="8007c-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8007c-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8007c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8007c-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8007c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8007c-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8007c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8007c-263">Search-Flags</span></span>           | <span data-ttu-id="8007c-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8007c-264">0x00000000</span></span>                                   |
| <span data-ttu-id="8007c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8007c-265">System-Flags</span></span>           | <span data-ttu-id="8007c-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8007c-266">0x00000010</span></span>                                   |
| <span data-ttu-id="8007c-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8007c-267">Classes used in</span></span>        | [<span data-ttu-id="8007c-268">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="8007c-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





