---
title: Atributo Trust-POSIX-offset
description: O deslocamento POSIX (interface do sistema operacional portátil) para o domínio confiável.
ms.assetid: a1263f9f-1577-44b8-b7cc-317a8ecb37f1
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo Trust-POSIX-offset
- Esquema de AD do atributo trustPosixOffset
topic_type:
- apiref
api_name:
- Trust-Posix-Offset
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de8f3dca090d44ea545dcc290b04d99131d50dc7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104009840"
---
# <a name="trust-posix-offset-attribute"></a><span data-ttu-id="19830-105">Atributo Trust-POSIX-offset</span><span class="sxs-lookup"><span data-stu-id="19830-105">Trust-Posix-Offset attribute</span></span>

<span data-ttu-id="19830-106">O deslocamento POSIX (interface do sistema operacional portátil) para o domínio confiável.</span><span class="sxs-lookup"><span data-stu-id="19830-106">The Portable Operating System Interface (POSIX) offset for the trusted domain.</span></span>



| <span data-ttu-id="19830-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="19830-107">Entry</span></span> | <span data-ttu-id="19830-108">Valor</span><span class="sxs-lookup"><span data-stu-id="19830-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="19830-109">CN</span><span class="sxs-lookup"><span data-stu-id="19830-109">CN</span></span>                | <span data-ttu-id="19830-110">Trust-POSIX-offset</span><span class="sxs-lookup"><span data-stu-id="19830-110">Trust-Posix-Offset</span></span>                   |
| <span data-ttu-id="19830-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="19830-111">Ldap-Display-Name</span></span> | <span data-ttu-id="19830-112">trustPosixOffset</span><span class="sxs-lookup"><span data-stu-id="19830-112">trustPosixOffset</span></span>                     |
| <span data-ttu-id="19830-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="19830-113">Size</span></span>              | <span data-ttu-id="19830-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="19830-114">4 bytes</span></span>                              |
| <span data-ttu-id="19830-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="19830-115">Update Privilege</span></span>  | <span data-ttu-id="19830-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="19830-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="19830-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="19830-117">Update Frequency</span></span>  | <span data-ttu-id="19830-118">Quando uma nova relação de confiança é criada.</span><span class="sxs-lookup"><span data-stu-id="19830-118">When a new trust is created.</span></span>         |
| <span data-ttu-id="19830-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="19830-119">Attribute-Id</span></span>      | <span data-ttu-id="19830-120">1.2.840.113556.1.4.134</span><span class="sxs-lookup"><span data-stu-id="19830-120">1.2.840.113556.1.4.134</span></span>               |
| <span data-ttu-id="19830-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="19830-121">System-Id-Guid</span></span>    | <span data-ttu-id="19830-122">bf967a5e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="19830-122">bf967a5e-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="19830-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="19830-123">Syntax</span></span>            | [<span data-ttu-id="19830-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="19830-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="19830-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="19830-125">Implementations</span></span>

-   [<span data-ttu-id="19830-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="19830-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="19830-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="19830-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="19830-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="19830-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="19830-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="19830-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="19830-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="19830-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="19830-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="19830-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="19830-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="19830-132">Windows 2000 Server</span></span>



| <span data-ttu-id="19830-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="19830-133">Entry</span></span> | <span data-ttu-id="19830-134">Valor</span><span class="sxs-lookup"><span data-stu-id="19830-134">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="19830-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="19830-135">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="19830-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19830-136">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="19830-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="19830-137">System-Only</span></span>            | <span data-ttu-id="19830-138">Falso</span><span class="sxs-lookup"><span data-stu-id="19830-138">False</span></span>                                                |
| <span data-ttu-id="19830-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="19830-139">Is-Single-Valued</span></span>       | <span data-ttu-id="19830-140">True</span><span class="sxs-lookup"><span data-stu-id="19830-140">True</span></span>                                                 |
| <span data-ttu-id="19830-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="19830-141">Is Indexed</span></span>             | <span data-ttu-id="19830-142">Falso</span><span class="sxs-lookup"><span data-stu-id="19830-142">False</span></span>                                                |
| <span data-ttu-id="19830-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="19830-143">In Global Catalog</span></span>      | <span data-ttu-id="19830-144">Falso</span><span class="sxs-lookup"><span data-stu-id="19830-144">False</span></span>                                                |
| <span data-ttu-id="19830-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19830-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="19830-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="19830-146">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="19830-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19830-147">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="19830-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19830-148">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="19830-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19830-149">Search-Flags</span></span>           | <span data-ttu-id="19830-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19830-150">0x00000000</span></span>                                           |
| <span data-ttu-id="19830-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19830-151">System-Flags</span></span>           | <span data-ttu-id="19830-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19830-152">0x00000010</span></span>                                           |
| <span data-ttu-id="19830-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="19830-153">Classes used in</span></span>        | [<span data-ttu-id="19830-154">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="19830-154">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="19830-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="19830-155">Windows Server 2003</span></span>



| <span data-ttu-id="19830-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="19830-156">Entry</span></span> | <span data-ttu-id="19830-157">Valor</span><span class="sxs-lookup"><span data-stu-id="19830-157">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="19830-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="19830-158">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="19830-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19830-159">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="19830-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="19830-160">System-Only</span></span>            | <span data-ttu-id="19830-161">Falso</span><span class="sxs-lookup"><span data-stu-id="19830-161">False</span></span>                                                |
| <span data-ttu-id="19830-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="19830-162">Is-Single-Valued</span></span>       | <span data-ttu-id="19830-163">True</span><span class="sxs-lookup"><span data-stu-id="19830-163">True</span></span>                                                 |
| <span data-ttu-id="19830-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="19830-164">Is Indexed</span></span>             | <span data-ttu-id="19830-165">Falso</span><span class="sxs-lookup"><span data-stu-id="19830-165">False</span></span>                                                |
| <span data-ttu-id="19830-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="19830-166">In Global Catalog</span></span>      | <span data-ttu-id="19830-167">Falso</span><span class="sxs-lookup"><span data-stu-id="19830-167">False</span></span>                                                |
| <span data-ttu-id="19830-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19830-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="19830-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="19830-169">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="19830-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19830-170">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="19830-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19830-171">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="19830-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19830-172">Search-Flags</span></span>           | <span data-ttu-id="19830-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19830-173">0x00000000</span></span>                                           |
| <span data-ttu-id="19830-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19830-174">System-Flags</span></span>           | <span data-ttu-id="19830-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19830-175">0x00000010</span></span>                                           |
| <span data-ttu-id="19830-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="19830-176">Classes used in</span></span>        | [<span data-ttu-id="19830-177">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="19830-177">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="19830-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="19830-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="19830-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="19830-179">Entry</span></span> | <span data-ttu-id="19830-180">Valor</span><span class="sxs-lookup"><span data-stu-id="19830-180">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="19830-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="19830-181">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="19830-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19830-182">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="19830-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="19830-183">System-Only</span></span>            | <span data-ttu-id="19830-184">Falso</span><span class="sxs-lookup"><span data-stu-id="19830-184">False</span></span>                                                |
| <span data-ttu-id="19830-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="19830-185">Is-Single-Valued</span></span>       | <span data-ttu-id="19830-186">True</span><span class="sxs-lookup"><span data-stu-id="19830-186">True</span></span>                                                 |
| <span data-ttu-id="19830-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="19830-187">Is Indexed</span></span>             | <span data-ttu-id="19830-188">Falso</span><span class="sxs-lookup"><span data-stu-id="19830-188">False</span></span>                                                |
| <span data-ttu-id="19830-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="19830-189">In Global Catalog</span></span>      | <span data-ttu-id="19830-190">Falso</span><span class="sxs-lookup"><span data-stu-id="19830-190">False</span></span>                                                |
| <span data-ttu-id="19830-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19830-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="19830-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="19830-192">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="19830-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19830-193">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="19830-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19830-194">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="19830-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19830-195">Search-Flags</span></span>           | <span data-ttu-id="19830-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19830-196">0x00000000</span></span>                                           |
| <span data-ttu-id="19830-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19830-197">System-Flags</span></span>           | <span data-ttu-id="19830-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19830-198">0x00000010</span></span>                                           |
| <span data-ttu-id="19830-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="19830-199">Classes used in</span></span>        | [<span data-ttu-id="19830-200">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="19830-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="19830-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19830-201">Windows Server 2008</span></span>



| <span data-ttu-id="19830-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="19830-202">Entry</span></span> | <span data-ttu-id="19830-203">Valor</span><span class="sxs-lookup"><span data-stu-id="19830-203">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="19830-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="19830-204">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="19830-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19830-205">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="19830-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="19830-206">System-Only</span></span>            | <span data-ttu-id="19830-207">Falso</span><span class="sxs-lookup"><span data-stu-id="19830-207">False</span></span>                                                |
| <span data-ttu-id="19830-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="19830-208">Is-Single-Valued</span></span>       | <span data-ttu-id="19830-209">True</span><span class="sxs-lookup"><span data-stu-id="19830-209">True</span></span>                                                 |
| <span data-ttu-id="19830-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="19830-210">Is Indexed</span></span>             | <span data-ttu-id="19830-211">Falso</span><span class="sxs-lookup"><span data-stu-id="19830-211">False</span></span>                                                |
| <span data-ttu-id="19830-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="19830-212">In Global Catalog</span></span>      | <span data-ttu-id="19830-213">Falso</span><span class="sxs-lookup"><span data-stu-id="19830-213">False</span></span>                                                |
| <span data-ttu-id="19830-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19830-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="19830-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="19830-215">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="19830-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19830-216">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="19830-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19830-217">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="19830-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19830-218">Search-Flags</span></span>           | <span data-ttu-id="19830-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19830-219">0x00000000</span></span>                                           |
| <span data-ttu-id="19830-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19830-220">System-Flags</span></span>           | <span data-ttu-id="19830-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19830-221">0x00000010</span></span>                                           |
| <span data-ttu-id="19830-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="19830-222">Classes used in</span></span>        | [<span data-ttu-id="19830-223">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="19830-223">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="19830-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="19830-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="19830-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="19830-225">Entry</span></span> | <span data-ttu-id="19830-226">Valor</span><span class="sxs-lookup"><span data-stu-id="19830-226">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="19830-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="19830-227">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="19830-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19830-228">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="19830-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="19830-229">System-Only</span></span>            | <span data-ttu-id="19830-230">Falso</span><span class="sxs-lookup"><span data-stu-id="19830-230">False</span></span>                                                |
| <span data-ttu-id="19830-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="19830-231">Is-Single-Valued</span></span>       | <span data-ttu-id="19830-232">True</span><span class="sxs-lookup"><span data-stu-id="19830-232">True</span></span>                                                 |
| <span data-ttu-id="19830-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="19830-233">Is Indexed</span></span>             | <span data-ttu-id="19830-234">Falso</span><span class="sxs-lookup"><span data-stu-id="19830-234">False</span></span>                                                |
| <span data-ttu-id="19830-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="19830-235">In Global Catalog</span></span>      | <span data-ttu-id="19830-236">Falso</span><span class="sxs-lookup"><span data-stu-id="19830-236">False</span></span>                                                |
| <span data-ttu-id="19830-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19830-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="19830-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="19830-238">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="19830-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19830-239">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="19830-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19830-240">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="19830-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19830-241">Search-Flags</span></span>           | <span data-ttu-id="19830-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19830-242">0x00000000</span></span>                                           |
| <span data-ttu-id="19830-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19830-243">System-Flags</span></span>           | <span data-ttu-id="19830-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19830-244">0x00000010</span></span>                                           |
| <span data-ttu-id="19830-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="19830-245">Classes used in</span></span>        | [<span data-ttu-id="19830-246">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="19830-246">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="19830-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="19830-247">Windows Server 2012</span></span>



| <span data-ttu-id="19830-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="19830-248">Entry</span></span> | <span data-ttu-id="19830-249">Valor</span><span class="sxs-lookup"><span data-stu-id="19830-249">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="19830-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="19830-250">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="19830-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19830-251">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="19830-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="19830-252">System-Only</span></span>            | <span data-ttu-id="19830-253">Falso</span><span class="sxs-lookup"><span data-stu-id="19830-253">False</span></span>                                                |
| <span data-ttu-id="19830-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="19830-254">Is-Single-Valued</span></span>       | <span data-ttu-id="19830-255">True</span><span class="sxs-lookup"><span data-stu-id="19830-255">True</span></span>                                                 |
| <span data-ttu-id="19830-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="19830-256">Is Indexed</span></span>             | <span data-ttu-id="19830-257">Falso</span><span class="sxs-lookup"><span data-stu-id="19830-257">False</span></span>                                                |
| <span data-ttu-id="19830-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="19830-258">In Global Catalog</span></span>      | <span data-ttu-id="19830-259">Falso</span><span class="sxs-lookup"><span data-stu-id="19830-259">False</span></span>                                                |
| <span data-ttu-id="19830-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19830-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="19830-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="19830-261">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="19830-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19830-262">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="19830-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19830-263">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="19830-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19830-264">Search-Flags</span></span>           | <span data-ttu-id="19830-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="19830-265">0x00000000</span></span>                                           |
| <span data-ttu-id="19830-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19830-266">System-Flags</span></span>           | <span data-ttu-id="19830-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19830-267">0x00000010</span></span>                                           |
| <span data-ttu-id="19830-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="19830-268">Classes used in</span></span>        | [<span data-ttu-id="19830-269">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="19830-269">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





