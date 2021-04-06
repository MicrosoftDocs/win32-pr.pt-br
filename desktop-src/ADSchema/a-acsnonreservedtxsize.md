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
# <a name="acs-non-reserved-tx-size-attribute"></a><span data-ttu-id="7f53c-105">ACS – atributo non-reserved-TX-size</span><span class="sxs-lookup"><span data-stu-id="7f53c-105">ACS-Non-Reserved-Tx-Size attribute</span></span>

<span data-ttu-id="7f53c-106">O tamanho do Bucket de token que um aplicativo pode usar antes que uma reserva esteja em vigor.</span><span class="sxs-lookup"><span data-stu-id="7f53c-106">The token bucket size an application can use before a reservation is in place.</span></span>



| <span data-ttu-id="7f53c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="7f53c-107">Entry</span></span> | <span data-ttu-id="7f53c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="7f53c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7f53c-109">CN</span><span class="sxs-lookup"><span data-stu-id="7f53c-109">CN</span></span>                | <span data-ttu-id="7f53c-110">ACS-não reservado-TX-tamanho</span><span class="sxs-lookup"><span data-stu-id="7f53c-110">ACS-Non-Reserved-Tx-Size</span></span>             |
| <span data-ttu-id="7f53c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7f53c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7f53c-112">aCSNonReservedTxSize</span><span class="sxs-lookup"><span data-stu-id="7f53c-112">aCSNonReservedTxSize</span></span>                 |
| <span data-ttu-id="7f53c-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="7f53c-113">Size</span></span>              | <span data-ttu-id="7f53c-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="7f53c-114">8 bytes</span></span>                              |
| <span data-ttu-id="7f53c-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="7f53c-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="7f53c-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="7f53c-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7f53c-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7f53c-117">Attribute-Id</span></span>      | <span data-ttu-id="7f53c-118">1.2.840.113556.1.4.898</span><span class="sxs-lookup"><span data-stu-id="7f53c-118">1.2.840.113556.1.4.898</span></span>               |
| <span data-ttu-id="7f53c-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7f53c-119">System-Id-Guid</span></span>    | <span data-ttu-id="7f53c-120">f072230d-aef5-11d1-bdcf-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="7f53c-120">f072230d-aef5-11d1-bdcf-0000f80367c1</span></span> |
| <span data-ttu-id="7f53c-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f53c-121">Syntax</span></span>            | [<span data-ttu-id="7f53c-122">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="7f53c-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="7f53c-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="7f53c-123">Implementations</span></span>

-   [<span data-ttu-id="7f53c-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7f53c-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7f53c-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7f53c-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7f53c-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7f53c-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7f53c-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7f53c-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7f53c-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7f53c-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7f53c-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7f53c-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7f53c-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7f53c-130">Windows 2000 Server</span></span>



| <span data-ttu-id="7f53c-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="7f53c-131">Entry</span></span> | <span data-ttu-id="7f53c-132">Valor</span><span class="sxs-lookup"><span data-stu-id="7f53c-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7f53c-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="7f53c-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7f53c-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f53c-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7f53c-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f53c-135">System-Only</span></span>            | <span data-ttu-id="7f53c-136">Falso</span><span class="sxs-lookup"><span data-stu-id="7f53c-136">False</span></span>                                        |
| <span data-ttu-id="7f53c-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7f53c-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7f53c-138">True</span><span class="sxs-lookup"><span data-stu-id="7f53c-138">True</span></span>                                         |
| <span data-ttu-id="7f53c-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="7f53c-139">Is Indexed</span></span>             | <span data-ttu-id="7f53c-140">Falso</span><span class="sxs-lookup"><span data-stu-id="7f53c-140">False</span></span>                                        |
| <span data-ttu-id="7f53c-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7f53c-141">In Global Catalog</span></span>      | <span data-ttu-id="7f53c-142">Falso</span><span class="sxs-lookup"><span data-stu-id="7f53c-142">False</span></span>                                        |
| <span data-ttu-id="7f53c-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7f53c-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f53c-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7f53c-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7f53c-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f53c-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7f53c-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f53c-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7f53c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f53c-147">Search-Flags</span></span>           | <span data-ttu-id="7f53c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f53c-148">0x00000000</span></span>                                   |
| <span data-ttu-id="7f53c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f53c-149">System-Flags</span></span>           | <span data-ttu-id="7f53c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f53c-150">0x00000010</span></span>                                   |
| <span data-ttu-id="7f53c-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7f53c-151">Classes used in</span></span>        | [<span data-ttu-id="7f53c-152">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="7f53c-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7f53c-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7f53c-153">Windows Server 2003</span></span>



| <span data-ttu-id="7f53c-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="7f53c-154">Entry</span></span> | <span data-ttu-id="7f53c-155">Valor</span><span class="sxs-lookup"><span data-stu-id="7f53c-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7f53c-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="7f53c-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7f53c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f53c-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7f53c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f53c-158">System-Only</span></span>            | <span data-ttu-id="7f53c-159">Falso</span><span class="sxs-lookup"><span data-stu-id="7f53c-159">False</span></span>                                        |
| <span data-ttu-id="7f53c-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7f53c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="7f53c-161">True</span><span class="sxs-lookup"><span data-stu-id="7f53c-161">True</span></span>                                         |
| <span data-ttu-id="7f53c-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="7f53c-162">Is Indexed</span></span>             | <span data-ttu-id="7f53c-163">Falso</span><span class="sxs-lookup"><span data-stu-id="7f53c-163">False</span></span>                                        |
| <span data-ttu-id="7f53c-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7f53c-164">In Global Catalog</span></span>      | <span data-ttu-id="7f53c-165">Falso</span><span class="sxs-lookup"><span data-stu-id="7f53c-165">False</span></span>                                        |
| <span data-ttu-id="7f53c-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7f53c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f53c-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7f53c-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7f53c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f53c-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7f53c-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f53c-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7f53c-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f53c-170">Search-Flags</span></span>           | <span data-ttu-id="7f53c-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f53c-171">0x00000000</span></span>                                   |
| <span data-ttu-id="7f53c-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f53c-172">System-Flags</span></span>           | <span data-ttu-id="7f53c-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f53c-173">0x00000010</span></span>                                   |
| <span data-ttu-id="7f53c-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7f53c-174">Classes used in</span></span>        | [<span data-ttu-id="7f53c-175">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="7f53c-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7f53c-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7f53c-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7f53c-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="7f53c-177">Entry</span></span> | <span data-ttu-id="7f53c-178">Valor</span><span class="sxs-lookup"><span data-stu-id="7f53c-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7f53c-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="7f53c-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7f53c-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f53c-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7f53c-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f53c-181">System-Only</span></span>            | <span data-ttu-id="7f53c-182">Falso</span><span class="sxs-lookup"><span data-stu-id="7f53c-182">False</span></span>                                        |
| <span data-ttu-id="7f53c-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7f53c-183">Is-Single-Valued</span></span>       | <span data-ttu-id="7f53c-184">True</span><span class="sxs-lookup"><span data-stu-id="7f53c-184">True</span></span>                                         |
| <span data-ttu-id="7f53c-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="7f53c-185">Is Indexed</span></span>             | <span data-ttu-id="7f53c-186">Falso</span><span class="sxs-lookup"><span data-stu-id="7f53c-186">False</span></span>                                        |
| <span data-ttu-id="7f53c-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7f53c-187">In Global Catalog</span></span>      | <span data-ttu-id="7f53c-188">Falso</span><span class="sxs-lookup"><span data-stu-id="7f53c-188">False</span></span>                                        |
| <span data-ttu-id="7f53c-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7f53c-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f53c-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7f53c-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7f53c-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f53c-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7f53c-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f53c-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7f53c-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f53c-193">Search-Flags</span></span>           | <span data-ttu-id="7f53c-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f53c-194">0x00000000</span></span>                                   |
| <span data-ttu-id="7f53c-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f53c-195">System-Flags</span></span>           | <span data-ttu-id="7f53c-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f53c-196">0x00000010</span></span>                                   |
| <span data-ttu-id="7f53c-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7f53c-197">Classes used in</span></span>        | [<span data-ttu-id="7f53c-198">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="7f53c-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7f53c-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f53c-199">Windows Server 2008</span></span>



| <span data-ttu-id="7f53c-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="7f53c-200">Entry</span></span> | <span data-ttu-id="7f53c-201">Valor</span><span class="sxs-lookup"><span data-stu-id="7f53c-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7f53c-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="7f53c-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7f53c-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f53c-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7f53c-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f53c-204">System-Only</span></span>            | <span data-ttu-id="7f53c-205">Falso</span><span class="sxs-lookup"><span data-stu-id="7f53c-205">False</span></span>                                        |
| <span data-ttu-id="7f53c-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7f53c-206">Is-Single-Valued</span></span>       | <span data-ttu-id="7f53c-207">True</span><span class="sxs-lookup"><span data-stu-id="7f53c-207">True</span></span>                                         |
| <span data-ttu-id="7f53c-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="7f53c-208">Is Indexed</span></span>             | <span data-ttu-id="7f53c-209">Falso</span><span class="sxs-lookup"><span data-stu-id="7f53c-209">False</span></span>                                        |
| <span data-ttu-id="7f53c-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7f53c-210">In Global Catalog</span></span>      | <span data-ttu-id="7f53c-211">Falso</span><span class="sxs-lookup"><span data-stu-id="7f53c-211">False</span></span>                                        |
| <span data-ttu-id="7f53c-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7f53c-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f53c-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7f53c-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7f53c-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f53c-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7f53c-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f53c-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7f53c-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f53c-216">Search-Flags</span></span>           | <span data-ttu-id="7f53c-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f53c-217">0x00000000</span></span>                                   |
| <span data-ttu-id="7f53c-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f53c-218">System-Flags</span></span>           | <span data-ttu-id="7f53c-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f53c-219">0x00000010</span></span>                                   |
| <span data-ttu-id="7f53c-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7f53c-220">Classes used in</span></span>        | [<span data-ttu-id="7f53c-221">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="7f53c-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7f53c-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7f53c-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7f53c-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="7f53c-223">Entry</span></span> | <span data-ttu-id="7f53c-224">Valor</span><span class="sxs-lookup"><span data-stu-id="7f53c-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7f53c-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="7f53c-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7f53c-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f53c-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7f53c-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f53c-227">System-Only</span></span>            | <span data-ttu-id="7f53c-228">Falso</span><span class="sxs-lookup"><span data-stu-id="7f53c-228">False</span></span>                                        |
| <span data-ttu-id="7f53c-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7f53c-229">Is-Single-Valued</span></span>       | <span data-ttu-id="7f53c-230">True</span><span class="sxs-lookup"><span data-stu-id="7f53c-230">True</span></span>                                         |
| <span data-ttu-id="7f53c-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="7f53c-231">Is Indexed</span></span>             | <span data-ttu-id="7f53c-232">Falso</span><span class="sxs-lookup"><span data-stu-id="7f53c-232">False</span></span>                                        |
| <span data-ttu-id="7f53c-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7f53c-233">In Global Catalog</span></span>      | <span data-ttu-id="7f53c-234">Falso</span><span class="sxs-lookup"><span data-stu-id="7f53c-234">False</span></span>                                        |
| <span data-ttu-id="7f53c-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7f53c-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f53c-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7f53c-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7f53c-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f53c-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7f53c-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f53c-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7f53c-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f53c-239">Search-Flags</span></span>           | <span data-ttu-id="7f53c-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f53c-240">0x00000000</span></span>                                   |
| <span data-ttu-id="7f53c-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f53c-241">System-Flags</span></span>           | <span data-ttu-id="7f53c-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f53c-242">0x00000010</span></span>                                   |
| <span data-ttu-id="7f53c-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7f53c-243">Classes used in</span></span>        | [<span data-ttu-id="7f53c-244">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="7f53c-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7f53c-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7f53c-245">Windows Server 2012</span></span>



| <span data-ttu-id="7f53c-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="7f53c-246">Entry</span></span> | <span data-ttu-id="7f53c-247">Valor</span><span class="sxs-lookup"><span data-stu-id="7f53c-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7f53c-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="7f53c-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7f53c-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f53c-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7f53c-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f53c-250">System-Only</span></span>            | <span data-ttu-id="7f53c-251">Falso</span><span class="sxs-lookup"><span data-stu-id="7f53c-251">False</span></span>                                        |
| <span data-ttu-id="7f53c-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7f53c-252">Is-Single-Valued</span></span>       | <span data-ttu-id="7f53c-253">True</span><span class="sxs-lookup"><span data-stu-id="7f53c-253">True</span></span>                                         |
| <span data-ttu-id="7f53c-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="7f53c-254">Is Indexed</span></span>             | <span data-ttu-id="7f53c-255">Falso</span><span class="sxs-lookup"><span data-stu-id="7f53c-255">False</span></span>                                        |
| <span data-ttu-id="7f53c-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7f53c-256">In Global Catalog</span></span>      | <span data-ttu-id="7f53c-257">Falso</span><span class="sxs-lookup"><span data-stu-id="7f53c-257">False</span></span>                                        |
| <span data-ttu-id="7f53c-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7f53c-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f53c-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7f53c-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7f53c-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f53c-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7f53c-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f53c-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7f53c-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f53c-262">Search-Flags</span></span>           | <span data-ttu-id="7f53c-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f53c-263">0x00000000</span></span>                                   |
| <span data-ttu-id="7f53c-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f53c-264">System-Flags</span></span>           | <span data-ttu-id="7f53c-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f53c-265">0x00000010</span></span>                                   |
| <span data-ttu-id="7f53c-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7f53c-266">Classes used in</span></span>        | [<span data-ttu-id="7f53c-267">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="7f53c-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





