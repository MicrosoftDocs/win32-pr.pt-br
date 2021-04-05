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
# <a name="print-spooling-attribute"></a><span data-ttu-id="83b0e-105">Print-Spooling atributo</span><span class="sxs-lookup"><span data-stu-id="83b0e-105">Print-Spooling attribute</span></span>

<span data-ttu-id="83b0e-106">Uma cadeia de caracteres que representa o tipo de spool de impressora.</span><span class="sxs-lookup"><span data-stu-id="83b0e-106">A string that represents the type of printer spooling.</span></span>



| <span data-ttu-id="83b0e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="83b0e-107">Entry</span></span> | <span data-ttu-id="83b0e-108">Valor</span><span class="sxs-lookup"><span data-stu-id="83b0e-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------|
| <span data-ttu-id="83b0e-109">CN</span><span class="sxs-lookup"><span data-stu-id="83b0e-109">CN</span></span>                | <span data-ttu-id="83b0e-110">Print-Spooling</span><span class="sxs-lookup"><span data-stu-id="83b0e-110">Print-Spooling</span></span>                                                       |
| <span data-ttu-id="83b0e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="83b0e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="83b0e-112">Spooling</span><span class="sxs-lookup"><span data-stu-id="83b0e-112">printSpooling</span></span>                                                        |
| <span data-ttu-id="83b0e-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="83b0e-113">Size</span></span>              | <span data-ttu-id="83b0e-114">Valores possíveis: Redirect, PrintWhileSpooling, PrintAfterSpooled.</span><span class="sxs-lookup"><span data-stu-id="83b0e-114">Possible values: PrintDirect, PrintWhileSpooling, PrintAfterSpooled.</span></span> |
| <span data-ttu-id="83b0e-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="83b0e-115">Update Privilege</span></span>  | \-                                                                   |
| <span data-ttu-id="83b0e-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="83b0e-116">Update Frequency</span></span>  | \-                                                                   |
| <span data-ttu-id="83b0e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="83b0e-117">Attribute-Id</span></span>      | <span data-ttu-id="83b0e-118">1.2.840.113556.1.4.274</span><span class="sxs-lookup"><span data-stu-id="83b0e-118">1.2.840.113556.1.4.274</span></span>                                               |
| <span data-ttu-id="83b0e-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="83b0e-119">System-Id-Guid</span></span>    | <span data-ttu-id="83b0e-120">ba305f6c-47e3-11d0-a1a6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="83b0e-120">ba305f6c-47e3-11d0-a1a6-00c04fd930c9</span></span>                                 |
| <span data-ttu-id="83b0e-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="83b0e-121">Syntax</span></span>            | [<span data-ttu-id="83b0e-122">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="83b0e-122">**String(Unicode)**</span></span>](s-string-unicode.md)                          |



## <a name="implementations"></a><span data-ttu-id="83b0e-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="83b0e-123">Implementations</span></span>

