---
title: ACS – atributo non-reserved-TX-size
description: O tamanho do Bucket de token que um aplicativo pode usar antes que uma reserva esteja em vigor.
ms.assetid: 67a0d6fd-b556-49d2-8c5b-6efebf1052c3
ms.tgt_platform: multiple
keywords:
- ACS-esquema não reservado de atributo de dimensão de tamanho TX
- Esquema de AD do atributo aCSNonReservedTxSize
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Tx-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cd19dde97e3a9fc6ef58165c8dbcbfbebba729
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825445"
---
# <a name="acs-non-reserved-tx-size-attribute"></a><span data-ttu-id="2db77-105">ACS – atributo non-reserved-TX-size</span><span class="sxs-lookup"><span data-stu-id="2db77-105">ACS-Non-Reserved-Tx-Size attribute</span></span>

<span data-ttu-id="2db77-106">O tamanho do Bucket de token que um aplicativo pode usar antes que uma reserva esteja em vigor.</span><span class="sxs-lookup"><span data-stu-id="2db77-106">The token bucket size an application can use before a reservation is in place.</span></span>



| <span data-ttu-id="2db77-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="2db77-107">Entry</span></span> | <span data-ttu-id="2db77-108">Valor</span><span class="sxs-lookup"><span data-stu-id="2db77-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2db77-109">CN</span><span class="sxs-lookup"><span data-stu-id="2db77-109">CN</span></span>                | <span data-ttu-id="2db77-110">ACS-não reservado-TX-tamanho</span><span class="sxs-lookup"><span data-stu-id="2db77-110">ACS-Non-Reserved-Tx-Size</span></span>             |
| <span data-ttu-id="2db77-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2db77-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2db77-112">aCSNonReservedTxSize</span><span class="sxs-lookup"><span data-stu-id="2db77-112">aCSNonReservedTxSize</span></span>                 |
| <span data-ttu-id="2db77-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="2db77-113">Size</span></span>              | <span data-ttu-id="2db77-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="2db77-114">8 bytes</span></span>                              |
| <span data-ttu-id="2db77-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="2db77-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="2db77-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="2db77-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2db77-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2db77-117">Attribute-Id</span></span>      | <span data-ttu-id="2db77-118">1.2.840.113556.1.4.898</span><span class="sxs-lookup"><span data-stu-id="2db77-118">1.2.840.113556.1.4.898</span></span>               |
| <span data-ttu-id="2db77-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2db77-119">System-Id-Guid</span></span>    | <span data-ttu-id="2db77-120">f072230d-aef5-11d1-bdcf-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="2db77-120">f072230d-aef5-11d1-bdcf-0000f80367c1</span></span> |
| <span data-ttu-id="2db77-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="2db77-121">Syntax</span></span>            | [<span data-ttu-id="2db77-122">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="2db77-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="2db77-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="2db77-123">Implementations</span></span>

