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
# <a name="acs-non-reserved-peak-rate-attribute"></a><span data-ttu-id="69aa9-105">ACS-não reservado-atributo de taxa de pico</span><span class="sxs-lookup"><span data-stu-id="69aa9-105">ACS-Non-Reserved-Peak-Rate attribute</span></span>

<span data-ttu-id="69aa9-106">O atributo **ACS-non-reservative-Rate** é somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="69aa9-106">The **ACS-Non-Reserved-Peak-Rate** attribute is for internal use only.</span></span> <span data-ttu-id="69aa9-107">Com base em RFC2814.</span><span class="sxs-lookup"><span data-stu-id="69aa9-107">Based on RFC2814.</span></span>



| <span data-ttu-id="69aa9-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="69aa9-108">Entry</span></span> | <span data-ttu-id="69aa9-109">Valor</span><span class="sxs-lookup"><span data-stu-id="69aa9-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="69aa9-110">CN</span><span class="sxs-lookup"><span data-stu-id="69aa9-110">CN</span></span>                | <span data-ttu-id="69aa9-111">ACS-não reservado-taxa de pico</span><span class="sxs-lookup"><span data-stu-id="69aa9-111">ACS-Non-Reserved-Peak-Rate</span></span>           |
| <span data-ttu-id="69aa9-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="69aa9-112">Ldap-Display-Name</span></span> | <span data-ttu-id="69aa9-113">aCSNonReservedPeakRate</span><span class="sxs-lookup"><span data-stu-id="69aa9-113">aCSNonReservedPeakRate</span></span>               |
| <span data-ttu-id="69aa9-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="69aa9-114">Size</span></span>              | <span data-ttu-id="69aa9-115">8 bytes</span><span class="sxs-lookup"><span data-stu-id="69aa9-115">8 bytes</span></span>                              |
| <span data-ttu-id="69aa9-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="69aa9-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="69aa9-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="69aa9-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="69aa9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="69aa9-118">Attribute-Id</span></span>      | <span data-ttu-id="69aa9-119">1.2.840.113556.1.4.1318</span><span class="sxs-lookup"><span data-stu-id="69aa9-119">1.2.840.113556.1.4.1318</span></span>              |
| <span data-ttu-id="69aa9-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="69aa9-120">System-Id-Guid</span></span>    | <span data-ttu-id="69aa9-121">a331a73f-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="69aa9-121">a331a73f-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="69aa9-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="69aa9-122">Syntax</span></span>            | [<span data-ttu-id="69aa9-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="69aa9-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="69aa9-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="69aa9-124">Implementations</span></span>

-   [<span data-ttu-id="69aa9-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="69aa9-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="69aa9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="69aa9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="69aa9-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="69aa9-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="69aa9-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="69aa9-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="69aa9-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="69aa9-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="69aa9-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="69aa9-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="69aa9-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="69aa9-131">Windows 2000 Server</span></span>



| <span data-ttu-id="69aa9-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="69aa9-132">Entry</span></span> | <span data-ttu-id="69aa9-133">Valor</span><span class="sxs-lookup"><span data-stu-id="69aa9-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69aa9-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="69aa9-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69aa9-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69aa9-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69aa9-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="69aa9-136">System-Only</span></span>            | <span data-ttu-id="69aa9-137">Falso</span><span class="sxs-lookup"><span data-stu-id="69aa9-137">False</span></span>                                        |
| <span data-ttu-id="69aa9-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="69aa9-138">Is-Single-Valued</span></span>       | <span data-ttu-id="69aa9-139">True</span><span class="sxs-lookup"><span data-stu-id="69aa9-139">True</span></span>                                         |
| <span data-ttu-id="69aa9-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="69aa9-140">Is Indexed</span></span>             | <span data-ttu-id="69aa9-141">Falso</span><span class="sxs-lookup"><span data-stu-id="69aa9-141">False</span></span>                                        |
| <span data-ttu-id="69aa9-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="69aa9-142">In Global Catalog</span></span>      | <span data-ttu-id="69aa9-143">Falso</span><span class="sxs-lookup"><span data-stu-id="69aa9-143">False</span></span>                                        |
| <span data-ttu-id="69aa9-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69aa9-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="69aa9-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="69aa9-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69aa9-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69aa9-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69aa9-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69aa9-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69aa9-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69aa9-148">Search-Flags</span></span>           | <span data-ttu-id="69aa9-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69aa9-149">0x00000000</span></span>                                   |
| <span data-ttu-id="69aa9-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69aa9-150">System-Flags</span></span>           | <span data-ttu-id="69aa9-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69aa9-151">0x00000010</span></span>                                   |
| <span data-ttu-id="69aa9-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="69aa9-152">Classes used in</span></span>        | [<span data-ttu-id="69aa9-153">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="69aa9-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="69aa9-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="69aa9-154">Windows Server 2003</span></span>



| <span data-ttu-id="69aa9-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="69aa9-155">Entry</span></span> | <span data-ttu-id="69aa9-156">Valor</span><span class="sxs-lookup"><span data-stu-id="69aa9-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69aa9-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="69aa9-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69aa9-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69aa9-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69aa9-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="69aa9-159">System-Only</span></span>            | <span data-ttu-id="69aa9-160">Falso</span><span class="sxs-lookup"><span data-stu-id="69aa9-160">False</span></span>                                        |
| <span data-ttu-id="69aa9-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="69aa9-161">Is-Single-Valued</span></span>       | <span data-ttu-id="69aa9-162">True</span><span class="sxs-lookup"><span data-stu-id="69aa9-162">True</span></span>                                         |
| <span data-ttu-id="69aa9-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="69aa9-163">Is Indexed</span></span>             | <span data-ttu-id="69aa9-164">Falso</span><span class="sxs-lookup"><span data-stu-id="69aa9-164">False</span></span>                                        |
| <span data-ttu-id="69aa9-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="69aa9-165">In Global Catalog</span></span>      | <span data-ttu-id="69aa9-166">Falso</span><span class="sxs-lookup"><span data-stu-id="69aa9-166">False</span></span>                                        |
| <span data-ttu-id="69aa9-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69aa9-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="69aa9-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="69aa9-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69aa9-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69aa9-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69aa9-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69aa9-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69aa9-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69aa9-171">Search-Flags</span></span>           | <span data-ttu-id="69aa9-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69aa9-172">0x00000000</span></span>                                   |
| <span data-ttu-id="69aa9-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69aa9-173">System-Flags</span></span>           | <span data-ttu-id="69aa9-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69aa9-174">0x00000010</span></span>                                   |
| <span data-ttu-id="69aa9-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="69aa9-175">Classes used in</span></span>        | [<span data-ttu-id="69aa9-176">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="69aa9-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="69aa9-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="69aa9-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="69aa9-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="69aa9-178">Entry</span></span> | <span data-ttu-id="69aa9-179">Valor</span><span class="sxs-lookup"><span data-stu-id="69aa9-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69aa9-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="69aa9-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69aa9-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69aa9-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69aa9-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="69aa9-182">System-Only</span></span>            | <span data-ttu-id="69aa9-183">Falso</span><span class="sxs-lookup"><span data-stu-id="69aa9-183">False</span></span>                                        |
| <span data-ttu-id="69aa9-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="69aa9-184">Is-Single-Valued</span></span>       | <span data-ttu-id="69aa9-185">True</span><span class="sxs-lookup"><span data-stu-id="69aa9-185">True</span></span>                                         |
| <span data-ttu-id="69aa9-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="69aa9-186">Is Indexed</span></span>             | <span data-ttu-id="69aa9-187">Falso</span><span class="sxs-lookup"><span data-stu-id="69aa9-187">False</span></span>                                        |
| <span data-ttu-id="69aa9-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="69aa9-188">In Global Catalog</span></span>      | <span data-ttu-id="69aa9-189">Falso</span><span class="sxs-lookup"><span data-stu-id="69aa9-189">False</span></span>                                        |
| <span data-ttu-id="69aa9-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69aa9-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="69aa9-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="69aa9-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69aa9-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69aa9-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69aa9-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69aa9-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69aa9-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69aa9-194">Search-Flags</span></span>           | <span data-ttu-id="69aa9-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69aa9-195">0x00000000</span></span>                                   |
| <span data-ttu-id="69aa9-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69aa9-196">System-Flags</span></span>           | <span data-ttu-id="69aa9-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69aa9-197">0x00000010</span></span>                                   |
| <span data-ttu-id="69aa9-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="69aa9-198">Classes used in</span></span>        | [<span data-ttu-id="69aa9-199">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="69aa9-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="69aa9-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69aa9-200">Windows Server 2008</span></span>



| <span data-ttu-id="69aa9-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="69aa9-201">Entry</span></span> | <span data-ttu-id="69aa9-202">Valor</span><span class="sxs-lookup"><span data-stu-id="69aa9-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69aa9-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="69aa9-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69aa9-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69aa9-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69aa9-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="69aa9-205">System-Only</span></span>            | <span data-ttu-id="69aa9-206">Falso</span><span class="sxs-lookup"><span data-stu-id="69aa9-206">False</span></span>                                        |
| <span data-ttu-id="69aa9-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="69aa9-207">Is-Single-Valued</span></span>       | <span data-ttu-id="69aa9-208">True</span><span class="sxs-lookup"><span data-stu-id="69aa9-208">True</span></span>                                         |
| <span data-ttu-id="69aa9-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="69aa9-209">Is Indexed</span></span>             | <span data-ttu-id="69aa9-210">Falso</span><span class="sxs-lookup"><span data-stu-id="69aa9-210">False</span></span>                                        |
| <span data-ttu-id="69aa9-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="69aa9-211">In Global Catalog</span></span>      | <span data-ttu-id="69aa9-212">Falso</span><span class="sxs-lookup"><span data-stu-id="69aa9-212">False</span></span>                                        |
| <span data-ttu-id="69aa9-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69aa9-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="69aa9-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="69aa9-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69aa9-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69aa9-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69aa9-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69aa9-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69aa9-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69aa9-217">Search-Flags</span></span>           | <span data-ttu-id="69aa9-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69aa9-218">0x00000000</span></span>                                   |
| <span data-ttu-id="69aa9-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69aa9-219">System-Flags</span></span>           | <span data-ttu-id="69aa9-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69aa9-220">0x00000010</span></span>                                   |
| <span data-ttu-id="69aa9-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="69aa9-221">Classes used in</span></span>        | [<span data-ttu-id="69aa9-222">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="69aa9-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="69aa9-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="69aa9-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="69aa9-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="69aa9-224">Entry</span></span> | <span data-ttu-id="69aa9-225">Valor</span><span class="sxs-lookup"><span data-stu-id="69aa9-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69aa9-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="69aa9-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69aa9-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69aa9-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69aa9-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="69aa9-228">System-Only</span></span>            | <span data-ttu-id="69aa9-229">Falso</span><span class="sxs-lookup"><span data-stu-id="69aa9-229">False</span></span>                                        |
| <span data-ttu-id="69aa9-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="69aa9-230">Is-Single-Valued</span></span>       | <span data-ttu-id="69aa9-231">True</span><span class="sxs-lookup"><span data-stu-id="69aa9-231">True</span></span>                                         |
| <span data-ttu-id="69aa9-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="69aa9-232">Is Indexed</span></span>             | <span data-ttu-id="69aa9-233">Falso</span><span class="sxs-lookup"><span data-stu-id="69aa9-233">False</span></span>                                        |
| <span data-ttu-id="69aa9-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="69aa9-234">In Global Catalog</span></span>      | <span data-ttu-id="69aa9-235">Falso</span><span class="sxs-lookup"><span data-stu-id="69aa9-235">False</span></span>                                        |
| <span data-ttu-id="69aa9-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69aa9-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="69aa9-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="69aa9-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69aa9-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69aa9-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69aa9-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69aa9-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69aa9-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69aa9-240">Search-Flags</span></span>           | <span data-ttu-id="69aa9-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69aa9-241">0x00000000</span></span>                                   |
| <span data-ttu-id="69aa9-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69aa9-242">System-Flags</span></span>           | <span data-ttu-id="69aa9-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69aa9-243">0x00000010</span></span>                                   |
| <span data-ttu-id="69aa9-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="69aa9-244">Classes used in</span></span>        | [<span data-ttu-id="69aa9-245">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="69aa9-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="69aa9-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="69aa9-246">Windows Server 2012</span></span>



| <span data-ttu-id="69aa9-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="69aa9-247">Entry</span></span> | <span data-ttu-id="69aa9-248">Valor</span><span class="sxs-lookup"><span data-stu-id="69aa9-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69aa9-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="69aa9-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69aa9-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69aa9-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69aa9-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="69aa9-251">System-Only</span></span>            | <span data-ttu-id="69aa9-252">Falso</span><span class="sxs-lookup"><span data-stu-id="69aa9-252">False</span></span>                                        |
| <span data-ttu-id="69aa9-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="69aa9-253">Is-Single-Valued</span></span>       | <span data-ttu-id="69aa9-254">True</span><span class="sxs-lookup"><span data-stu-id="69aa9-254">True</span></span>                                         |
| <span data-ttu-id="69aa9-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="69aa9-255">Is Indexed</span></span>             | <span data-ttu-id="69aa9-256">Falso</span><span class="sxs-lookup"><span data-stu-id="69aa9-256">False</span></span>                                        |
| <span data-ttu-id="69aa9-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="69aa9-257">In Global Catalog</span></span>      | <span data-ttu-id="69aa9-258">Falso</span><span class="sxs-lookup"><span data-stu-id="69aa9-258">False</span></span>                                        |
| <span data-ttu-id="69aa9-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="69aa9-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="69aa9-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="69aa9-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69aa9-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69aa9-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69aa9-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69aa9-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69aa9-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69aa9-263">Search-Flags</span></span>           | <span data-ttu-id="69aa9-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69aa9-264">0x00000000</span></span>                                   |
| <span data-ttu-id="69aa9-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69aa9-265">System-Flags</span></span>           | <span data-ttu-id="69aa9-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69aa9-266">0x00000010</span></span>                                   |
| <span data-ttu-id="69aa9-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="69aa9-267">Classes used in</span></span>        | [<span data-ttu-id="69aa9-268">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="69aa9-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





