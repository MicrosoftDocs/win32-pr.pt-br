---
title: Print-Spooling atributo
description: Uma cadeia de caracteres que representa o tipo de spool de impressora.
ms.assetid: cbfa0a3f-dec1-4b7b-855d-426733bcd7f2
ms.tgt_platform: multiple
keywords:
- Esquema de Print-Spooling do atributo AD
- Esquema de AD do atributo de hiperspooling
topic_type:
- apiref
api_name:
- Print-Spooling
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c669a00ab523051d3708cc485f65ba484df003c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825290"
---
# <a name="print-spooling-attribute"></a><span data-ttu-id="b01a1-105">Print-Spooling atributo</span><span class="sxs-lookup"><span data-stu-id="b01a1-105">Print-Spooling attribute</span></span>

<span data-ttu-id="b01a1-106">Uma cadeia de caracteres que representa o tipo de spool de impressora.</span><span class="sxs-lookup"><span data-stu-id="b01a1-106">A string that represents the type of printer spooling.</span></span>



| <span data-ttu-id="b01a1-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="b01a1-107">Entry</span></span> | <span data-ttu-id="b01a1-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b01a1-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------|
| <span data-ttu-id="b01a1-109">CN</span><span class="sxs-lookup"><span data-stu-id="b01a1-109">CN</span></span>                | <span data-ttu-id="b01a1-110">Print-Spooling</span><span class="sxs-lookup"><span data-stu-id="b01a1-110">Print-Spooling</span></span>                                                       |
| <span data-ttu-id="b01a1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b01a1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b01a1-112">Spooling</span><span class="sxs-lookup"><span data-stu-id="b01a1-112">printSpooling</span></span>                                                        |
| <span data-ttu-id="b01a1-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b01a1-113">Size</span></span>              | <span data-ttu-id="b01a1-114">Valores possíveis: Redirect, PrintWhileSpooling, PrintAfterSpooled.</span><span class="sxs-lookup"><span data-stu-id="b01a1-114">Possible values: PrintDirect, PrintWhileSpooling, PrintAfterSpooled.</span></span> |
| <span data-ttu-id="b01a1-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="b01a1-115">Update Privilege</span></span>  | \-                                                                   |
| <span data-ttu-id="b01a1-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="b01a1-116">Update Frequency</span></span>  | \-                                                                   |
| <span data-ttu-id="b01a1-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b01a1-117">Attribute-Id</span></span>      | <span data-ttu-id="b01a1-118">1.2.840.113556.1.4.274</span><span class="sxs-lookup"><span data-stu-id="b01a1-118">1.2.840.113556.1.4.274</span></span>                                               |
| <span data-ttu-id="b01a1-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b01a1-119">System-Id-Guid</span></span>    | <span data-ttu-id="b01a1-120">ba305f6c-47e3-11d0-a1a6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="b01a1-120">ba305f6c-47e3-11d0-a1a6-00c04fd930c9</span></span>                                 |
| <span data-ttu-id="b01a1-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="b01a1-121">Syntax</span></span>            | [<span data-ttu-id="b01a1-122">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b01a1-122">**String(Unicode)**</span></span>](s-string-unicode.md)                          |



## <a name="implementations"></a><span data-ttu-id="b01a1-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="b01a1-123">Implementations</span></span>