-   [<span data-ttu-id="2db77-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2db77-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2db77-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2db77-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2db77-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2db77-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2db77-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2db77-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2db77-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2db77-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2db77-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2db77-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2db77-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2db77-130">Windows 2000 Server</span></span>



| <span data-ttu-id="2db77-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="2db77-131">Entry</span></span> | <span data-ttu-id="2db77-132">Valor</span><span class="sxs-lookup"><span data-stu-id="2db77-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2db77-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="2db77-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2db77-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2db77-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2db77-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="2db77-135">System-Only</span></span>            | <span data-ttu-id="2db77-136">Falso</span><span class="sxs-lookup"><span data-stu-id="2db77-136">False</span></span>                                        |
| <span data-ttu-id="2db77-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2db77-137">Is-Single-Valued</span></span>       | <span data-ttu-id="2db77-138">True</span><span class="sxs-lookup"><span data-stu-id="2db77-138">True</span></span>                                         |
| <span data-ttu-id="2db77-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="2db77-139">Is Indexed</span></span>             | <span data-ttu-id="2db77-140">Falso</span><span class="sxs-lookup"><span data-stu-id="2db77-140">False</span></span>                                        |
| <span data-ttu-id="2db77-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2db77-141">In Global Catalog</span></span>      | <span data-ttu-id="2db77-142">Falso</span><span class="sxs-lookup"><span data-stu-id="2db77-142">False</span></span>                                        |
| <span data-ttu-id="2db77-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2db77-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="2db77-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2db77-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2db77-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2db77-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2db77-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2db77-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2db77-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2db77-147">Search-Flags</span></span>           | <span data-ttu-id="2db77-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2db77-148">0x00000000</span></span>                                   |
| <span data-ttu-id="2db77-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2db77-149">System-Flags</span></span>           | <span data-ttu-id="2db77-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2db77-150">0x00000010</span></span>                                   |
| <span data-ttu-id="2db77-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2db77-151">Classes used in</span></span>        | [<span data-ttu-id="2db77-152">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="2db77-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2db77-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2db77-153">Windows Server 2003</span></span>



| <span data-ttu-id="2db77-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="2db77-154">Entry</span></span> | <span data-ttu-id="2db77-155">Valor</span><span class="sxs-lookup"><span data-stu-id="2db77-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2db77-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="2db77-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2db77-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2db77-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2db77-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="2db77-158">System-Only</span></span>            | <span data-ttu-id="2db77-159">Falso</span><span class="sxs-lookup"><span data-stu-id="2db77-159">False</span></span>                                        |
| <span data-ttu-id="2db77-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2db77-160">Is-Single-Valued</span></span>       | <span data-ttu-id="2db77-161">True</span><span class="sxs-lookup"><span data-stu-id="2db77-161">True</span></span>                                         |
| <span data-ttu-id="2db77-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="2db77-162">Is Indexed</span></span>             | <span data-ttu-id="2db77-163">Falso</span><span class="sxs-lookup"><span data-stu-id="2db77-163">False</span></span>                                        |
| <span data-ttu-id="2db77-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2db77-164">In Global Catalog</span></span>      | <span data-ttu-id="2db77-165">Falso</span><span class="sxs-lookup"><span data-stu-id="2db77-165">False</span></span>                                        |
| <span data-ttu-id="2db77-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2db77-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="2db77-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2db77-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2db77-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2db77-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2db77-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2db77-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2db77-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2db77-170">Search-Flags</span></span>           | <span data-ttu-id="2db77-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2db77-171">0x00000000</span></span>                                   |
| <span data-ttu-id="2db77-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2db77-172">System-Flags</span></span>           | <span data-ttu-id="2db77-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2db77-173">0x00000010</span></span>                                   |
| <span data-ttu-id="2db77-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2db77-174">Classes used in</span></span>        | [<span data-ttu-id="2db77-175">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="2db77-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2db77-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2db77-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2db77-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="2db77-177">Entry</span></span> | <span data-ttu-id="2db77-178">Valor</span><span class="sxs-lookup"><span data-stu-id="2db77-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2db77-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="2db77-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2db77-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2db77-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2db77-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="2db77-181">System-Only</span></span>            | <span data-ttu-id="2db77-182">Falso</span><span class="sxs-lookup"><span data-stu-id="2db77-182">False</span></span>                                        |
| <span data-ttu-id="2db77-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2db77-183">Is-Single-Valued</span></span>       | <span data-ttu-id="2db77-184">True</span><span class="sxs-lookup"><span data-stu-id="2db77-184">True</span></span>                                         |
| <span data-ttu-id="2db77-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="2db77-185">Is Indexed</span></span>             | <span data-ttu-id="2db77-186">Falso</span><span class="sxs-lookup"><span data-stu-id="2db77-186">False</span></span>                                        |
| <span data-ttu-id="2db77-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2db77-187">In Global Catalog</span></span>      | <span data-ttu-id="2db77-188">Falso</span><span class="sxs-lookup"><span data-stu-id="2db77-188">False</span></span>                                        |
| <span data-ttu-id="2db77-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2db77-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="2db77-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2db77-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2db77-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2db77-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2db77-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2db77-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2db77-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2db77-193">Search-Flags</span></span>           | <span data-ttu-id="2db77-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2db77-194">0x00000000</span></span>                                   |
| <span data-ttu-id="2db77-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2db77-195">System-Flags</span></span>           | <span data-ttu-id="2db77-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2db77-196">0x00000010</span></span>                                   |
| <span data-ttu-id="2db77-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2db77-197">Classes used in</span></span>        | [<span data-ttu-id="2db77-198">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="2db77-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2db77-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2db77-199">Windows Server 2008</span></span>



| <span data-ttu-id="2db77-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="2db77-200">Entry</span></span> | <span data-ttu-id="2db77-201">Valor</span><span class="sxs-lookup"><span data-stu-id="2db77-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2db77-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="2db77-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2db77-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2db77-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2db77-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="2db77-204">System-Only</span></span>            | <span data-ttu-id="2db77-205">Falso</span><span class="sxs-lookup"><span data-stu-id="2db77-205">False</span></span>                                        |
| <span data-ttu-id="2db77-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2db77-206">Is-Single-Valued</span></span>       | <span data-ttu-id="2db77-207">True</span><span class="sxs-lookup"><span data-stu-id="2db77-207">True</span></span>                                         |
| <span data-ttu-id="2db77-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="2db77-208">Is Indexed</span></span>             | <span data-ttu-id="2db77-209">Falso</span><span class="sxs-lookup"><span data-stu-id="2db77-209">False</span></span>                                        |
| <span data-ttu-id="2db77-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2db77-210">In Global Catalog</span></span>      | <span data-ttu-id="2db77-211">Falso</span><span class="sxs-lookup"><span data-stu-id="2db77-211">False</span></span>                                        |
| <span data-ttu-id="2db77-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2db77-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="2db77-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2db77-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2db77-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2db77-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2db77-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2db77-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2db77-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2db77-216">Search-Flags</span></span>           | <span data-ttu-id="2db77-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2db77-217">0x00000000</span></span>                                   |
| <span data-ttu-id="2db77-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2db77-218">System-Flags</span></span>           | <span data-ttu-id="2db77-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2db77-219">0x00000010</span></span>                                   |
| <span data-ttu-id="2db77-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2db77-220">Classes used in</span></span>        | [<span data-ttu-id="2db77-221">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="2db77-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2db77-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2db77-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2db77-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="2db77-223">Entry</span></span> | <span data-ttu-id="2db77-224">Valor</span><span class="sxs-lookup"><span data-stu-id="2db77-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2db77-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="2db77-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2db77-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2db77-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2db77-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="2db77-227">System-Only</span></span>            | <span data-ttu-id="2db77-228">Falso</span><span class="sxs-lookup"><span data-stu-id="2db77-228">False</span></span>                                        |
| <span data-ttu-id="2db77-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2db77-229">Is-Single-Valued</span></span>       | <span data-ttu-id="2db77-230">True</span><span class="sxs-lookup"><span data-stu-id="2db77-230">True</span></span>                                         |
| <span data-ttu-id="2db77-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="2db77-231">Is Indexed</span></span>             | <span data-ttu-id="2db77-232">Falso</span><span class="sxs-lookup"><span data-stu-id="2db77-232">False</span></span>                                        |
| <span data-ttu-id="2db77-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2db77-233">In Global Catalog</span></span>      | <span data-ttu-id="2db77-234">Falso</span><span class="sxs-lookup"><span data-stu-id="2db77-234">False</span></span>                                        |
| <span data-ttu-id="2db77-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2db77-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="2db77-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2db77-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2db77-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2db77-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2db77-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2db77-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2db77-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2db77-239">Search-Flags</span></span>           | <span data-ttu-id="2db77-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2db77-240">0x00000000</span></span>                                   |
| <span data-ttu-id="2db77-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2db77-241">System-Flags</span></span>           | <span data-ttu-id="2db77-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2db77-242">0x00000010</span></span>                                   |
| <span data-ttu-id="2db77-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2db77-243">Classes used in</span></span>        | [<span data-ttu-id="2db77-244">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="2db77-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2db77-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2db77-245">Windows Server 2012</span></span>



| <span data-ttu-id="2db77-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="2db77-246">Entry</span></span> | <span data-ttu-id="2db77-247">Valor</span><span class="sxs-lookup"><span data-stu-id="2db77-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2db77-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="2db77-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2db77-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2db77-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2db77-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="2db77-250">System-Only</span></span>            | <span data-ttu-id="2db77-251">Falso</span><span class="sxs-lookup"><span data-stu-id="2db77-251">False</span></span>                                        |
| <span data-ttu-id="2db77-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2db77-252">Is-Single-Valued</span></span>       | <span data-ttu-id="2db77-253">True</span><span class="sxs-lookup"><span data-stu-id="2db77-253">True</span></span>                                         |
| <span data-ttu-id="2db77-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="2db77-254">Is Indexed</span></span>             | <span data-ttu-id="2db77-255">Falso</span><span class="sxs-lookup"><span data-stu-id="2db77-255">False</span></span>                                        |
| <span data-ttu-id="2db77-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2db77-256">In Global Catalog</span></span>      | <span data-ttu-id="2db77-257">Falso</span><span class="sxs-lookup"><span data-stu-id="2db77-257">False</span></span>                                        |
| <span data-ttu-id="2db77-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2db77-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="2db77-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2db77-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2db77-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2db77-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2db77-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2db77-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2db77-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2db77-262">Search-Flags</span></span>           | <span data-ttu-id="2db77-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2db77-263">0x00000000</span></span>                                   |
| <span data-ttu-id="2db77-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2db77-264">System-Flags</span></span>           | <span data-ttu-id="2db77-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2db77-265">0x00000010</span></span>                                   |
| <span data-ttu-id="2db77-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2db77-266">Classes used in</span></span>        | [<span data-ttu-id="2db77-267">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="2db77-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





