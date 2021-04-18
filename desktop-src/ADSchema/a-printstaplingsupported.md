---
title: Grampeamento de impressão-atributo com suporte
description: TRUE se a impressora oferecer suporte a grampeamento. Fornecido pelo driver.
ms.assetid: c0d1cbc5-7657-45a8-b154-a67f57386f52
ms.tgt_platform: multiple
keywords:
- Grampeamento de impressão-esquema de anúncio de atributo com suporte
- Esquema de AD do atributo printStaplingSupported
topic_type:
- apiref
api_name:
- Print-Stapling-Supported
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12303d9a18f267ec4eaef3a33dc8ec7350967aa6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105756053"
---
# <a name="print-stapling-supported-attribute"></a><span data-ttu-id="c5357-106">Grampeamento de impressão-atributo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5357-106">Print-Stapling-Supported attribute</span></span>

<span data-ttu-id="c5357-107">**True** se a impressora oferecer suporte a grampeamento.</span><span class="sxs-lookup"><span data-stu-id="c5357-107">**TRUE** if the printer supports stapling.</span></span> <span data-ttu-id="c5357-108">Fornecido pelo driver.</span><span class="sxs-lookup"><span data-stu-id="c5357-108">Supplied by the driver.</span></span>



| <span data-ttu-id="c5357-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="c5357-109">Entry</span></span> | <span data-ttu-id="c5357-110">Valor</span><span class="sxs-lookup"><span data-stu-id="c5357-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c5357-111">CN</span><span class="sxs-lookup"><span data-stu-id="c5357-111">CN</span></span>                | <span data-ttu-id="c5357-112">Grampeamento de impressão-com suporte</span><span class="sxs-lookup"><span data-stu-id="c5357-112">Print-Stapling-Supported</span></span>             |
| <span data-ttu-id="c5357-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c5357-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c5357-114">printStaplingSupported</span><span class="sxs-lookup"><span data-stu-id="c5357-114">printStaplingSupported</span></span>               |
| <span data-ttu-id="c5357-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c5357-115">Size</span></span>              | <span data-ttu-id="c5357-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="c5357-116">4 bytes</span></span>                              |
| <span data-ttu-id="c5357-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="c5357-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c5357-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="c5357-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c5357-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c5357-119">Attribute-Id</span></span>      | <span data-ttu-id="c5357-120">1.2.840.113556.1.4.281</span><span class="sxs-lookup"><span data-stu-id="c5357-120">1.2.840.113556.1.4.281</span></span>               |
| <span data-ttu-id="c5357-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c5357-121">System-Id-Guid</span></span>    | <span data-ttu-id="c5357-122">ba305f73-47e3-11d0-a1a6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="c5357-122">ba305f73-47e3-11d0-a1a6-00c04fd930c9</span></span> |
| <span data-ttu-id="c5357-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5357-123">Syntax</span></span>            | [<span data-ttu-id="c5357-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c5357-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="c5357-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="c5357-125">Implementations</span></span>

-   [<span data-ttu-id="c5357-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c5357-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c5357-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c5357-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c5357-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c5357-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c5357-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c5357-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c5357-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c5357-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c5357-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c5357-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c5357-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c5357-132">Windows 2000 Server</span></span>



| <span data-ttu-id="c5357-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="c5357-133">Entry</span></span> | <span data-ttu-id="c5357-134">Valor</span><span class="sxs-lookup"><span data-stu-id="c5357-134">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="c5357-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="c5357-135">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="c5357-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5357-136">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="c5357-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5357-137">System-Only</span></span>            | <span data-ttu-id="c5357-138">Falso</span><span class="sxs-lookup"><span data-stu-id="c5357-138">False</span></span>                                          |
| <span data-ttu-id="c5357-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c5357-139">Is-Single-Valued</span></span>       | <span data-ttu-id="c5357-140">True</span><span class="sxs-lookup"><span data-stu-id="c5357-140">True</span></span>                                           |
| <span data-ttu-id="c5357-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="c5357-141">Is Indexed</span></span>             | <span data-ttu-id="c5357-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c5357-142">False</span></span>                                          |
| <span data-ttu-id="c5357-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c5357-143">In Global Catalog</span></span>      | <span data-ttu-id="c5357-144">True</span><span class="sxs-lookup"><span data-stu-id="c5357-144">True</span></span>                                           |
| <span data-ttu-id="c5357-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c5357-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5357-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c5357-146">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="c5357-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5357-147">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="c5357-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5357-148">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="c5357-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5357-149">Search-Flags</span></span>           | <span data-ttu-id="c5357-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5357-150">0x00000000</span></span>                                     |
| <span data-ttu-id="c5357-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5357-151">System-Flags</span></span>           | <span data-ttu-id="c5357-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5357-152">0x00000010</span></span>                                     |
| <span data-ttu-id="c5357-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c5357-153">Classes used in</span></span>        | [<span data-ttu-id="c5357-154">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="c5357-154">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c5357-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c5357-155">Windows Server 2003</span></span>



| <span data-ttu-id="c5357-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="c5357-156">Entry</span></span> | <span data-ttu-id="c5357-157">Valor</span><span class="sxs-lookup"><span data-stu-id="c5357-157">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="c5357-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="c5357-158">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="c5357-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5357-159">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="c5357-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5357-160">System-Only</span></span>            | <span data-ttu-id="c5357-161">Falso</span><span class="sxs-lookup"><span data-stu-id="c5357-161">False</span></span>                                          |
| <span data-ttu-id="c5357-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c5357-162">Is-Single-Valued</span></span>       | <span data-ttu-id="c5357-163">True</span><span class="sxs-lookup"><span data-stu-id="c5357-163">True</span></span>                                           |
| <span data-ttu-id="c5357-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="c5357-164">Is Indexed</span></span>             | <span data-ttu-id="c5357-165">Falso</span><span class="sxs-lookup"><span data-stu-id="c5357-165">False</span></span>                                          |
| <span data-ttu-id="c5357-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c5357-166">In Global Catalog</span></span>      | <span data-ttu-id="c5357-167">True</span><span class="sxs-lookup"><span data-stu-id="c5357-167">True</span></span>                                           |
| <span data-ttu-id="c5357-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c5357-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5357-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c5357-169">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="c5357-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5357-170">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="c5357-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5357-171">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="c5357-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5357-172">Search-Flags</span></span>           | <span data-ttu-id="c5357-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5357-173">0x00000000</span></span>                                     |
| <span data-ttu-id="c5357-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5357-174">System-Flags</span></span>           | <span data-ttu-id="c5357-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5357-175">0x00000010</span></span>                                     |
| <span data-ttu-id="c5357-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c5357-176">Classes used in</span></span>        | [<span data-ttu-id="c5357-177">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="c5357-177">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c5357-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c5357-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c5357-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="c5357-179">Entry</span></span> | <span data-ttu-id="c5357-180">Valor</span><span class="sxs-lookup"><span data-stu-id="c5357-180">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="c5357-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="c5357-181">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="c5357-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5357-182">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="c5357-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5357-183">System-Only</span></span>            | <span data-ttu-id="c5357-184">Falso</span><span class="sxs-lookup"><span data-stu-id="c5357-184">False</span></span>                                          |
| <span data-ttu-id="c5357-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c5357-185">Is-Single-Valued</span></span>       | <span data-ttu-id="c5357-186">True</span><span class="sxs-lookup"><span data-stu-id="c5357-186">True</span></span>                                           |
| <span data-ttu-id="c5357-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="c5357-187">Is Indexed</span></span>             | <span data-ttu-id="c5357-188">Falso</span><span class="sxs-lookup"><span data-stu-id="c5357-188">False</span></span>                                          |
| <span data-ttu-id="c5357-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c5357-189">In Global Catalog</span></span>      | <span data-ttu-id="c5357-190">True</span><span class="sxs-lookup"><span data-stu-id="c5357-190">True</span></span>                                           |
| <span data-ttu-id="c5357-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c5357-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5357-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c5357-192">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="c5357-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5357-193">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="c5357-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5357-194">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="c5357-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5357-195">Search-Flags</span></span>           | <span data-ttu-id="c5357-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5357-196">0x00000000</span></span>                                     |
| <span data-ttu-id="c5357-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5357-197">System-Flags</span></span>           | <span data-ttu-id="c5357-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5357-198">0x00000010</span></span>                                     |
| <span data-ttu-id="c5357-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c5357-199">Classes used in</span></span>        | [<span data-ttu-id="c5357-200">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="c5357-200">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c5357-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5357-201">Windows Server 2008</span></span>



| <span data-ttu-id="c5357-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="c5357-202">Entry</span></span> | <span data-ttu-id="c5357-203">Valor</span><span class="sxs-lookup"><span data-stu-id="c5357-203">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="c5357-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="c5357-204">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="c5357-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5357-205">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="c5357-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5357-206">System-Only</span></span>            | <span data-ttu-id="c5357-207">Falso</span><span class="sxs-lookup"><span data-stu-id="c5357-207">False</span></span>                                          |
| <span data-ttu-id="c5357-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c5357-208">Is-Single-Valued</span></span>       | <span data-ttu-id="c5357-209">True</span><span class="sxs-lookup"><span data-stu-id="c5357-209">True</span></span>                                           |
| <span data-ttu-id="c5357-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="c5357-210">Is Indexed</span></span>             | <span data-ttu-id="c5357-211">Falso</span><span class="sxs-lookup"><span data-stu-id="c5357-211">False</span></span>                                          |
| <span data-ttu-id="c5357-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c5357-212">In Global Catalog</span></span>      | <span data-ttu-id="c5357-213">True</span><span class="sxs-lookup"><span data-stu-id="c5357-213">True</span></span>                                           |
| <span data-ttu-id="c5357-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c5357-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5357-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c5357-215">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="c5357-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5357-216">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="c5357-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5357-217">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="c5357-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5357-218">Search-Flags</span></span>           | <span data-ttu-id="c5357-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5357-219">0x00000000</span></span>                                     |
| <span data-ttu-id="c5357-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5357-220">System-Flags</span></span>           | <span data-ttu-id="c5357-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5357-221">0x00000010</span></span>                                     |
| <span data-ttu-id="c5357-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c5357-222">Classes used in</span></span>        | [<span data-ttu-id="c5357-223">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="c5357-223">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c5357-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c5357-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c5357-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="c5357-225">Entry</span></span> | <span data-ttu-id="c5357-226">Valor</span><span class="sxs-lookup"><span data-stu-id="c5357-226">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="c5357-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="c5357-227">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="c5357-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5357-228">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="c5357-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5357-229">System-Only</span></span>            | <span data-ttu-id="c5357-230">Falso</span><span class="sxs-lookup"><span data-stu-id="c5357-230">False</span></span>                                          |
| <span data-ttu-id="c5357-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c5357-231">Is-Single-Valued</span></span>       | <span data-ttu-id="c5357-232">True</span><span class="sxs-lookup"><span data-stu-id="c5357-232">True</span></span>                                           |
| <span data-ttu-id="c5357-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="c5357-233">Is Indexed</span></span>             | <span data-ttu-id="c5357-234">Falso</span><span class="sxs-lookup"><span data-stu-id="c5357-234">False</span></span>                                          |
| <span data-ttu-id="c5357-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c5357-235">In Global Catalog</span></span>      | <span data-ttu-id="c5357-236">True</span><span class="sxs-lookup"><span data-stu-id="c5357-236">True</span></span>                                           |
| <span data-ttu-id="c5357-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c5357-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5357-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c5357-238">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="c5357-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5357-239">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="c5357-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5357-240">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="c5357-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5357-241">Search-Flags</span></span>           | <span data-ttu-id="c5357-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5357-242">0x00000000</span></span>                                     |
| <span data-ttu-id="c5357-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5357-243">System-Flags</span></span>           | <span data-ttu-id="c5357-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5357-244">0x00000010</span></span>                                     |
| <span data-ttu-id="c5357-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c5357-245">Classes used in</span></span>        | [<span data-ttu-id="c5357-246">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="c5357-246">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c5357-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c5357-247">Windows Server 2012</span></span>



| <span data-ttu-id="c5357-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="c5357-248">Entry</span></span> | <span data-ttu-id="c5357-249">Valor</span><span class="sxs-lookup"><span data-stu-id="c5357-249">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="c5357-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="c5357-250">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="c5357-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5357-251">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="c5357-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5357-252">System-Only</span></span>            | <span data-ttu-id="c5357-253">Falso</span><span class="sxs-lookup"><span data-stu-id="c5357-253">False</span></span>                                          |
| <span data-ttu-id="c5357-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c5357-254">Is-Single-Valued</span></span>       | <span data-ttu-id="c5357-255">True</span><span class="sxs-lookup"><span data-stu-id="c5357-255">True</span></span>                                           |
| <span data-ttu-id="c5357-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="c5357-256">Is Indexed</span></span>             | <span data-ttu-id="c5357-257">Falso</span><span class="sxs-lookup"><span data-stu-id="c5357-257">False</span></span>                                          |
| <span data-ttu-id="c5357-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c5357-258">In Global Catalog</span></span>      | <span data-ttu-id="c5357-259">True</span><span class="sxs-lookup"><span data-stu-id="c5357-259">True</span></span>                                           |
| <span data-ttu-id="c5357-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c5357-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5357-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c5357-261">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="c5357-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5357-262">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="c5357-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5357-263">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="c5357-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5357-264">Search-Flags</span></span>           | <span data-ttu-id="c5357-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5357-265">0x00000000</span></span>                                     |
| <span data-ttu-id="c5357-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5357-266">System-Flags</span></span>           | <span data-ttu-id="c5357-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5357-267">0x00000010</span></span>                                     |
| <span data-ttu-id="c5357-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c5357-268">Classes used in</span></span>        | [<span data-ttu-id="c5357-269">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="c5357-269">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





