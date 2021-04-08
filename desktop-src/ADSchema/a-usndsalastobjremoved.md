---
title: USN-DSA-Last-obj-removeu o atributo
description: Contém o USN (número de sequência de atualização) do último objeto do sistema que foi removido de um servidor.
ms.assetid: af0afd80-fe4a-4bc6-84e3-14c2900bec93
ms.tgt_platform: multiple
keywords:
- USN-DSA-Last-obj-atributo de anúncio de atributos removidos
- Esquema de AD do atributo uSNDSALastObjRemoved
topic_type:
- apiref
api_name:
- USN-DSA-Last-Obj-Removed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbc246aa1a0f7c794b9dc0a9d2a725273a918e3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919543"
---
# <a name="usn-dsa-last-obj-removed-attribute"></a><span data-ttu-id="2d986-105">USN-DSA-Last-obj-removeu o atributo</span><span class="sxs-lookup"><span data-stu-id="2d986-105">USN-DSA-Last-Obj-Removed attribute</span></span>

<span data-ttu-id="2d986-106">Contém o USN (número de sequência de atualização) do último objeto do sistema que foi removido de um servidor.</span><span class="sxs-lookup"><span data-stu-id="2d986-106">Contains the update sequence number (USN) for the last system object that was removed from a server.</span></span>



