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
# <a name="acs-non-reserved-peak-rate-attribute"></a><span data-ttu-id="8bb97-105">ACS-não reservado-atributo de taxa de pico</span><span class="sxs-lookup"><span data-stu-id="8bb97-105">ACS-Non-Reserved-Peak-Rate attribute</span></span>

<span data-ttu-id="8bb97-106">O atributo **ACS-non-reservative-Rate** é somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="8bb97-106">The **ACS-Non-Reserved-Peak-Rate** attribute is for internal use only.</span></span> <span data-ttu-id="8bb97-107">Com base em RFC2814.</span><span class="sxs-lookup"><span data-stu-id="8bb97-107">Based on RFC2814.</span></span>



| <span data-ttu-id="8bb97-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="8bb97-108">Entry</span></span> | <span data-ttu-id="8bb97-109">Valor</span><span class="sxs-lookup"><span data-stu-id="8bb97-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8bb97-110">CN</span><span class="sxs-lookup"><span data-stu-id="8bb97-110">CN</span></span>                | <span data-ttu-id="8bb97-111">ACS-não reservado-taxa de pico</span><span class="sxs-lookup"><span data-stu-id="8bb97-111">ACS-Non-Reserved-Peak-Rate</span></span>           |
| <span data-ttu-id="8bb97-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8bb97-112">Ldap-Display-Name</span></span> | <span data-ttu-id="8bb97-113">aCSNonReservedPeakRate</span><span class="sxs-lookup"><span data-stu-id="8bb97-113">aCSNonReservedPeakRate</span></span>               |
| <span data-ttu-id="8bb97-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="8bb97-114">Size</span></span>              | <span data-ttu-id="8bb97-115">8 bytes</span><span class="sxs-lookup"><span data-stu-id="8bb97-115">8 bytes</span></span>                              |
| <span data-ttu-id="8bb97-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="8bb97-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="8bb97-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="8bb97-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8bb97-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8bb97-118">Attribute-Id</span></span>      | <span data-ttu-id="8bb97-119">1.2.840.113556.1.4.1318</span><span class="sxs-lookup"><span data-stu-id="8bb97-119">1.2.840.113556.1.4.1318</span></span>              |
| <span data-ttu-id="8bb97-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8bb97-120">System-Id-Guid</span></span>    | <span data-ttu-id="8bb97-121">a331a73f-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="8bb97-121">a331a73f-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="8bb97-122">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8bb97-122">Syntax</span></span>            | [<span data-ttu-id="8bb97-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="8bb97-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="8bb97-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="8bb97-124">Implementations</span></span>

