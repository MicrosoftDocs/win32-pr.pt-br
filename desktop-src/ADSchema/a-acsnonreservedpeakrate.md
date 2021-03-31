---
title: ACS-não reservado-atributo de taxa de pico
description: O atributo ACS-non-Reservative-rate é somente para uso interno.
ms.assetid: 4080839c-d99e-4527-8c81-6d23ab0d3d70
ms.tgt_platform: multiple
keywords:
- ACS-não reservado-esquema de AD de atributo de taxa de pico
- Esquema de AD do atributo aCSNonReservedPeakRate
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Peak-Rate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea3d2075e90648388a9a1277dbbe768a3fc616f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086771"
---
# <a name="acs-non-reserved-peak-rate-attribute"></a><span data-ttu-id="72e82-105">ACS-não reservado-atributo de taxa de pico</span><span class="sxs-lookup"><span data-stu-id="72e82-105">ACS-Non-Reserved-Peak-Rate attribute</span></span>

<span data-ttu-id="72e82-106">O atributo **ACS-non-reservative-Rate** é somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="72e82-106">The **ACS-Non-Reserved-Peak-Rate** attribute is for internal use only.</span></span> <span data-ttu-id="72e82-107">Com base em RFC2814.</span><span class="sxs-lookup"><span data-stu-id="72e82-107">Based on RFC2814.</span></span>