-   [<span data-ttu-id="b01a1-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b01a1-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b01a1-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b01a1-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b01a1-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b01a1-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b01a1-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b01a1-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b01a1-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b01a1-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b01a1-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b01a1-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b01a1-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b01a1-130">Windows 2000 Server</span></span>



| <span data-ttu-id="b01a1-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="b01a1-131">Entry</span></span> | <span data-ttu-id="b01a1-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b01a1-132">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="b01a1-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="b01a1-133">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="b01a1-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01a1-134">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="b01a1-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01a1-135">System-Only</span></span>            | <span data-ttu-id="b01a1-136">Falso</span><span class="sxs-lookup"><span data-stu-id="b01a1-136">False</span></span>                                          |
| <span data-ttu-id="b01a1-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b01a1-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b01a1-138">True</span><span class="sxs-lookup"><span data-stu-id="b01a1-138">True</span></span>                                           |
| <span data-ttu-id="b01a1-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="b01a1-139">Is Indexed</span></span>             | <span data-ttu-id="b01a1-140">Falso</span><span class="sxs-lookup"><span data-stu-id="b01a1-140">False</span></span>                                          |
| <span data-ttu-id="b01a1-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b01a1-141">In Global Catalog</span></span>      | <span data-ttu-id="b01a1-142">Falso</span><span class="sxs-lookup"><span data-stu-id="b01a1-142">False</span></span>                                          |
| <span data-ttu-id="b01a1-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b01a1-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01a1-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b01a1-144">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="b01a1-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01a1-145">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="b01a1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01a1-146">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="b01a1-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01a1-147">Search-Flags</span></span>           | <span data-ttu-id="b01a1-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01a1-148">0x00000000</span></span>                                     |
| <span data-ttu-id="b01a1-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01a1-149">System-Flags</span></span>           | <span data-ttu-id="b01a1-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01a1-150">0x00000010</span></span>                                     |
| <span data-ttu-id="b01a1-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b01a1-151">Classes used in</span></span>        | [<span data-ttu-id="b01a1-152">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="b01a1-152">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b01a1-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b01a1-153">Windows Server 2003</span></span>



| <span data-ttu-id="b01a1-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="b01a1-154">Entry</span></span> | <span data-ttu-id="b01a1-155">Valor</span><span class="sxs-lookup"><span data-stu-id="b01a1-155">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="b01a1-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="b01a1-156">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="b01a1-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01a1-157">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="b01a1-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01a1-158">System-Only</span></span>            | <span data-ttu-id="b01a1-159">Falso</span><span class="sxs-lookup"><span data-stu-id="b01a1-159">False</span></span>                                          |
| <span data-ttu-id="b01a1-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b01a1-160">Is-Single-Valued</span></span>       | <span data-ttu-id="b01a1-161">True</span><span class="sxs-lookup"><span data-stu-id="b01a1-161">True</span></span>                                           |
| <span data-ttu-id="b01a1-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="b01a1-162">Is Indexed</span></span>             | <span data-ttu-id="b01a1-163">Falso</span><span class="sxs-lookup"><span data-stu-id="b01a1-163">False</span></span>                                          |
| <span data-ttu-id="b01a1-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b01a1-164">In Global Catalog</span></span>      | <span data-ttu-id="b01a1-165">Falso</span><span class="sxs-lookup"><span data-stu-id="b01a1-165">False</span></span>                                          |
| <span data-ttu-id="b01a1-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b01a1-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01a1-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b01a1-167">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="b01a1-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01a1-168">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="b01a1-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01a1-169">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="b01a1-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01a1-170">Search-Flags</span></span>           | <span data-ttu-id="b01a1-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01a1-171">0x00000000</span></span>                                     |
| <span data-ttu-id="b01a1-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01a1-172">System-Flags</span></span>           | <span data-ttu-id="b01a1-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01a1-173">0x00000010</span></span>                                     |
| <span data-ttu-id="b01a1-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b01a1-174">Classes used in</span></span>        | [<span data-ttu-id="b01a1-175">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="b01a1-175">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b01a1-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b01a1-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b01a1-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="b01a1-177">Entry</span></span> | <span data-ttu-id="b01a1-178">Valor</span><span class="sxs-lookup"><span data-stu-id="b01a1-178">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="b01a1-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="b01a1-179">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="b01a1-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01a1-180">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="b01a1-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01a1-181">System-Only</span></span>            | <span data-ttu-id="b01a1-182">Falso</span><span class="sxs-lookup"><span data-stu-id="b01a1-182">False</span></span>                                          |
| <span data-ttu-id="b01a1-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b01a1-183">Is-Single-Valued</span></span>       | <span data-ttu-id="b01a1-184">True</span><span class="sxs-lookup"><span data-stu-id="b01a1-184">True</span></span>                                           |
| <span data-ttu-id="b01a1-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="b01a1-185">Is Indexed</span></span>             | <span data-ttu-id="b01a1-186">Falso</span><span class="sxs-lookup"><span data-stu-id="b01a1-186">False</span></span>                                          |
| <span data-ttu-id="b01a1-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b01a1-187">In Global Catalog</span></span>      | <span data-ttu-id="b01a1-188">Falso</span><span class="sxs-lookup"><span data-stu-id="b01a1-188">False</span></span>                                          |
| <span data-ttu-id="b01a1-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b01a1-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01a1-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b01a1-190">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="b01a1-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01a1-191">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="b01a1-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01a1-192">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="b01a1-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01a1-193">Search-Flags</span></span>           | <span data-ttu-id="b01a1-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01a1-194">0x00000000</span></span>                                     |
| <span data-ttu-id="b01a1-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01a1-195">System-Flags</span></span>           | <span data-ttu-id="b01a1-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01a1-196">0x00000010</span></span>                                     |
| <span data-ttu-id="b01a1-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b01a1-197">Classes used in</span></span>        | [<span data-ttu-id="b01a1-198">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="b01a1-198">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b01a1-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b01a1-199">Windows Server 2008</span></span>



| <span data-ttu-id="b01a1-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="b01a1-200">Entry</span></span> | <span data-ttu-id="b01a1-201">Valor</span><span class="sxs-lookup"><span data-stu-id="b01a1-201">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="b01a1-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="b01a1-202">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="b01a1-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01a1-203">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="b01a1-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01a1-204">System-Only</span></span>            | <span data-ttu-id="b01a1-205">Falso</span><span class="sxs-lookup"><span data-stu-id="b01a1-205">False</span></span>                                          |
| <span data-ttu-id="b01a1-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b01a1-206">Is-Single-Valued</span></span>       | <span data-ttu-id="b01a1-207">True</span><span class="sxs-lookup"><span data-stu-id="b01a1-207">True</span></span>                                           |
| <span data-ttu-id="b01a1-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="b01a1-208">Is Indexed</span></span>             | <span data-ttu-id="b01a1-209">Falso</span><span class="sxs-lookup"><span data-stu-id="b01a1-209">False</span></span>                                          |
| <span data-ttu-id="b01a1-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b01a1-210">In Global Catalog</span></span>      | <span data-ttu-id="b01a1-211">Falso</span><span class="sxs-lookup"><span data-stu-id="b01a1-211">False</span></span>                                          |
| <span data-ttu-id="b01a1-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b01a1-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01a1-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b01a1-213">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="b01a1-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01a1-214">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="b01a1-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01a1-215">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="b01a1-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01a1-216">Search-Flags</span></span>           | <span data-ttu-id="b01a1-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01a1-217">0x00000000</span></span>                                     |
| <span data-ttu-id="b01a1-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01a1-218">System-Flags</span></span>           | <span data-ttu-id="b01a1-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01a1-219">0x00000010</span></span>                                     |
| <span data-ttu-id="b01a1-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b01a1-220">Classes used in</span></span>        | [<span data-ttu-id="b01a1-221">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="b01a1-221">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b01a1-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b01a1-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b01a1-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="b01a1-223">Entry</span></span> | <span data-ttu-id="b01a1-224">Valor</span><span class="sxs-lookup"><span data-stu-id="b01a1-224">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="b01a1-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="b01a1-225">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="b01a1-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01a1-226">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="b01a1-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01a1-227">System-Only</span></span>            | <span data-ttu-id="b01a1-228">Falso</span><span class="sxs-lookup"><span data-stu-id="b01a1-228">False</span></span>                                          |
| <span data-ttu-id="b01a1-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b01a1-229">Is-Single-Valued</span></span>       | <span data-ttu-id="b01a1-230">True</span><span class="sxs-lookup"><span data-stu-id="b01a1-230">True</span></span>                                           |
| <span data-ttu-id="b01a1-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="b01a1-231">Is Indexed</span></span>             | <span data-ttu-id="b01a1-232">Falso</span><span class="sxs-lookup"><span data-stu-id="b01a1-232">False</span></span>                                          |
| <span data-ttu-id="b01a1-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b01a1-233">In Global Catalog</span></span>      | <span data-ttu-id="b01a1-234">Falso</span><span class="sxs-lookup"><span data-stu-id="b01a1-234">False</span></span>                                          |
| <span data-ttu-id="b01a1-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b01a1-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01a1-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b01a1-236">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="b01a1-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01a1-237">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="b01a1-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01a1-238">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="b01a1-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01a1-239">Search-Flags</span></span>           | <span data-ttu-id="b01a1-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01a1-240">0x00000000</span></span>                                     |
| <span data-ttu-id="b01a1-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01a1-241">System-Flags</span></span>           | <span data-ttu-id="b01a1-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01a1-242">0x00000010</span></span>                                     |
| <span data-ttu-id="b01a1-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b01a1-243">Classes used in</span></span>        | [<span data-ttu-id="b01a1-244">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="b01a1-244">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b01a1-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b01a1-245">Windows Server 2012</span></span>



| <span data-ttu-id="b01a1-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="b01a1-246">Entry</span></span> | <span data-ttu-id="b01a1-247">Valor</span><span class="sxs-lookup"><span data-stu-id="b01a1-247">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="b01a1-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="b01a1-248">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="b01a1-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b01a1-249">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="b01a1-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="b01a1-250">System-Only</span></span>            | <span data-ttu-id="b01a1-251">Falso</span><span class="sxs-lookup"><span data-stu-id="b01a1-251">False</span></span>                                          |
| <span data-ttu-id="b01a1-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b01a1-252">Is-Single-Valued</span></span>       | <span data-ttu-id="b01a1-253">True</span><span class="sxs-lookup"><span data-stu-id="b01a1-253">True</span></span>                                           |
| <span data-ttu-id="b01a1-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="b01a1-254">Is Indexed</span></span>             | <span data-ttu-id="b01a1-255">Falso</span><span class="sxs-lookup"><span data-stu-id="b01a1-255">False</span></span>                                          |
| <span data-ttu-id="b01a1-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b01a1-256">In Global Catalog</span></span>      | <span data-ttu-id="b01a1-257">Falso</span><span class="sxs-lookup"><span data-stu-id="b01a1-257">False</span></span>                                          |
| <span data-ttu-id="b01a1-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b01a1-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="b01a1-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b01a1-259">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="b01a1-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b01a1-260">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="b01a1-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b01a1-261">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="b01a1-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b01a1-262">Search-Flags</span></span>           | <span data-ttu-id="b01a1-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b01a1-263">0x00000000</span></span>                                     |
| <span data-ttu-id="b01a1-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b01a1-264">System-Flags</span></span>           | <span data-ttu-id="b01a1-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b01a1-265">0x00000010</span></span>                                     |
| <span data-ttu-id="b01a1-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b01a1-266">Classes used in</span></span>        | [<span data-ttu-id="b01a1-267">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="b01a1-267">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