-   [<span data-ttu-id="8bb97-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8bb97-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8bb97-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8bb97-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8bb97-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8bb97-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8bb97-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8bb97-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8bb97-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8bb97-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8bb97-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8bb97-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8bb97-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8bb97-131">Windows 2000 Server</span></span>



| <span data-ttu-id="8bb97-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="8bb97-132">Entry</span></span> | <span data-ttu-id="8bb97-133">Valor</span><span class="sxs-lookup"><span data-stu-id="8bb97-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8bb97-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="8bb97-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8bb97-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8bb97-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8bb97-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8bb97-136">System-Only</span></span>            | <span data-ttu-id="8bb97-137">Falso</span><span class="sxs-lookup"><span data-stu-id="8bb97-137">False</span></span>                                        |
| <span data-ttu-id="8bb97-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8bb97-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8bb97-139">True</span><span class="sxs-lookup"><span data-stu-id="8bb97-139">True</span></span>                                         |
| <span data-ttu-id="8bb97-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="8bb97-140">Is Indexed</span></span>             | <span data-ttu-id="8bb97-141">Falso</span><span class="sxs-lookup"><span data-stu-id="8bb97-141">False</span></span>                                        |
| <span data-ttu-id="8bb97-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8bb97-142">In Global Catalog</span></span>      | <span data-ttu-id="8bb97-143">Falso</span><span class="sxs-lookup"><span data-stu-id="8bb97-143">False</span></span>                                        |
| <span data-ttu-id="8bb97-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8bb97-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8bb97-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8bb97-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8bb97-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8bb97-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8bb97-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8bb97-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8bb97-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8bb97-148">Search-Flags</span></span>           | <span data-ttu-id="8bb97-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8bb97-149">0x00000000</span></span>                                   |
| <span data-ttu-id="8bb97-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8bb97-150">System-Flags</span></span>           | <span data-ttu-id="8bb97-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8bb97-151">0x00000010</span></span>                                   |
| <span data-ttu-id="8bb97-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8bb97-152">Classes used in</span></span>        | [<span data-ttu-id="8bb97-153">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="8bb97-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8bb97-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8bb97-154">Windows Server 2003</span></span>



| <span data-ttu-id="8bb97-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="8bb97-155">Entry</span></span> | <span data-ttu-id="8bb97-156">Valor</span><span class="sxs-lookup"><span data-stu-id="8bb97-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8bb97-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="8bb97-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8bb97-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8bb97-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8bb97-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="8bb97-159">System-Only</span></span>            | <span data-ttu-id="8bb97-160">Falso</span><span class="sxs-lookup"><span data-stu-id="8bb97-160">False</span></span>                                        |
| <span data-ttu-id="8bb97-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8bb97-161">Is-Single-Valued</span></span>       | <span data-ttu-id="8bb97-162">True</span><span class="sxs-lookup"><span data-stu-id="8bb97-162">True</span></span>                                         |
| <span data-ttu-id="8bb97-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="8bb97-163">Is Indexed</span></span>             | <span data-ttu-id="8bb97-164">Falso</span><span class="sxs-lookup"><span data-stu-id="8bb97-164">False</span></span>                                        |
| <span data-ttu-id="8bb97-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8bb97-165">In Global Catalog</span></span>      | <span data-ttu-id="8bb97-166">Falso</span><span class="sxs-lookup"><span data-stu-id="8bb97-166">False</span></span>                                        |
| <span data-ttu-id="8bb97-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8bb97-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="8bb97-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8bb97-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8bb97-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8bb97-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8bb97-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8bb97-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8bb97-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8bb97-171">Search-Flags</span></span>           | <span data-ttu-id="8bb97-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8bb97-172">0x00000000</span></span>                                   |
| <span data-ttu-id="8bb97-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8bb97-173">System-Flags</span></span>           | <span data-ttu-id="8bb97-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8bb97-174">0x00000010</span></span>                                   |
| <span data-ttu-id="8bb97-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8bb97-175">Classes used in</span></span>        | [<span data-ttu-id="8bb97-176">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="8bb97-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8bb97-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8bb97-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8bb97-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="8bb97-178">Entry</span></span> | <span data-ttu-id="8bb97-179">Valor</span><span class="sxs-lookup"><span data-stu-id="8bb97-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8bb97-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="8bb97-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8bb97-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8bb97-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8bb97-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="8bb97-182">System-Only</span></span>            | <span data-ttu-id="8bb97-183">Falso</span><span class="sxs-lookup"><span data-stu-id="8bb97-183">False</span></span>                                        |
| <span data-ttu-id="8bb97-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8bb97-184">Is-Single-Valued</span></span>       | <span data-ttu-id="8bb97-185">True</span><span class="sxs-lookup"><span data-stu-id="8bb97-185">True</span></span>                                         |
| <span data-ttu-id="8bb97-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="8bb97-186">Is Indexed</span></span>             | <span data-ttu-id="8bb97-187">Falso</span><span class="sxs-lookup"><span data-stu-id="8bb97-187">False</span></span>                                        |
| <span data-ttu-id="8bb97-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8bb97-188">In Global Catalog</span></span>      | <span data-ttu-id="8bb97-189">Falso</span><span class="sxs-lookup"><span data-stu-id="8bb97-189">False</span></span>                                        |
| <span data-ttu-id="8bb97-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8bb97-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="8bb97-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8bb97-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8bb97-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8bb97-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8bb97-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8bb97-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8bb97-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8bb97-194">Search-Flags</span></span>           | <span data-ttu-id="8bb97-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8bb97-195">0x00000000</span></span>                                   |
| <span data-ttu-id="8bb97-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8bb97-196">System-Flags</span></span>           | <span data-ttu-id="8bb97-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8bb97-197">0x00000010</span></span>                                   |
| <span data-ttu-id="8bb97-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8bb97-198">Classes used in</span></span>        | [<span data-ttu-id="8bb97-199">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="8bb97-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8bb97-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8bb97-200">Windows Server 2008</span></span>



| <span data-ttu-id="8bb97-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="8bb97-201">Entry</span></span> | <span data-ttu-id="8bb97-202">Valor</span><span class="sxs-lookup"><span data-stu-id="8bb97-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8bb97-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="8bb97-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8bb97-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8bb97-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8bb97-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="8bb97-205">System-Only</span></span>            | <span data-ttu-id="8bb97-206">Falso</span><span class="sxs-lookup"><span data-stu-id="8bb97-206">False</span></span>                                        |
| <span data-ttu-id="8bb97-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8bb97-207">Is-Single-Valued</span></span>       | <span data-ttu-id="8bb97-208">True</span><span class="sxs-lookup"><span data-stu-id="8bb97-208">True</span></span>                                         |
| <span data-ttu-id="8bb97-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="8bb97-209">Is Indexed</span></span>             | <span data-ttu-id="8bb97-210">Falso</span><span class="sxs-lookup"><span data-stu-id="8bb97-210">False</span></span>                                        |
| <span data-ttu-id="8bb97-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8bb97-211">In Global Catalog</span></span>      | <span data-ttu-id="8bb97-212">Falso</span><span class="sxs-lookup"><span data-stu-id="8bb97-212">False</span></span>                                        |
| <span data-ttu-id="8bb97-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8bb97-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="8bb97-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8bb97-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8bb97-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8bb97-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8bb97-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8bb97-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8bb97-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8bb97-217">Search-Flags</span></span>           | <span data-ttu-id="8bb97-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8bb97-218">0x00000000</span></span>                                   |
| <span data-ttu-id="8bb97-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8bb97-219">System-Flags</span></span>           | <span data-ttu-id="8bb97-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8bb97-220">0x00000010</span></span>                                   |
| <span data-ttu-id="8bb97-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8bb97-221">Classes used in</span></span>        | [<span data-ttu-id="8bb97-222">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="8bb97-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8bb97-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8bb97-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8bb97-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="8bb97-224">Entry</span></span> | <span data-ttu-id="8bb97-225">Valor</span><span class="sxs-lookup"><span data-stu-id="8bb97-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8bb97-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="8bb97-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8bb97-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8bb97-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8bb97-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="8bb97-228">System-Only</span></span>            | <span data-ttu-id="8bb97-229">Falso</span><span class="sxs-lookup"><span data-stu-id="8bb97-229">False</span></span>                                        |
| <span data-ttu-id="8bb97-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8bb97-230">Is-Single-Valued</span></span>       | <span data-ttu-id="8bb97-231">True</span><span class="sxs-lookup"><span data-stu-id="8bb97-231">True</span></span>                                         |
| <span data-ttu-id="8bb97-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="8bb97-232">Is Indexed</span></span>             | <span data-ttu-id="8bb97-233">Falso</span><span class="sxs-lookup"><span data-stu-id="8bb97-233">False</span></span>                                        |
| <span data-ttu-id="8bb97-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8bb97-234">In Global Catalog</span></span>      | <span data-ttu-id="8bb97-235">Falso</span><span class="sxs-lookup"><span data-stu-id="8bb97-235">False</span></span>                                        |
| <span data-ttu-id="8bb97-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8bb97-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="8bb97-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8bb97-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8bb97-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8bb97-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8bb97-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8bb97-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8bb97-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8bb97-240">Search-Flags</span></span>           | <span data-ttu-id="8bb97-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8bb97-241">0x00000000</span></span>                                   |
| <span data-ttu-id="8bb97-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8bb97-242">System-Flags</span></span>           | <span data-ttu-id="8bb97-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8bb97-243">0x00000010</span></span>                                   |
| <span data-ttu-id="8bb97-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8bb97-244">Classes used in</span></span>        | [<span data-ttu-id="8bb97-245">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="8bb97-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8bb97-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8bb97-246">Windows Server 2012</span></span>



| <span data-ttu-id="8bb97-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="8bb97-247">Entry</span></span> | <span data-ttu-id="8bb97-248">Valor</span><span class="sxs-lookup"><span data-stu-id="8bb97-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8bb97-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="8bb97-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8bb97-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8bb97-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8bb97-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="8bb97-251">System-Only</span></span>            | <span data-ttu-id="8bb97-252">Falso</span><span class="sxs-lookup"><span data-stu-id="8bb97-252">False</span></span>                                        |
| <span data-ttu-id="8bb97-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8bb97-253">Is-Single-Valued</span></span>       | <span data-ttu-id="8bb97-254">True</span><span class="sxs-lookup"><span data-stu-id="8bb97-254">True</span></span>                                         |
| <span data-ttu-id="8bb97-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="8bb97-255">Is Indexed</span></span>             | <span data-ttu-id="8bb97-256">Falso</span><span class="sxs-lookup"><span data-stu-id="8bb97-256">False</span></span>                                        |
| <span data-ttu-id="8bb97-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8bb97-257">In Global Catalog</span></span>      | <span data-ttu-id="8bb97-258">Falso</span><span class="sxs-lookup"><span data-stu-id="8bb97-258">False</span></span>                                        |
| <span data-ttu-id="8bb97-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8bb97-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="8bb97-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8bb97-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8bb97-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8bb97-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8bb97-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8bb97-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8bb97-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8bb97-263">Search-Flags</span></span>           | <span data-ttu-id="8bb97-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8bb97-264">0x00000000</span></span>                                   |
| <span data-ttu-id="8bb97-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8bb97-265">System-Flags</span></span>           | <span data-ttu-id="8bb97-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8bb97-266">0x00000010</span></span>                                   |
| <span data-ttu-id="8bb97-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8bb97-267">Classes used in</span></span>        | [<span data-ttu-id="8bb97-268">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="8bb97-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





