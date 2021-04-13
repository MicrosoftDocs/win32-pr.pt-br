---
title: Atributo USN-Last-obj-REM
description: Contém o USN (número de sequência de atualização) do último objeto que não é do sistema que foi removido de um servidor.
ms.assetid: 34718bea-fa19-4084-b97f-d72a1681c3f4
ms.tgt_platform: multiple
keywords:
- USN-Last-obj-REM atributo AD Schema
- Esquema de AD do atributo uSNLastObjRem
topic_type:
- apiref
api_name:
- USN-Last-Obj-Rem
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9836bd93ca065fdfa53b0246a5bab0142e84ced6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104500023"
---
# <a name="usn-last-obj-rem-attribute"></a><span data-ttu-id="56cc2-105">Atributo USN-Last-obj-REM</span><span class="sxs-lookup"><span data-stu-id="56cc2-105">USN-Last-Obj-Rem attribute</span></span>

<span data-ttu-id="56cc2-106">Contém o USN (número de sequência de atualização) do último objeto que não é do sistema que foi removido de um servidor.</span><span class="sxs-lookup"><span data-stu-id="56cc2-106">Contains the update sequence number (USN) for the last non-system object that was removed from a server.</span></span>



| <span data-ttu-id="56cc2-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="56cc2-107">Entry</span></span> | <span data-ttu-id="56cc2-108">Valor</span><span class="sxs-lookup"><span data-stu-id="56cc2-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="56cc2-109">CN</span><span class="sxs-lookup"><span data-stu-id="56cc2-109">CN</span></span>                | <span data-ttu-id="56cc2-110">USN-Last-obj-REM</span><span class="sxs-lookup"><span data-stu-id="56cc2-110">USN-Last-Obj-Rem</span></span>                     |
| <span data-ttu-id="56cc2-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="56cc2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="56cc2-112">uSNLastObjRem</span><span class="sxs-lookup"><span data-stu-id="56cc2-112">uSNLastObjRem</span></span>                        |
| <span data-ttu-id="56cc2-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="56cc2-113">Size</span></span>              | <span data-ttu-id="56cc2-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="56cc2-114">8 bytes</span></span>                              |
| <span data-ttu-id="56cc2-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="56cc2-115">Update Privilege</span></span>  | <span data-ttu-id="56cc2-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="56cc2-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="56cc2-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="56cc2-117">Update Frequency</span></span>  | <span data-ttu-id="56cc2-118">Sempre que um objeto de diretório é alterado.</span><span class="sxs-lookup"><span data-stu-id="56cc2-118">Whenever a directory object changes.</span></span> |
| <span data-ttu-id="56cc2-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="56cc2-119">Attribute-Id</span></span>      | <span data-ttu-id="56cc2-120">1.2.840.113556.1.2.121</span><span class="sxs-lookup"><span data-stu-id="56cc2-120">1.2.840.113556.1.2.121</span></span>               |
| <span data-ttu-id="56cc2-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="56cc2-121">System-Id-Guid</span></span>    | <span data-ttu-id="56cc2-122">bf967a73-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="56cc2-122">bf967a73-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="56cc2-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="56cc2-123">Syntax</span></span>            | [<span data-ttu-id="56cc2-124">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="56cc2-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="56cc2-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="56cc2-125">Implementations</span></span>

-   [<span data-ttu-id="56cc2-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="56cc2-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="56cc2-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="56cc2-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="56cc2-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="56cc2-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="56cc2-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="56cc2-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="56cc2-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="56cc2-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="56cc2-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="56cc2-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="56cc2-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="56cc2-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="56cc2-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="56cc2-133">Windows 2000 Server</span></span>



| <span data-ttu-id="56cc2-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="56cc2-134">Entry</span></span> | <span data-ttu-id="56cc2-135">Valor</span><span class="sxs-lookup"><span data-stu-id="56cc2-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="56cc2-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="56cc2-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="56cc2-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56cc2-137">MAPI-Id</span></span>                | <span data-ttu-id="56cc2-138">0x8156</span><span class="sxs-lookup"><span data-stu-id="56cc2-138">0x8156</span></span>                          |
| <span data-ttu-id="56cc2-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="56cc2-139">System-Only</span></span>            | <span data-ttu-id="56cc2-140">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-140">True</span></span>                            |
| <span data-ttu-id="56cc2-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="56cc2-141">Is-Single-Valued</span></span>       | <span data-ttu-id="56cc2-142">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-142">True</span></span>                            |
| <span data-ttu-id="56cc2-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="56cc2-143">Is Indexed</span></span>             | <span data-ttu-id="56cc2-144">Falso</span><span class="sxs-lookup"><span data-stu-id="56cc2-144">False</span></span>                           |
| <span data-ttu-id="56cc2-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="56cc2-145">In Global Catalog</span></span>      | <span data-ttu-id="56cc2-146">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-146">True</span></span>                            |
| <span data-ttu-id="56cc2-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56cc2-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="56cc2-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="56cc2-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="56cc2-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56cc2-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="56cc2-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56cc2-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="56cc2-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56cc2-151">Search-Flags</span></span>           | <span data-ttu-id="56cc2-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56cc2-152">0x00000000</span></span>                      |
| <span data-ttu-id="56cc2-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56cc2-153">System-Flags</span></span>           | <span data-ttu-id="56cc2-154">0x00000013</span><span class="sxs-lookup"><span data-stu-id="56cc2-154">0x00000013</span></span>                      |
| <span data-ttu-id="56cc2-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="56cc2-155">Classes used in</span></span>        | [<span data-ttu-id="56cc2-156">**Início**</span><span class="sxs-lookup"><span data-stu-id="56cc2-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="56cc2-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="56cc2-157">Windows Server 2003</span></span>



| <span data-ttu-id="56cc2-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="56cc2-158">Entry</span></span> | <span data-ttu-id="56cc2-159">Valor</span><span class="sxs-lookup"><span data-stu-id="56cc2-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="56cc2-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="56cc2-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="56cc2-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56cc2-161">MAPI-Id</span></span>                | <span data-ttu-id="56cc2-162">0x8156</span><span class="sxs-lookup"><span data-stu-id="56cc2-162">0x8156</span></span>                          |
| <span data-ttu-id="56cc2-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="56cc2-163">System-Only</span></span>            | <span data-ttu-id="56cc2-164">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-164">True</span></span>                            |
| <span data-ttu-id="56cc2-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="56cc2-165">Is-Single-Valued</span></span>       | <span data-ttu-id="56cc2-166">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-166">True</span></span>                            |
| <span data-ttu-id="56cc2-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="56cc2-167">Is Indexed</span></span>             | <span data-ttu-id="56cc2-168">Falso</span><span class="sxs-lookup"><span data-stu-id="56cc2-168">False</span></span>                           |
| <span data-ttu-id="56cc2-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="56cc2-169">In Global Catalog</span></span>      | <span data-ttu-id="56cc2-170">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-170">True</span></span>                            |
| <span data-ttu-id="56cc2-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56cc2-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="56cc2-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="56cc2-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="56cc2-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56cc2-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="56cc2-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56cc2-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="56cc2-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56cc2-175">Search-Flags</span></span>           | <span data-ttu-id="56cc2-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56cc2-176">0x00000000</span></span>                      |
| <span data-ttu-id="56cc2-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56cc2-177">System-Flags</span></span>           | <span data-ttu-id="56cc2-178">0x00000013</span><span class="sxs-lookup"><span data-stu-id="56cc2-178">0x00000013</span></span>                      |
| <span data-ttu-id="56cc2-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="56cc2-179">Classes used in</span></span>        | [<span data-ttu-id="56cc2-180">**Início**</span><span class="sxs-lookup"><span data-stu-id="56cc2-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="56cc2-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="56cc2-181">ADAM</span></span>



| <span data-ttu-id="56cc2-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="56cc2-182">Entry</span></span> | <span data-ttu-id="56cc2-183">Valor</span><span class="sxs-lookup"><span data-stu-id="56cc2-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="56cc2-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="56cc2-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="56cc2-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56cc2-185">MAPI-Id</span></span>                | <span data-ttu-id="56cc2-186">0x8156</span><span class="sxs-lookup"><span data-stu-id="56cc2-186">0x8156</span></span>                          |
| <span data-ttu-id="56cc2-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="56cc2-187">System-Only</span></span>            | <span data-ttu-id="56cc2-188">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-188">True</span></span>                            |
| <span data-ttu-id="56cc2-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="56cc2-189">Is-Single-Valued</span></span>       | <span data-ttu-id="56cc2-190">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-190">True</span></span>                            |
| <span data-ttu-id="56cc2-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="56cc2-191">Is Indexed</span></span>             | <span data-ttu-id="56cc2-192">Falso</span><span class="sxs-lookup"><span data-stu-id="56cc2-192">False</span></span>                           |
| <span data-ttu-id="56cc2-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="56cc2-193">In Global Catalog</span></span>      | <span data-ttu-id="56cc2-194">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-194">True</span></span>                            |
| <span data-ttu-id="56cc2-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56cc2-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="56cc2-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="56cc2-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="56cc2-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56cc2-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="56cc2-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56cc2-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="56cc2-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56cc2-199">Search-Flags</span></span>           | <span data-ttu-id="56cc2-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56cc2-200">0x00000000</span></span>                      |
| <span data-ttu-id="56cc2-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56cc2-201">System-Flags</span></span>           | <span data-ttu-id="56cc2-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="56cc2-202">0x00000013</span></span>                      |
| <span data-ttu-id="56cc2-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="56cc2-203">Classes used in</span></span>        | [<span data-ttu-id="56cc2-204">**Início**</span><span class="sxs-lookup"><span data-stu-id="56cc2-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="56cc2-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="56cc2-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="56cc2-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="56cc2-206">Entry</span></span> | <span data-ttu-id="56cc2-207">Valor</span><span class="sxs-lookup"><span data-stu-id="56cc2-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="56cc2-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="56cc2-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="56cc2-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56cc2-209">MAPI-Id</span></span>                | <span data-ttu-id="56cc2-210">0x8156</span><span class="sxs-lookup"><span data-stu-id="56cc2-210">0x8156</span></span>                          |
| <span data-ttu-id="56cc2-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="56cc2-211">System-Only</span></span>            | <span data-ttu-id="56cc2-212">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-212">True</span></span>                            |
| <span data-ttu-id="56cc2-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="56cc2-213">Is-Single-Valued</span></span>       | <span data-ttu-id="56cc2-214">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-214">True</span></span>                            |
| <span data-ttu-id="56cc2-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="56cc2-215">Is Indexed</span></span>             | <span data-ttu-id="56cc2-216">Falso</span><span class="sxs-lookup"><span data-stu-id="56cc2-216">False</span></span>                           |
| <span data-ttu-id="56cc2-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="56cc2-217">In Global Catalog</span></span>      | <span data-ttu-id="56cc2-218">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-218">True</span></span>                            |
| <span data-ttu-id="56cc2-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56cc2-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="56cc2-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="56cc2-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="56cc2-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56cc2-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="56cc2-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56cc2-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="56cc2-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56cc2-223">Search-Flags</span></span>           | <span data-ttu-id="56cc2-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56cc2-224">0x00000000</span></span>                      |
| <span data-ttu-id="56cc2-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56cc2-225">System-Flags</span></span>           | <span data-ttu-id="56cc2-226">0x00000013</span><span class="sxs-lookup"><span data-stu-id="56cc2-226">0x00000013</span></span>                      |
| <span data-ttu-id="56cc2-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="56cc2-227">Classes used in</span></span>        | [<span data-ttu-id="56cc2-228">**Início**</span><span class="sxs-lookup"><span data-stu-id="56cc2-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="56cc2-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56cc2-229">Windows Server 2008</span></span>



| <span data-ttu-id="56cc2-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="56cc2-230">Entry</span></span> | <span data-ttu-id="56cc2-231">Valor</span><span class="sxs-lookup"><span data-stu-id="56cc2-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="56cc2-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="56cc2-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="56cc2-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56cc2-233">MAPI-Id</span></span>                | <span data-ttu-id="56cc2-234">0x8156</span><span class="sxs-lookup"><span data-stu-id="56cc2-234">0x8156</span></span>                          |
| <span data-ttu-id="56cc2-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="56cc2-235">System-Only</span></span>            | <span data-ttu-id="56cc2-236">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-236">True</span></span>                            |
| <span data-ttu-id="56cc2-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="56cc2-237">Is-Single-Valued</span></span>       | <span data-ttu-id="56cc2-238">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-238">True</span></span>                            |
| <span data-ttu-id="56cc2-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="56cc2-239">Is Indexed</span></span>             | <span data-ttu-id="56cc2-240">Falso</span><span class="sxs-lookup"><span data-stu-id="56cc2-240">False</span></span>                           |
| <span data-ttu-id="56cc2-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="56cc2-241">In Global Catalog</span></span>      | <span data-ttu-id="56cc2-242">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-242">True</span></span>                            |
| <span data-ttu-id="56cc2-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56cc2-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="56cc2-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="56cc2-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="56cc2-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56cc2-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="56cc2-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56cc2-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="56cc2-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56cc2-247">Search-Flags</span></span>           | <span data-ttu-id="56cc2-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56cc2-248">0x00000000</span></span>                      |
| <span data-ttu-id="56cc2-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56cc2-249">System-Flags</span></span>           | <span data-ttu-id="56cc2-250">0x00000013</span><span class="sxs-lookup"><span data-stu-id="56cc2-250">0x00000013</span></span>                      |
| <span data-ttu-id="56cc2-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="56cc2-251">Classes used in</span></span>        | [<span data-ttu-id="56cc2-252">**Início**</span><span class="sxs-lookup"><span data-stu-id="56cc2-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="56cc2-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="56cc2-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="56cc2-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="56cc2-254">Entry</span></span> | <span data-ttu-id="56cc2-255">Valor</span><span class="sxs-lookup"><span data-stu-id="56cc2-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="56cc2-256">ID do link</span><span class="sxs-lookup"><span data-stu-id="56cc2-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="56cc2-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56cc2-257">MAPI-Id</span></span>                | <span data-ttu-id="56cc2-258">0x8156</span><span class="sxs-lookup"><span data-stu-id="56cc2-258">0x8156</span></span>                          |
| <span data-ttu-id="56cc2-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="56cc2-259">System-Only</span></span>            | <span data-ttu-id="56cc2-260">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-260">True</span></span>                            |
| <span data-ttu-id="56cc2-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="56cc2-261">Is-Single-Valued</span></span>       | <span data-ttu-id="56cc2-262">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-262">True</span></span>                            |
| <span data-ttu-id="56cc2-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="56cc2-263">Is Indexed</span></span>             | <span data-ttu-id="56cc2-264">Falso</span><span class="sxs-lookup"><span data-stu-id="56cc2-264">False</span></span>                           |
| <span data-ttu-id="56cc2-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="56cc2-265">In Global Catalog</span></span>      | <span data-ttu-id="56cc2-266">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-266">True</span></span>                            |
| <span data-ttu-id="56cc2-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56cc2-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="56cc2-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="56cc2-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="56cc2-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56cc2-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="56cc2-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56cc2-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="56cc2-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56cc2-271">Search-Flags</span></span>           | <span data-ttu-id="56cc2-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56cc2-272">0x00000000</span></span>                      |
| <span data-ttu-id="56cc2-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56cc2-273">System-Flags</span></span>           | <span data-ttu-id="56cc2-274">0x00000013</span><span class="sxs-lookup"><span data-stu-id="56cc2-274">0x00000013</span></span>                      |
| <span data-ttu-id="56cc2-275">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="56cc2-275">Classes used in</span></span>        | [<span data-ttu-id="56cc2-276">**Início**</span><span class="sxs-lookup"><span data-stu-id="56cc2-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="56cc2-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="56cc2-277">Windows Server 2012</span></span>



| <span data-ttu-id="56cc2-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="56cc2-278">Entry</span></span> | <span data-ttu-id="56cc2-279">Valor</span><span class="sxs-lookup"><span data-stu-id="56cc2-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="56cc2-280">ID do link</span><span class="sxs-lookup"><span data-stu-id="56cc2-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="56cc2-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56cc2-281">MAPI-Id</span></span>                | <span data-ttu-id="56cc2-282">0x8156</span><span class="sxs-lookup"><span data-stu-id="56cc2-282">0x8156</span></span>                          |
| <span data-ttu-id="56cc2-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="56cc2-283">System-Only</span></span>            | <span data-ttu-id="56cc2-284">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-284">True</span></span>                            |
| <span data-ttu-id="56cc2-285">É de valor único</span><span class="sxs-lookup"><span data-stu-id="56cc2-285">Is-Single-Valued</span></span>       | <span data-ttu-id="56cc2-286">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-286">True</span></span>                            |
| <span data-ttu-id="56cc2-287">É indexado</span><span class="sxs-lookup"><span data-stu-id="56cc2-287">Is Indexed</span></span>             | <span data-ttu-id="56cc2-288">Falso</span><span class="sxs-lookup"><span data-stu-id="56cc2-288">False</span></span>                           |
| <span data-ttu-id="56cc2-289">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="56cc2-289">In Global Catalog</span></span>      | <span data-ttu-id="56cc2-290">True</span><span class="sxs-lookup"><span data-stu-id="56cc2-290">True</span></span>                            |
| <span data-ttu-id="56cc2-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56cc2-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="56cc2-292">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="56cc2-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="56cc2-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56cc2-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="56cc2-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56cc2-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="56cc2-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56cc2-295">Search-Flags</span></span>           | <span data-ttu-id="56cc2-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56cc2-296">0x00000000</span></span>                      |
| <span data-ttu-id="56cc2-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56cc2-297">System-Flags</span></span>           | <span data-ttu-id="56cc2-298">0x00000013</span><span class="sxs-lookup"><span data-stu-id="56cc2-298">0x00000013</span></span>                      |
| <span data-ttu-id="56cc2-299">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="56cc2-299">Classes used in</span></span>        | [<span data-ttu-id="56cc2-300">**Início**</span><span class="sxs-lookup"><span data-stu-id="56cc2-300">**Top**</span></span>](c-top.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="56cc2-301">Confira também</span><span class="sxs-lookup"><span data-stu-id="56cc2-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56cc2-302">**USN-DSA-Last-obj-removido**</span><span class="sxs-lookup"><span data-stu-id="56cc2-302">**USN-DSA-Last-Obj-Removed**</span></span>](a-usndsalastobjremoved.md)
</dt> </dl>

 

 