| <span data-ttu-id="72e82-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="72e82-108">Entry</span></span> | <span data-ttu-id="72e82-109">Valor</span><span class="sxs-lookup"><span data-stu-id="72e82-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="72e82-110">CN</span><span class="sxs-lookup"><span data-stu-id="72e82-110">CN</span></span>                | <span data-ttu-id="72e82-111">ACS-não reservado-taxa de pico</span><span class="sxs-lookup"><span data-stu-id="72e82-111">ACS-Non-Reserved-Peak-Rate</span></span>           |
| <span data-ttu-id="72e82-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="72e82-112">Ldap-Display-Name</span></span> | <span data-ttu-id="72e82-113">aCSNonReservedPeakRate</span><span class="sxs-lookup"><span data-stu-id="72e82-113">aCSNonReservedPeakRate</span></span>               |
| <span data-ttu-id="72e82-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="72e82-114">Size</span></span>              | <span data-ttu-id="72e82-115">8 bytes</span><span class="sxs-lookup"><span data-stu-id="72e82-115">8 bytes</span></span>                              |
| <span data-ttu-id="72e82-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="72e82-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="72e82-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="72e82-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="72e82-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="72e82-118">Attribute-Id</span></span>      | <span data-ttu-id="72e82-119">1.2.840.113556.1.4.1318</span><span class="sxs-lookup"><span data-stu-id="72e82-119">1.2.840.113556.1.4.1318</span></span>              |
| <span data-ttu-id="72e82-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="72e82-120">System-Id-Guid</span></span>    | <span data-ttu-id="72e82-121">a331a73f-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="72e82-121">a331a73f-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="72e82-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="72e82-122">Syntax</span></span>            | [<span data-ttu-id="72e82-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="72e82-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="72e82-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="72e82-124">Implementations</span></span>

-   [<span data-ttu-id="72e82-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="72e82-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="72e82-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="72e82-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="72e82-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="72e82-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="72e82-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="72e82-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="72e82-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="72e82-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="72e82-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="72e82-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="72e82-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="72e82-131">Windows 2000 Server</span></span>



| <span data-ttu-id="72e82-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="72e82-132">Entry</span></span> | <span data-ttu-id="72e82-133">Valor</span><span class="sxs-lookup"><span data-stu-id="72e82-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="72e82-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="72e82-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="72e82-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e82-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="72e82-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e82-136">System-Only</span></span>            | <span data-ttu-id="72e82-137">Falso</span><span class="sxs-lookup"><span data-stu-id="72e82-137">False</span></span>                                        |
| <span data-ttu-id="72e82-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72e82-138">Is-Single-Valued</span></span>       | <span data-ttu-id="72e82-139">True</span><span class="sxs-lookup"><span data-stu-id="72e82-139">True</span></span>                                         |
| <span data-ttu-id="72e82-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="72e82-140">Is Indexed</span></span>             | <span data-ttu-id="72e82-141">Falso</span><span class="sxs-lookup"><span data-stu-id="72e82-141">False</span></span>                                        |
| <span data-ttu-id="72e82-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72e82-142">In Global Catalog</span></span>      | <span data-ttu-id="72e82-143">Falso</span><span class="sxs-lookup"><span data-stu-id="72e82-143">False</span></span>                                        |
| <span data-ttu-id="72e82-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72e82-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e82-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72e82-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="72e82-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e82-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="72e82-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e82-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="72e82-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e82-148">Search-Flags</span></span>           | <span data-ttu-id="72e82-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72e82-149">0x00000000</span></span>                                   |
| <span data-ttu-id="72e82-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e82-150">System-Flags</span></span>           | <span data-ttu-id="72e82-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72e82-151">0x00000010</span></span>                                   |
| <span data-ttu-id="72e82-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72e82-152">Classes used in</span></span>        | [<span data-ttu-id="72e82-153">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="72e82-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="72e82-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="72e82-154">Windows Server 2003</span></span>



| <span data-ttu-id="72e82-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="72e82-155">Entry</span></span> | <span data-ttu-id="72e82-156">Valor</span><span class="sxs-lookup"><span data-stu-id="72e82-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="72e82-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="72e82-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="72e82-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e82-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="72e82-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e82-159">System-Only</span></span>            | <span data-ttu-id="72e82-160">Falso</span><span class="sxs-lookup"><span data-stu-id="72e82-160">False</span></span>                                        |
| <span data-ttu-id="72e82-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72e82-161">Is-Single-Valued</span></span>       | <span data-ttu-id="72e82-162">True</span><span class="sxs-lookup"><span data-stu-id="72e82-162">True</span></span>                                         |
| <span data-ttu-id="72e82-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="72e82-163">Is Indexed</span></span>             | <span data-ttu-id="72e82-164">Falso</span><span class="sxs-lookup"><span data-stu-id="72e82-164">False</span></span>                                        |
| <span data-ttu-id="72e82-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72e82-165">In Global Catalog</span></span>      | <span data-ttu-id="72e82-166">Falso</span><span class="sxs-lookup"><span data-stu-id="72e82-166">False</span></span>                                        |
| <span data-ttu-id="72e82-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72e82-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e82-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72e82-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="72e82-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e82-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="72e82-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e82-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="72e82-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e82-171">Search-Flags</span></span>           | <span data-ttu-id="72e82-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72e82-172">0x00000000</span></span>                                   |
| <span data-ttu-id="72e82-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e82-173">System-Flags</span></span>           | <span data-ttu-id="72e82-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72e82-174">0x00000010</span></span>                                   |
| <span data-ttu-id="72e82-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72e82-175">Classes used in</span></span>        | [<span data-ttu-id="72e82-176">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="72e82-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="72e82-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="72e82-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="72e82-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="72e82-178">Entry</span></span> | <span data-ttu-id="72e82-179">Valor</span><span class="sxs-lookup"><span data-stu-id="72e82-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="72e82-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="72e82-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="72e82-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e82-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="72e82-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e82-182">System-Only</span></span>            | <span data-ttu-id="72e82-183">Falso</span><span class="sxs-lookup"><span data-stu-id="72e82-183">False</span></span>                                        |
| <span data-ttu-id="72e82-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72e82-184">Is-Single-Valued</span></span>       | <span data-ttu-id="72e82-185">True</span><span class="sxs-lookup"><span data-stu-id="72e82-185">True</span></span>                                         |
| <span data-ttu-id="72e82-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="72e82-186">Is Indexed</span></span>             | <span data-ttu-id="72e82-187">Falso</span><span class="sxs-lookup"><span data-stu-id="72e82-187">False</span></span>                                        |
| <span data-ttu-id="72e82-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72e82-188">In Global Catalog</span></span>      | <span data-ttu-id="72e82-189">Falso</span><span class="sxs-lookup"><span data-stu-id="72e82-189">False</span></span>                                        |
| <span data-ttu-id="72e82-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72e82-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e82-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72e82-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="72e82-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e82-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="72e82-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e82-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="72e82-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e82-194">Search-Flags</span></span>           | <span data-ttu-id="72e82-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72e82-195">0x00000000</span></span>                                   |
| <span data-ttu-id="72e82-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e82-196">System-Flags</span></span>           | <span data-ttu-id="72e82-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72e82-197">0x00000010</span></span>                                   |
| <span data-ttu-id="72e82-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72e82-198">Classes used in</span></span>        | [<span data-ttu-id="72e82-199">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="72e82-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="72e82-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72e82-200">Windows Server 2008</span></span>



| <span data-ttu-id="72e82-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="72e82-201">Entry</span></span> | <span data-ttu-id="72e82-202">Valor</span><span class="sxs-lookup"><span data-stu-id="72e82-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="72e82-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="72e82-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="72e82-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e82-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="72e82-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e82-205">System-Only</span></span>            | <span data-ttu-id="72e82-206">Falso</span><span class="sxs-lookup"><span data-stu-id="72e82-206">False</span></span>                                        |
| <span data-ttu-id="72e82-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72e82-207">Is-Single-Valued</span></span>       | <span data-ttu-id="72e82-208">True</span><span class="sxs-lookup"><span data-stu-id="72e82-208">True</span></span>                                         |
| <span data-ttu-id="72e82-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="72e82-209">Is Indexed</span></span>             | <span data-ttu-id="72e82-210">Falso</span><span class="sxs-lookup"><span data-stu-id="72e82-210">False</span></span>                                        |
| <span data-ttu-id="72e82-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72e82-211">In Global Catalog</span></span>      | <span data-ttu-id="72e82-212">Falso</span><span class="sxs-lookup"><span data-stu-id="72e82-212">False</span></span>                                        |
| <span data-ttu-id="72e82-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72e82-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e82-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72e82-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="72e82-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e82-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="72e82-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e82-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="72e82-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e82-217">Search-Flags</span></span>           | <span data-ttu-id="72e82-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72e82-218">0x00000000</span></span>                                   |
| <span data-ttu-id="72e82-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e82-219">System-Flags</span></span>           | <span data-ttu-id="72e82-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72e82-220">0x00000010</span></span>                                   |
| <span data-ttu-id="72e82-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72e82-221">Classes used in</span></span>        | [<span data-ttu-id="72e82-222">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="72e82-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="72e82-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="72e82-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="72e82-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="72e82-224">Entry</span></span> | <span data-ttu-id="72e82-225">Valor</span><span class="sxs-lookup"><span data-stu-id="72e82-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="72e82-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="72e82-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="72e82-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e82-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="72e82-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e82-228">System-Only</span></span>            | <span data-ttu-id="72e82-229">Falso</span><span class="sxs-lookup"><span data-stu-id="72e82-229">False</span></span>                                        |
| <span data-ttu-id="72e82-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72e82-230">Is-Single-Valued</span></span>       | <span data-ttu-id="72e82-231">True</span><span class="sxs-lookup"><span data-stu-id="72e82-231">True</span></span>                                         |
| <span data-ttu-id="72e82-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="72e82-232">Is Indexed</span></span>             | <span data-ttu-id="72e82-233">Falso</span><span class="sxs-lookup"><span data-stu-id="72e82-233">False</span></span>                                        |
| <span data-ttu-id="72e82-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72e82-234">In Global Catalog</span></span>      | <span data-ttu-id="72e82-235">Falso</span><span class="sxs-lookup"><span data-stu-id="72e82-235">False</span></span>                                        |
| <span data-ttu-id="72e82-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72e82-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e82-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72e82-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="72e82-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e82-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="72e82-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e82-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="72e82-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e82-240">Search-Flags</span></span>           | <span data-ttu-id="72e82-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72e82-241">0x00000000</span></span>                                   |
| <span data-ttu-id="72e82-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e82-242">System-Flags</span></span>           | <span data-ttu-id="72e82-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72e82-243">0x00000010</span></span>                                   |
| <span data-ttu-id="72e82-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72e82-244">Classes used in</span></span>        | [<span data-ttu-id="72e82-245">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="72e82-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="72e82-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="72e82-246">Windows Server 2012</span></span>



| <span data-ttu-id="72e82-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="72e82-247">Entry</span></span> | <span data-ttu-id="72e82-248">Valor</span><span class="sxs-lookup"><span data-stu-id="72e82-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="72e82-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="72e82-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="72e82-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72e82-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="72e82-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="72e82-251">System-Only</span></span>            | <span data-ttu-id="72e82-252">Falso</span><span class="sxs-lookup"><span data-stu-id="72e82-252">False</span></span>                                        |
| <span data-ttu-id="72e82-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72e82-253">Is-Single-Valued</span></span>       | <span data-ttu-id="72e82-254">True</span><span class="sxs-lookup"><span data-stu-id="72e82-254">True</span></span>                                         |
| <span data-ttu-id="72e82-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="72e82-255">Is Indexed</span></span>             | <span data-ttu-id="72e82-256">Falso</span><span class="sxs-lookup"><span data-stu-id="72e82-256">False</span></span>                                        |
| <span data-ttu-id="72e82-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72e82-257">In Global Catalog</span></span>      | <span data-ttu-id="72e82-258">Falso</span><span class="sxs-lookup"><span data-stu-id="72e82-258">False</span></span>                                        |
| <span data-ttu-id="72e82-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72e82-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="72e82-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72e82-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="72e82-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72e82-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="72e82-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72e82-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="72e82-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72e82-263">Search-Flags</span></span>           | <span data-ttu-id="72e82-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72e82-264">0x00000000</span></span>                                   |
| <span data-ttu-id="72e82-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72e82-265">System-Flags</span></span>           | <span data-ttu-id="72e82-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72e82-266">0x00000010</span></span>                                   |
| <span data-ttu-id="72e82-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72e82-267">Classes used in</span></span>        | [<span data-ttu-id="72e82-268">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="72e82-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