-   [<span data-ttu-id="83b0e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="83b0e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="83b0e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="83b0e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="83b0e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="83b0e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="83b0e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="83b0e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="83b0e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="83b0e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="83b0e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="83b0e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="83b0e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="83b0e-130">Windows 2000 Server</span></span>



| <span data-ttu-id="83b0e-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="83b0e-131">Entry</span></span> | <span data-ttu-id="83b0e-132">Valor</span><span class="sxs-lookup"><span data-stu-id="83b0e-132">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="83b0e-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="83b0e-133">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="83b0e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="83b0e-134">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="83b0e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="83b0e-135">System-Only</span></span>            | <span data-ttu-id="83b0e-136">Falso</span><span class="sxs-lookup"><span data-stu-id="83b0e-136">False</span></span>                                          |
| <span data-ttu-id="83b0e-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="83b0e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="83b0e-138">True</span><span class="sxs-lookup"><span data-stu-id="83b0e-138">True</span></span>                                           |
| <span data-ttu-id="83b0e-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="83b0e-139">Is Indexed</span></span>             | <span data-ttu-id="83b0e-140">Falso</span><span class="sxs-lookup"><span data-stu-id="83b0e-140">False</span></span>                                          |
| <span data-ttu-id="83b0e-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="83b0e-141">In Global Catalog</span></span>      | <span data-ttu-id="83b0e-142">Falso</span><span class="sxs-lookup"><span data-stu-id="83b0e-142">False</span></span>                                          |
| <span data-ttu-id="83b0e-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="83b0e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="83b0e-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="83b0e-144">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="83b0e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="83b0e-145">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="83b0e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="83b0e-146">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="83b0e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="83b0e-147">Search-Flags</span></span>           | <span data-ttu-id="83b0e-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="83b0e-148">0x00000000</span></span>                                     |
| <span data-ttu-id="83b0e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="83b0e-149">System-Flags</span></span>           | <span data-ttu-id="83b0e-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="83b0e-150">0x00000010</span></span>                                     |
| <span data-ttu-id="83b0e-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="83b0e-151">Classes used in</span></span>        | [<span data-ttu-id="83b0e-152">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="83b0e-152">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="83b0e-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="83b0e-153">Windows Server 2003</span></span>



| <span data-ttu-id="83b0e-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="83b0e-154">Entry</span></span> | <span data-ttu-id="83b0e-155">Valor</span><span class="sxs-lookup"><span data-stu-id="83b0e-155">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="83b0e-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="83b0e-156">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="83b0e-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="83b0e-157">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="83b0e-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="83b0e-158">System-Only</span></span>            | <span data-ttu-id="83b0e-159">Falso</span><span class="sxs-lookup"><span data-stu-id="83b0e-159">False</span></span>                                          |
| <span data-ttu-id="83b0e-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="83b0e-160">Is-Single-Valued</span></span>       | <span data-ttu-id="83b0e-161">True</span><span class="sxs-lookup"><span data-stu-id="83b0e-161">True</span></span>                                           |
| <span data-ttu-id="83b0e-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="83b0e-162">Is Indexed</span></span>             | <span data-ttu-id="83b0e-163">Falso</span><span class="sxs-lookup"><span data-stu-id="83b0e-163">False</span></span>                                          |
| <span data-ttu-id="83b0e-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="83b0e-164">In Global Catalog</span></span>      | <span data-ttu-id="83b0e-165">Falso</span><span class="sxs-lookup"><span data-stu-id="83b0e-165">False</span></span>                                          |
| <span data-ttu-id="83b0e-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="83b0e-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="83b0e-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="83b0e-167">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="83b0e-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="83b0e-168">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="83b0e-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="83b0e-169">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="83b0e-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="83b0e-170">Search-Flags</span></span>           | <span data-ttu-id="83b0e-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="83b0e-171">0x00000000</span></span>                                     |
| <span data-ttu-id="83b0e-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="83b0e-172">System-Flags</span></span>           | <span data-ttu-id="83b0e-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="83b0e-173">0x00000010</span></span>                                     |
| <span data-ttu-id="83b0e-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="83b0e-174">Classes used in</span></span>        | [<span data-ttu-id="83b0e-175">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="83b0e-175">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="83b0e-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="83b0e-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="83b0e-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="83b0e-177">Entry</span></span> | <span data-ttu-id="83b0e-178">Valor</span><span class="sxs-lookup"><span data-stu-id="83b0e-178">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="83b0e-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="83b0e-179">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="83b0e-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="83b0e-180">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="83b0e-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="83b0e-181">System-Only</span></span>            | <span data-ttu-id="83b0e-182">Falso</span><span class="sxs-lookup"><span data-stu-id="83b0e-182">False</span></span>                                          |
| <span data-ttu-id="83b0e-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="83b0e-183">Is-Single-Valued</span></span>       | <span data-ttu-id="83b0e-184">True</span><span class="sxs-lookup"><span data-stu-id="83b0e-184">True</span></span>                                           |
| <span data-ttu-id="83b0e-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="83b0e-185">Is Indexed</span></span>             | <span data-ttu-id="83b0e-186">Falso</span><span class="sxs-lookup"><span data-stu-id="83b0e-186">False</span></span>                                          |
| <span data-ttu-id="83b0e-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="83b0e-187">In Global Catalog</span></span>      | <span data-ttu-id="83b0e-188">Falso</span><span class="sxs-lookup"><span data-stu-id="83b0e-188">False</span></span>                                          |
| <span data-ttu-id="83b0e-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="83b0e-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="83b0e-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="83b0e-190">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="83b0e-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="83b0e-191">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="83b0e-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="83b0e-192">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="83b0e-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="83b0e-193">Search-Flags</span></span>           | <span data-ttu-id="83b0e-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="83b0e-194">0x00000000</span></span>                                     |
| <span data-ttu-id="83b0e-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="83b0e-195">System-Flags</span></span>           | <span data-ttu-id="83b0e-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="83b0e-196">0x00000010</span></span>                                     |
| <span data-ttu-id="83b0e-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="83b0e-197">Classes used in</span></span>        | [<span data-ttu-id="83b0e-198">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="83b0e-198">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="83b0e-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83b0e-199">Windows Server 2008</span></span>



| <span data-ttu-id="83b0e-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="83b0e-200">Entry</span></span> | <span data-ttu-id="83b0e-201">Valor</span><span class="sxs-lookup"><span data-stu-id="83b0e-201">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="83b0e-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="83b0e-202">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="83b0e-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="83b0e-203">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="83b0e-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="83b0e-204">System-Only</span></span>            | <span data-ttu-id="83b0e-205">Falso</span><span class="sxs-lookup"><span data-stu-id="83b0e-205">False</span></span>                                          |
| <span data-ttu-id="83b0e-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="83b0e-206">Is-Single-Valued</span></span>       | <span data-ttu-id="83b0e-207">True</span><span class="sxs-lookup"><span data-stu-id="83b0e-207">True</span></span>                                           |
| <span data-ttu-id="83b0e-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="83b0e-208">Is Indexed</span></span>             | <span data-ttu-id="83b0e-209">Falso</span><span class="sxs-lookup"><span data-stu-id="83b0e-209">False</span></span>                                          |
| <span data-ttu-id="83b0e-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="83b0e-210">In Global Catalog</span></span>      | <span data-ttu-id="83b0e-211">Falso</span><span class="sxs-lookup"><span data-stu-id="83b0e-211">False</span></span>                                          |
| <span data-ttu-id="83b0e-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="83b0e-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="83b0e-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="83b0e-213">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="83b0e-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="83b0e-214">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="83b0e-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="83b0e-215">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="83b0e-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="83b0e-216">Search-Flags</span></span>           | <span data-ttu-id="83b0e-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="83b0e-217">0x00000000</span></span>                                     |
| <span data-ttu-id="83b0e-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="83b0e-218">System-Flags</span></span>           | <span data-ttu-id="83b0e-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="83b0e-219">0x00000010</span></span>                                     |
| <span data-ttu-id="83b0e-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="83b0e-220">Classes used in</span></span>        | [<span data-ttu-id="83b0e-221">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="83b0e-221">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="83b0e-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="83b0e-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="83b0e-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="83b0e-223">Entry</span></span> | <span data-ttu-id="83b0e-224">Valor</span><span class="sxs-lookup"><span data-stu-id="83b0e-224">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="83b0e-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="83b0e-225">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="83b0e-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="83b0e-226">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="83b0e-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="83b0e-227">System-Only</span></span>            | <span data-ttu-id="83b0e-228">Falso</span><span class="sxs-lookup"><span data-stu-id="83b0e-228">False</span></span>                                          |
| <span data-ttu-id="83b0e-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="83b0e-229">Is-Single-Valued</span></span>       | <span data-ttu-id="83b0e-230">True</span><span class="sxs-lookup"><span data-stu-id="83b0e-230">True</span></span>                                           |
| <span data-ttu-id="83b0e-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="83b0e-231">Is Indexed</span></span>             | <span data-ttu-id="83b0e-232">Falso</span><span class="sxs-lookup"><span data-stu-id="83b0e-232">False</span></span>                                          |
| <span data-ttu-id="83b0e-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="83b0e-233">In Global Catalog</span></span>      | <span data-ttu-id="83b0e-234">Falso</span><span class="sxs-lookup"><span data-stu-id="83b0e-234">False</span></span>                                          |
| <span data-ttu-id="83b0e-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="83b0e-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="83b0e-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="83b0e-236">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="83b0e-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="83b0e-237">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="83b0e-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="83b0e-238">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="83b0e-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="83b0e-239">Search-Flags</span></span>           | <span data-ttu-id="83b0e-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="83b0e-240">0x00000000</span></span>                                     |
| <span data-ttu-id="83b0e-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="83b0e-241">System-Flags</span></span>           | <span data-ttu-id="83b0e-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="83b0e-242">0x00000010</span></span>                                     |
| <span data-ttu-id="83b0e-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="83b0e-243">Classes used in</span></span>        | [<span data-ttu-id="83b0e-244">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="83b0e-244">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="83b0e-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="83b0e-245">Windows Server 2012</span></span>



| <span data-ttu-id="83b0e-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="83b0e-246">Entry</span></span> | <span data-ttu-id="83b0e-247">Valor</span><span class="sxs-lookup"><span data-stu-id="83b0e-247">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="83b0e-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="83b0e-248">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="83b0e-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="83b0e-249">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="83b0e-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="83b0e-250">System-Only</span></span>            | <span data-ttu-id="83b0e-251">Falso</span><span class="sxs-lookup"><span data-stu-id="83b0e-251">False</span></span>                                          |
| <span data-ttu-id="83b0e-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="83b0e-252">Is-Single-Valued</span></span>       | <span data-ttu-id="83b0e-253">True</span><span class="sxs-lookup"><span data-stu-id="83b0e-253">True</span></span>                                           |
| <span data-ttu-id="83b0e-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="83b0e-254">Is Indexed</span></span>             | <span data-ttu-id="83b0e-255">Falso</span><span class="sxs-lookup"><span data-stu-id="83b0e-255">False</span></span>                                          |
| <span data-ttu-id="83b0e-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="83b0e-256">In Global Catalog</span></span>      | <span data-ttu-id="83b0e-257">Falso</span><span class="sxs-lookup"><span data-stu-id="83b0e-257">False</span></span>                                          |
| <span data-ttu-id="83b0e-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="83b0e-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="83b0e-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="83b0e-259">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="83b0e-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="83b0e-260">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="83b0e-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="83b0e-261">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="83b0e-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="83b0e-262">Search-Flags</span></span>           | <span data-ttu-id="83b0e-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="83b0e-263">0x00000000</span></span>                                     |
| <span data-ttu-id="83b0e-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="83b0e-264">System-Flags</span></span>           | <span data-ttu-id="83b0e-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="83b0e-265">0x00000010</span></span>                                     |
| <span data-ttu-id="83b0e-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="83b0e-266">Classes used in</span></span>        | [<span data-ttu-id="83b0e-267">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="83b0e-267">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