| <span data-ttu-id="2d986-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="2d986-107">Entry</span></span> | <span data-ttu-id="2d986-108">Valor</span><span class="sxs-lookup"><span data-stu-id="2d986-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2d986-109">CN</span><span class="sxs-lookup"><span data-stu-id="2d986-109">CN</span></span>                | <span data-ttu-id="2d986-110">USN-DSA-Last-obj-removido</span><span class="sxs-lookup"><span data-stu-id="2d986-110">USN-DSA-Last-Obj-Removed</span></span>             |
| <span data-ttu-id="2d986-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2d986-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2d986-112">uSNDSALastObjRemoved</span><span class="sxs-lookup"><span data-stu-id="2d986-112">uSNDSALastObjRemoved</span></span>                 |
| <span data-ttu-id="2d986-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="2d986-113">Size</span></span>              | <span data-ttu-id="2d986-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="2d986-114">8 bytes</span></span>                              |
| <span data-ttu-id="2d986-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="2d986-115">Update Privilege</span></span>  | <span data-ttu-id="2d986-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="2d986-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="2d986-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="2d986-117">Update Frequency</span></span>  | <span data-ttu-id="2d986-118">Sempre que um objeto de diretório é alterado.</span><span class="sxs-lookup"><span data-stu-id="2d986-118">Whenever a directory object changes.</span></span> |
| <span data-ttu-id="2d986-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2d986-119">Attribute-Id</span></span>      | <span data-ttu-id="2d986-120">1.2.840.113556.1.2.267</span><span class="sxs-lookup"><span data-stu-id="2d986-120">1.2.840.113556.1.2.267</span></span>               |
| <span data-ttu-id="2d986-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2d986-121">System-Id-Guid</span></span>    | <span data-ttu-id="2d986-122">bf967a71-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2d986-122">bf967a71-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="2d986-123">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d986-123">Syntax</span></span>            | [<span data-ttu-id="2d986-124">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="2d986-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="2d986-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="2d986-125">Implementations</span></span>

-   [<span data-ttu-id="2d986-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2d986-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2d986-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2d986-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2d986-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2d986-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2d986-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2d986-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2d986-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2d986-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2d986-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2d986-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2d986-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2d986-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2d986-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2d986-133">Windows 2000 Server</span></span>



| <span data-ttu-id="2d986-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="2d986-134">Entry</span></span> | <span data-ttu-id="2d986-135">Valor</span><span class="sxs-lookup"><span data-stu-id="2d986-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2d986-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="2d986-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2d986-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d986-137">MAPI-Id</span></span>                | <span data-ttu-id="2d986-138">0x8155</span><span class="sxs-lookup"><span data-stu-id="2d986-138">0x8155</span></span>                          |
| <span data-ttu-id="2d986-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d986-139">System-Only</span></span>            | <span data-ttu-id="2d986-140">True</span><span class="sxs-lookup"><span data-stu-id="2d986-140">True</span></span>                            |
| <span data-ttu-id="2d986-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2d986-141">Is-Single-Valued</span></span>       | <span data-ttu-id="2d986-142">True</span><span class="sxs-lookup"><span data-stu-id="2d986-142">True</span></span>                            |
| <span data-ttu-id="2d986-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="2d986-143">Is Indexed</span></span>             | <span data-ttu-id="2d986-144">Falso</span><span class="sxs-lookup"><span data-stu-id="2d986-144">False</span></span>                           |
| <span data-ttu-id="2d986-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2d986-145">In Global Catalog</span></span>      | <span data-ttu-id="2d986-146">Falso</span><span class="sxs-lookup"><span data-stu-id="2d986-146">False</span></span>                           |
| <span data-ttu-id="2d986-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2d986-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d986-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2d986-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2d986-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d986-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2d986-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d986-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2d986-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d986-151">Search-Flags</span></span>           | <span data-ttu-id="2d986-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d986-152">0x00000000</span></span>                      |
| <span data-ttu-id="2d986-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d986-153">System-Flags</span></span>           | <span data-ttu-id="2d986-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d986-154">0x00000010</span></span>                      |
| <span data-ttu-id="2d986-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2d986-155">Classes used in</span></span>        | [<span data-ttu-id="2d986-156">**Início**</span><span class="sxs-lookup"><span data-stu-id="2d986-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2d986-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2d986-157">Windows Server 2003</span></span>



| <span data-ttu-id="2d986-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="2d986-158">Entry</span></span> | <span data-ttu-id="2d986-159">Valor</span><span class="sxs-lookup"><span data-stu-id="2d986-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2d986-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="2d986-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2d986-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d986-161">MAPI-Id</span></span>                | <span data-ttu-id="2d986-162">0x8155</span><span class="sxs-lookup"><span data-stu-id="2d986-162">0x8155</span></span>                          |
| <span data-ttu-id="2d986-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d986-163">System-Only</span></span>            | <span data-ttu-id="2d986-164">True</span><span class="sxs-lookup"><span data-stu-id="2d986-164">True</span></span>                            |
| <span data-ttu-id="2d986-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2d986-165">Is-Single-Valued</span></span>       | <span data-ttu-id="2d986-166">True</span><span class="sxs-lookup"><span data-stu-id="2d986-166">True</span></span>                            |
| <span data-ttu-id="2d986-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="2d986-167">Is Indexed</span></span>             | <span data-ttu-id="2d986-168">Falso</span><span class="sxs-lookup"><span data-stu-id="2d986-168">False</span></span>                           |
| <span data-ttu-id="2d986-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2d986-169">In Global Catalog</span></span>      | <span data-ttu-id="2d986-170">Falso</span><span class="sxs-lookup"><span data-stu-id="2d986-170">False</span></span>                           |
| <span data-ttu-id="2d986-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2d986-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d986-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2d986-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2d986-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d986-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2d986-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d986-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2d986-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d986-175">Search-Flags</span></span>           | <span data-ttu-id="2d986-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d986-176">0x00000000</span></span>                      |
| <span data-ttu-id="2d986-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d986-177">System-Flags</span></span>           | <span data-ttu-id="2d986-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d986-178">0x00000010</span></span>                      |
| <span data-ttu-id="2d986-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2d986-179">Classes used in</span></span>        | [<span data-ttu-id="2d986-180">**Início**</span><span class="sxs-lookup"><span data-stu-id="2d986-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2d986-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="2d986-181">ADAM</span></span>



| <span data-ttu-id="2d986-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="2d986-182">Entry</span></span> | <span data-ttu-id="2d986-183">Valor</span><span class="sxs-lookup"><span data-stu-id="2d986-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2d986-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="2d986-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2d986-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d986-185">MAPI-Id</span></span>                | <span data-ttu-id="2d986-186">0x8155</span><span class="sxs-lookup"><span data-stu-id="2d986-186">0x8155</span></span>                          |
| <span data-ttu-id="2d986-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d986-187">System-Only</span></span>            | <span data-ttu-id="2d986-188">True</span><span class="sxs-lookup"><span data-stu-id="2d986-188">True</span></span>                            |
| <span data-ttu-id="2d986-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2d986-189">Is-Single-Valued</span></span>       | <span data-ttu-id="2d986-190">True</span><span class="sxs-lookup"><span data-stu-id="2d986-190">True</span></span>                            |
| <span data-ttu-id="2d986-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="2d986-191">Is Indexed</span></span>             | <span data-ttu-id="2d986-192">Falso</span><span class="sxs-lookup"><span data-stu-id="2d986-192">False</span></span>                           |
| <span data-ttu-id="2d986-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2d986-193">In Global Catalog</span></span>      | <span data-ttu-id="2d986-194">Falso</span><span class="sxs-lookup"><span data-stu-id="2d986-194">False</span></span>                           |
| <span data-ttu-id="2d986-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2d986-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d986-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2d986-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2d986-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d986-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2d986-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d986-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2d986-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d986-199">Search-Flags</span></span>           | <span data-ttu-id="2d986-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d986-200">0x00000000</span></span>                      |
| <span data-ttu-id="2d986-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d986-201">System-Flags</span></span>           | <span data-ttu-id="2d986-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d986-202">0x00000010</span></span>                      |
| <span data-ttu-id="2d986-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2d986-203">Classes used in</span></span>        | [<span data-ttu-id="2d986-204">**Início**</span><span class="sxs-lookup"><span data-stu-id="2d986-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2d986-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2d986-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2d986-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="2d986-206">Entry</span></span> | <span data-ttu-id="2d986-207">Valor</span><span class="sxs-lookup"><span data-stu-id="2d986-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2d986-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="2d986-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2d986-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d986-209">MAPI-Id</span></span>                | <span data-ttu-id="2d986-210">0x8155</span><span class="sxs-lookup"><span data-stu-id="2d986-210">0x8155</span></span>                          |
| <span data-ttu-id="2d986-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d986-211">System-Only</span></span>            | <span data-ttu-id="2d986-212">True</span><span class="sxs-lookup"><span data-stu-id="2d986-212">True</span></span>                            |
| <span data-ttu-id="2d986-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2d986-213">Is-Single-Valued</span></span>       | <span data-ttu-id="2d986-214">True</span><span class="sxs-lookup"><span data-stu-id="2d986-214">True</span></span>                            |
| <span data-ttu-id="2d986-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="2d986-215">Is Indexed</span></span>             | <span data-ttu-id="2d986-216">Falso</span><span class="sxs-lookup"><span data-stu-id="2d986-216">False</span></span>                           |
| <span data-ttu-id="2d986-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2d986-217">In Global Catalog</span></span>      | <span data-ttu-id="2d986-218">Falso</span><span class="sxs-lookup"><span data-stu-id="2d986-218">False</span></span>                           |
| <span data-ttu-id="2d986-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2d986-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d986-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2d986-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2d986-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d986-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2d986-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d986-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2d986-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d986-223">Search-Flags</span></span>           | <span data-ttu-id="2d986-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d986-224">0x00000000</span></span>                      |
| <span data-ttu-id="2d986-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d986-225">System-Flags</span></span>           | <span data-ttu-id="2d986-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d986-226">0x00000010</span></span>                      |
| <span data-ttu-id="2d986-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2d986-227">Classes used in</span></span>        | [<span data-ttu-id="2d986-228">**Início**</span><span class="sxs-lookup"><span data-stu-id="2d986-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2d986-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d986-229">Windows Server 2008</span></span>



| <span data-ttu-id="2d986-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="2d986-230">Entry</span></span> | <span data-ttu-id="2d986-231">Valor</span><span class="sxs-lookup"><span data-stu-id="2d986-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2d986-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="2d986-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2d986-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d986-233">MAPI-Id</span></span>                | <span data-ttu-id="2d986-234">0x8155</span><span class="sxs-lookup"><span data-stu-id="2d986-234">0x8155</span></span>                          |
| <span data-ttu-id="2d986-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d986-235">System-Only</span></span>            | <span data-ttu-id="2d986-236">True</span><span class="sxs-lookup"><span data-stu-id="2d986-236">True</span></span>                            |
| <span data-ttu-id="2d986-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2d986-237">Is-Single-Valued</span></span>       | <span data-ttu-id="2d986-238">True</span><span class="sxs-lookup"><span data-stu-id="2d986-238">True</span></span>                            |
| <span data-ttu-id="2d986-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="2d986-239">Is Indexed</span></span>             | <span data-ttu-id="2d986-240">Falso</span><span class="sxs-lookup"><span data-stu-id="2d986-240">False</span></span>                           |
| <span data-ttu-id="2d986-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2d986-241">In Global Catalog</span></span>      | <span data-ttu-id="2d986-242">Falso</span><span class="sxs-lookup"><span data-stu-id="2d986-242">False</span></span>                           |
| <span data-ttu-id="2d986-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2d986-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d986-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2d986-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2d986-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d986-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2d986-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d986-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2d986-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d986-247">Search-Flags</span></span>           | <span data-ttu-id="2d986-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d986-248">0x00000000</span></span>                      |
| <span data-ttu-id="2d986-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d986-249">System-Flags</span></span>           | <span data-ttu-id="2d986-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d986-250">0x00000010</span></span>                      |
| <span data-ttu-id="2d986-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2d986-251">Classes used in</span></span>        | [<span data-ttu-id="2d986-252">**Início**</span><span class="sxs-lookup"><span data-stu-id="2d986-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2d986-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2d986-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2d986-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="2d986-254">Entry</span></span> | <span data-ttu-id="2d986-255">Valor</span><span class="sxs-lookup"><span data-stu-id="2d986-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2d986-256">ID do link</span><span class="sxs-lookup"><span data-stu-id="2d986-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2d986-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d986-257">MAPI-Id</span></span>                | <span data-ttu-id="2d986-258">0x8155</span><span class="sxs-lookup"><span data-stu-id="2d986-258">0x8155</span></span>                          |
| <span data-ttu-id="2d986-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d986-259">System-Only</span></span>            | <span data-ttu-id="2d986-260">True</span><span class="sxs-lookup"><span data-stu-id="2d986-260">True</span></span>                            |
| <span data-ttu-id="2d986-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2d986-261">Is-Single-Valued</span></span>       | <span data-ttu-id="2d986-262">True</span><span class="sxs-lookup"><span data-stu-id="2d986-262">True</span></span>                            |
| <span data-ttu-id="2d986-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="2d986-263">Is Indexed</span></span>             | <span data-ttu-id="2d986-264">Falso</span><span class="sxs-lookup"><span data-stu-id="2d986-264">False</span></span>                           |
| <span data-ttu-id="2d986-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2d986-265">In Global Catalog</span></span>      | <span data-ttu-id="2d986-266">Falso</span><span class="sxs-lookup"><span data-stu-id="2d986-266">False</span></span>                           |
| <span data-ttu-id="2d986-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2d986-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d986-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2d986-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2d986-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d986-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2d986-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d986-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2d986-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d986-271">Search-Flags</span></span>           | <span data-ttu-id="2d986-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d986-272">0x00000000</span></span>                      |
| <span data-ttu-id="2d986-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d986-273">System-Flags</span></span>           | <span data-ttu-id="2d986-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d986-274">0x00000010</span></span>                      |
| <span data-ttu-id="2d986-275">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2d986-275">Classes used in</span></span>        | [<span data-ttu-id="2d986-276">**Início**</span><span class="sxs-lookup"><span data-stu-id="2d986-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2d986-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2d986-277">Windows Server 2012</span></span>



| <span data-ttu-id="2d986-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="2d986-278">Entry</span></span> | <span data-ttu-id="2d986-279">Valor</span><span class="sxs-lookup"><span data-stu-id="2d986-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2d986-280">ID do link</span><span class="sxs-lookup"><span data-stu-id="2d986-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2d986-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d986-281">MAPI-Id</span></span>                | <span data-ttu-id="2d986-282">0x8155</span><span class="sxs-lookup"><span data-stu-id="2d986-282">0x8155</span></span>                          |
| <span data-ttu-id="2d986-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d986-283">System-Only</span></span>            | <span data-ttu-id="2d986-284">True</span><span class="sxs-lookup"><span data-stu-id="2d986-284">True</span></span>                            |
| <span data-ttu-id="2d986-285">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2d986-285">Is-Single-Valued</span></span>       | <span data-ttu-id="2d986-286">True</span><span class="sxs-lookup"><span data-stu-id="2d986-286">True</span></span>                            |
| <span data-ttu-id="2d986-287">É indexado</span><span class="sxs-lookup"><span data-stu-id="2d986-287">Is Indexed</span></span>             | <span data-ttu-id="2d986-288">Falso</span><span class="sxs-lookup"><span data-stu-id="2d986-288">False</span></span>                           |
| <span data-ttu-id="2d986-289">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2d986-289">In Global Catalog</span></span>      | <span data-ttu-id="2d986-290">Falso</span><span class="sxs-lookup"><span data-stu-id="2d986-290">False</span></span>                           |
| <span data-ttu-id="2d986-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2d986-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d986-292">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2d986-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2d986-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d986-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2d986-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d986-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2d986-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d986-295">Search-Flags</span></span>           | <span data-ttu-id="2d986-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d986-296">0x00000000</span></span>                      |
| <span data-ttu-id="2d986-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d986-297">System-Flags</span></span>           | <span data-ttu-id="2d986-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d986-298">0x00000010</span></span>                      |
| <span data-ttu-id="2d986-299">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2d986-299">Classes used in</span></span>        | [<span data-ttu-id="2d986-300">**Início**</span><span class="sxs-lookup"><span data-stu-id="2d986-300">**Top**</span></span>](c-top.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="2d986-301">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d986-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d986-302">**USN-Last-obj-REM**</span><span class="sxs-lookup"><span data-stu-id="2d986-302">**USN-Last-Obj-Rem**</span></span>](a-usnlastobjrem.md)
</dt> </dl>

 

 





